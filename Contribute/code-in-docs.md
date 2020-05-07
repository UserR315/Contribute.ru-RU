---
title: Включение кода в документы
description: Узнайте, как включить элементы и фрагменты кода в статьи, публикуемые на сайте docs.microsoft.com.
author: tdykstra
ms.author: tdykstra
ms.date: 03/03/2020
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 4aa34196f59a69651dd19add35a0351dd9b5d59b
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336469"
---
# <a name="how-to-include-code-in-docs"></a><span data-ttu-id="8a69b-103">Включение кода в документы</span><span class="sxs-lookup"><span data-stu-id="8a69b-103">How to include code in docs</span></span>

<span data-ttu-id="8a69b-104">Есть несколько способов включить код в статью, публикуемую на сайте docs.microsoft.com:</span><span class="sxs-lookup"><span data-stu-id="8a69b-104">There are several ways to include code in an article published on docs.microsoft.com:</span></span>

* <span data-ttu-id="8a69b-105">Отдельные элементы (слова) в строке.</span><span class="sxs-lookup"><span data-stu-id="8a69b-105">Individual elements (words) within a line.</span></span>

  <span data-ttu-id="8a69b-106">Ниже приведен пример стиля `code`.</span><span class="sxs-lookup"><span data-stu-id="8a69b-106">Here's an example of `code` style.</span></span>

  <span data-ttu-id="8a69b-107">Используйте формат кода при ссылке на именованные параметры и переменные в ближайшем блоке кода в тексте.</span><span class="sxs-lookup"><span data-stu-id="8a69b-107">Use code format when referring to named parameters and variables in a nearby code block in your text.</span></span> <span data-ttu-id="8a69b-108">Формат кода также можно использовать для свойств, методов, классов и ключевых слов языка.</span><span class="sxs-lookup"><span data-stu-id="8a69b-108">Code format may also be used for properties, methods, classes, and language keywords.</span></span> <span data-ttu-id="8a69b-109">Дополнительные сведения см. в разделе [Элементы кода](#code-elements) далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="8a69b-109">For more information, see [Code elements](#code-elements) later in this article..</span></span>

* <span data-ttu-id="8a69b-110">Блоки кода в файле Markdown, содержащем статью.</span><span class="sxs-lookup"><span data-stu-id="8a69b-110">Code blocks in the article Markdown file.</span></span>

  ```markdown
      ```csharp
      public static void Log(string message)
      {
          _logger.LogInformation(message);
      }
      ```
  ```

  <span data-ttu-id="8a69b-111">Используйте встроенные блоки кода, когда непрактично отображать код по ссылке на файл кода.</span><span class="sxs-lookup"><span data-stu-id="8a69b-111">Use inline code blocks when it's impractical to display code by reference to a code file.</span></span> <span data-ttu-id="8a69b-112">Дополнительные сведения см. в разделе [Блоки кода](#inline-code-blocks) далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="8a69b-112">For more information, see [Code blocks](#inline-code-blocks) later in this article.</span></span>

* <span data-ttu-id="8a69b-113">Блоки кода с использованием ссылки на файл кода в локальном репозитории.</span><span class="sxs-lookup"><span data-stu-id="8a69b-113">Code blocks by reference to a code file in the local repository.</span></span>

  ```markdown
  :::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
  ```

  <span data-ttu-id="8a69b-114">Дополнительные сведения см. в разделе [Ссылки на фрагменты кода в репозитории](#in-repo-snippet-references) далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="8a69b-114">For more information, see [In-repo snippet references](#in-repo-snippet-references) later in this article.</span></span>

* <span data-ttu-id="8a69b-115">Блоки кода с использованием ссылки на файл кода в другом репозитории.</span><span class="sxs-lookup"><span data-stu-id="8a69b-115">Code blocks by reference to a code file in another repository.</span></span>

  ```markdown
  :::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
  ```
  
  <span data-ttu-id="8a69b-116">Дополнительные сведения см. в разделе [Ссылки на фрагменты кода вне репозитория](#out-of-repo-snippet-references) далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="8a69b-116">For more information, see [Out-of-repo snippet references](#out-of-repo-snippet-references) later in this article.</span></span>
  
* <span data-ttu-id="8a69b-117">Блоки кода, которые позволяют пользователю выполнять код в браузере.</span><span class="sxs-lookup"><span data-stu-id="8a69b-117">Code blocks that let the user execute code in the browser.</span></span>

   ```markdown
  :::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
  ```

  <span data-ttu-id="8a69b-118">Дополнительные сведения см. в разделе [Интерактивные фрагменты кода](#interactive-code-snippets) далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="8a69b-118">For more information, see [Interactive code snippets](#interactive-code-snippets) later in this article.</span></span>

<span data-ttu-id="8a69b-119">Помимо описания синтаксиса Markdown для каждого метода включения кода, в статье приведено [общее руководство для всех блоков кода](#code-blocks).</span><span class="sxs-lookup"><span data-stu-id="8a69b-119">Besides explaining the Markdown for each of these ways to include code, the article provides some [general guidance for all code blocks](#code-blocks).</span></span>

## <a name="code-elements"></a><span data-ttu-id="8a69b-120">Элементы кода</span><span class="sxs-lookup"><span data-stu-id="8a69b-120">Code elements</span></span>

<span data-ttu-id="8a69b-121">"Элемент кода" является ключевым словом языка программирования, именем класса, именем свойства и т. д.</span><span class="sxs-lookup"><span data-stu-id="8a69b-121">A "code element" is a programming language keyword, class name, property name, and so forth.</span></span> <span data-ttu-id="8a69b-122">Не всегда очевидно, что рассматривается в качестве кода.</span><span class="sxs-lookup"><span data-stu-id="8a69b-122">It's not always obvious what qualifies as code.</span></span> <span data-ttu-id="8a69b-123">Например, имена пакетов NuGet должны считаться кодом.</span><span class="sxs-lookup"><span data-stu-id="8a69b-123">For example, NuGet package names should be treated as code.</span></span> <span data-ttu-id="8a69b-124">Если возникают сомнения, ознакомьтесь с [рекомендациями по форматированию текста](text-formatting-guidelines.md).</span><span class="sxs-lookup"><span data-stu-id="8a69b-124">When in doubt, see [Text formatting guidelines](text-formatting-guidelines.md).</span></span>

### <a name="inline-code-style"></a><span data-ttu-id="8a69b-125">Встроенные стили кода</span><span class="sxs-lookup"><span data-stu-id="8a69b-125">Inline code style</span></span>

<span data-ttu-id="8a69b-126">Чтобы включить элемент кода в текст статьи, поместите его между одинарными кавычками в виде обратного апострофа (\`) для указания стиля кода.</span><span class="sxs-lookup"><span data-stu-id="8a69b-126">To include a code element in article text, surround it with backticks (\`) to indicate code style.</span></span>
<span data-ttu-id="8a69b-127">Встроенный стиль кода не должен использовать формат тройных кавычек.</span><span class="sxs-lookup"><span data-stu-id="8a69b-127">Inline code style shouldn't use the triple-backtick format.</span></span>

|<span data-ttu-id="8a69b-128">Markdown</span><span class="sxs-lookup"><span data-stu-id="8a69b-128">Markdown</span></span> |<span data-ttu-id="8a69b-129">Отображение</span><span class="sxs-lookup"><span data-stu-id="8a69b-129">Rendered</span></span> |
|---------|---------|
|<span data-ttu-id="8a69b-130">По умолчанию Entity Framework интерпретирует свойство с именем \`Id\` или \`ClassnameID\` как первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="8a69b-130">By default, the Entity Framework interprets a property that's named \`Id\` or \`ClassnameID\` as the primary key.</span></span>|<span data-ttu-id="8a69b-131">По умолчанию Entity Framework интерпретирует свойство с именем `Id` или `ClassnameID` как первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="8a69b-131">By default, the Entity Framework interprets a property that's named `Id` or `ClassnameID` as the primary key.</span></span>|

<span data-ttu-id="8a69b-132">При локализации статьи (переводе на другие языки) текст, имеющий стиль кода, не переводится.</span><span class="sxs-lookup"><span data-stu-id="8a69b-132">When an article is localized (translated into other languages), text styled as code is left untranslated.</span></span> <span data-ttu-id="8a69b-133">Если вы хотите предотвратить локализацию без использования стиля кода, см. раздел [Нелокализованные строки](markdown-reference.md#non-localized-strings).</span><span class="sxs-lookup"><span data-stu-id="8a69b-133">If you want to prevent localization without using code style, see [Non-localized strings](markdown-reference.md#non-localized-strings).</span></span>

### <a name="bold-style"></a><span data-ttu-id="8a69b-134">Полужирный стиль</span><span class="sxs-lookup"><span data-stu-id="8a69b-134">Bold style</span></span>

<span data-ttu-id="8a69b-135">В более старых руководствах по стилю для встроенного кода используется полужирный шрифт.</span><span class="sxs-lookup"><span data-stu-id="8a69b-135">Some older style guides specify bold for inline code.</span></span> <span data-ttu-id="8a69b-136">Полужирный шрифт можно использовать, когда стиль кода настолько перегружен, что его трудно читать.</span><span class="sxs-lookup"><span data-stu-id="8a69b-136">Bold is an option when code style is so obtrusive as to compromise readability.</span></span> <span data-ttu-id="8a69b-137">Например, таблица Markdown со множеством элементов кода может выглядеть перегруженной, если везде применять стилизацию кода.</span><span class="sxs-lookup"><span data-stu-id="8a69b-137">For example, a Markdown table with mostly code elements might look too busy with code styling everywhere.</span></span> <span data-ttu-id="8a69b-138">Если выбрано использование полужирного начертания, используйте [синтаксис нелокализованных строк](markdown-reference.md#non-localized-strings), чтобы код не был локализован.</span><span class="sxs-lookup"><span data-stu-id="8a69b-138">If you choose to use bold style, use [non-localized strings syntax](markdown-reference.md#non-localized-strings) to make sure that code is not localized.</span></span>

### <a name="links"></a><span data-ttu-id="8a69b-139">Создание ссылок</span><span class="sxs-lookup"><span data-stu-id="8a69b-139">Links</span></span>

<span data-ttu-id="8a69b-140">Ссылка на справочную документацию может оказаться более полезной, чем формат кода в некоторых контекстах.</span><span class="sxs-lookup"><span data-stu-id="8a69b-140">A link to reference documentation may be more helpful than code format in some contexts.</span></span> <span data-ttu-id="8a69b-141">Если используется ссылка, не применяйте формат кода к тексту ссылки.</span><span class="sxs-lookup"><span data-stu-id="8a69b-141">If you use a link, don't apply code format to the link text.</span></span> <span data-ttu-id="8a69b-142">Стилизация ссылки как кода может скрыть тот факт, что текст является ссылкой.</span><span class="sxs-lookup"><span data-stu-id="8a69b-142">Styling a link as code can obscure the fact that the text is a link.</span></span>

<span data-ttu-id="8a69b-143">Если вы используете ссылку и ссылаетесь на тот же элемент позже в том же контексте, сделайте последующие экземпляры форматом кода, а не ссылками.</span><span class="sxs-lookup"><span data-stu-id="8a69b-143">If you use a link and refer to the same element later in the same context, make the subsequent instances code format rather than links.</span></span>

### <a name="placeholders"></a><span data-ttu-id="8a69b-144">Заполнители</span><span class="sxs-lookup"><span data-stu-id="8a69b-144">Placeholders</span></span>

<span data-ttu-id="8a69b-145">Если требуется, чтобы пользователь заменил часть отображаемого кода собственными значениями, используйте текст заполнителя, заключенный в угловые или фигурные скобки.</span><span class="sxs-lookup"><span data-stu-id="8a69b-145">If you want the user to replace a section of displayed code with their own values, use placeholder text marked off by angle brackets or curly braces.</span></span> <span data-ttu-id="8a69b-146">Например, `az group delete -n <ResourceGroupName>`.</span><span class="sxs-lookup"><span data-stu-id="8a69b-146">For example: `az group delete -n <ResourceGroupName>`.</span></span> <span data-ttu-id="8a69b-147">Объясните, что квадратные или фигурные скобки необходимо удалить при замене на реальные значения.</span><span class="sxs-lookup"><span data-stu-id="8a69b-147">Explain that the brackets or braces must be removed when substituting real values.</span></span>

## <a name="code-blocks"></a><span data-ttu-id="8a69b-148">Блоки кода</span><span class="sxs-lookup"><span data-stu-id="8a69b-148">Code blocks</span></span>

<span data-ttu-id="8a69b-149">Синтаксис для включения кода в документ зависит от того, где находится код:</span><span class="sxs-lookup"><span data-stu-id="8a69b-149">The syntax for including code in a doc depends on where the code is located:</span></span>

* <span data-ttu-id="8a69b-150">[в файле Markdown статьи](#inline-code-blocks);</span><span class="sxs-lookup"><span data-stu-id="8a69b-150">[In the article Markdown file](#inline-code-blocks)</span></span>
* <span data-ttu-id="8a69b-151">[в файле кода в том же репозитории](#in-repo-snippet-references);</span><span class="sxs-lookup"><span data-stu-id="8a69b-151">[In a code file in the same repository](#in-repo-snippet-references)</span></span>
* <span data-ttu-id="8a69b-152">[в файле кода в другом репозитории](#out-of-repo-snippet-references).</span><span class="sxs-lookup"><span data-stu-id="8a69b-152">[In a code file in a different repository](#out-of-repo-snippet-references)</span></span>

<span data-ttu-id="8a69b-153">Ниже приведены рекомендации, которые применяются для всех трех типов блоков кода:</span><span class="sxs-lookup"><span data-stu-id="8a69b-153">Following are guidelines that apply to all three types of code blocks:</span></span>

* <span data-ttu-id="8a69b-154">[автоматизируйте проверку кода](#code-validation);</span><span class="sxs-lookup"><span data-stu-id="8a69b-154">[Automate code validation.](#code-validation)</span></span>
* <span data-ttu-id="8a69b-155">[выделяйте основные строки кода](#highlighting);</span><span class="sxs-lookup"><span data-stu-id="8a69b-155">[Highlight key lines of code.](#highlighting)</span></span>
* <span data-ttu-id="8a69b-156">[избегайте горизонтальных полос прокрутки](#horizontal-scroll-bars).</span><span class="sxs-lookup"><span data-stu-id="8a69b-156">[Avoid horizontal scroll bars.](#horizontal-scroll-bars)</span></span>

### <a name="screenshots"></a><span data-ttu-id="8a69b-157">Снимки экрана</span><span class="sxs-lookup"><span data-stu-id="8a69b-157">Screenshots</span></span>

<span data-ttu-id="8a69b-158">Все методы, перечисленные в предыдущем разделе, приводят к созданию пригодных для использования блоков кода:</span><span class="sxs-lookup"><span data-stu-id="8a69b-158">All of the methods listed in the preceding section result in usable code blocks:</span></span>

* <span data-ttu-id="8a69b-159">Вы можете копировать их.</span><span class="sxs-lookup"><span data-stu-id="8a69b-159">You can copy and paste from them.</span></span>
* <span data-ttu-id="8a69b-160">Они индексируются поисковыми механизмами.</span><span class="sxs-lookup"><span data-stu-id="8a69b-160">They're indexed by search engines.</span></span>
* <span data-ttu-id="8a69b-161">Они доступны для средств чтения с экрана.</span><span class="sxs-lookup"><span data-stu-id="8a69b-161">They're accessible to screen readers.</span></span>

<span data-ttu-id="8a69b-162">Это лишь несколько из причин, по которым снимки экрана IDE не рекомендуются в качестве метода включения кода в статью.</span><span class="sxs-lookup"><span data-stu-id="8a69b-162">These are just a few of the reasons why IDE screenshots aren't recommended as a method of including code in an article.</span></span> <span data-ttu-id="8a69b-163">Используйте снимки экрана IDE для кода только в том случае, если вы показываете что-то о самой среде IDE, например IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="8a69b-163">Use IDE screenshots for code only if you're showing something about the IDE itself, like IntelliSense.</span></span> <span data-ttu-id="8a69b-164">Не используйте снимки экрана, только чтобы показать цвета и выделение.</span><span class="sxs-lookup"><span data-stu-id="8a69b-164">Don't use screenshots just to show colorization and highlighting.</span></span>

### <a name="code-validation"></a><span data-ttu-id="8a69b-165">Проверка кода</span><span class="sxs-lookup"><span data-stu-id="8a69b-165">Code validation</span></span>

<span data-ttu-id="8a69b-166">В некоторых репозиториях реализованы процессы, которые автоматически компилируют все примеры кода для проверки на наличие ошибок.</span><span class="sxs-lookup"><span data-stu-id="8a69b-166">Some repositories have implemented processes that automatically compile all sample code to check for errors.</span></span> <span data-ttu-id="8a69b-167">Это делается в репозитории .NET.</span><span class="sxs-lookup"><span data-stu-id="8a69b-167">The .NET repository does this.</span></span> <span data-ttu-id="8a69b-168">Дополнительные сведения см. в разделе об [участии](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md) в репозитории .NET.</span><span class="sxs-lookup"><span data-stu-id="8a69b-168">For more information, see [Contributing](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md) in the .NET repository.</span></span>

<span data-ttu-id="8a69b-169">Если вы включаете блоки кода из другого репозитория, обсудите с владельцами стратегию обслуживания кода, чтобы включенный код не перестал работать и не устарел при обновлении версий библиотек, используемых кодом.</span><span class="sxs-lookup"><span data-stu-id="8a69b-169">If you are including code blocks from another repository, work with the owners on a maintenance strategy for the code so that your included code does not break or go out of date as new versions of the libraries the code uses are shipped.</span></span>

### <a name="highlighting"></a><span data-ttu-id="8a69b-170">Выделение</span><span class="sxs-lookup"><span data-stu-id="8a69b-170">Highlighting</span></span>

<span data-ttu-id="8a69b-171">Фрагменты кода обычно содержат больше кода, чем необходимо для предоставления контекста.</span><span class="sxs-lookup"><span data-stu-id="8a69b-171">Snippets typically include more code than necessary in order to provide context.</span></span> <span data-ttu-id="8a69b-172">Чтобы улучшить читаемость, рекомендуется выделить ключевые строки, на которых нужно сконцентрировать внимание во фрагменте кода, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="8a69b-172">It helps readability when you highlight the key lines that you're focusing on in the snippet, as in this example:</span></span>

![Пример отображения выделенного кода](media/code-in-docs/highlighted-code.png)

<span data-ttu-id="8a69b-174">Если код включен в файл Markdown статьи, его не удастся выделить.</span><span class="sxs-lookup"><span data-stu-id="8a69b-174">You can't highlight code when you include it in the article Markdown file.</span></span> <span data-ttu-id="8a69b-175">Выделение поддерживается только для фрагментов кода, включенных с помощью ссылки на файл кода.</span><span class="sxs-lookup"><span data-stu-id="8a69b-175">It works only for code snippets included by reference to a code file.</span></span>

### <a name="horizontal-scroll-bars"></a><span data-ttu-id="8a69b-176">Горизонтальные полосы прокрутки</span><span class="sxs-lookup"><span data-stu-id="8a69b-176">Horizontal scroll bars</span></span>

<span data-ttu-id="8a69b-177">Разбейте длинные строки, чтобы избежать горизонтальных полос прокрутки.</span><span class="sxs-lookup"><span data-stu-id="8a69b-177">Break up long lines to avoid horizontal scroll bars.</span></span> <span data-ttu-id="8a69b-178">Полосы прокрутки в блоках кода затрудняют его чтение.</span><span class="sxs-lookup"><span data-stu-id="8a69b-178">Scroll bars on code blocks make code hard to read.</span></span> <span data-ttu-id="8a69b-179">Это особенно проблематично в более длинных блоках кода, где невозможно одновременно показать полосу прокрутки и строку, которую необходимо прочитать.</span><span class="sxs-lookup"><span data-stu-id="8a69b-179">They're especially problematic on longer code blocks, where it may be impossible to see the scroll bar and the line you want to read at the same time.</span></span>

<span data-ttu-id="8a69b-180">Чтобы свести к минимуму горизонтальные полосы прокрутки в блоках кода, рекомендуется разбивать строки кода, длиннее 85 символов.</span><span class="sxs-lookup"><span data-stu-id="8a69b-180">A good practice for minimizing horizontal scroll bars on code blocks is to break up code lines longer than 85 characters.</span></span> <span data-ttu-id="8a69b-181">Но помните, что присутствие или отсутствие полосы прокрутки не является единственным критерием удобочитаемости.</span><span class="sxs-lookup"><span data-stu-id="8a69b-181">But keep in mind that the presence or absence of a scroll bar isn't the only criterion of readability.</span></span> <span data-ttu-id="8a69b-182">Если разбивка длинной строки затрудняет чтение или удобство копирования и вставки, строка может быть длиннее 85 символов.</span><span class="sxs-lookup"><span data-stu-id="8a69b-182">If breaking a line before 85 hurts readability or copy-paste convenience, feel free to go over 85.</span></span>

## <a name="inline-code-blocks"></a><span data-ttu-id="8a69b-183">Встроенные блоки кода</span><span class="sxs-lookup"><span data-stu-id="8a69b-183">Inline code blocks</span></span>

<span data-ttu-id="8a69b-184">Используйте встроенные блоки кода, только когда непрактично отображать код по ссылке на файл кода.</span><span class="sxs-lookup"><span data-stu-id="8a69b-184">Use inline code blocks only when it's impractical to display code by reference to a code file.</span></span> <span data-ttu-id="8a69b-185">Как правило, встроенный код сложнее тестировать и обновлять по сравнению с файлом кода, который является частью полного проекта.</span><span class="sxs-lookup"><span data-stu-id="8a69b-185">Inline code is generally more difficult to test and keep up to date compared to a code file that is part of a complete project.</span></span>  <span data-ttu-id="8a69b-186">И встроенный код может опускать контекст, который может помочь разработчику понять и использовать код.</span><span class="sxs-lookup"><span data-stu-id="8a69b-186">And inline code may omit context that could help the developer to understand and use the code.</span></span> <span data-ttu-id="8a69b-187">Эти рекомендации относятся главным образом к языкам программирования.</span><span class="sxs-lookup"><span data-stu-id="8a69b-187">These considerations apply mainly to programming languages.</span></span> <span data-ttu-id="8a69b-188">Встроенные блоки кода также могут использоваться для выходных и входных данных (например, JSON), языков запросов (таких как SQL) и языков сценариев (например, PowerShell).</span><span class="sxs-lookup"><span data-stu-id="8a69b-188">Inline code blocks can also be used for outputs and inputs (such as JSON), query languages (such as SQL), and scripting languages (such as PowerShell).</span></span>
  
<span data-ttu-id="8a69b-189">Есть два способа обозначить, что раздел текста в файле статьи является блоком кода: *отделив* его тройными обратными кавычками (\`\`\`) или добавив отступ.</span><span class="sxs-lookup"><span data-stu-id="8a69b-189">There are two ways to indicate a section of text in an article file is a code block: by *fencing* it in triple-backticks (\`\`\`) or by indenting it.</span></span> <span data-ttu-id="8a69b-190">Отделение является предпочтительным, так как в этом случае можно указать язык.</span><span class="sxs-lookup"><span data-stu-id="8a69b-190">Fencing is preferred because it lets you specify the language.</span></span> <span data-ttu-id="8a69b-191">Старайтесь не использовать отступы, потому что с ними просто ошибиться и другому автору будет сложно понять ваше намерение при редактировании статьи.</span><span class="sxs-lookup"><span data-stu-id="8a69b-191">Avoid using indentation because it's too easy to get wrong and it may be hard for another writer to understand your intent when they need to edit your article.</span></span>

<span data-ttu-id="8a69b-192">Языковые индикаторы размещаются сразу же после открытия тройных обратных кавычек, как в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="8a69b-192">Language indicators are placed immediately after the opening triple-backticks, as in the following example:</span></span>

<span data-ttu-id="8a69b-193">Markdown:</span><span class="sxs-lookup"><span data-stu-id="8a69b-193">Markdown:</span></span>

```markdown
    ```json
    {
        "aggregator": {
            "batchSize": 1000,
            "flushTimeout": "00:00:30"
        }
    }
    ```
```

<span data-ttu-id="8a69b-194">Отображение:</span><span class="sxs-lookup"><span data-stu-id="8a69b-194">Rendered:</span></span>

```json
{
    "aggregator": {
        "batchSize": 1000,
        "flushTimeout": "00:00:30"
    }
}
```

<span data-ttu-id="8a69b-195">Дополнительные сведения о значениях, которые можно использовать в качестве индикаторов языка, см. в разделе [об именах и псевдонимах языков](http://highlightjs.readthedocs.io/en/latest/css-classes-reference.html#language-names-and-aliases).</span><span class="sxs-lookup"><span data-stu-id="8a69b-195">For information about the values you can use as language indicators, see [Language names and aliases](http://highlightjs.readthedocs.io/en/latest/css-classes-reference.html#language-names-and-aliases).</span></span>

<span data-ttu-id="8a69b-196">Если вы используете слово языка или среды после тройных кавычек (\`\`\`), которые не поддерживаются, это слово отображается в заголовке раздела кода на отрисованной странице.</span><span class="sxs-lookup"><span data-stu-id="8a69b-196">If you use a language or environment word after the triple-backticks (\`\`\`) that isn't supported, that word appears in the code section title bar on the rendered page.</span></span> <span data-ttu-id="8a69b-197">По возможности используйте индикатор языка или среды во встроенных блоках кода.</span><span class="sxs-lookup"><span data-stu-id="8a69b-197">Whenever possible, use a language or environment indicator in your inline code blocks.</span></span>

> [!NOTE]
> <span data-ttu-id="8a69b-198">При копировании и вставке кода из документа Word убедитесь, что в нем нет изогнутых кавычек, которые не являются допустимыми в коде (например, `“` и `’`).</span><span class="sxs-lookup"><span data-stu-id="8a69b-198">If you copy and paste code from a Word document, make sure it has no "curly quotes," which aren't valid in code (for example, `“` and `’`).</span></span> <span data-ttu-id="8a69b-199">Если есть, замените их на обычные кавычки (`'` и `"`).</span><span class="sxs-lookup"><span data-stu-id="8a69b-199">If it does, change them back to normal quotes (`'` and `"`).</span></span> <span data-ttu-id="8a69b-200">В качестве альтернативы можно воспользоваться пакетом Docs Authoring Pack с [функцией замены парных кавычек](docs-authoring/smart-quote-replacement.md).</span><span class="sxs-lookup"><span data-stu-id="8a69b-200">Alternatively, rely on the Docs Authoring Pack, [smart quotes replacement feature](docs-authoring/smart-quote-replacement.md).</span></span>

## <a name="in-repo-snippet-references"></a><span data-ttu-id="8a69b-201">Ссылки на фрагмент кода в репозитории</span><span class="sxs-lookup"><span data-stu-id="8a69b-201">In-repo snippet references</span></span>

<span data-ttu-id="8a69b-202">Предпочтительный способ включения фрагментов кода для языков программирования в документы — использование ссылки на файл кода.</span><span class="sxs-lookup"><span data-stu-id="8a69b-202">The preferred way to include code snippets for programming languages in docs is by reference to a code file.</span></span> <span data-ttu-id="8a69b-203">Этот метод позволяет выделить строки кода и предоставить больше контекста для фрагмента кода, доступного в GitHub для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="8a69b-203">This method gives you the ability to highlight lines of code and makes the wider context of the snippet available on GitHub for developers to use.</span></span> <span data-ttu-id="8a69b-204">Код можно включить с помощью тройного двоеточия (:\:\:) вручную или в Visual Studio Code с помощью пакета [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span><span class="sxs-lookup"><span data-stu-id="8a69b-204">You can include code by using the triple colon format (:\:\:) either manually or in Visual Studio Code with the help of the [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span></span>

1. <span data-ttu-id="8a69b-205">Находясь в Visual Studio Code, нажмите клавиши <kbd>ALT+M</kbd> или <kbd>OPTION+M</kbd> и выберите "Фрагмент кода".</span><span class="sxs-lookup"><span data-stu-id="8a69b-205">In Visual Studio Code, click <kbd>Alt + M</kbd> or <kbd>Option + M</kbd> and select Snippet.</span></span>
2. <span data-ttu-id="8a69b-206">Вам будет предложено выполнить поиск по всему содержимому, в какой-то области или по различным репозиториям.</span><span class="sxs-lookup"><span data-stu-id="8a69b-206">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="8a69b-207">Для локального поиска выберите полный поиск.</span><span class="sxs-lookup"><span data-stu-id="8a69b-207">To search locally, select Full Search.</span></span>
3. <span data-ttu-id="8a69b-208">Введите условие поиска и найдите нужный файл.</span><span class="sxs-lookup"><span data-stu-id="8a69b-208">Enter a search term to find the file.</span></span> <span data-ttu-id="8a69b-209">Найдя файл, выберите его.</span><span class="sxs-lookup"><span data-stu-id="8a69b-209">Once you've found the file, select the file.</span></span>
4. <span data-ttu-id="8a69b-210">Затем выберите, какие строки кода нужно включить в фрагмент, используя</span><span class="sxs-lookup"><span data-stu-id="8a69b-210">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="8a69b-211">следующие параметры: **ИД**, **Диапазон** или **Никакие**.</span><span class="sxs-lookup"><span data-stu-id="8a69b-211">The options are: **ID**, **Range** and **None**.</span></span>
5. <span data-ttu-id="8a69b-212">В зависимости от выбора на шаге 4 предоставьте необходимые значения.</span><span class="sxs-lookup"><span data-stu-id="8a69b-212">Based on your selection from Step 4, provide a value if necessary.</span></span>

<span data-ttu-id="8a69b-213">Отображение всего файла кода:</span><span class="sxs-lookup"><span data-stu-id="8a69b-213">Display entire code file:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

<span data-ttu-id="8a69b-214">Отображение части файла кода путем указания номера строк:</span><span class="sxs-lookup"><span data-stu-id="8a69b-214">Display part of a code file by specifying line numbers:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="8a69b-215">Отображение части файла кода путем указания имени фрагмента кода:</span><span class="sxs-lookup"><span data-stu-id="8a69b-215">Display part of a code file by specifying a snippet name:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

<span data-ttu-id="8a69b-216">В следующих разделах описаны эти примеры:</span><span class="sxs-lookup"><span data-stu-id="8a69b-216">The following sections explain these examples:</span></span>

* [<span data-ttu-id="8a69b-217">Использование относительного пути к файлу кода</span><span class="sxs-lookup"><span data-stu-id="8a69b-217">Use a relative path to the code file</span></span>](#path-to-code-file)
* [<span data-ttu-id="8a69b-218">Включение только выбранных номеров строк</span><span class="sxs-lookup"><span data-stu-id="8a69b-218">Include only selected line numbers</span></span>](#selected-line-numbers)
* [<span data-ttu-id="8a69b-219">Использование ссылки на фрагмент кода с именем</span><span class="sxs-lookup"><span data-stu-id="8a69b-219">Refer to a named snippet</span></span>](#named-snippet)
* [<span data-ttu-id="8a69b-220">Выделение выбранных строк</span><span class="sxs-lookup"><span data-stu-id="8a69b-220">Highlight selected lines</span></span>](#highlighting-selected-lines)

<span data-ttu-id="8a69b-221">Дополнительные сведения см. в разделе [Ссылки на синтаксис фрагментов кода](#snippet-syntax-reference) далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="8a69b-221">For more information, see [Snippet syntax reference](#snippet-syntax-reference) later in this article.</span></span>

### <a name="path-to-code-file"></a><span data-ttu-id="8a69b-222">Путь к файлу кода</span><span class="sxs-lookup"><span data-stu-id="8a69b-222">Path to code file</span></span>

<span data-ttu-id="8a69b-223">Пример.</span><span class="sxs-lookup"><span data-stu-id="8a69b-223">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="8a69b-224">Пример взят из репозитория документов ASP.NET, файла статьи [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md).</span><span class="sxs-lookup"><span data-stu-id="8a69b-224">The example is from the ASP.NET docs repo, [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) article file.</span></span> <span data-ttu-id="8a69b-225">Для ссылки на файл кода используется относительный путь к [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) в том же репозитории.</span><span class="sxs-lookup"><span data-stu-id="8a69b-225">The code file is referenced by a relative path to [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) in the same repository.</span></span>

### <a name="selected-line-numbers"></a><span data-ttu-id="8a69b-226">Выбранные номера строк</span><span class="sxs-lookup"><span data-stu-id="8a69b-226">Selected line numbers</span></span>

<span data-ttu-id="8a69b-227">Пример.</span><span class="sxs-lookup"><span data-stu-id="8a69b-227">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="8a69b-228">В этом примере отображаются только строки 2–24 и 26 из файла кода *StudentController.cs*.</span><span class="sxs-lookup"><span data-stu-id="8a69b-228">This example displays only lines 2-24 and 26 of the *StudentController.cs* code file.</span></span>

<span data-ttu-id="8a69b-229">Предпочтительнее использовать именованные фрагменты кода, а не жестко заданные номера строк, как описано в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="8a69b-229">Prefer named snippets over hard-coded line numbers, as explained in the next section.</span></span>

### <a name="named-snippet"></a><span data-ttu-id="8a69b-230">Именованный фрагмент кода</span><span class="sxs-lookup"><span data-stu-id="8a69b-230">Named snippet</span></span>

<span data-ttu-id="8a69b-231">Пример.</span><span class="sxs-lookup"><span data-stu-id="8a69b-231">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

<span data-ttu-id="8a69b-232">Используйте для имени только буквы и символы подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="8a69b-232">Use only letters and underscores for the name.</span></span>

<span data-ttu-id="8a69b-233">В примере отображается раздел `snippet_Create` файла кода.</span><span class="sxs-lookup"><span data-stu-id="8a69b-233">The example displays the `snippet_Create` section of the code file.</span></span> <span data-ttu-id="8a69b-234">Файл кода для этого примера содержит теги фрагментов в комментариях в коде C#:</span><span class="sxs-lookup"><span data-stu-id="8a69b-234">The code file for this example has snippet tags in comments in the C# code:</span></span>

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

<span data-ttu-id="8a69b-235">По возможности ссылайтесь на именованный раздел, а не указывайте номера строк.</span><span class="sxs-lookup"><span data-stu-id="8a69b-235">Whenever you can, refer to a named section rather than specifying line numbers.</span></span> <span data-ttu-id="8a69b-236">Ссылки на номера строк являются ненадежными, так как файлы кода неизбежно изменяются с помощью способов, которые изменяют номера строк.</span><span class="sxs-lookup"><span data-stu-id="8a69b-236">Line number references are brittle because code files inevitably change in ways that make line numbers change.</span></span>
<span data-ttu-id="8a69b-237">Вы не обязательно получите уведомления об этих изменениях.</span><span class="sxs-lookup"><span data-stu-id="8a69b-237">You don't necessarily get notified of such changes.</span></span> <span data-ttu-id="8a69b-238">В статье в конечном итоге будут отображаться неправильные строки, и вы даже не будете об этом знать.</span><span class="sxs-lookup"><span data-stu-id="8a69b-238">Your article eventually starts showing the wrong lines and you have no clue anything has changed.</span></span>

### <a name="highlighting-selected-lines"></a><span data-ttu-id="8a69b-239">Выделение выбранных строк</span><span class="sxs-lookup"><span data-stu-id="8a69b-239">Highlighting selected lines</span></span>

<span data-ttu-id="8a69b-240">Пример.</span><span class="sxs-lookup"><span data-stu-id="8a69b-240">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

<span data-ttu-id="8a69b-241">В примере выделены строки 2 и 5, если считать от начала отображаемого фрагмента кода.</span><span class="sxs-lookup"><span data-stu-id="8a69b-241">The example highlights lines 2 and 5, counting from the start of the displayed snippet.</span></span> <span data-ttu-id="8a69b-242">Подсчет выделяемых номеров строк не начинается от начала файла кода.</span><span class="sxs-lookup"><span data-stu-id="8a69b-242">Line numbers to highlight don't count from the start of the code file.</span></span> <span data-ttu-id="8a69b-243">Другими словами, выделяются строки 3 и 6 файла кода.</span><span class="sxs-lookup"><span data-stu-id="8a69b-243">In other words, lines 3 and 6 of the code file are highlighted.</span></span>

## <a name="out-of-repo-snippet-references"></a><span data-ttu-id="8a69b-244">Ссылки на фрагменты кода в другом репозитории</span><span class="sxs-lookup"><span data-stu-id="8a69b-244">Out-of-repo snippet references</span></span>

<span data-ttu-id="8a69b-245">Если файл кода, на который необходимо сослаться, находится в другом репозитории, необходимо настроить репозиторий кода в качестве *зависимого репозитория*.</span><span class="sxs-lookup"><span data-stu-id="8a69b-245">If the code file you want to reference is in a different repository, set up the code repository as a *dependent repository*.</span></span> <span data-ttu-id="8a69b-246">При этом нужно указать его имя.</span><span class="sxs-lookup"><span data-stu-id="8a69b-246">When you do that, you specify a name for it.</span></span> <span data-ttu-id="8a69b-247">Это имя затем выступает в качестве имени папки, используемого для ссылки на код.</span><span class="sxs-lookup"><span data-stu-id="8a69b-247">That name then acts like a folder name for purposes of code references.</span></span>

<span data-ttu-id="8a69b-248">Например, репозиторий документов — *Azure/azure-docs*, а репозиторий кода — *Azure/azure-functions-durable-extension*.</span><span class="sxs-lookup"><span data-stu-id="8a69b-248">For example, the docs repository is *Azure/azure-docs*, and the code repository is *Azure/azure-functions-durable-extension*.</span></span>

<span data-ttu-id="8a69b-249">В корневой папке *azure-docs* добавьте следующий раздел в *.openpublishing.publish.config.json*:</span><span class="sxs-lookup"><span data-stu-id="8a69b-249">In the root folder of *azure-docs*, add the following section in *.openpublishing.publish.config.json*:</span></span>

```json
    {
      "path_to_root": "samples-durable-functions",
      "url": "https://github.com/Azure/azure-functions-durable-extension",
      "branch": "master",
      "branch_mapping": {}
    },
```

<span data-ttu-id="8a69b-250">Теперь при добавлении ссылки на *sample-durable-functions*, как если бы это была папка в *azure-docs*, вы на самом деле ссылаетесь на корневую папку в репозитории *azure-functions-durable-extension*.</span><span class="sxs-lookup"><span data-stu-id="8a69b-250">Now when you refer to *samples-durable-functions* as if it were a folder in *azure-docs*, you're actually referring to the root folder in the *azure-functions-durable-extension* repository.</span></span>

<span data-ttu-id="8a69b-251">Код можно включить с помощью тройного двоеточия (:\:\:) вручную или в Visual Studio Code с помощью пакета [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span><span class="sxs-lookup"><span data-stu-id="8a69b-251">You can include code by using the triple colon format (:\:\:) either manually or in Visual Studio Code with the help of the [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span></span>

1. <span data-ttu-id="8a69b-252">Находясь в Visual Studio Code, нажмите клавиши <kbd>ALT+M</kbd> или <kbd>OPTION+M</kbd> и выберите "Фрагмент кода".</span><span class="sxs-lookup"><span data-stu-id="8a69b-252">In Visual Studio Code, click <kbd>Alt + M</kbd> or <kbd>Option + M</kbd> and select Snippet.</span></span>
2. <span data-ttu-id="8a69b-253">Вам будет предложено выполнить поиск по всему содержимому, в какой-то области или по различным репозиториям.</span><span class="sxs-lookup"><span data-stu-id="8a69b-253">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="8a69b-254">Выберите поиск по репозиториям.</span><span class="sxs-lookup"><span data-stu-id="8a69b-254">To search across repositories, select Cross-Repository Reference.</span></span>
3. <span data-ttu-id="8a69b-255">Вам будет представлен набор репозиториев из *.openpublishing.publish.config.json*.</span><span class="sxs-lookup"><span data-stu-id="8a69b-255">You will be given a selection of repositories that are in *.openpublishing.publish.config.json*.</span></span> <span data-ttu-id="8a69b-256">Выберите репозиторий.</span><span class="sxs-lookup"><span data-stu-id="8a69b-256">Select a repository.</span></span>
4. <span data-ttu-id="8a69b-257">Введите условие поиска и найдите нужный файл.</span><span class="sxs-lookup"><span data-stu-id="8a69b-257">Enter a search term to find the file.</span></span> <span data-ttu-id="8a69b-258">Найдя файл, выберите его.</span><span class="sxs-lookup"><span data-stu-id="8a69b-258">Once you've found the file, select the file.</span></span>
5. <span data-ttu-id="8a69b-259">Затем выберите, какие строки кода нужно включить в фрагмент, используя</span><span class="sxs-lookup"><span data-stu-id="8a69b-259">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="8a69b-260">следующие параметры: **ИД**, **Диапазон** или **Никакие**.</span><span class="sxs-lookup"><span data-stu-id="8a69b-260">The options are: **ID**, **Range** and **None**.</span></span>
6. <span data-ttu-id="8a69b-261">В зависимости от выбора на шаге 5 предоставьте значение.</span><span class="sxs-lookup"><span data-stu-id="8a69b-261">Based on your selection from Step 5, provide a value.</span></span>

<span data-ttu-id="8a69b-262">Ссылка на фрагмент кода будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8a69b-262">Your snippet reference will look like this:</span></span>

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

<span data-ttu-id="8a69b-263">В репозитории *azure-functions-durable-extension* этот файл кода находится в папке *samples/csx/shared*.</span><span class="sxs-lookup"><span data-stu-id="8a69b-263">In the *azure-functions-durable-extension* repository, that code file is in the *samples/csx/shared* folder.</span></span> <span data-ttu-id="8a69b-264">Как отмечалось [ранее](#highlighting-selected-lines), номера строк для выделения начинаются от начала фрагмента, а не от начала файла.</span><span class="sxs-lookup"><span data-stu-id="8a69b-264">As noted [earlier](#highlighting-selected-lines), line numbers for highlighting are relative to the start of the snippet rather than the start of the file.</span></span>

> [!NOTE]
> <span data-ttu-id="8a69b-265">Имя, назначаемое зависимому репозиторию, указывается относительно корня основного репозитория, но тильда (~) относится к корню набора документов.</span><span class="sxs-lookup"><span data-stu-id="8a69b-265">The name you assign to the dependent repository is relative to the root of the main repository, but the tilde (~) refers to the root of the doc set.</span></span> <span data-ttu-id="8a69b-266">Корень набора документов определяется `build_source_folder` в *.openpublishing.publish.config.json*.</span><span class="sxs-lookup"><span data-stu-id="8a69b-266">The doc set root is determined by `build_source_folder` in *.openpublishing.publish.config.json*.</span></span> <span data-ttu-id="8a69b-267">Путь к фрагменту кода в предыдущем примере работает в репозитории azure-docs, так как `build_source_folder` относится к корню репозитория (`.`).</span><span class="sxs-lookup"><span data-stu-id="8a69b-267">The path to the snippet in the preceding example works in the azure-docs repo because `build_source_folder` refers to the repo root (`.`).</span></span> <span data-ttu-id="8a69b-268">Если бы в качестве `build_source_folder` использовалось `articles`, путь начинался бы с `~/../samples-durable-functions`, а не с `~/samples-durable-functions`.</span><span class="sxs-lookup"><span data-stu-id="8a69b-268">If `build_source_folder` were `articles`, the path would start with `~/../samples-durable-functions` instead of `~/samples-durable-functions`.</span></span>

## <a name="interactive-code-snippets"></a><span data-ttu-id="8a69b-269">Интерактивные фрагменты кода</span><span class="sxs-lookup"><span data-stu-id="8a69b-269">Interactive code snippets</span></span>

### <a name="inline-interactive-code-blocks"></a><span data-ttu-id="8a69b-270">Встроенные блоки интерактивного кода</span><span class="sxs-lookup"><span data-stu-id="8a69b-270">Inline interactive code blocks</span></span>

<span data-ttu-id="8a69b-271">Для следующих языков фрагменты кода можно сделать исполняемыми в окне браузера:</span><span class="sxs-lookup"><span data-stu-id="8a69b-271">For the following languages, code snippets can be made executable in the browser window:</span></span>

* <span data-ttu-id="8a69b-272">Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="8a69b-272">Azure Cloud Shell</span></span>
* <span data-ttu-id="8a69b-273">Azure PowerShell Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="8a69b-273">Azure PowerShell Cloud Shell</span></span>
* <span data-ttu-id="8a69b-274">C# REPL</span><span class="sxs-lookup"><span data-stu-id="8a69b-274">C# REPL</span></span>

<span data-ttu-id="8a69b-275">Если включен интерактивный режим, в отображаемых полях с кодом будут кнопки **Попробовать** или **Запустить**.</span><span class="sxs-lookup"><span data-stu-id="8a69b-275">When interactive mode is enabled, the rendered code boxes have a **Try It** or **Run** button.</span></span> <span data-ttu-id="8a69b-276">Например:</span><span class="sxs-lookup"><span data-stu-id="8a69b-276">For example:</span></span>

```markdown
    ```azurepowershell-interactive
    New-AzResourceGroup -Name myResourceGroup -Location westeurope
    ```
```

<span data-ttu-id="8a69b-277">отображается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8a69b-277">renders as follows:</span></span>

```azurepowershell-interactive
New-AzResourceGroup -Name myResourceGroup -Location westeurope
```

<span data-ttu-id="8a69b-278">Чтобы включить эту функцию для конкретного блока кода, используйте специальный идентификатор языка.</span><span class="sxs-lookup"><span data-stu-id="8a69b-278">To turn on this feature for a particular code block, use a special language identifier.</span></span> <span data-ttu-id="8a69b-279">Доступны следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="8a69b-279">The available options are:</span></span>

* <span data-ttu-id="8a69b-280">`azurepowershell-interactive` — активирует Cloud Shell в Azure PowerShell, как в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="8a69b-280">`azurepowershell-interactive` - Enables the Azure PowerShell Cloud Shell, as in the preceding example</span></span>
* <span data-ttu-id="8a69b-281">`azurecli-interactive` — включает Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="8a69b-281">`azurecli-interactive` - Enables the Azure Cloud Shell</span></span>
* <span data-ttu-id="8a69b-282">`csharp-interactive` — включает C# REPL</span><span class="sxs-lookup"><span data-stu-id="8a69b-282">`csharp-interactive` - Enables the C# REPL</span></span>

<span data-ttu-id="8a69b-283">В Azure Cloud Shell и PowerShell Cloud Shell пользователи могут выполнять команды только с собственной учетной записью Azure.</span><span class="sxs-lookup"><span data-stu-id="8a69b-283">For the Azure Cloud Shell and PowerShell Cloud Shell, users can run commands against only their own Azure account.</span></span>

### <a name="code-snippets-included-by-reference"></a><span data-ttu-id="8a69b-284">Фрагменты кода, включаемые по ссылке</span><span class="sxs-lookup"><span data-stu-id="8a69b-284">Code snippets included by reference</span></span>

<span data-ttu-id="8a69b-285">Для фрагментов кода, включаемых по ссылке, можно включить интерактивный режим.</span><span class="sxs-lookup"><span data-stu-id="8a69b-285">You can enable interactive mode for code snippets included by reference.</span></span> <span data-ttu-id="8a69b-286">Ниже приведены примеры:</span><span class="sxs-lookup"><span data-stu-id="8a69b-286">Here are examples:</span></span>

```markdown
:::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code source="Bash.sh" interactive="cloudshell-bash":::
```

<span data-ttu-id="8a69b-287">Чтобы включить эту функцию для конкретного блока кода, используйте атрибут `interactive`.</span><span class="sxs-lookup"><span data-stu-id="8a69b-287">To turn on this feature for a particular code block, use the `interactive` attribute.</span></span> <span data-ttu-id="8a69b-288">Допустимые значения атрибута:</span><span class="sxs-lookup"><span data-stu-id="8a69b-288">The available attribute values are:</span></span>

* <span data-ttu-id="8a69b-289">`cloudshell-powershell` — активирует Cloud Shell в Azure PowerShell, как в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="8a69b-289">`cloudshell-powershell` - Enables the Azure PowerShell Cloud Shell, as in the preceding example</span></span>
* <span data-ttu-id="8a69b-290">`cloudshell-bash` — включает Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="8a69b-290">`cloudshell-bash` - Enables the Azure Cloud Shell</span></span>
* <span data-ttu-id="8a69b-291">`try-dotnet` — активирует Try .NET.</span><span class="sxs-lookup"><span data-stu-id="8a69b-291">`try-dotnet` - Enables Try .NET</span></span>
* <span data-ttu-id="8a69b-292">`try-dotnet-class` — активирует Try .NET с формированием шаблонов классов.</span><span class="sxs-lookup"><span data-stu-id="8a69b-292">`try-dotnet-class` - Enables Try .NET with class scaffolding</span></span>
* <span data-ttu-id="8a69b-293">`try-dotnet-method` — активирует Try .NET с формированием шаблонов методов.</span><span class="sxs-lookup"><span data-stu-id="8a69b-293">`try-dotnet-method` - Enables Try .NET with method scaffolding</span></span>

<span data-ttu-id="8a69b-294">В Azure Cloud Shell и PowerShell Cloud Shell пользователи могут выполнять команды только с собственной учетной записью Azure.</span><span class="sxs-lookup"><span data-stu-id="8a69b-294">For the Azure Cloud Shell and PowerShell Cloud Shell, users can only run commands against their own Azure account.</span></span>

## <a name="snippet-syntax-reference"></a><span data-ttu-id="8a69b-295">Синтаксис ссылок на фрагменты</span><span class="sxs-lookup"><span data-stu-id="8a69b-295">Snippet syntax reference</span></span>

<span data-ttu-id="8a69b-296">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a69b-296">Syntax:</span></span>

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> <span data-ttu-id="8a69b-297">Этот синтаксис является блоком расширения Markdown.</span><span class="sxs-lookup"><span data-stu-id="8a69b-297">This syntax is a block Markdown extension.</span></span> <span data-ttu-id="8a69b-298">Он должен использоваться в отдельной строке.</span><span class="sxs-lookup"><span data-stu-id="8a69b-298">It must be used on its own line.</span></span>

* <span data-ttu-id="8a69b-299">`<language>` (*необязательно*)</span><span class="sxs-lookup"><span data-stu-id="8a69b-299">`<language>` (*optional*)</span></span>
  * <span data-ttu-id="8a69b-300">Язык фрагмента кода.</span><span class="sxs-lookup"><span data-stu-id="8a69b-300">Language of the code snippet.</span></span> <span data-ttu-id="8a69b-301">Дополнительные сведения см. в разделе [Поддерживаемые языки](#supported-languages) далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="8a69b-301">For more information, see the [Supported languages](#supported-languages) section later in this article.</span></span>

* <span data-ttu-id="8a69b-302">`<path>` (*обязательно*)</span><span class="sxs-lookup"><span data-stu-id="8a69b-302">`<path>` (*mandatory*)</span></span>
  * <span data-ttu-id="8a69b-303">Относительный путь в файловой системе, который указывает файл фрагмента кода для ссылки.</span><span class="sxs-lookup"><span data-stu-id="8a69b-303">Relative path in the file system that indicates the code snippet file to reference.</span></span>

* <span data-ttu-id="8a69b-304">`<attribute>` и `<attribute-value>` (*необязательно*)</span><span class="sxs-lookup"><span data-stu-id="8a69b-304">`<attribute>` and `<attribute-value>` (*optional*)</span></span>
  * <span data-ttu-id="8a69b-305">Используются вместе для указания способа получения кода из файла и его отображения:</span><span class="sxs-lookup"><span data-stu-id="8a69b-305">Used together to specify how the code should be retrieved from the file and how it should be displayed:</span></span>
    * <span data-ttu-id="8a69b-306">`range`: `1,3-5` Диапазон строк.</span><span class="sxs-lookup"><span data-stu-id="8a69b-306">`range`: `1,3-5` A range of lines.</span></span> <span data-ttu-id="8a69b-307">Этот пример содержит строки 1, 3, 4 и 5.</span><span class="sxs-lookup"><span data-stu-id="8a69b-307">This example includes lines 1, 3, 4, and 5.</span></span>
    * <span data-ttu-id="8a69b-308">`id`: `snippet_Create` Идентификатор фрагмента, который нужно вставить из файла кода.</span><span class="sxs-lookup"><span data-stu-id="8a69b-308">`id`: `snippet_Create` The ID of the snippet that needs to be inserted from the code file.</span></span> <span data-ttu-id="8a69b-309">Это значение не может существовать одновременно с диапазоном.</span><span class="sxs-lookup"><span data-stu-id="8a69b-309">This value cannot co-exist with range.</span></span>
    * <span data-ttu-id="8a69b-310">`highlight`: `2-4,6` Диапазон и (или) номера строк, которые должны выделяться в создаваемом фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="8a69b-310">`highlight`: `2-4,6` Range and/or numbers of lines that need to be highlighted in the generated code snippet.</span></span> <span data-ttu-id="8a69b-311">Нумерация задается относительно отображаемых строк (в соответствии с диапазоном или идентификатором), а не файла.</span><span class="sxs-lookup"><span data-stu-id="8a69b-311">The numbering is relative to the lines displayed (as specified by range or id), not the file.</span></span>
    * <span data-ttu-id="8a69b-312">`interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` Строковое значение, определяющее тип используемой интерактивности.</span><span class="sxs-lookup"><span data-stu-id="8a69b-312">`interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` String value determines what kinds of interactivity are enabled.</span></span>
    * <span data-ttu-id="8a69b-313">Сведения о представлении имени тега в исходных файлах фрагмента кода для каждого языка см. в разделе с [рекомендациями по DocFX](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span><span class="sxs-lookup"><span data-stu-id="8a69b-313">For details about tag name representation in code snippet source files by language, see the [DocFX guidelines](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="8a69b-314">Поддерживаемые языки</span><span class="sxs-lookup"><span data-stu-id="8a69b-314">Supported languages</span></span>

<span data-ttu-id="8a69b-315">Пакет [Docs Authoring Pack](how-to-write-docs-auth-pack.md) содержит функцию, обеспечивающую завершение операторов и проверку доступных идентификаторов языков для блоков границ кода.</span><span class="sxs-lookup"><span data-stu-id="8a69b-315">The [Docs Authoring Pack](how-to-write-docs-auth-pack.md) includes a feature to provide statement completion and validation of the available language identifiers for code fence blocks.</span></span>

### <a name="fenced-code-blocks"></a><span data-ttu-id="8a69b-316">Огороженные блоки кода</span><span class="sxs-lookup"><span data-stu-id="8a69b-316">Fenced code blocks</span></span>

| <span data-ttu-id="8a69b-317">Имя</span><span class="sxs-lookup"><span data-stu-id="8a69b-317">Name</span></span>                           | <span data-ttu-id="8a69b-318">Допустимые псевдонимы</span><span class="sxs-lookup"><span data-stu-id="8a69b-318">Valid aliases</span></span>                                                                  |
|--------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="8a69b-319">.NET Core CLI</span><span class="sxs-lookup"><span data-stu-id="8a69b-319">.NET Core CLI</span></span>                  | `dotnetcli`                                                                    |
| <span data-ttu-id="8a69b-320">1C</span><span class="sxs-lookup"><span data-stu-id="8a69b-320">1C</span></span>                             | `1c`                                                                           |
| <span data-ttu-id="8a69b-321">ABNF</span><span class="sxs-lookup"><span data-stu-id="8a69b-321">ABNF</span></span>                           | `abnf`                                                                         |
| <span data-ttu-id="8a69b-322">Журналы доступа</span><span class="sxs-lookup"><span data-stu-id="8a69b-322">Access logs</span></span>                    | `accesslog`                                                                    |
| <span data-ttu-id="8a69b-323">Ada</span><span class="sxs-lookup"><span data-stu-id="8a69b-323">Ada</span></span>                            | `ada`                                                                          |
| <span data-ttu-id="8a69b-324">Ассемблер ARM</span><span class="sxs-lookup"><span data-stu-id="8a69b-324">ARM assembler</span></span>                  | <span data-ttu-id="8a69b-325">`armasm`, `arm`</span><span class="sxs-lookup"><span data-stu-id="8a69b-325">`armasm`, `arm`</span></span>                                                                |
| <span data-ttu-id="8a69b-326">Ассемблер AVR</span><span class="sxs-lookup"><span data-stu-id="8a69b-326">AVR assembler</span></span>                  | `avrasm`                                                                       |
| <span data-ttu-id="8a69b-327">ActionScript</span><span class="sxs-lookup"><span data-stu-id="8a69b-327">ActionScript</span></span>                   | <span data-ttu-id="8a69b-328">`actionscript`, `as`</span><span class="sxs-lookup"><span data-stu-id="8a69b-328">`actionscript`, `as`</span></span>                                                           |
| <span data-ttu-id="8a69b-329">Alan</span><span class="sxs-lookup"><span data-stu-id="8a69b-329">Alan</span></span>                           | <span data-ttu-id="8a69b-330">`alan`, `i`</span><span class="sxs-lookup"><span data-stu-id="8a69b-330">`alan`, `i`</span></span>                                                                    |
| <span data-ttu-id="8a69b-331">AngelScript</span><span class="sxs-lookup"><span data-stu-id="8a69b-331">AngelScript</span></span>                    | <span data-ttu-id="8a69b-332">`angelscript`, `asc`</span><span class="sxs-lookup"><span data-stu-id="8a69b-332">`angelscript`, `asc`</span></span>                                                           |
| <span data-ttu-id="8a69b-333">ANTLR</span><span class="sxs-lookup"><span data-stu-id="8a69b-333">ANTLR</span></span>                          | `antlr`                                                                        |
| <span data-ttu-id="8a69b-334">Apache</span><span class="sxs-lookup"><span data-stu-id="8a69b-334">Apache</span></span>                         | <span data-ttu-id="8a69b-335">`apache`, `apacheconf`</span><span class="sxs-lookup"><span data-stu-id="8a69b-335">`apache`, `apacheconf`</span></span>                                                         |
| <span data-ttu-id="8a69b-336">AppleScript</span><span class="sxs-lookup"><span data-stu-id="8a69b-336">AppleScript</span></span>                    | <span data-ttu-id="8a69b-337">`applescript`, `osascript`</span><span class="sxs-lookup"><span data-stu-id="8a69b-337">`applescript`, `osascript`</span></span>                                                     |
| <span data-ttu-id="8a69b-338">Arcade</span><span class="sxs-lookup"><span data-stu-id="8a69b-338">Arcade</span></span>                         | `arcade`                                                                       |
| <span data-ttu-id="8a69b-339">AsciiDoc</span><span class="sxs-lookup"><span data-stu-id="8a69b-339">AsciiDoc</span></span>                       | <span data-ttu-id="8a69b-340">`asciidoc`, `adoc`</span><span class="sxs-lookup"><span data-stu-id="8a69b-340">`asciidoc`, `adoc`</span></span>                                                             |
| <span data-ttu-id="8a69b-341">AspectJ</span><span class="sxs-lookup"><span data-stu-id="8a69b-341">AspectJ</span></span>                        | `aspectj`                                                                      |
| <span data-ttu-id="8a69b-342">ASPX</span><span class="sxs-lookup"><span data-stu-id="8a69b-342">ASPX</span></span>                           | `aspx`                                                                         |
| <span data-ttu-id="8a69b-343">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="8a69b-343">ASP.NET (C#)</span></span>                   | `aspx-csharp`                                                                  |
| <span data-ttu-id="8a69b-344">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="8a69b-344">ASP.NET (VB)</span></span>                   | `aspx-vb`                                                                      |
| <span data-ttu-id="8a69b-345">AutoHotkey</span><span class="sxs-lookup"><span data-stu-id="8a69b-345">AutoHotkey</span></span>                     | `autohotkey`                                                                   |
| <span data-ttu-id="8a69b-346">AutoIt</span><span class="sxs-lookup"><span data-stu-id="8a69b-346">AutoIt</span></span>                         | `autoit`                                                                       |
| <span data-ttu-id="8a69b-347">Awk</span><span class="sxs-lookup"><span data-stu-id="8a69b-347">Awk</span></span>                            | <span data-ttu-id="8a69b-348">`awk`, `mawk`, `nawk`, `gawk`</span><span class="sxs-lookup"><span data-stu-id="8a69b-348">`awk`, `mawk`, `nawk`, `gawk`</span></span>                                                  |
| <span data-ttu-id="8a69b-349">Axapta</span><span class="sxs-lookup"><span data-stu-id="8a69b-349">Axapta</span></span>                         | `axapta`                                                                       |
| <span data-ttu-id="8a69b-350">AzCopy</span><span class="sxs-lookup"><span data-stu-id="8a69b-350">AzCopy</span></span>                         | `azcopy`                                                                       |
| <span data-ttu-id="8a69b-351">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="8a69b-351">Azure CLI</span></span>                      | `azurecli`                                                                     |
| <span data-ttu-id="8a69b-352">Azure CLI (интерактивный)</span><span class="sxs-lookup"><span data-stu-id="8a69b-352">Azure CLI (Interactive)</span></span>        | `azurecli-interactive`                                                         |
| <span data-ttu-id="8a69b-353">Azure Powershell</span><span class="sxs-lookup"><span data-stu-id="8a69b-353">Azure Powershell</span></span>               | `azurepowershell`                                                              |
| <span data-ttu-id="8a69b-354">Azure Powershell (интерактивный)</span><span class="sxs-lookup"><span data-stu-id="8a69b-354">Azure Powershell (Interactive)</span></span> | `azurepowershell-interactive`                                                  |
| <span data-ttu-id="8a69b-355">Bash</span><span class="sxs-lookup"><span data-stu-id="8a69b-355">Bash</span></span>                           | <span data-ttu-id="8a69b-356">`bash`, `sh`, `zsh`</span><span class="sxs-lookup"><span data-stu-id="8a69b-356">`bash`, `sh`, `zsh`</span></span>                                                            |
| <span data-ttu-id="8a69b-357">Basic</span><span class="sxs-lookup"><span data-stu-id="8a69b-357">Basic</span></span>                          | `basic`                                                                        |
| <span data-ttu-id="8a69b-358">BNF</span><span class="sxs-lookup"><span data-stu-id="8a69b-358">BNF</span></span>                            | `bnf`                                                                          |
| <span data-ttu-id="8a69b-359">C</span><span class="sxs-lookup"><span data-stu-id="8a69b-359">C</span></span>                              | `c`                                                                            |
| <span data-ttu-id="8a69b-360">C#</span><span class="sxs-lookup"><span data-stu-id="8a69b-360">C#</span></span>                             | <span data-ttu-id="8a69b-361">`csharp`, `cs`</span><span class="sxs-lookup"><span data-stu-id="8a69b-361">`csharp`, `cs`</span></span>                                                                 |
| <span data-ttu-id="8a69b-362">C# (интерактивный)</span><span class="sxs-lookup"><span data-stu-id="8a69b-362">C# (Interactive)</span></span>               | `csharp-interactive`                                                           |
| <span data-ttu-id="8a69b-363">C++</span><span class="sxs-lookup"><span data-stu-id="8a69b-363">C++</span></span>                            | <span data-ttu-id="8a69b-364">`cpp`, `c`, `cc`, `h`, `c++`, `h++`, `hpp`</span><span class="sxs-lookup"><span data-stu-id="8a69b-364">`cpp`, `c`, `cc`, `h`, `c++`, `h++`, `hpp`</span></span>                                     |
| <span data-ttu-id="8a69b-365">C++/CX</span><span class="sxs-lookup"><span data-stu-id="8a69b-365">C++/CX</span></span>                         | `cppcx`                                                                        |
| <span data-ttu-id="8a69b-366">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="8a69b-366">C++/WinRT</span></span>                      | `cppwinrt`                                                                     |
| <span data-ttu-id="8a69b-367">C/AL</span><span class="sxs-lookup"><span data-stu-id="8a69b-367">C/AL</span></span>                           | `cal`                                                                          |
| <span data-ttu-id="8a69b-368">Cache Object Script</span><span class="sxs-lookup"><span data-stu-id="8a69b-368">Cache Object Script</span></span>            | <span data-ttu-id="8a69b-369">`cos`, `cls`</span><span class="sxs-lookup"><span data-stu-id="8a69b-369">`cos`, `cls`</span></span>                                                                   |
| <span data-ttu-id="8a69b-370">CMake</span><span class="sxs-lookup"><span data-stu-id="8a69b-370">CMake</span></span>                          | <span data-ttu-id="8a69b-371">`cmake`, `cmake.in`</span><span class="sxs-lookup"><span data-stu-id="8a69b-371">`cmake`, `cmake.in`</span></span>                                                            |
| <span data-ttu-id="8a69b-372">Coq</span><span class="sxs-lookup"><span data-stu-id="8a69b-372">Coq</span></span>                            | `coq`                                                                          |
| <span data-ttu-id="8a69b-373">CSP</span><span class="sxs-lookup"><span data-stu-id="8a69b-373">CSP</span></span>                            | `csp`                                                                          |
| <span data-ttu-id="8a69b-374">CSS</span><span class="sxs-lookup"><span data-stu-id="8a69b-374">CSS</span></span>                            | `css`                                                                          |
| <span data-ttu-id="8a69b-375">Cap'n Proto</span><span class="sxs-lookup"><span data-stu-id="8a69b-375">Cap'n Proto</span></span>                    | <span data-ttu-id="8a69b-376">`capnproto`, `capnp`</span><span class="sxs-lookup"><span data-stu-id="8a69b-376">`capnproto`, `capnp`</span></span>                                                           |
| <span data-ttu-id="8a69b-377">Clojure</span><span class="sxs-lookup"><span data-stu-id="8a69b-377">Clojure</span></span>                        | <span data-ttu-id="8a69b-378">`clojure`, `clj`</span><span class="sxs-lookup"><span data-stu-id="8a69b-378">`clojure`, `clj`</span></span>                                                               |
| <span data-ttu-id="8a69b-379">CoffeeScript</span><span class="sxs-lookup"><span data-stu-id="8a69b-379">CoffeeScript</span></span>                   | <span data-ttu-id="8a69b-380">`coffeescript`, `coffee`, `cson`, `iced`</span><span class="sxs-lookup"><span data-stu-id="8a69b-380">`coffeescript`, `coffee`, `cson`, `iced`</span></span>                                       |
| <span data-ttu-id="8a69b-381">Crmsh</span><span class="sxs-lookup"><span data-stu-id="8a69b-381">Crmsh</span></span>                          | <span data-ttu-id="8a69b-382">`crmsh`, `crm`, `pcmk`</span><span class="sxs-lookup"><span data-stu-id="8a69b-382">`crmsh`, `crm`, `pcmk`</span></span>                                                         |
| <span data-ttu-id="8a69b-383">Crystal</span><span class="sxs-lookup"><span data-stu-id="8a69b-383">Crystal</span></span>                        | <span data-ttu-id="8a69b-384">`crystal`, `cr`</span><span class="sxs-lookup"><span data-stu-id="8a69b-384">`crystal`, `cr`</span></span>                                                                |
| <span data-ttu-id="8a69b-385">Cypher (Neo4j)</span><span class="sxs-lookup"><span data-stu-id="8a69b-385">Cypher (Neo4j)</span></span>                 | `cypher`                                                                       |
| <span data-ttu-id="8a69b-386">D</span><span class="sxs-lookup"><span data-stu-id="8a69b-386">D</span></span>                              | `d`                                                                            |
| <span data-ttu-id="8a69b-387">DAX Power BI</span><span class="sxs-lookup"><span data-stu-id="8a69b-387">DAX Power BI</span></span>                   | `dax`                                                                          |
| <span data-ttu-id="8a69b-388">Файл зоны DNS</span><span class="sxs-lookup"><span data-stu-id="8a69b-388">DNS Zone file</span></span>                  | <span data-ttu-id="8a69b-389">`dns`, `zone`, `bind`</span><span class="sxs-lookup"><span data-stu-id="8a69b-389">`dns`, `zone`, `bind`</span></span>                                                          |
| <span data-ttu-id="8a69b-390">DOS</span><span class="sxs-lookup"><span data-stu-id="8a69b-390">DOS</span></span>                            | <span data-ttu-id="8a69b-391">`dos`, `bat`, `cmd`</span><span class="sxs-lookup"><span data-stu-id="8a69b-391">`dos`, `bat`, `cmd`</span></span>                                                            |
| <span data-ttu-id="8a69b-392">Dart</span><span class="sxs-lookup"><span data-stu-id="8a69b-392">Dart</span></span>                           | `dart`                                                                         |
| <span data-ttu-id="8a69b-393">Delphi</span><span class="sxs-lookup"><span data-stu-id="8a69b-393">Delphi</span></span>                         | <span data-ttu-id="8a69b-394">`delphi`, `dpr`, `dfm`, `pas`, `pascal`, `freepascal`, `lazarus`, `lpr`, `lfm`</span><span class="sxs-lookup"><span data-stu-id="8a69b-394">`delphi`, `dpr`, `dfm`, `pas`, `pascal`, `freepascal`, `lazarus`, `lpr`, `lfm`</span></span> |
| <span data-ttu-id="8a69b-395">Diff</span><span class="sxs-lookup"><span data-stu-id="8a69b-395">Diff</span></span>                           | <span data-ttu-id="8a69b-396">`diff`, `patch`</span><span class="sxs-lookup"><span data-stu-id="8a69b-396">`diff`, `patch`</span></span>                                                                |
| <span data-ttu-id="8a69b-397">Django</span><span class="sxs-lookup"><span data-stu-id="8a69b-397">Django</span></span>                         | <span data-ttu-id="8a69b-398">`django`, `jinja`</span><span class="sxs-lookup"><span data-stu-id="8a69b-398">`django`, `jinja`</span></span>                                                              |
| <span data-ttu-id="8a69b-399">Dockerfile</span><span class="sxs-lookup"><span data-stu-id="8a69b-399">Dockerfile</span></span>                     | <span data-ttu-id="8a69b-400">`dockerfile`, `docker`</span><span class="sxs-lookup"><span data-stu-id="8a69b-400">`dockerfile`, `docker`</span></span>                                                         |
| <span data-ttu-id="8a69b-401">dsconfig</span><span class="sxs-lookup"><span data-stu-id="8a69b-401">dsconfig</span></span>                       | `dsconfig`                                                                     |
| <span data-ttu-id="8a69b-402">DTS (дерево устройств)</span><span class="sxs-lookup"><span data-stu-id="8a69b-402">DTS (Device Tree)</span></span>              | `dts`                                                                          |
| <span data-ttu-id="8a69b-403">Dust</span><span class="sxs-lookup"><span data-stu-id="8a69b-403">Dust</span></span>                           | <span data-ttu-id="8a69b-404">`dust`, `dst`</span><span class="sxs-lookup"><span data-stu-id="8a69b-404">`dust`, `dst`</span></span>                                                                  |
| <span data-ttu-id="8a69b-405">Dylan</span><span class="sxs-lookup"><span data-stu-id="8a69b-405">Dylan</span></span>                          | `dylan`                                                                        |
| <span data-ttu-id="8a69b-406">EBNF</span><span class="sxs-lookup"><span data-stu-id="8a69b-406">EBNF</span></span>                           | `ebnf`                                                                         |
| <span data-ttu-id="8a69b-407">Elixir</span><span class="sxs-lookup"><span data-stu-id="8a69b-407">Elixir</span></span>                         | `elixir`                                                                       |
| <span data-ttu-id="8a69b-408">Elm</span><span class="sxs-lookup"><span data-stu-id="8a69b-408">Elm</span></span>                            | `elm`                                                                          |
| <span data-ttu-id="8a69b-409">Erlang</span><span class="sxs-lookup"><span data-stu-id="8a69b-409">Erlang</span></span>                         | <span data-ttu-id="8a69b-410">`erlang`, `erl`</span><span class="sxs-lookup"><span data-stu-id="8a69b-410">`erlang`, `erl`</span></span>                                                                |
| <span data-ttu-id="8a69b-411">Excel</span><span class="sxs-lookup"><span data-stu-id="8a69b-411">Excel</span></span>                          | <span data-ttu-id="8a69b-412">`excel`, `xls`, `xlsx`</span><span class="sxs-lookup"><span data-stu-id="8a69b-412">`excel`, `xls`, `xlsx`</span></span>                                                         |
| <span data-ttu-id="8a69b-413">Extempore</span><span class="sxs-lookup"><span data-stu-id="8a69b-413">Extempore</span></span>                      | <span data-ttu-id="8a69b-414">`extempore`, `xtlang`, `xtm`</span><span class="sxs-lookup"><span data-stu-id="8a69b-414">`extempore`, `xtlang`, `xtm`</span></span>                                                   |
| <span data-ttu-id="8a69b-415">F#</span><span class="sxs-lookup"><span data-stu-id="8a69b-415">F#</span></span>                             | <span data-ttu-id="8a69b-416">`fsharp`, `fs`</span><span class="sxs-lookup"><span data-stu-id="8a69b-416">`fsharp`, `fs`</span></span>                                                                 |
| <span data-ttu-id="8a69b-417">FIX</span><span class="sxs-lookup"><span data-stu-id="8a69b-417">FIX</span></span>                            | `fix`                                                                          |
| <span data-ttu-id="8a69b-418">Fortran</span><span class="sxs-lookup"><span data-stu-id="8a69b-418">Fortran</span></span>                        | <span data-ttu-id="8a69b-419">`fortran`, `f90`, `f95`</span><span class="sxs-lookup"><span data-stu-id="8a69b-419">`fortran`, `f90`, `f95`</span></span>                                                        |
| <span data-ttu-id="8a69b-420">G-Code</span><span class="sxs-lookup"><span data-stu-id="8a69b-420">G-Code</span></span>                         | <span data-ttu-id="8a69b-421">`gcode`, `nc`</span><span class="sxs-lookup"><span data-stu-id="8a69b-421">`gcode`, `nc`</span></span>                                                                  |
| <span data-ttu-id="8a69b-422">Gams</span><span class="sxs-lookup"><span data-stu-id="8a69b-422">Gams</span></span>                           | <span data-ttu-id="8a69b-423">`gams`, `gms`</span><span class="sxs-lookup"><span data-stu-id="8a69b-423">`gams`, `gms`</span></span>                                                                  |
| <span data-ttu-id="8a69b-424">GAUSS</span><span class="sxs-lookup"><span data-stu-id="8a69b-424">GAUSS</span></span>                          | <span data-ttu-id="8a69b-425">`gauss`, `gss`</span><span class="sxs-lookup"><span data-stu-id="8a69b-425">`gauss`, `gss`</span></span>                                                                 |
| <span data-ttu-id="8a69b-426">GDScript</span><span class="sxs-lookup"><span data-stu-id="8a69b-426">GDScript</span></span>                       | <span data-ttu-id="8a69b-427">`godot`, `gdscript`</span><span class="sxs-lookup"><span data-stu-id="8a69b-427">`godot`, `gdscript`</span></span>                                                            |
| <span data-ttu-id="8a69b-428">Gherkin</span><span class="sxs-lookup"><span data-stu-id="8a69b-428">Gherkin</span></span>                        | `gherkin`                                                                      |
| <span data-ttu-id="8a69b-429">GN for Ninja</span><span class="sxs-lookup"><span data-stu-id="8a69b-429">GN for Ninja</span></span>                   | <span data-ttu-id="8a69b-430">`gn`, `gni`</span><span class="sxs-lookup"><span data-stu-id="8a69b-430">`gn`, `gni`</span></span>                                                                    |
| <span data-ttu-id="8a69b-431">Go</span><span class="sxs-lookup"><span data-stu-id="8a69b-431">Go</span></span>                             | <span data-ttu-id="8a69b-432">`go`, `golang`</span><span class="sxs-lookup"><span data-stu-id="8a69b-432">`go`, `golang`</span></span>                                                                 |
| <span data-ttu-id="8a69b-433">Golo</span><span class="sxs-lookup"><span data-stu-id="8a69b-433">Golo</span></span>                           | <span data-ttu-id="8a69b-434">`golo`, `gololang`</span><span class="sxs-lookup"><span data-stu-id="8a69b-434">`golo`, `gololang`</span></span>                                                             |
| <span data-ttu-id="8a69b-435">Gradle</span><span class="sxs-lookup"><span data-stu-id="8a69b-435">Gradle</span></span>                         | `gradle`                                                                       |
| <span data-ttu-id="8a69b-436">Groovy</span><span class="sxs-lookup"><span data-stu-id="8a69b-436">Groovy</span></span>                         | `groovy`                                                                       |
| <span data-ttu-id="8a69b-437">HTML</span><span class="sxs-lookup"><span data-stu-id="8a69b-437">HTML</span></span>                           | <span data-ttu-id="8a69b-438">`html`, `xhtml`</span><span class="sxs-lookup"><span data-stu-id="8a69b-438">`html`, `xhtml`</span></span>                                                                |
| <span data-ttu-id="8a69b-439">HTTP</span><span class="sxs-lookup"><span data-stu-id="8a69b-439">HTTP</span></span>                           | <span data-ttu-id="8a69b-440">`http`, `https`</span><span class="sxs-lookup"><span data-stu-id="8a69b-440">`http`, `https`</span></span>                                                                |
| <span data-ttu-id="8a69b-441">Haml</span><span class="sxs-lookup"><span data-stu-id="8a69b-441">Haml</span></span>                           | `haml`                                                                         |
| <span data-ttu-id="8a69b-442">Handlebars</span><span class="sxs-lookup"><span data-stu-id="8a69b-442">Handlebars</span></span>                     | <span data-ttu-id="8a69b-443">`handlebars`, `hbs`, `html.hbs`, `html.handlebars`</span><span class="sxs-lookup"><span data-stu-id="8a69b-443">`handlebars`, `hbs`, `html.hbs`, `html.handlebars`</span></span>                             |
| <span data-ttu-id="8a69b-444">Haskell</span><span class="sxs-lookup"><span data-stu-id="8a69b-444">Haskell</span></span>                        | <span data-ttu-id="8a69b-445">`haskell`, `hs`</span><span class="sxs-lookup"><span data-stu-id="8a69b-445">`haskell`, `hs`</span></span>                                                                |
| <span data-ttu-id="8a69b-446">Haxe</span><span class="sxs-lookup"><span data-stu-id="8a69b-446">Haxe</span></span>                           | <span data-ttu-id="8a69b-447">`haxe`, `hx`</span><span class="sxs-lookup"><span data-stu-id="8a69b-447">`haxe`, `hx`</span></span>                                                                   |
| <span data-ttu-id="8a69b-448">Hy</span><span class="sxs-lookup"><span data-stu-id="8a69b-448">Hy</span></span>                             | <span data-ttu-id="8a69b-449">`hy`, `hylang`</span><span class="sxs-lookup"><span data-stu-id="8a69b-449">`hy`, `hylang`</span></span>                                                                 |
| <span data-ttu-id="8a69b-450">Ini</span><span class="sxs-lookup"><span data-stu-id="8a69b-450">Ini</span></span>                            | `ini`                                                                          |
| <span data-ttu-id="8a69b-451">Inform7</span><span class="sxs-lookup"><span data-stu-id="8a69b-451">Inform7</span></span>                        | <span data-ttu-id="8a69b-452">`inform7`, `i7`</span><span class="sxs-lookup"><span data-stu-id="8a69b-452">`inform7`, `i7`</span></span>                                                                |
| <span data-ttu-id="8a69b-453">IRPF90</span><span class="sxs-lookup"><span data-stu-id="8a69b-453">IRPF90</span></span>                         | `irpf90`                                                                       |
| <span data-ttu-id="8a69b-454">JSON</span><span class="sxs-lookup"><span data-stu-id="8a69b-454">JSON</span></span>                           | `json`                                                                         |
| <span data-ttu-id="8a69b-455">Java</span><span class="sxs-lookup"><span data-stu-id="8a69b-455">Java</span></span>                           | <span data-ttu-id="8a69b-456">`java`, `jsp`</span><span class="sxs-lookup"><span data-stu-id="8a69b-456">`java`, `jsp`</span></span>                                                                  |
| <span data-ttu-id="8a69b-457">JavaScript</span><span class="sxs-lookup"><span data-stu-id="8a69b-457">JavaScript</span></span>                     | <span data-ttu-id="8a69b-458">`javascript`, `js`, `jsx`</span><span class="sxs-lookup"><span data-stu-id="8a69b-458">`javascript`, `js`, `jsx`</span></span>                                                      |
| <span data-ttu-id="8a69b-459">Kotlin</span><span class="sxs-lookup"><span data-stu-id="8a69b-459">Kotlin</span></span>                         | <span data-ttu-id="8a69b-460">`kotlin`, `kt`</span><span class="sxs-lookup"><span data-stu-id="8a69b-460">`kotlin`, `kt`</span></span>                                                                 |
| <span data-ttu-id="8a69b-461">Kusto</span><span class="sxs-lookup"><span data-stu-id="8a69b-461">Kusto</span></span>                          | `kusto`                                                                        |
| <span data-ttu-id="8a69b-462">Leaf</span><span class="sxs-lookup"><span data-stu-id="8a69b-462">Leaf</span></span>                           | `leaf`                                                                         |
| <span data-ttu-id="8a69b-463">Lasso</span><span class="sxs-lookup"><span data-stu-id="8a69b-463">Lasso</span></span>                          | <span data-ttu-id="8a69b-464">`lasso`, `ls`, `lassoscript`</span><span class="sxs-lookup"><span data-stu-id="8a69b-464">`lasso`, `ls`, `lassoscript`</span></span>                                                   |
| <span data-ttu-id="8a69b-465">Less</span><span class="sxs-lookup"><span data-stu-id="8a69b-465">Less</span></span>                           | `less`                                                                         |
| <span data-ttu-id="8a69b-466">LDIF</span><span class="sxs-lookup"><span data-stu-id="8a69b-466">LDIF</span></span>                           | `ldif`                                                                         |
| <span data-ttu-id="8a69b-467">Lisp</span><span class="sxs-lookup"><span data-stu-id="8a69b-467">Lisp</span></span>                           | `lisp`                                                                         |
| <span data-ttu-id="8a69b-468">LiveCode Server</span><span class="sxs-lookup"><span data-stu-id="8a69b-468">LiveCode Server</span></span>                | `livecodeserver`                                                               |
| <span data-ttu-id="8a69b-469">LiveScript</span><span class="sxs-lookup"><span data-stu-id="8a69b-469">LiveScript</span></span>                     | <span data-ttu-id="8a69b-470">`livescript`, `ls`</span><span class="sxs-lookup"><span data-stu-id="8a69b-470">`livescript`, `ls`</span></span>                                                             |
| <span data-ttu-id="8a69b-471">Lua</span><span class="sxs-lookup"><span data-stu-id="8a69b-471">Lua</span></span>                            | `lua`                                                                          |
| <span data-ttu-id="8a69b-472">Makefile</span><span class="sxs-lookup"><span data-stu-id="8a69b-472">Makefile</span></span>                       | <span data-ttu-id="8a69b-473">`makefile`, `mk`, `mak`</span><span class="sxs-lookup"><span data-stu-id="8a69b-473">`makefile`, `mk`, `mak`</span></span>                                                        |
| <span data-ttu-id="8a69b-474">Markdown</span><span class="sxs-lookup"><span data-stu-id="8a69b-474">Markdown</span></span>                       | <span data-ttu-id="8a69b-475">`markdown`, `md`, `mkdown`, `mkd`</span><span class="sxs-lookup"><span data-stu-id="8a69b-475">`markdown`, `md`, `mkdown`, `mkd`</span></span>                                              |
| <span data-ttu-id="8a69b-476">Mathematica</span><span class="sxs-lookup"><span data-stu-id="8a69b-476">Mathematica</span></span>                    | <span data-ttu-id="8a69b-477">`mathematica`, `mma`, `wl`</span><span class="sxs-lookup"><span data-stu-id="8a69b-477">`mathematica`, `mma`, `wl`</span></span>                                                     |
| <span data-ttu-id="8a69b-478">Matlab</span><span class="sxs-lookup"><span data-stu-id="8a69b-478">Matlab</span></span>                         | `matlab`                                                                       |
| <span data-ttu-id="8a69b-479">Maxima</span><span class="sxs-lookup"><span data-stu-id="8a69b-479">Maxima</span></span>                         | `maxima`                                                                       |
| <span data-ttu-id="8a69b-480">Maya Embedded Language</span><span class="sxs-lookup"><span data-stu-id="8a69b-480">Maya Embedded Language</span></span>         | `mel`                                                                          |
| <span data-ttu-id="8a69b-481">Mercury</span><span class="sxs-lookup"><span data-stu-id="8a69b-481">Mercury</span></span>                        | `mercury`                                                                      |
| <span data-ttu-id="8a69b-482">Язык сценариев mIRC</span><span class="sxs-lookup"><span data-stu-id="8a69b-482">mIRC Scripting Language</span></span>        | <span data-ttu-id="8a69b-483">`mirc`, `mrc`</span><span class="sxs-lookup"><span data-stu-id="8a69b-483">`mirc`, `mrc`</span></span>                                                                  |
| <span data-ttu-id="8a69b-484">Mizar</span><span class="sxs-lookup"><span data-stu-id="8a69b-484">Mizar</span></span>                          | `mizar`                                                                        |
| <span data-ttu-id="8a69b-485">MOF</span><span class="sxs-lookup"><span data-stu-id="8a69b-485">Managed Object Format</span></span>          | `mof`                                                                          |
| <span data-ttu-id="8a69b-486">Mojolicious</span><span class="sxs-lookup"><span data-stu-id="8a69b-486">Mojolicious</span></span>                    | `mojolicious`                                                                  |
| <span data-ttu-id="8a69b-487">Monkey</span><span class="sxs-lookup"><span data-stu-id="8a69b-487">Monkey</span></span>                         | `monkey`                                                                       |
| <span data-ttu-id="8a69b-488">Moonscript</span><span class="sxs-lookup"><span data-stu-id="8a69b-488">Moonscript</span></span>                     | <span data-ttu-id="8a69b-489">`moonscript`, `moon`</span><span class="sxs-lookup"><span data-stu-id="8a69b-489">`moonscript`, `moon`</span></span>                                                           |
| <span data-ttu-id="8a69b-490">MS Graph (интерактивный)</span><span class="sxs-lookup"><span data-stu-id="8a69b-490">MS Graph (Interactive)</span></span>         | `msgraph-interactive`                                                          |
| <span data-ttu-id="8a69b-491">N1QL</span><span class="sxs-lookup"><span data-stu-id="8a69b-491">N1QL</span></span>                           | `n1ql`                                                                         |
| <span data-ttu-id="8a69b-492">NSIS</span><span class="sxs-lookup"><span data-stu-id="8a69b-492">NSIS</span></span>                           | `nsis`                                                                         |
| <span data-ttu-id="8a69b-493">Nginx</span><span class="sxs-lookup"><span data-stu-id="8a69b-493">Nginx</span></span>                          | <span data-ttu-id="8a69b-494">`nginx`, `nginxconf`</span><span class="sxs-lookup"><span data-stu-id="8a69b-494">`nginx`, `nginxconf`</span></span>                                                           |
| <span data-ttu-id="8a69b-495">Nimrod</span><span class="sxs-lookup"><span data-stu-id="8a69b-495">Nimrod</span></span>                         | <span data-ttu-id="8a69b-496">`nimrod`, `nim`</span><span class="sxs-lookup"><span data-stu-id="8a69b-496">`nimrod`, `nim`</span></span>                                                                |
| <span data-ttu-id="8a69b-497">Nix</span><span class="sxs-lookup"><span data-stu-id="8a69b-497">Nix</span></span>                            | `nix`                                                                          |
| <span data-ttu-id="8a69b-498">OCaml</span><span class="sxs-lookup"><span data-stu-id="8a69b-498">OCaml</span></span>                          | <span data-ttu-id="8a69b-499">`ocaml`, `ml`</span><span class="sxs-lookup"><span data-stu-id="8a69b-499">`ocaml`, `ml`</span></span>                                                                  |
| <span data-ttu-id="8a69b-500">Objective C</span><span class="sxs-lookup"><span data-stu-id="8a69b-500">Objective C</span></span>                    | <span data-ttu-id="8a69b-501">`objectivec`, `mm`, `objc`, `obj-c`</span><span class="sxs-lookup"><span data-stu-id="8a69b-501">`objectivec`, `mm`, `objc`, `obj-c`</span></span>                                            |
| <span data-ttu-id="8a69b-502">OpenGL Shading Language</span><span class="sxs-lookup"><span data-stu-id="8a69b-502">OpenGL Shading Language</span></span>        | `glsl`                                                                         |
| <span data-ttu-id="8a69b-503">OpenSCAD</span><span class="sxs-lookup"><span data-stu-id="8a69b-503">OpenSCAD</span></span>                       | <span data-ttu-id="8a69b-504">`openscad`, `scad`</span><span class="sxs-lookup"><span data-stu-id="8a69b-504">`openscad`, `scad`</span></span>                                                             |
| <span data-ttu-id="8a69b-505">Язык правил Oracle</span><span class="sxs-lookup"><span data-stu-id="8a69b-505">Oracle Rules Language</span></span>          | `ruleslanguage`                                                                |
| <span data-ttu-id="8a69b-506">Oxygene</span><span class="sxs-lookup"><span data-stu-id="8a69b-506">Oxygene</span></span>                        | `oxygene`                                                                      |
| <span data-ttu-id="8a69b-507">PF</span><span class="sxs-lookup"><span data-stu-id="8a69b-507">PF</span></span>                             | <span data-ttu-id="8a69b-508">`pf`, `pf.conf`</span><span class="sxs-lookup"><span data-stu-id="8a69b-508">`pf`, `pf.conf`</span></span>                                                                |
| <span data-ttu-id="8a69b-509">PHP</span><span class="sxs-lookup"><span data-stu-id="8a69b-509">PHP</span></span>                            | <span data-ttu-id="8a69b-510">`php`, `php3`, `php4`, `php5`, `php6`</span><span class="sxs-lookup"><span data-stu-id="8a69b-510">`php`, `php3`, `php4`, `php5`, `php6`</span></span>                                          |
| <span data-ttu-id="8a69b-511">Parser3</span><span class="sxs-lookup"><span data-stu-id="8a69b-511">Parser3</span></span>                        | `parser3`                                                                      |
| <span data-ttu-id="8a69b-512">Perl</span><span class="sxs-lookup"><span data-stu-id="8a69b-512">Perl</span></span>                           | <span data-ttu-id="8a69b-513">`perl`, `pl`, `pm`</span><span class="sxs-lookup"><span data-stu-id="8a69b-513">`perl`, `pl`, `pm`</span></span>                                                             |
| <span data-ttu-id="8a69b-514">Обычный текст без выделения</span><span class="sxs-lookup"><span data-stu-id="8a69b-514">Plaintext no highlight</span></span>         | `plaintext`                                                                    |
| <span data-ttu-id="8a69b-515">Pony</span><span class="sxs-lookup"><span data-stu-id="8a69b-515">Pony</span></span>                           | `pony`                                                                         |
| <span data-ttu-id="8a69b-516">PostgreSQL и PL/pgSQL</span><span class="sxs-lookup"><span data-stu-id="8a69b-516">PostgreSQL & PL/pgSQL</span></span>          | <span data-ttu-id="8a69b-517">`pgsql`, `postgres`, `postgresql`</span><span class="sxs-lookup"><span data-stu-id="8a69b-517">`pgsql`, `postgres`, `postgresql`</span></span>                                              |
| <span data-ttu-id="8a69b-518">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8a69b-518">PowerShell</span></span>                     | <span data-ttu-id="8a69b-519">`powershell`, `ps`</span><span class="sxs-lookup"><span data-stu-id="8a69b-519">`powershell`, `ps`</span></span>                                                             |
| <span data-ttu-id="8a69b-520">PowerShell (интерактивный)</span><span class="sxs-lookup"><span data-stu-id="8a69b-520">PowerShell (Interactive)</span></span>       | `powershell-interactive`                                                       |
| <span data-ttu-id="8a69b-521">Обработка</span><span class="sxs-lookup"><span data-stu-id="8a69b-521">Processing</span></span>                     | `processing`                                                                   |
| <span data-ttu-id="8a69b-522">Prolog</span><span class="sxs-lookup"><span data-stu-id="8a69b-522">Prolog</span></span>                         | `prolog`                                                                       |
| <span data-ttu-id="8a69b-523">Свойства</span><span class="sxs-lookup"><span data-stu-id="8a69b-523">Properties</span></span>                     | `properties`                                                                   |
| <span data-ttu-id="8a69b-524">Буферы протоколов</span><span class="sxs-lookup"><span data-stu-id="8a69b-524">Protocol Buffers</span></span>               | `protobuf`                                                                     |
| <span data-ttu-id="8a69b-525">Puppet</span><span class="sxs-lookup"><span data-stu-id="8a69b-525">Puppet</span></span>                         | <span data-ttu-id="8a69b-526">`puppet`, `pp`</span><span class="sxs-lookup"><span data-stu-id="8a69b-526">`puppet`, `pp`</span></span>                                                                 |
| <span data-ttu-id="8a69b-527">Python</span><span class="sxs-lookup"><span data-stu-id="8a69b-527">Python</span></span>                         | <span data-ttu-id="8a69b-528">`python`, `py`, `gyp`</span><span class="sxs-lookup"><span data-stu-id="8a69b-528">`python`, `py`, `gyp`</span></span>                                                          |
| <span data-ttu-id="8a69b-529">Результаты профилировщика Python</span><span class="sxs-lookup"><span data-stu-id="8a69b-529">Python profiler results</span></span>        | `profile`                                                                      |
| <span data-ttu-id="8a69b-530">Q#</span><span class="sxs-lookup"><span data-stu-id="8a69b-530">Q#</span></span>                             | `qsharp`                                                                       |
| <span data-ttu-id="8a69b-531">Q</span><span class="sxs-lookup"><span data-stu-id="8a69b-531">Q</span></span>                              | <span data-ttu-id="8a69b-532">`k`, `kdb`</span><span class="sxs-lookup"><span data-stu-id="8a69b-532">`k`, `kdb`</span></span>                                                                     |
| <span data-ttu-id="8a69b-533">QML</span><span class="sxs-lookup"><span data-stu-id="8a69b-533">QML</span></span>                            | `qml`                                                                          |
| <span data-ttu-id="8a69b-534">R</span><span class="sxs-lookup"><span data-stu-id="8a69b-534">R</span></span>                              | `r`                                                                            |
| <span data-ttu-id="8a69b-535">Razor CSHTML</span><span class="sxs-lookup"><span data-stu-id="8a69b-535">Razor CSHTML</span></span>                   | <span data-ttu-id="8a69b-536">`cshtml`, `razor`, `razor-cshtml`</span><span class="sxs-lookup"><span data-stu-id="8a69b-536">`cshtml`, `razor`, `razor-cshtml`</span></span>                                              |
| <span data-ttu-id="8a69b-537">ReasonML</span><span class="sxs-lookup"><span data-stu-id="8a69b-537">ReasonML</span></span>                       | <span data-ttu-id="8a69b-538">`reasonml`, `re`</span><span class="sxs-lookup"><span data-stu-id="8a69b-538">`reasonml`, `re`</span></span>                                                               |
| <span data-ttu-id="8a69b-539">RenderMan RIB</span><span class="sxs-lookup"><span data-stu-id="8a69b-539">RenderMan RIB</span></span>                  | `rib`                                                                          |
| <span data-ttu-id="8a69b-540">RenderMan RSL</span><span class="sxs-lookup"><span data-stu-id="8a69b-540">RenderMan RSL</span></span>                  | `rsl`                                                                          |
| <span data-ttu-id="8a69b-541">Roboconf</span><span class="sxs-lookup"><span data-stu-id="8a69b-541">Roboconf</span></span>                       | <span data-ttu-id="8a69b-542">`graph`, `instances`</span><span class="sxs-lookup"><span data-stu-id="8a69b-542">`graph`, `instances`</span></span>                                                           |
| <span data-ttu-id="8a69b-543">Robot Framework</span><span class="sxs-lookup"><span data-stu-id="8a69b-543">Robot Framework</span></span>                | <span data-ttu-id="8a69b-544">`robot`, `rf`</span><span class="sxs-lookup"><span data-stu-id="8a69b-544">`robot`, `rf`</span></span>                                                                  |
| <span data-ttu-id="8a69b-545">Файлы спецификаций RPM</span><span class="sxs-lookup"><span data-stu-id="8a69b-545">RPM spec files</span></span>                 | <span data-ttu-id="8a69b-546">`rpm-specfile`, `rpm`, `spec`, `rpm-spec`, `specfile`</span><span class="sxs-lookup"><span data-stu-id="8a69b-546">`rpm-specfile`, `rpm`, `spec`, `rpm-spec`, `specfile`</span></span>                          |
| <span data-ttu-id="8a69b-547">Ruby</span><span class="sxs-lookup"><span data-stu-id="8a69b-547">Ruby</span></span>                           | <span data-ttu-id="8a69b-548">`ruby`, `rb`, `gemspec`, `podspec`, `thor`, `irb`</span><span class="sxs-lookup"><span data-stu-id="8a69b-548">`ruby`, `rb`, `gemspec`, `podspec`, `thor`, `irb`</span></span>                              |
| <span data-ttu-id="8a69b-549">Rust</span><span class="sxs-lookup"><span data-stu-id="8a69b-549">Rust</span></span>                           | <span data-ttu-id="8a69b-550">`rust`, `rs`</span><span class="sxs-lookup"><span data-stu-id="8a69b-550">`rust`, `rs`</span></span>                                                                   |
| <span data-ttu-id="8a69b-551">SAS</span><span class="sxs-lookup"><span data-stu-id="8a69b-551">SAS</span></span>                            | <span data-ttu-id="8a69b-552">`SAS`, `sas`</span><span class="sxs-lookup"><span data-stu-id="8a69b-552">`SAS`, `sas`</span></span>                                                                   |
| <span data-ttu-id="8a69b-553">SCSS</span><span class="sxs-lookup"><span data-stu-id="8a69b-553">SCSS</span></span>                           | `scss`                                                                         |
| <span data-ttu-id="8a69b-554">SQL</span><span class="sxs-lookup"><span data-stu-id="8a69b-554">SQL</span></span>                            | `sql`                                                                          |
| <span data-ttu-id="8a69b-555">STEP Part 21</span><span class="sxs-lookup"><span data-stu-id="8a69b-555">STEP Part 21</span></span>                   | <span data-ttu-id="8a69b-556">`p21`, `step`, `stp`</span><span class="sxs-lookup"><span data-stu-id="8a69b-556">`p21`, `step`, `stp`</span></span>                                                           |
| <span data-ttu-id="8a69b-557">Scala</span><span class="sxs-lookup"><span data-stu-id="8a69b-557">Scala</span></span>                          | `scala`                                                                        |
| <span data-ttu-id="8a69b-558">Схема</span><span class="sxs-lookup"><span data-stu-id="8a69b-558">Scheme</span></span>                         | `scheme`                                                                       |
| <span data-ttu-id="8a69b-559">Scilab</span><span class="sxs-lookup"><span data-stu-id="8a69b-559">Scilab</span></span>                         | <span data-ttu-id="8a69b-560">`scilab`, `sci`</span><span class="sxs-lookup"><span data-stu-id="8a69b-560">`scilab`, `sci`</span></span>                                                                |
| <span data-ttu-id="8a69b-561">Выражения фигуры</span><span class="sxs-lookup"><span data-stu-id="8a69b-561">Shape Expressions</span></span>              | `shexc`                                                                        |
| <span data-ttu-id="8a69b-562">Оболочка</span><span class="sxs-lookup"><span data-stu-id="8a69b-562">Shell</span></span>                          | <span data-ttu-id="8a69b-563">`shell`, `console`</span><span class="sxs-lookup"><span data-stu-id="8a69b-563">`shell`, `console`</span></span>                                                             |
| <span data-ttu-id="8a69b-564">Smali</span><span class="sxs-lookup"><span data-stu-id="8a69b-564">Smali</span></span>                          | `smali`                                                                        |
| <span data-ttu-id="8a69b-565">Smalltalk</span><span class="sxs-lookup"><span data-stu-id="8a69b-565">Smalltalk</span></span>                      | <span data-ttu-id="8a69b-566">`smalltalk`, `st`</span><span class="sxs-lookup"><span data-stu-id="8a69b-566">`smalltalk`, `st`</span></span>                                                              |
| <span data-ttu-id="8a69b-567">Solidity</span><span class="sxs-lookup"><span data-stu-id="8a69b-567">Solidity</span></span>                       | <span data-ttu-id="8a69b-568">`solidity`, `sol`</span><span class="sxs-lookup"><span data-stu-id="8a69b-568">`solidity`, `sol`</span></span>                                                              |
| <span data-ttu-id="8a69b-569">Stan</span><span class="sxs-lookup"><span data-stu-id="8a69b-569">Stan</span></span>                           | `stan`                                                                         |
| <span data-ttu-id="8a69b-570">Stata</span><span class="sxs-lookup"><span data-stu-id="8a69b-570">Stata</span></span>                          | `stata`                                                                        |
| <span data-ttu-id="8a69b-571">Структурированный текст</span><span class="sxs-lookup"><span data-stu-id="8a69b-571">Structured Text</span></span>                | <span data-ttu-id="8a69b-572">`iecst`, `scl`, `stl`, `structured-text`</span><span class="sxs-lookup"><span data-stu-id="8a69b-572">`iecst`, `scl`, `stl`, `structured-text`</span></span>                                       |
| <span data-ttu-id="8a69b-573">Stylus</span><span class="sxs-lookup"><span data-stu-id="8a69b-573">Stylus</span></span>                         | <span data-ttu-id="8a69b-574">`stylus`, `styl`</span><span class="sxs-lookup"><span data-stu-id="8a69b-574">`stylus`, `styl`</span></span>                                                               |
| <span data-ttu-id="8a69b-575">SubUnit</span><span class="sxs-lookup"><span data-stu-id="8a69b-575">SubUnit</span></span>                        | `subunit`                                                                      |
| <span data-ttu-id="8a69b-576">Supercollider</span><span class="sxs-lookup"><span data-stu-id="8a69b-576">Supercollider</span></span>                  | <span data-ttu-id="8a69b-577">`supercollider`, `sc`</span><span class="sxs-lookup"><span data-stu-id="8a69b-577">`supercollider`, `sc`</span></span>                                                          |
| <span data-ttu-id="8a69b-578">Swift</span><span class="sxs-lookup"><span data-stu-id="8a69b-578">Swift</span></span>                          | `swift`                                                                        |
| <span data-ttu-id="8a69b-579">Tcl</span><span class="sxs-lookup"><span data-stu-id="8a69b-579">Tcl</span></span>                            | <span data-ttu-id="8a69b-580">`tcl`, `tk`</span><span class="sxs-lookup"><span data-stu-id="8a69b-580">`tcl`, `tk`</span></span>                                                                    |
| <span data-ttu-id="8a69b-581">Terraform (HCL)</span><span class="sxs-lookup"><span data-stu-id="8a69b-581">Terraform (HCL)</span></span>                | <span data-ttu-id="8a69b-582">`terraform`, `tf`, `hcl`</span><span class="sxs-lookup"><span data-stu-id="8a69b-582">`terraform`, `tf`, `hcl`</span></span>                                                       |
| <span data-ttu-id="8a69b-583">Test Anything Protocol</span><span class="sxs-lookup"><span data-stu-id="8a69b-583">Test Anything Protocol</span></span>         | `tap`                                                                          |
| <span data-ttu-id="8a69b-584">TeX</span><span class="sxs-lookup"><span data-stu-id="8a69b-584">TeX</span></span>                            | `tex`                                                                          |
| <span data-ttu-id="8a69b-585">Thrift</span><span class="sxs-lookup"><span data-stu-id="8a69b-585">Thrift</span></span>                         | `thrift`                                                                       |
| <span data-ttu-id="8a69b-586">TOML</span><span class="sxs-lookup"><span data-stu-id="8a69b-586">TOML</span></span>                           | `toml`                                                                         |
| <span data-ttu-id="8a69b-587">TP</span><span class="sxs-lookup"><span data-stu-id="8a69b-587">TP</span></span>                             | `tp`                                                                           |
| <span data-ttu-id="8a69b-588">Twig</span><span class="sxs-lookup"><span data-stu-id="8a69b-588">Twig</span></span>                           | <span data-ttu-id="8a69b-589">`twig`, `craftcms`</span><span class="sxs-lookup"><span data-stu-id="8a69b-589">`twig`, `craftcms`</span></span>                                                             |
| <span data-ttu-id="8a69b-590">TypeScript</span><span class="sxs-lookup"><span data-stu-id="8a69b-590">TypeScript</span></span>                     | <span data-ttu-id="8a69b-591">`typescript`, `ts`</span><span class="sxs-lookup"><span data-stu-id="8a69b-591">`typescript`, `ts`</span></span>                                                             |
| <span data-ttu-id="8a69b-592">VB.NET</span><span class="sxs-lookup"><span data-stu-id="8a69b-592">VB.NET</span></span>                         | <span data-ttu-id="8a69b-593">`vbnet`, `vb`</span><span class="sxs-lookup"><span data-stu-id="8a69b-593">`vbnet`, `vb`</span></span>                                                                  |
| <span data-ttu-id="8a69b-594">VBScript</span><span class="sxs-lookup"><span data-stu-id="8a69b-594">VBScript</span></span>                       | <span data-ttu-id="8a69b-595">`vbscript`, `vbs`</span><span class="sxs-lookup"><span data-stu-id="8a69b-595">`vbscript`, `vbs`</span></span>                                                              |
| <span data-ttu-id="8a69b-596">VHDL</span><span class="sxs-lookup"><span data-stu-id="8a69b-596">VHDL</span></span>                           | `vhdl`                                                                         |
| <span data-ttu-id="8a69b-597">Vala</span><span class="sxs-lookup"><span data-stu-id="8a69b-597">Vala</span></span>                           | `vala`                                                                         |
| <span data-ttu-id="8a69b-598">Verilog</span><span class="sxs-lookup"><span data-stu-id="8a69b-598">Verilog</span></span>                        | <span data-ttu-id="8a69b-599">`verilog`, `v`</span><span class="sxs-lookup"><span data-stu-id="8a69b-599">`verilog`, `v`</span></span>                                                                 |
| <span data-ttu-id="8a69b-600">Скрипт Vim</span><span class="sxs-lookup"><span data-stu-id="8a69b-600">Vim Script</span></span>                     | `vim`                                                                          |
| <span data-ttu-id="8a69b-601">X++</span><span class="sxs-lookup"><span data-stu-id="8a69b-601">X++</span></span>                            | `xpp`                                                                          |
| <span data-ttu-id="8a69b-602">Сборка x86</span><span class="sxs-lookup"><span data-stu-id="8a69b-602">x86 Assembly</span></span>                   | `x86asm`                                                                       |
| <span data-ttu-id="8a69b-603">XL</span><span class="sxs-lookup"><span data-stu-id="8a69b-603">XL</span></span>                             | <span data-ttu-id="8a69b-604">`xl`, `tao`</span><span class="sxs-lookup"><span data-stu-id="8a69b-604">`xl`, `tao`</span></span>                                                                    |
| <span data-ttu-id="8a69b-605">XQuery</span><span class="sxs-lookup"><span data-stu-id="8a69b-605">XQuery</span></span>                         | <span data-ttu-id="8a69b-606">`xquery`, `xpath`, `xq`</span><span class="sxs-lookup"><span data-stu-id="8a69b-606">`xquery`, `xpath`, `xq`</span></span>                                                        |
| <span data-ttu-id="8a69b-607">XAML</span><span class="sxs-lookup"><span data-stu-id="8a69b-607">XAML</span></span>                           | `xaml`                                                                         |
| <span data-ttu-id="8a69b-608">XML</span><span class="sxs-lookup"><span data-stu-id="8a69b-608">XML</span></span>                            | <span data-ttu-id="8a69b-609">`xml`, `xhtml`, `rss`, `atom`, `xjb`, `xsd`, `xsl`, `plist`</span><span class="sxs-lookup"><span data-stu-id="8a69b-609">`xml`, `xhtml`, `rss`, `atom`, `xjb`, `xsd`, `xsl`, `plist`</span></span>                    |
| <span data-ttu-id="8a69b-610">YAML</span><span class="sxs-lookup"><span data-stu-id="8a69b-610">YAML</span></span>                           | <span data-ttu-id="8a69b-611">`yml`, `yaml`</span><span class="sxs-lookup"><span data-stu-id="8a69b-611">`yml`, `yaml`</span></span>                                                                  |
| <span data-ttu-id="8a69b-612">Zephir</span><span class="sxs-lookup"><span data-stu-id="8a69b-612">Zephir</span></span>                         | <span data-ttu-id="8a69b-613">`zephir`, `zep`</span><span class="sxs-lookup"><span data-stu-id="8a69b-613">`zephir`, `zep`</span></span>                                                                |

> [!TIP]
> <span data-ttu-id="8a69b-614">При наличии нескольких псевдонимов в пакете Docs Authoring Pack [функции завершения языка разработки](docs-authoring/dev-lang-completion.md) используется первый допустимый псевдоним.</span><span class="sxs-lookup"><span data-stu-id="8a69b-614">The Docs Authoring Pack, [Dev Lang Completion feature](docs-authoring/dev-lang-completion.md) uses the first valid alias when multiple aliases are available.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8a69b-615">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="8a69b-615">Next steps</span></span>

<span data-ttu-id="8a69b-616">Сведения о форматировании текста для типов содержимого, отличных от кода, см. в разделе [Рекомендации по форматированию текста](text-formatting-guidelines.md).</span><span class="sxs-lookup"><span data-stu-id="8a69b-616">For information on text formatting for content types other than code, see [Text formatting guidelines](text-formatting-guidelines.md).</span></span>
