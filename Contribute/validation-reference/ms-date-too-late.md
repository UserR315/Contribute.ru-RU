---
title: ms-date-too-late
description: Объяснение и устранение проблем сборки документов ms-date-too-late
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4cb5da1da2fee59302791e729e5fcfb8e84170e5
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637398"
---
# <a name="ms-date-too-late"></a>ms-date-too-late

## <a name="warning"></a>Предупреждение

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

Атрибут `ms.date` используется, чтобы показать актуальность, то есть когда содержимое статьи последний раз проверялось на соответствие, точность, правильность снимков экрана и правильную работу ссылок. Таким образом, этот атрибут нельзя указать в будущем. У учетной записи есть пять дней для выпуска, например, когда содержимое заморожено для контроля качества при подготовке к крупному событию.

## <a name="resolution"></a>Способы устранения

В качестве значения `ms.date` укажите дату, не менее чем на 5 дней отстающую от текущей, в формате ММ/ДД/ГГГГ:

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
