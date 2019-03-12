---
title: manager-missing
description: Объяснение проблемы со сборкой документов manager-missing и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 16da241a21d400d5a5dfb101e247e55d95567485
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427823"
---
# <a name="manager-missing"></a>manager-missing

**Ожидается в ближайшее время.**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Предложение

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

Для определения руководителя автора в некоторых группах содержимого требуется атрибут `manager`.

## <a name="resolution"></a>Способы устранения

Добавьте допустимый псевдоним Майкрософт в качестве значения атрибута `manager`.

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
