---
ms.date: 03/29/2019
title: Элемент с вкладками
ms.openlocfilehash: 3d6f38c1659297182a8bd50bf52b9853bd21b2c8
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/12/2019
ms.locfileid: "66841303"
---
# <a name="tabbed-conceptual"></a><span data-ttu-id="d6390-102">Элемент с вкладками</span><span class="sxs-lookup"><span data-stu-id="d6390-102">Tabbed conceptual</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d6390-103">Синтаксис элемента с вкладками признан устаревшим, и добавлять новые вкладки больше не следует.</span><span class="sxs-lookup"><span data-stu-id="d6390-103">The tabbed conceptual syntax has been deprecated and new tabs should not be added.</span></span> <span data-ttu-id="d6390-104">Проверки, которые описаны в этой статье, применяются к наборам содержимого, в которых может использоваться элемент с вкладками, до тех пор, пока не будут реализованы функции для его замены.</span><span class="sxs-lookup"><span data-stu-id="d6390-104">The validations described in this article apply to content sets that have been approved to use tabbed conceptual until replacement functionality is available.</span></span>

## <a name="tab-syntax"></a><span data-ttu-id="d6390-105">Синтаксис вкладок</span><span class="sxs-lookup"><span data-stu-id="d6390-105">Tab syntax</span></span>

<span data-ttu-id="d6390-106">Используйте следующий синтаксис для вкладок:</span><span class="sxs-lookup"><span data-stu-id="d6390-106">The syntax for tabs is as follows:</span></span>

<span data-ttu-id="d6390-107">Одноуровневая вкладка:</span><span class="sxs-lookup"><span data-stu-id="d6390-107">Single level tab:</span></span>

`# [Tab Display Name](#tab/tab-id)`

<span data-ttu-id="d6390-108">Дополнительная зависимая вкладка:</span><span class="sxs-lookup"><span data-stu-id="d6390-108">Optional dependent tab:</span></span>

`# [Tab Display Name](#tab/tab-id/tab-condition)`

<span data-ttu-id="d6390-109">Пример раздела одноуровневых вкладок с двумя вкладками и разделителями группы вкладок (---):</span><span class="sxs-lookup"><span data-stu-id="d6390-109">Example of a single-level tab section with two tabs and the tab group terminator (---):</span></span>

```markdown
# [Linux](#tab/linux)

Content for Linux...

# [Windows](#tab/windows)

Content for Windows...

---
```

<span data-ttu-id="d6390-110">Вкладки также могут включать вторичные, или зависимые вкладки.</span><span class="sxs-lookup"><span data-stu-id="d6390-110">Tabs can optionally contain secondary tabs, or dependency tabs.</span></span> <span data-ttu-id="d6390-111">Эти вкладки зависят от выделенных элементов в другом наборе вкладок.</span><span class="sxs-lookup"><span data-stu-id="d6390-111">This makes tabs dependent on the selection in another set of tabs.</span></span> <span data-ttu-id="d6390-112">Ниже приведен пример.</span><span class="sxs-lookup"><span data-stu-id="d6390-112">Here's an example:</span></span>

```markdown
# [Azure CLI](#tab/azure-cli/linux)

Azure CLI content for Linux...

# [Azure CLI](#tab/azure-cli/windows)

Azure CLI content for Windows...

# [PowerShell](#tab/azure-powershell/linux)

PowerShell content for Linux...

# [PowerShell](#tab/azure-powershell/windows)

PowerShell content for Windows...

---
```

<span data-ttu-id="d6390-113">К синтаксису вкладок применяются следующие проверки:</span><span class="sxs-lookup"><span data-stu-id="d6390-113">The following validations apply to tab syntax:</span></span>

- <span data-ttu-id="d6390-114">Синтаксис вкладок должен быть правильным.</span><span class="sxs-lookup"><span data-stu-id="d6390-114">Tab syntax must be correct.</span></span>
- <span data-ttu-id="d6390-115">Зависимые вкладки должны быть определены в предыдущей группе вкладок.</span><span class="sxs-lookup"><span data-stu-id="d6390-115">Dependent tabs must have been defined in a previous tab group.</span></span>
- <span data-ttu-id="d6390-116">Допускается использовать только один уровень зависимости.</span><span class="sxs-lookup"><span data-stu-id="d6390-116">Only one level of dependency is allowed.</span></span>
- <span data-ttu-id="d6390-117">Минимально возможное число вкладок — две.</span><span class="sxs-lookup"><span data-stu-id="d6390-117">No fewer than two tabs are allowed.</span></span>
- <span data-ttu-id="d6390-118">Максимально возможное число вкладок — четыре.</span><span class="sxs-lookup"><span data-stu-id="d6390-118">No more than four tabs are allowed.</span></span>
- <span data-ttu-id="d6390-119">Вкладки должны быть утверждены.</span><span class="sxs-lookup"><span data-stu-id="d6390-119">Tabs must be approved.</span></span>
- <span data-ttu-id="d6390-120">Пары вкладок и идентификаторов должны быть допустимыми.</span><span class="sxs-lookup"><span data-stu-id="d6390-120">Tab/ID pairs must be valid.</span></span>
- <span data-ttu-id="d6390-121">Один и тот же идентификатор вкладки не может использоваться несколько раз в одной группе вкладок.</span><span class="sxs-lookup"><span data-stu-id="d6390-121">Cannot have the same tab ID multiple times in one tab group.</span></span>

