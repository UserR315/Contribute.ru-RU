---
title: author-missing
description: Объяснение и устранение проблем сборки документов author-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 904ec2ad495945d882e581a240f6a72ca650c37e
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848579"
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
