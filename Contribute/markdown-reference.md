---
title: Справочник по разметке Markdown для docs.microsoft.com
description: Ознакомьтесь с функциями и синтаксисом Markdown, используемыми на платформе Документации Майкрософт.
author: meganbradley
ms.author: mbradley
ms.date: 01/30/2020
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: 14cc9f0912149eb342c97d0dd7d2776bd54c84e7
ms.sourcegitcommit: 804a99b89785e5c8f056a9da3f0fbde9f0a56a51
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "78331977"
---
# <a name="docs-markdown-reference"></a>Справочник по Docs Markdown

Эта статья содержит алфавитный справочник по работе с Markdown для docs.microsoft.com (Документация).

[Markdown](https://daringfireball.net/projects/markdown/) — это облегченный язык разметки с синтаксисом форматирования обычного текста. Документация поддерживает разметку Markdown в соответствии с [CommonMark](https://commonmark.org/) и ее синтаксический анализ через подсистему [Markdig](https://github.com/lunet-io/markdig). Документация также поддерживает пользовательские расширения Markdown, которые предоставляют более обширный контент на сайте документации.

Для записи Markdown можно использовать любой текстовый редактор, но мы рекомендуем [Visual Studio Code](https://code.visualstudio.com/) с расширением [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack). Расширение Docs Authoring Pack содержит средства редактирования и функции предварительного просмотра, позволяющие увидеть, как будут выглядеть статьи на сайте Документации.

## <a name="alerts-note-tip-important-caution-warning"></a>Оповещения ("Примечание", "Совет", "Важно!", "Внимание!", "Предупреждение")

Оповещения — это специальные расширения Markdown, которые используются для создания блоков цитирования, отображаемых на сайте docs.microsoft.com с помощью цветов и значков, указывающих на важность содержимого. Поддерживаются следующие типы оповещений:

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

На сайте docs.microsoft.com эти оповещения отображаются следующим образом:

> [!NOTE]
> Информация, которую пользователь должен заметить даже при беглом просмотре.

> [!TIP]
> Дополнительные сведения, помогающие пользователю лучше решить задачу.

> [!IMPORTANT]
> Важные сведения для успешного решения задачи.

> [!CAUTION]
> Потенциальные негативные последствия действия.

> [!WARNING]
> Опасные последствия действия.

### <a name="angle-brackets"></a>Угловые скобки

Если в тексте файла используются угловые скобки (например, для обозначения заполнителя), их нужно кодировать вручную. В противном случае разметка Markdown считает их HTML-тегами.

Например, `<script name>` следует закодировать как `&lt;script name&gt;` или `\<script name>`.

Угловые скобки не обязательно должны быть экранированы в тексте, отформатированном как встроенный код, или в блоках кода.

## <a name="apostrophes-and-quotation-marks"></a>Апострофы и кавычки

Если вы копируете текст из Word в редактор Markdown, он может содержать книжные (изогнутые) апострофы или кавычки. Их нужно заменить кодом или обычными апострофами или кавычками. В противном случае после публикации файла может отобразиться нечитаемый текст, например: Itâ€™s

Ниже приведены кодировки для этих знаков пунктуации:

- левая (открывающая) кавычка: `&#8220;`;
- правая (закрывающая) кавычка: `&#8221;`;
- правая закрывающая одинарная кавычка или апостроф: `&#8217;`;
- левая открывающая одинарная кавычка (используется редко): `&#8216;`.

## <a name="blockquotes"></a>Блоки цитирования

Блоки цитирования создаются с помощью символа `>`:

```md
> This is a blockquote. It is usually rendered indented and with a different background color.
```

Предыдущий пример отображается следующим образом:

> Это блок цитирования. Обычно он отображается с отступом и имеет другой цвет фона.

## <a name="bold-and-italic-text"></a>Полужирное и курсивное начертания

Чтобы задать для текста **полужирное начертание**, заключите его в двойные звездочки:

```markdown
This text is **bold**.
```

Чтобы задать для текста *курсивное начертание*, заключите его в одинарные звездочки:

```markdown
This text is *italic*.
```

Чтобы задать для текста ***полужирное и курсивное*** начертание, заключите его в тройные звездочки:

```markdown
This text is both ***bold and italic***.
```

## <a name="code-snippets"></a>Фрагменты кода

Расширение Docs Markdown поддерживает как встраивание фрагментов кода в предложение, так и их размещение между предложениями в виде отдельных огражденных блоков. Дополнительные сведения см. в разделе [Как добавить код в документацию](code-in-docs.md).

## <a name="columns"></a>Столбцы

Расширение Markdown **столбцы** дает авторам документации возможность добавлять макеты содержимого на основе столбцов, которые являются более гибкими и эффективными, чем базовые таблицы Markdown, подходящие только для действительно табличных данных. Можно добавить до четырех столбцов и использовать необязательный атрибут `span` для объединения двух или более столбцов.

Используйте следующий синтаксис для столбцов:

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

Столбцы должны содержать только базовый Markdown, включая изображения. Заголовки, таблицы, вкладки и другие сложные структуры не должны включаться. Строка не может иметь содержимое вне столбца.

Например, следующий Markdown создает один столбец, охватывающий две ширины столбца, и один стандартный столбец (без `span`):

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

Это отображается следующим образом:

:::row:::
   :::column span="2":::
      **Это столбец двойной ширины с большим объемом текста.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **Это столбец одинарной ширины с изображением.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::

## <a name="headings"></a>Заголовки

Платформа Docs поддерживает шесть уровней заголовков Markdown:

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- Между последним символом `#` и содержимым заголовка должен присутствовать пробел.
- В одном файле Markdown должен быть один и только один заголовок H1.
- Заголовок H1 указывается в файле в первую очередь, сразу после блока метаданных YML.
- Заголовки H2 автоматически отображаются в правом меню навигации опубликованного файла. Заголовки более низкого уровня не отображаются, поэтому для удобства перехода по содержимому рекомендуется использовать заголовки H2.
- Использовать заголовки HTML, такие как `<h1>`, не рекомендуется, и в некоторых случаях из-за них могут возникать предупреждения при сборке.
- Привязка к отдельным заголовкам в файле выполняется с помощью [ссылок на закладки](how-to-write-links.md#links-to-anchors).

## <a name="html"></a>HTML

Хотя Markdown поддерживает встроенный HTML-код, HTML не рекомендуется использовать для публикации на сайте Документации. Любой код, за исключением ограниченного списка значений, будет вызывать появление ошибок и предупреждений при сборке. 

## <a name="images"></a>Изображения

Для изображений по умолчанию поддерживаются следующие типы файлов:

- JPG,
- PNG.

### <a name="standard-conceptual-images-default-markdown"></a>Стандартные схематические изображения (Markdown по умолчанию)

Базовый синтаксис Markdown для внедрения изображения:

```Markdown
![<alt text>](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

Где `<alt text>` — краткое описание изображения, а `<folder path>` — относительный путь к нему. Заменяющий текст необходим для средств чтения с экрана для слабовидящих. Он также удобен при возникновении ошибок на сайте, из-за которых не удается воспроизвести изображение.

Знаки подчеркивания в замещающем тексте не отображаются должным образом, если они не экранированы с помощью префикса — обратной косой черты (`\_`). Но не стоит копировать имена файлов для использования в качестве замещающего текста. Например, вместо:

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

Напишите:

```markdown
![Active Directory extension for two-factor authentication, step 4: Configure](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="standard-conceptual-images-docs-markdown"></a>Стандартные схематические изображения (Docs Markdown)

Пользовательское расширение "Документация" `:::image:::` поддерживает стандартные изображения, сложные изображения и значки.

Для стандартных изображений старый синтаксис Markdown по-прежнему будет работать, но рекомендуется использовать новое расширение, так как оно поддерживает более широкие функциональные возможности, такие как указание области локализации, отличной от родительской темы. В будущем будут доступны другие расширенные функции, такие как выбор из общей коллекции изображений вместо указания локального изображения. Используйте следующий новый синтаксис:

```Markdown
:::image type="content" source="<folderPath>" alt-text="<alt text>":::
```

Если `type="content"` (по умолчанию), требуются `source` и `alt-text`.

### <a name="complex-images-with-long-descriptions"></a>Сложные изображения с длинными описаниями

Это расширение также можно использовать для добавления изображения с длинным описанием, которое считывается программами чтения с экрана, но не отображается визуально на опубликованной странице. Длинные описания являются требованием для специальных возможностей для сложных изображений, таких как диаграммы. Используется следующий синтаксис:

```Markdown
:::image type="complex" source="<folderPath>" alt-text="<alt text>":::
   <long description here>
:::image-end:::
```

Если `type="complex"`, `source`, `alt-text`, требуется длинное описание и тег `:::image-end:::`.

### <a name="specifying-loc-scope"></a>Указание области локализации

Иногда область локализации для изображения отличается от области локализации для статьи или модуля, в которых оно содержится. Это может привести к неправильному глобальному интерфейсу: например, если снимок экрана продукта случайно локализован на язык, на котором продукт недоступен. Чтобы избежать этого, можно указать необязательный атрибут `loc-scope` в изображениях типов `content` и `complex`.

### <a name="icons"></a>Значки

Расширение изображения поддерживает значки, которые являются декоративными изображениями и не должны иметь замещающий текст. Для значков используется следующий синтаксис:

```Markdown
:::image type="icon" source="<folderPath>":::
```

Если `type="icon"`, нужно указать только `source`.

## <a name="included-markdown-files"></a>Включаемые файлы Markdown

Если файлы Markdown необходимо повторить в нескольких статьях, можно использовать включаемый файл. Функция включения указывает сайту Документации заменить ссылку на содержимое включаемого файла во время сборки. Для включения можно использовать следующие способы.

- Встроенные: используются для многократного использования фрагмента стандартного текста путем его встраивания в предложение.
- Блочные: Используются для многократного использования всего файла Markdown в качестве блока путем его вложения в раздел или статью.

Встроенные и блочные включаемые файлы — это файлы Markdown с расширением MD. Они могут содержать любую допустимую разметку Markdown. Включаемые файлы обычно находятся в общем подкаталоге *includes* в корне репозитория. Когда статья публикуется, включаемый файл легко интегрируется в нее.

### <a name="includes-syntax"></a>Синтаксис включаемых файлов

Блочные включаемые файлы находятся в отдельной строке:

```markdown
[!INCLUDE [<title>](<filepath>)]
```

Встроенные включаемые файлы находятся в строке:

```markdown
Text before [!INCLUDE [<title>](<filepath>)] and after.
```

Где `<title>` — имя файла, а `<filepath>` — относительный путь к файлу. Слово `INCLUDE` должно быть написано прописными буквами, а перед `<title>` должен быть пробел.

Ниже приведены требования к включаемым файлам и соображения по работе с ними:

- Блочные включаемые файлы предназначены для значительных объемов текста: один или два абзаца, общая процедура или общий раздел. Не используйте их для фрагментов текста меньше одного предложения.
- Включаемые файлы не отображаются в представлении статьи на сайте GitHub. Они используют расширения "Документация". Они отображаются только после публикации.
- Весь текст во включаемом файле должен состоять из полноценных предложений или фраз, не зависящих от остального текста статьи, в которую добавляется ссылка на такой файл. Если не следовать этой инструкции, в статье создаются непереводимые строки.
- Не внедряйте одни включаемые файлы в другие.
- Файлы мультимедиа должны быть помещены в отдельную папку мультимедиа в подкаталоге включаемых файлов. Например, `<repo>` */includes/media*. В корне каталога *media* не должны содержаться изображения. Если во включаемом файле нет изображений, соответствующий каталог *media* не требуется.
- Как и в обычных статьях, не используйте общий файл мультимедиа для включаемых файлов. Для каждого включаемого файла в статье должен быть создан отдельный файл мультимедиа с уникальным именем. Файл мультимедиа должен храниться в папке мультимедиа, связанной с включаемым файлом.
- Не используйте включаемый файл как единственное содержимое статьи.  Включаемые файлы предназначены для дополнения основных материалов статьи.

## <a name="links"></a>Создание ссылок

Сведения о синтаксисе ссылок см. в разделе [Использование ссылок в документации](how-to-write-links.md).

## <a name="lists-numbered-bulleted-checklist"></a>Списки (нумерованные, маркированные, контрольные)

### <a name="numbered-list"></a>Нумерованный список

Чтобы создать нумерованный список, можно использовать все единицы. При публикации числа отображаются в возрастающем порядке в виде последовательного списка. Для повышения удобства чтения исходного кода списки можно вводить с приращением вручную.

Не используйте в списках, включая вложенные списки, буквы. При публикации на сайте документации они отображаются некорректно. Вложенные списки с цифрами преобразуются в списки со строчными буквами при публикации. Например:

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

Это отображается следующим образом:

1. Это
1. родительский нумерованный список,
   1. а это
   1. вложенный нумерованный список
1. (конец)

### <a name="bulleted-list"></a>Маркированный список

Для создания маркированного списка используйте `-` или `*`, за которым следует пробел в начале каждой строки:

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

Это отображается следующим образом:

- Это
- родительский маркированный список,
  - а это
  - вложенный маркированный список
- Готово!

Независимо от используемого синтаксиса, `-` или `*`, используйте его согласованно в статье.

### <a name="checklist"></a>Контрольный список

Контрольные списки можно использовать на сайте документации с помощью пользовательского расширения Markdown:

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

Этот пример отображается на сайте документации следующим образом:

> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3

Контрольные списки используются в начале или конце статьи для подведения итогов "Чему вы научитесь" или "Чему вы научились". Не вставляйте контрольные списки в статьи по случайному принципу.

## <a name="next-step-action"></a>Действие "Дальнейшие действия"

Пользовательское расширение можно использовать для добавления кнопки "Дальнейшие действия" на страницы сайта Документации.

Используйте следующий синтаксис:

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

Например:

```markdown
> [!div class="nextstepaction"]
> [Learn about adding code to articles](code-in-docs.md)
```

Это отображается следующим образом:

> [!div class="nextstepaction"]
> [Дополнительные сведения о добавлении кода в статьи](code-in-docs.md)

Вы можете использовать любые поддерживаемые ссылки в действии "Дальнейшие действия", включая ссылку Markdown на другую веб-страницу. Как правило, ссылка "Дальнейшие действия" — это относительная ссылка на другой файл в том же наборе документации.

## <a name="non-localized-strings"></a>Нелокализованные строки

Вы можете использовать пользовательское расширение Markdown `no-loc`, чтобы указать строки содержимого, не подлежащие локализации.

Для всех указанных строк учитывается регистр; то есть строка должна полностью соответствовать указанному значению, чтобы игнорироваться при локализации.

Чтобы пометить отдельную строку как не подлежащую локализации, используйте следующий синтаксис:

```markdown
:::no-loc text="String":::
```

Например, в следующем примере только один экземпляр `Document` будет игнорироваться в процессе локализации:

```markdown
# Heading 1 of the Document

Markdown content within the :::no-loc text="Document":::.  The are multiple instances of Document, document, and documents.
```

> [!NOTE]
> Используйте `\`, чтобы экранировать специальные символы:
> ```markdown
> Lorem :::no-loc text="Find a \"Quotation\""::: Ipsum.
> ```

Можно также использовать метаданные в заголовке YAML, чтобы пометить все экземпляры строки в текущем файле Markdown как нелокализуемые:

```yml
author: cillroy
no-loc: [Global, Strings, to be, Ignored]
```

> [!NOTE]
> Метаданные no-loc не поддерживаются в качестве глобальных метаданных в файле *docfx.json*. Конвейер локализации не считывает файл *docfx.json*, поэтому метаданные no-loc должны быть добавлены в каждый отдельный исходный файл.

В следующем примере и в метаданных `title`, и в заголовке Markdown слово `Document` будет игнорироваться в процессе локализации.

В метаданных `description` и основном содержимом Markdown слово `document` локализовано, так как оно не начинается с прописной буквы `D`.

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

## <a name="selectors"></a>Селекторы

Селекторы — это элементы пользовательского интерфейса, позволяющие пользователю переключаться между несколькими разновидностями одной и той же статьи. Они используются в некоторых наборах документов для реализаций разных технологий или платформ. Селекторы обычно применяются к материалам о мобильных платформах для разработчиков.

В каждой статье с возможностью выбора используется одна и та же разметка Markdown для селектора. Поэтому рекомендуется поместить селектор для статьи во включаемый файл. Затем нужно добавить ссылки на этот файл во все статьи, для которых используется селектор.

Сейчас существует два типа селекторов: для единичного и множественного выбора.

### <a name="single-selector"></a>Единичный выбор

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

... будет иметь следующий вид:

> [!div class="op_single_selector"]
> - [Универсальные приложения Windows](how-to-write-links.md)
> - [Windows Phone](how-to-write-links.md)
> - [iOS](how-to-write-links.md)
> - [Android](how-to-write-links.md)
> - [Kindle](how-to-write-links.md)
> - [Baidu](how-to-write-links.md)
> - [Xamarin.iOS](how-to-write-links.md)
> - [Xamarin.Android](how-to-write-links.md)

### <a name="multi-selector"></a>Множественный выбор

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

... будет иметь следующий вид:

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

## <a name="subscript-and-superscript"></a>Подстрочные и надстрочные символы

Подстрочные и надстрочные символы следует использовать только при необходимости для технической точности, например при написании математических формул. Не используйте их для нестандартных стилей, например сносок.

Для подстрочных и надстрочных символов используйте HTML:

```html
Hello <sub>This is subscript!</sub>
```

Это отображается следующим образом:

Здравствуйте, <sub>это подстрочный текст!</sub>

```html
Goodbye <sup>This is superscript!</sup>
```

Это отображается следующим образом:

До свидания, <sup>это надстрочный текст!</sup>

## <a name="tables"></a>Tables

Использование вертикальных линий и строк является самым простым способом создания таблиц в Markdown. Чтобы создать стандартную таблицу с заголовком, вставьте пунктирную линию после первой строки.

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

Это отображается следующим образом:

|Это   |просто   |заголовок таблицы|
|----------|-----------|------------|
|данные     |таблицы       |здесь        |
|вообще-то|не всегда   |отображаются аккуратно!||

Можно выровнять столбцы с помощью двоеточий:

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

Отображается следующим образом:

| Fun                  | with                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |

> [!TIP]
> Расширение создания документации для VS Code упрощает добавление базовых таблиц Markdown.
>
> Кроме того, можно использовать [веб-инструмент создания таблиц](http://www.tablesgenerator.com/markdown_tables).

### <a name="line-breaks-within-words-in-any-table-cell"></a>Разрывы строк внутри слов в любой ячейке таблицы

Длинные слова в таблице Markdown могут привести к тому, что таблица сдвинется вправо и станет нечитаемой. Эту проблему можно решить, разрешив отрисовке на сайте документации автоматически вставлять разрывы строк внутри слов при необходимости. Нужно просто заключить таблицу в настраиваемый класс `[!div class="mx-tdBreakAll"]`.

Далее приведен пример Markdown таблицы с тремя строками, которая будет заключена с помощью `div` с классом `mx-tdBreakAll`.

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

Она будет иметь следующий вид:

> [!div class="mx-tdBreakAll"]
> |Имя|Синтаксис|Обязательно для автоматический установки?|Описание|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Да|Запускает установщик без отображения пользовательского интерфейса и запросов.|
> |NoRestart|/norestart|Нет|Подавляет попытки перезапуска. По умолчанию пользовательский интерфейс выведет запрос перед перезапуском.|
> |Help|/help|Нет|Предоставляет справку и краткие инструкции. Отображает правильное использование команды setup, включая список всех параметров и вариантов поведения.|

### <a name="line-breaks-within-words-in-second-column-table-cells"></a>Разрывы строк внутри слов в ячейках второго столбца

Разрывы строк могут вставляться автоматически внутри слов только во втором столбце таблицы. Чтобы разрешить разрывы только во втором столбце, примените класс `mx-tdCol2BreakAll` с помощью синтаксиса переноса `div`, как показано выше.

### <a name="html-tables"></a>Таблицы HTML

Таблицы HTML не рекомендуется использовать для docs.microsoft.com. Они трудны для восприятия в исходном виде — это нарушает основной принцип Markdown.
