---
author: meganbradley
ms.author: mbradley
ms.openlocfilehash: fa048980afcf3c50f7d990f9c88064df6ee5ebb5
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084624"
---
# <a name="docs-pr-validation-service"></a><span data-ttu-id="6ac73-101">Служба проверки запросов на вытягивание документов</span><span class="sxs-lookup"><span data-stu-id="6ac73-101">Docs PR validation service</span></span>

<span data-ttu-id="6ac73-102">Служба проверки запросов на вытягивание документов представляет собой приложение GitHub, которое применяет правила проверки к файлам в запросах на вытягивание.</span><span class="sxs-lookup"><span data-stu-id="6ac73-102">The Docs PR validation service is a GitHub app that runs validation rules on the files in a PR.</span></span>

<span data-ttu-id="6ac73-103">Если для репозитория включена служба проверки, рабочий процесс реализуется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6ac73-103">When the validation service is enabled on a repo, you'll see the following behavior:</span></span>

1. <span data-ttu-id="6ac73-104">Вы отправляете запрос на вытягивание.</span><span class="sxs-lookup"><span data-stu-id="6ac73-104">You submit a PR.</span></span>
1. <span data-ttu-id="6ac73-105">В комментарии GitHub, указывающем на состояние вашего запроса на вытягивание, отображается состояние проверок, включенных для репозитория.</span><span class="sxs-lookup"><span data-stu-id="6ac73-105">In the GitHub comment that indicates the status of your PR, you'll see the status of "checks" enabled on the repo.</span></span> <span data-ttu-id="6ac73-106">Обратите внимание, что в этом примере включены две проверки: "Проверка фиксации" и "OpenPublishing.Build":</span><span class="sxs-lookup"><span data-stu-id="6ac73-106">Note that in this example, there are two checks enabled, "Commit Validation" and "OpenPublishing.Build":</span></span>

   ![сбой некоторых проверок](media/validation-failed.png)

   <span data-ttu-id="6ac73-108">Сборка может быть выполнена даже в том случае, если проверка фиксации завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="6ac73-108">Build can pass even if commit validation fails.</span></span>

1. <span data-ttu-id="6ac73-109">Выберите пункт **Подробности**, чтобы просмотреть дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="6ac73-109">Click **Details** for more information.</span></span>
1. <span data-ttu-id="6ac73-110">На странице подробностей отображаются проверки, которые завершились сбоем, а также сведения об устранении соответствующих проблем:</span><span class="sxs-lookup"><span data-stu-id="6ac73-110">On the Details page, you'll see all the validation checks that failed, with information about how to fix the issues:</span></span>

   ![сообщение проверки](media/validation-details.png)

<span data-ttu-id="6ac73-112">Список доступных на данный момент в службе проверок см. в с содержании этой статьи слева.</span><span class="sxs-lookup"><span data-stu-id="6ac73-112">See the left-hand TOC of this article for the list of validations currently in the service.</span></span>