---
title: validation-timeout
description: Объяснение проблемы validation-timeout, связанной со сборкой документов, и способа ее устранения
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: f75f005ce9ab0cf332667d5c8b7778ba4ef35a0a
ms.sourcegitcommit: 254c804bb0b451c262745fe8d87e2e8f9196440c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2019
ms.locfileid: "73592541"
---
# <a name="validation-timeout"></a><span data-ttu-id="064e9-103">validation-timeout</span><span class="sxs-lookup"><span data-stu-id="064e9-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="064e9-104">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="064e9-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or force a full build of your branch via https://ops.microsoft.com. Note that forcing a full build requires admin permissions to the repo. If you don’t know who your repo admin is, or if you continue to see this message after a forced build, file an issue via https://SiteHelp.`

<span data-ttu-id="064e9-105">Иногда временные проблемы в службе проверки, например "server in a bad state" (Сервер находится в нерабочем состоянии), препятствуют вызову службы при сборке документов.</span><span class="sxs-lookup"><span data-stu-id="064e9-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="064e9-106">После нескольких попыток время ожидания вызова истекает и проверка отменяется, чтобы избежать задержек при сборке и затруднений в работе конвейера сборки.</span><span class="sxs-lookup"><span data-stu-id="064e9-106">After several tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="064e9-107">Способы устранения</span><span class="sxs-lookup"><span data-stu-id="064e9-107">Resolution</span></span>

<span data-ttu-id="064e9-108">Попробуйте закрыть и вновь открыть свой запрос на вытягивание или принудительно выполнить полную сборку на [портале Docs](https://ops.microsoft.com/#/).</span><span class="sxs-lookup"><span data-stu-id="064e9-108">Try closing and re-opening your PR, or forcing a full build via [Docs Portal](https://ops.microsoft.com/#/).</span></span> <span data-ttu-id="064e9-109">Часто проблемы со службой исчезают сами собой после первой повторной попытки.</span><span class="sxs-lookup"><span data-stu-id="064e9-109">Often service issues clear themselves up after the initial retry.</span></span>

<span data-ttu-id="064e9-110">Обратите внимание, что для принудительной сборки на портале Docs необходимо быть администратором репозитория.</span><span class="sxs-lookup"><span data-stu-id="064e9-110">Note that you must be a repo admin to force a build via Docs Portal.</span></span> <span data-ttu-id="064e9-111">Если вы не знаете администратора своего репозитория, или если сообщение продолжит появляться даже после принудительной сборки, сообщите о проблеме через [https://SiteHelp](https://SiteHelp) (если вы сотрудник Майкрософт) или обратитесь за помощью, @упомянув автора статьи в своем запросе на вытягивание (если вы внешний участник).</span><span class="sxs-lookup"><span data-stu-id="064e9-111">If you don't know who your repo admin is, or if you continue to get this message after a forced build, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<span data-ttu-id="064e9-112">Если вы администратор репозитория, принудительно выполнить полную сборку можно следующим образом.</span><span class="sxs-lookup"><span data-stu-id="064e9-112">If you're a repo admin, you can force a full build as follows:</span></span>

1. <span data-ttu-id="064e9-113">Выполните вход на [портале Docs](https://ops.microsoft.com/#/).</span><span class="sxs-lookup"><span data-stu-id="064e9-113">Go to [Docs Portal](https://ops.microsoft.com/#/) and sign in.</span></span>
1. <span data-ttu-id="064e9-114">В верхнем левом углу выполните поиск своего репозитория, а затем выберите его.</span><span class="sxs-lookup"><span data-stu-id="064e9-114">Find your repo by searching in the upper left corner, and select it.</span></span>

   <span data-ttu-id="064e9-115">:::image type="content" source="media/find-repo.png" alt-text="Найдите свой репозиторий в поле поиска на портале Docs":::</span><span class="sxs-lookup"><span data-stu-id="064e9-115">:::image type="content" source="media/find-repo.png" alt-text="find your repo via the Docs Portal search box":::</span></span>
1. <span data-ttu-id="064e9-116">На вкладке **Build History** (Журнал сборок) щелкните **+ Manual Publish** (Опубликовать вручную).</span><span class="sxs-lookup"><span data-stu-id="064e9-116">On the **Build History** tab, click **+ Manual Publish**.</span></span>
1. <span data-ttu-id="064e9-117">Выберите ветвь, которая получает предупреждение, например master (главная ветвь).</span><span class="sxs-lookup"><span data-stu-id="064e9-117">Select the branch that's getting the Warning, such as master.</span></span>
1. <span data-ttu-id="064e9-118">Для целевого объекта оставьте значение по умолчанию: **Docs Site** (Сайт документации).</span><span class="sxs-lookup"><span data-stu-id="064e9-118">For target, keep the default, **Docs Site**.</span></span>
1. <span data-ttu-id="064e9-119">Установите флажок **Force Publish** (Опубликовать принудительно).</span><span class="sxs-lookup"><span data-stu-id="064e9-119">Check the **Force Publish** checkbox.</span></span>
1. <span data-ttu-id="064e9-120">Щелкните **Publish** (Опубликовать).</span><span class="sxs-lookup"><span data-stu-id="064e9-120">Click **Publish**.</span></span>

   <span data-ttu-id="064e9-121">:::image type="content" source="media/force-build.png" alt-text="Этапы принудительного выполнения полной сборки":::</span><span class="sxs-lookup"><span data-stu-id="064e9-121">:::image type="content" source="media/force-build.png" alt-text="steps to force a full build":::</span></span>

<span data-ttu-id="064e9-122">В результате будет принудительно выполнена полная сборка ветви.</span><span class="sxs-lookup"><span data-stu-id="064e9-122">This will force a full build on the branch.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
