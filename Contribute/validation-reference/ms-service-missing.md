---
title: ms-service-missing
description: Объяснение и устранение проблем сборки документов ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7c5860d9ef50598ad5b3e9546100af0ba436e69f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987728"
---
# <a name="ms-service-missing"></a><span data-ttu-id="41289-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="41289-103">ms-service-missing</span></span>

<span data-ttu-id="41289-104">**Ожидается в ближайшее время.**</span><span class="sxs-lookup"><span data-stu-id="41289-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="41289-105">Предложение</span><span class="sxs-lookup"><span data-stu-id="41289-105">Suggestion</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="41289-106">Используйте `ms.service`, чтобы указать облачные службы.</span><span class="sxs-lookup"><span data-stu-id="41289-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="41289-107">Чтобы указать более подробные сведения об `ms.service`, вы можете дополнительно указать `ms.subservice`, но вместе с ним нужно также указать `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="41289-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="41289-108">Пара значений `ms.service` и `ms.subservice` должна быть допустимой.</span><span class="sxs-lookup"><span data-stu-id="41289-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="41289-109">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="41289-109">Resolution</span></span>

<span data-ttu-id="41289-110">Убедитесь, что указанное значение `ms.subservice` подходит для вашей статьи.</span><span class="sxs-lookup"><span data-stu-id="41289-110">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="41289-111">Затем добавьте соответствующее значение `ms.service`, которое является родительским для `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="41289-111">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="41289-112">Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="41289-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
