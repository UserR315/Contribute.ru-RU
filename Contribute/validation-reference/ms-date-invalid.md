---
title: ms-date-invalid
description: Объяснение и устранение проблем сборки документов ms-date-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: a54dc495593315a0382ea99e46a86145fbfa8577
ms.sourcegitcommit: 836d4d6127fabb5569ffc0809db5fb25e46038b5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2019
ms.locfileid: "72590881"
---
# <a name="ms-date-invalid"></a>ms-date-invalid

## <a name="warning"></a>Предупреждение

`Invalid value for ms.date: '{value}'. Must be a date in format MM/DD/YYYY, no more than 30 days from today.`

## <a name="resolution"></a>Способы устранения

Убедитесь, что статья актуальна и в ней отсутствует испорченное содержимое, и добавьте допустимую дату в формате ММ/ДД/ГГГГ.

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
