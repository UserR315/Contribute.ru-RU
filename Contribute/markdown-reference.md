---
title: Справочник по разметке Markdown для docs.microsoft.com
description: Руководство по платформе Docs для Markdown.
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
audience: internal,external
ms.openlocfilehash: 1023f3036e5c1facd0bcd4c31069e6faf3c95483
ms.sourcegitcommit: 21c9ac71e1abff946466cddf17a1ee97bc349ec5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2018
ms.locfileid: "53245879"
---
# <a name="markdown-reference"></a><span data-ttu-id="99f03-103">Справочник по разметке Markdown</span><span class="sxs-lookup"><span data-stu-id="99f03-103">Markdown Reference</span></span>

<span data-ttu-id="99f03-104">Markdown — это облегченный язык разметки с синтаксисом форматирования обычного текста.</span><span class="sxs-lookup"><span data-stu-id="99f03-104">Markdown is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="99f03-105">Платформа Docs поддерживает стандарт CommonMark для Markdown, а также несколько пользовательских расширений Markdown, предоставляющих дополнительное содержимое для docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="99f03-105">The Docs platform supports the CommonMark standard for Markdown, plus some custom Markdown extensions designed to provide richer content on docs.microsoft.com.</span></span> <span data-ttu-id="99f03-106">Эта статья содержит алфавитный справочник по работе с Markdown для docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="99f03-106">This article provides an alphabetical reference for using Markdown for docs.microsoft.com.</span></span>

