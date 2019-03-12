---
title: yaml-header-invalid
description: Объяснение проблемы со сборкой документов yaml-header-invalid и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 62b3b2c2aa47525cae5dd5c0955eb88463124359
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459034"
---
# <a name="yaml-header-invalid"></a>yaml-header-invalid

## <a name="warning"></a>Предупреждение

`Invalid YAML header: Improper use of a colon in a metadata entry.`

Как правило, это означает, что не заключенное в кавычки значение метаданных в заголовке YAML содержит двоеточие или другой специальный символ. Это предупреждение также может указывать на отсутствие пробела после двоеточия в паре "ключ-значение".

## <a name="resolution"></a>Способы устранения

Проверьте заголовок YAML. Найдите приведенные ниже ошибки.

Двоеточие в значении, не заключенном в кавычки:

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

Внесите следующие изменения:

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

Отсутствие пробела после двоеточия в паре "ключ-значение":

```yml
---
title:I omitted a space.
---
```

Внесите следующие изменения:

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
