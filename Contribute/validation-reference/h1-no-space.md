---
title: h1-no-space
description: Объяснение и решение проблемы со сборкой документов h1-no-space.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 7dd6a3d5cfc6def000d5bf7a5bf7810a16625cae
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2019
ms.locfileid: "70856250"
---
# <a name="h1-no-space"></a>h1-no-space

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Предложение

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
