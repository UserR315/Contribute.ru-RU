---
title: ms-service-and-subservice-invalid
description: Объяснение и устранение проблем сборки документов ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7dee18e7b902b660a8071bcb4a0dee21c19f4f7f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987650"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="0b20e-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="0b20e-103">ms-service-and-subservice-invalid</span></span>

<span data-ttu-id="0b20e-104">**Ожидается в ближайшее время.**</span><span class="sxs-lookup"><span data-stu-id="0b20e-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="0b20e-105">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="0b20e-105">Warning</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="0b20e-106">Используйте `ms.service`, чтобы указать облачные службы.</span><span class="sxs-lookup"><span data-stu-id="0b20e-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="0b20e-107">Чтобы указать более подробные сведения о `ms.service`, вы можете дополнительно указать `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="0b20e-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="0b20e-108">Пара значений `ms.service` и `ms.subservice` должна быть допустимой.</span><span class="sxs-lookup"><span data-stu-id="0b20e-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="0b20e-109">Значение `ms.service` недопустимо, или же значение `ms.subservice` не является допустимой парой для значения `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="0b20e-109">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="0b20e-110">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="0b20e-110">Resolution</span></span>

<span data-ttu-id="0b20e-111">Убедитесь, что значение `ms.service` подходит для вашей статьи.</span><span class="sxs-lookup"><span data-stu-id="0b20e-111">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="0b20e-112">Затем выберите допустимое значение `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="0b20e-112">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="0b20e-113">Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="0b20e-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
