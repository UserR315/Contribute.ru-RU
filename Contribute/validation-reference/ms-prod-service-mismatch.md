---
title: ms-prod-service-mismatch
description: Объяснение и устранение проблем сборки документов ms-prod-service-mismatch
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a7de44e9930def2d2582194f28695e3ef3940541
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987622"
---
# <a name="ms-prod-service-mismatch"></a><span data-ttu-id="96295-103">ms-prod-service-mismatch</span><span class="sxs-lookup"><span data-stu-id="96295-103">ms-prod-service-mismatch</span></span>

<span data-ttu-id="96295-104">**Ожидается в ближайшее время.**</span><span class="sxs-lookup"><span data-stu-id="96295-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="96295-105">Предложение</span><span class="sxs-lookup"><span data-stu-id="96295-105">Suggestion</span></span>

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

<span data-ttu-id="96295-106">Используйте `ms.prod`, чтобы указать локальные продукты для облачных служб `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="96295-106">Use `ms.prod` to specify on-premises products; `ms.service` for cloud services.</span></span> <span data-ttu-id="96295-107">Чтобы указать более подробные сведения о `ms.prod`, вы можете дополнительно указать `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="96295-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="96295-108">Чтобы указать более подробные сведения о `ms.service`, вы можете указать `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="96295-108">To specify more detailed information about `ms.service`, you can specify `ms.subservice`.</span></span> <span data-ttu-id="96295-109">Вы не можете использовать `ms.prod` с `ms.subservice` или `ms.service` с `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="96295-109">You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.</span></span>

## <a name="resolution"></a><span data-ttu-id="96295-110">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="96295-110">Resolution</span></span>

<span data-ttu-id="96295-111">Сначала проверьте, что вы выбрали правильный родительский атрибут (`ms.prod` или `ms.service`) для статьи.</span><span class="sxs-lookup"><span data-stu-id="96295-111">First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article.</span></span> <span data-ttu-id="96295-112">Затем добавьте соответствующий дочерний элемент с допустимым значением пары.</span><span class="sxs-lookup"><span data-stu-id="96295-112">Then, add the appropriate child field with a valid paired value.</span></span> <span data-ttu-id="96295-113">Удалите любые дополнительные поля.</span><span class="sxs-lookup"><span data-stu-id="96295-113">Remove any extra fields.</span></span>

<span data-ttu-id="96295-114">Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="96295-114">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
