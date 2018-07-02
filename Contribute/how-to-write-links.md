---
title: Использование ссылок в документации
description: В этой статье содержатся инструкции по созданию ссылок на содержимое на сайте docs.microsoft.com.
ms.date: 06/29/2017
ms.openlocfilehash: a66e2fb4febf1947afe01919b96b1c10873cf57d
ms.sourcegitcommit: 92aef5ea8bdd692c5c393d5c8f99b9e4f672ef2b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2018
ms.locfileid: "36239733"
---
# <a name="using-links-in-documentation"></a><span data-ttu-id="580d7-103">Использование ссылок в документации</span><span class="sxs-lookup"><span data-stu-id="580d7-103">Using links in documentation</span></span>
<span data-ttu-id="580d7-104">В этой статье описывается использование гиперссылок со страниц, размещенных на сайте docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="580d7-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com.</span></span> <span data-ttu-id="580d7-105">Добавление ссылок в Markdown не представляет труда, но следует придерживаться ряда определенных правил.</span><span class="sxs-lookup"><span data-stu-id="580d7-105">Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="580d7-106">Ссылки могут указывать на содержимое на той же странице, на соседних страницах или вести на внешние сайты и URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="580d7-106">Links point users to content in the same page, point off into other neighboring pages, or point to external sites and URLs.</span></span>

<span data-ttu-id="580d7-107">В серверной части сайта docs.microsoft.com используются службы Open Publishing Services (OPS), которые поддерживают формат DocFX Flavored Markdown (DFM).</span><span class="sxs-lookup"><span data-stu-id="580d7-107">The docs.microsoft.com site backend uses Open Publishing Services (OPS) which implements DocFX Flavored Markdown (DFM).</span></span> <span data-ttu-id="580d7-108">DFM характеризуется высоким уровнем совместимости с форматом GitHub Flavored Markdown (GFM) и предоставляет дополнительные функции за счет применения расширений Markdown.</span><span class="sxs-lookup"><span data-stu-id="580d7-108">DFM is highly compatible with GitHub Flavored Markdown (GFM), and DFM adds additional functionality through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="580d7-109">Все ссылки должны быть безопасными (с протоколом `https` вместо `http`), если целевой объект поддерживает такой протокол (большинство целевых объектов поддерживают).</span><span class="sxs-lookup"><span data-stu-id="580d7-109">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="580d7-110">Текст ссылки</span><span class="sxs-lookup"><span data-stu-id="580d7-110">Link text</span></span>

<span data-ttu-id="580d7-111">Фраза для ссылки должна быть понятной.</span><span class="sxs-lookup"><span data-stu-id="580d7-111">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="580d7-112">Иными словами, это должен быть полноценный текст или название страницы, на которую указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="580d7-112">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="580d7-113">Не используйте конструкцию "щелкните здесь".</span><span class="sxs-lookup"><span data-stu-id="580d7-113">Do not use "click here."</span></span> <span data-ttu-id="580d7-114">Она плохо сказывается на SEO-оптимизации и не дает адекватного представления о целевой странице.</span><span class="sxs-lookup"><span data-stu-id="580d7-114">It's bad for SEO and doesn't adequately describe the target.</span></span>

<span data-ttu-id="580d7-115">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="580d7-115">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

<span data-ttu-id="580d7-116">**Неправильно:**</span><span class="sxs-lookup"><span data-stu-id="580d7-116">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="580d7-117">Ссылки для перехода от одной статьи к другой</span><span class="sxs-lookup"><span data-stu-id="580d7-117">Links from one article to another</span></span>

<span data-ttu-id="580d7-118">Чтобы добавить в статью, содержащую техническую документацию, встроенную ссылку на другую такую статью в том же docset, используйте следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="580d7-118">To create an inline link from a Docs technical article to another Docs technical article within the same docset, use the following link syntax:</span></span>

- <span data-ttu-id="580d7-119">Для статьи в каталоге, в которую добавляется ссылка на другую статью в том же каталоге:</span><span class="sxs-lookup"><span data-stu-id="580d7-119">An article in a directory links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="580d7-120">Для статьи в подкаталоге, в которую добавляется ссылка на статью в корневом каталоге:</span><span class="sxs-lookup"><span data-stu-id="580d7-120">An article links from a subdirectory to an article in the root directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="580d7-121">Для статьи в корневом каталоге, в которую добавляется ссылка на статью в подкаталоге:</span><span class="sxs-lookup"><span data-stu-id="580d7-121">An article in the root directory links to an article in a subdirectory:</span></span>

  `[link text](./directory/article-name.md)`

