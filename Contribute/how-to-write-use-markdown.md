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
ms.openlocfilehash: 041398361aef90c44bdf3a0dad4aaa2d40a38289
ms.sourcegitcommit: 782b689882cce3ce07f5613763322989f2d0d63f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/05/2018
ms.locfileid: "34469953"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="9a6a0-103">Использование языка разметки Markdown для написания документации</span><span class="sxs-lookup"><span data-stu-id="9a6a0-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="9a6a0-104">Статьи на сайте docs.microsoft.com написаны на [Markdown](https://daringfireball.net/projects/markdown/) — упрощенном языке разметки, который легко использовать и изучать.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-104">Docs.microsoft.com articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="9a6a0-105">Благодаря своей простоте он быстро становится отраслевым стандартом.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="9a6a0-106">Так как документация хранится в репозитории GitHub, для нее можно использовать расширенный набор Markdown под названием [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/). Этот формат предусматривает дополнительные возможности для решения распространенных задач.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-106">Because Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="9a6a0-107">Кроме того, службы Open Publishing Services (OPS) используют Markdig, синтаксический анализатор Markdown.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="9a6a0-108">Он обеспечивает высокую совместимость с диалектом GitHub Flavored Markdown (GFM), предоставляя дополнительные функции для работы с порталом Docs.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-108">Markdig is highly compatible with GitHub Flavored Markdown (GFM), adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="9a6a0-109">Markdig — это быстрый и мощный обработчик Markdown для .NET, обеспечивающий соответствие CommonMark и поддержку расширений.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="9a6a0-110">Улучшенная поддержка сообщества</span><span class="sxs-lookup"><span data-stu-id="9a6a0-110">Better community support</span></span>
* <span data-ttu-id="9a6a0-111">Улучшенная поддержка стандартов</span><span class="sxs-lookup"><span data-stu-id="9a6a0-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="9a6a0-112">Базовые сведения о Markdown</span><span class="sxs-lookup"><span data-stu-id="9a6a0-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="9a6a0-113">Заголовки</span><span class="sxs-lookup"><span data-stu-id="9a6a0-113">Headings</span></span>

