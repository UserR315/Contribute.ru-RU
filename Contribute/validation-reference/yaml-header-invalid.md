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
# <a name="yaml-header-invalid"></a><span data-ttu-id="d951e-103">yaml-header-invalid</span><span class="sxs-lookup"><span data-stu-id="d951e-103">yaml-header-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="d951e-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="d951e-104">Warning</span></span>

`Invalid YAML header: Improper use of a colon in a metadata entry.`

<span data-ttu-id="d951e-105">Как правило, это означает, что не заключенное в кавычки значение метаданных в заголовке YAML содержит двоеточие или другой специальный символ.</span><span class="sxs-lookup"><span data-stu-id="d951e-105">Usually this means an unquoted metadata value in a YAML header includes a colon or another special character.</span></span> <span data-ttu-id="d951e-106">Это предупреждение также может указывать на отсутствие пробела после двоеточия в паре "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="d951e-106">It can also mean that a space is missing after the colon in a key/value pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="d951e-107">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="d951e-107">Resolution</span></span>

<span data-ttu-id="d951e-108">Проверьте заголовок YAML.</span><span class="sxs-lookup"><span data-stu-id="d951e-108">Review your YAML header.</span></span> <span data-ttu-id="d951e-109">Найдите приведенные ниже ошибки.</span><span class="sxs-lookup"><span data-stu-id="d951e-109">Look for the following mistakes.</span></span>

<span data-ttu-id="d951e-110">Двоеточие в значении, не заключенном в кавычки:</span><span class="sxs-lookup"><span data-stu-id="d951e-110">Colon in unquoted value:</span></span>

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

<span data-ttu-id="d951e-111">Внесите следующие изменения:</span><span class="sxs-lookup"><span data-stu-id="d951e-111">Change to:</span></span>

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

<span data-ttu-id="d951e-112">Отсутствие пробела после двоеточия в паре "ключ-значение":</span><span class="sxs-lookup"><span data-stu-id="d951e-112">No space after colon in key/value pair:</span></span>

```yml
---
title:I omitted a space.
---
```

<span data-ttu-id="d951e-113">Внесите следующие изменения:</span><span class="sxs-lookup"><span data-stu-id="d951e-113">Change to:</span></span>

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
