---
title: insecure-link
description: Объяснение проблемы со сборкой документов insecure-link и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4735d47cdf2029d2c613c9b333a393c7d978c58e
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528849"
---
# <a name="insecure-link"></a>insecure-link

> [!IMPORTANT]
> Это правило изначально использовалось как "Предложение", чтобы дать командам по работе с содержимым время на оценку возможных последствий и разработку плана по очистке своих репозиториев. **Ему будет назначено состояние "Предупреждение" с 20 декабря 2019 г**.

## <a name="suggestion"></a>Предложение

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

Это сообщение означает, что вы либо использовали явную ссылку Markdown с `http`, либо использовали необработанный URL-адрес, например `www.microsoft.com`. Необработанные URL-адреса преобразуются в небезопасные ссылки при публикации в документации, поэтому не должны использоваться.

## <a name="resolution"></a>Способы устранения

Измените все URL-адреса сайтов Майкрософт так, чтобы в них использовался префикс `https`, а не `http`.

Если ссылка представляет собой необработанный URL-адрес, измените ее на явную ссылку Markdown, начинающуюся с `https`, например:

```md
`[www.microsoft.com](https://www.microsoft.com)`.
```

> [!TIP]
> Расширение Docs Markdown для VS Code включает в себя скрипт очистки для ссылок на сайты Майкрософт. Он проверяет все ссылки на сайты Майкрософт в репозитории на предмет того, что они начинаются с `https`, а не `http`, и не содержат коды языковых стандартов, например `en-us`. Чтобы запустить этот скрипт, выполните указанные ниже действия.
>
> 1. Установите расширение [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) для VS Code.
> 1. Нажмите клавиши ALT+M, чтобы открыть меню Markdown.
> 1. Выберите пункт **Cleanup** (Очистка), а затем — **Microsoft links** (Ссылки на сайты Майкрософт).

В некоторых случаях может потребоваться зафиксировать веб-адреса (например, полные доменные имена), которые не должны использоваться как доступные для щелчка ссылки. Их нужно указывать в стиле встроенного кода, например:

```md
`www.microsoft.com:90`
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