<span data-ttu-id="99f03-107">Для работы с разметкой Markdown можно использовать любой текстовый редактор.</span><span class="sxs-lookup"><span data-stu-id="99f03-107">You can use any text editor to author Markdown.</span></span> <span data-ttu-id="99f03-108">В качестве редактора, упрощающего вставку стандартного синтаксиса Markdown и пользовательских расширений Docs, рекомендуем использовать [VS Code](https://code.visualstudio.com/) с установленным [пакетом создания документации](https://aka.ms/DocsAuthoringPack).</span><span class="sxs-lookup"><span data-stu-id="99f03-108">For an editor that facilitates inserting both standard Markdown syntax and custom Docs extensions, we recommend [VS Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installed.</span></span>

<span data-ttu-id="99f03-109">Платформа Docs использует модуль Markdig для разметки Markdown.</span><span class="sxs-lookup"><span data-stu-id="99f03-109">Docs uses the Markdig Markdown engine.</span></span> <span data-ttu-id="99f03-110">Сравнить отрисовку разметки Markdown в Markdig с другими обработчиками можно по адресу [https://babelmark.github.io/](https://babelmark.github.io/).</span><span class="sxs-lookup"><span data-stu-id="99f03-110">You can test the rendering of Markdown in Markdig vs. other engines at [https://babelmark.github.io/](https://babelmark.github.io/).</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="99f03-111">Оповещения ("Примечание", "Совет", "Важно!", "Внимание!", "Предупреждение")</span><span class="sxs-lookup"><span data-stu-id="99f03-111">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="99f03-112">Оповещения — это специальные расширения Markdown для платформы Docs, которые используются для создания блоков цитирования, отображаемых на сайте docs.microsoft.com с помощью цветов и значков, указывающих на важность содержимого.</span><span class="sxs-lookup"><span data-stu-id="99f03-112">Alerts are a Docs Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="99f03-113">Поддерживаются следующие типы оповещений:</span><span class="sxs-lookup"><span data-stu-id="99f03-113">The following alert types are supported:</span></span>

```markdown
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

<span data-ttu-id="99f03-114">На сайте docs.microsoft.com эти оповещения отображаются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="99f03-114">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="99f03-115">Информация, которую пользователь должен заметить даже при беглом просмотре.</span><span class="sxs-lookup"><span data-stu-id="99f03-115">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="99f03-116">Дополнительные сведения, помогающие пользователю лучше решить задачу.</span><span class="sxs-lookup"><span data-stu-id="99f03-116">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="99f03-117">Важные сведения для успешного решения задачи.</span><span class="sxs-lookup"><span data-stu-id="99f03-117">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="99f03-118">Потенциальные негативные последствия действия.</span><span class="sxs-lookup"><span data-stu-id="99f03-118">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="99f03-119">Опасные последствия действия.</span><span class="sxs-lookup"><span data-stu-id="99f03-119">Dangerous certain consequences of an action.</span></span>

## <a name="code-snippets"></a><span data-ttu-id="99f03-120">Фрагменты кода</span><span class="sxs-lookup"><span data-stu-id="99f03-120">Code snippets</span></span>

<span data-ttu-id="99f03-121">Вы можете вставить фрагменты кода в свои файлы Markdown:</span><span class="sxs-lookup"><span data-stu-id="99f03-121">You can embed code snippets in your Markdown files:</span></span>

```markdown
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a><span data-ttu-id="99f03-122">Заголовки</span><span class="sxs-lookup"><span data-stu-id="99f03-122">Headings</span></span>

<span data-ttu-id="99f03-123">Платформа Docs поддерживает шесть уровней заголовков Markdown:</span><span class="sxs-lookup"><span data-stu-id="99f03-123">Docs supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="99f03-124">Между последним символом `#` и содержимым заголовка должен присутствовать пробел.</span><span class="sxs-lookup"><span data-stu-id="99f03-124">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="99f03-125">В одном файле Markdown должен быть один и только один заголовок H1.</span><span class="sxs-lookup"><span data-stu-id="99f03-125">Each Markdown file must have one and only one H1.</span></span>
- <span data-ttu-id="99f03-126">Заголовок H1 указывается в файле в первую очередь, сразу после блока метаданных YML.</span><span class="sxs-lookup"><span data-stu-id="99f03-126">The H1 must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="99f03-127">Заголовки H2 автоматически отображаются в правом меню навигации опубликованного файла.</span><span class="sxs-lookup"><span data-stu-id="99f03-127">H2s automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="99f03-128">Это правило не применяется к заголовкам следующих уровней, поэтому для удобства перехода по содержимому рекомендуется использовать заголовки H2.</span><span class="sxs-lookup"><span data-stu-id="99f03-128">Lower-level headings do not, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="99f03-129">Использовать заголовки HMTL, такие как `<h1>`, не рекомендуется, и в некоторых случаях из-за них могут возникать предупреждения при сборке.</span><span class="sxs-lookup"><span data-stu-id="99f03-129">HMTL headings, such as `<h1>`, are not recommended and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="99f03-130">Привязка к отдельным заголовкам в файле выполняется с помощью [закладок](#bookmark-links).</span><span class="sxs-lookup"><span data-stu-id="99f03-130">You can link to individual headings in a file via [bookmarks](#bookmark-links).</span></span>

## <a name="html"></a><span data-ttu-id="99f03-131">HTML</span><span class="sxs-lookup"><span data-stu-id="99f03-131">HTML</span></span>

<span data-ttu-id="99f03-132">Хотя Markdown поддерживает встроенный HTML-код, HTML не рекомендуется использовать для публикации на платформе Docs. Любой код, за исключением ограниченного списка значений, будет вызывать появление ошибок и предупреждений при сборке.</span><span class="sxs-lookup"><span data-stu-id="99f03-132">Although Markdown supports inline HTML, HTML is not recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span> <!--For more information, see HTML Whitelist. // do we want to add the whitelist? -->

## <a name="images"></a><span data-ttu-id="99f03-133">Изображения</span><span class="sxs-lookup"><span data-stu-id="99f03-133">Images</span></span>

<span data-ttu-id="99f03-134">Для включения изображения используется следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="99f03-134">The syntax to include an image is:</span></span>

```markdown
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="99f03-135">Где `alt text` — краткое описание изображения, а `<folder path>` — относительный путь к нему.</span><span class="sxs-lookup"><span data-stu-id="99f03-135">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="99f03-136">Заменяющий текст необходим для средств чтения с экрана для слабовидящих.</span><span class="sxs-lookup"><span data-stu-id="99f03-136">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="99f03-137">Он также удобен при возникновении ошибок на сайте, из-за которых не удается воспроизвести изображение.</span><span class="sxs-lookup"><span data-stu-id="99f03-137">It is also useful if there is a site bug where the image cannot render.</span></span>

<span data-ttu-id="99f03-138">Изображения должны храниться в папке `/media` в наборе документации.</span><span class="sxs-lookup"><span data-stu-id="99f03-138">Images should be stored in a `/media` folder within your doc set.</span></span> <span data-ttu-id="99f03-139">Для изображений по умолчанию поддерживаются следующие типы файлов:</span><span class="sxs-lookup"><span data-stu-id="99f03-139">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="99f03-140">JPG,</span><span class="sxs-lookup"><span data-stu-id="99f03-140">.jpg</span></span>
- <span data-ttu-id="99f03-141">PNG.</span><span class="sxs-lookup"><span data-stu-id="99f03-141">.png</span></span>

<span data-ttu-id="99f03-142">Чтобы добавить поддержку других типов изображений, добавьте их в качестве ресурсов в файл<!--add link to reference when available--> docfx.json для набора документации.</span><span class="sxs-lookup"><span data-stu-id="99f03-142">You can add support for other image types by adding them as resources to the docfx.json file<!--add link to reference when available--> for your doc set.</span></span>

## <a name="links"></a><span data-ttu-id="99f03-143">Создание ссылок</span><span class="sxs-lookup"><span data-stu-id="99f03-143">Links</span></span>

<span data-ttu-id="99f03-144">Как правило, платформа Docs использует стандартные ссылки Markdown на другие файлы и страницы.</span><span class="sxs-lookup"><span data-stu-id="99f03-144">In most cases, Docs uses standard Markdown links to other files and pages.</span></span> <span data-ttu-id="99f03-145">Типы ссылок описываются в подразделах ниже.</span><span class="sxs-lookup"><span data-stu-id="99f03-145">The types of links are described in subsections below.</span></span>

> [!TIP]
> <span data-ttu-id="99f03-146">Пакет создания документации для VS Code помогает правильно вставлять ссылки и закладки в автоматическом режиме.</span><span class="sxs-lookup"><span data-stu-id="99f03-146">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span></span>

> [!IMPORTANT]
> <span data-ttu-id="99f03-147">Не включайте коды языковых стандартов, такие как en-us, в ссылки на сайты Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="99f03-147">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span></span> <span data-ttu-id="99f03-148">Жестко закодированные коды языков блокируют воспроизведение локализованного содержимого: это неудобно для пользователей, говорящих на других языках, и влечет за собой большие затраты на локализацию.</span><span class="sxs-lookup"><span data-stu-id="99f03-148">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span></span> <span data-ttu-id="99f03-149">При копировании URL-адреса из браузера код языка включается по умолчанию, поэтому его необходимо удалить вручную при создании ссылки.</span><span class="sxs-lookup"><span data-stu-id="99f03-149">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link.</span></span> <span data-ttu-id="99f03-150">Например, используйте:</span><span class="sxs-lookup"><span data-stu-id="99f03-150">For example, use:</span></span>
>
> `[Microsoft](https://www.microsoft.com)`
>
> <span data-ttu-id="99f03-151">А не:</span><span class="sxs-lookup"><span data-stu-id="99f03-151">Not:</span></span>
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a><span data-ttu-id="99f03-152">Относительные ссылки на файлы в том же наборе документации</span><span class="sxs-lookup"><span data-stu-id="99f03-152">Relative links to files in the same doc set</span></span>

<span data-ttu-id="99f03-153">Относительный путь — это путь к целевому файлу относительно текущего файла.</span><span class="sxs-lookup"><span data-stu-id="99f03-153">A relative path is the path to the target file relative to the current file.</span></span> <span data-ttu-id="99f03-154">На платформе Docs относительные пути можно использовать для связывания файлов в одном наборе документов.</span><span class="sxs-lookup"><span data-stu-id="99f03-154">In Docs, you can use a relative path to link to another file within the same doc set.</span></span> <span data-ttu-id="99f03-155">Синтаксис относительного пути следующий:</span><span class="sxs-lookup"><span data-stu-id="99f03-155">The syntax for a relative path is as follows:</span></span>

```markdown
[link text](../../folder/filename.md)
```

<span data-ttu-id="99f03-156">Где `../` означает один уровень выше в иерархии.</span><span class="sxs-lookup"><span data-stu-id="99f03-156">Where `../` indicates one level above in the hierarchy.</span></span>

- <span data-ttu-id="99f03-157">Относительный путь будет разрешаться во время сборки, включая удаление расширения MD.</span><span class="sxs-lookup"><span data-stu-id="99f03-157">The relative path will be resolved during the build, including removal of the .md extension.</span></span>
- <span data-ttu-id="99f03-158">Можно использовать "../" для указания на файл в родительской папке, но этот файл должен быть в том же наборе документации.</span><span class="sxs-lookup"><span data-stu-id="99f03-158">You can use "../" to link to a file in the parent folder, but that file has to be in the same doc set.</span></span> <span data-ttu-id="99f03-159">"../" нельзя использовать для указания на файл в другой папке набора документации.</span><span class="sxs-lookup"><span data-stu-id="99f03-159">You cannot use "../" to link to a file in another doc set folder.</span></span>
- <span data-ttu-id="99f03-160">Платформа Docs также поддерживает особый формат относительного пути, начинающийся с символа "~" (например, ~/foo/bar.md).</span><span class="sxs-lookup"><span data-stu-id="99f03-160">Docs also supports a special form of relative path that starts with "~" (for example, ~/foo/bar.md).</span></span> <span data-ttu-id="99f03-161">Этот синтаксис указывает файл относительно корневой папки набора документации.</span><span class="sxs-lookup"><span data-stu-id="99f03-161">This syntax indicates a file relative to the root folder of a doc set.</span></span> <span data-ttu-id="99f03-162">Этот вид пути также проверяется и разрешается во время сборки.</span><span class="sxs-lookup"><span data-stu-id="99f03-162">This kind of path is also validated and resolved during the build.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="99f03-163">Включите расширение файла в относительный путь.</span><span class="sxs-lookup"><span data-stu-id="99f03-163">Include the file extension in the relative path.</span></span> <span data-ttu-id="99f03-164">В ходе сборки проверяется существование целевого файла по этому относительному пути.</span><span class="sxs-lookup"><span data-stu-id="99f03-164">Build validates the existence of the target file of that relative path.</span></span> <span data-ttu-id="99f03-165">Если относительный путь не включает расширение файла, в ходе сборки, скорее всего, будет создано предупреждение или неработающая ссылка.</span><span class="sxs-lookup"><span data-stu-id="99f03-165">If relative path does not include file extension, it is likely build will report a warning of broken link.</span></span> <span data-ttu-id="99f03-166">Например, используйте:</span><span class="sxs-lookup"><span data-stu-id="99f03-166">For example, use:</span></span>
>
> `[link text](../../folder/filename.md)`
>
> <span data-ttu-id="99f03-167">А не:</span><span class="sxs-lookup"><span data-stu-id="99f03-167">Not:</span></span>
>
> `[link text](../../folder/filename)`

### <a name="site-relative-links-to-other-files-on-docs"></a><span data-ttu-id="99f03-168">Относительные ссылки на другие файлы на платформе Docs на сайте</span><span class="sxs-lookup"><span data-stu-id="99f03-168">Site relative links to other files on Docs</span></span>

```markdown
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

<span data-ttu-id="99f03-169">Не включайте расширение файла (MD).</span><span class="sxs-lookup"><span data-stu-id="99f03-169">Do not include the file extension (.md).</span></span> <span data-ttu-id="99f03-170">Это ссылка на обзорный файл Linux за пределами набора документации "статей" Azure.</span><span class="sxs-lookup"><span data-stu-id="99f03-170">This links to the Linux overview file from outside the Azure "articles" doc set.</span></span>

### <a name="links-to-external-sites"></a><span data-ttu-id="99f03-171">Ссылки на внешние сайты</span><span class="sxs-lookup"><span data-stu-id="99f03-171">Links to external sites</span></span>

```markdown
[Microsoft](https://www.microsoft.com)
```

<span data-ttu-id="99f03-172">Ссылка на основе URL-адреса на другую веб-страницу (должна включать https://).</span><span class="sxs-lookup"><span data-stu-id="99f03-172">URL-based link to another web page (must include https://).</span></span>

### <a name="bookmark-links"></a><span data-ttu-id="99f03-173">Ссылки закладок</span><span class="sxs-lookup"><span data-stu-id="99f03-173">Bookmark links</span></span>

<span data-ttu-id="99f03-174">Ссылка-закладка на заголовок в другом файле в том же репозитории:</span><span class="sxs-lookup"><span data-stu-id="99f03-174">Bookmark link to a heading in another file in the same repo:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="99f03-175">Ссылка-закладка на заголовок в текущем файле:</span><span class="sxs-lookup"><span data-stu-id="99f03-175">Bookmark link to a heading in the current file:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="99f03-176">Используйте хэш-тег, за которым следуют слова заголовка: без знаков препинания, пробелы заменяются дефисами.</span><span class="sxs-lookup"><span data-stu-id="99f03-176">Use a hash tag followed by the words of the heading with punctuation removed and spaces replaced with dashes.</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="99f03-177">Явные ссылки привязки</span><span class="sxs-lookup"><span data-stu-id="99f03-177">Explicit anchor links</span></span>

<span data-ttu-id="99f03-178">Явные ссылки привязки, использующие HTML-тег `<a>` **не требуются и не рекомендуются**, за исключением страниц-концентраторов и целевых страниц.</span><span class="sxs-lookup"><span data-stu-id="99f03-178">Explicit anchor links using the `<a>` HTML tag are **not required or recommended** except in hub and landing pages.</span></span> <span data-ttu-id="99f03-179">Используйте закладки, как описано выше, в общих файлах Markdown.</span><span class="sxs-lookup"><span data-stu-id="99f03-179">Use bookmarks as described above in general Markdown files.</span></span> <span data-ttu-id="99f03-180">Для страниц-концентраторов и целевых страниц привязки используются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="99f03-180">For hub and landing pages, use anchors as follows:</span></span>

<span data-ttu-id="99f03-181">`## <a id="AnchorText"> </a>Header text` или `## <a name="AnchorText"> </a>Header text`</span><span class="sxs-lookup"><span data-stu-id="99f03-181">`## <a id="AnchorText"> </a>Header text` or `## <a name="AnchorText"> </a>Header text`</span></span>

<span data-ttu-id="99f03-182">Для ссылки на явные привязки используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="99f03-182">To link to explicit anchors, use the following syntax:</span></span>

```markdown
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a><span data-ttu-id="99f03-183">Ссылки XREF (перекрестные ссылки)</span><span class="sxs-lookup"><span data-stu-id="99f03-183">XREF (cross reference) links</span></span>

<span data-ttu-id="99f03-184">Для ссылки на автоматически создаваемые страницы справочных материалов по API в текущем или другом наборе документации используйте ссылки XREF с уникальным идентификатором (UID).</span><span class="sxs-lookup"><span data-stu-id="99f03-184">To link to auto-generated API references pages in the current doc set or other doc sets, use XREF links with the unique ID (UID).</span></span>

> [!NOTE]
> <span data-ttu-id="99f03-185">Для ссылки на страницы справочных материалов по API в других наборах документации потребуется добавить конфигурацию `xrefService` в файл `docfx.json`.</span><span class="sxs-lookup"><span data-stu-id="99f03-185">To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.</span></span>
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

<span data-ttu-id="99f03-186">Уникальный идентификатор совпадает с полным именем класса и члена.</span><span class="sxs-lookup"><span data-stu-id="99f03-186">The UID equates to the fully qualified class and member name.</span></span> <span data-ttu-id="99f03-187">Если добавить символ \* после UID, ссылка будет вести на страницу перегрузки, а не к конкретному API.</span><span class="sxs-lookup"><span data-stu-id="99f03-187">If you add a \* after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="99f03-188">Например, используйте `List<T>.BinarySearch*` для ссылки на страницу "Метод BinarySearch" вместо ссылки на конкретную перегрузку, например `List<T>.BinarySearch(T, IComparer<T>)`.</span><span class="sxs-lookup"><span data-stu-id="99f03-188">For example, use `List<T>.BinarySearch*` to link to the BinarySearch Method page instead of linking to a specific overload such as `List<T>.BinarySearch(T, IComparer<T>)`.</span></span>

<span data-ttu-id="99f03-189">Можно выбрать один из следующих вариантов синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="99f03-189">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="99f03-190">Автоматическая ссылка: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="99f03-190">Auto-link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span></span>

  <span data-ttu-id="99f03-191">Необязательный параметр запроса `displayProperty` создает полный текст ссылки.</span><span class="sxs-lookup"><span data-stu-id="99f03-191">The optional `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="99f03-192">По умолчанию в тексте ссылки отображается только имя члена или типа.</span><span class="sxs-lookup"><span data-stu-id="99f03-192">By default, link text shows only the member or type name.</span></span>

- <span data-ttu-id="99f03-193">Ссылка с разметкой Markdown: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="99f03-193">Markdown link: `[link text](xref:UID)`</span></span>
  
  <span data-ttu-id="99f03-194">Используется, когда требуется настроить текст ссылки.</span><span class="sxs-lookup"><span data-stu-id="99f03-194">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="99f03-195">Примеры:</span><span class="sxs-lookup"><span data-stu-id="99f03-195">Examples:</span></span>

- <span data-ttu-id="99f03-196">`<xref:System.String>` отображается как String;</span><span class="sxs-lookup"><span data-stu-id="99f03-196">`<xref:System.String>` renders as "String".</span></span>
- <span data-ttu-id="99f03-197">`<xref:System.String?displayProperty=nameWithType>` отображается как System.String;</span><span class="sxs-lookup"><span data-stu-id="99f03-197">`<xref:System.String?displayProperty=nameWithType>` renders as "System.String".</span></span>
- <span data-ttu-id="99f03-198">`[String class](xref:System.String)` отображается как String class.</span><span class="sxs-lookup"><span data-stu-id="99f03-198">`[String class](xref:System.String)` renders as "String class".</span></span>

<span data-ttu-id="99f03-199">Сейчас не существует простого способа поиска UID.</span><span class="sxs-lookup"><span data-stu-id="99f03-199">Right now, there is no easy way to find the UIDs.</span></span> <span data-ttu-id="99f03-200"><!-- ? -->Чтобы найти UID для API, просмотрите исходный код страницы API, на которую нужно создать ссылку, и найдите значение ms.assetid.</span><span class="sxs-lookup"><span data-stu-id="99f03-200"><!-- ? -->The best way to find the UID for an API is to view the source for the API page you want to link to and find the ms.assetid value.</span></span> <span data-ttu-id="99f03-201">Отдельные значения перегрузки не отображаются в исходном коде.</span><span class="sxs-lookup"><span data-stu-id="99f03-201">Individual overload values are not shown in the source.</span></span> <span data-ttu-id="99f03-202">Мы работаем над улучшением нашей системы.</span><span class="sxs-lookup"><span data-stu-id="99f03-202">We're working on having a better system in the future.</span></span>

<span data-ttu-id="99f03-203">Если идентификатор содержит специальные символы \`, \# или \*, значение UID должно быть закодировано в HTML как `%60`, `%23` и `%2A` соответственно.</span><span class="sxs-lookup"><span data-stu-id="99f03-203">When the UID contains the special characters \`, \#, or \*, the UID value needs to be HTML encoded as `%60`, `%23`, and `%2A`, respectively.</span></span> <span data-ttu-id="99f03-204">Иногда круглые скобки тоже кодируются, но это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="99f03-204">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="99f03-205">Примеры:</span><span class="sxs-lookup"><span data-stu-id="99f03-205">Examples:</span></span>

- <span data-ttu-id="99f03-206">System.Threading.Tasks.Task\`1 заменяется на `System.Threading.Tasks.Task%601`;</span><span class="sxs-lookup"><span data-stu-id="99f03-206">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="99f03-207">System.Exception.\#ctor заменяется на `System.Exception.%23ctor`;</span><span class="sxs-lookup"><span data-stu-id="99f03-207">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="99f03-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) заменяется на `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`.</span><span class="sxs-lookup"><span data-stu-id="99f03-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="99f03-209">Списки (нумерованные, маркированные, контрольные)</span><span class="sxs-lookup"><span data-stu-id="99f03-209">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="99f03-210">Нумерованный список</span><span class="sxs-lookup"><span data-stu-id="99f03-210">Numbered list</span></span>

<span data-ttu-id="99f03-211">Для создания нумерованного списка можно использовать все 1, которые при публикации отображаются как последовательный список.</span><span class="sxs-lookup"><span data-stu-id="99f03-211">To create a numbered list, you can use all 1s, which are rendered as a sequential list when published.</span></span> <span data-ttu-id="99f03-212">Для повышения удобства чтения исходного кода списки можно вводить с приращением.</span><span class="sxs-lookup"><span data-stu-id="99f03-212">For increased source readability, you can increment your lists.</span></span>

<span data-ttu-id="99f03-213">Не используйте в списках, включая вложенные списки, буквы.</span><span class="sxs-lookup"><span data-stu-id="99f03-213">Do not use letters in lists, including nested lists.</span></span> <span data-ttu-id="99f03-214">При публикации на платформе Docs они преобразуются некорректно. Вложенные списки с цифрами преобразуются в списки со строчными буквами при публикации.</span><span class="sxs-lookup"><span data-stu-id="99f03-214">They do not render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="99f03-215">Например:</span><span class="sxs-lookup"><span data-stu-id="99f03-215">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="99f03-216">Это отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="99f03-216">This renders as follows:</span></span>

1. <span data-ttu-id="99f03-217">Это</span><span class="sxs-lookup"><span data-stu-id="99f03-217">This is</span></span>
1. <span data-ttu-id="99f03-218">родительский нумерованный список,</span><span class="sxs-lookup"><span data-stu-id="99f03-218">a parent numbered list</span></span>
   1. <span data-ttu-id="99f03-219">а это</span><span class="sxs-lookup"><span data-stu-id="99f03-219">and this is</span></span>
   1. <span data-ttu-id="99f03-220">вложенный нумерованный список</span><span class="sxs-lookup"><span data-stu-id="99f03-220">a nested numbered list</span></span>
1. <span data-ttu-id="99f03-221">(конец)</span><span class="sxs-lookup"><span data-stu-id="99f03-221">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="99f03-222">Маркированный список</span><span class="sxs-lookup"><span data-stu-id="99f03-222">Bulleted list</span></span>

<span data-ttu-id="99f03-223">Для создания маркированного списка используйте `-`, за которым следует пробел в начале каждой строки.</span><span class="sxs-lookup"><span data-stu-id="99f03-223">To create a bulleted list, use `-` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="99f03-224">Это отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="99f03-224">This renders as follows:</span></span>

- <span data-ttu-id="99f03-225">Это</span><span class="sxs-lookup"><span data-stu-id="99f03-225">This is</span></span>
- <span data-ttu-id="99f03-226">родительский маркированный список,</span><span class="sxs-lookup"><span data-stu-id="99f03-226">a parent bulleted list</span></span>
  - <span data-ttu-id="99f03-227">а это</span><span class="sxs-lookup"><span data-stu-id="99f03-227">and this is</span></span>
  - <span data-ttu-id="99f03-228">вложенный маркированный список</span><span class="sxs-lookup"><span data-stu-id="99f03-228">a nested bulleted list</span></span>
- <span data-ttu-id="99f03-229">Готово!</span><span class="sxs-lookup"><span data-stu-id="99f03-229">All done!</span></span>

### <a name="checklist"></a><span data-ttu-id="99f03-230">Контрольный список</span><span class="sxs-lookup"><span data-stu-id="99f03-230">Checklist</span></span>

<span data-ttu-id="99f03-231">Контрольные списки можно использовать (только) на сайте docs.microsoft.com с помощью пользовательского расширения Markdown:</span><span class="sxs-lookup"><span data-stu-id="99f03-231">Checklists are available for use on docs.microsoft.com (only) via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="99f03-232">Этот пример отображается на сайте docs.microsoft.com следующим образом:</span><span class="sxs-lookup"><span data-stu-id="99f03-232">This example renders on docs.microsoft.com like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="99f03-233">List item 1</span><span class="sxs-lookup"><span data-stu-id="99f03-233">List item 1</span></span>
> * <span data-ttu-id="99f03-234">List item 2</span><span class="sxs-lookup"><span data-stu-id="99f03-234">List item 2</span></span>
> * <span data-ttu-id="99f03-235">List item 3</span><span class="sxs-lookup"><span data-stu-id="99f03-235">List item 3</span></span>

<span data-ttu-id="99f03-236">Контрольные списки используются в начале или конце статьи для подведения итогов "Чему вы научитесь" или "Чему вы научились".</span><span class="sxs-lookup"><span data-stu-id="99f03-236">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="99f03-237">Не вставляйте контрольные списки в статьи по случайному принципу.</span><span class="sxs-lookup"><span data-stu-id="99f03-237">Do not add random checklists throughout your articles.</span></span>
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a><span data-ttu-id="99f03-238">Действие "Дальнейшие действия"</span><span class="sxs-lookup"><span data-stu-id="99f03-238">Next step action</span></span>

<span data-ttu-id="99f03-239">Пользовательское расширение можно использовать для добавления кнопки "Дальнейшие действия" на страницы (только) docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="99f03-239">You can use a custom extension to add a next step action button to pages on docs.microsoft.com (only).</span></span>

<span data-ttu-id="99f03-240">Используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="99f03-240">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="99f03-241">Например:</span><span class="sxs-lookup"><span data-stu-id="99f03-241">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

<span data-ttu-id="99f03-242">Это отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="99f03-242">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="99f03-243">Подробнее о базовом стиле</span><span class="sxs-lookup"><span data-stu-id="99f03-243">Learn about basic style</span></span>](style-quick-start.md)

<span data-ttu-id="99f03-244">Вы можете использовать любые поддерживаемые ссылки в действии "Дальнейшие действия", включая ссылку Markdown на другую веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="99f03-244">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="99f03-245">Как правило, ссылка "Дальнейшие действия" — это относительная ссылка на другой файл в том же наборе документации.</span><span class="sxs-lookup"><span data-stu-id="99f03-245">In most cases, the next action link will be a relative link to another file in the same doc set.</span></span>

## <a name="section-definition"></a><span data-ttu-id="99f03-246">Определение раздела</span><span class="sxs-lookup"><span data-stu-id="99f03-246">Section definition</span></span>

<span data-ttu-id="99f03-247"><!-- more info about this would be helpful! --> Вам может потребоваться определить раздел.</span><span class="sxs-lookup"><span data-stu-id="99f03-247"><!-- more info about this would be helpful! --> You might need to define a section.</span></span> <span data-ttu-id="99f03-248">Этот синтаксис в основном используется для таблиц кодов.</span><span class="sxs-lookup"><span data-stu-id="99f03-248">This syntax is mostly used for code tables.</span></span>
<span data-ttu-id="99f03-249">См. указанный ниже пример.</span><span class="sxs-lookup"><span data-stu-id="99f03-249">See the following example:</span></span>

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

<span data-ttu-id="99f03-250">Предыдущий текст Markdown будет отображаться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="99f03-250">The preceding blockquote Markdown text will be rendered as:</span></span>
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a><span data-ttu-id="99f03-251">Селекторы</span><span class="sxs-lookup"><span data-stu-id="99f03-251">Selectors</span></span>

<span data-ttu-id="99f03-252"><!-- could be more clear! --> Селектор можно использовать, когда требуется связать различные страницы одной статьи.</span><span class="sxs-lookup"><span data-stu-id="99f03-252"><!-- could be more clear! --> You can use a selector when you want to connect different pages for the same article.</span></span> <span data-ttu-id="99f03-253">Затем читатели смогут переключаться между этими страницами.</span><span class="sxs-lookup"><span data-stu-id="99f03-253">Readers can then switch between those pages.</span></span>

> [!NOTE]
> <span data-ttu-id="99f03-254">Это расширение функционирует по-разному на сайтах docs.microsoft.com и MSDN.</span><span class="sxs-lookup"><span data-stu-id="99f03-254">This extension works differently between docs.microsoft.com and MSDN.</span></span> <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a><span data-ttu-id="99f03-255">Единичный выбор</span><span class="sxs-lookup"><span data-stu-id="99f03-255">Single selector</span></span>

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

<span data-ttu-id="99f03-256">... будет иметь следующий вид:</span><span class="sxs-lookup"><span data-stu-id="99f03-256">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Универсальные приложения Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a><span data-ttu-id="99f03-265">Множественный выбор</span><span class="sxs-lookup"><span data-stu-id="99f03-265">Multi-selector</span></span>

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

<span data-ttu-id="99f03-266">... будет иметь следующий вид:</span><span class="sxs-lookup"><span data-stu-id="99f03-266">... will be rendered like this:</span></span>

> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
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

## <a name="tables"></a><span data-ttu-id="99f03-277">Tables</span><span class="sxs-lookup"><span data-stu-id="99f03-277">Tables</span></span>

<span data-ttu-id="99f03-278">Использование вертикальных линий и строк является самым простым способом создания таблиц в Markdown.</span><span class="sxs-lookup"><span data-stu-id="99f03-278">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="99f03-279">Чтобы создать стандартную таблицу с заголовком, вставьте пунктирную линию после первой строки.</span><span class="sxs-lookup"><span data-stu-id="99f03-279">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="99f03-280">Это отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="99f03-280">This renders as follows:</span></span>

|<span data-ttu-id="99f03-281">Это</span><span class="sxs-lookup"><span data-stu-id="99f03-281">This is</span></span>   |<span data-ttu-id="99f03-282">просто</span><span class="sxs-lookup"><span data-stu-id="99f03-282">a simple</span></span>   |<span data-ttu-id="99f03-283">заголовок таблицы</span><span class="sxs-lookup"><span data-stu-id="99f03-283">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="99f03-284">данные</span><span class="sxs-lookup"><span data-stu-id="99f03-284">table</span></span>     |<span data-ttu-id="99f03-285">таблицы</span><span class="sxs-lookup"><span data-stu-id="99f03-285">data</span></span>       |<span data-ttu-id="99f03-286">здесь</span><span class="sxs-lookup"><span data-stu-id="99f03-286">here</span></span>        |
|<span data-ttu-id="99f03-287">вообще-то</span><span class="sxs-lookup"><span data-stu-id="99f03-287">it doesn't</span></span>|<span data-ttu-id="99f03-288">не всегда</span><span class="sxs-lookup"><span data-stu-id="99f03-288">actually</span></span>   |<span data-ttu-id="99f03-289">отображаются аккуратно!</span><span class="sxs-lookup"><span data-stu-id="99f03-289">have to line up nicely!</span></span>||

<span data-ttu-id="99f03-290">Можно также создать таблицу без заголовка.</span><span class="sxs-lookup"><span data-stu-id="99f03-290">You can also create a table without a header.</span></span> <span data-ttu-id="99f03-291">Например, чтобы создать список с несколькими столбцами:</span><span class="sxs-lookup"><span data-stu-id="99f03-291">For example, to create a multiple-column list:</span></span>

```markdown
|   |   |
| - | - |
| This | table |
| has no | header |
```

<span data-ttu-id="99f03-292">Это отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="99f03-292">This renders like this:</span></span>

|   |   |
| - | - |
| <span data-ttu-id="99f03-293">Это</span><span class="sxs-lookup"><span data-stu-id="99f03-293">This</span></span> | <span data-ttu-id="99f03-294">таблица</span><span class="sxs-lookup"><span data-stu-id="99f03-294">table</span></span> |
| <span data-ttu-id="99f03-295">без</span><span class="sxs-lookup"><span data-stu-id="99f03-295">has no</span></span> | <span data-ttu-id="99f03-296">заголовка</span><span class="sxs-lookup"><span data-stu-id="99f03-296">header</span></span> |

<span data-ttu-id="99f03-297">Можно выровнять столбцы с помощью двоеточий:</span><span class="sxs-lookup"><span data-stu-id="99f03-297">You can align the columns by using colons:</span></span>

```markdown
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

<span data-ttu-id="99f03-298">Отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="99f03-298">Renders as follows:</span></span>

|                  |
|------------------|
|    <span data-ttu-id="99f03-299">по правому краю:</span><span class="sxs-lookup"><span data-stu-id="99f03-299">right aligned:</span></span>|
|<span data-ttu-id="99f03-300">:по левому краю</span><span class="sxs-lookup"><span data-stu-id="99f03-300">:left aligned</span></span>     |
|<span data-ttu-id="99f03-301">:по центру            :</span><span class="sxs-lookup"><span data-stu-id="99f03-301">:centered        :</span></span>|

> [!TIP]
> Расширение создания документации для VS Code упрощает добавление базовых таблиц Markdown.
>
> Кроме того, можно использовать [веб-инструмент создания таблиц](http://www.tablesgenerator.com/markdown_tables).

### <a name="mx-tdbreakall"></a><span data-ttu-id="99f03-304">mx-tdBreakAll</span><span class="sxs-lookup"><span data-stu-id="99f03-304">mx-tdBreakAll</span></span>

> [!IMPORTANT]
> Эта функция работает только на веб-сайте docs.microsoft.com.

<span data-ttu-id="99f03-306">Создаваемая в Markdown таблица может выходить вправо, что делает ее нечитаемой.</span><span class="sxs-lookup"><span data-stu-id="99f03-306">If you create a table in Markdown, the table might expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="99f03-307">Эту проблему можно устранить, разрешив при необходимости разрыв таблицы при отображении документов.</span><span class="sxs-lookup"><span data-stu-id="99f03-307">You can solve that by allowing Docs rendering to break the table when needed.</span></span> <span data-ttu-id="99f03-308">Нужно просто заключить таблицу в настраиваемый класс `[!div class="mx-tdBreakAll"]`.</span><span class="sxs-lookup"><span data-stu-id="99f03-308">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="99f03-309">Далее приведен пример Markdown таблицы с тремя строками, которая будет заключена с помощью `div` с классом `mx-tdBreakAll`.</span><span class="sxs-lookup"><span data-stu-id="99f03-309">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="99f03-310">Она будет иметь следующий вид:</span><span class="sxs-lookup"><span data-stu-id="99f03-310">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="99f03-311">Имя</span><span class="sxs-lookup"><span data-stu-id="99f03-311">Name</span></span>|<span data-ttu-id="99f03-312">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99f03-312">Syntax</span></span>|<span data-ttu-id="99f03-313">Обязательно для автоматический установки?</span><span class="sxs-lookup"><span data-stu-id="99f03-313">Mandatory for silent installation?</span></span>|<span data-ttu-id="99f03-314">Описание</span><span class="sxs-lookup"><span data-stu-id="99f03-314">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="99f03-315">Quiet</span><span class="sxs-lookup"><span data-stu-id="99f03-315">Quiet</span></span>|<span data-ttu-id="99f03-316">/quiet</span><span class="sxs-lookup"><span data-stu-id="99f03-316">/quiet</span></span>|<span data-ttu-id="99f03-317">Да</span><span class="sxs-lookup"><span data-stu-id="99f03-317">Yes</span></span>|<span data-ttu-id="99f03-318">Запускает установщик без отображения пользовательского интерфейса и запросов.</span><span class="sxs-lookup"><span data-stu-id="99f03-318">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="99f03-319">NoRestart</span><span class="sxs-lookup"><span data-stu-id="99f03-319">NoRestart</span></span>|<span data-ttu-id="99f03-320">/norestart</span><span class="sxs-lookup"><span data-stu-id="99f03-320">/norestart</span></span>|<span data-ttu-id="99f03-321">Нет</span><span class="sxs-lookup"><span data-stu-id="99f03-321">No</span></span>|<span data-ttu-id="99f03-322">Подавляет попытки перезапуска.</span><span class="sxs-lookup"><span data-stu-id="99f03-322">Suppresses any attempts to restart.</span></span> <span data-ttu-id="99f03-323">По умолчанию пользовательский интерфейс выведет запрос перед перезапуском.</span><span class="sxs-lookup"><span data-stu-id="99f03-323">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="99f03-324">Help</span><span class="sxs-lookup"><span data-stu-id="99f03-324">Help</span></span>|<span data-ttu-id="99f03-325">/help</span><span class="sxs-lookup"><span data-stu-id="99f03-325">/help</span></span>|<span data-ttu-id="99f03-326">Нет</span><span class="sxs-lookup"><span data-stu-id="99f03-326">No</span></span>|<span data-ttu-id="99f03-327">Предоставляет справку и краткие инструкции.</span><span class="sxs-lookup"><span data-stu-id="99f03-327">Provides help and quick reference.</span></span> <span data-ttu-id="99f03-328">Отображает правильное использование команды setup, включая список всех параметров и вариантов поведения.</span><span class="sxs-lookup"><span data-stu-id="99f03-328">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="mx-tdcol2breakall"></a><span data-ttu-id="99f03-329">mx-tdCol2BreakAll</span><span class="sxs-lookup"><span data-stu-id="99f03-329">mx-tdCol2BreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="99f03-330">Эта функция работает только на веб-сайте docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="99f03-330">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="99f03-331">Время от времени во втором столбце таблицы могут находиться очень длинные слова.</span><span class="sxs-lookup"><span data-stu-id="99f03-331">From time to time, you might have very long words in the second column of a table.</span></span> <span data-ttu-id="99f03-332">Чтобы правильно разделить эти слова, можно применить класс `mx-tdCol2BreakAll` с помощью синтаксиса оболочки `div`, как показано выше.</span><span class="sxs-lookup"><span data-stu-id="99f03-332">To ensure they are broken apart nicely, you can apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="html-tables"></a><span data-ttu-id="99f03-333">Таблицы HTML</span><span class="sxs-lookup"><span data-stu-id="99f03-333">HTML Tables</span></span>

<span data-ttu-id="99f03-334">Таблицы HTML не рекомендуется использовать для docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="99f03-334">HTML tables are not recommended for docs.microsoft.com.</span></span> <span data-ttu-id="99f03-335">Они трудны для восприятия в исходном виде — это нарушает основной принцип Markdown.</span><span class="sxs-lookup"><span data-stu-id="99f03-335">They are not human readable in the source - which is a key principle of Markdown.</span></span>

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a><span data-ttu-id="99f03-336">Видеоролики</span><span class="sxs-lookup"><span data-stu-id="99f03-336">Videos</span></span>

### <a name="embedding-videos-into-a-markdown-page"></a><span data-ttu-id="99f03-337">Внедрение видео на страницу Markdown</span><span class="sxs-lookup"><span data-stu-id="99f03-337">Embedding videos into a Markdown page</span></span>

<span data-ttu-id="99f03-338">Сейчас платформа Docs поддерживает видеоролики, опубликованные в одной из трех платформ:</span><span class="sxs-lookup"><span data-stu-id="99f03-338">Currently, Docs can support videos published to one of three locations:</span></span>

- <span data-ttu-id="99f03-339">YouTube</span><span class="sxs-lookup"><span data-stu-id="99f03-339">YouTube</span></span>
- <span data-ttu-id="99f03-340">Channel 9</span><span class="sxs-lookup"><span data-stu-id="99f03-340">Channel 9</span></span>
- <span data-ttu-id="99f03-341">собственной системе Майкрософт One Player.</span><span class="sxs-lookup"><span data-stu-id="99f03-341">Microsoft's own 'One Player' system</span></span>

<span data-ttu-id="99f03-342">Вы можете встроить видео с помощью следующего синтаксиса, и это видео будет отображено на платформе Docs.</span><span class="sxs-lookup"><span data-stu-id="99f03-342">You can embed a video with the following syntax, and Docs will render it.</span></span>

```markdown
> [!VIDEO <embedded_video_link>]
```

<span data-ttu-id="99f03-343">Пример.</span><span class="sxs-lookup"><span data-stu-id="99f03-343">Example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

<span data-ttu-id="99f03-344">... будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="99f03-344">... will be rendered as:</span></span>

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

<span data-ttu-id="99f03-345">Содержимое на опубликованных страницах будет отображаться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="99f03-345">And it will be displayed like this on published pages:</span></span>

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> <span data-ttu-id="99f03-346">URL-адрес видео для канала CH9 должен начинаться с `https` и заканчиваться `/player`.</span><span class="sxs-lookup"><span data-stu-id="99f03-346">The CH9 video URL should start with `https` and end with `/player`.</span></span> <span data-ttu-id="99f03-347">В противном случае будет внедрена вся страница, а не только видео.</span><span class="sxs-lookup"><span data-stu-id="99f03-347">Otherwise, it will embed the whole page instead of the video only.</span></span>

### <a name="uploading-new-videos"></a><span data-ttu-id="99f03-348">Отправка новых видео</span><span class="sxs-lookup"><span data-stu-id="99f03-348">Uploading new videos</span></span>

<span data-ttu-id="99f03-349">Для загрузки новых видео используйте следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="99f03-349">Any new videos should be uploaded using the following process:</span></span>

1. <span data-ttu-id="99f03-350">Присоединитесь к группе **docs_video_users** на портале IDWEB.</span><span class="sxs-lookup"><span data-stu-id="99f03-350">Join the **docs_video_users** group on IDWEB.</span></span>
1. <span data-ttu-id="99f03-351">Перейдите на страницу https://aka.ms/VideoUploadRequest и введите сведения о видеоролике.</span><span class="sxs-lookup"><span data-stu-id="99f03-351">Go to https://aka.ms/VideoUploadRequest and fill in the details for your video.</span></span> <span data-ttu-id="99f03-352">Вам потребуются следующие сведения (ни один из пунктов не будет отображаться для зрителей):</span><span class="sxs-lookup"><span data-stu-id="99f03-352">You will need (note that none of these items will be visible to the public):</span></span>
    1. <span data-ttu-id="99f03-353">название видео;</span><span class="sxs-lookup"><span data-stu-id="99f03-353">A title for your video.</span></span>
    1. <span data-ttu-id="99f03-354">список продуктов или служб, с которыми связано видео;</span><span class="sxs-lookup"><span data-stu-id="99f03-354">A list of products/services that your video is related to.</span></span>
    1. <span data-ttu-id="99f03-355">целевая страница или (если такой страницы еще нет) набор документации, где будет размещаться ваше видео;</span><span class="sxs-lookup"><span data-stu-id="99f03-355">The target page or (if you don’t have the page yet) doc set that your video will be hosted on.</span></span>
    1. <span data-ttu-id="99f03-356">ссылка на файл MP4 видео (если вам некуда отправить файл, можете временно поместить его сюда: `\\scratch2\scratch\apex`)</span><span class="sxs-lookup"><span data-stu-id="99f03-356">A link to the MP4 file for your video (if you don’t have a location to put the file, you can put it here temporarily:   `\\scratch2\scratch\apex`).</span></span> <span data-ttu-id="99f03-357">(разрешение файла MP4 должно быть не менее 720p);</span><span class="sxs-lookup"><span data-stu-id="99f03-357">MP4 files should be 720p or higher.</span></span>
    1. <span data-ttu-id="99f03-358">описание видео.</span><span class="sxs-lookup"><span data-stu-id="99f03-358">A description of the video.</span></span>
1. <span data-ttu-id="99f03-359">Отправьте (сохраните) этот элемент.</span><span class="sxs-lookup"><span data-stu-id="99f03-359">Submit (save) that item.</span></span>
1. <span data-ttu-id="99f03-360">Видео будет выгружено в течение двух рабочих дней.</span><span class="sxs-lookup"><span data-stu-id="99f03-360">Within two business days, the video will get uploaded.</span></span> <span data-ttu-id="99f03-361">Ссылка, необходимая для внедрения, будет помещена в рабочий элемент и *возвращена вам*.</span><span class="sxs-lookup"><span data-stu-id="99f03-361">The link you need for embedding will be placed into the work item, and it will be resolved *back to you*.</span></span>
1. <span data-ttu-id="99f03-362">Получив ссылку на видео, закройте рабочий элемент.</span><span class="sxs-lookup"><span data-stu-id="99f03-362">Once you have grabbed the video link, close the work item.</span></span>
1. <span data-ttu-id="99f03-363">Ссылку на видео можно добавить в публикацию, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="99f03-363">The video link can then be added to your post, using this syntax:</span></span>

   ```markdown
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
