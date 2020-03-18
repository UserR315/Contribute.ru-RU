---
title: Выполнение языка разработки — Docs Authoring Pack
description: Узнайте о том, как выполнение языка разработки в Docs Authoring Pack, расширении Visual Studio Code, помогает участникам.
author: scottaddie
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: scaddie
ms.openlocfilehash: f81dc2315dc09256639c98ed72484517ff2c6ff3
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336803"
---
# <a name="dev-lang-completion"></a><span data-ttu-id="a643f-103">Выполнение языка разработки</span><span class="sxs-lookup"><span data-stu-id="a643f-103">Dev lang completion</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="a643f-104">Сводка</span><span class="sxs-lookup"><span data-stu-id="a643f-104">Summary</span></span>

<span data-ttu-id="a643f-105">Участникам необходима помощь в определении допустимых идентификаторов языков (языков разработки), которые могут следовать за тройными кавычками (начало ограждения кода) в файле Markdown.</span><span class="sxs-lookup"><span data-stu-id="a643f-105">Contributors need assistance determining the valid language identifiers (dev langs) that can follow triple-backticks (code fence openings) in a Markdown file.</span></span> <span data-ttu-id="a643f-106">К сожалению, проверки языков разработки во время сборки не существует.</span><span class="sxs-lookup"><span data-stu-id="a643f-106">Unfortunately, build-time validation of dev langs doesn't exist.</span></span> <span data-ttu-id="a643f-107">В результате появляются разнородные представления одного языка в рамках одного набора документации.</span><span class="sxs-lookup"><span data-stu-id="a643f-107">The result is disparate representations of a single language within the same conceptual docset.</span></span>

<span data-ttu-id="a643f-108">Рассмотрим C# в качестве примера.</span><span class="sxs-lookup"><span data-stu-id="a643f-108">Consider C# as an example.</span></span> <span data-ttu-id="a643f-109">Участники использовали `c#`, `C#`, `cs`, `csharp` и др. в качестве представлений языка разработки.</span><span class="sxs-lookup"><span data-stu-id="a643f-109">Contributors have used `c#`, `C#`, `cs`, `csharp`, and others as dev lang representations of the language.</span></span> <span data-ttu-id="a643f-110">Какое из предыдущих представлений является правильным?</span><span class="sxs-lookup"><span data-stu-id="a643f-110">Which of the preceding representations is correct?</span></span>

<span data-ttu-id="a643f-111">Функция *Выполнение языка разработки* устраняет путаницу, показывая список известных языков разработки.</span><span class="sxs-lookup"><span data-stu-id="a643f-111">The *Dev lang completion* feature dispels the confusion by displaying a list of known dev langs.</span></span> <span data-ttu-id="a643f-112">После выбора имени языка разработки в IntelliSense</span><span class="sxs-lookup"><span data-stu-id="a643f-112">Upon selecting a dev lang name from IntelliSense:</span></span>

* <span data-ttu-id="a643f-113">Ограждение кода закрывается.</span><span class="sxs-lookup"><span data-stu-id="a643f-113">The code fence is closed.</span></span>
* <span data-ttu-id="a643f-114">Курсор размещается в ограждении кода.</span><span class="sxs-lookup"><span data-stu-id="a643f-114">The caret is positioned in the code fence.</span></span>

## <a name="preferences"></a><span data-ttu-id="a643f-115">Настройки</span><span class="sxs-lookup"><span data-stu-id="a643f-115">Preferences</span></span>

<span data-ttu-id="a643f-116">Отключить эту функцию невозможно.</span><span class="sxs-lookup"><span data-stu-id="a643f-116">It's not possible to disable this feature.</span></span> <span data-ttu-id="a643f-117">Доступны следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="a643f-117">The following settings are available:</span></span>

