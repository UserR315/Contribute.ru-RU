---
title: ms-prod-and-service
description: Объяснение и устранение проблем сборки документов ms-prod-and-service
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25a5d2be7d6aad175d746e49e064728020a8ac93
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236347"
---
# <a name="ms-prod-and-service"></a><span data-ttu-id="32450-103">ms-prod-and-service</span><span class="sxs-lookup"><span data-stu-id="32450-103">ms-prod-and-service</span></span>

## <a name="warning"></a><span data-ttu-id="32450-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="32450-104">Warning</span></span>
<span data-ttu-id="32450-105">https://review.docs.microsoft.com/en-us/help/contribute/metadata-changes?branch=master `Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`</span><span class="sxs-lookup"><span data-stu-id="32450-105">https://review.docs.microsoft.com/en-us/help/contribute/metadata-changes?branch=master `Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`</span></span>

## <a name="resolution"></a><span data-ttu-id="32450-106">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="32450-106">Resolution</span></span>

<span data-ttu-id="32450-107">Требуется указать значение `ms.prod` или `ms.service`, которые нельзя указывать одновременно: `ms.prod` используется для локальных продуктов, а `ms.service` — для облачных служб.</span><span class="sxs-lookup"><span data-stu-id="32450-107">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="32450-108">Определите подходящее значение для своей статьи, убедитесь в его правильности и удалите другое поле.</span><span class="sxs-lookup"><span data-stu-id="32450-108">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="32450-109">Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="32450-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="32450-110">Для запроса новых значений следуйте [этой процедуре](https://review.docs.microsoft.com/en-us/help/contribute/metadata-changes?branch=master).</span><span class="sxs-lookup"><span data-stu-id="32450-110">To request new values, follow [this process](https://review.docs.microsoft.com/en-us/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
