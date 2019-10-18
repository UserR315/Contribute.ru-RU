---
title: multiple-h1
description: Объяснение проблемы со сборкой документов multiple-h1 и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/09/2019
ms.prod: non-product-specific
ms.openlocfilehash: c97ae237cd2ce657bd02132af5169cb6544ae306
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246272"
---
# <a name="multiple-h1"></a>multiple-h1

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Предложение

`Multiple H1s are not allowed. You can only have one top-level heading.`

H1 — это первый заголовок в файле Markdown. При публикации на веб-сайте docs.microsoft.com заголовок H1 отображается крупным шрифтом в верхней части страницы. Для создания заголовка H1 необходимо указать в начале строки один символ решетки (#), после которого следует пробел и текст заголовка. В каждом файле может быть только один заголовок H1.

Кроме того, это сообщение можно получить, если статья содержит строку, состоящую из знаков равенства, которые образуют двойное подчеркивание, например: `=======`. Это альтернативный синтаксис Markdown для заголовков H1. Он также часто встречается в конфликтах слияния:

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a>Способы устранения

Чтобы устранить эту проблему, измените уровень последующих заголовков H1 на H2 (`##`) либо реорганизуйте файл. Обратите внимание на то, что пропускать уровни заголовков, например указывать H3 сразу после H1, запрещено.

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

Если дополнительный заголовок H1 фактически является двойным подчеркиванием (`=======`), удалите его или замените на заголовок из хэштегов, например `##`, в зависимости от ситуации. Если двойное подчеркивание является частью конфликта слияния, необходимо также удалить начальный и конечный маркеры конфликта слияния и устаревший текст.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
