---
title: Локальная настройка репозитория Git
description: В этой статье приводятся инструкции по созданию локального репозитория Git, включая создание вилки и клонирование, для участия в разработке документации.
author: jasonwhowell
ms.author: jasonh
ms.date: 01/18/2018
ms.openlocfilehash: 285c25fe0e5df067ceeaa5a42da1bad5533d2c84
ms.sourcegitcommit: 7e73bef8bcdca39fd54cd79fbe8cb22da5566411
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/24/2019
ms.locfileid: "71247388"
---
# <a name="set-up-git-repository-locally-for-documentation"></a><span data-ttu-id="8965f-103">Локальная настройка репозитория Git для документации</span><span class="sxs-lookup"><span data-stu-id="8965f-103">Set up Git repository locally for documentation</span></span>

<span data-ttu-id="8965f-104">В этой статье описаны действия по настройке репозитория Git на локальном компьютере для разработки документации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="8965f-104">This article describes the steps to set up a git repository on your local machine, with the intent to contribute to Microsoft documentation.</span></span> <span data-ttu-id="8965f-105">Добавлять новые статьи, вносить значительные правки в существующие и изменять графическое оформление можно при помощи локально клонированного репозитория.</span><span class="sxs-lookup"><span data-stu-id="8965f-105">Contributors may use a locally cloned repository to add new articles, do major edits on existing articles, or change artwork.</span></span>

<span data-ttu-id="8965f-106">Чтобы приступить к работе с документацией, необходимо однократно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="8965f-106">You run these one-time setup activities to start contributing:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="8965f-107">определить соответствующий репозиторий;</span><span class="sxs-lookup"><span data-stu-id="8965f-107">Determine the appropriate repository</span></span>
> * <span data-ttu-id="8965f-108">создать вилку репозитория Git в учетной записи GitHub;</span><span class="sxs-lookup"><span data-stu-id="8965f-108">Fork the repository to your GitHub account</span></span>
> * <span data-ttu-id="8965f-109">выбрать локальную папку для клонированных файлов;</span><span class="sxs-lookup"><span data-stu-id="8965f-109">Choose a local folder for the cloned files</span></span>
> * <span data-ttu-id="8965f-110">клонировать репозиторий на локальный компьютер;</span><span class="sxs-lookup"><span data-stu-id="8965f-110">Clone the repository to your local machine</span></span>
> * <span data-ttu-id="8965f-111">настроить значение вышестоящего удаленного источника.</span><span class="sxs-lookup"><span data-stu-id="8965f-111">Configure the upstream remote value</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8965f-112">Если вы вносите в статью лишь небольшие изменения, вам *не* нужно выполнять описанные здесь шаги.</span><span class="sxs-lookup"><span data-stu-id="8965f-112">If you're making only minor changes to an article, you *do not* need to complete the steps in this article.</span></span> <span data-ttu-id="8965f-113">Вы можете перейти непосредственно к [рабочему процессу по внесению быстрых изменений](index.md#quick-edits-to-existing-documents).</span><span class="sxs-lookup"><span data-stu-id="8965f-113">You can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>

## <a name="overview"></a><span data-ttu-id="8965f-114">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="8965f-114">Overview</span></span>

<span data-ttu-id="8965f-115">Для участия в разработке документации на сайте Майкрософт вы можете локально создавать и редактировать файлы Markdown, клонировав соответствующий репозиторий документации.</span><span class="sxs-lookup"><span data-stu-id="8965f-115">To contribute to Microsoft's documentation site, you can make and edit Markdown files locally by cloning the corresponding documentation repository.</span></span> <span data-ttu-id="8965f-116">Чтобы получить разрешения Майкрософт на чтение и запись для соответствующего репозитория, нужно создать его вилку в учетной записи GitHub. Это позволит сохранять предлагаемые изменения.</span><span class="sxs-lookup"><span data-stu-id="8965f-116">Microsoft requires you to fork the appropriate repository into your own GitHub account so that you have read/write permissions there to store your proposed changes.</span></span> <span data-ttu-id="8965f-117">Затем изменения объединяются в центральном общем репозитории, доступном только для чтения, с помощью запросов на вытягивание.</span><span class="sxs-lookup"><span data-stu-id="8965f-117">Then you use pull requests to merge changes into the read-only central shared repository.</span></span>

