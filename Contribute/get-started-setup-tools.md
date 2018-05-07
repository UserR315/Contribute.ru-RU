---
title: Установка средств для создания содержимого
description: Эта статья поможет вам скачать и установить клиентские средства, необходимые для редактирования файлов Markdown и работы с Git.
author: jasonwhowell
ms.author: jasonh
manager: kfile
ms.date: 04/30/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 1011c3fc829202a3df134ddc80eb05b8959b7bf6
ms.sourcegitcommit: 7b668124f25b8ad0442937a3ad05b19a47af5970
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/03/2018
---
# <a name="install-content-authoring-tools"></a><span data-ttu-id="667d7-103">Установка средств для создания содержимого</span><span class="sxs-lookup"><span data-stu-id="667d7-103">Install content authoring tools</span></span>

<span data-ttu-id="667d7-104">В этой статье объясняется, как установить клиентские средства Git и Visual Studio Code в интерактивном режиме.</span><span class="sxs-lookup"><span data-stu-id="667d7-104">This article describes the steps to interactively install Git client tools and Visual Studio Code.</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="667d7-105">Установка [Git для Windows](https://git-scm.com/download/win).</span><span class="sxs-lookup"><span data-stu-id="667d7-105">Install [Git for Windows](https://git-scm.com/download/win)</span></span>
> * <span data-ttu-id="667d7-106">Установка [Visual Studio Code](https://code.visualstudio.com/).</span><span class="sxs-lookup"><span data-stu-id="667d7-106">Install [Visual Studio Code](https://code.visualstudio.com/)</span></span>
> * <span data-ttu-id="667d7-107">Установка [пакета создания документации](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span><span class="sxs-lookup"><span data-stu-id="667d7-107">Install [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)</span></span>

>[!IMPORTANT]
> <span data-ttu-id="667d7-108">Если вы вносите в статью лишь небольшие изменения, вам *не* нужно выполнять описанные здесь шаги. Вы можете сразу перейти к [рабочему процессу по внесению быстрых изменений](index.md#quick-edits-to-existing-documents).</span><span class="sxs-lookup"><span data-stu-id="667d7-108">If you're making only minor changes to an article, you *do not* need to complete the steps in this article and can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>
> <span data-ttu-id="667d7-109">Участникам, которые вносят много изменений, рекомендуется выполнить инструкции, которые позволят применить [рабочий процесс по внесению значительных или времязатратных изменений](how-to-write-workflows-major.md).</span><span class="sxs-lookup"><span data-stu-id="667d7-109">Major contributors are encouraged to complete these steps, which enable you to use the [major/long-running changes workflow](how-to-write-workflows-major.md).</span></span> <span data-ttu-id="667d7-110">Даже если у вас есть разрешения на запись в основном репозитории, *настоятельно рекомендуется (и в этом руководстве предполагается, что вы это сделаете) создать вилку и клон репозитория*, чтобы у вас были права на чтение и запись для хранения в этой вилке предлагаемых вами изменений.</span><span class="sxs-lookup"><span data-stu-id="667d7-110">Even if you have write permissions in the main repository, *we highly recommend (and this guide assumes) that you fork and clone the repository*, so that you have read/write permissions to store your proposed changes in your fork.</span></span>

## <a name="install-git-client-tools-on-windows"></a><span data-ttu-id="667d7-111">Установка клиентских средств Git в Windows</span><span class="sxs-lookup"><span data-stu-id="667d7-111">Install Git client tools on Windows</span></span>

 <span data-ttu-id="667d7-112">Установите последние версии [клиентских средств Git от Software Freedom Conservancy](https://git-scm.com/download/).</span><span class="sxs-lookup"><span data-stu-id="667d7-112">Install the latest version of [Software Freedom Conservancy's Git client tools](https://git-scm.com/download/).</span></span> <span data-ttu-id="667d7-113">Пакет установки включает систему управления версиями Git и приложение командной строки Git Bash, используемое для взаимодействия с локальным репозиторием Git.</span><span class="sxs-lookup"><span data-stu-id="667d7-113">The install includes the Git version control system and Git Bash, the command-line app that you use to interact with your local Git repository.</span></span>

<span data-ttu-id="667d7-114">Если вы предпочитаете использовать графический пользовательский интерфейс вместо интерфейса командной строки, см. сведения о часто используемых параметрах на странице [доступных средств графического пользовательского интерфейса Software Freedom Conservancy](https://git-scm.com/downloads/guis), на сайте [версии GitHub для настольного компьютера](https://desktop.github.com/) или на сайте [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx).</span><span class="sxs-lookup"><span data-stu-id="667d7-114">If you prefer a graphical user interface (GUI) over a command-line interface (CLI), see [Software Freedom Conservancy's available GUI Clients page](https://git-scm.com/downloads/guis), [GitHub's GitHub Desktop](https://desktop.github.com/), or [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) for some popular options.</span></span>

<span data-ttu-id="667d7-115">Следуйте инструкциям по установке и настройке для выбранного клиента.</span><span class="sxs-lookup"><span data-stu-id="667d7-115">Follow the instructions for your chosen client for installation and configuration.</span></span>

<span data-ttu-id="667d7-116">В следующей статье вы [настроите локальный репозиторий Git](get-started-setup-local.md).</span><span class="sxs-lookup"><span data-stu-id="667d7-116">In the next article, you will [Set up a local Git repository](get-started-setup-local.md).</span></span>

   <span data-ttu-id="667d7-117">Дополнительные ресурсы по Git см. здесь: [Глоссарий GitHub ](https://help.github.com/articles/github-glossary) | [Базовые возможности Git](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Обучающие ресурсы по Git и GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/).</span><span class="sxs-lookup"><span data-stu-id="667d7-117">Additional Git resources are available here: [Git terminology](https://help.github.com/articles/github-glossary) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span></span>

## <a name="understand-markdown-editors"></a><span data-ttu-id="667d7-118">Сведения о редакторах Markdown</span><span class="sxs-lookup"><span data-stu-id="667d7-118">Understand Markdown editors</span></span>

<span data-ttu-id="667d7-119">Markdown — это упрощенный язык разметки, который легко использовать и осваивать.</span><span class="sxs-lookup"><span data-stu-id="667d7-119">Markdown is a lightweight markup language that is both easy to read and easy to learn.</span></span> <span data-ttu-id="667d7-120">Поэтому он быстро стал отраслевым стандартом.</span><span class="sxs-lookup"><span data-stu-id="667d7-120">Therefore, it has rapidly become an industry standard.</span></span> <span data-ttu-id="667d7-121">Чтобы писать статьи на языке Markdown, мы рекомендуем скачать и установить Markdown editor.</span><span class="sxs-lookup"><span data-stu-id="667d7-121">To write articles in Markdown, we recommend that you first download and install a Markdown editor.</span></span>  <span data-ttu-id="667d7-122">[Visual Studio Code](https://code.visualstudio.com/) — предпочтительное средство для редактирования разметки Markdown в Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="667d7-122">[Visual Studio Code](https://code.visualstudio.com/) is the preferred tool for editing Markdown at Microsoft.</span></span> <span data-ttu-id="667d7-123">[Atom](https://atom.io) — еще одно популярное средство для редактирования разметки Markdown.</span><span class="sxs-lookup"><span data-stu-id="667d7-123">[Atom](https://atom.io) is another popular tool for editing Markdown.</span></span>

<span data-ttu-id="667d7-124">Тексты с разметкой Markdown сохраняются в файлы с расширением MD.</span><span class="sxs-lookup"><span data-stu-id="667d7-124">Markdown text is saved into files with .md extension.</span></span>

<span data-ttu-id="667d7-125">Дополнительные сведения о написании кода на языке Markdown, включая основные сведения о Markdown и функциях, которые поддерживаются настраиваемыми расширениями OPS для Markdown, см. в статье об [использовании Markdown](how-to-write-use-markdown.md).</span><span class="sxs-lookup"><span data-stu-id="667d7-125">Additional details on how to write with Markdown, including Markdown basics and the features supported by OPS custom Markdown extensions, are covered later in the [How to use Markdown](how-to-write-use-markdown.md) article.</span></span>

## <a name="visual-studio-code"></a><span data-ttu-id="667d7-126">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="667d7-126">Visual Studio Code</span></span>

<span data-ttu-id="667d7-127">[Visual Studio Code](https://code.visualstudio.com/) (также называется VS Code) — это простой редактор, который работает в Windows, Linux и Mac.</span><span class="sxs-lookup"><span data-stu-id="667d7-127">[Visual Studio Code](https://code.visualstudio.com/), also known as VS Code, is a lightweight editor that works on Windows, Linux, and Mac.</span></span> <span data-ttu-id="667d7-128">Он включает интеграцию с Git и поддержку расширений.</span><span class="sxs-lookup"><span data-stu-id="667d7-128">It includes git integration, and support for extensions.</span></span>

<span data-ttu-id="667d7-129">Скачайте и установите [VS Code](https://code.visualstudio.com/).</span><span class="sxs-lookup"><span data-stu-id="667d7-129">Download and install [VS Code](https://code.visualstudio.com/).</span></span> <span data-ttu-id="667d7-130">На главной странице VS Code должна правильно определиться ваша операционная система:</span><span class="sxs-lookup"><span data-stu-id="667d7-130">The VS Code home page should detect your operating system correctly.</span></span>

- <span data-ttu-id="667d7-131">[Windows](https://code.visualstudio.com/docs/setup/windows);</span><span class="sxs-lookup"><span data-stu-id="667d7-131">[Windows](https://code.visualstudio.com/docs/setup/windows)</span></span>
- <span data-ttu-id="667d7-132">[Mac](https://code.visualstudio.com/docs/setup/mac);</span><span class="sxs-lookup"><span data-stu-id="667d7-132">[Mac](https://code.visualstudio.com/docs/setup/mac)</span></span>
- <span data-ttu-id="667d7-133">[Linux](https://code.visualstudio.com/docs/setup/linux).</span><span class="sxs-lookup"><span data-stu-id="667d7-133">[Linux](https://code.visualstudio.com/docs/setup/linux)</span></span>

> [!TIP]
> <span data-ttu-id="667d7-134">Чтобы запустить VS Code и открыть текущую папку, выполните команду `code .` в командной строке или оболочке Bash.</span><span class="sxs-lookup"><span data-stu-id="667d7-134">To launch VS Code and open the current folder, run the command `code .` in the command line or bash shell.</span></span> <span data-ttu-id="667d7-135">Если текущая папка содержится в локальном репозитории Git, в Visual Studio Code автоматически отобразятся данные об интеграции с GitHub.</span><span class="sxs-lookup"><span data-stu-id="667d7-135">If the current folder is part of a local git repo, the github integration appears in Visual Studio Code automatically.</span></span>

## <a name="docs-authoring-pack"></a><span data-ttu-id="667d7-136">Пакет создания документации</span><span class="sxs-lookup"><span data-stu-id="667d7-136">Docs Authoring Pack</span></span>
<span data-ttu-id="667d7-137">Установка пакета создания документации для Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="667d7-137">Install the Docs Authoring Pack for Visual Studio Code.</span></span> <span data-ttu-id="667d7-138">Этот набор исключений включает базовые рекомендации по использованию справки при написании с помощью Markdown и функцию предварительного просмотра. Это позволяет просматривать стиль текстов Markdown на сайте docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="667d7-138">This set of extensions includes basic authoring assistance for help when writing Markdown, and a preview feature, so that you can see what the Markdown looks like in the style of the docs.microsoft.com site.</span></span>

   <span data-ttu-id="667d7-139">На этой [странице Marketplace](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) выберите **Установить** или найдите `docsmsft.docs-authoring-pack` в списке расширений в окне VS Code.</span><span class="sxs-lookup"><span data-stu-id="667d7-139">Visit this [marketplace page](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) and select **Install**, or search for `docsmsft.docs-authoring-pack` in your extensions list in the VS Code window.</span></span> 

   <span data-ttu-id="667d7-140">Пакет создания документации можно открыть с помощь.клавиш ALT+M за пределами VS Code.</span><span class="sxs-lookup"><span data-stu-id="667d7-140">The Docs Authoring Pack is accessible by pressing Alt+M inside of VS Code.</span></span> <span data-ttu-id="667d7-141">Панель инструментов по умолчанию спрятана, но ее можно отобразить.</span><span class="sxs-lookup"><span data-stu-id="667d7-141">The toolbar is hidden by default but can be shown.</span></span> <span data-ttu-id="667d7-142">Измените параметры VS Code (CTRL+запятая) и добавьте пользовательский параметр `"markdown.showToolbar": true` для отображения панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="667d7-142">Edit the VS Code settings (Control+comma) and adding user setting `"markdown.showToolbar": true` to show the toolbar.</span></span>

   <span data-ttu-id="667d7-143">Дополнительные сведения см. на [странице справки по пакету создания документации](how-to-write-docs-auth-pack.md).</span><span class="sxs-lookup"><span data-stu-id="667d7-143">For more information, see the [Docs Authoring Pack](how-to-write-docs-auth-pack.md) page.</span></span>


## <a name="next-steps"></a><span data-ttu-id="667d7-144">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="667d7-144">Next steps</span></span>

<span data-ttu-id="667d7-145">Теперь все готово к [настройке локального репозитория](get-started-setup-local.md).</span><span class="sxs-lookup"><span data-stu-id="667d7-145">Now you are ready to [Set up a local Git repository](get-started-setup-local.md).</span></span>
