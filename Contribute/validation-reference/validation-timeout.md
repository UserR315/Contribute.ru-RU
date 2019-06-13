---
title: validation-timeout
description: Объяснение проблемы validation-timeout, связанной со сборкой документов, и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 018634b1c5fba0848fb36a70d81c46be9acf2ecd
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/12/2019
ms.locfileid: "67024217"
---
# <a name="validation-timeout"></a>validation-timeout

## <a name="warning"></a>Предупреждение

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and open your PR. If you continue to see this message, file an issue via https://SiteHelp.`

Иногда временные проблемы в службе проверки, например "server in a bad state" (Сервер находится в нерабочем состоянии), препятствуют вызову службы при сборке документов. После трех попыток время ожидания вызова истекает и проверка отменяется, чтобы избежать задержек при сборке и затруднений в работе конвейера сборки.

## <a name="resolution"></a>Способы устранения

Попробуйте закрыть и повторно открыть запрос на вытягивание или еще раз запустите задачу сборки вручную (только для администраторов репозитория). Часто проблемы со службой исчезают сами собой после первой повторной попытки. Если сообщение по-прежнему поступает, сообщите о проблеме на сайте [https://SiteHelp](https://SiteHelp) (для сотрудников корпорации Майкрософт). Сторонние участники могут @упомянуть имя автора статьи в запросе на вытягивание, чтобы получить помощь.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
