---
title: Использование языка разметки Markdown для написания документации
description: В этой статье приводятся базовые и справочные сведения о языке разметки Markdown, используемом для написания статей на сайте docs.microsoft.com.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 07/13/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 96d00abc052c3b23ca62201dccdbe590a927e72d
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2018
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="1a44f-103">Использование языка разметки Markdown для написания документации</span><span class="sxs-lookup"><span data-stu-id="1a44f-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="1a44f-104">Статьи на сайте docs.microsoft.com написаны на [Markdown](https://daringfireball.net/projects/markdown/) — упрощенном языке разметки, который легко использовать и изучать.</span><span class="sxs-lookup"><span data-stu-id="1a44f-104">Docs.microsoft.com articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="1a44f-105">Благодаря своей простоте он быстро становится отраслевым стандартом.</span><span class="sxs-lookup"><span data-stu-id="1a44f-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="1a44f-106">Так как документация хранится в репозитории GitHub, для нее можно использовать расширенный набор Markdown под названием [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/). Этот формат предусматривает дополнительные возможности для решения распространенных задач.</span><span class="sxs-lookup"><span data-stu-id="1a44f-106">Because Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="1a44f-107">Кроме того, службы Open Publishing Services (OPS) поддерживают формат DocFX Flavored Markdown (DFM).</span><span class="sxs-lookup"><span data-stu-id="1a44f-107">Additionally, Open Publishing Services (OPS) implements DocFX Flavored Markdown (DFM).</span></span> <span data-ttu-id="1a44f-108">DFM обеспечивает высокий уровень совместимости с форматом GitHub Flavored Markdown (GFM), предоставляя специальные функции для работы с документацией.</span><span class="sxs-lookup"><span data-stu-id="1a44f-108">DFM is highly compatible with GitHub Flavored Markdown (GFM), adding functionality to enable Docs-specific features.</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="1a44f-109">Базовые сведения о Markdown</span><span class="sxs-lookup"><span data-stu-id="1a44f-109">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="1a44f-110">Заголовки</span><span class="sxs-lookup"><span data-stu-id="1a44f-110">Headings</span></span>

