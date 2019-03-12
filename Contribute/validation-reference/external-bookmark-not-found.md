---
title: external-bookmark-not-found
description: Объяснение проблемы со сборкой документов external-bookmark-not-found и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: b533a463ac38d6445ab84c74bf14b2065a0a63f3
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427776"
---
# <a name="external-bookmark-not-found"></a><span data-ttu-id="4ae25-103">external-bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="4ae25-103">external-bookmark-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="4ae25-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="4ae25-104">Warning</span></span>

`File '{file name}' doesn't contain a bookmark named '{bookmark text}'.`

<span data-ttu-id="4ae25-105">Вы пытаетесь добавить ссылку на несуществующий заголовок в другом файле.</span><span class="sxs-lookup"><span data-stu-id="4ae25-105">You're trying to link to a heading in another file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="4ae25-106">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="4ae25-106">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="4ae25-107">Проверьте файл, ссылку на который вы добавляете, и измените ссылку-закладку так, чтобы она указывала на допустимый раздел в файле.</span><span class="sxs-lookup"><span data-stu-id="4ae25-107">Review the file you're linking to and update your bookmark link to point to a valid section in the file.</span></span>

<span data-ttu-id="4ae25-108">Чтобы добавить ссылку на заголовок раздела в другой статье, используйте относительную ссылку на файл или сайт, после которой укажите символ решетки и текст заголовка.</span><span class="sxs-lookup"><span data-stu-id="4ae25-108">To link to a section heading in another article, use the file-relative or site-relative link plus a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="4ae25-109">Удалите знаки препинания из заголовка и замените пробелы дефисами.</span><span class="sxs-lookup"><span data-stu-id="4ae25-109">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="4ae25-110">Ниже приведен пример.</span><span class="sxs-lookup"><span data-stu-id="4ae25-110">The following is an example:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
