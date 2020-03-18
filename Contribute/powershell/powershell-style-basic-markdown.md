---
title: Шаблон и подсказки для статей о PowerShell
description: В этой статье приводится удобный шаблон написания статей для документации по PowerShell.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 073a44240b1aa4baa9e655dab069097d21cdd66d
ms.sourcegitcommit: 804a99b89785e5c8f056a9da3f0fbde9f0a56a51
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "78331936"
---
# <a name="markdown-style-guide-for-powershell-docs"></a><span data-ttu-id="21b98-103">Руководство по стилю Markdown для документации по PowerShell</span><span class="sxs-lookup"><span data-stu-id="21b98-103">Markdown style guide for PowerShell-Docs</span></span>

<span data-ttu-id="21b98-104">В этой статье приводятся некоторые указания по стилю, относящиеся к содержимому документации по PowerShell.</span><span class="sxs-lookup"><span data-stu-id="21b98-104">This article provides some style guidance specific to the PowerShell-Docs content.</span></span>

<span data-ttu-id="21b98-105">Другие рекомендации по стилю написания см. в [руководстве по стилю Майкрософт](https://docs.microsoft.com/style-guide/welcome/).</span><span class="sxs-lookup"><span data-stu-id="21b98-105">For other writing style guidance, see the [Microsoft Style Guide](https://docs.microsoft.com/style-guide/welcome/).</span></span>

## <a name="metadata"></a><span data-ttu-id="21b98-106">Метаданные</span><span class="sxs-lookup"><span data-stu-id="21b98-106">Metadata</span></span>

<span data-ttu-id="21b98-107">Этот шаблон содержит примеры синтаксиса Markdown, а также инструкции по указанию метаданных.</span><span class="sxs-lookup"><span data-stu-id="21b98-107">This template contains examples of Markdown syntax, as well as guidance on setting the metadata.</span></span>
<span data-ttu-id="21b98-108">При создании файла Markdown скопируйте приведенный шаблон в новый файл, укажите метаданные, как описано ниже, и установите заголовок H1 над названием статьи.</span><span class="sxs-lookup"><span data-stu-id="21b98-108">When creating a Markdown file, you should copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

<span data-ttu-id="21b98-109">Необходимый блок метаданных приводится в следующем примере блока метаданных:</span><span class="sxs-lookup"><span data-stu-id="21b98-109">The required metadata block is in the following sample metadata block:</span></span>

```md
---
author: [GITHUB USERNAME]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
title: [ARTICLE TITLE]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="21b98-110">Между двоеточием (:) и значением в элементе метаданных **должен** быть пробел.</span><span class="sxs-lookup"><span data-stu-id="21b98-110">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="21b98-111">Двоеточия в значении (например, заголовке) прерывают анализ метаданных.</span><span class="sxs-lookup"><span data-stu-id="21b98-111">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="21b98-112">В этом случае заключите заголовок в двойные кавычки (например, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span><span class="sxs-lookup"><span data-stu-id="21b98-112">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="21b98-113">**author**: В этом поле необходимо указать **имя пользователя автора на GitHub**.</span><span class="sxs-lookup"><span data-stu-id="21b98-113">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="21b98-114">**description**: Описание содержимого статьи.</span><span class="sxs-lookup"><span data-stu-id="21b98-114">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="21b98-115">Обычно описание отображается на странице результатов поиска, но не используется для упорядочивания результатов.</span><span class="sxs-lookup"><span data-stu-id="21b98-115">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="21b98-116">Длина: 115–145 символов с пробелами.</span><span class="sxs-lookup"><span data-stu-id="21b98-116">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="21b98-117">**ms.date**: Дата последнего значительного изменения.</span><span class="sxs-lookup"><span data-stu-id="21b98-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="21b98-118">Измените это значение в существующей статье, если вы пересмотрели и обновили всю статью.</span><span class="sxs-lookup"><span data-stu-id="21b98-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="21b98-119">Небольшие исправления, вроде опечаток, не считаются обновлением.</span><span class="sxs-lookup"><span data-stu-id="21b98-119">Small fixes, such as typos or similar don't warrant an update.</span></span>
- <span data-ttu-id="21b98-120">**title**: Отображается в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="21b98-120">**title**: Appears in search engine results.</span></span> <span data-ttu-id="21b98-121">Название не должно совпадать со значением в заголовке H1 и превышать 60 символов в длину.</span><span class="sxs-lookup"><span data-stu-id="21b98-121">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or fewer.</span></span>

<span data-ttu-id="21b98-122">К каждой статье прикрепляются другие метаданные, но обычно мы применяем значения большинства метаданных на уровне папки в файле **docfx.json**.</span><span class="sxs-lookup"><span data-stu-id="21b98-122">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="product-terminology"></a><span data-ttu-id="21b98-123">Названия продуктов</span><span class="sxs-lookup"><span data-stu-id="21b98-123">Product Terminology</span></span>

<span data-ttu-id="21b98-124">Существует несколько вариантов PowerShell.</span><span class="sxs-lookup"><span data-stu-id="21b98-124">There are several variants of PowerShell.</span></span> <span data-ttu-id="21b98-125">В этой таблице поясняется ряд терминов, используемых в отношении PowerShell.</span><span class="sxs-lookup"><span data-stu-id="21b98-125">This table defines some of the different terms used to discuss PowerShell.</span></span>

- <span data-ttu-id="21b98-126">**PowerShell** — термин по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="21b98-126">**PowerShell** - This is the default.</span></span> <span data-ttu-id="21b98-127">Это название предоставляемого нами продукта.</span><span class="sxs-lookup"><span data-stu-id="21b98-127">PowerShell is the product we ship.</span></span> <span data-ttu-id="21b98-128">Термин PowerShell можно использовать в отношении любого выпуска продукта.</span><span class="sxs-lookup"><span data-stu-id="21b98-128">The term PowerShell can be used to describe any edition of the product.</span></span>
- <span data-ttu-id="21b98-129">**PowerShell Core** — это продукт PowerShell на основе среды выполнения .NET Core (CoreCLR) для любой из поддерживаемых платформ.</span><span class="sxs-lookup"><span data-stu-id="21b98-129">**PowerShell Core** - PowerShell built on .NET Core Common Language Runtime (CoreCLR) for any of the supported platforms.</span></span>
- <span data-ttu-id="21b98-130">**Windows PowerShell** — это продукт PowerShell на основе среды выполнения (CLR) .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="21b98-130">**Windows PowerShell** - PowerShell built on .NET Framework Common Language Runtime (CLR).</span></span> <span data-ttu-id="21b98-131">Windows PowerShell поставляется только с Windows и требует наличия полнофункциональной среды выполнения .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="21b98-131">Windows PowerShell ships only on Windows and requires the full .Net Framework CLR.</span></span>

<span data-ttu-id="21b98-132">В общем случае термин "Windows PowerShell" в документации можно сокращать до "PowerShell".</span><span class="sxs-lookup"><span data-stu-id="21b98-132">In general, references to "Windows PowerShell" in documentation can be changed to "PowerShell".</span></span>
<span data-ttu-id="21b98-133">Термин "Windows PowerShell" **не следует** сокращать при обсуждении продукта, предназначенного для Windows.</span><span class="sxs-lookup"><span data-stu-id="21b98-133">"Windows PowerShell" should **not** be changed when Windows-specific technology is being discussed.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="21b98-134">Базовый Markdown, GFM и специальные символы</span><span class="sxs-lookup"><span data-stu-id="21b98-134">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="21b98-135">О базовых принципах Markdown, GitHub Flavored Markdown (GFM) и конкретных расширениях OPS можно прочитать в статье [Справочник по Markdown](../markdown-reference.md).</span><span class="sxs-lookup"><span data-stu-id="21b98-135">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS specific extensions in the [Markdown reference](../markdown-reference.md) article.</span></span>

<span data-ttu-id="21b98-136">Markdown использует для форматирования специальные символы, например \*, \` и \#.</span><span class="sxs-lookup"><span data-stu-id="21b98-136">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="21b98-137">Если вы хотите включить такой символ в свою статью, сделайте одно из двух:</span><span class="sxs-lookup"><span data-stu-id="21b98-137">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="21b98-138">Поставьте обратную косую черту перед символом, чтобы экранировать его (например, `\*` для \*)</span><span class="sxs-lookup"><span data-stu-id="21b98-138">Put a backslash before the special character to "escape" it (for example, `\*` for a \*)</span></span>
- <span data-ttu-id="21b98-139">Используйте [код сущности HTML](http://www.ascii.cl/htmlcodes.htm) для символа (например, `&#42;` для &#42;).</span><span class="sxs-lookup"><span data-stu-id="21b98-139">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>
- <span data-ttu-id="21b98-140">В файлах Markdown должен использоваться обычный текст ASCII или кодировка UTF-8.</span><span class="sxs-lookup"><span data-stu-id="21b98-140">Markdown files should use plain ASCII text or UTF-8 encoding.</span></span> <span data-ttu-id="21b98-141">Однако старайтесь не использовать многобайтовые символы UTF-8.</span><span class="sxs-lookup"><span data-stu-id="21b98-141">However, avoid using multi-byte UTF-8 characters.</span></span> <span data-ttu-id="21b98-142">Вместо этого используйте сущность HTML.</span><span class="sxs-lookup"><span data-stu-id="21b98-142">Instead use an HTML entity.</span></span> <span data-ttu-id="21b98-143">Например, для символа авторского права используйте `&copy;`.</span><span class="sxs-lookup"><span data-stu-id="21b98-143">For example, for the copyright symbols use `&copy;`.</span></span>
  <span data-ttu-id="21b98-144">Он отображается как "&copy;".</span><span class="sxs-lookup"><span data-stu-id="21b98-144">It is rendered as: "&copy;".</span></span>

## <a name="hyperlinks"></a><span data-ttu-id="21b98-145">Гиперссылки</span><span class="sxs-lookup"><span data-stu-id="21b98-145">Hyperlinks</span></span>

- <span data-ttu-id="21b98-146">Старайтесь не использовать чистые URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="21b98-146">Avoid using bare URLs.</span></span> <span data-ttu-id="21b98-147">В ссылках следует использовать синтаксис разметки Markdown `[friendlyname](url-or-path)`.</span><span class="sxs-lookup"><span data-stu-id="21b98-147">Links should use Markdown syntax `[friendlyname](url-or-path)`</span></span>
- <span data-ttu-id="21b98-148">Ссылки должны иметь понятные имена. Обычно это заголовки соответствующих статей.</span><span class="sxs-lookup"><span data-stu-id="21b98-148">Links must have a friendly name, usually the title of the linked topic</span></span>
- <span data-ttu-id="21b98-149">Все элементы в разделе "Связанные ссылки" внизу статьи должны быть снабжены гиперссылками.</span><span class="sxs-lookup"><span data-stu-id="21b98-149">All items in the "related links" section at the bottom should be hyperlinked.</span></span>
- <span data-ttu-id="21b98-150">Используйте относительные ссылки на другое содержимое, размещенное на сайте **docs.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="21b98-150">Use relative links when linking to other content that is hosted on **docs.microsoft.com**.</span></span>
- <span data-ttu-id="21b98-151">Не используйте обратные галочки (грависы), полужирное начертание или другие элементы разметки в квадратных скобках гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="21b98-151">Do not use backticks, bold, or other markup inside the brackets of a hyperlink.</span></span>

<span data-ttu-id="21b98-152">Более подробные сведения о ссылках см. в разделе [Использование ссылок в документации](../how-to-write-links.md).</span><span class="sxs-lookup"><span data-stu-id="21b98-152">For more detailed information about linking, see [Using links in documentation](../how-to-write-links.md).</span></span>

## <a name="filenames"></a><span data-ttu-id="21b98-153">Имена файлов</span><span class="sxs-lookup"><span data-stu-id="21b98-153">Filenames</span></span>

<span data-ttu-id="21b98-154">Имена файлов подчиняются указанным ниже правилам.</span><span class="sxs-lookup"><span data-stu-id="21b98-154">Filenames use the following rules:</span></span>

- <span data-ttu-id="21b98-155">Содержат только буквы, цифры и дефисы.</span><span class="sxs-lookup"><span data-stu-id="21b98-155">Contain only letters, numbers, and hyphens.</span></span>
- <span data-ttu-id="21b98-156">Должны отсутствовать пробелы и знаки препинания.</span><span class="sxs-lookup"><span data-stu-id="21b98-156">No spaces or punctuation characters.</span></span> <span data-ttu-id="21b98-157">Для разделения слов и чисел в имени файла следует использовать дефисы.</span><span class="sxs-lookup"><span data-stu-id="21b98-157">Use the hyphens to separate words and numbers in the file name.</span></span>
- <span data-ttu-id="21b98-158">Следует использовать конкретные команды действий, такие как develop, buy, build, troubleshoot.</span><span class="sxs-lookup"><span data-stu-id="21b98-158">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="21b98-159">Использование слов, оканчивающихся на -ing, не допускается.</span><span class="sxs-lookup"><span data-stu-id="21b98-159">No -ing words.</span></span>
- <span data-ttu-id="21b98-160">Нельзя использовать служебные (короткие) слова, такие как a, and, the, in, or и т. д.</span><span class="sxs-lookup"><span data-stu-id="21b98-160">No small words - don't include a, and, the, in, or, etc.</span></span>
- <span data-ttu-id="21b98-161">Имя должно быть основано на разметке Markdown и иметь расширение файла .md.</span><span class="sxs-lookup"><span data-stu-id="21b98-161">Must be in Markdown and use the .md file extension.</span></span>
- <span data-ttu-id="21b98-162">Имя файла должно быть коротким в разумных пределах.</span><span class="sxs-lookup"><span data-stu-id="21b98-162">Keep file names reasonably short.</span></span> <span data-ttu-id="21b98-163">Оно будет частью URL-адреса статьи.</span><span class="sxs-lookup"><span data-stu-id="21b98-163">They are part of the URL for your articles.</span></span>

## <a name="blank-lines-spaces-and-tabs"></a><span data-ttu-id="21b98-164">Пустые строки, пробелы и символы табуляции</span><span class="sxs-lookup"><span data-stu-id="21b98-164">Blank lines, spaces, and tabs</span></span>

<span data-ttu-id="21b98-165">Удаляйте дублирующиеся пустые строки.</span><span class="sxs-lookup"><span data-stu-id="21b98-165">Remove duplicate blank lines.</span></span> <span data-ttu-id="21b98-166">Несколько пустых строк отображаются в HTML как одна, поэтому использовать их нет смысла.</span><span class="sxs-lookup"><span data-stu-id="21b98-166">Multiple blank lines render as a single blank line in HTML so there is not purpose for multiple blank lines.</span></span>

<span data-ttu-id="21b98-167">Кроме того, в Markdown пустые строки означают конец блока.</span><span class="sxs-lookup"><span data-stu-id="21b98-167">Blank lines also signal the end of a block in Markdown.</span></span> <span data-ttu-id="21b98-168">Между блоками Markdown разных типов (например, абзацем и списком или заголовком) должна быть одна пустая строка.</span><span class="sxs-lookup"><span data-stu-id="21b98-168">There should be a single blank between Markdown blocks of different types (for example, between a paragraph and a list or header).</span></span>

> [!NOTE]
> <span data-ttu-id="21b98-169">Пробелы в Markdown имеют значение.</span><span class="sxs-lookup"><span data-stu-id="21b98-169">Spacing is significant in Markdown.</span></span> <span data-ttu-id="21b98-170">Всегда используйте пробелы вместо жесткой табуляции.</span><span class="sxs-lookup"><span data-stu-id="21b98-170">Always uses spaces instead of hard tabs.</span></span> <span data-ttu-id="21b98-171">Удаляйте лишние пробелы в конце строк.</span><span class="sxs-lookup"><span data-stu-id="21b98-171">Remove extra spaces at the end of lines.</span></span>

## <a name="titles-and-headings"></a><span data-ttu-id="21b98-172">Названия и заголовки</span><span class="sxs-lookup"><span data-stu-id="21b98-172">Titles and headings</span></span>

<span data-ttu-id="21b98-173">Используйте только [заголовки в стиле ATX][atx] (то есть выделенные символами #, а не `=` или `-`).</span><span class="sxs-lookup"><span data-stu-id="21b98-173">Only use [ATX headings][atx] (# style, as opposed to `=` or `-` style headers).</span></span>

- <span data-ttu-id="21b98-174">Используйте регистр как в предложении: с прописной буквы следует начинать только имена собственные, а также первые слова в названиях или заголовках.</span><span class="sxs-lookup"><span data-stu-id="21b98-174">Use sentence case - only proper nouns and the first letter of a title or header should be capitalized</span></span>
- <span data-ttu-id="21b98-175">Между символом `#` и первым словом заголовка должен быть один пробел.</span><span class="sxs-lookup"><span data-stu-id="21b98-175">There must be a single space between the `#` and the first letter of the heading</span></span>
- <span data-ttu-id="21b98-176">Перед заголовком и после него должна быть одна пустая строка.</span><span class="sxs-lookup"><span data-stu-id="21b98-176">Headings should be surrounded by a single blank line</span></span>
- <span data-ttu-id="21b98-177">В каждом документе должен быть только один заголовок H1.</span><span class="sxs-lookup"><span data-stu-id="21b98-177">Only one H1 per document</span></span>
- <span data-ttu-id="21b98-178">Уровни заголовков должны увеличиваться последовательно — не пропускайте уровни.</span><span class="sxs-lookup"><span data-stu-id="21b98-178">Header levels should increment by one - do not skip levels</span></span>
- <span data-ttu-id="21b98-179">Не используйте обратные галочки, полужирное начертание или другие элементы разметки в заголовках.</span><span class="sxs-lookup"><span data-stu-id="21b98-179">Do not use backticks, bold, or other markup in headers</span></span>

> [!CAUTION]
> <span data-ttu-id="21b98-180">Схема, применяемая в [PlatyPS][platyPS] для справки по командлетам, требует наличия определенных заголовков H2 и H3.</span><span class="sxs-lookup"><span data-stu-id="21b98-180">The schema enforced by [PlatyPS][platyPS] for cmdlet reference requires specific H2 and H3 headers.</span></span> <span data-ttu-id="21b98-181">Добавление или удаление заголовков может привести к ошибкам при сборке.</span><span class="sxs-lookup"><span data-stu-id="21b98-181">Adding or removing headers can break the build.</span></span> <span data-ttu-id="21b98-182">Дополнительные сведения см. в [руководстве по стилю для справки по командлетам](powershell-style-reference.md).</span><span class="sxs-lookup"><span data-stu-id="21b98-182">For more information, see the [cmdlet reference style guide](powershell-style-reference.md).</span></span>

## <a name="limit-line-length-to-100-characters"></a><span data-ttu-id="21b98-183">Ограничьте длину строк 100 символами</span><span class="sxs-lookup"><span data-stu-id="21b98-183">Limit line length to 100 characters</span></span>

<span data-ttu-id="21b98-184">Это упростит вывод изменений и истории в командной строке.</span><span class="sxs-lookup"><span data-stu-id="21b98-184">This simplifies the command-line output of diffs and history.</span></span>

<span data-ttu-id="21b98-185">Данное правило не соблюдалось для большей части существующего содержимого в документации по PowerShell, однако мы работаем над исправлением этой ситуации.</span><span class="sxs-lookup"><span data-stu-id="21b98-185">This rule was not in force for much of the existing content in PowerShell-Docs, but we are working towards it over time.</span></span> <span data-ttu-id="21b98-186">Вы можете помочь нам в этом. [Расширение расплавления][reflow] в Visual Studio Code (VSCode) позволяет легко переформатировать абзацы так, чтобы это ограничение соблюдалось.</span><span class="sxs-lookup"><span data-stu-id="21b98-186">Feel free to help out. The [reflow extension][reflow] in Visual Studio Code (VSCode) makes it easy to reformat paragraphs to this limit.</span></span>

## <a name="lists"></a><span data-ttu-id="21b98-187">Списки</span><span class="sxs-lookup"><span data-stu-id="21b98-187">Lists</span></span>

<span data-ttu-id="21b98-188">Если список должен содержать несколько предложений или абзацев, можно использовать вместо него подзаголовки.</span><span class="sxs-lookup"><span data-stu-id="21b98-188">If your list contains multiple sentences or paragraphs, consider using a sub-level header rather than a list.</span></span>

<span data-ttu-id="21b98-189">Перед списком и после него должна быть одна пустая строка.</span><span class="sxs-lookup"><span data-stu-id="21b98-189">List should be surrounded by a single blank line.</span></span>

### <a name="unordered-lists"></a><span data-ttu-id="21b98-190">Неупорядоченные списки</span><span class="sxs-lookup"><span data-stu-id="21b98-190">Unordered lists</span></span>

<span data-ttu-id="21b98-191">Ставить точки в конце элементов списка следует, только если они содержат несколько предложений.</span><span class="sxs-lookup"><span data-stu-id="21b98-191">Do not end list items with a period unless they contain multiple sentences.</span></span> <span data-ttu-id="21b98-192">В качестве маркеров для элементов списка используйте символы дефиса (`-`).</span><span class="sxs-lookup"><span data-stu-id="21b98-192">Use the hyphen character (`-`) for list item bullets.</span></span> <span data-ttu-id="21b98-193">Это позволяет избежать путаницы с разметкой полужирного шрифта или курсивного начертания, в которой используется звездочка (`*`).</span><span class="sxs-lookup"><span data-stu-id="21b98-193">This avoids confusion with bold or italic markup that uses the asterisk [`*`].</span></span> <span data-ttu-id="21b98-194">Чтобы включить абзац или другие элементы в элемент маркированного списка, добавьте разрыв строки и выровняйте отступы с первым символом после маркера.</span><span class="sxs-lookup"><span data-stu-id="21b98-194">To include a paragraph or other elements under a bullet item, insert a line break and align indentation with the first character after the bullet.</span></span>

<span data-ttu-id="21b98-195">Например:</span><span class="sxs-lookup"><span data-stu-id="21b98-195">For example:</span></span>

```markdown
This is a list that contain sub-elements under a bullet item.

- First bullet item

  Sentence explaining the first bullet.

  - Sub-bullet item

    Sentence explaining the sub-bullet.

- Second bullet item
- Third bullet item
```

<span data-ttu-id="21b98-196">Это маркированный список, элемент которого имеет вложенные элементы.</span><span class="sxs-lookup"><span data-stu-id="21b98-196">This is a list that contains sub-elements under a bullet item.</span></span>

- <span data-ttu-id="21b98-197">Первый элемент маркированного списка</span><span class="sxs-lookup"><span data-stu-id="21b98-197">First bullet item</span></span>

  <span data-ttu-id="21b98-198">Предложение, поясняющее первый элемент.</span><span class="sxs-lookup"><span data-stu-id="21b98-198">Sentence explaining the first bullet.</span></span>

  - <span data-ttu-id="21b98-199">Вложенный элемент маркированного списка</span><span class="sxs-lookup"><span data-stu-id="21b98-199">Sub-bullet item</span></span>

    <span data-ttu-id="21b98-200">Предложение, поясняющее вложенный элемент.</span><span class="sxs-lookup"><span data-stu-id="21b98-200">Sentence explaining the sub-bullet.</span></span>

- <span data-ttu-id="21b98-201">Второй элемент маркированного списка</span><span class="sxs-lookup"><span data-stu-id="21b98-201">Second bullet item</span></span>
- <span data-ttu-id="21b98-202">Третий элемент маркированного списка</span><span class="sxs-lookup"><span data-stu-id="21b98-202">Third bullet item</span></span>

### <a name="ordered-lists"></a><span data-ttu-id="21b98-203">Упорядоченные списки</span><span class="sxs-lookup"><span data-stu-id="21b98-203">Ordered lists</span></span>

<span data-ttu-id="21b98-204">Чтобы включить абзац или другие элементы в элемент нумерованного списка, выровняйте отступы с первым символом после номера элемента.</span><span class="sxs-lookup"><span data-stu-id="21b98-204">To include a paragraph or other elements under a numbered item, align indentation with the first character after the item number.</span></span>

```markdown
1. For the first element, insert a single space after the 1. Long sentences should be
   wrapped to the next line and must line up with the first character after the numbered
   list marker.

   To include a second element (like this one), insert a line break after the first
   and align indentations. The indentation of the second element must line up with
   the first character after the numbered list marker. For single digit items, like
   this one, you indent to column 4. For double digits items, for example item number
   10, you indent to column 5.

1. The next numbered item starts here.
```

<span data-ttu-id="21b98-205">Например, нужно получить такой результат:</span><span class="sxs-lookup"><span data-stu-id="21b98-205">to get this output:</span></span>

> 1. <span data-ttu-id="21b98-206">Для первого элемента добавьте один пробел после цифры 1.</span><span class="sxs-lookup"><span data-stu-id="21b98-206">For the first element, insert a single space after the 1.</span></span> <span data-ttu-id="21b98-207">Длинные предложения должны переноситься по строкам, причем все строки должны быть выровнены по первому символу после номера элемента списка.</span><span class="sxs-lookup"><span data-stu-id="21b98-207">Long sentences should be wrapped to the next line and must line up with the first character after the numbered list marker.</span></span>
>
>    <span data-ttu-id="21b98-208">Чтобы включить еще один элемент (например, как этот), добавьте разрыв строки после первого и выровняйте отступы.</span><span class="sxs-lookup"><span data-stu-id="21b98-208">To include a second element (like this one), insert a line break after the first and align indentations.</span></span> <span data-ttu-id="21b98-209">Отступ второго элемента должен быть выровнен по первому символу после номера элемента списка.</span><span class="sxs-lookup"><span data-stu-id="21b98-209">The indentation of the second element must line up with the first character after the numbered list marker.</span></span> <span data-ttu-id="21b98-210">Для элементов с однозначными номерами, таких как этот, необходимо отступить до столбца 4.</span><span class="sxs-lookup"><span data-stu-id="21b98-210">For single digit items, like this one, you indent to column 4.</span></span> <span data-ttu-id="21b98-211">Для элементов с двузначными номерами, например 10, необходимо отступить до столбца 5.</span><span class="sxs-lookup"><span data-stu-id="21b98-211">For double digits items, for example item number 10, you indent to column 5.</span></span>
>
> 1. <span data-ttu-id="21b98-212">Следующий нумерованный элемент начинается здесь.</span><span class="sxs-lookup"><span data-stu-id="21b98-212">The next numbered item starts here.</span></span>

<span data-ttu-id="21b98-213">Для всех элементов в нумерованном списке должен использоваться номер `1.` вместо увеличения номера для каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="21b98-213">All items in a numbered listed should use the number `1.` instead of incrementing for each item.</span></span>
<span data-ttu-id="21b98-214">При преобразовании разметки Markdown для просмотра значение увеличивается автоматически.</span><span class="sxs-lookup"><span data-stu-id="21b98-214">Markdown rendering increments the value automatically.</span></span> <span data-ttu-id="21b98-215">Это упрощает переупорядочение элементов и позволяет стандартизировать отступы вложенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="21b98-215">This makes reordering items easier and standardizes the indentation of subordinate content.</span></span>

## <a name="formatting-command-syntax-elements"></a><span data-ttu-id="21b98-216">Форматирование элементов синтаксиса команд</span><span class="sxs-lookup"><span data-stu-id="21b98-216">Formatting command syntax elements</span></span>

- <span data-ttu-id="21b98-217">В именах командлетов PowerShell используется [регистр Pascal][pascal-case].</span><span class="sxs-lookup"><span data-stu-id="21b98-217">PowerShell cmdlet names are [Pascal Cased][pascal-case].</span></span> <span data-ttu-id="21b98-218">Глаголы от существительных отделяются дефисами.</span><span class="sxs-lookup"><span data-stu-id="21b98-218">Verbs are separated from nouns by a hyphen.</span></span> <span data-ttu-id="21b98-219">Всегда используйте полные имена командлетов и параметров в регистре Pascal.</span><span class="sxs-lookup"><span data-stu-id="21b98-219">Always use the full Pascal Case name for cmdlets and parameters.</span></span> <span data-ttu-id="21b98-220">Используйте псевдонимы, только если речь идет именно о них.</span><span class="sxs-lookup"><span data-stu-id="21b98-220">Avoid using aliases unless you are specifically talking about an alias.</span></span>

- <span data-ttu-id="21b98-221">В абзаце ключевые слова языка, имена командлетов и ссылки на переменные должны заключаться в грависы (`` ` ``).</span><span class="sxs-lookup"><span data-stu-id="21b98-221">Within a paragraph, language keywords, cmdlet names, and variable references should be wrapped in backtick (`` ` ``) characters.</span></span> <span data-ttu-id="21b98-222">Имена свойств, параметров и классов должны выделяться **полужирным шрифтом**.</span><span class="sxs-lookup"><span data-stu-id="21b98-222">Property, parameter, and class names should be **bold**.</span></span>

  <span data-ttu-id="21b98-223">Например:</span><span class="sxs-lookup"><span data-stu-id="21b98-223">For example:</span></span>

  ~~~markdown
  The following code assigns the output of `Get-ChildItem` to the `$files` variable.

  ```powershell
  $files = Get-ChildItem C:\Windows
  ```
  ~~~

- <span data-ttu-id="21b98-224">Если параметр указывается по имени, он должен быть выделен **полужирным шрифтом**.</span><span class="sxs-lookup"><span data-stu-id="21b98-224">When referring to a parameter by name, the name should be **bold**.</span></span> <span data-ttu-id="21b98-225">Если иллюстрируется использование параметра с префиксом в виде дефиса, параметр должен быть заключен в грависы.</span><span class="sxs-lookup"><span data-stu-id="21b98-225">When illustrating the use of a parameter with the hyphen prefix, the parameter should be wrapped in backticks.</span></span> <span data-ttu-id="21b98-226">Например:</span><span class="sxs-lookup"><span data-stu-id="21b98-226">For example:</span></span>

  ```markdown
  The parameter's name is **Name**, but it is typed as `-Name` when used on the command
  line as a parameter.
  ```

- <span data-ttu-id="21b98-227">При упоминании внешних команд (исполняемых файлов, скриптов и т. д.) имя команды должно быть полужирным, состоять из прописных букв (в начале предложения первая буква прописная) и включать в себя соответствующее расширение имени файла.</span><span class="sxs-lookup"><span data-stu-id="21b98-227">When referring to external commands (EXEs, scripts, etc.), the command name should be bold, all lowercase (or capitalized if at the beginning of a sentence), and include the appropriate file extension.</span></span> <span data-ttu-id="21b98-228">Например:</span><span class="sxs-lookup"><span data-stu-id="21b98-228">For example:</span></span>

  ```markdown
  For example, on Windows systems, you can use the `net start` and `net stop` commands
  to start and stop a service. **Sc.exe** is another service control tool for Windows.
  That name does not fit into the naming pattern for the **net.exe** service commands.
  ```

- <span data-ttu-id="21b98-229">Если приводится пример использования внешней команды, он должен быть заключен в грависы.</span><span class="sxs-lookup"><span data-stu-id="21b98-229">When showing example usage of an external command, the example should be wrapped in backticks.</span></span>
  <span data-ttu-id="21b98-230">При совпадении имени с псевдонимом в пример команды необходимо включить расширение имени файла.</span><span class="sxs-lookup"><span data-stu-id="21b98-230">When there is a name collision with an alias you must include the file extension in the command example.</span></span> <span data-ttu-id="21b98-231">Например:</span><span class="sxs-lookup"><span data-stu-id="21b98-231">For example:</span></span>

  ```markdown
  To start the spooler service on a remote computer named DC01, you type `sc.exe \\DC01 start spooler`.
  ```

- <span data-ttu-id="21b98-232">При написании концептуальной статьи (а не справочного содержимого) первое упоминание имени командлета должно быть гиперссылкой на документацию по командлету.</span><span class="sxs-lookup"><span data-stu-id="21b98-232">When writing a conceptual article (as opposed to reference content), the first instance of a cmdlet name should be hyperlinked to the cmdlet documentation.</span></span> <span data-ttu-id="21b98-233">Не используйте обратные галочки (грависы), полужирное начертание или другие элементы разметки в квадратных скобках гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="21b98-233">Do not use backticks, bold, or other markup inside the brackets of a hyperlink.</span></span>

  <span data-ttu-id="21b98-234">Например:</span><span class="sxs-lookup"><span data-stu-id="21b98-234">For example:</span></span>

  ```markdown
  This [Write-Host](/powershell/module/Microsoft.PowerShell.Utility/Write-Host) cmdlet
  uses the **Object** parameter to ...
  ```

  <span data-ttu-id="21b98-235">Дополнительные сведения см. в разделе [Гиперссылки](#hyperlinks) руководства по стилю.</span><span class="sxs-lookup"><span data-stu-id="21b98-235">For more information, see [Hyperlinks](#hyperlinks) section of the Style Guide.</span></span>

## <a name="images"></a><span data-ttu-id="21b98-236">Изображения</span><span class="sxs-lookup"><span data-stu-id="21b98-236">Images</span></span>

<span data-ttu-id="21b98-237">Для включения изображения используется следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="21b98-237">The syntax to include an image is:</span></span>

```Syntax
![[alt text]](<folderPath>)
```

<span data-ttu-id="21b98-238">Пример.</span><span class="sxs-lookup"><span data-stu-id="21b98-238">Example:</span></span>

```markdown
![Introduction](./media/overview/Introduction.png)
```

<span data-ttu-id="21b98-239">Где `alt text` — краткое описание изображения, а `<folder path>` — относительный путь к нему.</span><span class="sxs-lookup"><span data-stu-id="21b98-239">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="21b98-240">Заменяющий текст необходим для средств чтения с экрана для слабовидящих.</span><span class="sxs-lookup"><span data-stu-id="21b98-240">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="21b98-241">Он также удобен при возникновении ошибок на сайте, из-за которых не удается отобразить изображение.</span><span class="sxs-lookup"><span data-stu-id="21b98-241">It is also useful in case there is a site bug where the image cannot be rendered.</span></span>

<span data-ttu-id="21b98-242">Изображения должны храниться в папке `media/<article-name>`, вложенной в папку со статьей.</span><span class="sxs-lookup"><span data-stu-id="21b98-242">Images should be stored in a `media/<article-name>` folder within the folder containing your article.</span></span> <span data-ttu-id="21b98-243">Одно и то же изображение не следует использовать в нескольких статьях.</span><span class="sxs-lookup"><span data-stu-id="21b98-243">Images should not be shared between articles.</span></span> <span data-ttu-id="21b98-244">В папке `media` создайте вложенную папку, имя которой совпадает с именем файла статьи.</span><span class="sxs-lookup"><span data-stu-id="21b98-244">Create a folder that matches the filename of your article under the `media` folder.</span></span> <span data-ttu-id="21b98-245">Скопируйте изображения для статьи в эту новую папку.</span><span class="sxs-lookup"><span data-stu-id="21b98-245">Copy the images for that article to that new folder.</span></span> <span data-ttu-id="21b98-246">Если изображение используется в нескольких статьях, его копия должна быть в папке с изображениями каждой из них.</span><span class="sxs-lookup"><span data-stu-id="21b98-246">If an image is used by multiple articles, each image folder must have a copy of that image file.</span></span> <span data-ttu-id="21b98-247">Это нужно для того, чтобы при изменении изображения в одной статье в остальных оно не менялось.</span><span class="sxs-lookup"><span data-stu-id="21b98-247">This practice prevents a change to an image in one article affecting another article.</span></span>

<span data-ttu-id="21b98-248">Некоторые изображения, например логотипы и значки, должны использоваться в нескольких статьях.</span><span class="sxs-lookup"><span data-stu-id="21b98-248">In some cases, you want to share images, like logos and icons, across multiple articles.</span></span> <span data-ttu-id="21b98-249">Такие изображения хранятся в папке `/media/shared` в корне репозитория.</span><span class="sxs-lookup"><span data-stu-id="21b98-249">These images are stored in the `/media/shared` folder at the root of the repository.</span></span>

<span data-ttu-id="21b98-250">Для изображений поддерживаются следующие типы файлов: PNG, GIF, JPEG, JPG, SVG.</span><span class="sxs-lookup"><span data-stu-id="21b98-250">The following image file types are supported: \*.png", \*.gif", \*.jpeg", \*.jpg", \*.svg</span></span>

<!-- External URLs -->
[platyPS]: https://github.com/PowerShell/platyPS
[markdig]: https://github.com/lunet-io/markdig
[CommonMark]: https://spec.commonmark.org/
[atx]: https://github.github.com/gfm/#atx-headings
[pascal-case]: https://en.wikipedia.org/wiki/PascalCase
[reflow]: https://marketplace.visualstudio.com/items?itemName=marvhen.reflow-markdown
