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
# <a name="contributing-to-powershell-documentation"></a>Участие в составлении документации по PowerShell

Благодарим вас за проявленный интерес к документации по PowerShell.

В этом документе рассказывается, как участвовать в написании статей и примеров кода, размещенных на сайте документации по PowerShell. Вы можете просто исправить опечатку или написать целую статью.

Сайт с документацией по PowerShell состоит из нескольких репозиториев, каждый из которых содержит один или несколько наборов документов:

- [Справочник по основным понятиям и командлетам PowerShell][psdocs]
- Примеры кода для пакета SDK PowerShell — частный репозиторий с примерами, используемыми в статьях о пакете SDK
- [Справочник по пакету SDK .NET для PowerShell](/dotnet/api/?view=pscore-6.2.0) — содержимое частного репозитория, созданное из исходного кода PowerShell

Проблемы, связанные со всем этим содержимым, отслеживаются в репозитории [PowerShell-Docs][docsrepo].

## <a name="repository-structure"></a>Структура репозитория

Репозиторий PowerShell-Docs состоит из трех наборов документов, которые публикуются на сайте [Документации Майкрософт][psdocs]. Наборы документов содержатся в указанных ниже папках.

- [/reference/][ref] — содержит справку по командлетам, входящим в состав PowerShell. Справка разбита по папкам версий (3.0, 4.0, 5.0, 5.1, 6 и 7). Этот набор документов не содержит справки по модулям, входящим в состав Windows или других продуктов Майкрософт.
- [/reference/docs-conceptual][conceptual] — содержит концептуальную документацию по PowerShell. Сюда входят инструкции по установке, примеры скриптов, практические руководства и многое другое.
- [/developer/][SDK] — содержит концептуальную документацию по пакету SDK для PowerShell.

<!--link refs-->
[psdocs]: https://docs.microsoft.com/powershell
[docsrepo]: https://github.com/MicrosoftDocs/PowerShell-Docs
[ref]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference
[conceptual]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference/docs-conceptual
[SDK]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/developer
