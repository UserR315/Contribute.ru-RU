---
title: ms-author-invalid
description: Объяснение проблемы со сборкой документов ms-author-invalid и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 5d4cc6a08c6e70824ee3f7117d58be9c75aa7fa4
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987774"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="bc6c8-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="bc6c8-103">ms-author-invalid</span></span>

<span data-ttu-id="bc6c8-104">**Ожидается в ближайшее время.**</span><span class="sxs-lookup"><span data-stu-id="bc6c8-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="bc6c8-105">Предложение</span><span class="sxs-lookup"><span data-stu-id="bc6c8-105">Suggestion</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="bc6c8-106">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="bc6c8-106">Resolution</span></span>

<span data-ttu-id="bc6c8-107">Проверьте, является ли значение `ms.author` допустимым псевдонимом Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="bc6c8-107">Verify that the `ms.author` value is a valid Microsoft alias.</span></span> <span data-ttu-id="bc6c8-108">Если псевдоним используется для списка рассылки, он должен быть добавлен в список разрешенных.</span><span class="sxs-lookup"><span data-stu-id="bc6c8-108">If the alias is a distribution list, it must also be on the allow list.</span></span>

<span data-ttu-id="bc6c8-109">Допустимые значения для списков рассылки см. на [этом внутреннем сайте Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="bc6c8-109">Valid values for DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