<span data-ttu-id="9a6a0-114">Чтобы создать заголовок, используйте знак (#), например:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="9a6a0-115">Полужирное начертание и курсив</span><span class="sxs-lookup"><span data-stu-id="9a6a0-115">Bold and italic text</span></span>

<span data-ttu-id="9a6a0-116">Чтобы задать для текста **полужирное начертание**, заключите его в двойные звездочки:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-116">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
    This text is **bold**.
```

<span data-ttu-id="9a6a0-117">Чтобы задать для текста *курсивное начертание*, заключите его в одинарные звездочки:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-117">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
    This text is *italic*.
```

<span data-ttu-id="9a6a0-118">Чтобы задать для текста ***полужирное и курсивное*** начертание, заключите его в тройные звездочки:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-118">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="9a6a0-119">Списки</span><span class="sxs-lookup"><span data-stu-id="9a6a0-119">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="9a6a0-120">Неупорядоченный список</span><span class="sxs-lookup"><span data-stu-id="9a6a0-120">Unordered list</span></span>

<span data-ttu-id="9a6a0-121">Неупорядоченный (маркированный) список можно отформатировать с помощью звездочек или тире.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-121">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="9a6a0-122">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-122">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="9a6a0-123">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-123">will be rendered as:</span></span>

- <span data-ttu-id="9a6a0-124">List item 1</span><span class="sxs-lookup"><span data-stu-id="9a6a0-124">List item 1</span></span>
- <span data-ttu-id="9a6a0-125">List item 2</span><span class="sxs-lookup"><span data-stu-id="9a6a0-125">List item 2</span></span>
- <span data-ttu-id="9a6a0-126">List item 3</span><span class="sxs-lookup"><span data-stu-id="9a6a0-126">List item 3</span></span>

<span data-ttu-id="9a6a0-127">Чтобы вложить один список в другой, добавьте отступ для элементов дочернего списка.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-127">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="9a6a0-128">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-128">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="9a6a0-129">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-129">will be rendered as:</span></span>

- <span data-ttu-id="9a6a0-130">List item 1</span><span class="sxs-lookup"><span data-stu-id="9a6a0-130">List item 1</span></span>
  - <span data-ttu-id="9a6a0-131">List item A</span><span class="sxs-lookup"><span data-stu-id="9a6a0-131">List item A</span></span>
  - <span data-ttu-id="9a6a0-132">List item B</span><span class="sxs-lookup"><span data-stu-id="9a6a0-132">List item B</span></span>
- <span data-ttu-id="9a6a0-133">List item 2</span><span class="sxs-lookup"><span data-stu-id="9a6a0-133">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="9a6a0-134">Упорядоченный список</span><span class="sxs-lookup"><span data-stu-id="9a6a0-134">Ordered list</span></span>

<span data-ttu-id="9a6a0-135">Упорядоченный (ступенчатый) список можно отформатировать с помощью соответствующих цифр.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-135">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="9a6a0-136">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-136">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="9a6a0-137">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-137">will be rendered as:</span></span>

1. <span data-ttu-id="9a6a0-138">First instruction</span><span class="sxs-lookup"><span data-stu-id="9a6a0-138">First instruction</span></span>
2. <span data-ttu-id="9a6a0-139">Second instruction</span><span class="sxs-lookup"><span data-stu-id="9a6a0-139">Second instruction</span></span>
3. <span data-ttu-id="9a6a0-140">Third instruction</span><span class="sxs-lookup"><span data-stu-id="9a6a0-140">Third instruction</span></span>

<span data-ttu-id="9a6a0-141">Чтобы вложить один список в другой, добавьте отступ для элементов дочернего списка.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-141">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="9a6a0-142">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-142">For example, the following Markdown:</span></span>

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="9a6a0-143">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-143">will be rendered as:</span></span>

1. <span data-ttu-id="9a6a0-144">First instruction</span><span class="sxs-lookup"><span data-stu-id="9a6a0-144">First instruction</span></span>
    1. <span data-ttu-id="9a6a0-145">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="9a6a0-145">Sub-instruction</span></span>
    2. <span data-ttu-id="9a6a0-146">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="9a6a0-146">Sub-instruction</span></span>
2. <span data-ttu-id="9a6a0-147">Second instruction</span><span class="sxs-lookup"><span data-stu-id="9a6a0-147">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="9a6a0-148">Tables</span><span class="sxs-lookup"><span data-stu-id="9a6a0-148">Tables</span></span>

<span data-ttu-id="9a6a0-149">Таблицы не входят в основную спецификацию Markdown, но их поддерживает GFM.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-149">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="9a6a0-150">Создавать таблицы можно с помощью символов вертикальной черты (|) и дефиса (-).</span><span class="sxs-lookup"><span data-stu-id="9a6a0-150">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="9a6a0-151">Дефисы позволяют создавать для каждого столбца заголовок. Вертикальные черты разделяют столбцы.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-151">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="9a6a0-152">Чтобы таблица правильно отображалась, включите перед ней пустую строку.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-152">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="9a6a0-153">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-153">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="9a6a0-154">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-154">will be rendered as:</span></span>

| <span data-ttu-id="9a6a0-155">Fun</span><span class="sxs-lookup"><span data-stu-id="9a6a0-155">Fun</span></span>                  | <span data-ttu-id="9a6a0-156">with</span><span class="sxs-lookup"><span data-stu-id="9a6a0-156">With</span></span>                 | <span data-ttu-id="9a6a0-157">Tables</span><span class="sxs-lookup"><span data-stu-id="9a6a0-157">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="9a6a0-158">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="9a6a0-158">left-aligned column</span></span>  | <span data-ttu-id="9a6a0-159">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="9a6a0-159">right-aligned column</span></span> | <span data-ttu-id="9a6a0-160">centered column</span><span class="sxs-lookup"><span data-stu-id="9a6a0-160">centered column</span></span> |
| <span data-ttu-id="9a6a0-161">$100</span><span class="sxs-lookup"><span data-stu-id="9a6a0-161">$100</span></span>                 | <span data-ttu-id="9a6a0-162">$100</span><span class="sxs-lookup"><span data-stu-id="9a6a0-162">$100</span></span>                 | <span data-ttu-id="9a6a0-163">$100</span><span class="sxs-lookup"><span data-stu-id="9a6a0-163">$100</span></span>            |
| <span data-ttu-id="9a6a0-164">$10</span><span class="sxs-lookup"><span data-stu-id="9a6a0-164">$10</span></span>                  | <span data-ttu-id="9a6a0-165">$10</span><span class="sxs-lookup"><span data-stu-id="9a6a0-165">$10</span></span>                  | <span data-ttu-id="9a6a0-166">$10</span><span class="sxs-lookup"><span data-stu-id="9a6a0-166">$10</span></span>             |
| <span data-ttu-id="9a6a0-167">$1</span><span class="sxs-lookup"><span data-stu-id="9a6a0-167">$1</span></span>                   | <span data-ttu-id="9a6a0-168">$1</span><span class="sxs-lookup"><span data-stu-id="9a6a0-168">$1</span></span>                   | <span data-ttu-id="9a6a0-169">$1</span><span class="sxs-lookup"><span data-stu-id="9a6a0-169">$1</span></span>              |

<span data-ttu-id="9a6a0-170">Дополнительные сведения о создании таблиц:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-170">For more information on creating tables, see:</span></span>

- <span data-ttu-id="9a6a0-171">[Функция обтекания таблиц](#table-wrapping) в Markdig, которая поможет при форматировании широких таблиц.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-171">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables</span></span>
- <span data-ttu-id="9a6a0-172">Статья на сайте GitHub [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/) (Упорядочение информации при помощи таблиц).</span><span class="sxs-lookup"><span data-stu-id="9a6a0-172">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)</span></span>
- <span data-ttu-id="9a6a0-173">Веб-приложение [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="9a6a0-173">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app</span></span>
- <span data-ttu-id="9a6a0-174">Статья Адама Притчарда (Adam Pritchard) [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables) (Шпаргалка по Markdown).</span><span class="sxs-lookup"><span data-stu-id="9a6a0-174">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)</span></span>
- <span data-ttu-id="9a6a0-175">Статья Майкла Фортина (Michel Fortin) [Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) (Расширение Markdown Extra).</span><span class="sxs-lookup"><span data-stu-id="9a6a0-175">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table)</span></span>
- <span data-ttu-id="9a6a0-176">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/) (Преобразование таблиц HTML в Markdown)</span><span class="sxs-lookup"><span data-stu-id="9a6a0-176">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/)</span></span>

