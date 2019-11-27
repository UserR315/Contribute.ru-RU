---
title: h1-empty
description: Объяснение проблемы со сборкой документов h1-empty и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: d0b3ab2206d66ff68a967d7868353b5b399da80a
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528791"
---
# <a name="h1-empty"></a>h1-empty

## <a name="warning"></a>Предупреждение

`H1 is required. Add content to your top-level heading.`

H1 — это первый заголовок в файле Markdown. При публикации на веб-сайте docs.microsoft.com заголовок H1 отображается крупным шрифтом в верхней части страницы. Для создания заголовка H1 необходимо указать в начале строки один символ решетки (#), после которого следует пробел и текст заголовка.

## <a name="resolution"></a>Способы устранения

Чтобы устранить эту проблему, убедитесь в том, что, помимо символа решетки, заголовок H1 также включает в себя содержимое.

Неверно:

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

Верно:

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
