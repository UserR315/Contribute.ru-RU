---
title: Использование языка разметки Markdown для написания документации
description: В этой статье приводятся базовые и справочные сведения о языке разметки Markdown, используемом для написания статей на сайте docs.microsoft.com.
ms.date: 01/29/2019
ms.openlocfilehash: 5235189d11c8c20ac20c91572d8bafcf525fb7c0
ms.sourcegitcommit: fbdd61ae4fb3761aec072732eefcbf2c2dca8011
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/07/2019
ms.locfileid: "55887305"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="b3195-103">Использование языка разметки Markdown для написания документации</span><span class="sxs-lookup"><span data-stu-id="b3195-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="b3195-104">Статьи на сайте [docs.microsoft.com](http://docs.microsoft.com) написаны на [Markdown](https://daringfireball.net/projects/markdown/) — упрощенном языке разметки, который легко использовать и изучать.</span><span class="sxs-lookup"><span data-stu-id="b3195-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="b3195-105">Благодаря своей простоте он быстро становится отраслевым стандартом.</span><span class="sxs-lookup"><span data-stu-id="b3195-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="b3195-106">Серверная часть сайта docs.microsoft.com использует службы Open Publishing Services (OPS), поддерживающие разметку, совместимую с [CommonMark](https://commonmark.org/), проанализированную через [Markdig](https://github.com/lunet-io/markdig), а также [DocFX Flavored Markdown (DFM)](https://dotnet.github.io/docfx/).</span><span class="sxs-lookup"><span data-stu-id="b3195-106">The docs.microsoft.com site backend uses Open Publishing Services (OPS) which supports [CommonMark](https://commonmark.org/) compliant markdown parsed through [Markdig](https://github.com/lunet-io/markdig) and also supports [DocFX Flavored Markdown (DFM)](https://dotnet.github.io/docfx/).</span></span> <span data-ttu-id="b3195-107">Большая часть этих типов разметки совместима с [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), так как большинство документов хранятся на GitHub, где их можно править.</span><span class="sxs-lookup"><span data-stu-id="b3195-107">These markdown flavors are mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="b3195-108">Дополнительные функции добавляются с помощью расширений Markdown.</span><span class="sxs-lookup"><span data-stu-id="b3195-108">Additional functionality is added through Markdown extensions.</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="b3195-109">Базовые сведения о Markdown</span><span class="sxs-lookup"><span data-stu-id="b3195-109">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="b3195-110">Заголовки</span><span class="sxs-lookup"><span data-stu-id="b3195-110">Headings</span></span>

