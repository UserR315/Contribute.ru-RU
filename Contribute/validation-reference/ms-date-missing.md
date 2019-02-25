---
title: ms-date-missing
description: Объяснение и устранение проблем сборки документов ms-date-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: d7697c8449e451879c137d9d6cdf42327e597be6
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431468"
---
# <a name="ms-date-missing"></a><span data-ttu-id="b9c1b-103">ms-date-missing</span><span class="sxs-lookup"><span data-stu-id="b9c1b-103">ms-date-missing</span></span>

<span data-ttu-id="b9c1b-104">**Ожидается в ближайшее время.**</span><span class="sxs-lookup"><span data-stu-id="b9c1b-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="b9c1b-105">Предложение</span><span class="sxs-lookup"><span data-stu-id="b9c1b-105">Suggestion</span></span>

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

<span data-ttu-id="b9c1b-106">Эта дата означала актуальность, то есть когда содержимое статьи последний раз проверялось на соответствие, точность, правильность снимков экрана и правильную работу ссылок.</span><span class="sxs-lookup"><span data-stu-id="b9c1b-106">This date is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="b9c1b-107">Она не соответствует дате последней *публикации* статьи, которая будет показана на странице, если `ms.date` не указано явно.</span><span class="sxs-lookup"><span data-stu-id="b9c1b-107">This is not the same as the last date the article was *published*, which will show on the page if `ms.date` is not explicitly specified.</span></span>

## <a name="resolution"></a><span data-ttu-id="b9c1b-108">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="b9c1b-108">Resolution</span></span>

<span data-ttu-id="b9c1b-109">Убедитесь, что статья актуальна и в ней отсутствует испорченное содержимое, и добавьте допустимую дату в формате ММ/ДД/ГГГГ.</span><span class="sxs-lookup"><span data-stu-id="b9c1b-109">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
