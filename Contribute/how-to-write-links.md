---
title: Использование ссылок в документации
description: В этой статье содержатся инструкции по созданию ссылок на содержимое на сайте docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: gewarren
ms.author: gewarren
ms.date: 03/31/2020
ms.openlocfilehash: ca29d4b9e81f8af3b680367b210bd1734860687d
ms.sourcegitcommit: 5ef2dc72e2ff8bddf873415a3f4b816eb16029dd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/03/2020
ms.locfileid: "80624743"
---
# <a name="use-links-in-documentation"></a><span data-ttu-id="19737-103">Использование ссылок в документации</span><span class="sxs-lookup"><span data-stu-id="19737-103">Use links in documentation</span></span>

<span data-ttu-id="19737-104">В этой статье описывается использование гиперссылок со страниц, размещенных на сайте docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="19737-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com.</span></span> <span data-ttu-id="19737-105">Добавление ссылок в Markdown не представляет труда, но следует придерживаться ряда определенных правил.</span><span class="sxs-lookup"><span data-stu-id="19737-105">Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="19737-106">Ссылки могут указывать на содержимое на той же странице, на соседних страницах или на внешних сайтах и URL-адресах.</span><span class="sxs-lookup"><span data-stu-id="19737-106">Links point users to content in the same page, in other neighboring pages, or on external sites and URLs.</span></span>

<span data-ttu-id="19737-107">Серверная часть сайта docs.microsoft.com использует службы Open Publishing Services (OPS), поддерживающие разметку, совместимую с [CommonMark][], проанализированную через подсистему синтаксического анализа [Markdig][].</span><span class="sxs-lookup"><span data-stu-id="19737-107">The docs.microsoft.com site backend uses Open Publishing Services (OPS), which supports [CommonMark][]-compliant markdown parsed through the [Markdig][] parsing engine.</span></span> <span data-ttu-id="19737-108">Такой тип разметки совместим с [GitHub Flavored Markdown (GFM)][GFM], так как большинство документов хранятся на GitHub, где их можно править.</span><span class="sxs-lookup"><span data-stu-id="19737-108">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)][GFM], as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="19737-109">Дополнительные функции добавляются с помощью расширений Markdown.</span><span class="sxs-lookup"><span data-stu-id="19737-109">Additional functionality is added through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="19737-110">Все ссылки должны быть безопасными (с протоколом `https` вместо `http`), если целевой объект поддерживает такой протокол (большинство целевых объектов поддерживают).</span><span class="sxs-lookup"><span data-stu-id="19737-110">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="19737-111">Текст ссылки</span><span class="sxs-lookup"><span data-stu-id="19737-111">Link text</span></span>

<span data-ttu-id="19737-112">Фраза для ссылки должна быть понятной.</span><span class="sxs-lookup"><span data-stu-id="19737-112">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="19737-113">Иными словами, это должен быть полноценный текст или название страницы, на которую указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="19737-113">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="19737-114">Не используйте конструкцию "щелкните здесь".</span><span class="sxs-lookup"><span data-stu-id="19737-114">Do not use "click here."</span></span> <span data-ttu-id="19737-115">Она плохо сказывается на оптимизации для поисковых систем и не дает адекватного представления о целевой странице.</span><span class="sxs-lookup"><span data-stu-id="19737-115">It's bad for search engine optimization and doesn't adequately describe the target.</span></span>

<span data-ttu-id="19737-116">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="19737-116">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://docs.microsoft.com/sql/t-sql/statements/set-transaction-isolation-level-transact-sql) reference.`

<span data-ttu-id="19737-117">**Неправильно:**</span><span class="sxs-lookup"><span data-stu-id="19737-117">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="19737-118">Ссылки для перехода от одной статьи к другой</span><span class="sxs-lookup"><span data-stu-id="19737-118">Links from one article to another</span></span>

<span data-ttu-id="19737-119">Система публикации поддерживает два типа гиперссылок: **URL-адреса** и **ссылки на файлы**.</span><span class="sxs-lookup"><span data-stu-id="19737-119">There are two types of hyperlinks supported by the publishing system: **URLs** and **file links**.</span></span>

<span data-ttu-id="19737-120">URL-ссылкой может быть URL-путь относительно корня сайта docs.microsoft.com или абсолютный URL-адрес, имеющий синтаксис полного URL-адреса (например, `https://github.com/MicrosoftDocs/PowerShell-Docs`).</span><span class="sxs-lookup"><span data-stu-id="19737-120">A URL link can be a URL path that is relative to the root of docs.microsoft.com, or an absolute URL that includes the full URL syntax (for example, `https://github.com/MicrosoftDocs/PowerShell-Docs`).</span></span>

- <span data-ttu-id="19737-121">Используйте URL-адреса для ссылки на содержимое за пределами текущего _набора документации_ или для ссылок между автоматически создаваемой справкой и концептуальными статьями в наборе документации.</span><span class="sxs-lookup"><span data-stu-id="19737-121">Use URL links when linking to content outside of the current _docset_ or between autogenerated reference and conceptual articles within the docset.</span></span>
- <span data-ttu-id="19737-122">Самый простой способ создать относительную ссылку — скопировать URL-адрес в браузере, а затем удалить часть `https://docs.microsoft.com/en-us` из значения, вставленного в разметку Markdown.</span><span class="sxs-lookup"><span data-stu-id="19737-122">The simplest way to create a relative link is to copy the URL from your browser, then remove `https://docs.microsoft.com/en-us` from the value you paste into markdown.</span></span>
   - <span data-ttu-id="19737-123">Не включайте языковой стандарт (например, "/ru-ru") в URL-адреса ресурсов Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="19737-123">Do not include locales in URLs for Microsoft properties (for example, remove "/en-us" from the URL).</span></span>

