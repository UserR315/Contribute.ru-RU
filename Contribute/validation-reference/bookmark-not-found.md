---
title: internal-bookmark-not-found
description: Объяснение проблемы со сборкой документов internal-bookmark-not-found и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 53b98f8da199e3495cc00b2388d983191268eee6
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2019
ms.locfileid: "70856227"
---
# <a name="bookmark-not-found"></a>bookmark-not-found

## <a name="warning"></a>Предупреждение

`Cannot find bookmark '{bookmark-id}' in '{parent-file}'.`

Вы пытаетесь добавить ссылку на заголовок в текущем или другом файле, которого не существует.

## <a name="resolution"></a>Способы устранения

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Проверьте заголовок, ссылку на который вы хотите добавить, и измените ссылку.

Чтобы добавить ссылку на раздел в текущей статье, используйте символ решетки, за которым следует текст заголовка. Удалите знаки препинания из заголовка и замените пробелы дефисами. Ниже приведен пример.

```markdown
[Managed Disks](#managed-disks)
```

Чтобы добавить ссылку на заголовок в другом файле, используйте относительную ссылку на файл, после которой укажите символ решетки и текст заголовка. Удалите знаки препинания из заголовка и замените пробелы дефисами. Ниже приведен пример.

```markdown
See [the Resolution section in h1-empty](h1-empty.md#resolution).
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
