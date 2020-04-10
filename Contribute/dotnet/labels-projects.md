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
# <a name="labels-and-projects-roadmap"></a>Принципы использования меток и проектов

Команда по разработке документации .NET активно использует [метки GitHub](https://github.com/dotnet/docs/labels) для организации работы. Путем фильтрации по сочетаниям меток мы можем быстро сосредотачиваться на интересующих нас разделах [веб-сайта документации по .NET](https://docs.microsoft.com/dotnet).

Мы также используем [проекты GitHub](https://github.com/dotnet/docs/projects) для организации спринтов и других целевых ситуаций.

В этом документе объясняется, как мы используем эти организационные средства, и приводятся ссылки на удобные фильтры, которые мы используем для поиска интересующих нас разделов.

## <a name="labels"></a>Метки

Если вы впервые приступаете к участию в работе над [dotnet/docs](https://github.com/dotnet/docs), начните с проблем с меткой [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs). Это узкоспециализированные проблемы. Они являются хорошей отправной точкой. В представлении up-for-grabs можно далее отфильтровать проблемы по области и приоритету. Хорошие проблемы для начинающих имеют метку [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue).

Мы используем метки для классификации проблем различными способами:

- [руководства по .NET](#find-a-single-net-guide) и [разделы руководств](#search-one-section-of-a-guide);
- [целевой выпуск](#releases);
- [приоритет](#priority).

Сочетая метки из каждого набора (руководство, выпуск, приоритет), можно найти узкий круг проблем, на которых вы хотели бы сосредоточиться.

### <a name="find-a-single-net-guide"></a>Поиск отдельного руководства по .NET

Каждая электронная книга по архитектуре и каждое руководство по .NET имеет свою метку.

![:book: guide на светло-зеленом фоне](./media/labels-projects/guide.png "Префикс для меток руководств по архитектуре")

Электронные книги по архитектуре обозначены префиксом `:book: guide` и имеют светло-зеленый фон. Это подробные документы по рекомендуемой архитектуре. Ниже приведены фильтры для текущих проблем, связанных с каждым из руководств по архитектуре .NET.

- [Веб-приложения ASP.NET Core](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [Blazor](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [Собственные облачные приложения](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [Жизненный цикл Docker](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [gRPC](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [Модернизация за счет контейнеров Windows](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [Микрослужбы .NET](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [Бессерверные приложения](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

Такой же стиль меток применяется и к [руководствам по проектированию платформы](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines). Эта область имеет ту же структуру меток, но запросы на вытягивание от сообщества не рекомендуются. Данные материалы воспроизводятся с разрешения и не должны редактироваться.

![:books: Area на темно-синем фоне](./media/labels-projects/area.png "Префикс для меток руководств по .NET")

Каждое руководство по .NET обозначено префиксом `:books: Area` и имеет темно-синий фон. Ниже приведены фильтры для текущих проблем, связанных с каждым из руководств по .NET.

- [Справочник по API](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [Azure .NET SDK](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk);
- [Руководство по C#](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [Руководство по классическим приложениям](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [Руководство по F#](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [Руководство по ML.NET](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- [Руководство по архитектуре .NET](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) — возможно, удалено
- [Руководство по .NET Core](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [Руководство по .NET для Apache Spark](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [Руководство по .NET Framework](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [Руководство по .NET](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- [Справочник по API Roslyn](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) — возможно, удален
- [Руководство по Visual Basic](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a>Поиск отдельного раздела руководства

![:card_file_box: Area на умеренно синем фоне](./media/labels-projects/technology.png "Префикс для меток разделов руководств по .NET")

Руководства по .NET имеют большой объем, поэтому данные метки позволяют далее ограничить область проблем отдельными разделами. Каждый раздел руководства по .NET обозначен префиксом `:card_file_box: Technology` и имеет умеренно синий фон. Многие из этих меток относятся к нескольким руководствам, а другие — только к одному. После фильтрации области добавьте одну из этих меток, чтобы сузить область проблем.

- AppCompat
- Асинхронная задача
- Углубленные понятия C#
- Компилятор C#
- Основы C#
- Начало работы с C#
- Справочник по языку C#
- NULL-безопасность в C#
- Новые возможности C#
- CLI
- Доступ к данным
- Docker
- Установщики
- LINQ
- NCL
- .NET Standard
- Интерфейсы API Roslyn
- Безопасность
- WCF
- WF
- WIF
- WinForms
- WPF

### <a name="releases"></a>Выпуски

![:checkered_flag: Release: на темно-желтом фоне](./media/labels-projects/release.png "Префикс для меток выпусков")

Проблемы, связанные с конкретным выпуском, обозначены префиксом `:checkered_flag: Release:` и имеют темно-желтый фон.

- .NET Core 2.2
- .NET Core 3.0
- .NET Framework 4.8
- .NET 5

### <a name="priority"></a>Приоритет

Метки приоритета состоят из буквы `P` и одной цифры. Чем меньше номер, тем выше приоритет.

- P0
- P1
- P2
- P3

### <a name="what-about-the-other-labels"></a>Другие метки

Команда по разработке содержимого использует также много других меток для классификации проблем иными способами. Если вы не являетесь участником этой команды, данные метки можно игнорировать.

## <a name="projects"></a>Проекты

Мы используем проекты двумя способами.

- Проекты типа "месяц YYYY": это доски Scrum для рабочих планов на каждый месяц.
- Долговременные ситуации: используются для упорядочения задач, работа над которыми будет продолжаться несколько месяцев.
