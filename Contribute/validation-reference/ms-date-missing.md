---
title: ms-date-missing
description: Объяснение и устранение проблем сборки документов ms-date-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: bb352552c133a77ec003bb54f3ab0f3bddfa1be6
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236248"
---
# <a name="ms-date-missing"></a><span data-ttu-id="a4f10-103">ms-date-missing</span><span class="sxs-lookup"><span data-stu-id="a4f10-103">ms-date-missing</span></span>

## <a name="warning"></a><span data-ttu-id="a4f10-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="a4f10-104">Warning</span></span>

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

<span data-ttu-id="a4f10-105">Для некоторых групп содержимого требуется атрибут `ms.date`, который используется, чтобы показать актуальность, то есть когда содержимое статьи последний раз проверялось на соответствие, точность, правильность снимков экрана и правильную работу ссылок.</span><span class="sxs-lookup"><span data-stu-id="a4f10-105">Some content groups require `ms.date` to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="a4f10-106">Она не соответствует дате последней *публикации* статьи, которая будет показана на странице, если `ms.date` не указано явно.</span><span class="sxs-lookup"><span data-stu-id="a4f10-106">This is not the same as the last date the article was *published*, which will show on the page if `ms.date` is not explicitly specified.</span></span>

## <a name="resolution"></a><span data-ttu-id="a4f10-107">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="a4f10-107">Resolution</span></span>

<span data-ttu-id="a4f10-108">Убедитесь, что статья актуальна и в ней отсутствует испорченное содержимое, и добавьте допустимую дату в формате ММ/ДД/ГГГГ.</span><span class="sxs-lookup"><span data-stu-id="a4f10-108">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
