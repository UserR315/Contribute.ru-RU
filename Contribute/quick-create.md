---
title: Краткое руководство. Настройка и получение секрета из Azure Key Vault | Документация Майкрософт
description: Краткое руководство. Настройка и получение секрета из Azure Key Vault
services: key-vault
author: syntaxc4
manager: erifkin
ms.date: 07/24/2018
ms.author: cfowler
zone_pivot_groups: keyvault-languages
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 497631fe46ac4e2c9c495a609547753a84d662bf
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805753"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a>Краткое руководство. Настройка и получение секрета из Azure Key Vault

Из этого краткого руководства вы узнаете, как сохранить секрет в службе Key Vault и как его получать с помощью веб-приложения. Чтобы была возможность просмотреть значение секрета, приложение должно работать в Azure. В этом кратком руководстве используются приложение Node.js и управляемые удостоверения служб (MSI).

> [!div class="checklist"]
> * Создание хранилища Key Vault.
> * Сохранение секрета в Key Vault.
> * Получение секрета из хранилища Key Vault.
> * Создание веб-приложения Azure.
> * [Настройка управляемых удостоверений служб](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).
> * Предоставление веб-приложению необходимых разрешений на чтение данных из хранилища Key Vault.

Прежде чем продолжить, убедитесь, что вы ознакомились с [основными понятиями](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).

> [!NOTE]
> Чтобы понять, почему в этом руководстве приводятся именно такие рекомендации, необходимо разобраться в нескольких основных понятиях. Хранилище Key Vault — это центральный репозиторий для хранения секретов программным способом. Но чтобы воспользоваться возможностями хранилища Key Vault, приложения или пользователи должны сначала пройти в нем проверку подлинности, т. е. предоставить секрет. В соответствии с рекомендациями по безопасности первый секрет должен периодически меняться. Однако благодаря [управляемому удостоверению службы](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) приложения, работающие в Azure, получают удостоверение, которым автоматически управляет служба Azure. Это помогает устранить **проблему введения секрета**, чтобы пользователи и приложения могли следовать рекомендациям и не беспокоиться об изменении первого секрета.

## <a name="prerequisites"></a>Предварительные требования

