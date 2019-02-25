---
title: ms-date-too-late
description: Объяснение и устранение проблем сборки документов ms-date-too-late
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: b38392e9f297e4ee4147ca7fc65f938b5cd53403
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431491"
---
# <a name="ms-date-too-late"></a><span data-ttu-id="2045e-103">ms-date-too-late</span><span class="sxs-lookup"><span data-stu-id="2045e-103">ms-date-too-late</span></span>

<span data-ttu-id="2045e-104">**Ожидается в ближайшее время.**</span><span class="sxs-lookup"><span data-stu-id="2045e-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="2045e-105">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="2045e-105">Warning</span></span>

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

<span data-ttu-id="2045e-106">Атрибут `ms.date` используется, чтобы показать актуальность, то есть когда содержимое статьи последний раз проверялось на соответствие, точность, правильность снимков экрана и правильную работу ссылок.</span><span class="sxs-lookup"><span data-stu-id="2045e-106">The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="2045e-107">Таким образом, этот атрибут нельзя указать в будущем.</span><span class="sxs-lookup"><span data-stu-id="2045e-107">Therefore, it can't be in the future!</span></span> <span data-ttu-id="2045e-108">У учетной записи есть пять дней для выпуска, например, когда содержимое заморожено для контроля качества при подготовке к крупному событию.</span><span class="sxs-lookup"><span data-stu-id="2045e-108">Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.</span></span>

## <a name="resolution"></a><span data-ttu-id="2045e-109">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="2045e-109">Resolution</span></span>

<span data-ttu-id="2045e-110">В качестве значения `ms.date` укажите дату, не менее чем на 5 дней отстающую от текущей, в формате ММ/ДД/ГГГГ:</span><span class="sxs-lookup"><span data-stu-id="2045e-110">Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
