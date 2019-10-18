---
title: ms-author-invalid
description: Объяснение проблемы со сборкой документов ms-author-invalid и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: 615d9f5978893196a24e3a043f3b71a22e1eb353
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246292"
---
# <a name="ms-author-invalid"></a>ms-author-invalid

## <a name="warning"></a>Предупреждение

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a>Способы устранения

Измените значение `ms.author` на допустимый псевдоним Майкрософт текущего автора. В качестве автора рекомендуется задавать сотрудника с полной занятостью или командный список рассылки, а не временного поставщика. Если псевдоним является списком рассылки, он также должен быть в списке разрешений `ms.author`.

Допустимые значения для списков рассылки `ms.author` см. на [этом внутреннем сайте Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
