---
title: Сжатие изображений — пакет Docs Authoring Pack
description: Узнайте, как сжимать изображения с помощью Docs Authoring Pack — расширения Visual Studio Code.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4b93ac23b83128d5b9125297879d008e9300509c
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336665"
---
# <a name="image-compression"></a><span data-ttu-id="cd063-103">Сжатие изображений</span><span class="sxs-lookup"><span data-stu-id="cd063-103">Image compression</span></span>

[!INCLUDE [markdown-extension](includes/image-extension.md)]

## <a name="summary"></a><span data-ttu-id="cd063-104">Сводка</span><span class="sxs-lookup"><span data-stu-id="cd063-104">Summary</span></span>

<span data-ttu-id="cd063-105">Вся документация предоставляется через Интернет, за исключением версий документов в формате PDF. При обслуживании статического содержимого рекомендуется сократить число байтов, передаваемых по сети.</span><span class="sxs-lookup"><span data-stu-id="cd063-105">All documentation is provided via the web, with the exception of PDF versions of docs. When serving static content, it is best to minimize the number of bytes sent over the wire.</span></span> <span data-ttu-id="cd063-106">Одним из способов сделать это является сжатие неактивных изображений.</span><span class="sxs-lookup"><span data-stu-id="cd063-106">One way to do that is to compress images at rest.</span></span>

<span data-ttu-id="cd063-107">Расширение Docs Authoring Pack включает в себя пункты контекстного меню сжатия изображений.</span><span class="sxs-lookup"><span data-stu-id="cd063-107">The Docs Authoring Pack extension includes image compression context menu items.</span></span> <span data-ttu-id="cd063-108">Поддерживаются следующие типы изображений и расширения.</span><span class="sxs-lookup"><span data-stu-id="cd063-108">The following image types / extensions are supported:</span></span>

* <span data-ttu-id="cd063-109">*\*.png*</span><span class="sxs-lookup"><span data-stu-id="cd063-109">*\*.png*</span></span>
* <span data-ttu-id="cd063-110">*\*.jpg*</span><span class="sxs-lookup"><span data-stu-id="cd063-110">*\*.jpg*</span></span>
* <span data-ttu-id="cd063-111">*\*.jpeg*</span><span class="sxs-lookup"><span data-stu-id="cd063-111">*\*.jpeg*</span></span>
* <span data-ttu-id="cd063-112">*\*.gif*</span><span class="sxs-lookup"><span data-stu-id="cd063-112">*\*.gif*</span></span>
* <span data-ttu-id="cd063-113">*\*.svg*</span><span class="sxs-lookup"><span data-stu-id="cd063-113">*\*.svg*</span></span>
* <span data-ttu-id="cd063-114">*\*.webp*</span><span class="sxs-lookup"><span data-stu-id="cd063-114">*\*.webp*</span></span>

<span data-ttu-id="cd063-115">По возможности используются алгоритмы сжатия изображений без потерь.</span><span class="sxs-lookup"><span data-stu-id="cd063-115">The lossless image compression algorithms are used, where applicable.</span></span>

## <a name="compress-image"></a><span data-ttu-id="cd063-116">Сжатие изображения</span><span class="sxs-lookup"><span data-stu-id="cd063-116">Compress image</span></span>

<span data-ttu-id="cd063-117">На панели навигации **Обозреватель** щелкните правой кнопкой мыши файл изображения, а затем выберите пункт **Сжать изображение**.</span><span class="sxs-lookup"><span data-stu-id="cd063-117">From the **Explorer** navigation pane, right-click on an image file - then select the **Compress image** option.</span></span> <span data-ttu-id="cd063-118">Изображение сжимается.</span><span class="sxs-lookup"><span data-stu-id="cd063-118">The image is then compressed.</span></span>

## <a name="compress-images-in-folder"></a><span data-ttu-id="cd063-119">Сжатие изображения в папке</span><span class="sxs-lookup"><span data-stu-id="cd063-119">Compress images in folder</span></span>

<span data-ttu-id="cd063-120">На панели навигации **Обозреватель** щелкните правой кнопкой мыши папку с изображением, а затем выберите пункт **Сжать изображение в папке**.</span><span class="sxs-lookup"><span data-stu-id="cd063-120">From the **Explorer** navigation pane, right-click on a folder containing images - then select the **Compress images in folder** option.</span></span> <span data-ttu-id="cd063-121">Все изображения в папке сжимаются.</span><span class="sxs-lookup"><span data-stu-id="cd063-121">All images in the folder are compressed.</span></span>

## <a name="considerations"></a><span data-ttu-id="cd063-122">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="cd063-122">Considerations</span></span>

<span data-ttu-id="cd063-123">Изображения с большими разрешениями неявно изменяют размер.</span><span class="sxs-lookup"><span data-stu-id="cd063-123">Large resolution images are implicitly resized.</span></span> <span data-ttu-id="cd063-124">Максимальный размер зависит от рекомендуемой максимальной ширины `1,200px` на платформе.</span><span class="sxs-lookup"><span data-stu-id="cd063-124">The maximum dimensions are based on the platform suggested max width of `1,200px`.</span></span> <span data-ttu-id="cd063-125">Ограничение максимального размера используется только в том случае, если размер изображений больше рекомендуемого и они сохраняют пропорции при автоматическом изменении размера.</span><span class="sxs-lookup"><span data-stu-id="cd063-125">The max is only used when images are larger than they are recommended to be, and they will maintain the aspect ratio when automatically resized.</span></span>

## <a name="preferences"></a><span data-ttu-id="cd063-126">Настройки</span><span class="sxs-lookup"><span data-stu-id="cd063-126">Preferences</span></span>

<span data-ttu-id="cd063-127">Максимальные размеры можно настроить, но по умолчанию используется максимальная ширина `1200` пикселей.</span><span class="sxs-lookup"><span data-stu-id="cd063-127">The maximum dimensions are configurable, but a default max width of `1200` pixels exists.</span></span> <span data-ttu-id="cd063-128">Чтобы настроить максимальный размер, выберите **Файл –> Настройки –> Параметры** и отфильтруйте результаты по `"Docs Image Extension"`.</span><span class="sxs-lookup"><span data-stu-id="cd063-128">To configure the max dimensions, select **File -> Preferences -> Settings** and filter by `"Docs Image Extension"`.</span></span>

:::image type="content" source="media/configure-image-compression.png" alt-text="Настройка сжатия изображения":::

> [!NOTE]
> <span data-ttu-id="cd063-130">Значение `0` в полях **Максимальная ширина** или **Максимальная высота** будет просто игнорировать различия разрешения.</span><span class="sxs-lookup"><span data-stu-id="cd063-130">A value of `0` in either the **Max Width** or **Max Height** will simply ignore resolution variances.</span></span>

## <a name="in-action"></a><span data-ttu-id="cd063-131">В действии</span><span class="sxs-lookup"><span data-stu-id="cd063-131">In action</span></span>

<span data-ttu-id="cd063-132">Ниже приведена краткая демонстрация этой функции.</span><span class="sxs-lookup"><span data-stu-id="cd063-132">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="cd063-133">[![Демонстрация сжатия изображения](media/compress-image.gif)](media/compress-image.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="cd063-133">[![Compress image demo](media/compress-image.gif)](media/compress-image.gif#lightbox)</span></span>
