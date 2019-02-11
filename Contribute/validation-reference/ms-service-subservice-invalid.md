---
title: ms-service-and-subservice-invalid
description: Объяснение и устранение проблем сборки документов ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 6a2efc5cee04d7721e7a8fe1602ca24dc09ca7fd
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713138"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="cc9fc-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="cc9fc-103">ms-service-and-subservice-invalid</span></span>

<span data-ttu-id="cc9fc-104">**Ожидается в ближайшее время.**</span><span class="sxs-lookup"><span data-stu-id="cc9fc-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="cc9fc-105">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="cc9fc-105">Warning</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="cc9fc-106">Используйте `ms.service`, чтобы указать облачные службы.</span><span class="sxs-lookup"><span data-stu-id="cc9fc-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="cc9fc-107">Чтобы указать более подробные сведения о `ms.service`, вы можете дополнительно указать `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="cc9fc-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="cc9fc-108">Пара значений `ms.service` и `ms.subservice` должна быть допустимой.</span><span class="sxs-lookup"><span data-stu-id="cc9fc-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="cc9fc-109">Значение `ms.service` недопустимо, или же значение `ms.subservice` не является допустимой парой для значения `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="cc9fc-109">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="cc9fc-110">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="cc9fc-110">Resolution</span></span>

<span data-ttu-id="cc9fc-111">Убедитесь, что значение `ms.service` подходит для вашей статьи.</span><span class="sxs-lookup"><span data-stu-id="cc9fc-111">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="cc9fc-112">Затем выберите допустимое значение `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="cc9fc-112">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="cc9fc-113">Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="cc9fc-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