<span data-ttu-id="b3195-111">Чтобы создать заголовок, используйте знак (#), например:</span><span class="sxs-lookup"><span data-stu-id="b3195-111">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="b3195-112">В заголовках следует использовать стиль atx, то есть 1–6 символов решетки (#) в начале строки, чтобы указать на заголовок, соответствующий заголовкам HTML уровней с H1 по H6.</span><span class="sxs-lookup"><span data-stu-id="b3195-112">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="b3195-113">Сверху приводятся примеры заголовков с первого по четвертый уровень.</span><span class="sxs-lookup"><span data-stu-id="b3195-113">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="b3195-114">В статье **должен** быть только один заголовок первого уровня (H1), который будет отображаться как заголовок страницы.</span><span class="sxs-lookup"><span data-stu-id="b3195-114">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="b3195-115">Если заголовок заканчивается на символ `#`, добавьте в конце еще символ `#`, чтобы заголовок отображался правильно.</span><span class="sxs-lookup"><span data-stu-id="b3195-115">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="b3195-116">Например, `# Async Programming in F# #`.</span><span class="sxs-lookup"><span data-stu-id="b3195-116">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="b3195-117">Заголовки второго уровня создадут оглавление, которое будет отображаться в разделе "В этой статье" под заголовком статьи.</span><span class="sxs-lookup"><span data-stu-id="b3195-117">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="b3195-118">Полужирное начертание и курсив</span><span class="sxs-lookup"><span data-stu-id="b3195-118">Bold and italic text</span></span>

<span data-ttu-id="b3195-119">Чтобы задать для текста **полужирное начертание**, заключите его в двойные звездочки:</span><span class="sxs-lookup"><span data-stu-id="b3195-119">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="b3195-120">Чтобы задать для текста *курсивное начертание*, заключите его в одинарные звездочки:</span><span class="sxs-lookup"><span data-stu-id="b3195-120">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="b3195-121">Чтобы задать для текста ***полужирное и курсивное*** начертание, заключите его в тройные звездочки:</span><span class="sxs-lookup"><span data-stu-id="b3195-121">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="b3195-122">Блоки цитирования</span><span class="sxs-lookup"><span data-stu-id="b3195-122">Blockquotes</span></span>

<span data-ttu-id="b3195-123">Блоки цитирования создаются с помощью символа `>`:</span><span class="sxs-lookup"><span data-stu-id="b3195-123">Blockquotes are created using the `>` character:</span></span>

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="b3195-124">Предыдущий пример отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b3195-124">The preceding example renders as follows:</span></span>

> <span data-ttu-id="b3195-125">Засуха продолжалась десять миллионов лет, и царству ужасных ящеров уже давно пришел конец.</span><span class="sxs-lookup"><span data-stu-id="b3195-125">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="b3195-126">Здесь, близ экватора, на материке, который позднее назовут Африкой, с новой яростью вспыхнула борьба за существование, и еще не ясно было, кто выйдет из нее победителем.</span><span class="sxs-lookup"><span data-stu-id="b3195-126">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="b3195-127">На этой бесплодной, иссушенной зноем земле благоденствовать или хотя бы просто выжить могли только маленькие, или ловкие, или свирепые.</span><span class="sxs-lookup"><span data-stu-id="b3195-127">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="b3195-128">Списки</span><span class="sxs-lookup"><span data-stu-id="b3195-128">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="b3195-129">Неупорядоченный список</span><span class="sxs-lookup"><span data-stu-id="b3195-129">Unordered list</span></span>

<span data-ttu-id="b3195-130">Неупорядоченный (маркированный) список можно отформатировать с помощью звездочек или тире.</span><span class="sxs-lookup"><span data-stu-id="b3195-130">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="b3195-131">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="b3195-131">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="b3195-132">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="b3195-132">will be rendered as:</span></span>

- <span data-ttu-id="b3195-133">List item 1</span><span class="sxs-lookup"><span data-stu-id="b3195-133">List item 1</span></span>
- <span data-ttu-id="b3195-134">List item 2</span><span class="sxs-lookup"><span data-stu-id="b3195-134">List item 2</span></span>
- <span data-ttu-id="b3195-135">List item 3</span><span class="sxs-lookup"><span data-stu-id="b3195-135">List item 3</span></span>

<span data-ttu-id="b3195-136">Чтобы вложить один список в другой, добавьте отступ для элементов дочернего списка.</span><span class="sxs-lookup"><span data-stu-id="b3195-136">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="b3195-137">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="b3195-137">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="b3195-138">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="b3195-138">will be rendered as:</span></span>

- <span data-ttu-id="b3195-139">List item 1</span><span class="sxs-lookup"><span data-stu-id="b3195-139">List item 1</span></span>
  - <span data-ttu-id="b3195-140">List item A</span><span class="sxs-lookup"><span data-stu-id="b3195-140">List item A</span></span>
  - <span data-ttu-id="b3195-141">List item B</span><span class="sxs-lookup"><span data-stu-id="b3195-141">List item B</span></span>
- <span data-ttu-id="b3195-142">List item 2</span><span class="sxs-lookup"><span data-stu-id="b3195-142">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="b3195-143">Упорядоченный список</span><span class="sxs-lookup"><span data-stu-id="b3195-143">Ordered list</span></span>

<span data-ttu-id="b3195-144">Упорядоченный (ступенчатый) список можно отформатировать с помощью соответствующих цифр.</span><span class="sxs-lookup"><span data-stu-id="b3195-144">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="b3195-145">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="b3195-145">For example, the following Markdown:</span></span>

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="b3195-146">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="b3195-146">will be rendered as:</span></span>

1. <span data-ttu-id="b3195-147">First instruction</span><span class="sxs-lookup"><span data-stu-id="b3195-147">First instruction</span></span>
2. <span data-ttu-id="b3195-148">Second instruction</span><span class="sxs-lookup"><span data-stu-id="b3195-148">Second instruction</span></span>
3. <span data-ttu-id="b3195-149">Third instruction</span><span class="sxs-lookup"><span data-stu-id="b3195-149">Third instruction</span></span>

<span data-ttu-id="b3195-150">Чтобы вложить один список в другой, добавьте отступ для элементов дочернего списка.</span><span class="sxs-lookup"><span data-stu-id="b3195-150">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="b3195-151">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="b3195-151">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="b3195-152">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="b3195-152">will be rendered as:</span></span>

1. <span data-ttu-id="b3195-153">First instruction</span><span class="sxs-lookup"><span data-stu-id="b3195-153">First instruction</span></span>
   1. <span data-ttu-id="b3195-154">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="b3195-154">Sub-instruction</span></span>
   2. <span data-ttu-id="b3195-155">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="b3195-155">Sub-instruction</span></span>
2. <span data-ttu-id="b3195-156">Second instruction</span><span class="sxs-lookup"><span data-stu-id="b3195-156">Second instruction</span></span>

<span data-ttu-id="b3195-157">Обратите внимание, что мы используем "1."</span><span class="sxs-lookup"><span data-stu-id="b3195-157">Note that we use '1.'</span></span> <span data-ttu-id="b3195-158">для всех записей.</span><span class="sxs-lookup"><span data-stu-id="b3195-158">for all entries.</span></span> <span data-ttu-id="b3195-159">Так проще увидеть различия, когда потом будут добавлены новые шаги или удалены существующие.</span><span class="sxs-lookup"><span data-stu-id="b3195-159">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="b3195-160">Tables</span><span class="sxs-lookup"><span data-stu-id="b3195-160">Tables</span></span>

<span data-ttu-id="b3195-161">Таблицы не входят в основную спецификацию Markdown, но их поддерживает GFM.</span><span class="sxs-lookup"><span data-stu-id="b3195-161">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="b3195-162">Создавать таблицы можно с помощью символов вертикальной черты (|) и дефиса (-).</span><span class="sxs-lookup"><span data-stu-id="b3195-162">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="b3195-163">Дефисы позволяют создавать для каждого столбца заголовок. Вертикальные черты разделяют столбцы.</span><span class="sxs-lookup"><span data-stu-id="b3195-163">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="b3195-164">Чтобы таблица правильно отображалась, включите перед ней пустую строку.</span><span class="sxs-lookup"><span data-stu-id="b3195-164">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="b3195-165">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="b3195-165">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="b3195-166">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="b3195-166">will be rendered as:</span></span>

| <span data-ttu-id="b3195-167">Fun</span><span class="sxs-lookup"><span data-stu-id="b3195-167">Fun</span></span>                  | <span data-ttu-id="b3195-168">with</span><span class="sxs-lookup"><span data-stu-id="b3195-168">With</span></span>                 | <span data-ttu-id="b3195-169">Tables</span><span class="sxs-lookup"><span data-stu-id="b3195-169">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="b3195-170">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="b3195-170">left-aligned column</span></span>  | <span data-ttu-id="b3195-171">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="b3195-171">right-aligned column</span></span> | <span data-ttu-id="b3195-172">centered column</span><span class="sxs-lookup"><span data-stu-id="b3195-172">centered column</span></span> |
| <span data-ttu-id="b3195-173">$100</span><span class="sxs-lookup"><span data-stu-id="b3195-173">$100</span></span>                 | <span data-ttu-id="b3195-174">$100</span><span class="sxs-lookup"><span data-stu-id="b3195-174">$100</span></span>                 | <span data-ttu-id="b3195-175">$100</span><span class="sxs-lookup"><span data-stu-id="b3195-175">$100</span></span>            |
| <span data-ttu-id="b3195-176">$10</span><span class="sxs-lookup"><span data-stu-id="b3195-176">$10</span></span>                  | <span data-ttu-id="b3195-177">$10</span><span class="sxs-lookup"><span data-stu-id="b3195-177">$10</span></span>                  | <span data-ttu-id="b3195-178">$10</span><span class="sxs-lookup"><span data-stu-id="b3195-178">$10</span></span>             |
| <span data-ttu-id="b3195-179">$1</span><span class="sxs-lookup"><span data-stu-id="b3195-179">$1</span></span>                   | <span data-ttu-id="b3195-180">$1</span><span class="sxs-lookup"><span data-stu-id="b3195-180">$1</span></span>                   | <span data-ttu-id="b3195-181">$1</span><span class="sxs-lookup"><span data-stu-id="b3195-181">$1</span></span>              |

<span data-ttu-id="b3195-182">Дополнительные сведения о создании таблиц:</span><span class="sxs-lookup"><span data-stu-id="b3195-182">For more information on creating tables, see:</span></span>

- <span data-ttu-id="b3195-183">[Функция обтекания таблиц](#table-wrapping) в Markdig, которая поможет при форматировании широких таблиц.</span><span class="sxs-lookup"><span data-stu-id="b3195-183">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="b3195-184">Статья на сайте GitHub [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/) (Организация информации с помощью таблиц).</span><span class="sxs-lookup"><span data-stu-id="b3195-184">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="b3195-185">Веб-приложение [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="b3195-185">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="b3195-186">Статья Адама Притчарда (Adam Pritchard) [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables) (Шпаргалка по Markdown).</span><span class="sxs-lookup"><span data-stu-id="b3195-186">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="b3195-187">Статья Майкла Фортина (Michel Fortin) [Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) (Расширение Markdown Extra).</span><span class="sxs-lookup"><span data-stu-id="b3195-187">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="b3195-188">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/) (Преобразование таблиц HTML в Markdown).</span><span class="sxs-lookup"><span data-stu-id="b3195-188">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="b3195-189">Создание ссылок</span><span class="sxs-lookup"><span data-stu-id="b3195-189">Links</span></span>

<span data-ttu-id="b3195-190">Синтаксис Markdown для встроенной ссылки состоит из части `[link text]`, представляющей текст гиперссылки, и части `(file-name.md)` — URL-адреса или имени файла, на который дается ссылка:</span><span class="sxs-lookup"><span data-stu-id="b3195-190">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="b3195-191">Дополнительные сведения о ссылках:</span><span class="sxs-lookup"><span data-stu-id="b3195-191">For more information on linking, see:</span></span>

- <span data-ttu-id="b3195-192">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax#link) (Руководство по синтаксису Markdown), в котором предоставлена основная информация по поддержке ссылок Markdown.</span><span class="sxs-lookup"><span data-stu-id="b3195-192">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="b3195-193">Страница [Ссылки](how-to-write-links.md) в этом руководстве содержит сведения о дополнительном синтаксисе Markdig для ссылок.</span><span class="sxs-lookup"><span data-stu-id="b3195-193">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="b3195-194">Фрагменты кода</span><span class="sxs-lookup"><span data-stu-id="b3195-194">Code snippets</span></span>

<span data-ttu-id="b3195-195">Markdown поддерживает как встраивание фрагментов кода в предложение, так и их размещение между предложениями в виде отдельных огражденных блоков.</span><span class="sxs-lookup"><span data-stu-id="b3195-195">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="b3195-196">Дополнительная информация:</span><span class="sxs-lookup"><span data-stu-id="b3195-196">For details, see:</span></span>

- [<span data-ttu-id="b3195-197">Сведения о собственной поддержке блоков кода Markdown</span><span class="sxs-lookup"><span data-stu-id="b3195-197">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="b3195-198">Сведения о поддержке GFM для ограждения кода и выделения синтаксиса</span><span class="sxs-lookup"><span data-stu-id="b3195-198">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="b3195-199">Огражденные блоки кода — это простой способ выделить синтаксис для фрагментов кода.</span><span class="sxs-lookup"><span data-stu-id="b3195-199">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="b3195-200">Общий формат огражденных блоков кода:</span><span class="sxs-lookup"><span data-stu-id="b3195-200">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="b3195-201">Псевдоним после трех начальных символов обратной галочки \` определяет использование выделения.</span><span class="sxs-lookup"><span data-stu-id="b3195-201">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="b3195-202">Ниже представлен список часто используемых языков программирования для написания документации и приводятся соответствующие метки.</span><span class="sxs-lookup"><span data-stu-id="b3195-202">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="b3195-203">Все эти языки поддерживают понятные имена, а большинство из них — выделение языка в имени.</span><span class="sxs-lookup"><span data-stu-id="b3195-203">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="b3195-204">Имя</span><span class="sxs-lookup"><span data-stu-id="b3195-204">Name</span></span>|<span data-ttu-id="b3195-205">Метка Markdown</span><span class="sxs-lookup"><span data-stu-id="b3195-205">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="b3195-206">.NET Console</span><span class="sxs-lookup"><span data-stu-id="b3195-206">.NET Console</span></span>|<span data-ttu-id="b3195-207">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="b3195-207">dotnetcli</span></span>|
|<span data-ttu-id="b3195-208">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="b3195-208">ASP.NET (C#)</span></span>|<span data-ttu-id="b3195-209">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="b3195-209">aspx-csharp</span></span>|
|<span data-ttu-id="b3195-210">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="b3195-210">ASP.NET (VB)</span></span>|<span data-ttu-id="b3195-211">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="b3195-211">aspx-vb</span></span>|
|<span data-ttu-id="b3195-212">AzCopy</span><span class="sxs-lookup"><span data-stu-id="b3195-212">AzCopy</span></span>|<span data-ttu-id="b3195-213">azcopy</span><span class="sxs-lookup"><span data-stu-id="b3195-213">azcopy</span></span>|
|<span data-ttu-id="b3195-214">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="b3195-214">Azure CLI</span></span>|<span data-ttu-id="b3195-215">azurecli</span><span class="sxs-lookup"><span data-stu-id="b3195-215">azurecli</span></span>|
|<span data-ttu-id="b3195-216">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b3195-216">Azure PowerShell</span></span>|<span data-ttu-id="b3195-217">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="b3195-217">azurepowershell</span></span>|
|<span data-ttu-id="b3195-218">C++</span><span class="sxs-lookup"><span data-stu-id="b3195-218">C++</span></span>|<span data-ttu-id="b3195-219">cpp</span><span class="sxs-lookup"><span data-stu-id="b3195-219">cpp</span></span>|
|<span data-ttu-id="b3195-220">C++/CX</span><span class="sxs-lookup"><span data-stu-id="b3195-220">C++/CX</span></span>|<span data-ttu-id="b3195-221">cppcx</span><span class="sxs-lookup"><span data-stu-id="b3195-221">cppcx</span></span>|
|<span data-ttu-id="b3195-222">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="b3195-222">C++/WinRT</span></span>|<span data-ttu-id="b3195-223">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="b3195-223">cppwinrt</span></span>|
|<span data-ttu-id="b3195-224">C#</span><span class="sxs-lookup"><span data-stu-id="b3195-224">C#</span></span>|<span data-ttu-id="b3195-225">csharp</span><span class="sxs-lookup"><span data-stu-id="b3195-225">csharp</span></span>|
|<span data-ttu-id="b3195-226">C# в браузере</span><span class="sxs-lookup"><span data-stu-id="b3195-226">C# in browser</span></span>|<span data-ttu-id="b3195-227">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="b3195-227">csharp-interactive</span></span>|
|<span data-ttu-id="b3195-228">Консоль</span><span class="sxs-lookup"><span data-stu-id="b3195-228">Console</span></span>|<span data-ttu-id="b3195-229">консоль</span><span class="sxs-lookup"><span data-stu-id="b3195-229">console</span></span>|
|<span data-ttu-id="b3195-230">CSHTML</span><span class="sxs-lookup"><span data-stu-id="b3195-230">CSHTML</span></span>|<span data-ttu-id="b3195-231">cshtml</span><span class="sxs-lookup"><span data-stu-id="b3195-231">cshtml</span></span>|
|<span data-ttu-id="b3195-232">DAX</span><span class="sxs-lookup"><span data-stu-id="b3195-232">DAX</span></span>|<span data-ttu-id="b3195-233">dax</span><span class="sxs-lookup"><span data-stu-id="b3195-233">dax</span></span>|
|<span data-ttu-id="b3195-234">Docker</span><span class="sxs-lookup"><span data-stu-id="b3195-234">Docker</span></span>|<span data-ttu-id="b3195-235">dockerfile</span><span class="sxs-lookup"><span data-stu-id="b3195-235">dockerfile</span></span>|
|<span data-ttu-id="b3195-236">F#</span><span class="sxs-lookup"><span data-stu-id="b3195-236">F#</span></span>|<span data-ttu-id="b3195-237">fsharp</span><span class="sxs-lookup"><span data-stu-id="b3195-237">fsharp</span></span>|
|<span data-ttu-id="b3195-238">Go</span><span class="sxs-lookup"><span data-stu-id="b3195-238">Go</span></span>|<span data-ttu-id="b3195-239">go</span><span class="sxs-lookup"><span data-stu-id="b3195-239">go</span></span>|
|<span data-ttu-id="b3195-240">HTML</span><span class="sxs-lookup"><span data-stu-id="b3195-240">HTML</span></span>|<span data-ttu-id="b3195-241">html</span><span class="sxs-lookup"><span data-stu-id="b3195-241">html</span></span>|
|<span data-ttu-id="b3195-242">HTTP</span><span class="sxs-lookup"><span data-stu-id="b3195-242">HTTP</span></span>|<span data-ttu-id="b3195-243">http</span><span class="sxs-lookup"><span data-stu-id="b3195-243">http</span></span>|
|<span data-ttu-id="b3195-244">Java</span><span class="sxs-lookup"><span data-stu-id="b3195-244">Java</span></span>|<span data-ttu-id="b3195-245">java</span><span class="sxs-lookup"><span data-stu-id="b3195-245">java</span></span>|
|<span data-ttu-id="b3195-246">JavaScript</span><span class="sxs-lookup"><span data-stu-id="b3195-246">JavaScript</span></span>|<span data-ttu-id="b3195-247">javascript</span><span class="sxs-lookup"><span data-stu-id="b3195-247">javascript</span></span>|
|<span data-ttu-id="b3195-248">JSON</span><span class="sxs-lookup"><span data-stu-id="b3195-248">JSON</span></span>|<span data-ttu-id="b3195-249">json</span><span class="sxs-lookup"><span data-stu-id="b3195-249">json</span></span>|
|<span data-ttu-id="b3195-250">Язык запросов Kusto</span><span class="sxs-lookup"><span data-stu-id="b3195-250">Kusto Query Language</span></span>|<span data-ttu-id="b3195-251">kusto</span><span class="sxs-lookup"><span data-stu-id="b3195-251">kusto</span></span>|
|<span data-ttu-id="b3195-252">Markdown</span><span class="sxs-lookup"><span data-stu-id="b3195-252">Markdown</span></span>|<span data-ttu-id="b3195-253">md</span><span class="sxs-lookup"><span data-stu-id="b3195-253">md</span></span>|
|<span data-ttu-id="b3195-254">Objective-C</span><span class="sxs-lookup"><span data-stu-id="b3195-254">Objective-C</span></span>|<span data-ttu-id="b3195-255">objc</span><span class="sxs-lookup"><span data-stu-id="b3195-255">objc</span></span>|
|<span data-ttu-id="b3195-256">OData</span><span class="sxs-lookup"><span data-stu-id="b3195-256">OData</span></span>|<span data-ttu-id="b3195-257">odata</span><span class="sxs-lookup"><span data-stu-id="b3195-257">odata</span></span>|
|<span data-ttu-id="b3195-258">PHP</span><span class="sxs-lookup"><span data-stu-id="b3195-258">PHP</span></span>|<span data-ttu-id="b3195-259">php</span><span class="sxs-lookup"><span data-stu-id="b3195-259">php</span></span>|
|<span data-ttu-id="b3195-260">PowerApps (десятичный разделитель — точка)</span><span class="sxs-lookup"><span data-stu-id="b3195-260">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="b3195-261">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="b3195-261">powerapps-dot</span></span>|
|<span data-ttu-id="b3195-262">PowerApps (десятичный разделитель — запятая)</span><span class="sxs-lookup"><span data-stu-id="b3195-262">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="b3195-263">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="b3195-263">powerapps-comma</span></span>|
|<span data-ttu-id="b3195-264">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b3195-264">PowerShell</span></span>|<span data-ttu-id="b3195-265">powershell</span><span class="sxs-lookup"><span data-stu-id="b3195-265">powershell</span></span>|
|<span data-ttu-id="b3195-266">Python</span><span class="sxs-lookup"><span data-stu-id="b3195-266">Python</span></span>|<span data-ttu-id="b3195-267">python</span><span class="sxs-lookup"><span data-stu-id="b3195-267">python</span></span>|
|<span data-ttu-id="b3195-268">Q#</span><span class="sxs-lookup"><span data-stu-id="b3195-268">Q#</span></span>|<span data-ttu-id="b3195-269">qsharp</span><span class="sxs-lookup"><span data-stu-id="b3195-269">qsharp</span></span>|
|<span data-ttu-id="b3195-270">R</span><span class="sxs-lookup"><span data-stu-id="b3195-270">R</span></span>|<span data-ttu-id="b3195-271">r</span><span class="sxs-lookup"><span data-stu-id="b3195-271">r</span></span>|
|<span data-ttu-id="b3195-272">Ruby</span><span class="sxs-lookup"><span data-stu-id="b3195-272">Ruby</span></span>|<span data-ttu-id="b3195-273">ruby</span><span class="sxs-lookup"><span data-stu-id="b3195-273">ruby</span></span>|
|<span data-ttu-id="b3195-274">SQL</span><span class="sxs-lookup"><span data-stu-id="b3195-274">SQL</span></span>|<span data-ttu-id="b3195-275">sql</span><span class="sxs-lookup"><span data-stu-id="b3195-275">sql</span></span>|
|<span data-ttu-id="b3195-276">Swift</span><span class="sxs-lookup"><span data-stu-id="b3195-276">Swift</span></span>|<span data-ttu-id="b3195-277">swift</span><span class="sxs-lookup"><span data-stu-id="b3195-277">swift</span></span>|
|<span data-ttu-id="b3195-278">TypeScript</span><span class="sxs-lookup"><span data-stu-id="b3195-278">TypeScript</span></span>|<span data-ttu-id="b3195-279">typescript</span><span class="sxs-lookup"><span data-stu-id="b3195-279">typescript</span></span>|
|<span data-ttu-id="b3195-280">VB</span><span class="sxs-lookup"><span data-stu-id="b3195-280">VB</span></span>|<span data-ttu-id="b3195-281">vb</span><span class="sxs-lookup"><span data-stu-id="b3195-281">vb</span></span>|
|<span data-ttu-id="b3195-282">XAML</span><span class="sxs-lookup"><span data-stu-id="b3195-282">XAML</span></span>|<span data-ttu-id="b3195-283">xaml</span><span class="sxs-lookup"><span data-stu-id="b3195-283">xaml</span></span>|
|<span data-ttu-id="b3195-284">XML</span><span class="sxs-lookup"><span data-stu-id="b3195-284">XML</span></span>|<span data-ttu-id="b3195-285">xml</span><span class="sxs-lookup"><span data-stu-id="b3195-285">xml</span></span>|

<span data-ttu-id="b3195-286">Имя `csharp-interactive` указывает на язык C# и возможность запускать примеры в браузере.</span><span class="sxs-lookup"><span data-stu-id="b3195-286">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="b3195-287">Эти фрагменты кода компилируются и выполняются в контейнере Docker, а результаты выполнения программы отображаются в окне браузера пользователя.</span><span class="sxs-lookup"><span data-stu-id="b3195-287">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="b3195-288">Пример. C\#</span><span class="sxs-lookup"><span data-stu-id="b3195-288">Example: C\#</span></span>

<span data-ttu-id="b3195-289">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="b3195-289">__Markdown__</span></span>

    ```csharp
    // Hello1.cs
    public class Hello1
    {
        public static void Main()
        {
            System.Console.WriteLine("Hello, World!");
        }
    }
    ```

<span data-ttu-id="b3195-290">__Отображение__</span><span class="sxs-lookup"><span data-stu-id="b3195-290">__Render__</span></span>

```csharp
// Hello1.cs
public class Hello1
{
    public static void Main()
    {
        System.Console.WriteLine("Hello, World!");
    }
}
```

#### <a name="example-sql"></a><span data-ttu-id="b3195-291">Пример. SQL</span><span class="sxs-lookup"><span data-stu-id="b3195-291">Example: SQL</span></span>

<span data-ttu-id="b3195-292">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="b3195-292">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="b3195-293">__Отображение__</span><span class="sxs-lookup"><span data-stu-id="b3195-293">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="b3195-294">Настраиваемые расширения OPS для Markdown</span><span class="sxs-lookup"><span data-stu-id="b3195-294">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="b3195-295">Службы Open Publishing Services (OPS) используют Markdig, синтаксический анализатор Markdown, обеспечивающий высокую совместимость с диалектом GitHub Flavored Markdown (GFM).</span><span class="sxs-lookup"><span data-stu-id="b3195-295">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="b3195-296">Markdig добавляет дополнительные функции за счет расширений Markdown.</span><span class="sxs-lookup"><span data-stu-id="b3195-296">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="b3195-297">Поэтому для справки мы включили в этот материал некоторые разделы из руководства по разработке OPS.</span><span class="sxs-lookup"><span data-stu-id="b3195-297">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="b3195-298">(Например, см. в содержании разделы "Markdig и расширения Markdown" и "Фрагменты кода".)</span><span class="sxs-lookup"><span data-stu-id="b3195-298">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="b3195-299">В статьях документации для общего форматирования, например для создания абзацев, ссылок, списков и заголовков, используется GFM.</span><span class="sxs-lookup"><span data-stu-id="b3195-299">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="b3195-300">Для расширенного форматирования в статьях можно использовать следующие функции Markdig:</span><span class="sxs-lookup"><span data-stu-id="b3195-300">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="b3195-301">Блоки заметок</span><span class="sxs-lookup"><span data-stu-id="b3195-301">Note blocks</span></span>
- <span data-ttu-id="b3195-302">Включаемые файлы</span><span class="sxs-lookup"><span data-stu-id="b3195-302">Include files</span></span>
- <span data-ttu-id="b3195-303">Селекторы</span><span class="sxs-lookup"><span data-stu-id="b3195-303">Selectors</span></span>
- <span data-ttu-id="b3195-304">внедренные видео;</span><span class="sxs-lookup"><span data-stu-id="b3195-304">Embedded videos</span></span>
- <span data-ttu-id="b3195-305">фрагменты или примеры кода.</span><span class="sxs-lookup"><span data-stu-id="b3195-305">Code snippets/samples</span></span>

<span data-ttu-id="b3195-306">Полный список см. в разделах "Markdig и расширения Markdown" и "Фрагменты кода".</span><span class="sxs-lookup"><span data-stu-id="b3195-306">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="b3195-307">Блоки заметок</span><span class="sxs-lookup"><span data-stu-id="b3195-307">Note blocks</span></span>

<span data-ttu-id="b3195-308">Есть четыре типа блоков заметок, которые позволяют привлечь внимание к определенному содержимому:</span><span class="sxs-lookup"><span data-stu-id="b3195-308">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="b3195-309">ПРИМЕЧАНИЕ;</span><span class="sxs-lookup"><span data-stu-id="b3195-309">NOTE</span></span>
- <span data-ttu-id="b3195-310">ПРЕДУПРЕЖДЕНИЕ;</span><span class="sxs-lookup"><span data-stu-id="b3195-310">WARNING</span></span>
- <span data-ttu-id="b3195-311">СОВЕТ;</span><span class="sxs-lookup"><span data-stu-id="b3195-311">TIP</span></span>
- <span data-ttu-id="b3195-312">ВАЖНО.</span><span class="sxs-lookup"><span data-stu-id="b3195-312">IMPORTANT</span></span>

<span data-ttu-id="b3195-313">В целом не следует часто использовать блоки заметок, так как они могут отвлекать пользователя от основного содержимого.</span><span class="sxs-lookup"><span data-stu-id="b3195-313">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="b3195-314">Хотя эти элементы также поддерживают блоки кода, изображения, списки и ссылки, лучше не перегружать их, делая простыми и понятными.</span><span class="sxs-lookup"><span data-stu-id="b3195-314">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="b3195-315">Примеры:</span><span class="sxs-lookup"><span data-stu-id="b3195-315">Examples:</span></span>

```markdown
> [!NOTE]
> This is a NOTE

> [!WARNING]
> This is a WARNING

> [!TIP]
> This is a TIP

> [!IMPORTANT]
> This is IMPORTANT
```

<span data-ttu-id="b3195-316">Это выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b3195-316">These render as follows:</span></span>

> [!NOTE]
> <span data-ttu-id="b3195-317">Это ПРИМЕЧАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3195-317">This is a NOTE</span></span>

> [!WARNING]
> <span data-ttu-id="b3195-318">Это ПРЕДУПРЕЖДЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3195-318">This is a WARNING</span></span>

> [!TIP]
> <span data-ttu-id="b3195-319">Это СОВЕТ</span><span class="sxs-lookup"><span data-stu-id="b3195-319">This is a TIP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b3195-320">Это ВАЖНО</span><span class="sxs-lookup"><span data-stu-id="b3195-320">This is IMPORTANT</span></span>

### <a name="include-files"></a><span data-ttu-id="b3195-321">Включаемые файлы</span><span class="sxs-lookup"><span data-stu-id="b3195-321">Include files</span></span>

<span data-ttu-id="b3195-322">Если вы хотите добавить в файлы статей многократно используемые изображения или текст, воспользуйтесь доступной в Markdig функцией включения ("include") файлов по ссылке.</span><span class="sxs-lookup"><span data-stu-id="b3195-322">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="b3195-323">Функция указывает OPS включить файл в файл статьи во время сборки, чтобы он стал частью опубликованной статьи.</span><span class="sxs-lookup"><span data-stu-id="b3195-323">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="b3195-324">Существует три типа включения файлов для многократного использования содержимого:</span><span class="sxs-lookup"><span data-stu-id="b3195-324">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="b3195-325">Встроенные: Используются для многократного использования фрагмента стандартного текста путем его встраивания в другое предложение.</span><span class="sxs-lookup"><span data-stu-id="b3195-325">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="b3195-326">Блочные: Используются для многократного использования всего файла Markdown в качестве блока путем его вложения в раздел или статью.</span><span class="sxs-lookup"><span data-stu-id="b3195-326">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="b3195-327">Изображения: Так на платформе Docs реализовано стандартное включение изображений.</span><span class="sxs-lookup"><span data-stu-id="b3195-327">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="b3195-328">Встроенные и блочные включаемые файлы — это простые файлы Markdown с расширением .md.</span><span class="sxs-lookup"><span data-stu-id="b3195-328">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="b3195-329">Они могут содержать любую допустимую разметку Markdown.</span><span class="sxs-lookup"><span data-stu-id="b3195-329">It can contain any valid Markdown.</span></span> <span data-ttu-id="b3195-330">Все включаемые файлы Markdown должны быть помещены в [общий подкаталог `/includes`](git-github-fundamentals.md#includes-subdirectory) в корневом каталоге репозитория.</span><span class="sxs-lookup"><span data-stu-id="b3195-330">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="b3195-331">Когда статья публикуется, включаемый файл легко интегрируется в нее.</span><span class="sxs-lookup"><span data-stu-id="b3195-331">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="b3195-332">Ниже приведены требования к включаемым файлам и соображения по работе с ними:</span><span class="sxs-lookup"><span data-stu-id="b3195-332">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="b3195-333">Используйте включаемые файлы, если вам нужно, чтобы один и тот же текст отображался в нескольких статьях.</span><span class="sxs-lookup"><span data-stu-id="b3195-333">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="b3195-334">Блочные включаемые файлы предназначены для значительных объемов текста: один или два абзаца, общая процедура или общий раздел.</span><span class="sxs-lookup"><span data-stu-id="b3195-334">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="b3195-335">Не используйте их для фрагментов текста меньше одного предложения.</span><span class="sxs-lookup"><span data-stu-id="b3195-335">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="b3195-336">Включаемые файлы не будут отображаться в представлении статьи на GitHub, так как они работают только с Markdig-расширениями.</span><span class="sxs-lookup"><span data-stu-id="b3195-336">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="b3195-337">Они отображаются только после публикации.</span><span class="sxs-lookup"><span data-stu-id="b3195-337">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="b3195-338">Весь текст во включаемом файле должен состоять из полноценных предложений или фраз, не зависящих от остального текста статьи, в которую добавляется ссылка на такой файл.</span><span class="sxs-lookup"><span data-stu-id="b3195-338">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="b3195-339">Если не следовать этой инструкции, в статье создаются непереводимые строки, которые нарушают процесс локализации.</span><span class="sxs-lookup"><span data-stu-id="b3195-339">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="b3195-340">Не внедряйте одни включаемые файлы в другие.</span><span class="sxs-lookup"><span data-stu-id="b3195-340">Don't embed include references within other include files.</span></span> <span data-ttu-id="b3195-341">Такая возможность не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b3195-341">They are not supported.</span></span>
- <span data-ttu-id="b3195-342">Файлы мультимедиа должны быть помещены в отдельную папку мультимедиа в подкаталоге включаемых файлов. Например, `<repo>`/включаемые файлы/папка мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b3195-342">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="b3195-343">В корне каталога мультимедиа не должны содержаться изображения.</span><span class="sxs-lookup"><span data-stu-id="b3195-343">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="b3195-344">Если во включаемом файле нет изображений, соответствующий каталог мультимедиа не требуется.</span><span class="sxs-lookup"><span data-stu-id="b3195-344">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="b3195-345">Как и в обычных статьях, не используйте общий файл мультимедиа для включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="b3195-345">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="b3195-346">Для каждого включаемого файла в статье должен быть создан отдельный файл с уникальным именем.</span><span class="sxs-lookup"><span data-stu-id="b3195-346">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="b3195-347">Файл мультимедиа должен храниться в папке мультимедиа, связанной с включаемым файлом.</span><span class="sxs-lookup"><span data-stu-id="b3195-347">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="b3195-348">Не используйте включаемый файл как единственное содержимое статьи.</span><span class="sxs-lookup"><span data-stu-id="b3195-348">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="b3195-349">Включаемые файлы предназначены для дополнения основных материалов статьи.</span><span class="sxs-lookup"><span data-stu-id="b3195-349">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="b3195-350">Пример.</span><span class="sxs-lookup"><span data-stu-id="b3195-350">Example:</span></span>

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="b3195-351">Селекторы</span><span class="sxs-lookup"><span data-stu-id="b3195-351">Selectors</span></span>

<span data-ttu-id="b3195-352">В технических статьях селекторы применяются для создания разных вариантов содержимого, чтобы проиллюстрировать различия в реализации, связанные с использованием нескольких технологий или платформ.</span><span class="sxs-lookup"><span data-stu-id="b3195-352">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="b3195-353">Это в особенности применимо к материалам о мобильных платформах для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="b3195-353">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="b3195-354">Сейчас в Markdig есть два типа селекторов: для единичного и множественного выбора.</span><span class="sxs-lookup"><span data-stu-id="b3195-354">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="b3195-355">В каждой статье с возможностью выбора используется одна и та же разметка Markdown для селектора. Поэтому рекомендуется поместить селектор для статьи во включаемый файл.</span><span class="sxs-lookup"><span data-stu-id="b3195-355">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="b3195-356">Затем нужно добавить ссылки на этот файл во все статьи, для которых используется селектор.</span><span class="sxs-lookup"><span data-stu-id="b3195-356">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="b3195-357">Ниже приведен пример селектора:</span><span class="sxs-lookup"><span data-stu-id="b3195-357">The following shows an example selector:</span></span>

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="b3195-358">Пример селекторов в действии можно посмотреть в [документации по Azure](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span><span class="sxs-lookup"><span data-stu-id="b3195-358">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="b3195-359">Включение фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="b3195-359">Code include references</span></span>

<span data-ttu-id="b3195-360">В Markdig есть расширение с расширенными функциями для включения в статью фрагментов кода.</span><span class="sxs-lookup"><span data-stu-id="b3195-360">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="b3195-361">Этот формат обеспечивает расширенный рендеринг на основе функций GFM, таких как выбор языка программирования и раскраска синтаксиса, а также другие полезные функции, например:</span><span class="sxs-lookup"><span data-stu-id="b3195-361">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="b3195-362">включение централизованных примеров или фрагментов кода из внешнего репозитория;</span><span class="sxs-lookup"><span data-stu-id="b3195-362">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="b3195-363">пользовательский интерфейс с вкладками для отображения нескольких версий примеров кода на разных языках.</span><span class="sxs-lookup"><span data-stu-id="b3195-363">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="b3195-364">Сбои и устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="b3195-364">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="b3195-365">Замещающий текст</span><span class="sxs-lookup"><span data-stu-id="b3195-365">Alt text</span></span>

<span data-ttu-id="b3195-366">Замещающий текст, который содержит символы подчеркивания, отображается некорректно.</span><span class="sxs-lookup"><span data-stu-id="b3195-366">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="b3195-367">Например, вместо</span><span class="sxs-lookup"><span data-stu-id="b3195-367">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="b3195-368">используйте следующий вариант, позволяющий избежать символов подчеркивания:</span><span class="sxs-lookup"><span data-stu-id="b3195-368">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="b3195-369">Апострофы и кавычки</span><span class="sxs-lookup"><span data-stu-id="b3195-369">Apostrophes and quotation marks</span></span>

<span data-ttu-id="b3195-370">Если вы копируете текст из Word в редактор Markdown, он может содержать книжные (изогнутые) апострофы или кавычки.</span><span class="sxs-lookup"><span data-stu-id="b3195-370">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="b3195-371">Их нужно заменить кодом или обычными апострофами или кавычками.</span><span class="sxs-lookup"><span data-stu-id="b3195-371">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="b3195-372">В противном случае после публикации файла может отобразиться нечитаемый текст, например: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="b3195-372">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="b3195-373">Ниже приведены кодировки для этих знаков пунктуации:</span><span class="sxs-lookup"><span data-stu-id="b3195-373">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="b3195-374">левая (открывающая) кавычка: `&#8220;`;</span><span class="sxs-lookup"><span data-stu-id="b3195-374">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="b3195-375">правая (закрывающая) кавычка: `&#8221;`;</span><span class="sxs-lookup"><span data-stu-id="b3195-375">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="b3195-376">правая закрывающая одинарная кавычка или апостроф: `&#8217;`;</span><span class="sxs-lookup"><span data-stu-id="b3195-376">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="b3195-377">левая открывающая одинарная кавычка (используется редко): `&#8216;`.</span><span class="sxs-lookup"><span data-stu-id="b3195-377">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="b3195-378">Угловые скобки</span><span class="sxs-lookup"><span data-stu-id="b3195-378">Angle brackets</span></span>

<span data-ttu-id="b3195-379">Угловые скобки, как правило, используются для обозначения заполнителя.</span><span class="sxs-lookup"><span data-stu-id="b3195-379">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="b3195-380">Если вы используете угловые скобки в тексте (а не в коде), их необходимо закодировать.</span><span class="sxs-lookup"><span data-stu-id="b3195-380">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="b3195-381">Иначе Markdown распознает их как часть тега HTML.</span><span class="sxs-lookup"><span data-stu-id="b3195-381">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="b3195-382">Например, `<script name>` следует закодировать как `&lt;script name&gt;`.</span><span class="sxs-lookup"><span data-stu-id="b3195-382">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="b3195-383">Дополнительные материалы</span><span class="sxs-lookup"><span data-stu-id="b3195-383">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="b3195-384">Ресурсы Markdown</span><span class="sxs-lookup"><span data-stu-id="b3195-384">Markdown resources</span></span>

- <span data-ttu-id="b3195-385">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax) (Синтаксис Markdown)</span><span class="sxs-lookup"><span data-stu-id="b3195-385">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- <span data-ttu-id="b3195-386">[Markdown cheat-sheet](./media/documents/markdown-cheatsheet.pdf?raw=true) (Шпаргалка по Markdown)</span><span class="sxs-lookup"><span data-stu-id="b3195-386">[Docs Markdown cheat sheet](./media/documents/markdown-cheatsheet.pdf?raw=true)</span></span>
- [<span data-ttu-id="b3195-387">Базовые сведения о разметке Markdown на GitHub</span><span class="sxs-lookup"><span data-stu-id="b3195-387">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- <span data-ttu-id="b3195-388">[The Markdown Guide](https://www.markdownguide.org/) (Руководство по Markdown)</span><span class="sxs-lookup"><span data-stu-id="b3195-388">[The Markdown Guide](https://www.markdownguide.org/)</span></span>
