---
title: ms-author-invalid
description: Объяснение проблемы со сборкой документов ms-author-invalid и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: b3100b4a304356aee3c50f805628890b8c738fe1
ms.sourcegitcommit: d2f5b68b6a6d1ac902dba5063482ff5955a5b1f7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2019
ms.locfileid: "71481694"
---
# <a name="ms-author-invalid"></a>ms-author-invalid

## <a name="warning"></a>Предупреждение

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a>Способы устранения

Проверьте, что значение `ms.author` является допустимым псевдонимом Майкрософт текущего автора. В качестве автора рекомендуется задавать сотрудника с полной занятостью или командный список рассылки, а не временного поставщика. Если псевдоним является списком рассылки, он также должен быть в списке разрешений `ms.author`.

Допустимые значения для списков рассылки `ms.author` см. на [этом внутреннем сайте Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
