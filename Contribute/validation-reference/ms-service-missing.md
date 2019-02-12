---
title: ms-service-missing
description: Объяснение и устранение проблем сборки документов ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2bc425726f82840565978072b2efdf13a1284ec0
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713092"
---
# <a name="ms-service-missing"></a><span data-ttu-id="f16e6-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="f16e6-103">ms-service-missing</span></span>

<span data-ttu-id="f16e6-104">**Ожидается в ближайшее время.**</span><span class="sxs-lookup"><span data-stu-id="f16e6-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="f16e6-105">Предложение</span><span class="sxs-lookup"><span data-stu-id="f16e6-105">Suggestion</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="f16e6-106">Используйте `ms.service`, чтобы указать облачные службы.</span><span class="sxs-lookup"><span data-stu-id="f16e6-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="f16e6-107">Чтобы указать более подробные сведения об `ms.service`, вы можете дополнительно указать `ms.subservice`, но вместе с ним нужно также указать `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="f16e6-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="f16e6-108">Пара значений `ms.service` и `ms.subservice` должна быть допустимой.</span><span class="sxs-lookup"><span data-stu-id="f16e6-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="f16e6-109">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="f16e6-109">Resolution</span></span>

<span data-ttu-id="f16e6-110">Убедитесь, что указанное значение `ms.subservice` подходит для вашей статьи.</span><span class="sxs-lookup"><span data-stu-id="f16e6-110">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="f16e6-111">Затем добавьте соответствующее значение `ms.service`, которое является родительским для `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="f16e6-111">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="f16e6-112">Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="f16e6-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
