---
title: multiple-h1
description: Объяснение проблемы со сборкой документов multiple-h1 и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 55ce6260cb4d1e09f63e0540528576ed3fa165f8
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427900"
---
# <a name="multiple-h1"></a>multiple-h1

## <a name="warning"></a>Предупреждение

`Multiple H1s are not allowed. You can only have one top-level heading.`

H1 — это первый заголовок в файле Markdown. При публикации на веб-сайте docs.microsoft.com заголовок H1 отображается крупным шрифтом в верхней части страницы. Для создания заголовка H1 необходимо указать в начале строки один символ решетки (#), после которого следует пробел и текст заголовка. В каждом файле может быть только один заголовок H1.

## <a name="resolution"></a>Способы устранения

Чтобы устранить эту проблему, измените уровень последующих заголовков H1 на H2 (`##`) либо реорганизуйте файл. Обратите внимание на то, что пропускать уровни заголовков, например указывать H3 сразу после H1, запрещено.

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]