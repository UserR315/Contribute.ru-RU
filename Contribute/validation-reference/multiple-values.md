---
title: multiple-values
description: Объяснение и устранение проблем со сборкой документов (multiple-values)
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: f8c2825801392e8ff1114e6abd08518a59ee8087
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637338"
---
# <a name="multiple-values"></a><span data-ttu-id="5a88a-103">multiple-values</span><span class="sxs-lookup"><span data-stu-id="5a88a-103">multiple-values</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="5a88a-104">Предложение</span><span class="sxs-lookup"><span data-stu-id="5a88a-104">Suggestion</span></span>

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

<span data-ttu-id="5a88a-105">Вы указали несколько значений для атрибута, а допускается только одно значение.</span><span class="sxs-lookup"><span data-stu-id="5a88a-105">You specified more than one value for an attribute that is ony allowed one value.</span></span>

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

<span data-ttu-id="5a88a-106">Атрибуты, которые могут принять только одно значение, должны быть указаны в формате YML с одним значением (скалярный формат).</span><span class="sxs-lookup"><span data-stu-id="5a88a-106">Attributes that aren't allowed to have more than one value must be specified in the single-valued (scalar) YML format.</span></span>

## <a name="resolution"></a><span data-ttu-id="5a88a-107">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="5a88a-107">Resolution</span></span>

<span data-ttu-id="5a88a-108">Такое предложение отображается каждый раз, когда для однозначного атрибута указывается массив с одним или несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="5a88a-108">You get this Suggestion any time a multi-valued array is used for a single-valued attribute, either with multiple values or a single value in the array.</span></span>

<span data-ttu-id="5a88a-109">Для многозначных атрибутов, например `ms.custom`, YML поддерживает такие форматы массивов:</span><span class="sxs-lookup"><span data-stu-id="5a88a-109">YML supports the following array formats for multi-valued attributes, such as `ms.custom`:</span></span>

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

<span data-ttu-id="5a88a-110">Такие форматы не допускаются для однозначных атрибутов, например `author`.</span><span class="sxs-lookup"><span data-stu-id="5a88a-110">These formats aren't valid for single-valued attributes, such as `author`.</span></span>

<span data-ttu-id="5a88a-111">Если вы указали несколько значений, проверьте их и определите, какое значение является правильным.</span><span class="sxs-lookup"><span data-stu-id="5a88a-111">If you specified multiple values, review the specified values and determine which is correct.</span></span> <span data-ttu-id="5a88a-112">Удалите другие значения и укажите одно значение без скобок в одной строке с атрибутом, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="5a88a-112">Remove other values and specify the single value on the same line as the attribute with no brackets, as follows:</span></span>

```yml
---
author: meganbradley
---
```

<span data-ttu-id="5a88a-113">Если вы указали массив с одним значением, измените его формат на скалярный, как показано выше.</span><span class="sxs-lookup"><span data-stu-id="5a88a-113">If you have a single-valued array, change it to the scalar format above.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
