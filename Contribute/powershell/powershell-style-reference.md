---
title: Рекомендации по написанию справки по командлетам
description: В этой статье приводятся правила, касающиеся форматирования примеров кода PowerShell. Они относятся как к концептуальным статьям с примерами, так и к справке по командлетам.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 793a3c02ae0edf192416ae514585d5161e8c1f98
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290295"
---
# <a name="updating-reference-articles"></a>Обновление справочных статей

Справочные статьи по командлетам имеют определенную структуру. Она определяется модулем [PlatyPS][].
PlatyPS — это средство, используемое для создания справки по командлетам для модулей PowerShell. PlatyPS создает базовый файл Markdown для командлета. После редактирования файлов Markdown с помощью PlatyPS создаются MAML-файлы справки, используемые командлетом `Get-Help`.

В коде PlatyPS жестко задана схема для справки по командлетам. Ее описание можно найти в файле [platyPS.schema.md][]. Нарушения схемы приводят к ошибкам сборки, которые необходимо исправить, иначе ваше содержимое не будет принято.

## <a name="general-guidelines"></a>Общие рекомендации

- Не удаляйте заголовки. PlatyPS требует определенного набора заголовков.
- Под заголовками **Input type** (Тип входных данных) и **Output type** (Тип выходных данных) должен быть указан тип. Если командлет не принимает входные данные или не возвращает значение, используйте значение None (Нет).
- Огражденные блоки кода допускаются только в разделе [Examples](#format-for-examples) (Примеры).
- Встроенные фрагменты кода можно использовать в любом абзаце.

## <a name="formatting-about_-files"></a>Форматирование файлов About_

Файлы `About_*` теперь обрабатываются средством [Pandoc][], в не PlatyPS. Файлы `About_*` форматируются так, чтобы они были максимально совместимы со всеми версиями PowerShell и средствами публикации.
Не изменяйте форматирование файлов `about_*` без согласования с командой сопровождения репозитория.

Основные рекомендации по форматированию:

- Ограничьте длину строк 80 символами.
- Длина строк в блоках кода, фрагментах кода и таблицах ограничена 76 символами, так как при преобразовании средством Pandoc они получают отступ в четыре пробела.
- Ширина таблиц должна быть не более 76 символов.
  - Переносите содержимое ячеек по строкам вручную.
  - Используйте открывающие и закрывающие символы `|` в каждой строке.
  - Рабочий пример см. в разделе [about_Comparison_Operators][about-example].
- Использование специальных символов Pandoc `\`,`$`,`` ` `` и `<`:
  - в заголовке эти символы должны быть экранированы с помощью начального символа `\`;
  - в абзаце эти символы должны включаться во фрагменты кода. Например:

    ~~~markdown
    ### The purpose of the \$foo variable

    The `$foo` variable is used to store ...
    ~~~

## <a name="format-for-examples"></a>Формат для примеров

В схеме PlatyPS заголовок **EXAMPLES** (Примеры) имеет уровень H2, а заголовок каждого примера — уровень H3.

Внутри примера схема не позволяет разделять блоки кода абзацами. Допустимая схема:

```
### Example #X title

0 or more paragraphs
1 or more code blocks
0 or more paragraphs.
```

Пронумеруйте все примеры и снабдите их краткими заголовками.

Например:

~~~markdown
### Example 1: Get cmdlets, functions, and aliases

This example gets the PowerShell cmdlets, functions, and aliases that are installed on the
computer.

```powershell
Get-Command
```
~~~


[PlatyPS]: https://github.com/powershell/platyps
[platyPS.schema.md]: https://github.com/PowerShell/platyPS/blob/master/platyPS.schema.md
[issue1806]: https://github.com/PowerShell/PowerShell-Docs/issues/1806
[about-example]: https://github.com/MicrosoftDocs/PowerShell-Docs/blob/staging/reference/6/Microsoft.PowerShell.Core/About/about_Comparison_Operators.md
[Pandoc]: https://pandoc.org