- <span data-ttu-id="580d7-122">Для статьи в подкаталоге, в которую добавляется ссылка на статью в другом подкаталоге:</span><span class="sxs-lookup"><span data-stu-id="580d7-122">An article in a subdirectory links to an article in another subdirectory:</span></span>

  `[link text](../directory/article-name.md)`

- <span data-ttu-id="580d7-123">Для статьи, ссылка на которую добавляется в разные docset (даже в рамках одного репозитория): `[link text](./directory/article-name)`</span><span class="sxs-lookup"><span data-stu-id="580d7-123">An article linking across docsets (even if in the same repository): `[link text](./directory/article-name)`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="580d7-124">Ни в одном из примеров выше `~/` не используется в качестве части ссылки.</span><span class="sxs-lookup"><span data-stu-id="580d7-124">None of the above examples use the `~/` as part of the link.</span></span> <span data-ttu-id="580d7-125">Если вы ссылаетесь на путь в корне репозитория, начните с `/`.</span><span class="sxs-lookup"><span data-stu-id="580d7-125">If you are linking to a path at the root of the repository, start with the `/`.</span></span> <span data-ttu-id="580d7-126">Добавление `~/` приведет к формированию недопустимых ссылок при навигации по репозиториям исходного кода на GitHub.</span><span class="sxs-lookup"><span data-stu-id="580d7-126">Including the `~/` produces invalid links when navigating the source repositories on GitHub.</span></span> <span data-ttu-id="580d7-127">Если начать путь с `/`, разрешение происходит успешно.</span><span class="sxs-lookup"><span data-stu-id="580d7-127">Starting the path with `/` resolves correctly.</span></span>

## <a name="links-to-anchors"></a><span data-ttu-id="580d7-128">Ссылки на привязки</span><span class="sxs-lookup"><span data-stu-id="580d7-128">Links to anchors</span></span>

<span data-ttu-id="580d7-129">Создавать привязки не требуется.</span><span class="sxs-lookup"><span data-stu-id="580d7-129">You do not have to create anchors.</span></span> <span data-ttu-id="580d7-130">Они автоматически генерируются для всех заголовков H2 во время публикации.</span><span class="sxs-lookup"><span data-stu-id="580d7-130">They're automatically generated at publishing time for all H2 headings.</span></span> <span data-ttu-id="580d7-131">Достаточно создать ссылки на разделы H2.</span><span class="sxs-lookup"><span data-stu-id="580d7-131">The only thing you have to do is create links to the H2 sections.</span></span>

- <span data-ttu-id="580d7-132">Для ссылки на заголовок в той же статье:</span><span class="sxs-lookup"><span data-stu-id="580d7-132">To link to a heading within the same article:</span></span>

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- <span data-ttu-id="580d7-133">Для ссылки на привязку в другой статье в том же подкаталоге:</span><span class="sxs-lookup"><span data-stu-id="580d7-133">To link to an anchor in another article in the same subdirectory:</span></span>

  `[link text](article-name.md#anchor-name)`
  `[Configure your profile](media-services-create-account.md#configure-your-profile)`

- <span data-ttu-id="580d7-134">Для ссылки на привязку в другом подкаталоге службы:</span><span class="sxs-lookup"><span data-stu-id="580d7-134">To link to an anchor in another service subdirectory:</span></span>

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a><span data-ttu-id="580d7-135">Ссылки во включаемых файлах</span><span class="sxs-lookup"><span data-stu-id="580d7-135">Links from includes</span></span>

<span data-ttu-id="580d7-136">Включаемые файлы содержатся в другом каталоге, поэтому для них используются более длинные относительные пути.</span><span class="sxs-lookup"><span data-stu-id="580d7-136">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="580d7-137">Чтобы добавить ссылку на статью во включаемый файл, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="580d7-137">To link to an article from an include file, use this format:</span></span>

    [link text](../articles/folder/article-name.md)

## <a name="links-in-selectors"></a><span data-ttu-id="580d7-138">Ссылки в селекторах</span><span class="sxs-lookup"><span data-stu-id="580d7-138">Links in selectors</span></span>

