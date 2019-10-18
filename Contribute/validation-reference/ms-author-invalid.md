---
title: ms-author-invalid
description: Объяснение проблемы со сборкой документов ms-author-invalid и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: 615d9f5978893196a24e3a043f3b71a22e1eb353
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246292"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="e4067-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="e4067-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="e4067-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="e4067-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="e4067-105">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="e4067-105">Resolution</span></span>

<span data-ttu-id="e4067-106">Измените значение `ms.author` на допустимый псевдоним Майкрософт текущего автора.</span><span class="sxs-lookup"><span data-stu-id="e4067-106">Update the `ms.author` value with the current author's valid Microsoft alias.</span></span> <span data-ttu-id="e4067-107">В качестве автора рекомендуется задавать сотрудника с полной занятостью или командный список рассылки, а не временного поставщика.</span><span class="sxs-lookup"><span data-stu-id="e4067-107">We recommend that the designated author be a full-time employee or team distribution list (DL), rather than a short-term vendor.</span></span> <span data-ttu-id="e4067-108">Если псевдоним является списком рассылки, он также должен быть в списке разрешений `ms.author`.</span><span class="sxs-lookup"><span data-stu-id="e4067-108">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="e4067-109">Допустимые значения для списков рассылки `ms.author` см. на [этом внутреннем сайте Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="e4067-109">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
