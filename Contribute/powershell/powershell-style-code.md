---
title: Рекомендации по написанию примеров скриптов
description: В этой статье приводятся правила, касающиеся форматирования примеров кода PowerShell. Они относятся как к концептуальным статьям с примерами, так и к справке по командлетам.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: f036ece21d139df0be1d677dc536023910c9d20b
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290272"
---
# <a name="formatting-code-samples"></a>Форматирование примеров кода

Правила форматирования со временем менялись, поэтому в существующей документации используются различные стили. Мы пытаемся привести блоки кода и выходные данные PowerShell в нашей документации к единому стилю.

Markdown поддерживает два разных стиля кода.

- Фрагменты кода (в тексте) — помечаются одинарным грависом (`` ` ``). Используются внутри абзацев, а не как отдельные блоки. Чаще всего применяются с именами командлетов. См. раздел [Форматирование элементов синтаксиса команд](powershell-style-basic-markdown.md#formatting-command-syntax-elements).
- Блоки кода — многострочные блоки, заключенные в строки из трех грависов (`` ``` ``).

## <a name="using-code-blocks"></a>Использование блоков кода

Markdown позволяет обозначать блоки кода отступами, но такой способ может создавать проблемы, и его следует избегать. Блоки кода следует ограждать. Огражденный код — это блок кода, заключенный в строки из трех грависов (`` ``` ``). Маркеры границ кода должны находиться в отдельных строках до и после примера кода. Маркер в начале блока может иметь метку языка (необязательно). Открытая система публикации Майкрософт (OPS) использует метку языка для поддержки функции выделения синтаксиса.

OPS также добавляет кнопку **Копировать**, при нажатии которой содержимое блока кода копируется в буфер обмена. Это позволяет быстро вставить код в скрипт для тестирования примера. Однако не все примеры в нашей документации предназначены для выполнения. Некоторые блоки кода могут просто иллюстрировать какой-либо принцип работы PowerShell или правило синтаксиса.

В нашей документации используются два типа блоков кода:

1. пояснительные примеры;
2. исполняемые примеры.

## <a name="formatting-illustrative-examples"></a>Форматирование пояснительных примеров

Пояснительные примеры служат для иллюстрации какого-либо аспекта PowerShell. Они не предназначены для копирования в буфер обмена с целью выполнения. Чаще всего это простые примеры, которые легко вводить.
Кроме того, они используются для иллюстрации синтаксиса команд.

В пояснительных примерах начало и конец блока кода обозначаются маркерами границ без дополнительных меток. Блок кода может содержать пример выходных данных иллюстрируемой команды.

### <a name="syntax-block"></a>Блок синтаксиса

В этом примере представлены все возможные параметры командлета `Get-Command`.

~~~markdown
```
Get-Command [-Verb <String[]>] [-Noun <String[]>] [-Module <String[]>]
  [-FullyQualifiedModule <ModuleSpecification[]>] [-TotalCount <Int32>] [-Syntax] [-ShowCommandInfo]
  [[-ArgumentList] <Object[]>] [-All] [-ListImported] [-ParameterName <String[]>]
  [-ParameterType <PSTypeName[]>] [<CommonParameters>]
```
~~~

В этом примере представлена общая форма оператора `for`:

~~~markdown
```
for (<init>; <condition>; <repeat>)
{<statement list>}
```
~~~

### <a name="simple-illustration-example"></a>Простой пояснительный пример

Вот пример представления операторов сравнения в PowerShell:

~~~markdown
```
PS> 2 -eq 2
True

PS> 2 -eq 3
False

PS>  1,2,3 -eq 2
2

PS> "abc" -eq "abc"
True

PS> "abc" -eq "abc", "def"
False

PS> "abc", "def" -eq "abc"
abc
```
~~~

Обратите внимание, что в нем показана упрощенная командная строка PowerShell и полученные выходные данные. Этот пример не предусматривает копирование и выполнение читателем.

## <a name="formatting-executable-examples"></a>Форматирование исполняемых примеров

В более сложных примерах или примерах, предназначенных для копирования и выполнения, должна использоваться следующая разметка блока:

~~~markdown
```powershell
<PowerShell code goes here>
```
~~~

Выходные данные команд PowerShell должны выноситься в отдельные блоки кода с меткой **Output**, чтобы не происходило выделение синтаксических конструкций. Например:

~~~markdown
```powershell
Get-Command -Module Microsoft.PowerShell.Security
```

```Output
CommandType  Name                        Version    Source
-----------  ----                        -------    ------
Cmdlet       ConvertFrom-SecureString    3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       ConvertTo-SecureString      3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-Acl                     3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-AuthenticodeSignature   3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-CmsMessage              3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-Credential              3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-ExecutionPolicy         3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-PfxCertificate          3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       New-FileCatalog             3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Protect-CmsMessage          3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-Acl                     3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-AuthenticodeSignature   3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-ExecutionPolicy         3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Test-FileCatalog            3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Unprotect-CmsMessage        3.0.0.0    Microsoft.PowerShell.Security
```
~~~

Метка кода **Output** не обозначает какой-либо язык, поддерживаемый системой выделения синтаксических конструкций.
Однако она полезна, так как OPS добавляет метку Output в поле кода на веб-странице.
В поле кода с меткой Output синтаксические конструкции не выделяются.

## <a name="coding-style-rules"></a>Правила в отношении стиля оформления кода

### <a name="avoid-line-continuation-in-code-samples"></a>Избегайте продолжения строк в примерах кода

Старайтесь не использовать символы продолжения строки (`` ` ``) в примерах кода PowerShell. Они малозаметны, а лишние пробелы в конце строки могут вызвать проблемы.

