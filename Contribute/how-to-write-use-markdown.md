---
title: Использование языка разметки Markdown для написания документации
description: В этой статье приводятся базовые и справочные сведения о языке разметки Markdown, используемом для написания статей на сайте docs.microsoft.com.
ms.date: 03/26/2019
ms.openlocfilehash: 9fcd76e6103761465815784e4bf24e7042fb9f34
ms.sourcegitcommit: 5f7212a091e9fc4e9cd1320fdfa8efaff51384c7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "66373114"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="afa52-103">Использование языка разметки Markdown для написания документации</span><span class="sxs-lookup"><span data-stu-id="afa52-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="afa52-104">Статьи на сайте [docs.microsoft.com](http://docs.microsoft.com) написаны на [Markdown](https://daringfireball.net/projects/markdown/) — упрощенном языке разметки, который легко использовать и изучать.</span><span class="sxs-lookup"><span data-stu-id="afa52-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="afa52-105">Благодаря своей простоте он быстро становится отраслевым стандартом.</span><span class="sxs-lookup"><span data-stu-id="afa52-105">Because of this, it has quickly become an industry standard.</span></span> <span data-ttu-id="afa52-106">Для документов сайта используется [тип Markdig](#markdown-flavor) разметки Markdown.</span><span class="sxs-lookup"><span data-stu-id="afa52-106">The docs site uses the [Markdig flavor](#markdown-flavor) of Markdown.</span></span>


## <a name="markdown-basics"></a><span data-ttu-id="afa52-107">Базовые сведения о Markdown</span><span class="sxs-lookup"><span data-stu-id="afa52-107">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="afa52-108">Заголовки</span><span class="sxs-lookup"><span data-stu-id="afa52-108">Headings</span></span>

<span data-ttu-id="afa52-109">Чтобы создать заголовок, используйте знак (#), например:</span><span class="sxs-lookup"><span data-stu-id="afa52-109">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="afa52-110">В заголовках следует использовать стиль atx, то есть 1–6 символов решетки (#) в начале строки, чтобы указать на заголовок, соответствующий заголовкам HTML уровней с H1 по H6.</span><span class="sxs-lookup"><span data-stu-id="afa52-110">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="afa52-111">Сверху приводятся примеры заголовков с первого по четвертый уровень.</span><span class="sxs-lookup"><span data-stu-id="afa52-111">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="afa52-112">В статье **должен** быть только один заголовок первого уровня (H1), который будет отображаться как заголовок страницы.</span><span class="sxs-lookup"><span data-stu-id="afa52-112">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="afa52-113">Если заголовок заканчивается на символ `#`, добавьте в конце еще символ `#`, чтобы заголовок отображался правильно.</span><span class="sxs-lookup"><span data-stu-id="afa52-113">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="afa52-114">Например, `# Async Programming in F# #`.</span><span class="sxs-lookup"><span data-stu-id="afa52-114">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="afa52-115">Заголовки второго уровня создадут оглавление, которое будет отображаться в разделе "В этой статье" под заголовком статьи.</span><span class="sxs-lookup"><span data-stu-id="afa52-115">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="afa52-116">Полужирное начертание и курсив</span><span class="sxs-lookup"><span data-stu-id="afa52-116">Bold and italic text</span></span>

<span data-ttu-id="afa52-117">Чтобы задать для текста **полужирное начертание**, заключите его в двойные звездочки:</span><span class="sxs-lookup"><span data-stu-id="afa52-117">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="afa52-118">Чтобы задать для текста *курсивное начертание*, заключите его в одинарные звездочки:</span><span class="sxs-lookup"><span data-stu-id="afa52-118">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="afa52-119">Чтобы задать для текста ***полужирное и курсивное*** начертание, заключите его в тройные звездочки:</span><span class="sxs-lookup"><span data-stu-id="afa52-119">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="afa52-120">Блоки цитирования</span><span class="sxs-lookup"><span data-stu-id="afa52-120">Blockquotes</span></span>

<span data-ttu-id="afa52-121">Блоки цитирования создаются с помощью символа `>`:</span><span class="sxs-lookup"><span data-stu-id="afa52-121">Blockquotes are created using the `>` character:</span></span>

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="afa52-122">Предыдущий пример отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="afa52-122">The preceding example renders as follows:</span></span>

> <span data-ttu-id="afa52-123">Засуха продолжалась десять миллионов лет, и царству ужасных ящеров уже давно пришел конец.</span><span class="sxs-lookup"><span data-stu-id="afa52-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="afa52-124">Здесь, близ экватора, на материке, который позднее назовут Африкой, с новой яростью вспыхнула борьба за существование, и еще не ясно было, кто выйдет из нее победителем.</span><span class="sxs-lookup"><span data-stu-id="afa52-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="afa52-125">На этой бесплодной, иссушенной зноем земле благоденствовать или хотя бы просто выжить могли только маленькие, или ловкие, или свирепые.</span><span class="sxs-lookup"><span data-stu-id="afa52-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="afa52-126">Списки</span><span class="sxs-lookup"><span data-stu-id="afa52-126">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="afa52-127">Неупорядоченный список</span><span class="sxs-lookup"><span data-stu-id="afa52-127">Unordered list</span></span>

<span data-ttu-id="afa52-128">Неупорядоченный (маркированный) список можно отформатировать с помощью звездочек или тире.</span><span class="sxs-lookup"><span data-stu-id="afa52-128">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="afa52-129">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="afa52-129">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="afa52-130">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="afa52-130">will be rendered as:</span></span>

- <span data-ttu-id="afa52-131">List item 1</span><span class="sxs-lookup"><span data-stu-id="afa52-131">List item 1</span></span>
- <span data-ttu-id="afa52-132">List item 2</span><span class="sxs-lookup"><span data-stu-id="afa52-132">List item 2</span></span>
- <span data-ttu-id="afa52-133">List item 3</span><span class="sxs-lookup"><span data-stu-id="afa52-133">List item 3</span></span>

<span data-ttu-id="afa52-134">Чтобы вложить один список в другой, добавьте отступ для элементов дочернего списка.</span><span class="sxs-lookup"><span data-stu-id="afa52-134">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="afa52-135">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="afa52-135">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="afa52-136">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="afa52-136">will be rendered as:</span></span>

- <span data-ttu-id="afa52-137">List item 1</span><span class="sxs-lookup"><span data-stu-id="afa52-137">List item 1</span></span>
  - <span data-ttu-id="afa52-138">List item A</span><span class="sxs-lookup"><span data-stu-id="afa52-138">List item A</span></span>
  - <span data-ttu-id="afa52-139">List item B</span><span class="sxs-lookup"><span data-stu-id="afa52-139">List item B</span></span>
- <span data-ttu-id="afa52-140">List item 2</span><span class="sxs-lookup"><span data-stu-id="afa52-140">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="afa52-141">Упорядоченный список</span><span class="sxs-lookup"><span data-stu-id="afa52-141">Ordered list</span></span>

<span data-ttu-id="afa52-142">Упорядоченный (ступенчатый) список можно отформатировать с помощью соответствующих цифр.</span><span class="sxs-lookup"><span data-stu-id="afa52-142">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="afa52-143">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="afa52-143">For example, the following Markdown:</span></span>

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="afa52-144">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="afa52-144">will be rendered as:</span></span>

1. <span data-ttu-id="afa52-145">First instruction</span><span class="sxs-lookup"><span data-stu-id="afa52-145">First instruction</span></span>
2. <span data-ttu-id="afa52-146">Second instruction</span><span class="sxs-lookup"><span data-stu-id="afa52-146">Second instruction</span></span>
3. <span data-ttu-id="afa52-147">Third instruction</span><span class="sxs-lookup"><span data-stu-id="afa52-147">Third instruction</span></span>

<span data-ttu-id="afa52-148">Чтобы вложить один список в другой, добавьте отступ для элементов дочернего списка.</span><span class="sxs-lookup"><span data-stu-id="afa52-148">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="afa52-149">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="afa52-149">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="afa52-150">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="afa52-150">will be rendered as:</span></span>

1. <span data-ttu-id="afa52-151">First instruction</span><span class="sxs-lookup"><span data-stu-id="afa52-151">First instruction</span></span>
   1. <span data-ttu-id="afa52-152">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="afa52-152">Sub-instruction</span></span>
   2. <span data-ttu-id="afa52-153">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="afa52-153">Sub-instruction</span></span>
2. <span data-ttu-id="afa52-154">Second instruction</span><span class="sxs-lookup"><span data-stu-id="afa52-154">Second instruction</span></span>

<span data-ttu-id="afa52-155">Обратите внимание, что мы используем "1."</span><span class="sxs-lookup"><span data-stu-id="afa52-155">Note that we use '1.'</span></span> <span data-ttu-id="afa52-156">для всех записей.</span><span class="sxs-lookup"><span data-stu-id="afa52-156">for all entries.</span></span> <span data-ttu-id="afa52-157">Так проще увидеть различия, когда потом будут добавлены новые шаги или удалены существующие.</span><span class="sxs-lookup"><span data-stu-id="afa52-157">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="afa52-158">Tables</span><span class="sxs-lookup"><span data-stu-id="afa52-158">Tables</span></span>

<span data-ttu-id="afa52-159">Таблицы не входят в основную спецификацию Markdown, но их поддерживает GFM.</span><span class="sxs-lookup"><span data-stu-id="afa52-159">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="afa52-160">Создавать таблицы можно с помощью символов вертикальной черты (|) и дефиса (-).</span><span class="sxs-lookup"><span data-stu-id="afa52-160">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="afa52-161">Дефисы позволяют создавать для каждого столбца заголовок. Вертикальные черты разделяют столбцы.</span><span class="sxs-lookup"><span data-stu-id="afa52-161">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="afa52-162">Чтобы таблица правильно отображалась, включите перед ней пустую строку.</span><span class="sxs-lookup"><span data-stu-id="afa52-162">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="afa52-163">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="afa52-163">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="afa52-164">Она будет отображаться так:</span><span class="sxs-lookup"><span data-stu-id="afa52-164">Will be rendered as:</span></span>

| <span data-ttu-id="afa52-165">Fun</span><span class="sxs-lookup"><span data-stu-id="afa52-165">Fun</span></span>                  | <span data-ttu-id="afa52-166">with</span><span class="sxs-lookup"><span data-stu-id="afa52-166">With</span></span>                 | <span data-ttu-id="afa52-167">Tables</span><span class="sxs-lookup"><span data-stu-id="afa52-167">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="afa52-168">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="afa52-168">left-aligned column</span></span>  | <span data-ttu-id="afa52-169">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="afa52-169">right-aligned column</span></span> | <span data-ttu-id="afa52-170">centered column</span><span class="sxs-lookup"><span data-stu-id="afa52-170">centered column</span></span> |
| <span data-ttu-id="afa52-171">$100</span><span class="sxs-lookup"><span data-stu-id="afa52-171">$100</span></span>                 | <span data-ttu-id="afa52-172">$100</span><span class="sxs-lookup"><span data-stu-id="afa52-172">$100</span></span>                 | <span data-ttu-id="afa52-173">$100</span><span class="sxs-lookup"><span data-stu-id="afa52-173">$100</span></span>            |
| <span data-ttu-id="afa52-174">$10</span><span class="sxs-lookup"><span data-stu-id="afa52-174">$10</span></span>                  | <span data-ttu-id="afa52-175">$10</span><span class="sxs-lookup"><span data-stu-id="afa52-175">$10</span></span>                  | <span data-ttu-id="afa52-176">$10</span><span class="sxs-lookup"><span data-stu-id="afa52-176">$10</span></span>             |
| <span data-ttu-id="afa52-177">$1</span><span class="sxs-lookup"><span data-stu-id="afa52-177">$1</span></span>                   | <span data-ttu-id="afa52-178">$1</span><span class="sxs-lookup"><span data-stu-id="afa52-178">$1</span></span>                   | <span data-ttu-id="afa52-179">$1</span><span class="sxs-lookup"><span data-stu-id="afa52-179">$1</span></span>              |

<span data-ttu-id="afa52-180">Дополнительные сведения о создании таблиц:</span><span class="sxs-lookup"><span data-stu-id="afa52-180">For more information on creating tables, see:</span></span>

- <span data-ttu-id="afa52-181">Статья на сайте GitHub [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/) (Организация информации с помощью таблиц).</span><span class="sxs-lookup"><span data-stu-id="afa52-181">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="afa52-182">Веб-приложение [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="afa52-182">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="afa52-183">Статья Адама Притчарда (Adam Pritchard) [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables) (Шпаргалка по Markdown).</span><span class="sxs-lookup"><span data-stu-id="afa52-183">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="afa52-184">Статья Майкла Фортина (Michel Fortin) [Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) (Расширение Markdown Extra).</span><span class="sxs-lookup"><span data-stu-id="afa52-184">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="afa52-185">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/) (Преобразование таблиц HTML в Markdown).</span><span class="sxs-lookup"><span data-stu-id="afa52-185">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="afa52-186">Создание ссылок</span><span class="sxs-lookup"><span data-stu-id="afa52-186">Links</span></span>

<span data-ttu-id="afa52-187">Синтаксис Markdown для встроенной ссылки состоит из части `[link text]`, представляющей текст гиперссылки, и части `(file-name.md)` — URL-адреса или имени файла, на который дается ссылка:</span><span class="sxs-lookup"><span data-stu-id="afa52-187">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="afa52-188">Дополнительные сведения о ссылках:</span><span class="sxs-lookup"><span data-stu-id="afa52-188">For more information on linking, see:</span></span>

- <span data-ttu-id="afa52-189">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax#link) (Руководство по синтаксису Markdown), в котором предоставлена основная информация по поддержке ссылок Markdown.</span><span class="sxs-lookup"><span data-stu-id="afa52-189">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="afa52-190">Страница [Ссылки](how-to-write-links.md) в этом руководстве содержит сведения о дополнительном синтаксисе Markdig для ссылок.</span><span class="sxs-lookup"><span data-stu-id="afa52-190">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="afa52-191">Фрагменты кода</span><span class="sxs-lookup"><span data-stu-id="afa52-191">Code snippets</span></span>

<span data-ttu-id="afa52-192">Markdown поддерживает как встраивание фрагментов кода в предложение, так и их размещение между предложениями в виде отдельных огражденных блоков.</span><span class="sxs-lookup"><span data-stu-id="afa52-192">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="afa52-193">Дополнительная информация:</span><span class="sxs-lookup"><span data-stu-id="afa52-193">For details, see:</span></span>

- [<span data-ttu-id="afa52-194">Сведения о собственной поддержке блоков кода Markdown</span><span class="sxs-lookup"><span data-stu-id="afa52-194">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="afa52-195">Сведения о поддержке GFM для ограждения кода и выделения синтаксиса</span><span class="sxs-lookup"><span data-stu-id="afa52-195">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="afa52-196">Огражденные блоки кода — это простой способ выделить синтаксис для фрагментов кода.</span><span class="sxs-lookup"><span data-stu-id="afa52-196">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="afa52-197">Общий формат огражденных блоков кода:</span><span class="sxs-lookup"><span data-stu-id="afa52-197">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="afa52-198">Псевдоним после трех начальных символов обратной галочки \` определяет использование выделения.</span><span class="sxs-lookup"><span data-stu-id="afa52-198">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="afa52-199">Ниже представлен список часто используемых языков программирования для написания документации и приводятся соответствующие метки.</span><span class="sxs-lookup"><span data-stu-id="afa52-199">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="afa52-200">Все эти языки поддерживают понятные имена, а большинство из них — выделение языка в имени.</span><span class="sxs-lookup"><span data-stu-id="afa52-200">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="afa52-201">Имя</span><span class="sxs-lookup"><span data-stu-id="afa52-201">Name</span></span>|<span data-ttu-id="afa52-202">Метка Markdown</span><span class="sxs-lookup"><span data-stu-id="afa52-202">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="afa52-203">.NET Console</span><span class="sxs-lookup"><span data-stu-id="afa52-203">.NET Console</span></span>|<span data-ttu-id="afa52-204">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="afa52-204">dotnetcli</span></span>|
|<span data-ttu-id="afa52-205">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="afa52-205">ASP.NET (C#)</span></span>|<span data-ttu-id="afa52-206">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="afa52-206">aspx-csharp</span></span>|
|<span data-ttu-id="afa52-207">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="afa52-207">ASP.NET (VB)</span></span>|<span data-ttu-id="afa52-208">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="afa52-208">aspx-vb</span></span>|
|<span data-ttu-id="afa52-209">AzCopy</span><span class="sxs-lookup"><span data-stu-id="afa52-209">AzCopy</span></span>|<span data-ttu-id="afa52-210">azcopy</span><span class="sxs-lookup"><span data-stu-id="afa52-210">azcopy</span></span>|
|<span data-ttu-id="afa52-211">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="afa52-211">Azure CLI</span></span>|<span data-ttu-id="afa52-212">azurecli</span><span class="sxs-lookup"><span data-stu-id="afa52-212">azurecli</span></span>|
|<span data-ttu-id="afa52-213">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="afa52-213">Azure PowerShell</span></span>|<span data-ttu-id="afa52-214">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="afa52-214">azurepowershell</span></span>|
|<span data-ttu-id="afa52-215">Bash</span><span class="sxs-lookup"><span data-stu-id="afa52-215">Bash</span></span>|<span data-ttu-id="afa52-216">Bash</span><span class="sxs-lookup"><span data-stu-id="afa52-216">bash</span></span>|
|<span data-ttu-id="afa52-217">C++</span><span class="sxs-lookup"><span data-stu-id="afa52-217">C++</span></span>|<span data-ttu-id="afa52-218">cpp</span><span class="sxs-lookup"><span data-stu-id="afa52-218">cpp</span></span>|
|<span data-ttu-id="afa52-219">C++/CX</span><span class="sxs-lookup"><span data-stu-id="afa52-219">C++/CX</span></span>|<span data-ttu-id="afa52-220">cppcx</span><span class="sxs-lookup"><span data-stu-id="afa52-220">cppcx</span></span>|
|<span data-ttu-id="afa52-221">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="afa52-221">C++/WinRT</span></span>|<span data-ttu-id="afa52-222">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="afa52-222">cppwinrt</span></span>|
|<span data-ttu-id="afa52-223">C#</span><span class="sxs-lookup"><span data-stu-id="afa52-223">C#</span></span>|<span data-ttu-id="afa52-224">csharp</span><span class="sxs-lookup"><span data-stu-id="afa52-224">csharp</span></span>|
|<span data-ttu-id="afa52-225">C# в браузере</span><span class="sxs-lookup"><span data-stu-id="afa52-225">C# in browser</span></span>|<span data-ttu-id="afa52-226">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="afa52-226">csharp-interactive</span></span>|
|<span data-ttu-id="afa52-227">Консоль</span><span class="sxs-lookup"><span data-stu-id="afa52-227">Console</span></span>|<span data-ttu-id="afa52-228">консоль</span><span class="sxs-lookup"><span data-stu-id="afa52-228">console</span></span>|
|<span data-ttu-id="afa52-229">CSHTML</span><span class="sxs-lookup"><span data-stu-id="afa52-229">CSHTML</span></span>|<span data-ttu-id="afa52-230">cshtml</span><span class="sxs-lookup"><span data-stu-id="afa52-230">cshtml</span></span>|
|<span data-ttu-id="afa52-231">DAX</span><span class="sxs-lookup"><span data-stu-id="afa52-231">DAX</span></span>|<span data-ttu-id="afa52-232">dax</span><span class="sxs-lookup"><span data-stu-id="afa52-232">dax</span></span>|
|<span data-ttu-id="afa52-233">Docker</span><span class="sxs-lookup"><span data-stu-id="afa52-233">Docker</span></span>|<span data-ttu-id="afa52-234">dockerfile</span><span class="sxs-lookup"><span data-stu-id="afa52-234">dockerfile</span></span>|
|<span data-ttu-id="afa52-235">F#</span><span class="sxs-lookup"><span data-stu-id="afa52-235">F#</span></span>|<span data-ttu-id="afa52-236">fsharp</span><span class="sxs-lookup"><span data-stu-id="afa52-236">fsharp</span></span>|
|<span data-ttu-id="afa52-237">Go</span><span class="sxs-lookup"><span data-stu-id="afa52-237">Go</span></span>|<span data-ttu-id="afa52-238">go</span><span class="sxs-lookup"><span data-stu-id="afa52-238">go</span></span>|
|<span data-ttu-id="afa52-239">HTML</span><span class="sxs-lookup"><span data-stu-id="afa52-239">HTML</span></span>|<span data-ttu-id="afa52-240">html</span><span class="sxs-lookup"><span data-stu-id="afa52-240">html</span></span>|
|<span data-ttu-id="afa52-241">HTTP</span><span class="sxs-lookup"><span data-stu-id="afa52-241">HTTP</span></span>|<span data-ttu-id="afa52-242">http</span><span class="sxs-lookup"><span data-stu-id="afa52-242">http</span></span>|
|<span data-ttu-id="afa52-243">Java</span><span class="sxs-lookup"><span data-stu-id="afa52-243">Java</span></span>|<span data-ttu-id="afa52-244">java</span><span class="sxs-lookup"><span data-stu-id="afa52-244">java</span></span>|
|<span data-ttu-id="afa52-245">JavaScript</span><span class="sxs-lookup"><span data-stu-id="afa52-245">JavaScript</span></span>|<span data-ttu-id="afa52-246">javascript</span><span class="sxs-lookup"><span data-stu-id="afa52-246">javascript</span></span>|
|<span data-ttu-id="afa52-247">JSON</span><span class="sxs-lookup"><span data-stu-id="afa52-247">JSON</span></span>|<span data-ttu-id="afa52-248">json</span><span class="sxs-lookup"><span data-stu-id="afa52-248">json</span></span>|
|<span data-ttu-id="afa52-249">Язык запросов Kusto</span><span class="sxs-lookup"><span data-stu-id="afa52-249">Kusto Query Language</span></span>|<span data-ttu-id="afa52-250">kusto</span><span class="sxs-lookup"><span data-stu-id="afa52-250">kusto</span></span>|
|<span data-ttu-id="afa52-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="afa52-251">Markdown</span></span>|<span data-ttu-id="afa52-252">md</span><span class="sxs-lookup"><span data-stu-id="afa52-252">md</span></span>|
|<span data-ttu-id="afa52-253">Objective-C</span><span class="sxs-lookup"><span data-stu-id="afa52-253">Objective-C</span></span>|<span data-ttu-id="afa52-254">objc</span><span class="sxs-lookup"><span data-stu-id="afa52-254">objc</span></span>|
|<span data-ttu-id="afa52-255">OData</span><span class="sxs-lookup"><span data-stu-id="afa52-255">OData</span></span>|<span data-ttu-id="afa52-256">odata</span><span class="sxs-lookup"><span data-stu-id="afa52-256">odata</span></span>|
|<span data-ttu-id="afa52-257">PHP</span><span class="sxs-lookup"><span data-stu-id="afa52-257">PHP</span></span>|<span data-ttu-id="afa52-258">php</span><span class="sxs-lookup"><span data-stu-id="afa52-258">php</span></span>|
|<span data-ttu-id="afa52-259">PowerApps (десятичный разделитель — точка)</span><span class="sxs-lookup"><span data-stu-id="afa52-259">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="afa52-260">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="afa52-260">powerapps-dot</span></span>|
|<span data-ttu-id="afa52-261">PowerApps (десятичный разделитель — запятая)</span><span class="sxs-lookup"><span data-stu-id="afa52-261">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="afa52-262">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="afa52-262">powerapps-comma</span></span>|
|<span data-ttu-id="afa52-263">PowerShell</span><span class="sxs-lookup"><span data-stu-id="afa52-263">PowerShell</span></span>|<span data-ttu-id="afa52-264">powershell</span><span class="sxs-lookup"><span data-stu-id="afa52-264">powershell</span></span>|
|<span data-ttu-id="afa52-265">Python</span><span class="sxs-lookup"><span data-stu-id="afa52-265">Python</span></span>|<span data-ttu-id="afa52-266">python</span><span class="sxs-lookup"><span data-stu-id="afa52-266">python</span></span>|
|<span data-ttu-id="afa52-267">Q#</span><span class="sxs-lookup"><span data-stu-id="afa52-267">Q#</span></span>|<span data-ttu-id="afa52-268">qsharp</span><span class="sxs-lookup"><span data-stu-id="afa52-268">qsharp</span></span>|
|<span data-ttu-id="afa52-269">R</span><span class="sxs-lookup"><span data-stu-id="afa52-269">R</span></span>|<span data-ttu-id="afa52-270">r</span><span class="sxs-lookup"><span data-stu-id="afa52-270">r</span></span>|
|<span data-ttu-id="afa52-271">Ruby</span><span class="sxs-lookup"><span data-stu-id="afa52-271">Ruby</span></span>|<span data-ttu-id="afa52-272">ruby</span><span class="sxs-lookup"><span data-stu-id="afa52-272">ruby</span></span>|
|<span data-ttu-id="afa52-273">SQL</span><span class="sxs-lookup"><span data-stu-id="afa52-273">SQL</span></span>|<span data-ttu-id="afa52-274">sql</span><span class="sxs-lookup"><span data-stu-id="afa52-274">sql</span></span>|
|<span data-ttu-id="afa52-275">Swift</span><span class="sxs-lookup"><span data-stu-id="afa52-275">Swift</span></span>|<span data-ttu-id="afa52-276">swift</span><span class="sxs-lookup"><span data-stu-id="afa52-276">swift</span></span>|
|<span data-ttu-id="afa52-277">TypeScript</span><span class="sxs-lookup"><span data-stu-id="afa52-277">TypeScript</span></span>|<span data-ttu-id="afa52-278">typescript</span><span class="sxs-lookup"><span data-stu-id="afa52-278">typescript</span></span>|
|<span data-ttu-id="afa52-279">VB</span><span class="sxs-lookup"><span data-stu-id="afa52-279">VB</span></span>|<span data-ttu-id="afa52-280">vb</span><span class="sxs-lookup"><span data-stu-id="afa52-280">vb</span></span>|
|<span data-ttu-id="afa52-281">XAML</span><span class="sxs-lookup"><span data-stu-id="afa52-281">XAML</span></span>|<span data-ttu-id="afa52-282">xaml</span><span class="sxs-lookup"><span data-stu-id="afa52-282">xaml</span></span>|
|<span data-ttu-id="afa52-283">XML</span><span class="sxs-lookup"><span data-stu-id="afa52-283">XML</span></span>|<span data-ttu-id="afa52-284">xml</span><span class="sxs-lookup"><span data-stu-id="afa52-284">xml</span></span>|

<span data-ttu-id="afa52-285">Имя `csharp-interactive` указывает на язык C# и возможность запускать примеры в браузере.</span><span class="sxs-lookup"><span data-stu-id="afa52-285">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="afa52-286">Эти фрагменты кода компилируются и выполняются в контейнере Docker, а результаты выполнения программы отображаются в окне браузера пользователя.</span><span class="sxs-lookup"><span data-stu-id="afa52-286">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="afa52-287">Пример. C\#</span><span class="sxs-lookup"><span data-stu-id="afa52-287">Example: C\#</span></span>

<span data-ttu-id="afa52-288">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="afa52-288">__Markdown__</span></span>

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

<span data-ttu-id="afa52-289">__Отображение__</span><span class="sxs-lookup"><span data-stu-id="afa52-289">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="afa52-290">Пример. SQL</span><span class="sxs-lookup"><span data-stu-id="afa52-290">Example: SQL</span></span>

<span data-ttu-id="afa52-291">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="afa52-291">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="afa52-292">__Отображение__</span><span class="sxs-lookup"><span data-stu-id="afa52-292">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="afa52-293">Настраиваемые расширения OPS для Markdown</span><span class="sxs-lookup"><span data-stu-id="afa52-293">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="afa52-294">Службы Open Publishing Services (OPS) используют Markdig, синтаксический анализатор Markdown, обеспечивающий высокую совместимость с диалектом GitHub Flavored Markdown (GFM).</span><span class="sxs-lookup"><span data-stu-id="afa52-294">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="afa52-295">Markdig добавляет дополнительные функции за счет расширений Markdown.</span><span class="sxs-lookup"><span data-stu-id="afa52-295">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="afa52-296">Поэтому для справки мы включили в этот материал некоторые разделы из руководства по разработке OPS.</span><span class="sxs-lookup"><span data-stu-id="afa52-296">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="afa52-297">(Например, см. в содержании разделы "Markdig и расширения Markdown" и "Фрагменты кода".)</span><span class="sxs-lookup"><span data-stu-id="afa52-297">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="afa52-298">В статьях документации для общего форматирования, например для создания абзацев, ссылок, списков и заголовков, используется GFM.</span><span class="sxs-lookup"><span data-stu-id="afa52-298">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="afa52-299">Для расширенного форматирования в статьях можно использовать следующие функции Markdig:</span><span class="sxs-lookup"><span data-stu-id="afa52-299">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="afa52-300">Блоки заметок</span><span class="sxs-lookup"><span data-stu-id="afa52-300">Note blocks</span></span>
- <span data-ttu-id="afa52-301">Включаемые файлы</span><span class="sxs-lookup"><span data-stu-id="afa52-301">Include files</span></span>
- <span data-ttu-id="afa52-302">Селекторы</span><span class="sxs-lookup"><span data-stu-id="afa52-302">Selectors</span></span>
- <span data-ttu-id="afa52-303">внедренные видео;</span><span class="sxs-lookup"><span data-stu-id="afa52-303">Embedded videos</span></span>
- <span data-ttu-id="afa52-304">фрагменты или примеры кода.</span><span class="sxs-lookup"><span data-stu-id="afa52-304">Code snippets/samples</span></span>

<span data-ttu-id="afa52-305">Полный список см. в разделах "Markdig и расширения Markdown" и "Фрагменты кода".</span><span class="sxs-lookup"><span data-stu-id="afa52-305">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="afa52-306">Блоки заметок</span><span class="sxs-lookup"><span data-stu-id="afa52-306">Note blocks</span></span>

<span data-ttu-id="afa52-307">Есть четыре типа блоков заметок, которые позволяют привлечь внимание к определенному содержимому:</span><span class="sxs-lookup"><span data-stu-id="afa52-307">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="afa52-308">ПРИМЕЧАНИЕ;</span><span class="sxs-lookup"><span data-stu-id="afa52-308">NOTE</span></span>
- <span data-ttu-id="afa52-309">ПРЕДУПРЕЖДЕНИЕ;</span><span class="sxs-lookup"><span data-stu-id="afa52-309">WARNING</span></span>
- <span data-ttu-id="afa52-310">СОВЕТ;</span><span class="sxs-lookup"><span data-stu-id="afa52-310">TIP</span></span>
- <span data-ttu-id="afa52-311">ВАЖНО.</span><span class="sxs-lookup"><span data-stu-id="afa52-311">IMPORTANT</span></span>

<span data-ttu-id="afa52-312">В целом не следует часто использовать блоки заметок, так как они могут отвлекать пользователя от основного содержимого.</span><span class="sxs-lookup"><span data-stu-id="afa52-312">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="afa52-313">Хотя эти элементы также поддерживают блоки кода, изображения, списки и ссылки, лучше не перегружать их, делая простыми и понятными.</span><span class="sxs-lookup"><span data-stu-id="afa52-313">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="afa52-314">Примеры:</span><span class="sxs-lookup"><span data-stu-id="afa52-314">Examples:</span></span>

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

<span data-ttu-id="afa52-315">Это выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="afa52-315">These render as follows:</span></span>

> [!NOTE]
> <span data-ttu-id="afa52-316">Это ПРИМЕЧАНИЕ</span><span class="sxs-lookup"><span data-stu-id="afa52-316">This is a NOTE</span></span>

> [!WARNING]
> <span data-ttu-id="afa52-317">Это ПРЕДУПРЕЖДЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="afa52-317">This is a WARNING</span></span>

> [!TIP]
> <span data-ttu-id="afa52-318">Это СОВЕТ</span><span class="sxs-lookup"><span data-stu-id="afa52-318">This is a TIP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="afa52-319">Это ВАЖНО</span><span class="sxs-lookup"><span data-stu-id="afa52-319">This is IMPORTANT</span></span>

### <a name="include-files"></a><span data-ttu-id="afa52-320">Включаемые файлы</span><span class="sxs-lookup"><span data-stu-id="afa52-320">Include files</span></span>

<span data-ttu-id="afa52-321">Если вы хотите добавить в файлы статей многократно используемые изображения или текст, воспользуйтесь доступной в Markdig функцией включения ("include") файлов по ссылке.</span><span class="sxs-lookup"><span data-stu-id="afa52-321">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="afa52-322">Функция указывает OPS включить файл в файл статьи во время сборки, чтобы он стал частью опубликованной статьи.</span><span class="sxs-lookup"><span data-stu-id="afa52-322">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="afa52-323">Существует три типа включения файлов для многократного использования содержимого:</span><span class="sxs-lookup"><span data-stu-id="afa52-323">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="afa52-324">Встроенные: Используются для многократного использования фрагмента стандартного текста путем его встраивания в другое предложение.</span><span class="sxs-lookup"><span data-stu-id="afa52-324">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="afa52-325">Блочные: Используются для многократного использования всего файла Markdown в качестве блока путем его вложения в раздел или статью.</span><span class="sxs-lookup"><span data-stu-id="afa52-325">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="afa52-326">Изображения: Так на платформе Docs реализовано стандартное включение изображений.</span><span class="sxs-lookup"><span data-stu-id="afa52-326">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="afa52-327">Встроенные и блочные включаемые файлы — это простые файлы Markdown с расширением .md.</span><span class="sxs-lookup"><span data-stu-id="afa52-327">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="afa52-328">Они могут содержать любую допустимую разметку Markdown.</span><span class="sxs-lookup"><span data-stu-id="afa52-328">It can contain any valid Markdown.</span></span> <span data-ttu-id="afa52-329">Все включаемые файлы Markdown должны быть помещены в [общий подкаталог `/includes`](git-github-fundamentals.md#includes-subdirectory) в корневом каталоге репозитория.</span><span class="sxs-lookup"><span data-stu-id="afa52-329">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="afa52-330">Когда статья публикуется, включаемый файл легко интегрируется в нее.</span><span class="sxs-lookup"><span data-stu-id="afa52-330">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="afa52-331">Ниже приведены требования к включаемым файлам и соображения по работе с ними:</span><span class="sxs-lookup"><span data-stu-id="afa52-331">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="afa52-332">Используйте включаемые файлы, если вам нужно, чтобы один и тот же текст отображался в нескольких статьях.</span><span class="sxs-lookup"><span data-stu-id="afa52-332">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="afa52-333">Блочные включаемые файлы предназначены для значительных объемов текста: один или два абзаца, общая процедура или общий раздел.</span><span class="sxs-lookup"><span data-stu-id="afa52-333">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="afa52-334">Не используйте их для фрагментов текста меньше одного предложения.</span><span class="sxs-lookup"><span data-stu-id="afa52-334">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="afa52-335">Включаемые файлы не будут отображаться в представлении статьи на GitHub, так как они работают только с Markdig-расширениями.</span><span class="sxs-lookup"><span data-stu-id="afa52-335">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="afa52-336">Они отображаются только после публикации.</span><span class="sxs-lookup"><span data-stu-id="afa52-336">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="afa52-337">Весь текст во включаемом файле должен состоять из полноценных предложений или фраз, не зависящих от остального текста статьи, в которую добавляется ссылка на такой файл.</span><span class="sxs-lookup"><span data-stu-id="afa52-337">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="afa52-338">Если не следовать этой инструкции, в статье создаются непереводимые строки, которые нарушают процесс локализации.</span><span class="sxs-lookup"><span data-stu-id="afa52-338">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="afa52-339">Не внедряйте одни включаемые файлы в другие.</span><span class="sxs-lookup"><span data-stu-id="afa52-339">Don't embed include references within other include files.</span></span> <span data-ttu-id="afa52-340">Такая возможность не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="afa52-340">They are not supported.</span></span>
- <span data-ttu-id="afa52-341">Файлы мультимедиа должны быть помещены в отдельную папку мультимедиа в подкаталоге включаемых файлов. Например, `<repo>`/включаемые файлы/папка мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="afa52-341">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="afa52-342">В корне каталога мультимедиа не должны содержаться изображения.</span><span class="sxs-lookup"><span data-stu-id="afa52-342">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="afa52-343">Если во включаемом файле нет изображений, соответствующий каталог мультимедиа не требуется.</span><span class="sxs-lookup"><span data-stu-id="afa52-343">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="afa52-344">Как и в обычных статьях, не используйте общий файл мультимедиа для включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="afa52-344">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="afa52-345">Для каждого включаемого файла в статье должен быть создан отдельный файл с уникальным именем.</span><span class="sxs-lookup"><span data-stu-id="afa52-345">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="afa52-346">Файл мультимедиа должен храниться в папке мультимедиа, связанной с включаемым файлом.</span><span class="sxs-lookup"><span data-stu-id="afa52-346">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="afa52-347">Не используйте включаемый файл как единственное содержимое статьи.</span><span class="sxs-lookup"><span data-stu-id="afa52-347">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="afa52-348">Включаемые файлы предназначены для дополнения основных материалов статьи.</span><span class="sxs-lookup"><span data-stu-id="afa52-348">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="afa52-349">Пример.</span><span class="sxs-lookup"><span data-stu-id="afa52-349">Example:</span></span>

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="afa52-350">Селекторы</span><span class="sxs-lookup"><span data-stu-id="afa52-350">Selectors</span></span>

<span data-ttu-id="afa52-351">В технических статьях селекторы применяются для создания разных вариантов содержимого, чтобы проиллюстрировать различия в реализации, связанные с использованием нескольких технологий или платформ.</span><span class="sxs-lookup"><span data-stu-id="afa52-351">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="afa52-352">Это в особенности применимо к материалам о мобильных платформах для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="afa52-352">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="afa52-353">Сейчас в Markdig есть два типа селекторов: для единичного и множественного выбора.</span><span class="sxs-lookup"><span data-stu-id="afa52-353">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="afa52-354">В каждой статье с возможностью выбора используется одна и та же разметка Markdown для селектора. Поэтому рекомендуется поместить селектор для статьи во включаемый файл.</span><span class="sxs-lookup"><span data-stu-id="afa52-354">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="afa52-355">Затем нужно добавить ссылки на этот файл во все статьи, для которых используется селектор.</span><span class="sxs-lookup"><span data-stu-id="afa52-355">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="afa52-356">Ниже приведен пример селектора:</span><span class="sxs-lookup"><span data-stu-id="afa52-356">The following shows an example selector:</span></span>

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="afa52-357">Пример селекторов в действии можно посмотреть в [документации по Azure](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span><span class="sxs-lookup"><span data-stu-id="afa52-357">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="afa52-358">Включение фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="afa52-358">Code include references</span></span>

<span data-ttu-id="afa52-359">В Markdig есть расширение с расширенными функциями для включения в статью фрагментов кода.</span><span class="sxs-lookup"><span data-stu-id="afa52-359">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="afa52-360">Этот формат обеспечивает расширенный рендеринг на основе функций GFM, таких как выбор языка программирования и раскраска синтаксиса, а также другие полезные функции, например:</span><span class="sxs-lookup"><span data-stu-id="afa52-360">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="afa52-361">включение централизованных примеров или фрагментов кода из внешнего репозитория;</span><span class="sxs-lookup"><span data-stu-id="afa52-361">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="afa52-362">пользовательский интерфейс с вкладками для отображения нескольких версий примеров кода на разных языках.</span><span class="sxs-lookup"><span data-stu-id="afa52-362">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="afa52-363">Сбои и устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="afa52-363">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="afa52-364">Замещающий текст</span><span class="sxs-lookup"><span data-stu-id="afa52-364">Alt text</span></span>

<span data-ttu-id="afa52-365">Замещающий текст, который содержит символы подчеркивания, отображается некорректно.</span><span class="sxs-lookup"><span data-stu-id="afa52-365">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="afa52-366">Например, вместо</span><span class="sxs-lookup"><span data-stu-id="afa52-366">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="afa52-367">используйте следующий вариант, позволяющий избежать символов подчеркивания:</span><span class="sxs-lookup"><span data-stu-id="afa52-367">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="afa52-368">Апострофы и кавычки</span><span class="sxs-lookup"><span data-stu-id="afa52-368">Apostrophes and quotation marks</span></span>

<span data-ttu-id="afa52-369">Если вы копируете текст из Word в редактор Markdown, он может содержать книжные (изогнутые) апострофы или кавычки.</span><span class="sxs-lookup"><span data-stu-id="afa52-369">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="afa52-370">Их нужно заменить кодом или обычными апострофами или кавычками.</span><span class="sxs-lookup"><span data-stu-id="afa52-370">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="afa52-371">В противном случае после публикации файла может отобразиться нечитаемый текст, например: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="afa52-371">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="afa52-372">Ниже приведены кодировки для этих знаков пунктуации:</span><span class="sxs-lookup"><span data-stu-id="afa52-372">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="afa52-373">левая (открывающая) кавычка: `&#8220;`;</span><span class="sxs-lookup"><span data-stu-id="afa52-373">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="afa52-374">правая (закрывающая) кавычка: `&#8221;`;</span><span class="sxs-lookup"><span data-stu-id="afa52-374">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="afa52-375">правая закрывающая одинарная кавычка или апостроф: `&#8217;`;</span><span class="sxs-lookup"><span data-stu-id="afa52-375">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="afa52-376">левая открывающая одинарная кавычка (используется редко): `&#8216;`.</span><span class="sxs-lookup"><span data-stu-id="afa52-376">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="afa52-377">Угловые скобки</span><span class="sxs-lookup"><span data-stu-id="afa52-377">Angle brackets</span></span>

<span data-ttu-id="afa52-378">Угловые скобки, как правило, используются для обозначения заполнителя.</span><span class="sxs-lookup"><span data-stu-id="afa52-378">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="afa52-379">Если вы используете угловые скобки в тексте (а не в коде), их необходимо закодировать.</span><span class="sxs-lookup"><span data-stu-id="afa52-379">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="afa52-380">Иначе Markdown распознает их как часть тега HTML.</span><span class="sxs-lookup"><span data-stu-id="afa52-380">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="afa52-381">Например, `<script name>` следует закодировать как `&lt;script name&gt;`.</span><span class="sxs-lookup"><span data-stu-id="afa52-381">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="markdown-flavor"></a><span data-ttu-id="afa52-382">Тип разметки Markdown</span><span class="sxs-lookup"><span data-stu-id="afa52-382">Markdown flavor</span></span>

<span data-ttu-id="afa52-383">Серверная часть сайта docs.microsoft.com использует службы Open Publishing Services (OPS), поддерживающие разметку, совместимую с [CommonMark](https://commonmark.org/), проанализированную через подсистему синтаксического анализа [Markdig](https://github.com/lunet-io/markdig).</span><span class="sxs-lookup"><span data-stu-id="afa52-383">The docs.microsoft.com site backend uses Open Publishing Services (OPS) which supports [CommonMark](https://commonmark.org/) compliant markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="afa52-384">Такой тип разметки совместим с [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), так как большинство документов хранятся на GitHub, где их можно править.</span><span class="sxs-lookup"><span data-stu-id="afa52-384">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="afa52-385">Дополнительные функции добавляются с помощью расширений Markdown.</span><span class="sxs-lookup"><span data-stu-id="afa52-385">Additional functionality is added through Markdown extensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="afa52-386">Дополнительные материалы</span><span class="sxs-lookup"><span data-stu-id="afa52-386">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="afa52-387">Ресурсы Markdown</span><span class="sxs-lookup"><span data-stu-id="afa52-387">Markdown resources</span></span>

- <span data-ttu-id="afa52-388">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax) (Синтаксис Markdown)</span><span class="sxs-lookup"><span data-stu-id="afa52-388">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- <span data-ttu-id="afa52-389">[Markdown cheat-sheet](./media/documents/markdown-cheatsheet.pdf?raw=true) (Шпаргалка по Markdown)</span><span class="sxs-lookup"><span data-stu-id="afa52-389">[Docs Markdown cheat sheet](./media/documents/markdown-cheatsheet.pdf?raw=true)</span></span>
- [<span data-ttu-id="afa52-390">Базовые сведения о разметке Markdown на GitHub</span><span class="sxs-lookup"><span data-stu-id="afa52-390">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- <span data-ttu-id="afa52-391">[The Markdown Guide](https://www.markdownguide.org/) (Руководство по Markdown)</span><span class="sxs-lookup"><span data-stu-id="afa52-391">[The Markdown Guide](https://www.markdownguide.org/)</span></span>
