---
title: block-section-invalid
description: Объяснение проблемы со сборкой документов block-section-invalid и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 257b963ae37f5a8f0edc2fbca6186ab0f258cfc0
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427887"
---
# <a name="block-section-invalid"></a><span data-ttu-id="86bab-103">block-section-invalid</span><span class="sxs-lookup"><span data-stu-id="86bab-103">block-section-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="86bab-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="86bab-104">Warning</span></span>

`Invalid syntax for alert, div, or video. The text will be rendered as a block quote.`

<span data-ttu-id="86bab-105">Несколько расширений Markdown для документов начинаются со строки `> [!`.</span><span class="sxs-lookup"><span data-stu-id="86bab-105">Several Docs Markdown extensions begin with the string `> [!`.</span></span> <span data-ttu-id="86bab-106">Между символами `>` и `[` требуется пробел. Кроме того, необходима закрывающая скобка `]`.</span><span class="sxs-lookup"><span data-stu-id="86bab-106">A space is required between `>` and `[`, and there must be a closing `]`.</span></span> <span data-ttu-id="86bab-107">Если синтаксис неверен, текст будет отображаться в виде цитаты.</span><span class="sxs-lookup"><span data-stu-id="86bab-107">If the syntax is incorrect, the text will be rendered as a block quote.</span></span>

## <a name="resolution"></a><span data-ttu-id="86bab-108">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="86bab-108">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="86bab-109">Убедитесь в том, что расширение имеет правильный синтаксис:</span><span class="sxs-lookup"><span data-stu-id="86bab-109">Ensure the syntax is correct for the extension you're using:</span></span>

```markdown

Alerts:

> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.

Videos:

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

Sections (div):

> [!div class="class"]

```


<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
