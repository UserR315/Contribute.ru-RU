---
title: Использование языка разметки Markdown для написания документации
description: В этой статье приводятся базовые и справочные сведения о языке разметки Markdown, используемом для написания статей на сайте docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/26/2019
ms.openlocfilehash: 086972acaef9647709fbe43f07c07abde71c7d9f
ms.sourcegitcommit: fd92198ec2d0ce2d6687b6f1521a82b3fefc60e0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/16/2020
ms.locfileid: "76111073"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="0de3d-103">Использование языка разметки Markdown для написания документации</span><span class="sxs-lookup"><span data-stu-id="0de3d-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="0de3d-104">Статьи на сайте [docs.microsoft.com](https://docs.microsoft.com) написаны на [Markdown](https://daringfireball.net/projects/markdown/) — упрощенном языке разметки, который легко использовать и изучать.</span><span class="sxs-lookup"><span data-stu-id="0de3d-104">[Docs.microsoft.com](https://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="0de3d-105">Благодаря своей простоте он быстро становится отраслевым стандартом.</span><span class="sxs-lookup"><span data-stu-id="0de3d-105">Because of this, it has quickly become an industry standard.</span></span> <span data-ttu-id="0de3d-106">Для документов сайта используется [тип Markdig](#markdown-flavor) разметки Markdown.</span><span class="sxs-lookup"><span data-stu-id="0de3d-106">The docs site uses the [Markdig flavor](#markdown-flavor) of Markdown.</span></span>


## <a name="markdown-basics"></a><span data-ttu-id="0de3d-107">Базовые сведения о Markdown</span><span class="sxs-lookup"><span data-stu-id="0de3d-107">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="0de3d-108">Заголовки</span><span class="sxs-lookup"><span data-stu-id="0de3d-108">Headings</span></span>