## <a name="approved-tabs"></a><span data-ttu-id="d6390-122">Утвержденные вкладки</span><span class="sxs-lookup"><span data-stu-id="d6390-122">Approved tabs</span></span>

<span data-ttu-id="d6390-123">Следующие пары имени и идентификатора вкладок являются утвержденными.</span><span class="sxs-lookup"><span data-stu-id="d6390-123">The following tab name/tab ID pairs are approved.</span></span> <span data-ttu-id="d6390-124">Идентификаторы зависимых вкладок не сопоставляются, но должны быть допустимыми в соответствии с содержимым столбца идентификатора вкладки.</span><span class="sxs-lookup"><span data-stu-id="d6390-124">Dependent tab IDs are not paired but must be valid per the Tab ID column.</span></span> <span data-ttu-id="d6390-125">Эти значения чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="d6390-125">The values are case-sensitive</span></span>

|<span data-ttu-id="d6390-126">Название вкладки</span><span class="sxs-lookup"><span data-stu-id="d6390-126">Tab name</span></span>              |<span data-ttu-id="d6390-127">Идентификатор вкладки</span><span class="sxs-lookup"><span data-stu-id="d6390-127">Tab ID</span></span>            |
|----------------------|------------------|
|`[.NET]`              |`(#tab/dotnet)`   |
|`[.NET Core 1.x]`     |`(#tab/netcore1x)`|
|`[.NET Core 2.x]`     |`(#tab/netcore2x)`|
|`[.NET Core 2.0]`     |`(#tab/netcore20)`|
|`[.NET Core 2.1]`     |`(#tab/netcore21)`|
|`[.NET Core 2.2]`     |`(#tab/netcore22)`|
|`[.NET Core 3.x]`     |`(#tab/netcore3x)`|
|`[.NET Core 3.0]`     |`(#tab/netcore30)`|
|`[.NET Core CLI]`     |`(#tab/netcore-cli)`|
|`[Azure CLI]`         |`(#tab/azure-cli)`|
|`[Android]`           |`(#tab/android)`  |
|`[Browser]`           |`(#tab/browser)`  |
|`[C#]`                |`(#tab/csharp)`   |
|`[C# Script]`         |`(#tab/csharp-script)`|
|`[CentOS]`            |`(#tab/centos)`|
|`[Command Line]`      |`(#tab/command-line)`|
|`[Debian]`            |`(#tab/debian)`|
|`[Docker Hub]`        |`(#tab/docker-hub)`|
|`[F#]`                |`(#tab/fsharp)`|
|`[Fedora]`            |`(#tab/fedora)`|
|`[iOS]`               |`(#tab/ios)`      |
|`[Java]`              |`(#tab/java)`|
|`[JavaScript]`        |`(#tab/javascript)`|
|`[Linux]`             |`(#tab/linux)`    |
|`[macOS]`             |`(#tab/macos)`    |
|`[Managed Kubernetes]`|`(#tab/kubernetes-managed)`|
|`[Maven]`             |`(#tab/maven)`|
|`[Mint]`              |`(#tab/mint)`|
|`[Node.js]`           |`(#tab/nodejs)`|
|`[npm]`               |`(#tab/npm)` |
|`[NuGet]`             |`(#tab/nuget)`|
|`[openSUSE]`          |`(#tab/opensuse)`|
|`[Other]`             |`(#tab/other)` |
|`[Oracle Linux]`      |`(#tab/oracle-linux)`|
|`[Package Manager]`   |`(#tab/package-manager)` |
|`[PEAR]`              |`(#tab/pear)`|
|`[pip]`               |`(#tab/pip)`|
|`[Portal]`            |`(#tab/azure-portal)`    |
|`[PowerShell]`        |`(#tab/azure-powershell)`|
|`[Private Registry]`  |`(#tab/private-registry)`|
|`[Python]`            |`(#tab/python)`|
|`[Resource Manager Template]`|`(#tab/azure-resource-manager)`|
|`[RHEL]`              |`(#tab/rhel)`|
|`[RubyGems]`          |`(#tab/rubygems)`|
|`[SQL Server]`        |`(#tab/sql-server)`|
|`[SQLite]`            |`(#tab/sqlite)`|
|`[TypeScript]`        |`(#tab/typescript)`|
|`[Visual Basic]`      |`(#tab/vb)` |
|`[Visual Studio]`     |`(#tab/visual-studio)`|
|`[Visual Studio 15.6 and earlier]`|`(#tab/vs156)`|
|`[Visual Studio 15.7 and later]`  |`(#tab/vs157)`|
|`[Visual Studio Code]`            |`(#tab/visual-studio-code)`|
|`[Visual Studio for Mac]`         |`(#tab/visual-studio-mac)`|
|`[Ubuntu]`                        |`(#tab/ubuntu)`|
|`[Unmanaged Kubernetes]`          |`(#tab/kubernetes-unmanaged)`|
|`[Windows]`   |`(#tab/windows)`   |