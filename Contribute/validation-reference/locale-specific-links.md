---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
title: Зависящие от языкового стандарта ссылки
ms.openlocfilehash: f42a26da45b48972bfc595cb26c67ab0acfe8603
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/12/2019
ms.locfileid: "66841245"
---
# <a name="locale-specific-links"></a><span data-ttu-id="4a2e0-102">Зависящие от языкового стандарта ссылки</span><span class="sxs-lookup"><span data-stu-id="4a2e0-102">Locale-specific links</span></span>

<span data-ttu-id="4a2e0-103">Ссылки на некоторые сайты Майкрософт не должны содержать коды языкового стандарта, такие как `en-us`.</span><span class="sxs-lookup"><span data-stu-id="4a2e0-103">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="4a2e0-104">Если вы включите код языкового стандарта в ссылку на содержимое на английском языке, он также будет включен в локализованные ссылки, в результате чего эффективность локализации будет поставлена под сомнение.</span><span class="sxs-lookup"><span data-stu-id="4a2e0-104">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="4a2e0-105">Например, если ссылка на локализованное содержимое на русском языке содержит код `en-us`, пользователи из России будут переходить по ней к статье на английском языке даже в том случае, если будет доступна русскоязычная версия публикации.</span><span class="sxs-lookup"><span data-stu-id="4a2e0-105">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="4a2e0-106">Удалите коды языковых стандартов из ссылок на сайты Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="4a2e0-106">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="4a2e0-107">Ниже приведен пример:</span><span class="sxs-lookup"><span data-stu-id="4a2e0-107">The following is an example.</span></span>

<span data-ttu-id="4a2e0-108">До:</span><span class="sxs-lookup"><span data-stu-id="4a2e0-108">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="4a2e0-109">После:</span><span class="sxs-lookup"><span data-stu-id="4a2e0-109">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="4a2e0-110">В область этой проверки входят следующие сайты:</span><span class="sxs-lookup"><span data-stu-id="4a2e0-110">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="4a2e0-111">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="4a2e0-111">azure.microsoft.com</span></span>
- <span data-ttu-id="4a2e0-112">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="4a2e0-112">docs.microsoft.com</span></span>
- <span data-ttu-id="4a2e0-113">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="4a2e0-113">msdn.microsoft.com</span></span>
- <span data-ttu-id="4a2e0-114">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="4a2e0-114">technet.microsoft.com</span></span>