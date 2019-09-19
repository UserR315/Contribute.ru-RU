---
title: h1-not-first
description: Объяснение проблемы со сборкой Документации h1-not-first и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: c5e2eeeb5c464cd2923e23110cdab9a83324e53e
ms.sourcegitcommit: 89ec9772d9cc8281c633833c6fa51f629e9cd566
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/11/2019
ms.locfileid: "70895469"
---
# <a name="h1-not-first"></a>h1-not-first

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Предложение

`Markdown content is not allowed before H1.`

Перед H1 в файле Markdown может располагаться только заголовок метаданных YAML. Например, если вы хотите добавить заметку или изображение в верхней части статьи, они должны располагаться после H1. Способ, использующийся в примере ниже, запрещен:

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

Правильно делать так:

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

Другой распространенной причиной этой проблемы являются [метки порядка байтов (BOM)](http://www.websina.com/bugzero/kb/unicode-bom.html) перед заголовком YAML. Иногда они возникают из-за проблем с кодированием при фиксации содержимого в репозиториях. Метки порядка байтов приводят к неправильной отрисовке в GitHub, и их следует удалить.

## <a name="resolution"></a>Способы устранения

Удалите все содержимое, кроме заголовка метаданных YAML, из кода, находящегося перед H1.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
