---
title: Справочник по разметке Markdown для docs.microsoft.com
description: Ознакомьтесь с функциями и синтаксисом Markdown, используемыми на платформе Документации Майкрософт.
author: meganbradley
ms.author: mbradley
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: a5ff6c5122a08d2b611fd6b0344a6f5740d93928
ms.sourcegitcommit: 254c804bb0b451c262745fe8d87e2e8f9196440c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2019
ms.locfileid: "73592569"
---
# <a name="markdown-reference"></a>Справочник по разметке Markdown

Markdown — это облегченный язык разметки с синтаксисом форматирования обычного текста. Платформа Docs поддерживает стандарт CommonMark для Markdown, а также несколько пользовательских расширений Markdown, предоставляющих дополнительное содержимое для docs.microsoft.com. Эта статья содержит алфавитный справочник по работе с Markdown для docs.microsoft.com.

Для работы с разметкой Markdown можно использовать любой текстовый редактор. В качестве редактора, упрощающего вставку стандартного синтаксиса Markdown и пользовательских расширений Docs, рекомендуем использовать [VS Code](https://code.visualstudio.com/) с установленным [пакетом создания документации](https://aka.ms/DocsAuthoringPack).

Платформа Docs использует модуль Markdig для разметки Markdown. Сравнить отрисовку разметки Markdown в Markdig с другими обработчиками можно по адресу [https://babelmark.github.io/](https://babelmark.github.io/).

## <a name="alerts-note-tip-important-caution-warning"></a>Оповещения ("Примечание", "Совет", "Важно!", "Внимание!", "Предупреждение")

Оповещения — это специальные расширения Markdown для платформы Docs, которые используются для создания блоков цитирования, отображаемых на сайте docs.microsoft.com с помощью цветов и значков, указывающих на важность содержимого. Поддерживаются следующие типы оповещений:

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

На сайте docs.microsoft.com эти оповещения отображаются следующим образом:

![Вид оповещений из предыдущего примера с разными значками и цветами на опубликованной странице портала документации.](media/alerts-rendering.png)

## <a name="code-snippets"></a>Фрагменты кода

Вы можете вставить фрагменты кода в свои файлы Markdown:

```md
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a>Заголовки

Платформа Docs поддерживает шесть уровней заголовков Markdown:

```md
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- Между последним символом `#` и содержимым заголовка должен присутствовать пробел.
- В одном файле Markdown должен быть один и только один заголовок H1.
- Заголовок H1 указывается в файле в первую очередь, сразу после блока метаданных YML.
- Заголовки H2 автоматически отображаются в правом меню навигации опубликованного файла. Это правило не применяется к заголовкам следующих уровней, поэтому для удобства перехода по содержимому рекомендуется использовать заголовки H2.
- Использовать заголовки HMTL, такие как `<h1>`, не рекомендуется, и в некоторых случаях из-за них могут возникать предупреждения при сборке.
- Привязка к отдельным заголовкам в файле выполняется с помощью [закладок](#bookmark-links).

## <a name="html"></a>HTML

Хотя Markdown поддерживает встроенный HTML-код, HTML не рекомендуется использовать для публикации на платформе Docs. Любой код, за исключением ограниченного списка значений, будет вызывать появление ошибок и предупреждений при сборке.

## <a name="images"></a>Изображения

Для включения изображения используется следующий синтаксис:

```md
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

Где `alt text` — краткое описание изображения, а `<folder path>` — относительный путь к нему. Заменяющий текст необходим для средств чтения с экрана для слабовидящих. Он также удобен при возникновении ошибок на сайте, из-за которых не удается воспроизвести изображение.

Изображения должны храниться в папке `/media` в наборе документации. Для изображений по умолчанию поддерживаются следующие типы файлов:

- JPG,
- PNG.

Вы можете добавить поддержку других типов изображений, добавив их в виде ресурсов в файл docfx.json<!--add link to reference when available--> для вашего набора документации.

## <a name="links"></a>Создание ссылок

Как правило, платформа Docs использует стандартные ссылки Markdown на другие файлы и страницы. Типы ссылок описываются в подразделах ниже.

> [!TIP]
> Пакет создания документации для VS Code помогает правильно вставлять ссылки и закладки в автоматическом режиме.

> [!IMPORTANT]
> Не включайте коды языковых стандартов, такие как en-us, в ссылки на сайты Майкрософт. Жестко закодированные коды языков блокируют воспроизведение локализованного содержимого: это неудобно для пользователей, говорящих на других языках, и влечет за собой большие затраты на локализацию. При копировании URL-адреса из браузера код языка включается по умолчанию, поэтому его необходимо удалить вручную при создании ссылки. Например, используйте:
>
> `[Microsoft](https://www.microsoft.com)`
>
> А не:
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a>Относительные ссылки на файлы в том же наборе документации

Относительный путь — это путь к целевому файлу относительно текущего файла. На платформе Docs относительные пути можно использовать для связывания файлов в одном наборе документов. Синтаксис относительного пути следующий:

```md
[link text](../../folder/filename.md)
```

Где `../` означает один уровень выше в иерархии.

- Относительный путь будет разрешаться во время сборки, включая удаление расширения MD.
- Можно использовать "../" для указания на файл в родительской папке, но этот файл должен быть в том же наборе документации. "../" нельзя использовать для указания на файл в другой папке набора документации.
- Платформа Docs также поддерживает особый формат относительного пути, начинающийся с символа "~" (например, ~/foo/bar.md). Этот синтаксис указывает файл относительно корневой папки набора документации. Этот вид пути также проверяется и разрешается во время сборки.

> [!IMPORTANT]
> Включите расширение файла в относительный путь. В ходе сборки проверяется существование целевого файла по этому относительному пути. Если относительный путь не включает расширение файла, в ходе сборки, скорее всего, будет создано предупреждение или неработающая ссылка. Например, используйте:
>
> `[link text](../../folder/filename.md)`
>
> А не:
>
> `[link text](../../folder/filename)`

### <a name="site-relative-links-to-other-files-on-docs"></a>Относительные ссылки на другие файлы на платформе Docs на сайте

```md
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

Не включайте расширение файла (MD). Это ссылка на обзорный файл Linux за пределами набора документации "статей" Azure.

### <a name="links-to-external-sites"></a>Ссылки на внешние сайты

```md
[Microsoft](https://www.microsoft.com)
```

Ссылка на основе URL-адреса на другую веб-страницу (должна включать https://).

### <a name="bookmark-links"></a>Ссылки закладок

Ссылка-закладка на заголовок в другом файле того же репозитория. Например:

```md
[Managed Disks](../../linux/overview.md#managed-disks)
```

Ссылка-закладка на заголовок в текущем файле:

```md
[Managed Disks](#managed-disks)
```

Используйте решетку `#`, а затем укажите слова заголовка на английском языке. Чтобы преобразовать текст заголовка в текст ссылки:
- Используйте строчные буквы
- Удалите знаки препинания
- Замените пробелы на дефисы

Например, если английская версия статьи имеет заголовок "2.2 Security concerns", то текст ссылки-закладки будет "#22-security-concerns".

### <a name="explicit-anchor-links"></a>Явные ссылки привязки

Явные ссылки привязки, использующие HTML-тег `<a>` **не требуются и не рекомендуются**, за исключением страниц-концентраторов и целевых страниц. Используйте закладки, как описано выше, в общих файлах Markdown. Для страниц-концентраторов и целевых страниц привязки используются следующим образом:

`## <a id="AnchorText"> </a>Header text` или `## <a name="AnchorText"> </a>Header text`

Для ссылки на явные привязки используйте следующий синтаксис:

```md
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a>Ссылки XREF (перекрестные ссылки)

Для ссылки на автоматически создаваемые страницы справочных материалов по API в текущем или другом наборе документации используйте ссылки XREF с уникальным идентификатором (UID).

> [!NOTE]
> Для ссылки на страницы справочных материалов по API в других наборах документации потребуется добавить конфигурацию `xrefService` в файл `docfx.json`.
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

Уникальный идентификатор совпадает с полным именем класса и члена. Если добавить символ * после UID, ссылка будет вести на страницу перегрузки, а не к конкретному API. Например, используйте `List<T>.BinarySearch*` для ссылки на страницу "Метод BinarySearch" вместо ссылки на конкретную перегрузку, например `List<T>.BinarySearch(T, IComparer<T>)`.

Можно выбрать один из следующих вариантов синтаксиса:

- Автоматическая ссылка: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`

  Необязательный параметр запроса `displayProperty` создает полный текст ссылки. По умолчанию в тексте ссылки отображается только имя члена или типа.

- Ссылка с разметкой Markdown: `[link text](xref:UID)`
  
  Используется, когда требуется настроить текст ссылки.

Примеры:

- `<xref:System.String>` отображается как String;
- `<xref:System.String?displayProperty=nameWithType>` отображается как System.String;
- `[String class](xref:System.String)` отображается как String class.

Сейчас не существует простого способа поиска UID. <!-- ? -->Чтобы найти UID для API, просмотрите исходный код страницы API, на которую нужно создать ссылку, и найдите значение ms.assetid. Отдельные значения перегрузки не отображаются в исходном коде. Мы работаем над улучшением нашей системы.

Если идентификатор содержит специальные символы \`, \# или \*, значение UID должно быть закодировано в HTML как `%60`, `%23` и `%2A` соответственно. Иногда круглые скобки тоже кодируются, но это не обязательно.

Примеры:

- System.Threading.Tasks.Task\`1 заменяется на `System.Threading.Tasks.Task%601`;
- System.Exception.\#ctor заменяется на `System.Exception.%23ctor`;
- System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) заменяется на `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`.

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a>Списки (нумерованные, маркированные, контрольные)

### <a name="numbered-list"></a>Нумерованный список

Для создания нумерованного списка можно использовать все 1, которые при публикации отображаются как последовательный список. Для повышения удобства чтения исходного кода списки можно вводить с приращением.

Не используйте в списках, включая вложенные списки, буквы. При публикации на платформе Docs они преобразуются некорректно. Вложенные списки с цифрами преобразуются в списки со строчными буквами при публикации. Например:

```md
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

Для создания маркированного списка используйте `-`, за которым следует пробел в начале каждой строки.

```md
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

### <a name="checklist"></a>Контрольный список

Контрольные списки можно использовать (только) на сайте docs.microsoft.com с помощью пользовательского расширения Markdown:

```md
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

Этот пример отображается на сайте docs.microsoft.com следующим образом:

> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3

Контрольные списки используются в начале или конце статьи для подведения итогов "Чему вы научитесь" или "Чему вы научились". Не вставляйте контрольные списки в статьи по случайному принципу.
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a>Действие "Дальнейшие действия"

Пользовательское расширение можно использовать для добавления кнопки "Дальнейшие действия" на страницы (только) docs.microsoft.com.

Используйте следующий синтаксис:

```md
> [!div class="nextstepaction"]
> [button text](link to topic)
```

Например:

```md
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

Это отображается следующим образом:

> [!div class="nextstepaction"]
> [Подробнее о базовом стиле](style-quick-start.md)

Вы можете использовать любые поддерживаемые ссылки в действии "Дальнейшие действия", включая ссылку Markdown на другую веб-страницу. Как правило, ссылка "Дальнейшие действия" — это относительная ссылка на другой файл в том же наборе документации.

## <a name="section-definition"></a>Определение раздела

<!-- more info about this would be helpful! -->
Вам может потребоваться определить раздел. Этот синтаксис в основном используется для таблиц кодов.
См. указанный ниже пример.

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

Предыдущий текст Markdown будет отображаться следующим образом:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a>Селекторы

<!-- could be more clear! -->
Используйте селектор для связи с разными страницами одной статьи. Затем читатели смогут переключаться между этими страницами.

> [!NOTE]
> Это расширение функционирует по-разному на сайтах docs.microsoft.com и MSDN. <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a>Единичный выбор

```
> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)
```

... будет иметь следующий вид:

> [!div class="op_single_selector"]
> - [Универсальные приложения Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a>Множественный выбор

```
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)
```

... будет иметь следующий вид:

> [!div class="op_multi_selector" title1="Платформа" title2="Серверная часть"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Универсальные приложения Windows на C# | .NET)](how-to-write-workflows-major.md)
> - [(Универсальные приложения Windows на C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)

## <a name="tables"></a>Tables

Использование вертикальных линий и строк является самым простым способом создания таблиц в Markdown. Чтобы создать стандартную таблицу с заголовком, вставьте пунктирную линию после первой строки.

```md
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

Можно также создать таблицу без заголовка. Например, чтобы создать список с несколькими столбцами:

```md
|   |   |
| - | - |
| This | table |
| has no | header |
```

Это отображается следующим образом:

|   |   |
| - | - |
| Это | таблица |
| без | заголовка |

Можно выровнять столбцы с помощью двоеточий:

```md
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

Отображается следующим образом:

|                  |
|------------------|
|    по правому краю:|
|:по левому краю     |
|:по центру            :|

> [!TIP]
> Расширение создания документации для VS Code упрощает добавление базовых таблиц Markdown.
>
> Кроме того, можно использовать [веб-инструмент создания таблиц](http://www.tablesgenerator.com/markdown_tables).

### <a name="mx-tdbreakall"></a>mx-tdBreakAll

> [!IMPORTANT]
> Эта функция работает только на веб-сайте docs.microsoft.com.

Создаваемая в Markdown таблица может выходить вправо, что делает ее нечитаемой. Эту проблему можно устранить, разрешив при необходимости разрыв таблицы при отображении документов. Нужно просто заключить таблицу в настраиваемый класс `[!div class="mx-tdBreakAll"]`.

Далее приведен пример Markdown таблицы с тремя строками, которая будет заключена с помощью `div` с классом `mx-tdBreakAll`.

```md
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

### <a name="mx-tdcol2breakall"></a>mx-tdCol2BreakAll

> [!IMPORTANT]
> Эта функция работает только на веб-сайте docs.microsoft.com.

Время от времени во втором столбце таблицы могут находиться очень длинные слова. Чтобы правильно разделить эти слова, можно применить класс `mx-tdCol2BreakAll` с помощью синтаксиса оболочки `div`, как показано выше.

### <a name="html-tables"></a>Таблицы HTML

Таблицы HTML не рекомендуется использовать для docs.microsoft.com. Они трудны для восприятия в исходном виде — это нарушает основной принцип Markdown.

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a>Видеоролики

### <a name="embedding-videos-into-a-markdown-page"></a>Внедрение видео на страницу Markdown

Сейчас платформа Docs поддерживает видеоролики, опубликованные в одной из трех платформ:

- YouTube
- Channel 9
- собственной системе Майкрософт One Player.

Вы можете встроить видео с помощью следующего синтаксиса, и это видео будет отображено на платформе Docs.

```md
> [!VIDEO <embedded_video_link>]
```

Пример.

```md
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

... будет отображаться как:

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

Содержимое на опубликованных страницах будет отображаться следующим образом:

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> URL-адрес видео для канала CH9 должен начинаться с `https` и заканчиваться `/player`. В противном случае будет внедрена вся страница, а не только видео.

### <a name="uploading-new-videos"></a>Отправка новых видео

Для загрузки новых видео используйте следующую процедуру.

1. Присоединитесь к группе **docs_video_users** на портале IDWEB.
1. Перейдите на страницу https://aka.ms/VideoUploadRequest и введите сведения о видеоролике. Вам потребуются следующие сведения (ни один из пунктов не будет отображаться для зрителей):
    1. название видео;
    1. список продуктов или служб, с которыми связано видео;
    1. целевая страница или (если такой страницы еще нет) набор документации, где будет размещаться ваше видео;
    1. ссылка на файл MP4 видео (если вам некуда отправить файл, можете временно поместить его сюда: `\\scratch2\scratch\apex`) (разрешение файла MP4 должно быть не менее 720p);
    1. описание видео.
1. Отправьте (сохраните) этот элемент.
1. Видео будет выгружено в течение двух рабочих дней. Ссылка, необходимая для внедрения, будет помещена в рабочий элемент и *возвращена вам*.
1. Получив ссылку на видео, закройте рабочий элемент.
1. Ссылку на видео можно добавить в публикацию, используя следующий синтаксис:

   ```md
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
