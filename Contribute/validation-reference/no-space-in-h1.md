---
title: no-space-in-h1
description: Объяснение проблемы со сборкой документов issue no-space-in-h1 и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 8c719a89e6373fb960f216a5b4ec01c6d1739a28
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427843"
---
# <a name="no-space-in-h1"></a>no-space-in-h1

## <a name="warning"></a>Предупреждение

`A space is required after the hash (#) in H1.`

H1 — это первый заголовок в файле Markdown. При публикации на веб-сайте docs.microsoft.com заголовок H1 отображается крупным шрифтом в верхней части страницы. Для создания заголовка H1 необходимо указать в начале строки один символ решетки (#), после которого следует пробел и текст заголовка. Без пробела после символа решетки заголовок H1 не будет распознаваться на веб-сайте документации.

## <a name="resolution"></a>Способы устранения

Чтобы устранить эту ошибку, добавьте в заголовке H1 пробел после символа решетки.

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]