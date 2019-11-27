---
title: h1-no-space
description: Объяснение и решение проблемы со сборкой документов h1-no-space.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7058367a6edd7f663ea42a4fc2e9fafd9cbfb34f
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528962"
---
# <a name="h1-no-space"></a>h1-no-space

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