<span data-ttu-id="1a44f-111">Чтобы создать заголовок, используйте знак (#), например:</span><span class="sxs-lookup"><span data-stu-id="1a44f-111">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="1a44f-112">Полужирное начертание и курсив</span><span class="sxs-lookup"><span data-stu-id="1a44f-112">Bold and italic text</span></span>

<span data-ttu-id="1a44f-113">Чтобы задать для текста **полужирное начертание**, заключите его в двойные звездочки:</span><span class="sxs-lookup"><span data-stu-id="1a44f-113">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
    This text is **bold**.
```

<span data-ttu-id="1a44f-114">Чтобы задать для текста *курсивное начертание*, заключите его в одинарные звездочки:</span><span class="sxs-lookup"><span data-stu-id="1a44f-114">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
    This text is *italic*.
```

<span data-ttu-id="1a44f-115">Чтобы задать для текста ***полужирное и курсивное*** начертание, заключите его в тройные звездочки:</span><span class="sxs-lookup"><span data-stu-id="1a44f-115">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="1a44f-116">Списки</span><span class="sxs-lookup"><span data-stu-id="1a44f-116">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="1a44f-117">Неупорядоченный список</span><span class="sxs-lookup"><span data-stu-id="1a44f-117">Unordered list</span></span>

<span data-ttu-id="1a44f-118">Неупорядоченный (маркированный) список можно отформатировать с помощью звездочек или тире.</span><span class="sxs-lookup"><span data-stu-id="1a44f-118">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="1a44f-119">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="1a44f-119">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="1a44f-120">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="1a44f-120">will be rendered as:</span></span>

- <span data-ttu-id="1a44f-121">List item 1</span><span class="sxs-lookup"><span data-stu-id="1a44f-121">List item 1</span></span>
- <span data-ttu-id="1a44f-122">List item 2</span><span class="sxs-lookup"><span data-stu-id="1a44f-122">List item 2</span></span>
- <span data-ttu-id="1a44f-123">List item 3</span><span class="sxs-lookup"><span data-stu-id="1a44f-123">List item 3</span></span>

<span data-ttu-id="1a44f-124">Чтобы вложить один список в другой, добавьте отступ для элементов дочернего списка.</span><span class="sxs-lookup"><span data-stu-id="1a44f-124">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="1a44f-125">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="1a44f-125">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="1a44f-126">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="1a44f-126">will be rendered as:</span></span>

- <span data-ttu-id="1a44f-127">List item 1</span><span class="sxs-lookup"><span data-stu-id="1a44f-127">List item 1</span></span>
  - <span data-ttu-id="1a44f-128">List item A</span><span class="sxs-lookup"><span data-stu-id="1a44f-128">List item A</span></span>
  - <span data-ttu-id="1a44f-129">List item B</span><span class="sxs-lookup"><span data-stu-id="1a44f-129">List item B</span></span>
- <span data-ttu-id="1a44f-130">List item 2</span><span class="sxs-lookup"><span data-stu-id="1a44f-130">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="1a44f-131">Упорядоченный список</span><span class="sxs-lookup"><span data-stu-id="1a44f-131">Ordered list</span></span>

<span data-ttu-id="1a44f-132">Упорядоченный (ступенчатый) список можно отформатировать с помощью соответствующих цифр.</span><span class="sxs-lookup"><span data-stu-id="1a44f-132">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="1a44f-133">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="1a44f-133">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="1a44f-134">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="1a44f-134">will be rendered as:</span></span>

1. <span data-ttu-id="1a44f-135">First instruction</span><span class="sxs-lookup"><span data-stu-id="1a44f-135">First instruction</span></span>
2. <span data-ttu-id="1a44f-136">Second instruction</span><span class="sxs-lookup"><span data-stu-id="1a44f-136">Second instruction</span></span>
3. <span data-ttu-id="1a44f-137">Third instruction</span><span class="sxs-lookup"><span data-stu-id="1a44f-137">Third instruction</span></span>

<span data-ttu-id="1a44f-138">Чтобы вложить один список в другой, добавьте отступ для элементов дочернего списка.</span><span class="sxs-lookup"><span data-stu-id="1a44f-138">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="1a44f-139">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="1a44f-139">For example, the following Markdown:</span></span>

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="1a44f-140">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="1a44f-140">will be rendered as:</span></span>

1. <span data-ttu-id="1a44f-141">First instruction</span><span class="sxs-lookup"><span data-stu-id="1a44f-141">First instruction</span></span>
    1. <span data-ttu-id="1a44f-142">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="1a44f-142">Sub-instruction</span></span>
    2. <span data-ttu-id="1a44f-143">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="1a44f-143">Sub-instruction</span></span>
2. <span data-ttu-id="1a44f-144">Second instruction</span><span class="sxs-lookup"><span data-stu-id="1a44f-144">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="1a44f-145">Tables</span><span class="sxs-lookup"><span data-stu-id="1a44f-145">Tables</span></span>

<span data-ttu-id="1a44f-146">Таблицы не входят в основную спецификацию Markdown, но их поддерживает GFM.</span><span class="sxs-lookup"><span data-stu-id="1a44f-146">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="1a44f-147">Создавать таблицы можно с помощью символов вертикальной черты (|) и дефиса (-).</span><span class="sxs-lookup"><span data-stu-id="1a44f-147">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="1a44f-148">Дефисы позволяют создавать для каждого столбца заголовок. Вертикальные черты разделяют столбцы.</span><span class="sxs-lookup"><span data-stu-id="1a44f-148">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="1a44f-149">Чтобы таблица правильно отображалась, включите перед ней пустую строку.</span><span class="sxs-lookup"><span data-stu-id="1a44f-149">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="1a44f-150">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="1a44f-150">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="1a44f-151">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="1a44f-151">will be rendered as:</span></span>

| <span data-ttu-id="1a44f-152">Fun</span><span class="sxs-lookup"><span data-stu-id="1a44f-152">Fun</span></span>                  | <span data-ttu-id="1a44f-153">with</span><span class="sxs-lookup"><span data-stu-id="1a44f-153">With</span></span>                 | <span data-ttu-id="1a44f-154">Tables</span><span class="sxs-lookup"><span data-stu-id="1a44f-154">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="1a44f-155">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="1a44f-155">left-aligned column</span></span>  | <span data-ttu-id="1a44f-156">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="1a44f-156">right-aligned column</span></span> | <span data-ttu-id="1a44f-157">centered column</span><span class="sxs-lookup"><span data-stu-id="1a44f-157">centered column</span></span> |
| <span data-ttu-id="1a44f-158">$100</span><span class="sxs-lookup"><span data-stu-id="1a44f-158">$100</span></span>                 | <span data-ttu-id="1a44f-159">$100</span><span class="sxs-lookup"><span data-stu-id="1a44f-159">$100</span></span>                 | <span data-ttu-id="1a44f-160">$100</span><span class="sxs-lookup"><span data-stu-id="1a44f-160">$100</span></span>            |
| <span data-ttu-id="1a44f-161">$10</span><span class="sxs-lookup"><span data-stu-id="1a44f-161">$10</span></span>                  | <span data-ttu-id="1a44f-162">$10</span><span class="sxs-lookup"><span data-stu-id="1a44f-162">$10</span></span>                  | <span data-ttu-id="1a44f-163">$10</span><span class="sxs-lookup"><span data-stu-id="1a44f-163">$10</span></span>             |
| <span data-ttu-id="1a44f-164">$1</span><span class="sxs-lookup"><span data-stu-id="1a44f-164">$1</span></span>                   | <span data-ttu-id="1a44f-165">$1</span><span class="sxs-lookup"><span data-stu-id="1a44f-165">$1</span></span>                   | <span data-ttu-id="1a44f-166">$1</span><span class="sxs-lookup"><span data-stu-id="1a44f-166">$1</span></span>              |

<span data-ttu-id="1a44f-167">Дополнительные сведения о создании таблиц:</span><span class="sxs-lookup"><span data-stu-id="1a44f-167">For more information on creating tables, see:</span></span>

- <span data-ttu-id="1a44f-168">Раздел о [функции переноса таблиц](#table-wrapping) DFM, которая поможет при форматировании широких таблиц.</span><span class="sxs-lookup"><span data-stu-id="1a44f-168">The DFM [table wrapping feature](#table-wrapping), which can help with formatting of wide tables</span></span>
- <span data-ttu-id="1a44f-169">Статья на сайте GitHub [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/) (Упорядочение информации при помощи таблиц).</span><span class="sxs-lookup"><span data-stu-id="1a44f-169">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)</span></span>
- <span data-ttu-id="1a44f-170">Веб-приложение [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="1a44f-170">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app</span></span>
- <span data-ttu-id="1a44f-171">Статья Адама Притчарда (Adam Pritchard) [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables) (Шпаргалка по Markdown).</span><span class="sxs-lookup"><span data-stu-id="1a44f-171">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)</span></span>
- <span data-ttu-id="1a44f-172">Статья Майкла Фортина (Michel Fortin) [Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) (Расширение Markdown Extra).</span><span class="sxs-lookup"><span data-stu-id="1a44f-172">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table)</span></span>
- <span data-ttu-id="1a44f-173">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/) (Преобразование таблиц HTML в Markdown)</span><span class="sxs-lookup"><span data-stu-id="1a44f-173">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/)</span></span>

