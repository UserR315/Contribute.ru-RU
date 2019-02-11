---
title: ms-date-too-late
description: Объяснение и устранение проблем сборки документов ms-date-too-late
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 863b13e55c2aaa2057920e3bd77ec75ab5945277
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713115"
---
# <a name="ms-date-too-late"></a>ms-date-too-late

**Ожидается в ближайшее время.**

## <a name="warning"></a>Предупреждение

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

Атрибут `ms.date` используется, чтобы показать актуальность, то есть когда содержимое статьи последний раз проверялось на соответствие, точность, правильность снимков экрана и правильную работу ссылок. Таким образом, этот атрибут нельзя указать в будущем. У учетной записи есть пять дней для выпуска, например, когда содержимое заморожено для контроля качества при подготовке к крупному событию.

## <a name="resolution"></a>Способы устранения

В качестве значения `ms.date` укажите дату, не менее чем на 5 дней отстающую от текущей, в формате ММ/ДД/ГГГГ.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
