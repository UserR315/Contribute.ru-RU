---
title: insecure-link
description: Объяснение проблемы со сборкой документов insecure-link и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: c22404e624ae85369d7b0b95f44e37d51f847368
ms.sourcegitcommit: ab31cbb17c64a06cab4ffb37b157fd812417a499
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2019
ms.locfileid: "72587675"
---
# <a name="insecure-link"></a>insecure-link

> [!IMPORTANT]
> Это правило изначально использовалось как "Предложение", чтобы дать командам по работе с содержимым время на оценку возможных последствий и разработку плана по очистке своих репозиториев. **Ему будет назначено состояние "Предупреждение" с 20 декабря 2019 г**.

## <a name="suggestion"></a>Предложение

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

Это сообщение означает, что вы либо использовали явную ссылку Markdown с `http`, либо использовали необработанный URL-адрес, например `www.microsoft.com`. Необработанные URL-адреса преобразуются в небезопасные ссылки при публикации в документации, поэтому не должны использоваться.

## <a name="resolution"></a>Способы устранения

Измените все URL-адреса сайтов Майкрософт так, чтобы в них использовался префикс `https`, а не `http`.

Если ссылка является необработанным URL-адресом, измените ее на явную ссылку Markdown, начинающуюся с `https`.

> [!TIP]
> Расширение Docs Markdown для VS Code включает в себя скрипт очистки для ссылок на сайты Майкрософт. Он проверяет все ссылки на сайты Майкрософт в репозитории на предмет того, что они начинаются с `https`, а не `http`, и не содержат коды языковых стандартов, например `en-us`. Чтобы запустить этот скрипт, выполните указанные ниже действия.
>
> 1. Установите расширение [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) для VS Code.
> 1. Нажмите клавиши ALT+M, чтобы открыть меню Markdown.
> 1. Выберите пункт **Cleanup** (Очистка), а затем — **Microsoft links** (Ссылки на сайты Майкрософт).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
