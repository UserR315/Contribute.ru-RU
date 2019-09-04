---
title: ms-prod-and-technology-invalid
description: Объяснение и устранение проблем сборки документов ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25a2b6a5bcb63388c119863ea82fb932dda4eec8
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236341"
---
# <a name="ms-prod-and-technology-invalid"></a>ms-prod-and-technology-invalid

## <a name="warning"></a>Предупреждение

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

Используйте `ms.prod`, чтобы указать локальные продукты. Чтобы указать более подробные сведения о `ms.prod`, вы можете дополнительно указать `ms.technology`. Пара значений `ms.prod` и `ms.technology` должна быть допустимой. Значение `ms.prod` недопустимо, или же значение `ms.technology` не является допустимой парой для значения `ms.prod`.

## <a name="resolution"></a>Способы устранения

Убедитесь, что значение `ms.prod` подходит для вашей статьи. Затем выберите допустимое значение `ms.technology`.

Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists). Для запроса новых значений следуйте [этой процедуре](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
