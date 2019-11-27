---
title: h1-no-space
description: Объяснение и решение проблемы со сборкой документов h1-no-space.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7058367a6edd7f663ea42a4fc2e9fafd9cbfb34f
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528962"
---
# <a name="h1-no-space"></a><span data-ttu-id="4ea17-103">h1-no-space</span><span class="sxs-lookup"><span data-stu-id="4ea17-103">h1-no-space</span></span>

## <a name="warning"></a><span data-ttu-id="4ea17-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="4ea17-104">Warning</span></span>

`A space is required after the hash (#) in H1.`

<span data-ttu-id="4ea17-105">H1 — это первый заголовок в файле Markdown.</span><span class="sxs-lookup"><span data-stu-id="4ea17-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="4ea17-106">При публикации на веб-сайте docs.microsoft.com заголовок H1 отображается крупным шрифтом в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="4ea17-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="4ea17-107">Для создания заголовка H1 необходимо указать в начале строки один символ решетки (#), после которого следует пробел и текст заголовка.</span><span class="sxs-lookup"><span data-stu-id="4ea17-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="4ea17-108">Без пробела после символа решетки заголовок H1 не будет распознаваться на веб-сайте документации.</span><span class="sxs-lookup"><span data-stu-id="4ea17-108">Without the space after the hash, Docs will not recognize an H1.</span></span>

## <a name="resolution"></a><span data-ttu-id="4ea17-109">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="4ea17-109">Resolution</span></span>

<span data-ttu-id="4ea17-110">Чтобы устранить эту ошибку, добавьте в заголовке H1 пробел после символа решетки.</span><span class="sxs-lookup"><span data-stu-id="4ea17-110">To fix this error, add a space after the hash in your H1.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
