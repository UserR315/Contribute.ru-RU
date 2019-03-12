---
title: h1-missing
description: Объяснение проблемы со сборкой документов h1-missing и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c920cc0f12a9fac41b640957d45452a7958d4b07
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459126"
---
# <a name="h1-missing"></a>h1-missing

## <a name="warning"></a>Предупреждение

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

H1 — это первый заголовок в файле Markdown. При публикации на веб-сайте docs.microsoft.com заголовок H1 отображается крупным шрифтом в верхней части страницы. Для создания заголовка H1 необходимо указать в начале строки один символ решетки (#), после которого следует пробел и текст заголовка.

## <a name="resolution"></a>Способы устранения

Чтобы устранить эту проблему, добавьте заголовок H1 сразу после блока метаданных YML в файле:

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> Это правило не применяется к включаемым файлам. Если предупреждения, касающиеся заголовка H1, выводятся для включаемых файлов, скорее всего, необходимо переместить эти файлы в папку `includes`. Папка `includes` может находиться на любом уровне в пути к файлу. При ее наличии в пути система сборки документов распознает файл как включаемый и проверки заголовка H1 выполняться не будут.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]