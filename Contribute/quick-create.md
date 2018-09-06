---
title: Краткое руководство. Настройка и получение секрета из Azure Key Vault | Документация Майкрософт
description: Краткое руководство. Настройка и получение секрета из Azure Key Vault
services: key-vault
author: syntaxc4
manager: erifkin
ms.date: 07/24/2018
ms.author: cfowler
zone_pivot_groups: keyvault-languages, keyvault-platforms
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 8b758274203748bb6e04c03dec5de38fb77947b4
ms.sourcegitcommit: b0105f322f91bb4dbde47f6da35b3c12271d5b03
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/29/2018
ms.locfileid: "43239510"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a><span data-ttu-id="fda10-103">Краткое руководство. Настройка и получение секрета из Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="fda10-103">Quickstart: Set and retrieve a secret from Azure Key Vault</span></span>

<span data-ttu-id="fda10-104">Из этого краткого руководства вы узнаете, как сохранить секрет в службе Key Vault и как его получать с помощью веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="fda10-104">This quickstart shows you how to store a secret in Key Vault and how to retrieve it using a Web app.</span></span> <span data-ttu-id="fda10-105">Чтобы была возможность просмотреть значение секрета, приложение должно работать в Azure.</span><span class="sxs-lookup"><span data-stu-id="fda10-105">To see the secret value you would have to run this on Azure.</span></span> <span data-ttu-id="fda10-106">В этом кратком руководстве используются приложение Node.js и управляемые удостоверения служб (MSI).</span><span class="sxs-lookup"><span data-stu-id="fda10-106">The quickstart uses Node.js and Managed service identities (MSIs)</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="fda10-107">Создание хранилища Key Vault.</span><span class="sxs-lookup"><span data-stu-id="fda10-107">Create a Key Vault.</span></span>
> * <span data-ttu-id="fda10-108">Сохранение секрета в хранилище Key Vault.</span><span class="sxs-lookup"><span data-stu-id="fda10-108">Store a secret in Key Vault.</span></span>
> * <span data-ttu-id="fda10-109">Получение секрета из хранилища Key Vault.</span><span class="sxs-lookup"><span data-stu-id="fda10-109">Retrieve a secret from Key Vault.</span></span>
> * <span data-ttu-id="fda10-110">Создание веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="fda10-110">Create an Azure Web Application.</span></span>
> * <span data-ttu-id="fda10-111">[Настройка управляемых удостоверений служб](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span><span class="sxs-lookup"><span data-stu-id="fda10-111">[Enable managed service identities](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span></span>
> * <span data-ttu-id="fda10-112">Предоставление веб-приложению необходимых разрешений на чтение данных из хранилища Key Vault.</span><span class="sxs-lookup"><span data-stu-id="fda10-112">Grant the required permissions for the web application to read data from Key vault.</span></span>

<span data-ttu-id="fda10-113">Прежде чем продолжить, убедитесь, что вы ознакомились с [основными понятиями](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span><span class="sxs-lookup"><span data-stu-id="fda10-113">Before you proceed make sure that you are familiar with the [basic concepts](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span></span>

>[!NOTE]
<span data-ttu-id="fda10-114">Чтобы понять, почему в этом руководстве приводятся именно такие рекомендации, необходимо разобраться в нескольких основных понятиях.</span><span class="sxs-lookup"><span data-stu-id="fda10-114">To understand why the below tutorial is the best practice we need to understand a few concepts.</span></span> <span data-ttu-id="fda10-115">Хранилище Key Vault — это центральный репозиторий для хранения секретов программным способом.</span><span class="sxs-lookup"><span data-stu-id="fda10-115">Key Vault is a central repository to store secrets programmatically.</span></span> <span data-ttu-id="fda10-116">Но чтобы воспользоваться возможностями хранилища Key Vault, приложения или пользователи должны сначала пройти в нем проверку подлинности, т. е. предоставить секрет.</span><span class="sxs-lookup"><span data-stu-id="fda10-116">But to do so applications / users need to first authenticate to Key Vault i.e. present a secret.</span></span> <span data-ttu-id="fda10-117">В соответствии с рекомендациями по безопасности первый секрет должен периодически меняться.</span><span class="sxs-lookup"><span data-stu-id="fda10-117">To follow security best practices this first secret needs to be rotated periodically as well.</span></span> <span data-ttu-id="fda10-118">Однако благодаря [управляемому удостоверению службы](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) приложения, работающие в Azure, получают удостоверение, которым автоматически управляет служба Azure.</span><span class="sxs-lookup"><span data-stu-id="fda10-118">But with [Managed Service Identity](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) applications that run in Azure are given an identity which is automatically managed by Azure.</span></span> <span data-ttu-id="fda10-119">Это помогает устранить **проблему введения секрета**, чтобы пользователи и приложения могли следовать рекомендациям и не беспокоиться об изменении первого секрета.</span><span class="sxs-lookup"><span data-stu-id="fda10-119">This helps solve the **Secret Introduction Problem** where users / applications can follow best practices and not have to worry about rotating the first secret</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fda10-120">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="fda10-120">Prerequisites</span></span>

<span data-ttu-id="fda10-121">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="fda10-121">::: zone pivot="nodejs"</span></span>
* <span data-ttu-id="fda10-122">[Node JS](https://nodejs.org/en/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="fda10-122">[Node JS](https://nodejs.org/en/) ::: zone-end</span></span>

<span data-ttu-id="fda10-123">::: zone pivot="dotnet, windows"</span><span class="sxs-lookup"><span data-stu-id="fda10-123">::: zone pivot="dotnet, windows"</span></span>
* <span data-ttu-id="fda10-124">[Visual Studio 2017 начиная с версии 15.7.3](https://www.microsoft.com/net/download/windows) со следующими рабочими нагрузками:</span><span class="sxs-lookup"><span data-stu-id="fda10-124">[Visual Studio 2017 version 15.7.3 or later](https://www.microsoft.com/net/download/windows) with the following workloads:</span></span>
  * <span data-ttu-id="fda10-125">ASP.NET и веб-разработка;</span><span class="sxs-lookup"><span data-stu-id="fda10-125">ASP.NET and web development</span></span>
  * <span data-ttu-id="fda10-126">кроссплатформенная разработка .NET Core.</span><span class="sxs-lookup"><span data-stu-id="fda10-126">.NET Core cross-platform development</span></span>
* <span data-ttu-id="fda10-127">[Пакет SDK для .NET Core начиная с версии 2.1](https://www.microsoft.com/net/download/windows) :::zone-end</span><span class="sxs-lookup"><span data-stu-id="fda10-127">[.NET Core 2.1 SDK or later](https://www.microsoft.com/net/download/windows) :::zone-end</span></span>

<span data-ttu-id="fda10-128">::: zone pivot="dotnet, mac"</span><span class="sxs-lookup"><span data-stu-id="fda10-128">::: zone pivot="dotnet, mac"</span></span>
* <span data-ttu-id="fda10-129">Дополнительные сведения см. в статье [Новые возможности Visual Studio для Mac](https://visualstudio.microsoft.com/vs/mac/).</span><span class="sxs-lookup"><span data-stu-id="fda10-129">See [What’s New in Visual Studio for Mac](https://visualstudio.microsoft.com/vs/mac/).</span></span>
<span data-ttu-id="fda10-130">:::zone-end</span><span class="sxs-lookup"><span data-stu-id="fda10-130">:::zone-end</span></span>

* <span data-ttu-id="fda10-131">Git ([скачать](https://git-scm.com/downloads)).</span><span class="sxs-lookup"><span data-stu-id="fda10-131">Git ([download](https://git-scm.com/downloads)).</span></span>
* <span data-ttu-id="fda10-132">Подписка Azure.</span><span class="sxs-lookup"><span data-stu-id="fda10-132">An Azure subscription.</span></span> <span data-ttu-id="fda10-133">Если у вас еще нет подписки Azure, [создайте бесплатную учетную запись Azure](https://azure.microsoft.com/free/?WT.mc_id=A261C142F), прежде чем начинать работу.</span><span class="sxs-lookup"><span data-stu-id="fda10-133">If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) before you begin.</span></span>
* <span data-ttu-id="fda10-134">[Интерфейс командной строки Azure](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) начиная с версии 2.0.4.</span><span class="sxs-lookup"><span data-stu-id="fda10-134">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) version 2.0.4 or later.</span></span> <span data-ttu-id="fda10-135">Доступен для Windows, Mac и Linux.</span><span class="sxs-lookup"><span data-stu-id="fda10-135">This is available for Windows, Mac, and Linux.</span></span>

## <a name="login-to-azure"></a><span data-ttu-id="fda10-136">Вход в Azure</span><span class="sxs-lookup"><span data-stu-id="fda10-136">Login to Azure</span></span>

<span data-ttu-id="fda10-137">Чтобы войти в Azure с помощью CLI, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="fda10-137">To log in to Azure using the CLI, you can type:</span></span>

```azurecli
az login
```

## <a name="create-resource-group"></a><span data-ttu-id="fda10-138">Создание группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="fda10-138">Create resource group</span></span>

<span data-ttu-id="fda10-139">Создайте группу ресурсов с помощью команды [az group create](/cli/azure/group#az-group-create).</span><span class="sxs-lookup"><span data-stu-id="fda10-139">Create a resource group with the [az group create](/cli/azure/group#az-group-create) command.</span></span> <span data-ttu-id="fda10-140">Группа ресурсов Azure — это логический контейнер, в котором происходит развертывание ресурсов Azure и управление ими.</span><span class="sxs-lookup"><span data-stu-id="fda10-140">An Azure resource group is a logical container into which Azure resources are deployed and managed.</span></span>

<span data-ttu-id="fda10-141">Выберите имя для группы ресурсов и укажите его вместо заполнителя.</span><span class="sxs-lookup"><span data-stu-id="fda10-141">Please select a Resource Group name and fill in the placeholder.</span></span>
<span data-ttu-id="fda10-142">В следующем примере создается группа ресурсов с именем *<YourResourceGroupName>* в расположении *eastus*.</span><span class="sxs-lookup"><span data-stu-id="fda10-142">The following example creates a resource group named *<YourResourceGroupName>* in the *eastus* location.</span></span>

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="fda10-143">Созданная группа ресурсов будет использоваться далее в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="fda10-143">The resource group you just created is used throughout this tutorial.</span></span>

## <a name="create-an-azure-key-vault"></a><span data-ttu-id="fda10-144">Создание хранилища Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="fda10-144">Create an Azure Key Vault</span></span>

<span data-ttu-id="fda10-145">Теперь создайте хранилище Key Vault в группе ресурсов, созданной на предыдущем этапе.</span><span class="sxs-lookup"><span data-stu-id="fda10-145">Next you create a Key Vault using the resource group created in the previous step.</span></span> <span data-ttu-id="fda10-146">Несмотря на то что в этом руководстве для хранилища Key Vault используется имя ContosoKeyVault, вам необходимо использовать уникальное имя.</span><span class="sxs-lookup"><span data-stu-id="fda10-146">Although “ContosoKeyVault” is used as the name for the Key Vault throughout this article, you have to use a unique name.</span></span> <span data-ttu-id="fda10-147">Введите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="fda10-147">Provide the following information:</span></span>

* <span data-ttu-id="fda10-148">Имя хранилища. **Здесь нужно выбрать имя для хранилища Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="fda10-148">Vault name - **Select a Key Vault Name here**.</span></span>
* <span data-ttu-id="fda10-149">Имя группы ресурсов. **Здесь нужно выбрать имя для группы ресурсов**.</span><span class="sxs-lookup"><span data-stu-id="fda10-149">Resource group name - **Select a Resource Group Name here**.</span></span>
* <span data-ttu-id="fda10-150">Расположение. **Восточная часть США**.</span><span class="sxs-lookup"><span data-stu-id="fda10-150">The location - **East US**.</span></span>

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="fda10-151">На этом этапе любые операции в новом хранилище может выполнять только ваша учетная запись Azure.</span><span class="sxs-lookup"><span data-stu-id="fda10-151">At this point, your Azure account is the only one authorized to perform any operations on this new vault.</span></span>

## <a name="add-a-secret-to-key-vault"></a><span data-ttu-id="fda10-152">Добавление секрета в хранилище ключей</span><span class="sxs-lookup"><span data-stu-id="fda10-152">Add a secret to key vault</span></span>

<span data-ttu-id="fda10-153">Теперь мы добавим секрет, чтобы продемонстрировать, как это работает.</span><span class="sxs-lookup"><span data-stu-id="fda10-153">We're adding a secret to help illustrate how this works.</span></span> <span data-ttu-id="fda10-154">Вы можете хранить здесь строки подключения SQL и прочие сведения, которые должны храниться в безопасности, но быть доступными для приложения.</span><span class="sxs-lookup"><span data-stu-id="fda10-154">You could be storing a SQL connection string or any other information that you need to keep securely but make available to your application.</span></span> <span data-ttu-id="fda10-155">В этом руководстве мы сохраним в хранилище пароль с именем **AppSecret** и значением **MySecret**.</span><span class="sxs-lookup"><span data-stu-id="fda10-155">In this tutorial, the password will be called **AppSecret** and will store the value of **MySecret** in it.</span></span>

<span data-ttu-id="fda10-156">Введите указанные ниже команды, чтобы создать в хранилище Key Vault секрет с именем **AppSecret** и значением **MySecret**.</span><span class="sxs-lookup"><span data-stu-id="fda10-156">Type the commands below to create a secret in Key Vault called **AppSecret** that will store the value **MySecret**:</span></span>

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

<span data-ttu-id="fda10-157">Чтобы просмотреть содержащееся в секрете значение в виде обычного текста, выполните такую команду:</span><span class="sxs-lookup"><span data-stu-id="fda10-157">To view the value contained in the secret as plain text:</span></span>

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

<span data-ttu-id="fda10-158">Эта команда возвращает значение секрета, включая URI.</span><span class="sxs-lookup"><span data-stu-id="fda10-158">This command shows the secret information including the URI.</span></span> <span data-ttu-id="fda10-159">Выполнив эти действия, вы сохраните в Azure Key Vault секрет со значением URI.</span><span class="sxs-lookup"><span data-stu-id="fda10-159">After completing these steps, you should have a URI to a secret in an Azure Key Vault.</span></span> <span data-ttu-id="fda10-160">Запишите эти сведения.</span><span class="sxs-lookup"><span data-stu-id="fda10-160">Write this information down.</span></span> <span data-ttu-id="fda10-161">Они потребуются вам на следующих этапах.</span><span class="sxs-lookup"><span data-stu-id="fda10-161">You need it in a later step.</span></span>

## <a name="clone-the-repo"></a><span data-ttu-id="fda10-162">Клонирование репозитория</span><span class="sxs-lookup"><span data-stu-id="fda10-162">Clone the Repo</span></span>

<span data-ttu-id="fda10-163">Чтобы создать локальную копию для изменения источника, клонируйте репозиторий, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="fda10-163">Clone the repo in order to make a local copy for you to edit the source by running the following command:</span></span>

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

<span data-ttu-id="fda10-164">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="fda10-164">::: zone pivot="nodejs"</span></span>

## <a name="install-dependencies"></a><span data-ttu-id="fda10-165">Установка зависимостей</span><span class="sxs-lookup"><span data-stu-id="fda10-165">Install dependencies</span></span>

<span data-ttu-id="fda10-166">На этом этапе мы установим зависимости.</span><span class="sxs-lookup"><span data-stu-id="fda10-166">Here we install the dependencies.</span></span> <span data-ttu-id="fda10-167">Выполните следующие команды: cd key-vault-node-quickstart npm install.</span><span class="sxs-lookup"><span data-stu-id="fda10-167">Run the following commands cd key-vault-node-quickstart npm install</span></span>

<span data-ttu-id="fda10-168">В этом проекте используются два модуля узла:</span><span class="sxs-lookup"><span data-stu-id="fda10-168">This project used 2 node modules:</span></span>

* <span data-ttu-id="fda10-169">[ms-rest-azure](https://www.npmjs.com/package/ms-rest-azure);</span><span class="sxs-lookup"><span data-stu-id="fda10-169">[ms-rest-azure](https://www.npmjs.com/package/ms-rest-azure)</span></span> 
* <span data-ttu-id="fda10-170">[azure-keyvault](https://www.npmjs.com/package/azure-keyvault).</span><span class="sxs-lookup"><span data-stu-id="fda10-170">[azure-keyvault](https://www.npmjs.com/package/azure-keyvault)</span></span>

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="fda10-171">Публикация веб-приложения в Azure</span><span class="sxs-lookup"><span data-stu-id="fda10-171">Publish the web application to Azure</span></span>

<span data-ttu-id="fda10-172">Ниже приведены несколько шагов, которые нам нужно выполнить.</span><span class="sxs-lookup"><span data-stu-id="fda10-172">Below are the few steps we need to do</span></span>

* <span data-ttu-id="fda10-173">Первый шаг — создание плана [Службы приложений Azure](https://azure.microsoft.com/services/app-service/).</span><span class="sxs-lookup"><span data-stu-id="fda10-173">The 1st step is to create a [Azure App Service](https://azure.microsoft.com/services/app-service/) Plan.</span></span> <span data-ttu-id="fda10-174">В этом плане можно хранить несколько веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="fda10-174">You can store multiple web apps in this plan.</span></span>

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* <span data-ttu-id="fda10-175">Затем нам нужно создать веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="fda10-175">Next we create a web app.</span></span> <span data-ttu-id="fda10-176">В примере ниже замените <app_name> глобальным уникальным именем приложения (допустимые символы: a-z, 0-9 и -).</span><span class="sxs-lookup"><span data-stu-id="fda10-176">In the following example, replace <app_name> with a globally unique app name (valid characters are a-z, 0-9, and -).</span></span> <span data-ttu-id="fda10-177">В качестве среды выполнения выбрано NODE|6.9.</span><span class="sxs-lookup"><span data-stu-id="fda10-177">The runtime is set to NODE|6.9.</span></span> <span data-ttu-id="fda10-178">Чтобы просмотреть все поддерживаемые среды выполнения, выполните команду az webapp list-runtimes.</span><span class="sxs-lookup"><span data-stu-id="fda10-178">To see all supported runtimes, run az webapp list-runtimes</span></span>

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    <span data-ttu-id="fda10-179">Когда веб-приложение будет создано, в Azure CLI отобразится примерно следующее:</span><span class="sxs-lookup"><span data-stu-id="fda10-179">When the web app has been created, the Azure CLI shows output similar to the following example:</span></span>

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
    <span data-ttu-id="fda10-180">Перейдите к только что созданному веб-приложению. Вы увидите действующее веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="fda10-180">Browse to your newly created web app and you should see a functioning web app.</span></span> <span data-ttu-id="fda10-181">Замените <app_name> уникальным именем приложения.</span><span class="sxs-lookup"><span data-stu-id="fda10-181">Replace <app_name> with a unique app name.</span></span>

    ```text
    http://<app name>.azurewebsites.net
    ```
    <span data-ttu-id="fda10-182">Приведенная выше команда также создает приложение с поддержкой Git, которое позволяет выполнять развертывание в Azure из локального репозитория Git.</span><span class="sxs-lookup"><span data-stu-id="fda10-182">The above command also creates a Git-enabled app which allows you to deploy to azure from your local git.</span></span> 
    <span data-ttu-id="fda10-183">Для локального репозитория Git настроен URL-адрес https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git.</span><span class="sxs-lookup"><span data-stu-id="fda10-183">Local git is configured with url of 'https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git'</span></span>

* <span data-ttu-id="fda10-184">Создайте пользователя развертывания. После завершения предыдущей команды можно добавить удаленную службу приложений Azure в локальный репозиторий Git.</span><span class="sxs-lookup"><span data-stu-id="fda10-184">Create a deployment user After the previous command is completed you can add add an Azure remote to your local Git repository.</span></span> <span data-ttu-id="fda10-185">Замените <url> URL-адресом удаленного репозитория Git, который был получен при включении использования репозитория Git для приложения.</span><span class="sxs-lookup"><span data-stu-id="fda10-185">Replace <url> with the URL of the Git remote that you got from Enable Git for your app.</span></span>

    ```bash
    git remote add azure <url>
    ```
<span data-ttu-id="fda10-186">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="fda10-186">::: zone-end</span></span>

<span data-ttu-id="fda10-187">::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="fda10-187">::: zone pivot="dotnet"</span></span>

## <a name="open-and-edit-the-solution"></a><span data-ttu-id="fda10-188">Открытие и изменение решения</span><span class="sxs-lookup"><span data-stu-id="fda10-188">Open and edit the solution</span></span>

<span data-ttu-id="fda10-189">Измените файл program.cs, чтобы запустить образец со своим именем хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="fda10-189">Edit the program.cs file to run the sample with your specific key vault name:</span></span>

1. <span data-ttu-id="fda10-190">Перейдите в папку key-vault-dotnet-core-quickstart.</span><span class="sxs-lookup"><span data-stu-id="fda10-190">Browse to the folder key-vault-dotnet-core-quickstart.</span></span>
2. <span data-ttu-id="fda10-191">Откройте в Visual Studio 2017 файл key-vault-dotnet-core-quickstart.sln.</span><span class="sxs-lookup"><span data-stu-id="fda10-191">Open the key-vault-dotnet-core-quickstart.sln file in Visual Studio 2017.</span></span>
3. <span data-ttu-id="fda10-192">Откройте файл Program.cs и вместо заполнителя *YourKeyVaultName* укажите имя вашего хранилища ключей, которое вы создали ранее.</span><span class="sxs-lookup"><span data-stu-id="fda10-192">Open the Program.cs file and update the placeholder *YourKeyVaultName* with the name of your key vault that you created earlier.</span></span>

<span data-ttu-id="fda10-193">В этом решении используются библиотеки NuGet [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) и [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault).</span><span class="sxs-lookup"><span data-stu-id="fda10-193">This solution uses [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) and [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet libraries.</span></span>

## <a name="run-the-app"></a><span data-ttu-id="fda10-194">Запуск приложения</span><span class="sxs-lookup"><span data-stu-id="fda10-194">Run the app</span></span>

<span data-ttu-id="fda10-195">В главном меню Visual Studio 2017 выберите **Отладка** > **Запуск без отладки**.</span><span class="sxs-lookup"><span data-stu-id="fda10-195">From the main menu of Visual Studio 2017, select **Debug** > **Start** without debugging.</span></span> <span data-ttu-id="fda10-196">Когда откроется браузер, перейдите на страницу **О программе**.</span><span class="sxs-lookup"><span data-stu-id="fda10-196">When the browser appears, go to the **About** page.</span></span> <span data-ttu-id="fda10-197">Вы увидите значение **AppSecret**.</span><span class="sxs-lookup"><span data-stu-id="fda10-197">The value for **AppSecret** is displayed.</span></span>

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="fda10-198">Публикация веб-приложения в Azure</span><span class="sxs-lookup"><span data-stu-id="fda10-198">Publish the web application to Azure</span></span>

<span data-ttu-id="fda10-199">Опубликуйте это приложение в Azure, чтобы увидеть, как оно работает в реальной среде, а также убедиться, что вы можете получить значение секрета.</span><span class="sxs-lookup"><span data-stu-id="fda10-199">Publish this app to Azure to see it live as a web app, and to see that you can fetch the secret value:</span></span>

1. <span data-ttu-id="fda10-200">В Visual Studio выберите проект **key-vault-dotnet-core-quickstart**.</span><span class="sxs-lookup"><span data-stu-id="fda10-200">In Visual Studio, select the **key-vault-dotnet-core-quickstart** project.</span></span>
2. <span data-ttu-id="fda10-201">Выберите **Опубликовать** > **Запуск**.</span><span class="sxs-lookup"><span data-stu-id="fda10-201">Select **Publish** > **Start**.</span></span>
3. <span data-ttu-id="fda10-202">Создайте новую **службу приложений**, а затем выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="fda10-202">Create a new **App Service**, and then select **Publish**.</span></span>
4. <span data-ttu-id="fda10-203">Измените имя приложения на **keyvaultdotnetcorequickstart**.</span><span class="sxs-lookup"><span data-stu-id="fda10-203">Change the app name to **keyvaultdotnetcorequickstart**.</span></span>
5. <span data-ttu-id="fda10-204">Щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="fda10-204">Select **Create**.</span></span>

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]

<span data-ttu-id="fda10-205">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="fda10-205">::: zone-end</span></span>

## <a name="enable-managed-service-identities"></a><span data-ttu-id="fda10-206">Настройка управляемых удостоверений служб</span><span class="sxs-lookup"><span data-stu-id="fda10-206">Enable managed service identities</span></span>

<span data-ttu-id="fda10-207">Azure Key Vault позволяет безопасно хранить учетные данные, а также другие ключи и секреты, но для их получения код должен пройти проверку подлинности в Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="fda10-207">Azure Key Vault provides a way to securely store credentials and other keys and secrets, but your code needs to authenticate to Azure Key Vault to retrieve them.</span></span> <span data-ttu-id="fda10-208">Управляемое удостоверение службы упрощает решение этой задачи, предоставляя службам Azure автоматически управляемое удостоверение из Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="fda10-208">Managed Service Identity makes this easier by giving Azure services an automatically managed identity in Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="fda10-209">Вы можете использовать это удостоверение для прохождения проверки подлинности в любой службе, которая поддерживает аутентификацию Azure AD, в том числе в Key Vault, не храня в коде никакие учетные данные.</span><span class="sxs-lookup"><span data-stu-id="fda10-209">You can use this identity to authenticate to any service that supports Azure AD authentication, including Key Vault, without having any credentials in your code.</span></span>

1. <span data-ttu-id="fda10-210">Вернитесь в окно Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="fda10-210">Return to the Azure CLI.</span></span>
2. <span data-ttu-id="fda10-211">Выполните команду назначения удостоверения, чтобы создать удостоверение для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="fda10-211">Run the assign-identity command to create the identity for this application:</span></span>

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
><span data-ttu-id="fda10-212">Выполнение этой команды равноценно выбору значения **Вкл.** для параметра **Управляемое удостоверение службы** в свойствах веб-приложения на портале.</span><span class="sxs-lookup"><span data-stu-id="fda10-212">The command in this procedure is the equivalent of going to the portal and switching **Managed service identity** to **On** in the web application properties.</span></span>

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a><span data-ttu-id="fda10-213">Назначение разрешений приложению для чтения секретов из хранилища Key Vault</span><span class="sxs-lookup"><span data-stu-id="fda10-213">Assign permissions to your application to read secrets from Key Vault</span></span>

<span data-ttu-id="fda10-214">Запишите выходные данные при публикации приложения в Azure.</span><span class="sxs-lookup"><span data-stu-id="fda10-214">Make a note of the output when you publish the application to Azure.</span></span> <span data-ttu-id="fda10-215">Они должны быть представлены в таком формате:</span><span class="sxs-lookup"><span data-stu-id="fda10-215">It should be of the format:</span></span>

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

<span data-ttu-id="fda10-216">Затем, используя имя своего хранилища ключей и значение **PrincipalId**, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="fda10-216">Then, run this command by using the name of your key vault and the value of **PrincipalId**:</span></span>

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

<span data-ttu-id="fda10-217">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="fda10-217">::: zone pivot="nodejs"</span></span>
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a><span data-ttu-id="fda10-218">Развертывание приложения Node.js в Azure и получение значения секрета</span><span class="sxs-lookup"><span data-stu-id="fda10-218">Deploy the Node App to Azure and retrieve the secret value</span></span>

<span data-ttu-id="fda10-219">Теперь, когда все готово,</span><span class="sxs-lookup"><span data-stu-id="fda10-219">Now that everything is set.</span></span> <span data-ttu-id="fda10-220">выполните приведенную ниже команду, чтобы развернуть приложение в Azure.</span><span class="sxs-lookup"><span data-stu-id="fda10-220">Run the following command to deploy the app to Azure</span></span>

```bash
git push azure master
```

<span data-ttu-id="fda10-221">После этого на странице https://<app_name>.azurewebsites.net вы сможете увидеть значение секрета.</span><span class="sxs-lookup"><span data-stu-id="fda10-221">After this when you browse https://<app_name>.azurewebsites.net you can see the secret value.</span></span>
<span data-ttu-id="fda10-222">Не забудьте заменить имя <YourKeyVaultName> именем своего хранилища. ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="fda10-222">Make sure that you replaced the name <YourKeyVaultName> with your vault name ::: zone-end</span></span>

<span data-ttu-id="fda10-223">::: zone pivot="dotnet" Теперь при запуске приложения вы должны увидеть извлеченное значение секрета.</span><span class="sxs-lookup"><span data-stu-id="fda10-223">::: zone pivot="dotnet" Now when you run the application, you should see your secret value retrieved.</span></span>
<span data-ttu-id="fda10-224">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="fda10-224">::: zone-end</span></span>

## <a name="next-steps"></a><span data-ttu-id="fda10-225">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="fda10-225">Next steps</span></span>

<span data-ttu-id="fda10-226">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="fda10-226">::: zone pivot="nodejs"</span></span>
* [<span data-ttu-id="fda10-227">Домашняя страница Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="fda10-227">Azure Key Vault Home Page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="fda10-228">Документация Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="fda10-228">Azure Key Vault Documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="fda10-229">Пакет SDK Azure для Node.js</span><span class="sxs-lookup"><span data-stu-id="fda10-229">Azure SDK For Node</span></span>](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* <span data-ttu-id="fda10-230">[Справочник по REST API в Azure](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="fda10-230">[Azure REST API Reference](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span></span>

<span data-ttu-id="fda10-231">::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="fda10-231">::: zone pivot="dotnet"</span></span>
* [<span data-ttu-id="fda10-232">Домашняя страница Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="fda10-232">Azure Key Vault home page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="fda10-233">Документация Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="fda10-233">Azure Key Vault documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="fda10-234">Пакет SDK Azure для .NET</span><span class="sxs-lookup"><span data-stu-id="fda10-234">Azure SDK For .NET</span></span>](https://github.com/Azure/azure-sdk-for-net)
* <span data-ttu-id="fda10-235">[Справочник по REST API в Azure](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="fda10-235">[Azure REST API reference](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span></span>