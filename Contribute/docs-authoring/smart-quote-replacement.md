---
title: Автоматическая замена парных кавычек — Docs Authoring Pack
description: Узнайте, как автоматически заменять парные кавычки с помощью Docs Authoring Pack — расширения Visual Studio Code.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 048f244324d7dde540c78e6631ccb5abbed3e431
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336711"
---
# <a name="smart-quote-replacement"></a><span data-ttu-id="33436-103">Замена парных кавычек</span><span class="sxs-lookup"><span data-stu-id="33436-103">Smart quote replacement</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="33436-104">Сводка</span><span class="sxs-lookup"><span data-stu-id="33436-104">Summary</span></span>

<span data-ttu-id="33436-105">Разработчики содержимого должны создавать сложные функции на основе современных технологий и средств аналитики, но сегодня наши инструменты предпочитают использовать в Markdown двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="33436-105">Content developers are responsible for authoring some of the most advanced features of modern technology and intelligence, yet our tooling today prefers the usage of "dumb quotes" in Markdown.</span></span> <span data-ttu-id="33436-106">Вместо них лучше использовать парные.</span><span class="sxs-lookup"><span data-stu-id="33436-106">The antonym of course being "smart quotes".</span></span> <span data-ttu-id="33436-107">Парные кавычки часто используются для идеального написания, но не являются предпочтительными в Markdown и отрисованном HTML.</span><span class="sxs-lookup"><span data-stu-id="33436-107">Smart quotes are common with ideal typographies, but not preferred with Markdown and rendered HTML.</span></span>

<span data-ttu-id="33436-108">Например, при работе с документом Microsoft Word можно заметить, что, если удерживать <kbd>SHIFT</kbd> и нажать <kbd>"</kbd>, Microsoft Word быстро заменяет символ `"` на эквивалентный символ `“`.</span><span class="sxs-lookup"><span data-stu-id="33436-108">When working on a Microsoft Word document for example, you may have noticed that when you hold the <kbd>Shift</kbd> and type a <kbd>"</kbd> Microsoft Word quickly replaces the `"` character with a smart quote equivalent `“` character.</span></span>

| <span data-ttu-id="33436-109">Описание</span><span class="sxs-lookup"><span data-stu-id="33436-109">Description</span></span>        | <span data-ttu-id="33436-110">Юникод</span><span class="sxs-lookup"><span data-stu-id="33436-110">Unicode</span></span>  | <span data-ttu-id="33436-111">Парная кавычка</span><span class="sxs-lookup"><span data-stu-id="33436-111">Smart Quote</span></span> | <span data-ttu-id="33436-112">Замена</span><span class="sxs-lookup"><span data-stu-id="33436-112">Replacement</span></span> |
|--------------------|----------|-------------|-------------|
| <span data-ttu-id="33436-113">Двойная левая кавычка</span><span class="sxs-lookup"><span data-stu-id="33436-113">Double left quote</span></span>  | `\u201c` | `“`         | `"`         |
| <span data-ttu-id="33436-114">Двойная правая кавычка</span><span class="sxs-lookup"><span data-stu-id="33436-114">Double right quote</span></span> | `\u201d` | `”`         | `"`         |
| <span data-ttu-id="33436-115">Одинарная левая кавычка</span><span class="sxs-lookup"><span data-stu-id="33436-115">Single left quote</span></span>  | `\u2018` | `‘`         | `'`         |
| <span data-ttu-id="33436-116">Одинарная правая кавычка</span><span class="sxs-lookup"><span data-stu-id="33436-116">Single right quote</span></span> | `\u2019` | `’`         | `'`         |

<span data-ttu-id="33436-117">В файле Markdown ( *\*.md*) при вставке в текст или при обновлении содержимого этот компонент будет активно оценивать содержимое и автоматически заменять значения соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="33436-117">In a Markdown (*\*.md*) file, when you paste in text or as you update content - this feature will actively evaluate the content and automatically replace values accordingly.</span></span>

> [!NOTE]
> <span data-ttu-id="33436-118">Функция замены парных кавычек также заменяет другие символы, например (`©, ™, ®, •`, подстрочные и надстрочные символы).</span><span class="sxs-lookup"><span data-stu-id="33436-118">The smart quote replacement feature also replaces other characters, such as but not limited to; (`©, ™, ®, •`, subscript and superscript characters).</span></span> <span data-ttu-id="33436-119">Это полезно при вставке текста из документов Word.</span><span class="sxs-lookup"><span data-stu-id="33436-119">This is useful when pasting text from Word documents.</span></span>

## <a name="preferences"></a><span data-ttu-id="33436-120">Настройки</span><span class="sxs-lookup"><span data-stu-id="33436-120">Preferences</span></span>

<span data-ttu-id="33436-121">Эта функция является необязательной, но по умолчанию имеет значение `true`.</span><span class="sxs-lookup"><span data-stu-id="33436-121">This feature is optional, but defaults to `true`.</span></span> <span data-ttu-id="33436-122">Включение или отключение этой функции:</span><span class="sxs-lookup"><span data-stu-id="33436-122">To toggle this feature on or off:</span></span>

1. <span data-ttu-id="33436-123">Выберите **Файл** > **Настройки** > **Параметры** и выберите фильтр *Расширение Docs Markdown*.</span><span class="sxs-lookup"><span data-stu-id="33436-123">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="33436-124">Включите параметр в разделе **Markdown: замена парных кавычек**.</span><span class="sxs-lookup"><span data-stu-id="33436-124">Toggle the setting in the **Markdown: Replace Smart Quotes** section.</span></span>

## <a name="in-action"></a><span data-ttu-id="33436-125">В действии</span><span class="sxs-lookup"><span data-stu-id="33436-125">In action</span></span>

<span data-ttu-id="33436-126">Ниже приведена краткая демонстрация этой функции.</span><span class="sxs-lookup"><span data-stu-id="33436-126">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="33436-127">[![Демонстрация замены парных кавычек](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="33436-127">[![Replace smart quotes demo](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)</span></span>
