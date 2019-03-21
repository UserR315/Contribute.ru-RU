---
title: ms-prod-or-service-missing
description: Объяснение и устранение проблем сборки документов ms-prod-or-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6eeb4a95e4d4aeba527b1078bc646fcbc56898a2
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987567"
---
# <a name="ms-prod-or-service-missing"></a>ms-prod-or-service-missing

**Ожидается в ближайшее время.**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Предложение

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a>Способы устранения

Требуется указать значение `ms.prod` или `ms.service`, которые нельзя указывать одновременно: `ms.prod` используется для локальных продуктов, а `ms.service` — для облачных служб. Определите подходящее значение для своей статьи, убедитесь в его правильности и удалите другое поле.

Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]