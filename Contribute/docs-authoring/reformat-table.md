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
# <a name="reformat-markdown-tables"></a>Переформатирование таблиц Markdown

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Резюме

В файле Markdown ( *\*MD*) при выборе всей таблицы теперь доступно два элемента контекстного меню форматирования. Чтобы открыть контекстное меню, щелкните правой кнопкой мыши выбранную таблицу Markdown. Вы увидите нечто похожее на следующие пункты меню.

:::image type="content" source="media/reformat-table-menu.png" alt-text="Контекстное меню переформатирования таблиц":::

> [!TIP]
> Эта функция **не** работает с несколькими выбранными таблицами, а предназначена для одной таблицы Markdown. Необходимо выбрать всю таблицу, включая заголовки, для нужных результатов.

## <a name="consolidate-selected-table"></a>Консолидация выбранной таблицы

Если выбрать параметр **Консолидация выбранной таблицы**, заголовки и содержимое таблицы будут свернуты и останется только по одному пробелу по обе стороны от каждого значения.

## <a name="evenly-distribute-selected-table"></a>Равномерное распределение выбранной таблицы

Если выбрать параметр **Равномерное распределение выбранной таблицы**, будет рассчитано наибольшее значение в каждом столбце и равномерно распределены все остальные значения в соответствии со свободным пространством.

## <a name="considerations"></a>Рекомендации

Эта функция не влияет на отрисовку таблицы, но позволяет улучшить ее удобочитаемость, упрощая ее обслуживание. Функция переформатирования таблицы сохранит выравнивание столбцов неизменным.

Рассмотрим следующую таблицу.

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

После равномерного распределения:

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

После консолидации:

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

## <a name="in-action"></a>В действии

Ниже приведена краткая демонстрация этой функции.

[![Демонстрация переформатирования таблиц](media/reformat-table.gif)](media/reformat-table.gif#lightbox)
