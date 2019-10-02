---
title: ms-author-invalid
description: Объяснение проблемы со сборкой документов ms-author-invalid и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: b3100b4a304356aee3c50f805628890b8c738fe1
ms.sourcegitcommit: d2f5b68b6a6d1ac902dba5063482ff5955a5b1f7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2019
ms.locfileid: "71481694"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="d155b-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="d155b-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="d155b-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="d155b-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="d155b-105">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="d155b-105">Resolution</span></span>

<span data-ttu-id="d155b-106">Проверьте, что значение `ms.author` является допустимым псевдонимом Майкрософт текущего автора.</span><span class="sxs-lookup"><span data-stu-id="d155b-106">Verify that the `ms.author` value is the current author's valid Microsoft alias.</span></span> <span data-ttu-id="d155b-107">В качестве автора рекомендуется задавать сотрудника с полной занятостью или командный список рассылки, а не временного поставщика.</span><span class="sxs-lookup"><span data-stu-id="d155b-107">We recommend that the designated author be a full-time employee or team distrubution list (DL), rather than a short-term vendor.</span></span> <span data-ttu-id="d155b-108">Если псевдоним является списком рассылки, он также должен быть в списке разрешений `ms.author`.</span><span class="sxs-lookup"><span data-stu-id="d155b-108">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="d155b-109">Допустимые значения для списков рассылки `ms.author` см. на [этом внутреннем сайте Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="d155b-109">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
