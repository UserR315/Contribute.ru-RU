---
title: ms-prod-service-mismatch
description: Объяснение и устранение проблем сборки документов ms-prod-service-mismatch
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a8d1698a4842ace0e5dd07db170f40a310c666a6
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636800"
---
# <a name="ms-prod-service-mismatch"></a><span data-ttu-id="0347d-103">ms-prod-service-mismatch</span><span class="sxs-lookup"><span data-stu-id="0347d-103">ms-prod-service-mismatch</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="0347d-104">Предложение</span><span class="sxs-lookup"><span data-stu-id="0347d-104">Suggestion</span></span>

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

<span data-ttu-id="0347d-105">Используйте `ms.prod`, чтобы указать локальные продукты для облачных служб `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="0347d-105">Use `ms.prod` to specify on-premises products; `ms.service` for cloud services.</span></span> <span data-ttu-id="0347d-106">Чтобы указать более подробные сведения о `ms.prod`, вы можете дополнительно указать `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="0347d-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="0347d-107">Чтобы указать более подробные сведения о `ms.service`, вы можете указать `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="0347d-107">To specify more detailed information about `ms.service`, you can specify `ms.subservice`.</span></span> <span data-ttu-id="0347d-108">Вы не можете использовать `ms.prod` с `ms.subservice` или `ms.service` с `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="0347d-108">You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.</span></span>

## <a name="resolution"></a><span data-ttu-id="0347d-109">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="0347d-109">Resolution</span></span>

<span data-ttu-id="0347d-110">Сначала проверьте, что вы выбрали правильный родительский атрибут (`ms.prod` или `ms.service`) для статьи.</span><span class="sxs-lookup"><span data-stu-id="0347d-110">First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article.</span></span> <span data-ttu-id="0347d-111">Затем добавьте соответствующий дочерний элемент с допустимым значением пары.</span><span class="sxs-lookup"><span data-stu-id="0347d-111">Then, add the appropriate child field with a valid paired value.</span></span> <span data-ttu-id="0347d-112">Удалите любые дополнительные поля.</span><span class="sxs-lookup"><span data-stu-id="0347d-112">Remove any extra fields.</span></span>

<span data-ttu-id="0347d-113">Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="0347d-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