<span data-ttu-id="580d7-139">Если во включаемый файл внедрены селекторы, как в документации Azure, используйте следующую структуру ссылки:</span><span class="sxs-lookup"><span data-stu-id="580d7-139">If you have selectors that are embedded in an include--as does the Azure documentation team--use the following link structure:</span></span>

    > <span data-ttu-id="580d7-140">[AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]</span><span class="sxs-lookup"><span data-stu-id="580d7-140">[AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]</span></span>
    - [<span data-ttu-id="580d7-141">(Text1 | Example1 )</span><span class="sxs-lookup"><span data-stu-id="580d7-141">(Text1 | Example1 )</span></span>](../articles/folder/article-name1.md)
    - [<span data-ttu-id="580d7-142">(Text1 | Example2 )</span><span class="sxs-lookup"><span data-stu-id="580d7-142">(Text1 | Example2 )</span></span>](../articles/folder/article-name2.md)
    - [<span data-ttu-id="580d7-143">(Text2 | Example3 )</span><span class="sxs-lookup"><span data-stu-id="580d7-143">(Text2 | Example3 )</span></span>](../articles/folder/article-name3.md)
    - <span data-ttu-id="580d7-144">[(Text2 | Example4 )](../articles/folder/article-name4.md) --></span><span class="sxs-lookup"><span data-stu-id="580d7-144">[(Text2 | Example4 )](../articles/folder/article-name4.md) --></span></span>

## <a name="reference-style-links"></a><span data-ttu-id="580d7-145">Ссылки типа сносок</span><span class="sxs-lookup"><span data-stu-id="580d7-145">Reference-style links</span></span>

<span data-ttu-id="580d7-146">Ссылки типа сносок используются для того, чтобы пользователю было легче воспринимать содержимое источника.</span><span class="sxs-lookup"><span data-stu-id="580d7-146">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="580d7-147">Для ссылок типа сносок синтаксис встроенной ссылки заменяется упрощенным вариантом, который позволяет переместить длинные URL-адреса в конец статьи.</span><span class="sxs-lookup"><span data-stu-id="580d7-147">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="580d7-148">Ниже приведен пример от [Daring Fireball](https://daringfireball.net/projects/markdown/).</span><span class="sxs-lookup"><span data-stu-id="580d7-148">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="580d7-149">Встроенный текст:</span><span class="sxs-lookup"><span data-stu-id="580d7-149">Inline text:</span></span>

    I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].

<span data-ttu-id="580d7-150">Ссылки типа сносок в конце статьи:</span><span class="sxs-lookup"><span data-stu-id="580d7-150">Link references at the end of the article:</span></span>

    <!--Reference links in article-->
    [1]: http://google.com/
    [2]: http://search.yahoo.com/
    [3]: http://search.msn.com/

<span data-ttu-id="580d7-151">Обязательно используйте пробел после двоеточия перед ссылкой.</span><span class="sxs-lookup"><span data-stu-id="580d7-151">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="580d7-152">Если при добавлении ссылок на другие технические статьи вы забудете включить пробел, ссылка не будет работать в опубликованной статье.</span><span class="sxs-lookup"><span data-stu-id="580d7-152">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="580d7-153">Ссылки на страницы, не являющиеся частью технической документации</span><span class="sxs-lookup"><span data-stu-id="580d7-153">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="580d7-154">Чтобы добавить ссылку на страницу корпорации Майкрософт другого характера (например, на страницу с ценами, страницу соглашения об уровне обслуживания или любую другую страницу, не являющуюся статьей документации), используйте абсолютный URL-адрес без указания языка.</span><span class="sxs-lookup"><span data-stu-id="580d7-154">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="580d7-155">Такие ссылки работают на сайте GitHub и на отображаемом сайте:</span><span class="sxs-lookup"><span data-stu-id="580d7-155">The goal here is that links work in GitHub and on the rendered site:</span></span>

    [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)

## <a name="links-to-third-party-sites"></a><span data-ttu-id="580d7-156">Ссылки на сторонние сайты</span><span class="sxs-lookup"><span data-stu-id="580d7-156">Links to third-party sites</span></span>

