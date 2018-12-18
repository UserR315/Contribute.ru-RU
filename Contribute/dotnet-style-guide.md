---
title: Шаблон и подсказки для статей о .NET
description: В этой статье приводится удобный шаблон написания статей для репозиториев с документацией по .NET
ms.date: 11/07/2018
ms.openlocfilehash: 08c8e19c858e7417d49cc2de543c67f330b93e89
ms.sourcegitcommit: b0556fc33803358009a030ac9efcaed23f562868
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2018
ms.locfileid: "53264509"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a><span data-ttu-id="89adb-103">Шаблон метаданных и Markdown для документации .NET</span><span class="sxs-lookup"><span data-stu-id="89adb-103">Metadata and Markdown template for .NET docs</span></span>

<span data-ttu-id="89adb-104">Этот шаблон dotnet/docs содержит примеры синтаксиса Markdown, а также инструкции по указанию метаданных.</span><span class="sxs-lookup"><span data-stu-id="89adb-104">This dotnet/docs template contains examples of Markdown syntax, as well as guidance on setting the metadata.</span></span>

<span data-ttu-id="89adb-105">При создании файла Markdown скопируйте приведенный шаблон в новый файл, укажите метаданные, как описано ниже, и установите заголовок H1 над названием статьи.</span><span class="sxs-lookup"><span data-stu-id="89adb-105">When creating a Markdown file, you should copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

## <a name="metadata"></a><span data-ttu-id="89adb-106">Метаданные</span><span class="sxs-lookup"><span data-stu-id="89adb-106">Metadata</span></span>

