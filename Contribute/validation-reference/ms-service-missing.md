---
title: ms-service-missing
description: Объяснение и устранение проблем сборки документов ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: b50d9d6f57c953569a4e5dd873961b8c511a8bb1
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236500"
---
# <a name="ms-service-missing"></a><span data-ttu-id="f0d22-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="f0d22-103">ms-service-missing</span></span>

## <a name="warning"></a><span data-ttu-id="f0d22-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="f0d22-104">Warning</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="f0d22-105">Используйте `ms.service`, чтобы указать облачные службы.</span><span class="sxs-lookup"><span data-stu-id="f0d22-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="f0d22-106">Чтобы указать более подробные сведения об `ms.service`, вы можете дополнительно указать `ms.subservice`, но вместе с ним нужно также указать `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="f0d22-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="f0d22-107">Пара значений `ms.service` и `ms.subservice` должна быть допустимой.</span><span class="sxs-lookup"><span data-stu-id="f0d22-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="f0d22-108">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="f0d22-108">Resolution</span></span>

<span data-ttu-id="f0d22-109">Убедитесь, что указанное значение `ms.subservice` подходит для вашей статьи.</span><span class="sxs-lookup"><span data-stu-id="f0d22-109">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="f0d22-110">Затем добавьте соответствующее значение `ms.service`, которое является родительским для `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="f0d22-110">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="f0d22-111">Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="f0d22-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="f0d22-112">Для запроса новых значений следуйте [этой процедуре](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span><span class="sxs-lookup"><span data-stu-id="f0d22-112">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