<span data-ttu-id="580d7-157">Лучше избегать перенаправления пользователей на другие сайты.</span><span class="sxs-lookup"><span data-stu-id="580d7-157">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="580d7-158">Но иногда это необходимо. При размещении ссылок на сторонние сайты руководствуйтесь следующей информацией:</span><span class="sxs-lookup"><span data-stu-id="580d7-158">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="580d7-159">**Отслеживаемость**. Добавляйте ссылки на содержимое сторонних поставщиков, если именно к нему требуется предоставить общий доступ.</span><span class="sxs-lookup"><span data-stu-id="580d7-159">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="580d7-160">Например, предоставлять описание того, как использовать средства разработчика Android, не входит в обязанности корпорации Майкрософт. Это задача Google.</span><span class="sxs-lookup"><span data-stu-id="580d7-160">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="580d7-161">При необходимости мы можем объяснить, как использовать средства разработчика Android *с* Azure, но руководство по применению этих средств должна предоставить корпорация Google.</span><span class="sxs-lookup"><span data-stu-id="580d7-161">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="580d7-162">**Утверждение руководителем проектов**. Запрашивайте в корпорации Майкрософт утверждение ссылок на содержимое сторонних поставщиков.</span><span class="sxs-lookup"><span data-stu-id="580d7-162">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="580d7-163">Такие ссылки предполагают определенный уровень ответственности за надежность информации и выполнение инструкций пользователем.</span><span class="sxs-lookup"><span data-stu-id="580d7-163">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="580d7-164">**Проверки актуальности**. Следите за актуальностью, правильностью и релевантностью информации. Регулярно проверяйте, не изменилась ли ссылка.</span><span class="sxs-lookup"><span data-stu-id="580d7-164">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn’t changed.</span></span>
- <span data-ttu-id="580d7-165">**Информация о переходе на сайт стороннего поставщика**. Обязательно уведомляйте пользователей о том, что они переходят на другой сайт.</span><span class="sxs-lookup"><span data-stu-id="580d7-165">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="580d7-166">Если это не следует из контекста, добавьте соответствующую фразу.</span><span class="sxs-lookup"><span data-stu-id="580d7-166">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="580d7-167">Например, "Предварительные требования включают установку средств разработчика Android, которые вы можете скачать на сайте Android Studio".</span><span class="sxs-lookup"><span data-stu-id="580d7-167">For example: “Prerequisites include the Android Developer Tools, which you can download on the Android Studio site.”</span></span>
- <span data-ttu-id="580d7-168">**Дальнейшие действия**. Неплохим решением будет добавить ссылку, скажем, на блог MVP, в разделе "Дальнейшие действия".</span><span class="sxs-lookup"><span data-stu-id="580d7-168">**Next steps**: It’s fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="580d7-169">Опять же, при этом пользователь должен понимать, что он покидает текущий сайт.</span><span class="sxs-lookup"><span data-stu-id="580d7-169">Again, just make sure that users understand they’ll be leaving the site.</span></span>
- <span data-ttu-id="580d7-170">**Юридическая информация**. Юридическая информация предоставляется в разделе **Ссылки на веб-сайты третьих лиц** на странице **условий использования**. Ссылка на нее размещена в нижнем колонтитуле каждой страницы ms.com.</span><span class="sxs-lookup"><span data-stu-id="580d7-170">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every ms.com page.</span></span>

## <a name="links-to-msdn-or-technet"></a><span data-ttu-id="580d7-171">Ссылки на MSDN или TechNet</span><span class="sxs-lookup"><span data-stu-id="580d7-171">Links to MSDN or TechNet</span></span>

<span data-ttu-id="580d7-172">Если нужно добавить ссылку на MSDN или TechNet, используйте полную ссылку на статью, удалив указатель языка "en-us".</span><span class="sxs-lookup"><span data-stu-id="580d7-172">When you need to link to MSDN or TechNet, use the full link to the topic, and remove the "en-us" language locale from the link.</span></span>

## <a name="links-to-azure-powershell-reference-content"></a><span data-ttu-id="580d7-173">Ссылки на справочные материалы по Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="580d7-173">Links to Azure PowerShell reference content</span></span>

<span data-ttu-id="580d7-174">Справочные материалы по Azure PowerShell с ноября 2016 г. претерпели некоторые изменения.</span><span class="sxs-lookup"><span data-stu-id="580d7-174">The Azure PowerShell reference content has been through several changes since November 2016.</span></span> <span data-ttu-id="580d7-175">Выполните приведенные ниже инструкции, чтобы добавить ссылку на эти материалы в другие статьи на сайте docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="580d7-175">Use the following guidelines for linking to this content from other articles on docs.microsoft.com.</span></span>

<span data-ttu-id="580d7-176">Структура URL-адреса:</span><span class="sxs-lookup"><span data-stu-id="580d7-176">Structure of the URL:</span></span>

* <span data-ttu-id="580d7-177">Для командлетов:</span><span class="sxs-lookup"><span data-stu-id="580d7-177">For cmdlets:</span></span>
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* <span data-ttu-id="580d7-178">Для тематических статей:</span><span class="sxs-lookup"><span data-stu-id="580d7-178">For conceptual topics:</span></span>
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

