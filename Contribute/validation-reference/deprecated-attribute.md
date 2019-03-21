---
title: deprecated-attribute
description: Объяснение и устранение проблем со сборкой документов (deprecated-attribute)
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 564bd35c418fb9def6bf20240fca64265a477f46
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987797"
---
# <a name="deprecated-attribute"></a><span data-ttu-id="c8930-103">deprecated-attribute</span><span class="sxs-lookup"><span data-stu-id="c8930-103">deprecated-attribute</span></span>

<span data-ttu-id="c8930-104">**Ожидается в ближайшее время.**</span><span class="sxs-lookup"><span data-stu-id="c8930-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="c8930-105">Предложение</span><span class="sxs-lookup"><span data-stu-id="c8930-105">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="c8930-106">Используйте `ms.service`, чтобы указать облачные службы.</span><span class="sxs-lookup"><span data-stu-id="c8930-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="c8930-107">Чтобы указать более подробные сведения о `ms.service`, вы можете дополнительно указать `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="c8930-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="c8930-108">Не используйте значение `ms.component`, так как оно устарело для этого содержимого.</span><span class="sxs-lookup"><span data-stu-id="c8930-108">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="c8930-109">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="c8930-109">Resolution</span></span>

<span data-ttu-id="c8930-110">Убедитесь, что значение `ms.service` подходит для вашей статьи.</span><span class="sxs-lookup"><span data-stu-id="c8930-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="c8930-111">Затем выберите допустимое значение `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="c8930-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="c8930-112">Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="c8930-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
