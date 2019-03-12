---
title: included-file-redirected
description: Объяснение проблемы со сборкой документов included-file-redirected и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8a40f04fe1a7e7f19ab9ee7ce684684184aa4dc7
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459080"
---
# <a name="included-file-redirected"></a>included-file-redirected

## <a name="warning"></a>Предупреждение

`Included file '{include path}' is redirected to '{target file path}'. Only include files that are not redirected and that are located in an includes folder.`

## <a name="resolution"></a>Способы устранения

Реструктуризируйте содержимое так, чтобы не включать перенаправленный файл. Например, создайте включаемый файл или удалите включаемую ссылку на содержимое либо добавьте встроенную ссылку.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
