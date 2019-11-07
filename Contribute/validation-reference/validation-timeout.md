---
title: validation-timeout
description: Объяснение проблемы validation-timeout, связанной со сборкой документов, и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: f75f005ce9ab0cf332667d5c8b7778ba4ef35a0a
ms.sourcegitcommit: 254c804bb0b451c262745fe8d87e2e8f9196440c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2019
ms.locfileid: "73592541"
---
# <a name="validation-timeout"></a>validation-timeout

## <a name="warning"></a>Предупреждение

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or force a full build of your branch via https://ops.microsoft.com. Note that forcing a full build requires admin permissions to the repo. If you don’t know who your repo admin is, or if you continue to see this message after a forced build, file an issue via https://SiteHelp.`

Иногда временные проблемы в службе проверки, например "server in a bad state" (Сервер находится в нерабочем состоянии), препятствуют вызову службы при сборке документов. После нескольких попыток время ожидания вызова истекает и проверка отменяется, чтобы избежать задержек при сборке и затруднений в работе конвейера сборки.

## <a name="resolution"></a>Способы устранения

Попробуйте закрыть и вновь открыть свой запрос на вытягивание или принудительно выполнить полную сборку на [портале Docs](https://ops.microsoft.com/#/). Часто проблемы со службой исчезают сами собой после первой повторной попытки.

Обратите внимание, что для принудительной сборки на портале Docs необходимо быть администратором репозитория. Если вы не знаете администратора своего репозитория, или если сообщение продолжит появляться даже после принудительной сборки, сообщите о проблеме через [https://SiteHelp](https://SiteHelp) (если вы сотрудник Майкрософт) или обратитесь за помощью, @упомянув автора статьи в своем запросе на вытягивание (если вы внешний участник).

Если вы администратор репозитория, принудительно выполнить полную сборку можно следующим образом.

1. Выполните вход на [портале Docs](https://ops.microsoft.com/#/).
1. В верхнем левом углу выполните поиск своего репозитория, а затем выберите его.

   :::image type="content" source="media/find-repo.png" alt-text="Найдите свой репозиторий в поле поиска на портале Docs":::
1. На вкладке **Build History** (Журнал сборок) щелкните **+ Manual Publish** (Опубликовать вручную).
1. Выберите ветвь, которая получает предупреждение, например master (главная ветвь).
1. Для целевого объекта оставьте значение по умолчанию: **Docs Site** (Сайт документации).
1. Установите флажок **Force Publish** (Опубликовать принудительно).
1. Щелкните **Publish** (Опубликовать).

   :::image type="content" source="media/force-build.png" alt-text="Этапы принудительного выполнения полной сборки":::

В результате будет принудительно выполнена полная сборка ветви.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
