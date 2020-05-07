---
title: Включение кода в документы
description: Узнайте, как включить элементы и фрагменты кода в статьи, публикуемые на сайте docs.microsoft.com.
author: tdykstra
ms.author: tdykstra
ms.date: 03/03/2020
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 4aa34196f59a69651dd19add35a0351dd9b5d59b
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336469"
---
# <a name="how-to-include-code-in-docs"></a>Включение кода в документы

Есть несколько способов включить код в статью, публикуемую на сайте docs.microsoft.com:

* Отдельные элементы (слова) в строке.

  Ниже приведен пример стиля `code`.

  Используйте формат кода при ссылке на именованные параметры и переменные в ближайшем блоке кода в тексте. Формат кода также можно использовать для свойств, методов, классов и ключевых слов языка. Дополнительные сведения см. в разделе [Элементы кода](#code-elements) далее в этой статье.

* Блоки кода в файле Markdown, содержащем статью.

  ```markdown
      ```csharp
      public static void Log(string message)
      {
          _logger.LogInformation(message);
      }
      ```
  ```

  Используйте встроенные блоки кода, когда непрактично отображать код по ссылке на файл кода. Дополнительные сведения см. в разделе [Блоки кода](#inline-code-blocks) далее в этой статье.

* Блоки кода с использованием ссылки на файл кода в локальном репозитории.

  ```markdown
  :::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
  ```

  Дополнительные сведения см. в разделе [Ссылки на фрагменты кода в репозитории](#in-repo-snippet-references) далее в этой статье.

* Блоки кода с использованием ссылки на файл кода в другом репозитории.

  ```markdown
  :::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
  ```
  
  Дополнительные сведения см. в разделе [Ссылки на фрагменты кода вне репозитория](#out-of-repo-snippet-references) далее в этой статье.
  
* Блоки кода, которые позволяют пользователю выполнять код в браузере.

   ```markdown
  :::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
  ```

  Дополнительные сведения см. в разделе [Интерактивные фрагменты кода](#interactive-code-snippets) далее в этой статье.

Помимо описания синтаксиса Markdown для каждого метода включения кода, в статье приведено [общее руководство для всех блоков кода](#code-blocks).

## <a name="code-elements"></a>Элементы кода

"Элемент кода" является ключевым словом языка программирования, именем класса, именем свойства и т. д. Не всегда очевидно, что рассматривается в качестве кода. Например, имена пакетов NuGet должны считаться кодом. Если возникают сомнения, ознакомьтесь с [рекомендациями по форматированию текста](text-formatting-guidelines.md).

### <a name="inline-code-style"></a>Встроенные стили кода

Чтобы включить элемент кода в текст статьи, поместите его между одинарными кавычками в виде обратного апострофа (\`) для указания стиля кода.
Встроенный стиль кода не должен использовать формат тройных кавычек.

|Markdown |Отображение |
|---------|---------|
|По умолчанию Entity Framework интерпретирует свойство с именем \`Id\` или \`ClassnameID\` как первичный ключ.|По умолчанию Entity Framework интерпретирует свойство с именем `Id` или `ClassnameID` как первичный ключ.|

При локализации статьи (переводе на другие языки) текст, имеющий стиль кода, не переводится. Если вы хотите предотвратить локализацию без использования стиля кода, см. раздел [Нелокализованные строки](markdown-reference.md#non-localized-strings).

### <a name="bold-style"></a>Полужирный стиль

В более старых руководствах по стилю для встроенного кода используется полужирный шрифт. Полужирный шрифт можно использовать, когда стиль кода настолько перегружен, что его трудно читать. Например, таблица Markdown со множеством элементов кода может выглядеть перегруженной, если везде применять стилизацию кода. Если выбрано использование полужирного начертания, используйте [синтаксис нелокализованных строк](markdown-reference.md#non-localized-strings), чтобы код не был локализован.

### <a name="links"></a>Создание ссылок

Ссылка на справочную документацию может оказаться более полезной, чем формат кода в некоторых контекстах. Если используется ссылка, не применяйте формат кода к тексту ссылки. Стилизация ссылки как кода может скрыть тот факт, что текст является ссылкой.

Если вы используете ссылку и ссылаетесь на тот же элемент позже в том же контексте, сделайте последующие экземпляры форматом кода, а не ссылками.

### <a name="placeholders"></a>Заполнители

Если требуется, чтобы пользователь заменил часть отображаемого кода собственными значениями, используйте текст заполнителя, заключенный в угловые или фигурные скобки. Например, `az group delete -n <ResourceGroupName>`. Объясните, что квадратные или фигурные скобки необходимо удалить при замене на реальные значения.

## <a name="code-blocks"></a>Блоки кода

Синтаксис для включения кода в документ зависит от того, где находится код:

* [в файле Markdown статьи](#inline-code-blocks);
* [в файле кода в том же репозитории](#in-repo-snippet-references);
* [в файле кода в другом репозитории](#out-of-repo-snippet-references).

Ниже приведены рекомендации, которые применяются для всех трех типов блоков кода:

* [автоматизируйте проверку кода](#code-validation);
* [выделяйте основные строки кода](#highlighting);
* [избегайте горизонтальных полос прокрутки](#horizontal-scroll-bars).

### <a name="screenshots"></a>Снимки экрана

Все методы, перечисленные в предыдущем разделе, приводят к созданию пригодных для использования блоков кода:

* Вы можете копировать их.
* Они индексируются поисковыми механизмами.
* Они доступны для средств чтения с экрана.

Это лишь несколько из причин, по которым снимки экрана IDE не рекомендуются в качестве метода включения кода в статью. Используйте снимки экрана IDE для кода только в том случае, если вы показываете что-то о самой среде IDE, например IntelliSense. Не используйте снимки экрана, только чтобы показать цвета и выделение.

### <a name="code-validation"></a>Проверка кода

В некоторых репозиториях реализованы процессы, которые автоматически компилируют все примеры кода для проверки на наличие ошибок. Это делается в репозитории .NET. Дополнительные сведения см. в разделе об [участии](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md) в репозитории .NET.

Если вы включаете блоки кода из другого репозитория, обсудите с владельцами стратегию обслуживания кода, чтобы включенный код не перестал работать и не устарел при обновлении версий библиотек, используемых кодом.

### <a name="highlighting"></a>Выделение

Фрагменты кода обычно содержат больше кода, чем необходимо для предоставления контекста. Чтобы улучшить читаемость, рекомендуется выделить ключевые строки, на которых нужно сконцентрировать внимание во фрагменте кода, как показано в следующем примере:

![Пример отображения выделенного кода](media/code-in-docs/highlighted-code.png)

Если код включен в файл Markdown статьи, его не удастся выделить. Выделение поддерживается только для фрагментов кода, включенных с помощью ссылки на файл кода.

### <a name="horizontal-scroll-bars"></a>Горизонтальные полосы прокрутки

Разбейте длинные строки, чтобы избежать горизонтальных полос прокрутки. Полосы прокрутки в блоках кода затрудняют его чтение. Это особенно проблематично в более длинных блоках кода, где невозможно одновременно показать полосу прокрутки и строку, которую необходимо прочитать.

Чтобы свести к минимуму горизонтальные полосы прокрутки в блоках кода, рекомендуется разбивать строки кода, длиннее 85 символов. Но помните, что присутствие или отсутствие полосы прокрутки не является единственным критерием удобочитаемости. Если разбивка длинной строки затрудняет чтение или удобство копирования и вставки, строка может быть длиннее 85 символов.

## <a name="inline-code-blocks"></a>Встроенные блоки кода

Используйте встроенные блоки кода, только когда непрактично отображать код по ссылке на файл кода. Как правило, встроенный код сложнее тестировать и обновлять по сравнению с файлом кода, который является частью полного проекта.  И встроенный код может опускать контекст, который может помочь разработчику понять и использовать код. Эти рекомендации относятся главным образом к языкам программирования. Встроенные блоки кода также могут использоваться для выходных и входных данных (например, JSON), языков запросов (таких как SQL) и языков сценариев (например, PowerShell).
  
Есть два способа обозначить, что раздел текста в файле статьи является блоком кода: *отделив* его тройными обратными кавычками (\`\`\`) или добавив отступ. Отделение является предпочтительным, так как в этом случае можно указать язык. Старайтесь не использовать отступы, потому что с ними просто ошибиться и другому автору будет сложно понять ваше намерение при редактировании статьи.

Языковые индикаторы размещаются сразу же после открытия тройных обратных кавычек, как в следующем примере:

Markdown:

```markdown
    ```json
    {
        "aggregator": {
            "batchSize": 1000,
            "flushTimeout": "00:00:30"
        }
    }
    ```
```

Отображение:

```json
{
    "aggregator": {
        "batchSize": 1000,
        "flushTimeout": "00:00:30"
    }
}
```

Дополнительные сведения о значениях, которые можно использовать в качестве индикаторов языка, см. в разделе [об именах и псевдонимах языков](http://highlightjs.readthedocs.io/en/latest/css-classes-reference.html#language-names-and-aliases).

Если вы используете слово языка или среды после тройных кавычек (\`\`\`), которые не поддерживаются, это слово отображается в заголовке раздела кода на отрисованной странице. По возможности используйте индикатор языка или среды во встроенных блоках кода.

> [!NOTE]
> При копировании и вставке кода из документа Word убедитесь, что в нем нет изогнутых кавычек, которые не являются допустимыми в коде (например, `“` и `’`). Если есть, замените их на обычные кавычки (`'` и `"`). В качестве альтернативы можно воспользоваться пакетом Docs Authoring Pack с [функцией замены парных кавычек](docs-authoring/smart-quote-replacement.md).

## <a name="in-repo-snippet-references"></a>Ссылки на фрагмент кода в репозитории

Предпочтительный способ включения фрагментов кода для языков программирования в документы — использование ссылки на файл кода. Этот метод позволяет выделить строки кода и предоставить больше контекста для фрагмента кода, доступного в GitHub для разработчиков. Код можно включить с помощью тройного двоеточия (:\:\:) вручную или в Visual Studio Code с помощью пакета [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).

1. Находясь в Visual Studio Code, нажмите клавиши <kbd>ALT+M</kbd> или <kbd>OPTION+M</kbd> и выберите "Фрагмент кода".
2. Вам будет предложено выполнить поиск по всему содержимому, в какой-то области или по различным репозиториям. Для локального поиска выберите полный поиск.
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

Отображение части файла кода путем указания имени фрагмента кода:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

В следующих разделах описаны эти примеры:

* [Использование относительного пути к файлу кода](#path-to-code-file)
* [Включение только выбранных номеров строк](#selected-line-numbers)
* [Использование ссылки на фрагмент кода с именем](#named-snippet)
* [Выделение выбранных строк](#highlighting-selected-lines)

Дополнительные сведения см. в разделе [Ссылки на синтаксис фрагментов кода](#snippet-syntax-reference) далее в этой статье.

### <a name="path-to-code-file"></a>Путь к файлу кода

Пример.

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

Пример взят из репозитория документов ASP.NET, файла статьи [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md). Для ссылки на файл кода используется относительный путь к [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) в том же репозитории.

### <a name="selected-line-numbers"></a>Выбранные номера строк

Пример.

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

В этом примере отображаются только строки 2–24 и 26 из файла кода *StudentController.cs*.

Предпочтительнее использовать именованные фрагменты кода, а не жестко заданные номера строк, как описано в следующем разделе.

### <a name="named-snippet"></a>Именованный фрагмент кода

Пример.

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

Используйте для имени только буквы и символы подчеркивания.

В примере отображается раздел `snippet_Create` файла кода. Файл кода для этого примера содержит теги фрагментов в комментариях в коде C#:

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

По возможности ссылайтесь на именованный раздел, а не указывайте номера строк. Ссылки на номера строк являются ненадежными, так как файлы кода неизбежно изменяются с помощью способов, которые изменяют номера строк.
Вы не обязательно получите уведомления об этих изменениях. В статье в конечном итоге будут отображаться неправильные строки, и вы даже не будете об этом знать.

### <a name="highlighting-selected-lines"></a>Выделение выбранных строк

Пример.

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

В примере выделены строки 2 и 5, если считать от начала отображаемого фрагмента кода. Подсчет выделяемых номеров строк не начинается от начала файла кода. Другими словами, выделяются строки 3 и 6 файла кода.

## <a name="out-of-repo-snippet-references"></a>Ссылки на фрагменты кода в другом репозитории

Если файл кода, на который необходимо сослаться, находится в другом репозитории, необходимо настроить репозиторий кода в качестве *зависимого репозитория*. При этом нужно указать его имя. Это имя затем выступает в качестве имени папки, используемого для ссылки на код.

Например, репозиторий документов — *Azure/azure-docs*, а репозиторий кода — *Azure/azure-functions-durable-extension*.

В корневой папке *azure-docs* добавьте следующий раздел в *.openpublishing.publish.config.json*:

```json
    {
      "path_to_root": "samples-durable-functions",
      "url": "https://github.com/Azure/azure-functions-durable-extension",
      "branch": "master",
      "branch_mapping": {}
    },
```

Теперь при добавлении ссылки на *sample-durable-functions*, как если бы это была папка в *azure-docs*, вы на самом деле ссылаетесь на корневую папку в репозитории *azure-functions-durable-extension*.

Код можно включить с помощью тройного двоеточия (:\:\:) вручную или в Visual Studio Code с помощью пакета [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).

1. Находясь в Visual Studio Code, нажмите клавиши <kbd>ALT+M</kbd> или <kbd>OPTION+M</kbd> и выберите "Фрагмент кода".
2. Вам будет предложено выполнить поиск по всему содержимому, в какой-то области или по различным репозиториям. Выберите поиск по репозиториям.
3. Вам будет представлен набор репозиториев из *.openpublishing.publish.config.json*. Выберите репозиторий.
4. Введите условие поиска и найдите нужный файл. Найдя файл, выберите его.
5. Затем выберите, какие строки кода нужно включить в фрагмент, используя следующие параметры: **ИД**, **Диапазон** или **Никакие**.
6. В зависимости от выбора на шаге 5 предоставьте значение.

Ссылка на фрагмент кода будет выглядеть следующим образом:

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

В репозитории *azure-functions-durable-extension* этот файл кода находится в папке *samples/csx/shared*. Как отмечалось [ранее](#highlighting-selected-lines), номера строк для выделения начинаются от начала фрагмента, а не от начала файла.

> [!NOTE]
> Имя, назначаемое зависимому репозиторию, указывается относительно корня основного репозитория, но тильда (~) относится к корню набора документов. Корень набора документов определяется `build_source_folder` в *.openpublishing.publish.config.json*. Путь к фрагменту кода в предыдущем примере работает в репозитории azure-docs, так как `build_source_folder` относится к корню репозитория (`.`). Если бы в качестве `build_source_folder` использовалось `articles`, путь начинался бы с `~/../samples-durable-functions`, а не с `~/samples-durable-functions`.

## <a name="interactive-code-snippets"></a>Интерактивные фрагменты кода

### <a name="inline-interactive-code-blocks"></a>Встроенные блоки интерактивного кода

Для следующих языков фрагменты кода можно сделать исполняемыми в окне браузера:

* Azure Cloud Shell
* Azure PowerShell Cloud Shell
* C# REPL

Если включен интерактивный режим, в отображаемых полях с кодом будут кнопки **Попробовать** или **Запустить**. Например:

```markdown
    ```azurepowershell-interactive
    New-AzResourceGroup -Name myResourceGroup -Location westeurope
    ```
```

отображается следующим образом:

```azurepowershell-interactive
New-AzResourceGroup -Name myResourceGroup -Location westeurope
```

Чтобы включить эту функцию для конкретного блока кода, используйте специальный идентификатор языка. Доступны следующие параметры:

* `azurepowershell-interactive` — активирует Cloud Shell в Azure PowerShell, как в предыдущем примере.
* `azurecli-interactive` — включает Azure Cloud Shell
* `csharp-interactive` — включает C# REPL

В Azure Cloud Shell и PowerShell Cloud Shell пользователи могут выполнять команды только с собственной учетной записью Azure.

### <a name="code-snippets-included-by-reference"></a>Фрагменты кода, включаемые по ссылке

Для фрагментов кода, включаемых по ссылке, можно включить интерактивный режим. Ниже приведены примеры:

```markdown
:::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code source="Bash.sh" interactive="cloudshell-bash":::
```

Чтобы включить эту функцию для конкретного блока кода, используйте атрибут `interactive`. Допустимые значения атрибута:

* `cloudshell-powershell` — активирует Cloud Shell в Azure PowerShell, как в предыдущем примере.
* `cloudshell-bash` — включает Azure Cloud Shell
* `try-dotnet` — активирует Try .NET.
* `try-dotnet-class` — активирует Try .NET с формированием шаблонов классов.
* `try-dotnet-method` — активирует Try .NET с формированием шаблонов методов.

В Azure Cloud Shell и PowerShell Cloud Shell пользователи могут выполнять команды только с собственной учетной записью Azure.

## <a name="snippet-syntax-reference"></a>Синтаксис ссылок на фрагменты

Синтаксис

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> Этот синтаксис является блоком расширения Markdown. Он должен использоваться в отдельной строке.

* `<language>` (*необязательно*)
  * Язык фрагмента кода. Дополнительные сведения см. в разделе [Поддерживаемые языки](#supported-languages) далее в этой статье.

* `<path>` (*обязательно*)
  * Относительный путь в файловой системе, который указывает файл фрагмента кода для ссылки.

* `<attribute>` и `<attribute-value>` (*необязательно*)
  * Используются вместе для указания способа получения кода из файла и его отображения:
    * `range`: `1,3-5` Диапазон строк. Этот пример содержит строки 1, 3, 4 и 5.
    * `id`: `snippet_Create` Идентификатор фрагмента, который нужно вставить из файла кода. Это значение не может существовать одновременно с диапазоном.
    * `highlight`: `2-4,6` Диапазон и (или) номера строк, которые должны выделяться в создаваемом фрагменте кода. Нумерация задается относительно отображаемых строк (в соответствии с диапазоном или идентификатором), а не файла.
    * `interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` Строковое значение, определяющее тип используемой интерактивности.
    * Сведения о представлении имени тега в исходных файлах фрагмента кода для каждого языка см. в разделе с [рекомендациями по DocFX](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).

## <a name="supported-languages"></a>Поддерживаемые языки

Пакет [Docs Authoring Pack](how-to-write-docs-auth-pack.md) содержит функцию, обеспечивающую завершение операторов и проверку доступных идентификаторов языков для блоков границ кода.

### <a name="fenced-code-blocks"></a>Огороженные блоки кода

| Имя                           | Допустимые псевдонимы                                                                  |
|--------------------------------|--------------------------------------------------------------------------------|
| .NET Core CLI                  | `dotnetcli`                                                                    |
| 1C                             | `1c`                                                                           |
| ABNF                           | `abnf`                                                                         |
| Журналы доступа                    | `accesslog`                                                                    |
| Ada                            | `ada`                                                                          |
| Ассемблер ARM                  | `armasm`, `arm`                                                                |
| Ассемблер AVR                  | `avrasm`                                                                       |
| ActionScript                   | `actionscript`, `as`                                                           |
| Alan                           | `alan`, `i`                                                                    |
| AngelScript                    | `angelscript`, `asc`                                                           |
| ANTLR                          | `antlr`                                                                        |
| Apache                         | `apache`, `apacheconf`                                                         |
| AppleScript                    | `applescript`, `osascript`                                                     |
| Arcade                         | `arcade`                                                                       |
| AsciiDoc                       | `asciidoc`, `adoc`                                                             |
| AspectJ                        | `aspectj`                                                                      |
| ASPX                           | `aspx`                                                                         |
| ASP.NET (C#)                   | `aspx-csharp`                                                                  |
| ASP.NET (VB)                   | `aspx-vb`                                                                      |
| AutoHotkey                     | `autohotkey`                                                                   |
| AutoIt                         | `autoit`                                                                       |
| Awk                            | `awk`, `mawk`, `nawk`, `gawk`                                                  |
| Axapta                         | `axapta`                                                                       |
| AzCopy                         | `azcopy`                                                                       |
| Azure CLI                      | `azurecli`                                                                     |
| Azure CLI (интерактивный)        | `azurecli-interactive`                                                         |
| Azure Powershell               | `azurepowershell`                                                              |
| Azure Powershell (интерактивный) | `azurepowershell-interactive`                                                  |
| Bash                           | `bash`, `sh`, `zsh`                                                            |
| Basic                          | `basic`                                                                        |
| BNF                            | `bnf`                                                                          |
| C                              | `c`                                                                            |
| C#                             | `csharp`, `cs`                                                                 |
| C# (интерактивный)               | `csharp-interactive`                                                           |
| C++                            | `cpp`, `c`, `cc`, `h`, `c++`, `h++`, `hpp`                                     |
| C++/CX                         | `cppcx`                                                                        |
| C++/WinRT                      | `cppwinrt`                                                                     |
| C/AL                           | `cal`                                                                          |
| Cache Object Script            | `cos`, `cls`                                                                   |
| CMake                          | `cmake`, `cmake.in`                                                            |
| Coq                            | `coq`                                                                          |
| CSP                            | `csp`                                                                          |
| CSS                            | `css`                                                                          |
| Cap'n Proto                    | `capnproto`, `capnp`                                                           |
| Clojure                        | `clojure`, `clj`                                                               |
| CoffeeScript                   | `coffeescript`, `coffee`, `cson`, `iced`                                       |
| Crmsh                          | `crmsh`, `crm`, `pcmk`                                                         |
| Crystal                        | `crystal`, `cr`                                                                |
| Cypher (Neo4j)                 | `cypher`                                                                       |
| D                              | `d`                                                                            |
| DAX Power BI                   | `dax`                                                                          |
| Файл зоны DNS                  | `dns`, `zone`, `bind`                                                          |
| DOS                            | `dos`, `bat`, `cmd`                                                            |
| Dart                           | `dart`                                                                         |
| Delphi                         | `delphi`, `dpr`, `dfm`, `pas`, `pascal`, `freepascal`, `lazarus`, `lpr`, `lfm` |
| Diff                           | `diff`, `patch`                                                                |
| Django                         | `django`, `jinja`                                                              |
| Dockerfile                     | `dockerfile`, `docker`                                                         |
| dsconfig                       | `dsconfig`                                                                     |
| DTS (дерево устройств)              | `dts`                                                                          |
| Dust                           | `dust`, `dst`                                                                  |
| Dylan                          | `dylan`                                                                        |
| EBNF                           | `ebnf`                                                                         |
| Elixir                         | `elixir`                                                                       |
| Elm                            | `elm`                                                                          |
| Erlang                         | `erlang`, `erl`                                                                |
| Excel                          | `excel`, `xls`, `xlsx`                                                         |
| Extempore                      | `extempore`, `xtlang`, `xtm`                                                   |
| F#                             | `fsharp`, `fs`                                                                 |
| FIX                            | `fix`                                                                          |
| Fortran                        | `fortran`, `f90`, `f95`                                                        |
| G-Code                         | `gcode`, `nc`                                                                  |
| Gams                           | `gams`, `gms`                                                                  |
| GAUSS                          | `gauss`, `gss`                                                                 |
| GDScript                       | `godot`, `gdscript`                                                            |
| Gherkin                        | `gherkin`                                                                      |
| GN for Ninja                   | `gn`, `gni`                                                                    |
| Go                             | `go`, `golang`                                                                 |
| Golo                           | `golo`, `gololang`                                                             |
| Gradle                         | `gradle`                                                                       |
| Groovy                         | `groovy`                                                                       |
| HTML                           | `html`, `xhtml`                                                                |
| HTTP                           | `http`, `https`                                                                |
| Haml                           | `haml`                                                                         |
| Handlebars                     | `handlebars`, `hbs`, `html.hbs`, `html.handlebars`                             |
| Haskell                        | `haskell`, `hs`                                                                |
| Haxe                           | `haxe`, `hx`                                                                   |
| Hy                             | `hy`, `hylang`                                                                 |
| Ini                            | `ini`                                                                          |
| Inform7                        | `inform7`, `i7`                                                                |
| IRPF90                         | `irpf90`                                                                       |
| JSON                           | `json`                                                                         |
| Java                           | `java`, `jsp`                                                                  |
| JavaScript                     | `javascript`, `js`, `jsx`                                                      |
| Kotlin                         | `kotlin`, `kt`                                                                 |
| Kusto                          | `kusto`                                                                        |
| Leaf                           | `leaf`                                                                         |
| Lasso                          | `lasso`, `ls`, `lassoscript`                                                   |
| Less                           | `less`                                                                         |
| LDIF                           | `ldif`                                                                         |
| Lisp                           | `lisp`                                                                         |
| LiveCode Server                | `livecodeserver`                                                               |
| LiveScript                     | `livescript`, `ls`                                                             |
| Lua                            | `lua`                                                                          |
| Makefile                       | `makefile`, `mk`, `mak`                                                        |
| Markdown                       | `markdown`, `md`, `mkdown`, `mkd`                                              |
| Mathematica                    | `mathematica`, `mma`, `wl`                                                     |
| Matlab                         | `matlab`                                                                       |
| Maxima                         | `maxima`                                                                       |
| Maya Embedded Language         | `mel`                                                                          |
| Mercury                        | `mercury`                                                                      |
| Язык сценариев mIRC        | `mirc`, `mrc`                                                                  |
| Mizar                          | `mizar`                                                                        |
| MOF          | `mof`                                                                          |
| Mojolicious                    | `mojolicious`                                                                  |
| Monkey                         | `monkey`                                                                       |
| Moonscript                     | `moonscript`, `moon`                                                           |
| MS Graph (интерактивный)         | `msgraph-interactive`                                                          |
| N1QL                           | `n1ql`                                                                         |
| NSIS                           | `nsis`                                                                         |
| Nginx                          | `nginx`, `nginxconf`                                                           |
| Nimrod                         | `nimrod`, `nim`                                                                |
| Nix                            | `nix`                                                                          |
| OCaml                          | `ocaml`, `ml`                                                                  |
| Objective C                    | `objectivec`, `mm`, `objc`, `obj-c`                                            |
| OpenGL Shading Language        | `glsl`                                                                         |
| OpenSCAD                       | `openscad`, `scad`                                                             |
| Язык правил Oracle          | `ruleslanguage`                                                                |
| Oxygene                        | `oxygene`                                                                      |
| PF                             | `pf`, `pf.conf`                                                                |
| PHP                            | `php`, `php3`, `php4`, `php5`, `php6`                                          |
| Parser3                        | `parser3`                                                                      |
| Perl                           | `perl`, `pl`, `pm`                                                             |
| Обычный текст без выделения         | `plaintext`                                                                    |
| Pony                           | `pony`                                                                         |
| PostgreSQL и PL/pgSQL          | `pgsql`, `postgres`, `postgresql`                                              |
| PowerShell                     | `powershell`, `ps`                                                             |
| PowerShell (интерактивный)       | `powershell-interactive`                                                       |
| Обработка                     | `processing`                                                                   |
| Prolog                         | `prolog`                                                                       |
| Свойства                     | `properties`                                                                   |
| Буферы протоколов               | `protobuf`                                                                     |
| Puppet                         | `puppet`, `pp`                                                                 |
| Python                         | `python`, `py`, `gyp`                                                          |
| Результаты профилировщика Python        | `profile`                                                                      |
| Q#                             | `qsharp`                                                                       |
| Q                              | `k`, `kdb`                                                                     |
| QML                            | `qml`                                                                          |
| R                              | `r`                                                                            |
| Razor CSHTML                   | `cshtml`, `razor`, `razor-cshtml`                                              |
| ReasonML                       | `reasonml`, `re`                                                               |
| RenderMan RIB                  | `rib`                                                                          |
| RenderMan RSL                  | `rsl`                                                                          |
| Roboconf                       | `graph`, `instances`                                                           |
| Robot Framework                | `robot`, `rf`                                                                  |
| Файлы спецификаций RPM                 | `rpm-specfile`, `rpm`, `spec`, `rpm-spec`, `specfile`                          |
| Ruby                           | `ruby`, `rb`, `gemspec`, `podspec`, `thor`, `irb`                              |
| Rust                           | `rust`, `rs`                                                                   |
| SAS                            | `SAS`, `sas`                                                                   |
| SCSS                           | `scss`                                                                         |
| SQL                            | `sql`                                                                          |
| STEP Part 21                   | `p21`, `step`, `stp`                                                           |
| Scala                          | `scala`                                                                        |
| Схема                         | `scheme`                                                                       |
| Scilab                         | `scilab`, `sci`                                                                |
| Выражения фигуры              | `shexc`                                                                        |
| Оболочка                          | `shell`, `console`                                                             |
| Smali                          | `smali`                                                                        |
| Smalltalk                      | `smalltalk`, `st`                                                              |
| Solidity                       | `solidity`, `sol`                                                              |
| Stan                           | `stan`                                                                         |
| Stata                          | `stata`                                                                        |
| Структурированный текст                | `iecst`, `scl`, `stl`, `structured-text`                                       |
| Stylus                         | `stylus`, `styl`                                                               |
| SubUnit                        | `subunit`                                                                      |
| Supercollider                  | `supercollider`, `sc`                                                          |
| Swift                          | `swift`                                                                        |
| Tcl                            | `tcl`, `tk`                                                                    |
| Terraform (HCL)                | `terraform`, `tf`, `hcl`                                                       |
| Test Anything Protocol         | `tap`                                                                          |
| TeX                            | `tex`                                                                          |
| Thrift                         | `thrift`                                                                       |
| TOML                           | `toml`                                                                         |
| TP                             | `tp`                                                                           |
| Twig                           | `twig`, `craftcms`                                                             |
| TypeScript                     | `typescript`, `ts`                                                             |
| VB.NET                         | `vbnet`, `vb`                                                                  |
| VBScript                       | `vbscript`, `vbs`                                                              |
| VHDL                           | `vhdl`                                                                         |
| Vala                           | `vala`                                                                         |
| Verilog                        | `verilog`, `v`                                                                 |
| Скрипт Vim                     | `vim`                                                                          |
| X++                            | `xpp`                                                                          |
| Сборка x86                   | `x86asm`                                                                       |
| XL                             | `xl`, `tao`                                                                    |
| XQuery                         | `xquery`, `xpath`, `xq`                                                        |
| XAML                           | `xaml`                                                                         |
| XML                            | `xml`, `xhtml`, `rss`, `atom`, `xjb`, `xsd`, `xsl`, `plist`                    |
| YAML                           | `yml`, `yaml`                                                                  |
| Zephir                         | `zephir`, `zep`                                                                |

> [!TIP]
> При наличии нескольких псевдонимов в пакете Docs Authoring Pack [функции завершения языка разработки](docs-authoring/dev-lang-completion.md) используется первый допустимый псевдоним.

## <a name="next-steps"></a>Дальнейшие действия

Сведения о форматировании текста для типов содержимого, отличных от кода, см. в разделе [Рекомендации по форматированию текста](text-formatting-guidelines.md).
