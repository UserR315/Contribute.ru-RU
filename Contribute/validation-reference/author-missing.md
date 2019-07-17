---
title: author-missing
description: Объяснение и устранение проблем сборки документов author-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 33d704d64f4a3a1d96792bb01b403aefb3143eb8
ms.sourcegitcommit: 1311ccbbf38312bfe6947082870bc9e90d38c986
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/11/2019
ms.locfileid: "67791510"
---
# <a name="author-missing"></a><span data-ttu-id="63f25-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="63f25-103">author-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="63f25-104">Предложение</span><span class="sxs-lookup"><span data-stu-id="63f25-104">Suggestion</span></span>

`Missing attribute: author. Add the current author's GitHub ID.`

<span data-ttu-id="63f25-105">Атрибут `author` определяет автора статьи по идентификатору GitHub.</span><span class="sxs-lookup"><span data-stu-id="63f25-105">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="63f25-106">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="63f25-106">Resolution</span></span>

<span data-ttu-id="63f25-107">Добавьте идентификатор текущего автора на GitHub к заголовку YML:</span><span class="sxs-lookup"><span data-stu-id="63f25-107">Add the current author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<span data-ttu-id="63f25-108">Обратите внимание, что это должен быть *текущий* владелец статьи, а не первоначальный автор, если владелец менялся.</span><span class="sxs-lookup"><span data-stu-id="63f25-108">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
