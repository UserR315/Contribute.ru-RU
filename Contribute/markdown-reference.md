---
title: Справочник по разметке Markdown для OPS и docs.microsoft.com
description: Руководство по использованию расширений Markdown и DocFX Flavored Markdown (DFM) на платформе OPS.
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
audience: internal,external
ms.openlocfilehash: 64921bacf48e638221048db4b24e1a941f1d2777
ms.sourcegitcommit: 44eb4f5ee65c1848d7f36fca107b296eb7687397
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/13/2018
ms.locfileid: "51609552"
---
# <a name="markdown-reference-for-ops"></a><span data-ttu-id="a710c-103">Справочник по разметке Markdown для OPS</span><span class="sxs-lookup"><span data-stu-id="a710c-103">Markdown Reference for OPS</span></span>

<span data-ttu-id="a710c-104">Markdown — это облегченный язык разметки с синтаксисом форматирования обычного текста.</span><span class="sxs-lookup"><span data-stu-id="a710c-104">Markdown is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="a710c-105">Платформа OPS поддерживает стандарт CommonMark для Markdown, а также несколько пользовательских расширений Markdown, обеспечивающих дополнительное содержимое для docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="a710c-105">Open Publishing Services (OPS) supports the CommonMark standard for Markdown, plus some custom Markdown extensions designed to provide richer content on docs.microsoft.com.</span></span> <span data-ttu-id="a710c-106">Эта статья содержит алфавитный справочник по работе с Markdown в OPS для docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="a710c-106">This article provides an alphabetical reference for using Markdown in OPS for docs.microsoft.com.</span></span>

