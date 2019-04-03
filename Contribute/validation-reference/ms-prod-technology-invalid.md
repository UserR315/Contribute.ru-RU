---
title: ms-prod-and-technology-invalid
description: Объяснение и устранение проблем сборки документов ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8c6f12629cf4b8cf7fd2471ef4d1287562435696
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636846"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="97d11-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="97d11-103">ms-prod-and-technology-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="97d11-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="97d11-104">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="97d11-105">Используйте `ms.prod`, чтобы указать локальные продукты.</span><span class="sxs-lookup"><span data-stu-id="97d11-105">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="97d11-106">Чтобы указать более подробные сведения о `ms.prod`, вы можете дополнительно указать `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="97d11-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="97d11-107">Пара значений `ms.prod` и `ms.technology` должна быть допустимой.</span><span class="sxs-lookup"><span data-stu-id="97d11-107">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="97d11-108">Значение `ms.prod` недопустимо, или же значение `ms.technology` не является допустимой парой для значения `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="97d11-108">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="97d11-109">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="97d11-109">Resolution</span></span>

<span data-ttu-id="97d11-110">Убедитесь, что значение `ms.prod` подходит для вашей статьи.</span><span class="sxs-lookup"><span data-stu-id="97d11-110">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="97d11-111">Затем выберите допустимое значение `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="97d11-111">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="97d11-112">Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="97d11-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
