---
title: ms-service-missing
description: Объяснение и устранение проблем сборки документов ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: b50d9d6f57c953569a4e5dd873961b8c511a8bb1
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236500"
---
# <a name="ms-service-missing"></a>ms-service-missing

## <a name="warning"></a>Предупреждение

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

Используйте `ms.service`, чтобы указать облачные службы. Чтобы указать более подробные сведения об `ms.service`, вы можете дополнительно указать `ms.subservice`, но вместе с ним нужно также указать `ms.service`. Пара значений `ms.service` и `ms.subservice` должна быть допустимой.

## <a name="resolution"></a>Способы устранения

Убедитесь, что указанное значение `ms.subservice` подходит для вашей статьи. Затем добавьте соответствующее значение `ms.service`, которое является родительским для `ms.subservice`.

Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists). Для запроса новых значений следуйте [этой процедуре](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