### <a name="links"></a><span data-ttu-id="1a44f-174">Создание ссылок</span><span class="sxs-lookup"><span data-stu-id="1a44f-174">Links</span></span>

<span data-ttu-id="1a44f-175">Синтаксис Markdown для встроенной ссылки состоит из части `[link text]`, представляющей текст гиперссылки, и части `(file-name.md)` — URL-адреса или имени файла, на который дается ссылка:</span><span class="sxs-lookup"><span data-stu-id="1a44f-175">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="1a44f-176">Дополнительные сведения о ссылках:</span><span class="sxs-lookup"><span data-stu-id="1a44f-176">For more information on linking, see:</span></span>

- <span data-ttu-id="1a44f-177">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax#link) (Руководство по синтаксису Markdown), в котором предоставлена основная информация по поддержке ссылок Markdown.</span><span class="sxs-lookup"><span data-stu-id="1a44f-177">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="1a44f-178">Страница [Links](how-to-write-links.md) (Ссылки) этого руководства, на которой рассматриваются дополнительные возможности синтаксиса ссылок, предоставляемые DFM.</span><span class="sxs-lookup"><span data-stu-id="1a44f-178">The [Links](how-to-write-links.md) section of this guide for details on additional linking syntax that DFM provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="1a44f-179">Фрагменты кода</span><span class="sxs-lookup"><span data-stu-id="1a44f-179">Code snippets</span></span>

<span data-ttu-id="1a44f-180">Markdown поддерживает как встраивание фрагментов кода в предложение, так и их размещение между предложениями в виде отдельных огражденных блоков.</span><span class="sxs-lookup"><span data-stu-id="1a44f-180">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="1a44f-181">Дополнительная информация:</span><span class="sxs-lookup"><span data-stu-id="1a44f-181">For details, see:</span></span>

