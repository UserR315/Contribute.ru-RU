---
title: multiple-values
description: Объяснение и устранение проблем со сборкой документов (multiple-values)
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: 479472abfb771ae5b4dc77cab2bf94633f3ead5c
ms.sourcegitcommit: fdaff82fec769f4ce9153ff1e0f968d3ea97a76d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/03/2019
ms.locfileid: "58899666"
---
# <a name="multiple-values"></a>multiple-values

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Предложение

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

Вы указали несколько значений для атрибута, а допускается только одно значение.

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

Атрибуты, которые могут принять только одно значение, должны быть указаны в формате YML с одним значением (скалярный формат).

## <a name="resolution"></a>Способы устранения

Такое предложение отображается каждый раз, когда для однозначного атрибута указывается массив с одним или несколькими значениями.

Для многозначных атрибутов, например `ms.custom`, YML поддерживает такие форматы массивов:

```yml
---
# comma-separated bracketed list:
ms.custom: [WIP, generated-via-CI]

# each value on its own line:
ms.custom:
  - WIP
  - generated-via-CI
---
```

Такие форматы не допускаются для однозначных атрибутов, например `author`.

Если вы указали несколько значений, проверьте их и определите, какое значение является правильным. Удалите другие значения и укажите одно значение без скобок в одной строке с атрибутом, как показано ниже:

```yml
---
author: meganbradley
---
```

Если вы указали массив с одним значением, измените его формат на скалярный, как показано выше.

## <a name="attributes-in-scope"></a>Атрибуты в области

Следующие атрибуты должны быть однозначными:

- `author`
- `ms.author`
- `ms.date`
- `ms.prod`
- `ms.service`
- `ms.subservice`
- `ms.technology`
- `ms.topic`
- `title`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
