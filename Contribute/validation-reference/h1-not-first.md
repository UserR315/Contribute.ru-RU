---
title: h1-not-first
description: Объяснение проблемы со сборкой Документации h1-not-first и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: c5e2eeeb5c464cd2923e23110cdab9a83324e53e
ms.sourcegitcommit: 89ec9772d9cc8281c633833c6fa51f629e9cd566
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/11/2019
ms.locfileid: "70895469"
---
# <a name="h1-not-first"></a><span data-ttu-id="b4cad-103">h1-not-first</span><span class="sxs-lookup"><span data-stu-id="b4cad-103">h1-not-first</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="b4cad-104">Предложение</span><span class="sxs-lookup"><span data-stu-id="b4cad-104">Suggestion</span></span>

`Markdown content is not allowed before H1.`

<span data-ttu-id="b4cad-105">Перед H1 в файле Markdown может располагаться только заголовок метаданных YAML.</span><span class="sxs-lookup"><span data-stu-id="b4cad-105">Only the YAML metadata header can come before the H1 in a Markdown file.</span></span> <span data-ttu-id="b4cad-106">Например, если вы хотите добавить заметку или изображение в верхней части статьи, они должны располагаться после H1.</span><span class="sxs-lookup"><span data-stu-id="b4cad-106">For example, if you want to add a note or an image at the top of the article, it must come after H1.</span></span> <span data-ttu-id="b4cad-107">Способ, использующийся в примере ниже, запрещен:</span><span class="sxs-lookup"><span data-stu-id="b4cad-107">The following is not allowed:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

<span data-ttu-id="b4cad-108">Правильно делать так:</span><span class="sxs-lookup"><span data-stu-id="b4cad-108">Do this instead:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

<span data-ttu-id="b4cad-109">Другой распространенной причиной этой проблемы являются [метки порядка байтов (BOM)](http://www.websina.com/bugzero/kb/unicode-bom.html) перед заголовком YAML.</span><span class="sxs-lookup"><span data-stu-id="b4cad-109">Another common cause of this issue is [byte order marks (BOMs)](http://www.websina.com/bugzero/kb/unicode-bom.html) before the YAML header.</span></span> <span data-ttu-id="b4cad-110">Иногда они возникают из-за проблем с кодированием при фиксации содержимого в репозиториях.</span><span class="sxs-lookup"><span data-stu-id="b4cad-110">These are sometimes introduced by encoding issues when committing content to repos.</span></span> <span data-ttu-id="b4cad-111">Метки порядка байтов приводят к неправильной отрисовке в GitHub, и их следует удалить.</span><span class="sxs-lookup"><span data-stu-id="b4cad-111">They result in bad rendering in GitHub and should be removed.</span></span>

## <a name="resolution"></a><span data-ttu-id="b4cad-112">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="b4cad-112">Resolution</span></span>

<span data-ttu-id="b4cad-113">Удалите все содержимое, кроме заголовка метаданных YAML, из кода, находящегося перед H1.</span><span class="sxs-lookup"><span data-stu-id="b4cad-113">Remove any content other than the YAML metadata header from before the H1.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
