---
title: Переформатирование таблиц Markdown — Docs Authoring Pack
description: Узнайте, как использовать различные функции форматирования таблиц Markdown в Docs Authoring Pack — расширении Visual Studio Code.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 07c95f2a0d24a49f59eaffe1bec64ee872530c2f
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336780"
---
# <a name="reformat-markdown-tables"></a><span data-ttu-id="c1ea6-103">Переформатирование таблиц Markdown</span><span class="sxs-lookup"><span data-stu-id="c1ea6-103">Reformat Markdown tables</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="c1ea6-104">Резюме</span><span class="sxs-lookup"><span data-stu-id="c1ea6-104">Summary</span></span>

<span data-ttu-id="c1ea6-105">В файле Markdown ( *\*MD*) при выборе всей таблицы теперь доступно два элемента контекстного меню форматирования.</span><span class="sxs-lookup"><span data-stu-id="c1ea6-105">In a Markdown (*\*.md*) file, when you select a complete table - two table formatting context menu items are now available.</span></span> <span data-ttu-id="c1ea6-106">Чтобы открыть контекстное меню, щелкните правой кнопкой мыши выбранную таблицу Markdown.</span><span class="sxs-lookup"><span data-stu-id="c1ea6-106">Right-click on the selected Markdown table to open the context menu.</span></span> <span data-ttu-id="c1ea6-107">Вы увидите нечто похожее на следующие пункты меню.</span><span class="sxs-lookup"><span data-stu-id="c1ea6-107">You will see something similar to the following menu items:</span></span>

:::image type="content" source="media/reformat-table-menu.png" alt-text="Контекстное меню переформатирования таблиц":::

> [!TIP]
> <span data-ttu-id="c1ea6-109">Эта функция **не** работает с несколькими выбранными таблицами, а предназначена для одной таблицы Markdown.</span><span class="sxs-lookup"><span data-stu-id="c1ea6-109">This feature **does not** work with multiple table selections, but rather is intended for a single Markdown table.</span></span> <span data-ttu-id="c1ea6-110">Необходимо выбрать всю таблицу, включая заголовки, для нужных результатов.</span><span class="sxs-lookup"><span data-stu-id="c1ea6-110">You must select the entire table, including headings for desired results.</span></span>

## <a name="consolidate-selected-table"></a><span data-ttu-id="c1ea6-111">Консолидация выбранной таблицы</span><span class="sxs-lookup"><span data-stu-id="c1ea6-111">Consolidate selected table</span></span>

<span data-ttu-id="c1ea6-112">Если выбрать параметр **Консолидация выбранной таблицы**, заголовки и содержимое таблицы будут свернуты и останется только по одному пробелу по обе стороны от каждого значения.</span><span class="sxs-lookup"><span data-stu-id="c1ea6-112">Selecting the **Consolidate selected table** option will collapse the table headings and contents with only a single space on either side of each value.</span></span>

## <a name="evenly-distribute-selected-table"></a><span data-ttu-id="c1ea6-113">Равномерное распределение выбранной таблицы</span><span class="sxs-lookup"><span data-stu-id="c1ea6-113">Evenly distribute selected table</span></span>

<span data-ttu-id="c1ea6-114">Если выбрать параметр **Равномерное распределение выбранной таблицы**, будет рассчитано наибольшее значение в каждом столбце и равномерно распределены все остальные значения в соответствии со свободным пространством.</span><span class="sxs-lookup"><span data-stu-id="c1ea6-114">Selecting the **Evenly distribute selected table** option will calculate the longest value in each column and evenly distribute all the other values accordingly with space.</span></span>

## <a name="considerations"></a><span data-ttu-id="c1ea6-115">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="c1ea6-115">Considerations</span></span>

<span data-ttu-id="c1ea6-116">Эта функция не влияет на отрисовку таблицы, но позволяет улучшить ее удобочитаемость, упрощая ее обслуживание.</span><span class="sxs-lookup"><span data-stu-id="c1ea6-116">The feature will not impact the rendering of the table, but it will help to improve the readability of the table - thus making more maintainable.</span></span> <span data-ttu-id="c1ea6-117">Функция переформатирования таблицы сохранит выравнивание столбцов неизменным.</span><span class="sxs-lookup"><span data-stu-id="c1ea6-117">The reformatting table feature will keep column alignment intact.</span></span>

<span data-ttu-id="c1ea6-118">Рассмотрим следующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="c1ea6-118">Consider the following table:</span></span>

```markdown
| Column1 | This is a long column name | Column3 |  |
|--:|---------|:--:|:----|
||         |  |         |
|     |  |         |   a value      |
||         |         |         |
|     |         | This is a long value |       but why? |
|     |         |         |         |
|     |                                           |         | Here is something |
|  |         |   |         |
```

<span data-ttu-id="c1ea6-119">После равномерного распределения:</span><span class="sxs-lookup"><span data-stu-id="c1ea6-119">After being "evenly distributed":</span></span>

```markdown
| Column1 | This is a long column name | Column3              |                   |
|--------:|----------------------------|:--------------------:|:------------------|
|         |                            |                      |                   |
|         |                            |                      | a value           |
|         |                            |                      |                   |
|         |                            | This is a long value | but why?          |
|         |                            |                      |                   |
|         |                            |                      | Here is something |
|         |                            |                      |                   |
```

<span data-ttu-id="c1ea6-120">После консолидации:</span><span class="sxs-lookup"><span data-stu-id="c1ea6-120">After being "consolidated":</span></span>

```markdown
| Column1 | This is a long column name | Column3 |  |
|-:|--|:-:|:-|
|  |  |  |  |
|  |  |  | a value |
|  |  |  |  |
|  |  | This is a long value | but why? |
|  |  |  |  |
|  |  |  | Here is something |
|  |  |  |  |
```

## <a name="in-action"></a><span data-ttu-id="c1ea6-121">В действии</span><span class="sxs-lookup"><span data-stu-id="c1ea6-121">In action</span></span>

<span data-ttu-id="c1ea6-122">Ниже приведена краткая демонстрация этой функции.</span><span class="sxs-lookup"><span data-stu-id="c1ea6-122">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="c1ea6-123">[![Демонстрация переформатирования таблиц](media/reformat-table.gif)](media/reformat-table.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="c1ea6-123">[![Reformat table demo](media/reformat-table.gif)](media/reformat-table.gif#lightbox)</span></span>