- Чтобы сократить длину строк для командлетов с большим количеством параметров, используйте сплаттинг PowerShell.
- Используйте разрывы строк там, где они естественны в PowerShell, например после символа вертикальной черты (`|`), открывающих фигурных скобок, кавычек и квадратных скобок.

### <a name="avoid-using-powershell-prompts-in-examples"></a>Избегайте использования приглашения командной строки PowerShell в примерах

Использовать строку приглашения не рекомендуется, кроме случаев, когда необходимо проиллюстрировать работу с командной строкой. Приглашения требуются, если в примере иллюстрируется команда, которая изменяет строку приглашения, или если важен отображаемый путь.

- Приглашения командной строки PowerShell следует использовать только в пояснительных примерах. В большинстве таких примеров строка приглашения должна иметь вид "`PS>`". Она не зависит от меток ОС.
- Приглашения **не следует** использовать в исполняемых примерах.

В приведенном ниже примере демонстрируется, как меняется строка приглашения при использовании поставщика реестра.

```powershell
PS C:\> cd HKCU:\System\
PS HKCU:\System\> dir

    Hive: HKEY_CURRENT_USER\System

Name                   Property
----                   --------
CurrentControlSet
GameConfigStore        GameDVR_Enabled                       : 1
                       GameDVR_FSEBehaviorMode               : 2
                       Win32_AutoGameModeDefaultProfile      : {2, 0, 1, 0...}
                       Win32_GameModeRelatedProcesses        : {1, 0, 1, 0...}
                       GameDVR_HonorUserFSEBehaviorMode      : 0
                       GameDVR_DXGIHonorFSEWindowsCompatible : 0
```

### <a name="do-not-use-aliases-in-examples"></a>Не используйте псевдонимы в примерах

Всегда используйте полные имена всех командлетов и параметров, если только речь не идет именно о псевдонимах. Для имен командлетов и параметров должно применяться правильное написание в стиле Pascal, определенное в коде.

### <a name="using-parameters-in-examples"></a>Использование параметров в примерах

Избегайте использования позиционных параметров. В общем случае в пример всегда следует включать имя параметра, даже если он позиционный. Это снижает вероятность возникновения путаницы.