![Треугольник GitHub](./media/git-and-github-initial-setup.png)

<span data-ttu-id="8965f-119">Если вы не работали с GitHub, просмотрите приведенное ниже видео, описывающее, как создать вилку и клон репозитория:</span><span class="sxs-lookup"><span data-stu-id="8965f-119">If you're new to GitHub, watch the following video for a conceptual overview of the forking and cloning process:</span></span>

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]

## <a name="determine-the-repository"></a><span data-ttu-id="8965f-120">Определение репозитория</span><span class="sxs-lookup"><span data-stu-id="8965f-120">Determine the repository</span></span>

<span data-ttu-id="8965f-121">Документация, размещенная на сайте [docs.microsoft.com](https://docs.microsoft.com), находится в нескольких разных репозиториях на [github.com](https://www.github.com).</span><span class="sxs-lookup"><span data-stu-id="8965f-121">Documentation hosted at [docs.microsoft.com](https://docs.microsoft.com) resides in several different repositories at [github.com](https://www.github.com).</span></span>

1. <span data-ttu-id="8965f-122">Если вы точно не знаете, какой репозиторий использовать, откройте статью на сайте [docs.microsoft.com](https://docs.microsoft.com) в своем веб-браузере.</span><span class="sxs-lookup"><span data-stu-id="8965f-122">If you are unsure of which repository to use, then visit the article on [docs.microsoft.com](https://docs.microsoft.com) using your web browser.</span></span> <span data-ttu-id="8965f-123">Справа над статьей выберите ссылку **Правка** (значок карандаша).</span><span class="sxs-lookup"><span data-stu-id="8965f-123">Select the **Edit** link (pencil icon) on the upper right of the article.</span></span>

   ![Щелкните "Правка", чтобы определить расположение репозитория и файлов.](media/index/edit-article.png)

2. <span data-ttu-id="8965f-125">По этой ссылке вы перейдете к расположению нужного файла Markdown в соответствующем репозитории на сайте github.com.</span><span class="sxs-lookup"><span data-stu-id="8965f-125">That link takes you to github.com location for the corresponding Markdown file in the appropriate repository.</span></span> <span data-ttu-id="8965f-126">Запишите URL-адрес, чтобы узнать имя репозитория.</span><span class="sxs-lookup"><span data-stu-id="8965f-126">Note the URL to view the repository name.</span></span>

   ![URL-адрес, по которому можно определить расположение репозитория](media/public-repo.png)

   <span data-ttu-id="8965f-128">Например, для участия в создании документации можно использовать следующие популярные репозитории:</span><span class="sxs-lookup"><span data-stu-id="8965f-128">For example, these popular repositories are available for public contributions:</span></span>
   - <span data-ttu-id="8965f-129">Документация по Azure [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)</span><span class="sxs-lookup"><span data-stu-id="8965f-129">Azure documentation [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)</span></span>
   - <span data-ttu-id="8965f-130">Документация по SQL Server [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)</span><span class="sxs-lookup"><span data-stu-id="8965f-130">SQL Server documentation [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)</span></span>
   - <span data-ttu-id="8965f-131">Документация по Visual Studio [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)</span><span class="sxs-lookup"><span data-stu-id="8965f-131">Visual Studio documentation [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)</span></span>
   - <span data-ttu-id="8965f-132">Документация по .NET [https://github.com/dotnet/docs](https://github.com/dotnet/docs)</span><span class="sxs-lookup"><span data-stu-id="8965f-132">.NET Documentation [https://github.com/dotnet/docs](https://github.com/dotnet/docs)</span></span>
   - <span data-ttu-id="8965f-133">Документация к пакету Azure SDK для .NET [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)</span><span class="sxs-lookup"><span data-stu-id="8965f-133">Azure .Net SDK documentation [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)</span></span>
   - <span data-ttu-id="8965f-134">Документация по Configuration Manager [https://github.com/MicrosoftDocs/SCCMdocs](https://github.com/MicrosoftDocs/SCCMdocs/)</span><span class="sxs-lookup"><span data-stu-id="8965f-134">ConfigMgr documentation [https://github.com/MicrosoftDocs/SCCMdocs](https://github.com/MicrosoftDocs/SCCMdocs/)</span></span>

## <a name="fork-the-repository"></a><span data-ttu-id="8965f-135">Создание вилки репозитория</span><span class="sxs-lookup"><span data-stu-id="8965f-135">Fork the repository</span></span>
<span data-ttu-id="8965f-136">Используя соответствующий репозиторий, создайте его вилку в своей учетной записи GitHub на сайте GitHub.</span><span class="sxs-lookup"><span data-stu-id="8965f-136">Using the appropriate repository, create a fork of the repository into your own GitHub account by using the GitHub website.</span></span>

<span data-ttu-id="8965f-137">Персональная вилка необходима, поскольку все основные репозитории документации предоставляют доступ только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8965f-137">A personal fork is required since all main documentation repositories provide read-only access.</span></span> <span data-ttu-id="8965f-138">Чтобы внести изменение, вам нужно отправить из вилки в основной репозиторий [запрос на вытягивание](git-github-fundamentals.md#pull-requests).</span><span class="sxs-lookup"><span data-stu-id="8965f-138">To make changes, you must submit a [pull request](git-github-fundamentals.md#pull-requests) from your fork into the main repository.</span></span> <span data-ttu-id="8965f-139">Чтобы ускорить этот процесс, сначала следует создать копию репозитория с доступом на запись.</span><span class="sxs-lookup"><span data-stu-id="8965f-139">To facilitate this process, you first need your own copy of the repository, in which you have write access.</span></span> <span data-ttu-id="8965f-140">Для этого служит *вилка* GitHub.</span><span class="sxs-lookup"><span data-stu-id="8965f-140">A GitHub *fork* serves that purpose.</span></span>

1. <span data-ttu-id="8965f-141">Перейдите на страницу GitHub основного репозитория, а затем нажмите кнопку **Fork** (Создать вилку) справа вверху.</span><span class="sxs-lookup"><span data-stu-id="8965f-141">Go to the main repository's GitHub page and click the **Fork** button on the upper right.</span></span>

   ![Пример профиля GitHub](./media/contribute-get-started-setup-local/fork.png)

2. <span data-ttu-id="8965f-143">Если будет предложено, выберите плитку своей учетной записи GitHub в качестве расположения для создаваемой вилки.</span><span class="sxs-lookup"><span data-stu-id="8965f-143">If you are prompted, select your GitHub account tile as the destination where the fork should be created.</span></span> <span data-ttu-id="8965f-144">После этого в вашей учетной записи GitHub будет создана копия репозитория, называемая вилкой.</span><span class="sxs-lookup"><span data-stu-id="8965f-144">This prompt creates a copy of the repository within your GitHub account, known as a fork.</span></span>

## <a name="choose-a-local-folder"></a><span data-ttu-id="8965f-145">Выбор локальной папки</span><span class="sxs-lookup"><span data-stu-id="8965f-145">Choose a local folder</span></span>
<span data-ttu-id="8965f-146">Создайте локальную папку для локального хранения копии репозитория.</span><span class="sxs-lookup"><span data-stu-id="8965f-146">Make a local folder to hold a copy of the repository locally.</span></span> <span data-ttu-id="8965f-147">Размер некоторых репозиториев может быть значительным, например до 5 ГБ для azure-docs.</span><span class="sxs-lookup"><span data-stu-id="8965f-147">Some of the repositories can be large; up to 5 GB for azure-docs for example.</span></span> <span data-ttu-id="8965f-148">Выберите расположение с доступным местом на диске.</span><span class="sxs-lookup"><span data-stu-id="8965f-148">Choose a location with available disk space.</span></span>

1. <span data-ttu-id="8965f-149">Выберите имя папки — оно должно быть простым для запоминания и ввода.</span><span class="sxs-lookup"><span data-stu-id="8965f-149">Choose a folder name should be easy for you to remember and type.</span></span> <span data-ttu-id="8965f-150">Например, можно использовать корневую папку `C:\docs\` или создать папку в каталоге профиля пользователя `~/Documents/docs/`</span><span class="sxs-lookup"><span data-stu-id="8965f-150">For example, consider a root folder `C:\docs\` or make a folder in your user profile directory `~/Documents/docs/`</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="8965f-151">Не следует выбирать путь к локальной папке, вложенной в другую папку репозитория Git.</span><span class="sxs-lookup"><span data-stu-id="8965f-151">Avoid choosing a local folder path that is nested inside of another git repository folder location.</span></span> <span data-ttu-id="8965f-152">Несмотря на то что, что клонированные папки Git можно хранить рядом друг с другом, вложение папок Git приводит к ошибкам отслеживания файлов.</span><span class="sxs-lookup"><span data-stu-id="8965f-152">While it is acceptable to store the git cloned folders adjacent to each other, nesting git folders inside one another causes errors for the file tracking.</span></span>

2. <span data-ttu-id="8965f-153">Запустите Git Bash</span><span class="sxs-lookup"><span data-stu-id="8965f-153">Launch Git Bash</span></span>

   ![Запустите Git Bash](./media/contribute-get-started-setup-local/gitbash-start.png)

   <span data-ttu-id="8965f-155">Расположением по умолчанию, в котором обычно запускается Git Bash, является домашний каталог (~) или `/c/users/<Windows-user-account>/` в ОС Windows.</span><span class="sxs-lookup"><span data-stu-id="8965f-155">The default location that Git Bash starts in is typically the home directory (~) or `/c/users/<Windows-user-account>/` on Windows OS.</span></span>

   <span data-ttu-id="8965f-156">Чтобы определить текущий каталог, ведите `pwd` в запросе $.</span><span class="sxs-lookup"><span data-stu-id="8965f-156">To determine the current directory, type `pwd` at the $ prompt.</span></span> 

3. <span data-ttu-id="8965f-157">Преобразуйте каталог (cd) в папку, созданную для локального размещения репозитория.</span><span class="sxs-lookup"><span data-stu-id="8965f-157">Change directory (cd) into the folder that you created for hosting the repository locally.</span></span> <span data-ttu-id="8965f-158">Обратите внимание, что Git Bash поддерживает соглашение Linux по использованию в путях к папкам прямых, а не обратных косых черт.</span><span class="sxs-lookup"><span data-stu-id="8965f-158">Note that Git Bash uses the Linux convention of forward-slashes instead of back-slashes for folder paths.</span></span>

   <span data-ttu-id="8965f-159">Например, `cd /c/docs/ ` или `cd ~/Documents/docs/`.</span><span class="sxs-lookup"><span data-stu-id="8965f-159">For example, `cd /c/docs/ ` or `cd ~/Documents/docs/`</span></span>

## <a name="create-a-local-clone"></a><span data-ttu-id="8965f-160">Создание локального клона</span><span class="sxs-lookup"><span data-stu-id="8965f-160">Create a local clone</span></span>

<span data-ttu-id="8965f-161">С помощью Git Bash подготовьтесь выполнить команду **клонирования** для вытягивания копии репозитории (вашей вилки) в текущий каталог на устройстве.</span><span class="sxs-lookup"><span data-stu-id="8965f-161">Using Git Bash, prepare to run the **clone** command to pull a copy of a repository (your fork) down to your device on the current directory.</span></span> 

### <a name="authenticate-by-using-git-credential-manager"></a><span data-ttu-id="8965f-162">Проверка подлинности с использованием Git Credential Manager</span><span class="sxs-lookup"><span data-stu-id="8965f-162">Authenticate by using Git Credential Manager</span></span>
<span data-ttu-id="8965f-163">Если вы установили последнюю версию Git для Windows, выполнив стандартную процедуру, Git Credential Manager будет включен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8965f-163">If you installed the latest version of Git for Windows and accepted the default installation, Git Credential Manager is enabled by default.</span></span> <span data-ttu-id="8965f-164">Git Credential Manager упрощает проверку подлинности, избавляя от необходимости отзывать личный маркер доступа при повторной установке подключений с проверкой подлинности и удаленных подключений с GitHub.</span><span class="sxs-lookup"><span data-stu-id="8965f-164">Git Credential Manager makes authentication much easier because you don't need to recall your personal access token when re-establishing authenticated connections and remotes with GitHub.</span></span>

1. <span data-ttu-id="8965f-165">Выполните команду **клонирования**, указав имя репозитория.</span><span class="sxs-lookup"><span data-stu-id="8965f-165">Run the **clone** command, by providing the repository name.</span></span> <span data-ttu-id="8965f-166">Во время клонирования разветвленный репозиторий скачивается (клонируется) на локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="8965f-166">Cloning downloads (clone) the forked repository on your local computer.</span></span> 

    > [!Tip]
    > <span data-ttu-id="8965f-167">URL-адрес вилки GitHub для команды клонирования можно получить, нажав кнопку **Clone or download** (Клонировать или скачать) в пользовательском интерфейсе GitHub.</span><span class="sxs-lookup"><span data-stu-id="8965f-167">You can get your fork's GitHub URL for the clone command from the **Clone or download** button in the GitHub UI:</span></span>
    >
    > !["Clone or download" (Клонировать или скачать)](./media/contribute-get-started-setup-local/clone-or-download.png)

    <span data-ttu-id="8965f-169">Во время клонирования обязательно укажите путь к *вашей вилке*, а не к основному репозиторию, из которого она была создана.</span><span class="sxs-lookup"><span data-stu-id="8965f-169">Be sure to specify the path to *your fork* during the cloning process, not the main repository from which you created the fork.</span></span> <span data-ttu-id="8965f-170">В противном случае вы не сможете вносить изменения.</span><span class="sxs-lookup"><span data-stu-id="8965f-170">Otherwise, you cannot contribute changes.</span></span> <span data-ttu-id="8965f-171">Ссылки на вашу вилку осуществляются по имени вашей личной учетной записи GitHub, например `github.com/<github-username>/<repo>`.</span><span class="sxs-lookup"><span data-stu-id="8965f-171">Your fork is referenced through your personal GitHub user account, such as `github.com/<github-username>/<repo>`.</span></span>

    ```bash
    git clone https://github.com/<github-username>/<repo>.git
    ```

    <span data-ttu-id="8965f-172">Команда клонирования должна выглядеть приблизительно следующим образом.</span><span class="sxs-lookup"><span data-stu-id="8965f-172">Your clone command should look similar to this example:</span></span>

    ```bash
    git clone https://github.com/smithj/azure-docs.git
    ```

2. <span data-ttu-id="8965f-173">При появлении запроса введите учетные данные GitHub.</span><span class="sxs-lookup"><span data-stu-id="8965f-173">When you're prompted, enter your GitHub credentials.</span></span>

    ![GitHub: вход в систему](./media/contribute-get-started-setup-local/github-login.png)

3. <span data-ttu-id="8965f-175">При появлении запроса введите код двухфакторной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="8965f-175">When you're prompted, enter your two-factor authentication code.</span></span>

    ![GitHub: двухфакторная проверка подлинности](./media/contribute-get-started-setup-local/github-2fa.png)

    > [!Note]
    > <span data-ttu-id="8965f-177">Ваши учетные данные будут сохранены для проверки подлинности последующих запросов GitHub.</span><span class="sxs-lookup"><span data-stu-id="8965f-177">Your credentials will be saved and used to authenticate future GitHub requests.</span></span> <span data-ttu-id="8965f-178">Проверка подлинности выполняется на каждом компьютере один раз.</span><span class="sxs-lookup"><span data-stu-id="8965f-178">You only need to do this authentication once per computer.</span></span> 

4. <span data-ttu-id="8965f-179">Запущенная команда клонирования скачивает копию файлов репозитория из вашей вилки в новую папку на локальном диске.</span><span class="sxs-lookup"><span data-stu-id="8965f-179">The clone command runs and downloads a copy of the repository files from your fork into a new folder on the local disk.</span></span> <span data-ttu-id="8965f-180">Новая папка создается в текущей папке.</span><span class="sxs-lookup"><span data-stu-id="8965f-180">A new folder is made within the current folder.</span></span> <span data-ttu-id="8965f-181">В зависимости от размера репозитория этот процесс может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="8965f-181">It may take a few minutes, depending on the repository size.</span></span> <span data-ttu-id="8965f-182">По его окончании вы можете открыть папку, чтобы просмотреть ее структуру.</span><span class="sxs-lookup"><span data-stu-id="8965f-182">You can explore the folder to see the structure once it is finished.</span></span>

## <a name="configure-remote-upstream"></a><span data-ttu-id="8965f-183">Настройка удаленного вышестоящего подключения</span><span class="sxs-lookup"><span data-stu-id="8965f-183">Configure remote upstream</span></span>
<span data-ttu-id="8965f-184">После клонирования репозитория следует установить удаленное подключение только для чтения, называемое **вышестоящим**, к основному репозиторию.</span><span class="sxs-lookup"><span data-stu-id="8965f-184">After cloning the repository, set up a read-only remote connection to the main repository named **upstream**.</span></span> <span data-ttu-id="8965f-185">С помощью URL-адреса вышестоящего подключения вы сможете обеспечить синхронизацию вашего локального репозитория с последними правками, внесенными другими участниками.</span><span class="sxs-lookup"><span data-stu-id="8965f-185">You use the upstream URL to keep your local repository in sync with the latest changes made by others.</span></span> <span data-ttu-id="8965f-186">Команда **git remote** служит для задания значения конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8965f-186">The **git remote** command is used to set the configuration value.</span></span> <span data-ttu-id="8965f-187">С помощью команды **принесения** можно обновить сведения о ветви из вышестоящего репозитория.</span><span class="sxs-lookup"><span data-stu-id="8965f-187">You use the **fetch** command to refresh the branch info from the upstream repository.</span></span>

1. <span data-ttu-id="8965f-188">Если вы используете **Git Credential Manager**, выполните следующие команды.</span><span class="sxs-lookup"><span data-stu-id="8965f-188">If you're using **Git Credential Manager**, use the following commands.</span></span> <span data-ttu-id="8965f-189">Замените заполнители \<repo\> и \<organization\>.</span><span class="sxs-lookup"><span data-stu-id="8965f-189">Replace the \<repo\> and \<organization\> placeholders.</span></span>
   ```bash
   cd <repo>
   git remote add upstream https://github.com/<organization>/<repo>.git
   git fetch upstream
   ```

2. <span data-ttu-id="8965f-190">Просмотрите настроенные значения и проверьте правильность URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="8965f-190">View the configured values and confirm the URLs are correct.</span></span> <span data-ttu-id="8965f-191">Убедитесь, что URL-адреса **исходного подключения** ведут к вашей персональной вилке.</span><span class="sxs-lookup"><span data-stu-id="8965f-191">Ensure the **origin** URLs point to your personal fork.</span></span> <span data-ttu-id="8965f-192">Убедитесь, что URL-адреса **вышестоящего подключения** ведут к основному репозиторию, например MicrosoftDocs или Azure.</span><span class="sxs-lookup"><span data-stu-id="8965f-192">Ensure the **upstream** URLs point to the main repository, such as MicrosoftDocs or Azure.</span></span> 
   ```bash
   git remote -v 
   ```

   <span data-ttu-id="8965f-193">Далее приводится пример выходных данных для подключения к удаленному репозиторию.</span><span class="sxs-lookup"><span data-stu-id="8965f-193">Example remote output is shown.</span></span> <span data-ttu-id="8965f-194">Здесь вымышленная учетная запись Git с именем MyGitAccount настраивается с личным маркером доступа для обращения к репозиторию azure-docs.</span><span class="sxs-lookup"><span data-stu-id="8965f-194">A fictitious git account named MyGitAccount is configured with a personal access token to access the repo azure-docs:</span></span>
   ```output
   origin  https://github.com/MyGitAccount/azure-docs.git (fetch)
   origin  https://github.com/MyGitAccount/azure-docs.git(push)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (fetch)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (push)
   ```

3. <span data-ttu-id="8965f-195">Если вы допустили ошибку, значение удаленного подключения можно очистить.</span><span class="sxs-lookup"><span data-stu-id="8965f-195">If you made a mistake, you can remove the remote value.</span></span> <span data-ttu-id="8965f-196">Чтобы удалить значение вышестоящего подключения, выполните команду `git remote remove upstream`.</span><span class="sxs-lookup"><span data-stu-id="8965f-196">To remove the upstream value, run the command `git remote remove upstream`.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8965f-197">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="8965f-197">Next steps</span></span>
- <span data-ttu-id="8965f-198">Дополнительные сведения о добавлении и обновлении содержимого см. на странице с описанием [рабочих процессов для участников GitHub](how-to-write-workflows-major.md).</span><span class="sxs-lookup"><span data-stu-id="8965f-198">To learn more about adding and updating content, continue to the [GitHub contribution workflow](how-to-write-workflows-major.md).</span></span>
