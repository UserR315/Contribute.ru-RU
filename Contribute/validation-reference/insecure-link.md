---
title: insecure-link
description: Объяснение проблемы со сборкой документов insecure-link и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: b97d4c4a0f61e5f3448331a56fe4bde442ff1cca
ms.sourcegitcommit: 0cb0177c209abab1a72af4f411ef527fa5cf10f9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2019
ms.locfileid: "72379511"
---
# <a name="insecure-link"></a>insecure-link

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

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
