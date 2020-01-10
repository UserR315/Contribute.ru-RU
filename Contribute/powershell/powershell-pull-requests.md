---
title: Отправка запроса на вытягивание
description: В этой статье описывается процесс отправки запросов на вытягивание и рекомендации по обеспечению слияния внесенных изменений.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 156b5ec7b77bba5cf0a0ef2756ed8b64c21a8342
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188223"
---
# <a name="best-practices-for-pull-requests"></a><span data-ttu-id="e05f4-103">Рекомендации по запросам на вытягивание</span><span class="sxs-lookup"><span data-stu-id="e05f4-103">Best Practices for Pull requests</span></span>

<span data-ttu-id="e05f4-104">Чтобы опубликовать изменения содержимого, необходимо отправить запрос на вытягивание из своей вилки.</span><span class="sxs-lookup"><span data-stu-id="e05f4-104">To publish changes to content, you submit a pull request from your fork.</span></span> <span data-ttu-id="e05f4-105">Все запросы на вытягивание должны проходить проверку перед слиянием.</span><span class="sxs-lookup"><span data-stu-id="e05f4-105">Every pull request has to be reviewed before it can be merged.</span></span>

## <a name="target-the-correct-branch"></a><span data-ttu-id="e05f4-106">Выбор правильной ветви</span><span class="sxs-lookup"><span data-stu-id="e05f4-106">Target the correct branch</span></span>

<span data-ttu-id="e05f4-107">Все изменения должны вноситься в ветвь `staging`.</span><span class="sxs-lookup"><span data-stu-id="e05f4-107">All changes should be made to the `staging` branch.</span></span> <span data-ttu-id="e05f4-108">В ветвь `live` изменения отправлять нельзя.</span><span class="sxs-lookup"><span data-stu-id="e05f4-108">Changes should never be targeted at the `live` branch.</span></span> <span data-ttu-id="e05f4-109">Изменения, внесенные в ветвь `staging`, объединяются с `live`, поэтому изменения, внесенные в `live`, перезаписываются.</span><span class="sxs-lookup"><span data-stu-id="e05f4-109">Changes made in the `staging` branch get merged into `live` so any changes made to `live` are overwritten.</span></span>

<span data-ttu-id="e05f4-110">Если вы отправляете изменение в документацию, которое относится только к невыпущенной версии PowerShell, проверьте наличие ветви выпуска для этой версии.</span><span class="sxs-lookup"><span data-stu-id="e05f4-110">If you are submitting a change to documentation that only applies to an unreleased version of PowerShell, check to see if there is a release branch for that version.</span></span> <span data-ttu-id="e05f4-111">Все изменения, которые относятся к определенной будущей версии, должны направляться в ветвь выпуска.</span><span class="sxs-lookup"><span data-stu-id="e05f4-111">All changes that apply to a specific, future version should be targeted at the release branch.</span></span> <span data-ttu-id="e05f4-112">Имена ветвей выпуска строятся по следующему шаблону: `release-<version>`.</span><span class="sxs-lookup"><span data-stu-id="e05f4-112">Release branches have the following name pattern: `release-<version>`.</span></span>

## <a name="make-the-pull-request-queue-work-better-for-everyone"></a><span data-ttu-id="e05f4-113">Как ускорить обработку запросов на вытягивание в очереди</span><span class="sxs-lookup"><span data-stu-id="e05f4-113">Make the pull request queue work better for everyone</span></span>

<span data-ttu-id="e05f4-114">Обработка очереди запросов на вытягивание выполняется так:</span><span class="sxs-lookup"><span data-stu-id="e05f4-114">There are two basic realities in the PR queue:</span></span>

- <span data-ttu-id="e05f4-115">Запросы на вытягивание меньшего объема и со связанными изменениями обрабатываются быстрее.</span><span class="sxs-lookup"><span data-stu-id="e05f4-115">Pull requests that are small in scope and relate changes take less time to review.</span></span>
- <span data-ttu-id="e05f4-116">Запросы на вытягивание большего объема или с несвязанными изменениями обрабатываются дольше.</span><span class="sxs-lookup"><span data-stu-id="e05f4-116">Pull requests that are large in scope or that contain unrelated changes take more time to review.</span></span>

