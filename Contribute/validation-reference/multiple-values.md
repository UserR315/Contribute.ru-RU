---
title: multiple-values
description: Объяснение и устранение проблем со сборкой документов (multiple-values)
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: 515a8cd76cbd3d9bd117b1d0d59492f4a77bea4c
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236468"
---
# <a name="multiple-values"></a><span data-ttu-id="c7e41-103">multiple-values</span><span class="sxs-lookup"><span data-stu-id="c7e41-103">multiple-values</span></span>

## <a name="warning"></a><span data-ttu-id="c7e41-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="c7e41-104">Warning</span></span>

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

<span data-ttu-id="c7e41-105">Вы указали несколько значений для атрибута, а допускается только одно значение.</span><span class="sxs-lookup"><span data-stu-id="c7e41-105">You specified more than one value for an attribute that is ony allowed one value.</span></span>

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

<span data-ttu-id="c7e41-106">Атрибуты, которые могут принять только одно значение, должны быть указаны в формате YML с одним значением (скалярный формат).</span><span class="sxs-lookup"><span data-stu-id="c7e41-106">Attributes that aren't allowed to have more than one value must be specified in the single-valued (scalar) YML format.</span></span>

## <a name="resolution"></a><span data-ttu-id="c7e41-107">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="c7e41-107">Resolution</span></span>

<span data-ttu-id="c7e41-108">Такое предложение отображается каждый раз, когда для однозначного атрибута указывается массив с одним или несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="c7e41-108">You get this Suggestion any time a multi-valued array is used for a single-valued attribute, either with multiple values or a single value in the array.</span></span>

<span data-ttu-id="c7e41-109">Для многозначных атрибутов, например `ms.custom`, YML поддерживает такие форматы массивов:</span><span class="sxs-lookup"><span data-stu-id="c7e41-109">YML supports the following array formats for multi-valued attributes, such as `ms.custom`:</span></span>

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

<span data-ttu-id="c7e41-110">Такие форматы не допускаются для однозначных атрибутов, например `author`.</span><span class="sxs-lookup"><span data-stu-id="c7e41-110">These formats aren't valid for single-valued attributes, such as `author`.</span></span>

<span data-ttu-id="c7e41-111">Если вы указали несколько значений, проверьте их и определите, какое значение является правильным.</span><span class="sxs-lookup"><span data-stu-id="c7e41-111">If you specified multiple values, review the specified values and determine which is correct.</span></span> <span data-ttu-id="c7e41-112">Удалите другие значения и укажите одно значение без скобок в одной строке с атрибутом, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="c7e41-112">Remove other values and specify the single value on the same line as the attribute with no brackets, as follows:</span></span>

```yml
---
author: meganbradley
---
```

<span data-ttu-id="c7e41-113">Если вы указали массив с одним значением, измените его формат на скалярный, как показано выше.</span><span class="sxs-lookup"><span data-stu-id="c7e41-113">If you have a single-valued array, change it to the scalar format above.</span></span>

## <a name="attributes-in-scope"></a><span data-ttu-id="c7e41-114">Атрибуты в области</span><span class="sxs-lookup"><span data-stu-id="c7e41-114">Attributes in scope</span></span>

<span data-ttu-id="c7e41-115">Следующие атрибуты должны быть однозначными:</span><span class="sxs-lookup"><span data-stu-id="c7e41-115">The following attributes are required to be single-valued:</span></span>

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
