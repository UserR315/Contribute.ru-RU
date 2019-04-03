---
title: ms-prod-missing
description: Объяснение и устранение проблем сборки документов ms-prod-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9b3f209ca2300735210490ffd58c3ac423c44fef
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636777"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="e290b-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="e290b-103">ms-prod-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="e290b-104">Предложение</span><span class="sxs-lookup"><span data-stu-id="e290b-104">Suggestion</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="e290b-105">Используйте `ms.prod`, чтобы указать локальные продукты.</span><span class="sxs-lookup"><span data-stu-id="e290b-105">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="e290b-106">Чтобы указать более подробные сведения об `ms.prod`, вы можете дополнительно указать `ms.technology`, но вместе с ним нужно также указать `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="e290b-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="e290b-107">Пара значений `ms.prod` и `ms.technology` должна быть допустимой.</span><span class="sxs-lookup"><span data-stu-id="e290b-107">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="e290b-108">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="e290b-108">Resolution</span></span>

<span data-ttu-id="e290b-109">Убедитесь, что указанное значение `ms.technology` подходит для вашей статьи.</span><span class="sxs-lookup"><span data-stu-id="e290b-109">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="e290b-110">Затем добавьте соответствующее значение `ms.prod`, которое является родительским для `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="e290b-110">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="e290b-111">Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="e290b-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
