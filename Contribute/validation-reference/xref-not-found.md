---
title: xref-not-found
description: Объяснение проблемы со сборкой документов xref-not-found и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: d51eace291bfac179be2701463d113c06627f92f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427878"
---
# <a name="xref-not-found"></a><span data-ttu-id="eb549-103">xref-not-found</span><span class="sxs-lookup"><span data-stu-id="eb549-103">xref-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="eb549-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="eb549-104">Warning</span></span>

`Cross reference not found: '<xref: {uid}>'.`

`Cross reference not found: '@{uid}'.`

<span data-ttu-id="eb549-105">Связанный уникальный идентификатор не существует или недоступен для вашего репозитория.</span><span class="sxs-lookup"><span data-stu-id="eb549-105">The UID you linked to doesn't exist, or isn't available to your repo.</span></span>

## <a name="resolution"></a><span data-ttu-id="eb549-106">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="eb549-106">Resolution</span></span>

<span data-ttu-id="eb549-107">Убедитесь в том, что указан правильный уникальный идентификатор и что в репозитории правильно настроена служба Xref, как описано в [документации](https://review.docs.microsoft.com/en-us/help/onboard/admin/xref-service?branch=master) на внутреннем сайте корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="eb549-107">Confirm that the UID is correct and that the Xref Service is properly configured on your repo, as described in the Microsoft-internal [Xref Service](https://review.docs.microsoft.com/en-us/help/onboard/admin/xref-service?branch=master) documentation.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
