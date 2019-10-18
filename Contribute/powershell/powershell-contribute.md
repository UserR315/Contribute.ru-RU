---
title: Участие в разработке репозиториев документации по PowerShell
description: В этой статье описываются репозитории, составляющие документацию по PowerShell.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 6b975c085aa42846be9951a77d3fdebbd5fb17a1
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290180"
---
# <a name="contributing-to-powershell-documentation"></a><span data-ttu-id="2906c-103">Участие в составлении документации по PowerShell</span><span class="sxs-lookup"><span data-stu-id="2906c-103">Contributing to PowerShell Documentation</span></span>

<span data-ttu-id="2906c-104">Благодарим вас за проявленный интерес к документации по PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2906c-104">Thank you for your interest in PowerShell documentation!</span></span>

<span data-ttu-id="2906c-105">В этом документе рассказывается, как участвовать в написании статей и примеров кода, размещенных на сайте документации по PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2906c-105">This document covers the process for contributing to the articles and code samples that are hosted on the PowerShell documentation site.</span></span> <span data-ttu-id="2906c-106">Вы можете просто исправить опечатку или написать целую статью.</span><span class="sxs-lookup"><span data-stu-id="2906c-106">Contributions may be as simple as typo corrections or as complex as new articles.</span></span>

<span data-ttu-id="2906c-107">Сайт с документацией по PowerShell состоит из нескольких репозиториев, каждый из которых содержит один или несколько наборов документов:</span><span class="sxs-lookup"><span data-stu-id="2906c-107">The PowerShell documentation site is built from multiple repositories containing one or more docsets:</span></span>

- <span data-ttu-id="2906c-108">[Справочник по основным понятиям и командлетам PowerShell][psdocs]</span><span class="sxs-lookup"><span data-stu-id="2906c-108">[PowerShell concepts & cmdlet reference][psdocs]</span></span>
- <span data-ttu-id="2906c-109">Примеры кода для пакета SDK PowerShell — частный репозиторий с примерами, используемыми в статьях о пакете SDK</span><span class="sxs-lookup"><span data-stu-id="2906c-109">PowerShell SDK code samples - private repository containing the samples used in the SDK articles</span></span>
- <span data-ttu-id="2906c-110">[Справочник по пакету SDK .NET для PowerShell](/dotnet/api/?view=pscore-6.2.0) — содержимое частного репозитория, созданное из исходного кода PowerShell</span><span class="sxs-lookup"><span data-stu-id="2906c-110">[PowerShell .NET SDK reference](/dotnet/api/?view=pscore-6.2.0) - private repository contents generated from PowerShell source code</span></span>

<span data-ttu-id="2906c-111">Проблемы, связанные со всем этим содержимым, отслеживаются в репозитории [PowerShell-Docs][docsrepo].</span><span class="sxs-lookup"><span data-stu-id="2906c-111">Issues for all this content are tracked in the [PowerShell-Docs][docsrepo] repository.</span></span>

## <a name="repository-structure"></a><span data-ttu-id="2906c-112">Структура репозитория</span><span class="sxs-lookup"><span data-stu-id="2906c-112">Repository Structure</span></span>

<span data-ttu-id="2906c-113">Репозиторий PowerShell-Docs состоит из трех наборов документов, которые публикуются на сайте [Документации Майкрософт][psdocs]. Наборы документов содержатся в указанных ниже папках.</span><span class="sxs-lookup"><span data-stu-id="2906c-113">The PowerShell-Docs repository consists of three docsets that are published to [Microsoft Docs][psdocs]. The docsets are contained in the following folders:</span></span>

- <span data-ttu-id="2906c-114">[/reference/][ref] — содержит справку по командлетам, входящим в состав PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2906c-114">[/reference/][ref] - contains the PowerShell cmdlet reference for the cmdlets that ship in PowerShell.</span></span> <span data-ttu-id="2906c-115">Справка разбита по папкам версий (3.0, 4.0, 5.0, 5.1, 6 и 7).</span><span class="sxs-lookup"><span data-stu-id="2906c-115">The reference is collected in versions folders (3.0, 4.0, 5.0, 5.1, 6, and 7).</span></span> <span data-ttu-id="2906c-116">Этот набор документов не содержит справки по модулям, входящим в состав Windows или других продуктов Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="2906c-116">This docset does not contain the reference for the modules that ship in Windows or other Microsoft products.</span></span>
- <span data-ttu-id="2906c-117">[/reference/docs-conceptual][conceptual] — содержит концептуальную документацию по PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2906c-117">[/reference/docs-conceptual][conceptual] - contains the PowerShell conceptual documentation.</span></span> <span data-ttu-id="2906c-118">Сюда входят инструкции по установке, примеры скриптов, практические руководства и многое другое.</span><span class="sxs-lookup"><span data-stu-id="2906c-118">This include setup instructions, sample scripts, how-to topics, and more.</span></span>
- <span data-ttu-id="2906c-119">[/developer/][SDK] — содержит концептуальную документацию по пакету SDK для PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2906c-119">[/developer/][SDK] - contains the PowerShell SDK conceptual documentation.</span></span>

<!--link refs-->
[psdocs]: https://docs.microsoft.com/powershell
[docsrepo]: https://github.com/MicrosoftDocs/PowerShell-Docs
[ref]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference
[conceptual]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference/docs-conceptual
[SDK]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/developer
