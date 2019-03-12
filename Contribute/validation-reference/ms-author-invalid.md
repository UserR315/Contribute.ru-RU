---
title: ms-author-invalid
description: Объяснение проблемы со сборкой документов ms-author-invalid и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 210ff6a18bd12585c81f461a87238aa8d20c0530
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427856"
---
# <a name="ms-author-invalid"></a>ms-author-invalid

**Ожидается в ближайшее время.**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Предложение

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not a whitelisted distribution list.`

## <a name="resolution"></a>Способы устранения

Проверьте, является ли значение `ms.author` допустимым псевдонимом Майкрософт. Если псевдоним используется для списка рассылки, он должен быть добавлен в список разрешенных.

Допустимые значения можно найти на [этом внутреннем сайте корпорации Майкрософт](https://docsmetadatatool.azurewebsites.net/whitelists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
