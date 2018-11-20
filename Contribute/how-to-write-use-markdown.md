---
title: Использование языка разметки Markdown для написания документации
description: В этой статье приводятся базовые и справочные сведения о языке разметки Markdown, используемом для написания статей на сайте docs.microsoft.com.
ms.date: 07/13/2017
ms.openlocfilehash: 21194c4bd6020d847b526a4d9544c826aa199e2a
ms.sourcegitcommit: 44eb4f5ee65c1848d7f36fca107b296eb7687397
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/13/2018
ms.locfileid: "51609529"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="d9c1d-103">Использование языка разметки Markdown для написания документации</span><span class="sxs-lookup"><span data-stu-id="d9c1d-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="d9c1d-104">Статьи на сайте [docs.microsoft.com](http://docs.microsoft.com) написаны на [Markdown](https://daringfireball.net/projects/markdown/) — упрощенном языке разметки, который легко использовать и изучать.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="d9c1d-105">Благодаря своей простоте он быстро становится отраслевым стандартом.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="d9c1d-106">Так как документация хранится в репозитории GitHub, для нее можно использовать расширенный набор Markdown под названием [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/). Этот формат предусматривает дополнительные возможности для решения распространенных задач.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-106">Since Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="d9c1d-107">Кроме того, службы Open Publishing Services (OPS) используют Markdig, синтаксический анализатор Markdown.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="d9c1d-108">Он обеспечивает высокую совместимость с диалектом GFM, предоставляя дополнительные функции для работы с документацией.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-108">Markdig is highly compatible with GFM, adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="d9c1d-109">Markdig — это быстрый и мощный обработчик Markdown для .NET, обеспечивающий соответствие CommonMark и поддержку расширений.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="d9c1d-110">Улучшенная поддержка сообщества</span><span class="sxs-lookup"><span data-stu-id="d9c1d-110">Better community support</span></span>
* <span data-ttu-id="d9c1d-111">Улучшенная поддержка стандартов</span><span class="sxs-lookup"><span data-stu-id="d9c1d-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="d9c1d-112">Базовые сведения о Markdown</span><span class="sxs-lookup"><span data-stu-id="d9c1d-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="d9c1d-113">Заголовки</span><span class="sxs-lookup"><span data-stu-id="d9c1d-113">Headings</span></span>

