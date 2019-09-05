---
title: ms-prod-missing
description: Объяснение и устранение проблем сборки документов ms-prod-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 5f0b5964dd66946f87d4535e134905db731743f2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236305"
---
# <a name="ms-prod-missing"></a>ms-prod-missing

## <a name="warning"></a>Предупреждение

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

Используйте `ms.prod`, чтобы указать локальные продукты. Чтобы указать более подробные сведения об `ms.prod`, вы можете дополнительно указать `ms.technology`, но вместе с ним нужно также указать `ms.prod`. Пара значений `ms.prod` и `ms.technology` должна быть допустимой.

## <a name="resolution"></a>Способы устранения

Убедитесь, что указанное значение `ms.technology` подходит для вашей статьи. Затем добавьте соответствующее значение `ms.prod`, которое является родительским для `ms.technology`.

Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists). Для запроса новых значений следуйте [этой процедуре](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
