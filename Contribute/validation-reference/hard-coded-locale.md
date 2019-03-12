---
title: hard-coded-locale
description: Объяснение проблемы со сборкой документов hard-coded-locale и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 1862014076fa4cbff18535095b244e8f94a17b0f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427676"
---
# <a name="hard-coded-locale"></a>hard-coded-locale

## <a name="warning"></a>Предупреждение

`Link {URL} contains locale code {code}. For localizability, remove {code} from links to Microsoft sites.`

Ссылки на некоторые сайты Майкрософт не должны содержать коды языкового стандарта, такие как `en-us`. Если вы включите код языкового стандарта в ссылку на содержимое на английском языке, он также будет включен в локализованные ссылки, в результате чего эффективность локализации будет поставлена под сомнение. Например, если ссылка на локализованное содержимое на русском языке содержит код `en-us`, пользователи из России будут переходить по ней к статье на английском языке даже в том случае, если будет доступна русскоязычная версия публикации.

В область этой проверки входят следующие сайты:

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
- technet.microsoft.com

## <a name="resolution"></a>Способы устранения

Удалите коды языковых стандартов из ссылок на сайты Майкрософт. Ниже приведен пример:

До:

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

После:

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]