<span data-ttu-id="a710c-107">Для работы с разметкой Markdown можно использовать любой текстовый редактор.</span><span class="sxs-lookup"><span data-stu-id="a710c-107">You can use any text editor to author Markdown.</span></span> <span data-ttu-id="a710c-108">В качестве редактора, упрощающего вставку стандартного синтаксиса Markdown и пользовательских расширений OPS, мы рекомендуем [VS Code](https://code.visualstudio.com/) с установленным [пакетом создания документации](https://aka.ms/DocsAuthoringPack).</span><span class="sxs-lookup"><span data-stu-id="a710c-108">For an editor that facilitates inserting both standard Markdown syntax and custom OPS extensions, we recommend [VS Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installed.</span></span>

<span data-ttu-id="a710c-109">В OPS реализуется стандарт Markdig для всех новых репозиториев. Старые репозитории также переводятся на Markdig.</span><span class="sxs-lookup"><span data-stu-id="a710c-109">OPS has standardized on Markdig for all new repos, and older repos are migrating to Markdig.</span></span> <span data-ttu-id="a710c-110">Сравнить отрисовку разметки Markdown в Markdig с другими обработчиками можно по адресу [https://babelmark.github.io/](https://babelmark.github.io/).</span><span class="sxs-lookup"><span data-stu-id="a710c-110">You can test the rendering of Markdown in Markdig vs. other engines at [https://babelmark.github.io/](https://babelmark.github.io/).</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="a710c-111">Оповещения ("Примечание", "Совет", "Важно!", "Внимание!", "Предупреждение")</span><span class="sxs-lookup"><span data-stu-id="a710c-111">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="a710c-112">Оповещения — это специальные расширения Markdown для OPS для создания блоков цитирования, которые отображаются на сайте docs.microsoft.com с помощью цветов и значков, указывающих на важность содержимого.</span><span class="sxs-lookup"><span data-stu-id="a710c-112">Alerts is an OPS-specific Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="a710c-113">Поддерживаются следующие типы оповещений:</span><span class="sxs-lookup"><span data-stu-id="a710c-113">The following alert types are supported:</span></span>

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

<span data-ttu-id="a710c-114">На сайте docs.microsoft.com эти оповещения отображаются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a710c-114">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="a710c-115">Информация, которую пользователь должен заметить даже при беглом просмотре.</span><span class="sxs-lookup"><span data-stu-id="a710c-115">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="a710c-116">Дополнительные сведения, помогающие пользователю лучше решить задачу.</span><span class="sxs-lookup"><span data-stu-id="a710c-116">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a710c-117">Важные сведения для успешного решения задачи.</span><span class="sxs-lookup"><span data-stu-id="a710c-117">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="a710c-118">Потенциальные негативные последствия действия.</span><span class="sxs-lookup"><span data-stu-id="a710c-118">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="a710c-119">Опасные последствия действия.</span><span class="sxs-lookup"><span data-stu-id="a710c-119">Dangerous certain consequences of an action.</span></span>

## <a name="code-snippets"></a><span data-ttu-id="a710c-120">Фрагменты кода</span><span class="sxs-lookup"><span data-stu-id="a710c-120">Code snippets</span></span>

<span data-ttu-id="a710c-121">Вы можете вставить фрагменты кода в свои файлы Markdown:</span><span class="sxs-lookup"><span data-stu-id="a710c-121">You can embed code snippets in your Markdown files:</span></span>

```markdown
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a><span data-ttu-id="a710c-122">Заголовки</span><span class="sxs-lookup"><span data-stu-id="a710c-122">Headings</span></span>

<span data-ttu-id="a710c-123">OPS поддерживает шесть уровней заголовков Markdown:</span><span class="sxs-lookup"><span data-stu-id="a710c-123">OPS supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="a710c-124">Между последним символом `#` и содержимым заголовка должен присутствовать пробел.</span><span class="sxs-lookup"><span data-stu-id="a710c-124">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="a710c-125">В одном файле Markdown должен быть один и только один заголовок H1.</span><span class="sxs-lookup"><span data-stu-id="a710c-125">Each Markdown file must have one and only one H1.</span></span>
- <span data-ttu-id="a710c-126">Заголовок H1 указывается в файле в первую очередь, сразу после блока метаданных YML.</span><span class="sxs-lookup"><span data-stu-id="a710c-126">The H1 must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="a710c-127">Заголовки H2 автоматически отображаются в правом меню навигации опубликованного файла.</span><span class="sxs-lookup"><span data-stu-id="a710c-127">H2s automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="a710c-128">Это правило не применяется к заголовкам следующих уровней, поэтому для удобства перехода по содержимому рекомендуется использовать заголовки H2.</span><span class="sxs-lookup"><span data-stu-id="a710c-128">Lower-level headings do not, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="a710c-129">Использовать заголовки HMTL, такие как `<h1>`, не рекомендуется, и в некоторых случаях из-за них могут возникать предупреждения при сборке.</span><span class="sxs-lookup"><span data-stu-id="a710c-129">HMTL headings, such as `<h1>`, are not recommended and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="a710c-130">Привязка к отдельным заголовкам в файле выполняется с помощью [закладок](#bookmark-links).</span><span class="sxs-lookup"><span data-stu-id="a710c-130">You can link to individual headings in a file via [bookmarks](#bookmark-links).</span></span>

## <a name="html"></a><span data-ttu-id="a710c-131">HTML</span><span class="sxs-lookup"><span data-stu-id="a710c-131">HTML</span></span>

<span data-ttu-id="a710c-132">Хотя Markdown поддерживает встроенный HTML-код, HTML не рекомендуется использовать для публикации через OPS. Любой код, за исключением ограниченного списка значений, будет вызывать появление ошибок и предупреждений при сборке.</span><span class="sxs-lookup"><span data-stu-id="a710c-132">Although Markdown supports inline HTML, HTML is not recommended for publishing via OPS, and except for a limited list of values will cause build errors or warnings.</span></span> <!--For more information, see HTML Whitelist. // do we want to add the whitelist? -->

## <a name="images"></a><span data-ttu-id="a710c-133">Изображения</span><span class="sxs-lookup"><span data-stu-id="a710c-133">Images</span></span>

<span data-ttu-id="a710c-134">Для включения изображения используется следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="a710c-134">The syntax to include an image is:</span></span>

```markdown
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="a710c-135">Где `alt text` — краткое описание изображения, а `<folder path>` — относительный путь к нему.</span><span class="sxs-lookup"><span data-stu-id="a710c-135">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="a710c-136">Заменяющий текст необходим для средств чтения с экрана для слабовидящих.</span><span class="sxs-lookup"><span data-stu-id="a710c-136">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="a710c-137">Он также удобен при возникновении ошибок на сайте, из-за которых не удается воспроизвести изображение.</span><span class="sxs-lookup"><span data-stu-id="a710c-137">It is also useful if there is a site bug where the image cannot render.</span></span>

<span data-ttu-id="a710c-138">Изображения должны храниться в папке `/media` в наборе документации.</span><span class="sxs-lookup"><span data-stu-id="a710c-138">Images should be stored in a `/media` folder within your doc set.</span></span> <span data-ttu-id="a710c-139">Для изображений по умолчанию поддерживаются следующие типы файлов:</span><span class="sxs-lookup"><span data-stu-id="a710c-139">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="a710c-140">JPG,</span><span class="sxs-lookup"><span data-stu-id="a710c-140">.jpg</span></span>
- <span data-ttu-id="a710c-141">PNG.</span><span class="sxs-lookup"><span data-stu-id="a710c-141">.png</span></span>

<span data-ttu-id="a710c-142">Чтобы добавить поддержку других типов изображений, добавьте их в качестве ресурсов в файл<!--add link to reference when available--> docfx.json для набора документации.</span><span class="sxs-lookup"><span data-stu-id="a710c-142">You can add support for other image types by adding them as resources to the docfx.json file<!--add link to reference when available--> for your doc set.</span></span>

## <a name="links"></a><span data-ttu-id="a710c-143">Создание ссылок</span><span class="sxs-lookup"><span data-stu-id="a710c-143">Links</span></span>

<span data-ttu-id="a710c-144">Как правило, OPS использует стандартные ссылки Markdown на другие файлы и страницы.</span><span class="sxs-lookup"><span data-stu-id="a710c-144">In most cases, OPS uses standard Markdown links to other files and pages.</span></span> <span data-ttu-id="a710c-145">Типы ссылок описываются в подразделах ниже.</span><span class="sxs-lookup"><span data-stu-id="a710c-145">The types of links are described in subsections below.</span></span>

> [!TIP]
> <span data-ttu-id="a710c-146">Пакет создания документации для VS Code помогает правильно вставлять ссылки и закладки в автоматическом режиме.</span><span class="sxs-lookup"><span data-stu-id="a710c-146">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a710c-147">Не включайте коды языковых стандартов, такие как en-us, в ссылки на сайты Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="a710c-147">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span></span> <span data-ttu-id="a710c-148">Жестко закодированные коды языков блокируют воспроизведение локализованного содержимого: это неудобно для пользователей, говорящих на других языках, и влечет за собой большие затраты на локализацию.</span><span class="sxs-lookup"><span data-stu-id="a710c-148">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span></span> <span data-ttu-id="a710c-149">При копировании URL-адреса из браузера код языка включается по умолчанию, поэтому его необходимо удалить вручную при создании ссылки.</span><span class="sxs-lookup"><span data-stu-id="a710c-149">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link.</span></span> <span data-ttu-id="a710c-150">Например, используйте:</span><span class="sxs-lookup"><span data-stu-id="a710c-150">For example, use:</span></span>
>
> `[Microsoft](https://www.microsoft.com)`
>
> <span data-ttu-id="a710c-151">А не:</span><span class="sxs-lookup"><span data-stu-id="a710c-151">Not:</span></span>
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a><span data-ttu-id="a710c-152">Относительные ссылки на файлы в том же наборе документации</span><span class="sxs-lookup"><span data-stu-id="a710c-152">Relative links to files in the same doc set</span></span>

<span data-ttu-id="a710c-153">Относительный путь — это путь к целевому файлу относительно текущего файла.</span><span class="sxs-lookup"><span data-stu-id="a710c-153">A relative path is the path to the target file relative to the current file.</span></span> <span data-ttu-id="a710c-154">В OPS относительные пути можно использовать для связывания файлов в одном наборе документов.</span><span class="sxs-lookup"><span data-stu-id="a710c-154">In OPS, you can use a relative path to link to another file within the same doc set.</span></span> <span data-ttu-id="a710c-155">Синтаксис относительного пути следующий:</span><span class="sxs-lookup"><span data-stu-id="a710c-155">The syntax for a relative path is as follows:</span></span>

```markdown
[link text](../../folder/filename.md)
```

<span data-ttu-id="a710c-156">Где `../` означает один уровень выше в иерархии.</span><span class="sxs-lookup"><span data-stu-id="a710c-156">Where `../` indicates one level above in the hierarchy.</span></span>

- <span data-ttu-id="a710c-157">Относительный путь будет разрешаться во время сборки, включая удаление расширения MD.</span><span class="sxs-lookup"><span data-stu-id="a710c-157">The relative path will be resolved during the build, including removal of the .md extension.</span></span>
- <span data-ttu-id="a710c-158">Можно использовать "../" для указания на файл в родительской папке, но этот файл должен быть в том же наборе документации.</span><span class="sxs-lookup"><span data-stu-id="a710c-158">You can use "../" to link to a file in the parent folder, but that file has to be in the same doc set.</span></span> <span data-ttu-id="a710c-159">"../" нельзя использовать для указания на файл в другой папке набора документации.</span><span class="sxs-lookup"><span data-stu-id="a710c-159">You cannot use "../" to link to a file in another doc set folder.</span></span>
- <span data-ttu-id="a710c-160">OPS также поддерживает особый формат относительного пути, начинающийся с символа "~" (например, ~/foo/bar.md).</span><span class="sxs-lookup"><span data-stu-id="a710c-160">OPS also supports a special form of relative path that starts with "~" (for example, ~/foo/bar.md).</span></span> <span data-ttu-id="a710c-161">Этот синтаксис указывает файл относительно корневой папки набора документации.</span><span class="sxs-lookup"><span data-stu-id="a710c-161">This syntax indicates a file relative to the root folder of a doc set.</span></span> <span data-ttu-id="a710c-162">Этот вид пути также проверяется и разрешается во время сборки.</span><span class="sxs-lookup"><span data-stu-id="a710c-162">This kind of path is also validated and resolved during the build.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a710c-163">Включите расширение файла в относительный путь.</span><span class="sxs-lookup"><span data-stu-id="a710c-163">Include the file extension in the relative path.</span></span> <span data-ttu-id="a710c-164">В ходе сборки проверяется существование целевого файла по этому относительному пути.</span><span class="sxs-lookup"><span data-stu-id="a710c-164">Build validates the existence of the target file of that relative path.</span></span> <span data-ttu-id="a710c-165">Если относительный путь не включает расширение файла, в ходе сборки, скорее всего, будет создано предупреждение или неработающая ссылка.</span><span class="sxs-lookup"><span data-stu-id="a710c-165">If relative path does not include file extension, it is likely build will report a warning of broken link.</span></span> <span data-ttu-id="a710c-166">Например, используйте:</span><span class="sxs-lookup"><span data-stu-id="a710c-166">For example, use:</span></span>
>
> `[link text](../../folder/filename.md)`
>
> <span data-ttu-id="a710c-167">А не:</span><span class="sxs-lookup"><span data-stu-id="a710c-167">Not:</span></span>
>
> `[link text](../../folder/filename)`

### <a name="absolute-links-to-other-files-in-ops"></a><span data-ttu-id="a710c-168">Абсолютные ссылки на другие файлы в OPS</span><span class="sxs-lookup"><span data-stu-id="a710c-168">Absolute links to other files in OPS</span></span>

```markdown
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

<span data-ttu-id="a710c-169">Не включайте расширение файла (MD).</span><span class="sxs-lookup"><span data-stu-id="a710c-169">Do not include the file extension (.md).</span></span> <span data-ttu-id="a710c-170">Это ссылка на обзорный файл Linux за пределами набора документации "статей" Azure.</span><span class="sxs-lookup"><span data-stu-id="a710c-170">This links to the Linux overview file from outside the Azure "articles" doc set.</span></span>

### <a name="links-to-external-sites"></a><span data-ttu-id="a710c-171">Ссылки на внешние сайты</span><span class="sxs-lookup"><span data-stu-id="a710c-171">Links to external sites</span></span>

```markdown
[Microsoft](https://www.microsoft.com)
```

<span data-ttu-id="a710c-172">Ссылка на основе URL-адреса на другую веб-страницу (должна включать https://).</span><span class="sxs-lookup"><span data-stu-id="a710c-172">URL-based link to another web page (must include https://).</span></span>

### <a name="bookmark-links"></a><span data-ttu-id="a710c-173">Ссылки закладок</span><span class="sxs-lookup"><span data-stu-id="a710c-173">Bookmark links</span></span>

<span data-ttu-id="a710c-174">Ссылка-закладка на заголовок в другом файле в том же репозитории:</span><span class="sxs-lookup"><span data-stu-id="a710c-174">Bookmark link to a heading in another file in the same repo:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="a710c-175">Ссылка-закладка на заголовок в текущем файле:</span><span class="sxs-lookup"><span data-stu-id="a710c-175">Bookmark link to a heading in the current file:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="a710c-176">Используйте хэш-тег, за которым следуют слова заголовка: без знаков препинания, пробелы заменяются дефисами.</span><span class="sxs-lookup"><span data-stu-id="a710c-176">Use a hash tag followed by the words of the heading with punctuation removed and spaces replaced with dashes.</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="a710c-177">Явные ссылки привязки</span><span class="sxs-lookup"><span data-stu-id="a710c-177">Explicit anchor links</span></span>

<span data-ttu-id="a710c-178">Явные ссылки привязки, использующие HTML-тег `<a>` **не требуются и не рекомендуются**, за исключением страниц-концентраторов и целевых страниц.</span><span class="sxs-lookup"><span data-stu-id="a710c-178">Explicit anchor links using the `<a>` HTML tag are **not required or recommended** except in hub and landing pages.</span></span> <span data-ttu-id="a710c-179">Используйте закладки, как описано выше, в общих файлах Markdown.</span><span class="sxs-lookup"><span data-stu-id="a710c-179">Use bookmarks as described above in general Markdown files.</span></span> <span data-ttu-id="a710c-180">Для страниц-концентраторов и целевых страниц привязки используются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a710c-180">For hub and landing pages, use anchors as follows:</span></span>

<span data-ttu-id="a710c-181">`## <a id="AnchorText"> </a>Header text` или `## <a name="AnchorText"> </a>Header text`</span><span class="sxs-lookup"><span data-stu-id="a710c-181">`## <a id="AnchorText"> </a>Header text` or `## <a name="AnchorText"> </a>Header text`</span></span>

<span data-ttu-id="a710c-182">Для ссылки на явные привязки используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="a710c-182">To link to explicit anchors, use the following syntax:</span></span>

```markdown
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a><span data-ttu-id="a710c-183">Ссылки XREF (перекрестные ссылки)</span><span class="sxs-lookup"><span data-stu-id="a710c-183">XREF (cross reference) links</span></span>

<span data-ttu-id="a710c-184">Для ссылки на автоматически создаваемые страницы справочных материалов по API в текущем или другом наборе документации используйте ссылки XREF с уникальным идентификатором (UID).</span><span class="sxs-lookup"><span data-stu-id="a710c-184">To link to auto-generated API references pages in the current doc set or other doc sets, use XREF links with the unique ID (UID).</span></span>

> [!NOTE]
> <span data-ttu-id="a710c-185">Для ссылки на страницы справочных материалов по API в других наборах документации потребуется добавить конфигурацию `xrefService` в файл `docfx.json`.</span><span class="sxs-lookup"><span data-stu-id="a710c-185">To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.</span></span>
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

<span data-ttu-id="a710c-186">Уникальный идентификатор совпадает с полным именем класса и члена.</span><span class="sxs-lookup"><span data-stu-id="a710c-186">The UID equates to the fully qualified class and member name.</span></span> <span data-ttu-id="a710c-187">Если добавить символ \* после UID, ссылка будет вести на страницу перегрузки, а не к конкретному API.</span><span class="sxs-lookup"><span data-stu-id="a710c-187">If you add a \* after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="a710c-188">Например, используйте `List<T>.BinarySearch*` для ссылки на страницу "Метод BinarySearch" вместо ссылки на конкретную перегрузку, например `List<T>.BinarySearch(T, IComparer<T>)`.</span><span class="sxs-lookup"><span data-stu-id="a710c-188">For example, use `List<T>.BinarySearch*` to link to the BinarySearch Method page instead of linking to a specific overload such as `List<T>.BinarySearch(T, IComparer<T>)`.</span></span>

<span data-ttu-id="a710c-189">Можно выбрать один из следующих вариантов синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="a710c-189">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="a710c-190">Автоматическая ссылка: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="a710c-190">Auto-link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span></span>

  <span data-ttu-id="a710c-191">Необязательный параметр запроса `displayProperty` создает полный текст ссылки.</span><span class="sxs-lookup"><span data-stu-id="a710c-191">The optional `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="a710c-192">По умолчанию в тексте ссылки отображается только имя члена или типа.</span><span class="sxs-lookup"><span data-stu-id="a710c-192">By default, link text shows only the member or type name.</span></span>

- <span data-ttu-id="a710c-193">Ссылка с разметкой Markdown: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="a710c-193">Markdown link: `[link text](xref:UID)`</span></span>
  
  <span data-ttu-id="a710c-194">Используется, когда требуется настроить текст ссылки.</span><span class="sxs-lookup"><span data-stu-id="a710c-194">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="a710c-195">Примеры:</span><span class="sxs-lookup"><span data-stu-id="a710c-195">Examples:</span></span>

- <span data-ttu-id="a710c-196">`<xref:System.String>` отображается как String;</span><span class="sxs-lookup"><span data-stu-id="a710c-196">`<xref:System.String>` renders as "String".</span></span>
- <span data-ttu-id="a710c-197">`<xref:System.String?displayProperty=nameWithType>` отображается как System.String;</span><span class="sxs-lookup"><span data-stu-id="a710c-197">`<xref:System.String?displayProperty=nameWithType>` renders as "System.String".</span></span>
- <span data-ttu-id="a710c-198">`[String class](xref:System.String)` отображается как String class.</span><span class="sxs-lookup"><span data-stu-id="a710c-198">`[String class](xref:System.String)` renders as "String class".</span></span>

<span data-ttu-id="a710c-199">Сейчас не существует простого способа поиска UID.</span><span class="sxs-lookup"><span data-stu-id="a710c-199">Right now, there is no easy way to find the UIDs.</span></span> <span data-ttu-id="a710c-200"><!-- ? -->Чтобы найти UID для API, просмотрите исходный код страницы API, на которую нужно создать ссылку, и найдите значение ms.assetid.</span><span class="sxs-lookup"><span data-stu-id="a710c-200"><!-- ? -->The best way to find the UID for an API is to view the source for the API page you want to link to and find the ms.assetid value.</span></span> <span data-ttu-id="a710c-201">Отдельные значения перегрузки не отображаются в исходном коде.</span><span class="sxs-lookup"><span data-stu-id="a710c-201">Individual overload values are not shown in the source.</span></span> <span data-ttu-id="a710c-202">Мы работаем над улучшением нашей системы.</span><span class="sxs-lookup"><span data-stu-id="a710c-202">We're working on having a better system in the future.</span></span>

<span data-ttu-id="a710c-203">Если идентификатор содержит специальные символы \`, \# или \*, значение UID должно быть закодировано в HTML как `%60`, `%23` и `%2A` соответственно.</span><span class="sxs-lookup"><span data-stu-id="a710c-203">When the UID contains the special characters \`, \#, or \*, the UID value needs to be HTML encoded as `%60`, `%23`, and `%2A`, respectively.</span></span> <span data-ttu-id="a710c-204">Иногда круглые скобки тоже кодируются, но это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="a710c-204">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="a710c-205">Примеры:</span><span class="sxs-lookup"><span data-stu-id="a710c-205">Examples:</span></span>

- <span data-ttu-id="a710c-206">System.Threading.Tasks.Task\`1 заменяется на `System.Threading.Tasks.Task%601`;</span><span class="sxs-lookup"><span data-stu-id="a710c-206">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="a710c-207">System.Exception.\#ctor заменяется на `System.Exception.%23ctor`;</span><span class="sxs-lookup"><span data-stu-id="a710c-207">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="a710c-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) заменяется на `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`.</span><span class="sxs-lookup"><span data-stu-id="a710c-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="a710c-209">Списки (нумерованные, маркированные, контрольные)</span><span class="sxs-lookup"><span data-stu-id="a710c-209">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="a710c-210">Нумерованный список</span><span class="sxs-lookup"><span data-stu-id="a710c-210">Numbered list</span></span>

<span data-ttu-id="a710c-211">Для создания нумерованного списка можно использовать все 1, которые при публикации отображаются как последовательный список.</span><span class="sxs-lookup"><span data-stu-id="a710c-211">To create a numbered list, you can use all 1s, which are rendered as a sequential list when published.</span></span> <span data-ttu-id="a710c-212">Для повышения удобства чтения исходного кода списки можно вводить с приращением.</span><span class="sxs-lookup"><span data-stu-id="a710c-212">For increased source readability, you can increment your lists.</span></span>

<span data-ttu-id="a710c-213">Не используйте в списках, включая вложенные списки, буквы.</span><span class="sxs-lookup"><span data-stu-id="a710c-213">Do not use letters in lists, including nested lists.</span></span> <span data-ttu-id="a710c-214">При публикации через OPS они преобразуются некорректно.</span><span class="sxs-lookup"><span data-stu-id="a710c-214">They do not render correctly when published via OPS.</span></span> <span data-ttu-id="a710c-215">Вложенные списки с цифрами преобразуются в списки со строчными буквами при публикации.</span><span class="sxs-lookup"><span data-stu-id="a710c-215">Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="a710c-216">Например:</span><span class="sxs-lookup"><span data-stu-id="a710c-216">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="a710c-217">Это отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a710c-217">This renders as follows:</span></span>

1. <span data-ttu-id="a710c-218">Это</span><span class="sxs-lookup"><span data-stu-id="a710c-218">This is</span></span>
1. <span data-ttu-id="a710c-219">родительский нумерованный список,</span><span class="sxs-lookup"><span data-stu-id="a710c-219">a parent numbered list</span></span>
   1. <span data-ttu-id="a710c-220">а это</span><span class="sxs-lookup"><span data-stu-id="a710c-220">and this is</span></span>
   1. <span data-ttu-id="a710c-221">вложенный нумерованный список</span><span class="sxs-lookup"><span data-stu-id="a710c-221">a nested numbered list</span></span>
1. <span data-ttu-id="a710c-222">(конец)</span><span class="sxs-lookup"><span data-stu-id="a710c-222">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="a710c-223">Маркированный список</span><span class="sxs-lookup"><span data-stu-id="a710c-223">Bulleted list</span></span>

<span data-ttu-id="a710c-224">Для создания маркированного списка используйте `-`, за которым следует пробел в начале каждой строки.</span><span class="sxs-lookup"><span data-stu-id="a710c-224">To create a bulleted list, use `-` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="a710c-225">Это отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a710c-225">This renders as follows:</span></span>

- <span data-ttu-id="a710c-226">Это</span><span class="sxs-lookup"><span data-stu-id="a710c-226">This is</span></span>
- <span data-ttu-id="a710c-227">родительский маркированный список,</span><span class="sxs-lookup"><span data-stu-id="a710c-227">a parent bulleted list</span></span>
  - <span data-ttu-id="a710c-228">а это</span><span class="sxs-lookup"><span data-stu-id="a710c-228">and this is</span></span>
  - <span data-ttu-id="a710c-229">вложенный маркированный список</span><span class="sxs-lookup"><span data-stu-id="a710c-229">a nested bulleted list</span></span>
- <span data-ttu-id="a710c-230">Готово!</span><span class="sxs-lookup"><span data-stu-id="a710c-230">All done!</span></span>

### <a name="checklist"></a><span data-ttu-id="a710c-231">Контрольный список</span><span class="sxs-lookup"><span data-stu-id="a710c-231">Checklist</span></span>

<span data-ttu-id="a710c-232">Контрольные списки можно использовать (только) на сайте docs.microsoft.com с помощью пользовательского расширения Markdown:</span><span class="sxs-lookup"><span data-stu-id="a710c-232">Checklists are available for use on docs.microsoft.com (only) via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="a710c-233">Этот пример отображается на сайте docs.microsoft.com следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a710c-233">This example renders on docs.microsoft.com like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="a710c-234">List item 1</span><span class="sxs-lookup"><span data-stu-id="a710c-234">List item 1</span></span>
> * <span data-ttu-id="a710c-235">List item 2</span><span class="sxs-lookup"><span data-stu-id="a710c-235">List item 2</span></span>
> * <span data-ttu-id="a710c-236">List item 3</span><span class="sxs-lookup"><span data-stu-id="a710c-236">List item 3</span></span>

<span data-ttu-id="a710c-237">Контрольные списки используются в начале или конце статьи для подведения итогов "Чему вы научитесь" или "Чему вы научились".</span><span class="sxs-lookup"><span data-stu-id="a710c-237">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="a710c-238">Не вставляйте контрольные списки в статьи по случайному принципу.</span><span class="sxs-lookup"><span data-stu-id="a710c-238">Do not add random checklists throughout your articles.</span></span>
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a><span data-ttu-id="a710c-239">Действие "Дальнейшие действия"</span><span class="sxs-lookup"><span data-stu-id="a710c-239">Next step action</span></span>

<span data-ttu-id="a710c-240">Пользовательское расширение можно использовать для добавления кнопки "Дальнейшие действия" на страницы (только) docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="a710c-240">You can use a custom extension to add a next step action button to pages on docs.microsoft.com (only).</span></span>

<span data-ttu-id="a710c-241">Используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="a710c-241">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="a710c-242">Например:</span><span class="sxs-lookup"><span data-stu-id="a710c-242">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

<span data-ttu-id="a710c-243">Это отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a710c-243">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="a710c-244">Подробнее о базовом стиле</span><span class="sxs-lookup"><span data-stu-id="a710c-244">Learn about basic style</span></span>](style-quick-start.md)

<span data-ttu-id="a710c-245">Вы можете использовать любые поддерживаемые ссылки в действии "Дальнейшие действия", включая ссылку Markdown на другую веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="a710c-245">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="a710c-246">Как правило, ссылка "Дальнейшие действия" — это относительная ссылка на другой файл в том же наборе документации.</span><span class="sxs-lookup"><span data-stu-id="a710c-246">In most cases, the next action link will be a relative link to another file in the same doc set.</span></span>

## <a name="section-definition"></a><span data-ttu-id="a710c-247">Определение раздела</span><span class="sxs-lookup"><span data-stu-id="a710c-247">Section definition</span></span>

<span data-ttu-id="a710c-248"><!-- more info about this would be helpful! --> Вам может потребоваться определить раздел.</span><span class="sxs-lookup"><span data-stu-id="a710c-248"><!-- more info about this would be helpful! --> You might need to define a section.</span></span> <span data-ttu-id="a710c-249">Этот синтаксис в основном используется для таблиц кодов.</span><span class="sxs-lookup"><span data-stu-id="a710c-249">This syntax is mostly used for code tables.</span></span>
<span data-ttu-id="a710c-250">См. указанный ниже пример.</span><span class="sxs-lookup"><span data-stu-id="a710c-250">See the following example:</span></span>

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

<span data-ttu-id="a710c-251">Предыдущий текст Markdown будет отображаться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a710c-251">The preceding blockquote Markdown text will be rendered as:</span></span>
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a><span data-ttu-id="a710c-252">Селекторы</span><span class="sxs-lookup"><span data-stu-id="a710c-252">Selectors</span></span>

<span data-ttu-id="a710c-253"><!-- could be more clear! --> Селектор можно использовать, когда требуется связать различные страницы одной статьи.</span><span class="sxs-lookup"><span data-stu-id="a710c-253"><!-- could be more clear! --> You can use a selector when you want to connect different pages for the same article.</span></span> <span data-ttu-id="a710c-254">Затем читатели смогут переключаться между этими страницами.</span><span class="sxs-lookup"><span data-stu-id="a710c-254">Readers can then switch between those pages.</span></span>

> [!NOTE]
> <span data-ttu-id="a710c-255">Это расширение функционирует по-разному на сайтах docs.microsoft.com и MSDN.</span><span class="sxs-lookup"><span data-stu-id="a710c-255">This extension works differently between docs.microsoft.com and MSDN.</span></span> <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a><span data-ttu-id="a710c-256">Единичный выбор</span><span class="sxs-lookup"><span data-stu-id="a710c-256">Single selector</span></span>

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

<span data-ttu-id="a710c-257">... будет иметь следующий вид:</span><span class="sxs-lookup"><span data-stu-id="a710c-257">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Универсальные приложения Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a><span data-ttu-id="a710c-266">Множественный выбор</span><span class="sxs-lookup"><span data-stu-id="a710c-266">Multi-selector</span></span>

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

<span data-ttu-id="a710c-267">... будет иметь следующий вид:</span><span class="sxs-lookup"><span data-stu-id="a710c-267">... will be rendered like this:</span></span>

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

<!-- uncomment and link when Cory's topic is live
## Tabbed content

Tabs are a Markdown extension for docs.microsoft.com that allow us to present different versions of content, such as procedural steps to accomplish the same task on different platforms, in a tabbed format.

Because the syntax and requirements for tabbed content are fairly complex, they are documented separately in Tabbed Content.
-->

## <a name="tables"></a><span data-ttu-id="a710c-278">Tables</span><span class="sxs-lookup"><span data-stu-id="a710c-278">Tables</span></span>

<span data-ttu-id="a710c-279">Использование вертикальных линий и строк является самым простым способом создания таблиц в Markdown.</span><span class="sxs-lookup"><span data-stu-id="a710c-279">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="a710c-280">Чтобы создать стандартную таблицу с заголовком, вставьте пунктирную линию после первой строки.</span><span class="sxs-lookup"><span data-stu-id="a710c-280">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="a710c-281">Это отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a710c-281">This renders as follows:</span></span>

|<span data-ttu-id="a710c-282">Это</span><span class="sxs-lookup"><span data-stu-id="a710c-282">This is</span></span>   |<span data-ttu-id="a710c-283">просто</span><span class="sxs-lookup"><span data-stu-id="a710c-283">a simple</span></span>   |<span data-ttu-id="a710c-284">заголовок таблицы</span><span class="sxs-lookup"><span data-stu-id="a710c-284">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="a710c-285">данные</span><span class="sxs-lookup"><span data-stu-id="a710c-285">table</span></span>     |<span data-ttu-id="a710c-286">таблицы</span><span class="sxs-lookup"><span data-stu-id="a710c-286">data</span></span>       |<span data-ttu-id="a710c-287">здесь</span><span class="sxs-lookup"><span data-stu-id="a710c-287">here</span></span>        |
|<span data-ttu-id="a710c-288">вообще-то</span><span class="sxs-lookup"><span data-stu-id="a710c-288">it doesn't</span></span>|<span data-ttu-id="a710c-289">не всегда</span><span class="sxs-lookup"><span data-stu-id="a710c-289">actually</span></span>   |<span data-ttu-id="a710c-290">отображаются аккуратно!</span><span class="sxs-lookup"><span data-stu-id="a710c-290">have to line up nicely!</span></span>||

<span data-ttu-id="a710c-291">Можно также создать таблицу без заголовка.</span><span class="sxs-lookup"><span data-stu-id="a710c-291">You can also create a table without a header.</span></span> <span data-ttu-id="a710c-292">Например, чтобы создать список с несколькими столбцами:</span><span class="sxs-lookup"><span data-stu-id="a710c-292">For example, to create a multiple-column list:</span></span>

```markdown
|   |   |
| - | - |
| This | table |
| has no | header |
```

<span data-ttu-id="a710c-293">Это отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a710c-293">This renders like this:</span></span>

|   |   |
| - | - |
| <span data-ttu-id="a710c-294">Это</span><span class="sxs-lookup"><span data-stu-id="a710c-294">This</span></span> | <span data-ttu-id="a710c-295">таблица</span><span class="sxs-lookup"><span data-stu-id="a710c-295">table</span></span> |
| <span data-ttu-id="a710c-296">без</span><span class="sxs-lookup"><span data-stu-id="a710c-296">has no</span></span> | <span data-ttu-id="a710c-297">заголовка</span><span class="sxs-lookup"><span data-stu-id="a710c-297">header</span></span> |

<span data-ttu-id="a710c-298">Можно выровнять столбцы с помощью двоеточий:</span><span class="sxs-lookup"><span data-stu-id="a710c-298">You can align the columns by using colons:</span></span>

```markdown
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

<span data-ttu-id="a710c-299">Отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a710c-299">Renders as follows:</span></span>

|                  |
|------------------|
|    <span data-ttu-id="a710c-300">по правому краю:</span><span class="sxs-lookup"><span data-stu-id="a710c-300">right aligned:</span></span>|
|<span data-ttu-id="a710c-301">:по левому краю</span><span class="sxs-lookup"><span data-stu-id="a710c-301">:left aligned</span></span>     |
|<span data-ttu-id="a710c-302">:по центру            :</span><span class="sxs-lookup"><span data-stu-id="a710c-302">:centered        :</span></span>|

> [!TIP]
> Расширение создания документации для VS Code упрощает добавление базовых таблиц Markdown.
>
> Кроме того, можно использовать [веб-инструмент создания таблиц](http://www.tablesgenerator.com/markdown_tables).

### <a name="mx-tdbreakall"></a><span data-ttu-id="a710c-305">mx-tdBreakAll</span><span class="sxs-lookup"><span data-stu-id="a710c-305">mx-tdBreakAll</span></span>

> [!IMPORTANT]
> Эта функция работает только на веб-сайте docs.microsoft.com.

<span data-ttu-id="a710c-307">Создаваемая в Markdown таблица может выходить вправо, что делает ее нечитаемой.</span><span class="sxs-lookup"><span data-stu-id="a710c-307">If you create a table in Markdown, the table might expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="a710c-308">Эту проблему можно устранить, разрешив при необходимости разрыв таблицы при отображении документов.</span><span class="sxs-lookup"><span data-stu-id="a710c-308">You can solve that by allowing Docs rendering to break the table when needed.</span></span> <span data-ttu-id="a710c-309">Нужно просто заключить таблицу в настраиваемый класс `[!div class="mx-tdBreakAll"]`.</span><span class="sxs-lookup"><span data-stu-id="a710c-309">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="a710c-310">Далее приведен пример Markdown таблицы с тремя строками, которая будет заключена с помощью `div` с классом `mx-tdBreakAll`.</span><span class="sxs-lookup"><span data-stu-id="a710c-310">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="a710c-311">Она будет иметь следующий вид:</span><span class="sxs-lookup"><span data-stu-id="a710c-311">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="a710c-312">Имя</span><span class="sxs-lookup"><span data-stu-id="a710c-312">Name</span></span>|<span data-ttu-id="a710c-313">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a710c-313">Syntax</span></span>|<span data-ttu-id="a710c-314">Обязательно для автоматический установки?</span><span class="sxs-lookup"><span data-stu-id="a710c-314">Mandatory for silent installation?</span></span>|<span data-ttu-id="a710c-315">Описание</span><span class="sxs-lookup"><span data-stu-id="a710c-315">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="a710c-316">Quiet</span><span class="sxs-lookup"><span data-stu-id="a710c-316">Quiet</span></span>|<span data-ttu-id="a710c-317">/quiet</span><span class="sxs-lookup"><span data-stu-id="a710c-317">/quiet</span></span>|<span data-ttu-id="a710c-318">Да</span><span class="sxs-lookup"><span data-stu-id="a710c-318">Yes</span></span>|<span data-ttu-id="a710c-319">Запускает установщик без отображения пользовательского интерфейса и запросов.</span><span class="sxs-lookup"><span data-stu-id="a710c-319">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="a710c-320">NoRestart</span><span class="sxs-lookup"><span data-stu-id="a710c-320">NoRestart</span></span>|<span data-ttu-id="a710c-321">/norestart</span><span class="sxs-lookup"><span data-stu-id="a710c-321">/norestart</span></span>|<span data-ttu-id="a710c-322">Нет</span><span class="sxs-lookup"><span data-stu-id="a710c-322">No</span></span>|<span data-ttu-id="a710c-323">Подавляет попытки перезапуска.</span><span class="sxs-lookup"><span data-stu-id="a710c-323">Suppresses any attempts to restart.</span></span> <span data-ttu-id="a710c-324">По умолчанию пользовательский интерфейс выведет запрос перед перезапуском.</span><span class="sxs-lookup"><span data-stu-id="a710c-324">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="a710c-325">Help</span><span class="sxs-lookup"><span data-stu-id="a710c-325">Help</span></span>|<span data-ttu-id="a710c-326">/help</span><span class="sxs-lookup"><span data-stu-id="a710c-326">/help</span></span>|<span data-ttu-id="a710c-327">Нет</span><span class="sxs-lookup"><span data-stu-id="a710c-327">No</span></span>|<span data-ttu-id="a710c-328">Предоставляет справку и краткие инструкции.</span><span class="sxs-lookup"><span data-stu-id="a710c-328">Provides help and quick reference.</span></span> <span data-ttu-id="a710c-329">Отображает правильное использование команды setup, включая список всех параметров и вариантов поведения.</span><span class="sxs-lookup"><span data-stu-id="a710c-329">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="mx-tdcol2breakall"></a><span data-ttu-id="a710c-330">mx-tdCol2BreakAll</span><span class="sxs-lookup"><span data-stu-id="a710c-330">mx-tdCol2BreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a710c-331">Эта функция работает только на веб-сайте docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="a710c-331">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="a710c-332">Время от времени во втором столбце таблицы могут находиться очень длинные слова.</span><span class="sxs-lookup"><span data-stu-id="a710c-332">From time to time, you might have very long words in the second column of a table.</span></span> <span data-ttu-id="a710c-333">Чтобы правильно разделить эти слова, можно применить класс `mx-tdCol2BreakAll` с помощью синтаксиса оболочки `div`, как показано выше.</span><span class="sxs-lookup"><span data-stu-id="a710c-333">To ensure they are broken apart nicely, you can apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="html-tables"></a><span data-ttu-id="a710c-334">Таблицы HTML</span><span class="sxs-lookup"><span data-stu-id="a710c-334">HTML Tables</span></span>

<span data-ttu-id="a710c-335">Таблицы HTML не рекомендуется использовать для docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="a710c-335">HTML tables are not recommended for docs.microsoft.com.</span></span> <span data-ttu-id="a710c-336">Они трудны для восприятия в исходном виде — это нарушает основной принцип Markdown.</span><span class="sxs-lookup"><span data-stu-id="a710c-336">They are not human readable in the source - which is a key principle of Markdown.</span></span>

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a><span data-ttu-id="a710c-337">Видеоролики</span><span class="sxs-lookup"><span data-stu-id="a710c-337">Videos</span></span>

### <a name="embedding-videos-into-a-markdown-page"></a><span data-ttu-id="a710c-338">Внедрение видео на страницу Markdown</span><span class="sxs-lookup"><span data-stu-id="a710c-338">Embedding videos into a Markdown page</span></span>

<span data-ttu-id="a710c-339">Сейчас OPS поддерживает видеоролики, опубликованные в одной из трех платформ:</span><span class="sxs-lookup"><span data-stu-id="a710c-339">Currently, OPS can support videos published to one of three locations:</span></span>

- <span data-ttu-id="a710c-340">YouTube</span><span class="sxs-lookup"><span data-stu-id="a710c-340">YouTube</span></span>
- <span data-ttu-id="a710c-341">Channel 9</span><span class="sxs-lookup"><span data-stu-id="a710c-341">Channel 9</span></span>
- <span data-ttu-id="a710c-342">собственной системе Майкрософт One Player.</span><span class="sxs-lookup"><span data-stu-id="a710c-342">Microsoft's own 'One Player' system</span></span>

<span data-ttu-id="a710c-343">Вы можете внедрить видео с помощью следующего синтаксиса, и OPS отобразит его.</span><span class="sxs-lookup"><span data-stu-id="a710c-343">You can embed a video with the following syntax, and OPS will render it.</span></span>

```markdown
> [!VIDEO <embedded_video_link>]
```

<span data-ttu-id="a710c-344">Пример.</span><span class="sxs-lookup"><span data-stu-id="a710c-344">Example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

<span data-ttu-id="a710c-345">... будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="a710c-345">... will be rendered as:</span></span>

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

<span data-ttu-id="a710c-346">Содержимое на опубликованных страницах будет отображаться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a710c-346">And it will be displayed like this on published pages:</span></span>

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> <span data-ttu-id="a710c-347">URL-адрес видео для канала CH9 должен начинаться с `https` и заканчиваться `/player`.</span><span class="sxs-lookup"><span data-stu-id="a710c-347">The CH9 video URL should start with `https` and end with `/player`.</span></span> <span data-ttu-id="a710c-348">В противном случае будет внедрена вся страница, а не только видео.</span><span class="sxs-lookup"><span data-stu-id="a710c-348">Otherwise, it will embed the whole page instead of the video only.</span></span>

### <a name="uploading-new-videos"></a><span data-ttu-id="a710c-349">Отправка новых видео</span><span class="sxs-lookup"><span data-stu-id="a710c-349">Uploading new videos</span></span>

<span data-ttu-id="a710c-350">Для загрузки новых видео используйте следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="a710c-350">Any new videos should be uploaded using the following process:</span></span>

1. <span data-ttu-id="a710c-351">Присоединитесь к группе **docs_video_users** на портале IDWEB.</span><span class="sxs-lookup"><span data-stu-id="a710c-351">Join the **docs_video_users** group on IDWEB.</span></span>
1. <span data-ttu-id="a710c-352">Перейдите на страницу https://aka.ms/VideoUploadRequest и введите сведения о видеоролике.</span><span class="sxs-lookup"><span data-stu-id="a710c-352">Go to https://aka.ms/VideoUploadRequest and fill in the details for your video.</span></span> <span data-ttu-id="a710c-353">Вам потребуются следующие сведения (ни один из пунктов не будет отображаться для зрителей):</span><span class="sxs-lookup"><span data-stu-id="a710c-353">You will need (note that none of these items will be visible to the public):</span></span>
    1. <span data-ttu-id="a710c-354">название видео;</span><span class="sxs-lookup"><span data-stu-id="a710c-354">A title for your video.</span></span>
    1. <span data-ttu-id="a710c-355">список продуктов или служб, с которыми связано видео;</span><span class="sxs-lookup"><span data-stu-id="a710c-355">A list of products/services that your video is related to.</span></span>
    1. <span data-ttu-id="a710c-356">целевая страница или (если такой страницы еще нет) набор документации, где будет размещаться ваше видео;</span><span class="sxs-lookup"><span data-stu-id="a710c-356">The target page or (if you don’t have the page yet) doc set that your video will be hosted on.</span></span>
    1. <span data-ttu-id="a710c-357">ссылка на файл MP4 видео (если вам некуда отправить файл, можете временно поместить его сюда: `\\scratch2\scratch\apex`)</span><span class="sxs-lookup"><span data-stu-id="a710c-357">A link to the MP4 file for your video (if you don’t have a location to put the file, you can put it here temporarily:   `\\scratch2\scratch\apex`).</span></span> <span data-ttu-id="a710c-358">(разрешение файла MP4 должно быть не менее 720p);</span><span class="sxs-lookup"><span data-stu-id="a710c-358">MP4 files should be 720p or higher.</span></span>
    1. <span data-ttu-id="a710c-359">описание видео.</span><span class="sxs-lookup"><span data-stu-id="a710c-359">A description of the video.</span></span>
1. <span data-ttu-id="a710c-360">Отправьте (сохраните) этот элемент.</span><span class="sxs-lookup"><span data-stu-id="a710c-360">Submit (save) that item.</span></span>
1. <span data-ttu-id="a710c-361">Видео будет выгружено в течение двух рабочих дней.</span><span class="sxs-lookup"><span data-stu-id="a710c-361">Within two business days, the video will get uploaded.</span></span> <span data-ttu-id="a710c-362">Ссылка, необходимая для внедрения, будет помещена в рабочий элемент и *возвращена вам*.</span><span class="sxs-lookup"><span data-stu-id="a710c-362">The link you need for embedding will be placed into the work item, and it will be resolved *back to you*.</span></span>
1. <span data-ttu-id="a710c-363">Получив ссылку на видео, закройте рабочий элемент.</span><span class="sxs-lookup"><span data-stu-id="a710c-363">Once you have grabbed the video link, close the work item.</span></span>
1. <span data-ttu-id="a710c-364">Ссылку на видео можно добавить в публикацию, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="a710c-364">The video link can then be added to your post, using this syntax:</span></span>

   ```markdown
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```