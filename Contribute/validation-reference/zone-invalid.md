---
title: zone-invalid
description: Объяснение проблемы со сборкой документов zone-invalid и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/4/2019
ms.prod: non-product-specific
ms.openlocfilehash: 0f654d553dcb48cadfc305b91e4f809e3fa69fc7
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2019
ms.locfileid: "57461725"
---
# <a name="zone-invalid"></a>zone-invalid

## <a name="warning"></a>Предупреждение

`Invalid zone: No "::: zone-end" found. Blocks should be explicitly closed.`

## <a name="resolution"></a>Способы устранения

Добавьте `::: zone-end` в конец своей зоны.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
