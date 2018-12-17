---
title: Использование языка разметки Markdown для написания документации
description: В этой статье приводятся базовые и справочные сведения о языке разметки Markdown, используемом для написания статей на сайте docs.microsoft.com.
ms.date: 07/13/2017
ms.openlocfilehash: 8613d525afc11caf9ec760c4f15ea44010781634
ms.sourcegitcommit: 21c9ac71e1abff946466cddf17a1ee97bc349ec5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2018
ms.locfileid: "53245902"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="b6001-103">Использование языка разметки Markdown для написания документации</span><span class="sxs-lookup"><span data-stu-id="b6001-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="b6001-104">Статьи на сайте [docs.microsoft.com](http://docs.microsoft.com) написаны на [Markdown](https://daringfireball.net/projects/markdown/) — упрощенном языке разметки, который легко использовать и изучать.</span><span class="sxs-lookup"><span data-stu-id="b6001-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="b6001-105">Благодаря своей простоте он быстро становится отраслевым стандартом.</span><span class="sxs-lookup"><span data-stu-id="b6001-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="b6001-106">Так как документация хранится в репозитории GitHub, для нее можно использовать расширенный набор Markdown под названием [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/). Этот формат предусматривает дополнительные возможности для решения распространенных задач.</span><span class="sxs-lookup"><span data-stu-id="b6001-106">Since Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="b6001-107">Кроме того, службы Open Publishing Services (OPS) используют Markdig, синтаксический анализатор Markdown.</span><span class="sxs-lookup"><span data-stu-id="b6001-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="b6001-108">Он обеспечивает высокую совместимость с диалектом GFM, предоставляя дополнительные функции для работы с документацией.</span><span class="sxs-lookup"><span data-stu-id="b6001-108">Markdig is highly compatible with GFM, adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="b6001-109">Markdig — это быстрый и мощный обработчик Markdown для .NET, обеспечивающий соответствие CommonMark и поддержку расширений.</span><span class="sxs-lookup"><span data-stu-id="b6001-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="b6001-110">Улучшенная поддержка сообщества</span><span class="sxs-lookup"><span data-stu-id="b6001-110">Better community support</span></span>
* <span data-ttu-id="b6001-111">Улучшенная поддержка стандартов</span><span class="sxs-lookup"><span data-stu-id="b6001-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="b6001-112">Базовые сведения о Markdown</span><span class="sxs-lookup"><span data-stu-id="b6001-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="b6001-113">Заголовки</span><span class="sxs-lookup"><span data-stu-id="b6001-113">Headings</span></span>

