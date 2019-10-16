---
title: author-missing
description: Объяснение и устранение проблем сборки документов author-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.prod: non-product-specific
ms.date: 09/10/2019
ms.openlocfilehash: e31c39ac9915b096e0b0745bf6d9d3ed6efb5412
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288501"
---
# <a name="author-missing"></a>author-missing

## <a name="warning"></a>Предупреждение

`Missing attribute: author. Add the current author's GitHub ID.`

Атрибут `author` определяет автора статьи по идентификатору GitHub. 

## <a name="resolution"></a>Способы устранения

Добавьте идентификатор текущего автора на GitHub к заголовку YML:

```yml
---
author: meganbradley
ms.author: mbradley
---
```

Обратите внимание, что это должен быть *текущий* владелец статьи, а не первоначальный автор, если владелец менялся.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
