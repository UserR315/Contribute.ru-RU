---
title: ms-service-missing
description: Объяснение и устранение проблем сборки документов ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 17e2e272e3a21e14e038e27ff68866afe28bee60
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636708"
---
# <a name="ms-service-missing"></a><span data-ttu-id="247de-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="247de-103">ms-service-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="247de-104">Предложение</span><span class="sxs-lookup"><span data-stu-id="247de-104">Suggestion</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="247de-105">Используйте `ms.service`, чтобы указать облачные службы.</span><span class="sxs-lookup"><span data-stu-id="247de-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="247de-106">Чтобы указать более подробные сведения об `ms.service`, вы можете дополнительно указать `ms.subservice`, но вместе с ним нужно также указать `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="247de-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="247de-107">Пара значений `ms.service` и `ms.subservice` должна быть допустимой.</span><span class="sxs-lookup"><span data-stu-id="247de-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="247de-108">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="247de-108">Resolution</span></span>

<span data-ttu-id="247de-109">Убедитесь, что указанное значение `ms.subservice` подходит для вашей статьи.</span><span class="sxs-lookup"><span data-stu-id="247de-109">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="247de-110">Затем добавьте соответствующее значение `ms.service`, которое является родительским для `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="247de-110">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="247de-111">Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="247de-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
