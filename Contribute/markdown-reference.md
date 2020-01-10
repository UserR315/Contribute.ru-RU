---
title: Справочник по разметке Markdown для docs.microsoft.com
description: Ознакомьтесь с функциями и синтаксисом Markdown, используемыми на платформе Документации Майкрософт.
author: meganbradley
ms.author: mbradley
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: 452cbf97db748532ae2b0e09b4bb558c8f757a61
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188255"
---
# <a name="markdown-reference"></a><span data-ttu-id="3730b-103">Справочник по разметке Markdown</span><span class="sxs-lookup"><span data-stu-id="3730b-103">Markdown Reference</span></span>

<span data-ttu-id="3730b-104">Markdown — это облегченный язык разметки с синтаксисом форматирования обычного текста.</span><span class="sxs-lookup"><span data-stu-id="3730b-104">Markdown is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="3730b-105">Платформа Docs поддерживает стандарт CommonMark для Markdown, а также несколько пользовательских расширений Markdown, предоставляющих дополнительное содержимое для docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="3730b-105">The Docs platform supports the CommonMark standard for Markdown, plus some custom Markdown extensions designed to provide richer content on docs.microsoft.com.</span></span> <span data-ttu-id="3730b-106">Эта статья содержит алфавитный справочник по работе с Markdown для docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="3730b-106">This article provides an alphabetical reference for using Markdown for docs.microsoft.com.</span></span>

