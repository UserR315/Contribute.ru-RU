---
title: ms-prod-and-technology-invalid
description: Объяснение и устранение проблем сборки документов ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 92e8b17c3b5c96d544d12d394534a494ada3b901
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713276"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="aa6d0-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="aa6d0-103">ms-prod-and-technology-invalid</span></span>

<span data-ttu-id="aa6d0-104">**Ожидается в ближайшее время.**</span><span class="sxs-lookup"><span data-stu-id="aa6d0-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="aa6d0-105">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="aa6d0-105">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="aa6d0-106">Используйте `ms.prod`, чтобы указать локальные продукты.</span><span class="sxs-lookup"><span data-stu-id="aa6d0-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="aa6d0-107">Чтобы указать более подробные сведения о `ms.prod`, вы можете дополнительно указать `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="aa6d0-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="aa6d0-108">Пара значений `ms.prod` и `ms.technology` должна быть допустимой.</span><span class="sxs-lookup"><span data-stu-id="aa6d0-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="aa6d0-109">Значение `ms.prod` недопустимо, или же значение `ms.technology` не является допустимой парой для значения `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="aa6d0-109">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="aa6d0-110">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="aa6d0-110">Resolution</span></span>

<span data-ttu-id="aa6d0-111">Убедитесь, что значение `ms.prod` подходит для вашей статьи.</span><span class="sxs-lookup"><span data-stu-id="aa6d0-111">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="aa6d0-112">Затем выберите допустимое значение `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="aa6d0-112">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="aa6d0-113">Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="aa6d0-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!-- Can we link to whitelist externally? -->

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
