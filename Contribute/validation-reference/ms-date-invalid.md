---
title: ms-date-invalid
description: Объяснение и устранение проблем сборки документов ms-date-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: a54dc495593315a0382ea99e46a86145fbfa8577
ms.sourcegitcommit: 836d4d6127fabb5569ffc0809db5fb25e46038b5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2019
ms.locfileid: "72590881"
---
# <a name="ms-date-invalid"></a><span data-ttu-id="8c73f-103">ms-date-invalid</span><span class="sxs-lookup"><span data-stu-id="8c73f-103">ms-date-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="8c73f-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="8c73f-104">Warning</span></span>

`Invalid value for ms.date: '{value}'. Must be a date in format MM/DD/YYYY, no more than 30 days from today.`

## <a name="resolution"></a><span data-ttu-id="8c73f-105">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="8c73f-105">Resolution</span></span>

<span data-ttu-id="8c73f-106">Убедитесь, что статья актуальна и в ней отсутствует испорченное содержимое, и добавьте допустимую дату в формате ММ/ДД/ГГГГ.</span><span class="sxs-lookup"><span data-stu-id="8c73f-106">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
