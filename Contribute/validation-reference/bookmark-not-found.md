---
title: internal-bookmark-not-found
description: Объяснение проблемы со сборкой документов internal-bookmark-not-found и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 53b98f8da199e3495cc00b2388d983191268eee6
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2019
ms.locfileid: "70856227"
---
# <a name="bookmark-not-found"></a><span data-ttu-id="0fe4c-103">bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="0fe4c-103">bookmark-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="0fe4c-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="0fe4c-104">Warning</span></span>

`Cannot find bookmark '{bookmark-id}' in '{parent-file}'.`

<span data-ttu-id="0fe4c-105">Вы пытаетесь добавить ссылку на заголовок в текущем или другом файле, которого не существует.</span><span class="sxs-lookup"><span data-stu-id="0fe4c-105">You're trying to link to a heading in the current file or another file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="0fe4c-106">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="0fe4c-106">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="0fe4c-107">Проверьте заголовок, ссылку на который вы хотите добавить, и измените ссылку.</span><span class="sxs-lookup"><span data-stu-id="0fe4c-107">Verify the heading you want to link to and update the link.</span></span>

<span data-ttu-id="0fe4c-108">Чтобы добавить ссылку на раздел в текущей статье, используйте символ решетки, за которым следует текст заголовка.</span><span class="sxs-lookup"><span data-stu-id="0fe4c-108">To link to a section in the current article, use a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="0fe4c-109">Удалите знаки препинания из заголовка и замените пробелы дефисами.</span><span class="sxs-lookup"><span data-stu-id="0fe4c-109">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="0fe4c-110">Ниже приведен пример.</span><span class="sxs-lookup"><span data-stu-id="0fe4c-110">The following is an example:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="0fe4c-111">Чтобы добавить ссылку на заголовок в другом файле, используйте относительную ссылку на файл, после которой укажите символ решетки и текст заголовка.</span><span class="sxs-lookup"><span data-stu-id="0fe4c-111">To link to a heading in another file, use a relative link to that file, followed by a hash symbol and the words of the heading.</span></span> <span data-ttu-id="0fe4c-112">Удалите знаки препинания из заголовка и замените пробелы дефисами.</span><span class="sxs-lookup"><span data-stu-id="0fe4c-112">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="0fe4c-113">Ниже приведен пример.</span><span class="sxs-lookup"><span data-stu-id="0fe4c-113">The following is an example:</span></span>

```markdown
See [the Resolution section in h1-empty](h1-empty.md#resolution).
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
