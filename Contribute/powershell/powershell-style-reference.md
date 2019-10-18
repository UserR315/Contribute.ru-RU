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
# <a name="updating-reference-articles"></a><span data-ttu-id="d42e5-104">Обновление справочных статей</span><span class="sxs-lookup"><span data-stu-id="d42e5-104">Updating reference articles</span></span>

<span data-ttu-id="d42e5-105">Справочные статьи по командлетам имеют определенную структуру.</span><span class="sxs-lookup"><span data-stu-id="d42e5-105">Cmdlet reference articles have a specific structure.</span></span> <span data-ttu-id="d42e5-106">Она определяется модулем [PlatyPS][].</span><span class="sxs-lookup"><span data-stu-id="d42e5-106">This structure is defined by [PlatyPS][].</span></span>
<span data-ttu-id="d42e5-107">PlatyPS — это средство, используемое для создания справки по командлетам для модулей PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d42e5-107">PlatyPS is the tool we use to generate cmdlet help for PowerShell modules.</span></span> <span data-ttu-id="d42e5-108">PlatyPS создает базовый файл Markdown для командлета.</span><span class="sxs-lookup"><span data-stu-id="d42e5-108">PlatyPS creates the base Markdown file for a cmdlet.</span></span> <span data-ttu-id="d42e5-109">После редактирования файлов Markdown с помощью PlatyPS создаются MAML-файлы справки, используемые командлетом `Get-Help`.</span><span class="sxs-lookup"><span data-stu-id="d42e5-109">After editing the Markdown files, PlatyPS is used create the MAML help files used by the `Get-Help` cmdlet.</span></span>

<span data-ttu-id="d42e5-110">В коде PlatyPS жестко задана схема для справки по командлетам.</span><span class="sxs-lookup"><span data-stu-id="d42e5-110">PlatyPS has a hard-coded schema for cmdlet reference that is written into the code.</span></span> <span data-ttu-id="d42e5-111">Ее описание можно найти в файле [platyPS.schema.md][].</span><span class="sxs-lookup"><span data-stu-id="d42e5-111">The [platyPS.schema.md][] document attempts to describe this structure.</span></span> <span data-ttu-id="d42e5-112">Нарушения схемы приводят к ошибкам сборки, которые необходимо исправить, иначе ваше содержимое не будет принято.</span><span class="sxs-lookup"><span data-stu-id="d42e5-112">Schema violations cause build errors that must be fixed before we can accept your contribution.</span></span>

## <a name="general-guidelines"></a><span data-ttu-id="d42e5-113">Общие рекомендации</span><span class="sxs-lookup"><span data-stu-id="d42e5-113">General guidelines</span></span>

