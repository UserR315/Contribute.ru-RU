---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
title: Зависящие от языкового стандарта ссылки
ms.openlocfilehash: f42a26da45b48972bfc595cb26c67ab0acfe8603
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/12/2019
ms.locfileid: "66841245"
---
# <a name="locale-specific-links"></a>Зависящие от языкового стандарта ссылки

Ссылки на некоторые сайты Майкрософт не должны содержать коды языкового стандарта, такие как `en-us`. Если вы включите код языкового стандарта в ссылку на содержимое на английском языке, он также будет включен в локализованные ссылки, в результате чего эффективность локализации будет поставлена под сомнение. Например, если ссылка на локализованное содержимое на русском языке содержит код `en-us`, пользователи из России будут переходить по ней к статье на английском языке даже в том случае, если будет доступна русскоязычная версия публикации.

Удалите коды языковых стандартов из ссылок на сайты Майкрософт. Ниже приведен пример:

До:

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

После:

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

В область этой проверки входят следующие сайты:

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
- technet.microsoft.com