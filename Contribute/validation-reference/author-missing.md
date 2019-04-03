---
title: author-missing
description: Объяснение и устранение проблем сборки документов author-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6c7306cf674a345b25d3e05c4e00662623c44469
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637444"
---
# <a name="author-missing"></a>author-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Предложение

`Missing attribute: author. Add a valid GitHub ID.`

Атрибут `author` определяет автора статьи по идентификатору GitHub. 

## <a name="resolution"></a>Способы устранения

Добавьте идентификатор GitHub автора к заголовку YML:

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]