---
title: ms-component-deprecated
description: Объяснение и устранение проблем сборки документов ms-component-deprecated
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4f89571e2d4c50439806fb26b9967a4b7588f4a9
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713161"
---
# <a name="ms-component-deprecated"></a><span data-ttu-id="8cd57-103">ms-component-deprecated</span><span class="sxs-lookup"><span data-stu-id="8cd57-103">ms-component-deprecated</span></span>

<span data-ttu-id="8cd57-104">**Ожидается в ближайшее время.**</span><span class="sxs-lookup"><span data-stu-id="8cd57-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="8cd57-105">Предложение</span><span class="sxs-lookup"><span data-stu-id="8cd57-105">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="8cd57-106">Используйте `ms.service`, чтобы указать облачные службы.</span><span class="sxs-lookup"><span data-stu-id="8cd57-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="8cd57-107">Чтобы указать более подробные сведения о `ms.service`, вы можете дополнительно указать `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="8cd57-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="8cd57-108">Не используйте значение `ms.component`, так как оно устарело для этого содержимого.</span><span class="sxs-lookup"><span data-stu-id="8cd57-108">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="8cd57-109">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="8cd57-109">Resolution</span></span>

<span data-ttu-id="8cd57-110">Убедитесь, что значение `ms.service` подходит для вашей статьи.</span><span class="sxs-lookup"><span data-stu-id="8cd57-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="8cd57-111">Затем выберите допустимое значение `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="8cd57-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="8cd57-112">Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="8cd57-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
