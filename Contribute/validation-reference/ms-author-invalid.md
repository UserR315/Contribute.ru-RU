---
title: ms-author-invalid
description: Объяснение проблемы со сборкой документов ms-author-invalid и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ae01c34ea60cec30698d7e11264d05c3f398d1c
ms.sourcegitcommit: 1311ccbbf38312bfe6947082870bc9e90d38c986
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/11/2019
ms.locfileid: "67791554"
---
# <a name="ms-author-invalid"></a>ms-author-invalid

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Предложение

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a>Способы устранения

Проверьте, что значение `ms.author` является допустимым псевдонимом Майкрософт текущего автора. Если псевдоним используется для списка рассылки, он должен быть добавлен в список разрешенных.

Допустимые значения для списков рассылки см. на [этом внутреннем сайте Майкрософт](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
