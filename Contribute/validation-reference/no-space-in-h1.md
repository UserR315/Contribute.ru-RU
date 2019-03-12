---
title: no-space-in-h1
description: Объяснение проблемы со сборкой документов issue no-space-in-h1 и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 8c719a89e6373fb960f216a5b4ec01c6d1739a28
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427843"
---
# <a name="no-space-in-h1"></a><span data-ttu-id="30b95-103">no-space-in-h1</span><span class="sxs-lookup"><span data-stu-id="30b95-103">no-space-in-h1</span></span>

## <a name="warning"></a><span data-ttu-id="30b95-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="30b95-104">Warning</span></span>

`A space is required after the hash (#) in H1.`

<span data-ttu-id="30b95-105">H1 — это первый заголовок в файле Markdown.</span><span class="sxs-lookup"><span data-stu-id="30b95-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="30b95-106">При публикации на веб-сайте docs.microsoft.com заголовок H1 отображается крупным шрифтом в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="30b95-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="30b95-107">Для создания заголовка H1 необходимо указать в начале строки один символ решетки (#), после которого следует пробел и текст заголовка.</span><span class="sxs-lookup"><span data-stu-id="30b95-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="30b95-108">Без пробела после символа решетки заголовок H1 не будет распознаваться на веб-сайте документации.</span><span class="sxs-lookup"><span data-stu-id="30b95-108">Without the space after the hash, Docs will not recognize an H1.</span></span>

## <a name="resolution"></a><span data-ttu-id="30b95-109">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="30b95-109">Resolution</span></span>

<span data-ttu-id="30b95-110">Чтобы устранить эту ошибку, добавьте в заголовке H1 пробел после символа решетки.</span><span class="sxs-lookup"><span data-stu-id="30b95-110">To fix this error, add a space after the hash in your H1.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]