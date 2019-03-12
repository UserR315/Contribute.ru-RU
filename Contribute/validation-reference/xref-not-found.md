---
title: xref-not-found
description: Объяснение проблемы со сборкой документов xref-not-found и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: d51eace291bfac179be2701463d113c06627f92f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427878"
---
# <a name="xref-not-found"></a>xref-not-found

## <a name="warning"></a>Предупреждение

`Cross reference not found: '<xref: {uid}>'.`

`Cross reference not found: '@{uid}'.`

Связанный уникальный идентификатор не существует или недоступен для вашего репозитория.

## <a name="resolution"></a>Способы устранения

Убедитесь в том, что указан правильный уникальный идентификатор и что в репозитории правильно настроена служба Xref, как описано в [документации](https://review.docs.microsoft.com/en-us/help/onboard/admin/xref-service?branch=master) на внутреннем сайте корпорации Майкрософт.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
