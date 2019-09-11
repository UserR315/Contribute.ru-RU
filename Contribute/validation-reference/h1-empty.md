---
title: h1-empty
description: Объяснение проблемы со сборкой документов h1-empty и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 691d72a3aee9204ba3fe55a398e954c7719f3680
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848552"
---
# <a name="h1-empty"></a><span data-ttu-id="eaf3d-103">h1-empty</span><span class="sxs-lookup"><span data-stu-id="eaf3d-103">h1-empty</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="eaf3d-104">Предложение</span><span class="sxs-lookup"><span data-stu-id="eaf3d-104">Suggestion</span></span>

`H1 is required. Add content to your top-level heading.`

<span data-ttu-id="eaf3d-105">H1 — это первый заголовок в файле Markdown.</span><span class="sxs-lookup"><span data-stu-id="eaf3d-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="eaf3d-106">При публикации на веб-сайте docs.microsoft.com заголовок H1 отображается крупным шрифтом в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="eaf3d-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="eaf3d-107">Для создания заголовка H1 необходимо указать в начале строки один символ решетки (#), после которого следует пробел и текст заголовка.</span><span class="sxs-lookup"><span data-stu-id="eaf3d-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="eaf3d-108">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="eaf3d-108">Resolution</span></span>

<span data-ttu-id="eaf3d-109">Чтобы устранить эту проблему, убедитесь в том, что, помимо символа решетки, заголовок H1 также включает в себя содержимое.</span><span class="sxs-lookup"><span data-stu-id="eaf3d-109">To fix this issue, make sure your H1 includes content, not just a hash.</span></span>

<span data-ttu-id="eaf3d-110">Неверно:</span><span class="sxs-lookup"><span data-stu-id="eaf3d-110">Bad:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

<span data-ttu-id="eaf3d-111">Верно:</span><span class="sxs-lookup"><span data-stu-id="eaf3d-111">Good:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]