- <span data-ttu-id="d42e5-114">Не удаляйте заголовки.</span><span class="sxs-lookup"><span data-stu-id="d42e5-114">Do not remove any of the header structures.</span></span> <span data-ttu-id="d42e5-115">PlatyPS требует определенного набора заголовков.</span><span class="sxs-lookup"><span data-stu-id="d42e5-115">PlatyPS expects a specific set of headers.</span></span>
- <span data-ttu-id="d42e5-116">Под заголовками **Input type** (Тип входных данных) и **Output type** (Тип выходных данных) должен быть указан тип.</span><span class="sxs-lookup"><span data-stu-id="d42e5-116">The **Input type** and **Output type** headers must have a type.</span></span> <span data-ttu-id="d42e5-117">Если командлет не принимает входные данные или не возвращает значение, используйте значение None (Нет).</span><span class="sxs-lookup"><span data-stu-id="d42e5-117">If the cmdlet does not take input or return a value then use the value "None".</span></span>
- <span data-ttu-id="d42e5-118">Огражденные блоки кода допускаются только в разделе [Examples](#format-for-examples) (Примеры).</span><span class="sxs-lookup"><span data-stu-id="d42e5-118">Fenced code blocks are only allowed in the [Examples](#format-for-examples) section.</span></span>
- <span data-ttu-id="d42e5-119">Встроенные фрагменты кода можно использовать в любом абзаце.</span><span class="sxs-lookup"><span data-stu-id="d42e5-119">Inline code spans can be used in any paragraph.</span></span>

## <a name="formatting-about_-files"></a><span data-ttu-id="d42e5-120">Форматирование файлов About_</span><span class="sxs-lookup"><span data-stu-id="d42e5-120">Formatting About_ files</span></span>

<span data-ttu-id="d42e5-121">Файлы `About_*` теперь обрабатываются средством [Pandoc][], в не PlatyPS.</span><span class="sxs-lookup"><span data-stu-id="d42e5-121">`About_*` files are now processed by [Pandoc][], instead of PlatyPS.</span></span> <span data-ttu-id="d42e5-122">Файлы `About_*` форматируются так, чтобы они были максимально совместимы со всеми версиями PowerShell и средствами публикации.</span><span class="sxs-lookup"><span data-stu-id="d42e5-122">`About_*` files are formatted for the best compatibility across with all versions of PowerShell and with the publishing tools.</span></span>
<span data-ttu-id="d42e5-123">Не изменяйте форматирование файлов `about_*` без согласования с командой сопровождения репозитория.</span><span class="sxs-lookup"><span data-stu-id="d42e5-123">Please do not alter the formatting of `about_*` files without checking in with a repository maintainer.</span></span>

<span data-ttu-id="d42e5-124">Основные рекомендации по форматированию:</span><span class="sxs-lookup"><span data-stu-id="d42e5-124">Basic formatting guidelines:</span></span>

- <span data-ttu-id="d42e5-125">Ограничьте длину строк 80 символами.</span><span class="sxs-lookup"><span data-stu-id="d42e5-125">Limit lines to 80 characters</span></span>
- <span data-ttu-id="d42e5-126">Длина строк в блоках кода, фрагментах кода и таблицах ограничена 76 символами, так как при преобразовании средством Pandoc они получают отступ в четыре пробела.</span><span class="sxs-lookup"><span data-stu-id="d42e5-126">Code blocks, block quotes, and tables are limited to 76 characters because Pandoc indents these by four spaces during conversion</span></span>
- <span data-ttu-id="d42e5-127">Ширина таблиц должна быть не более 76 символов.</span><span class="sxs-lookup"><span data-stu-id="d42e5-127">Tables need fit within 76 characters</span></span>
  - <span data-ttu-id="d42e5-128">Переносите содержимое ячеек по строкам вручную.</span><span class="sxs-lookup"><span data-stu-id="d42e5-128">Manually wrap contents of cells across multiple lines</span></span>
  - <span data-ttu-id="d42e5-129">Используйте открывающие и закрывающие символы `|` в каждой строке.</span><span class="sxs-lookup"><span data-stu-id="d42e5-129">Use opening and closing `|` characters on each line</span></span>
  - <span data-ttu-id="d42e5-130">Рабочий пример см. в разделе [about_Comparison_Operators][about-example].</span><span class="sxs-lookup"><span data-stu-id="d42e5-130">See a working example in [about_Comparison_Operators][about-example]</span></span>
- <span data-ttu-id="d42e5-131">Использование специальных символов Pandoc `\`,`$`,`` ` `` и `<`:</span><span class="sxs-lookup"><span data-stu-id="d42e5-131">When using Pandoc's special characters `\`,`$`,`` ` ``, and `<`</span></span>
  - <span data-ttu-id="d42e5-132">в заголовке эти символы должны быть экранированы с помощью начального символа `\`;</span><span class="sxs-lookup"><span data-stu-id="d42e5-132">Within a header - these characters must be escaped using a leading `\` character</span></span>
  - <span data-ttu-id="d42e5-133">в абзаце эти символы должны включаться во фрагменты кода.</span><span class="sxs-lookup"><span data-stu-id="d42e5-133">Within a paragraph - these characters should be put into code spans.</span></span> <span data-ttu-id="d42e5-134">Например:</span><span class="sxs-lookup"><span data-stu-id="d42e5-134">For example:</span></span>

    ~~~markdown
    ### The purpose of the \$foo variable

    The `$foo` variable is used to store ...
    ~~~

## <a name="format-for-examples"></a><span data-ttu-id="d42e5-135">Формат для примеров</span><span class="sxs-lookup"><span data-stu-id="d42e5-135">Format for examples</span></span>

<span data-ttu-id="d42e5-136">В схеме PlatyPS заголовок **EXAMPLES** (Примеры) имеет уровень H2, а заголовок каждого примера — уровень H3.</span><span class="sxs-lookup"><span data-stu-id="d42e5-136">In the PlatyPS schema, the **EXAMPLES** header is an H2 header and each example is an H3 header.</span></span>

<span data-ttu-id="d42e5-137">Внутри примера схема не позволяет разделять блоки кода абзацами.</span><span class="sxs-lookup"><span data-stu-id="d42e5-137">Within an example, the schema does not allow code blocks to be separated by paragraphs.</span></span> <span data-ttu-id="d42e5-138">Допустимая схема:</span><span class="sxs-lookup"><span data-stu-id="d42e5-138">The valid schema is:</span></span>

```
### Example #X title

0 or more paragraphs
1 or more code blocks
0 or more paragraphs.
```

<span data-ttu-id="d42e5-139">Пронумеруйте все примеры и снабдите их краткими заголовками.</span><span class="sxs-lookup"><span data-stu-id="d42e5-139">Number each example and add a brief title.</span></span>

<span data-ttu-id="d42e5-140">Например:</span><span class="sxs-lookup"><span data-stu-id="d42e5-140">For example:</span></span>

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