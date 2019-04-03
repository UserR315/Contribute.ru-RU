---
title: deprecated-attribute
description: Объяснение и устранение проблем со сборкой документов (deprecated-attribute)
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 113ca759af1765a2a51cadc721fa59743b699475
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636892"
---
# <a name="deprecated-attribute"></a><span data-ttu-id="b7a7d-103">deprecated-attribute</span><span class="sxs-lookup"><span data-stu-id="b7a7d-103">deprecated-attribute</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="b7a7d-104">Предложение</span><span class="sxs-lookup"><span data-stu-id="b7a7d-104">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="b7a7d-105">Используйте `ms.service`, чтобы указать облачные службы.</span><span class="sxs-lookup"><span data-stu-id="b7a7d-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="b7a7d-106">Чтобы указать более подробные сведения о `ms.service`, вы можете дополнительно указать `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="b7a7d-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="b7a7d-107">Не используйте значение `ms.component`, так как оно устарело для этого содержимого.</span><span class="sxs-lookup"><span data-stu-id="b7a7d-107">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="b7a7d-108">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="b7a7d-108">Resolution</span></span>

<span data-ttu-id="b7a7d-109">Убедитесь, что значение `ms.service` подходит для вашей статьи.</span><span class="sxs-lookup"><span data-stu-id="b7a7d-109">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="b7a7d-110">Затем выберите допустимое значение `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="b7a7d-110">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="b7a7d-111">Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="b7a7d-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