### <a name="links"></a><span data-ttu-id="9a6a0-177">Создание ссылок</span><span class="sxs-lookup"><span data-stu-id="9a6a0-177">Links</span></span>

<span data-ttu-id="9a6a0-178">Синтаксис Markdown для встроенной ссылки состоит из части `[link text]`, представляющей текст гиперссылки, и части `(file-name.md)` — URL-адреса или имени файла, на который дается ссылка:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-178">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="9a6a0-179">Дополнительные сведения о ссылках:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-179">For more information on linking, see:</span></span>

- <span data-ttu-id="9a6a0-180">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax#link) (Руководство по синтаксису Markdown), в котором предоставлена основная информация по поддержке ссылок Markdown.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-180">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="9a6a0-181">Страница [Ссылки](how-to-write-links.md) в этом руководстве содержит сведения о дополнительном синтаксисе Markdig для ссылок.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-181">The [Links](how-to-write-links.md) section of this guide for details on additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="9a6a0-182">Фрагменты кода</span><span class="sxs-lookup"><span data-stu-id="9a6a0-182">Code snippets</span></span>

<span data-ttu-id="9a6a0-183">Markdown поддерживает как встраивание фрагментов кода в предложение, так и их размещение между предложениями в виде отдельных огражденных блоков.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-183">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="9a6a0-184">Дополнительная информация:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-184">For details, see:</span></span>

