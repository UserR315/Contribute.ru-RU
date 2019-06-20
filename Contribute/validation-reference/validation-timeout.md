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
# <a name="validation-timeout"></a><span data-ttu-id="f124d-103">validation-timeout</span><span class="sxs-lookup"><span data-stu-id="f124d-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="f124d-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="f124d-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or rebuild your branch via Docs Portal (requires admin permissions). If you need admin help or  If you continue to see this message, file an issue via https://SiteHelp.`

<span data-ttu-id="f124d-105">Иногда временные проблемы в службе проверки, например "server in a bad state" (Сервер находится в нерабочем состоянии), препятствуют вызову службы при сборке документов.</span><span class="sxs-lookup"><span data-stu-id="f124d-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="f124d-106">После нескольких попыток время ожидания вызова истекает и проверка отменяется, чтобы избежать задержек при сборке и затруднений в работе конвейера сборки.</span><span class="sxs-lookup"><span data-stu-id="f124d-106">After several tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="f124d-107">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="f124d-107">Resolution</span></span>

<span data-ttu-id="f124d-108">Попробуйте закрыть и повторно открыть запрос на включение внесенных изменений или еще раз запустите задачу сборки вручную на портале документации (только для администраторов репозитория).</span><span class="sxs-lookup"><span data-stu-id="f124d-108">Try closing and re-opening your PR, or re-running a manual build via Docs Portal (repo admins only).</span></span> <span data-ttu-id="f124d-109">Часто проблемы со службой исчезают сами собой после первой повторной попытки.</span><span class="sxs-lookup"><span data-stu-id="f124d-109">Often service issues clear themselves up after the initial retry.</span></span> <span data-ttu-id="f124d-110">Если вам требуется помощь администратора или это сообщение по-прежнему поступает, сообщите о проблеме на сайте [https://SiteHelp](https://SiteHelp) (для сотрудников корпорации Майкрософт). Сторонние участники могут @упомянуть имя автора статьи в запросе на включение внесенных изменений, чтобы получить помощь.</span><span class="sxs-lookup"><span data-stu-id="f124d-110">If you need help from an admin or if you continue to get this message, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
