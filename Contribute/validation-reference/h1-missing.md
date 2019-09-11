---
title: h1-missing
description: Объяснение проблемы со сборкой документов h1-missing и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 677127d09349445bb80778dfb501d7d4294ea46b
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848485"
---
# <a name="h1-missing"></a><span data-ttu-id="aeb96-103">h1-missing</span><span class="sxs-lookup"><span data-stu-id="aeb96-103">h1-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="aeb96-104">Предложение</span><span class="sxs-lookup"><span data-stu-id="aeb96-104">Suggestion</span></span>

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

<span data-ttu-id="aeb96-105">H1 — это первый заголовок в файле Markdown.</span><span class="sxs-lookup"><span data-stu-id="aeb96-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="aeb96-106">При публикации на веб-сайте docs.microsoft.com заголовок H1 отображается крупным шрифтом в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="aeb96-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="aeb96-107">Для создания заголовка H1 необходимо указать в начале строки один символ решетки (#), после которого следует пробел и текст заголовка.</span><span class="sxs-lookup"><span data-stu-id="aeb96-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="aeb96-108">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="aeb96-108">Resolution</span></span>

<span data-ttu-id="aeb96-109">Чтобы устранить эту проблему, добавьте заголовок H1 сразу после блока метаданных YML в файле:</span><span class="sxs-lookup"><span data-stu-id="aeb96-109">To fix this issue, add an H1 as the first content after the YML metadata block in your file:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> <span data-ttu-id="aeb96-110">Это правило не применяется к включаемым файлам.</span><span class="sxs-lookup"><span data-stu-id="aeb96-110">This rule does not apply to included files.</span></span> <span data-ttu-id="aeb96-111">Если предупреждения, касающиеся заголовка H1, выводятся для включаемых файлов, скорее всего, необходимо переместить эти файлы в папку `includes`.</span><span class="sxs-lookup"><span data-stu-id="aeb96-111">If you get H1 warnings on included files, you most likely need to move your included files into an `includes` folder.</span></span> <span data-ttu-id="aeb96-112">Папка `includes` может находиться на любом уровне в пути к файлу.</span><span class="sxs-lookup"><span data-stu-id="aeb96-112">The `includes` folder can be at any level in the file path.</span></span> <span data-ttu-id="aeb96-113">При ее наличии в пути система сборки документов распознает файл как включаемый и проверки заголовка H1 выполняться не будут.</span><span class="sxs-lookup"><span data-stu-id="aeb96-113">Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]