<span data-ttu-id="0de3d-109">Чтобы создать заголовок, используйте знак (#), например:</span><span class="sxs-lookup"><span data-stu-id="0de3d-109">To create a heading, you use a hash mark (#), as follows:</span></span>

```md
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="0de3d-110">В заголовках следует использовать стиль atx, то есть 1–6 символов решетки (#) в начале строки, чтобы указать на заголовок, соответствующий заголовкам HTML уровней с H1 по H6.</span><span class="sxs-lookup"><span data-stu-id="0de3d-110">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="0de3d-111">Сверху приводятся примеры заголовков с первого по четвертый уровень.</span><span class="sxs-lookup"><span data-stu-id="0de3d-111">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="0de3d-112">В статье **должен** быть только один заголовок первого уровня (H1), который будет отображаться как заголовок страницы.</span><span class="sxs-lookup"><span data-stu-id="0de3d-112">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="0de3d-113">Если заголовок заканчивается на символ `#`, добавьте в конце еще символ `#`, чтобы заголовок отображался правильно.</span><span class="sxs-lookup"><span data-stu-id="0de3d-113">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="0de3d-114">Например, `# Async Programming in F# #`.</span><span class="sxs-lookup"><span data-stu-id="0de3d-114">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="0de3d-115">Заголовки второго уровня создадут оглавление, которое будет отображаться в разделе "В этой статье" под заголовком статьи.</span><span class="sxs-lookup"><span data-stu-id="0de3d-115">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="0de3d-116">Полужирное и курсивное начертания</span><span class="sxs-lookup"><span data-stu-id="0de3d-116">Bold and italic text</span></span>

<span data-ttu-id="0de3d-117">Чтобы задать для текста **полужирное начертание**, заключите его в двойные звездочки:</span><span class="sxs-lookup"><span data-stu-id="0de3d-117">To format text as **bold**, you enclose it in two asterisks:</span></span>

```md
This text is **bold**.
```

<span data-ttu-id="0de3d-118">Чтобы задать для текста *курсивное начертание*, заключите его в одинарные звездочки:</span><span class="sxs-lookup"><span data-stu-id="0de3d-118">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```md
This text is *italic*.
```

<span data-ttu-id="0de3d-119">Чтобы задать для текста ***полужирное и курсивное*** начертание, заключите его в тройные звездочки:</span><span class="sxs-lookup"><span data-stu-id="0de3d-119">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```md
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="0de3d-120">Блоки цитирования</span><span class="sxs-lookup"><span data-stu-id="0de3d-120">Blockquotes</span></span>

<span data-ttu-id="0de3d-121">Блоки цитирования создаются с помощью символа `>`:</span><span class="sxs-lookup"><span data-stu-id="0de3d-121">Blockquotes are created using the `>` character:</span></span>

```md
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="0de3d-122">Предыдущий пример отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0de3d-122">The preceding example renders as follows:</span></span>

> <span data-ttu-id="0de3d-123">Засуха продолжалась десять миллионов лет, и царству ужасных ящеров уже давно пришел конец.</span><span class="sxs-lookup"><span data-stu-id="0de3d-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="0de3d-124">Здесь, близ экватора, на материке, который позднее назовут Африкой, с новой яростью вспыхнула борьба за существование, и еще не ясно было, кто выйдет из нее победителем.</span><span class="sxs-lookup"><span data-stu-id="0de3d-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="0de3d-125">На этой бесплодной, иссушенной зноем земле благоденствовать или хотя бы просто выжить могли только маленькие, или ловкие, или свирепые.</span><span class="sxs-lookup"><span data-stu-id="0de3d-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="0de3d-126">Списки</span><span class="sxs-lookup"><span data-stu-id="0de3d-126">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="0de3d-127">Неупорядоченный список</span><span class="sxs-lookup"><span data-stu-id="0de3d-127">Unordered list</span></span>

<span data-ttu-id="0de3d-128">Неупорядоченный (маркированный) список можно отформатировать с помощью звездочек или тире.</span><span class="sxs-lookup"><span data-stu-id="0de3d-128">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="0de3d-129">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="0de3d-129">For example, the following Markdown:</span></span>

```md
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="0de3d-130">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="0de3d-130">will be rendered as:</span></span>

- <span data-ttu-id="0de3d-131">List item 1</span><span class="sxs-lookup"><span data-stu-id="0de3d-131">List item 1</span></span>
- <span data-ttu-id="0de3d-132">List item 2</span><span class="sxs-lookup"><span data-stu-id="0de3d-132">List item 2</span></span>
- <span data-ttu-id="0de3d-133">List item 3</span><span class="sxs-lookup"><span data-stu-id="0de3d-133">List item 3</span></span>

<span data-ttu-id="0de3d-134">Чтобы вложить один список в другой, добавьте отступ для элементов дочернего списка.</span><span class="sxs-lookup"><span data-stu-id="0de3d-134">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="0de3d-135">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="0de3d-135">For example, the following Markdown:</span></span>

```md
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="0de3d-136">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="0de3d-136">will be rendered as:</span></span>

- <span data-ttu-id="0de3d-137">List item 1</span><span class="sxs-lookup"><span data-stu-id="0de3d-137">List item 1</span></span>
  - <span data-ttu-id="0de3d-138">List item A</span><span class="sxs-lookup"><span data-stu-id="0de3d-138">List item A</span></span>
  - <span data-ttu-id="0de3d-139">List item B</span><span class="sxs-lookup"><span data-stu-id="0de3d-139">List item B</span></span>
- <span data-ttu-id="0de3d-140">List item 2</span><span class="sxs-lookup"><span data-stu-id="0de3d-140">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="0de3d-141">Упорядоченный список</span><span class="sxs-lookup"><span data-stu-id="0de3d-141">Ordered list</span></span>

<span data-ttu-id="0de3d-142">Упорядоченный (ступенчатый) список можно отформатировать с помощью соответствующих цифр.</span><span class="sxs-lookup"><span data-stu-id="0de3d-142">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="0de3d-143">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="0de3d-143">For example, the following Markdown:</span></span>

```md
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="0de3d-144">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="0de3d-144">will be rendered as:</span></span>

1. <span data-ttu-id="0de3d-145">First instruction</span><span class="sxs-lookup"><span data-stu-id="0de3d-145">First instruction</span></span>
2. <span data-ttu-id="0de3d-146">Second instruction</span><span class="sxs-lookup"><span data-stu-id="0de3d-146">Second instruction</span></span>
3. <span data-ttu-id="0de3d-147">Third instruction</span><span class="sxs-lookup"><span data-stu-id="0de3d-147">Third instruction</span></span>

<span data-ttu-id="0de3d-148">Чтобы вложить один список в другой, добавьте отступ для элементов дочернего списка.</span><span class="sxs-lookup"><span data-stu-id="0de3d-148">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="0de3d-149">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="0de3d-149">For example, the following Markdown:</span></span>

```md
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="0de3d-150">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="0de3d-150">will be rendered as:</span></span>

1. <span data-ttu-id="0de3d-151">First instruction</span><span class="sxs-lookup"><span data-stu-id="0de3d-151">First instruction</span></span>
   1. <span data-ttu-id="0de3d-152">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="0de3d-152">Sub-instruction</span></span>
   2. <span data-ttu-id="0de3d-153">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="0de3d-153">Sub-instruction</span></span>
2. <span data-ttu-id="0de3d-154">Second instruction</span><span class="sxs-lookup"><span data-stu-id="0de3d-154">Second instruction</span></span>

<span data-ttu-id="0de3d-155">Обратите внимание, что мы используем "1."</span><span class="sxs-lookup"><span data-stu-id="0de3d-155">Note that we use '1.'</span></span> <span data-ttu-id="0de3d-156">для всех записей.</span><span class="sxs-lookup"><span data-stu-id="0de3d-156">for all entries.</span></span> <span data-ttu-id="0de3d-157">Так проще увидеть различия, когда потом будут добавлены новые шаги или удалены существующие.</span><span class="sxs-lookup"><span data-stu-id="0de3d-157">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="0de3d-158">Tables</span><span class="sxs-lookup"><span data-stu-id="0de3d-158">Tables</span></span>

<span data-ttu-id="0de3d-159">Таблицы не входят в основную спецификацию Markdown, но они поддерживаются в GFM.</span><span class="sxs-lookup"><span data-stu-id="0de3d-159">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="0de3d-160">Создавать таблицы можно с помощью символов вертикальной черты (|) и дефиса (-).</span><span class="sxs-lookup"><span data-stu-id="0de3d-160">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="0de3d-161">Дефисы позволяют создавать для каждого столбца заголовок. Вертикальные черты разделяют столбцы.</span><span class="sxs-lookup"><span data-stu-id="0de3d-161">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="0de3d-162">Чтобы таблица правильно отображалась, включите перед ней пустую строку.</span><span class="sxs-lookup"><span data-stu-id="0de3d-162">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="0de3d-163">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="0de3d-163">For example, the following Markdown:</span></span>

```md
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="0de3d-164">Она будет отображаться так:</span><span class="sxs-lookup"><span data-stu-id="0de3d-164">Will be rendered as:</span></span>

| <span data-ttu-id="0de3d-165">Fun</span><span class="sxs-lookup"><span data-stu-id="0de3d-165">Fun</span></span>                  | <span data-ttu-id="0de3d-166">with</span><span class="sxs-lookup"><span data-stu-id="0de3d-166">With</span></span>                 | <span data-ttu-id="0de3d-167">Tables</span><span class="sxs-lookup"><span data-stu-id="0de3d-167">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="0de3d-168">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="0de3d-168">left-aligned column</span></span>  | <span data-ttu-id="0de3d-169">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="0de3d-169">right-aligned column</span></span> | <span data-ttu-id="0de3d-170">centered column</span><span class="sxs-lookup"><span data-stu-id="0de3d-170">centered column</span></span> |
| <span data-ttu-id="0de3d-171">$100</span><span class="sxs-lookup"><span data-stu-id="0de3d-171">$100</span></span>                 | <span data-ttu-id="0de3d-172">$100</span><span class="sxs-lookup"><span data-stu-id="0de3d-172">$100</span></span>                 | <span data-ttu-id="0de3d-173">$100</span><span class="sxs-lookup"><span data-stu-id="0de3d-173">$100</span></span>            |
| <span data-ttu-id="0de3d-174">$10</span><span class="sxs-lookup"><span data-stu-id="0de3d-174">$10</span></span>                  | <span data-ttu-id="0de3d-175">$10</span><span class="sxs-lookup"><span data-stu-id="0de3d-175">$10</span></span>                  | <span data-ttu-id="0de3d-176">$10</span><span class="sxs-lookup"><span data-stu-id="0de3d-176">$10</span></span>             |
| <span data-ttu-id="0de3d-177">$1</span><span class="sxs-lookup"><span data-stu-id="0de3d-177">$1</span></span>                   | <span data-ttu-id="0de3d-178">$1</span><span class="sxs-lookup"><span data-stu-id="0de3d-178">$1</span></span>                   | <span data-ttu-id="0de3d-179">$1</span><span class="sxs-lookup"><span data-stu-id="0de3d-179">$1</span></span>              |

<span data-ttu-id="0de3d-180">Дополнительные сведения о создании таблиц:</span><span class="sxs-lookup"><span data-stu-id="0de3d-180">For more information on creating tables, see:</span></span>

- <span data-ttu-id="0de3d-181">Статья на сайте GitHub [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/) (Организация информации с помощью таблиц).</span><span class="sxs-lookup"><span data-stu-id="0de3d-181">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="0de3d-182">Веб-приложение [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="0de3d-182">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="0de3d-183">Статья Адама Притчарда (Adam Pritchard) [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables) (Шпаргалка по Markdown).</span><span class="sxs-lookup"><span data-stu-id="0de3d-183">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="0de3d-184">Статья Майкла Фортина (Michel Fortin) [Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) (Расширение Markdown Extra).</span><span class="sxs-lookup"><span data-stu-id="0de3d-184">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="0de3d-185">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/) (Преобразование таблиц HTML в Markdown).</span><span class="sxs-lookup"><span data-stu-id="0de3d-185">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="0de3d-186">Создание ссылок</span><span class="sxs-lookup"><span data-stu-id="0de3d-186">Links</span></span>

<span data-ttu-id="0de3d-187">Синтаксис Markdown для встроенной ссылки состоит из части `[link text]`, представляющей текст гиперссылки, и части `(file-name.md)` — URL-адреса или имени файла, на который дается ссылка:</span><span class="sxs-lookup"><span data-stu-id="0de3d-187">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="0de3d-188">Дополнительные сведения о ссылках:</span><span class="sxs-lookup"><span data-stu-id="0de3d-188">For more information on linking, see:</span></span>

- <span data-ttu-id="0de3d-189">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax#link) (Руководство по синтаксису Markdown), в котором предоставлена основная информация по поддержке ссылок Markdown.</span><span class="sxs-lookup"><span data-stu-id="0de3d-189">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="0de3d-190">Страница [Ссылки](how-to-write-links.md) в этом руководстве содержит сведения о дополнительном синтаксисе Markdig для ссылок.</span><span class="sxs-lookup"><span data-stu-id="0de3d-190">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="0de3d-191">Фрагменты кода</span><span class="sxs-lookup"><span data-stu-id="0de3d-191">Code snippets</span></span>

<span data-ttu-id="0de3d-192">Markdown поддерживает как встраивание фрагментов кода в предложение, так и их размещение между предложениями в виде отдельных огражденных блоков.</span><span class="sxs-lookup"><span data-stu-id="0de3d-192">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="0de3d-193">Дополнительная информация:</span><span class="sxs-lookup"><span data-stu-id="0de3d-193">For details, see:</span></span>

- [<span data-ttu-id="0de3d-194">Сведения о собственной поддержке блоков кода Markdown</span><span class="sxs-lookup"><span data-stu-id="0de3d-194">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="0de3d-195">Сведения о поддержке GFM для ограждения кода и выделения синтаксиса</span><span class="sxs-lookup"><span data-stu-id="0de3d-195">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="0de3d-196">Огражденные блоки кода — это простой способ выделить синтаксис для фрагментов кода.</span><span class="sxs-lookup"><span data-stu-id="0de3d-196">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="0de3d-197">Общий формат огражденных блоков кода:</span><span class="sxs-lookup"><span data-stu-id="0de3d-197">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="0de3d-198">Псевдоним после трех начальных символов обратного апострофа (\`) определяет использование выделения синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="0de3d-198">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="0de3d-199">Ниже представлен список часто используемых языков программирования для написания документации и приводятся соответствующие метки.</span><span class="sxs-lookup"><span data-stu-id="0de3d-199">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="0de3d-200">Все эти языки поддерживают понятные имена, а большинство из них — выделение языка в имени.</span><span class="sxs-lookup"><span data-stu-id="0de3d-200">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="0de3d-201">Имя</span><span class="sxs-lookup"><span data-stu-id="0de3d-201">Name</span></span>|<span data-ttu-id="0de3d-202">Метка Markdown</span><span class="sxs-lookup"><span data-stu-id="0de3d-202">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="0de3d-203">.NET Console</span><span class="sxs-lookup"><span data-stu-id="0de3d-203">.NET Console</span></span>|<span data-ttu-id="0de3d-204">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="0de3d-204">dotnetcli</span></span>|
|<span data-ttu-id="0de3d-205">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="0de3d-205">ASP.NET (C#)</span></span>|<span data-ttu-id="0de3d-206">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="0de3d-206">aspx-csharp</span></span>|
|<span data-ttu-id="0de3d-207">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="0de3d-207">ASP.NET (VB)</span></span>|<span data-ttu-id="0de3d-208">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="0de3d-208">aspx-vb</span></span>|
|<span data-ttu-id="0de3d-209">AzCopy</span><span class="sxs-lookup"><span data-stu-id="0de3d-209">AzCopy</span></span>|<span data-ttu-id="0de3d-210">azcopy</span><span class="sxs-lookup"><span data-stu-id="0de3d-210">azcopy</span></span>|
|<span data-ttu-id="0de3d-211">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="0de3d-211">Azure CLI</span></span>|<span data-ttu-id="0de3d-212">azurecli</span><span class="sxs-lookup"><span data-stu-id="0de3d-212">azurecli</span></span>|
|<span data-ttu-id="0de3d-213">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0de3d-213">Azure PowerShell</span></span>|<span data-ttu-id="0de3d-214">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="0de3d-214">azurepowershell</span></span>|
|<span data-ttu-id="0de3d-215">Bash</span><span class="sxs-lookup"><span data-stu-id="0de3d-215">Bash</span></span>|<span data-ttu-id="0de3d-216">Bash</span><span class="sxs-lookup"><span data-stu-id="0de3d-216">bash</span></span>|
|<span data-ttu-id="0de3d-217">C++</span><span class="sxs-lookup"><span data-stu-id="0de3d-217">C++</span></span>|<span data-ttu-id="0de3d-218">cpp</span><span class="sxs-lookup"><span data-stu-id="0de3d-218">cpp</span></span>|
|<span data-ttu-id="0de3d-219">C++/CX</span><span class="sxs-lookup"><span data-stu-id="0de3d-219">C++/CX</span></span>|<span data-ttu-id="0de3d-220">cppcx</span><span class="sxs-lookup"><span data-stu-id="0de3d-220">cppcx</span></span>|
|<span data-ttu-id="0de3d-221">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="0de3d-221">C++/WinRT</span></span>|<span data-ttu-id="0de3d-222">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="0de3d-222">cppwinrt</span></span>|
|<span data-ttu-id="0de3d-223">C#</span><span class="sxs-lookup"><span data-stu-id="0de3d-223">C#</span></span>|<span data-ttu-id="0de3d-224">csharp</span><span class="sxs-lookup"><span data-stu-id="0de3d-224">csharp</span></span>|
|<span data-ttu-id="0de3d-225">C# в браузере</span><span class="sxs-lookup"><span data-stu-id="0de3d-225">C# in browser</span></span>|<span data-ttu-id="0de3d-226">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="0de3d-226">csharp-interactive</span></span>|
|<span data-ttu-id="0de3d-227">Консоль</span><span class="sxs-lookup"><span data-stu-id="0de3d-227">Console</span></span>|<span data-ttu-id="0de3d-228">консоль</span><span class="sxs-lookup"><span data-stu-id="0de3d-228">console</span></span>|
|<span data-ttu-id="0de3d-229">CSHTML</span><span class="sxs-lookup"><span data-stu-id="0de3d-229">CSHTML</span></span>|<span data-ttu-id="0de3d-230">cshtml</span><span class="sxs-lookup"><span data-stu-id="0de3d-230">cshtml</span></span>|
|<span data-ttu-id="0de3d-231">DAX</span><span class="sxs-lookup"><span data-stu-id="0de3d-231">DAX</span></span>|<span data-ttu-id="0de3d-232">dax</span><span class="sxs-lookup"><span data-stu-id="0de3d-232">dax</span></span>|
|<span data-ttu-id="0de3d-233">Docker</span><span class="sxs-lookup"><span data-stu-id="0de3d-233">Docker</span></span>|<span data-ttu-id="0de3d-234">dockerfile</span><span class="sxs-lookup"><span data-stu-id="0de3d-234">dockerfile</span></span>|
|<span data-ttu-id="0de3d-235">F#</span><span class="sxs-lookup"><span data-stu-id="0de3d-235">F#</span></span>|<span data-ttu-id="0de3d-236">fsharp</span><span class="sxs-lookup"><span data-stu-id="0de3d-236">fsharp</span></span>|
|<span data-ttu-id="0de3d-237">Go</span><span class="sxs-lookup"><span data-stu-id="0de3d-237">Go</span></span>|<span data-ttu-id="0de3d-238">go</span><span class="sxs-lookup"><span data-stu-id="0de3d-238">go</span></span>|
|<span data-ttu-id="0de3d-239">HTML</span><span class="sxs-lookup"><span data-stu-id="0de3d-239">HTML</span></span>|<span data-ttu-id="0de3d-240">html</span><span class="sxs-lookup"><span data-stu-id="0de3d-240">html</span></span>|
|<span data-ttu-id="0de3d-241">HTTP</span><span class="sxs-lookup"><span data-stu-id="0de3d-241">HTTP</span></span>|<span data-ttu-id="0de3d-242">http</span><span class="sxs-lookup"><span data-stu-id="0de3d-242">http</span></span>|
|<span data-ttu-id="0de3d-243">Java</span><span class="sxs-lookup"><span data-stu-id="0de3d-243">Java</span></span>|<span data-ttu-id="0de3d-244">java</span><span class="sxs-lookup"><span data-stu-id="0de3d-244">java</span></span>|
|<span data-ttu-id="0de3d-245">JavaScript</span><span class="sxs-lookup"><span data-stu-id="0de3d-245">JavaScript</span></span>|<span data-ttu-id="0de3d-246">javascript</span><span class="sxs-lookup"><span data-stu-id="0de3d-246">javascript</span></span>|
|<span data-ttu-id="0de3d-247">JSON</span><span class="sxs-lookup"><span data-stu-id="0de3d-247">JSON</span></span>|<span data-ttu-id="0de3d-248">json</span><span class="sxs-lookup"><span data-stu-id="0de3d-248">json</span></span>|
|<span data-ttu-id="0de3d-249">Язык запросов Kusto</span><span class="sxs-lookup"><span data-stu-id="0de3d-249">Kusto Query Language</span></span>|<span data-ttu-id="0de3d-250">kusto</span><span class="sxs-lookup"><span data-stu-id="0de3d-250">kusto</span></span>|
|<span data-ttu-id="0de3d-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="0de3d-251">Markdown</span></span>|<span data-ttu-id="0de3d-252">md</span><span class="sxs-lookup"><span data-stu-id="0de3d-252">md</span></span>|
|<span data-ttu-id="0de3d-253">Objective-C</span><span class="sxs-lookup"><span data-stu-id="0de3d-253">Objective-C</span></span>|<span data-ttu-id="0de3d-254">objc</span><span class="sxs-lookup"><span data-stu-id="0de3d-254">objc</span></span>|
|<span data-ttu-id="0de3d-255">OData</span><span class="sxs-lookup"><span data-stu-id="0de3d-255">OData</span></span>|<span data-ttu-id="0de3d-256">odata</span><span class="sxs-lookup"><span data-stu-id="0de3d-256">odata</span></span>|
|<span data-ttu-id="0de3d-257">PHP</span><span class="sxs-lookup"><span data-stu-id="0de3d-257">PHP</span></span>|<span data-ttu-id="0de3d-258">php</span><span class="sxs-lookup"><span data-stu-id="0de3d-258">php</span></span>|
|<span data-ttu-id="0de3d-259">protobuf</span><span class="sxs-lookup"><span data-stu-id="0de3d-259">protobuf</span></span>|<span data-ttu-id="0de3d-260">protobuf</span><span class="sxs-lookup"><span data-stu-id="0de3d-260">protobuf</span></span>|
|<span data-ttu-id="0de3d-261">PowerApps (десятичный разделитель — точка)</span><span class="sxs-lookup"><span data-stu-id="0de3d-261">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="0de3d-262">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="0de3d-262">powerapps-dot</span></span>|
|<span data-ttu-id="0de3d-263">PowerApps (десятичный разделитель — запятая)</span><span class="sxs-lookup"><span data-stu-id="0de3d-263">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="0de3d-264">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="0de3d-264">powerapps-comma</span></span>|
|<span data-ttu-id="0de3d-265">PowerShell</span><span class="sxs-lookup"><span data-stu-id="0de3d-265">PowerShell</span></span>|<span data-ttu-id="0de3d-266">powershell</span><span class="sxs-lookup"><span data-stu-id="0de3d-266">powershell</span></span>|
|<span data-ttu-id="0de3d-267">Python</span><span class="sxs-lookup"><span data-stu-id="0de3d-267">Python</span></span>|<span data-ttu-id="0de3d-268">python</span><span class="sxs-lookup"><span data-stu-id="0de3d-268">python</span></span>|
|<span data-ttu-id="0de3d-269">Q#</span><span class="sxs-lookup"><span data-stu-id="0de3d-269">Q#</span></span>|<span data-ttu-id="0de3d-270">qsharp</span><span class="sxs-lookup"><span data-stu-id="0de3d-270">qsharp</span></span>|
|<span data-ttu-id="0de3d-271">R</span><span class="sxs-lookup"><span data-stu-id="0de3d-271">R</span></span>|<span data-ttu-id="0de3d-272">r</span><span class="sxs-lookup"><span data-stu-id="0de3d-272">r</span></span>|
|<span data-ttu-id="0de3d-273">Ruby</span><span class="sxs-lookup"><span data-stu-id="0de3d-273">Ruby</span></span>|<span data-ttu-id="0de3d-274">ruby</span><span class="sxs-lookup"><span data-stu-id="0de3d-274">ruby</span></span>|
|<span data-ttu-id="0de3d-275">SQL</span><span class="sxs-lookup"><span data-stu-id="0de3d-275">SQL</span></span>|<span data-ttu-id="0de3d-276">sql</span><span class="sxs-lookup"><span data-stu-id="0de3d-276">sql</span></span>|
|<span data-ttu-id="0de3d-277">Swift</span><span class="sxs-lookup"><span data-stu-id="0de3d-277">Swift</span></span>|<span data-ttu-id="0de3d-278">swift</span><span class="sxs-lookup"><span data-stu-id="0de3d-278">swift</span></span>|
|<span data-ttu-id="0de3d-279">TypeScript</span><span class="sxs-lookup"><span data-stu-id="0de3d-279">TypeScript</span></span>|<span data-ttu-id="0de3d-280">typescript</span><span class="sxs-lookup"><span data-stu-id="0de3d-280">typescript</span></span>|
|<span data-ttu-id="0de3d-281">VB</span><span class="sxs-lookup"><span data-stu-id="0de3d-281">VB</span></span>|<span data-ttu-id="0de3d-282">vb</span><span class="sxs-lookup"><span data-stu-id="0de3d-282">vb</span></span>|
|<span data-ttu-id="0de3d-283">XAML</span><span class="sxs-lookup"><span data-stu-id="0de3d-283">XAML</span></span>|<span data-ttu-id="0de3d-284">xaml</span><span class="sxs-lookup"><span data-stu-id="0de3d-284">xaml</span></span>|
|<span data-ttu-id="0de3d-285">XML</span><span class="sxs-lookup"><span data-stu-id="0de3d-285">XML</span></span>|<span data-ttu-id="0de3d-286">xml</span><span class="sxs-lookup"><span data-stu-id="0de3d-286">xml</span></span>|

<span data-ttu-id="0de3d-287">Имя `csharp-interactive` указывает на язык C# и возможность запускать примеры в браузере.</span><span class="sxs-lookup"><span data-stu-id="0de3d-287">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="0de3d-288">Эти фрагменты кода компилируются и выполняются в контейнере Docker, а результаты выполнения программы отображаются в окне браузера пользователя.</span><span class="sxs-lookup"><span data-stu-id="0de3d-288">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="0de3d-289">Пример. C\#</span><span class="sxs-lookup"><span data-stu-id="0de3d-289">Example: C\#</span></span>

<span data-ttu-id="0de3d-290">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="0de3d-290">__Markdown__</span></span>

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

<span data-ttu-id="0de3d-291">__Отображение__</span><span class="sxs-lookup"><span data-stu-id="0de3d-291">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="0de3d-292">Пример. SQL</span><span class="sxs-lookup"><span data-stu-id="0de3d-292">Example: SQL</span></span>

<span data-ttu-id="0de3d-293">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="0de3d-293">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="0de3d-294">__Отображение__</span><span class="sxs-lookup"><span data-stu-id="0de3d-294">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="docs-custom-markdown-extensions"></a><span data-ttu-id="0de3d-295">Настраиваемые расширения Markdown для документации</span><span class="sxs-lookup"><span data-stu-id="0de3d-295">Docs custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="0de3d-296">Сайт Docs.Microsoft.com (сайт документации) использует Markdig, синтаксический анализатор Markdown, обеспечивающий высокую совместимость с диалектом GitHub Flavored Markdown (GFM).</span><span class="sxs-lookup"><span data-stu-id="0de3d-296">Docs.Microsoft.com (Docs) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="0de3d-297">Markdig добавляет дополнительные функции за счет расширений Markdown.</span><span class="sxs-lookup"><span data-stu-id="0de3d-297">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="0de3d-298">Поэтому для справки мы включили в этот материал некоторые разделы из руководства по разработке OPS.</span><span class="sxs-lookup"><span data-stu-id="0de3d-298">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="0de3d-299">(Например, см. в содержании разделы "Markdig и расширения Markdown" и "Фрагменты кода".)</span><span class="sxs-lookup"><span data-stu-id="0de3d-299">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="0de3d-300">В статьях документации для общего форматирования, например для создания абзацев, ссылок, списков и заголовков, используется GFM.</span><span class="sxs-lookup"><span data-stu-id="0de3d-300">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="0de3d-301">Для расширенного форматирования в статьях можно использовать следующие функции Markdig:</span><span class="sxs-lookup"><span data-stu-id="0de3d-301">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="0de3d-302">Блоки заметок</span><span class="sxs-lookup"><span data-stu-id="0de3d-302">Note blocks</span></span>
- <span data-ttu-id="0de3d-303">Включаемые файлы</span><span class="sxs-lookup"><span data-stu-id="0de3d-303">Include files</span></span>
- <span data-ttu-id="0de3d-304">Селекторы</span><span class="sxs-lookup"><span data-stu-id="0de3d-304">Selectors</span></span>
- <span data-ttu-id="0de3d-305">Внедряемые видео</span><span class="sxs-lookup"><span data-stu-id="0de3d-305">Embedded videos</span></span>
- <span data-ttu-id="0de3d-306">Фрагменты или примеры кода</span><span class="sxs-lookup"><span data-stu-id="0de3d-306">Code snippets/samples</span></span>

<span data-ttu-id="0de3d-307">Полный список см. в разделах "Markdig и расширения Markdown" и "Фрагменты кода".</span><span class="sxs-lookup"><span data-stu-id="0de3d-307">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="0de3d-308">Блоки заметок</span><span class="sxs-lookup"><span data-stu-id="0de3d-308">Note blocks</span></span>

<span data-ttu-id="0de3d-309">Есть четыре типа блоков заметок, которые позволяют привлечь внимание к определенному содержимому:</span><span class="sxs-lookup"><span data-stu-id="0de3d-309">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="0de3d-310">NOTE (примечание)</span><span class="sxs-lookup"><span data-stu-id="0de3d-310">NOTE</span></span>
- <span data-ttu-id="0de3d-311">WARNING (предупреждение)</span><span class="sxs-lookup"><span data-stu-id="0de3d-311">WARNING</span></span>
- <span data-ttu-id="0de3d-312">TIP (подсказка)</span><span class="sxs-lookup"><span data-stu-id="0de3d-312">TIP</span></span>
- <span data-ttu-id="0de3d-313">IMPORTANT (важно)</span><span class="sxs-lookup"><span data-stu-id="0de3d-313">IMPORTANT</span></span>

<span data-ttu-id="0de3d-314">В целом не следует часто использовать блоки заметок, так как они могут отвлекать пользователя от основного содержимого.</span><span class="sxs-lookup"><span data-stu-id="0de3d-314">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="0de3d-315">Хотя эти элементы также поддерживают блоки кода, изображения, списки и ссылки, лучше не перегружать их, делая простыми и понятными.</span><span class="sxs-lookup"><span data-stu-id="0de3d-315">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="0de3d-316">Примеры:</span><span class="sxs-lookup"><span data-stu-id="0de3d-316">Examples:</span></span>

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

<span data-ttu-id="0de3d-317">На сайте docs.microsoft.com эти оповещения отображаются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0de3d-317">These alerts look like this on docs.microsoft.com:</span></span>

![Вид оповещений из предыдущего примера с разными значками и цветами на опубликованной странице портала документации.](media/alerts-rendering.png)

### <a name="include-files"></a><span data-ttu-id="0de3d-319">Включаемые файлы</span><span class="sxs-lookup"><span data-stu-id="0de3d-319">Include files</span></span>

<span data-ttu-id="0de3d-320">Если вы хотите добавить в файлы статей многократно используемые изображения или текст, воспользуйтесь доступной в Markdig функцией включения ("include") файлов по ссылке.</span><span class="sxs-lookup"><span data-stu-id="0de3d-320">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="0de3d-321">Функция указывает OPS включить файл в файл статьи во время сборки, чтобы он стал частью опубликованной статьи.</span><span class="sxs-lookup"><span data-stu-id="0de3d-321">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="0de3d-322">Существует три типа включения файлов для многократного использования содержимого:</span><span class="sxs-lookup"><span data-stu-id="0de3d-322">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="0de3d-323">Встроенные: Используются для многократного использования фрагмента стандартного текста путем его встраивания в другое предложение.</span><span class="sxs-lookup"><span data-stu-id="0de3d-323">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="0de3d-324">Блочные: Используются для многократного использования всего файла Markdown в качестве блока путем его вложения в раздел или статью.</span><span class="sxs-lookup"><span data-stu-id="0de3d-324">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="0de3d-325">Изображения: Так на платформе Docs реализовано стандартное включение изображений.</span><span class="sxs-lookup"><span data-stu-id="0de3d-325">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="0de3d-326">Встроенные и блочные включаемые файлы — это простые файлы Markdown с расширением .md.</span><span class="sxs-lookup"><span data-stu-id="0de3d-326">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="0de3d-327">Они могут содержать любую допустимую разметку Markdown.</span><span class="sxs-lookup"><span data-stu-id="0de3d-327">It can contain any valid Markdown.</span></span> <span data-ttu-id="0de3d-328">Все включаемые файлы Markdown должны быть помещены в [общий подкаталог `/includes`](git-github-fundamentals.md#includes-subdirectory) в корневом каталоге репозитория.</span><span class="sxs-lookup"><span data-stu-id="0de3d-328">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="0de3d-329">Когда статья публикуется, включаемый файл легко интегрируется в нее.</span><span class="sxs-lookup"><span data-stu-id="0de3d-329">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="0de3d-330">Ниже приведены требования к включаемым файлам и соображения по работе с ними:</span><span class="sxs-lookup"><span data-stu-id="0de3d-330">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="0de3d-331">Используйте включаемые файлы, если вам нужно, чтобы один и тот же текст отображался в нескольких статьях.</span><span class="sxs-lookup"><span data-stu-id="0de3d-331">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="0de3d-332">Блочные включаемые файлы предназначены для значительных объемов текста: один или два абзаца, общая процедура или общий раздел.</span><span class="sxs-lookup"><span data-stu-id="0de3d-332">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="0de3d-333">Не используйте их для фрагментов текста меньше одного предложения.</span><span class="sxs-lookup"><span data-stu-id="0de3d-333">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="0de3d-334">Включаемые файлы не будут отображаться в представлении статьи на GitHub, так как они работают только с Markdig-расширениями.</span><span class="sxs-lookup"><span data-stu-id="0de3d-334">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="0de3d-335">Они отображаются только после публикации.</span><span class="sxs-lookup"><span data-stu-id="0de3d-335">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="0de3d-336">Весь текст во включаемом файле должен состоять из полноценных предложений или фраз, не зависящих от остального текста статьи, в которую добавляется ссылка на такой файл.</span><span class="sxs-lookup"><span data-stu-id="0de3d-336">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="0de3d-337">Если не следовать этой инструкции, в статье создаются непереводимые строки, которые нарушают процесс локализации.</span><span class="sxs-lookup"><span data-stu-id="0de3d-337">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="0de3d-338">Не внедряйте одни включаемые файлы в другие.</span><span class="sxs-lookup"><span data-stu-id="0de3d-338">Don't embed include references within other include files.</span></span> <span data-ttu-id="0de3d-339">Такая возможность не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0de3d-339">They are not supported.</span></span>
- <span data-ttu-id="0de3d-340">Файлы мультимедиа должны быть помещены в отдельную папку мультимедиа в подкаталоге включаемых файлов. Например, `<repo>`/включаемые файлы/папка мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0de3d-340">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="0de3d-341">В корне каталога мультимедиа не должны содержаться изображения.</span><span class="sxs-lookup"><span data-stu-id="0de3d-341">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="0de3d-342">Если во включаемом файле нет изображений, соответствующий каталог мультимедиа не требуется.</span><span class="sxs-lookup"><span data-stu-id="0de3d-342">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="0de3d-343">Как и в обычных статьях, не используйте общий файл мультимедиа для включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="0de3d-343">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="0de3d-344">Для каждого включаемого файла в статье должен быть создан отдельный файл с уникальным именем.</span><span class="sxs-lookup"><span data-stu-id="0de3d-344">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="0de3d-345">Файл мультимедиа должен храниться в папке мультимедиа, связанной с включаемым файлом.</span><span class="sxs-lookup"><span data-stu-id="0de3d-345">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="0de3d-346">Не используйте включаемый файл как единственное содержимое статьи.</span><span class="sxs-lookup"><span data-stu-id="0de3d-346">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="0de3d-347">Включаемые файлы предназначены для дополнения основных материалов статьи.</span><span class="sxs-lookup"><span data-stu-id="0de3d-347">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="0de3d-348">Пример.</span><span class="sxs-lookup"><span data-stu-id="0de3d-348">Example:</span></span>

```md
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="0de3d-349">Селекторы</span><span class="sxs-lookup"><span data-stu-id="0de3d-349">Selectors</span></span>

<span data-ttu-id="0de3d-350">В технических статьях селекторы применяются для создания разных вариантов содержимого, чтобы проиллюстрировать различия в реализации, связанные с использованием нескольких технологий или платформ.</span><span class="sxs-lookup"><span data-stu-id="0de3d-350">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="0de3d-351">Это в особенности применимо к материалам о мобильных платформах для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="0de3d-351">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="0de3d-352">Сейчас в Markdig есть два типа селекторов: для единичного и множественного выбора.</span><span class="sxs-lookup"><span data-stu-id="0de3d-352">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="0de3d-353">В каждой статье с возможностью выбора используется одна и та же разметка Markdown для селектора. Поэтому рекомендуется поместить селектор для статьи во включаемый файл.</span><span class="sxs-lookup"><span data-stu-id="0de3d-353">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="0de3d-354">Затем нужно добавить ссылки на этот файл во все статьи, для которых используется селектор.</span><span class="sxs-lookup"><span data-stu-id="0de3d-354">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="0de3d-355">Ниже приведен пример селектора:</span><span class="sxs-lookup"><span data-stu-id="0de3d-355">The following shows an example selector:</span></span>

```md
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="0de3d-356">Пример селекторов в действии можно посмотреть в [документации по Azure](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span><span class="sxs-lookup"><span data-stu-id="0de3d-356">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="0de3d-357">Включение фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="0de3d-357">Code include references</span></span>

<span data-ttu-id="0de3d-358">Расширение Markdown для фрагментов кода в документации позволяет вам вставлять в свои статьи фрагменты кода и форматировать их синтаксис в соответствии с используемым языком программирования.</span><span class="sxs-lookup"><span data-stu-id="0de3d-358">The Docs code snippet Markdown extension allows you to embed code samples in your articles and render them with language-specific syntax coloring.</span></span> <span data-ttu-id="0de3d-359">Вы можете включать код из текущего либо из какого-то другого репозитория.</span><span class="sxs-lookup"><span data-stu-id="0de3d-359">You can include code from either the current repository or another repository.</span></span> <span data-ttu-id="0de3d-360">Ниже приведены инструкции по использованию этой функции с пакетом создания документации [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span><span class="sxs-lookup"><span data-stu-id="0de3d-360">The instructions below provides an overview of how to use the feature with the [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span></span> <span data-ttu-id="0de3d-361">Доступен **Предварительный просмотр** фрагментов кода в Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="0de3d-361">In Visual Studio Code, you can preview the code snippets by opening **Preview**.</span></span> <span data-ttu-id="0de3d-362">Предварительный просмотр не поддерживает выделение и интерактивные возможности.</span><span class="sxs-lookup"><span data-stu-id="0de3d-362">Highlighting and interactivity are not available in preview.</span></span>

> [!NOTE]
> <span data-ttu-id="0de3d-363">Расширение не поддерживает включение в содержимое кода во встроенном (inline) режиме. Используйте для этого стандартный элемент \`\`\` в Markdown.</span><span class="sxs-lookup"><span data-stu-id="0de3d-363">The extension does not support including code content within it inline – this is to be done through the standard triple-tick Markdown convention.</span></span>

#### <a name="code-from-current-repository"></a><span data-ttu-id="0de3d-364">Код из текущего репозитория</span><span class="sxs-lookup"><span data-stu-id="0de3d-364">Code from current repository</span></span>

1. <span data-ttu-id="0de3d-365">Находясь в Visual Studio Code, нажмите клавиши **ALT+M** или **OPTION+M** и выберите "Фрагмент кода".</span><span class="sxs-lookup"><span data-stu-id="0de3d-365">In Visual Studio Code, click **Alt + M** or **Option + M** and select Snippet.</span></span>
2. <span data-ttu-id="0de3d-366">Вам будет предложено выполнить поиск по всему содержимому, в какой-то области или по различным репозиториям.</span><span class="sxs-lookup"><span data-stu-id="0de3d-366">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="0de3d-367">Выберите поиск по всему локальному содержимому.</span><span class="sxs-lookup"><span data-stu-id="0de3d-367">To search locally, select Full Local Search.</span></span>
3. <span data-ttu-id="0de3d-368">Введите условие поиска и найдите нужный файл.</span><span class="sxs-lookup"><span data-stu-id="0de3d-368">Enter a search term to find the file.</span></span> <span data-ttu-id="0de3d-369">Найдя файл, выберите его.</span><span class="sxs-lookup"><span data-stu-id="0de3d-369">Once you’ve found the file, select the file.</span></span>
4. <span data-ttu-id="0de3d-370">Затем выберите, какие строки кода нужно включить в фрагмент, используя</span><span class="sxs-lookup"><span data-stu-id="0de3d-370">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="0de3d-371">следующие параметры: **ИД**, **Диапазон** или **Никакие**.</span><span class="sxs-lookup"><span data-stu-id="0de3d-371">The options are: **ID**, **Range** and **None**.</span></span>
5. <span data-ttu-id="0de3d-372">В зависимости от выбора на шаге 4 предоставьте необходимые значения.</span><span class="sxs-lookup"><span data-stu-id="0de3d-372">Based on your selection from Step 4, provide a value if necessary.</span></span>

<span data-ttu-id="0de3d-373">Отображение всего файла кода:</span><span class="sxs-lookup"><span data-stu-id="0de3d-373">Display entire code file:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

<span data-ttu-id="0de3d-374">Отображение части файла кода путем указания номера строк:</span><span class="sxs-lookup"><span data-stu-id="0de3d-374">Display part of a code file by specifying line numbers:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="0de3d-375">Отображение части файла кода путем указания имени фрагмента:</span><span class="sxs-lookup"><span data-stu-id="0de3d-375">Display part of a code file by a snippet name:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

#### <a name="code-from-another-repository"></a><span data-ttu-id="0de3d-376">Код из другого репозитория</span><span class="sxs-lookup"><span data-stu-id="0de3d-376">Code from another repository</span></span>

1. <span data-ttu-id="0de3d-377">Находясь в Visual Studio Code, нажмите клавиши **ALT+M** или **OPTION+M** и выберите "Фрагмент кода".</span><span class="sxs-lookup"><span data-stu-id="0de3d-377">In Visual Studio Code, click **Alt + M** or **Option + M** and select Snippet.</span></span>
2. <span data-ttu-id="0de3d-378">Вам будет предложено выполнить поиск по всему содержимому, в какой-то области или по различным репозиториям.</span><span class="sxs-lookup"><span data-stu-id="0de3d-378">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="0de3d-379">Выберите поиск по репозиториям.</span><span class="sxs-lookup"><span data-stu-id="0de3d-379">To search across repositories, select Cross-Repository Reference.</span></span>
3. <span data-ttu-id="0de3d-380">Вам будет представлен набор репозиториев из *.openpublishing.publish.config.json*.</span><span class="sxs-lookup"><span data-stu-id="0de3d-380">You will be given a selection of repositories that are in *.openpublishing.publish.config.json*.</span></span> <span data-ttu-id="0de3d-381">Выберите репозиторий.</span><span class="sxs-lookup"><span data-stu-id="0de3d-381">Select a repository.</span></span>
3. <span data-ttu-id="0de3d-382">Введите условие поиска и найдите нужный файл.</span><span class="sxs-lookup"><span data-stu-id="0de3d-382">Enter a search term to find the file.</span></span> <span data-ttu-id="0de3d-383">Найдя файл, выберите его.</span><span class="sxs-lookup"><span data-stu-id="0de3d-383">Once you’ve found the file, select the file.</span></span>
4. <span data-ttu-id="0de3d-384">Затем выберите, какие строки кода нужно включить в фрагмент, используя</span><span class="sxs-lookup"><span data-stu-id="0de3d-384">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="0de3d-385">следующие параметры: **ИД**, **Диапазон** или **Никакие**.</span><span class="sxs-lookup"><span data-stu-id="0de3d-385">The options are: **ID**, **Range** and **None**.</span></span>
5. <span data-ttu-id="0de3d-386">В зависимости от выбора на шаге 5 предоставьте необходимые значения.</span><span class="sxs-lookup"><span data-stu-id="0de3d-386">Based on your selection from Step 5, provide a value if necessary.</span></span>

<span data-ttu-id="0de3d-387">Ссылка на фрагмент кода будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0de3d-387">Your snippet reference will look like this:</span></span>

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

#### <a name="path-to-code-file"></a><span data-ttu-id="0de3d-388">Путь к файлу кода</span><span class="sxs-lookup"><span data-stu-id="0de3d-388">Path to code file</span></span>

<span data-ttu-id="0de3d-389">Пример.</span><span class="sxs-lookup"><span data-stu-id="0de3d-389">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="0de3d-390">Пример взят из репозитория документов ASP.NET, файла статьи [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md).</span><span class="sxs-lookup"><span data-stu-id="0de3d-390">The example is from the ASP.NET docs repo, [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) article file.</span></span> <span data-ttu-id="0de3d-391">Для ссылки на файл кода используется относительный путь к [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) в том же репозитории.</span><span class="sxs-lookup"><span data-stu-id="0de3d-391">The code file is referenced by a relative path to [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) in the same repository.</span></span>

#### <a name="selected-line-numbers"></a><span data-ttu-id="0de3d-392">Выбранные номера строк</span><span class="sxs-lookup"><span data-stu-id="0de3d-392">Selected line numbers</span></span>

<span data-ttu-id="0de3d-393">Пример.</span><span class="sxs-lookup"><span data-stu-id="0de3d-393">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="0de3d-394">В этом примере отображаются только строки 2–24 и 26 из файла кода *StudentController.cs*.</span><span class="sxs-lookup"><span data-stu-id="0de3d-394">This example displays only lines 2-24 and 26 of the *StudentController.cs* code file.</span></span>

<span data-ttu-id="0de3d-395">Предпочтительнее использовать фрагменты кода по номерам жестко закодированных строк, как описано в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="0de3d-395">Prefer snippets over hard-coded line numbers, as explained in the next section.</span></span>

#### <a name="named-snippet"></a><span data-ttu-id="0de3d-396">Именованный фрагмент кода</span><span class="sxs-lookup"><span data-stu-id="0de3d-396">Named snippet</span></span>

<span data-ttu-id="0de3d-397">Пример.</span><span class="sxs-lookup"><span data-stu-id="0de3d-397">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

<span data-ttu-id="0de3d-398">Используйте для имени только буквы и символы подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="0de3d-398">Use only letters and underscores for the name.</span></span>

<span data-ttu-id="0de3d-399">В примере отображается раздел `snippet_Create` файла кода.</span><span class="sxs-lookup"><span data-stu-id="0de3d-399">The example displays the `snippet_Create` section of the code file.</span></span> <span data-ttu-id="0de3d-400">В файле кода для этого примера имеется часть на C# с именем `snippet_Create`:</span><span class="sxs-lookup"><span data-stu-id="0de3d-400">The code file for this example has a C# region named `snippet_Create`:</span></span>

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

<span data-ttu-id="0de3d-401">По возможности ссылайтесь на именованный раздел, а не указывайте номера строк.</span><span class="sxs-lookup"><span data-stu-id="0de3d-401">Whenever you can, refer to a named section rather than specifying line numbers.</span></span> <span data-ttu-id="0de3d-402">Ссылки на номера строк являются ненадежными, так как файлы кода неизбежно изменяются с помощью способов, которые изменяют номера строк.</span><span class="sxs-lookup"><span data-stu-id="0de3d-402">Line number references are brittle because code files inevitably change in ways that make line numbers change.</span></span>
<span data-ttu-id="0de3d-403">Вы не обязательно получите уведомления об этих изменениях.</span><span class="sxs-lookup"><span data-stu-id="0de3d-403">You don't necessarily get notified of such changes.</span></span> <span data-ttu-id="0de3d-404">В статье в конечном итоге будут отображаться неправильные строки, и вы даже не будете об этом знать.</span><span class="sxs-lookup"><span data-stu-id="0de3d-404">Your article eventually starts showing the wrong lines and you have no clue anything has changed.</span></span>

#### <a name="highlighting-selected-lines"></a><span data-ttu-id="0de3d-405">Выделение выбранных строк</span><span class="sxs-lookup"><span data-stu-id="0de3d-405">Highlighting selected lines</span></span>

<span data-ttu-id="0de3d-406">Пример.</span><span class="sxs-lookup"><span data-stu-id="0de3d-406">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

<span data-ttu-id="0de3d-407">В примере выделены строки 2 и 5, если считать от начала отображаемого фрагмента кода.</span><span class="sxs-lookup"><span data-stu-id="0de3d-407">The example highlights lines 2 and 5, counting from the start of the displayed snippet.</span></span> <span data-ttu-id="0de3d-408">(Подсчет выделяемых номеров строк не начинается от начала файла кода.) Другими словами, выделяются строки 3 и 6 файла кода.</span><span class="sxs-lookup"><span data-stu-id="0de3d-408">(Line numbers to highlight don't count from the start of the code file.) In other words, lines 3 and 6 of the code file are highlighted.</span></span>

#### <a name="interactive-code-snippets"></a><span data-ttu-id="0de3d-409">Интерактивные фрагменты кода</span><span class="sxs-lookup"><span data-stu-id="0de3d-409">Interactive code snippets</span></span>

<span data-ttu-id="0de3d-410">Для фрагментов кода, включаемых по ссылке, можно включить интерактивный режим.</span><span class="sxs-lookup"><span data-stu-id="0de3d-410">You can enable interactive mode for code snippets included by reference.</span></span> <span data-ttu-id="0de3d-411">Ниже приведены примеры:</span><span class="sxs-lookup"><span data-stu-id="0de3d-411">Here are examples:</span></span>

```markdown
:::code language="powershell" source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code language="bash" source="Bash.sh" interactive="cloudshell-bash":::
```

<span data-ttu-id="0de3d-412">Чтобы включить эту функцию для конкретного блока кода, используйте атрибут `interactive`.</span><span class="sxs-lookup"><span data-stu-id="0de3d-412">To turn on this feature for a particular code block, use the `interactive` attribute.</span></span> <span data-ttu-id="0de3d-413">Допустимые значения атрибута:</span><span class="sxs-lookup"><span data-stu-id="0de3d-413">The available attribute values are:</span></span>

- <span data-ttu-id="0de3d-414">`cloudshell-powershell` — активирует Cloud Shell в Azure PowerShell, как в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="0de3d-414">`cloudshell-powershell` - Enables the Azure PowerShell Cloud Shell, as in the preceding example</span></span>
- <span data-ttu-id="0de3d-415">`cloudshell-bash` — включает Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="0de3d-415">`cloudshell-bash` - Enables the Azure Cloud Shell</span></span>
- <span data-ttu-id="0de3d-416">`try-dotnet` — активирует Try .NET.</span><span class="sxs-lookup"><span data-stu-id="0de3d-416">`try-dotnet` - Enables Try .NET</span></span>
- <span data-ttu-id="0de3d-417">`try-dotnet-class` — активирует Try .NET с формированием шаблонов классов.</span><span class="sxs-lookup"><span data-stu-id="0de3d-417">`try-dotnet-class` - Enables Try .NET with class scaffolding</span></span>
- <span data-ttu-id="0de3d-418">`try-dotnet-method` — активирует Try .NET с формированием шаблонов методов.</span><span class="sxs-lookup"><span data-stu-id="0de3d-418">`try-dotnet-method` - Enables Try .NET with method scaffolding</span></span>

<span data-ttu-id="0de3d-419">Существуют совместимые пары `language` и `interactive`.</span><span class="sxs-lookup"><span data-stu-id="0de3d-419">There are pairs of `language` and `interactive` that are compatible.</span></span> <span data-ttu-id="0de3d-420">Например, если для `interactive` задано `try-dotnet`, должен использоваться язык `csharp`.</span><span class="sxs-lookup"><span data-stu-id="0de3d-420">For example, if `interactive` is `try-dotnet`, the language must be `csharp`.</span></span> <span data-ttu-id="0de3d-421">Аналогичным образом `cloudshell-powershell` будет работать только с `powershell`, а `cloudshell-bash` — только с языком `bash`.</span><span class="sxs-lookup"><span data-stu-id="0de3d-421">Similarly, `cloudshell-powershell` would only work with `powershell` and `cloudshell-bash` would work only with `bash` as the language.</span></span>

<span data-ttu-id="0de3d-422">В Azure Cloud Shell и PowerShell Cloud Shell пользователи могут выполнять команды только с собственной учетной записью Azure.</span><span class="sxs-lookup"><span data-stu-id="0de3d-422">For the Azure Cloud Shell and PowerShell Cloud Shell, users can run commands against only their own Azure account.</span></span>

<span data-ttu-id="0de3d-423">[Try .NET](https://github.com/dotnet/try) позволяет использовать интерактивное выполнение кода .NET (C#) в браузере.</span><span class="sxs-lookup"><span data-stu-id="0de3d-423">[Try .NET](https://github.com/dotnet/try) enables interactive execution of .NET code (C#) in the browser.</span></span> <span data-ttu-id="0de3d-424">Для Try .NET доступны три варианта интерактивности: `try-dotnet`, `try-dotnet-class` и `try-dotnet-method`.</span><span class="sxs-lookup"><span data-stu-id="0de3d-424">For Try .NET, there are three options for interactivity: `try-dotnet`, `try-dotnet-class`, and `try-dotnet-method`.</span></span> <span data-ttu-id="0de3d-425">Для этих возможностей не требуется какая-либо дополнительная конфигурация в фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="0de3d-425">Use of these options require no additional configuration within the code snippet.</span></span> <span data-ttu-id="0de3d-426">Доступные сейчас по умолчанию пространства имен:</span><span class="sxs-lookup"><span data-stu-id="0de3d-426">The namespaces currently available by default are:</span></span>

- <span data-ttu-id="0de3d-427">System</span><span class="sxs-lookup"><span data-stu-id="0de3d-427">System</span></span>
- <span data-ttu-id="0de3d-428">System.Linq</span><span class="sxs-lookup"><span data-stu-id="0de3d-428">System.Linq</span></span>
- <span data-ttu-id="0de3d-429">System.Collections.Generic</span><span class="sxs-lookup"><span data-stu-id="0de3d-429">System.Collections.Generic</span></span>
- <span data-ttu-id="0de3d-430">System.Text</span><span class="sxs-lookup"><span data-stu-id="0de3d-430">System.Text</span></span>
- <span data-ttu-id="0de3d-431">System.Globalization</span><span class="sxs-lookup"><span data-stu-id="0de3d-431">System.Globalization</span></span>
- <span data-ttu-id="0de3d-432">System.Text.RegularExpressions</span><span class="sxs-lookup"><span data-stu-id="0de3d-432">System.Text.RegularExpressions</span></span>

<span data-ttu-id="0de3d-433">Значение атрибута `try-dotnet` позволяет пользователям выполнять код C# в браузере напрямую, не заключая его в код-оболочку.</span><span class="sxs-lookup"><span data-stu-id="0de3d-433">The `try-dotnet` attribute value enables users to run C# code in the browser without the need to wrap the code in any custom code.</span></span>

<span data-ttu-id="0de3d-434">Пример.</span><span class="sxs-lookup"><span data-stu-id="0de3d-434">Example:</span></span>

```md
:::code language="csharp" source="relative/path/source.cs" interactive="try-dotnet":::
```

<span data-ttu-id="0de3d-435">Значение `try-dotnet-class` активирует формирование шаблонов на уровне классов для кода, передаваемого интерактивному компоненту.</span><span class="sxs-lookup"><span data-stu-id="0de3d-435">The `try-dotnet-class` value applies class-level scaffolding to the code passed to the interactive component.</span></span>

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-class":::
```

<span data-ttu-id="0de3d-436">Пример.</span><span class="sxs-lookup"><span data-stu-id="0de3d-436">Example:</span></span>

<span data-ttu-id="0de3d-437">Фрагмент кода без формирования шаблонов классов</span><span class="sxs-lookup"><span data-stu-id="0de3d-437">Code Snippet without Class Scaffolding Applied</span></span>

```md
public static void Main()
    {  
        // Specify the data source.  
        int[] scores = new int[] { 97, 92, 81, 60 };        // Define the query expression.

        IEnumerable<int> scoreQuery =
            from score in scores  
            where score > 80  
            select score;

        // Execute the query.  
        foreach (int i in scoreQuery)
        {  
            Console.Write(i + " ");
        }
    }  
}
```

<span data-ttu-id="0de3d-438">Фрагмент кода с формированием шаблонов классов</span><span class="sxs-lookup"><span data-stu-id="0de3d-438">Code Snippet with Class Scaffolding Applied</span></span>

```md
class NameOfClass {

   public static void Main()
    {
        // Specify the data source.
        int[] scores = new int[] { 97, 92, 81, 60 };

        // Define the query expression.
        IEnumerable<int> scoreQuery =
            from score in scores
            where score > 80
            select score;

        // Execute the query.
        foreach (int i in scoreQuery)
        {
            Console.Write(i + " ");
        }
    }  
}
```

<span data-ttu-id="0de3d-439">Значение `try-dotnet-method` активирует формирование шаблонов на уровне методов для кода, передаваемого интерактивному компоненту.</span><span class="sxs-lookup"><span data-stu-id="0de3d-439">The `try-dotnet-method` value applies method-level scaffolding to the code passed to the interactive component.</span></span>

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-method":::
```

<span data-ttu-id="0de3d-440">Пример.</span><span class="sxs-lookup"><span data-stu-id="0de3d-440">Example:</span></span>

<span data-ttu-id="0de3d-441">Фрагмент кода без формирования шаблонов методов</span><span class="sxs-lookup"><span data-stu-id="0de3d-441">Code Snippet without Method Scaffolding Applied</span></span>

```md
/*Print some string in C#*/

Console.WriteLine("Hello C#.);
```

<span data-ttu-id="0de3d-442">Фрагмент кода с формированием шаблонов методов</span><span class="sxs-lookup"><span data-stu-id="0de3d-442">Code Snippet with Method Scaffolding Applied</span></span>

```md
public static void Main(string args[]) {

/*Print some string in C#*/

Console.WriteLine("Hello C#.);
}
```

#### <a name="snippet-syntax-reference"></a><span data-ttu-id="0de3d-443">Синтаксис ссылок на фрагменты</span><span class="sxs-lookup"><span data-stu-id="0de3d-443">Snippet syntax reference</span></span>

<span data-ttu-id="0de3d-444">Вы можете ссылаться на фрагменты кода, хранящиеся в репозитории, с помощью указанного языка кода.</span><span class="sxs-lookup"><span data-stu-id="0de3d-444">You can reference code snippets stored in your repo by using the specified code language.</span></span> <span data-ttu-id="0de3d-445">Содержимое заданного пути к коду будет развернуто и включено в файл.</span><span class="sxs-lookup"><span data-stu-id="0de3d-445">The content of the specified code path will be expanded and included in your file.</span></span>

<span data-ttu-id="0de3d-446">Какие-либо ограничения на структуру папок для фрагментов кода отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="0de3d-446">There aren't restrictions on the folder structure of code snippets.</span></span> <span data-ttu-id="0de3d-447">Управление фрагментами кода осуществляется аналогично управлению обычным исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="0de3d-447">You can manage the code snippets as normal source code.</span></span>

<span data-ttu-id="0de3d-448">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0de3d-448">Syntax:</span></span>

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> <span data-ttu-id="0de3d-449">Этот синтаксис является блоком расширения Markdown.</span><span class="sxs-lookup"><span data-stu-id="0de3d-449">This syntax is a block Markdown extension.</span></span> <span data-ttu-id="0de3d-450">Он должен использоваться в отдельной строке.</span><span class="sxs-lookup"><span data-stu-id="0de3d-450">It must be used on its own line.</span></span>

- <span data-ttu-id="0de3d-451">`<language>` (*необязательно*)</span><span class="sxs-lookup"><span data-stu-id="0de3d-451">`<language>` (*optional*)</span></span>
  - <span data-ttu-id="0de3d-452">Язык фрагмента кода.</span><span class="sxs-lookup"><span data-stu-id="0de3d-452">Language of the code snippet.</span></span> <span data-ttu-id="0de3d-453">Дополнительные сведения см. в разделе [Поддерживаемые языки](#supported-languages) далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="0de3d-453">For more information, see the [Supported languages](#supported-languages) section later in this article.</span></span>

- <span data-ttu-id="0de3d-454">`<path>` (*обязательно*)</span><span class="sxs-lookup"><span data-stu-id="0de3d-454">`<path>` (*mandatory*)</span></span>
  - <span data-ttu-id="0de3d-455">Относительный путь в файловой системе, который указывает файл фрагмента кода для ссылки.</span><span class="sxs-lookup"><span data-stu-id="0de3d-455">Relative path in the file system that indicates the code snippet file to reference.</span></span>

- <span data-ttu-id="0de3d-456">`<attribute>` и `<attribute-value>` (*необязательно*)</span><span class="sxs-lookup"><span data-stu-id="0de3d-456">`<attribute>` and `<attribute-value>` (*optional*)</span></span>
  - <span data-ttu-id="0de3d-457">Используются вместе для указания способа получения кода из файла:</span><span class="sxs-lookup"><span data-stu-id="0de3d-457">Used together to specify how the code should be retrieved from the file:</span></span>
    - <span data-ttu-id="0de3d-458">`range`: `1,3-5` Диапазон строк.</span><span class="sxs-lookup"><span data-stu-id="0de3d-458">`range`: `1,3-5` A range of lines.</span></span> <span data-ttu-id="0de3d-459">Этот пример содержит строки 1, 3, 4 и 5.</span><span class="sxs-lookup"><span data-stu-id="0de3d-459">This example includes lines 1, 3, 4, and 5.</span></span>
    - <span data-ttu-id="0de3d-460">`id`: `snippet_Create` Идентификатор фрагмента, который нужно вставить из файла кода.</span><span class="sxs-lookup"><span data-stu-id="0de3d-460">`id`: `snippet_Create` The ID of the snippet that needs to be inserted from the code file.</span></span> <span data-ttu-id="0de3d-461">Это значение не может существовать одновременно с диапазоном.</span><span class="sxs-lookup"><span data-stu-id="0de3d-461">This value cannot co-exist with range.</span></span>
    - <span data-ttu-id="0de3d-462">`highlight`: `2-4,6` Диапазон и (или) номера строк, которые должны выделяться в создаваемом фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="0de3d-462">`highlight`: `2-4,6` Range and/or numbers of lines that need to be highlighted in the generated code snippet.</span></span> <span data-ttu-id="0de3d-463">Нумерация ведется в масштабе самого фрагмента, а не импортируемого диапазона.</span><span class="sxs-lookup"><span data-stu-id="0de3d-463">The numbering is relative to the code snippet itself, not the imported range.</span></span>
    - <span data-ttu-id="0de3d-464">`interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` Строковое значение, определяющее тип используемой интерактивности.</span><span class="sxs-lookup"><span data-stu-id="0de3d-464">`interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` String value determines what kinds of interactivity are enabled.</span></span>

#### <a name="supported-languages"></a><span data-ttu-id="0de3d-465">Поддерживаемые языки</span><span class="sxs-lookup"><span data-stu-id="0de3d-465">Supported languages</span></span>

|<span data-ttu-id="0de3d-466">Имя</span><span class="sxs-lookup"><span data-stu-id="0de3d-466">Name</span></span>|<span data-ttu-id="0de3d-467">Название Markdown</span><span class="sxs-lookup"><span data-stu-id="0de3d-467">Markdown label</span></span>|
|-----|-------|
|<span data-ttu-id="0de3d-468">.NET Core CLI</span><span class="sxs-lookup"><span data-stu-id="0de3d-468">.NET Core CLI</span></span>|`dotnetcli`|
|<span data-ttu-id="0de3d-469">ASP.NET с C#</span><span class="sxs-lookup"><span data-stu-id="0de3d-469">ASP.NET with C#</span></span>|`aspx-csharp`|
|<span data-ttu-id="0de3d-470">ASP.NET с Visual Basic</span><span class="sxs-lookup"><span data-stu-id="0de3d-470">ASP.NET with VB</span></span>|`aspx-vb`|
|<span data-ttu-id="0de3d-471">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="0de3d-471">Azure CLI</span></span>|`azurecli`|
|<span data-ttu-id="0de3d-472">Azure CLI в браузере</span><span class="sxs-lookup"><span data-stu-id="0de3d-472">Azure CLI in browser</span></span>|`azurecli-interactive`|
|<span data-ttu-id="0de3d-473">Azure PowerShell в браузере</span><span class="sxs-lookup"><span data-stu-id="0de3d-473">Azure PowerShell in browser</span></span>|`azurepowershell-interactive`|
|<span data-ttu-id="0de3d-474">AzCopy</span><span class="sxs-lookup"><span data-stu-id="0de3d-474">AzCopy</span></span>|`azcopy`|
|<span data-ttu-id="0de3d-475">Bash</span><span class="sxs-lookup"><span data-stu-id="0de3d-475">Bash</span></span>|`bash`|
|<span data-ttu-id="0de3d-476">C++</span><span class="sxs-lookup"><span data-stu-id="0de3d-476">C++</span></span>|`cpp`|
|<span data-ttu-id="0de3d-477">C#</span><span class="sxs-lookup"><span data-stu-id="0de3d-477">C#</span></span>|`csharp`|
|<span data-ttu-id="0de3d-478">C# в браузере</span><span class="sxs-lookup"><span data-stu-id="0de3d-478">C# in browser</span></span>|`csharp-interactive`|
|<span data-ttu-id="0de3d-479">Консоль</span><span class="sxs-lookup"><span data-stu-id="0de3d-479">Console</span></span>|`console`|
|<span data-ttu-id="0de3d-480">CSHTML</span><span class="sxs-lookup"><span data-stu-id="0de3d-480">CSHTML</span></span>|`cshtml`|
|<span data-ttu-id="0de3d-481">DAX</span><span class="sxs-lookup"><span data-stu-id="0de3d-481">DAX</span></span>|`dax`|
|<span data-ttu-id="0de3d-482">Docker</span><span class="sxs-lookup"><span data-stu-id="0de3d-482">Docker</span></span>|`Dockerfile`|
|<span data-ttu-id="0de3d-483">F#</span><span class="sxs-lookup"><span data-stu-id="0de3d-483">F#</span></span>|`fsharp`|
|<span data-ttu-id="0de3d-484">HTML</span><span class="sxs-lookup"><span data-stu-id="0de3d-484">HTML</span></span>|`html`|
|<span data-ttu-id="0de3d-485">Java</span><span class="sxs-lookup"><span data-stu-id="0de3d-485">Java</span></span>|`java`|
|<span data-ttu-id="0de3d-486">JavaScript</span><span class="sxs-lookup"><span data-stu-id="0de3d-486">JavaScript</span></span>|`javascript`|
|<span data-ttu-id="0de3d-487">JSON</span><span class="sxs-lookup"><span data-stu-id="0de3d-487">JSON</span></span>|`json`|
|<span data-ttu-id="0de3d-488">Язык запросов Kusto</span><span class="sxs-lookup"><span data-stu-id="0de3d-488">Kusto Query Language</span></span>|`kusto`|
|<span data-ttu-id="0de3d-489">Markdown</span><span class="sxs-lookup"><span data-stu-id="0de3d-489">Markdown</span></span>|`md`|
|<span data-ttu-id="0de3d-490">Objective-C</span><span class="sxs-lookup"><span data-stu-id="0de3d-490">Objective-C</span></span>|`objc`|
|<span data-ttu-id="0de3d-491">PHP</span><span class="sxs-lookup"><span data-stu-id="0de3d-491">PHP</span></span>|`php`|
|<span data-ttu-id="0de3d-492">PowerShell</span><span class="sxs-lookup"><span data-stu-id="0de3d-492">PowerShell</span></span>|`powershell`|
|<span data-ttu-id="0de3d-493">Power Query M</span><span class="sxs-lookup"><span data-stu-id="0de3d-493">Power Query M</span></span>|`powerquery-m`|
|<span data-ttu-id="0de3d-494">protobuf</span><span class="sxs-lookup"><span data-stu-id="0de3d-494">protobuf</span></span>|`protobuf`|
|<span data-ttu-id="0de3d-495">Python</span><span class="sxs-lookup"><span data-stu-id="0de3d-495">Python</span></span>|`python`|
|<span data-ttu-id="0de3d-496">Ruby</span><span class="sxs-lookup"><span data-stu-id="0de3d-496">Ruby</span></span>|`ruby`|
|<span data-ttu-id="0de3d-497">SQL</span><span class="sxs-lookup"><span data-stu-id="0de3d-497">SQL</span></span>|`sql`|
|<span data-ttu-id="0de3d-498">Swift</span><span class="sxs-lookup"><span data-stu-id="0de3d-498">Swift</span></span>|`swift`|
|<span data-ttu-id="0de3d-499">VB</span><span class="sxs-lookup"><span data-stu-id="0de3d-499">VB</span></span>|`vb`|
|<span data-ttu-id="0de3d-500">XAML</span><span class="sxs-lookup"><span data-stu-id="0de3d-500">XAML</span></span>|`xaml`|
|<span data-ttu-id="0de3d-501">XML</span><span class="sxs-lookup"><span data-stu-id="0de3d-501">XML</span></span>|`xml`|
|<span data-ttu-id="0de3d-502">YAML</span><span class="sxs-lookup"><span data-stu-id="0de3d-502">YAML</span></span>|`yml`|

#### <a name="code-extensions"></a><span data-ttu-id="0de3d-503">Расширения кода</span><span class="sxs-lookup"><span data-stu-id="0de3d-503">Code extensions</span></span>

|<span data-ttu-id="0de3d-504">Имя</span><span class="sxs-lookup"><span data-stu-id="0de3d-504">Name</span></span>|<span data-ttu-id="0de3d-505">Название Markdown</span><span class="sxs-lookup"><span data-stu-id="0de3d-505">Markdown label</span></span>|<span data-ttu-id="0de3d-506">Расширение файла</span><span class="sxs-lookup"><span data-stu-id="0de3d-506">File extension</span></span>|
|-----|-------|-----|
|<span data-ttu-id="0de3d-507">C#</span><span class="sxs-lookup"><span data-stu-id="0de3d-507">C#</span></span>|<span data-ttu-id="0de3d-508">csharp</span><span class="sxs-lookup"><span data-stu-id="0de3d-508">csharp</span></span>|<span data-ttu-id="0de3d-509">.cs, .csx</span><span class="sxs-lookup"><span data-stu-id="0de3d-509">.cs, .csx</span></span>|
|<span data-ttu-id="0de3d-510">C++</span><span class="sxs-lookup"><span data-stu-id="0de3d-510">C++</span></span>|<span data-ttu-id="0de3d-511">cpp</span><span class="sxs-lookup"><span data-stu-id="0de3d-511">cpp</span></span>|<span data-ttu-id="0de3d-512">.cpp, .h</span><span class="sxs-lookup"><span data-stu-id="0de3d-512">.cpp, .h</span></span>|
|<span data-ttu-id="0de3d-513">F#</span><span class="sxs-lookup"><span data-stu-id="0de3d-513">F#</span></span>|<span data-ttu-id="0de3d-514">fsharp</span><span class="sxs-lookup"><span data-stu-id="0de3d-514">fsharp</span></span>|<span data-ttu-id="0de3d-515">.fs</span><span class="sxs-lookup"><span data-stu-id="0de3d-515">.fs</span></span>|
|<span data-ttu-id="0de3d-516">Java</span><span class="sxs-lookup"><span data-stu-id="0de3d-516">Java</span></span>|<span data-ttu-id="0de3d-517">java</span><span class="sxs-lookup"><span data-stu-id="0de3d-517">java</span></span>|<span data-ttu-id="0de3d-518">.java</span><span class="sxs-lookup"><span data-stu-id="0de3d-518">.java</span></span>|
|<span data-ttu-id="0de3d-519">JavaScript</span><span class="sxs-lookup"><span data-stu-id="0de3d-519">JavaScript</span></span>|<span data-ttu-id="0de3d-520">javascript</span><span class="sxs-lookup"><span data-stu-id="0de3d-520">javascript</span></span>|<span data-ttu-id="0de3d-521">.js</span><span class="sxs-lookup"><span data-stu-id="0de3d-521">.js</span></span>|
|<span data-ttu-id="0de3d-522">Python</span><span class="sxs-lookup"><span data-stu-id="0de3d-522">Python</span></span>|<span data-ttu-id="0de3d-523">python</span><span class="sxs-lookup"><span data-stu-id="0de3d-523">python</span></span>|<span data-ttu-id="0de3d-524">.py</span><span class="sxs-lookup"><span data-stu-id="0de3d-524">.py</span></span>|
|<span data-ttu-id="0de3d-525">SQL</span><span class="sxs-lookup"><span data-stu-id="0de3d-525">SQL</span></span>|<span data-ttu-id="0de3d-526">sql</span><span class="sxs-lookup"><span data-stu-id="0de3d-526">sql</span></span>|<span data-ttu-id="0de3d-527">.sql</span><span class="sxs-lookup"><span data-stu-id="0de3d-527">.sql</span></span>|
|<span data-ttu-id="0de3d-528">VB</span><span class="sxs-lookup"><span data-stu-id="0de3d-528">VB</span></span>|<span data-ttu-id="0de3d-529">vb</span><span class="sxs-lookup"><span data-stu-id="0de3d-529">vb</span></span>|<span data-ttu-id="0de3d-530">.vb</span><span class="sxs-lookup"><span data-stu-id="0de3d-530">.vb</span></span>|
|<span data-ttu-id="0de3d-531">XAML</span><span class="sxs-lookup"><span data-stu-id="0de3d-531">XAML</span></span>|<span data-ttu-id="0de3d-532">xaml</span><span class="sxs-lookup"><span data-stu-id="0de3d-532">xaml</span></span>|<span data-ttu-id="0de3d-533">.xaml</span><span class="sxs-lookup"><span data-stu-id="0de3d-533">.xaml</span></span>|
|<span data-ttu-id="0de3d-534">XML</span><span class="sxs-lookup"><span data-stu-id="0de3d-534">XML</span></span>|<span data-ttu-id="0de3d-535">xml</span><span class="sxs-lookup"><span data-stu-id="0de3d-535">xml</span></span>|<span data-ttu-id="0de3d-536">.xml</span><span class="sxs-lookup"><span data-stu-id="0de3d-536">.xml</span></span>|

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="0de3d-537">Сбои и устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="0de3d-537">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="0de3d-538">Замещающий текст</span><span class="sxs-lookup"><span data-stu-id="0de3d-538">Alt text</span></span>

<span data-ttu-id="0de3d-539">Замещающий текст, который содержит символы подчеркивания, отображается некорректно.</span><span class="sxs-lookup"><span data-stu-id="0de3d-539">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="0de3d-540">Например, вместо</span><span class="sxs-lookup"><span data-stu-id="0de3d-540">For example, instead of using this:</span></span>

```md
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="0de3d-541">используйте следующий вариант, позволяющий избежать символов подчеркивания:</span><span class="sxs-lookup"><span data-stu-id="0de3d-541">Escape the underscores like this:</span></span>

```md
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="0de3d-542">Апострофы и кавычки</span><span class="sxs-lookup"><span data-stu-id="0de3d-542">Apostrophes and quotation marks</span></span>

<span data-ttu-id="0de3d-543">Если вы копируете текст из Word в редактор Markdown, он может содержать книжные (изогнутые) апострофы или кавычки.</span><span class="sxs-lookup"><span data-stu-id="0de3d-543">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="0de3d-544">Их нужно заменить кодом или обычными апострофами или кавычками.</span><span class="sxs-lookup"><span data-stu-id="0de3d-544">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="0de3d-545">В противном случае после публикации файла может отобразиться нечитаемый текст, например: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="0de3d-545">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="0de3d-546">Ниже приведены кодировки для этих знаков пунктуации:</span><span class="sxs-lookup"><span data-stu-id="0de3d-546">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="0de3d-547">левая (открывающая) кавычка: `&#8220;`;</span><span class="sxs-lookup"><span data-stu-id="0de3d-547">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="0de3d-548">правая (закрывающая) кавычка: `&#8221;`;</span><span class="sxs-lookup"><span data-stu-id="0de3d-548">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="0de3d-549">правая закрывающая одинарная кавычка или апостроф: `&#8217;`;</span><span class="sxs-lookup"><span data-stu-id="0de3d-549">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="0de3d-550">левая открывающая одинарная кавычка (используется редко): `&#8216;`.</span><span class="sxs-lookup"><span data-stu-id="0de3d-550">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="0de3d-551">Угловые скобки</span><span class="sxs-lookup"><span data-stu-id="0de3d-551">Angle brackets</span></span>

<span data-ttu-id="0de3d-552">Угловые скобки, как правило, используются для обозначения заполнителя.</span><span class="sxs-lookup"><span data-stu-id="0de3d-552">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="0de3d-553">Если вы используете угловые скобки в тексте (а не в коде), их необходимо закодировать.</span><span class="sxs-lookup"><span data-stu-id="0de3d-553">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="0de3d-554">В противном случае разметка Markdown считает их HTML-тегами.</span><span class="sxs-lookup"><span data-stu-id="0de3d-554">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="0de3d-555">Например, `<script name>` следует закодировать как `&lt;script name&gt;`.</span><span class="sxs-lookup"><span data-stu-id="0de3d-555">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="markdown-flavor"></a><span data-ttu-id="0de3d-556">Тип разметки Markdown</span><span class="sxs-lookup"><span data-stu-id="0de3d-556">Markdown flavor</span></span>

<span data-ttu-id="0de3d-557">Серверная часть сайта docs.microsoft.com поддерживает разметку Markdown в соответствии с [CommonMark](https://commonmark.org/) и ее синтаксический анализ через подсистему [Markdig](https://github.com/lunet-io/markdig).</span><span class="sxs-lookup"><span data-stu-id="0de3d-557">The docs.microsoft.com site backend supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="0de3d-558">Такой тип разметки совместим с [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), так как большинство документов хранятся на GitHub, где их можно править.</span><span class="sxs-lookup"><span data-stu-id="0de3d-558">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="0de3d-559">Дополнительные функции добавляются с помощью расширений Markdown.</span><span class="sxs-lookup"><span data-stu-id="0de3d-559">Additional functionality is added through Markdown extensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="0de3d-560">Дополнительные материалы</span><span class="sxs-lookup"><span data-stu-id="0de3d-560">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="0de3d-561">Ресурсы Markdown</span><span class="sxs-lookup"><span data-stu-id="0de3d-561">Markdown resources</span></span>

- <span data-ttu-id="0de3d-562">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax) (Синтаксис Markdown)</span><span class="sxs-lookup"><span data-stu-id="0de3d-562">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- <span data-ttu-id="0de3d-563">[Markdown cheat-sheet](./media/documents/markdown-cheatsheet.pdf?raw=true) (Шпаргалка по Markdown)</span><span class="sxs-lookup"><span data-stu-id="0de3d-563">[Docs Markdown cheat sheet](./media/documents/markdown-cheatsheet.pdf?raw=true)</span></span>
- [<span data-ttu-id="0de3d-564">Базовые сведения о разметке Markdown на GitHub</span><span class="sxs-lookup"><span data-stu-id="0de3d-564">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- <span data-ttu-id="0de3d-565">[The Markdown Guide](https://www.markdownguide.org/) (Руководство по Markdown)</span><span class="sxs-lookup"><span data-stu-id="0de3d-565">[The Markdown Guide](https://www.markdownguide.org/)</span></span>