<span data-ttu-id="19737-124">Ссылка на файл служит для перехода от одной статьи к другой в наборе документации.</span><span class="sxs-lookup"><span data-stu-id="19737-124">A file link is used to link from one article to another within the docset.</span></span>

- <span data-ttu-id="19737-125">В путях к файлам используются прямые (`/`), а не обратные косые черты.</span><span class="sxs-lookup"><span data-stu-id="19737-125">All file paths use forward-slash (`/`) characters instead of back-slash characters.</span></span>
- <span data-ttu-id="19737-126">Для статьи, в которую добавляется ссылка на другую статью в том же каталоге:</span><span class="sxs-lookup"><span data-stu-id="19737-126">An article links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="19737-127">Для статьи, в которую добавляется ссылка на статью в родительском каталоге текущего каталога:</span><span class="sxs-lookup"><span data-stu-id="19737-127">An article links to an article in the parent directory of the current directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="19737-128">Для статьи, в которую добавляется ссылка на статью в подкаталоге текущего каталога:</span><span class="sxs-lookup"><span data-stu-id="19737-128">An article links to an article in a subdirectory of the current directory:</span></span>

  `[link text](directory/article-name.md)`

- <span data-ttu-id="19737-129">Для статьи, в которую добавляется ссылка на статью в подкаталоге родительского каталога текущего каталога:</span><span class="sxs-lookup"><span data-stu-id="19737-129">An article links to an article in a subdirectory of the parent directory of the current directory:</span></span>

  `[link text](../directory/article-name.md)`

> [!NOTE]
> <span data-ttu-id="19737-130">Ни в одном из предыдущих примеров `~/` не используется в качестве части ссылки.</span><span class="sxs-lookup"><span data-stu-id="19737-130">None of the previous examples use the `~/` as part of the link.</span></span> <span data-ttu-id="19737-131">Если вы ссылаетесь на абсолютный путь в корне репозитория, начните с `/`.</span><span class="sxs-lookup"><span data-stu-id="19737-131">To link to an absolute path that begins at the root of the repository, start the link with `/`.</span></span> <span data-ttu-id="19737-132">Добавление `~/` приведет к формированию недопустимых ссылок при навигации по репозиториям исходного кода на GitHub.</span><span class="sxs-lookup"><span data-stu-id="19737-132">Including the `~/` produces invalid links when navigating the source repositories on GitHub.</span></span> <span data-ttu-id="19737-133">Если начать путь с `/`, разрешение происходит успешно.</span><span class="sxs-lookup"><span data-stu-id="19737-133">Starting the path with `/` resolves correctly.</span></span>

### <a name="structure-of-links-on-docsmicrosoftcom"></a><span data-ttu-id="19737-134">Структура ссылок на docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="19737-134">Structure of links on docs.microsoft.com</span></span>

<span data-ttu-id="19737-135">Содержимое, публикуемое на сайте docs.microsoft.com, имеет следующую структуру URL-адресов:</span><span class="sxs-lookup"><span data-stu-id="19737-135">Content published on docs.microsoft.com has the following URL structure:</span></span>

```
https://docs.microsoft.com/<locale>/<product-service>/[<feature-service>]/[<subfolder>]/<topic>[?view=<view-name>]
```

<span data-ttu-id="19737-136">Примеры:</span><span class="sxs-lookup"><span data-stu-id="19737-136">Examples:</span></span>

```
https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview
https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-5.1.1
```

- <span data-ttu-id="19737-137">`<locale>` — определяет язык статьи (например, en-us или ru-ru).</span><span class="sxs-lookup"><span data-stu-id="19737-137">`<locale>` - identifies the language of the article (example: en-us or de-de)</span></span>
- <span data-ttu-id="19737-138">`<product-service>` — название продукта или службы (например, powershell, dotnet или azure).</span><span class="sxs-lookup"><span data-stu-id="19737-138">`<product-service>` - the name of the product or service (example: powershell, dotnet, or azure)</span></span>
- <span data-ttu-id="19737-139">`[<feature-service>]` — (необязательно) имя компонента или подслужбы продукта (например, csharp или load-balancer).</span><span class="sxs-lookup"><span data-stu-id="19737-139">`[<feature-service>]` - (optional) the name of the product's feature or subservice (example: csharp or load-balancer)</span></span>
- <span data-ttu-id="19737-140">`[<subfolder>]` — (необязательно) имя подпапки компонента.</span><span class="sxs-lookup"><span data-stu-id="19737-140">`[<subfolder>]` - (optional) the name of a subfolder within a feature</span></span>
- <span data-ttu-id="19737-141">`<topic>` — имя файла статьи (например, load-balancer-overview или overview).</span><span class="sxs-lookup"><span data-stu-id="19737-141">`<topic>` - the name of the article file for the topic (example: load-balancer-overview or overview)</span></span>
- <span data-ttu-id="19737-142">`[?view=\<view-name>]` — (необязательно) имя представления, используемое средством выбора версии для содержимого, имеющего несколько версий (например, azps-3.5.0).</span><span class="sxs-lookup"><span data-stu-id="19737-142">`[?view=\<view-name>]` - (optional) the view name used by the version selector for content that has multiple versions available (example: azps-3.5.0)</span></span>

