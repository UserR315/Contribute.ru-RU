---
title: hard-coded-locale
description: Объяснение проблемы со сборкой документов hard-coded-locale и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/18/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ab511398cbd622906ccb0a67e2b24968ee29374
ms.sourcegitcommit: 55624c641bea5367bcfa08655c085bc950e8beae
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/30/2019
ms.locfileid: "73166832"
---
# <a name="hard-coded-locale"></a>hard-coded-locale

> [!IMPORTANT]
> Это правило изначально использовалось как "Предложение", чтобы дать командам по работе с содержимым время на оценку возможных последствий и разработку плана по очистке своих репозиториев. **Ему будет назначено состояние "Предупреждение" с 20 декабря 2019 г**.

## <a name="suggestion"></a>Предложение

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to most Microsoft sites.`

Ссылки на некоторые сайты Майкрософт не должны содержать коды языкового стандарта, такие как `en-us`. Если вы включите код языкового стандарта в ссылку на содержимое на английском языке, он также будет включен в локализованные ссылки, в результате чего эффективность локализации будет поставлена под сомнение. Например, если ссылка на локализованное содержимое на русском языке содержит код `en-us`, пользователи из России будут переходить по ней к статье на английском языке даже в том случае, если будет доступна русскоязычная версия публикации.

В область этой проверки входят следующие сайты:

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com (кроме social.msdn.com, которому требуется языковой стандарт для ссылки на корректный форум)
- technet.microsoft.com

## <a name="resolution"></a>Способы устранения

Удалите коды языковых стандартов из ссылок на сайты Майкрософт. Ниже приведен пример:

До:

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

После:

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> Расширение Docs Markdown для VS Code включает в себя скрипт очистки для ссылок на сайты Майкрософт. Он проверяет все ссылки на сайты Майкрософт в репозитории на предмет того, что они начинаются с `https`, а не `http`, и не содержат коды языковых стандартов, например `en-us`. Чтобы запустить этот скрипт, выполните указанные ниже действия.
>
> 1. Установите расширение [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) для VS Code.
> 1. Нажмите клавиши ALT+M, чтобы открыть меню Markdown.
> 1. Выберите пункт **Cleanup** (Очистка), а затем — **Microsoft links** (Ссылки на сайты Майкрософт).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