<span data-ttu-id="d9c1d-114">Чтобы создать заголовок, используйте знак (#), например:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="d9c1d-115">В заголовках следует использовать стиль atx, то есть 1–6 символов решетки (#) в начале строки, чтобы указать на заголовок, соответствующий заголовкам HTML уровней с H1 по H6.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-115">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="d9c1d-116">Сверху приводятся примеры заголовков с первого по четвертый уровень.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-116">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="d9c1d-117">В статье **должен** быть только один заголовок первого уровня (H1), который будет отображаться как заголовок страницы.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-117">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="d9c1d-118">Если заголовок заканчивается на символ `#`, добавьте в конце еще символ `#`, чтобы заголовок отображался правильно.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-118">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="d9c1d-119">Например, `# Async Programming in F# #`.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-119">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="d9c1d-120">Заголовки второго уровня создадут оглавление, которое будет отображаться в разделе "В этой статье" под заголовком статьи.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-120">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="d9c1d-121">Полужирное начертание и курсив</span><span class="sxs-lookup"><span data-stu-id="d9c1d-121">Bold and italic text</span></span>

<span data-ttu-id="d9c1d-122">Чтобы задать для текста **полужирное начертание**, заключите его в двойные звездочки:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-122">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="d9c1d-123">Чтобы задать для текста *курсивное начертание*, заключите его в одинарные звездочки:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-123">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="d9c1d-124">Чтобы задать для текста ***полужирное и курсивное*** начертание, заключите его в тройные звездочки:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-124">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="d9c1d-125">Блоки цитирования</span><span class="sxs-lookup"><span data-stu-id="d9c1d-125">Blockquotes</span></span>

<span data-ttu-id="d9c1d-126">Блоки цитирования создаются с помощью символа `>`:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-126">Blockquotes are created using the `>` character:</span></span>

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="d9c1d-127">Предыдущий пример отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-127">The preceding example renders as follows:</span></span>

> <span data-ttu-id="d9c1d-128">Засуха продолжалась десять миллионов лет, и царству ужасных ящеров уже давно пришел конец.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-128">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="d9c1d-129">Здесь, близ экватора, на материке, который позднее назовут Африкой, с новой яростью вспыхнула борьба за существование, и еще не ясно было, кто выйдет из нее победителем.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-129">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="d9c1d-130">На этой бесплодной, иссушенной зноем земле благоденствовать или хотя бы просто выжить могли только маленькие, или ловкие, или свирепые.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-130">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="d9c1d-131">Списки</span><span class="sxs-lookup"><span data-stu-id="d9c1d-131">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="d9c1d-132">Неупорядоченный список</span><span class="sxs-lookup"><span data-stu-id="d9c1d-132">Unordered list</span></span>

<span data-ttu-id="d9c1d-133">Неупорядоченный (маркированный) список можно отформатировать с помощью звездочек или тире.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-133">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="d9c1d-134">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-134">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="d9c1d-135">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-135">will be rendered as:</span></span>

- <span data-ttu-id="d9c1d-136">List item 1</span><span class="sxs-lookup"><span data-stu-id="d9c1d-136">List item 1</span></span>
- <span data-ttu-id="d9c1d-137">List item 2</span><span class="sxs-lookup"><span data-stu-id="d9c1d-137">List item 2</span></span>
- <span data-ttu-id="d9c1d-138">List item 3</span><span class="sxs-lookup"><span data-stu-id="d9c1d-138">List item 3</span></span>

<span data-ttu-id="d9c1d-139">Чтобы вложить один список в другой, добавьте отступ для элементов дочернего списка.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-139">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="d9c1d-140">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-140">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="d9c1d-141">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-141">will be rendered as:</span></span>

- <span data-ttu-id="d9c1d-142">List item 1</span><span class="sxs-lookup"><span data-stu-id="d9c1d-142">List item 1</span></span>
  - <span data-ttu-id="d9c1d-143">List item A</span><span class="sxs-lookup"><span data-stu-id="d9c1d-143">List item A</span></span>
  - <span data-ttu-id="d9c1d-144">List item B</span><span class="sxs-lookup"><span data-stu-id="d9c1d-144">List item B</span></span>
- <span data-ttu-id="d9c1d-145">List item 2</span><span class="sxs-lookup"><span data-stu-id="d9c1d-145">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="d9c1d-146">Упорядоченный список</span><span class="sxs-lookup"><span data-stu-id="d9c1d-146">Ordered list</span></span>

<span data-ttu-id="d9c1d-147">Упорядоченный (ступенчатый) список можно отформатировать с помощью соответствующих цифр.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-147">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="d9c1d-148">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-148">For example, the following Markdown:</span></span>

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="d9c1d-149">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-149">will be rendered as:</span></span>

1. <span data-ttu-id="d9c1d-150">First instruction</span><span class="sxs-lookup"><span data-stu-id="d9c1d-150">First instruction</span></span>
2. <span data-ttu-id="d9c1d-151">Second instruction</span><span class="sxs-lookup"><span data-stu-id="d9c1d-151">Second instruction</span></span>
3. <span data-ttu-id="d9c1d-152">Third instruction</span><span class="sxs-lookup"><span data-stu-id="d9c1d-152">Third instruction</span></span>

<span data-ttu-id="d9c1d-153">Чтобы вложить один список в другой, добавьте отступ для элементов дочернего списка.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-153">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="d9c1d-154">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-154">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="d9c1d-155">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-155">will be rendered as:</span></span>

1. <span data-ttu-id="d9c1d-156">First instruction</span><span class="sxs-lookup"><span data-stu-id="d9c1d-156">First instruction</span></span>
   1. <span data-ttu-id="d9c1d-157">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="d9c1d-157">Sub-instruction</span></span>
   2. <span data-ttu-id="d9c1d-158">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="d9c1d-158">Sub-instruction</span></span>
2. <span data-ttu-id="d9c1d-159">Second instruction</span><span class="sxs-lookup"><span data-stu-id="d9c1d-159">Second instruction</span></span>

<span data-ttu-id="d9c1d-160">Обратите внимание, что мы используем "1."</span><span class="sxs-lookup"><span data-stu-id="d9c1d-160">Note that we use '1.'</span></span> <span data-ttu-id="d9c1d-161">для всех записей.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-161">for all entries.</span></span> <span data-ttu-id="d9c1d-162">Так проще увидеть различия, когда потом будут добавлены новые шаги или удалены существующие.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-162">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="d9c1d-163">Tables</span><span class="sxs-lookup"><span data-stu-id="d9c1d-163">Tables</span></span>

<span data-ttu-id="d9c1d-164">Таблицы не входят в основную спецификацию Markdown, но их поддерживает GFM.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-164">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="d9c1d-165">Создавать таблицы можно с помощью символов вертикальной черты (|) и дефиса (-).</span><span class="sxs-lookup"><span data-stu-id="d9c1d-165">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="d9c1d-166">Дефисы позволяют создавать для каждого столбца заголовок. Вертикальные черты разделяют столбцы.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-166">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="d9c1d-167">Чтобы таблица правильно отображалась, включите перед ней пустую строку.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-167">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="d9c1d-168">Например, следующая разметка Markdown:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-168">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="d9c1d-169">будет отображаться как:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-169">will be rendered as:</span></span>

| <span data-ttu-id="d9c1d-170">Fun</span><span class="sxs-lookup"><span data-stu-id="d9c1d-170">Fun</span></span>                  | <span data-ttu-id="d9c1d-171">with</span><span class="sxs-lookup"><span data-stu-id="d9c1d-171">With</span></span>                 | <span data-ttu-id="d9c1d-172">Tables</span><span class="sxs-lookup"><span data-stu-id="d9c1d-172">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="d9c1d-173">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="d9c1d-173">left-aligned column</span></span>  | <span data-ttu-id="d9c1d-174">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="d9c1d-174">right-aligned column</span></span> | <span data-ttu-id="d9c1d-175">centered column</span><span class="sxs-lookup"><span data-stu-id="d9c1d-175">centered column</span></span> |
| <span data-ttu-id="d9c1d-176">$100</span><span class="sxs-lookup"><span data-stu-id="d9c1d-176">$100</span></span>                 | <span data-ttu-id="d9c1d-177">$100</span><span class="sxs-lookup"><span data-stu-id="d9c1d-177">$100</span></span>                 | <span data-ttu-id="d9c1d-178">$100</span><span class="sxs-lookup"><span data-stu-id="d9c1d-178">$100</span></span>            |
| <span data-ttu-id="d9c1d-179">$10</span><span class="sxs-lookup"><span data-stu-id="d9c1d-179">$10</span></span>                  | <span data-ttu-id="d9c1d-180">$10</span><span class="sxs-lookup"><span data-stu-id="d9c1d-180">$10</span></span>                  | <span data-ttu-id="d9c1d-181">$10</span><span class="sxs-lookup"><span data-stu-id="d9c1d-181">$10</span></span>             |
| <span data-ttu-id="d9c1d-182">$1</span><span class="sxs-lookup"><span data-stu-id="d9c1d-182">$1</span></span>                   | <span data-ttu-id="d9c1d-183">$1</span><span class="sxs-lookup"><span data-stu-id="d9c1d-183">$1</span></span>                   | <span data-ttu-id="d9c1d-184">$1</span><span class="sxs-lookup"><span data-stu-id="d9c1d-184">$1</span></span>              |

<span data-ttu-id="d9c1d-185">Дополнительные сведения о создании таблиц:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-185">For more information on creating tables, see:</span></span>

- <span data-ttu-id="d9c1d-186">[Функция обтекания таблиц](#table-wrapping) в Markdig, которая поможет при форматировании широких таблиц.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-186">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="d9c1d-187">Статья на сайте GitHub [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/) (Организация информации с помощью таблиц).</span><span class="sxs-lookup"><span data-stu-id="d9c1d-187">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="d9c1d-188">Веб-приложение [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="d9c1d-188">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="d9c1d-189">Статья Адама Притчарда (Adam Pritchard) [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables) (Шпаргалка по Markdown).</span><span class="sxs-lookup"><span data-stu-id="d9c1d-189">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="d9c1d-190">Статья Майкла Фортина (Michel Fortin) [Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) (Расширение Markdown Extra).</span><span class="sxs-lookup"><span data-stu-id="d9c1d-190">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="d9c1d-191">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/) (Преобразование таблиц HTML в Markdown).</span><span class="sxs-lookup"><span data-stu-id="d9c1d-191">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="d9c1d-192">Создание ссылок</span><span class="sxs-lookup"><span data-stu-id="d9c1d-192">Links</span></span>

<span data-ttu-id="d9c1d-193">Синтаксис Markdown для встроенной ссылки состоит из части `[link text]`, представляющей текст гиперссылки, и части `(file-name.md)` — URL-адреса или имени файла, на который дается ссылка:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-193">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="d9c1d-194">Дополнительные сведения о ссылках:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-194">For more information on linking, see:</span></span>

- <span data-ttu-id="d9c1d-195">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax#link) (Руководство по синтаксису Markdown), в котором предоставлена основная информация по поддержке ссылок Markdown.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-195">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="d9c1d-196">Страница [Ссылки](how-to-write-links.md) в этом руководстве содержит сведения о дополнительном синтаксисе Markdig для ссылок.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-196">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="d9c1d-197">Фрагменты кода</span><span class="sxs-lookup"><span data-stu-id="d9c1d-197">Code snippets</span></span>

<span data-ttu-id="d9c1d-198">Markdown поддерживает как встраивание фрагментов кода в предложение, так и их размещение между предложениями в виде отдельных огражденных блоков.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-198">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="d9c1d-199">Дополнительная информация:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-199">For details, see:</span></span>

- [<span data-ttu-id="d9c1d-200">Сведения о собственной поддержке блоков кода Markdown</span><span class="sxs-lookup"><span data-stu-id="d9c1d-200">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="d9c1d-201">Сведения о поддержке GFM для ограждения кода и выделения синтаксиса</span><span class="sxs-lookup"><span data-stu-id="d9c1d-201">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="d9c1d-202">Огражденные блоки кода — это простой способ выделить синтаксис для фрагментов кода.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-202">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="d9c1d-203">Общий формат огражденных блоков кода:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-203">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="d9c1d-204">Псевдоним после трех начальных символов обратной галочки \` определяет использование выделения.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-204">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="d9c1d-205">Ниже представлен список часто используемых языков программирования для написания документации и приводятся соответствующие метки.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-205">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="d9c1d-206">Все эти языки поддерживают понятные имена, а большинство из них — выделение языка в имени.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-206">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="d9c1d-207">Имя</span><span class="sxs-lookup"><span data-stu-id="d9c1d-207">Name</span></span>|<span data-ttu-id="d9c1d-208">Метка Markdown</span><span class="sxs-lookup"><span data-stu-id="d9c1d-208">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="d9c1d-209">.NET Console</span><span class="sxs-lookup"><span data-stu-id="d9c1d-209">.NET Console</span></span>|<span data-ttu-id="d9c1d-210">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="d9c1d-210">dotnetcli</span></span>|
|<span data-ttu-id="d9c1d-211">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="d9c1d-211">ASP.NET (C#)</span></span>|<span data-ttu-id="d9c1d-212">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="d9c1d-212">aspx-csharp</span></span>|
|<span data-ttu-id="d9c1d-213">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="d9c1d-213">ASP.NET (VB)</span></span>|<span data-ttu-id="d9c1d-214">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="d9c1d-214">aspx-vb</span></span>|
|<span data-ttu-id="d9c1d-215">AzCopy</span><span class="sxs-lookup"><span data-stu-id="d9c1d-215">AzCopy</span></span>|<span data-ttu-id="d9c1d-216">azcopy</span><span class="sxs-lookup"><span data-stu-id="d9c1d-216">azcopy</span></span>|
|<span data-ttu-id="d9c1d-217">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="d9c1d-217">Azure CLI</span></span>|<span data-ttu-id="d9c1d-218">azurecli</span><span class="sxs-lookup"><span data-stu-id="d9c1d-218">azurecli</span></span>|
|<span data-ttu-id="d9c1d-219">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d9c1d-219">Azure PowerShell</span></span>|<span data-ttu-id="d9c1d-220">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="d9c1d-220">azurepowershell</span></span>|
|<span data-ttu-id="d9c1d-221">C++</span><span class="sxs-lookup"><span data-stu-id="d9c1d-221">C++</span></span>|<span data-ttu-id="d9c1d-222">cpp</span><span class="sxs-lookup"><span data-stu-id="d9c1d-222">cpp</span></span>|
|<span data-ttu-id="d9c1d-223">C++/CX</span><span class="sxs-lookup"><span data-stu-id="d9c1d-223">C++/CX</span></span>|<span data-ttu-id="d9c1d-224">cppcx</span><span class="sxs-lookup"><span data-stu-id="d9c1d-224">cppcx</span></span>|
|<span data-ttu-id="d9c1d-225">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="d9c1d-225">C++/WinRT</span></span>|<span data-ttu-id="d9c1d-226">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="d9c1d-226">cppwinrt</span></span>|
|<span data-ttu-id="d9c1d-227">C#</span><span class="sxs-lookup"><span data-stu-id="d9c1d-227">C#</span></span>|<span data-ttu-id="d9c1d-228">csharp</span><span class="sxs-lookup"><span data-stu-id="d9c1d-228">csharp</span></span>|
|<span data-ttu-id="d9c1d-229">C# в браузере</span><span class="sxs-lookup"><span data-stu-id="d9c1d-229">C# in browser</span></span>|<span data-ttu-id="d9c1d-230">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="d9c1d-230">csharp-interactive</span></span>|
|<span data-ttu-id="d9c1d-231">Консоль</span><span class="sxs-lookup"><span data-stu-id="d9c1d-231">Console</span></span>|<span data-ttu-id="d9c1d-232">консоль</span><span class="sxs-lookup"><span data-stu-id="d9c1d-232">console</span></span>|
|<span data-ttu-id="d9c1d-233">CSHTML</span><span class="sxs-lookup"><span data-stu-id="d9c1d-233">CSHTML</span></span>|<span data-ttu-id="d9c1d-234">cshtml</span><span class="sxs-lookup"><span data-stu-id="d9c1d-234">cshtml</span></span>|
|<span data-ttu-id="d9c1d-235">DAX</span><span class="sxs-lookup"><span data-stu-id="d9c1d-235">DAX</span></span>|<span data-ttu-id="d9c1d-236">dax</span><span class="sxs-lookup"><span data-stu-id="d9c1d-236">dax</span></span>|
|<span data-ttu-id="d9c1d-237">F#</span><span class="sxs-lookup"><span data-stu-id="d9c1d-237">F#</span></span>|<span data-ttu-id="d9c1d-238">fsharp</span><span class="sxs-lookup"><span data-stu-id="d9c1d-238">fsharp</span></span>|
|<span data-ttu-id="d9c1d-239">Go</span><span class="sxs-lookup"><span data-stu-id="d9c1d-239">Go</span></span>|<span data-ttu-id="d9c1d-240">go</span><span class="sxs-lookup"><span data-stu-id="d9c1d-240">go</span></span>|
|<span data-ttu-id="d9c1d-241">HTML</span><span class="sxs-lookup"><span data-stu-id="d9c1d-241">HTML</span></span>|<span data-ttu-id="d9c1d-242">html</span><span class="sxs-lookup"><span data-stu-id="d9c1d-242">html</span></span>|
|<span data-ttu-id="d9c1d-243">HTTP</span><span class="sxs-lookup"><span data-stu-id="d9c1d-243">HTTP</span></span>|<span data-ttu-id="d9c1d-244">http</span><span class="sxs-lookup"><span data-stu-id="d9c1d-244">http</span></span>|
|<span data-ttu-id="d9c1d-245">Java</span><span class="sxs-lookup"><span data-stu-id="d9c1d-245">Java</span></span>|<span data-ttu-id="d9c1d-246">java</span><span class="sxs-lookup"><span data-stu-id="d9c1d-246">java</span></span>|
|<span data-ttu-id="d9c1d-247">JavaScript</span><span class="sxs-lookup"><span data-stu-id="d9c1d-247">JavaScript</span></span>|<span data-ttu-id="d9c1d-248">javascript</span><span class="sxs-lookup"><span data-stu-id="d9c1d-248">javascript</span></span>|
|<span data-ttu-id="d9c1d-249">JSON</span><span class="sxs-lookup"><span data-stu-id="d9c1d-249">JSON</span></span>|<span data-ttu-id="d9c1d-250">json</span><span class="sxs-lookup"><span data-stu-id="d9c1d-250">json</span></span>|
|<span data-ttu-id="d9c1d-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="d9c1d-251">Markdown</span></span>|<span data-ttu-id="d9c1d-252">md</span><span class="sxs-lookup"><span data-stu-id="d9c1d-252">md</span></span>|
|<span data-ttu-id="d9c1d-253">NodeJS</span><span class="sxs-lookup"><span data-stu-id="d9c1d-253">NodeJS</span></span>|<span data-ttu-id="d9c1d-254">nodejs</span><span class="sxs-lookup"><span data-stu-id="d9c1d-254">nodejs</span></span>|
|<span data-ttu-id="d9c1d-255">Objective-C</span><span class="sxs-lookup"><span data-stu-id="d9c1d-255">Objective-C</span></span>|<span data-ttu-id="d9c1d-256">objc</span><span class="sxs-lookup"><span data-stu-id="d9c1d-256">objc</span></span>|
|<span data-ttu-id="d9c1d-257">OData</span><span class="sxs-lookup"><span data-stu-id="d9c1d-257">OData</span></span>|<span data-ttu-id="d9c1d-258">odata</span><span class="sxs-lookup"><span data-stu-id="d9c1d-258">odata</span></span>|
|<span data-ttu-id="d9c1d-259">PHP</span><span class="sxs-lookup"><span data-stu-id="d9c1d-259">PHP</span></span>|<span data-ttu-id="d9c1d-260">php</span><span class="sxs-lookup"><span data-stu-id="d9c1d-260">php</span></span>|
|<span data-ttu-id="d9c1d-261">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="d9c1d-261">Power Apps Formula</span></span>|<span data-ttu-id="d9c1d-262">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="d9c1d-262">powerappsfl</span></span>|
|<span data-ttu-id="d9c1d-263">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d9c1d-263">PowerShell</span></span>|<span data-ttu-id="d9c1d-264">powershell</span><span class="sxs-lookup"><span data-stu-id="d9c1d-264">powershell</span></span>|
|<span data-ttu-id="d9c1d-265">Python</span><span class="sxs-lookup"><span data-stu-id="d9c1d-265">Python</span></span>|<span data-ttu-id="d9c1d-266">python</span><span class="sxs-lookup"><span data-stu-id="d9c1d-266">python</span></span>|
|<span data-ttu-id="d9c1d-267">Q#</span><span class="sxs-lookup"><span data-stu-id="d9c1d-267">Q#</span></span>|<span data-ttu-id="d9c1d-268">qsharp</span><span class="sxs-lookup"><span data-stu-id="d9c1d-268">qsharp</span></span>|
|<span data-ttu-id="d9c1d-269">R</span><span class="sxs-lookup"><span data-stu-id="d9c1d-269">R</span></span>|<span data-ttu-id="d9c1d-270">r</span><span class="sxs-lookup"><span data-stu-id="d9c1d-270">r</span></span>|
|<span data-ttu-id="d9c1d-271">Ruby</span><span class="sxs-lookup"><span data-stu-id="d9c1d-271">Ruby</span></span>|<span data-ttu-id="d9c1d-272">ruby</span><span class="sxs-lookup"><span data-stu-id="d9c1d-272">ruby</span></span>|
|<span data-ttu-id="d9c1d-273">SQL</span><span class="sxs-lookup"><span data-stu-id="d9c1d-273">SQL</span></span>|<span data-ttu-id="d9c1d-274">sql</span><span class="sxs-lookup"><span data-stu-id="d9c1d-274">sql</span></span>|
|<span data-ttu-id="d9c1d-275">Swift</span><span class="sxs-lookup"><span data-stu-id="d9c1d-275">Swift</span></span>|<span data-ttu-id="d9c1d-276">swift</span><span class="sxs-lookup"><span data-stu-id="d9c1d-276">swift</span></span>|
|<span data-ttu-id="d9c1d-277">TypeScript</span><span class="sxs-lookup"><span data-stu-id="d9c1d-277">TypeScript</span></span>|<span data-ttu-id="d9c1d-278">typescript</span><span class="sxs-lookup"><span data-stu-id="d9c1d-278">typescript</span></span>|
|<span data-ttu-id="d9c1d-279">VB</span><span class="sxs-lookup"><span data-stu-id="d9c1d-279">VB</span></span>|<span data-ttu-id="d9c1d-280">vb</span><span class="sxs-lookup"><span data-stu-id="d9c1d-280">vb</span></span>|
|<span data-ttu-id="d9c1d-281">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="d9c1d-281">VSTS CLI</span></span>|<span data-ttu-id="d9c1d-282">vstscli</span><span class="sxs-lookup"><span data-stu-id="d9c1d-282">vstscli</span></span>|
|<span data-ttu-id="d9c1d-283">XAML</span><span class="sxs-lookup"><span data-stu-id="d9c1d-283">XAML</span></span>|<span data-ttu-id="d9c1d-284">xaml</span><span class="sxs-lookup"><span data-stu-id="d9c1d-284">xaml</span></span>|
|<span data-ttu-id="d9c1d-285">XML</span><span class="sxs-lookup"><span data-stu-id="d9c1d-285">XML</span></span>|<span data-ttu-id="d9c1d-286">xml</span><span class="sxs-lookup"><span data-stu-id="d9c1d-286">xml</span></span>|

<span data-ttu-id="d9c1d-287">Имя `csharp-interactive` указывает на язык C# и возможность запускать примеры в браузере.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-287">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="d9c1d-288">Эти фрагменты кода компилируются и выполняются в контейнере Docker, а результаты выполнения программы отображаются в окне браузера пользователя.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-288">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="d9c1d-289">Пример: C\#</span><span class="sxs-lookup"><span data-stu-id="d9c1d-289">Example: C\#</span></span>

<span data-ttu-id="d9c1d-290">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="d9c1d-290">__Markdown__</span></span>

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

<span data-ttu-id="d9c1d-291">__Отображение__</span><span class="sxs-lookup"><span data-stu-id="d9c1d-291">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="d9c1d-292">Пример: SQL</span><span class="sxs-lookup"><span data-stu-id="d9c1d-292">Example: SQL</span></span>

<span data-ttu-id="d9c1d-293">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="d9c1d-293">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="d9c1d-294">__Отображение__</span><span class="sxs-lookup"><span data-stu-id="d9c1d-294">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="d9c1d-295">Настраиваемые расширения OPS для Markdown</span><span class="sxs-lookup"><span data-stu-id="d9c1d-295">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="d9c1d-296">Службы Open Publishing Services (OPS) используют Markdig, синтаксический анализатор Markdown, обеспечивающий высокую совместимость с диалектом GitHub Flavored Markdown (GFM).</span><span class="sxs-lookup"><span data-stu-id="d9c1d-296">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="d9c1d-297">Markdig добавляет дополнительные функции за счет расширений Markdown.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-297">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="d9c1d-298">Поэтому для справки мы включили в этот материал некоторые разделы из руководства по разработке OPS.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-298">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="d9c1d-299">(Например, см. в содержании разделы "Markdig и расширения Markdown" и "Фрагменты кода".)</span><span class="sxs-lookup"><span data-stu-id="d9c1d-299">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="d9c1d-300">В статьях документации для общего форматирования, например для создания абзацев, ссылок, списков и заголовков, используется GFM.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-300">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="d9c1d-301">Для расширенного форматирования в статьях можно использовать следующие функции Markdig:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-301">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="d9c1d-302">Блоки заметок</span><span class="sxs-lookup"><span data-stu-id="d9c1d-302">Note blocks</span></span>
- <span data-ttu-id="d9c1d-303">включаемые файлы;</span><span class="sxs-lookup"><span data-stu-id="d9c1d-303">Includes</span></span>
- <span data-ttu-id="d9c1d-304">селекторы;</span><span class="sxs-lookup"><span data-stu-id="d9c1d-304">Selectors</span></span>
- <span data-ttu-id="d9c1d-305">внедренные видео;</span><span class="sxs-lookup"><span data-stu-id="d9c1d-305">Embedded videos</span></span>
- <span data-ttu-id="d9c1d-306">фрагменты или примеры кода.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-306">Code snippets/samples</span></span>

<span data-ttu-id="d9c1d-307">Полный список см. в разделах "Markdig и расширения Markdown" и "Фрагменты кода".</span><span class="sxs-lookup"><span data-stu-id="d9c1d-307">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="d9c1d-308">Блоки заметок</span><span class="sxs-lookup"><span data-stu-id="d9c1d-308">Note blocks</span></span>

<span data-ttu-id="d9c1d-309">Есть четыре типа блоков заметок, которые позволяют привлечь внимание к определенному содержимому:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-309">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="d9c1d-310">ПРИМЕЧАНИЕ;</span><span class="sxs-lookup"><span data-stu-id="d9c1d-310">NOTE</span></span>
- <span data-ttu-id="d9c1d-311">ПРЕДУПРЕЖДЕНИЕ;</span><span class="sxs-lookup"><span data-stu-id="d9c1d-311">WARNING</span></span>
- <span data-ttu-id="d9c1d-312">СОВЕТ;</span><span class="sxs-lookup"><span data-stu-id="d9c1d-312">TIP</span></span>
- <span data-ttu-id="d9c1d-313">ВАЖНО.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-313">IMPORTANT</span></span>

<span data-ttu-id="d9c1d-314">В целом не следует часто использовать блоки заметок, так как они могут отвлекать пользователя от основного содержимого.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-314">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="d9c1d-315">Хотя эти элементы также поддерживают блоки кода, изображения, списки и ссылки, лучше не перегружать их, делая простыми и понятными.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-315">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="d9c1d-316">Примеры:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-316">Examples:</span></span>

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

<span data-ttu-id="d9c1d-317">Это выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-317">These render as follows:</span></span>

> [!NOTE]
> <span data-ttu-id="d9c1d-318">Это ПРИМЕЧАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9c1d-318">This is a NOTE</span></span>

> [!WARNING]
> <span data-ttu-id="d9c1d-319">Это ПРЕДУПРЕЖДЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9c1d-319">This is a WARNING</span></span>

> [!TIP]
> <span data-ttu-id="d9c1d-320">Это СОВЕТ</span><span class="sxs-lookup"><span data-stu-id="d9c1d-320">This is a TIP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d9c1d-321">Это ВАЖНО</span><span class="sxs-lookup"><span data-stu-id="d9c1d-321">This is IMPORTANT</span></span>

### <a name="includes"></a><span data-ttu-id="d9c1d-322">Включаемые файлы</span><span class="sxs-lookup"><span data-stu-id="d9c1d-322">Includes</span></span>

<span data-ttu-id="d9c1d-323">Если вы хотите добавить в файлы статей многократно используемые изображения или текст, воспользуйтесь доступной в Markdig функцией включения ("include") файлов по ссылке.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-323">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="d9c1d-324">Функция указывает OPS включить файл в файл статьи во время сборки, чтобы он стал частью опубликованной статьи.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-324">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="d9c1d-325">Существует три типа включаемых файлов для многократного использования содержимого:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-325">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="d9c1d-326">Встроенные — для многократного использования фрагмента стандартного текста путем его встраивания в другое предложение.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-326">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="d9c1d-327">Блочные — для многократного использования всего файла Markdown в качестве блока путем его вложения в раздел или статью.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-327">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="d9c1d-328">Изображения — позволяют включать стандартное изображение в документацию.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-328">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="d9c1d-329">Встроенные и блочные включаемые файлы — это простые файлы Markdown с расширением .md.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-329">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="d9c1d-330">Они могут содержать любую допустимую разметку Markdown.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-330">It can contain any valid Markdown.</span></span> <span data-ttu-id="d9c1d-331">Все включаемые файлы Markdown должны быть помещены в [общий подкаталог `/includes`](git-github-fundamentals.md#includes-subdirectory) в корневом каталоге репозитория.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-331">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="d9c1d-332">Когда статья публикуется, включаемый файл легко интегрируется в нее.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-332">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="d9c1d-333">Далее приведены требования по работе с включаемыми файлами.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-333">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="d9c1d-334">Используйте включаемые файлы, если вам нужно, чтобы один и тот же текст отображался в нескольких статьях.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-334">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="d9c1d-335">Блочные включаемые файлы предназначены для значительных объемов текста: один или два абзаца, общая процедура или общий раздел.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-335">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="d9c1d-336">Не используйте их для фрагментов текста меньше одного предложения.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-336">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="d9c1d-337">Включаемые файлы не будут отображаться в представлении статьи на GitHub, так как они работают только с Markdig-расширениями.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-337">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="d9c1d-338">Они отображаются только после публикации.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-338">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="d9c1d-339">Весь текст во включаемом файле должен состоять из полноценных предложений или фраз, не зависящих от остального текста статьи, в которую добавляется ссылка на такой файл.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-339">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="d9c1d-340">Если не следовать этой инструкции, в статье создаются непереводимые строки, которые нарушают процесс локализации.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-340">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="d9c1d-341">Не внедряйте одни включаемые файлы в другие.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-341">Don't embed includes within other includes.</span></span> <span data-ttu-id="d9c1d-342">Такая возможность не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-342">They are not supported.</span></span>
- <span data-ttu-id="d9c1d-343">Файлы мультимедиа должны быть помещены в отдельную папку мультимедиа в подкаталоге включаемых файлов. Например, `<repo>`/включаемые файлы/папка мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-343">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="d9c1d-344">В корне каталога мультимедиа не должны содержаться изображения.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-344">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="d9c1d-345">Если во включаемом файле нет изображений, соответствующий каталог мультимедиа не требуется.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-345">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="d9c1d-346">Как и в обычных статьях, не используйте общий файл мультимедиа для включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-346">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="d9c1d-347">Для каждого включаемого файла в статье должен быть создан отдельный файл мультимедиа с уникальным именем.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-347">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="d9c1d-348">Файл мультимедиа должен храниться в папке мультимедиа, связанной с включаемым файлом.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-348">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="d9c1d-349">Не используйте включаемый файл как единственное содержимое статьи.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-349">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="d9c1d-350">Включаемые файлы предназначены для дополнения основных материалов статьи.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-350">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="d9c1d-351">Пример.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-351">Example:</span></span>

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="d9c1d-352">Селекторы</span><span class="sxs-lookup"><span data-stu-id="d9c1d-352">Selectors</span></span>

<span data-ttu-id="d9c1d-353">В технических статьях селекторы применяются для создания разных вариантов содержимого, чтобы проиллюстрировать различия в реализации, связанные с использованием нескольких технологий или платформ.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-353">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="d9c1d-354">Это в особенности применимо к материалам о мобильных платформах для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-354">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="d9c1d-355">Сейчас в Markdig есть два типа селекторов: для единичного и множественного выбора.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-355">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="d9c1d-356">В каждой статье с возможностью выбора используется одна и та же разметка Markdown для селектора. Поэтому рекомендуется поместить селектор для статьи во включаемый файл.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-356">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="d9c1d-357">Затем нужно добавить ссылки на этот файл во все статьи, для которых используется селектор.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-357">Then you can reference that include in all your articles that use the same selector.</span></span>

<span data-ttu-id="d9c1d-358">Ниже приведен пример селектора:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-358">The following shows an example selector:</span></span>

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="d9c1d-359">Пример селекторов в действии можно посмотреть в [документации по Azure](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span><span class="sxs-lookup"><span data-stu-id="d9c1d-359">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-includes"></a><span data-ttu-id="d9c1d-360">Включения кода</span><span class="sxs-lookup"><span data-stu-id="d9c1d-360">Code includes</span></span>

<span data-ttu-id="d9c1d-361">В Markdig есть расширение с расширенными функциями для включения в статью фрагментов кода.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-361">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="d9c1d-362">Этот формат обеспечивает расширенный рендеринг на основе функций GFM, таких как выбор языка программирования и раскраска синтаксиса, а также другие полезные функции, например:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-362">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="d9c1d-363">включение централизованных примеров или фрагментов кода из внешнего репозитория;</span><span class="sxs-lookup"><span data-stu-id="d9c1d-363">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="d9c1d-364">пользовательский интерфейс с вкладками для отображения нескольких версий примеров кода на разных языках.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-364">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="d9c1d-365">Сбои и устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="d9c1d-365">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="d9c1d-366">Замещающий текст</span><span class="sxs-lookup"><span data-stu-id="d9c1d-366">Alt text</span></span>

<span data-ttu-id="d9c1d-367">Замещающий текст, который содержит символы подчеркивания, отображается некорректно.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-367">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="d9c1d-368">Например, вместо</span><span class="sxs-lookup"><span data-stu-id="d9c1d-368">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="d9c1d-369">используйте следующий вариант, позволяющий избежать символов подчеркивания:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-369">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="d9c1d-370">Апострофы и кавычки</span><span class="sxs-lookup"><span data-stu-id="d9c1d-370">Apostrophes and quotation marks</span></span>

<span data-ttu-id="d9c1d-371">Если вы копируете текст из Word в редактор Markdown, он может содержать книжные (изогнутые) апострофы или кавычки.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-371">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="d9c1d-372">Их нужно заменить кодом или обычными апострофами или кавычками.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-372">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="d9c1d-373">В противном случае после публикации файла может отобразиться нечитаемый текст, например Itâ€™s.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-373">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="d9c1d-374">Ниже приведены кодировки для этих знаков пунктуации:</span><span class="sxs-lookup"><span data-stu-id="d9c1d-374">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="d9c1d-375">левая (открывающая) кавычка: `&#8220;`;</span><span class="sxs-lookup"><span data-stu-id="d9c1d-375">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="d9c1d-376">правая (закрывающая) кавычка: `&#8221;`;</span><span class="sxs-lookup"><span data-stu-id="d9c1d-376">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="d9c1d-377">правая закрывающая одинарная кавычка или апостроф: `&#8217;`;</span><span class="sxs-lookup"><span data-stu-id="d9c1d-377">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="d9c1d-378">левая открывающая одинарная кавычка (используется редко): `&#8216;`.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-378">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="d9c1d-379">Угловые скобки</span><span class="sxs-lookup"><span data-stu-id="d9c1d-379">Angle brackets</span></span>

<span data-ttu-id="d9c1d-380">Угловые скобки, как правило, используются для обозначения заполнителя.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-380">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="d9c1d-381">Если вы используете угловые скобки в тексте (а не в коде), их необходимо закодировать.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-381">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="d9c1d-382">Иначе Markdown распознает их как часть тега HTML.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-382">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="d9c1d-383">Например, `<script name>` следует закодировать как `&lt;script name&gt;`.</span><span class="sxs-lookup"><span data-stu-id="d9c1d-383">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="d9c1d-384">Дополнительные материалы</span><span class="sxs-lookup"><span data-stu-id="d9c1d-384">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="d9c1d-385">Ресурсы Markdown</span><span class="sxs-lookup"><span data-stu-id="d9c1d-385">Markdown resources</span></span>

- <span data-ttu-id="d9c1d-386">[Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax) (Синтаксис Markdown)</span><span class="sxs-lookup"><span data-stu-id="d9c1d-386">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- <span data-ttu-id="d9c1d-387">[Markdown cheat-sheet](./media/documents/markdown-cheatsheet.pdf?raw=true) (Шпаргалка по Markdown)</span><span class="sxs-lookup"><span data-stu-id="d9c1d-387">[Docs Markdown cheat sheet](./media/documents/markdown-cheatsheet.pdf?raw=true)</span></span>
- [<span data-ttu-id="d9c1d-388">Базовые сведения о разметке Markdown на GitHub</span><span class="sxs-lookup"><span data-stu-id="d9c1d-388">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- <span data-ttu-id="d9c1d-389">[The Markdown Guide](https://www.markdownguide.org/) (Руководство по Markdown)</span><span class="sxs-lookup"><span data-stu-id="d9c1d-389">[The Markdown Guide](https://www.markdownguide.org/)</span></span>
