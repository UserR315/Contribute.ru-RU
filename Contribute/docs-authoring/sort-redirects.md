---
title: Сортировка перенаправлений — Docs Authoring Pack
description: Узнайте, как сортировать перенаправления с помощью Docs Authoring Pack — расширения Visual Studio Code.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4924c631c8720743c283083e53b3a1e9af86b00a
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336688"
---
# <a name="sort-redirects"></a><span data-ttu-id="8a5d3-103">Сортировка перенаправлений</span><span class="sxs-lookup"><span data-stu-id="8a5d3-103">Sort redirects</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="8a5d3-104">Сводка</span><span class="sxs-lookup"><span data-stu-id="8a5d3-104">Summary</span></span>

<span data-ttu-id="8a5d3-105">В результате развития набора документации docs.microsoft.com некоторые файлы Markdown в конечном итоге будут удалены.</span><span class="sxs-lookup"><span data-stu-id="8a5d3-105">With the evolution of a docs.microsoft.com docset, some Markdown files eventually will be deleted.</span></span> <span data-ttu-id="8a5d3-106">При удалении файла Markdown необходимо предоставить перенаправление, чтобы любая ссылка на удаленную статью правильно разрешалась через перенаправление.</span><span class="sxs-lookup"><span data-stu-id="8a5d3-106">When a Markdown file is deleted, we're required to provide a redirect so that any reference to the deleted article is properly resolved via the redirect.</span></span> <span data-ttu-id="8a5d3-107">Перенаправления указываются в файле *.openpublishing.redirection.json*.</span><span class="sxs-lookup"><span data-stu-id="8a5d3-107">Redirections are specified in the *.openpublishing.redirection.json* file.</span></span>

1. <span data-ttu-id="8a5d3-108">Откройте палитру команд, нажмите клавишу <kbd>F1</kbd> (или <kbd>⇧⌘P</kbd> на macOS).</span><span class="sxs-lookup"><span data-stu-id="8a5d3-108">Open the Command Palette, press <kbd>F1</kbd> (or <kbd>⇧⌘P</kbd> on macOS)</span></span>
1. <span data-ttu-id="8a5d3-109">Тип: **Документация. Сортировка главного файла перенаправления**</span><span class="sxs-lookup"><span data-stu-id="8a5d3-109">Type: **Docs: Sort master redirection file**</span></span>
1. <span data-ttu-id="8a5d3-110">Выберите команду для выполнения</span><span class="sxs-lookup"><span data-stu-id="8a5d3-110">Select the command to execute it</span></span>
1. <span data-ttu-id="8a5d3-111">Обратите внимание на изменения в файле *.openpublishing.redirection.json*</span><span class="sxs-lookup"><span data-stu-id="8a5d3-111">Observe changes to *.openpublishing.redirection.json* file</span></span>

## <a name="considerations"></a><span data-ttu-id="8a5d3-112">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="8a5d3-112">Considerations</span></span>

<span data-ttu-id="8a5d3-113">Файл *.openpublishing.redirection.json* был создан по принципу гирляндной цепи.</span><span class="sxs-lookup"><span data-stu-id="8a5d3-113">The concept of "daisy chaining" exists with how the *.openpublishing.redirection.json* file was originally designed.</span></span> <span data-ttu-id="8a5d3-114">Со временем файлы, добавленные в качестве перенаправления, будут устаревать.</span><span class="sxs-lookup"><span data-stu-id="8a5d3-114">Over time, files added as a redirect will eventually become stale.</span></span> <span data-ttu-id="8a5d3-115">Это происходит, когда файл A удаляется и ему требуется перенаправление на файл Б, затем файл Б удаляется и перенаправляется на файл В. В идеале обе записи будут указывать на В, чтобы существовало перенаправление на файл В из файлов А и Б.</span><span class="sxs-lookup"><span data-stu-id="8a5d3-115">This happens when file A is deleted and needs a redirect to file B, then later file B is deleted and then redirects to file C. Ideally, both entries would point to C - so that A redirects to C, and B remains the same.</span></span> <span data-ttu-id="8a5d3-116">Это незначительное увеличение производительности, и эта функция активно разрабатывается.</span><span class="sxs-lookup"><span data-stu-id="8a5d3-116">This is a minor performance gain, and the feature is actively being worked on.</span></span>

## <a name="in-action"></a><span data-ttu-id="8a5d3-117">В действии</span><span class="sxs-lookup"><span data-stu-id="8a5d3-117">In action</span></span>

<span data-ttu-id="8a5d3-118">Ниже приведена краткая демонстрация этой функции.</span><span class="sxs-lookup"><span data-stu-id="8a5d3-118">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="8a5d3-119">[![Демонстрация сортировки перенаправлений](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="8a5d3-119">[![Sort redirects demo](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)</span></span>
