---
title: Установка средств для создания содержимого
description: Эта статья поможет вам скачать и установить клиентские средства, необходимые для редактирования файлов Markdown и работы с Git.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 01/04/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 0ca942e557640db1ba36d3f5b1064656ed3dea8d
ms.sourcegitcommit: 3ec397fab57ea582edb03a59609f62d886410ee8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2018
---
# <a name="install-content-authoring-tools"></a><span data-ttu-id="a8c3e-103">Установка средств для создания содержимого</span><span class="sxs-lookup"><span data-stu-id="a8c3e-103">Install content authoring tools</span></span>

<span data-ttu-id="a8c3e-104">В этой статье объясняется, как установить клиентские средства Git и Visual Studio Code в интерактивном режиме.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-104">This article describes the steps to interactively install Git client tools and Visual Studio Code.</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="a8c3e-105">Установка [Git для Windows](https://git-scm.com/download/win).</span><span class="sxs-lookup"><span data-stu-id="a8c3e-105">Install [Git for Windows](https://git-scm.com/download/win)</span></span>
> * <span data-ttu-id="a8c3e-106">Установка [Visual Studio Code](https://code.visualstudio.com/).</span><span class="sxs-lookup"><span data-stu-id="a8c3e-106">Install [Visual Studio Code](https://code.visualstudio.com/)</span></span>

>[!IMPORTANT]
> <span data-ttu-id="a8c3e-107">Если вы вносите в статью лишь небольшие изменения, вам *не* нужно выполнять описанные здесь шаги. Вы можете сразу перейти к [рабочему процессу по внесению быстрых изменений](index.md#quick-edits-to-existing-documents).</span><span class="sxs-lookup"><span data-stu-id="a8c3e-107">If you're making only minor changes to an article, you *do not* need to complete the steps in this article and can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>
> <span data-ttu-id="a8c3e-108">Участникам, которые вносят много изменений, рекомендуется выполнить инструкции, которые позволят применить [рабочий процесс по внесению значительных или времязатратных изменений](how-to-write-workflows-major.md).</span><span class="sxs-lookup"><span data-stu-id="a8c3e-108">Major contributors are encouraged to complete these steps, which enable you to use the [major/long-running changes workflow](how-to-write-workflows-major.md).</span></span> <span data-ttu-id="a8c3e-109">Даже если у вас есть разрешения на запись в основном репозитории, *настоятельно рекомендуется (и в этом руководстве предполагается, что вы это сделаете) создать вилку и клон репозитория*, чтобы у вас были права на чтение и запись для хранения в этой вилке предлагаемых вами изменений.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-109">Even if you have write permissions in the main repository, *we highly recommend (and this guide assumes) that you fork and clone the repository*, so that you have read/write permissions to store your proposed changes in your fork.</span></span>

## <a name="install-git-client-tools-on-windows"></a><span data-ttu-id="a8c3e-110">Установка клиентских средств Git в Windows</span><span class="sxs-lookup"><span data-stu-id="a8c3e-110">Install Git client tools on Windows</span></span>

 <span data-ttu-id="a8c3e-111">Установите последние версии [клиентских средств Git от Software Freedom Conservancy](https://git-scm.com/download/).</span><span class="sxs-lookup"><span data-stu-id="a8c3e-111">Install the latest version of [Software Freedom Conservancy's Git client tools](https://git-scm.com/download/).</span></span> <span data-ttu-id="a8c3e-112">Пакет установки включает систему управления версиями Git и приложение командной строки Git Bash, используемое для взаимодействия с локальным репозиторием Git.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-112">The install includes the Git version control system and Git Bash, the command-line app that you use to interact with your local Git repository.</span></span>

<span data-ttu-id="a8c3e-113">Если вы предпочитаете использовать графический пользовательский интерфейс вместо интерфейса командной строки, см. сведения о часто используемых параметрах на странице [доступных средств графического пользовательского интерфейса Software Freedom Conservancy](https://git-scm.com/downloads/guis), на сайте [версии GitHub для настольного компьютера](https://desktop.github.com/) или на сайте [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx).</span><span class="sxs-lookup"><span data-stu-id="a8c3e-113">If you prefer a graphical user interface (GUI) over a command-line interface (CLI), see [Software Freedom Conservancy's available GUI Clients page](https://git-scm.com/downloads/guis), [GitHub's GitHub Desktop](https://desktop.github.com/), or [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) for some popular options.</span></span>

<span data-ttu-id="a8c3e-114">Следуйте инструкциям по установке и настройке для выбранного клиента.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-114">Follow the instructions for your chosen client for installation and configuration.</span></span>

<span data-ttu-id="a8c3e-115">В следующей статье вы [настроите локальный репозиторий Git](get-started-setup-local.md).</span><span class="sxs-lookup"><span data-stu-id="a8c3e-115">In the next article, you will [Set up a local Git repository](get-started-setup-local.md).</span></span>

   <span data-ttu-id="a8c3e-116">Дополнительные ресурсы по Git см. здесь: [Глоссарий GitHub ](https://help.github.com/articles/github-glossary) | [Базовые возможности Git](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Обучающие ресурсы по Git и GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/).</span><span class="sxs-lookup"><span data-stu-id="a8c3e-116">Additional Git resources are available here: [Git terminology](https://help.github.com/articles/github-glossary) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span></span>

## <a name="understand-markdown-editors"></a><span data-ttu-id="a8c3e-117">Сведения о редакторах Markdown</span><span class="sxs-lookup"><span data-stu-id="a8c3e-117">Understand Markdown editors</span></span>

<span data-ttu-id="a8c3e-118">Markdown — это упрощенный язык разметки, который легко использовать и осваивать.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-118">Markdown is a lightweight markup language that is both easy to read and easy to learn.</span></span> <span data-ttu-id="a8c3e-119">Поэтому он быстро стал отраслевым стандартом.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-119">Therefore, it has rapidly become an industry standard.</span></span> <span data-ttu-id="a8c3e-120">Чтобы писать статьи на языке Markdown, мы рекомендуем скачать и установить Markdown editor.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-120">To write articles in Markdown, we recommend that you first download and install a Markdown editor.</span></span>  <span data-ttu-id="a8c3e-121">[Visual Studio Code](https://code.visualstudio.com/) — предпочтительное средство для редактирования разметки Markdown в Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-121">[Visual Studio Code](https://code.visualstudio.com/) is the preferred tool for editing Markdown at Microsoft.</span></span> <span data-ttu-id="a8c3e-122">[Atom](https://atom.io) — еще одно популярное средство для редактирования разметки Markdown.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-122">[Atom](https://atom.io) is another popular tool for editing Markdown.</span></span>

<span data-ttu-id="a8c3e-123">Тексты с разметкой Markdown сохраняются в файлы с расширением MD.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-123">Markdown text is saved into files with .md extension.</span></span>

<span data-ttu-id="a8c3e-124">Дополнительные сведения о написании кода на языке Markdown, включая основные сведения о Markdown и функциях, которые поддерживаются настраиваемыми расширениями OPS для Markdown, см. в статье об [использовании Markdown](how-to-write-use-markdown.md).</span><span class="sxs-lookup"><span data-stu-id="a8c3e-124">Additional details on how to write with Markdown, including Markdown basics and the features supported by OPS custom Markdown extensions, are covered later in the [How to use Markdown](how-to-write-use-markdown.md) article.</span></span>

## <a name="visual-studio-code"></a><span data-ttu-id="a8c3e-125">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="a8c3e-125">Visual Studio Code</span></span>

<span data-ttu-id="a8c3e-126">[Visual Studio Code](https://code.visualstudio.com/) (также называется VS Code) — это простой редактор, который работает в Windows, Linux и Mac.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-126">[Visual Studio Code](https://code.visualstudio.com/), also known as VS Code, is a lightweight editor that works on Windows, Linux, and Mac.</span></span> <span data-ttu-id="a8c3e-127">Он включает интеграцию с Git и поддержку расширений.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-127">It includes git integration, and support for extensions.</span></span>

<span data-ttu-id="a8c3e-128">Скачайте и установите [VS Code](https://code.visualstudio.com/).</span><span class="sxs-lookup"><span data-stu-id="a8c3e-128">Download and install [VS Code](https://code.visualstudio.com/).</span></span> <span data-ttu-id="a8c3e-129">На главной странице VS Code должна правильно определиться ваша операционная система:</span><span class="sxs-lookup"><span data-stu-id="a8c3e-129">The VS Code home page should detect your operating system correctly.</span></span>

- <span data-ttu-id="a8c3e-130">[Windows](https://code.visualstudio.com/docs/setup/windows);</span><span class="sxs-lookup"><span data-stu-id="a8c3e-130">[Windows](https://code.visualstudio.com/docs/setup/windows)</span></span>
- <span data-ttu-id="a8c3e-131">[Mac](https://code.visualstudio.com/docs/setup/mac);</span><span class="sxs-lookup"><span data-stu-id="a8c3e-131">[Mac](https://code.visualstudio.com/docs/setup/mac)</span></span>
- <span data-ttu-id="a8c3e-132">[Linux](https://code.visualstudio.com/docs/setup/linux).</span><span class="sxs-lookup"><span data-stu-id="a8c3e-132">[Linux](https://code.visualstudio.com/docs/setup/linux)</span></span>

> [!TIP]
> <span data-ttu-id="a8c3e-133">Чтобы запустить VS Code и открыть текущую папку, выполните команду `code .` в командной строке или оболочке Bash.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-133">To launch VS Code and open the current folder, run the command `code .` in the command line or bash shell.</span></span> <span data-ttu-id="a8c3e-134">Если текущая папка содержится в локальном репозитории Git, в Visual Studio Code автоматически отобразятся данные об интеграции с GitHub.</span><span class="sxs-lookup"><span data-stu-id="a8c3e-134">If the current folder is part of a local git repo, the github integration appears in Visual Studio Code automatically.</span></span>

## <a name="next-steps"></a><span data-ttu-id="a8c3e-135">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="a8c3e-135">Next steps</span></span>

<span data-ttu-id="a8c3e-136">Теперь все готово к [настройке локального репозитория](get-started-setup-local.md).</span><span class="sxs-lookup"><span data-stu-id="a8c3e-136">Now you are ready to [Set up a local Git repository](get-started-setup-local.md).</span></span>
