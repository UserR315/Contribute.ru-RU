---
title: deprecated-attribute
description: Объяснение и устранение проблем со сборкой документов (deprecated-attribute)
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 113ca759af1765a2a51cadc721fa59743b699475
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636892"
---
# <a name="deprecated-attribute"></a>deprecated-attribute

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Предложение

`Deprecated attribute: ms.component. Use ms.subservice instead.`

Используйте `ms.service`, чтобы указать облачные службы. Чтобы указать более подробные сведения о `ms.service`, вы можете дополнительно указать `ms.subservice`. Не используйте значение `ms.component`, так как оно устарело для этого содержимого.

## <a name="resolution"></a>Способы устранения

Убедитесь, что значение `ms.service` подходит для вашей статьи. Затем выберите допустимое значение `ms.subservice`.

Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
