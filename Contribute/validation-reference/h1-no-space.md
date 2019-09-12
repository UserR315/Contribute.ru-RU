---
title: h1-no-space
description: Объяснение и решение проблемы со сборкой документов h1-no-space.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 7dd6a3d5cfc6def000d5bf7a5bf7810a16625cae
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2019
ms.locfileid: "70856250"
---
# <a name="h1-no-space"></a><span data-ttu-id="5aae3-103">h1-no-space</span><span class="sxs-lookup"><span data-stu-id="5aae3-103">h1-no-space</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="5aae3-104">Предложение</span><span class="sxs-lookup"><span data-stu-id="5aae3-104">Suggestion</span></span>

`A space is required after the hash (#) in H1.`

<span data-ttu-id="5aae3-105">H1 — это первый заголовок в файле Markdown.</span><span class="sxs-lookup"><span data-stu-id="5aae3-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="5aae3-106">При публикации на веб-сайте docs.microsoft.com заголовок H1 отображается крупным шрифтом в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="5aae3-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="5aae3-107">Для создания заголовка H1 необходимо указать в начале строки один символ решетки (#), после которого следует пробел и текст заголовка.</span><span class="sxs-lookup"><span data-stu-id="5aae3-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="5aae3-108">Без пробела после символа решетки заголовок H1 не будет распознаваться на веб-сайте документации.</span><span class="sxs-lookup"><span data-stu-id="5aae3-108">Without the space after the hash, Docs will not recognize an H1.</span></span>

## <a name="resolution"></a><span data-ttu-id="5aae3-109">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="5aae3-109">Resolution</span></span>

<span data-ttu-id="5aae3-110">Чтобы устранить эту ошибку, добавьте в заголовке H1 пробел после символа решетки.</span><span class="sxs-lookup"><span data-stu-id="5aae3-110">To fix this error, add a space after the hash in your H1.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
