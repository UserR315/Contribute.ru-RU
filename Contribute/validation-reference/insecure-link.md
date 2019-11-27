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
# <a name="insecure-link"></a><span data-ttu-id="5aab0-103">insecure-link</span><span class="sxs-lookup"><span data-stu-id="5aab0-103">insecure-link</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5aab0-104">Это правило изначально использовалось как "Предложение", чтобы дать командам по работе с содержимым время на оценку возможных последствий и разработку плана по очистке своих репозиториев.</span><span class="sxs-lookup"><span data-stu-id="5aab0-104">This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos.</span></span> <span data-ttu-id="5aab0-105">**Ему будет назначено состояние "Предупреждение" с 20 декабря 2019 г**.</span><span class="sxs-lookup"><span data-stu-id="5aab0-105">**It will be elevated to a "Warning" on 12/20/2019**.</span></span>

## <a name="suggestion"></a><span data-ttu-id="5aab0-106">Предложение</span><span class="sxs-lookup"><span data-stu-id="5aab0-106">Suggestion</span></span>

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

<span data-ttu-id="5aab0-107">Это сообщение означает, что вы либо использовали явную ссылку Markdown с `http`, либо использовали необработанный URL-адрес, например `www.microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="5aab0-107">This message means that you either used an explicit Markdown link with `http` or you used a raw URL, such as `www.microsoft.com`.</span></span> <span data-ttu-id="5aab0-108">Необработанные URL-адреса преобразуются в небезопасные ссылки при публикации в документации, поэтому не должны использоваться.</span><span class="sxs-lookup"><span data-stu-id="5aab0-108">Raw URLs are converted to insecure links when published to Docs, and should not be used.</span></span>

## <a name="resolution"></a><span data-ttu-id="5aab0-109">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="5aab0-109">Resolution</span></span>

<span data-ttu-id="5aab0-110">Измените все URL-адреса сайтов Майкрософт так, чтобы в них использовался префикс `https`, а не `http`.</span><span class="sxs-lookup"><span data-stu-id="5aab0-110">Change all URLs to Microsoft sites to use `https` instead of `http`.</span></span>

<span data-ttu-id="5aab0-111">Если ссылка представляет собой необработанный URL-адрес, измените ее на явную ссылку Markdown, начинающуюся с `https`, например:</span><span class="sxs-lookup"><span data-stu-id="5aab0-111">If your link is a raw URL, change it to an explicit Markdown link beginning with `https`, such as:</span></span>

```md
`[www.microsoft.com](https://www.microsoft.com)`.
```

> [!TIP]
> <span data-ttu-id="5aab0-112">Расширение Docs Markdown для VS Code включает в себя скрипт очистки для ссылок на сайты Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="5aab0-112">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="5aab0-113">Он проверяет все ссылки на сайты Майкрософт в репозитории на предмет того, что они начинаются с `https`, а не `http`, и не содержат коды языковых стандартов, например `en-us`.</span><span class="sxs-lookup"><span data-stu-id="5aab0-113">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="5aab0-114">Чтобы запустить этот скрипт, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5aab0-114">To run the script:</span></span>
>
> 1. <span data-ttu-id="5aab0-115">Установите расширение [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) для VS Code.</span><span class="sxs-lookup"><span data-stu-id="5aab0-115">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="5aab0-116">Нажмите клавиши ALT+M, чтобы открыть меню Markdown.</span><span class="sxs-lookup"><span data-stu-id="5aab0-116">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="5aab0-117">Выберите пункт **Cleanup** (Очистка), а затем — **Microsoft links** (Ссылки на сайты Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="5aab0-117">Select **Cleanup**, then **Microsoft links**.</span></span>

<span data-ttu-id="5aab0-118">В некоторых случаях может потребоваться зафиксировать веб-адреса (например, полные доменные имена), которые не должны использоваться как доступные для щелчка ссылки.</span><span class="sxs-lookup"><span data-stu-id="5aab0-118">In some cases, you might need to document web addresses, such as fully-qualified domain names, that aren't meant to be clickable links.</span></span> <span data-ttu-id="5aab0-119">Их нужно указывать в стиле встроенного кода, например:</span><span class="sxs-lookup"><span data-stu-id="5aab0-119">These should be styled as inline code, such as:</span></span>

```md
`www.microsoft.com:90`
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
