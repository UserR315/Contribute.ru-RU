---
title: ms-prod-missing
description: Объяснение и устранение проблем сборки документов ms-prod-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2578ab47dab315a446529d24357e9489d7fd0bad
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987705"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="0597d-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="0597d-103">ms-prod-missing</span></span>

<span data-ttu-id="0597d-104">**Ожидается в ближайшее время.**</span><span class="sxs-lookup"><span data-stu-id="0597d-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="0597d-105">Предложение</span><span class="sxs-lookup"><span data-stu-id="0597d-105">Suggestion</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="0597d-106">Используйте `ms.prod`, чтобы указать локальные продукты.</span><span class="sxs-lookup"><span data-stu-id="0597d-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="0597d-107">Чтобы указать более подробные сведения об `ms.prod`, вы можете дополнительно указать `ms.technology`, но вместе с ним нужно также указать `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="0597d-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="0597d-108">Пара значений `ms.prod` и `ms.technology` должна быть допустимой.</span><span class="sxs-lookup"><span data-stu-id="0597d-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="0597d-109">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="0597d-109">Resolution</span></span>

<span data-ttu-id="0597d-110">Убедитесь, что указанное значение `ms.technology` подходит для вашей статьи.</span><span class="sxs-lookup"><span data-stu-id="0597d-110">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="0597d-111">Затем добавьте соответствующее значение `ms.prod`, которое является родительским для `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="0597d-111">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="0597d-112">Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="0597d-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
