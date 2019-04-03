---
title: ms-prod-service-mismatch
description: Объяснение и устранение проблем сборки документов ms-prod-service-mismatch
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a8d1698a4842ace0e5dd07db170f40a310c666a6
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636800"
---
# <a name="ms-prod-service-mismatch"></a>ms-prod-service-mismatch

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Предложение

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

Используйте `ms.prod`, чтобы указать локальные продукты для облачных служб `ms.service`. Чтобы указать более подробные сведения о `ms.prod`, вы можете дополнительно указать `ms.technology`. Чтобы указать более подробные сведения о `ms.service`, вы можете указать `ms.subservice`. Вы не можете использовать `ms.prod` с `ms.subservice` или `ms.service` с `ms.technology`.

## <a name="resolution"></a>Способы устранения

Сначала проверьте, что вы выбрали правильный родительский атрибут (`ms.prod` или `ms.service`) для статьи. Затем добавьте соответствующий дочерний элемент с допустимым значением пары. Удалите любые дополнительные поля.

Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