### <a name="avoid-branches-that-update-large-numbers-of-files"></a><span data-ttu-id="e05f4-117">Как избежать использования ветвей с обновлением большого количества файлов</span><span class="sxs-lookup"><span data-stu-id="e05f4-117">Avoid branches that update large numbers of files</span></span>

<span data-ttu-id="e05f4-118">Создавайте запросы на незначительные обновления для существующих статей отдельно от запросов на новые статьи или значительные изменения.</span><span class="sxs-lookup"><span data-stu-id="e05f4-118">Separate minor updates to existing articles from new articles or major rewrites.</span></span> <span data-ttu-id="e05f4-119">Работайте над этими изменениями в отдельных рабочих ветвях.</span><span class="sxs-lookup"><span data-stu-id="e05f4-119">Work on these changes in separate working branches.</span></span>

<span data-ttu-id="e05f4-120">Массовые изменения приводят к созданию запросов на вытягивание с большим количеством измененных файлов.</span><span class="sxs-lookup"><span data-stu-id="e05f4-120">Bulk changes drive PRs with large numbers of changed files.</span></span> <span data-ttu-id="e05f4-121">Включайте в запросы на вытягивание не более 50 измененных файлов.</span><span class="sxs-lookup"><span data-stu-id="e05f4-121">Limit your PRs to a maximum of 50 changed files.</span></span> <span data-ttu-id="e05f4-122">Большие запросы на вытягивание труднее проверять, и они более подвержены ошибкам.</span><span class="sxs-lookup"><span data-stu-id="e05f4-122">Large PRs are difficult to review and are more prone to contain errors.</span></span>

### <a name="renaming-or-deleting-files"></a><span data-ttu-id="e05f4-123">Переименование или удаление файлов</span><span class="sxs-lookup"><span data-stu-id="e05f4-123">Renaming or deleting files</span></span>

<span data-ttu-id="e05f4-124">Если необходимо переименовать или удалить файлы, не совмещайте это с добавлением или обновлением содержимого.</span><span class="sxs-lookup"><span data-stu-id="e05f4-124">When you rename or delete files, avoid mixing these changes with content additions or updates.</span></span>
<span data-ttu-id="e05f4-125">Создайте для этих изменений отдельный запрос на вытягивание. Его слияние должно выполняться после обработки запроса на вытягивание для связанных дополнений.</span><span class="sxs-lookup"><span data-stu-id="e05f4-125">Handle these changes in a separate PR that gets merged after the PR for related updates.</span></span> <span data-ttu-id="e05f4-126">Например, перед удалением статьи обновляется файл перенаправлений и проверяется их работа.</span><span class="sxs-lookup"><span data-stu-id="e05f4-126">For example, update the redirects file and verify the redirect is working before deleting an article.</span></span>

<span data-ttu-id="e05f4-127">Необходимо обновить все файлы, в которых есть ссылки на переименованный файл.</span><span class="sxs-lookup"><span data-stu-id="e05f4-127">You must update all files that link to the renamed file.</span></span> <span data-ttu-id="e05f4-128">Это относится и к файлам оглавлений.</span><span class="sxs-lookup"><span data-stu-id="e05f4-128">This includes any TOC files.</span></span> <span data-ttu-id="e05f4-129">Кроме того, необходимо добавить записи перенаправления в главный файл перенаправлений (`.openpublishing.redirection.json`) в корневом каталоге репозитория.</span><span class="sxs-lookup"><span data-stu-id="e05f4-129">You must also add redirection entries in the master redirection file (`.openpublishing.redirection.json`) in the root of the repository.</span></span>

## <a name="docs-pr-validation-service"></a><span data-ttu-id="e05f4-130">Служба проверки запросов на вытягивание документов</span><span class="sxs-lookup"><span data-stu-id="e05f4-130">Docs PR validation service</span></span>

<span data-ttu-id="e05f4-131">Служба проверки запросов на вытягивание документов представляет собой приложение GitHub, которое применяет правила проверки к файлам в запросах на вытягивание.</span><span class="sxs-lookup"><span data-stu-id="e05f4-131">The Docs PR validation service is a GitHub app that runs validation rules on the files in a PR.</span></span>

<span data-ttu-id="e05f4-132">Работает она так.</span><span class="sxs-lookup"><span data-stu-id="e05f4-132">You'll see the following behavior:</span></span>

