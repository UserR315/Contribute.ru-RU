---
title: ms-author-invalid
description: Объяснение проблемы со сборкой документов ms-author-invalid и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 6d6c77b9b378865913e2055abf2b64ccba8ca482
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636731"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="7b685-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="7b685-103">ms-author-invalid</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="7b685-104">Предложение</span><span class="sxs-lookup"><span data-stu-id="7b685-104">Suggestion</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="7b685-105">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="7b685-105">Resolution</span></span>

<span data-ttu-id="7b685-106">Проверьте, является ли значение `ms.author` допустимым псевдонимом Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="7b685-106">Verify that the `ms.author` value is a valid Microsoft alias.</span></span> <span data-ttu-id="7b685-107">Если псевдоним используется для списка рассылки, он должен быть добавлен в список разрешенных.</span><span class="sxs-lookup"><span data-stu-id="7b685-107">If the alias is a distribution list, it must also be on the allow list.</span></span>

<span data-ttu-id="7b685-108">Допустимые значения для списков рассылки см. на [этом внутреннем сайте Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="7b685-108">Valid values for DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
