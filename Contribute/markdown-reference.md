---
title: Справочник по разметке Markdown для docs.microsoft.com
description: Ознакомьтесь с функциями и синтаксисом Markdown, используемыми на платформе Документации Майкрософт.
author: meganbradley
ms.author: mbradley
ms.date: 03/31/2020
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: f0aed4ebb57ee1ce34f55d9085bab718fd4511cb
ms.sourcegitcommit: 5ef2dc72e2ff8bddf873415a3f4b816eb16029dd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/03/2020
ms.locfileid: "80624733"
---
# <a name="docs-markdown-reference"></a><span data-ttu-id="20255-103">Справочник по Docs Markdown</span><span class="sxs-lookup"><span data-stu-id="20255-103">Docs Markdown reference</span></span>

<span data-ttu-id="20255-104">Эта статья содержит алфавитный справочник по работе с Markdown для docs.microsoft.com (Документация).</span><span class="sxs-lookup"><span data-stu-id="20255-104">This article provides an alphabetical reference for writing Markdown for docs.microsoft.com (Docs).</span></span>

<span data-ttu-id="20255-105">[Markdown](https://daringfireball.net/projects/markdown/) — это облегченный язык разметки с синтаксисом форматирования обычного текста.</span><span class="sxs-lookup"><span data-stu-id="20255-105">[Markdown](https://daringfireball.net/projects/markdown/) is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="20255-106">Документация поддерживает разметку Markdown в соответствии с [CommonMark](https://commonmark.org/) и ее синтаксический анализ через подсистему [Markdig](https://github.com/lunet-io/markdig).</span><span class="sxs-lookup"><span data-stu-id="20255-106">Docs supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="20255-107">Документация также поддерживает пользовательские расширения Markdown, которые предоставляют более обширный контент на сайте документации.</span><span class="sxs-lookup"><span data-stu-id="20255-107">Docs also supports custom Markdown extensions that provide richer content on the Docs site.</span></span>

<span data-ttu-id="20255-108">Для записи Markdown можно использовать любой текстовый редактор, но мы рекомендуем [Visual Studio Code](https://code.visualstudio.com/) с расширением [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack).</span><span class="sxs-lookup"><span data-stu-id="20255-108">You can use any text editor to write Markdown, but we recommend [Visual Studio Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack).</span></span> <span data-ttu-id="20255-109">Расширение Docs Authoring Pack содержит средства редактирования и функции предварительного просмотра, позволяющие увидеть, как будут выглядеть статьи на сайте Документации.</span><span class="sxs-lookup"><span data-stu-id="20255-109">The Docs Authoring Pack provides editing tools and preview functionality that lets you see what your articles will look like when rendered on Docs.</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="20255-110">Оповещения ("Примечание", "Совет", "Важно!", "Внимание!", "Предупреждение")</span><span class="sxs-lookup"><span data-stu-id="20255-110">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="20255-111">Оповещения — это специальные расширения Markdown, которые используются для создания блоков цитирования, отображаемых на сайте docs.microsoft.com с помощью цветов и значков, указывающих на важность содержимого.</span><span class="sxs-lookup"><span data-stu-id="20255-111">Alerts are a Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="20255-112">Поддерживаются следующие типы оповещений:</span><span class="sxs-lookup"><span data-stu-id="20255-112">The following alert types are supported:</span></span>

```markdown
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

<span data-ttu-id="20255-113">На сайте docs.microsoft.com эти оповещения отображаются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="20255-113">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="20255-114">Информация, которую пользователь должен заметить даже при беглом просмотре.</span><span class="sxs-lookup"><span data-stu-id="20255-114">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="20255-115">Дополнительные сведения, помогающие пользователю лучше решить задачу.</span><span class="sxs-lookup"><span data-stu-id="20255-115">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="20255-116">Важные сведения для успешного решения задачи.</span><span class="sxs-lookup"><span data-stu-id="20255-116">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="20255-117">Потенциальные негативные последствия действия.</span><span class="sxs-lookup"><span data-stu-id="20255-117">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="20255-118">Опасные последствия действия.</span><span class="sxs-lookup"><span data-stu-id="20255-118">Dangerous certain consequences of an action.</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="20255-119">Угловые скобки</span><span class="sxs-lookup"><span data-stu-id="20255-119">Angle brackets</span></span>

<span data-ttu-id="20255-120">Если в тексте файла используются угловые скобки (например, для обозначения заполнителя), их нужно кодировать вручную.</span><span class="sxs-lookup"><span data-stu-id="20255-120">If you use angle brackets in text in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="20255-121">В противном случае разметка Markdown считает их HTML-тегами.</span><span class="sxs-lookup"><span data-stu-id="20255-121">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="20255-122">Например, `<script name>` следует закодировать как `&lt;script name&gt;` или `\<script name>`.</span><span class="sxs-lookup"><span data-stu-id="20255-122">For example, encode `<script name>` as `&lt;script name&gt;` or `\<script name>`.</span></span>

<span data-ttu-id="20255-123">Угловые скобки не обязательно должны быть экранированы в тексте, отформатированном как встроенный код, или в блоках кода.</span><span class="sxs-lookup"><span data-stu-id="20255-123">Angle brackets don't have to be escaped in text formatted as inline code or in code blocks.</span></span>

## <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="20255-124">Апострофы и кавычки</span><span class="sxs-lookup"><span data-stu-id="20255-124">Apostrophes and quotation marks</span></span>

<span data-ttu-id="20255-125">Если вы копируете текст из Word в редактор Markdown, он может содержать книжные (изогнутые) апострофы или кавычки.</span><span class="sxs-lookup"><span data-stu-id="20255-125">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="20255-126">Их нужно заменить кодом или обычными апострофами или кавычками.</span><span class="sxs-lookup"><span data-stu-id="20255-126">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="20255-127">В противном случае после публикации файла может отобразиться нечитаемый текст, например: Itâ&euro;&trade;s</span><span class="sxs-lookup"><span data-stu-id="20255-127">Otherwise, you end up with things like this when the file is published: Itâ&euro;&trade;s</span></span>

<span data-ttu-id="20255-128">Ниже приведены кодировки для этих знаков пунктуации:</span><span class="sxs-lookup"><span data-stu-id="20255-128">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="20255-129">левая (открывающая) кавычка: `&#8220;`;</span><span class="sxs-lookup"><span data-stu-id="20255-129">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="20255-130">правая (закрывающая) кавычка: `&#8221;`;</span><span class="sxs-lookup"><span data-stu-id="20255-130">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="20255-131">правая закрывающая одинарная кавычка или апостроф: `&#8217;`;</span><span class="sxs-lookup"><span data-stu-id="20255-131">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="20255-132">левая открывающая одинарная кавычка (используется редко): `&#8216;`.</span><span class="sxs-lookup"><span data-stu-id="20255-132">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

## <a name="blockquotes"></a><span data-ttu-id="20255-133">Блоки цитирования</span><span class="sxs-lookup"><span data-stu-id="20255-133">Blockquotes</span></span>

<span data-ttu-id="20255-134">Блоки цитирования создаются с помощью символа `>`:</span><span class="sxs-lookup"><span data-stu-id="20255-134">Blockquotes are created using the `>` character:</span></span>

```md
> This is a blockquote. It is usually rendered indented and with a different background color.
```

<span data-ttu-id="20255-135">Предыдущий пример отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="20255-135">The preceding example renders as follows:</span></span>

> <span data-ttu-id="20255-136">Это блок цитирования.</span><span class="sxs-lookup"><span data-stu-id="20255-136">This is a blockquote.</span></span> <span data-ttu-id="20255-137">Обычно он отображается с отступом и имеет другой цвет фона.</span><span class="sxs-lookup"><span data-stu-id="20255-137">It is usually rendered indented and with a different background color.</span></span>

## <a name="bold-and-italic-text"></a><span data-ttu-id="20255-138">Полужирное и курсивное начертания</span><span class="sxs-lookup"><span data-stu-id="20255-138">Bold and italic text</span></span>

<span data-ttu-id="20255-139">Чтобы задать для текста **полужирное начертание**, заключите его в двойные звездочки:</span><span class="sxs-lookup"><span data-stu-id="20255-139">To format text as **bold**, enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="20255-140">Чтобы задать для текста *курсивное начертание*, заключите его в одинарные звездочки:</span><span class="sxs-lookup"><span data-stu-id="20255-140">To format text as *italic*, enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="20255-141">Чтобы задать для текста ***полужирное и курсивное*** начертание, заключите его в тройные звездочки:</span><span class="sxs-lookup"><span data-stu-id="20255-141">To format text as both ***bold and italic***, enclose it in three asterisks:</span></span>

```markdown
This text is both ***bold and italic***.
```

## <a name="code-snippets"></a><span data-ttu-id="20255-142">Фрагменты кода</span><span class="sxs-lookup"><span data-stu-id="20255-142">Code snippets</span></span>

<span data-ttu-id="20255-143">Расширение Docs Markdown поддерживает как встраивание фрагментов кода в предложение, так и их размещение между предложениями в виде отдельных огражденных блоков.</span><span class="sxs-lookup"><span data-stu-id="20255-143">Docs Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="20255-144">Дополнительные сведения см. в разделе [Как добавить код в документацию](code-in-docs.md).</span><span class="sxs-lookup"><span data-stu-id="20255-144">For more information, see [How to add code to docs](code-in-docs.md).</span></span>

## <a name="columns"></a><span data-ttu-id="20255-145">Столбцы</span><span class="sxs-lookup"><span data-stu-id="20255-145">Columns</span></span>

<span data-ttu-id="20255-146">Расширение Markdown **столбцы** дает авторам документации возможность добавлять макеты содержимого на основе столбцов, которые являются более гибкими и эффективными, чем базовые таблицы Markdown, подходящие только для действительно табличных данных.</span><span class="sxs-lookup"><span data-stu-id="20255-146">The **columns** Markdown extension gives Docs authors the ability to add column-based content layouts that are more flexible and powerful than basic Markdown tables, which are only suited for true tabular data.</span></span> <span data-ttu-id="20255-147">Можно добавить до четырех столбцов и использовать необязательный атрибут `span` для объединения двух или более столбцов.</span><span class="sxs-lookup"><span data-stu-id="20255-147">You can add up to four columns, and use the optional `span` attribute to merge two or more columns.</span></span>

<span data-ttu-id="20255-148">Используйте следующий синтаксис для столбцов:</span><span class="sxs-lookup"><span data-stu-id="20255-148">The syntax for columns is as follows:</span></span>

```markdown
:::row:::
   :::column span="":::
      Content...
   :::column-end:::
   :::column span="":::
      More content...
   :::column-end:::
:::row-end:::
```

<span data-ttu-id="20255-149">Столбцы должны содержать только базовый Markdown, включая изображения.</span><span class="sxs-lookup"><span data-stu-id="20255-149">Columns should only contain basic Markdown, including images.</span></span> <span data-ttu-id="20255-150">Заголовки, таблицы, вкладки и другие сложные структуры не должны включаться.</span><span class="sxs-lookup"><span data-stu-id="20255-150">Headings, tables, tabs, and other complex structures shouldn't be included.</span></span> <span data-ttu-id="20255-151">Строка не может иметь содержимое вне столбца.</span><span class="sxs-lookup"><span data-stu-id="20255-151">A row can't have any content outside of column.</span></span>

<span data-ttu-id="20255-152">Например, следующий Markdown создает один столбец, охватывающий две ширины столбца, и один стандартный столбец (без `span`):</span><span class="sxs-lookup"><span data-stu-id="20255-152">For example, the following Markdown creates one column that spans two column widths, and one standard (no `span`) column:</span></span>

```markdown
:::row:::
   :::column span="2":::
      **This is a 2-span column with lots of text.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc
      ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec
      rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **This is a single-span column with an image in it.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::
```

<span data-ttu-id="20255-153">Это отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="20255-153">This renders as follows:</span></span>

:::row:::
   :::column span="2":::
      <span data-ttu-id="20255-154">**Это столбец двойной ширины с большим объемом текста.**</span><span class="sxs-lookup"><span data-stu-id="20255-154">**This is a 2-span column with lots of text.**</span></span>

      <span data-ttu-id="20255-155">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span><span class="sxs-lookup"><span data-stu-id="20255-155">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span></span> <span data-ttu-id="20255-156">Donec vestibulum mollis nunc ornare commodo.</span><span class="sxs-lookup"><span data-stu-id="20255-156">Donec vestibulum mollis nunc ornare commodo.</span></span> <span data-ttu-id="20255-157">Nullam ac metus imperdiet, rutrum justo vel, vulputate leo.</span><span class="sxs-lookup"><span data-stu-id="20255-157">Nullam ac metus imperdiet, rutrum justo vel, vulputate leo.</span></span> <span data-ttu-id="20255-158">Donec rutrum non eros eget consectetur.</span><span class="sxs-lookup"><span data-stu-id="20255-158">Donec rutrum non eros eget consectetur.</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="20255-159">**Это столбец одинарной ширины с изображением.**</span><span class="sxs-lookup"><span data-stu-id="20255-159">**This is a single-span column with an image in it.**</span></span>

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::

## <a name="headings"></a><span data-ttu-id="20255-161">Заголовки</span><span class="sxs-lookup"><span data-stu-id="20255-161">Headings</span></span>

<span data-ttu-id="20255-162">Платформа Docs поддерживает шесть уровней заголовков Markdown:</span><span class="sxs-lookup"><span data-stu-id="20255-162">Docs supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="20255-163">Между последним символом `#` и содержимым заголовка должен присутствовать пробел.</span><span class="sxs-lookup"><span data-stu-id="20255-163">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="20255-164">В одном файле Markdown должен быть один и только один заголовок H1.</span><span class="sxs-lookup"><span data-stu-id="20255-164">Each Markdown file must have one and only one H1 heading.</span></span>
- <span data-ttu-id="20255-165">Заголовок H1 указывается в файле в первую очередь, сразу после блока метаданных YML.</span><span class="sxs-lookup"><span data-stu-id="20255-165">The H1 heading must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="20255-166">Заголовки H2 автоматически отображаются в правом меню навигации опубликованного файла.</span><span class="sxs-lookup"><span data-stu-id="20255-166">H2 headings automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="20255-167">Заголовки более низкого уровня не отображаются, поэтому для удобства перехода по содержимому рекомендуется использовать заголовки H2.</span><span class="sxs-lookup"><span data-stu-id="20255-167">Lower-level headings don't appear, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="20255-168">Использовать заголовки HTML, такие как `<h1>`, не рекомендуется, и в некоторых случаях из-за них могут возникать предупреждения при сборке.</span><span class="sxs-lookup"><span data-stu-id="20255-168">HTML headings, such as `<h1>`, aren't recommended, and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="20255-169">Привязка к отдельным заголовкам в файле выполняется с помощью [ссылок на закладки](how-to-write-links.md#explicit-anchor-links).</span><span class="sxs-lookup"><span data-stu-id="20255-169">You can link to individual headings in a file via [bookmark links](how-to-write-links.md#explicit-anchor-links).</span></span>

## <a name="html"></a><span data-ttu-id="20255-170">HTML</span><span class="sxs-lookup"><span data-stu-id="20255-170">HTML</span></span>

<span data-ttu-id="20255-171">Хотя Markdown поддерживает встроенный HTML-код, HTML не рекомендуется использовать для публикации на сайте Документации. Любой код, за исключением ограниченного списка значений, будет вызывать появление ошибок и предупреждений при сборке.</span><span class="sxs-lookup"><span data-stu-id="20255-171">Although Markdown supports inline HTML, HTML isn't recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span>

## <a name="images"></a><span data-ttu-id="20255-172">Изображения</span><span class="sxs-lookup"><span data-stu-id="20255-172">Images</span></span>

<span data-ttu-id="20255-173">Для изображений по умолчанию поддерживаются следующие типы файлов:</span><span class="sxs-lookup"><span data-stu-id="20255-173">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="20255-174">JPG,</span><span class="sxs-lookup"><span data-stu-id="20255-174">.jpg</span></span>
- <span data-ttu-id="20255-175">PNG.</span><span class="sxs-lookup"><span data-stu-id="20255-175">.png</span></span>

### <a name="standard-conceptual-images-default-markdown"></a><span data-ttu-id="20255-176">Стандартные схематические изображения (Markdown по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="20255-176">Standard conceptual images (default Markdown)</span></span>

<span data-ttu-id="20255-177">Базовый синтаксис Markdown для внедрения изображения:</span><span class="sxs-lookup"><span data-stu-id="20255-177">The basic Markdown syntax to embed an image is:</span></span>

```Markdown
![<alt text>](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="20255-178">Где `<alt text>` — краткое описание изображения, а `<folder path>` — относительный путь к нему.</span><span class="sxs-lookup"><span data-stu-id="20255-178">Where `<alt text>` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="20255-179">Заменяющий текст необходим для средств чтения с экрана для слабовидящих.</span><span class="sxs-lookup"><span data-stu-id="20255-179">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="20255-180">Он также удобен при возникновении ошибок на сайте, из-за которых не удается воспроизвести изображение.</span><span class="sxs-lookup"><span data-stu-id="20255-180">It's also useful if there's a site bug where the image can't render.</span></span>

<span data-ttu-id="20255-181">Знаки подчеркивания в замещающем тексте не отображаются должным образом, если они не экранированы с помощью префикса — обратной косой черты (`\_`).</span><span class="sxs-lookup"><span data-stu-id="20255-181">Underscores in alt text aren't rendered properly unless you escape them by prefixing them with a backslash (`\_`).</span></span> <span data-ttu-id="20255-182">Но не стоит копировать имена файлов для использования в качестве замещающего текста.</span><span class="sxs-lookup"><span data-stu-id="20255-182">However, don't copy file names for use as alt text.</span></span> <span data-ttu-id="20255-183">Например, вместо:</span><span class="sxs-lookup"><span data-stu-id="20255-183">For example, instead of this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="20255-184">Напишите:</span><span class="sxs-lookup"><span data-stu-id="20255-184">Write this:</span></span>

```markdown
![Active Directory extension for two-factor authentication, step 4: Configure](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="standard-conceptual-images-docs-markdown"></a><span data-ttu-id="20255-185">Стандартные схематические изображения (Docs Markdown)</span><span class="sxs-lookup"><span data-stu-id="20255-185">Standard conceptual images (Docs Markdown)</span></span>

<span data-ttu-id="20255-186">Пользовательское расширение "Документация" `:::image:::` поддерживает стандартные изображения, сложные изображения и значки.</span><span class="sxs-lookup"><span data-stu-id="20255-186">The Docs custom `:::image:::` extension supports standard images, complex images, and icons.</span></span>

<span data-ttu-id="20255-187">Для стандартных изображений старый синтаксис Markdown по-прежнему будет работать, но рекомендуется использовать новое расширение, так как оно поддерживает более широкие функциональные возможности, такие как указание области локализации, отличной от родительской темы.</span><span class="sxs-lookup"><span data-stu-id="20255-187">For standard images, the older Markdown syntax will still work, but the new extension is recommended because it supports more powerful functionality, such as specifying a localization scope that's different from the parent topic.</span></span> <span data-ttu-id="20255-188">В будущем будут доступны другие расширенные функции, такие как выбор из общей коллекции изображений вместо указания локального изображения.</span><span class="sxs-lookup"><span data-stu-id="20255-188">Other advanced functionality, such as selecting from the shared image gallery instead of specifying a local image, will be available in the future.</span></span> <span data-ttu-id="20255-189">Используйте следующий новый синтаксис:</span><span class="sxs-lookup"><span data-stu-id="20255-189">The new syntax is as follows:</span></span>

```Markdown
:::image type="content" source="<folderPath>" alt-text="<alt text>":::
```

<span data-ttu-id="20255-190">Если `type="content"` (по умолчанию), требуются `source` и `alt-text`.</span><span class="sxs-lookup"><span data-stu-id="20255-190">If `type="content"` (the default), both `source` and `alt-text` are required.</span></span>

### <a name="complex-images-with-long-descriptions"></a><span data-ttu-id="20255-191">Сложные изображения с длинными описаниями</span><span class="sxs-lookup"><span data-stu-id="20255-191">Complex images with long descriptions</span></span>

<span data-ttu-id="20255-192">Это расширение также можно использовать для добавления изображения с длинным описанием, которое считывается программами чтения с экрана, но не отображается визуально на опубликованной странице.</span><span class="sxs-lookup"><span data-stu-id="20255-192">You can also use this extension to add an image with a long description that is read by screen readers but not rendered visually on the published page.</span></span> <span data-ttu-id="20255-193">Длинные описания являются требованием для специальных возможностей для сложных изображений, таких как диаграммы.</span><span class="sxs-lookup"><span data-stu-id="20255-193">Long descriptions are an accessibility requirement for complex images, such as graphs.</span></span> <span data-ttu-id="20255-194">Используется следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="20255-194">The syntax is the following:</span></span>

```Markdown
:::image type="complex" source="<folderPath>" alt-text="<alt text>":::
   <long description here>
:::image-end:::
```

<span data-ttu-id="20255-195">Если `type="complex"`, `source`, `alt-text`, требуется длинное описание и тег `:::image-end:::`.</span><span class="sxs-lookup"><span data-stu-id="20255-195">If `type="complex"`, `source`, `alt-text`, a long description, and the `:::image-end:::` tag are all required.</span></span>

### <a name="specifying-loc-scope"></a><span data-ttu-id="20255-196">Указание области локализации</span><span class="sxs-lookup"><span data-stu-id="20255-196">Specifying loc-scope</span></span>

<span data-ttu-id="20255-197">Иногда область локализации для изображения отличается от области локализации для статьи или модуля, в которых оно содержится.</span><span class="sxs-lookup"><span data-stu-id="20255-197">Sometimes the localization scope for an image is different from that of the article or module that contains it.</span></span> <span data-ttu-id="20255-198">Это может привести к неправильному глобальному интерфейсу: например, если снимок экрана продукта случайно локализован на язык, на котором продукт недоступен.</span><span class="sxs-lookup"><span data-stu-id="20255-198">This can cause a bad global experience: for example, if a screenshot of a product is accidentally localized into a language the product isn't available in.</span></span> <span data-ttu-id="20255-199">Чтобы избежать этого, можно указать необязательный атрибут `loc-scope` в изображениях типов `content` и `complex`.</span><span class="sxs-lookup"><span data-stu-id="20255-199">To prevent this, you can specify the optional `loc-scope` attribute in images of types `content` and `complex`.</span></span>

### <a name="icons"></a><span data-ttu-id="20255-200">Значки</span><span class="sxs-lookup"><span data-stu-id="20255-200">Icons</span></span>

<span data-ttu-id="20255-201">Расширение изображения поддерживает значки, которые являются декоративными изображениями и не должны иметь замещающий текст.</span><span class="sxs-lookup"><span data-stu-id="20255-201">The image extension supports icons, which are decorative images and should not have alt text.</span></span> <span data-ttu-id="20255-202">Для значков используется следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="20255-202">The syntax for icons is:</span></span>

```Markdown
:::image type="icon" source="<folderPath>":::
```

<span data-ttu-id="20255-203">Если `type="icon"`, нужно указать только `source`.</span><span class="sxs-lookup"><span data-stu-id="20255-203">If `type="icon"`, only `source` should be specified.</span></span>

## <a name="included-markdown-files"></a><span data-ttu-id="20255-204">Включаемые файлы Markdown</span><span class="sxs-lookup"><span data-stu-id="20255-204">Included Markdown files</span></span>

<span data-ttu-id="20255-205">Если файлы Markdown необходимо повторить в нескольких статьях, можно использовать включаемый файл.</span><span class="sxs-lookup"><span data-stu-id="20255-205">Where markdown files need to be repeated in multiple articles, you can use an include file.</span></span> <span data-ttu-id="20255-206">Функция включения указывает сайту Документации заменить ссылку на содержимое включаемого файла во время сборки.</span><span class="sxs-lookup"><span data-stu-id="20255-206">The includes feature instructs Docs to replace the reference with the contents of the include file at build time.</span></span> <span data-ttu-id="20255-207">Для включения можно использовать следующие способы.</span><span class="sxs-lookup"><span data-stu-id="20255-207">You can use includes in the following ways:</span></span>

- <span data-ttu-id="20255-208">Встроенные: используются для многократного использования фрагмента стандартного текста путем его встраивания в предложение.</span><span class="sxs-lookup"><span data-stu-id="20255-208">Inline: Reuse a common text snippet inline with within a sentence.</span></span>
- <span data-ttu-id="20255-209">Блочные: Используются для многократного использования всего файла Markdown в качестве блока путем его вложения в раздел или статью.</span><span class="sxs-lookup"><span data-stu-id="20255-209">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>

<span data-ttu-id="20255-210">Встроенные и блочные включаемые файлы — это файлы Markdown с расширением MD.</span><span class="sxs-lookup"><span data-stu-id="20255-210">An inline or block include file is a Markdown (.md) file.</span></span> <span data-ttu-id="20255-211">Они могут содержать любую допустимую разметку Markdown.</span><span class="sxs-lookup"><span data-stu-id="20255-211">It can contain any valid Markdown.</span></span> <span data-ttu-id="20255-212">Включаемые файлы обычно находятся в общем подкаталоге *includes* в корне репозитория.</span><span class="sxs-lookup"><span data-stu-id="20255-212">Include files are typically located in a common *includes* subdirectory, in the root of the repository.</span></span> <span data-ttu-id="20255-213">Когда статья публикуется, включаемый файл легко интегрируется в нее.</span><span class="sxs-lookup"><span data-stu-id="20255-213">When the article is published, the included file is seamlessly integrated into it.</span></span>

### <a name="includes-syntax"></a><span data-ttu-id="20255-214">Синтаксис включаемых файлов</span><span class="sxs-lookup"><span data-stu-id="20255-214">Includes syntax</span></span>

<span data-ttu-id="20255-215">Блочные включаемые файлы находятся в отдельной строке:</span><span class="sxs-lookup"><span data-stu-id="20255-215">Block include is on its own line:</span></span>

```markdown
[!INCLUDE [<title>](<filepath>)]
```

<span data-ttu-id="20255-216">Встроенные включаемые файлы находятся в строке:</span><span class="sxs-lookup"><span data-stu-id="20255-216">Inline include is within a line:</span></span>

```markdown
Text before [!INCLUDE [<title>](<filepath>)] and after.
```

<span data-ttu-id="20255-217">Где `<title>` — имя файла, а `<filepath>` — относительный путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="20255-217">Where `<title>` is the name of the file and `<filepath>` is the relative path to the file.</span></span> <span data-ttu-id="20255-218">Слово `INCLUDE` должно быть написано прописными буквами, а перед `<title>` должен быть пробел.</span><span class="sxs-lookup"><span data-stu-id="20255-218">`INCLUDE` must be capitalized and there must be a space before the `<title>`.</span></span>

<span data-ttu-id="20255-219">Ниже приведены требования к включаемым файлам и соображения по работе с ними:</span><span class="sxs-lookup"><span data-stu-id="20255-219">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="20255-220">Блочные включаемые файлы предназначены для значительных объемов текста: один или два абзаца, общая процедура или общий раздел.</span><span class="sxs-lookup"><span data-stu-id="20255-220">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="20255-221">Не используйте их для фрагментов текста меньше одного предложения.</span><span class="sxs-lookup"><span data-stu-id="20255-221">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="20255-222">Включаемые файлы не отображаются в представлении статьи на сайте GitHub. Они используют расширения "Документация".</span><span class="sxs-lookup"><span data-stu-id="20255-222">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Docs extensions.</span></span> <span data-ttu-id="20255-223">Они отображаются только после публикации.</span><span class="sxs-lookup"><span data-stu-id="20255-223">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="20255-224">Весь текст во включаемом файле должен состоять из полноценных предложений или фраз, не зависящих от остального текста статьи, в которую добавляется ссылка на такой файл.</span><span class="sxs-lookup"><span data-stu-id="20255-224">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="20255-225">Если не следовать этой инструкции, в статье создаются непереводимые строки.</span><span class="sxs-lookup"><span data-stu-id="20255-225">Ignoring this guidance creates an untranslatable string in the article.</span></span>
- <span data-ttu-id="20255-226">Не внедряйте одни включаемые файлы в другие.</span><span class="sxs-lookup"><span data-stu-id="20255-226">Don't embed include files within other include files.</span></span>
- <span data-ttu-id="20255-227">Файлы мультимедиа должны быть помещены в отдельную папку мультимедиа в подкаталоге включаемых файлов. Например, `<repo>` */includes/media*.</span><span class="sxs-lookup"><span data-stu-id="20255-227">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`*/includes/media* folder.</span></span> <span data-ttu-id="20255-228">В корне каталога *media* не должны содержаться изображения.</span><span class="sxs-lookup"><span data-stu-id="20255-228">The *media* directory should not contain any images in its root.</span></span> <span data-ttu-id="20255-229">Если во включаемом файле нет изображений, соответствующий каталог *media* не требуется.</span><span class="sxs-lookup"><span data-stu-id="20255-229">If the include does not have images, a corresponding *media* directory is not required.</span></span>
- <span data-ttu-id="20255-230">Как и в обычных статьях, не используйте общий файл мультимедиа для включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="20255-230">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="20255-231">Для каждого включаемого файла в статье должен быть создан отдельный файл мультимедиа с уникальным именем.</span><span class="sxs-lookup"><span data-stu-id="20255-231">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="20255-232">Файл мультимедиа должен храниться в папке мультимедиа, связанной с включаемым файлом.</span><span class="sxs-lookup"><span data-stu-id="20255-232">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="20255-233">Не используйте включаемый файл как единственное содержимое статьи.</span><span class="sxs-lookup"><span data-stu-id="20255-233">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="20255-234">Включаемые файлы предназначены для дополнения основных материалов статьи.</span><span class="sxs-lookup"><span data-stu-id="20255-234">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

## <a name="links"></a><span data-ttu-id="20255-235">Создание ссылок</span><span class="sxs-lookup"><span data-stu-id="20255-235">Links</span></span>

<span data-ttu-id="20255-236">Сведения о синтаксисе ссылок см. в разделе [Использование ссылок в документации](how-to-write-links.md).</span><span class="sxs-lookup"><span data-stu-id="20255-236">For information on syntax for links, see [Use links in documentation](how-to-write-links.md).</span></span>

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="20255-237">Списки (нумерованные, маркированные, контрольные)</span><span class="sxs-lookup"><span data-stu-id="20255-237">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="20255-238">Нумерованный список</span><span class="sxs-lookup"><span data-stu-id="20255-238">Numbered list</span></span>

<span data-ttu-id="20255-239">Чтобы создать нумерованный список, можно использовать все единицы.</span><span class="sxs-lookup"><span data-stu-id="20255-239">To create a numbered list, you can use all 1s.</span></span> <span data-ttu-id="20255-240">При публикации числа отображаются в возрастающем порядке в виде последовательного списка.</span><span class="sxs-lookup"><span data-stu-id="20255-240">The numbers are rendered in ascending order as a sequential list when published.</span></span> <span data-ttu-id="20255-241">Для повышения удобства чтения исходного кода списки можно вводить с приращением вручную.</span><span class="sxs-lookup"><span data-stu-id="20255-241">For increased source readability, you can increment your lists manually.</span></span>

<span data-ttu-id="20255-242">Не используйте в списках, включая вложенные списки, буквы.</span><span class="sxs-lookup"><span data-stu-id="20255-242">Don't use letters in lists, including nested lists.</span></span> <span data-ttu-id="20255-243">При публикации на сайте документации они отображаются некорректно. Вложенные списки с цифрами преобразуются в списки со строчными буквами при публикации.</span><span class="sxs-lookup"><span data-stu-id="20255-243">They don't render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="20255-244">Например:</span><span class="sxs-lookup"><span data-stu-id="20255-244">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="20255-245">Это отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="20255-245">This renders as follows:</span></span>

1. <span data-ttu-id="20255-246">Это</span><span class="sxs-lookup"><span data-stu-id="20255-246">This is</span></span>
1. <span data-ttu-id="20255-247">родительский нумерованный список,</span><span class="sxs-lookup"><span data-stu-id="20255-247">a parent numbered list</span></span>
   1. <span data-ttu-id="20255-248">а это</span><span class="sxs-lookup"><span data-stu-id="20255-248">and this is</span></span>
   1. <span data-ttu-id="20255-249">вложенный нумерованный список</span><span class="sxs-lookup"><span data-stu-id="20255-249">a nested numbered list</span></span>
1. <span data-ttu-id="20255-250">(конец)</span><span class="sxs-lookup"><span data-stu-id="20255-250">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="20255-251">Маркированный список</span><span class="sxs-lookup"><span data-stu-id="20255-251">Bulleted list</span></span>

<span data-ttu-id="20255-252">Для создания маркированного списка используйте `-` или `*`, за которым следует пробел в начале каждой строки:</span><span class="sxs-lookup"><span data-stu-id="20255-252">To create a bulleted list, use `-` or `*` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="20255-253">Это отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="20255-253">This renders as follows:</span></span>

- <span data-ttu-id="20255-254">Это</span><span class="sxs-lookup"><span data-stu-id="20255-254">This is</span></span>
- <span data-ttu-id="20255-255">родительский маркированный список,</span><span class="sxs-lookup"><span data-stu-id="20255-255">a parent bulleted list</span></span>
  - <span data-ttu-id="20255-256">а это</span><span class="sxs-lookup"><span data-stu-id="20255-256">and this is</span></span>
  - <span data-ttu-id="20255-257">вложенный маркированный список</span><span class="sxs-lookup"><span data-stu-id="20255-257">a nested bulleted list</span></span>
- <span data-ttu-id="20255-258">Готово!</span><span class="sxs-lookup"><span data-stu-id="20255-258">All done!</span></span>

<span data-ttu-id="20255-259">Независимо от используемого синтаксиса, `-` или `*`, используйте его согласованно в статье.</span><span class="sxs-lookup"><span data-stu-id="20255-259">Whichever syntax you use, `-` or `*`, use it consistently within an article.</span></span>

### <a name="checklist"></a><span data-ttu-id="20255-260">Контрольный список</span><span class="sxs-lookup"><span data-stu-id="20255-260">Checklist</span></span>

<span data-ttu-id="20255-261">Контрольные списки можно использовать на сайте документации с помощью пользовательского расширения Markdown:</span><span class="sxs-lookup"><span data-stu-id="20255-261">Checklists are available for use on Docs via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="20255-262">Этот пример отображается на сайте документации следующим образом:</span><span class="sxs-lookup"><span data-stu-id="20255-262">This example renders on Docs like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="20255-263">List item 1</span><span class="sxs-lookup"><span data-stu-id="20255-263">List item 1</span></span>
> * <span data-ttu-id="20255-264">List item 2</span><span class="sxs-lookup"><span data-stu-id="20255-264">List item 2</span></span>
> * <span data-ttu-id="20255-265">List item 3</span><span class="sxs-lookup"><span data-stu-id="20255-265">List item 3</span></span>

<span data-ttu-id="20255-266">Контрольные списки используются в начале или конце статьи для подведения итогов "Чему вы научитесь" или "Чему вы научились".</span><span class="sxs-lookup"><span data-stu-id="20255-266">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="20255-267">Не вставляйте контрольные списки в статьи по случайному принципу.</span><span class="sxs-lookup"><span data-stu-id="20255-267">Do not add random checklists throughout your articles.</span></span>

## <a name="next-step-action"></a><span data-ttu-id="20255-268">Действие "Дальнейшие действия"</span><span class="sxs-lookup"><span data-stu-id="20255-268">Next step action</span></span>

<span data-ttu-id="20255-269">Пользовательское расширение можно использовать для добавления кнопки "Дальнейшие действия" на страницы сайта Документации.</span><span class="sxs-lookup"><span data-stu-id="20255-269">You can use a custom extension to add a next step action button to Docs pages.</span></span>

<span data-ttu-id="20255-270">Используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="20255-270">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="20255-271">Например:</span><span class="sxs-lookup"><span data-stu-id="20255-271">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about adding code to articles](code-in-docs.md)
```

<span data-ttu-id="20255-272">Это отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="20255-272">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="20255-273">Дополнительные сведения о добавлении кода в статьи</span><span class="sxs-lookup"><span data-stu-id="20255-273">Learn about adding code to articles</span></span>](code-in-docs.md)

<span data-ttu-id="20255-274">Вы можете использовать любые поддерживаемые ссылки в действии "Дальнейшие действия", включая ссылку Markdown на другую веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="20255-274">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="20255-275">Как правило, ссылка "Дальнейшие действия" — это относительная ссылка на другой файл в том же наборе документации.</span><span class="sxs-lookup"><span data-stu-id="20255-275">In most cases, the next action link will be a relative link to another file in the same docset.</span></span>

## <a name="non-localized-strings"></a><span data-ttu-id="20255-276">Нелокализованные строки</span><span class="sxs-lookup"><span data-stu-id="20255-276">Non-localized strings</span></span>

<span data-ttu-id="20255-277">Вы можете использовать пользовательское расширение Markdown `no-loc`, чтобы указать строки содержимого, не подлежащие локализации.</span><span class="sxs-lookup"><span data-stu-id="20255-277">You can use the custom `no-loc` Markdown extension to identify strings of content that you would like the localization process to ignore.</span></span>

<span data-ttu-id="20255-278">Для всех указанных строк учитывается регистр; то есть строка должна полностью соответствовать указанному значению, чтобы игнорироваться при локализации.</span><span class="sxs-lookup"><span data-stu-id="20255-278">All strings called out will be case-sensitive; that is, the string must match exactly to be ignored for localization.</span></span>

<span data-ttu-id="20255-279">Чтобы пометить отдельную строку как не подлежащую локализации, используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="20255-279">To mark an individual string as non-localizable, use this syntax:</span></span>

```markdown
:::no-loc text="String":::
```

<span data-ttu-id="20255-280">Например, в следующем примере только один экземпляр `Document` будет игнорироваться в процессе локализации:</span><span class="sxs-lookup"><span data-stu-id="20255-280">For example, in the following, only the single instance of `Document` will be ignored during the localization process:</span></span>

```markdown
# Heading 1 of the Document

Markdown content within the :::no-loc text="Document":::.  The are multiple instances of Document, document, and documents.
```

> [!NOTE]
> <span data-ttu-id="20255-281">Используйте `\`, чтобы экранировать специальные символы:</span><span class="sxs-lookup"><span data-stu-id="20255-281">Use `\` to escape special characters:</span></span>
> ```markdown
> Lorem :::no-loc text="Find a \"Quotation\""::: Ipsum.
> ```

<span data-ttu-id="20255-282">Можно также использовать метаданные в заголовке YAML, чтобы пометить все экземпляры строки в текущем файле Markdown как нелокализуемые:</span><span class="sxs-lookup"><span data-stu-id="20255-282">You can also use metadata in the YAML header to mark all instances of a string within the current Markdown file as non-localizable:</span></span>

```yml
author: cillroy
no-loc: [Global, Strings, to be, Ignored]
```

> [!NOTE]
> <span data-ttu-id="20255-283">Метаданные no-loc не поддерживаются в качестве глобальных метаданных в файле *docfx.json*.</span><span class="sxs-lookup"><span data-stu-id="20255-283">The no-loc metadata is not supported as global metadata in *docfx.json* file.</span></span> <span data-ttu-id="20255-284">Конвейер локализации не считывает файл *docfx.json*, поэтому метаданные no-loc должны быть добавлены в каждый отдельный исходный файл.</span><span class="sxs-lookup"><span data-stu-id="20255-284">The localization pipeline doesn't read the *docfx.json* file, so the no-loc metadata must be added into each individual source file.</span></span>

<span data-ttu-id="20255-285">В следующем примере и в метаданных `title`, и в заголовке Markdown слово `Document` будет игнорироваться в процессе локализации.</span><span class="sxs-lookup"><span data-stu-id="20255-285">In the following example, both in the metadata `title` and the Markdown header the word `Document` will be ignored during the localization process.</span></span>

<span data-ttu-id="20255-286">В метаданных `description` и основном содержимом Markdown слово `document` локализовано, так как оно не начинается с прописной буквы `D`.</span><span class="sxs-lookup"><span data-stu-id="20255-286">In the metadata `description` and the Markdown main content the word `document` is localized, because it does not start with a capital `D`.</span></span>

```markdown
---
title: Title of the Document
author: author-name
description: Description for the document
no-loc: [Title, Document]
---
# Heading 1 of the Document

Markdown content within the document.
```

<!-- commenting out for now because no one knows what this means
## Section definition

You might need to define a section. This syntax is mostly used for code tables.
See the following example:

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

The preceding blockquote Markdown text will be rendered as:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
-->

## <a name="selectors"></a><span data-ttu-id="20255-287">Селекторы</span><span class="sxs-lookup"><span data-stu-id="20255-287">Selectors</span></span>

<span data-ttu-id="20255-288">Селекторы — это элементы пользовательского интерфейса, позволяющие пользователю переключаться между несколькими разновидностями одной и той же статьи.</span><span class="sxs-lookup"><span data-stu-id="20255-288">Selectors are UI elements that let the user switch between multiple flavors of the same article.</span></span> <span data-ttu-id="20255-289">Они используются в некоторых наборах документов для реализаций разных технологий или платформ.</span><span class="sxs-lookup"><span data-stu-id="20255-289">They are used in some doc sets to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="20255-290">Селекторы обычно применяются к материалам о мобильных платформах для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="20255-290">Selectors are typically most applicable to our mobile platform content for developers.</span></span>

<span data-ttu-id="20255-291">В каждой статье с возможностью выбора используется одна и та же разметка Markdown для селектора. Поэтому рекомендуется поместить селектор для статьи во включаемый файл.</span><span class="sxs-lookup"><span data-stu-id="20255-291">Because the same selector Markdown goes in each article file that uses the selector, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="20255-292">Затем нужно добавить ссылки на этот файл во все статьи, для которых используется селектор.</span><span class="sxs-lookup"><span data-stu-id="20255-292">Then you can reference that include file in all your article files that use the same selector.</span></span>

<span data-ttu-id="20255-293">Сейчас существует два типа селекторов: для единичного и множественного выбора.</span><span class="sxs-lookup"><span data-stu-id="20255-293">There are two types of selectors: a single selector and a multi-selector.</span></span>

### <a name="single-selector"></a><span data-ttu-id="20255-294">Единичный выбор</span><span class="sxs-lookup"><span data-stu-id="20255-294">Single selector</span></span>

```markdown
> [!div class="op_single_selector"]
> - [Universal Windows](../articles/notification-hubs-windows-store-dotnet-get-started/)
> - [Windows Phone](../articles/notification-hubs-windows-phone-get-started/)
> - [iOS](../articles/notification-hubs-ios-get-started/)
> - [Android](../articles/notification-hubs-android-get-started/)
> - [Kindle](../articles/notification-hubs-kindle-get-started/)
> - [Baidu](../articles/notification-hubs-baidu-get-started/)
> - [Xamarin.iOS](../articles/partner-xamarin-notification-hubs-ios-get-started/)
> - [Xamarin.Android](../articles/partner-xamarin-notification-hubs-android-get-started/)
```

<span data-ttu-id="20255-295">... будет иметь следующий вид:</span><span class="sxs-lookup"><span data-stu-id="20255-295">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Универсальные приложения Windows](how-to-write-links.md)
> - [Windows Phone](how-to-write-links.md)
> - [iOS](how-to-write-links.md)
> - [Android](how-to-write-links.md)
> - [Kindle](how-to-write-links.md)
> - [Baidu](how-to-write-links.md)
> - [Xamarin.iOS](how-to-write-links.md)
> - [Xamarin.Android](how-to-write-links.md)

### <a name="multi-selector"></a><span data-ttu-id="20255-304">Множественный выбор</span><span class="sxs-lookup"><span data-stu-id="20255-304">Multi-selector</span></span>

```markdown
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](./mobile-services-dotnet-backend-ios-get-started-push.md)
> - [(iOS | JavaScript)](./mobile-services-javascript-backend-ios-get-started-push.md)
> - [(Windows universal C# | .NET)](./mobile-services-dotnet-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows universal C# | Javascript)](./mobile-services-javascript-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows Phone | .NET)](./mobile-services-dotnet-backend-windows-phone-get-started-push.md)
> - [(Windows Phone | Javascript)](./mobile-services-javascript-backend-windows-phone-get-started-push.md)
> - [(Android | .NET)](./mobile-services-dotnet-backend-android-get-started-push.md)
> - [(Android | Javascript)](./mobile-services-javascript-backend-android-get-started-push.md)
> - [(Xamarin iOS | Javascript)](./partner-xamarin-mobile-services-ios-get-started-push.md)
> - [(Xamarin Android | Javascript)](./partner-xamarin-mobile-services-android-get-started-push.md)
```

<span data-ttu-id="20255-305">... будет иметь следующий вид:</span><span class="sxs-lookup"><span data-stu-id="20255-305">... will be rendered like this:</span></span>

> [!div class="op_multi_selector" title1="Платформа" title2="Серверная часть"]
> - [(iOS | .NET)](how-to-write-links.md)
> - [(iOS | JavaScript)](how-to-write-links.md)
> - [(Универсальные приложения Windows на C# | .NET)](how-to-write-links.md)
> - [(Универсальные приложения Windows на C# | Javascript)](how-to-write-links.md)
> - [(Windows Phone | .NET)](how-to-write-links.md)
> - [(Windows Phone | Javascript)](how-to-write-links.md)
> - [(Android | .NET)](how-to-write-links.md)
> - [(Android | Javascript)](how-to-write-links.md)
> - [(Xamarin iOS | Javascript)](how-to-write-links.md)
> - [(Xamarin Android | Javascript)](how-to-write-links.md)

## <a name="subscript-and-superscript"></a><span data-ttu-id="20255-318">Подстрочные и надстрочные символы</span><span class="sxs-lookup"><span data-stu-id="20255-318">Subscript and superscript</span></span>

<span data-ttu-id="20255-319">Подстрочные и надстрочные символы следует использовать только при необходимости для технической точности, например при написании математических формул.</span><span class="sxs-lookup"><span data-stu-id="20255-319">You should only use subscript or superscript when necessary for technical accuracy, such as when writing about mathematical formulas.</span></span> <span data-ttu-id="20255-320">Не используйте их для нестандартных стилей, например сносок.</span><span class="sxs-lookup"><span data-stu-id="20255-320">Don't use them for non-standard styles, such as footnotes.</span></span>

<span data-ttu-id="20255-321">Для подстрочных и надстрочных символов используйте HTML:</span><span class="sxs-lookup"><span data-stu-id="20255-321">For both subscript and superscript, use HTML:</span></span>

```html
Hello <sub>This is subscript!</sub>
```

<span data-ttu-id="20255-322">Это отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="20255-322">This renders as follows:</span></span>

<span data-ttu-id="20255-323">Здравствуйте, <sub>это подстрочный текст!</sub></span><span class="sxs-lookup"><span data-stu-id="20255-323">Hello <sub>This is subscript!</sub></span></span>

```html
Goodbye <sup>This is superscript!</sup>
```

<span data-ttu-id="20255-324">Это отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="20255-324">This renders as follows:</span></span>

<span data-ttu-id="20255-325">До свидания, <sup>это надстрочный текст!</sup></span><span class="sxs-lookup"><span data-stu-id="20255-325">Goodbye <sup>This is superscript!</sup></span></span>

## <a name="tables"></a><span data-ttu-id="20255-326">Tables</span><span class="sxs-lookup"><span data-stu-id="20255-326">Tables</span></span>

<span data-ttu-id="20255-327">Использование вертикальных линий и строк является самым простым способом создания таблиц в Markdown.</span><span class="sxs-lookup"><span data-stu-id="20255-327">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="20255-328">Чтобы создать стандартную таблицу с заголовком, вставьте пунктирную линию после первой строки.</span><span class="sxs-lookup"><span data-stu-id="20255-328">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="20255-329">Это отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="20255-329">This renders as follows:</span></span>

|<span data-ttu-id="20255-330">Это</span><span class="sxs-lookup"><span data-stu-id="20255-330">This is</span></span>   |<span data-ttu-id="20255-331">просто</span><span class="sxs-lookup"><span data-stu-id="20255-331">a simple</span></span>   |<span data-ttu-id="20255-332">заголовок таблицы</span><span class="sxs-lookup"><span data-stu-id="20255-332">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="20255-333">данные</span><span class="sxs-lookup"><span data-stu-id="20255-333">table</span></span>     |<span data-ttu-id="20255-334">таблицы</span><span class="sxs-lookup"><span data-stu-id="20255-334">data</span></span>       |<span data-ttu-id="20255-335">здесь</span><span class="sxs-lookup"><span data-stu-id="20255-335">here</span></span>        |
|<span data-ttu-id="20255-336">вообще-то</span><span class="sxs-lookup"><span data-stu-id="20255-336">it doesn't</span></span>|<span data-ttu-id="20255-337">не всегда</span><span class="sxs-lookup"><span data-stu-id="20255-337">actually</span></span>   |<span data-ttu-id="20255-338">отображаются аккуратно!</span><span class="sxs-lookup"><span data-stu-id="20255-338">have to line up nicely!</span></span>||

<span data-ttu-id="20255-339">Можно выровнять столбцы с помощью двоеточий:</span><span class="sxs-lookup"><span data-stu-id="20255-339">You can align the columns by using colons:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="20255-340">Отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="20255-340">Renders as follows:</span></span>

| <span data-ttu-id="20255-341">Fun</span><span class="sxs-lookup"><span data-stu-id="20255-341">Fun</span></span>                  | <span data-ttu-id="20255-342">with</span><span class="sxs-lookup"><span data-stu-id="20255-342">With</span></span>                 | <span data-ttu-id="20255-343">Tables</span><span class="sxs-lookup"><span data-stu-id="20255-343">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="20255-344">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="20255-344">left-aligned column</span></span>  | <span data-ttu-id="20255-345">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="20255-345">right-aligned column</span></span> | <span data-ttu-id="20255-346">centered column</span><span class="sxs-lookup"><span data-stu-id="20255-346">centered column</span></span> |
| <span data-ttu-id="20255-347">$100</span><span class="sxs-lookup"><span data-stu-id="20255-347">$100</span></span>                 | <span data-ttu-id="20255-348">$100</span><span class="sxs-lookup"><span data-stu-id="20255-348">$100</span></span>                 | <span data-ttu-id="20255-349">$100</span><span class="sxs-lookup"><span data-stu-id="20255-349">$100</span></span>            |
| <span data-ttu-id="20255-350">$10</span><span class="sxs-lookup"><span data-stu-id="20255-350">$10</span></span>                  | <span data-ttu-id="20255-351">$10</span><span class="sxs-lookup"><span data-stu-id="20255-351">$10</span></span>                  | <span data-ttu-id="20255-352">$10</span><span class="sxs-lookup"><span data-stu-id="20255-352">$10</span></span>             |
| <span data-ttu-id="20255-353">$1</span><span class="sxs-lookup"><span data-stu-id="20255-353">$1</span></span>                   | <span data-ttu-id="20255-354">$1</span><span class="sxs-lookup"><span data-stu-id="20255-354">$1</span></span>                   | <span data-ttu-id="20255-355">$1</span><span class="sxs-lookup"><span data-stu-id="20255-355">$1</span></span>              |

> [!TIP]
> <span data-ttu-id="20255-356">Расширение создания документации для VS Code упрощает добавление базовых таблиц Markdown.</span><span class="sxs-lookup"><span data-stu-id="20255-356">The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!</span></span>
>
> <span data-ttu-id="20255-357">Кроме того, можно использовать [веб-инструмент создания таблиц](http://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="20255-357">You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).</span></span>

### <a name="line-breaks-within-words-in-any-table-cell"></a><span data-ttu-id="20255-358">Разрывы строк внутри слов в любой ячейке таблицы</span><span class="sxs-lookup"><span data-stu-id="20255-358">Line breaks within words in any table cell</span></span>

<span data-ttu-id="20255-359">Длинные слова в таблице Markdown могут привести к тому, что таблица сдвинется вправо и станет нечитаемой.</span><span class="sxs-lookup"><span data-stu-id="20255-359">Long words in a Markdown table might make the table expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="20255-360">Эту проблему можно решить, разрешив отрисовке на сайте документации автоматически вставлять разрывы строк внутри слов при необходимости.</span><span class="sxs-lookup"><span data-stu-id="20255-360">You can solve that by allowing Docs rendering to automatically insert line breaks within words when needed.</span></span> <span data-ttu-id="20255-361">Нужно просто заключить таблицу в настраиваемый класс `[!div class="mx-tdBreakAll"]`.</span><span class="sxs-lookup"><span data-stu-id="20255-361">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="20255-362">Далее приведен пример Markdown таблицы с тремя строками, которая будет заключена с помощью `div` с классом `mx-tdBreakAll`.</span><span class="sxs-lookup"><span data-stu-id="20255-362">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="20255-363">Она будет иметь следующий вид:</span><span class="sxs-lookup"><span data-stu-id="20255-363">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="20255-364">Имя</span><span class="sxs-lookup"><span data-stu-id="20255-364">Name</span></span>|<span data-ttu-id="20255-365">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20255-365">Syntax</span></span>|<span data-ttu-id="20255-366">Обязательно для автоматический установки?</span><span class="sxs-lookup"><span data-stu-id="20255-366">Mandatory for silent installation?</span></span>|<span data-ttu-id="20255-367">Описание</span><span class="sxs-lookup"><span data-stu-id="20255-367">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="20255-368">Quiet</span><span class="sxs-lookup"><span data-stu-id="20255-368">Quiet</span></span>|<span data-ttu-id="20255-369">/quiet</span><span class="sxs-lookup"><span data-stu-id="20255-369">/quiet</span></span>|<span data-ttu-id="20255-370">Да</span><span class="sxs-lookup"><span data-stu-id="20255-370">Yes</span></span>|<span data-ttu-id="20255-371">Запускает установщик без отображения пользовательского интерфейса и запросов.</span><span class="sxs-lookup"><span data-stu-id="20255-371">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="20255-372">NoRestart</span><span class="sxs-lookup"><span data-stu-id="20255-372">NoRestart</span></span>|<span data-ttu-id="20255-373">/norestart</span><span class="sxs-lookup"><span data-stu-id="20255-373">/norestart</span></span>|<span data-ttu-id="20255-374">Нет</span><span class="sxs-lookup"><span data-stu-id="20255-374">No</span></span>|<span data-ttu-id="20255-375">Подавляет попытки перезапуска.</span><span class="sxs-lookup"><span data-stu-id="20255-375">Suppresses any attempts to restart.</span></span> <span data-ttu-id="20255-376">По умолчанию пользовательский интерфейс выведет запрос перед перезапуском.</span><span class="sxs-lookup"><span data-stu-id="20255-376">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="20255-377">Help</span><span class="sxs-lookup"><span data-stu-id="20255-377">Help</span></span>|<span data-ttu-id="20255-378">/help</span><span class="sxs-lookup"><span data-stu-id="20255-378">/help</span></span>|<span data-ttu-id="20255-379">Нет</span><span class="sxs-lookup"><span data-stu-id="20255-379">No</span></span>|<span data-ttu-id="20255-380">Предоставляет справку и краткие инструкции.</span><span class="sxs-lookup"><span data-stu-id="20255-380">Provides help and quick reference.</span></span> <span data-ttu-id="20255-381">Отображает правильное использование команды setup, включая список всех параметров и вариантов поведения.</span><span class="sxs-lookup"><span data-stu-id="20255-381">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="line-breaks-within-words-in-second-column-table-cells"></a><span data-ttu-id="20255-382">Разрывы строк внутри слов в ячейках второго столбца</span><span class="sxs-lookup"><span data-stu-id="20255-382">Line breaks within words in second column table cells</span></span>

<span data-ttu-id="20255-383">Разрывы строк могут вставляться автоматически внутри слов только во втором столбце таблицы.</span><span class="sxs-lookup"><span data-stu-id="20255-383">You might want line breaks to be automatically inserted within words only in the second column of a table.</span></span> <span data-ttu-id="20255-384">Чтобы разрешить разрывы только во втором столбце, примените класс `mx-tdCol2BreakAll` с помощью синтаксиса переноса `div`, как показано выше.</span><span class="sxs-lookup"><span data-stu-id="20255-384">To limit the breaks to the second column, apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="data-matrix-tables"></a><span data-ttu-id="20255-385">Таблицы матриц данных</span><span class="sxs-lookup"><span data-stu-id="20255-385">Data matrix tables</span></span>

<span data-ttu-id="20255-386">Таблица матрицы данных содержит заголовок и взвешенный первый столбец. Она позволяет создать матрицу с пустой ячейкой в верхнем углу слева.</span><span class="sxs-lookup"><span data-stu-id="20255-386">A data matrix table has both a header and a weighted first column, creating a matrix with an empty cell in the top left.</span></span> <span data-ttu-id="20255-387">Пользовательскую разметку Markdown для таблиц матриц данных можно найти на сайте документации:</span><span class="sxs-lookup"><span data-stu-id="20255-387">Docs has custom Markdown for data matrix tables:</span></span>

```md
|                  |Header 1 |Header 2|
|------------------|---------|--------|
|**First column A**|Cell 1A  |Cell 2A |
|**First column B**|Cell 1B  |Cell 2B |
```

<span data-ttu-id="20255-388">Для каждой запись в первом столбце нужно задать полужирное начертание (`**bold**`). Иначе таблицы будут недоступны для средств чтения с экрана или недопустимы для сайта документации.</span><span class="sxs-lookup"><span data-stu-id="20255-388">Every entry in the first column must be styled as bold (`**bold**`); otherwise the tables won't be accessible for screen readers or valid for Docs.</span></span>

### <a name="html-tables"></a><span data-ttu-id="20255-389">Таблицы HTML</span><span class="sxs-lookup"><span data-stu-id="20255-389">HTML Tables</span></span>

<span data-ttu-id="20255-390">Таблицы HTML не рекомендуется использовать для docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="20255-390">HTML tables aren't recommended for docs.microsoft.com.</span></span> <span data-ttu-id="20255-391">Они трудны для восприятия в исходном виде — это нарушает основной принцип Markdown.</span><span class="sxs-lookup"><span data-stu-id="20255-391">They aren't human readable in the source - which is a key principle of Markdown.</span></span>
