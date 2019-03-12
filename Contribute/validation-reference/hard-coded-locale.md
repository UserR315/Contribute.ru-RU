---
title: hard-coded-locale
description: Объяснение проблемы со сборкой документов hard-coded-locale и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 1862014076fa4cbff18535095b244e8f94a17b0f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427676"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="94bdf-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="94bdf-103">hard-coded-locale</span></span>

## <a name="warning"></a><span data-ttu-id="94bdf-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="94bdf-104">Warning</span></span>

`Link {URL} contains locale code {code}. For localizability, remove {code} from links to Microsoft sites.`

<span data-ttu-id="94bdf-105">Ссылки на некоторые сайты Майкрософт не должны содержать коды языкового стандарта, такие как `en-us`.</span><span class="sxs-lookup"><span data-stu-id="94bdf-105">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="94bdf-106">Если вы включите код языкового стандарта в ссылку на содержимое на английском языке, он также будет включен в локализованные ссылки, в результате чего эффективность локализации будет поставлена под сомнение.</span><span class="sxs-lookup"><span data-stu-id="94bdf-106">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="94bdf-107">Например, если ссылка на локализованное содержимое на русском языке содержит код `en-us`, пользователи из России будут переходить по ней к статье на английском языке даже в том случае, если будет доступна русскоязычная версия публикации.</span><span class="sxs-lookup"><span data-stu-id="94bdf-107">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="94bdf-108">В область этой проверки входят следующие сайты:</span><span class="sxs-lookup"><span data-stu-id="94bdf-108">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="94bdf-109">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="94bdf-109">azure.microsoft.com</span></span>
- <span data-ttu-id="94bdf-110">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="94bdf-110">docs.microsoft.com</span></span>
- <span data-ttu-id="94bdf-111">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="94bdf-111">msdn.microsoft.com</span></span>
- <span data-ttu-id="94bdf-112">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="94bdf-112">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="94bdf-113">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="94bdf-113">Resolution</span></span>

<span data-ttu-id="94bdf-114">Удалите коды языковых стандартов из ссылок на сайты Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="94bdf-114">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="94bdf-115">Ниже приведен пример:</span><span class="sxs-lookup"><span data-stu-id="94bdf-115">The following is an example.</span></span>

<span data-ttu-id="94bdf-116">До:</span><span class="sxs-lookup"><span data-stu-id="94bdf-116">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="94bdf-117">После:</span><span class="sxs-lookup"><span data-stu-id="94bdf-117">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]