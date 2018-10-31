---
title: Использование языка разметки Markdown для написания документации
description: В этой статье приводятся базовые и справочные сведения о языке разметки Markdown, используемом для написания статей на сайте docs.microsoft.com.
ms.date: 07/13/2017
ms.openlocfilehash: 6bb8a1fa20957512addb07dda0e68abec4b0a83f
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805738"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="6fb6f-103">Использование языка разметки Markdown для написания документации</span><span class="sxs-lookup"><span data-stu-id="6fb6f-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="6fb6f-104">Статьи на сайте [docs.microsoft.com](http://docs.microsoft.com) написаны на [Markdown](https://daringfireball.net/projects/markdown/) — упрощенном языке разметки, который легко использовать и изучать.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="6fb6f-105">Благодаря своей простоте он быстро становится отраслевым стандартом.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="6fb6f-106">Так как документация хранится в репозитории GitHub, для нее можно использовать расширенный набор Markdown под названием [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/). Этот формат предусматривает дополнительные возможности для решения распространенных задач.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-106">Since Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="6fb6f-107">Кроме того, службы Open Publishing Services (OPS) используют Markdig, синтаксический анализатор Markdown.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="6fb6f-108">Он обеспечивает высокую совместимость с диалектом GFM, предоставляя дополнительные функции для работы с документацией.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-108">Markdig is highly compatible with GFM, adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="6fb6f-109">Markdig — это быстрый и мощный обработчик Markdown для .NET, обеспечивающий соответствие CommonMark и поддержку расширений.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="6fb6f-110">Улучшенная поддержка сообщества</span><span class="sxs-lookup"><span data-stu-id="6fb6f-110">Better community support</span></span>
* <span data-ttu-id="6fb6f-111">Улучшенная поддержка стандартов</span><span class="sxs-lookup"><span data-stu-id="6fb6f-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="6fb6f-112">Базовые сведения о Markdown</span><span class="sxs-lookup"><span data-stu-id="6fb6f-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="6fb6f-113">Заголовки</span><span class="sxs-lookup"><span data-stu-id="6fb6f-113">Headings</span></span>

<span data-ttu-id="6fb6f-114">Чтобы создать заголовок, используйте знак (#), например:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="6fb6f-115">Полужирное начертание и курсив</span><span class="sxs-lookup"><span data-stu-id="6fb6f-115">Bold and italic text</span></span>

<span data-ttu-id="6fb6f-116">Чтобы задать для текста **полужирное начертание**, заключите его в двойные звездочки:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-116">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="6fb6f-117">Чтобы задать для текста *курсивное начертание*, заключите его в одинарные звездочки:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-117">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="6fb6f-118">Чтобы задать для текста ***полужирное и курсивное*** начертание, заключите его в тройные звездочки:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-118">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="6fb6f-119">Списки</span><span class="sxs-lookup"><span data-stu-id="6fb6f-119">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="6fb6f-120">Неупорядоченный список</span><span class="sxs-lookup"><span data-stu-id="6fb6f-120">Unordered list</span></span>

<span data-ttu-id="6fb6f-121">Неупорядоченный (маркированный) список можно отформатировать с помощью звездочек или тире.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-121">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="6fb6f-122">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-122">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="6fb6f-123">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-123">will be rendered as:</span></span>

- <span data-ttu-id="6fb6f-124">List item 1</span><span class="sxs-lookup"><span data-stu-id="6fb6f-124">List item 1</span></span>
- <span data-ttu-id="6fb6f-125">List item 2</span><span class="sxs-lookup"><span data-stu-id="6fb6f-125">List item 2</span></span>
- <span data-ttu-id="6fb6f-126">List item 3</span><span class="sxs-lookup"><span data-stu-id="6fb6f-126">List item 3</span></span>

<span data-ttu-id="6fb6f-127">Чтобы вложить один список в другой, добавьте отступ для элементов дочернего списка.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-127">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="6fb6f-128">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-128">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="6fb6f-129">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-129">will be rendered as:</span></span>

- <span data-ttu-id="6fb6f-130">List item 1</span><span class="sxs-lookup"><span data-stu-id="6fb6f-130">List item 1</span></span>
  - <span data-ttu-id="6fb6f-131">List item A</span><span class="sxs-lookup"><span data-stu-id="6fb6f-131">List item A</span></span>
  - <span data-ttu-id="6fb6f-132">List item B</span><span class="sxs-lookup"><span data-stu-id="6fb6f-132">List item B</span></span>
- <span data-ttu-id="6fb6f-133">List item 2</span><span class="sxs-lookup"><span data-stu-id="6fb6f-133">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="6fb6f-134">Упорядоченный список</span><span class="sxs-lookup"><span data-stu-id="6fb6f-134">Ordered list</span></span>

<span data-ttu-id="6fb6f-135">Упорядоченный (ступенчатый) список можно отформатировать с помощью соответствующих цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-135">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="6fb6f-136">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-136">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="6fb6f-137">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-137">will be rendered as:</span></span>

1. <span data-ttu-id="6fb6f-138">First instruction</span><span class="sxs-lookup"><span data-stu-id="6fb6f-138">First instruction</span></span>
2. <span data-ttu-id="6fb6f-139">Second instruction</span><span class="sxs-lookup"><span data-stu-id="6fb6f-139">Second instruction</span></span>
3. <span data-ttu-id="6fb6f-140">Third instruction</span><span class="sxs-lookup"><span data-stu-id="6fb6f-140">Third instruction</span></span>

<span data-ttu-id="6fb6f-141">Чтобы вложить один список в другой, добавьте отступ для элементов дочернего списка.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-141">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="6fb6f-142">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-142">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="6fb6f-143">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-143">will be rendered as:</span></span>

1. <span data-ttu-id="6fb6f-144">First instruction</span><span class="sxs-lookup"><span data-stu-id="6fb6f-144">First instruction</span></span>
   1. <span data-ttu-id="6fb6f-145">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="6fb6f-145">Sub-instruction</span></span>
   2. <span data-ttu-id="6fb6f-146">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="6fb6f-146">Sub-instruction</span></span>
2. <span data-ttu-id="6fb6f-147">Second instruction</span><span class="sxs-lookup"><span data-stu-id="6fb6f-147">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="6fb6f-148">Tables</span><span class="sxs-lookup"><span data-stu-id="6fb6f-148">Tables</span></span>

<span data-ttu-id="6fb6f-149">Таблицы не входят в основную спецификацию Markdown, но их поддерживает GFM.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-149">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="6fb6f-150">Создавать таблицы можно с помощью символов вертикальной черты (|) и дефиса (-).</span><span class="sxs-lookup"><span data-stu-id="6fb6f-150">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="6fb6f-151">Дефисы позволяют создавать для каждого столбца заголовок. Вертикальные черты разделяют столбцы.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-151">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="6fb6f-152">Чтобы таблица правильно отображалась, включите перед ней пустую строку.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-152">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="6fb6f-153">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-153">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="6fb6f-154">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-154">will be rendered as:</span></span>

| <span data-ttu-id="6fb6f-155">Fun</span><span class="sxs-lookup"><span data-stu-id="6fb6f-155">Fun</span></span>                  | <span data-ttu-id="6fb6f-156">with</span><span class="sxs-lookup"><span data-stu-id="6fb6f-156">With</span></span>                 | <span data-ttu-id="6fb6f-157">Tables</span><span class="sxs-lookup"><span data-stu-id="6fb6f-157">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="6fb6f-158">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="6fb6f-158">left-aligned column</span></span>  | <span data-ttu-id="6fb6f-159">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="6fb6f-159">right-aligned column</span></span> | <span data-ttu-id="6fb6f-160">centered column</span><span class="sxs-lookup"><span data-stu-id="6fb6f-160">centered column</span></span> |
| <span data-ttu-id="6fb6f-161">$100</span><span class="sxs-lookup"><span data-stu-id="6fb6f-161">$100</span></span>                 | <span data-ttu-id="6fb6f-162">$100</span><span class="sxs-lookup"><span data-stu-id="6fb6f-162">$100</span></span>                 | <span data-ttu-id="6fb6f-163">$100</span><span class="sxs-lookup"><span data-stu-id="6fb6f-163">$100</span></span>            |
| <span data-ttu-id="6fb6f-164">$10</span><span class="sxs-lookup"><span data-stu-id="6fb6f-164">$10</span></span>                  | <span data-ttu-id="6fb6f-165">$10</span><span class="sxs-lookup"><span data-stu-id="6fb6f-165">$10</span></span>                  | <span data-ttu-id="6fb6f-166">$10</span><span class="sxs-lookup"><span data-stu-id="6fb6f-166">$10</span></span>             |
| <span data-ttu-id="6fb6f-167">$1</span><span class="sxs-lookup"><span data-stu-id="6fb6f-167">$1</span></span>                   | <span data-ttu-id="6fb6f-168">$1</span><span class="sxs-lookup"><span data-stu-id="6fb6f-168">$1</span></span>                   | <span data-ttu-id="6fb6f-169">$1</span><span class="sxs-lookup"><span data-stu-id="6fb6f-169">$1</span></span>              |

<span data-ttu-id="6fb6f-170">Дополнительные сведения о создании таблиц:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-170">For more information on creating tables, see:</span></span>

- <span data-ttu-id="6fb6f-171">[Функция обтекания таблиц](#table-wrapping) в Markdig, которая поможет при форматировании широких таблиц.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-171">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="6fb6f-172">Статья на сайте GitHub [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/) (Организация информации с помощью таблиц).</span><span class="sxs-lookup"><span data-stu-id="6fb6f-172">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="6fb6f-173">Веб-приложение [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="6fb6f-173">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="6fb6f-174">Статья Адама Притчарда (Adam Pritchard) [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables) (Шпаргалка по Markdown).</span><span class="sxs-lookup"><span data-stu-id="6fb6f-174">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="6fb6f-175">Статья Майкла Фортина (Michel Fortin) [Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) (Расширение Markdown Extra).</span><span class="sxs-lookup"><span data-stu-id="6fb6f-175">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="6fb6f-176">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/) (Преобразование таблиц HTML в Markdown).</span><span class="sxs-lookup"><span data-stu-id="6fb6f-176">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="6fb6f-177">Создание ссылок</span><span class="sxs-lookup"><span data-stu-id="6fb6f-177">Links</span></span>

<span data-ttu-id="6fb6f-178">Синтаксис Markdown для встроенной ссылки состоит из части `[link text]`, представляющей текст гиперссылки, и части `(file-name.md)` — URL-адреса или имени файла, на который дается ссылка:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-178">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="6fb6f-179">Дополнительные сведения о ссылках:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-179">For more information on linking, see:</span></span>

- <span data-ttu-id="6fb6f-180">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax#link) (Руководство по синтаксису Markdown), в котором предоставлена основная информация по поддержке ссылок Markdown.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-180">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="6fb6f-181">Страница [Ссылки](how-to-write-links.md) в этом руководстве содержит сведения о дополнительном синтаксисе Markdig для ссылок.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-181">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="6fb6f-182">Фрагменты кода</span><span class="sxs-lookup"><span data-stu-id="6fb6f-182">Code snippets</span></span>

<span data-ttu-id="6fb6f-183">Markdown поддерживает как встраивание фрагментов кода в предложение, так и их размещение между предложениями в виде отдельных огражденных блоков.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-183">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="6fb6f-184">Дополнительная информация:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-184">For details, see:</span></span>

- [<span data-ttu-id="6fb6f-185">Сведения о собственной поддержке блоков кода Markdown</span><span class="sxs-lookup"><span data-stu-id="6fb6f-185">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="6fb6f-186">Сведения о поддержке GFM для ограждения кода и выделения синтаксиса</span><span class="sxs-lookup"><span data-stu-id="6fb6f-186">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="6fb6f-187">Огражденные блоки кода — это простой способ выделить синтаксис для фрагментов кода.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-187">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="6fb6f-188">Общий формат огражденных блоков кода:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-188">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="6fb6f-189">Псевдоним после трех начальных символов обратной галочки \` определяет использование выделения.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-189">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="6fb6f-190">Ниже представлен список часто используемых языков программирования для написания документации и приводятся соответствующие метки.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-190">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="6fb6f-191">Все эти языки поддерживают понятные имена, а большинство из них — выделение языка в имени.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-191">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="6fb6f-192">Имя</span><span class="sxs-lookup"><span data-stu-id="6fb6f-192">Name</span></span>|<span data-ttu-id="6fb6f-193">Метка Markdown</span><span class="sxs-lookup"><span data-stu-id="6fb6f-193">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="6fb6f-194">.NET Console</span><span class="sxs-lookup"><span data-stu-id="6fb6f-194">.NET Console</span></span>|<span data-ttu-id="6fb6f-195">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="6fb6f-195">dotnetcli</span></span>|
|<span data-ttu-id="6fb6f-196">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="6fb6f-196">ASP.NET (C#)</span></span>|<span data-ttu-id="6fb6f-197">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="6fb6f-197">aspx-csharp</span></span>|
|<span data-ttu-id="6fb6f-198">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="6fb6f-198">ASP.NET (VB)</span></span>|<span data-ttu-id="6fb6f-199">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="6fb6f-199">aspx-vb</span></span>|
|<span data-ttu-id="6fb6f-200">AzCopy</span><span class="sxs-lookup"><span data-stu-id="6fb6f-200">AzCopy</span></span>|<span data-ttu-id="6fb6f-201">azcopy</span><span class="sxs-lookup"><span data-stu-id="6fb6f-201">azcopy</span></span>|
|<span data-ttu-id="6fb6f-202">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="6fb6f-202">Azure CLI</span></span>|<span data-ttu-id="6fb6f-203">azurecli</span><span class="sxs-lookup"><span data-stu-id="6fb6f-203">azurecli</span></span>|
|<span data-ttu-id="6fb6f-204">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6fb6f-204">Azure PowerShell</span></span>|<span data-ttu-id="6fb6f-205">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="6fb6f-205">azurepowershell</span></span>|
|<span data-ttu-id="6fb6f-206">C++</span><span class="sxs-lookup"><span data-stu-id="6fb6f-206">C++</span></span>|<span data-ttu-id="6fb6f-207">cpp</span><span class="sxs-lookup"><span data-stu-id="6fb6f-207">cpp</span></span>|
|<span data-ttu-id="6fb6f-208">C++/CX</span><span class="sxs-lookup"><span data-stu-id="6fb6f-208">C++/CX</span></span>|<span data-ttu-id="6fb6f-209">cppcx</span><span class="sxs-lookup"><span data-stu-id="6fb6f-209">cppcx</span></span>|
|<span data-ttu-id="6fb6f-210">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="6fb6f-210">C++/WinRT</span></span>|<span data-ttu-id="6fb6f-211">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="6fb6f-211">cppwinrt</span></span>|
|<span data-ttu-id="6fb6f-212">C#</span><span class="sxs-lookup"><span data-stu-id="6fb6f-212">C#</span></span>|<span data-ttu-id="6fb6f-213">csharp</span><span class="sxs-lookup"><span data-stu-id="6fb6f-213">csharp</span></span>|
|<span data-ttu-id="6fb6f-214">CSHTML</span><span class="sxs-lookup"><span data-stu-id="6fb6f-214">CSHTML</span></span>|<span data-ttu-id="6fb6f-215">cshtml</span><span class="sxs-lookup"><span data-stu-id="6fb6f-215">cshtml</span></span>|
|<span data-ttu-id="6fb6f-216">DAX</span><span class="sxs-lookup"><span data-stu-id="6fb6f-216">DAX</span></span>|<span data-ttu-id="6fb6f-217">dax</span><span class="sxs-lookup"><span data-stu-id="6fb6f-217">dax</span></span>|
|<span data-ttu-id="6fb6f-218">F#</span><span class="sxs-lookup"><span data-stu-id="6fb6f-218">F#</span></span>|<span data-ttu-id="6fb6f-219">fsharp</span><span class="sxs-lookup"><span data-stu-id="6fb6f-219">fsharp</span></span>|
|<span data-ttu-id="6fb6f-220">Go</span><span class="sxs-lookup"><span data-stu-id="6fb6f-220">Go</span></span>|<span data-ttu-id="6fb6f-221">go</span><span class="sxs-lookup"><span data-stu-id="6fb6f-221">go</span></span>|
|<span data-ttu-id="6fb6f-222">HTML</span><span class="sxs-lookup"><span data-stu-id="6fb6f-222">HTML</span></span>|<span data-ttu-id="6fb6f-223">html</span><span class="sxs-lookup"><span data-stu-id="6fb6f-223">html</span></span>|
|<span data-ttu-id="6fb6f-224">HTTP</span><span class="sxs-lookup"><span data-stu-id="6fb6f-224">HTTP</span></span>|<span data-ttu-id="6fb6f-225">http</span><span class="sxs-lookup"><span data-stu-id="6fb6f-225">http</span></span>|
|<span data-ttu-id="6fb6f-226">Java</span><span class="sxs-lookup"><span data-stu-id="6fb6f-226">Java</span></span>|<span data-ttu-id="6fb6f-227">java</span><span class="sxs-lookup"><span data-stu-id="6fb6f-227">java</span></span>|
|<span data-ttu-id="6fb6f-228">JavaScript</span><span class="sxs-lookup"><span data-stu-id="6fb6f-228">JavaScript</span></span>|<span data-ttu-id="6fb6f-229">javascript</span><span class="sxs-lookup"><span data-stu-id="6fb6f-229">javascript</span></span>|
|<span data-ttu-id="6fb6f-230">JSON</span><span class="sxs-lookup"><span data-stu-id="6fb6f-230">JSON</span></span>|<span data-ttu-id="6fb6f-231">json</span><span class="sxs-lookup"><span data-stu-id="6fb6f-231">json</span></span>|
|<span data-ttu-id="6fb6f-232">Markdown</span><span class="sxs-lookup"><span data-stu-id="6fb6f-232">Markdown</span></span>|<span data-ttu-id="6fb6f-233">md</span><span class="sxs-lookup"><span data-stu-id="6fb6f-233">md</span></span>|
|<span data-ttu-id="6fb6f-234">NodeJS</span><span class="sxs-lookup"><span data-stu-id="6fb6f-234">NodeJS</span></span>|<span data-ttu-id="6fb6f-235">nodejs</span><span class="sxs-lookup"><span data-stu-id="6fb6f-235">nodejs</span></span>|
|<span data-ttu-id="6fb6f-236">Objective-C</span><span class="sxs-lookup"><span data-stu-id="6fb6f-236">Objective-C</span></span>|<span data-ttu-id="6fb6f-237">objc</span><span class="sxs-lookup"><span data-stu-id="6fb6f-237">objc</span></span>|
|<span data-ttu-id="6fb6f-238">OData</span><span class="sxs-lookup"><span data-stu-id="6fb6f-238">OData</span></span>|<span data-ttu-id="6fb6f-239">odata</span><span class="sxs-lookup"><span data-stu-id="6fb6f-239">odata</span></span>|
|<span data-ttu-id="6fb6f-240">PHP</span><span class="sxs-lookup"><span data-stu-id="6fb6f-240">PHP</span></span>|<span data-ttu-id="6fb6f-241">php</span><span class="sxs-lookup"><span data-stu-id="6fb6f-241">php</span></span>|
|<span data-ttu-id="6fb6f-242">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="6fb6f-242">Power Apps Formula</span></span>|<span data-ttu-id="6fb6f-243">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="6fb6f-243">powerappsfl</span></span>|
|<span data-ttu-id="6fb6f-244">PowerShell</span><span class="sxs-lookup"><span data-stu-id="6fb6f-244">PowerShell</span></span>|<span data-ttu-id="6fb6f-245">powershell</span><span class="sxs-lookup"><span data-stu-id="6fb6f-245">powershell</span></span>|
|<span data-ttu-id="6fb6f-246">Python</span><span class="sxs-lookup"><span data-stu-id="6fb6f-246">Python</span></span>|<span data-ttu-id="6fb6f-247">python</span><span class="sxs-lookup"><span data-stu-id="6fb6f-247">python</span></span>|
|<span data-ttu-id="6fb6f-248">Q#</span><span class="sxs-lookup"><span data-stu-id="6fb6f-248">Q#</span></span>|<span data-ttu-id="6fb6f-249">qsharp</span><span class="sxs-lookup"><span data-stu-id="6fb6f-249">qsharp</span></span>|
|<span data-ttu-id="6fb6f-250">R</span><span class="sxs-lookup"><span data-stu-id="6fb6f-250">R</span></span>|<span data-ttu-id="6fb6f-251">r</span><span class="sxs-lookup"><span data-stu-id="6fb6f-251">r</span></span>|
|<span data-ttu-id="6fb6f-252">Ruby</span><span class="sxs-lookup"><span data-stu-id="6fb6f-252">Ruby</span></span>|<span data-ttu-id="6fb6f-253">ruby</span><span class="sxs-lookup"><span data-stu-id="6fb6f-253">ruby</span></span>|
|<span data-ttu-id="6fb6f-254">SQL</span><span class="sxs-lookup"><span data-stu-id="6fb6f-254">SQL</span></span>|<span data-ttu-id="6fb6f-255">sql</span><span class="sxs-lookup"><span data-stu-id="6fb6f-255">sql</span></span>|
|<span data-ttu-id="6fb6f-256">Swift</span><span class="sxs-lookup"><span data-stu-id="6fb6f-256">Swift</span></span>|<span data-ttu-id="6fb6f-257">swift</span><span class="sxs-lookup"><span data-stu-id="6fb6f-257">swift</span></span>|
|<span data-ttu-id="6fb6f-258">TypeScript</span><span class="sxs-lookup"><span data-stu-id="6fb6f-258">TypeScript</span></span>|<span data-ttu-id="6fb6f-259">typescript</span><span class="sxs-lookup"><span data-stu-id="6fb6f-259">typescript</span></span>|
|<span data-ttu-id="6fb6f-260">VB</span><span class="sxs-lookup"><span data-stu-id="6fb6f-260">VB</span></span>|<span data-ttu-id="6fb6f-261">vb</span><span class="sxs-lookup"><span data-stu-id="6fb6f-261">vb</span></span>|
|<span data-ttu-id="6fb6f-262">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="6fb6f-262">VSTS CLI</span></span>|<span data-ttu-id="6fb6f-263">vstscli</span><span class="sxs-lookup"><span data-stu-id="6fb6f-263">vstscli</span></span>|
|<span data-ttu-id="6fb6f-264">XAML</span><span class="sxs-lookup"><span data-stu-id="6fb6f-264">XAML</span></span>|<span data-ttu-id="6fb6f-265">xaml</span><span class="sxs-lookup"><span data-stu-id="6fb6f-265">xaml</span></span>|
|<span data-ttu-id="6fb6f-266">XML</span><span class="sxs-lookup"><span data-stu-id="6fb6f-266">XML</span></span>|<span data-ttu-id="6fb6f-267">xml</span><span class="sxs-lookup"><span data-stu-id="6fb6f-267">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="6fb6f-268">Пример: C\#</span><span class="sxs-lookup"><span data-stu-id="6fb6f-268">Example: C\#</span></span>

<span data-ttu-id="6fb6f-269">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="6fb6f-269">__Markdown__</span></span>

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

<span data-ttu-id="6fb6f-270">__Отображение__</span><span class="sxs-lookup"><span data-stu-id="6fb6f-270">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="6fb6f-271">Пример: SQL</span><span class="sxs-lookup"><span data-stu-id="6fb6f-271">Example: SQL</span></span>

<span data-ttu-id="6fb6f-272">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="6fb6f-272">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="6fb6f-273">__Отображение__</span><span class="sxs-lookup"><span data-stu-id="6fb6f-273">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="6fb6f-274">Настраиваемые расширения OPS для Markdown</span><span class="sxs-lookup"><span data-stu-id="6fb6f-274">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="6fb6f-275">Службы Open Publishing Services (OPS) используют Markdig, синтаксический анализатор Markdown, обеспечивающий высокую совместимость с диалектом GitHub Flavored Markdown (GFM).</span><span class="sxs-lookup"><span data-stu-id="6fb6f-275">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="6fb6f-276">Markdig добавляет дополнительные функции за счет расширений Markdown.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-276">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="6fb6f-277">Поэтому для справки мы включили в этот материал некоторые разделы из руководства по разработке OPS.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-277">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="6fb6f-278">(Например, см. в содержании разделы "Markdig и расширения Markdown" и "Фрагменты кода".)</span><span class="sxs-lookup"><span data-stu-id="6fb6f-278">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="6fb6f-279">В статьях документации для общего форматирования, например для создания абзацев, ссылок, списков и заголовков, используется GFM.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-279">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="6fb6f-280">Для расширенного форматирования в статьях можно использовать следующие функции Markdig:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-280">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="6fb6f-281">Блоки заметок</span><span class="sxs-lookup"><span data-stu-id="6fb6f-281">Note blocks</span></span>
- <span data-ttu-id="6fb6f-282">включаемые файлы;</span><span class="sxs-lookup"><span data-stu-id="6fb6f-282">Includes</span></span>
- <span data-ttu-id="6fb6f-283">селекторы;</span><span class="sxs-lookup"><span data-stu-id="6fb6f-283">Selectors</span></span>
- <span data-ttu-id="6fb6f-284">внедренные видео;</span><span class="sxs-lookup"><span data-stu-id="6fb6f-284">Embedded videos</span></span>
- <span data-ttu-id="6fb6f-285">фрагменты или примеры кода.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-285">Code snippets/samples</span></span>

<span data-ttu-id="6fb6f-286">Полный список см. в разделах "Markdig и расширения Markdown" и "Фрагменты кода".</span><span class="sxs-lookup"><span data-stu-id="6fb6f-286">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="6fb6f-287">Блоки заметок</span><span class="sxs-lookup"><span data-stu-id="6fb6f-287">Note blocks</span></span>

<span data-ttu-id="6fb6f-288">Есть четыре типа блоков заметок, которые позволяют привлечь внимание к определенному содержимому:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-288">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="6fb6f-289">ПРИМЕЧАНИЕ;</span><span class="sxs-lookup"><span data-stu-id="6fb6f-289">NOTE</span></span>
- <span data-ttu-id="6fb6f-290">ПРЕДУПРЕЖДЕНИЕ;</span><span class="sxs-lookup"><span data-stu-id="6fb6f-290">WARNING</span></span>
- <span data-ttu-id="6fb6f-291">СОВЕТ;</span><span class="sxs-lookup"><span data-stu-id="6fb6f-291">TIP</span></span>
- <span data-ttu-id="6fb6f-292">ВАЖНО.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-292">IMPORTANT</span></span>

<span data-ttu-id="6fb6f-293">В целом не следует часто использовать блоки заметок, так как они могут отвлекать пользователя от основного содержимого.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-293">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="6fb6f-294">Хотя эти элементы также поддерживают блоки кода, изображения, списки и ссылки, лучше не перегружать их, делая простыми и понятными.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-294">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="6fb6f-295">Включаемые файлы</span><span class="sxs-lookup"><span data-stu-id="6fb6f-295">Includes</span></span>

<span data-ttu-id="6fb6f-296">Если вы хотите добавить в файлы статей многократно используемые изображения или текст, воспользуйтесь доступной в Markdig функцией включения ("include") файлов по ссылке.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-296">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="6fb6f-297">Функция указывает OPS включить файл в файл статьи во время сборки, чтобы он стал частью опубликованной статьи.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-297">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="6fb6f-298">Существует три типа включаемых файлов для многократного использования содержимого:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-298">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="6fb6f-299">Встроенные — для многократного использования фрагмента стандартного текста путем его встраивания в другое предложение.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-299">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="6fb6f-300">Блочные — для многократного использования всего файла Markdown в качестве блока путем его вложения в раздел или статью.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-300">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="6fb6f-301">Изображения — позволяют включать стандартное изображение в документацию.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-301">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="6fb6f-302">Встроенные и блочные включаемые файлы — это простые файлы Markdown с расширением .md.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-302">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="6fb6f-303">Они могут содержать любую допустимую разметку Markdown.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-303">It can contain any valid Markdown.</span></span> <span data-ttu-id="6fb6f-304">Все включаемые файлы Markdown должны быть помещены в [общий подкаталог `/includes`](git-github-fundamentals.md#includes-subdirectory) в корневом каталоге репозитория.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-304">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="6fb6f-305">Когда статья публикуется, включаемый файл легко интегрируется в нее.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-305">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="6fb6f-306">Далее приведены требования по работе с включаемыми файлами.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-306">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="6fb6f-307">Используйте включаемые файлы, если вам нужно, чтобы один и тот же текст отображался в нескольких статьях.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-307">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="6fb6f-308">Блочные включаемые файлы предназначены для значительных объемов текста: один или два абзаца, общая процедура или общий раздел.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-308">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="6fb6f-309">Не используйте их для фрагментов текста меньше одного предложения.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-309">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="6fb6f-310">Включаемые файлы не будут отображаться в представлении статьи на GitHub, так как они работают только с Markdig-расширениями.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-310">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="6fb6f-311">Они отображаются только после публикации.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-311">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="6fb6f-312">Весь текст во включаемом файле должен состоять из полноценных предложений или фраз, не зависящих от остального текста статьи, в которую добавляется ссылка на такой файл.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-312">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="6fb6f-313">Если не следовать этой инструкции, в статье создаются непереводимые строки, которые нарушают процесс локализации.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-313">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="6fb6f-314">Не внедряйте одни включаемые файлы в другие.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-314">Don't embed includes within other includes.</span></span> <span data-ttu-id="6fb6f-315">Такая возможность не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-315">They are not supported.</span></span>
- <span data-ttu-id="6fb6f-316">Файлы мультимедиа должны быть помещены в отдельную папку мультимедиа в подкаталоге включаемых файлов. Например, `<repo>`/включаемые файлы/папка мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-316">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="6fb6f-317">В корне каталога мультимедиа не должны содержаться изображения.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-317">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="6fb6f-318">Если во включаемом файле нет изображений, соответствующий каталог мультимедиа не требуется.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-318">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="6fb6f-319">Как и в обычных статьях, не используйте общий файл мультимедиа для включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-319">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="6fb6f-320">Для каждого включаемого файла в статье должен быть создан отдельный файл мультимедиа с уникальным именем.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-320">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="6fb6f-321">Файл мультимедиа должен храниться в папке мультимедиа, связанной с включаемым файлом.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-321">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="6fb6f-322">Не используйте включаемый файл как единственное содержимое статьи.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-322">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="6fb6f-323">Включаемые файлы предназначены для дополнения основных материалов статьи.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-323">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="6fb6f-324">Селекторы</span><span class="sxs-lookup"><span data-stu-id="6fb6f-324">Selectors</span></span>

<span data-ttu-id="6fb6f-325">В технических статьях селекторы применяются для создания разных вариантов содержимого, чтобы проиллюстрировать различия в реализации, связанные с использованием нескольких технологий или платформ.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-325">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="6fb6f-326">Это в особенности применимо к материалам о мобильных платформах для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-326">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="6fb6f-327">Сейчас в Markdig есть два типа селекторов: для единичного и множественного выбора.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-327">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="6fb6f-328">В каждой статье с возможностью выбора используется одна и та же разметка Markdown для селектора. Поэтому рекомендуется поместить селектор для статьи во включаемый файл.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-328">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="6fb6f-329">Затем нужно добавить ссылки на этот файл во все статьи, для которых используется селектор.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-329">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="6fb6f-330">Фрагменты кода</span><span class="sxs-lookup"><span data-stu-id="6fb6f-330">Code snippets</span></span>

<span data-ttu-id="6fb6f-331">В Markdig есть расширение с расширенными функциями для включения в статью фрагментов кода.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-331">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="6fb6f-332">Этот формат обеспечивает расширенный рендеринг на основе функций GFM, таких как выбор языка программирования и раскраска синтаксиса, а также другие полезные функции, например:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-332">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="6fb6f-333">включение централизованных примеров или фрагментов кода из внешнего репозитория;</span><span class="sxs-lookup"><span data-stu-id="6fb6f-333">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="6fb6f-334">пользовательский интерфейс с вкладками для отображения нескольких версий примеров кода на разных языках.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-334">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="6fb6f-335">Сбои и устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="6fb6f-335">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="6fb6f-336">Замещающий текст</span><span class="sxs-lookup"><span data-stu-id="6fb6f-336">Alt text</span></span>

<span data-ttu-id="6fb6f-337">Замещающий текст, который содержит символы подчеркивания, отображается некорректно.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-337">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="6fb6f-338">Например, вместо</span><span class="sxs-lookup"><span data-stu-id="6fb6f-338">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="6fb6f-339">используйте следующий вариант, позволяющий избежать символов подчеркивания:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-339">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="6fb6f-340">Апострофы и кавычки</span><span class="sxs-lookup"><span data-stu-id="6fb6f-340">Apostrophes and quotation marks</span></span>

<span data-ttu-id="6fb6f-341">Если вы копируете текст из Word в редактор Markdown, он может содержать книжные (изогнутые) апострофы или кавычки.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-341">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="6fb6f-342">Их нужно заменить кодом или обычными апострофами или кавычками.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-342">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span>
<span data-ttu-id="6fb6f-343">В противном случае после публикации файла может отобразиться нечитаемый текст, например Itâ€™s.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-343">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="6fb6f-344">Ниже приведены кодировки для этих знаков пунктуации:</span><span class="sxs-lookup"><span data-stu-id="6fb6f-344">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="6fb6f-345">левая (открывающая) кавычка: `&#8220;`;</span><span class="sxs-lookup"><span data-stu-id="6fb6f-345">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="6fb6f-346">правая (закрывающая) кавычка: `&#8221;`;</span><span class="sxs-lookup"><span data-stu-id="6fb6f-346">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="6fb6f-347">правая закрывающая одинарная кавычка или апостроф: `&#8217;`;</span><span class="sxs-lookup"><span data-stu-id="6fb6f-347">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="6fb6f-348">левая открывающая одинарная кавычка (используется редко): `&#8216;`.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-348">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="6fb6f-349">Угловые скобки</span><span class="sxs-lookup"><span data-stu-id="6fb6f-349">Angle brackets</span></span>

<span data-ttu-id="6fb6f-350">Угловые скобки, как правило, используются для обозначения заполнителя.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-350">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="6fb6f-351">Если вы используете угловые скобки в тексте (а не в коде), их необходимо закодировать.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-351">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="6fb6f-352">Иначе Markdown распознает их как часть тега HTML.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-352">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="6fb6f-353">Например, `<script name>` следует закодировать как `&lt;script name&gt;`.</span><span class="sxs-lookup"><span data-stu-id="6fb6f-353">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="6fb6f-354">Дополнительные материалы</span><span class="sxs-lookup"><span data-stu-id="6fb6f-354">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="6fb6f-355">Ресурсы Markdown</span><span class="sxs-lookup"><span data-stu-id="6fb6f-355">Markdown resources</span></span>

- <span data-ttu-id="6fb6f-356">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax) (Синтаксис Markdown)</span><span class="sxs-lookup"><span data-stu-id="6fb6f-356">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- <span data-ttu-id="6fb6f-357">[Markdown cheat-sheet](./media/documents/markdown-cheatsheet.pdf?raw=true) (Шпаргалка по Markdown)</span><span class="sxs-lookup"><span data-stu-id="6fb6f-357">[Docs Markdown cheat sheet](./media/documents/markdown-cheatsheet.pdf?raw=true)</span></span>
- [<span data-ttu-id="6fb6f-358">Базовые сведения о разметке Markdown на GitHub</span><span class="sxs-lookup"><span data-stu-id="6fb6f-358">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- <span data-ttu-id="6fb6f-359">[The Markdown Guide](https://www.markdownguide.org/) (Руководство по Markdown)</span><span class="sxs-lookup"><span data-stu-id="6fb6f-359">[The Markdown Guide](https://www.markdownguide.org/)</span></span>
