---
title: ms-prod-service-mismatch
description: Объяснение и устранение проблем сборки документов ms-prod-service-mismatch
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4a3cf8bc5435972f0442ca1d41d4147e1ea00d78
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713184"
---
# <a name="ms-prod-service-mismatch"></a><span data-ttu-id="8e129-103">ms-prod-service-mismatch</span><span class="sxs-lookup"><span data-stu-id="8e129-103">ms-prod-service-mismatch</span></span>

<span data-ttu-id="8e129-104">**Ожидается в ближайшее время.**</span><span class="sxs-lookup"><span data-stu-id="8e129-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="8e129-105">Предложение</span><span class="sxs-lookup"><span data-stu-id="8e129-105">Suggestion</span></span>

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

<span data-ttu-id="8e129-106">Используйте `ms.prod`, чтобы указать локальные продукты для облачных служб `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="8e129-106">Use `ms.prod` to specify on-premises products; `ms.service` for cloud services.</span></span> <span data-ttu-id="8e129-107">Чтобы указать более подробные сведения о `ms.prod`, вы можете дополнительно указать `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="8e129-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="8e129-108">Чтобы указать более подробные сведения о `ms.service`, вы можете указать `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="8e129-108">To specify more detailed information about `ms.service`, you can specify `ms.subservice`.</span></span> <span data-ttu-id="8e129-109">Вы не можете использовать `ms.prod` с `ms.subservice` или `ms.service` с `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="8e129-109">You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.</span></span>

## <a name="resolution"></a><span data-ttu-id="8e129-110">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="8e129-110">Resolution</span></span>

<span data-ttu-id="8e129-111">Сначала проверьте, что вы выбрали правильный родительский атрибут (`ms.prod` или `ms.service`) для статьи.</span><span class="sxs-lookup"><span data-stu-id="8e129-111">First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article.</span></span> <span data-ttu-id="8e129-112">Затем добавьте соответствующий дочерний элемент с допустимым значением пары.</span><span class="sxs-lookup"><span data-stu-id="8e129-112">Then, add the appropriate child field with a valid paired value.</span></span> <span data-ttu-id="8e129-113">Удалите любые дополнительные поля.</span><span class="sxs-lookup"><span data-stu-id="8e129-113">Remove any extra fields.</span></span>

<span data-ttu-id="8e129-114">Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="8e129-114">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
