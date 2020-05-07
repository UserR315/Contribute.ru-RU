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
# <a name="sort-selection"></a>Сортировка выделенных фрагментов

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Резюме

В файле Markdown ( *\*MD*) после выбора фрагмента теперь доступны два элемента контекстного меню сортировки. Чтобы открыть контекстное меню, щелкните правой кнопкой мыши выбранный текст. Вы увидите нечто похожее на следующие пункты меню.

:::image type="content" source="media/sort-selection-menu.png" alt-text="Контекстное меню сортировки выделенных фрагментов":::

> [!TIP]
> Элементы контекстного меню сортировки скрыты, если не выбран допустимый фрагмент в текстовом редакторе Visual Studio Code.

## <a name="sort-selection-ascending-a-to-z"></a>Сортировка выделенного фрагмента по возрастанию (от А до Я)

Если выбрать параметр **Сортировка выделенного фрагмента по возрастанию (от А до Я)** , весь выделенный фрагмент будет отсортирован по возрастанию в алфавитном порядке от А до Я.

## <a name="sort-selection-descending-z-to-a"></a>Сортировка выделенного фрагмента по убыванию (от Я до А)

Если выбрать параметр **Сортировка выделенного фрагмента по убыванию (от Я до А)** , весь выделенный фрагмент будет отсортирован по убыванию в алфавитном порядке от Я до А.

## <a name="considerations"></a>Рекомендации

Базовый механизм сортировки использует *естественный язык*. Благодаря этому он является более эффективным и комплексным, чем стандартная сортировка. Рассмотрим следующую таблицу.

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

Без использования сортировки на естественном языке порядок для `Column1` был бы 1, 11, 2 и т. д., но вместо этого механизм понимает, что 11 больше 2, что приводит к следующему порядку по возрастанию:

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

## <a name="in-action"></a>В действии

Ниже приведена краткая демонстрация этой функции.

[![Демонстрация сортировки выделенных фрагментов](media/sort-selection.gif)](media/sort-selection.gif#lightbox)