<span data-ttu-id="89adb-107">Необходимый блок метаданных приводится в следующем примере блока метаданных:</span><span class="sxs-lookup"><span data-stu-id="89adb-107">The required metadata block is in the following sample metadata block:</span></span>

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="89adb-108">Между двоеточием (:) и значением в элементе метаданных **должен** быть пробел.</span><span class="sxs-lookup"><span data-stu-id="89adb-108">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="89adb-109">Двоеточия в значении (например, заголовке) прерывают анализ метаданных.</span><span class="sxs-lookup"><span data-stu-id="89adb-109">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="89adb-110">В этом случае заключите заголовок в двойные кавычки (например, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span><span class="sxs-lookup"><span data-stu-id="89adb-110">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="89adb-111">**title**: Отображается в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="89adb-111">**title**: Appears in search engine results.</span></span> <span data-ttu-id="89adb-112">Заголовок должен совпадать со значением в заголовке H1 и не превышать 60 символов.</span><span class="sxs-lookup"><span data-stu-id="89adb-112">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or less.</span></span>
- <span data-ttu-id="89adb-113">**description**: Описание содержимого статьи.</span><span class="sxs-lookup"><span data-stu-id="89adb-113">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="89adb-114">Обычно описание отображается на странице результатов поиска, но не используется для упорядочивания результатов.</span><span class="sxs-lookup"><span data-stu-id="89adb-114">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="89adb-115">Длина: 115–145 символов с пробелами.</span><span class="sxs-lookup"><span data-stu-id="89adb-115">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="89adb-116">**author**: В этом поле необходимо указать **имя пользователя автора на GitHub**.</span><span class="sxs-lookup"><span data-stu-id="89adb-116">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="89adb-117">**ms.date**: Дата последнего значительного изменения.</span><span class="sxs-lookup"><span data-stu-id="89adb-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="89adb-118">Измените это значение в существующей статье, если вы пересмотрели и обновили всю статью.</span><span class="sxs-lookup"><span data-stu-id="89adb-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="89adb-119">Небольшие исправления, вроде опечаток, не считаются обновлением.</span><span class="sxs-lookup"><span data-stu-id="89adb-119">Small fixes, such as typos or similar do not warrant an update.</span></span>

<span data-ttu-id="89adb-120">К каждой статье прикрепляются другие метаданные, но обычно мы применяем значения большинства метаданных на уровне папки в файле **docfx.json**.</span><span class="sxs-lookup"><span data-stu-id="89adb-120">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="89adb-121">Базовый Markdown, GFM и специальные символы</span><span class="sxs-lookup"><span data-stu-id="89adb-121">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="89adb-122">О базовых принципах Markdown, GitHub Flavored Markdown (GFM) и конкретных расширениях OPS можно прочитать в статьях о [Markdown](how-to-write-use-markdown.md) и в [справочнике Markdown](markdown-reference.md).</span><span class="sxs-lookup"><span data-stu-id="89adb-122">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS specific extensions in the general articles on [Markdown](how-to-write-use-markdown.md) and [Markdown reference](markdown-reference.md).</span></span>

<span data-ttu-id="89adb-123">Markdown использует для форматирования специальные символы, например \*, \` и \#.</span><span class="sxs-lookup"><span data-stu-id="89adb-123">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="89adb-124">Если вы хотите включить такой символ в свою статью, сделайте одно из двух:</span><span class="sxs-lookup"><span data-stu-id="89adb-124">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="89adb-125">Поставьте обратную косую черту перед символом, чтобы экранировать его (например, `\*` для \*)</span><span class="sxs-lookup"><span data-stu-id="89adb-125">Put a backslash before the special character to "escape" it (for example, `\*` for a \*)</span></span>
- <span data-ttu-id="89adb-126">Используйте [код сущности HTML](http://www.ascii.cl/htmlcodes.htm) для символа (например, `&#42;` для &#42;).</span><span class="sxs-lookup"><span data-stu-id="89adb-126">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>

## <a name="file-names"></a><span data-ttu-id="89adb-127">Имена файлов</span><span class="sxs-lookup"><span data-stu-id="89adb-127">File names</span></span>

<span data-ttu-id="89adb-128">В именах файлов используются следующие правила:</span><span class="sxs-lookup"><span data-stu-id="89adb-128">File names use the following rules:</span></span>

* <span data-ttu-id="89adb-129">Имя может содержать только строчные буквы, цифры и дефисы.</span><span class="sxs-lookup"><span data-stu-id="89adb-129">Contain only lowercase letters, numbers, and hyphens.</span></span>
* <span data-ttu-id="89adb-130">Должны отсутствовать пробелы и знаки препинания.</span><span class="sxs-lookup"><span data-stu-id="89adb-130">No spaces or punctuation characters.</span></span> <span data-ttu-id="89adb-131">Для разделения слов и чисел в имени файла следует использовать дефисы.</span><span class="sxs-lookup"><span data-stu-id="89adb-131">Use the hyphens to separate words and numbers in the file name.</span></span>
* <span data-ttu-id="89adb-132">Следует использовать конкретные команды действий, такие как develop, buy, build, troubleshoot.</span><span class="sxs-lookup"><span data-stu-id="89adb-132">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="89adb-133">Использование слов, оканчивающихся на -ing, не допускается.</span><span class="sxs-lookup"><span data-stu-id="89adb-133">No -ing words.</span></span>
* <span data-ttu-id="89adb-134">Нельзя использовать служебные (короткие) слова, такие как a, and, the, in, or и т. д.</span><span class="sxs-lookup"><span data-stu-id="89adb-134">No small words - don't include a, and, the, in, or, etc.</span></span>
* <span data-ttu-id="89adb-135">Имя должно быть основано на разметке Markdown и иметь расширение файла .md.</span><span class="sxs-lookup"><span data-stu-id="89adb-135">Must be in Markdown and use the .md file extension.</span></span>
* <span data-ttu-id="89adb-136">Имя файла должно быть коротким в разумных пределах.</span><span class="sxs-lookup"><span data-stu-id="89adb-136">Keep file names reasonably short.</span></span> <span data-ttu-id="89adb-137">Оно будет частью URL-адреса статьи.</span><span class="sxs-lookup"><span data-stu-id="89adb-137">They are part of the URL for your articles.</span></span>

## <a name="headings"></a><span data-ttu-id="89adb-138">Заголовки</span><span class="sxs-lookup"><span data-stu-id="89adb-138">Headings</span></span>

<span data-ttu-id="89adb-139">Используйте выделение прописных букв, как в предложении.</span><span class="sxs-lookup"><span data-stu-id="89adb-139">Use sentence-style capitalization.</span></span> <span data-ttu-id="89adb-140">Первое слово заголовка всегда должно начинаться с прописной буквы.</span><span class="sxs-lookup"><span data-stu-id="89adb-140">Always capitalize the first word of a heading.</span></span>

## <a name="text-styling"></a><span data-ttu-id="89adb-141">Стиль текста</span><span class="sxs-lookup"><span data-stu-id="89adb-141">Text styling</span></span>

<span data-ttu-id="89adb-142">*Курсив* Используйте для обозначения файлов, папок, путей (длинные элементы вынесите в отдельную строку), новых терминов.</span><span class="sxs-lookup"><span data-stu-id="89adb-142">*Italics* Use for files, folders, paths (for long items, split onto their own line), new terms.</span></span>

<span data-ttu-id="89adb-143">**Полужирный** Используйте для обозначения элементов пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="89adb-143">**Bold** Use for UI elements.</span></span>

<span data-ttu-id="89adb-144">`Code` Используйте для встроенного кода, ключевых слов языка, имен пакетов NuGet, команд в командной строке, имен таблиц баз данных и столбцов и URL-адресов, которые не должны быть активными.</span><span class="sxs-lookup"><span data-stu-id="89adb-144">`Code` Use for inline code, language keywords, NuGet package names, command-line commands, database table and column names, and URLs that you don't want to be clickable.</span></span>

## <a name="links"></a><span data-ttu-id="89adb-145">Создание ссылок</span><span class="sxs-lookup"><span data-stu-id="89adb-145">Links</span></span>

<span data-ttu-id="89adb-146">См. общую статью о [Ссылках](how-to-write-links.md), чтобы узнать больше о привязках, внутренних ссылках, ссылках на другие документы, включениях кода и внешних ссылках.</span><span class="sxs-lookup"><span data-stu-id="89adb-146">See the general article on [Links](how-to-write-links.md) for information about anchors, internal links, links to other documents, code includes, and external links.</span></span>

<span data-ttu-id="89adb-147">Команда по документации .NET использует следующие соглашения:</span><span class="sxs-lookup"><span data-stu-id="89adb-147">The .NET docs team uses the following conventions:</span></span>

- <span data-ttu-id="89adb-148">В большинстве случаев мы используем относительные ссылки и не рекомендуем использовать `~/` в ссылках, поскольку относительные ссылки разрешаются в источнике на GitHub.</span><span class="sxs-lookup"><span data-stu-id="89adb-148">In most cases, we use the relative links and discourage the use of `~/` in links because relative links resolve in the source on GitHub.</span></span> <span data-ttu-id="89adb-149">Но если мы размещаем ссылку на файл в зависимом репозитории, мы используем символ `~/`, чтобы указать путь.</span><span class="sxs-lookup"><span data-stu-id="89adb-149">However, whenever we link to a file in a dependent repo, we'll use the `~/` character to provide the path.</span></span> <span data-ttu-id="89adb-150">Поскольку файлы в зависимом репозитории располагаются в другом месте на GitHub, ссылки не будут корректно разрешаться при использовании относительных ссылок, как бы они ни были записаны.</span><span class="sxs-lookup"><span data-stu-id="89adb-150">Because the files in the dependent repo are in a different location in GitHub the links won't resolve correctly with relative links regardless of how they were written.</span></span>
- <span data-ttu-id="89adb-151">Спецификации языка C# и Visual Basic включены в документацию .NET путем включения источника из репозиториев этих языков.</span><span class="sxs-lookup"><span data-stu-id="89adb-151">The C# language specification and the Visual Basic language specification are included in the .NET docs by including the source from the language repositories.</span></span> <span data-ttu-id="89adb-152">Источники Markdown управляются в репозиториях [csharplang](https://github.com/dotnet/csharplang) и [vblang](https://github.com/dotnet/vblang).</span><span class="sxs-lookup"><span data-stu-id="89adb-152">The markdown sources are managed in the [csharplang](https://github.com/dotnet/csharplang) and [vblang](https://github.com/dotnet/vblang) repositories.</span></span>

<span data-ttu-id="89adb-153">Ссылки на спецификации должны указывать на исходные каталоги, содержащие эти спецификации.</span><span class="sxs-lookup"><span data-stu-id="89adb-153">Links to the spec must point to the source directories where those specs are included.</span></span> <span data-ttu-id="89adb-154">Для C# это **~/_csharplang/spec**, а для VB — **~/_vblang/spec**, как в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="89adb-154">For C#, it's **~/_csharplang/spec** and for VB, it's **~/_vblang/spec**, as in the following example:</span></span>

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### <a name="links-to-apis"></a><span data-ttu-id="89adb-155">Ссылки на API</span><span class="sxs-lookup"><span data-stu-id="89adb-155">Links to APIs</span></span>

<span data-ttu-id="89adb-156">Система сборки имеет некоторые расширения, которые позволяют нам ссылаться на API .NET без использования внешних ссылок.</span><span class="sxs-lookup"><span data-stu-id="89adb-156">The build system has some extensions that allow us to link to .NET APIs without having to use external links.</span></span> <span data-ttu-id="89adb-157">Можно выбрать один из следующих вариантов синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="89adb-157">You use one of the following syntax:</span></span>

1. <span data-ttu-id="89adb-158">Автоматическая ссылка: `<xref:UID>` или `<xref:UID?displayProperty=nameWithType>`.</span><span class="sxs-lookup"><span data-stu-id="89adb-158">Auto-link: `<xref:UID>` or `<xref:UID?displayProperty=nameWithType>`</span></span>

   <span data-ttu-id="89adb-159">Параметр запроса `displayProperty` создает полный текст ссылки.</span><span class="sxs-lookup"><span data-stu-id="89adb-159">The `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="89adb-160">По умолчанию в тексте ссылки отображается только имя члена или типа.</span><span class="sxs-lookup"><span data-stu-id="89adb-160">By default, link text shows only the member or type name.</span></span>

2. <span data-ttu-id="89adb-161">Ссылка с разметкой Markdown: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="89adb-161">Markdown link: `[link text](xref:UID)`</span></span>

   <span data-ttu-id="89adb-162">Используется, когда требуется настроить текст ссылки.</span><span class="sxs-lookup"><span data-stu-id="89adb-162">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="89adb-163">Примеры:</span><span class="sxs-lookup"><span data-stu-id="89adb-163">Examples:</span></span>

- <span data-ttu-id="89adb-164">`<xref:System.String>` отображается как [String](https://docs.microsoft.com/dotnet/api/system.string);</span><span class="sxs-lookup"><span data-stu-id="89adb-164">`<xref:System.String>` renders as [String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="89adb-165">`<xref:System.String?displayProperty=nameWithType>` отображается как [System.String](https://docs.microsoft.com/dotnet/api/system.string);</span><span class="sxs-lookup"><span data-stu-id="89adb-165">`<xref:System.String?displayProperty=nameWithType>` renders as [System.String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="89adb-166">`[String class](xref:System.String)` отображается как [String class](https://docs.microsoft.com/dotnet/api/system.string).</span><span class="sxs-lookup"><span data-stu-id="89adb-166">`[String class](xref:System.String)` renders as [String class](https://docs.microsoft.com/dotnet/api/system.string)</span></span>

<span data-ttu-id="89adb-167">Дополнительные сведения об использовании этой нотации см. в разделе об [использовании перекрестных ссылок](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference).</span><span class="sxs-lookup"><span data-stu-id="89adb-167">For more information about using this notation, see [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference).</span></span>

<span data-ttu-id="89adb-168">Если идентификатор содержит специальные символы \`, \# или \*, значение UID должно быть закодировано в HTML как `%60`, `%23` и `%2A` соответственно.</span><span class="sxs-lookup"><span data-stu-id="89adb-168">Some UIDs contain the special characters \`, \# or \*, the UID value needs to be HTML encoded as `%60`, `%23` and `%2A` respectively.</span></span> <span data-ttu-id="89adb-169">Иногда круглые скобки тоже кодируются, но это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="89adb-169">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="89adb-170">Примеры:</span><span class="sxs-lookup"><span data-stu-id="89adb-170">Examples:</span></span>

- <span data-ttu-id="89adb-171">System.Threading.Tasks.Task\`1 заменяется на `System.Threading.Tasks.Task%601`;</span><span class="sxs-lookup"><span data-stu-id="89adb-171">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="89adb-172">System.Exception.\#ctor заменяется на `System.Exception.%23ctor`;</span><span class="sxs-lookup"><span data-stu-id="89adb-172">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="89adb-173">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) заменяется на `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`.</span><span class="sxs-lookup"><span data-stu-id="89adb-173">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<span data-ttu-id="89adb-174">UID для типов, список перегрузки членов или конкретный перегруженный член можно найти в `https://xref.docs.microsoft.com/autocomplete`.</span><span class="sxs-lookup"><span data-stu-id="89adb-174">You can find the UIDs of types, a member overload list, or a particular overloaded member from `https://xref.docs.microsoft.com/autocomplete`.</span></span> <span data-ttu-id="89adb-175">Строка запроса `?text=*\<type-member-name>*` определяет тип или элемент, UID которых вы хотите увидеть.</span><span class="sxs-lookup"><span data-stu-id="89adb-175">The query string `?text=*\<type-member-name>*` identifies the type or member whose UIDs you'd like to see.</span></span> <span data-ttu-id="89adb-176">Например, `https://xref.docs.microsoft.com/autocomplete?text=string.format` извлекает перегрузки [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format).</span><span class="sxs-lookup"><span data-stu-id="89adb-176">For example, `https://xref.docs.microsoft.com/autocomplete?text=string.format` retrieves the [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) overloads.</span></span> <span data-ttu-id="89adb-177">Инструмент ищет предоставленный параметр запроса `text` в любой части UID.</span><span class="sxs-lookup"><span data-stu-id="89adb-177">The tool searches for the provided `text` query parameter in any part of the UID.</span></span> <span data-ttu-id="89adb-178">Например, вы можете искать имя члена (ToString), частичное имя члена (ToStri), тип и имя члена (Double.ToString) и т. д.</span><span class="sxs-lookup"><span data-stu-id="89adb-178">For example, you can search for member name (ToString), partial member name (ToStri), type and member name (Double.ToString), etc.</span></span>

<span data-ttu-id="89adb-179">Если добавить символ \* (или `%2A`) после UID, ссылка будет представлять страницу перегрузки, а не конкретный API.</span><span class="sxs-lookup"><span data-stu-id="89adb-179">If you add a \* (or `%2A`) after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="89adb-180">Например, этот символ можно использовать, если требуется создать ссылку на страницу [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) обычным способом, а не на конкретную перегрузку, например [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_).</span><span class="sxs-lookup"><span data-stu-id="89adb-180">For example, you can use that when you want to link to the [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) page in a generic way instead of a specific overload such as [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_).</span></span> <span data-ttu-id="89adb-181">Также можно использовать \* для ссылки на страницу члена, если этот член не перегружен. Это позволит не включать список параметров в UID.</span><span class="sxs-lookup"><span data-stu-id="89adb-181">You can also use \* to link to a member page when the member is not overloaded; this saves you from having to include the parameter list in the UID.</span></span>

<span data-ttu-id="89adb-182">Чтобы сослаться на конкретную перегрузку метода, включите полное имя типа каждого параметра метода.</span><span class="sxs-lookup"><span data-stu-id="89adb-182">To link to a specific method overload, you must include the fully qualified type name of each of the method's parameters.</span></span> <span data-ttu-id="89adb-183">Например, \<xref:System.DateTime.ToString> ведет к методу [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) без параметров, а \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> ведет к методу [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_).</span><span class="sxs-lookup"><span data-stu-id="89adb-183">For example, \<xref:System.DateTime.ToString> links to the parameterless [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) method, while \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> links to the  [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) method.</span></span>

<span data-ttu-id="89adb-184">Чтобы сослаться на универсальный тип, например [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), используйте символ \` (`%60`) с указанием числа параметров универсального типа.</span><span class="sxs-lookup"><span data-stu-id="89adb-184">To link to a generic type, such as [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), you use the \` (`%60`) character followed by the number of generic type parameters.</span></span> <span data-ttu-id="89adb-185">Например, `<xref:System.Nullable%601>` ссылается на тип [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1), а `<xref:System.Func%602>` — на делегат [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2).</span><span class="sxs-lookup"><span data-stu-id="89adb-185">For example, `<xref:System.Nullable%601>` links to the [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) type, while `<xref:System.Func%602>` links to the [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) delegate.</span></span>

## <a name="code"></a><span data-ttu-id="89adb-186">Код</span><span class="sxs-lookup"><span data-stu-id="89adb-186">Code</span></span>

<span data-ttu-id="89adb-187">Лучший способ включить код — включить фрагменты кода из рабочего примера.</span><span class="sxs-lookup"><span data-stu-id="89adb-187">The best way to include code is to include snippets from a working sample.</span></span> <span data-ttu-id="89adb-188">Создайте свой пример кода в соответствии с инструкциями из статьи [об участии в составлении документации по .NET](dotnet-contribute-process.md#contributing-to-samples).</span><span class="sxs-lookup"><span data-stu-id="89adb-188">Create your sample following the instructions in the [contributing to .NET](dotnet-contribute-process.md#contributing-to-samples) article.</span></span> <span data-ttu-id="89adb-189">Основные правила по включению кода вы найдете в общих рекомендациях по [коду](how-to-write-use-markdown.md#code-includes).</span><span class="sxs-lookup"><span data-stu-id="89adb-189">The basic rules for including code are located in the general guidance on [code](how-to-write-use-markdown.md#code-includes).</span></span>

<span data-ttu-id="89adb-190">Вы можете включить код, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="89adb-190">You can include the code using the following syntax:</span></span>

```markdown
[!code-<language>[<name>](<pathToFile><queryoption><queryoptionvalue>)]
```

* <span data-ttu-id="89adb-191">`-<language>` (*необязательно*, но *рекомендуется*)</span><span class="sxs-lookup"><span data-stu-id="89adb-191">`-<language>` (*optional* but *recommended*)</span></span>
  * <span data-ttu-id="89adb-192">Язык фрагмента кода, на который мы ссылаемся.</span><span class="sxs-lookup"><span data-stu-id="89adb-192">Language of the code snippet being referenced.</span></span> <span data-ttu-id="89adb-193">Список поддерживаемых значений см. в разделе [Поддерживаемые языки](#supported-languages).</span><span class="sxs-lookup"><span data-stu-id="89adb-193">For a list of supported values, see [Supported languages](#supported-languages).</span></span>

* <span data-ttu-id="89adb-194">`<name>` (*необязательно*)</span><span class="sxs-lookup"><span data-stu-id="89adb-194">`<name>` (*optional*)</span></span>
  * <span data-ttu-id="89adb-195">Имя фрагмента кода.</span><span class="sxs-lookup"><span data-stu-id="89adb-195">Name for the code snippet.</span></span> <span data-ttu-id="89adb-196">Оно не влияет на выходной HTML, но его можно использовать для улучшения читаемости исходного Markdown.</span><span class="sxs-lookup"><span data-stu-id="89adb-196">It doesn’t have any impact on the output HTML, but you can use it to improve the readability of your Markdown source.</span></span>

* <span data-ttu-id="89adb-197">`<pathToFile>` (*обязательно*)</span><span class="sxs-lookup"><span data-stu-id="89adb-197">`<pathToFile>` (*mandatory*)</span></span>
  * <span data-ttu-id="89adb-198">Относительный путь в файловой системе, который указывает файл фрагмента кода для ссылки.</span><span class="sxs-lookup"><span data-stu-id="89adb-198">Relative path in the file system that indicates the code snippet file to reference.</span></span> <span data-ttu-id="89adb-199">Он может усложняться из-за разных репозиториев, составляющих набор документации по .NET.</span><span class="sxs-lookup"><span data-stu-id="89adb-199">This can be complicated by the different repos that make up the .NET doc set.</span></span> <span data-ttu-id="89adb-200">Примеры .NET находятся в репозитории dotnet/samples.</span><span class="sxs-lookup"><span data-stu-id="89adb-200">The .NET samples are in the dotnet/samples repo.</span></span> <span data-ttu-id="89adb-201">Все пути к фрагментам кода начинаются с `~/samples`, а остальное составляет путь к источнику в корне репозитория.</span><span class="sxs-lookup"><span data-stu-id="89adb-201">All snippet paths would start with `~/samples`, the rest of the path being the path to the source from the root of that repo.</span></span>

* <span data-ttu-id="89adb-202">`<queryoption>` (*необязательно*)</span><span class="sxs-lookup"><span data-stu-id="89adb-202">`<queryoption>` (*optional*)</span></span>
  * <span data-ttu-id="89adb-203">Используется для указания способа получения кода из файла:</span><span class="sxs-lookup"><span data-stu-id="89adb-203">Used to specify how the code should be retrieved from the file:</span></span>
    * <span data-ttu-id="89adb-204">`#`: `#{tagname}` (имя тега) *или* `#L{startlinenumber}-L{endlinenumber}` (диапазон строк).</span><span class="sxs-lookup"><span data-stu-id="89adb-204">`#`:  `#{tagname}` (tag name) *or* `#L{startlinenumber}-L{endlinenumber}` (line range).</span></span>
    <span data-ttu-id="89adb-205">Мы не рекомендуем использовать номера строк, потому что это ненадежное значение.</span><span class="sxs-lookup"><span data-stu-id="89adb-205">We discourage the use of line numbers because they are very brittle.</span></span> <span data-ttu-id="89adb-206">Лучше ссылаться на фрагменты кода по имени тега.</span><span class="sxs-lookup"><span data-stu-id="89adb-206">Tag name is the preferred way of referencing code snippets.</span></span> <span data-ttu-id="89adb-207">Используйте понятные имена тегов.</span><span class="sxs-lookup"><span data-stu-id="89adb-207">Use meaningful tag names.</span></span> <span data-ttu-id="89adb-208">(Многие фрагменты кода перенесены с предыдущей платформы, и теги называются `Snippet1`, `Snippet2` и т. д. Такую практику сложнее соблюдать.)</span><span class="sxs-lookup"><span data-stu-id="89adb-208">(Many snippets were migrated from a previous platform and the tags have names such as `Snippet1`, `Snippet2` etc. That practice is much harder to maintain.)</span></span>
    * <span data-ttu-id="89adb-209">`range`: `?range=1,3-5` Диапазон строк.</span><span class="sxs-lookup"><span data-stu-id="89adb-209">`range`: `?range=1,3-5` A range of lines.</span></span> <span data-ttu-id="89adb-210">Этот пример содержит строки 1, 3, 4 и 5.</span><span class="sxs-lookup"><span data-stu-id="89adb-210">This example includes lines 1, 3, 4, and 5.</span></span>

<span data-ttu-id="89adb-211">Рекомендуем использовать имя тега по возможности.</span><span class="sxs-lookup"><span data-stu-id="89adb-211">We recommend using the tag name option whenever possible.</span></span> <span data-ttu-id="89adb-212">Имя тега — это имя региона или комментария к коду в формате `Snippettagname`, присутствующее в исходном коде.</span><span class="sxs-lookup"><span data-stu-id="89adb-212">The tag name is the name of a region or of a code comment in the format of `Snippettagname` present in the source code.</span></span> <span data-ttu-id="89adb-213">В следующем примере показано, как сослаться на имя тега `BasicThrow`:</span><span class="sxs-lookup"><span data-stu-id="89adb-213">The following example shows how to refer to the tag name `BasicThrow`:</span></span>

```markdown
[!code-csharp[csrefKeyword#1](~/samples/snippets/snippets/csharp/language-reference/operators/ConditionalExamples.csConditionalRef)]
```

<span data-ttu-id="89adb-214">Относительный путь к источнику в репозитории **dotnet/samples** соответствует пути `~/samples`.</span><span class="sxs-lookup"><span data-stu-id="89adb-214">The relative path to the source in the **dotnet/samples** repo follows the `~/samples` path.</span></span>

<span data-ttu-id="89adb-215">Вы видите, как структурированы теги фрагмента кода [в этом исходном файле](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs).</span><span class="sxs-lookup"><span data-stu-id="89adb-215">And you can see how the snippet tags are structured in [this source file](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs).</span></span> <span data-ttu-id="89adb-216">Сведения о представлении имени тега в исходных файлах фрагмента кода для каждого языка см. в разделе с [рекомендациями по DocFX](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span><span class="sxs-lookup"><span data-stu-id="89adb-216">For details about tag name representation in code snippet source files by language, see the [DocFX guidelines](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span></span>

<span data-ttu-id="89adb-217">В следующем примере показан код, включенный на всех трех языках .NET:</span><span class="sxs-lookup"><span data-stu-id="89adb-217">The following example shows code included in all three .NET languages:</span></span>

```markdown
[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]
 [!code-csharp[ADCreateDomain#2](../../../samples/snippets/csharp/VS_Snippets_CLR/ADCreateDomain/CS/source2.cs#2)]
 [!code-vb[ADCreateDomain#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/ADCreateDomain/VB/source2.vb#2)]  
```

<span data-ttu-id="89adb-218">Если включать фрагменты кода из полных программ, весь код будет проходить через систему непрерывной интеграции.</span><span class="sxs-lookup"><span data-stu-id="89adb-218">Including snippets from full programs ensures that all code runs through our Continuous Integration (CI) system.</span></span> <span data-ttu-id="89adb-219">Но если вам нужно показать что-то, что вызывает ошибки во время компиляции или выполнения, используйте встроенные блоки кода.</span><span class="sxs-lookup"><span data-stu-id="89adb-219">However, if you need to show something that causes compile time or runtime errors, you can use inline code blocks.</span></span>

## <a name="images"></a><span data-ttu-id="89adb-220">Изображения</span><span class="sxs-lookup"><span data-stu-id="89adb-220">Images</span></span>

### <a name="static-image-or-animated-gif"></a><span data-ttu-id="89adb-221">Статическое изображение или анимационный GIF</span><span class="sxs-lookup"><span data-stu-id="89adb-221">Static image or animated GIF</span></span>

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a><span data-ttu-id="89adb-222">Изображения по ссылкам</span><span class="sxs-lookup"><span data-stu-id="89adb-222">Linked image</span></span>

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a><span data-ttu-id="89adb-223">Видеоролики</span><span class="sxs-lookup"><span data-stu-id="89adb-223">Videos</span></span>

<span data-ttu-id="89adb-224">Сейчас можно встраивать видео Channel 9 и YouTube со следующим синтаксисом:</span><span class="sxs-lookup"><span data-stu-id="89adb-224">Currently, you can embed both Channel 9 and YouTube videos with the following syntax:</span></span>

### <a name="channel-9"></a><span data-ttu-id="89adb-225">Channel 9</span><span class="sxs-lookup"><span data-stu-id="89adb-225">Channel 9</span></span>

```markdown
> [!VIDEO <channel9_video_link>]
```

<span data-ttu-id="89adb-226">Чтобы получить корректный URL-адрес видео, откройте вкладку **Встроить** под видео и скопируйте URL-адрес из элемента `<iframe>`.</span><span class="sxs-lookup"><span data-stu-id="89adb-226">To get the video's correct URL, select the **Embed** tab below the video frame, and copy the URL from the `<iframe>` element.</span></span> <span data-ttu-id="89adb-227">Например:</span><span class="sxs-lookup"><span data-stu-id="89adb-227">For example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a><span data-ttu-id="89adb-228">YouTube</span><span class="sxs-lookup"><span data-stu-id="89adb-228">YouTube</span></span>

<span data-ttu-id="89adb-229">Чтобы получить корректный URL-адрес видео, щелкните правой кнопкой мыши на видео, выберите **Копировать код внедрения** и скопируйте URL-адрес из элемента `<iframe>`.</span><span class="sxs-lookup"><span data-stu-id="89adb-229">To get the video's correct URL, right-click on the video, select **Copy Embed Code**, and copy the URL from the `<iframe>` element.</span></span>

```markdown
> [!VIDEO <youtube_video_link>]
```

<span data-ttu-id="89adb-230">Например:</span><span class="sxs-lookup"><span data-stu-id="89adb-230">For example:</span></span>

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a><span data-ttu-id="89adb-231">Расширения docs.microsoft</span><span class="sxs-lookup"><span data-stu-id="89adb-231">docs.microsoft extensions</span></span>

<span data-ttu-id="89adb-232">docs.microsoft предоставляет несколько дополнительных расширений для GitHub Flavored Markdown.</span><span class="sxs-lookup"><span data-stu-id="89adb-232">docs.microsoft provides a few additional extensions to GitHub Flavored Markdown.</span></span>

### <a name="checked-lists"></a><span data-ttu-id="89adb-233">Списки с установленными флажками</span><span class="sxs-lookup"><span data-stu-id="89adb-233">Checked lists</span></span>

<span data-ttu-id="89adb-234">К спискам можно применять настраиваемые стили.</span><span class="sxs-lookup"><span data-stu-id="89adb-234">A custom style is available for lists.</span></span> <span data-ttu-id="89adb-235">Можно отображать списки с зелеными флажками.</span><span class="sxs-lookup"><span data-stu-id="89adb-235">You can render lists with green check marks.</span></span>

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

<span data-ttu-id="89adb-236">Это выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="89adb-236">This renders as:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="89adb-237">Создание приложения .NET Core</span><span class="sxs-lookup"><span data-stu-id="89adb-237">How to create a .NET Core app</span></span>
> * <span data-ttu-id="89adb-238">Добавление ссылки на пакет Microsoft.XmlSerializer.Generator</span><span class="sxs-lookup"><span data-stu-id="89adb-238">How to add a reference to the Microsoft.XmlSerializer.Generator package</span></span>
> * <span data-ttu-id="89adb-239">Редактирование MyApp.csproj для добавления зависимостей</span><span class="sxs-lookup"><span data-stu-id="89adb-239">How to edit your MyApp.csproj to add dependencies</span></span>
> * <span data-ttu-id="89adb-240">Добавление класса как XmlSerializer</span><span class="sxs-lookup"><span data-stu-id="89adb-240">How to add a class and an XmlSerializer</span></span>
> * <span data-ttu-id="89adb-241">Создание и запуск приложения</span><span class="sxs-lookup"><span data-stu-id="89adb-241">How to build and run the application</span></span>

<span data-ttu-id="89adb-242">Пример списков с флажками в действии можно посмотреть в [документации по .NET Core](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).</span><span class="sxs-lookup"><span data-stu-id="89adb-242">You can see an example of checked lists in action in the [.NET Core docs](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).</span></span>

### <a name="buttons"></a><span data-ttu-id="89adb-243">Кнопки</span><span class="sxs-lookup"><span data-stu-id="89adb-243">Buttons</span></span>

<span data-ttu-id="89adb-244">Ссылки на кнопки:</span><span class="sxs-lookup"><span data-stu-id="89adb-244">Button links:</span></span>

```markdown
> [!div class="button"]
> [button links](dotnet-contribute.md)
```

<span data-ttu-id="89adb-245">Это выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="89adb-245">This renders as:</span></span>

> [!div class="button"]
> [<span data-ttu-id="89adb-246">ссылки на кнопки</span><span class="sxs-lookup"><span data-stu-id="89adb-246">button links</span></span>](dotnet-contribute.md)

<span data-ttu-id="89adb-247">Пример кнопок в действии можно посмотреть в [документации по Visual Studio](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="89adb-247">You can see an example of buttons in action in the [Visual Studio docs](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).</span></span>

### <a name="step-by-steps"></a><span data-ttu-id="89adb-248">Пошаговые инструкции</span><span class="sxs-lookup"><span data-stu-id="89adb-248">Step-by-steps</span></span>

```markdown
>[!div class="step-by-step"]
> [Pre](../docs/csharp/expression-trees-interpreting.md)
> [Next](../docs/csharp/expression-trees-translating.md)
```

<span data-ttu-id="89adb-249">Пример пошаговых инструкций в действии можно посмотреть в [руководстве по C#](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).</span><span class="sxs-lookup"><span data-stu-id="89adb-249">You can see an example of step-by-steps in action at the [C# Guide](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).</span></span>
