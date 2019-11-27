---
title: multiple-h1s
description: Пояснение и решение проблемы сборки Docs с multiple-h1s.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: e2912066895494e221181f2de2bb117ff9ed1636
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528945"
---
# <a name="multiple-h1s"></a><span data-ttu-id="5c3fa-103">multiple-h1s</span><span class="sxs-lookup"><span data-stu-id="5c3fa-103">multiple-h1s</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="5c3fa-104">Предложение</span><span class="sxs-lookup"><span data-stu-id="5c3fa-104">Suggestion</span></span>

`Multiple H1s are not allowed. You can only have one top-level heading.`

<span data-ttu-id="5c3fa-105">H1 — это первый заголовок в файле Markdown.</span><span class="sxs-lookup"><span data-stu-id="5c3fa-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="5c3fa-106">При публикации на веб-сайте docs.microsoft.com заголовок H1 отображается крупным шрифтом в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="5c3fa-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="5c3fa-107">Для создания заголовка H1 необходимо указать в начале строки один символ решетки (#), после которого следует пробел и текст заголовка.</span><span class="sxs-lookup"><span data-stu-id="5c3fa-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="5c3fa-108">В каждом файле может быть только один заголовок H1.</span><span class="sxs-lookup"><span data-stu-id="5c3fa-108">You can only have one H1 in each file.</span></span>

<span data-ttu-id="5c3fa-109">Кроме того, это сообщение можно получить, если статья содержит строку, состоящую из знаков равенства, которые образуют двойное подчеркивание, например: `=======`.</span><span class="sxs-lookup"><span data-stu-id="5c3fa-109">You might also get this message if your article contains a line of equals signs making a double underline, like this: `=======`.</span></span> <span data-ttu-id="5c3fa-110">Это альтернативный синтаксис Markdown для заголовков H1.</span><span class="sxs-lookup"><span data-stu-id="5c3fa-110">This is an alternative Markdown syntax for an H1.</span></span> <span data-ttu-id="5c3fa-111">Он также часто встречается в конфликтах слияния:</span><span class="sxs-lookup"><span data-stu-id="5c3fa-111">It's also commonly seen in merge conflicts:</span></span>

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a><span data-ttu-id="5c3fa-112">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="5c3fa-112">Resolution</span></span>

<span data-ttu-id="5c3fa-113">Чтобы устранить эту проблему, измените уровень последующих заголовков H1 на H2 (`##`) либо реорганизуйте файл.</span><span class="sxs-lookup"><span data-stu-id="5c3fa-113">To fix this issue, change the heading level of subsequent H1s to H2 (`##`), or otherwise reorganize your file.</span></span> <span data-ttu-id="5c3fa-114">Обратите внимание на то, что пропускать уровни заголовков, например указывать H3 сразу после H1, запрещено.</span><span class="sxs-lookup"><span data-stu-id="5c3fa-114">Note that skipping heading levels, such as following H1 with H3, isn't allowed.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<span data-ttu-id="5c3fa-115">Если дополнительный заголовок H1 фактически является двойным подчеркиванием (`=======`), удалите его или замените на заголовок из хэштегов, например `##`, в зависимости от ситуации.</span><span class="sxs-lookup"><span data-stu-id="5c3fa-115">If an additional H1 is actually a double underline (`=======`), remove it or replace it with a hashtag heading, such as `##`, as appropriate.</span></span> <span data-ttu-id="5c3fa-116">Если двойное подчеркивание является частью конфликта слияния, необходимо также удалить начальный и конечный маркеры конфликта слияния и устаревший текст.</span><span class="sxs-lookup"><span data-stu-id="5c3fa-116">If the double underline is part of a merge conflict, make sure to also remove the merge conflict beginning and ending markers and the obsolete text.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