> [!TIP]
> <span data-ttu-id="19737-143">В большинстве случаев для статей в одном _наборе документации_ указывается один и тот же фрагмент URL-адреса `<product-service>`.</span><span class="sxs-lookup"><span data-stu-id="19737-143">In most cases, articles in the same _docset_ have the same `<product-service>` URL fragment.</span></span> <span data-ttu-id="19737-144">Например:</span><span class="sxs-lookup"><span data-stu-id="19737-144">For example:</span></span>
> - <span data-ttu-id="19737-145">Один набор документации</span><span class="sxs-lookup"><span data-stu-id="19737-145">Same docset</span></span>
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/dotnet/framework/install`
> - <span data-ttu-id="19737-146">Разные наборы документации</span><span class="sxs-lookup"><span data-stu-id="19737-146">Different docset</span></span>
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/visualstudio/whats-new`

## <a name="bookmark-links"></a><span data-ttu-id="19737-147">Ссылки закладок</span><span class="sxs-lookup"><span data-stu-id="19737-147">Bookmark links</span></span>

<span data-ttu-id="19737-148">Чтобы добавить ссылку закладки на заголовок в *текущем* файле, используйте символ решетки, за которым следует текст заголовка в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="19737-148">For a bookmark link to a heading in the *current* file, use a hash symbol followed by the lowercase words of the heading.</span></span> <span data-ttu-id="19737-149">Удалите знаки препинания из заголовка и замените пробелы дефисами.</span><span class="sxs-lookup"><span data-stu-id="19737-149">Remove punctuation from the heading and replace spaces with dashes:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="19737-150">Чтобы добавить ссылку закладки на заголовок в другой статье, используйте относительную ссылку на файл или сайт, после которой укажите символ решетки и текст заголовка.</span><span class="sxs-lookup"><span data-stu-id="19737-150">To link to a bookmark heading in another article, use the file-relative or site-relative link plus a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="19737-151">Удалите знаки препинания из заголовка и замените пробелы дефисами.</span><span class="sxs-lookup"><span data-stu-id="19737-151">Remove punctuation from the heading and replace spaces with dashes:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="19737-152">Можно также скопировать ссылку закладки из URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="19737-152">You can also copy the bookmark link from the URL.</span></span> <span data-ttu-id="19737-153">Чтобы увидеть URL-адрес, наведите указатель мыши на строку заголовка на сайте docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="19737-153">To find the URL, hover your mouse over the heading line on docs.microsoft.com.</span></span> <span data-ttu-id="19737-154">Должен появиться значок ссылки:</span><span class="sxs-lookup"><span data-stu-id="19737-154">You should see a link icon appear:</span></span>

![Значок ссылки в заголовке статьи](media/how-to-write-links/bookmark-link.png)

<span data-ttu-id="19737-156">Щелкните значок ссылки, а затем скопируйте текст закладки из URL-адреса (то есть часть после символа решетки).</span><span class="sxs-lookup"><span data-stu-id="19737-156">Click the link icon and then copy the bookmark anchor text from the URL (that is, the part after the hash).</span></span>

> [!NOTE]
> <span data-ttu-id="19737-157">В расширении для работы с документацией также есть инструменты, помогающие создавать ссылки.</span><span class="sxs-lookup"><span data-stu-id="19737-157">The Docs Extension also has tools to help create links.</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="19737-158">Явные ссылки привязки</span><span class="sxs-lookup"><span data-stu-id="19737-158">Explicit anchor links</span></span>

<span data-ttu-id="19737-159">Добавлять явные ссылки привязки, использующие HTML-тег `<a>`, не требуется и не рекомендуется, за исключением страниц-концентраторов и целевых страниц.</span><span class="sxs-lookup"><span data-stu-id="19737-159">Adding explicit anchor links using the `<a>` HTML tag isn't required or recommended, except in hub and landing pages.</span></span> <span data-ttu-id="19737-160">Вместо них используйте автоматически созданные закладки, как описано в [этом разделе](#bookmark-links).</span><span class="sxs-lookup"><span data-stu-id="19737-160">Instead, use the auto-generated bookmarks as described in [bookmark links](#bookmark-links).</span></span> <span data-ttu-id="19737-161">Для страниц-концентраторов и целевых страниц привязки объявляются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="19737-161">For hub and landing pages, declare anchors as follows:</span></span>

```markdown
## <a id="anchortext" />Header text
```

<span data-ttu-id="19737-162">или</span><span class="sxs-lookup"><span data-stu-id="19737-162">or</span></span>

```markdown
## <a name="anchortext" />Header text
```

<span data-ttu-id="19737-163">Ссылка на привязку добавляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="19737-163">And the following to link to the anchor:</span></span>

```markdown
To go to a section on the same page:
[text](#anchortext)

To go to a section on another page.
[text](filename.md#anchortext)
```

> [!NOTE]
> <span data-ttu-id="19737-164">Текст привязки должен всегда быть в нижнем регистре и не содержать пробелов.</span><span class="sxs-lookup"><span data-stu-id="19737-164">Anchor text must always be lowercase and not contain spaces.</span></span>