- [<span data-ttu-id="9a6a0-185">Сведения о собственной поддержке блоков кода Markdown</span><span class="sxs-lookup"><span data-stu-id="9a6a0-185">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="9a6a0-186">Сведения о поддержке GFM для ограждения кода и выделения синтаксиса</span><span class="sxs-lookup"><span data-stu-id="9a6a0-186">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="9a6a0-187">Огражденные блоки кода — это простой способ выделить синтаксис для фрагментов кода.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-187">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="9a6a0-188">Общий формат огражденных блоков кода:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-188">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="9a6a0-189">Псевдоним после трех начальных символов обратной галочки \` определяет использование выделения.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-189">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="9a6a0-190">Ниже представлен список часто используемых языков программирования для написания документации и приводятся соответствующие метки.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-190">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="9a6a0-191">Все эти языки поддерживают понятные имена, а большинство из них — выделение языка в имени.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-191">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="9a6a0-192">Имя</span><span class="sxs-lookup"><span data-stu-id="9a6a0-192">Name</span></span>|<span data-ttu-id="9a6a0-193">Метка Markdown</span><span class="sxs-lookup"><span data-stu-id="9a6a0-193">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="9a6a0-194">.NET Console</span><span class="sxs-lookup"><span data-stu-id="9a6a0-194">.NET Console</span></span>|<span data-ttu-id="9a6a0-195">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="9a6a0-195">dotnetcli</span></span>|
|<span data-ttu-id="9a6a0-196">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="9a6a0-196">ASP.NET (C#)</span></span>|<span data-ttu-id="9a6a0-197">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="9a6a0-197">aspx-csharp</span></span>|
|<span data-ttu-id="9a6a0-198">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="9a6a0-198">ASP.NET (VB)</span></span>|<span data-ttu-id="9a6a0-199">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="9a6a0-199">aspx-vb</span></span>|
|<span data-ttu-id="9a6a0-200">AzCopy</span><span class="sxs-lookup"><span data-stu-id="9a6a0-200">AzCopy</span></span>|<span data-ttu-id="9a6a0-201">azcopy</span><span class="sxs-lookup"><span data-stu-id="9a6a0-201">azcopy</span></span>|
|<span data-ttu-id="9a6a0-202">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="9a6a0-202">Azure CLI</span></span>|<span data-ttu-id="9a6a0-203">azurecli</span><span class="sxs-lookup"><span data-stu-id="9a6a0-203">azurecli</span></span>|
|<span data-ttu-id="9a6a0-204">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9a6a0-204">Azure PowerShell</span></span>|<span data-ttu-id="9a6a0-205">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="9a6a0-205">azurepowershell</span></span>|
|<span data-ttu-id="9a6a0-206">C++</span><span class="sxs-lookup"><span data-stu-id="9a6a0-206">C++</span></span>|<span data-ttu-id="9a6a0-207">cpp</span><span class="sxs-lookup"><span data-stu-id="9a6a0-207">cpp</span></span>|
|<span data-ttu-id="9a6a0-208">C++/CX</span><span class="sxs-lookup"><span data-stu-id="9a6a0-208">C++/CX</span></span>|<span data-ttu-id="9a6a0-209">cppcx</span><span class="sxs-lookup"><span data-stu-id="9a6a0-209">cppcx</span></span>|
|<span data-ttu-id="9a6a0-210">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="9a6a0-210">C++/WinRT</span></span>|<span data-ttu-id="9a6a0-211">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="9a6a0-211">cppwinrt</span></span>|
|<span data-ttu-id="9a6a0-212">C#</span><span class="sxs-lookup"><span data-stu-id="9a6a0-212">C#</span></span>|<span data-ttu-id="9a6a0-213">csharp</span><span class="sxs-lookup"><span data-stu-id="9a6a0-213">csharp</span></span>|
|<span data-ttu-id="9a6a0-214">CSHTML</span><span class="sxs-lookup"><span data-stu-id="9a6a0-214">CSHTML</span></span>|<span data-ttu-id="9a6a0-215">cshtml</span><span class="sxs-lookup"><span data-stu-id="9a6a0-215">cshtml</span></span>|
|<span data-ttu-id="9a6a0-216">DAX</span><span class="sxs-lookup"><span data-stu-id="9a6a0-216">DAX</span></span>|<span data-ttu-id="9a6a0-217">dax</span><span class="sxs-lookup"><span data-stu-id="9a6a0-217">dax</span></span>|
|<span data-ttu-id="9a6a0-218">F#</span><span class="sxs-lookup"><span data-stu-id="9a6a0-218">F#</span></span>|<span data-ttu-id="9a6a0-219">fsharp</span><span class="sxs-lookup"><span data-stu-id="9a6a0-219">fsharp</span></span>|
|<span data-ttu-id="9a6a0-220">Go</span><span class="sxs-lookup"><span data-stu-id="9a6a0-220">Go</span></span>|<span data-ttu-id="9a6a0-221">go</span><span class="sxs-lookup"><span data-stu-id="9a6a0-221">go</span></span>|
|<span data-ttu-id="9a6a0-222">HTML</span><span class="sxs-lookup"><span data-stu-id="9a6a0-222">HTML</span></span>|<span data-ttu-id="9a6a0-223">html</span><span class="sxs-lookup"><span data-stu-id="9a6a0-223">html</span></span>|
|<span data-ttu-id="9a6a0-224">HTTP</span><span class="sxs-lookup"><span data-stu-id="9a6a0-224">HTTP</span></span>|<span data-ttu-id="9a6a0-225">http</span><span class="sxs-lookup"><span data-stu-id="9a6a0-225">http</span></span>|
|<span data-ttu-id="9a6a0-226">Java</span><span class="sxs-lookup"><span data-stu-id="9a6a0-226">Java</span></span>|<span data-ttu-id="9a6a0-227">java</span><span class="sxs-lookup"><span data-stu-id="9a6a0-227">java</span></span>|
|<span data-ttu-id="9a6a0-228">JavaScript</span><span class="sxs-lookup"><span data-stu-id="9a6a0-228">JavaScript</span></span>|<span data-ttu-id="9a6a0-229">javascript</span><span class="sxs-lookup"><span data-stu-id="9a6a0-229">javascript</span></span>|
|<span data-ttu-id="9a6a0-230">JSON</span><span class="sxs-lookup"><span data-stu-id="9a6a0-230">JSON</span></span>|<span data-ttu-id="9a6a0-231">json</span><span class="sxs-lookup"><span data-stu-id="9a6a0-231">json</span></span>|
|<span data-ttu-id="9a6a0-232">Markdown</span><span class="sxs-lookup"><span data-stu-id="9a6a0-232">Markdown</span></span>|<span data-ttu-id="9a6a0-233">md</span><span class="sxs-lookup"><span data-stu-id="9a6a0-233">md</span></span>|
|<span data-ttu-id="9a6a0-234">NodeJS</span><span class="sxs-lookup"><span data-stu-id="9a6a0-234">NodeJS</span></span>|<span data-ttu-id="9a6a0-235">nodejs</span><span class="sxs-lookup"><span data-stu-id="9a6a0-235">nodejs</span></span>|
|<span data-ttu-id="9a6a0-236">Objective-C</span><span class="sxs-lookup"><span data-stu-id="9a6a0-236">Objective-C</span></span>|<span data-ttu-id="9a6a0-237">objc</span><span class="sxs-lookup"><span data-stu-id="9a6a0-237">objc</span></span>|
|<span data-ttu-id="9a6a0-238">OData</span><span class="sxs-lookup"><span data-stu-id="9a6a0-238">OData</span></span>|<span data-ttu-id="9a6a0-239">odata</span><span class="sxs-lookup"><span data-stu-id="9a6a0-239">odata</span></span>|
|<span data-ttu-id="9a6a0-240">PHP</span><span class="sxs-lookup"><span data-stu-id="9a6a0-240">PHP</span></span>|<span data-ttu-id="9a6a0-241">php</span><span class="sxs-lookup"><span data-stu-id="9a6a0-241">php</span></span>|
|<span data-ttu-id="9a6a0-242">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="9a6a0-242">Power Apps Formula</span></span>|<span data-ttu-id="9a6a0-243">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="9a6a0-243">powerappsfl</span></span>|
|<span data-ttu-id="9a6a0-244">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9a6a0-244">PowerShell</span></span>|<span data-ttu-id="9a6a0-245">powershell</span><span class="sxs-lookup"><span data-stu-id="9a6a0-245">powershell</span></span>|
|<span data-ttu-id="9a6a0-246">Python</span><span class="sxs-lookup"><span data-stu-id="9a6a0-246">Python</span></span>|<span data-ttu-id="9a6a0-247">python</span><span class="sxs-lookup"><span data-stu-id="9a6a0-247">python</span></span>|
|<span data-ttu-id="9a6a0-248">Q#</span><span class="sxs-lookup"><span data-stu-id="9a6a0-248">Q#</span></span>|<span data-ttu-id="9a6a0-249">qsharp</span><span class="sxs-lookup"><span data-stu-id="9a6a0-249">qsharp</span></span>|
|<span data-ttu-id="9a6a0-250">Ruby</span><span class="sxs-lookup"><span data-stu-id="9a6a0-250">Ruby</span></span>|<span data-ttu-id="9a6a0-251">ruby</span><span class="sxs-lookup"><span data-stu-id="9a6a0-251">ruby</span></span>|
|<span data-ttu-id="9a6a0-252">SQL</span><span class="sxs-lookup"><span data-stu-id="9a6a0-252">SQL</span></span>|<span data-ttu-id="9a6a0-253">sql</span><span class="sxs-lookup"><span data-stu-id="9a6a0-253">sql</span></span>|
|<span data-ttu-id="9a6a0-254">Swift</span><span class="sxs-lookup"><span data-stu-id="9a6a0-254">Swift</span></span>|<span data-ttu-id="9a6a0-255">swift</span><span class="sxs-lookup"><span data-stu-id="9a6a0-255">swift</span></span>|
|<span data-ttu-id="9a6a0-256">TypeScript</span><span class="sxs-lookup"><span data-stu-id="9a6a0-256">TypeScript</span></span>|<span data-ttu-id="9a6a0-257">typescript</span><span class="sxs-lookup"><span data-stu-id="9a6a0-257">typescript</span></span>|
|<span data-ttu-id="9a6a0-258">VB</span><span class="sxs-lookup"><span data-stu-id="9a6a0-258">VB</span></span>|<span data-ttu-id="9a6a0-259">vb</span><span class="sxs-lookup"><span data-stu-id="9a6a0-259">vb</span></span>|
|<span data-ttu-id="9a6a0-260">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="9a6a0-260">VSTS CLI</span></span>|<span data-ttu-id="9a6a0-261">vstscli</span><span class="sxs-lookup"><span data-stu-id="9a6a0-261">vstscli</span></span>|
|<span data-ttu-id="9a6a0-262">XAML</span><span class="sxs-lookup"><span data-stu-id="9a6a0-262">XAML</span></span>|<span data-ttu-id="9a6a0-263">xaml</span><span class="sxs-lookup"><span data-stu-id="9a6a0-263">xaml</span></span>|
|<span data-ttu-id="9a6a0-264">XML</span><span class="sxs-lookup"><span data-stu-id="9a6a0-264">XML</span></span>|<span data-ttu-id="9a6a0-265">xml</span><span class="sxs-lookup"><span data-stu-id="9a6a0-265">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="9a6a0-266">Пример: C\#</span><span class="sxs-lookup"><span data-stu-id="9a6a0-266">Example: C\#</span></span>

<span data-ttu-id="9a6a0-267">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="9a6a0-267">__Markdown__</span></span>

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

<span data-ttu-id="9a6a0-268">__Отображение__</span><span class="sxs-lookup"><span data-stu-id="9a6a0-268">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="9a6a0-269">Пример: SQL</span><span class="sxs-lookup"><span data-stu-id="9a6a0-269">Example: SQL</span></span>

<span data-ttu-id="9a6a0-270">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="9a6a0-270">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="9a6a0-271">__Отображение__</span><span class="sxs-lookup"><span data-stu-id="9a6a0-271">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="9a6a0-272">Настраиваемые расширения OPS для Markdown</span><span class="sxs-lookup"><span data-stu-id="9a6a0-272">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="9a6a0-273">Службы Open Publishing Services (OPS) используют Markdig, синтаксический анализатор Markdown, обеспечивающий высокую совместимость с диалектом GitHub Flavored Markdown (GFM).</span><span class="sxs-lookup"><span data-stu-id="9a6a0-273">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="9a6a0-274">Markdig добавляет дополнительные функции за счет расширений Markdown.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-274">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="9a6a0-275">Поэтому для справки мы включили в этот материал некоторые разделы из руководства по разработке OPS.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-275">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="9a6a0-276">(Например, см. в содержании разделы "Markdig и расширения Markdown" и "Фрагменты кода".)</span><span class="sxs-lookup"><span data-stu-id="9a6a0-276">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="9a6a0-277">В статьях документации для общего форматирования, например для создания абзацев, ссылок, списков и заголовков, используется GFM.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-277">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="9a6a0-278">Для расширенного форматирования в статьях можно использовать следующие функции Markdig:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-278">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="9a6a0-279">Блоки заметок</span><span class="sxs-lookup"><span data-stu-id="9a6a0-279">Note blocks</span></span>
- <span data-ttu-id="9a6a0-280">включаемые файлы;</span><span class="sxs-lookup"><span data-stu-id="9a6a0-280">Includes</span></span>
- <span data-ttu-id="9a6a0-281">селекторы;</span><span class="sxs-lookup"><span data-stu-id="9a6a0-281">Selectors</span></span>
- <span data-ttu-id="9a6a0-282">внедренные видео;</span><span class="sxs-lookup"><span data-stu-id="9a6a0-282">Embedded videos</span></span>
- <span data-ttu-id="9a6a0-283">фрагменты или примеры кода.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-283">Code snippets/samples</span></span>

<span data-ttu-id="9a6a0-284">Полный список см. в разделах "Markdig и расширения Markdown" и "Фрагменты кода".</span><span class="sxs-lookup"><span data-stu-id="9a6a0-284">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="9a6a0-285">Блоки заметок</span><span class="sxs-lookup"><span data-stu-id="9a6a0-285">Note blocks</span></span>

<span data-ttu-id="9a6a0-286">Есть четыре типа блоков заметок, которые позволяют привлечь внимание к определенному содержимому:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-286">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="9a6a0-287">ПРИМЕЧАНИЕ;</span><span class="sxs-lookup"><span data-stu-id="9a6a0-287">NOTE</span></span>
- <span data-ttu-id="9a6a0-288">ПРЕДУПРЕЖДЕНИЕ;</span><span class="sxs-lookup"><span data-stu-id="9a6a0-288">WARNING</span></span>
- <span data-ttu-id="9a6a0-289">СОВЕТ;</span><span class="sxs-lookup"><span data-stu-id="9a6a0-289">TIP</span></span>
- <span data-ttu-id="9a6a0-290">ВАЖНО.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-290">IMPORTANT</span></span>

<span data-ttu-id="9a6a0-291">В целом не следует часто использовать блоки заметок, так как они могут отвлекать пользователя от основного содержимого.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-291">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="9a6a0-292">Хотя эти элементы также поддерживают блоки кода, изображения, списки и ссылки, лучше не перегружать их, делая простыми и понятными.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-292">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="9a6a0-293">Включаемые файлы</span><span class="sxs-lookup"><span data-stu-id="9a6a0-293">Includes</span></span>

<span data-ttu-id="9a6a0-294">Если вы хотите добавить в файлы статей многократно используемые изображения или текст, воспользуйтесь доступной в Markdig функцией включения ("include") файлов по ссылке.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-294">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="9a6a0-295">Функция указывает OPS включить файл в файл статьи во время сборки, чтобы он стал частью опубликованной статьи.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-295">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="9a6a0-296">Существует три типа включаемых файлов для многократного использования содержимого:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-296">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="9a6a0-297">Встроенные — для многократного использования фрагмента стандартного текста путем его встраивания в другое предложение.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-297">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="9a6a0-298">Блочные — для многократного использования всего файла Markdown в качестве блока путем его вложения в раздел или статью.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-298">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="9a6a0-299">Изображения — позволяют включать стандартное изображение в документацию.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-299">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="9a6a0-300">Встроенные и блочные включаемые файлы — это простые файлы Markdown с расширением .md.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-300">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="9a6a0-301">Они могут содержать любую допустимую разметку Markdown.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-301">It can contain any valid Markdown.</span></span> <span data-ttu-id="9a6a0-302">Все включаемые файлы Markdown должны быть помещены в [общий подкаталог `/includes`](git-github-fundamentals.md#includes-subdirectory) в корневом каталоге репозитория.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-302">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="9a6a0-303">Когда статья публикуется, включаемый файл легко интегрируется в нее.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-303">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="9a6a0-304">Далее приведены требования по работе с включаемыми файлами.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-304">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="9a6a0-305">Используйте включаемые файлы, если вам нужно, чтобы один и тот же текст отображался в нескольких статьях.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-305">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="9a6a0-306">Блочные включаемые файлы предназначены для значительных объемов текста: один или два абзаца, общая процедура или общий раздел.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-306">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="9a6a0-307">Не используйте их для фрагментов текста меньше одного предложения.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-307">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="9a6a0-308">Включаемые файлы не будут отображаться в представлении статьи на GitHub, так как они работают только с Markdig-расширениями.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-308">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="9a6a0-309">Они отображаются только после публикации.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-309">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="9a6a0-310">Весь текст во включаемом файле должен состоять из полноценных предложений или фраз, не зависящих от остального текста статьи, в которую добавляется ссылка на такой файл.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-310">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="9a6a0-311">Если не следовать этой инструкции, в статье создаются непереводимые строки, которые нарушают процесс локализации.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-311">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="9a6a0-312">Не внедряйте одни включаемые файлы в другие.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-312">Don't embed includes within other includes.</span></span> <span data-ttu-id="9a6a0-313">Такая возможность не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-313">They are not supported.</span></span>
- <span data-ttu-id="9a6a0-314">Файлы мультимедиа должны быть помещены в отдельную папку мультимедиа в подкаталоге включаемых файлов. Например, `<repo>`/включаемые файлы/папка мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-314">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="9a6a0-315">В корне каталога мультимедиа не должны содержаться изображения.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-315">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="9a6a0-316">Если во включаемом файле нет изображений, соответствующий каталог мультимедиа не требуется.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-316">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="9a6a0-317">Как и в обычных статьях, не используйте общий файл мультимедиа для включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-317">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="9a6a0-318">Для каждого включаемого файла в статье должен быть создан отдельный файл мультимедиа с уникальным именем.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-318">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="9a6a0-319">Файл мультимедиа должен храниться в папке мультимедиа, связанной с включаемым файлом.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-319">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="9a6a0-320">Не используйте включаемый файл как единственное содержимое статьи.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-320">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="9a6a0-321">Включаемые файлы предназначены для дополнения основных материалов статьи.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-321">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="9a6a0-322">Селекторы</span><span class="sxs-lookup"><span data-stu-id="9a6a0-322">Selectors</span></span>

<span data-ttu-id="9a6a0-323">В технических статьях селекторы применяются для создания разных вариантов содержимого, чтобы проиллюстрировать различия в реализации, связанные с использованием нескольких технологий или платформ.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-323">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="9a6a0-324">Это в особенности применимо к материалам о мобильных платформах для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-324">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="9a6a0-325">Сейчас в Markdig есть два типа селекторов: для единичного и множественного выбора.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-325">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="9a6a0-326">В каждой статье с возможностью выбора используется одна и та же разметка Markdown для селектора. Поэтому рекомендуется поместить селектор для статьи во включаемый файл.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-326">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="9a6a0-327">Затем нужно добавить ссылки на этот файл во все статьи, для которых используется селектор.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-327">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="9a6a0-328">Фрагменты кода</span><span class="sxs-lookup"><span data-stu-id="9a6a0-328">Code snippets</span></span>

<span data-ttu-id="9a6a0-329">В Markdig есть расширение с расширенными функциями для включения в статью фрагментов кода.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-329">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="9a6a0-330">Этот формат обеспечивает расширенный рендеринг на основе функций GFM, таких как выбор языка программирования и раскраска синтаксиса, а также другие полезные функции, например:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-330">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="9a6a0-331">включение централизованных примеров или фрагментов кода из внешнего репозитория;</span><span class="sxs-lookup"><span data-stu-id="9a6a0-331">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="9a6a0-332">пользовательский интерфейс с вкладками для отображения нескольких версий примеров кода на разных языках.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-332">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="9a6a0-333">Сбои и устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="9a6a0-333">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="9a6a0-334">Замещающий текст</span><span class="sxs-lookup"><span data-stu-id="9a6a0-334">Alt text</span></span>

<span data-ttu-id="9a6a0-335">Замещающий текст, который содержит символы подчеркивания, отображается некорректно.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-335">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="9a6a0-336">Например, вместо</span><span class="sxs-lookup"><span data-stu-id="9a6a0-336">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="9a6a0-337">используйте следующий вариант, позволяющий избежать символов подчеркивания:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-337">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="9a6a0-338">Апострофы и кавычки</span><span class="sxs-lookup"><span data-stu-id="9a6a0-338">Apostrophes and quotation marks</span></span>

<span data-ttu-id="9a6a0-339">Если вы копируете текст из Word в редактор Markdown, он может содержать книжные (изогнутые) апострофы или кавычки.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-339">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="9a6a0-340">Их нужно заменить кодом или обычными апострофами или кавычками.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-340">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="9a6a0-341">В противном случае после публикации файла может отобразиться нечитаемый текст, например Itâ€™s.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-341">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="9a6a0-342">Ниже приведены кодировки для этих знаков пунктуации:</span><span class="sxs-lookup"><span data-stu-id="9a6a0-342">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="9a6a0-343">левая (открывающая) кавычка: `&#8220;`;</span><span class="sxs-lookup"><span data-stu-id="9a6a0-343">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="9a6a0-344">правая (закрывающая) кавычка: `&#8221;`;</span><span class="sxs-lookup"><span data-stu-id="9a6a0-344">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="9a6a0-345">правая закрывающая одинарная кавычка или апостроф: `&#8217;`;</span><span class="sxs-lookup"><span data-stu-id="9a6a0-345">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="9a6a0-346">левая открывающая одинарная кавычка (используется редко): `&#8216;`.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-346">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="9a6a0-347">Угловые скобки</span><span class="sxs-lookup"><span data-stu-id="9a6a0-347">Angle brackets</span></span>

<span data-ttu-id="9a6a0-348">Если в тексте файла (не в коде) используются угловые скобки (например, для обозначения заполнителя), их нужно кодировать вручную.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-348">If you use angle brackets in text (not code) in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="9a6a0-349">Иначе Markdown распознает их как часть тега HTML.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-349">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="9a6a0-350">Например, `<script name>` следует закодировать как `&lt;script name&gt;`.</span><span class="sxs-lookup"><span data-stu-id="9a6a0-350">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="9a6a0-351">Дополнительные материалы</span><span class="sxs-lookup"><span data-stu-id="9a6a0-351">See also</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="9a6a0-352">Ресурсы Markdown</span><span class="sxs-lookup"><span data-stu-id="9a6a0-352">Markdown resources</span></span>

- <span data-ttu-id="9a6a0-353">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax) (Синтаксис Markdown)</span><span class="sxs-lookup"><span data-stu-id="9a6a0-353">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- <span data-ttu-id="9a6a0-354">[Markdown cheat-sheet](./media/documents/markdown-cheatsheet.pdf?raw=true) (Шпаргалка по Markdown)</span><span class="sxs-lookup"><span data-stu-id="9a6a0-354">[Docs Markdown cheat sheet](./media/documents/markdown-cheatsheet.pdf?raw=true)</span></span>
- [<span data-ttu-id="9a6a0-355">Базовые сведения о разметке Markdown на GitHub</span><span class="sxs-lookup"><span data-stu-id="9a6a0-355">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
