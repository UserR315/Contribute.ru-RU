---
title: validation-timeout
description: Объяснение проблемы validation-timeout, связанной со сборкой документов, и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 00461768491c25b9bafaff6b117a356d9e291e22
ms.sourcegitcommit: 412ce4ab23e758d41947043f1463e96595ba3bfe
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/12/2019
ms.locfileid: "67033298"
---
# <a name="validation-timeout"></a>validation-timeout

## <a name="warning"></a>Предупреждение

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or rebuild your branch via Docs Portal (requires admin permissions). If you need admin help or  If you continue to see this message, file an issue via https://SiteHelp.`

Иногда временные проблемы в службе проверки, например "server in a bad state" (Сервер находится в нерабочем состоянии), препятствуют вызову службы при сборке документов. После нескольких попыток время ожидания вызова истекает и проверка отменяется, чтобы избежать задержек при сборке и затруднений в работе конвейера сборки.

## <a name="resolution"></a>Способы устранения

Попробуйте закрыть и повторно открыть запрос на включение внесенных изменений или еще раз запустите задачу сборки вручную на портале документации (только для администраторов репозитория). Часто проблемы со службой исчезают сами собой после первой повторной попытки. Если вам требуется помощь администратора или это сообщение по-прежнему поступает, сообщите о проблеме на сайте [https://SiteHelp](https://SiteHelp) (для сотрудников корпорации Майкрософт). Сторонние участники могут @упомянуть имя автора статьи в запросе на включение внесенных изменений, чтобы получить помощь.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
