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
ms.openlocfilehash: 27ebd3e348fc231d8b82e6c17f282bd9ca4afb9f
ms.sourcegitcommit: 5e508a7ad2991632a38f302e4769b36e3bf37eb2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/30/2018
ms.locfileid: "43308831"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a><span data-ttu-id="d8b3a-103">Краткое руководство. Настройка и получение секрета из Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="d8b3a-103">Quickstart: Set and retrieve a secret from Azure Key Vault</span></span>

<span data-ttu-id="d8b3a-104">Из этого краткого руководства вы узнаете, как сохранить секрет в службе Key Vault и как его получать с помощью веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-104">This quickstart shows you how to store a secret in Key Vault and how to retrieve it using a Web app.</span></span> <span data-ttu-id="d8b3a-105">Чтобы была возможность просмотреть значение секрета, приложение должно работать в Azure.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-105">To see the secret value you would have to run this on Azure.</span></span> <span data-ttu-id="d8b3a-106">В этом кратком руководстве используются приложение Node.js и управляемые удостоверения служб (MSI).</span><span class="sxs-lookup"><span data-stu-id="d8b3a-106">The quickstart uses Node.js and Managed service identities (MSIs)</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="d8b3a-107">Создание хранилища Key Vault.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-107">Create a Key Vault.</span></span>
> * <span data-ttu-id="d8b3a-108">Сохранение секрета в хранилище Key Vault.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-108">Store a secret in Key Vault.</span></span>
> * <span data-ttu-id="d8b3a-109">Получение секрета из хранилища Key Vault.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-109">Retrieve a secret from Key Vault.</span></span>
> * <span data-ttu-id="d8b3a-110">Создание веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-110">Create an Azure Web Application.</span></span>
> * <span data-ttu-id="d8b3a-111">[Настройка управляемых удостоверений служб](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span><span class="sxs-lookup"><span data-stu-id="d8b3a-111">[Enable managed service identities](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span></span>
> * <span data-ttu-id="d8b3a-112">Предоставление веб-приложению необходимых разрешений на чтение данных из хранилища Key Vault.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-112">Grant the required permissions for the web application to read data from Key vault.</span></span>

<span data-ttu-id="d8b3a-113">Прежде чем продолжить, убедитесь, что вы ознакомились с [основными понятиями](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span><span class="sxs-lookup"><span data-stu-id="d8b3a-113">Before you proceed make sure that you are familiar with the [basic concepts](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span></span>

> [!NOTE]
> <span data-ttu-id="d8b3a-114">Чтобы понять, почему в этом руководстве приводятся именно такие рекомендации, необходимо разобраться в нескольких основных понятиях.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-114">To understand why the below tutorial is the best practice we need to understand a few concepts.</span></span> <span data-ttu-id="d8b3a-115">Хранилище Key Vault — это центральный репозиторий для хранения секретов программным способом.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-115">Key Vault is a central repository to store secrets programmatically.</span></span> <span data-ttu-id="d8b3a-116">Но чтобы воспользоваться возможностями хранилища Key Vault, приложения или пользователи должны сначала пройти в нем проверку подлинности, т. е. предоставить секрет.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-116">But to do so applications / users need to first authenticate to Key Vault i.e. present a secret.</span></span> <span data-ttu-id="d8b3a-117">В соответствии с рекомендациями по безопасности первый секрет должен периодически меняться.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-117">To follow security best practices this first secret needs to be rotated periodically as well.</span></span> <span data-ttu-id="d8b3a-118">Однако благодаря [управляемому удостоверению службы](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) приложения, работающие в Azure, получают удостоверение, которым автоматически управляет служба Azure.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-118">But with [Managed Service Identity](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) applications that run in Azure are given an identity which is automatically managed by Azure.</span></span> <span data-ttu-id="d8b3a-119">Это помогает устранить **проблему введения секрета**, чтобы пользователи и приложения могли следовать рекомендациям и не беспокоиться об изменении первого секрета.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-119">This helps solve the **Secret Introduction Problem** where users / applications can follow best practices and not have to worry about rotating the first secret</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d8b3a-120">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="d8b3a-120">Prerequisites</span></span>

<span data-ttu-id="d8b3a-121">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="d8b3a-121">::: zone pivot="nodejs"</span></span>
* <span data-ttu-id="d8b3a-122">[Node JS](https://nodejs.org/en/) ::: zone-end ::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="d8b3a-122">[Node JS](https://nodejs.org/en/) ::: zone-end ::: zone pivot="dotnet"</span></span>
* <span data-ttu-id="d8b3a-123">[Visual Studio 2017 начиная с версии 15.7.3](https://www.microsoft.com/net/download/windows) со следующими рабочими нагрузками:</span><span class="sxs-lookup"><span data-stu-id="d8b3a-123">[Visual Studio 2017 version 15.7.3 or later](https://www.microsoft.com/net/download/windows) with the following workloads:</span></span>
  * <span data-ttu-id="d8b3a-124">ASP.NET и веб-разработка;</span><span class="sxs-lookup"><span data-stu-id="d8b3a-124">ASP.NET and web development</span></span>
  * <span data-ttu-id="d8b3a-125">кроссплатформенная разработка .NET Core.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-125">.NET Core cross-platform development</span></span>
* <span data-ttu-id="d8b3a-126">[Пакет SDK для .NET Core начиная с версии 2.1](https://www.microsoft.com/net/download/windows) :::zone-end</span><span class="sxs-lookup"><span data-stu-id="d8b3a-126">[.NET Core 2.1 SDK or later](https://www.microsoft.com/net/download/windows) ::: zone-end</span></span>
* <span data-ttu-id="d8b3a-127">Git ([скачать](https://git-scm.com/downloads)).</span><span class="sxs-lookup"><span data-stu-id="d8b3a-127">Git ([download](https://git-scm.com/downloads)).</span></span>
* <span data-ttu-id="d8b3a-128">Подписка Azure.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-128">An Azure subscription.</span></span> <span data-ttu-id="d8b3a-129">Если у вас еще нет подписки Azure, [создайте бесплатную учетную запись Azure](https://azure.microsoft.com/free/?WT.mc_id=A261C142F), прежде чем начинать работу.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-129">If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) before you begin.</span></span>
* <span data-ttu-id="d8b3a-130">[Интерфейс командной строки Azure](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) начиная с версии 2.0.4.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-130">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) version 2.0.4 or later.</span></span> <span data-ttu-id="d8b3a-131">Доступен для Windows, Mac и Linux.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-131">This is available for Windows, Mac, and Linux.</span></span>

## <a name="login-to-azure"></a><span data-ttu-id="d8b3a-132">Вход в Azure</span><span class="sxs-lookup"><span data-stu-id="d8b3a-132">Login to Azure</span></span>

<span data-ttu-id="d8b3a-133">Чтобы войти в Azure с помощью CLI, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d8b3a-133">To log in to Azure using the CLI, you can type:</span></span>

```azurecli
az login
```

## <a name="create-resource-group"></a><span data-ttu-id="d8b3a-134">Создание группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d8b3a-134">Create resource group</span></span>

<span data-ttu-id="d8b3a-135">Создайте группу ресурсов с помощью команды [az group create](/cli/azure/group#az-group-create).</span><span class="sxs-lookup"><span data-stu-id="d8b3a-135">Create a resource group with the [az group create](/cli/azure/group#az-group-create) command.</span></span> <span data-ttu-id="d8b3a-136">Группа ресурсов Azure — это логический контейнер, в котором происходит развертывание ресурсов Azure и управление ими.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-136">An Azure resource group is a logical container into which Azure resources are deployed and managed.</span></span>

<span data-ttu-id="d8b3a-137">Выберите имя для группы ресурсов и укажите его вместо заполнителя.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-137">Please select a Resource Group name and fill in the placeholder.</span></span>
<span data-ttu-id="d8b3a-138">В следующем примере создается группа ресурсов с именем *<YourResourceGroupName>* в расположении *eastus*.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-138">The following example creates a resource group named *<YourResourceGroupName>* in the *eastus* location.</span></span>

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="d8b3a-139">Созданная группа ресурсов будет использоваться далее в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-139">The resource group you just created is used throughout this tutorial.</span></span>

## <a name="create-an-azure-key-vault"></a><span data-ttu-id="d8b3a-140">Создание хранилища Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="d8b3a-140">Create an Azure Key Vault</span></span>

<span data-ttu-id="d8b3a-141">Теперь создайте хранилище Key Vault в группе ресурсов, созданной на предыдущем этапе.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-141">Next you create a Key Vault using the resource group created in the previous step.</span></span> <span data-ttu-id="d8b3a-142">Несмотря на то что в этом руководстве для хранилища Key Vault используется имя ContosoKeyVault, вам необходимо использовать уникальное имя.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-142">Although “ContosoKeyVault” is used as the name for the Key Vault throughout this article, you have to use a unique name.</span></span> <span data-ttu-id="d8b3a-143">Введите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="d8b3a-143">Provide the following information:</span></span>

* <span data-ttu-id="d8b3a-144">Имя хранилища. **Здесь нужно выбрать имя для хранилища Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-144">Vault name - **Select a Key Vault Name here**.</span></span>
* <span data-ttu-id="d8b3a-145">Имя группы ресурсов. **Здесь нужно выбрать имя для группы ресурсов**.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-145">Resource group name - **Select a Resource Group Name here**.</span></span>
* <span data-ttu-id="d8b3a-146">Расположение. **Восточная часть США**.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-146">The location - **East US**.</span></span>

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="d8b3a-147">На этом этапе любые операции в новом хранилище может выполнять только ваша учетная запись Azure.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-147">At this point, your Azure account is the only one authorized to perform any operations on this new vault.</span></span>

## <a name="add-a-secret-to-key-vault"></a><span data-ttu-id="d8b3a-148">Добавление секрета в хранилище ключей</span><span class="sxs-lookup"><span data-stu-id="d8b3a-148">Add a secret to key vault</span></span>

<span data-ttu-id="d8b3a-149">Теперь мы добавим секрет, чтобы продемонстрировать, как это работает.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-149">We're adding a secret to help illustrate how this works.</span></span> <span data-ttu-id="d8b3a-150">Вы можете хранить здесь строки подключения SQL и прочие сведения, которые должны храниться в безопасности, но быть доступными для приложения.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-150">You could be storing a SQL connection string or any other information that you need to keep securely but make available to your application.</span></span> <span data-ttu-id="d8b3a-151">В этом руководстве мы сохраним в хранилище пароль с именем **AppSecret** и значением **MySecret**.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-151">In this tutorial, the password will be called **AppSecret** and will store the value of **MySecret** in it.</span></span>

<span data-ttu-id="d8b3a-152">Введите указанные ниже команды, чтобы создать в хранилище Key Vault секрет с именем **AppSecret** и значением **MySecret**.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-152">Type the commands below to create a secret in Key Vault called **AppSecret** that will store the value **MySecret**:</span></span>

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

<span data-ttu-id="d8b3a-153">Чтобы просмотреть содержащееся в секрете значение в виде обычного текста, выполните такую команду:</span><span class="sxs-lookup"><span data-stu-id="d8b3a-153">To view the value contained in the secret as plain text:</span></span>

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

<span data-ttu-id="d8b3a-154">Эта команда возвращает значение секрета, включая URI.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-154">This command shows the secret information including the URI.</span></span> <span data-ttu-id="d8b3a-155">Выполнив эти действия, вы сохраните в Azure Key Vault секрет со значением URI.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-155">After completing these steps, you should have a URI to a secret in an Azure Key Vault.</span></span> <span data-ttu-id="d8b3a-156">Запишите эти сведения.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-156">Write this information down.</span></span> <span data-ttu-id="d8b3a-157">Они потребуются вам на следующих этапах.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-157">You need it in a later step.</span></span>

## <a name="clone-the-repo"></a><span data-ttu-id="d8b3a-158">Клонирование репозитория</span><span class="sxs-lookup"><span data-stu-id="d8b3a-158">Clone the Repo</span></span>

<span data-ttu-id="d8b3a-159">Чтобы создать локальную копию для изменения источника, клонируйте репозиторий, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d8b3a-159">Clone the repo in order to make a local copy for you to edit the source by running the following command:</span></span>

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

<span data-ttu-id="d8b3a-160">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="d8b3a-160">::: zone pivot="nodejs"</span></span>

## <a name="install-dependencies"></a><span data-ttu-id="d8b3a-161">Установка зависимостей</span><span class="sxs-lookup"><span data-stu-id="d8b3a-161">Install dependencies</span></span>

<span data-ttu-id="d8b3a-162">На этом этапе мы установим зависимости.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-162">Here we install the dependencies.</span></span> <span data-ttu-id="d8b3a-163">Выполните следующие команды: cd key-vault-node-quickstart npm install.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-163">Run the following commands cd key-vault-node-quickstart npm install</span></span>

<span data-ttu-id="d8b3a-164">В этом проекте используются два модуля узла:</span><span class="sxs-lookup"><span data-stu-id="d8b3a-164">This project used 2 node modules:</span></span>

* <span data-ttu-id="d8b3a-165">[ms-rest-azure](https://www.npmjs.com/package/ms-rest-azure);</span><span class="sxs-lookup"><span data-stu-id="d8b3a-165">[ms-rest-azure](https://www.npmjs.com/package/ms-rest-azure)</span></span> 
* <span data-ttu-id="d8b3a-166">[azure-keyvault](https://www.npmjs.com/package/azure-keyvault).</span><span class="sxs-lookup"><span data-stu-id="d8b3a-166">[azure-keyvault](https://www.npmjs.com/package/azure-keyvault)</span></span>

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="d8b3a-167">Публикация веб-приложения в Azure</span><span class="sxs-lookup"><span data-stu-id="d8b3a-167">Publish the web application to Azure</span></span>

<span data-ttu-id="d8b3a-168">Ниже приведены несколько шагов, которые нам нужно выполнить.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-168">Below are the few steps we need to do</span></span>

* <span data-ttu-id="d8b3a-169">Первый шаг — создание плана [Службы приложений Azure](https://azure.microsoft.com/services/app-service/).</span><span class="sxs-lookup"><span data-stu-id="d8b3a-169">The 1st step is to create a [Azure App Service](https://azure.microsoft.com/services/app-service/) Plan.</span></span> <span data-ttu-id="d8b3a-170">В этом плане можно хранить несколько веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-170">You can store multiple web apps in this plan.</span></span>

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* <span data-ttu-id="d8b3a-171">Затем нам нужно создать веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-171">Next we create a web app.</span></span> <span data-ttu-id="d8b3a-172">В примере ниже замените <app_name> глобальным уникальным именем приложения (допустимые символы: a-z, 0-9 и -).</span><span class="sxs-lookup"><span data-stu-id="d8b3a-172">In the following example, replace <app_name> with a globally unique app name (valid characters are a-z, 0-9, and -).</span></span> <span data-ttu-id="d8b3a-173">В качестве среды выполнения выбрано NODE|6.9.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-173">The runtime is set to NODE|6.9.</span></span> <span data-ttu-id="d8b3a-174">Чтобы просмотреть все поддерживаемые среды выполнения, выполните команду az webapp list-runtimes.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-174">To see all supported runtimes, run az webapp list-runtimes</span></span>

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    <span data-ttu-id="d8b3a-175">Когда веб-приложение будет создано, в Azure CLI отобразится примерно следующее:</span><span class="sxs-lookup"><span data-stu-id="d8b3a-175">When the web app has been created, the Azure CLI shows output similar to the following example:</span></span>

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
    <span data-ttu-id="d8b3a-176">Перейдите к только что созданному веб-приложению. Вы увидите действующее веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-176">Browse to your newly created web app and you should see a functioning web app.</span></span> <span data-ttu-id="d8b3a-177">Замените <app_name> уникальным именем приложения.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-177">Replace <app_name> with a unique app name.</span></span>

    ```text
    http://<app name>.azurewebsites.net
    ```
    <span data-ttu-id="d8b3a-178">Приведенная выше команда также создает приложение с поддержкой Git, которое позволяет выполнять развертывание в Azure из локального репозитория Git.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-178">The above command also creates a Git-enabled app which allows you to deploy to azure from your local git.</span></span> 
    <span data-ttu-id="d8b3a-179">Для локального репозитория Git настроен URL-адрес https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-179">Local git is configured with url of 'https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git'</span></span>

* <span data-ttu-id="d8b3a-180">Создайте пользователя развертывания. После завершения предыдущей команды можно добавить удаленную службу приложений Azure в локальный репозиторий Git.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-180">Create a deployment user After the previous command is completed you can add add an Azure remote to your local Git repository.</span></span> <span data-ttu-id="d8b3a-181">Замените <url> URL-адресом удаленного репозитория Git, который был получен при включении использования репозитория Git для приложения.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-181">Replace <url> with the URL of the Git remote that you got from Enable Git for your app.</span></span>

    ```bash
    git remote add azure <url>
    ```
    
<span data-ttu-id="d8b3a-182">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="d8b3a-182">::: zone-end</span></span>

<span data-ttu-id="d8b3a-183">::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="d8b3a-183">::: zone pivot="dotnet"</span></span>
## <a name="open-and-edit-the-solution"></a><span data-ttu-id="d8b3a-184">Открытие и изменение решения</span><span class="sxs-lookup"><span data-stu-id="d8b3a-184">Open and edit the solution</span></span>

<span data-ttu-id="d8b3a-185">Измените файл program.cs, чтобы запустить образец со своим именем хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-185">Edit the program.cs file to run the sample with your specific key vault name:</span></span>

1. <span data-ttu-id="d8b3a-186">Перейдите в папку key-vault-dotnet-core-quickstart.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-186">Browse to the folder key-vault-dotnet-core-quickstart.</span></span>
2. <span data-ttu-id="d8b3a-187">Откройте в Visual Studio 2017 файл key-vault-dotnet-core-quickstart.sln.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-187">Open the key-vault-dotnet-core-quickstart.sln file in Visual Studio 2017.</span></span>
3. <span data-ttu-id="d8b3a-188">Откройте файл Program.cs и вместо заполнителя *YourKeyVaultName* укажите имя вашего хранилища ключей, которое вы создали ранее.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-188">Open the Program.cs file and update the placeholder *YourKeyVaultName* with the name of your key vault that you created earlier.</span></span>

<span data-ttu-id="d8b3a-189">В этом решении используются библиотеки NuGet [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) и [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault).</span><span class="sxs-lookup"><span data-stu-id="d8b3a-189">This solution uses [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) and [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet libraries.</span></span>

## <a name="run-the-app"></a><span data-ttu-id="d8b3a-190">Запуск приложения</span><span class="sxs-lookup"><span data-stu-id="d8b3a-190">Run the app</span></span>

<span data-ttu-id="d8b3a-191">В главном меню Visual Studio 2017 выберите **Отладка** > **Запуск без отладки**.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-191">From the main menu of Visual Studio 2017, select **Debug** > **Start** without debugging.</span></span> <span data-ttu-id="d8b3a-192">Когда откроется браузер, перейдите на страницу **О программе**.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-192">When the browser appears, go to the **About** page.</span></span> <span data-ttu-id="d8b3a-193">Вы увидите значение **AppSecret**.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-193">The value for **AppSecret** is displayed.</span></span>

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="d8b3a-194">Публикация веб-приложения в Azure</span><span class="sxs-lookup"><span data-stu-id="d8b3a-194">Publish the web application to Azure</span></span>

<span data-ttu-id="d8b3a-195">Опубликуйте это приложение в Azure, чтобы увидеть, как оно работает в реальной среде, а также убедиться, что вы можете получить значение секрета.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-195">Publish this app to Azure to see it live as a web app, and to see that you can fetch the secret value:</span></span>

1. <span data-ttu-id="d8b3a-196">В Visual Studio выберите проект **key-vault-dotnet-core-quickstart**.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-196">In Visual Studio, select the **key-vault-dotnet-core-quickstart** project.</span></span>
2. <span data-ttu-id="d8b3a-197">Выберите **Опубликовать** > **Запуск**.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-197">Select **Publish** > **Start**.</span></span>
3. <span data-ttu-id="d8b3a-198">Создайте новую **службу приложений**, а затем выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-198">Create a new **App Service**, and then select **Publish**.</span></span>
4. <span data-ttu-id="d8b3a-199">Измените имя приложения на **keyvaultdotnetcorequickstart**.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-199">Change the app name to **keyvaultdotnetcorequickstart**.</span></span>
5. <span data-ttu-id="d8b3a-200">Щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-200">Select **Create**.</span></span>

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]
<span data-ttu-id="d8b3a-201">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="d8b3a-201">::: zone-end</span></span>

## <a name="enable-managed-service-identities"></a><span data-ttu-id="d8b3a-202">Настройка управляемых удостоверений служб</span><span class="sxs-lookup"><span data-stu-id="d8b3a-202">Enable managed service identities</span></span>

<span data-ttu-id="d8b3a-203">Azure Key Vault позволяет безопасно хранить учетные данные, а также другие ключи и секреты, но для их получения код должен пройти проверку подлинности в Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-203">Azure Key Vault provides a way to securely store credentials and other keys and secrets, but your code needs to authenticate to Azure Key Vault to retrieve them.</span></span> <span data-ttu-id="d8b3a-204">Управляемое удостоверение службы упрощает решение этой задачи, предоставляя службам Azure автоматически управляемое удостоверение из Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="d8b3a-204">Managed Service Identity makes this easier by giving Azure services an automatically managed identity in Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="d8b3a-205">Вы можете использовать это удостоверение для прохождения проверки подлинности в любой службе, которая поддерживает аутентификацию Azure AD, в том числе в Key Vault, не храня в коде никакие учетные данные.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-205">You can use this identity to authenticate to any service that supports Azure AD authentication, including Key Vault, without having any credentials in your code.</span></span>

1. <span data-ttu-id="d8b3a-206">Вернитесь в окно Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-206">Return to the Azure CLI.</span></span>
2. <span data-ttu-id="d8b3a-207">Выполните команду назначения удостоверения, чтобы создать удостоверение для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-207">Run the assign-identity command to create the identity for this application:</span></span>

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
><span data-ttu-id="d8b3a-208">Выполнение этой команды равноценно выбору значения **Вкл.** для параметра **Управляемое удостоверение службы** в свойствах веб-приложения на портале.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-208">The command in this procedure is the equivalent of going to the portal and switching **Managed service identity** to **On** in the web application properties.</span></span>

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a><span data-ttu-id="d8b3a-209">Назначение разрешений приложению для чтения секретов из хранилища Key Vault</span><span class="sxs-lookup"><span data-stu-id="d8b3a-209">Assign permissions to your application to read secrets from Key Vault</span></span>

<span data-ttu-id="d8b3a-210">Запишите выходные данные при публикации приложения в Azure.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-210">Make a note of the output when you publish the application to Azure.</span></span> <span data-ttu-id="d8b3a-211">Они должны быть представлены в таком формате:</span><span class="sxs-lookup"><span data-stu-id="d8b3a-211">It should be of the format:</span></span>

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

<span data-ttu-id="d8b3a-212">Затем, используя имя своего хранилища ключей и значение **PrincipalId**, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d8b3a-212">Then, run this command by using the name of your key vault and the value of **PrincipalId**:</span></span>

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

<span data-ttu-id="d8b3a-213">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="d8b3a-213">::: zone pivot="nodejs"</span></span>
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a><span data-ttu-id="d8b3a-214">Развертывание приложения Node.js в Azure и получение значения секрета</span><span class="sxs-lookup"><span data-stu-id="d8b3a-214">Deploy the Node App to Azure and retrieve the secret value</span></span>

<span data-ttu-id="d8b3a-215">Теперь, когда все готово,</span><span class="sxs-lookup"><span data-stu-id="d8b3a-215">Now that everything is set.</span></span> <span data-ttu-id="d8b3a-216">выполните приведенную ниже команду, чтобы развернуть приложение в Azure.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-216">Run the following command to deploy the app to Azure</span></span>

```bash
git push azure master
```

<span data-ttu-id="d8b3a-217">После этого на странице https://<app_name>.azurewebsites.net вы сможете увидеть значение секрета.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-217">After this when you browse https://<app_name>.azurewebsites.net you can see the secret value.</span></span>
<span data-ttu-id="d8b3a-218">Убедитесь, что вы заменили имя <YourKeyVaultName> именем своего хранилища</span><span class="sxs-lookup"><span data-stu-id="d8b3a-218">Make sure that you replaced the name <YourKeyVaultName> with your vault name</span></span>

<span data-ttu-id="d8b3a-219">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="d8b3a-219">::: zone-end</span></span>

<span data-ttu-id="d8b3a-220">::: zone pivot="dotnet" Теперь при запуске приложения вы должны увидеть извлеченное значение секрета.</span><span class="sxs-lookup"><span data-stu-id="d8b3a-220">::: zone pivot="dotnet" Now when you run the application, you should see your secret value retrieved.</span></span>
<span data-ttu-id="d8b3a-221">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="d8b3a-221">::: zone-end</span></span>

## <a name="next-steps"></a><span data-ttu-id="d8b3a-222">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="d8b3a-222">Next steps</span></span>

<span data-ttu-id="d8b3a-223">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="d8b3a-223">::: zone pivot="nodejs"</span></span>
* [<span data-ttu-id="d8b3a-224">Домашняя страница Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="d8b3a-224">Azure Key Vault Home Page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="d8b3a-225">Документация Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="d8b3a-225">Azure Key Vault Documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="d8b3a-226">Пакет SDK Azure для Node.js</span><span class="sxs-lookup"><span data-stu-id="d8b3a-226">Azure SDK For Node</span></span>](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* <span data-ttu-id="d8b3a-227">[Справочник по REST API в Azure](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="d8b3a-227">[Azure REST API Reference](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span></span>

<span data-ttu-id="d8b3a-228">::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="d8b3a-228">::: zone pivot="dotnet"</span></span>
* [<span data-ttu-id="d8b3a-229">Домашняя страница Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="d8b3a-229">Azure Key Vault home page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="d8b3a-230">Документация Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="d8b3a-230">Azure Key Vault documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="d8b3a-231">Пакет SDK Azure для .NET</span><span class="sxs-lookup"><span data-stu-id="d8b3a-231">Azure SDK For .NET</span></span>](https://github.com/Azure/azure-sdk-for-net)
* <span data-ttu-id="d8b3a-232">[Справочник по REST API в Azure](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="d8b3a-232">[Azure REST API reference](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span></span>
