---
title: circular-reference
description: Объяснение проблемы со сборкой документов circular-reference и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4600465cf940efa82c61bcbac4a1d912c16e6903
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459218"
---
# <a name="circular-reference"></a>circular-reference

## <a name="error"></a>Ошибка

`Files '{file name 1}' and '{file name 2}' reference each other.`

Например, это может быть включаемый файл со ссылкой на текущий файл или ссылка на файл, из которого происходит перенаправление на текущий файл.

## <a name="resolution"></a>Способы устранения

Проверьте ссылки в файлах и внесите необходимые изменения, чтобы файлы не содержали ссылки на себя или не включали сами себя.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
