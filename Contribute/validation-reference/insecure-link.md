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
# <a name="insecure-link"></a><span data-ttu-id="c0c67-103">insecure-link</span><span class="sxs-lookup"><span data-stu-id="c0c67-103">insecure-link</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c0c67-104">Это правило изначально использовалось как "Предложение", чтобы дать командам по работе с содержимым время на оценку возможных последствий и разработку плана по очистке своих репозиториев.</span><span class="sxs-lookup"><span data-stu-id="c0c67-104">This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos.</span></span> <span data-ttu-id="c0c67-105">**Ему будет назначено состояние "Предупреждение" с 20 декабря 2019 г**.</span><span class="sxs-lookup"><span data-stu-id="c0c67-105">**It will be elevated to a "Warning" on 12/20/2019**.</span></span>

## <a name="suggestion"></a><span data-ttu-id="c0c67-106">Предложение</span><span class="sxs-lookup"><span data-stu-id="c0c67-106">Suggestion</span></span>

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

<span data-ttu-id="c0c67-107">Это сообщение означает, что вы либо использовали явную ссылку Markdown с `http`, либо использовали необработанный URL-адрес, например `www.microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="c0c67-107">This message means that you either used an explicit Markdown link with `http` or you used a raw URL, such as `www.microsoft.com`.</span></span> <span data-ttu-id="c0c67-108">Необработанные URL-адреса преобразуются в небезопасные ссылки при публикации в документации, поэтому не должны использоваться.</span><span class="sxs-lookup"><span data-stu-id="c0c67-108">Raw URLs are converted to insecure links when published to Docs, and should not be used.</span></span>

## <a name="resolution"></a><span data-ttu-id="c0c67-109">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="c0c67-109">Resolution</span></span>

<span data-ttu-id="c0c67-110">Измените все URL-адреса сайтов Майкрософт так, чтобы в них использовался префикс `https`, а не `http`.</span><span class="sxs-lookup"><span data-stu-id="c0c67-110">Change all URLs to Microsoft sites to use `https` instead of `http`.</span></span>

<span data-ttu-id="c0c67-111">Если ссылка является необработанным URL-адресом, измените ее на явную ссылку Markdown, начинающуюся с `https`.</span><span class="sxs-lookup"><span data-stu-id="c0c67-111">If your link is a raw URL, change it to an explicit Markdown link beginning with `https`.</span></span>

> [!TIP]
> <span data-ttu-id="c0c67-112">Расширение Docs Markdown для VS Code включает в себя скрипт очистки для ссылок на сайты Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="c0c67-112">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="c0c67-113">Он проверяет все ссылки на сайты Майкрософт в репозитории на предмет того, что они начинаются с `https`, а не `http`, и не содержат коды языковых стандартов, например `en-us`.</span><span class="sxs-lookup"><span data-stu-id="c0c67-113">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="c0c67-114">Чтобы запустить этот скрипт, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c0c67-114">To run the script:</span></span>
>
> 1. <span data-ttu-id="c0c67-115">Установите расширение [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) для VS Code.</span><span class="sxs-lookup"><span data-stu-id="c0c67-115">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="c0c67-116">Нажмите клавиши ALT+M, чтобы открыть меню Markdown.</span><span class="sxs-lookup"><span data-stu-id="c0c67-116">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="c0c67-117">Выберите пункт **Cleanup** (Очистка), а затем — **Microsoft links** (Ссылки на сайты Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="c0c67-117">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