## <a name="xref-cross-reference-links"></a><span data-ttu-id="19737-165">Ссылки XRef (перекрестные ссылки)</span><span class="sxs-lookup"><span data-stu-id="19737-165">XRef (cross reference) links</span></span>

<span data-ttu-id="19737-166">Ссылки XRef — это рекомендуемый способ ссылки на интерфейсы API, так как они проверяются во время сборки.</span><span class="sxs-lookup"><span data-stu-id="19737-166">XRef links are the recommended way to link to APIs, because they're validated at build time.</span></span> <span data-ttu-id="19737-167">Для ссылки на автоматически создаваемые страницы справочных материалов по API в текущем или другом наборе документации используйте ссылки XRef с уникальным идентификатором ([UID](#determine-the-uid)) типа или члена.</span><span class="sxs-lookup"><span data-stu-id="19737-167">To link to auto-generated API reference pages in the current docset or other docsets, use XRef links with the unique ID ([UID](#determine-the-uid)) of the type or member.</span></span>

> [!TIP]
> <span data-ttu-id="19737-168">Для вставки ссылок XRref .NET, доступных в [Обозреватель API .NET][], можно использовать [расширение Docs Markdown для VS Code][docsextension] (является частью Docs Authoring Pack).</span><span class="sxs-lookup"><span data-stu-id="19737-168">You can use the [Docs Markdown extension for VS Code][docsextension] (part of the Docs Authoring Pack) to insert .NET XRref links that are surfaced in the [.NET API Browser][].</span></span>

<span data-ttu-id="19737-169">Проверьте, имеется ли интерфейс API, на который нужно добавить ссылку, на сайте [docs.microsoft.com][docs], введя его полное имя или его часть в поле поиска в [Обозреватель API .NET][] или [Windows UWP][].</span><span class="sxs-lookup"><span data-stu-id="19737-169">Check if the API you want to link to is on [docs.microsoft.com][docs] by typing all or some of its full name in the [.NET API browser][] or [Windows UWP][] search box.</span></span> <span data-ttu-id="19737-170">Если результаты не отображаются, данный тип пока отсутствует на сайте docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="19737-170">If you don't see any results displayed, the type isn't yet on docs.microsoft.com.</span></span>

<span data-ttu-id="19737-171">Можно выбрать один из следующих вариантов синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="19737-171">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="19737-172">Автоматические ссылки:</span><span class="sxs-lookup"><span data-stu-id="19737-172">Auto-links:</span></span>

   ```markdown
   <xref:UID>
   <xref:UID?displayProperty=nameWithType>
   ```

   <span data-ttu-id="19737-173">По умолчанию в тексте ссылки отображается только имя члена или типа.</span><span class="sxs-lookup"><span data-stu-id="19737-173">By default, link text shows only the member or type name.</span></span> <span data-ttu-id="19737-174">Необязательный параметр запроса `displayProperty=nameWithType` создает полный текст ссылки, то есть **namespace.type** для типов и **type.member** для членов типов, включая перечисления.</span><span class="sxs-lookup"><span data-stu-id="19737-174">The optional `displayProperty=nameWithType` query parameter produces fully qualified link text, that is, **namespace.type** for types, and **type.member** for type members, including enumeration type members.</span></span>

- <span data-ttu-id="19737-175">Ссылки в стиле Markdown:</span><span class="sxs-lookup"><span data-stu-id="19737-175">Markdown-style links:</span></span>

   ```markdown
   [link text](xref:UID)
   ```

   <span data-ttu-id="19737-176">Ссылки в стиле Markdown используются, когда требуется настроить отображаемый текст ссылки.</span><span class="sxs-lookup"><span data-stu-id="19737-176">Use Markdown-style links for XRef when you want to customize the link text that's displayed.</span></span>

<span data-ttu-id="19737-177">Примеры:</span><span class="sxs-lookup"><span data-stu-id="19737-177">Examples:</span></span>

- <span data-ttu-id="19737-178">**\<xref:System.String>** отображается как <xref:System.String>.</span><span class="sxs-lookup"><span data-stu-id="19737-178">**\<xref:System.String>** displays as <xref:System.String></span></span>

- <span data-ttu-id="19737-179">**\<xref:System.String?displayProperty=nameWithType>** отображается как <xref:System.String?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="19737-179">**\<xref:System.String?displayProperty=nameWithType>** displays as <xref:System.String?displayProperty=nameWithType></span></span>

- <span data-ttu-id="19737-180">**\[Класс String](xref:System.String)** отображается как [Класс String](xref:System.String).</span><span class="sxs-lookup"><span data-stu-id="19737-180">**\[String class](xref:System.String)** displays as [String class](xref:System.String).</span></span>

<span data-ttu-id="19737-181">Параметр запроса `displayProperty=fullName` работает так же, как `displayProperty=nameWithType` для классов.</span><span class="sxs-lookup"><span data-stu-id="19737-181">The `displayProperty=fullName` query parameter works the same way as `displayProperty=nameWithType` for classes.</span></span> <span data-ttu-id="19737-182">То есть текст ссылки принимает вид **пространство_имен.имя_класса**.</span><span class="sxs-lookup"><span data-stu-id="19737-182">That is, the link text becomes **namespace.classname**.</span></span> <span data-ttu-id="19737-183">Однако для членов текст ссылки отображается в виде **пространство_имен.имя_класса.имя_члена**, что может быть нежелательным.</span><span class="sxs-lookup"><span data-stu-id="19737-183">However, for members, the link text displays as **namespace.classname.membername**, which may be undesirable.</span></span>

