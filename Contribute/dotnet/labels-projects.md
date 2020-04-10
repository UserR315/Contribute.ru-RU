---
title: Принципы использования меток и проектов
description: В этой статье объясняется, как метки и проекты используются в репозитории dotnet/docs.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/24/2020
ms.openlocfilehash: 0dcac28db04378730b186c0f23064c1433d9f80e
ms.sourcegitcommit: bf2f4c7d9050b480d4db306df19d4c9f8714eff0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/07/2020
ms.locfileid: "80760383"
---
# <a name="labels-and-projects-roadmap"></a><span data-ttu-id="dffbf-103">Принципы использования меток и проектов</span><span class="sxs-lookup"><span data-stu-id="dffbf-103">Labels and projects roadmap</span></span>

<span data-ttu-id="dffbf-104">Команда по разработке документации .NET активно использует [метки GitHub](https://github.com/dotnet/docs/labels) для организации работы.</span><span class="sxs-lookup"><span data-stu-id="dffbf-104">The .NET docs team makes extensive use of [GitHub labels](https://github.com/dotnet/docs/labels) to organize our work.</span></span> <span data-ttu-id="dffbf-105">Путем фильтрации по сочетаниям меток мы можем быстро сосредотачиваться на интересующих нас разделах [веб-сайта документации по .NET](https://docs.microsoft.com/dotnet).</span><span class="sxs-lookup"><span data-stu-id="dffbf-105">By filtering on combinations of labels, we can quickly focus on sections of interest on the [.NET docs website](https://docs.microsoft.com/dotnet).</span></span>

<span data-ttu-id="dffbf-106">Мы также используем [проекты GitHub](https://github.com/dotnet/docs/projects) для организации спринтов и других целевых ситуаций.</span><span class="sxs-lookup"><span data-stu-id="dffbf-106">We also use [GitHub projects](https://github.com/dotnet/docs/projects) to organize sprints and other goal-oriented epics.</span></span>

<span data-ttu-id="dffbf-107">В этом документе объясняется, как мы используем эти организационные средства, и приводятся ссылки на удобные фильтры, которые мы используем для поиска интересующих нас разделов.</span><span class="sxs-lookup"><span data-stu-id="dffbf-107">This roadmap explains how we use these organizational tools and has links to handy filters we use to find areas of interest.</span></span>

## <a name="labels"></a><span data-ttu-id="dffbf-108">Метки</span><span class="sxs-lookup"><span data-stu-id="dffbf-108">Labels</span></span>

<span data-ttu-id="dffbf-109">Если вы впервые приступаете к участию в работе над [dotnet/docs](https://github.com/dotnet/docs), начните с проблем с меткой [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs).</span><span class="sxs-lookup"><span data-stu-id="dffbf-109">If this is your first experience contributing to [dotnet/docs](https://github.com/dotnet/docs), start with the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) issues.</span></span> <span data-ttu-id="dffbf-110">Это узкоспециализированные проблемы.</span><span class="sxs-lookup"><span data-stu-id="dffbf-110">These are issues that have a more focused scope.</span></span> <span data-ttu-id="dffbf-111">Они являются хорошей отправной точкой.</span><span class="sxs-lookup"><span data-stu-id="dffbf-111">They are a great way to make your first contribution.</span></span> <span data-ttu-id="dffbf-112">В представлении up-for-grabs можно далее отфильтровать проблемы по области и приоритету.</span><span class="sxs-lookup"><span data-stu-id="dffbf-112">From the up-for-grabs view, you can further filter issues based on areas and priority.</span></span> <span data-ttu-id="dffbf-113">Хорошие проблемы для начинающих имеют метку [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue).</span><span class="sxs-lookup"><span data-stu-id="dffbf-113">We've identified good issues for beginners with the [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) if you want to try a smaller first contribution.</span></span>

<span data-ttu-id="dffbf-114">Мы используем метки для классификации проблем различными способами:</span><span class="sxs-lookup"><span data-stu-id="dffbf-114">We use labels to classify issues in many different ways:</span></span>

- <span data-ttu-id="dffbf-115">[руководства по .NET](#find-a-single-net-guide) и [разделы руководств](#search-one-section-of-a-guide);</span><span class="sxs-lookup"><span data-stu-id="dffbf-115">[.NET Guides](#find-a-single-net-guide) and [sections of a guide](#search-one-section-of-a-guide).</span></span>
- <span data-ttu-id="dffbf-116">[целевой выпуск](#releases);</span><span class="sxs-lookup"><span data-stu-id="dffbf-116">[Target release](#releases)</span></span>
- <span data-ttu-id="dffbf-117">[приоритет](#priority).</span><span class="sxs-lookup"><span data-stu-id="dffbf-117">[Priority](#priority)</span></span>

<span data-ttu-id="dffbf-118">Сочетая метки из каждого набора (руководство, выпуск, приоритет), можно найти узкий круг проблем, на которых вы хотели бы сосредоточиться.</span><span class="sxs-lookup"><span data-stu-id="dffbf-118">You can combine a label from each set (guide, release, priority) to create a narrow focus to find issues you want to work on.</span></span>

### <a name="find-a-single-net-guide"></a><span data-ttu-id="dffbf-119">Поиск отдельного руководства по .NET</span><span class="sxs-lookup"><span data-stu-id="dffbf-119">Find a single .NET guide</span></span>

<span data-ttu-id="dffbf-120">Каждая электронная книга по архитектуре и каждое руководство по .NET имеет свою метку.</span><span class="sxs-lookup"><span data-stu-id="dffbf-120">We use labels for each of the architecture e-books and for each .NET Guide.</span></span>

<span data-ttu-id="dffbf-121">![:book: guide на светло-зеленом фоне](./media/labels-projects/guide.png "Префикс для меток руководств по архитектуре")</span><span class="sxs-lookup"><span data-stu-id="dffbf-121">![:book: guide on light green background](./media/labels-projects/guide.png "Prefix for architecture guide labels")</span></span>

<span data-ttu-id="dffbf-122">Электронные книги по архитектуре обозначены префиксом `:book: guide` и имеют светло-зеленый фон.</span><span class="sxs-lookup"><span data-stu-id="dffbf-122">Architecture e-books are noted with the `:book: guide` prefix and have a light green background.</span></span> <span data-ttu-id="dffbf-123">Это подробные документы по рекомендуемой архитектуре.</span><span class="sxs-lookup"><span data-stu-id="dffbf-123">These are the long-form areas that cover recommended architecture.</span></span> <span data-ttu-id="dffbf-124">Ниже приведены фильтры для текущих проблем, связанных с каждым из руководств по архитектуре .NET.</span><span class="sxs-lookup"><span data-stu-id="dffbf-124">Here are current issues filtered for each of the .NET architecture guides.</span></span>

- [<span data-ttu-id="dffbf-125">Веб-приложения ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="dffbf-125">ASP.NET Core web apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [<span data-ttu-id="dffbf-126">Blazor</span><span class="sxs-lookup"><span data-stu-id="dffbf-126">Blazor</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [<span data-ttu-id="dffbf-127">Собственные облачные приложения</span><span class="sxs-lookup"><span data-stu-id="dffbf-127">Cloud Native</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [<span data-ttu-id="dffbf-128">Жизненный цикл Docker</span><span class="sxs-lookup"><span data-stu-id="dffbf-128">Docker lifecycle</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [<span data-ttu-id="dffbf-129">gRPC</span><span class="sxs-lookup"><span data-stu-id="dffbf-129">gRPC</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [<span data-ttu-id="dffbf-130">Модернизация за счет контейнеров Windows</span><span class="sxs-lookup"><span data-stu-id="dffbf-130">Modernizing w/ Windows containers</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [<span data-ttu-id="dffbf-131">Микрослужбы .NET</span><span class="sxs-lookup"><span data-stu-id="dffbf-131">.NET Microservices</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [<span data-ttu-id="dffbf-132">Бессерверные приложения</span><span class="sxs-lookup"><span data-stu-id="dffbf-132">Serverless apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

<span data-ttu-id="dffbf-133">Такой же стиль меток применяется и к [руководствам по проектированию платформы](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines).</span><span class="sxs-lookup"><span data-stu-id="dffbf-133">This label style is also applied to the [Framework design guidelines](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines).</span></span> <span data-ttu-id="dffbf-134">Эта область имеет ту же структуру меток, но запросы на вытягивание от сообщества не рекомендуются.</span><span class="sxs-lookup"><span data-stu-id="dffbf-134">This area has the same label design, but community PRs are discouraged.</span></span> <span data-ttu-id="dffbf-135">Данные материалы воспроизводятся с разрешения и не должны редактироваться.</span><span class="sxs-lookup"><span data-stu-id="dffbf-135">This is material reprinted with permission and should not be edited.</span></span>

<span data-ttu-id="dffbf-136">![:books: Area на темно-синем фоне](./media/labels-projects/area.png "Префикс для меток руководств по .NET")</span><span class="sxs-lookup"><span data-stu-id="dffbf-136">![:books: Area on dark blue background](./media/labels-projects/area.png "Prefix for .NET Guide area labels")</span></span>

<span data-ttu-id="dffbf-137">Каждое руководство по .NET обозначено префиксом `:books: Area` и имеет темно-синий фон.</span><span class="sxs-lookup"><span data-stu-id="dffbf-137">Each .NET Guide is noted with the `:books: Area` prefix and has a dark blue background.</span></span> <span data-ttu-id="dffbf-138">Ниже приведены фильтры для текущих проблем, связанных с каждым из руководств по .NET.</span><span class="sxs-lookup"><span data-stu-id="dffbf-138">Here are current issues filtered for each of the .NET guides.</span></span>

- [<span data-ttu-id="dffbf-139">Справочник по API</span><span class="sxs-lookup"><span data-stu-id="dffbf-139">API Reference</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- <span data-ttu-id="dffbf-140">[Azure .NET SDK](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk);</span><span class="sxs-lookup"><span data-stu-id="dffbf-140">[Azure .NET SDK](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)</span></span>
- [<span data-ttu-id="dffbf-141">Руководство по C#</span><span class="sxs-lookup"><span data-stu-id="dffbf-141">C# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [<span data-ttu-id="dffbf-142">Руководство по классическим приложениям</span><span class="sxs-lookup"><span data-stu-id="dffbf-142">Desktop Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [<span data-ttu-id="dffbf-143">Руководство по F#</span><span class="sxs-lookup"><span data-stu-id="dffbf-143">F# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [<span data-ttu-id="dffbf-144">Руководство по ML.NET</span><span class="sxs-lookup"><span data-stu-id="dffbf-144">ML.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- <span data-ttu-id="dffbf-145">[Руководство по архитектуре .NET](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) — возможно, удалено</span><span class="sxs-lookup"><span data-stu-id="dffbf-145">[.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - Could be removed</span></span>
- [<span data-ttu-id="dffbf-146">Руководство по .NET Core</span><span class="sxs-lookup"><span data-stu-id="dffbf-146">.NET Core Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [<span data-ttu-id="dffbf-147">Руководство по .NET для Apache Spark</span><span class="sxs-lookup"><span data-stu-id="dffbf-147">.NET for Apache Spark Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [<span data-ttu-id="dffbf-148">Руководство по .NET Framework</span><span class="sxs-lookup"><span data-stu-id="dffbf-148">.NET Framework Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [<span data-ttu-id="dffbf-149">Руководство по .NET</span><span class="sxs-lookup"><span data-stu-id="dffbf-149">.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- <span data-ttu-id="dffbf-150">[Справочник по API Roslyn](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) — возможно, удален</span><span class="sxs-lookup"><span data-stu-id="dffbf-150">[Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - could be removed.</span></span>
- [<span data-ttu-id="dffbf-151">Руководство по Visual Basic</span><span class="sxs-lookup"><span data-stu-id="dffbf-151">Visual Basic Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a><span data-ttu-id="dffbf-152">Поиск отдельного раздела руководства</span><span class="sxs-lookup"><span data-stu-id="dffbf-152">Search one section of a guide</span></span>

<span data-ttu-id="dffbf-153">![:card_file_box: Area на умеренно синем фоне](./media/labels-projects/technology.png "Префикс для меток разделов руководств по .NET")</span><span class="sxs-lookup"><span data-stu-id="dffbf-153">![:card_file_box: Area on medium blue background](./media/labels-projects/technology.png "Prefix for .NET Guide sub-area labels")</span></span>

<span data-ttu-id="dffbf-154">Руководства по .NET имеют большой объем, поэтому данные метки позволяют далее ограничить область проблем отдельными разделами.</span><span class="sxs-lookup"><span data-stu-id="dffbf-154">The .NET guides are large, so these labels further limit the scope by a section of a guide.</span></span> <span data-ttu-id="dffbf-155">Каждый раздел руководства по .NET обозначен префиксом `:card_file_box: Technology` и имеет умеренно синий фон.</span><span class="sxs-lookup"><span data-stu-id="dffbf-155">Each .NET Guide subarea is noted with the `:card_file_box: Technology` prefix and has a medium blue background.</span></span> <span data-ttu-id="dffbf-156">Многие из этих меток относятся к нескольким руководствам, а другие — только к одному.</span><span class="sxs-lookup"><span data-stu-id="dffbf-156">Many of these labels apply to multiple guides, while others are in only one guide.</span></span> <span data-ttu-id="dffbf-157">После фильтрации области добавьте одну из этих меток, чтобы сузить область проблем.</span><span class="sxs-lookup"><span data-stu-id="dffbf-157">After filtering on an area, add one of these labels to further limit the scope of issues.</span></span>

- <span data-ttu-id="dffbf-158">AppCompat</span><span class="sxs-lookup"><span data-stu-id="dffbf-158">AppCompat</span></span>
- <span data-ttu-id="dffbf-159">Асинхронная задача</span><span class="sxs-lookup"><span data-stu-id="dffbf-159">Async Task</span></span>
- <span data-ttu-id="dffbf-160">Углубленные понятия C#</span><span class="sxs-lookup"><span data-stu-id="dffbf-160">C# Advanced concepts</span></span>
- <span data-ttu-id="dffbf-161">Компилятор C#</span><span class="sxs-lookup"><span data-stu-id="dffbf-161">C# compiler</span></span>
- <span data-ttu-id="dffbf-162">Основы C#</span><span class="sxs-lookup"><span data-stu-id="dffbf-162">C# Fundamentals</span></span>
- <span data-ttu-id="dffbf-163">Начало работы с C#</span><span class="sxs-lookup"><span data-stu-id="dffbf-163">C# Get Started</span></span>
- <span data-ttu-id="dffbf-164">Справочник по языку C#</span><span class="sxs-lookup"><span data-stu-id="dffbf-164">C# Language Reference</span></span>
- <span data-ttu-id="dffbf-165">NULL-безопасность в C#</span><span class="sxs-lookup"><span data-stu-id="dffbf-165">C# Null safety</span></span>
- <span data-ttu-id="dffbf-166">Новые возможности C#</span><span class="sxs-lookup"><span data-stu-id="dffbf-166">C# What's new</span></span>
- <span data-ttu-id="dffbf-167">CLI</span><span class="sxs-lookup"><span data-stu-id="dffbf-167">CLI</span></span>
- <span data-ttu-id="dffbf-168">Доступ к данным</span><span class="sxs-lookup"><span data-stu-id="dffbf-168">Data Access</span></span>
- <span data-ttu-id="dffbf-169">Docker</span><span class="sxs-lookup"><span data-stu-id="dffbf-169">Docker</span></span>
- <span data-ttu-id="dffbf-170">Установщики</span><span class="sxs-lookup"><span data-stu-id="dffbf-170">Installers</span></span>
- <span data-ttu-id="dffbf-171">LINQ</span><span class="sxs-lookup"><span data-stu-id="dffbf-171">LINQ</span></span>
- <span data-ttu-id="dffbf-172">NCL</span><span class="sxs-lookup"><span data-stu-id="dffbf-172">NCL</span></span>
- <span data-ttu-id="dffbf-173">.NET Standard</span><span class="sxs-lookup"><span data-stu-id="dffbf-173">.NET Standard</span></span>
- <span data-ttu-id="dffbf-174">Интерфейсы API Roslyn</span><span class="sxs-lookup"><span data-stu-id="dffbf-174">Roslyn APIs</span></span>
- <span data-ttu-id="dffbf-175">Безопасность</span><span class="sxs-lookup"><span data-stu-id="dffbf-175">Security</span></span>
- <span data-ttu-id="dffbf-176">WCF</span><span class="sxs-lookup"><span data-stu-id="dffbf-176">WCF</span></span>
- <span data-ttu-id="dffbf-177">WF</span><span class="sxs-lookup"><span data-stu-id="dffbf-177">WF</span></span>
- <span data-ttu-id="dffbf-178">WIF</span><span class="sxs-lookup"><span data-stu-id="dffbf-178">WIF</span></span>
- <span data-ttu-id="dffbf-179">WinForms</span><span class="sxs-lookup"><span data-stu-id="dffbf-179">WinForms</span></span>
- <span data-ttu-id="dffbf-180">WPF</span><span class="sxs-lookup"><span data-stu-id="dffbf-180">WPF</span></span>

### <a name="releases"></a><span data-ttu-id="dffbf-181">Выпуски</span><span class="sxs-lookup"><span data-stu-id="dffbf-181">Releases</span></span>

<span data-ttu-id="dffbf-182">![:checkered_flag: Release: на темно-желтом фоне](./media/labels-projects/release.png "Префикс для меток выпусков")</span><span class="sxs-lookup"><span data-stu-id="dffbf-182">![:checkered_flag: Release: on dark yellow](./media/labels-projects/release.png "Prefix for release labels")</span></span>

<span data-ttu-id="dffbf-183">Проблемы, связанные с конкретным выпуском, обозначены префиксом `:checkered_flag: Release:` и имеют темно-желтый фон.</span><span class="sxs-lookup"><span data-stu-id="dffbf-183">Issues tagged for a specific release are noted with the `:checkered_flag: Release:` prefix and have a dark yellow background.</span></span>

- <span data-ttu-id="dffbf-184">.NET Core 2.2</span><span class="sxs-lookup"><span data-stu-id="dffbf-184">.NET Core 2.2</span></span>
- <span data-ttu-id="dffbf-185">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="dffbf-185">.NET Core 3.0</span></span>
- <span data-ttu-id="dffbf-186">.NET Framework 4.8</span><span class="sxs-lookup"><span data-stu-id="dffbf-186">.NET Framework 4.8</span></span>
- <span data-ttu-id="dffbf-187">.NET 5</span><span class="sxs-lookup"><span data-stu-id="dffbf-187">.NET 5</span></span>

### <a name="priority"></a><span data-ttu-id="dffbf-188">Приоритет</span><span class="sxs-lookup"><span data-stu-id="dffbf-188">Priority</span></span>

<span data-ttu-id="dffbf-189">Метки приоритета состоят из буквы `P` и одной цифры.</span><span class="sxs-lookup"><span data-stu-id="dffbf-189">Priority labels are all `P` followed by a single digit.</span></span> <span data-ttu-id="dffbf-190">Чем меньше номер, тем выше приоритет.</span><span class="sxs-lookup"><span data-stu-id="dffbf-190">Lower numbers are higher priority:</span></span>

- <span data-ttu-id="dffbf-191">P0</span><span class="sxs-lookup"><span data-stu-id="dffbf-191">P0</span></span>
- <span data-ttu-id="dffbf-192">P1</span><span class="sxs-lookup"><span data-stu-id="dffbf-192">P1</span></span>
- <span data-ttu-id="dffbf-193">P2</span><span class="sxs-lookup"><span data-stu-id="dffbf-193">P2</span></span>
- <span data-ttu-id="dffbf-194">P3</span><span class="sxs-lookup"><span data-stu-id="dffbf-194">P3</span></span>

### <a name="what-about-the-other-labels"></a><span data-ttu-id="dffbf-195">Другие метки</span><span class="sxs-lookup"><span data-stu-id="dffbf-195">What about the other labels?</span></span>

<span data-ttu-id="dffbf-196">Команда по разработке содержимого использует также много других меток для классификации проблем иными способами.</span><span class="sxs-lookup"><span data-stu-id="dffbf-196">There are many other labels used by the content teams to manage different classifications of issues.</span></span> <span data-ttu-id="dffbf-197">Если вы не являетесь участником этой команды, данные метки можно игнорировать.</span><span class="sxs-lookup"><span data-stu-id="dffbf-197">If you're not on the content team, you can ignore these other labels.</span></span>

## <a name="projects"></a><span data-ttu-id="dffbf-198">Проекты</span><span class="sxs-lookup"><span data-stu-id="dffbf-198">Projects</span></span>

<span data-ttu-id="dffbf-199">Мы используем проекты двумя способами.</span><span class="sxs-lookup"><span data-stu-id="dffbf-199">We use projects in two ways:</span></span>

- <span data-ttu-id="dffbf-200">Проекты типа "месяц YYYY": это доски Scrum для рабочих планов на каждый месяц.</span><span class="sxs-lookup"><span data-stu-id="dffbf-200">Month YYYY project types: These are scrum boards for each month's working plan.</span></span>
- <span data-ttu-id="dffbf-201">Долговременные ситуации: используются для упорядочения задач, работа над которыми будет продолжаться несколько месяцев.</span><span class="sxs-lookup"><span data-stu-id="dffbf-201">Long-running epics: These are used to organize tasks toward a goal when the work will occur over several months.</span></span>
