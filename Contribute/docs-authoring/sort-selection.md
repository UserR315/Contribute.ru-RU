---
title: Сортировка выделенных фрагментов — Docs Authoring Pack
description: Узнайте, как использовать функцию сортировки выделенных фрагментов в Docs Authoring Pack — расширении Visual Studio Code.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: b4bd1761dc1bd9326275f011bb1935f6b695404d
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336757"
---
# <a name="sort-selection"></a><span data-ttu-id="5f535-103">Сортировка выделенных фрагментов</span><span class="sxs-lookup"><span data-stu-id="5f535-103">Sort selection</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="5f535-104">Резюме</span><span class="sxs-lookup"><span data-stu-id="5f535-104">Summary</span></span>

<span data-ttu-id="5f535-105">В файле Markdown ( *\*MD*) после выбора фрагмента теперь доступны два элемента контекстного меню сортировки.</span><span class="sxs-lookup"><span data-stu-id="5f535-105">In a Markdown (*\*.md*) file, when you've made a selection - two sorting context menu items are now available.</span></span> <span data-ttu-id="5f535-106">Чтобы открыть контекстное меню, щелкните правой кнопкой мыши выбранный текст.</span><span class="sxs-lookup"><span data-stu-id="5f535-106">Right-click on the selected text to open the context menu.</span></span> <span data-ttu-id="5f535-107">Вы увидите нечто похожее на следующие пункты меню.</span><span class="sxs-lookup"><span data-stu-id="5f535-107">You will see something similar to the following menu items:</span></span>

:::image type="content" source="media/sort-selection-menu.png" alt-text="Контекстное меню сортировки выделенных фрагментов":::

> [!TIP]
> <span data-ttu-id="5f535-109">Элементы контекстного меню сортировки скрыты, если не выбран допустимый фрагмент в текстовом редакторе Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="5f535-109">The sorting context menu items are hidden until there is a valid selection in the Visual Studio Code text editor.</span></span>

## <a name="sort-selection-ascending-a-to-z"></a><span data-ttu-id="5f535-110">Сортировка выделенного фрагмента по возрастанию (от А до Я)</span><span class="sxs-lookup"><span data-stu-id="5f535-110">Sort selection ascending (A to Z)</span></span>

<span data-ttu-id="5f535-111">Если выбрать параметр **Сортировка выделенного фрагмента по возрастанию (от А до Я)** , весь выделенный фрагмент будет отсортирован по возрастанию в алфавитном порядке от А до Я.</span><span class="sxs-lookup"><span data-stu-id="5f535-111">Selecting the **Sort selection ascending (A to Z)** option will sort the entire selection ascending, alphabetically from A to Z.</span></span>

## <a name="sort-selection-descending-z-to-a"></a><span data-ttu-id="5f535-112">Сортировка выделенного фрагмента по убыванию (от Я до А)</span><span class="sxs-lookup"><span data-stu-id="5f535-112">Sort selection descending (Z to A)</span></span>

<span data-ttu-id="5f535-113">Если выбрать параметр **Сортировка выделенного фрагмента по убыванию (от Я до А)** , весь выделенный фрагмент будет отсортирован по убыванию в алфавитном порядке от Я до А.</span><span class="sxs-lookup"><span data-stu-id="5f535-113">Selecting the **Sort selection descending (Z to A)** option will sort the entire selection ascending, alphabetically from Z to A.</span></span>

## <a name="considerations"></a><span data-ttu-id="5f535-114">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="5f535-114">Considerations</span></span>

<span data-ttu-id="5f535-115">Базовый механизм сортировки использует *естественный язык*.</span><span class="sxs-lookup"><span data-stu-id="5f535-115">The underlying sorting mechanism uses *natural language* sorting.</span></span> <span data-ttu-id="5f535-116">Благодаря этому он является более эффективным и комплексным, чем стандартная сортировка.</span><span class="sxs-lookup"><span data-stu-id="5f535-116">This makes it more powerful and comprehensive than standard sorting.</span></span> <span data-ttu-id="5f535-117">Рассмотрим следующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="5f535-117">Consider the following table:</span></span>

```markdown
| Column1 | Column2                                |
|---------|----------------------------------------|
| 1       | Number 1                               |
| Aa      | The first letter in the alphabet       |
| Ab      | The first letter in the alphabet       |
| C       | The a letter after A in the alphabet   |
| M       | Somewhere in the middle?               |
| 2       | Number 2                               |
| X       | The alphabet letter is towards the end |
| Z       | The last letter in the alphabet        |
| 11      | Number 11                              |
```

<span data-ttu-id="5f535-118">Без использования сортировки на естественном языке порядок для `Column1` был бы 1, 11, 2 и т. д., но вместо этого механизм понимает, что 11 больше 2, что приводит к следующему порядку по возрастанию:</span><span class="sxs-lookup"><span data-stu-id="5f535-118">Without natural language sorting, the order for `Column1` would have been 1, 11, 2, etc. but instead it understands that 11 is greater than 2 - resulting in the following ascending order:</span></span>

```markdown
| Column1 | Column2                                |
|---------|----------------------------------------|
| 1       | Number 1                               |
| 2       | Number 2                               |
| 11      | Number 11                              |
| Aa      | The first letter in the alphabet       |
| Ab      | The first letter in the alphabet       |
| C       | The a letter after A in the alphabet   |
| M       | Somewhere in the middle?               |
| X       | The alphabet letter is towards the end |
| Z       | The last letter in the alphabet        |
```

## <a name="in-action"></a><span data-ttu-id="5f535-119">В действии</span><span class="sxs-lookup"><span data-stu-id="5f535-119">In action</span></span>

<span data-ttu-id="5f535-120">Ниже приведена краткая демонстрация этой функции.</span><span class="sxs-lookup"><span data-stu-id="5f535-120">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="5f535-121">[![Демонстрация сортировки выделенных фрагментов](media/sort-selection.gif)](media/sort-selection.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="5f535-121">[![Sort selection demo](media/sort-selection.gif)](media/sort-selection.gif#lightbox)</span></span>