> [!NOTE]
> <span data-ttu-id="19737-184">Регистр в уникальных идентификаторах учитывается.</span><span class="sxs-lookup"><span data-stu-id="19737-184">UIDs are case sensitive.</span></span> <span data-ttu-id="19737-185">Например, `<xref:System.Object>` разрешается успешно, а `<xref:system.object>` нет.</span><span class="sxs-lookup"><span data-stu-id="19737-185">For example, `<xref:System.Object>` resolves correctly but `<xref:system.object>` does not.</span></span>

### <a name="xref-build-warnings-and-incremental-builds"></a><span data-ttu-id="19737-186">Предупреждения сборки XRef и добавочные сборки</span><span class="sxs-lookup"><span data-stu-id="19737-186">XRef build warnings and incremental builds</span></span>

<span data-ttu-id="19737-187">При добавочной сборке выполняется сборка только тех файлов, которые были изменены или затронуты изменением.</span><span class="sxs-lookup"><span data-stu-id="19737-187">An incremental build only builds files that have changed or been affected by a change.</span></span> <span data-ttu-id="19737-188">Если выводится предупреждение о недействительной ссылке XRef, которая на самом деле действительна, это может быть вызвано тем, что сборка была добавочной.</span><span class="sxs-lookup"><span data-stu-id="19737-188">If you see a build warning about an invalid XREF link, but the link is actually valid, this could be because the build was incremental.</span></span> <span data-ttu-id="19737-189">Файл, вызвавший предупреждение, не изменялся, поэтому его сборка не выполнялась и были повторно выданы прошлые предупреждения.</span><span class="sxs-lookup"><span data-stu-id="19737-189">The file causing the warning didn't change, so it wasn't built and past warnings were replayed.</span></span> <span data-ttu-id="19737-190">Предупреждение исчезнет после изменения файла или запуска полной сборки (запустить ее можно на сайте ops.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="19737-190">The warning will disappear when the file changes or if you trigger a full build (you can start a full build on ops.microsoft.com).</span></span> <span data-ttu-id="19737-191">Это недостаток добавочных сборок, так как DocFX не может обнаружить изменение данных в службе XREF.</span><span class="sxs-lookup"><span data-stu-id="19737-191">This is a drawback to incremental builds, because DocFX can't detect a data update inside the XREF service.</span></span>

### <a name="determine-the-uid"></a><span data-ttu-id="19737-192">Определение уникального идентификатора</span><span class="sxs-lookup"><span data-stu-id="19737-192">Determine the UID</span></span>

<span data-ttu-id="19737-193">Уникальный идентификатор обычно совпадает с полным именем класса или члена.</span><span class="sxs-lookup"><span data-stu-id="19737-193">The UID is usually the fully qualified class or member name.</span></span> <span data-ttu-id="19737-194">Определить уникальный идентификатор можно по крайней мере двумя способами.</span><span class="sxs-lookup"><span data-stu-id="19737-194">There are at least two ways to determine the UID:</span></span>

- <span data-ttu-id="19737-195">Щелкните правой кнопкой мыши страницу [документации][docs] по типу или члену, выберите пункт **Просмотреть исходный код**, а затем скопируйте значение **content** для **ms.assetid**:</span><span class="sxs-lookup"><span data-stu-id="19737-195">Right-click on the [Docs][docs] page for a type or member, select **View source**, and then copy the **content** value for **ms.assetid**:</span></span>

  ![ms.assetid в исходном коде веб-страницы](media/how-to-write-links/ms-assetid.png)

- <span data-ttu-id="19737-197">Используйте [сайт автозаполнения][], добавив к URL-адресу имя типа или его часть.</span><span class="sxs-lookup"><span data-stu-id="19737-197">Use the [autocomplete site][] by appending some or all of the name of the type to the URL.</span></span> <span data-ttu-id="19737-198">Например, если ввести `https://xref.docs.microsoft.com/autocomplete?text=Writeline` в адресной строке браузера, будут выведены все типы и методы, в именах которых есть строка **Writeline**, а также их уникальные идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="19737-198">For example, entering `https://xref.docs.microsoft.com/autocomplete?text=Writeline` in the address bar of your browser displays all the types and methods that contain **Writeline** in their name, along with their UID.</span></span>

#### <a name="verify-the-uid"></a><span data-ttu-id="19737-199">Проверка уникального идентификатора</span><span class="sxs-lookup"><span data-stu-id="19737-199">Verify the UID</span></span>

<span data-ttu-id="19737-200">Чтобы проверить правильность уникального идентификатора, замените строку **System.String** в следующем URL-адресе на свой уникальный идентификатор, а затем вставьте получившийся адрес в адресной строке браузера:</span><span class="sxs-lookup"><span data-stu-id="19737-200">To test if you have the correct UID, replace **System.String** in the following URL with your UID, and then paste it into the address bar of a browser:</span></span>

`https://xref.docs.microsoft.com/query?uid=System.String`

> [!TIP]
> <span data-ttu-id="19737-201">Регистр в уникальном идентификаторе в URL-адресе учитывается. Если вы проверяете уникальный идентификатор перегрузки метода, не включайте пробелы между типами параметров.</span><span class="sxs-lookup"><span data-stu-id="19737-201">The UID in the URL is case-sensitive, and if you're checking a method overload UID, don't include spaces between the parameter types.</span></span>

<span data-ttu-id="19737-202">Если результат будет следующим, значит уникальный идентификатор правилен:</span><span class="sxs-lookup"><span data-stu-id="19737-202">If you see something like the following, you have the correct UID:</span></span>

```text
[{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,...xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"},{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,netframework-4.6,netframework-4.6.1,...,xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"}]
```

<span data-ttu-id="19737-203">Если на странице отображается просто `[]`, значит уникальный идентификатор неправилен.</span><span class="sxs-lookup"><span data-stu-id="19737-203">If you just see `[]` displayed on the page, you have the wrong UID.</span></span>

### <a name="percent-encoding-of-urls"></a><span data-ttu-id="19737-204">Кодирование URL-адресов с помощью символа процента</span><span class="sxs-lookup"><span data-stu-id="19737-204">Percent-encoding of URLs</span></span>

<span data-ttu-id="19737-205">Специальные символы в уникальном идентификаторе должны быть закодированы в формате HTML следующим образом:</span><span class="sxs-lookup"><span data-stu-id="19737-205">Special characters in the UID need to be HTML encoded as follows:</span></span>

| <span data-ttu-id="19737-206">Символ</span><span class="sxs-lookup"><span data-stu-id="19737-206">Character</span></span> | <span data-ttu-id="19737-207">Кодирование HTML</span><span class="sxs-lookup"><span data-stu-id="19737-207">HTML encoding</span></span> |
| --------- | ------------- |
| `` ` ``   | <span data-ttu-id="19737-208">%60</span><span class="sxs-lookup"><span data-stu-id="19737-208">%60</span></span>           |
| `#`       | <span data-ttu-id="19737-209">%23</span><span class="sxs-lookup"><span data-stu-id="19737-209">%23</span></span>           |
| `*`       | <span data-ttu-id="19737-210">%2A</span><span class="sxs-lookup"><span data-stu-id="19737-210">%2A</span></span>           |

<span data-ttu-id="19737-211">См. полный список [кодов с символом процента](https://en.wikipedia.org/wiki/Percent-encoding).</span><span class="sxs-lookup"><span data-stu-id="19737-211">See a full list of [percent-codes](https://en.wikipedia.org/wiki/Percent-encoding).</span></span>

<span data-ttu-id="19737-212">Примеры кодирования:</span><span class="sxs-lookup"><span data-stu-id="19737-212">Encoding examples:</span></span>

- <span data-ttu-id="19737-213">`System.Threading.Tasks.Task``1` кодируется как `System.Threading.Tasks.Task%601` (см. [раздел об универсальных типах](#generic-types)).</span><span class="sxs-lookup"><span data-stu-id="19737-213">`System.Threading.Tasks.Task``1` encodes as `System.Threading.Tasks.Task%601` (see the [section on generic types](#generic-types))</span></span>

- <span data-ttu-id="19737-214">`System.Exception.#ctor` кодируется как `System.Exception.%23ctor`.</span><span class="sxs-lookup"><span data-stu-id="19737-214">`System.Exception.#ctor` encodes as `System.Exception.%23ctor`</span></span>

- <span data-ttu-id="19737-215">`System.Object.Equals*` кодируется как `System.Object.Equals%2A`.</span><span class="sxs-lookup"><span data-stu-id="19737-215">`System.Object.Equals*` encodes as `System.Object.Equals%2A`</span></span>

### <a name="generic-types"></a><span data-ttu-id="19737-216">Универсальные типы</span><span class="sxs-lookup"><span data-stu-id="19737-216">Generic types</span></span>

<span data-ttu-id="19737-217">Универсальные типы — это такие типы, как `System.Collections.Generic.List<T>`.</span><span class="sxs-lookup"><span data-stu-id="19737-217">Generic types are those types such as `System.Collections.Generic.List<T>`.</span></span> <span data-ttu-id="19737-218">При переходе к этому типу в [обозревателе API .NET](https://docs.microsoft.com/dotnet/api/) и просмотре его URL-адреса вы увидите, что `<T>` записывается в URL-адресе как `-1`, что фактически представляет **\`1**:</span><span class="sxs-lookup"><span data-stu-id="19737-218">If you browse to this type in the [.NET API browser](https://docs.microsoft.com/dotnet/api/) and look at its URL, you see that `<T>` is written as `-1` in the URL, which actually represents **\`1**:</span></span>

`https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1`

<span data-ttu-id="19737-219">Чтобы создать ссылку на универсальный тип, например **List\<T>** , закодируйте символ обратного апострофа **\`** как **%60**, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="19737-219">To link to a generic type such as **List\<T>**, encode the **\`** backtick character as **%60**, as shown in the following example:</span></span>

```markdown
<xref:System.Collections.Generic.List%601>
```

### <a name="methods"></a><span data-ttu-id="19737-220">Методы</span><span class="sxs-lookup"><span data-stu-id="19737-220">Methods</span></span>

<span data-ttu-id="19737-221">Чтобы создать ссылку на метод, можно использовать ссылку либо на общую страницу метода (при этом после имени метода нужно добавить звездочку (`*`)), либо на конкретную перегрузку.</span><span class="sxs-lookup"><span data-stu-id="19737-221">To link to a method, you can either link to the general method page by adding an asterisk (`*`) after the method name, or to a specific overload.</span></span> <span data-ttu-id="19737-222">Например, используйте общую страницу, если нужно указать ссылку на метод `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` без конкретных типов параметров.</span><span class="sxs-lookup"><span data-stu-id="19737-222">For example, use the general page when you want to link to the `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` method without specific parameter types.</span></span> <span data-ttu-id="19737-223">Символ звездочки кодируется как `%2A`.</span><span class="sxs-lookup"><span data-stu-id="19737-223">The asterisk character is encoded as `%2A`.</span></span> <span data-ttu-id="19737-224">Например:</span><span class="sxs-lookup"><span data-stu-id="19737-224">For example:</span></span>

<span data-ttu-id="19737-225">`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` указывает на <xref:System.Object.Equals%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="19737-225">`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` links to <xref:System.Object.Equals%2A?displayProperty=nameWithType></span></span>

<span data-ttu-id="19737-226">Чтобы сослаться на конкретную перегрузку, добавьте скобки после имени метода и включите полное имя типа каждого параметра.</span><span class="sxs-lookup"><span data-stu-id="19737-226">To link to a specific overload, add parenthesis after the method name and include the full type name of each parameter.</span></span> <span data-ttu-id="19737-227">Не ставьте пробелы между именами типов, иначе ссылка не будет работать.</span><span class="sxs-lookup"><span data-stu-id="19737-227">Do not put a space character between the type names or the link won't work.</span></span> <span data-ttu-id="19737-228">Например:</span><span class="sxs-lookup"><span data-stu-id="19737-228">For example:</span></span>

<span data-ttu-id="19737-229">`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` указывает на <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="19737-229">`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` links to <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType></span></span>

## <a name="links-from-includes"></a><span data-ttu-id="19737-230">Ссылки во включаемых файлах</span><span class="sxs-lookup"><span data-stu-id="19737-230">Links from includes</span></span>

<span data-ttu-id="19737-231">Включаемые файлы содержатся в другом каталоге, поэтому для них используются более длинные относительные пути.</span><span class="sxs-lookup"><span data-stu-id="19737-231">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="19737-232">Чтобы добавить ссылку на статью во включаемый файл, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="19737-232">To link to an article from an include file, use this format:</span></span>

```markdown
[link text](../articles/folder/article-name.md)
```

> [!TIP]
> <span data-ttu-id="19737-233">Расширение [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) для Visual Studio Code помогает правильно вставлять относительные ссылки и закладки в автоматическом режиме.</span><span class="sxs-lookup"><span data-stu-id="19737-233">The [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) extension for Visual Studio Code helps you insert relative links and bookmarks correctly without the tedium of figuring out paths.</span></span>

## <a name="links-in-selectors"></a><span data-ttu-id="19737-234">Ссылки в селекторах</span><span class="sxs-lookup"><span data-stu-id="19737-234">Links in selectors</span></span>

<span data-ttu-id="19737-235">Селектор — это компонент навигации, который отображается в статье в документации как раскрывающийся список.</span><span class="sxs-lookup"><span data-stu-id="19737-235">A selector is a navigation component that appears in a docs article as a drop-down list.</span></span> <span data-ttu-id="19737-236">Когда читатель выбирает значение в раскрывающемся списке, браузер открывает выбранную статью.</span><span class="sxs-lookup"><span data-stu-id="19737-236">When a reader selects a value in the drop-down, the browser opens the selected article.</span></span> <span data-ttu-id="19737-237">Обычно список в селекторе содержит ссылки на связанные статьи, например, та же тема на разных языках программирования или тесно связанная серия статей.</span><span class="sxs-lookup"><span data-stu-id="19737-237">Typically the selector list contains links to closely related articles, for example the same subject matter in multiple programming languages or a closely related series of articles.</span></span>

<span data-ttu-id="19737-238">Если во включаемый файл внедрены селекторы, используйте следующую структуру ссылки:</span><span class="sxs-lookup"><span data-stu-id="19737-238">If you have selectors that are embedded in an include, use the following link structure:</span></span>

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md)
   ```

## <a name="reference-style-links"></a><span data-ttu-id="19737-239">Ссылки типа сносок</span><span class="sxs-lookup"><span data-stu-id="19737-239">Reference-style links</span></span>

<span data-ttu-id="19737-240">Ссылки типа сносок используются для того, чтобы пользователю было легче воспринимать содержимое источника.</span><span class="sxs-lookup"><span data-stu-id="19737-240">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="19737-241">Для ссылок типа сносок синтаксис встроенной ссылки заменяется упрощенным вариантом, который позволяет переместить длинные URL-адреса в конец статьи.</span><span class="sxs-lookup"><span data-stu-id="19737-241">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="19737-242">Ниже приведен пример от [Daring Fireball](https://daringfireball.net/projects/markdown/).</span><span class="sxs-lookup"><span data-stu-id="19737-242">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="19737-243">Встроенный текст:</span><span class="sxs-lookup"><span data-stu-id="19737-243">Inline text:</span></span>

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

<span data-ttu-id="19737-244">Ссылки типа сносок в конце статьи:</span><span class="sxs-lookup"><span data-stu-id="19737-244">Link references at the end of the article:</span></span>

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```

<span data-ttu-id="19737-245">Обязательно используйте пробел после двоеточия перед ссылкой.</span><span class="sxs-lookup"><span data-stu-id="19737-245">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="19737-246">Если при добавлении ссылок на другие технические статьи вы забудете включить пробел, ссылка не будет работать в опубликованной статье.</span><span class="sxs-lookup"><span data-stu-id="19737-246">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="19737-247">Ссылки на страницы, не являющиеся частью технической документации</span><span class="sxs-lookup"><span data-stu-id="19737-247">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="19737-248">Чтобы добавить ссылку на страницу корпорации Майкрософт другого характера (например, на страницу с ценами, страницу соглашения об уровне обслуживания или любую другую страницу, не являющуюся статьей документации), используйте абсолютный URL-адрес без указания языка.</span><span class="sxs-lookup"><span data-stu-id="19737-248">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="19737-249">Такие ссылки работают на сайте GitHub и на отображаемом сайте:</span><span class="sxs-lookup"><span data-stu-id="19737-249">The goal here is that links work in GitHub and on the rendered site:</span></span>

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```

## <a name="links-to-third-party-sites"></a><span data-ttu-id="19737-250">Ссылки на сторонние сайты</span><span class="sxs-lookup"><span data-stu-id="19737-250">Links to third-party sites</span></span>

<span data-ttu-id="19737-251">Лучше избегать перенаправления пользователей на другие сайты.</span><span class="sxs-lookup"><span data-stu-id="19737-251">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="19737-252">Но иногда это необходимо. При размещении ссылок на сторонние сайты руководствуйтесь следующей информацией:</span><span class="sxs-lookup"><span data-stu-id="19737-252">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="19737-253">**Отслеживаемость**. Добавляйте ссылки на содержимое сторонних поставщиков, если именно к нему требуется предоставить общий доступ.</span><span class="sxs-lookup"><span data-stu-id="19737-253">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="19737-254">Например, предоставлять описание того, как использовать средства разработчика Android, не входит в обязанности корпорации Майкрософт. Это задача Google.</span><span class="sxs-lookup"><span data-stu-id="19737-254">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="19737-255">При необходимости мы можем объяснить, как использовать средства разработчика Android *с* Azure, но руководство по применению этих средств должна предоставить корпорация Google.</span><span class="sxs-lookup"><span data-stu-id="19737-255">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="19737-256">**Утверждение руководителем проектов**. Запрашивайте в корпорации Майкрософт утверждение ссылок на содержимое сторонних поставщиков.</span><span class="sxs-lookup"><span data-stu-id="19737-256">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="19737-257">Такие ссылки предполагают определенный уровень ответственности за надежность информации и выполнение инструкций пользователем.</span><span class="sxs-lookup"><span data-stu-id="19737-257">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="19737-258">**Проверки актуальности**. Следите за актуальностью, правильностью и релевантностью информации. Регулярно проверяйте, не изменилась ли ссылка.</span><span class="sxs-lookup"><span data-stu-id="19737-258">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn't changed.</span></span>
- <span data-ttu-id="19737-259">**Информация о переходе на сайт стороннего поставщика**. Обязательно уведомляйте пользователей о том, что они переходят на другой сайт.</span><span class="sxs-lookup"><span data-stu-id="19737-259">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="19737-260">Если это не следует из контекста, добавьте соответствующую фразу.</span><span class="sxs-lookup"><span data-stu-id="19737-260">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="19737-261">Например: "Предварительные требования включают установку средств для разработчиков Android, которые вы можете скачать на сайте Android Studio".</span><span class="sxs-lookup"><span data-stu-id="19737-261">For example: "Prerequisites include the Android Developer Tools, which you can download on the Android Studio site."</span></span>
- <span data-ttu-id="19737-262">**Дальнейшие действия**. Неплохим решением будет добавить ссылку, скажем, на блог MVP в разделе "Дальнейшие действия".</span><span class="sxs-lookup"><span data-stu-id="19737-262">**Next steps**: It's fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="19737-263">Опять же, при этом пользователь должен понимать, что он покидает текущий сайт.</span><span class="sxs-lookup"><span data-stu-id="19737-263">Again, just make sure that users understand they'll be leaving the site.</span></span>
- <span data-ttu-id="19737-264">**Юридическая информация**. Юридическая информация предоставляется в разделе **Ссылки на веб-сайты третьих лиц** на странице **условий использования**. Ссылка на нее размещена в нижнем колонтитуле каждой страницы сайта microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="19737-264">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every microsoft.com page.</span></span>

<!-- link references -->
[CommonMark]: https://commonmark.org/
[Markdig]: https://github.com/lunet-io/markdig
[GFM]: https://help.github.com/categories/writing-on-github/
[docs]: https://docs.microsoft.com
[Обозреватель API .NET]: https://docs.microsoft.com/dotnet/api/
[.NET API browser]: https://docs.microsoft.com/dotnet/api/
[Windows UWP]: https://docs.microsoft.com/uwp/api
[docsextension]: https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown
[Сайт автозаполнения]: https://xref.docs.microsoft.com/autocomplete?text=
[autocomplete site]: https://xref.docs.microsoft.com/autocomplete?text=
