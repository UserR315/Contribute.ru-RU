---
title: ms-prod-service-mismatch
description: Объяснение и устранение проблем сборки документов ms-prod-service-mismatch
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a7de44e9930def2d2582194f28695e3ef3940541
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987622"
---
# <a name="ms-prod-service-mismatch"></a>ms-prod-service-mismatch

**Ожидается в ближайшее время.**

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