* [<span data-ttu-id="a643f-118">Отображение часто используемых языков разработки</span><span class="sxs-lookup"><span data-stu-id="a643f-118">Display commonly used dev langs</span></span>](#display-commonly-used-dev-langs)
* [<span data-ttu-id="a643f-119">Отображение всех известных языков разработки</span><span class="sxs-lookup"><span data-stu-id="a643f-119">Display all known dev langs</span></span>](#display-all-known-dev-langs)

### <a name="display-commonly-used-dev-langs"></a><span data-ttu-id="a643f-120">Отображение часто используемых языков разработки</span><span class="sxs-lookup"><span data-stu-id="a643f-120">Display commonly used dev langs</span></span>

<span data-ttu-id="a643f-121">В одном наборе документов будет использоваться только подмножество допустимых языков разработки.</span><span class="sxs-lookup"><span data-stu-id="a643f-121">Only a subset of the valid dev langs will be used in a single docset.</span></span> <span data-ttu-id="a643f-122">Чтобы улучшить взаимодействие с пользователем, сделайте следующее.</span><span class="sxs-lookup"><span data-stu-id="a643f-122">To enhance the user experience:</span></span>

1. <span data-ttu-id="a643f-123">В Visual Studio Code откройте набор документов в корневом каталоге.</span><span class="sxs-lookup"><span data-stu-id="a643f-123">In Visual Studio Code, open the docset to the root directory.</span></span>
1. <span data-ttu-id="a643f-124">Выберите **Файл** > **Настройки** > **Параметры** и выберите фильтр *Расширение Docs Markdown*.</span><span class="sxs-lookup"><span data-stu-id="a643f-124">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="a643f-125">Щелкните ссылку **Изменить в settings.json** в разделе **Markdown: языки набора документации**.</span><span class="sxs-lookup"><span data-stu-id="a643f-125">Click the **Edit in settings.json** link in the **Markdown: Docset Languages** section.</span></span>
1. <span data-ttu-id="a643f-126">Добавьте следующее свойство `markdown.docsetLanguages` в файл *settings.json*:</span><span class="sxs-lookup"><span data-stu-id="a643f-126">Add the following `markdown.docsetLanguages` property to the *settings.json* file:</span></span>

    ```json
    {
        "markdown.docsetLanguages": [

        ]
    }
    ```

1. <span data-ttu-id="a643f-127">Поместите курсор в пустой массив свойства и активируйте IntelliSense (нажав <kbd>CTRL</kbd> + <kbd>ПРОБЕЛ</kbd>).</span><span class="sxs-lookup"><span data-stu-id="a643f-127">Position your caret in the property's empty array, and activate IntelliSense (via <kbd>Ctrl</kbd> + <kbd>Space</kbd>).</span></span> <span data-ttu-id="a643f-128">Появится список известных имен языков разработки.</span><span class="sxs-lookup"><span data-stu-id="a643f-128">A list of known dev lang names appears.</span></span>
1. <span data-ttu-id="a643f-129">Добавьте необходимые имена языков разработки в массив.</span><span class="sxs-lookup"><span data-stu-id="a643f-129">Add dev lang names to the array until you're satisfied with the list.</span></span> <span data-ttu-id="a643f-130">Например, в следующем списке для пользователя будут показаны четыре имени языка разработки после ввода тройных кавычек:</span><span class="sxs-lookup"><span data-stu-id="a643f-130">For example, the following list will display four dev lang names to the user after typing triple-ticks:</span></span>

    ```json
    {
        "markdown.docsetLanguages": [
            ".NET Core CLI",
            "C#",
            "Markdown",
            "YAML"
        ]
    }
    ```

1. <span data-ttu-id="a643f-131">Сохраните изменения в файле *settings.json*.</span><span class="sxs-lookup"><span data-stu-id="a643f-131">Save your changes to the *settings.json* file.</span></span>

> [!WARNING]
> <span data-ttu-id="a643f-132">Пустой массив `markdown.docsetLanguages` вызывает отображение всех известных языков разработки.</span><span class="sxs-lookup"><span data-stu-id="a643f-132">An empty `markdown.docsetLanguages` array causes all known dev langs to display.</span></span>

### <a name="display-all-known-dev-langs"></a><span data-ttu-id="a643f-133">Отображение всех известных языков разработки</span><span class="sxs-lookup"><span data-stu-id="a643f-133">Display all known dev langs</span></span>

<span data-ttu-id="a643f-134">По умолчанию в IntelliSense отображаются все известные имена языков разработки.</span><span class="sxs-lookup"><span data-stu-id="a643f-134">By default, all known dev lang names are displayed in IntelliSense.</span></span> <span data-ttu-id="a643f-135">Этот параметр переопределяет свойство `markdown.docsetLanguages`, описанное в разделе [Отображение часто используемых языков разработки](#display-commonly-used-dev-langs).</span><span class="sxs-lookup"><span data-stu-id="a643f-135">This setting overrides the `markdown.docsetLanguages` property described in [Display commonly used dev langs](#display-commonly-used-dev-langs).</span></span>

<span data-ttu-id="a643f-136">Чтобы изменить этот параметр, сделайте следующее.</span><span class="sxs-lookup"><span data-stu-id="a643f-136">To change this setting:</span></span>

1. <span data-ttu-id="a643f-137">Выберите **Файл** > **Настройки** > **Параметры** и выберите фильтр *Расширение Docs Markdown*.</span><span class="sxs-lookup"><span data-stu-id="a643f-137">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="a643f-138">Включите параметр в разделе **Markdown: все доступные языки**.</span><span class="sxs-lookup"><span data-stu-id="a643f-138">Toggle the setting in the **Markdown: All Available Languages** section.</span></span>

## <a name="in-action"></a><span data-ttu-id="a643f-139">В действии</span><span class="sxs-lookup"><span data-stu-id="a643f-139">In action</span></span>

<span data-ttu-id="a643f-140">Ниже приведена краткая демонстрация этой функции.</span><span class="sxs-lookup"><span data-stu-id="a643f-140">Below is a brief demonstration of this feature:</span></span>

<span data-ttu-id="a643f-141">[![Выполнение языка разработки](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="a643f-141">[![Dev lang completion](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)</span></span>
