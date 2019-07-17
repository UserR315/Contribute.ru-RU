---
title: ms-author-invalid
description: Объяснение проблемы со сборкой документов ms-author-invalid и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ae01c34ea60cec30698d7e11264d05c3f398d1c
ms.sourcegitcommit: 1311ccbbf38312bfe6947082870bc9e90d38c986
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/11/2019
ms.locfileid: "67791554"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="da4d0-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="da4d0-103">ms-author-invalid</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="da4d0-104">Предложение</span><span class="sxs-lookup"><span data-stu-id="da4d0-104">Suggestion</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="da4d0-105">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="da4d0-105">Resolution</span></span>

<span data-ttu-id="da4d0-106">Проверьте, что значение `ms.author` является допустимым псевдонимом Майкрософт текущего автора.</span><span class="sxs-lookup"><span data-stu-id="da4d0-106">Verify that the `ms.author` value is the current author's valid Microsoft alias.</span></span> <span data-ttu-id="da4d0-107">Если псевдоним используется для списка рассылки, он должен быть добавлен в список разрешенных.</span><span class="sxs-lookup"><span data-stu-id="da4d0-107">If the alias is a distribution list, it must also be on the allow list.</span></span>

<span data-ttu-id="da4d0-108">Допустимые значения для списков рассылки см. на [этом внутреннем сайте Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="da4d0-108">Valid values for DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
