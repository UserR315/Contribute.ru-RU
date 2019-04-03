---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
ms.openlocfilehash: a3b383021046412620c616882b19cb06f4dc59f8
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653558"
---
# <a name="locale-specific-links"></a><span data-ttu-id="5bfa7-101">Зависящие от языкового стандарта ссылки</span><span class="sxs-lookup"><span data-stu-id="5bfa7-101">Locale-specific links</span></span>

<span data-ttu-id="5bfa7-102">Ссылки на некоторые сайты Майкрософт не должны содержать коды языкового стандарта, такие как `en-us`.</span><span class="sxs-lookup"><span data-stu-id="5bfa7-102">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="5bfa7-103">Если вы включите код языкового стандарта в ссылку на содержимое на английском языке, он также будет включен в локализованные ссылки, в результате чего эффективность локализации будет поставлена под сомнение.</span><span class="sxs-lookup"><span data-stu-id="5bfa7-103">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="5bfa7-104">Например, если ссылка на локализованное содержимое на русском языке содержит код `en-us`, пользователи из России будут переходить по ней к статье на английском языке даже в том случае, если будет доступна русскоязычная версия публикации.</span><span class="sxs-lookup"><span data-stu-id="5bfa7-104">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="5bfa7-105">Удалите коды языковых стандартов из ссылок на сайты Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="5bfa7-105">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="5bfa7-106">Ниже приведен пример:</span><span class="sxs-lookup"><span data-stu-id="5bfa7-106">The following is an example.</span></span>

<span data-ttu-id="5bfa7-107">До:</span><span class="sxs-lookup"><span data-stu-id="5bfa7-107">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="5bfa7-108">После:</span><span class="sxs-lookup"><span data-stu-id="5bfa7-108">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="5bfa7-109">В область этой проверки входят следующие сайты:</span><span class="sxs-lookup"><span data-stu-id="5bfa7-109">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="5bfa7-110">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="5bfa7-110">azure.microsoft.com</span></span>
- <span data-ttu-id="5bfa7-111">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="5bfa7-111">docs.microsoft.com</span></span>
- <span data-ttu-id="5bfa7-112">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="5bfa7-112">msdn.microsoft.com</span></span>
- <span data-ttu-id="5bfa7-113">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="5bfa7-113">technet.microsoft.com</span></span>