<span data-ttu-id="b6001-114">Чтобы создать заголовок, используйте знак (#), например:</span><span class="sxs-lookup"><span data-stu-id="b6001-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="b6001-115">В заголовках следует использовать стиль atx, то есть 1–6 символов решетки (#) в начале строки, чтобы указать на заголовок, соответствующий заголовкам HTML уровней с H1 по H6.</span><span class="sxs-lookup"><span data-stu-id="b6001-115">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="b6001-116">Сверху приводятся примеры заголовков с первого по четвертый уровень.</span><span class="sxs-lookup"><span data-stu-id="b6001-116">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="b6001-117">В статье **должен** быть только один заголовок первого уровня (H1), который будет отображаться как заголовок страницы.</span><span class="sxs-lookup"><span data-stu-id="b6001-117">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="b6001-118">Если заголовок заканчивается на символ `#`, добавьте в конце еще символ `#`, чтобы заголовок отображался правильно.</span><span class="sxs-lookup"><span data-stu-id="b6001-118">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="b6001-119">Например, `# Async Programming in F# #`.</span><span class="sxs-lookup"><span data-stu-id="b6001-119">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="b6001-120">Заголовки второго уровня создадут оглавление, которое будет отображаться в разделе "В этой статье" под заголовком статьи.</span><span class="sxs-lookup"><span data-stu-id="b6001-120">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="b6001-121">Полужирное начертание и курсив</span><span class="sxs-lookup"><span data-stu-id="b6001-121">Bold and italic text</span></span>

<span data-ttu-id="b6001-122">Чтобы задать для текста **полужирное начертание**, заключите его в двойные звездочки:</span><span class="sxs-lookup"><span data-stu-id="b6001-122">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="b6001-123">Чтобы задать для текста *курсивное начертание*, заключите его в одинарные звездочки:</span><span class="sxs-lookup"><span data-stu-id="b6001-123">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="b6001-124">Чтобы задать для текста ***полужирное и курсивное*** начертание, заключите его в тройные звездочки:</span><span class="sxs-lookup"><span data-stu-id="b6001-124">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="b6001-125">Блоки цитирования</span><span class="sxs-lookup"><span data-stu-id="b6001-125">Blockquotes</span></span>

<span data-ttu-id="b6001-126">Блоки цитирования создаются с помощью символа `>`:</span><span class="sxs-lookup"><span data-stu-id="b6001-126">Blockquotes are created using the `>` character:</span></span>

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="b6001-127">Предыдущий пример отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b6001-127">The preceding example renders as follows:</span></span>

> <span data-ttu-id="b6001-128">Засуха продолжалась десять миллионов лет, и царству ужасных ящеров уже давно пришел конец.</span><span class="sxs-lookup"><span data-stu-id="b6001-128">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="b6001-129">Здесь, близ экватора, на материке, который позднее назовут Африкой, с новой яростью вспыхнула борьба за существование, и еще не ясно было, кто выйдет из нее победителем.</span><span class="sxs-lookup"><span data-stu-id="b6001-129">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="b6001-130">На этой бесплодной, иссушенной зноем земле благоденствовать или хотя бы просто выжить могли только маленькие, или ловкие, или свирепые.</span><span class="sxs-lookup"><span data-stu-id="b6001-130">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="b6001-131">Списки</span><span class="sxs-lookup"><span data-stu-id="b6001-131">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="b6001-132">Неупорядоченный список</span><span class="sxs-lookup"><span data-stu-id="b6001-132">Unordered list</span></span>

<span data-ttu-id="b6001-133">Неупорядоченный (маркированный) список можно отформатировать с помощью звездочек или тире.</span><span class="sxs-lookup"><span data-stu-id="b6001-133">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="b6001-134">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="b6001-134">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="b6001-135">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="b6001-135">will be rendered as:</span></span>

- <span data-ttu-id="b6001-136">List item 1</span><span class="sxs-lookup"><span data-stu-id="b6001-136">List item 1</span></span>
- <span data-ttu-id="b6001-137">List item 2</span><span class="sxs-lookup"><span data-stu-id="b6001-137">List item 2</span></span>
- <span data-ttu-id="b6001-138">List item 3</span><span class="sxs-lookup"><span data-stu-id="b6001-138">List item 3</span></span>

<span data-ttu-id="b6001-139">Чтобы вложить один список в другой, добавьте отступ для элементов дочернего списка.</span><span class="sxs-lookup"><span data-stu-id="b6001-139">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="b6001-140">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="b6001-140">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="b6001-141">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="b6001-141">will be rendered as:</span></span>

- <span data-ttu-id="b6001-142">List item 1</span><span class="sxs-lookup"><span data-stu-id="b6001-142">List item 1</span></span>
  - <span data-ttu-id="b6001-143">List item A</span><span class="sxs-lookup"><span data-stu-id="b6001-143">List item A</span></span>
  - <span data-ttu-id="b6001-144">List item B</span><span class="sxs-lookup"><span data-stu-id="b6001-144">List item B</span></span>
- <span data-ttu-id="b6001-145">List item 2</span><span class="sxs-lookup"><span data-stu-id="b6001-145">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="b6001-146">Упорядоченный список</span><span class="sxs-lookup"><span data-stu-id="b6001-146">Ordered list</span></span>

<span data-ttu-id="b6001-147">Упорядоченный (ступенчатый) список можно отформатировать с помощью соответствующих цифр.</span><span class="sxs-lookup"><span data-stu-id="b6001-147">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="b6001-148">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="b6001-148">For example, the following Markdown:</span></span>

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="b6001-149">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="b6001-149">will be rendered as:</span></span>

1. <span data-ttu-id="b6001-150">First instruction</span><span class="sxs-lookup"><span data-stu-id="b6001-150">First instruction</span></span>
2. <span data-ttu-id="b6001-151">Second instruction</span><span class="sxs-lookup"><span data-stu-id="b6001-151">Second instruction</span></span>
3. <span data-ttu-id="b6001-152">Third instruction</span><span class="sxs-lookup"><span data-stu-id="b6001-152">Third instruction</span></span>

<span data-ttu-id="b6001-153">Чтобы вложить один список в другой, добавьте отступ для элементов дочернего списка.</span><span class="sxs-lookup"><span data-stu-id="b6001-153">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="b6001-154">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="b6001-154">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="b6001-155">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="b6001-155">will be rendered as:</span></span>

1. <span data-ttu-id="b6001-156">First instruction</span><span class="sxs-lookup"><span data-stu-id="b6001-156">First instruction</span></span>
   1. <span data-ttu-id="b6001-157">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="b6001-157">Sub-instruction</span></span>
   2. <span data-ttu-id="b6001-158">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="b6001-158">Sub-instruction</span></span>
2. <span data-ttu-id="b6001-159">Second instruction</span><span class="sxs-lookup"><span data-stu-id="b6001-159">Second instruction</span></span>

<span data-ttu-id="b6001-160">Обратите внимание, что мы используем "1."</span><span class="sxs-lookup"><span data-stu-id="b6001-160">Note that we use '1.'</span></span> <span data-ttu-id="b6001-161">для всех записей.</span><span class="sxs-lookup"><span data-stu-id="b6001-161">for all entries.</span></span> <span data-ttu-id="b6001-162">Так проще увидеть различия, когда потом будут добавлены новые шаги или удалены существующие.</span><span class="sxs-lookup"><span data-stu-id="b6001-162">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="b6001-163">Tables</span><span class="sxs-lookup"><span data-stu-id="b6001-163">Tables</span></span>

<span data-ttu-id="b6001-164">Таблицы не входят в основную спецификацию Markdown, но их поддерживает GFM.</span><span class="sxs-lookup"><span data-stu-id="b6001-164">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="b6001-165">Создавать таблицы можно с помощью символов вертикальной черты (|) и дефиса (-).</span><span class="sxs-lookup"><span data-stu-id="b6001-165">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="b6001-166">Дефисы позволяют создавать для каждого столбца заголовок. Вертикальные черты разделяют столбцы.</span><span class="sxs-lookup"><span data-stu-id="b6001-166">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="b6001-167">Чтобы таблица правильно отображалась, включите перед ней пустую строку.</span><span class="sxs-lookup"><span data-stu-id="b6001-167">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="b6001-168">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="b6001-168">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="b6001-169">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="b6001-169">will be rendered as:</span></span>

| <span data-ttu-id="b6001-170">Fun</span><span class="sxs-lookup"><span data-stu-id="b6001-170">Fun</span></span>                  | <span data-ttu-id="b6001-171">with</span><span class="sxs-lookup"><span data-stu-id="b6001-171">With</span></span>                 | <span data-ttu-id="b6001-172">Tables</span><span class="sxs-lookup"><span data-stu-id="b6001-172">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="b6001-173">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="b6001-173">left-aligned column</span></span>  | <span data-ttu-id="b6001-174">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="b6001-174">right-aligned column</span></span> | <span data-ttu-id="b6001-175">centered column</span><span class="sxs-lookup"><span data-stu-id="b6001-175">centered column</span></span> |
| <span data-ttu-id="b6001-176">$100</span><span class="sxs-lookup"><span data-stu-id="b6001-176">$100</span></span>                 | <span data-ttu-id="b6001-177">$100</span><span class="sxs-lookup"><span data-stu-id="b6001-177">$100</span></span>                 | <span data-ttu-id="b6001-178">$100</span><span class="sxs-lookup"><span data-stu-id="b6001-178">$100</span></span>            |
| <span data-ttu-id="b6001-179">$10</span><span class="sxs-lookup"><span data-stu-id="b6001-179">$10</span></span>                  | <span data-ttu-id="b6001-180">$10</span><span class="sxs-lookup"><span data-stu-id="b6001-180">$10</span></span>                  | <span data-ttu-id="b6001-181">$10</span><span class="sxs-lookup"><span data-stu-id="b6001-181">$10</span></span>             |
| <span data-ttu-id="b6001-182">$1</span><span class="sxs-lookup"><span data-stu-id="b6001-182">$1</span></span>                   | <span data-ttu-id="b6001-183">$1</span><span class="sxs-lookup"><span data-stu-id="b6001-183">$1</span></span>                   | <span data-ttu-id="b6001-184">$1</span><span class="sxs-lookup"><span data-stu-id="b6001-184">$1</span></span>              |

<span data-ttu-id="b6001-185">Дополнительные сведения о создании таблиц:</span><span class="sxs-lookup"><span data-stu-id="b6001-185">For more information on creating tables, see:</span></span>

- <span data-ttu-id="b6001-186">[Функция обтекания таблиц](#table-wrapping) в Markdig, которая поможет при форматировании широких таблиц.</span><span class="sxs-lookup"><span data-stu-id="b6001-186">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="b6001-187">Статья на сайте GitHub [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/) (Организация информации с помощью таблиц).</span><span class="sxs-lookup"><span data-stu-id="b6001-187">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="b6001-188">Веб-приложение [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="b6001-188">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="b6001-189">Статья Адама Притчарда (Adam Pritchard) [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables) (Шпаргалка по Markdown).</span><span class="sxs-lookup"><span data-stu-id="b6001-189">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="b6001-190">Статья Майкла Фортина (Michel Fortin) [Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) (Расширение Markdown Extra).</span><span class="sxs-lookup"><span data-stu-id="b6001-190">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="b6001-191">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/) (Преобразование таблиц HTML в Markdown).</span><span class="sxs-lookup"><span data-stu-id="b6001-191">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="b6001-192">Создание ссылок</span><span class="sxs-lookup"><span data-stu-id="b6001-192">Links</span></span>

<span data-ttu-id="b6001-193">Синтаксис Markdown для встроенной ссылки состоит из части `[link text]`, представляющей текст гиперссылки, и части `(file-name.md)` — URL-адреса или имени файла, на который дается ссылка:</span><span class="sxs-lookup"><span data-stu-id="b6001-193">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="b6001-194">Дополнительные сведения о ссылках:</span><span class="sxs-lookup"><span data-stu-id="b6001-194">For more information on linking, see:</span></span>

- <span data-ttu-id="b6001-195">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax#link) (Руководство по синтаксису Markdown), в котором предоставлена основная информация по поддержке ссылок Markdown.</span><span class="sxs-lookup"><span data-stu-id="b6001-195">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="b6001-196">Страница [Ссылки](how-to-write-links.md) в этом руководстве содержит сведения о дополнительном синтаксисе Markdig для ссылок.</span><span class="sxs-lookup"><span data-stu-id="b6001-196">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="b6001-197">Фрагменты кода</span><span class="sxs-lookup"><span data-stu-id="b6001-197">Code snippets</span></span>

<span data-ttu-id="b6001-198">Markdown поддерживает как встраивание фрагментов кода в предложение, так и их размещение между предложениями в виде отдельных огражденных блоков.</span><span class="sxs-lookup"><span data-stu-id="b6001-198">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="b6001-199">Дополнительная информация:</span><span class="sxs-lookup"><span data-stu-id="b6001-199">For details, see:</span></span>

- [<span data-ttu-id="b6001-200">Сведения о собственной поддержке блоков кода Markdown</span><span class="sxs-lookup"><span data-stu-id="b6001-200">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="b6001-201">Сведения о поддержке GFM для ограждения кода и выделения синтаксиса</span><span class="sxs-lookup"><span data-stu-id="b6001-201">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="b6001-202">Огражденные блоки кода — это простой способ выделить синтаксис для фрагментов кода.</span><span class="sxs-lookup"><span data-stu-id="b6001-202">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="b6001-203">Общий формат огражденных блоков кода:</span><span class="sxs-lookup"><span data-stu-id="b6001-203">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="b6001-204">Псевдоним после трех начальных символов обратной галочки \` определяет использование выделения.</span><span class="sxs-lookup"><span data-stu-id="b6001-204">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="b6001-205">Ниже представлен список часто используемых языков программирования для написания документации и приводятся соответствующие метки.</span><span class="sxs-lookup"><span data-stu-id="b6001-205">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="b6001-206">Все эти языки поддерживают понятные имена, а большинство из них — выделение языка в имени.</span><span class="sxs-lookup"><span data-stu-id="b6001-206">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="b6001-207">Имя</span><span class="sxs-lookup"><span data-stu-id="b6001-207">Name</span></span>|<span data-ttu-id="b6001-208">Метка Markdown</span><span class="sxs-lookup"><span data-stu-id="b6001-208">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="b6001-209">.NET Console</span><span class="sxs-lookup"><span data-stu-id="b6001-209">.NET Console</span></span>|<span data-ttu-id="b6001-210">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="b6001-210">dotnetcli</span></span>|
|<span data-ttu-id="b6001-211">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="b6001-211">ASP.NET (C#)</span></span>|<span data-ttu-id="b6001-212">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="b6001-212">aspx-csharp</span></span>|
|<span data-ttu-id="b6001-213">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="b6001-213">ASP.NET (VB)</span></span>|<span data-ttu-id="b6001-214">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="b6001-214">aspx-vb</span></span>|
|<span data-ttu-id="b6001-215">AzCopy</span><span class="sxs-lookup"><span data-stu-id="b6001-215">AzCopy</span></span>|<span data-ttu-id="b6001-216">azcopy</span><span class="sxs-lookup"><span data-stu-id="b6001-216">azcopy</span></span>|
|<span data-ttu-id="b6001-217">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="b6001-217">Azure CLI</span></span>|<span data-ttu-id="b6001-218">azurecli</span><span class="sxs-lookup"><span data-stu-id="b6001-218">azurecli</span></span>|
|<span data-ttu-id="b6001-219">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b6001-219">Azure PowerShell</span></span>|<span data-ttu-id="b6001-220">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="b6001-220">azurepowershell</span></span>|
|<span data-ttu-id="b6001-221">C++</span><span class="sxs-lookup"><span data-stu-id="b6001-221">C++</span></span>|<span data-ttu-id="b6001-222">cpp</span><span class="sxs-lookup"><span data-stu-id="b6001-222">cpp</span></span>|
|<span data-ttu-id="b6001-223">C++/CX</span><span class="sxs-lookup"><span data-stu-id="b6001-223">C++/CX</span></span>|<span data-ttu-id="b6001-224">cppcx</span><span class="sxs-lookup"><span data-stu-id="b6001-224">cppcx</span></span>|
|<span data-ttu-id="b6001-225">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="b6001-225">C++/WinRT</span></span>|<span data-ttu-id="b6001-226">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="b6001-226">cppwinrt</span></span>|
|<span data-ttu-id="b6001-227">C#</span><span class="sxs-lookup"><span data-stu-id="b6001-227">C#</span></span>|<span data-ttu-id="b6001-228">csharp</span><span class="sxs-lookup"><span data-stu-id="b6001-228">csharp</span></span>|
|<span data-ttu-id="b6001-229">C# в браузере</span><span class="sxs-lookup"><span data-stu-id="b6001-229">C# in browser</span></span>|<span data-ttu-id="b6001-230">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="b6001-230">csharp-interactive</span></span>|
|<span data-ttu-id="b6001-231">Консоль</span><span class="sxs-lookup"><span data-stu-id="b6001-231">Console</span></span>|<span data-ttu-id="b6001-232">консоль</span><span class="sxs-lookup"><span data-stu-id="b6001-232">console</span></span>|
|<span data-ttu-id="b6001-233">CSHTML</span><span class="sxs-lookup"><span data-stu-id="b6001-233">CSHTML</span></span>|<span data-ttu-id="b6001-234">cshtml</span><span class="sxs-lookup"><span data-stu-id="b6001-234">cshtml</span></span>|
|<span data-ttu-id="b6001-235">DAX</span><span class="sxs-lookup"><span data-stu-id="b6001-235">DAX</span></span>|<span data-ttu-id="b6001-236">dax</span><span class="sxs-lookup"><span data-stu-id="b6001-236">dax</span></span>|
|<span data-ttu-id="b6001-237">F#</span><span class="sxs-lookup"><span data-stu-id="b6001-237">F#</span></span>|<span data-ttu-id="b6001-238">fsharp</span><span class="sxs-lookup"><span data-stu-id="b6001-238">fsharp</span></span>|
|<span data-ttu-id="b6001-239">Go</span><span class="sxs-lookup"><span data-stu-id="b6001-239">Go</span></span>|<span data-ttu-id="b6001-240">go</span><span class="sxs-lookup"><span data-stu-id="b6001-240">go</span></span>|
|<span data-ttu-id="b6001-241">HTML</span><span class="sxs-lookup"><span data-stu-id="b6001-241">HTML</span></span>|<span data-ttu-id="b6001-242">html</span><span class="sxs-lookup"><span data-stu-id="b6001-242">html</span></span>|
|<span data-ttu-id="b6001-243">HTTP</span><span class="sxs-lookup"><span data-stu-id="b6001-243">HTTP</span></span>|<span data-ttu-id="b6001-244">http</span><span class="sxs-lookup"><span data-stu-id="b6001-244">http</span></span>|
|<span data-ttu-id="b6001-245">Java</span><span class="sxs-lookup"><span data-stu-id="b6001-245">Java</span></span>|<span data-ttu-id="b6001-246">java</span><span class="sxs-lookup"><span data-stu-id="b6001-246">java</span></span>|
|<span data-ttu-id="b6001-247">JavaScript</span><span class="sxs-lookup"><span data-stu-id="b6001-247">JavaScript</span></span>|<span data-ttu-id="b6001-248">javascript</span><span class="sxs-lookup"><span data-stu-id="b6001-248">javascript</span></span>|
|<span data-ttu-id="b6001-249">JSON</span><span class="sxs-lookup"><span data-stu-id="b6001-249">JSON</span></span>|<span data-ttu-id="b6001-250">json</span><span class="sxs-lookup"><span data-stu-id="b6001-250">json</span></span>|
|<span data-ttu-id="b6001-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="b6001-251">Markdown</span></span>|<span data-ttu-id="b6001-252">md</span><span class="sxs-lookup"><span data-stu-id="b6001-252">md</span></span>|
|<span data-ttu-id="b6001-253">NodeJS</span><span class="sxs-lookup"><span data-stu-id="b6001-253">NodeJS</span></span>|<span data-ttu-id="b6001-254">nodejs</span><span class="sxs-lookup"><span data-stu-id="b6001-254">nodejs</span></span>|
|<span data-ttu-id="b6001-255">Objective-C</span><span class="sxs-lookup"><span data-stu-id="b6001-255">Objective-C</span></span>|<span data-ttu-id="b6001-256">objc</span><span class="sxs-lookup"><span data-stu-id="b6001-256">objc</span></span>|
|<span data-ttu-id="b6001-257">OData</span><span class="sxs-lookup"><span data-stu-id="b6001-257">OData</span></span>|<span data-ttu-id="b6001-258">odata</span><span class="sxs-lookup"><span data-stu-id="b6001-258">odata</span></span>|
|<span data-ttu-id="b6001-259">PHP</span><span class="sxs-lookup"><span data-stu-id="b6001-259">PHP</span></span>|<span data-ttu-id="b6001-260">php</span><span class="sxs-lookup"><span data-stu-id="b6001-260">php</span></span>|
|<span data-ttu-id="b6001-261">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="b6001-261">Power Apps Formula</span></span>|<span data-ttu-id="b6001-262">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="b6001-262">powerappsfl</span></span>|
|<span data-ttu-id="b6001-263">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b6001-263">PowerShell</span></span>|<span data-ttu-id="b6001-264">powershell</span><span class="sxs-lookup"><span data-stu-id="b6001-264">powershell</span></span>|
|<span data-ttu-id="b6001-265">Python</span><span class="sxs-lookup"><span data-stu-id="b6001-265">Python</span></span>|<span data-ttu-id="b6001-266">python</span><span class="sxs-lookup"><span data-stu-id="b6001-266">python</span></span>|
|<span data-ttu-id="b6001-267">Q#</span><span class="sxs-lookup"><span data-stu-id="b6001-267">Q#</span></span>|<span data-ttu-id="b6001-268">qsharp</span><span class="sxs-lookup"><span data-stu-id="b6001-268">qsharp</span></span>|
|<span data-ttu-id="b6001-269">R</span><span class="sxs-lookup"><span data-stu-id="b6001-269">R</span></span>|<span data-ttu-id="b6001-270">r</span><span class="sxs-lookup"><span data-stu-id="b6001-270">r</span></span>|
|<span data-ttu-id="b6001-271">Ruby</span><span class="sxs-lookup"><span data-stu-id="b6001-271">Ruby</span></span>|<span data-ttu-id="b6001-272">ruby</span><span class="sxs-lookup"><span data-stu-id="b6001-272">ruby</span></span>|
|<span data-ttu-id="b6001-273">SQL</span><span class="sxs-lookup"><span data-stu-id="b6001-273">SQL</span></span>|<span data-ttu-id="b6001-274">sql</span><span class="sxs-lookup"><span data-stu-id="b6001-274">sql</span></span>|
|<span data-ttu-id="b6001-275">Swift</span><span class="sxs-lookup"><span data-stu-id="b6001-275">Swift</span></span>|<span data-ttu-id="b6001-276">swift</span><span class="sxs-lookup"><span data-stu-id="b6001-276">swift</span></span>|
|<span data-ttu-id="b6001-277">TypeScript</span><span class="sxs-lookup"><span data-stu-id="b6001-277">TypeScript</span></span>|<span data-ttu-id="b6001-278">typescript</span><span class="sxs-lookup"><span data-stu-id="b6001-278">typescript</span></span>|
|<span data-ttu-id="b6001-279">VB</span><span class="sxs-lookup"><span data-stu-id="b6001-279">VB</span></span>|<span data-ttu-id="b6001-280">vb</span><span class="sxs-lookup"><span data-stu-id="b6001-280">vb</span></span>|
|<span data-ttu-id="b6001-281">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="b6001-281">VSTS CLI</span></span>|<span data-ttu-id="b6001-282">vstscli</span><span class="sxs-lookup"><span data-stu-id="b6001-282">vstscli</span></span>|
|<span data-ttu-id="b6001-283">XAML</span><span class="sxs-lookup"><span data-stu-id="b6001-283">XAML</span></span>|<span data-ttu-id="b6001-284">xaml</span><span class="sxs-lookup"><span data-stu-id="b6001-284">xaml</span></span>|
|<span data-ttu-id="b6001-285">XML</span><span class="sxs-lookup"><span data-stu-id="b6001-285">XML</span></span>|<span data-ttu-id="b6001-286">xml</span><span class="sxs-lookup"><span data-stu-id="b6001-286">xml</span></span>|

<span data-ttu-id="b6001-287">Имя `csharp-interactive` указывает на язык C# и возможность запускать примеры в браузере.</span><span class="sxs-lookup"><span data-stu-id="b6001-287">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="b6001-288">Эти фрагменты кода компилируются и выполняются в контейнере Docker, а результаты выполнения программы отображаются в окне браузера пользователя.</span><span class="sxs-lookup"><span data-stu-id="b6001-288">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="b6001-289">Пример. C\#</span><span class="sxs-lookup"><span data-stu-id="b6001-289">Example: C\#</span></span>

<span data-ttu-id="b6001-290">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="b6001-290">__Markdown__</span></span>

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

<span data-ttu-id="b6001-291">__Отображение__</span><span class="sxs-lookup"><span data-stu-id="b6001-291">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="b6001-292">Пример. SQL</span><span class="sxs-lookup"><span data-stu-id="b6001-292">Example: SQL</span></span>

<span data-ttu-id="b6001-293">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="b6001-293">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="b6001-294">__Отображение__</span><span class="sxs-lookup"><span data-stu-id="b6001-294">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="b6001-295">Настраиваемые расширения OPS для Markdown</span><span class="sxs-lookup"><span data-stu-id="b6001-295">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="b6001-296">Службы Open Publishing Services (OPS) используют Markdig, синтаксический анализатор Markdown, обеспечивающий высокую совместимость с диалектом GitHub Flavored Markdown (GFM).</span><span class="sxs-lookup"><span data-stu-id="b6001-296">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="b6001-297">Markdig добавляет дополнительные функции за счет расширений Markdown.</span><span class="sxs-lookup"><span data-stu-id="b6001-297">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="b6001-298">Поэтому для справки мы включили в этот материал некоторые разделы из руководства по разработке OPS.</span><span class="sxs-lookup"><span data-stu-id="b6001-298">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="b6001-299">(Например, см. в содержании разделы "Markdig и расширения Markdown" и "Фрагменты кода".)</span><span class="sxs-lookup"><span data-stu-id="b6001-299">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="b6001-300">В статьях документации для общего форматирования, например для создания абзацев, ссылок, списков и заголовков, используется GFM.</span><span class="sxs-lookup"><span data-stu-id="b6001-300">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="b6001-301">Для расширенного форматирования в статьях можно использовать следующие функции Markdig:</span><span class="sxs-lookup"><span data-stu-id="b6001-301">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="b6001-302">Блоки заметок</span><span class="sxs-lookup"><span data-stu-id="b6001-302">Note blocks</span></span>
- <span data-ttu-id="b6001-303">Включаемые файлы</span><span class="sxs-lookup"><span data-stu-id="b6001-303">Include files</span></span>
- <span data-ttu-id="b6001-304">Селекторы</span><span class="sxs-lookup"><span data-stu-id="b6001-304">Selectors</span></span>
- <span data-ttu-id="b6001-305">внедренные видео;</span><span class="sxs-lookup"><span data-stu-id="b6001-305">Embedded videos</span></span>
- <span data-ttu-id="b6001-306">фрагменты или примеры кода.</span><span class="sxs-lookup"><span data-stu-id="b6001-306">Code snippets/samples</span></span>

<span data-ttu-id="b6001-307">Полный список см. в разделах "Markdig и расширения Markdown" и "Фрагменты кода".</span><span class="sxs-lookup"><span data-stu-id="b6001-307">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="b6001-308">Блоки заметок</span><span class="sxs-lookup"><span data-stu-id="b6001-308">Note blocks</span></span>

<span data-ttu-id="b6001-309">Есть четыре типа блоков заметок, которые позволяют привлечь внимание к определенному содержимому:</span><span class="sxs-lookup"><span data-stu-id="b6001-309">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="b6001-310">ПРИМЕЧАНИЕ;</span><span class="sxs-lookup"><span data-stu-id="b6001-310">NOTE</span></span>
- <span data-ttu-id="b6001-311">ПРЕДУПРЕЖДЕНИЕ;</span><span class="sxs-lookup"><span data-stu-id="b6001-311">WARNING</span></span>
- <span data-ttu-id="b6001-312">СОВЕТ;</span><span class="sxs-lookup"><span data-stu-id="b6001-312">TIP</span></span>
- <span data-ttu-id="b6001-313">ВАЖНО.</span><span class="sxs-lookup"><span data-stu-id="b6001-313">IMPORTANT</span></span>

<span data-ttu-id="b6001-314">В целом не следует часто использовать блоки заметок, так как они могут отвлекать пользователя от основного содержимого.</span><span class="sxs-lookup"><span data-stu-id="b6001-314">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="b6001-315">Хотя эти элементы также поддерживают блоки кода, изображения, списки и ссылки, лучше не перегружать их, делая простыми и понятными.</span><span class="sxs-lookup"><span data-stu-id="b6001-315">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="b6001-316">Примеры:</span><span class="sxs-lookup"><span data-stu-id="b6001-316">Examples:</span></span>

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

<span data-ttu-id="b6001-317">Это выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b6001-317">These render as follows:</span></span>

> [!NOTE]
> <span data-ttu-id="b6001-318">Это ПРИМЕЧАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6001-318">This is a NOTE</span></span>

> [!WARNING]
> <span data-ttu-id="b6001-319">Это ПРЕДУПРЕЖДЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6001-319">This is a WARNING</span></span>

> [!TIP]
> <span data-ttu-id="b6001-320">Это СОВЕТ</span><span class="sxs-lookup"><span data-stu-id="b6001-320">This is a TIP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b6001-321">Это ВАЖНО</span><span class="sxs-lookup"><span data-stu-id="b6001-321">This is IMPORTANT</span></span>

### <a name="include-files"></a><span data-ttu-id="b6001-322">Включаемые файлы</span><span class="sxs-lookup"><span data-stu-id="b6001-322">Include files</span></span>

<span data-ttu-id="b6001-323">Если вы хотите добавить в файлы статей многократно используемые изображения или текст, воспользуйтесь доступной в Markdig функцией включения ("include") файлов по ссылке.</span><span class="sxs-lookup"><span data-stu-id="b6001-323">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="b6001-324">Функция указывает OPS включить файл в файл статьи во время сборки, чтобы он стал частью опубликованной статьи.</span><span class="sxs-lookup"><span data-stu-id="b6001-324">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="b6001-325">Существует три типа включения файлов для многократного использования содержимого:</span><span class="sxs-lookup"><span data-stu-id="b6001-325">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="b6001-326">Встроенные: Используются для многократного использования фрагмента стандартного текста путем его встраивания в другое предложение.</span><span class="sxs-lookup"><span data-stu-id="b6001-326">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="b6001-327">Блочные: Используются для многократного использования всего файла Markdown в качестве блока путем его вложения в раздел или статью.</span><span class="sxs-lookup"><span data-stu-id="b6001-327">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="b6001-328">Изображения: Так на платформе Docs реализовано стандартное включение изображений.</span><span class="sxs-lookup"><span data-stu-id="b6001-328">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="b6001-329">Встроенные и блочные включаемые файлы — это простые файлы Markdown с расширением .md.</span><span class="sxs-lookup"><span data-stu-id="b6001-329">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="b6001-330">Они могут содержать любую допустимую разметку Markdown.</span><span class="sxs-lookup"><span data-stu-id="b6001-330">It can contain any valid Markdown.</span></span> <span data-ttu-id="b6001-331">Все включаемые файлы Markdown должны быть помещены в [общий подкаталог `/includes`](git-github-fundamentals.md#includes-subdirectory) в корневом каталоге репозитория.</span><span class="sxs-lookup"><span data-stu-id="b6001-331">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="b6001-332">Когда статья публикуется, включаемый файл легко интегрируется в нее.</span><span class="sxs-lookup"><span data-stu-id="b6001-332">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="b6001-333">Ниже приведены требования к включаемым файлам и соображения по работе с ними:</span><span class="sxs-lookup"><span data-stu-id="b6001-333">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="b6001-334">Используйте включаемые файлы, если вам нужно, чтобы один и тот же текст отображался в нескольких статьях.</span><span class="sxs-lookup"><span data-stu-id="b6001-334">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="b6001-335">Блочные включаемые файлы предназначены для значительных объемов текста: один или два абзаца, общая процедура или общий раздел.</span><span class="sxs-lookup"><span data-stu-id="b6001-335">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="b6001-336">Не используйте их для фрагментов текста меньше одного предложения.</span><span class="sxs-lookup"><span data-stu-id="b6001-336">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="b6001-337">Включаемые файлы не будут отображаться в представлении статьи на GitHub, так как они работают только с Markdig-расширениями.</span><span class="sxs-lookup"><span data-stu-id="b6001-337">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="b6001-338">Они отображаются только после публикации.</span><span class="sxs-lookup"><span data-stu-id="b6001-338">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="b6001-339">Весь текст во включаемом файле должен состоять из полноценных предложений или фраз, не зависящих от остального текста статьи, в которую добавляется ссылка на такой файл.</span><span class="sxs-lookup"><span data-stu-id="b6001-339">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="b6001-340">Если не следовать этой инструкции, в статье создаются непереводимые строки, которые нарушают процесс локализации.</span><span class="sxs-lookup"><span data-stu-id="b6001-340">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="b6001-341">Не внедряйте одни включаемые файлы в другие.</span><span class="sxs-lookup"><span data-stu-id="b6001-341">Don't embed include references within other include files.</span></span> <span data-ttu-id="b6001-342">Такая возможность не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b6001-342">They are not supported.</span></span>
- <span data-ttu-id="b6001-343">Файлы мультимедиа должны быть помещены в отдельную папку мультимедиа в подкаталоге включаемых файлов. Например, `<repo>`/включаемые файлы/папка мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b6001-343">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="b6001-344">В корне каталога мультимедиа не должны содержаться изображения.</span><span class="sxs-lookup"><span data-stu-id="b6001-344">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="b6001-345">Если во включаемом файле нет изображений, соответствующий каталог мультимедиа не требуется.</span><span class="sxs-lookup"><span data-stu-id="b6001-345">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="b6001-346">Как и в обычных статьях, не используйте общий файл мультимедиа для включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="b6001-346">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="b6001-347">Для каждого включаемого файла в статье должен быть создан отдельный файл с уникальным именем.</span><span class="sxs-lookup"><span data-stu-id="b6001-347">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="b6001-348">Файл мультимедиа должен храниться в папке мультимедиа, связанной с включаемым файлом.</span><span class="sxs-lookup"><span data-stu-id="b6001-348">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="b6001-349">Не используйте включаемый файл как единственное содержимое статьи.</span><span class="sxs-lookup"><span data-stu-id="b6001-349">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="b6001-350">Включаемые файлы предназначены для дополнения основных материалов статьи.</span><span class="sxs-lookup"><span data-stu-id="b6001-350">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="b6001-351">Пример.</span><span class="sxs-lookup"><span data-stu-id="b6001-351">Example:</span></span>

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="b6001-352">Селекторы</span><span class="sxs-lookup"><span data-stu-id="b6001-352">Selectors</span></span>

<span data-ttu-id="b6001-353">В технических статьях селекторы применяются для создания разных вариантов содержимого, чтобы проиллюстрировать различия в реализации, связанные с использованием нескольких технологий или платформ.</span><span class="sxs-lookup"><span data-stu-id="b6001-353">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="b6001-354">Это в особенности применимо к материалам о мобильных платформах для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="b6001-354">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="b6001-355">Сейчас в Markdig есть два типа селекторов: для единичного и множественного выбора.</span><span class="sxs-lookup"><span data-stu-id="b6001-355">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="b6001-356">В каждой статье с возможностью выбора используется одна и та же разметка Markdown для селектора. Поэтому рекомендуется поместить селектор для статьи во включаемый файл.</span><span class="sxs-lookup"><span data-stu-id="b6001-356">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="b6001-357">Затем нужно добавить ссылки на этот файл во все статьи, для которых используется селектор.</span><span class="sxs-lookup"><span data-stu-id="b6001-357">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="b6001-358">Ниже приведен пример селектора:</span><span class="sxs-lookup"><span data-stu-id="b6001-358">The following shows an example selector:</span></span>

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="b6001-359">Пример селекторов в действии можно посмотреть в [документации по Azure](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span><span class="sxs-lookup"><span data-stu-id="b6001-359">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="b6001-360">Включение фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="b6001-360">Code include references</span></span>

<span data-ttu-id="b6001-361">В Markdig есть расширение с расширенными функциями для включения в статью фрагментов кода.</span><span class="sxs-lookup"><span data-stu-id="b6001-361">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="b6001-362">Этот формат обеспечивает расширенный рендеринг на основе функций GFM, таких как выбор языка программирования и раскраска синтаксиса, а также другие полезные функции, например:</span><span class="sxs-lookup"><span data-stu-id="b6001-362">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="b6001-363">включение централизованных примеров или фрагментов кода из внешнего репозитория;</span><span class="sxs-lookup"><span data-stu-id="b6001-363">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="b6001-364">пользовательский интерфейс с вкладками для отображения нескольких версий примеров кода на разных языках.</span><span class="sxs-lookup"><span data-stu-id="b6001-364">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="b6001-365">Сбои и устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="b6001-365">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="b6001-366">Замещающий текст</span><span class="sxs-lookup"><span data-stu-id="b6001-366">Alt text</span></span>

<span data-ttu-id="b6001-367">Замещающий текст, который содержит символы подчеркивания, отображается некорректно.</span><span class="sxs-lookup"><span data-stu-id="b6001-367">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="b6001-368">Например, вместо</span><span class="sxs-lookup"><span data-stu-id="b6001-368">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="b6001-369">используйте следующий вариант, позволяющий избежать символов подчеркивания:</span><span class="sxs-lookup"><span data-stu-id="b6001-369">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="b6001-370">Апострофы и кавычки</span><span class="sxs-lookup"><span data-stu-id="b6001-370">Apostrophes and quotation marks</span></span>

<span data-ttu-id="b6001-371">Если вы копируете текст из Word в редактор Markdown, он может содержать книжные (изогнутые) апострофы или кавычки.</span><span class="sxs-lookup"><span data-stu-id="b6001-371">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="b6001-372">Их нужно заменить кодом или обычными апострофами или кавычками.</span><span class="sxs-lookup"><span data-stu-id="b6001-372">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="b6001-373">В противном случае после публикации файла может отобразиться нечитаемый текст, например: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="b6001-373">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="b6001-374">Ниже приведены кодировки для этих знаков пунктуации:</span><span class="sxs-lookup"><span data-stu-id="b6001-374">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="b6001-375">левая (открывающая) кавычка: `&#8220;`;</span><span class="sxs-lookup"><span data-stu-id="b6001-375">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="b6001-376">правая (закрывающая) кавычка: `&#8221;`;</span><span class="sxs-lookup"><span data-stu-id="b6001-376">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="b6001-377">правая закрывающая одинарная кавычка или апостроф: `&#8217;`;</span><span class="sxs-lookup"><span data-stu-id="b6001-377">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="b6001-378">левая открывающая одинарная кавычка (используется редко): `&#8216;`.</span><span class="sxs-lookup"><span data-stu-id="b6001-378">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="b6001-379">Угловые скобки</span><span class="sxs-lookup"><span data-stu-id="b6001-379">Angle brackets</span></span>

<span data-ttu-id="b6001-380">Угловые скобки, как правило, используются для обозначения заполнителя.</span><span class="sxs-lookup"><span data-stu-id="b6001-380">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="b6001-381">Если вы используете угловые скобки в тексте (а не в коде), их необходимо закодировать.</span><span class="sxs-lookup"><span data-stu-id="b6001-381">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="b6001-382">Иначе Markdown распознает их как часть тега HTML.</span><span class="sxs-lookup"><span data-stu-id="b6001-382">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="b6001-383">Например, `<script name>` следует закодировать как `&lt;script name&gt;`.</span><span class="sxs-lookup"><span data-stu-id="b6001-383">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="b6001-384">Дополнительные материалы</span><span class="sxs-lookup"><span data-stu-id="b6001-384">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="b6001-385">Ресурсы Markdown</span><span class="sxs-lookup"><span data-stu-id="b6001-385">Markdown resources</span></span>

- <span data-ttu-id="b6001-386">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax) (Синтаксис Markdown)</span><span class="sxs-lookup"><span data-stu-id="b6001-386">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- <span data-ttu-id="b6001-387">[Markdown cheat-sheet](./media/documents/markdown-cheatsheet.pdf?raw=true) (Шпаргалка по Markdown)</span><span class="sxs-lookup"><span data-stu-id="b6001-387">[Docs Markdown cheat sheet](./media/documents/markdown-cheatsheet.pdf?raw=true)</span></span>
- [<span data-ttu-id="b6001-388">Базовые сведения о разметке Markdown на GitHub</span><span class="sxs-lookup"><span data-stu-id="b6001-388">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- <span data-ttu-id="b6001-389">[The Markdown Guide](https://www.markdownguide.org/) (Руководство по Markdown)</span><span class="sxs-lookup"><span data-stu-id="b6001-389">[The Markdown Guide](https://www.markdownguide.org/)</span></span>