<span data-ttu-id="3730b-107">Для работы с разметкой Markdown можно использовать любой текстовый редактор.</span><span class="sxs-lookup"><span data-stu-id="3730b-107">You can use any text editor to author Markdown.</span></span> <span data-ttu-id="3730b-108">В качестве редактора, упрощающего вставку стандартного синтаксиса Markdown и пользовательских расширений Docs, рекомендуем использовать [VS Code](https://code.visualstudio.com/) с установленным [пакетом создания документации](https://aka.ms/DocsAuthoringPack).</span><span class="sxs-lookup"><span data-stu-id="3730b-108">For an editor that facilitates inserting both standard Markdown syntax and custom Docs extensions, we recommend [VS Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installed.</span></span>

<span data-ttu-id="3730b-109">Платформа Docs использует модуль Markdig для разметки Markdown.</span><span class="sxs-lookup"><span data-stu-id="3730b-109">Docs uses the Markdig Markdown engine.</span></span> <span data-ttu-id="3730b-110">Сравнить отрисовку разметки Markdown в Markdig с другими обработчиками можно по адресу [https://babelmark.github.io/](https://babelmark.github.io/).</span><span class="sxs-lookup"><span data-stu-id="3730b-110">You can test the rendering of Markdown in Markdig vs. other engines at [https://babelmark.github.io/](https://babelmark.github.io/).</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="3730b-111">Оповещения ("Примечание", "Совет", "Важно!", "Внимание!", "Предупреждение")</span><span class="sxs-lookup"><span data-stu-id="3730b-111">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="3730b-112">Оповещения — это специальные расширения Markdown для платформы Docs, которые используются для создания блоков цитирования, отображаемых на сайте docs.microsoft.com с помощью цветов и значков, указывающих на важность содержимого.</span><span class="sxs-lookup"><span data-stu-id="3730b-112">Alerts are a Docs Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="3730b-113">Поддерживаются следующие типы оповещений:</span><span class="sxs-lookup"><span data-stu-id="3730b-113">The following alert types are supported:</span></span>

```md
> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.
```

<span data-ttu-id="3730b-114">На сайте docs.microsoft.com эти оповещения отображаются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3730b-114">These alerts look like this on docs.microsoft.com:</span></span>

![Вид оповещений из предыдущего примера с разными значками и цветами на опубликованной странице портала документации.](media/alerts-rendering.png)

## <a name="code-snippets"></a><span data-ttu-id="3730b-116">Фрагменты кода</span><span class="sxs-lookup"><span data-stu-id="3730b-116">Code snippets</span></span>

<span data-ttu-id="3730b-117">Вы можете вставить фрагменты кода в свои файлы Markdown:</span><span class="sxs-lookup"><span data-stu-id="3730b-117">You can embed code snippets in your Markdown files:</span></span>

```md
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a><span data-ttu-id="3730b-118">Заголовки</span><span class="sxs-lookup"><span data-stu-id="3730b-118">Headings</span></span>

<span data-ttu-id="3730b-119">Платформа Docs поддерживает шесть уровней заголовков Markdown:</span><span class="sxs-lookup"><span data-stu-id="3730b-119">Docs supports six levels of Markdown headings:</span></span>

```md
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="3730b-120">Между последним символом `#` и содержимым заголовка должен присутствовать пробел.</span><span class="sxs-lookup"><span data-stu-id="3730b-120">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="3730b-121">В одном файле Markdown должен быть один и только один заголовок H1.</span><span class="sxs-lookup"><span data-stu-id="3730b-121">Each Markdown file must have one and only one H1.</span></span>
- <span data-ttu-id="3730b-122">Заголовок H1 указывается в файле в первую очередь, сразу после блока метаданных YML.</span><span class="sxs-lookup"><span data-stu-id="3730b-122">The H1 must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="3730b-123">Заголовки H2 автоматически отображаются в правом меню навигации опубликованного файла.</span><span class="sxs-lookup"><span data-stu-id="3730b-123">H2s automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="3730b-124">Это правило не применяется к заголовкам следующих уровней, поэтому для удобства перехода по содержимому рекомендуется использовать заголовки H2.</span><span class="sxs-lookup"><span data-stu-id="3730b-124">Lower-level headings do not, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="3730b-125">Использовать заголовки HTML, такие как `<h1>`, не рекомендуется, и в некоторых случаях из-за них могут возникать предупреждения при сборке.</span><span class="sxs-lookup"><span data-stu-id="3730b-125">HTML headings, such as `<h1>`, are not recommended and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="3730b-126">Привязка к отдельным заголовкам в файле выполняется с помощью [закладок](#bookmark-links).</span><span class="sxs-lookup"><span data-stu-id="3730b-126">You can link to individual headings in a file via [bookmarks](#bookmark-links).</span></span>

## <a name="html"></a><span data-ttu-id="3730b-127">HTML</span><span class="sxs-lookup"><span data-stu-id="3730b-127">HTML</span></span>

<span data-ttu-id="3730b-128">Хотя Markdown поддерживает встроенный HTML-код, HTML не рекомендуется использовать для публикации на платформе Docs. Любой код, за исключением ограниченного списка значений, будет вызывать появление ошибок и предупреждений при сборке.</span><span class="sxs-lookup"><span data-stu-id="3730b-128">Although Markdown supports inline HTML, HTML is not recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span>

## <a name="images"></a><span data-ttu-id="3730b-129">Изображения</span><span class="sxs-lookup"><span data-stu-id="3730b-129">Images</span></span>

<span data-ttu-id="3730b-130">Для включения изображения используется следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="3730b-130">The syntax to include an image is:</span></span>

```md
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="3730b-131">Где `alt text` — краткое описание изображения, а `<folder path>` — относительный путь к нему.</span><span class="sxs-lookup"><span data-stu-id="3730b-131">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="3730b-132">Заменяющий текст необходим для средств чтения с экрана для слабовидящих.</span><span class="sxs-lookup"><span data-stu-id="3730b-132">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="3730b-133">Он также удобен при возникновении ошибок на сайте, из-за которых не удается воспроизвести изображение.</span><span class="sxs-lookup"><span data-stu-id="3730b-133">It is also useful if there is a site bug where the image cannot render.</span></span>

<span data-ttu-id="3730b-134">Изображения должны храниться в папке `/media` в наборе документации.</span><span class="sxs-lookup"><span data-stu-id="3730b-134">Images should be stored in a `/media` folder within your doc set.</span></span> <span data-ttu-id="3730b-135">Для изображений по умолчанию поддерживаются следующие типы файлов:</span><span class="sxs-lookup"><span data-stu-id="3730b-135">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="3730b-136">JPG,</span><span class="sxs-lookup"><span data-stu-id="3730b-136">.jpg</span></span>
- <span data-ttu-id="3730b-137">PNG.</span><span class="sxs-lookup"><span data-stu-id="3730b-137">.png</span></span>

<span data-ttu-id="3730b-138">Вы можете добавить поддержку других типов изображений, добавив их в виде ресурсов в файл docfx.json</span><span class="sxs-lookup"><span data-stu-id="3730b-138">You can add support for other image types by adding them as resources to the docfx.json file</span></span><!--add link to reference when available--> <span data-ttu-id="3730b-139">для вашего набора документации.</span><span class="sxs-lookup"><span data-stu-id="3730b-139">for your doc set.</span></span>

## <a name="links"></a><span data-ttu-id="3730b-140">Создание ссылок</span><span class="sxs-lookup"><span data-stu-id="3730b-140">Links</span></span>

<span data-ttu-id="3730b-141">Как правило, платформа Docs использует стандартные ссылки Markdown на другие файлы и страницы.</span><span class="sxs-lookup"><span data-stu-id="3730b-141">In most cases, Docs uses standard Markdown links to other files and pages.</span></span> <span data-ttu-id="3730b-142">Типы ссылок описываются в подразделах ниже.</span><span class="sxs-lookup"><span data-stu-id="3730b-142">The types of links are described in subsections below.</span></span>

> [!TIP]
> <span data-ttu-id="3730b-143">Пакет создания документации для VS Code помогает правильно вставлять ссылки и закладки в автоматическом режиме.</span><span class="sxs-lookup"><span data-stu-id="3730b-143">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3730b-144">Не включайте коды языковых стандартов, такие как en-us, в ссылки на сайты Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="3730b-144">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span></span> <span data-ttu-id="3730b-145">Жестко закодированные коды языков блокируют воспроизведение локализованного содержимого: это неудобно для пользователей, говорящих на других языках, и влечет за собой большие затраты на локализацию.</span><span class="sxs-lookup"><span data-stu-id="3730b-145">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span></span> <span data-ttu-id="3730b-146">При копировании URL-адреса из браузера код языка включается по умолчанию, поэтому его необходимо удалить вручную при создании ссылки.</span><span class="sxs-lookup"><span data-stu-id="3730b-146">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link.</span></span> <span data-ttu-id="3730b-147">Например, используйте:</span><span class="sxs-lookup"><span data-stu-id="3730b-147">For example, use:</span></span>
>
> `[Microsoft](https://www.microsoft.com)`
>
> <span data-ttu-id="3730b-148">А не:</span><span class="sxs-lookup"><span data-stu-id="3730b-148">Not:</span></span>
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a><span data-ttu-id="3730b-149">Относительные ссылки на файлы в том же наборе документации</span><span class="sxs-lookup"><span data-stu-id="3730b-149">Relative links to files in the same doc set</span></span>

<span data-ttu-id="3730b-150">Относительный путь — это путь к целевому файлу относительно текущего файла.</span><span class="sxs-lookup"><span data-stu-id="3730b-150">A relative path is the path to the target file relative to the current file.</span></span> <span data-ttu-id="3730b-151">На платформе Docs относительные пути можно использовать для связывания файлов в одном наборе документов.</span><span class="sxs-lookup"><span data-stu-id="3730b-151">In Docs, you can use a relative path to link to another file within the same doc set.</span></span> <span data-ttu-id="3730b-152">Синтаксис относительного пути следующий:</span><span class="sxs-lookup"><span data-stu-id="3730b-152">The syntax for a relative path is as follows:</span></span>

```md
[link text](../../folder/filename.md)
```

<span data-ttu-id="3730b-153">Где `../` означает один уровень выше в иерархии.</span><span class="sxs-lookup"><span data-stu-id="3730b-153">Where `../` indicates one level above in the hierarchy.</span></span>

- <span data-ttu-id="3730b-154">Относительный путь будет разрешаться во время сборки, включая удаление расширения MD.</span><span class="sxs-lookup"><span data-stu-id="3730b-154">The relative path will be resolved during the build, including removal of the .md extension.</span></span>
- <span data-ttu-id="3730b-155">Можно использовать "../" для указания на файл в родительской папке, но этот файл должен быть в том же наборе документации.</span><span class="sxs-lookup"><span data-stu-id="3730b-155">You can use "../" to link to a file in the parent folder, but that file has to be in the same doc set.</span></span> <span data-ttu-id="3730b-156">"../" нельзя использовать для указания на файл в другой папке набора документации.</span><span class="sxs-lookup"><span data-stu-id="3730b-156">You cannot use "../" to link to a file in another doc set folder.</span></span>
- <span data-ttu-id="3730b-157">Платформа Docs также поддерживает особый формат относительного пути, начинающийся с символа "~" (например, ~/foo/bar.md).</span><span class="sxs-lookup"><span data-stu-id="3730b-157">Docs also supports a special form of relative path that starts with "~" (for example, ~/foo/bar.md).</span></span> <span data-ttu-id="3730b-158">Этот синтаксис указывает файл относительно корневой папки набора документации.</span><span class="sxs-lookup"><span data-stu-id="3730b-158">This syntax indicates a file relative to the root folder of a doc set.</span></span> <span data-ttu-id="3730b-159">Этот вид пути также проверяется и разрешается во время сборки.</span><span class="sxs-lookup"><span data-stu-id="3730b-159">This kind of path is also validated and resolved during the build.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3730b-160">Включите расширение файла в относительный путь.</span><span class="sxs-lookup"><span data-stu-id="3730b-160">Include the file extension in the relative path.</span></span> <span data-ttu-id="3730b-161">В ходе сборки проверяется существование целевого файла по этому относительному пути.</span><span class="sxs-lookup"><span data-stu-id="3730b-161">Build validates the existence of the target file of that relative path.</span></span> <span data-ttu-id="3730b-162">Если относительный путь не включает расширение файла, в ходе сборки, скорее всего, будет создано предупреждение или неработающая ссылка.</span><span class="sxs-lookup"><span data-stu-id="3730b-162">If relative path does not include file extension, it is likely build will report a warning of broken link.</span></span> <span data-ttu-id="3730b-163">Например, используйте:</span><span class="sxs-lookup"><span data-stu-id="3730b-163">For example, use:</span></span>
>
> `[link text](../../folder/filename.md)`
>
> <span data-ttu-id="3730b-164">А не:</span><span class="sxs-lookup"><span data-stu-id="3730b-164">Not:</span></span>
>
> `[link text](../../folder/filename)`

### <a name="site-relative-links-to-other-files-on-docs"></a><span data-ttu-id="3730b-165">Относительные ссылки на другие файлы на платформе Docs на сайте</span><span class="sxs-lookup"><span data-stu-id="3730b-165">Site relative links to other files on Docs</span></span>

```md
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

<span data-ttu-id="3730b-166">Не включайте расширение файла (MD).</span><span class="sxs-lookup"><span data-stu-id="3730b-166">Do not include the file extension (.md).</span></span> <span data-ttu-id="3730b-167">Это ссылка на обзорный файл Linux за пределами набора документации "статей" Azure.</span><span class="sxs-lookup"><span data-stu-id="3730b-167">This links to the Linux overview file from outside the Azure "articles" doc set.</span></span>

### <a name="links-to-external-sites"></a><span data-ttu-id="3730b-168">Ссылки на внешние сайты</span><span class="sxs-lookup"><span data-stu-id="3730b-168">Links to external sites</span></span>

```md
[Microsoft](https://www.microsoft.com)
```

<span data-ttu-id="3730b-169">Ссылка на основе URL-адреса на другую веб-страницу (должна включать https://).</span><span class="sxs-lookup"><span data-stu-id="3730b-169">URL-based link to another web page (must include https://).</span></span>

### <a name="bookmark-links"></a><span data-ttu-id="3730b-170">Ссылки закладок</span><span class="sxs-lookup"><span data-stu-id="3730b-170">Bookmark links</span></span>

<span data-ttu-id="3730b-171">Ссылка-закладка на заголовок в другом файле того же репозитория.</span><span class="sxs-lookup"><span data-stu-id="3730b-171">Bookmark link to a heading in another file in the same repo.</span></span> <span data-ttu-id="3730b-172">Например:</span><span class="sxs-lookup"><span data-stu-id="3730b-172">For example:</span></span>

```md
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="3730b-173">Ссылка-закладка на заголовок в текущем файле:</span><span class="sxs-lookup"><span data-stu-id="3730b-173">Bookmark link to a heading in the current file:</span></span>

```md
[Managed Disks](#managed-disks)
```

<span data-ttu-id="3730b-174">Используйте решетку `#`, а затем укажите слова заголовка на английском языке.</span><span class="sxs-lookup"><span data-stu-id="3730b-174">Use a hash mark `#` followed by the words of the heading.</span></span> <span data-ttu-id="3730b-175">Чтобы преобразовать текст заголовка в текст ссылки:</span><span class="sxs-lookup"><span data-stu-id="3730b-175">To change the heading text into link text:</span></span>
- <span data-ttu-id="3730b-176">Используйте строчные буквы</span><span class="sxs-lookup"><span data-stu-id="3730b-176">Use all lowercase characters</span></span>
- <span data-ttu-id="3730b-177">Удалите знаки препинания</span><span class="sxs-lookup"><span data-stu-id="3730b-177">Remove punctuation</span></span>
- <span data-ttu-id="3730b-178">Замените пробелы на дефисы</span><span class="sxs-lookup"><span data-stu-id="3730b-178">Replace spaces with dashes</span></span>

<span data-ttu-id="3730b-179">Например, если английская версия статьи имеет заголовок "2.2 Security concerns", то текст ссылки-закладки будет "#22-security-concerns".</span><span class="sxs-lookup"><span data-stu-id="3730b-179">For example, if the heading name is "2.2 Security concerns", then the bookmark link text will be "#22-security-concerns".</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="3730b-180">Явные ссылки привязки</span><span class="sxs-lookup"><span data-stu-id="3730b-180">Explicit anchor links</span></span>

<span data-ttu-id="3730b-181">Явные ссылки привязки, использующие HTML-тег `<a>`**не требуются и не рекомендуются**, за исключением страниц-концентраторов и целевых страниц.</span><span class="sxs-lookup"><span data-stu-id="3730b-181">Explicit anchor links using the `<a>` HTML tag are **not required or recommended** except in hub and landing pages.</span></span> <span data-ttu-id="3730b-182">Используйте закладки, как описано выше, в общих файлах Markdown.</span><span class="sxs-lookup"><span data-stu-id="3730b-182">Use bookmarks as described above in general Markdown files.</span></span> <span data-ttu-id="3730b-183">Для страниц-концентраторов и целевых страниц привязки используются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3730b-183">For hub and landing pages, use anchors as follows:</span></span>

<span data-ttu-id="3730b-184">`## <a id="AnchorText"> </a>Header text` или `## <a name="AnchorText"> </a>Header text`</span><span class="sxs-lookup"><span data-stu-id="3730b-184">`## <a id="AnchorText"> </a>Header text` or `## <a name="AnchorText"> </a>Header text`</span></span>

<span data-ttu-id="3730b-185">Для ссылки на явные привязки используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="3730b-185">To link to explicit anchors, use the following syntax:</span></span>

```md
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a><span data-ttu-id="3730b-186">Ссылки XREF (перекрестные ссылки)</span><span class="sxs-lookup"><span data-stu-id="3730b-186">XREF (cross reference) links</span></span>

<span data-ttu-id="3730b-187">Для ссылки на автоматически создаваемые страницы справочных материалов по API в текущем или другом наборе документации используйте ссылки XREF с уникальным идентификатором (UID).</span><span class="sxs-lookup"><span data-stu-id="3730b-187">To link to auto-generated API references pages in the current doc set or other doc sets, use XREF links with the unique ID (UID).</span></span>

> [!NOTE]
> <span data-ttu-id="3730b-188">Для ссылки на страницы справочных материалов по API в других наборах документации потребуется добавить конфигурацию `xrefService` в файл `docfx.json`.</span><span class="sxs-lookup"><span data-stu-id="3730b-188">To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.</span></span>
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

<span data-ttu-id="3730b-189">Уникальный идентификатор совпадает с полным именем класса и члена.</span><span class="sxs-lookup"><span data-stu-id="3730b-189">The UID equates to the fully qualified class and member name.</span></span> <span data-ttu-id="3730b-190">Если добавить символ \* после UID, ссылка будет вести на страницу перегрузки, а не к конкретному API.</span><span class="sxs-lookup"><span data-stu-id="3730b-190">If you add a \* after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="3730b-191">Например, используйте `List<T>.BinarySearch*` для ссылки на страницу "Метод BinarySearch" вместо ссылки на конкретную перегрузку, например `List<T>.BinarySearch(T, IComparer<T>)`.</span><span class="sxs-lookup"><span data-stu-id="3730b-191">For example, use `List<T>.BinarySearch*` to link to the BinarySearch Method page instead of linking to a specific overload such as `List<T>.BinarySearch(T, IComparer<T>)`.</span></span>

<span data-ttu-id="3730b-192">Можно выбрать один из следующих вариантов синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="3730b-192">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="3730b-193">Автоматическая ссылка: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="3730b-193">Auto-link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span></span>

  <span data-ttu-id="3730b-194">Необязательный параметр запроса `displayProperty` создает полный текст ссылки.</span><span class="sxs-lookup"><span data-stu-id="3730b-194">The optional `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="3730b-195">По умолчанию в тексте ссылки отображается только имя члена или типа.</span><span class="sxs-lookup"><span data-stu-id="3730b-195">By default, link text shows only the member or type name.</span></span>

- <span data-ttu-id="3730b-196">Ссылка с разметкой Markdown: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="3730b-196">Markdown link: `[link text](xref:UID)`</span></span>
  
  <span data-ttu-id="3730b-197">Используется, когда требуется настроить текст ссылки.</span><span class="sxs-lookup"><span data-stu-id="3730b-197">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="3730b-198">Примеры:</span><span class="sxs-lookup"><span data-stu-id="3730b-198">Examples:</span></span>

- <span data-ttu-id="3730b-199">`<xref:System.String>` отображается как String;</span><span class="sxs-lookup"><span data-stu-id="3730b-199">`<xref:System.String>` renders as "String".</span></span>
- <span data-ttu-id="3730b-200">`<xref:System.String?displayProperty=nameWithType>` отображается как System.String;</span><span class="sxs-lookup"><span data-stu-id="3730b-200">`<xref:System.String?displayProperty=nameWithType>` renders as "System.String".</span></span>
- <span data-ttu-id="3730b-201">`[String class](xref:System.String)` отображается как String class.</span><span class="sxs-lookup"><span data-stu-id="3730b-201">`[String class](xref:System.String)` renders as "String class".</span></span>

<span data-ttu-id="3730b-202">Сейчас не существует простого способа поиска UID.</span><span class="sxs-lookup"><span data-stu-id="3730b-202">Right now, there is no easy way to find the UIDs.</span></span> <!-- ? --><span data-ttu-id="3730b-203">Чтобы найти UID для API, просмотрите исходный код страницы API, на которую нужно создать ссылку, и найдите значение ms.assetid.</span><span class="sxs-lookup"><span data-stu-id="3730b-203">The best way to find the UID for an API is to view the source for the API page you want to link to and find the ms.assetid value.</span></span> <span data-ttu-id="3730b-204">Отдельные значения перегрузки не отображаются в исходном коде.</span><span class="sxs-lookup"><span data-stu-id="3730b-204">Individual overload values are not shown in the source.</span></span> <span data-ttu-id="3730b-205">Мы работаем над улучшением нашей системы.</span><span class="sxs-lookup"><span data-stu-id="3730b-205">We're working on having a better system in the future.</span></span>

<span data-ttu-id="3730b-206">Если идентификатор содержит специальные символы \`, \# или \*, значение UID должно быть закодировано в HTML как `%60`, `%23` и `%2A` соответственно.</span><span class="sxs-lookup"><span data-stu-id="3730b-206">When the UID contains the special characters \`, \#, or \*, the UID value needs to be HTML encoded as `%60`, `%23`, and `%2A`, respectively.</span></span> <span data-ttu-id="3730b-207">Иногда круглые скобки тоже кодируются, но это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="3730b-207">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="3730b-208">Примеры:</span><span class="sxs-lookup"><span data-stu-id="3730b-208">Examples:</span></span>

- <span data-ttu-id="3730b-209">System.Threading.Tasks.Task\`1 заменяется на `System.Threading.Tasks.Task%601`;</span><span class="sxs-lookup"><span data-stu-id="3730b-209">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="3730b-210">System.Exception.\#ctor заменяется на `System.Exception.%23ctor`;</span><span class="sxs-lookup"><span data-stu-id="3730b-210">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="3730b-211">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) заменяется на `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`.</span><span class="sxs-lookup"><span data-stu-id="3730b-211">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="3730b-212">Списки (нумерованные, маркированные, контрольные)</span><span class="sxs-lookup"><span data-stu-id="3730b-212">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="3730b-213">Нумерованный список</span><span class="sxs-lookup"><span data-stu-id="3730b-213">Numbered list</span></span>

<span data-ttu-id="3730b-214">Для создания нумерованного списка можно использовать все 1, которые при публикации отображаются как последовательный список.</span><span class="sxs-lookup"><span data-stu-id="3730b-214">To create a numbered list, you can use all 1s, which are rendered as a sequential list when published.</span></span> <span data-ttu-id="3730b-215">Для повышения удобства чтения исходного кода списки можно вводить с приращением.</span><span class="sxs-lookup"><span data-stu-id="3730b-215">For increased source readability, you can increment your lists.</span></span>

<span data-ttu-id="3730b-216">Не используйте в списках, включая вложенные списки, буквы.</span><span class="sxs-lookup"><span data-stu-id="3730b-216">Do not use letters in lists, including nested lists.</span></span> <span data-ttu-id="3730b-217">При публикации на платформе Docs они преобразуются некорректно. Вложенные списки с цифрами преобразуются в списки со строчными буквами при публикации.</span><span class="sxs-lookup"><span data-stu-id="3730b-217">They do not render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="3730b-218">Например:</span><span class="sxs-lookup"><span data-stu-id="3730b-218">For example:</span></span>

```md
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="3730b-219">Это отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3730b-219">This renders as follows:</span></span>

1. <span data-ttu-id="3730b-220">Это</span><span class="sxs-lookup"><span data-stu-id="3730b-220">This is</span></span>
1. <span data-ttu-id="3730b-221">родительский нумерованный список,</span><span class="sxs-lookup"><span data-stu-id="3730b-221">a parent numbered list</span></span>
   1. <span data-ttu-id="3730b-222">а это</span><span class="sxs-lookup"><span data-stu-id="3730b-222">and this is</span></span>
   1. <span data-ttu-id="3730b-223">вложенный нумерованный список</span><span class="sxs-lookup"><span data-stu-id="3730b-223">a nested numbered list</span></span>
1. <span data-ttu-id="3730b-224">(конец)</span><span class="sxs-lookup"><span data-stu-id="3730b-224">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="3730b-225">Маркированный список</span><span class="sxs-lookup"><span data-stu-id="3730b-225">Bulleted list</span></span>

<span data-ttu-id="3730b-226">Для создания маркированного списка используйте `-`, за которым следует пробел в начале каждой строки.</span><span class="sxs-lookup"><span data-stu-id="3730b-226">To create a bulleted list, use `-` followed by a space at the beginning of each line:</span></span>

```md
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="3730b-227">Это отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3730b-227">This renders as follows:</span></span>

- <span data-ttu-id="3730b-228">Это</span><span class="sxs-lookup"><span data-stu-id="3730b-228">This is</span></span>
- <span data-ttu-id="3730b-229">родительский маркированный список,</span><span class="sxs-lookup"><span data-stu-id="3730b-229">a parent bulleted list</span></span>
  - <span data-ttu-id="3730b-230">а это</span><span class="sxs-lookup"><span data-stu-id="3730b-230">and this is</span></span>
  - <span data-ttu-id="3730b-231">вложенный маркированный список</span><span class="sxs-lookup"><span data-stu-id="3730b-231">a nested bulleted list</span></span>
- <span data-ttu-id="3730b-232">Готово!</span><span class="sxs-lookup"><span data-stu-id="3730b-232">All done!</span></span>

### <a name="checklist"></a><span data-ttu-id="3730b-233">Контрольный список</span><span class="sxs-lookup"><span data-stu-id="3730b-233">Checklist</span></span>

<span data-ttu-id="3730b-234">Контрольные списки можно использовать (только) на сайте docs.microsoft.com с помощью пользовательского расширения Markdown:</span><span class="sxs-lookup"><span data-stu-id="3730b-234">Checklists are available for use on docs.microsoft.com (only) via a custom Markdown extension:</span></span>

```md
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="3730b-235">Этот пример отображается на сайте docs.microsoft.com следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3730b-235">This example renders on docs.microsoft.com like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="3730b-236">List item 1</span><span class="sxs-lookup"><span data-stu-id="3730b-236">List item 1</span></span>
> * <span data-ttu-id="3730b-237">List item 2</span><span class="sxs-lookup"><span data-stu-id="3730b-237">List item 2</span></span>
> * <span data-ttu-id="3730b-238">List item 3</span><span class="sxs-lookup"><span data-stu-id="3730b-238">List item 3</span></span>

<span data-ttu-id="3730b-239">Контрольные списки используются в начале или конце статьи для подведения итогов "Чему вы научитесь" или "Чему вы научились".</span><span class="sxs-lookup"><span data-stu-id="3730b-239">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="3730b-240">Не вставляйте контрольные списки в статьи по случайному принципу.</span><span class="sxs-lookup"><span data-stu-id="3730b-240">Do not add random checklists throughout your articles.</span></span>
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a><span data-ttu-id="3730b-241">Действие "Дальнейшие действия"</span><span class="sxs-lookup"><span data-stu-id="3730b-241">Next step action</span></span>

<span data-ttu-id="3730b-242">Пользовательское расширение можно использовать для добавления кнопки "Дальнейшие действия" на страницы (только) docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="3730b-242">You can use a custom extension to add a next step action button to pages on docs.microsoft.com (only).</span></span>

<span data-ttu-id="3730b-243">Используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="3730b-243">The syntax is as follows:</span></span>

```md
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="3730b-244">Например:</span><span class="sxs-lookup"><span data-stu-id="3730b-244">For example:</span></span>

```md
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

<span data-ttu-id="3730b-245">Это отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3730b-245">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="3730b-246">Подробнее о базовом стиле</span><span class="sxs-lookup"><span data-stu-id="3730b-246">Learn about basic style</span></span>](style-quick-start.md)

<span data-ttu-id="3730b-247">Вы можете использовать любые поддерживаемые ссылки в действии "Дальнейшие действия", включая ссылку Markdown на другую веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="3730b-247">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="3730b-248">Как правило, ссылка "Дальнейшие действия" — это относительная ссылка на другой файл в том же наборе документации.</span><span class="sxs-lookup"><span data-stu-id="3730b-248">In most cases, the next action link will be a relative link to another file in the same doc set.</span></span>

## <a name="section-definition"></a><span data-ttu-id="3730b-249">Определение раздела</span><span class="sxs-lookup"><span data-stu-id="3730b-249">Section definition</span></span>

<!-- more info about this would be helpful! -->
<span data-ttu-id="3730b-250">Вам может потребоваться определить раздел.</span><span class="sxs-lookup"><span data-stu-id="3730b-250">You might need to define a section.</span></span> <span data-ttu-id="3730b-251">Этот синтаксис в основном используется для таблиц кодов.</span><span class="sxs-lookup"><span data-stu-id="3730b-251">This syntax is mostly used for code tables.</span></span>
<span data-ttu-id="3730b-252">См. указанный ниже пример.</span><span class="sxs-lookup"><span data-stu-id="3730b-252">See the following example:</span></span>

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

<span data-ttu-id="3730b-253">Предыдущий текст Markdown будет отображаться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3730b-253">The preceding blockquote Markdown text will be rendered as:</span></span>
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a><span data-ttu-id="3730b-254">Селекторы</span><span class="sxs-lookup"><span data-stu-id="3730b-254">Selectors</span></span>

<!-- could be more clear! -->
<span data-ttu-id="3730b-255">Используйте селектор для связи с разными страницами одной статьи.</span><span class="sxs-lookup"><span data-stu-id="3730b-255">You can use a selector when you want to connect different pages for the same article.</span></span> <span data-ttu-id="3730b-256">Затем читатели смогут переключаться между этими страницами.</span><span class="sxs-lookup"><span data-stu-id="3730b-256">Readers can then switch between those pages.</span></span>

> [!NOTE]
> <span data-ttu-id="3730b-257">Это расширение функционирует по-разному на сайтах docs.microsoft.com и MSDN.</span><span class="sxs-lookup"><span data-stu-id="3730b-257">This extension works differently between docs.microsoft.com and MSDN.</span></span> <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a><span data-ttu-id="3730b-258">Единичный выбор</span><span class="sxs-lookup"><span data-stu-id="3730b-258">Single selector</span></span>

```
> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)
```

<span data-ttu-id="3730b-259">... будет иметь следующий вид:</span><span class="sxs-lookup"><span data-stu-id="3730b-259">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Универсальные приложения Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a><span data-ttu-id="3730b-268">Множественный выбор</span><span class="sxs-lookup"><span data-stu-id="3730b-268">Multi-selector</span></span>

```
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)
```

<span data-ttu-id="3730b-269">... будет иметь следующий вид:</span><span class="sxs-lookup"><span data-stu-id="3730b-269">... will be rendered like this:</span></span>

> [!div class="op_multi_selector" title1="Платформа" title2="Серверная часть"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Универсальные приложения Windows на C# | .NET)](how-to-write-workflows-major.md)
> - [(Универсальные приложения Windows на C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)

## <a name="tables"></a><span data-ttu-id="3730b-282">Tables</span><span class="sxs-lookup"><span data-stu-id="3730b-282">Tables</span></span>

<span data-ttu-id="3730b-283">Использование вертикальных линий и строк является самым простым способом создания таблиц в Markdown.</span><span class="sxs-lookup"><span data-stu-id="3730b-283">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="3730b-284">Чтобы создать стандартную таблицу с заголовком, вставьте пунктирную линию после первой строки.</span><span class="sxs-lookup"><span data-stu-id="3730b-284">To create a standard table with a header, follow the first line with dashed line:</span></span>

```md
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="3730b-285">Это отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3730b-285">This renders as follows:</span></span>

|<span data-ttu-id="3730b-286">Это</span><span class="sxs-lookup"><span data-stu-id="3730b-286">This is</span></span>   |<span data-ttu-id="3730b-287">просто</span><span class="sxs-lookup"><span data-stu-id="3730b-287">a simple</span></span>   |<span data-ttu-id="3730b-288">заголовок таблицы</span><span class="sxs-lookup"><span data-stu-id="3730b-288">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="3730b-289">данные</span><span class="sxs-lookup"><span data-stu-id="3730b-289">table</span></span>     |<span data-ttu-id="3730b-290">таблицы</span><span class="sxs-lookup"><span data-stu-id="3730b-290">data</span></span>       |<span data-ttu-id="3730b-291">здесь</span><span class="sxs-lookup"><span data-stu-id="3730b-291">here</span></span>        |
|<span data-ttu-id="3730b-292">вообще-то</span><span class="sxs-lookup"><span data-stu-id="3730b-292">it doesn't</span></span>|<span data-ttu-id="3730b-293">не всегда</span><span class="sxs-lookup"><span data-stu-id="3730b-293">actually</span></span>   |<span data-ttu-id="3730b-294">отображаются аккуратно!</span><span class="sxs-lookup"><span data-stu-id="3730b-294">have to line up nicely!</span></span>||

<span data-ttu-id="3730b-295">Можно также создать таблицу без заголовка.</span><span class="sxs-lookup"><span data-stu-id="3730b-295">You can also create a table without a header.</span></span> <span data-ttu-id="3730b-296">Например, чтобы создать список с несколькими столбцами:</span><span class="sxs-lookup"><span data-stu-id="3730b-296">For example, to create a multiple-column list:</span></span>

```md
|   |   |
| - | - |
| This | table |
| has no | header |
```

<span data-ttu-id="3730b-297">Это отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3730b-297">This renders like this:</span></span>

|   |   |
| - | - |
| <span data-ttu-id="3730b-298">Это</span><span class="sxs-lookup"><span data-stu-id="3730b-298">This</span></span> | <span data-ttu-id="3730b-299">таблица</span><span class="sxs-lookup"><span data-stu-id="3730b-299">table</span></span> |
| <span data-ttu-id="3730b-300">без</span><span class="sxs-lookup"><span data-stu-id="3730b-300">has no</span></span> | <span data-ttu-id="3730b-301">заголовка</span><span class="sxs-lookup"><span data-stu-id="3730b-301">header</span></span> |

<span data-ttu-id="3730b-302">Можно выровнять столбцы с помощью двоеточий:</span><span class="sxs-lookup"><span data-stu-id="3730b-302">You can align the columns by using colons:</span></span>

```md
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

<span data-ttu-id="3730b-303">Отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3730b-303">Renders as follows:</span></span>

|                  |
|------------------|
|    <span data-ttu-id="3730b-304">по правому краю:</span><span class="sxs-lookup"><span data-stu-id="3730b-304">right aligned:</span></span>|
|<span data-ttu-id="3730b-305">:по левому краю</span><span class="sxs-lookup"><span data-stu-id="3730b-305">:left aligned</span></span>     |
|<span data-ttu-id="3730b-306">:по центру            :</span><span class="sxs-lookup"><span data-stu-id="3730b-306">:centered        :</span></span>|

> [!TIP]
> <span data-ttu-id="3730b-307">Расширение создания документации для VS Code упрощает добавление базовых таблиц Markdown.</span><span class="sxs-lookup"><span data-stu-id="3730b-307">The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!</span></span>
>
> <span data-ttu-id="3730b-308">Кроме того, можно использовать [веб-инструмент создания таблиц](http://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="3730b-308">You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).</span></span>

### <a name="mx-tdbreakall"></a><span data-ttu-id="3730b-309">mx-tdBreakAll</span><span class="sxs-lookup"><span data-stu-id="3730b-309">mx-tdBreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3730b-310">Эта функция работает только на веб-сайте docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="3730b-310">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="3730b-311">Создаваемая в Markdown таблица может выходить вправо, что делает ее нечитаемой.</span><span class="sxs-lookup"><span data-stu-id="3730b-311">If you create a table in Markdown, the table might expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="3730b-312">Эту проблему можно устранить, разрешив при необходимости разрыв таблицы при отображении документов.</span><span class="sxs-lookup"><span data-stu-id="3730b-312">You can solve that by allowing Docs rendering to break the table when needed.</span></span> <span data-ttu-id="3730b-313">Нужно просто заключить таблицу в настраиваемый класс `[!div class="mx-tdBreakAll"]`.</span><span class="sxs-lookup"><span data-stu-id="3730b-313">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="3730b-314">Далее приведен пример Markdown таблицы с тремя строками, которая будет заключена с помощью `div` с классом `mx-tdBreakAll`.</span><span class="sxs-lookup"><span data-stu-id="3730b-314">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```md
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="3730b-315">Она будет иметь следующий вид:</span><span class="sxs-lookup"><span data-stu-id="3730b-315">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="3730b-316">Имя</span><span class="sxs-lookup"><span data-stu-id="3730b-316">Name</span></span>|<span data-ttu-id="3730b-317">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3730b-317">Syntax</span></span>|<span data-ttu-id="3730b-318">Обязательно для автоматический установки?</span><span class="sxs-lookup"><span data-stu-id="3730b-318">Mandatory for silent installation?</span></span>|<span data-ttu-id="3730b-319">Описание</span><span class="sxs-lookup"><span data-stu-id="3730b-319">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="3730b-320">Quiet</span><span class="sxs-lookup"><span data-stu-id="3730b-320">Quiet</span></span>|<span data-ttu-id="3730b-321">/quiet</span><span class="sxs-lookup"><span data-stu-id="3730b-321">/quiet</span></span>|<span data-ttu-id="3730b-322">Да</span><span class="sxs-lookup"><span data-stu-id="3730b-322">Yes</span></span>|<span data-ttu-id="3730b-323">Запускает установщик без отображения пользовательского интерфейса и запросов.</span><span class="sxs-lookup"><span data-stu-id="3730b-323">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="3730b-324">NoRestart</span><span class="sxs-lookup"><span data-stu-id="3730b-324">NoRestart</span></span>|<span data-ttu-id="3730b-325">/norestart</span><span class="sxs-lookup"><span data-stu-id="3730b-325">/norestart</span></span>|<span data-ttu-id="3730b-326">Нет</span><span class="sxs-lookup"><span data-stu-id="3730b-326">No</span></span>|<span data-ttu-id="3730b-327">Подавляет попытки перезапуска.</span><span class="sxs-lookup"><span data-stu-id="3730b-327">Suppresses any attempts to restart.</span></span> <span data-ttu-id="3730b-328">По умолчанию пользовательский интерфейс выведет запрос перед перезапуском.</span><span class="sxs-lookup"><span data-stu-id="3730b-328">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="3730b-329">Help</span><span class="sxs-lookup"><span data-stu-id="3730b-329">Help</span></span>|<span data-ttu-id="3730b-330">/help</span><span class="sxs-lookup"><span data-stu-id="3730b-330">/help</span></span>|<span data-ttu-id="3730b-331">Нет</span><span class="sxs-lookup"><span data-stu-id="3730b-331">No</span></span>|<span data-ttu-id="3730b-332">Предоставляет справку и краткие инструкции.</span><span class="sxs-lookup"><span data-stu-id="3730b-332">Provides help and quick reference.</span></span> <span data-ttu-id="3730b-333">Отображает правильное использование команды setup, включая список всех параметров и вариантов поведения.</span><span class="sxs-lookup"><span data-stu-id="3730b-333">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="mx-tdcol2breakall"></a><span data-ttu-id="3730b-334">mx-tdCol2BreakAll</span><span class="sxs-lookup"><span data-stu-id="3730b-334">mx-tdCol2BreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3730b-335">Эта функция работает только на веб-сайте docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="3730b-335">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="3730b-336">Время от времени во втором столбце таблицы могут находиться очень длинные слова.</span><span class="sxs-lookup"><span data-stu-id="3730b-336">From time to time, you might have very long words in the second column of a table.</span></span> <span data-ttu-id="3730b-337">Чтобы правильно разделить эти слова, можно применить класс `mx-tdCol2BreakAll` с помощью синтаксиса оболочки `div`, как показано выше.</span><span class="sxs-lookup"><span data-stu-id="3730b-337">To ensure they are broken apart nicely, you can apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="html-tables"></a><span data-ttu-id="3730b-338">Таблицы HTML</span><span class="sxs-lookup"><span data-stu-id="3730b-338">HTML Tables</span></span>

<span data-ttu-id="3730b-339">Таблицы HTML не рекомендуется использовать для docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="3730b-339">HTML tables are not recommended for docs.microsoft.com.</span></span> <span data-ttu-id="3730b-340">Они трудны для восприятия в исходном виде — это нарушает основной принцип Markdown.</span><span class="sxs-lookup"><span data-stu-id="3730b-340">They are not human readable in the source - which is a key principle of Markdown.</span></span>

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a><span data-ttu-id="3730b-341">Видеоролики</span><span class="sxs-lookup"><span data-stu-id="3730b-341">Videos</span></span>

### <a name="embedding-videos-into-a-markdown-page"></a><span data-ttu-id="3730b-342">Внедрение видео на страницу Markdown</span><span class="sxs-lookup"><span data-stu-id="3730b-342">Embedding videos into a Markdown page</span></span>

<span data-ttu-id="3730b-343">Сейчас платформа Docs поддерживает видеоролики, опубликованные в одной из трех платформ:</span><span class="sxs-lookup"><span data-stu-id="3730b-343">Currently, Docs can support videos published to one of three locations:</span></span>

- <span data-ttu-id="3730b-344">YouTube</span><span class="sxs-lookup"><span data-stu-id="3730b-344">YouTube</span></span>
- <span data-ttu-id="3730b-345">Channel 9</span><span class="sxs-lookup"><span data-stu-id="3730b-345">Channel 9</span></span>
- <span data-ttu-id="3730b-346">собственной системе Майкрософт One Player.</span><span class="sxs-lookup"><span data-stu-id="3730b-346">Microsoft's own 'One Player' system</span></span>

<span data-ttu-id="3730b-347">Вы можете встроить видео с помощью следующего синтаксиса, и это видео будет отображено на платформе Docs.</span><span class="sxs-lookup"><span data-stu-id="3730b-347">You can embed a video with the following syntax, and Docs will render it.</span></span>

```md
> [!VIDEO <embedded_video_link>]
```

<span data-ttu-id="3730b-348">Пример.</span><span class="sxs-lookup"><span data-stu-id="3730b-348">Example:</span></span>

```md
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

<span data-ttu-id="3730b-349">... будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="3730b-349">... will be rendered as:</span></span>

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

<span data-ttu-id="3730b-350">Содержимое на опубликованных страницах будет отображаться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3730b-350">And it will be displayed like this on published pages:</span></span>

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> <span data-ttu-id="3730b-351">URL-адрес видео для канала CH9 должен начинаться с `https` и заканчиваться `/player`.</span><span class="sxs-lookup"><span data-stu-id="3730b-351">The CH9 video URL should start with `https` and end with `/player`.</span></span> <span data-ttu-id="3730b-352">В противном случае будет внедрена вся страница, а не только видео.</span><span class="sxs-lookup"><span data-stu-id="3730b-352">Otherwise, it will embed the whole page instead of the video only.</span></span>

### <a name="uploading-new-videos"></a><span data-ttu-id="3730b-353">Отправка новых видео</span><span class="sxs-lookup"><span data-stu-id="3730b-353">Uploading new videos</span></span>

<span data-ttu-id="3730b-354">Для загрузки новых видео используйте следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="3730b-354">Any new videos should be uploaded using the following process:</span></span>

1. <span data-ttu-id="3730b-355">Присоединитесь к группе **docs_video_users** на портале IDWEB.</span><span class="sxs-lookup"><span data-stu-id="3730b-355">Join the **docs_video_users** group on IDWEB.</span></span>
1. <span data-ttu-id="3730b-356">Перейдите на страницу https://aka.ms/VideoUploadRequest и введите сведения о видеоролике.</span><span class="sxs-lookup"><span data-stu-id="3730b-356">Go to https://aka.ms/VideoUploadRequest and fill in the details for your video.</span></span> <span data-ttu-id="3730b-357">Вам потребуются следующие сведения (ни один из пунктов не будет отображаться для зрителей):</span><span class="sxs-lookup"><span data-stu-id="3730b-357">You will need (note that none of these items will be visible to the public):</span></span>
    1. <span data-ttu-id="3730b-358">название видео;</span><span class="sxs-lookup"><span data-stu-id="3730b-358">A title for your video.</span></span>
    1. <span data-ttu-id="3730b-359">список продуктов или служб, с которыми связано видео;</span><span class="sxs-lookup"><span data-stu-id="3730b-359">A list of products/services that your video is related to.</span></span>
    1. <span data-ttu-id="3730b-360">целевая страница или (если такой страницы еще нет) набор документации, где будет размещаться ваше видео;</span><span class="sxs-lookup"><span data-stu-id="3730b-360">The target page or (if you don’t have the page yet) doc set that your video will be hosted on.</span></span>
    1. <span data-ttu-id="3730b-361">ссылка на файл MP4 видео (если вам некуда отправить файл, можете временно поместить его сюда: `\\scratch2\scratch\apex`)</span><span class="sxs-lookup"><span data-stu-id="3730b-361">A link to the MP4 file for your video (if you don’t have a location to put the file, you can put it here temporarily:   `\\scratch2\scratch\apex`).</span></span> <span data-ttu-id="3730b-362">(разрешение файла MP4 должно быть не менее 720p);</span><span class="sxs-lookup"><span data-stu-id="3730b-362">MP4 files should be 720p or higher.</span></span>
    1. <span data-ttu-id="3730b-363">описание видео.</span><span class="sxs-lookup"><span data-stu-id="3730b-363">A description of the video.</span></span>
1. <span data-ttu-id="3730b-364">Отправьте (сохраните) этот элемент.</span><span class="sxs-lookup"><span data-stu-id="3730b-364">Submit (save) that item.</span></span>
1. <span data-ttu-id="3730b-365">Видео будет выгружено в течение двух рабочих дней.</span><span class="sxs-lookup"><span data-stu-id="3730b-365">Within two business days, the video will get uploaded.</span></span> <span data-ttu-id="3730b-366">Ссылка, необходимая для внедрения, будет помещена в рабочий элемент и *возвращена вам*.</span><span class="sxs-lookup"><span data-stu-id="3730b-366">The link you need for embedding will be placed into the work item, and it will be resolved *back to you*.</span></span>
1. <span data-ttu-id="3730b-367">Получив ссылку на видео, закройте рабочий элемент.</span><span class="sxs-lookup"><span data-stu-id="3730b-367">Once you have grabbed the video link, close the work item.</span></span>
1. <span data-ttu-id="3730b-368">Ссылку на видео можно добавить в публикацию, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="3730b-368">The video link can then be added to your post, using this syntax:</span></span>

   ```md
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
