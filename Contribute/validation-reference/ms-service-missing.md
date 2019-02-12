---
title: ms-service-missing
description: Объяснение и устранение проблем сборки документов ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2bc425726f82840565978072b2efdf13a1284ec0
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713092"
---
# <a name="ms-service-missing"></a>ms-service-missing

**Ожидается в ближайшее время.**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Предложение

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

Используйте `ms.service`, чтобы указать облачные службы. Чтобы указать более подробные сведения об `ms.service`, вы можете дополнительно указать `ms.subservice`, но вместе с ним нужно также указать `ms.service`. Пара значений `ms.service` и `ms.subservice` должна быть допустимой.

## <a name="resolution"></a>Способы устранения

Убедитесь, что указанное значение `ms.subservice` подходит для вашей статьи. Затем добавьте соответствующее значение `ms.service`, которое является родительским для `ms.subservice`.

Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/whitelists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
