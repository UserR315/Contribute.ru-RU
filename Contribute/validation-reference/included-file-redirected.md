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
# <a name="included-file-redirected"></a><span data-ttu-id="2f40a-103">included-file-redirected</span><span class="sxs-lookup"><span data-stu-id="2f40a-103">included-file-redirected</span></span>

## <a name="warning"></a><span data-ttu-id="2f40a-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="2f40a-104">Warning</span></span>

`Included file '{include path}' is redirected to '{target file path}'. Only include files that are not redirected and that are located in an includes folder.`

## <a name="resolution"></a><span data-ttu-id="2f40a-105">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="2f40a-105">Resolution</span></span>

<span data-ttu-id="2f40a-106">Реструктуризируйте содержимое так, чтобы не включать перенаправленный файл.</span><span class="sxs-lookup"><span data-stu-id="2f40a-106">Restructure your content so you aren't including a redirected file.</span></span> <span data-ttu-id="2f40a-107">Например, создайте включаемый файл или удалите включаемую ссылку на содержимое либо добавьте встроенную ссылку.</span><span class="sxs-lookup"><span data-stu-id="2f40a-107">For example, create a new file to include or remove the included reference and link to content or write it inline.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
