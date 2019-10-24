---
title: hard-coded-locale
description: Объяснение проблемы со сборкой документов hard-coded-locale и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/18/2019
ms.prod: non-product-specific
ms.openlocfilehash: 0fbc7634e00202fdfdf607b9504744a6d9846792
ms.sourcegitcommit: 836d4d6127fabb5569ffc0809db5fb25e46038b5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2019
ms.locfileid: "72590874"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="fae38-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="fae38-103">hard-coded-locale</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fae38-104">Это правило изначально использовалось как "Предложение", чтобы дать командам по работе с содержимым время на оценку возможных последствий и разработку плана по очистке своих репозиториев.</span><span class="sxs-lookup"><span data-stu-id="fae38-104">This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos.</span></span> <span data-ttu-id="fae38-105">**Ему будет назначено состояние "Предупреждение" с 20 декабря 2019 г**.</span><span class="sxs-lookup"><span data-stu-id="fae38-105">**It will be elevated to a "Warning" on 12/20/2019**.</span></span>

## <a name="suggestion"></a><span data-ttu-id="fae38-106">Предложение</span><span class="sxs-lookup"><span data-stu-id="fae38-106">Suggestion</span></span>

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to Microsoft sites.`

<span data-ttu-id="fae38-107">Ссылки на некоторые сайты Майкрософт не должны содержать коды языкового стандарта, такие как `en-us`.</span><span class="sxs-lookup"><span data-stu-id="fae38-107">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="fae38-108">Если вы включите код языкового стандарта в ссылку на содержимое на английском языке, он также будет включен в локализованные ссылки, в результате чего эффективность локализации будет поставлена под сомнение.</span><span class="sxs-lookup"><span data-stu-id="fae38-108">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="fae38-109">Например, если ссылка на локализованное содержимое на русском языке содержит код `en-us`, пользователи из России будут переходить по ней к статье на английском языке даже в том случае, если будет доступна русскоязычная версия публикации.</span><span class="sxs-lookup"><span data-stu-id="fae38-109">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="fae38-110">В область этой проверки входят следующие сайты:</span><span class="sxs-lookup"><span data-stu-id="fae38-110">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="fae38-111">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="fae38-111">azure.microsoft.com</span></span>
- <span data-ttu-id="fae38-112">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="fae38-112">docs.microsoft.com</span></span>
- <span data-ttu-id="fae38-113">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="fae38-113">msdn.microsoft.com</span></span>
- <span data-ttu-id="fae38-114">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="fae38-114">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="fae38-115">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="fae38-115">Resolution</span></span>

<span data-ttu-id="fae38-116">Удалите коды языковых стандартов из ссылок на сайты Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="fae38-116">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="fae38-117">Ниже приведен пример:</span><span class="sxs-lookup"><span data-stu-id="fae38-117">The following is an example.</span></span>

<span data-ttu-id="fae38-118">До:</span><span class="sxs-lookup"><span data-stu-id="fae38-118">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="fae38-119">После:</span><span class="sxs-lookup"><span data-stu-id="fae38-119">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> <span data-ttu-id="fae38-120">Расширение Docs Markdown для VS Code включает в себя скрипт очистки для ссылок на сайты Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="fae38-120">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="fae38-121">Он проверяет все ссылки на сайты Майкрософт в репозитории на предмет того, что они начинаются с `https`, а не `http`, и не содержат коды языковых стандартов, например `en-us`.</span><span class="sxs-lookup"><span data-stu-id="fae38-121">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="fae38-122">Чтобы запустить этот скрипт, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="fae38-122">To run the script:</span></span>
>
> 1. <span data-ttu-id="fae38-123">Установите расширение [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) для VS Code.</span><span class="sxs-lookup"><span data-stu-id="fae38-123">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="fae38-124">Нажмите клавиши ALT+M, чтобы открыть меню Markdown.</span><span class="sxs-lookup"><span data-stu-id="fae38-124">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="fae38-125">Выберите пункт **Cleanup** (Очистка), а затем — **Microsoft links** (Ссылки на сайты Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="fae38-125">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
