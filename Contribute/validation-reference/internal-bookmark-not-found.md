---
title: internal-bookmark-not-found
description: Объяснение проблемы со сборкой документов internal-bookmark-not-found и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9073603d4e745db2f49b57a8901e00a03d8f570f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427836"
---
# <a name="internal-bookmark-not-found"></a>internal-bookmark-not-found

**Ожидается в ближайшее время.**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Предложение

`Current file doesn't contain a bookmark named '{bookmark}'.`

Вы пытаетесь добавить ссылку на заголовок, которого нет в текущем файле.

## <a name="resolution"></a>Способы устранения

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Проверьте заголовок, ссылку на который вы хотите добавить, и измените ссылку.

Чтобы добавить ссылку на раздел в текущей статье, используйте символ решетки, за которым следует текст заголовка. Удалите знаки препинания из заголовка и замените пробелы дефисами. Ниже приведен пример.

```markdown
[Managed Disks](#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
