---
title: ms-author-invalid
description: Объяснение проблемы со сборкой документов ms-author-invalid и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 210ff6a18bd12585c81f461a87238aa8d20c0530
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427856"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="a98fd-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="a98fd-103">ms-author-invalid</span></span>

<span data-ttu-id="a98fd-104">**Ожидается в ближайшее время.**</span><span class="sxs-lookup"><span data-stu-id="a98fd-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="a98fd-105">Предложение</span><span class="sxs-lookup"><span data-stu-id="a98fd-105">Suggestion</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not a whitelisted distribution list.`

## <a name="resolution"></a><span data-ttu-id="a98fd-106">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="a98fd-106">Resolution</span></span>

<span data-ttu-id="a98fd-107">Проверьте, является ли значение `ms.author` допустимым псевдонимом Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="a98fd-107">Verify that the `ms.author` value is a valid Microsoft alias.</span></span> <span data-ttu-id="a98fd-108">Если псевдоним используется для списка рассылки, он должен быть добавлен в список разрешенных.</span><span class="sxs-lookup"><span data-stu-id="a98fd-108">If the alias is a distribution list, it must also be whitelisted.</span></span>

<span data-ttu-id="a98fd-109">Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="a98fd-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
