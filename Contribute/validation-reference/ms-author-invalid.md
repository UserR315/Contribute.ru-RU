---
title: ms-author-invalid
description: Объяснение проблемы со сборкой документов ms-author-invalid и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25428f93eaa7d36a5bbe35d77434ef33972e8944
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236532"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="6057d-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="6057d-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="6057d-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="6057d-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="6057d-105">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="6057d-105">Resolution</span></span>

<span data-ttu-id="6057d-106">Проверьте, что значение `ms.author` является допустимым псевдонимом Майкрософт текущего автора.</span><span class="sxs-lookup"><span data-stu-id="6057d-106">Verify that the `ms.author` value is the current author's valid Microsoft alias.</span></span> <span data-ttu-id="6057d-107">Если псевдоним используется для списка рассылки, он должен быть добавлен в список разрешенных.</span><span class="sxs-lookup"><span data-stu-id="6057d-107">If the alias is a distribution list, it must also be on the allow list.</span></span>

<span data-ttu-id="6057d-108">Допустимые значения для списков рассылки см. на [этом внутреннем сайте Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="6057d-108">Valid values for DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
