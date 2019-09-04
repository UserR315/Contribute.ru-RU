---
title: ms-service-and-subservice-invalid
description: Объяснение и устранение проблем сборки документов ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a6059d592212b271780344a086ee68c7133e15cd
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236514"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="0a862-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="0a862-103">ms-service-and-subservice-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="0a862-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="0a862-104">Warning</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="0a862-105">Используйте `ms.service`, чтобы указать облачные службы.</span><span class="sxs-lookup"><span data-stu-id="0a862-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="0a862-106">Чтобы указать более подробные сведения о `ms.service`, вы можете дополнительно указать `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="0a862-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="0a862-107">Пара значений `ms.service` и `ms.subservice` должна быть допустимой.</span><span class="sxs-lookup"><span data-stu-id="0a862-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="0a862-108">Значение `ms.service` недопустимо, или же значение `ms.subservice` не является допустимой парой для значения `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="0a862-108">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="0a862-109">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="0a862-109">Resolution</span></span>

<span data-ttu-id="0a862-110">Убедитесь, что значение `ms.service` подходит для вашей статьи.</span><span class="sxs-lookup"><span data-stu-id="0a862-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="0a862-111">Затем выберите допустимое значение `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="0a862-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="0a862-112">Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="0a862-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="0a862-113">Для запроса новых значений следуйте [этой процедуре](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span><span class="sxs-lookup"><span data-stu-id="0a862-113">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
