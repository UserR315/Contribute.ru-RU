---
title: Обновления метаданных — Docs Authoring Pack
description: Узнайте, как обновлять метаданные в Docs Authoring Pack — расширении Visual Studio Code.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 391ea6c523d1f1b82b21883cea5e3428e86633e9
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336642"
---
# <a name="update-metadata"></a>Обновление метаданных

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Сводка

В файле Markdown ( *\*.md*) есть два элемента контекстного меню, относящиеся к метаданным. Щелкнув правой кнопкой мыши в любом месте текстового редактора, вы увидите примерно такие пункты меню.

:::image type="content" source="media/update-metadata-menu.png" alt-text="Контекстное меню обновления метаданных":::

## <a name="update-msdate-metadata-value"></a>Обновление значения метаданных `ms.date`

Выберите **Обновить значение метаданных `ms.date`** , чтобы установить текущее значение в файлах Markdown `ms.date` на сегодняшнюю дату. Если в документе нет поля метаданных `ms.date`, ничего делать не нужно.

## <a name="update-implicit-metadata-values"></a>Обновление неявных значений метаданных

Если выбрать параметр **Обновить неявные значения метаданных**, будут найдены и заменены все возможные значения метаданных, которые могут быть заданы неявно. Значения метаданных неявно указываются в файле *docfx.json* в узле `build/fileMetadata`. Каждая пара "ключ-значение" в узле `fileMetadata` представляет значения по умолчанию для метаданных. Например, файл Markdown в каталоге *верхнего уровня или вложенной папки*, в котором опущено значение метаданных `ms.author`, может неявно указывать значение по умолчанию для использования в узле `fileMetadata`.

```json
{
    "build": {
        "fileMetadata": {
            "ms.author": {
                "top-level/sub-folder/**/**.md": "dapine"
            }
        }
    }
}
```

В этом случае все файлы Markdown будут неявно принимать значение метаданных `ms.author: dapine`. Эта функция работает с этими неявными параметрами, которые находятся в файле *docfx.json*. Если файл Markdown содержит метаданные со значениями, которые явно заданы и не совпадают с неявными значениями, они переопределяются.

Рассмотрим следующие метаданные файла Markdown, где этот файл Markdown находится в папке **top-level/sub-folder/includes/example.md**:

```markdown
---
ms.author: someone-else
---

# Content
```

Если в этом файле был выполнен параметр **Обновить неявные значения метаданных**, то содержимое *docfx.json* будет изменено на `ms.author: dapine`.

```markdown
---
ms.author: dapine
---

# Content
```

## <a name="in-action"></a>В действии

Ниже приведена краткая демонстрация этой функции.

[![Демонстрация обновления метаданных](media/update-metadata.gif)](media/update-metadata.gif#lightbox)
