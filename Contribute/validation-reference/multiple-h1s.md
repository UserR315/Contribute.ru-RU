---
title: multiple-h1
description: Объяснение проблемы со сборкой документов multiple-h1 и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 55ce6260cb4d1e09f63e0540528576ed3fa165f8
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427900"
---
# <a name="multiple-h1"></a><span data-ttu-id="6b255-103">multiple-h1</span><span class="sxs-lookup"><span data-stu-id="6b255-103">multiple-h1</span></span>

## <a name="warning"></a><span data-ttu-id="6b255-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="6b255-104">Warning</span></span>

`Multiple H1s are not allowed. You can only have one top-level heading.`

<span data-ttu-id="6b255-105">H1 — это первый заголовок в файле Markdown.</span><span class="sxs-lookup"><span data-stu-id="6b255-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="6b255-106">При публикации на веб-сайте docs.microsoft.com заголовок H1 отображается крупным шрифтом в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="6b255-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="6b255-107">Для создания заголовка H1 необходимо указать в начале строки один символ решетки (#), после которого следует пробел и текст заголовка.</span><span class="sxs-lookup"><span data-stu-id="6b255-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="6b255-108">В каждом файле может быть только один заголовок H1.</span><span class="sxs-lookup"><span data-stu-id="6b255-108">You can only have one H1 in each file.</span></span>

## <a name="resolution"></a><span data-ttu-id="6b255-109">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="6b255-109">Resolution</span></span>

<span data-ttu-id="6b255-110">Чтобы устранить эту проблему, измените уровень последующих заголовков H1 на H2 (`##`) либо реорганизуйте файл.</span><span class="sxs-lookup"><span data-stu-id="6b255-110">To fix this issue, change the heading level of subsequent H1s to H2 (`##`), or otherwise reorganize your file.</span></span> <span data-ttu-id="6b255-111">Обратите внимание на то, что пропускать уровни заголовков, например указывать H3 сразу после H1, запрещено.</span><span class="sxs-lookup"><span data-stu-id="6b255-111">Note that skipping heading levels, such as following H1 with H3, is not allowed.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]