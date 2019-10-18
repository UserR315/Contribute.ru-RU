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
# <a name="insecure-link"></a><span data-ttu-id="659f9-103">insecure-link</span><span class="sxs-lookup"><span data-stu-id="659f9-103">insecure-link</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="659f9-104">Предложение</span><span class="sxs-lookup"><span data-stu-id="659f9-104">Suggestion</span></span>

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

<span data-ttu-id="659f9-105">Это сообщение означает, что вы либо использовали явную ссылку Markdown с `http`, либо использовали необработанный URL-адрес, например `www.microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="659f9-105">This message means that you either used an explicit Markdown link with `http` or you used a raw URL, such as `www.microsoft.com`.</span></span> <span data-ttu-id="659f9-106">Необработанные URL-адреса преобразуются в небезопасные ссылки при публикации в документации, поэтому не должны использоваться.</span><span class="sxs-lookup"><span data-stu-id="659f9-106">Raw URLs are converted to insecure links when published to Docs, and should not be used.</span></span>

## <a name="resolution"></a><span data-ttu-id="659f9-107">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="659f9-107">Resolution</span></span>

<span data-ttu-id="659f9-108">Измените все URL-адреса сайтов Майкрософт так, чтобы в них использовался префикс `https`, а не `http`.</span><span class="sxs-lookup"><span data-stu-id="659f9-108">Change all URLs to Microsoft sites to use `https` instead of `http`.</span></span>

<span data-ttu-id="659f9-109">Если ссылка является необработанным URL-адресом, измените ее на явную ссылку Markdown, начинающуюся с `https`.</span><span class="sxs-lookup"><span data-stu-id="659f9-109">If your link is a raw URL, change it to an explicit Markdown link beginning with `https`.</span></span>

> [!TIP]
> <span data-ttu-id="659f9-110">Расширение Docs Markdown для VS Code включает в себя скрипт очистки для ссылок на сайты Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="659f9-110">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="659f9-111">Он проверяет все ссылки на сайты Майкрософт в репозитории на предмет того, что они начинаются с `https`, а не `http`, и не содержат коды языковых стандартов, например `en-us`.</span><span class="sxs-lookup"><span data-stu-id="659f9-111">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="659f9-112">Чтобы запустить этот скрипт, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="659f9-112">To run the script:</span></span>
>
> 1. <span data-ttu-id="659f9-113">Установите расширение [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) для VS Code.</span><span class="sxs-lookup"><span data-stu-id="659f9-113">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="659f9-114">Нажмите клавиши ALT+M, чтобы открыть меню Markdown.</span><span class="sxs-lookup"><span data-stu-id="659f9-114">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="659f9-115">Выберите пункт **Cleanup** (Очистка), а затем — **Microsoft links** (Ссылки на сайты Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="659f9-115">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
