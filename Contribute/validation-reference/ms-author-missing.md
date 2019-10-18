---
title: ms-author-missing
description: Объяснение и устранение проблем сборки документов ms-author-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6b313bd6b168b913d82721607126fcd4e6255009
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246254"
---
# <a name="ms-author-missing"></a><span data-ttu-id="69e41-103">ms-author-missing</span><span class="sxs-lookup"><span data-stu-id="69e41-103">ms-author-missing</span></span>

## <a name="warning"></a><span data-ttu-id="69e41-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="69e41-104">Warning</span></span>

`Missing attribute: ms.author. Add the current author's Microsoft alias.`

## <a name="resolution"></a><span data-ttu-id="69e41-105">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="69e41-105">Resolution</span></span>

<span data-ttu-id="69e41-106">Укажите псевдоним Майкрософт текущего автора в качестве значения `ms.author`.</span><span class="sxs-lookup"><span data-stu-id="69e41-106">Add the current author's Microsoft alias for `ms.author`.</span></span> <span data-ttu-id="69e41-107">Обратите внимание, что это должен быть *текущий* владелец статьи, а не первоначальный автор, если владелец менялся.</span><span class="sxs-lookup"><span data-stu-id="69e41-107">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span> <span data-ttu-id="69e41-108">В качестве автора рекомендуется задавать сотрудника с полной занятостью или командный список рассылки, а не временного поставщика.</span><span class="sxs-lookup"><span data-stu-id="69e41-108">We recommend that the designated author be a full-time employee or team distribution list (DL), rather than a short-term vendor.</span></span> 

<span data-ttu-id="69e41-109">Если псевдоним является списком рассылки, он также должен быть в списке разрешений `ms.author`.</span><span class="sxs-lookup"><span data-stu-id="69e41-109">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="69e41-110">Допустимые значения для списков рассылки `ms.author` см. на [этом внутреннем сайте Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="69e41-110">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
