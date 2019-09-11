---
title: author-missing
description: Объяснение и устранение проблем сборки документов author-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 904ec2ad495945d882e581a240f6a72ca650c37e
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848579"
---
# <a name="author-missing"></a><span data-ttu-id="c3e19-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="c3e19-103">author-missing</span></span>

## <a name="warning"></a><span data-ttu-id="c3e19-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="c3e19-104">Warning</span></span>

`Missing attribute: author. Add the current author's GitHub ID.`

<span data-ttu-id="c3e19-105">Атрибут `author` определяет автора статьи по идентификатору GitHub.</span><span class="sxs-lookup"><span data-stu-id="c3e19-105">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="c3e19-106">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="c3e19-106">Resolution</span></span>

<span data-ttu-id="c3e19-107">Добавьте идентификатор текущего автора на GitHub к заголовку YML:</span><span class="sxs-lookup"><span data-stu-id="c3e19-107">Add the current author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<span data-ttu-id="c3e19-108">Обратите внимание, что это должен быть *текущий* владелец статьи, а не первоначальный автор, если владелец менялся.</span><span class="sxs-lookup"><span data-stu-id="c3e19-108">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
