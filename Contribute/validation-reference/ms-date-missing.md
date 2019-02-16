---
title: ms-date-missing
description: Объяснение и устранение проблем сборки документов ms-date-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: f5603dee7efe5c7ce3eaa4fa944031d94a9283d8
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713253"
---
# <a name="ms-date-missing"></a><span data-ttu-id="50ade-103">ms-date-missing</span><span class="sxs-lookup"><span data-stu-id="50ade-103">ms-date-missing</span></span>

<span data-ttu-id="50ade-104">**Ожидается в ближайшее время.**</span><span class="sxs-lookup"><span data-stu-id="50ade-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="50ade-105">Предложение</span><span class="sxs-lookup"><span data-stu-id="50ade-105">Suggestion</span></span>

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

<span data-ttu-id="50ade-106">Эта дата означала актуальность, то есть когда содержимое статьи последний раз проверялось на соответствие, точность, правильность снимков экрана и правильную работу ссылок.</span><span class="sxs-lookup"><span data-stu-id="50ade-106">This date is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="50ade-107">Она не соответствует дате последней *публикации* статьи, которая будет показана на странице, если `ms.date` не указано явно.</span><span class="sxs-lookup"><span data-stu-id="50ade-107">This is not the same as the last date the article was *published*, which will show on the page if `ms.date` is not explicitly specified.</span></span>

## <a name="resolution"></a><span data-ttu-id="50ade-108">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="50ade-108">Resolution</span></span>

<span data-ttu-id="50ade-109">Убедитесь, что статья актуальна и в ней отсутствует неправильно работающее содержимое, и добавьте допустимую дату в формате ММ/ДД/ГГГГ.</span><span class="sxs-lookup"><span data-stu-id="50ade-109">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]