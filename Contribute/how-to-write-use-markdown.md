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
# <a name="how-to-use-markdown-for-writing-docs"></a>Использование языка разметки Markdown для написания документации

Статьи на сайте [docs.microsoft.com](https://docs.microsoft.com) написаны на [Markdown](https://daringfireball.net/projects/markdown/) — упрощенном языке разметки, который легко использовать и изучать. Благодаря своей простоте он быстро становится отраслевым стандартом. Для документов сайта используется [тип Markdig](#markdown-flavor) разметки Markdown.


## <a name="markdown-basics"></a>Базовые сведения о Markdown

### <a name="headings"></a>Заголовки

Чтобы создать заголовок, используйте знак (#), например:

```md
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

В заголовках следует использовать стиль atx, то есть 1–6 символов решетки (#) в начале строки, чтобы указать на заголовок, соответствующий заголовкам HTML уровней с H1 по H6. Сверху приводятся примеры заголовков с первого по четвертый уровень.

В статье **должен** быть только один заголовок первого уровня (H1), который будет отображаться как заголовок страницы.

Если заголовок заканчивается на символ `#`, добавьте в конце еще символ `#`, чтобы заголовок отображался правильно. Например, `# Async Programming in F# #`.

Заголовки второго уровня создадут оглавление, которое будет отображаться в разделе "В этой статье" под заголовком статьи.

### <a name="bold-and-italic-text"></a>Полужирное и курсивное начертания

Чтобы задать для текста **полужирное начертание**, заключите его в двойные звездочки:

```md
This text is **bold**.
```

Чтобы задать для текста *курсивное начертание*, заключите его в одинарные звездочки:

```md
This text is *italic*.
```

Чтобы задать для текста ***полужирное и курсивное*** начертание, заключите его в тройные звездочки:

```md
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a>Блоки цитирования

Блоки цитирования создаются с помощью символа `>`:

```md
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

Предыдущий пример отображается следующим образом:

> Засуха продолжалась десять миллионов лет, и царству ужасных ящеров уже давно пришел конец. Здесь, близ экватора, на материке, который позднее назовут Африкой, с новой яростью вспыхнула борьба за существование, и еще не ясно было, кто выйдет из нее победителем. На этой бесплодной, иссушенной зноем земле благоденствовать или хотя бы просто выжить могли только маленькие, или ловкие, или свирепые.

### <a name="lists"></a>Списки

#### <a name="unordered-list"></a>Неупорядоченный список

Неупорядоченный (маркированный) список можно отформатировать с помощью звездочек или тире. Например, следующая разметка Markdown:

```md
- List item 1
- List item 2
- List item 3
```

будет отображаться как:

- List item 1
- List item 2
- List item 3

Чтобы вложить один список в другой, добавьте отступ для элементов дочернего списка. Например, следующая разметка Markdown:

```md
- List item 1
  - List item A
  - List item B
- List item 2
```

будет отображаться как:

- List item 1
  - List item A
  - List item B
- List item 2

#### <a name="ordered-list"></a>Упорядоченный список

Упорядоченный (ступенчатый) список можно отформатировать с помощью соответствующих цифр. Например, следующая разметка Markdown:

```md
1. First instruction
1. Second instruction
1. Third instruction
```

будет отображаться как:

1. First instruction
2. Second instruction
3. Third instruction

Чтобы вложить один список в другой, добавьте отступ для элементов дочернего списка. Например, следующая разметка Markdown:

```md
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

будет отображаться как:

1. First instruction
   1. Sub-instruction
   2. Sub-instruction
2. Second instruction

Обратите внимание, что мы используем "1." для всех записей. Так проще увидеть различия, когда потом будут добавлены новые шаги или удалены существующие.

### <a name="tables"></a>Tables

Таблицы не входят в основную спецификацию Markdown, но они поддерживаются в GFM. Создавать таблицы можно с помощью символов вертикальной черты (|) и дефиса (-). Дефисы позволяют создавать для каждого столбца заголовок. Вертикальные черты разделяют столбцы. Чтобы таблица правильно отображалась, включите перед ней пустую строку.

Например, следующая разметка Markdown:

```md
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

Она будет отображаться так:

| Fun                  | with                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |

Дополнительные сведения о создании таблиц:

- Статья на сайте GitHub [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/) (Организация информации с помощью таблиц).
- Веб-приложение [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables).
- Статья Адама Притчарда (Adam Pritchard) [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables) (Шпаргалка по Markdown).
- Статья Майкла Фортина (Michel Fortin) [Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) (Расширение Markdown Extra).
- [Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/) (Преобразование таблиц HTML в Markdown).

### <a name="links"></a>Создание ссылок

Синтаксис Markdown для встроенной ссылки состоит из части `[link text]`, представляющей текст гиперссылки, и части `(file-name.md)` — URL-адреса или имени файла, на который дается ссылка:

 `[link text](file-name.md)`

Дополнительные сведения о ссылках:

- [Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax#link) (Руководство по синтаксису Markdown), в котором предоставлена основная информация по поддержке ссылок Markdown.
- Страница [Ссылки](how-to-write-links.md) в этом руководстве содержит сведения о дополнительном синтаксисе Markdig для ссылок.

### <a name="code-snippets"></a>Фрагменты кода

Markdown поддерживает как встраивание фрагментов кода в предложение, так и их размещение между предложениями в виде отдельных огражденных блоков. Дополнительная информация:

- [Сведения о собственной поддержке блоков кода Markdown](https://daringfireball.net/projects/markdown/syntax#precode)
- [Сведения о поддержке GFM для ограждения кода и выделения синтаксиса](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

Огражденные блоки кода — это простой способ выделить синтаксис для фрагментов кода. Общий формат огражденных блоков кода:

    ```alias
    ...
    your code goes in here
    ...
    ```

Псевдоним после трех начальных символов обратного апострофа (\`) определяет использование выделения синтаксиса. Ниже представлен список часто используемых языков программирования для написания документации и приводятся соответствующие метки.

Все эти языки поддерживают понятные имена, а большинство из них — выделение языка в имени.

|Имя|Метка Markdown|
|-----|-------|
|.NET Console|dotnetcli|
|ASP.NET (C#)|aspx-csharp|
|ASP.NET (VB)|aspx-vb|
|AzCopy|azcopy|
|Azure CLI|azurecli|
|Azure PowerShell|azurepowershell|
|Bash|Bash|
|C++|cpp|
|C++/CX|cppcx|
|C++/WinRT|cppwinrt|
|C#|csharp|
|C# в браузере|csharp-interactive|
|Консоль|консоль|
|CSHTML|cshtml|
|DAX|dax|
|Docker|dockerfile|
|F#|fsharp|
|Go|go|
|HTML|html|
|HTTP|http|
|Java|java|
|JavaScript|javascript|
|JSON|json|
|Язык запросов Kusto|kusto|
|Markdown|md|
|Objective-C|objc|
|OData|odata|
|PHP|php|
|protobuf|protobuf|
|PowerApps (десятичный разделитель — точка)|powerapps-dot|
|PowerApps (десятичный разделитель — запятая)|powerapps-comma|
|PowerShell|powershell|
|Python|python|
|Q#|qsharp|
|R|r|
|Ruby|ruby|
|SQL|sql|
|Swift|swift|
|TypeScript|typescript|
|VB|vb|
|XAML|xaml|
|XML|xml|

Имя `csharp-interactive` указывает на язык C# и возможность запускать примеры в браузере. Эти фрагменты кода компилируются и выполняются в контейнере Docker, а результаты выполнения программы отображаются в окне браузера пользователя.

#### <a name="example-c"></a>Пример. C\#

__Markdown__

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

__Отображение__

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

#### <a name="example-sql"></a>Пример. SQL

__Markdown__

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

__Отображение__

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="docs-custom-markdown-extensions"></a>Настраиваемые расширения Markdown для документации

> [!NOTE]
> Сайт Docs.Microsoft.com (сайт документации) использует Markdig, синтаксический анализатор Markdown, обеспечивающий высокую совместимость с диалектом GitHub Flavored Markdown (GFM). Markdig добавляет дополнительные функции за счет расширений Markdown. Поэтому для справки мы включили в этот материал некоторые разделы из руководства по разработке OPS. (Например, см. в содержании разделы "Markdig и расширения Markdown" и "Фрагменты кода".)

В статьях документации для общего форматирования, например для создания абзацев, ссылок, списков и заголовков, используется GFM. Для расширенного форматирования в статьях можно использовать следующие функции Markdig:

- Блоки заметок
- Включаемые файлы
- Селекторы
- Внедряемые видео
- Фрагменты или примеры кода

Полный список см. в разделах "Markdig и расширения Markdown" и "Фрагменты кода".

### <a name="note-blocks"></a>Блоки заметок

Есть четыре типа блоков заметок, которые позволяют привлечь внимание к определенному содержимому:

- NOTE (примечание)
- WARNING (предупреждение)
- TIP (подсказка)
- IMPORTANT (важно)

В целом не следует часто использовать блоки заметок, так как они могут отвлекать пользователя от основного содержимого. Хотя эти элементы также поддерживают блоки кода, изображения, списки и ссылки, лучше не перегружать их, делая простыми и понятными.

Примеры:

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

### <a name="include-files"></a>Включаемые файлы

Если вы хотите добавить в файлы статей многократно используемые изображения или текст, воспользуйтесь доступной в Markdig функцией включения ("include") файлов по ссылке. Функция указывает OPS включить файл в файл статьи во время сборки, чтобы он стал частью опубликованной статьи. Существует три типа включения файлов для многократного использования содержимого:

- Встроенные: Используются для многократного использования фрагмента стандартного текста путем его встраивания в другое предложение.
- Блочные: Используются для многократного использования всего файла Markdown в качестве блока путем его вложения в раздел или статью.
- Изображения: Так на платформе Docs реализовано стандартное включение изображений.

Встроенные и блочные включаемые файлы — это простые файлы Markdown с расширением .md. Они могут содержать любую допустимую разметку Markdown. Все включаемые файлы Markdown должны быть помещены в [общий подкаталог `/includes`](git-github-fundamentals.md#includes-subdirectory) в корневом каталоге репозитория. Когда статья публикуется, включаемый файл легко интегрируется в нее.

Ниже приведены требования к включаемым файлам и соображения по работе с ними:

- Используйте включаемые файлы, если вам нужно, чтобы один и тот же текст отображался в нескольких статьях.
- Блочные включаемые файлы предназначены для значительных объемов текста: один или два абзаца, общая процедура или общий раздел. Не используйте их для фрагментов текста меньше одного предложения.
- Включаемые файлы не будут отображаться в представлении статьи на GitHub, так как они работают только с Markdig-расширениями. Они отображаются только после публикации.
- Весь текст во включаемом файле должен состоять из полноценных предложений или фраз, не зависящих от остального текста статьи, в которую добавляется ссылка на такой файл. Если не следовать этой инструкции, в статье создаются непереводимые строки, которые нарушают процесс локализации.
- Не внедряйте одни включаемые файлы в другие. Такая возможность не поддерживается.
- Файлы мультимедиа должны быть помещены в отдельную папку мультимедиа в подкаталоге включаемых файлов. Например, `<repo>`/включаемые файлы/папка мультимедиа. В корне каталога мультимедиа не должны содержаться изображения. Если во включаемом файле нет изображений, соответствующий каталог мультимедиа не требуется.
- Как и в обычных статьях, не используйте общий файл мультимедиа для включаемых файлов. Для каждого включаемого файла в статье должен быть создан отдельный файл с уникальным именем. Файл мультимедиа должен храниться в папке мультимедиа, связанной с включаемым файлом.
- Не используйте включаемый файл как единственное содержимое статьи.  Включаемые файлы предназначены для дополнения основных материалов статьи.

Пример.

```md
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a>Селекторы

В технических статьях селекторы применяются для создания разных вариантов содержимого, чтобы проиллюстрировать различия в реализации, связанные с использованием нескольких технологий или платформ. Это в особенности применимо к материалам о мобильных платформах для разработчиков. Сейчас в Markdig есть два типа селекторов: для единичного и множественного выбора.

В каждой статье с возможностью выбора используется одна и та же разметка Markdown для селектора. Поэтому рекомендуется поместить селектор для статьи во включаемый файл. Затем нужно добавить ссылки на этот файл во все статьи, для которых используется селектор.

Ниже приведен пример селектора:

```md
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

Пример селекторов в действии можно посмотреть в [документации по Azure](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).

### <a name="code-include-references"></a>Включение фрагментов кода

Расширение Markdown для фрагментов кода в документации позволяет вам вставлять в свои статьи фрагменты кода и форматировать их синтаксис в соответствии с используемым языком программирования. Вы можете включать код из текущего либо из какого-то другого репозитория. Ниже приведены инструкции по использованию этой функции с пакетом создания документации [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack). Доступен **Предварительный просмотр** фрагментов кода в Visual Studio Code. Предварительный просмотр не поддерживает выделение и интерактивные возможности.

> [!NOTE]
> Расширение не поддерживает включение в содержимое кода во встроенном (inline) режиме. Используйте для этого стандартный элемент ``` в Markdown.

#### <a name="code-from-current-repository"></a>Код из текущего репозитория

1. Находясь в Visual Studio Code, нажмите клавиши **ALT+M** или **OPTION+M** и выберите "Фрагмент кода".
2. Вам будет предложено выполнить поиск по всему содержимому, в какой-то области или по различным репозиториям. Выберите поиск по всему локальному содержимому.
3. Введите условие поиска и найдите нужный файл. Найдя файл, выберите его.
4. Затем выберите, какие строки кода нужно включить в фрагмент, используя следующие параметры: **ИД**, **Диапазон** или **Никакие**.
5. В зависимости от выбора на шаге 4 предоставьте необходимые значения.

Отображение всего файла кода:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

Отображение части файла кода путем указания номера строк:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

Отображение части файла кода путем указания имени фрагмента:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

#### <a name="code-from-another-repository"></a>Код из другого репозитория

1. Находясь в Visual Studio Code, нажмите клавиши **ALT+M** или **OPTION+M** и выберите "Фрагмент кода".
2. Вам будет предложено выполнить поиск по всему содержимому, в какой-то области или по различным репозиториям. Выберите поиск по репозиториям.
3. Вам будет представлен набор репозиториев из *.openpublishing.publish.config.json*. Выберите репозиторий.
3. Введите условие поиска и найдите нужный файл. Найдя файл, выберите его.
4. Затем выберите, какие строки кода нужно включить в фрагмент, используя следующие параметры: **ИД**, **Диапазон** или **Никакие**.
5. В зависимости от выбора на шаге 5 предоставьте необходимые значения.

Ссылка на фрагмент кода будет выглядеть следующим образом:

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

#### <a name="path-to-code-file"></a>Путь к файлу кода

Пример.

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

Пример взят из репозитория документов ASP.NET, файла статьи [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md). Для ссылки на файл кода используется относительный путь к [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) в том же репозитории.

#### <a name="selected-line-numbers"></a>Выбранные номера строк

Пример.

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

В этом примере отображаются только строки 2–24 и 26 из файла кода *StudentController.cs*.

Предпочтительнее использовать фрагменты кода по номерам жестко закодированных строк, как описано в следующем разделе.

#### <a name="named-snippet"></a>Именованный фрагмент кода

Пример.

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

Используйте для имени только буквы и символы подчеркивания.

В примере отображается раздел `snippet_Create` файла кода. В файле кода для этого примера имеется часть на C# с именем `snippet_Create`:

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

По возможности ссылайтесь на именованный раздел, а не указывайте номера строк. Ссылки на номера строк являются ненадежными, так как файлы кода неизбежно изменяются с помощью способов, которые изменяют номера строк.
Вы не обязательно получите уведомления об этих изменениях. В статье в конечном итоге будут отображаться неправильные строки, и вы даже не будете об этом знать.

#### <a name="highlighting-selected-lines"></a>Выделение выбранных строк

Пример.

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

В примере выделены строки 2 и 5, если считать от начала отображаемого фрагмента кода. (Подсчет выделяемых номеров строк не начинается от начала файла кода.) Другими словами, выделяются строки 3 и 6 файла кода.

#### <a name="interactive-code-snippets"></a>Интерактивные фрагменты кода

Для фрагментов кода, включаемых по ссылке, можно включить интерактивный режим. Ниже приведены примеры:

```markdown
:::code language="powershell" source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code language="bash" source="Bash.sh" interactive="cloudshell-bash":::
```

Чтобы включить эту функцию для конкретного блока кода, используйте атрибут `interactive`. Допустимые значения атрибута:

- `cloudshell-powershell` — активирует Cloud Shell в Azure PowerShell, как в предыдущем примере.
- `cloudshell-bash` — включает Azure Cloud Shell
- `try-dotnet` — активирует Try .NET.
- `try-dotnet-class` — активирует Try .NET с формированием шаблонов классов.
- `try-dotnet-method` — активирует Try .NET с формированием шаблонов методов.

Существуют совместимые пары `language` и `interactive`. Например, если для `interactive` задано `try-dotnet`, должен использоваться язык `csharp`. Аналогичным образом `cloudshell-powershell` будет работать только с `powershell`, а `cloudshell-bash` — только с языком `bash`.

В Azure Cloud Shell и PowerShell Cloud Shell пользователи могут выполнять команды только с собственной учетной записью Azure.

[Try .NET](https://github.com/dotnet/try) позволяет использовать интерактивное выполнение кода .NET (C#) в браузере. Для Try .NET доступны три варианта интерактивности: `try-dotnet`, `try-dotnet-class` и `try-dotnet-method`. Для этих возможностей не требуется какая-либо дополнительная конфигурация в фрагменте кода. Доступные сейчас по умолчанию пространства имен:

- System
- System.Linq
- System.Collections.Generic
- System.Text
- System.Globalization
- System.Text.RegularExpressions

Значение атрибута `try-dotnet` позволяет пользователям выполнять код C# в браузере напрямую, не заключая его в код-оболочку.

Пример.

```md
:::code language="csharp" source="relative/path/source.cs" interactive="try-dotnet":::
```

Значение `try-dotnet-class` активирует формирование шаблонов на уровне классов для кода, передаваемого интерактивному компоненту.

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-class":::
```

Пример.

Фрагмент кода без формирования шаблонов классов

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

Фрагмент кода с формированием шаблонов классов

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

Значение `try-dotnet-method` активирует формирование шаблонов на уровне методов для кода, передаваемого интерактивному компоненту.

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-method":::
```

Пример.

Фрагмент кода без формирования шаблонов методов

```md
/*Print some string in C#*/

Console.WriteLine("Hello C#.);
```

Фрагмент кода с формированием шаблонов методов

```md
public static void Main(string args[]) {

/*Print some string in C#*/

Console.WriteLine("Hello C#.);
}
```

#### <a name="snippet-syntax-reference"></a>Синтаксис ссылок на фрагменты

Вы можете ссылаться на фрагменты кода, хранящиеся в репозитории, с помощью указанного языка кода. Содержимое заданного пути к коду будет развернуто и включено в файл.

Какие-либо ограничения на структуру папок для фрагментов кода отсутствуют. Управление фрагментами кода осуществляется аналогично управлению обычным исходным кодом.

Синтаксис

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> Этот синтаксис является блоком расширения Markdown. Он должен использоваться в отдельной строке.

- `<language>` (*необязательно*)
  - Язык фрагмента кода. Дополнительные сведения см. в разделе [Поддерживаемые языки](#supported-languages) далее в этой статье.

- `<path>` (*обязательно*)
  - Относительный путь в файловой системе, который указывает файл фрагмента кода для ссылки.

- `<attribute>` и `<attribute-value>` (*необязательно*)
  - Используются вместе для указания способа получения кода из файла:
    - `range`: `1,3-5` Диапазон строк. Этот пример содержит строки 1, 3, 4 и 5.
    - `id`: `snippet_Create` Идентификатор фрагмента, который нужно вставить из файла кода. Это значение не может существовать одновременно с диапазоном.
    - `highlight`: `2-4,6` Диапазон и (или) номера строк, которые должны выделяться в создаваемом фрагменте кода. Нумерация ведется в масштабе самого фрагмента, а не импортируемого диапазона.
    - `interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` Строковое значение, определяющее тип используемой интерактивности.

#### <a name="supported-languages"></a>Поддерживаемые языки

|Имя|Название Markdown|
|-----|-------|
|.NET Core CLI|`dotnetcli`|
|ASP.NET с C#|`aspx-csharp`|
|ASP.NET с Visual Basic|`aspx-vb`|
|Azure CLI|`azurecli`|
|Azure CLI в браузере|`azurecli-interactive`|
|Azure PowerShell в браузере|`azurepowershell-interactive`|
|AzCopy|`azcopy`|
|Bash|`bash`|
|C++|`cpp`|
|C#|`csharp`|
|C# в браузере|`csharp-interactive`|
|Консоль|`console`|
|CSHTML|`cshtml`|
|DAX|`dax`|
|Docker|`Dockerfile`|
|F#|`fsharp`|
|HTML|`html`|
|Java|`java`|
|JavaScript|`javascript`|
|JSON|`json`|
|Язык запросов Kusto|`kusto`|
|Markdown|`md`|
|Objective-C|`objc`|
|PHP|`php`|
|PowerShell|`powershell`|
|Power Query M|`powerquery-m`|
|protobuf|`protobuf`|
|Python|`python`|
|Ruby|`ruby`|
|SQL|`sql`|
|Swift|`swift`|
|VB|`vb`|
|XAML|`xaml`|
|XML|`xml`|
|YAML|`yml`|

#### <a name="code-extensions"></a>Расширения кода

|Имя|Название Markdown|Расширение файла|
|-----|-------|-----|
|C#|csharp|.cs, .csx|
|C++|cpp|.cpp, .h|
|F#|fsharp|.fs|
|Java|java|.java|
|JavaScript|javascript|.js|
|Python|python|.py|
|SQL|sql|.sql|
|VB|vb|.vb|
|XAML|xaml|.xaml|
|XML|xml|.xml|

## <a name="gotchas-and-troubleshooting"></a>Сбои и устранение неполадок

### <a name="alt-text"></a>Замещающий текст

Замещающий текст, который содержит символы подчеркивания, отображается некорректно. Например, вместо

```md
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

используйте следующий вариант, позволяющий избежать символов подчеркивания:

```md
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a>Апострофы и кавычки

Если вы копируете текст из Word в редактор Markdown, он может содержать книжные (изогнутые) апострофы или кавычки. Их нужно заменить кодом или обычными апострофами или кавычками. В противном случае после публикации файла может отобразиться нечитаемый текст, например: Itâ€™s

Ниже приведены кодировки для этих знаков пунктуации:

- левая (открывающая) кавычка: `&#8220;`;
- правая (закрывающая) кавычка: `&#8221;`;
- правая закрывающая одинарная кавычка или апостроф: `&#8217;`;
- левая открывающая одинарная кавычка (используется редко): `&#8216;`.

### <a name="angle-brackets"></a>Угловые скобки

Угловые скобки, как правило, используются для обозначения заполнителя. Если вы используете угловые скобки в тексте (а не в коде), их необходимо закодировать. В противном случае разметка Markdown считает их HTML-тегами.

Например, `<script name>` следует закодировать как `&lt;script name&gt;`.

## <a name="markdown-flavor"></a>Тип разметки Markdown

Серверная часть сайта docs.microsoft.com поддерживает разметку Markdown в соответствии с [CommonMark](https://commonmark.org/) и ее синтаксический анализ через подсистему [Markdig](https://github.com/lunet-io/markdig). Такой тип разметки совместим с [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), так как большинство документов хранятся на GitHub, где их можно править. Дополнительные функции добавляются с помощью расширений Markdown.

## <a name="see-also"></a>Дополнительные материалы

### <a name="markdown-resources"></a>Ресурсы Markdown

- [Markdown: Syntax](https://daringfireball.net/projects/markdown/syntax) (Синтаксис Markdown)
- [Markdown cheat-sheet](./media/documents/markdown-cheatsheet.pdf?raw=true) (Шпаргалка по Markdown)
- [Базовые сведения о разметке Markdown на GitHub](https://help.github.com/articles/markdown-basics/)
- [The Markdown Guide](https://www.markdownguide.org/) (Руководство по Markdown)
