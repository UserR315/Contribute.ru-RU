---
title: deprecated-attribute
description: Объяснение и устранение проблем со сборкой документов (deprecated-attribute)
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4f9ddc611d401bc7003e1b7d378517d5e374da87
ms.sourcegitcommit: a2c8317ccf8b56371773c84f4960a44787ce8666
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2019
ms.locfileid: "56322698"
---
# <a name="deprecated-attribute"></a>deprecated-attribute

**Ожидается в ближайшее время.**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Предложение

`Deprecated attribute: ms.component. Use ms.subservice instead.`

Используйте `ms.service`, чтобы указать облачные службы. Чтобы указать более подробные сведения о `ms.service`, вы можете дополнительно указать `ms.subservice`. Не используйте значение `ms.component`, так как оно устарело для этого содержимого.

## <a name="resolution"></a>Способы устранения

Убедитесь, что значение `ms.service` подходит для вашей статьи. Затем выберите допустимое значение `ms.subservice`.

Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/whitelists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
