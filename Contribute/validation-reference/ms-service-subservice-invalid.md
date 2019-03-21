---
title: ms-service-and-subservice-invalid
description: Объяснение и устранение проблем сборки документов ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7dee18e7b902b660a8071bcb4a0dee21c19f4f7f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987650"
---
# <a name="ms-service-and-subservice-invalid"></a>ms-service-and-subservice-invalid

**Ожидается в ближайшее время.**

## <a name="warning"></a>Предупреждение

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

Используйте `ms.service`, чтобы указать облачные службы. Чтобы указать более подробные сведения о `ms.service`, вы можете дополнительно указать `ms.subservice`. Пара значений `ms.service` и `ms.subservice` должна быть допустимой. Значение `ms.service` недопустимо, или же значение `ms.subservice` не является допустимой парой для значения `ms.service`.

## <a name="resolution"></a>Способы устранения

Убедитесь, что значение `ms.service` подходит для вашей статьи. Затем выберите допустимое значение `ms.subservice`.

Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