- [<span data-ttu-id="1a44f-182">Сведения о собственной поддержке блоков кода Markdown</span><span class="sxs-lookup"><span data-stu-id="1a44f-182">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="1a44f-183">Сведения о поддержке GFM для ограждения кода и выделения синтаксиса</span><span class="sxs-lookup"><span data-stu-id="1a44f-183">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="1a44f-184">Огражденные блоки кода — это простой способ выделить синтаксис для фрагментов кода.</span><span class="sxs-lookup"><span data-stu-id="1a44f-184">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="1a44f-185">Общий формат огражденных блоков кода:</span><span class="sxs-lookup"><span data-stu-id="1a44f-185">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="1a44f-186">Псевдоним после трех начальных символов обратной галочки \` определяет использование выделения.</span><span class="sxs-lookup"><span data-stu-id="1a44f-186">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="1a44f-187">Ниже представлен список часто используемых языков программирования для написания документации и приводятся соответствующие метки.</span><span class="sxs-lookup"><span data-stu-id="1a44f-187">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="1a44f-188">Все эти языки поддерживают понятные имена, а большинство из них — выделение языка в имени.</span><span class="sxs-lookup"><span data-stu-id="1a44f-188">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="1a44f-189">Имя</span><span class="sxs-lookup"><span data-stu-id="1a44f-189">Name</span></span>|<span data-ttu-id="1a44f-190">Метка Markdown</span><span class="sxs-lookup"><span data-stu-id="1a44f-190">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="1a44f-191">.NET Console</span><span class="sxs-lookup"><span data-stu-id="1a44f-191">.NET Console</span></span>|<span data-ttu-id="1a44f-192">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="1a44f-192">dotnetcli</span></span>|
|<span data-ttu-id="1a44f-193">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="1a44f-193">ASP.NET (C#)</span></span>|<span data-ttu-id="1a44f-194">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="1a44f-194">aspx-csharp</span></span>|
|<span data-ttu-id="1a44f-195">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="1a44f-195">ASP.NET (VB)</span></span>|<span data-ttu-id="1a44f-196">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="1a44f-196">aspx-vb</span></span>|
|<span data-ttu-id="1a44f-197">AzCopy</span><span class="sxs-lookup"><span data-stu-id="1a44f-197">AzCopy</span></span>|<span data-ttu-id="1a44f-198">azcopy</span><span class="sxs-lookup"><span data-stu-id="1a44f-198">azcopy</span></span>|
|<span data-ttu-id="1a44f-199">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="1a44f-199">Azure CLI</span></span>|<span data-ttu-id="1a44f-200">azurecli</span><span class="sxs-lookup"><span data-stu-id="1a44f-200">azurecli</span></span>|
|<span data-ttu-id="1a44f-201">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1a44f-201">Azure PowerShell</span></span>|<span data-ttu-id="1a44f-202">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="1a44f-202">azurepowershell</span></span>|
|<span data-ttu-id="1a44f-203">C++</span><span class="sxs-lookup"><span data-stu-id="1a44f-203">C++</span></span>|<span data-ttu-id="1a44f-204">cpp</span><span class="sxs-lookup"><span data-stu-id="1a44f-204">cpp</span></span>|
|<span data-ttu-id="1a44f-205">C++/CX</span><span class="sxs-lookup"><span data-stu-id="1a44f-205">C++/CX</span></span>|<span data-ttu-id="1a44f-206">cppcx</span><span class="sxs-lookup"><span data-stu-id="1a44f-206">cppcx</span></span>|
|<span data-ttu-id="1a44f-207">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="1a44f-207">C++/WinRT</span></span>|<span data-ttu-id="1a44f-208">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="1a44f-208">cppwinrt</span></span>|
|<span data-ttu-id="1a44f-209">C#</span><span class="sxs-lookup"><span data-stu-id="1a44f-209">C#</span></span>|<span data-ttu-id="1a44f-210">csharp</span><span class="sxs-lookup"><span data-stu-id="1a44f-210">csharp</span></span>|
|<span data-ttu-id="1a44f-211">CSHTML</span><span class="sxs-lookup"><span data-stu-id="1a44f-211">CSHTML</span></span>|<span data-ttu-id="1a44f-212">cshtml</span><span class="sxs-lookup"><span data-stu-id="1a44f-212">cshtml</span></span>|
|<span data-ttu-id="1a44f-213">DAX</span><span class="sxs-lookup"><span data-stu-id="1a44f-213">DAX</span></span>|<span data-ttu-id="1a44f-214">dax</span><span class="sxs-lookup"><span data-stu-id="1a44f-214">dax</span></span>|
|<span data-ttu-id="1a44f-215">F#</span><span class="sxs-lookup"><span data-stu-id="1a44f-215">F#</span></span>|<span data-ttu-id="1a44f-216">fsharp</span><span class="sxs-lookup"><span data-stu-id="1a44f-216">fsharp</span></span>|
|<span data-ttu-id="1a44f-217">Go</span><span class="sxs-lookup"><span data-stu-id="1a44f-217">Go</span></span>|<span data-ttu-id="1a44f-218">go</span><span class="sxs-lookup"><span data-stu-id="1a44f-218">go</span></span>|
|<span data-ttu-id="1a44f-219">HTML</span><span class="sxs-lookup"><span data-stu-id="1a44f-219">HTML</span></span>|<span data-ttu-id="1a44f-220">html</span><span class="sxs-lookup"><span data-stu-id="1a44f-220">html</span></span>|
|<span data-ttu-id="1a44f-221">HTTP</span><span class="sxs-lookup"><span data-stu-id="1a44f-221">HTTP</span></span>|<span data-ttu-id="1a44f-222">http</span><span class="sxs-lookup"><span data-stu-id="1a44f-222">http</span></span>|
|<span data-ttu-id="1a44f-223">Java</span><span class="sxs-lookup"><span data-stu-id="1a44f-223">Java</span></span>|<span data-ttu-id="1a44f-224">java</span><span class="sxs-lookup"><span data-stu-id="1a44f-224">java</span></span>|
|<span data-ttu-id="1a44f-225">JavaScript</span><span class="sxs-lookup"><span data-stu-id="1a44f-225">JavaScript</span></span>|<span data-ttu-id="1a44f-226">javascript</span><span class="sxs-lookup"><span data-stu-id="1a44f-226">javascript</span></span>|
|<span data-ttu-id="1a44f-227">JSON</span><span class="sxs-lookup"><span data-stu-id="1a44f-227">JSON</span></span>|<span data-ttu-id="1a44f-228">json</span><span class="sxs-lookup"><span data-stu-id="1a44f-228">json</span></span>|
|<span data-ttu-id="1a44f-229">Markdown</span><span class="sxs-lookup"><span data-stu-id="1a44f-229">Markdown</span></span>|<span data-ttu-id="1a44f-230">md</span><span class="sxs-lookup"><span data-stu-id="1a44f-230">md</span></span>|
|<span data-ttu-id="1a44f-231">NodeJS</span><span class="sxs-lookup"><span data-stu-id="1a44f-231">NodeJS</span></span>|<span data-ttu-id="1a44f-232">nodejs</span><span class="sxs-lookup"><span data-stu-id="1a44f-232">nodejs</span></span>|
|<span data-ttu-id="1a44f-233">Objective-C</span><span class="sxs-lookup"><span data-stu-id="1a44f-233">Objective-C</span></span>|<span data-ttu-id="1a44f-234">objc</span><span class="sxs-lookup"><span data-stu-id="1a44f-234">objc</span></span>|
|<span data-ttu-id="1a44f-235">OData</span><span class="sxs-lookup"><span data-stu-id="1a44f-235">OData</span></span>|<span data-ttu-id="1a44f-236">odata</span><span class="sxs-lookup"><span data-stu-id="1a44f-236">odata</span></span>|
|<span data-ttu-id="1a44f-237">PHP</span><span class="sxs-lookup"><span data-stu-id="1a44f-237">PHP</span></span>|<span data-ttu-id="1a44f-238">php</span><span class="sxs-lookup"><span data-stu-id="1a44f-238">php</span></span>|
|<span data-ttu-id="1a44f-239">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="1a44f-239">Power Apps Formula</span></span>|<span data-ttu-id="1a44f-240">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="1a44f-240">powerappsfl</span></span>|
|<span data-ttu-id="1a44f-241">PowerShell</span><span class="sxs-lookup"><span data-stu-id="1a44f-241">PowerShell</span></span>|<span data-ttu-id="1a44f-242">powershell</span><span class="sxs-lookup"><span data-stu-id="1a44f-242">powershell</span></span>|
|<span data-ttu-id="1a44f-243">Python</span><span class="sxs-lookup"><span data-stu-id="1a44f-243">Python</span></span>|<span data-ttu-id="1a44f-244">python</span><span class="sxs-lookup"><span data-stu-id="1a44f-244">python</span></span>|
|<span data-ttu-id="1a44f-245">Q#</span><span class="sxs-lookup"><span data-stu-id="1a44f-245">Q#</span></span>|<span data-ttu-id="1a44f-246">qsharp</span><span class="sxs-lookup"><span data-stu-id="1a44f-246">qsharp</span></span>|
|<span data-ttu-id="1a44f-247">Ruby</span><span class="sxs-lookup"><span data-stu-id="1a44f-247">Ruby</span></span>|<span data-ttu-id="1a44f-248">ruby</span><span class="sxs-lookup"><span data-stu-id="1a44f-248">ruby</span></span>|
|<span data-ttu-id="1a44f-249">SQL</span><span class="sxs-lookup"><span data-stu-id="1a44f-249">SQL</span></span>|<span data-ttu-id="1a44f-250">sql</span><span class="sxs-lookup"><span data-stu-id="1a44f-250">sql</span></span>|
|<span data-ttu-id="1a44f-251">Swift</span><span class="sxs-lookup"><span data-stu-id="1a44f-251">Swift</span></span>|<span data-ttu-id="1a44f-252">swift</span><span class="sxs-lookup"><span data-stu-id="1a44f-252">swift</span></span>|
|<span data-ttu-id="1a44f-253">TypeScript</span><span class="sxs-lookup"><span data-stu-id="1a44f-253">TypeScript</span></span>|<span data-ttu-id="1a44f-254">typescript</span><span class="sxs-lookup"><span data-stu-id="1a44f-254">typescript</span></span>|
|<span data-ttu-id="1a44f-255">VB</span><span class="sxs-lookup"><span data-stu-id="1a44f-255">VB</span></span>|<span data-ttu-id="1a44f-256">vb</span><span class="sxs-lookup"><span data-stu-id="1a44f-256">vb</span></span>|
|<span data-ttu-id="1a44f-257">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="1a44f-257">VSTS CLI</span></span>|<span data-ttu-id="1a44f-258">vstscli</span><span class="sxs-lookup"><span data-stu-id="1a44f-258">vstscli</span></span>|
|<span data-ttu-id="1a44f-259">XAML</span><span class="sxs-lookup"><span data-stu-id="1a44f-259">XAML</span></span>|<span data-ttu-id="1a44f-260">xaml</span><span class="sxs-lookup"><span data-stu-id="1a44f-260">xaml</span></span>|
|<span data-ttu-id="1a44f-261">XML</span><span class="sxs-lookup"><span data-stu-id="1a44f-261">XML</span></span>|<span data-ttu-id="1a44f-262">xml</span><span class="sxs-lookup"><span data-stu-id="1a44f-262">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="1a44f-263">Пример: C\#</span><span class="sxs-lookup"><span data-stu-id="1a44f-263">Example: C\#</span></span>

<span data-ttu-id="1a44f-264">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="1a44f-264">__Markdown__</span></span>

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

<span data-ttu-id="1a44f-265">__Отображение__</span><span class="sxs-lookup"><span data-stu-id="1a44f-265">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="1a44f-266">Пример: SQL</span><span class="sxs-lookup"><span data-stu-id="1a44f-266">Example: SQL</span></span>

<span data-ttu-id="1a44f-267">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="1a44f-267">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="1a44f-268">__Отображение__</span><span class="sxs-lookup"><span data-stu-id="1a44f-268">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="1a44f-269">Настраиваемые расширения OPS для Markdown</span><span class="sxs-lookup"><span data-stu-id="1a44f-269">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="1a44f-270">Службы Open Publishing Services (OPS) поддерживают формат DocFX Flavored Markdown (DFM), который обеспечивает высокий уровень совместимости с форматом GitHub Flavored Markdown (GFM).</span><span class="sxs-lookup"><span data-stu-id="1a44f-270">Open Publishing Services (OPS) implements DocFX Flavored Markdown (DFM), which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="1a44f-271">DFM предоставляет дополнительные функции при использовании расширений Markdown.</span><span class="sxs-lookup"><span data-stu-id="1a44f-271">DFM adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="1a44f-272">Поэтому для справки мы включили в этот материал некоторые разделы из руководства по разработке OPS.</span><span class="sxs-lookup"><span data-stu-id="1a44f-272">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="1a44f-273">(Например, см. разделы с инструкциями по использованию фрагментов кода и расширений DFM и Markdown.)</span><span class="sxs-lookup"><span data-stu-id="1a44f-273">(For example, see "DFM and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="1a44f-274">В статьях документации для общего форматирования, например для создания абзацев, ссылок, списков и заголовков, используется GFM.</span><span class="sxs-lookup"><span data-stu-id="1a44f-274">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="1a44f-275">Для расширенного форматирования можно использовать функции DFM, например:</span><span class="sxs-lookup"><span data-stu-id="1a44f-275">For richer formatting, articles can use DFM features such as:</span></span>

- <span data-ttu-id="1a44f-276">блоки заметок;</span><span class="sxs-lookup"><span data-stu-id="1a44f-276">Note blocks</span></span>
- <span data-ttu-id="1a44f-277">включаемые файлы;</span><span class="sxs-lookup"><span data-stu-id="1a44f-277">Includes</span></span>
- <span data-ttu-id="1a44f-278">селекторы;</span><span class="sxs-lookup"><span data-stu-id="1a44f-278">Selectors</span></span>
- <span data-ttu-id="1a44f-279">внедренные видео;</span><span class="sxs-lookup"><span data-stu-id="1a44f-279">Embedded videos</span></span>
- <span data-ttu-id="1a44f-280">фрагменты или примеры кода.</span><span class="sxs-lookup"><span data-stu-id="1a44f-280">Code snippets/samples</span></span>

<span data-ttu-id="1a44f-281">Чтобы ознакомиться с полным списком, см. разделы с инструкциями по использованию фрагментов кода и расширений DFM и Markdown.</span><span class="sxs-lookup"><span data-stu-id="1a44f-281">For the complete list, refer to "DFM and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="1a44f-282">Блоки заметок</span><span class="sxs-lookup"><span data-stu-id="1a44f-282">Note blocks</span></span>

<span data-ttu-id="1a44f-283">Есть четыре типа блоков заметок, которые позволяют привлечь внимание к определенному содержимому:</span><span class="sxs-lookup"><span data-stu-id="1a44f-283">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="1a44f-284">ПРИМЕЧАНИЕ;</span><span class="sxs-lookup"><span data-stu-id="1a44f-284">NOTE</span></span>
- <span data-ttu-id="1a44f-285">ПРЕДУПРЕЖДЕНИЕ;</span><span class="sxs-lookup"><span data-stu-id="1a44f-285">WARNING</span></span>
- <span data-ttu-id="1a44f-286">СОВЕТ;</span><span class="sxs-lookup"><span data-stu-id="1a44f-286">TIP</span></span>
- <span data-ttu-id="1a44f-287">ВАЖНО.</span><span class="sxs-lookup"><span data-stu-id="1a44f-287">IMPORTANT</span></span>

<span data-ttu-id="1a44f-288">В целом не следует часто использовать блоки заметок, так как они могут отвлекать пользователя от основного содержимого.</span><span class="sxs-lookup"><span data-stu-id="1a44f-288">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="1a44f-289">Хотя эти элементы также поддерживают блоки кода, изображения, списки и ссылки, лучше не перегружать их, делая простыми и понятными.</span><span class="sxs-lookup"><span data-stu-id="1a44f-289">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="1a44f-290">Включаемые файлы</span><span class="sxs-lookup"><span data-stu-id="1a44f-290">Includes</span></span>

<span data-ttu-id="1a44f-291">Чтобы включить в файлы статьи многократно используемые текстовые файлы или файлы изображения, можно добавить на них ссылки с помощью функции DFM для включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="1a44f-291">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the DFM file include feature.</span></span> <span data-ttu-id="1a44f-292">Функция указывает OPS включить файл в файл статьи во время сборки, чтобы он стал частью опубликованной статьи.</span><span class="sxs-lookup"><span data-stu-id="1a44f-292">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="1a44f-293">Существует три типа включаемых файлов для многократного использования содержимого:</span><span class="sxs-lookup"><span data-stu-id="1a44f-293">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="1a44f-294">Встроенные — для многократного использования фрагмента стандартного текста путем его встраивания в другое предложение.</span><span class="sxs-lookup"><span data-stu-id="1a44f-294">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="1a44f-295">Блочные — для многократного использования всего файла Markdown в качестве блока путем его вложения в раздел или статью.</span><span class="sxs-lookup"><span data-stu-id="1a44f-295">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="1a44f-296">Изображения — позволяют включать стандартное изображение в документацию.</span><span class="sxs-lookup"><span data-stu-id="1a44f-296">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="1a44f-297">Встроенные и блочные включаемые файлы — это простые файлы Markdown с расширением .md.</span><span class="sxs-lookup"><span data-stu-id="1a44f-297">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="1a44f-298">Они могут содержать любую допустимую разметку Markdown.</span><span class="sxs-lookup"><span data-stu-id="1a44f-298">It can contain any valid Markdown.</span></span> <span data-ttu-id="1a44f-299">Все включаемые файлы Markdown должны быть помещены в [общий подкаталог `/includes`](git-github-fundamentals.md#includes-subdirectory) в корневом каталоге репозитория.</span><span class="sxs-lookup"><span data-stu-id="1a44f-299">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="1a44f-300">Когда статья публикуется, включаемый файл легко интегрируется в нее.</span><span class="sxs-lookup"><span data-stu-id="1a44f-300">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="1a44f-301">Далее приведены требования по работе с включаемыми файлами.</span><span class="sxs-lookup"><span data-stu-id="1a44f-301">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="1a44f-302">Используйте включаемые файлы, если вам нужно, чтобы один и тот же текст отображался в нескольких статьях.</span><span class="sxs-lookup"><span data-stu-id="1a44f-302">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="1a44f-303">Блочные включаемые файлы предназначены для значительных объемов текста: один или два абзаца, общая процедура или общий раздел.</span><span class="sxs-lookup"><span data-stu-id="1a44f-303">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="1a44f-304">Не используйте их для фрагментов текста меньше одного предложения.</span><span class="sxs-lookup"><span data-stu-id="1a44f-304">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="1a44f-305">Включаемые файлы не отображаются в представлении статьи на сайте GitHub. Они используют расширения DFM</span><span class="sxs-lookup"><span data-stu-id="1a44f-305">Includes won't be rendered in the GitHub rendered view of your article, because they rely on DFM extensions.</span></span> <span data-ttu-id="1a44f-306">Они отображаются только после публикации.</span><span class="sxs-lookup"><span data-stu-id="1a44f-306">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="1a44f-307">Весь текст во включаемом файле должен состоять из полноценных предложений или фраз, не зависящих от остального текста статьи, в которую добавляется ссылка на такой файл.</span><span class="sxs-lookup"><span data-stu-id="1a44f-307">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="1a44f-308">Если не следовать этой инструкции, в статье создаются непереводимые строки, которые нарушают процесс локализации.</span><span class="sxs-lookup"><span data-stu-id="1a44f-308">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="1a44f-309">Не внедряйте одни включаемые файлы в другие.</span><span class="sxs-lookup"><span data-stu-id="1a44f-309">Don't embed includes within other includes.</span></span> <span data-ttu-id="1a44f-310">Такая возможность не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1a44f-310">They are not supported.</span></span>
- <span data-ttu-id="1a44f-311">Файлы мультимедиа должны быть помещены в отдельную папку мультимедиа в подкаталоге включаемых файлов. Например, `<repo>`/включаемые файлы/папка мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1a44f-311">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="1a44f-312">В корне каталога мультимедиа не должны содержаться изображения.</span><span class="sxs-lookup"><span data-stu-id="1a44f-312">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="1a44f-313">Если во включаемом файле нет изображений, соответствующий каталог мультимедиа не требуется.</span><span class="sxs-lookup"><span data-stu-id="1a44f-313">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="1a44f-314">Как и в обычных статьях, не используйте общий файл мультимедиа для включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="1a44f-314">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="1a44f-315">Для каждого включаемого файла в статье должен быть создан отдельный файл мультимедиа с уникальным именем.</span><span class="sxs-lookup"><span data-stu-id="1a44f-315">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="1a44f-316">Файл мультимедиа должен храниться в папке мультимедиа, связанной с включаемым файлом.</span><span class="sxs-lookup"><span data-stu-id="1a44f-316">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="1a44f-317">Не используйте включаемый файл как единственное содержимое статьи.</span><span class="sxs-lookup"><span data-stu-id="1a44f-317">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="1a44f-318">Включаемые файлы предназначены для дополнения основных материалов статьи.</span><span class="sxs-lookup"><span data-stu-id="1a44f-318">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="1a44f-319">Селекторы</span><span class="sxs-lookup"><span data-stu-id="1a44f-319">Selectors</span></span>

<span data-ttu-id="1a44f-320">В технических статьях селекторы применяются для создания разных вариантов содержимого, чтобы проиллюстрировать различия в реализации, связанные с использованием нескольких технологий или платформ.</span><span class="sxs-lookup"><span data-stu-id="1a44f-320">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="1a44f-321">Это в особенности применимо к материалам о мобильных платформах для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="1a44f-321">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="1a44f-322">Сейчас в DFM есть два типа селекторов: для единичного и множественного выбора.</span><span class="sxs-lookup"><span data-stu-id="1a44f-322">There are currently two different types of selectors in DFM, a single selector and a multi-selector.</span></span>

<span data-ttu-id="1a44f-323">В каждой статье с возможностью выбора используется одна и та же разметка Markdown для селектора. Поэтому рекомендуется поместить селектор для статьи во включаемый файл.</span><span class="sxs-lookup"><span data-stu-id="1a44f-323">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="1a44f-324">Затем нужно добавить ссылки на этот файл во все статьи, для которых используется селектор.</span><span class="sxs-lookup"><span data-stu-id="1a44f-324">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="1a44f-325">Фрагменты кода</span><span class="sxs-lookup"><span data-stu-id="1a44f-325">Code snippets</span></span>

<span data-ttu-id="1a44f-326">DFM поддерживает включение дополнительного кода в статью с помощью расширения для фрагментов кода.</span><span class="sxs-lookup"><span data-stu-id="1a44f-326">DFM supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="1a44f-327">Этот формат обеспечивает расширенный рендеринг на основе функций GFM, таких как выбор языка программирования и раскраска синтаксиса, а также другие полезные функции, например:</span><span class="sxs-lookup"><span data-stu-id="1a44f-327">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="1a44f-328">включение централизованных примеров или фрагментов кода из внешнего репозитория;</span><span class="sxs-lookup"><span data-stu-id="1a44f-328">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="1a44f-329">пользовательский интерфейс с вкладками для отображения нескольких версий примеров кода на разных языках.</span><span class="sxs-lookup"><span data-stu-id="1a44f-329">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="1a44f-330">Сбои и устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="1a44f-330">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="1a44f-331">Замещающий текст</span><span class="sxs-lookup"><span data-stu-id="1a44f-331">Alt text</span></span>

<span data-ttu-id="1a44f-332">Замещающий текст, который содержит символы подчеркивания, отображается некорректно.</span><span class="sxs-lookup"><span data-stu-id="1a44f-332">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="1a44f-333">Например, вместо</span><span class="sxs-lookup"><span data-stu-id="1a44f-333">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="1a44f-334">используйте следующий вариант, позволяющий избежать символов подчеркивания:</span><span class="sxs-lookup"><span data-stu-id="1a44f-334">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="1a44f-335">Апострофы и кавычки</span><span class="sxs-lookup"><span data-stu-id="1a44f-335">Apostrophes and quotation marks</span></span>

<span data-ttu-id="1a44f-336">Если вы копируете текст из Word в редактор Markdown, он может содержать книжные (изогнутые) апострофы или кавычки.</span><span class="sxs-lookup"><span data-stu-id="1a44f-336">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="1a44f-337">Их нужно заменить кодом или обычными апострофами или кавычками.</span><span class="sxs-lookup"><span data-stu-id="1a44f-337">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="1a44f-338">В противном случае после публикации файла может отобразиться нечитаемый текст, например Itâ€™s.</span><span class="sxs-lookup"><span data-stu-id="1a44f-338">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="1a44f-339">Ниже приведены кодировки для этих знаков пунктуации:</span><span class="sxs-lookup"><span data-stu-id="1a44f-339">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="1a44f-340">левая (открывающая) кавычка: `&#8220;`;</span><span class="sxs-lookup"><span data-stu-id="1a44f-340">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="1a44f-341">правая (закрывающая) кавычка: `&#8221;`;</span><span class="sxs-lookup"><span data-stu-id="1a44f-341">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="1a44f-342">правая закрывающая одинарная кавычка или апостроф: `&#8217;`;</span><span class="sxs-lookup"><span data-stu-id="1a44f-342">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="1a44f-343">левая открывающая одинарная кавычка (используется редко): `&#8216;`.</span><span class="sxs-lookup"><span data-stu-id="1a44f-343">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="1a44f-344">Угловые скобки</span><span class="sxs-lookup"><span data-stu-id="1a44f-344">Angle brackets</span></span>

<span data-ttu-id="1a44f-345">Если в тексте файла (не в коде) используются угловые скобки (например, для обозначения заполнителя), их нужно кодировать вручную.</span><span class="sxs-lookup"><span data-stu-id="1a44f-345">If you use angle brackets in text (not code) in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="1a44f-346">Иначе Markdown распознает их как часть тега HTML.</span><span class="sxs-lookup"><span data-stu-id="1a44f-346">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="1a44f-347">Например, `<script name>` следует закодировать как `&lt;script name&gt;`.</span><span class="sxs-lookup"><span data-stu-id="1a44f-347">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="1a44f-348">Дополнительные материалы</span><span class="sxs-lookup"><span data-stu-id="1a44f-348">See also</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="1a44f-349">Ресурсы Markdown</span><span class="sxs-lookup"><span data-stu-id="1a44f-349">Markdown resources</span></span>

- <span data-ttu-id="1a44f-350">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax) (Синтаксис Markdown)</span><span class="sxs-lookup"><span data-stu-id="1a44f-350">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- <span data-ttu-id="1a44f-351">[Markdown cheat-sheet](./media/documents/markdown-cheatsheet.pdf?raw=true) (Шпаргалка по Markdown)</span><span class="sxs-lookup"><span data-stu-id="1a44f-351">[Docs Markdown cheat sheet](./media/documents/markdown-cheatsheet.pdf?raw=true)</span></span>
- [<span data-ttu-id="1a44f-352">Базовые сведения о разметке Markdown на GitHub</span><span class="sxs-lookup"><span data-stu-id="1a44f-352">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
