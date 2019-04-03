---
title: ms-prod-and-technology-invalid
description: Объяснение и устранение проблем сборки документов ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8c6f12629cf4b8cf7fd2471ef4d1287562435696
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636846"
---
# <a name="ms-prod-and-technology-invalid"></a>ms-prod-and-technology-invalid

## <a name="warning"></a>Предупреждение

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

Используйте `ms.prod`, чтобы указать локальные продукты. Чтобы указать более подробные сведения о `ms.prod`, вы можете дополнительно указать `ms.technology`. Пара значений `ms.prod` и `ms.technology` должна быть допустимой. Значение `ms.prod` недопустимо, или же значение `ms.technology` не является допустимой парой для значения `ms.prod`.

## <a name="resolution"></a>Способы устранения

Убедитесь, что значение `ms.prod` подходит для вашей статьи. Затем выберите допустимое значение `ms.technology`.

Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
