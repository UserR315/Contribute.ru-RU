---
title: ms-prod-missing
description: Объяснение и устранение проблем сборки документов ms-prod-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: ee29396a20345f6884a5bbc94aa25f48dafaff52
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713230"
---
# <a name="ms-prod-missing"></a>ms-prod-missing

**Ожидается в ближайшее время.**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Предложение

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

Используйте `ms.prod`, чтобы указать локальные продукты. Чтобы указать более подробные сведения об `ms.prod`, вы можете дополнительно указать `ms.technology`, но вместе с ним нужно также указать `ms.prod`. Пара значений `ms.prod` и `ms.technology` должна быть допустимой.

## <a name="resolution"></a>Способы устранения

Убедитесь, что указанное значение `ms.technology` подходит для вашей статьи. Затем добавьте соответствующее значение `ms.prod`, которое является родительским для `ms.technology`.

Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/whitelists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
