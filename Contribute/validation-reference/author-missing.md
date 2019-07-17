---
title: author-missing
description: Объяснение и устранение проблем сборки документов author-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 33d704d64f4a3a1d96792bb01b403aefb3143eb8
ms.sourcegitcommit: 1311ccbbf38312bfe6947082870bc9e90d38c986
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/11/2019
ms.locfileid: "67791510"
---
# <a name="author-missing"></a>author-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Предложение

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
