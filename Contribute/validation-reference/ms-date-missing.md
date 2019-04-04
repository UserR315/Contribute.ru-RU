---
title: ms-date-missing
description: Объяснение и устранение проблем сборки документов ms-date-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: ae2a28993671255a9ffd4503eebdbee404e52373
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637283"
---
# <a name="ms-date-missing"></a>ms-date-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Предложение

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

Для некоторых групп содержимого требуется атрибут `ms.date`, который используется, чтобы показать актуальность, то есть когда содержимое статьи последний раз проверялось на соответствие, точность, правильность снимков экрана и правильную работу ссылок. Она не соответствует дате последней *публикации* статьи, которая будет показана на странице, если `ms.date` не указано явно.

## <a name="resolution"></a>Способы устранения

Убедитесь, что статья актуальна и в ней отсутствует испорченное содержимое, и добавьте допустимую дату в формате ММ/ДД/ГГГГ.

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