::: zone pivot="nodejs"
* [Node.js](https://nodejs.org/en/)
::: zone-end
::: zone pivot="dotnet"
* [Visual Studio 2017 начиная с версии 15.7.3](https://www.microsoft.com/net/download/windows) со следующими рабочими нагрузками:
  * ASP.NET и веб-разработка;
  * кроссплатформенная разработка .NET Core.
* [Пакет SDK для .NET Core 2.1 или более поздней версии](https://www.microsoft.com/net/download/windows).
::: zone-end
* Git ([скачать](https://git-scm.com/downloads)).
* Подписка Azure. Если у вас еще нет подписки Azure, [создайте бесплатную учетную запись Azure](https://azure.microsoft.com/free/?WT.mc_id=A261C142F), прежде чем начинать работу.
* [Интерфейс командной строки Azure](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) начиная с версии 2.0.4. Доступен для Windows, Mac и Linux.

## <a name="login-to-azure"></a>Вход в Azure

Чтобы войти в Azure с помощью CLI, выполните следующую команду:

```azurecli
az login
```

## <a name="create-resource-group"></a>Создание группы ресурсов

Создайте группу ресурсов с помощью команды [az group create](/cli/azure/group#az-group-create). Группа ресурсов Azure — это логический контейнер, в котором происходит развертывание ресурсов Azure и управление ими.

Выберите имя для группы ресурсов и укажите его вместо заполнителя.
В следующем примере создается группа ресурсов с именем *<YourResourceGroupName>* в расположении *eastus*.

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

Созданная группа ресурсов будет использоваться далее в этом руководстве.

## <a name="create-an-azure-key-vault"></a>Создание хранилища Azure Key Vault

Теперь создайте хранилище Key Vault в группе ресурсов, созданной на предыдущем этапе. Несмотря на то что в этом руководстве для хранилища Key Vault используется имя ContosoKeyVault, вам необходимо использовать уникальное имя. Введите следующие сведения:

* Имя хранилища. **Здесь нужно выбрать имя для хранилища Key Vault**.
* Имя группы ресурсов. **Здесь нужно выбрать имя для группы ресурсов**.
* Расположение. **Восточная часть США**.

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

На этом этапе любые операции в новом хранилище может выполнять только ваша учетная запись Azure.

## <a name="add-a-secret-to-key-vault"></a>Добавление секрета в хранилище ключей

Теперь мы добавим секрет, чтобы продемонстрировать, как это работает. Вы можете хранить здесь строки подключения SQL и прочие сведения, которые должны храниться в безопасности, но быть доступными для приложения. В этом руководстве мы сохраним в хранилище пароль с именем **AppSecret** и значением **MySecret**.

Введите указанные ниже команды, чтобы создать в хранилище Key Vault секрет с именем **AppSecret** и значением **MySecret**.

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

Чтобы просмотреть содержащееся в секрете значение в виде обычного текста, выполните такую команду:

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

Эта команда возвращает значение секрета, включая URI. Выполнив эти действия, вы сохраните в Azure Key Vault секрет со значением URI. Запишите эти сведения. Они потребуются вам на следующих этапах.

## <a name="clone-the-repo"></a>Клонирование репозитория

Чтобы создать локальную копию для изменения источника, клонируйте репозиторий, выполнив следующую команду:

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

::: zone pivot="nodejs"

## <a name="install-dependencies"></a>Установка зависимостей

На этом этапе мы установим зависимости. Выполните следующие команды:

    cd key-vault-node-quickstart
    npm install

В этом проекте используются два модуля узла:

* [ms-rest-azure](https://www.npmjs.com/package/ms-rest-azure); 
* [azure-keyvault](https://www.npmjs.com/package/azure-keyvault).

## <a name="publish-the-web-application-to-azure"></a>Публикация веб-приложения в Azure

Ниже приведены несколько шагов, которые нужно выполнить для публикации приложения в Azure.

* Первый шаг — создание плана [Службы приложений Azure](https://azure.microsoft.com/services/app-service/). В этом плане можно хранить несколько веб-приложений.

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* Затем нам нужно создать веб-приложение. В примере ниже замените <app_name> глобальным уникальным именем приложения (допустимые символы: a-z, 0-9 и -). В качестве среды выполнения выбрано NODE|6.9. Список всех поддерживаемых сред выполнения можно получить с помощью команды `az webapp list-runtimes`.

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    Когда веб-приложение будет создано, в Azure CLI отобразится примерно следующее:

    ```json
    {
      "availabilityState": "Normal",
      "clientAffinityEnabled": true,
      "clientCertEnabled": false,
      "cloningInfo": null,
      "containerSize": 0,
      "dailyMemoryTimeQuota": 0,
      "defaultHostName": "<app_name>.azurewebsites.net",
      "enabled": true,
      "deploymentLocalGitUrl": "https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git"
      < JSON data removed for brevity. >
    }
    ```
    Перейдите к только что созданному веб-приложению. Вы увидите действующее веб-приложение. Замените <app_name> уникальным именем приложения.

    ```text
    http://<app name>.azurewebsites.net
    ```
    Приведенная выше команда также создает приложение с поддержкой Git, которое позволяет выполнять развертывание в Azure из локального репозитория Git. 
    Для локального репозитория Git настроен URL-адрес https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git.

* Создайте пользователя развертывания. После завершения предыдущей команды можно добавить удаленную службу приложений Azure в локальный репозиторий Git. Замените <url> URL-адресом удаленного репозитория Git, который был получен при включении использования репозитория Git для приложения.

    ```bash
    git remote add azure <url>
    ```
    
::: zone-end

::: zone pivot="dotnet"
## <a name="open-and-edit-the-solution"></a>Открытие и изменение решения

Измените файл program.cs, чтобы запустить образец со своим именем хранилища ключей.

1. Перейдите в папку key-vault-dotnet-core-quickstart.
2. Откройте в Visual Studio 2017 файл key-vault-dotnet-core-quickstart.sln.
3. Откройте файл Program.cs и вместо заполнителя *YourKeyVaultName* укажите имя вашего хранилища ключей, которое вы создали ранее.

В этом решении используются библиотеки NuGet [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) и [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault).

## <a name="run-the-app"></a>Запуск приложения

В главном меню Visual Studio 2017 выберите **Отладка** > **Запуск без отладки**. Когда откроется браузер, перейдите на страницу **О программе**. Вы увидите значение **AppSecret**.

## <a name="publish-the-web-application-to-azure"></a>Публикация веб-приложения в Azure

Опубликуйте это приложение в Azure, чтобы увидеть, как оно работает в реальной среде, а также убедиться, что вы можете получить значение секрета.

1. В Visual Studio выберите проект **key-vault-dotnet-core-quickstart**.
2. Выберите **Опубликовать** > **Запуск**.
3. Создайте новую **службу приложений**, а затем выберите **Опубликовать**.
4. Измените имя приложения на **keyvaultdotnetcorequickstart**.
5. Щелкните **Создать**.

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]
::: zone-end

## <a name="enable-managed-service-identities"></a>Настройка управляемых удостоверений служб

Azure Key Vault позволяет безопасно хранить учетные данные, а также другие ключи и секреты, но для их получения код должен пройти проверку подлинности в Azure Key Vault. Управляемое удостоверение службы упрощает решение этой задачи, предоставляя службам Azure автоматически управляемое удостоверение из Azure Active Directory (Azure AD). Вы можете использовать это удостоверение для прохождения проверки подлинности в любой службе, которая поддерживает аутентификацию Azure AD, в том числе в Key Vault, не храня в коде никакие учетные данные.

1. Вернитесь в окно Azure CLI.
2. Выполните команду назначения удостоверения, чтобы создать удостоверение для этого приложения.

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
>Выполнение этой команды равноценно выбору значения **Вкл.** для параметра **Управляемое удостоверение службы** в свойствах веб-приложения на портале.

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a>Назначение разрешений приложению для чтения секретов из хранилища Key Vault

Запишите выходные данные при публикации приложения в Azure. Они должны быть представлены в таком формате:

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

Затем, используя имя своего хранилища ключей и значение **PrincipalId**, выполните следующую команду:

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

::: zone pivot="nodejs"
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a>Развертывание приложения Node.js в Azure и получение значения секрета

Теперь, когда все готово, выполните приведенную ниже команду, чтобы развернуть приложение в Azure.

```bash
git push azure master
```

После этого на странице https://<app_name>.azurewebsites.net вы сможете увидеть значение секрета.
Убедитесь, что вы заменили имя <YourKeyVaultName> именем своего хранилища

::: zone-end

::: zone pivot="dotnet"
Теперь при запуске приложения должно отображаться полученное значение секрета.
::: zone-end

## <a name="next-steps"></a>Дальнейшие действия

::: zone pivot="nodejs"
* [Домашняя страница Azure Key Vault](https://azure.microsoft.com/services/key-vault/)
* [Документация Azure Key Vault](https://docs.microsoft.com/azure/key-vault/)
* [Пакет SDK Azure для Node.js](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* [Справочник по REST API Azure](https://docs.microsoft.com/rest/api/keyvault/)
::: zone-end

::: zone pivot="dotnet"
* [Домашняя страница Azure Key Vault](https://azure.microsoft.com/services/key-vault/)
* [Документация Azure Key Vault](https://docs.microsoft.com/azure/key-vault/)
* [Пакет SDK Azure для .NET](https://github.com/Azure/azure-sdk-for-net)
* [Справочник по REST API Azure](https://docs.microsoft.com/rest/api/keyvault/)
::: zone-end