1. <span data-ttu-id="e05f4-133">Вы отправляете запрос на вытягивание.</span><span class="sxs-lookup"><span data-stu-id="e05f4-133">You submit a PR.</span></span>
1. <span data-ttu-id="e05f4-134">В комментарии GitHub, указывающем на состояние вашего запроса на вытягивание, отображается состояние проверок, включенных для репозитория.</span><span class="sxs-lookup"><span data-stu-id="e05f4-134">In the GitHub comment that indicates the status of your PR, you'll see the status of "checks" enabled on the repo.</span></span> <span data-ttu-id="e05f4-135">Обратите внимание, что в этом примере включены две проверки: "Проверка фиксации" и "OpenPublishing.Build":</span><span class="sxs-lookup"><span data-stu-id="e05f4-135">Note that in this example, there are two checks enabled, "Commit Validation" and "OpenPublishing.Build":</span></span>

   ![сбой некоторых проверок](media/powershell-pull-requests/validation-failed.png)

   <span data-ttu-id="e05f4-137">Сборка может быть выполнена даже в том случае, если проверка фиксации завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="e05f4-137">Build can pass even if commit validation fails.</span></span>

1. <span data-ttu-id="e05f4-138">Выберите пункт **Подробности**, чтобы просмотреть дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="e05f4-138">Click **Details** for more information.</span></span>
1. <span data-ttu-id="e05f4-139">На странице подробностей отображаются проверки, которые завершились сбоем, а также сведения об устранении соответствующих проблем.</span><span class="sxs-lookup"><span data-stu-id="e05f4-139">On the Details page, you'll see all the validation checks that failed, with information about how to fix the issues.</span></span>
1. <span data-ttu-id="e05f4-140">При успешном завершении проверки к запросу на вытягивание добавляется следующий комментарий:</span><span class="sxs-lookup"><span data-stu-id="e05f4-140">When validation succeeds, the following comment is added to the PR:</span></span>

   ![build validation (проверка сборки)](media/powershell-pull-requests/build-validation.png)

<span data-ttu-id="e05f4-142">У внешних авторов (не являющихся сотрудниками корпорации Майкрософт) нет доступа к подробным отчетам о сборке и ссылкам для предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="e05f4-142">If you are an external (non-Microsoft) contributor you do not have access to the detailed build reports or preview links.</span></span>

### <a name="build-warnings"></a><span data-ttu-id="e05f4-143">Предупреждения о сборке</span><span class="sxs-lookup"><span data-stu-id="e05f4-143">Build warnings</span></span>

<span data-ttu-id="e05f4-144">Как правило, следует исправлять все ошибки сборки, а также учитывать все предупреждения и предложения.</span><span class="sxs-lookup"><span data-stu-id="e05f4-144">Normally you should fix all build errors, warnings, and suggestions.</span></span> <span data-ttu-id="e05f4-145">Однако некоторые предупреждения можно игнорировать.</span><span class="sxs-lookup"><span data-stu-id="e05f4-145">However, there are some warnings that can be ignored.</span></span>

<span data-ttu-id="e05f4-146">Они приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="e05f4-146">The following warnings can be ignored:</span></span>

- > <span data-ttu-id="e05f4-147">Не найдено имя службы для `<version>/<modulepath>/About/About.md`</span><span class="sxs-lookup"><span data-stu-id="e05f4-147">Can't find service name for `<version>/<modulepath>/About/About.md`</span></span>

- > <span data-ttu-id="e05f4-148">Метаданные со следующими именами нельзя задать в заголовке YAML либо как метаданные на уровне файла, либо как глобальные метаданные в файле docfx.json: `locale`.</span><span class="sxs-lookup"><span data-stu-id="e05f4-148">Metadata with following name(s) are not allowed to be set in Yaml header, or as file level metadata in docfx.json, or as global metadata in docfx.json: `locale`.</span></span> <span data-ttu-id="e05f4-149">Они создаются платформой документации, поэтому значения, заданные в этих трех местах, будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="e05f4-149">They are generated by Docs platform, so the values set in these 3 places will be ignored.</span></span> <span data-ttu-id="e05f4-150">Чтобы устранить предупреждение, удалите эти значения из всех трех мест.</span><span class="sxs-lookup"><span data-stu-id="e05f4-150">Please remove them from all 3 places to resolve the warning.</span></span>
