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
# <a name="formatting-code-samples"></a><span data-ttu-id="c86df-104">Форматирование примеров кода</span><span class="sxs-lookup"><span data-stu-id="c86df-104">Formatting code samples</span></span>

<span data-ttu-id="c86df-105">Правила форматирования со временем менялись, поэтому в существующей документации используются различные стили.</span><span class="sxs-lookup"><span data-stu-id="c86df-105">The existing documentation has used multiple styles, over time, and the formatting rules have changed multiple times.</span></span> <span data-ttu-id="c86df-106">Мы пытаемся привести блоки кода и выходные данные PowerShell в нашей документации к единому стилю.</span><span class="sxs-lookup"><span data-stu-id="c86df-106">We are trying to establish a consistent style for PowerShell code blocks and output in our documentation.</span></span>

<span data-ttu-id="c86df-107">Markdown поддерживает два разных стиля кода.</span><span class="sxs-lookup"><span data-stu-id="c86df-107">Markdown supports two different code styles:</span></span>

- <span data-ttu-id="c86df-108">Фрагменты кода (в тексте) — помечаются одинарным грависом (`` ` ``).</span><span class="sxs-lookup"><span data-stu-id="c86df-108">Code spans (inline) - marked by a single backtick (`` ` ``) character.</span></span> <span data-ttu-id="c86df-109">Используются внутри абзацев, а не как отдельные блоки.</span><span class="sxs-lookup"><span data-stu-id="c86df-109">Used inline in a paragraph rather than as a standalone block.</span></span> <span data-ttu-id="c86df-110">Чаще всего применяются с именами командлетов.</span><span class="sxs-lookup"><span data-stu-id="c86df-110">Most commonly used around cmdlet names.</span></span> <span data-ttu-id="c86df-111">См. раздел [Форматирование элементов синтаксиса команд](powershell-style-basic-markdown.md#formatting-command-syntax-elements).</span><span class="sxs-lookup"><span data-stu-id="c86df-111">See [Formatting command syntax elements](powershell-style-basic-markdown.md#formatting-command-syntax-elements).</span></span>
- <span data-ttu-id="c86df-112">Блоки кода — многострочные блоки, заключенные в строки из трех грависов (`` ``` ``).</span><span class="sxs-lookup"><span data-stu-id="c86df-112">Code blocks - a multi-line block surrounded by triple-backtick (`` ``` ``) strings.</span></span>

## <a name="using-code-blocks"></a><span data-ttu-id="c86df-113">Использование блоков кода</span><span class="sxs-lookup"><span data-stu-id="c86df-113">Using code blocks</span></span>

<span data-ttu-id="c86df-114">Markdown позволяет обозначать блоки кода отступами, но такой способ может создавать проблемы, и его следует избегать.</span><span class="sxs-lookup"><span data-stu-id="c86df-114">Markdown allows for indentation to signify a code block, but this pattern can be problematic and should be avoided.</span></span> <span data-ttu-id="c86df-115">Блоки кода следует ограждать.</span><span class="sxs-lookup"><span data-stu-id="c86df-115">All code blocks should be contained in a code fence.</span></span> <span data-ttu-id="c86df-116">Огражденный код — это блок кода, заключенный в строки из трех грависов (`` ``` ``).</span><span class="sxs-lookup"><span data-stu-id="c86df-116">A code fence is a block of code surrounded by triple-backtick (`` ``` ``) strings.</span></span> <span data-ttu-id="c86df-117">Маркеры границ кода должны находиться в отдельных строках до и после примера кода.</span><span class="sxs-lookup"><span data-stu-id="c86df-117">The code fence markers must be on their own line before and after the code sample.</span></span> <span data-ttu-id="c86df-118">Маркер в начале блока может иметь метку языка (необязательно).</span><span class="sxs-lookup"><span data-stu-id="c86df-118">The marker at the start of the code block may have an optional language label.</span></span> <span data-ttu-id="c86df-119">Открытая система публикации Майкрософт (OPS) использует метку языка для поддержки функции выделения синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="c86df-119">Microsoft's Open Publishing System (OPS) uses the language label to support the syntax highlighting feature.</span></span>

<span data-ttu-id="c86df-120">OPS также добавляет кнопку **Копировать**, при нажатии которой содержимое блока кода копируется в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="c86df-120">OPS also adds a **Copy** button that copies the contents of the code block to the clipboard.</span></span> <span data-ttu-id="c86df-121">Это позволяет быстро вставить код в скрипт для тестирования примера.</span><span class="sxs-lookup"><span data-stu-id="c86df-121">This allows you to quickly paste the code into a script for testing the code example.</span></span> <span data-ttu-id="c86df-122">Однако не все примеры в нашей документации предназначены для выполнения.</span><span class="sxs-lookup"><span data-stu-id="c86df-122">However, not all examples in our documentation are intended to be run that way.</span></span> <span data-ttu-id="c86df-123">Некоторые блоки кода могут просто иллюстрировать какой-либо принцип работы PowerShell или правило синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="c86df-123">Some code blocks may be a simple illustration of a PowerShell concept or an abstract representation of syntax.</span></span>

<span data-ttu-id="c86df-124">В нашей документации используются два типа блоков кода:</span><span class="sxs-lookup"><span data-stu-id="c86df-124">There are two types code blocks used in our documentation:</span></span>

1. <span data-ttu-id="c86df-125">пояснительные примеры;</span><span class="sxs-lookup"><span data-stu-id="c86df-125">Illustrative examples</span></span>
2. <span data-ttu-id="c86df-126">исполняемые примеры.</span><span class="sxs-lookup"><span data-stu-id="c86df-126">Executable examples</span></span>

## <a name="formatting-illustrative-examples"></a><span data-ttu-id="c86df-127">Форматирование пояснительных примеров</span><span class="sxs-lookup"><span data-stu-id="c86df-127">Formatting illustrative examples</span></span>

<span data-ttu-id="c86df-128">Пояснительные примеры служат для иллюстрации какого-либо аспекта PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c86df-128">Illustrative examples are used to explain a PowerShell concept.</span></span> <span data-ttu-id="c86df-129">Они не предназначены для копирования в буфер обмена с целью выполнения.</span><span class="sxs-lookup"><span data-stu-id="c86df-129">They are not meant to be copied to the clipboard for execution.</span></span> <span data-ttu-id="c86df-130">Чаще всего это простые примеры, которые легко вводить.</span><span class="sxs-lookup"><span data-stu-id="c86df-130">These are most commonly used for simple examples that are easy to type.</span></span>
<span data-ttu-id="c86df-131">Кроме того, они используются для иллюстрации синтаксиса команд.</span><span class="sxs-lookup"><span data-stu-id="c86df-131">They are also used for syntax examples where you are illustrating the syntax of a command.</span></span>

<span data-ttu-id="c86df-132">В пояснительных примерах начало и конец блока кода обозначаются маркерами границ без дополнительных меток.</span><span class="sxs-lookup"><span data-stu-id="c86df-132">Illustrative examples use a "naked" code fence to mark the beginning and end of the code block.</span></span> <span data-ttu-id="c86df-133">Блок кода может содержать пример выходных данных иллюстрируемой команды.</span><span class="sxs-lookup"><span data-stu-id="c86df-133">The code block may contain example output from the command being illustrated.</span></span>

### <a name="syntax-block"></a><span data-ttu-id="c86df-134">Блок синтаксиса</span><span class="sxs-lookup"><span data-stu-id="c86df-134">Syntax block</span></span>

<span data-ttu-id="c86df-135">В этом примере представлены все возможные параметры командлета `Get-Command`.</span><span class="sxs-lookup"><span data-stu-id="c86df-135">This example illustrates all the possible parameters of the `Get-Command` cmdlet.</span></span>

~~~markdown
```
Get-Command [-Verb <String[]>] [-Noun <String[]>] [-Module <String[]>]
  [-FullyQualifiedModule <ModuleSpecification[]>] [-TotalCount <Int32>] [-Syntax] [-ShowCommandInfo]
  [[-ArgumentList] <Object[]>] [-All] [-ListImported] [-ParameterName <String[]>]
  [-ParameterType <PSTypeName[]>] [<CommonParameters>]
```
~~~

<span data-ttu-id="c86df-136">В этом примере представлена общая форма оператора `for`:</span><span class="sxs-lookup"><span data-stu-id="c86df-136">This example describes the `for` statement in generalized terms:</span></span>

~~~markdown
```
for (<init>; <condition>; <repeat>)
{<statement list>}
```
~~~

### <a name="simple-illustration-example"></a><span data-ttu-id="c86df-137">Простой пояснительный пример</span><span class="sxs-lookup"><span data-stu-id="c86df-137">Simple illustration example</span></span>

<span data-ttu-id="c86df-138">Вот пример представления операторов сравнения в PowerShell:</span><span class="sxs-lookup"><span data-stu-id="c86df-138">Here is an example illustrating PowerShell comparison operators:</span></span>

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

<span data-ttu-id="c86df-139">Обратите внимание, что в нем показана упрощенная командная строка PowerShell и полученные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="c86df-139">Note that this example has the simplified PowerShell prompt and shows the resulting output.</span></span> <span data-ttu-id="c86df-140">Этот пример не предусматривает копирование и выполнение читателем.</span><span class="sxs-lookup"><span data-stu-id="c86df-140">In this case, we don't intend the reader to copy and run this example.</span></span>

## <a name="formatting-executable-examples"></a><span data-ttu-id="c86df-141">Форматирование исполняемых примеров</span><span class="sxs-lookup"><span data-stu-id="c86df-141">Formatting executable examples</span></span>

<span data-ttu-id="c86df-142">В более сложных примерах или примерах, предназначенных для копирования и выполнения, должна использоваться следующая разметка блока:</span><span class="sxs-lookup"><span data-stu-id="c86df-142">More complex examples or examples that are intended to be useful to copy and execute should use the following block-style markup:</span></span>

~~~markdown
```powershell
<PowerShell code goes here>
```
~~~

<span data-ttu-id="c86df-143">Выходные данные команд PowerShell должны выноситься в отдельные блоки кода с меткой **Output**, чтобы не происходило выделение синтаксических конструкций.</span><span class="sxs-lookup"><span data-stu-id="c86df-143">The output displayed by PowerShell commands should be enclosed in an **Output** code block to prevent syntax highlighting.</span></span> <span data-ttu-id="c86df-144">Например:</span><span class="sxs-lookup"><span data-stu-id="c86df-144">For example:</span></span>

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

<span data-ttu-id="c86df-145">Метка кода **Output** не обозначает какой-либо язык, поддерживаемый системой выделения синтаксических конструкций.</span><span class="sxs-lookup"><span data-stu-id="c86df-145">The **Output** code label is not an official "language" supported by the syntax highlighting system.</span></span>
<span data-ttu-id="c86df-146">Однако она полезна, так как OPS добавляет метку Output в поле кода на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="c86df-146">However, this label is useful because OPS adds the "Output" label to the code box on the web page.</span></span>
<span data-ttu-id="c86df-147">В поле кода с меткой Output синтаксические конструкции не выделяются.</span><span class="sxs-lookup"><span data-stu-id="c86df-147">And this "Output" code box has no syntax highlighting.</span></span>

## <a name="coding-style-rules"></a><span data-ttu-id="c86df-148">Правила в отношении стиля оформления кода</span><span class="sxs-lookup"><span data-stu-id="c86df-148">Coding style rules</span></span>

### <a name="avoid-line-continuation-in-code-samples"></a><span data-ttu-id="c86df-149">Избегайте продолжения строк в примерах кода</span><span class="sxs-lookup"><span data-stu-id="c86df-149">Avoid line continuation in code samples</span></span>

<span data-ttu-id="c86df-150">Старайтесь не использовать символы продолжения строки (`` ` ``) в примерах кода PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c86df-150">Avoid using line continuation characters (`` ` ``) in PowerShell code examples.</span></span> <span data-ttu-id="c86df-151">Они малозаметны, а лишние пробелы в конце строки могут вызвать проблемы.</span><span class="sxs-lookup"><span data-stu-id="c86df-151">These are hard to see and can cause problems if there are extra spaces at the end of the line.</span></span>

- <span data-ttu-id="c86df-152">Чтобы сократить длину строк для командлетов с большим количеством параметров, используйте сплаттинг PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c86df-152">Use PowerShell splatting to reduce line length for cmdlets that have a lot of parameters.</span></span>
- <span data-ttu-id="c86df-153">Используйте разрывы строк там, где они естественны в PowerShell, например после символа вертикальной черты (`|`), открывающих фигурных скобок, кавычек и квадратных скобок.</span><span class="sxs-lookup"><span data-stu-id="c86df-153">Take advantage of PowerShell's natural line break opportunities, like after pipe (`|`) characters, opening braces, parentheses, and brackets.</span></span>

### <a name="avoid-using-powershell-prompts-in-examples"></a><span data-ttu-id="c86df-154">Избегайте использования приглашения командной строки PowerShell в примерах</span><span class="sxs-lookup"><span data-stu-id="c86df-154">Avoid using PowerShell prompts in examples</span></span>

<span data-ttu-id="c86df-155">Использовать строку приглашения не рекомендуется, кроме случаев, когда необходимо проиллюстрировать работу с командной строкой.</span><span class="sxs-lookup"><span data-stu-id="c86df-155">Use of the prompt string is discouraged and should be limited to scenarios that are meant to illustrate command line usage.</span></span> <span data-ttu-id="c86df-156">Приглашения требуются, если в примере иллюстрируется команда, которая изменяет строку приглашения, или если важен отображаемый путь.</span><span class="sxs-lookup"><span data-stu-id="c86df-156">Prompts are required for examples that illustrate commands that alter the prompt or when the path displayed is significant to the scenario being illustrated.</span></span>

- <span data-ttu-id="c86df-157">Приглашения командной строки PowerShell следует использовать только в пояснительных примерах.</span><span class="sxs-lookup"><span data-stu-id="c86df-157">PowerShell prompts should only be used in illustrative examples.</span></span> <span data-ttu-id="c86df-158">В большинстве таких примеров строка приглашения должна иметь вид "`PS>`".</span><span class="sxs-lookup"><span data-stu-id="c86df-158">For most of these examples, the prompt string should be "`PS>`".</span></span> <span data-ttu-id="c86df-159">Она не зависит от меток ОС.</span><span class="sxs-lookup"><span data-stu-id="c86df-159">This prompt is independent of OS-specific indicators.</span></span>
- <span data-ttu-id="c86df-160">Приглашения **не следует** использовать в исполняемых примерах.</span><span class="sxs-lookup"><span data-stu-id="c86df-160">Prompts should **NOT** be used in executable examples.</span></span>

<span data-ttu-id="c86df-161">В приведенном ниже примере демонстрируется, как меняется строка приглашения при использовании поставщика реестра.</span><span class="sxs-lookup"><span data-stu-id="c86df-161">The following example illustrates how the prompt changes when using the Registry provider.</span></span>

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

### <a name="do-not-use-aliases-in-examples"></a><span data-ttu-id="c86df-162">Не используйте псевдонимы в примерах</span><span class="sxs-lookup"><span data-stu-id="c86df-162">Do not use aliases in examples</span></span>

<span data-ttu-id="c86df-163">Всегда используйте полные имена всех командлетов и параметров, если только речь не идет именно о псевдонимах.</span><span class="sxs-lookup"><span data-stu-id="c86df-163">You should always use the full name of all cmdlets and parameters unless you are specifically talking about the alias.</span></span> <span data-ttu-id="c86df-164">Для имен командлетов и параметров должно применяться правильное написание в стиле Pascal, определенное в коде.</span><span class="sxs-lookup"><span data-stu-id="c86df-164">Cmdlet and parameter names must use the proper Pascal-case spelling defined in the code.</span></span>

### <a name="using-parameters-in-examples"></a><span data-ttu-id="c86df-165">Использование параметров в примерах</span><span class="sxs-lookup"><span data-stu-id="c86df-165">Using parameters in examples</span></span>

<span data-ttu-id="c86df-166">Избегайте использования позиционных параметров.</span><span class="sxs-lookup"><span data-stu-id="c86df-166">Avoid using positional parameters.</span></span> <span data-ttu-id="c86df-167">В общем случае в пример всегда следует включать имя параметра, даже если он позиционный.</span><span class="sxs-lookup"><span data-stu-id="c86df-167">In general, you should use always include the parameter name in an example, even if the parameter positional.</span></span> <span data-ttu-id="c86df-168">Это снижает вероятность возникновения путаницы.</span><span class="sxs-lookup"><span data-stu-id="c86df-168">This reduces the chance of confusion in your examples.</span></span>
