---
title: external-bookmark-not-found
description: Объяснение проблемы со сборкой документов external-bookmark-not-found и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: b533a463ac38d6445ab84c74bf14b2065a0a63f3
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427776"
---
# <a name="external-bookmark-not-found"></a>external-bookmark-not-found

## <a name="warning"></a>Предупреждение

`File '{file name}' doesn't contain a bookmark named '{bookmark text}'.`

Вы пытаетесь добавить ссылку на несуществующий заголовок в другом файле.

## <a name="resolution"></a>Способы устранения

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Проверьте файл, ссылку на который вы добавляете, и измените ссылку-закладку так, чтобы она указывала на допустимый раздел в файле.

Чтобы добавить ссылку на заголовок раздела в другой статье, используйте относительную ссылку на файл или сайт, после которой укажите символ решетки и текст заголовка. Удалите знаки препинания из заголовка и замените пробелы дефисами. Ниже приведен пример.

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
