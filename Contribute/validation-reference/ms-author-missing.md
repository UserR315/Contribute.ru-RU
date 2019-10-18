---
title: ms-author-missing
description: Объяснение и устранение проблем сборки документов ms-author-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6b313bd6b168b913d82721607126fcd4e6255009
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246254"
---
# <a name="ms-author-missing"></a>ms-author-missing

## <a name="warning"></a>Предупреждение

`Missing attribute: ms.author. Add the current author's Microsoft alias.`

## <a name="resolution"></a>Способы устранения

Укажите псевдоним Майкрософт текущего автора в качестве значения `ms.author`. Обратите внимание, что это должен быть *текущий* владелец статьи, а не первоначальный автор, если владелец менялся. В качестве автора рекомендуется задавать сотрудника с полной занятостью или командный список рассылки, а не временного поставщика. 

Если псевдоним является списком рассылки, он также должен быть в списке разрешений `ms.author`.

Допустимые значения для списков рассылки `ms.author` см. на [этом внутреннем сайте Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
