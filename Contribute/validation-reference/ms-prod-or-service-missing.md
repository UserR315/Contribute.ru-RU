---
title: ms-prod-or-service-missing
description: Объяснение и устранение проблем сборки документов ms-prod-or-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 8d8d01f95af74009cfa9cb1a57531663df4edf4d
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637375"
---
# <a name="ms-prod-or-service-missing"></a><span data-ttu-id="e71ac-103">ms-prod-or-service-missing</span><span class="sxs-lookup"><span data-stu-id="e71ac-103">ms-prod-or-service-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="e71ac-104">Предложение</span><span class="sxs-lookup"><span data-stu-id="e71ac-104">Suggestion</span></span>

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="e71ac-105">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="e71ac-105">Resolution</span></span>

<span data-ttu-id="e71ac-106">Требуется указать значение `ms.prod` или `ms.service`, которые нельзя указывать одновременно: `ms.prod` используется для локальных продуктов, а `ms.service` — для облачных служб.</span><span class="sxs-lookup"><span data-stu-id="e71ac-106">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="e71ac-107">Определите подходящее значение для своей статьи, убедитесь в его правильности и удалите другое поле.</span><span class="sxs-lookup"><span data-stu-id="e71ac-107">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="e71ac-108">Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="e71ac-108">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]