---
title: h1-missing
description: Объяснение проблемы со сборкой документов h1-missing и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ff29a06b5a8d53d0152329807acc416463f4fe2
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528872"
---
# <a name="h1-missing"></a><span data-ttu-id="d7bc4-103">h1-missing</span><span class="sxs-lookup"><span data-stu-id="d7bc4-103">h1-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="d7bc4-104">Предложение</span><span class="sxs-lookup"><span data-stu-id="d7bc4-104">Suggestion</span></span>

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

<span data-ttu-id="d7bc4-105">H1 — это первый заголовок в файле Markdown.</span><span class="sxs-lookup"><span data-stu-id="d7bc4-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="d7bc4-106">При публикации на веб-сайте docs.microsoft.com заголовок H1 отображается крупным шрифтом в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="d7bc4-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="d7bc4-107">Для создания заголовка H1 необходимо указать в начале строки один символ решетки (#), после которого следует пробел и текст заголовка.</span><span class="sxs-lookup"><span data-stu-id="d7bc4-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="d7bc4-108">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="d7bc4-108">Resolution</span></span>

<span data-ttu-id="d7bc4-109">Чтобы устранить эту проблему, добавьте заголовок H1 сразу после блока метаданных YML в файле:</span><span class="sxs-lookup"><span data-stu-id="d7bc4-109">To fix this issue, add an H1 as the first content after the YML metadata block in your file:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> <span data-ttu-id="d7bc4-110">Это правило не применяется к включаемым файлам.</span><span class="sxs-lookup"><span data-stu-id="d7bc4-110">This rule does not apply to included files.</span></span> <span data-ttu-id="d7bc4-111">Если вы получаете результаты, касающиеся заголовка H1, во включенных файлах, скорее всего, вам нужно переместить эти файлы в папку `includes`.</span><span class="sxs-lookup"><span data-stu-id="d7bc4-111">If you get H1 results on included files, you most likely need to move your included files into an `includes` folder.</span></span> <span data-ttu-id="d7bc4-112">Папка `includes` может находиться на любом уровне в пути к файлу.</span><span class="sxs-lookup"><span data-stu-id="d7bc4-112">The `includes` folder can be at any level in the file path.</span></span> <span data-ttu-id="d7bc4-113">При ее наличии в пути система сборки документов распознает файл как включаемый и проверки заголовка H1 выполняться не будут.</span><span class="sxs-lookup"><span data-stu-id="d7bc4-113">Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.</span></span>
>
> <span data-ttu-id="d7bc4-114">Распространенной причиной отсутствия заголовков H1 в родительских файлах является неправильное использование включенных файлов: H1 находится во включенном, а не родительском файле.</span><span class="sxs-lookup"><span data-stu-id="d7bc4-114">A common cause of missing H1s in parent files is misuse of included files: the H1 is in the included file, not in the parent file.</span></span> <span data-ttu-id="d7bc4-115">Это недопустимо, так как использование заголовка H1 в включенном файле означает, что у заголовков H1 есть дубликаты в родительских файлах или что включенный файл используется только один раз.</span><span class="sxs-lookup"><span data-stu-id="d7bc4-115">This isn't allowed, because using an H1 in an included file either means there are duplicate H1s in parent files or the included file is used only once.</span></span> <span data-ttu-id="d7bc4-116">Заголовки H1 должны быть уникальными в пределах набора содержимого, и включаемые файлы следует использовать только для обмена содержимым между несколькими файлами.</span><span class="sxs-lookup"><span data-stu-id="d7bc4-116">H1s should be unique within a content set and included files should only be used to share content among multiple files.</span></span> <span data-ttu-id="d7bc4-117">Если вы получаете результаты `h1-missing` из-за того, что заголовок H1 находится в включенном файле, переместите заголовок H1 и все включенное содержимое, если включенный файл используется только один раз, в родительский файл.</span><span class="sxs-lookup"><span data-stu-id="d7bc4-117">If you get `h1-missing` results because the H1 is in an included file, the solution is to move the H1 - and all the included content if the included file is used only once - into the parent file.</span></span> <span data-ttu-id="d7bc4-118">См. сведения о включенных файлах в руководстве Майкрософт по [включению повторно используемого содержимого в статьи](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master).</span><span class="sxs-lookup"><span data-stu-id="d7bc4-118">For more information about included files in Docs, see the Microsoft-internal article [Include reusable content in articles](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