<span data-ttu-id="580d7-179">Часть &lt;moniker-name&gt; является необязательной.</span><span class="sxs-lookup"><span data-stu-id="580d7-179">The &lt;moniker-name&gt; portion is optional.</span></span> <span data-ttu-id="580d7-180">Если ее исключить, пользователь будет направлен к последней версии содержимого.</span><span class="sxs-lookup"><span data-stu-id="580d7-180">If it's omitted, you will be directed to the latest version of the content.</span></span> <span data-ttu-id="580d7-181">Для части &lt;service-name&gt; можно задать одно из значений в примерах базовых URL-адресов ниже:</span><span class="sxs-lookup"><span data-stu-id="580d7-181">The &lt;service-name&gt; portion is one of the examples shown in the following base URLs:</span></span>

- <span data-ttu-id="580d7-182">Содержимое Azure PowerShell (AzureRM): https://docs.microsoft.com/powershell/azure/</span><span class="sxs-lookup"><span data-stu-id="580d7-182">Azure PowerShell (AzureRM) content: https://docs.microsoft.com/powershell/azure/</span></span>
- <span data-ttu-id="580d7-183">Содержимое Azure PowerShell (ASM) : https://docs.microsoft.com/powershell/azure/_servicemanagement_</span><span class="sxs-lookup"><span data-stu-id="580d7-183">Azure PowerShell (ASM) content: https://docs.microsoft.com/powershell/azure/_servicemanagement_</span></span>
- <span data-ttu-id="580d7-184">Содержимое Azure PowerShell для Active Directory (AzureAD): https://docs.microsoft.com/powershell/azure/_active-directory_</span><span class="sxs-lookup"><span data-stu-id="580d7-184">Azure Active Directory (AzureAD) PowerShell content: https://docs.microsoft.com/powershell/azure/_active-directory_</span></span>
- <span data-ttu-id="580d7-185">PowerShell для Azure Service Fabric https://docs.microsoft.com/powershell/azure/_service-fabric_</span><span class="sxs-lookup"><span data-stu-id="580d7-185">Azure Service Fabric PowerShell: https://docs.microsoft.com/powershell/azure/_service-fabric_</span></span>
- <span data-ttu-id="580d7-186">PowerShell для Azure Information Protection: https://docs.microsoft.com/powershell/azure/_aip_</span><span class="sxs-lookup"><span data-stu-id="580d7-186">Azure Information Protection PowerShell: https://docs.microsoft.com/powershell/azure/_aip_</span></span>
- <span data-ttu-id="580d7-187">PowerShell для заданий эластичной базы данных заданий Azure: https://docs.microsoft.com/powershell/azure/_elasticdbjobs_</span><span class="sxs-lookup"><span data-stu-id="580d7-187">Azure Elastic DB Jobs PowerShell: https://docs.microsoft.com/powershell/azure/_elasticdbjobs_</span></span>

<span data-ttu-id="580d7-188">Если включить эти URL-адреса, пользователь будет перенаправлен к последней версии содержимого.</span><span class="sxs-lookup"><span data-stu-id="580d7-188">When you use these URLs, you will be redirected to the latest version of the content.</span></span> <span data-ttu-id="580d7-189">В таком случае указывать моникер версии не требуется.</span><span class="sxs-lookup"><span data-stu-id="580d7-189">This way, you don't have to specify a version moniker.</span></span> <span data-ttu-id="580d7-190">Кроме того, вам не придется обновлять ссылки на тематические материалы при изменении версии.</span><span class="sxs-lookup"><span data-stu-id="580d7-190">And you won't have links to conceptual content that must be updated when the version changes.</span></span>

<span data-ttu-id="580d7-191">Чтобы создать правильную ссылку на страницу, откройте ее в браузере и скопируйте URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="580d7-191">To create the correct link, find the page that you want to link to in your browser, and copy the URL.</span></span>
<span data-ttu-id="580d7-192">Удалите https://docs.microsoft.com и сведения о языковом стандарте.</span><span class="sxs-lookup"><span data-stu-id="580d7-192">Then, remove "https://docs.microsoft.com" and the locale info.</span></span>

<span data-ttu-id="580d7-193">Если ссылка размещена в оглавлении, используйте полный URL-адрес без указателя языка.</span><span class="sxs-lookup"><span data-stu-id="580d7-193">When you're linking from a TOC, you must use the full URL without the locale information.</span></span>

<span data-ttu-id="580d7-194">Пример разметки Markdown:</span><span class="sxs-lookup"><span data-stu-id="580d7-194">Example markdown:</span></span>

```markdown
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](/powershell/azure/install-azurerm-ps)
```
