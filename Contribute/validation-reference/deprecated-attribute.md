---
title: deprecated-attribute
description: Объяснение и устранение проблем со сборкой документов (deprecated-attribute)
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 15d285159b361b7fb9dbc1774e6c4b2f5f5758ed
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236207"
---
# <a name="deprecated-attribute"></a>deprecated-attribute

## <a name="warning"></a>Предупреждение

`Deprecated attribute: ms.component. Use ms.subservice instead.`

Используйте `ms.service`, чтобы указать облачные службы. Чтобы указать более подробные сведения о `ms.service`, вы можете дополнительно указать `ms.subservice`. Не используйте значение `ms.component`, так как оно устарело для этого содержимого.

## <a name="resolution"></a>Способы устранения

Убедитесь, что значение `ms.service` подходит для вашей статьи. Затем выберите допустимое значение `ms.subservice`.

Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
