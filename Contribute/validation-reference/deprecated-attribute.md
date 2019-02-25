---
title: deprecated-attribute
description: Объяснение и устранение проблем со сборкой документов (deprecated-attribute)
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4f9ddc611d401bc7003e1b7d378517d5e374da87
ms.sourcegitcommit: a2c8317ccf8b56371773c84f4960a44787ce8666
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2019
ms.locfileid: "56322698"
---
# <a name="deprecated-attribute"></a><span data-ttu-id="dca2a-103">deprecated-attribute</span><span class="sxs-lookup"><span data-stu-id="dca2a-103">deprecated-attribute</span></span>

<span data-ttu-id="dca2a-104">**Ожидается в ближайшее время.**</span><span class="sxs-lookup"><span data-stu-id="dca2a-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="dca2a-105">Предложение</span><span class="sxs-lookup"><span data-stu-id="dca2a-105">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="dca2a-106">Используйте `ms.service`, чтобы указать облачные службы.</span><span class="sxs-lookup"><span data-stu-id="dca2a-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="dca2a-107">Чтобы указать более подробные сведения о `ms.service`, вы можете дополнительно указать `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="dca2a-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="dca2a-108">Не используйте значение `ms.component`, так как оно устарело для этого содержимого.</span><span class="sxs-lookup"><span data-stu-id="dca2a-108">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="dca2a-109">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="dca2a-109">Resolution</span></span>

<span data-ttu-id="dca2a-110">Убедитесь, что значение `ms.service` подходит для вашей статьи.</span><span class="sxs-lookup"><span data-stu-id="dca2a-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="dca2a-111">Затем выберите допустимое значение `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="dca2a-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="dca2a-112">Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="dca2a-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
