---
title: Обновления метаданных — Docs Authoring Pack
description: Узнайте, как обновлять метаданные в Docs Authoring Pack — расширении Visual Studio Code.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 391ea6c523d1f1b82b21883cea5e3428e86633e9
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336642"
---
# <a name="update-metadata"></a><span data-ttu-id="f44b9-103">Обновление метаданных</span><span class="sxs-lookup"><span data-stu-id="f44b9-103">Update metadata</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="f44b9-104">Резюме</span><span class="sxs-lookup"><span data-stu-id="f44b9-104">Summary</span></span>

<span data-ttu-id="f44b9-105">В файле Markdown ( *\*.md*) есть два элемента контекстного меню, относящиеся к метаданным.</span><span class="sxs-lookup"><span data-stu-id="f44b9-105">In a Markdown (*\*.md*) file, there are two contextual menu items specific to metadata.</span></span> <span data-ttu-id="f44b9-106">Щелкнув правой кнопкой мыши в любом месте текстового редактора, вы увидите примерно такие пункты меню.</span><span class="sxs-lookup"><span data-stu-id="f44b9-106">When you right-click anywhere in the text editor, you will see something similar to the following menu items:</span></span>

:::image type="content" source="media/update-metadata-menu.png" alt-text="Контекстное меню обновления метаданных":::

## <a name="update-msdate-metadata-value"></a><span data-ttu-id="f44b9-108">Обновление значения метаданных `ms.date`</span><span class="sxs-lookup"><span data-stu-id="f44b9-108">Update `ms.date` metadata value</span></span>

<span data-ttu-id="f44b9-109">Выберите **Обновить значение метаданных `ms.date`** , чтобы установить текущее значение в файлах Markdown `ms.date` на сегодняшнюю дату.</span><span class="sxs-lookup"><span data-stu-id="f44b9-109">Selecting the **Update `ms.date` Metadata Value** option will set the current Markdown files `ms.date` value to today's date.</span></span> <span data-ttu-id="f44b9-110">Если в документе нет поля метаданных `ms.date`, ничего делать не нужно.</span><span class="sxs-lookup"><span data-stu-id="f44b9-110">If the document does not have an `ms.date` metadata field, no action is taken.</span></span>

## <a name="update-implicit-metadata-values"></a><span data-ttu-id="f44b9-111">Обновление неявных значений метаданных</span><span class="sxs-lookup"><span data-stu-id="f44b9-111">Update implicit metadata values</span></span>

<span data-ttu-id="f44b9-112">Если выбрать параметр **Обновить неявные значения метаданных**, будут найдены и заменены все возможные значения метаданных, которые могут быть заданы неявно.</span><span class="sxs-lookup"><span data-stu-id="f44b9-112">Selecting the **Update implicit metadata values** option will find and replace all possible metadata values that could be implicitly specified.</span></span> <span data-ttu-id="f44b9-113">Значения метаданных неявно указываются в файле *docfx.json* в узле `build/fileMetadata`.</span><span class="sxs-lookup"><span data-stu-id="f44b9-113">Metadata values are implicitly specified in the *docfx.json* file, under the `build/fileMetadata` node.</span></span> <span data-ttu-id="f44b9-114">Каждая пара "ключ-значение" в узле `fileMetadata` представляет значения по умолчанию для метаданных.</span><span class="sxs-lookup"><span data-stu-id="f44b9-114">Each key value pair in the `fileMetadata` node represents metadata defaults.</span></span> <span data-ttu-id="f44b9-115">Например, файл Markdown в каталоге *верхнего уровня или вложенной папки*, в котором опущено значение метаданных `ms.author`, может неявно указывать значение по умолчанию для использования в узле `fileMetadata`.</span><span class="sxs-lookup"><span data-stu-id="f44b9-115">For example, a Markdown file in the *top-level/sub-folder* directory that omits the `ms.author` metadata value could implicitly specify a default value to use in the `fileMetadata` node.</span></span>

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

<span data-ttu-id="f44b9-116">В этом случае все файлы Markdown будут неявно принимать значение метаданных `ms.author: dapine`.</span><span class="sxs-lookup"><span data-stu-id="f44b9-116">In this case, all Markdown files would implicitly take on the `ms.author: dapine` metadata value.</span></span> <span data-ttu-id="f44b9-117">Эта функция работает с этими неявными параметрами, которые находятся в файле *docfx.json*.</span><span class="sxs-lookup"><span data-stu-id="f44b9-117">The feature acts on these implicit settings found in the *docfx.json* file.</span></span> <span data-ttu-id="f44b9-118">Если файл Markdown содержит метаданные со значениями, которые явно заданы и не совпадают с неявными значениями, они переопределяются.</span><span class="sxs-lookup"><span data-stu-id="f44b9-118">If a Markdown file contains metadata with values that are explicitly set to something other than the implicit values, they are overridden.</span></span>

<span data-ttu-id="f44b9-119">Рассмотрим следующие метаданные файла Markdown, где этот файл Markdown находится в папке **top-level/sub-folder/includes/example.md**:</span><span class="sxs-lookup"><span data-stu-id="f44b9-119">Consider the following Markdown file metadata, where this Markdown file resides in **top-level/sub-folder/includes/example.md**:</span></span>

```markdown
---
ms.author: someone-else
---

# Content
```

<span data-ttu-id="f44b9-120">Если в этом файле был выполнен параметр **Обновить неявные значения метаданных**, то содержимое *docfx.json* будет изменено на `ms.author: dapine`.</span><span class="sxs-lookup"><span data-stu-id="f44b9-120">If the **Update implicit metadata values** option was executed on this file, with the assumed *docfx.json* content from above the metadata value would be updated to `ms.author: dapine`.</span></span>

```markdown
---
ms.author: dapine
---

# Content
```

## <a name="in-action"></a><span data-ttu-id="f44b9-121">В действии</span><span class="sxs-lookup"><span data-stu-id="f44b9-121">In action</span></span>

<span data-ttu-id="f44b9-122">Ниже приведена краткая демонстрация этой функции.</span><span class="sxs-lookup"><span data-stu-id="f44b9-122">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="f44b9-123">[![Демонстрация обновления метаданных](media/update-metadata.gif)](media/update-metadata.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="f44b9-123">[![Update metadata demo](media/update-metadata.gif)](media/update-metadata.gif#lightbox)</span></span>
