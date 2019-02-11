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
# <a name="ms-date-missing"></a>ms-date-missing

**Ожидается в ближайшее время.**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Предложение

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

Эта дата означала актуальность, то есть когда содержимое статьи последний раз проверялось на соответствие, точность, правильность снимков экрана и правильную работу ссылок. Она не соответствует дате последней *публикации* статьи, которая будет показана на странице, если `ms.date` не указано явно.

## <a name="resolution"></a>Способы устранения

Убедитесь, что статья актуальна и в ней отсутствует неправильно работающее содержимое, и добавьте допустимую дату в формате ММ/ДД/ГГГГ.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
