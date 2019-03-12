---
title: manager-missing
description: Объяснение проблемы со сборкой документов manager-missing и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 16da241a21d400d5a5dfb101e247e55d95567485
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427823"
---
# <a name="manager-missing"></a><span data-ttu-id="da61d-103">manager-missing</span><span class="sxs-lookup"><span data-stu-id="da61d-103">manager-missing</span></span>

<span data-ttu-id="da61d-104">**Ожидается в ближайшее время.**</span><span class="sxs-lookup"><span data-stu-id="da61d-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="da61d-105">Предложение</span><span class="sxs-lookup"><span data-stu-id="da61d-105">Suggestion</span></span>

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

<span data-ttu-id="da61d-106">Для определения руководителя автора в некоторых группах содержимого требуется атрибут `manager`.</span><span class="sxs-lookup"><span data-stu-id="da61d-106">Some content groups require the `manager` attribute to identify the author's manager.</span></span>

## <a name="resolution"></a><span data-ttu-id="da61d-107">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="da61d-107">Resolution</span></span>

<span data-ttu-id="da61d-108">Добавьте допустимый псевдоним Майкрософт в качестве значения атрибута `manager`.</span><span class="sxs-lookup"><span data-stu-id="da61d-108">Add a valid Microsoft alias for `manager`:</span></span>

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
