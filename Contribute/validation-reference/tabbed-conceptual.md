# <a name="tabbed-conceptual"></a><span data-ttu-id="d5dd9-101">Элемент с вкладками</span><span class="sxs-lookup"><span data-stu-id="d5dd9-101">Tabbed conceptual</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d5dd9-102">Синтаксис элемента с вкладками признан устаревшим, и добавлять новые вкладки больше не следует.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-102">The tabbed conceptual syntax has been deprecated and new tabs should not be added.</span></span> <span data-ttu-id="d5dd9-103">Проверки, которые описаны в этой статье, применяются к наборам содержимого, в которых может использоваться элемент с вкладками, до тех пор, пока не будут реализованы функции для его замены.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-103">The validations described in this article apply to content sets that have been approved to use tabbed conceptual until replacement functionality is available.</span></span>

## <a name="tab-syntax"></a><span data-ttu-id="d5dd9-104">Синтаксис вкладок</span><span class="sxs-lookup"><span data-stu-id="d5dd9-104">Tab syntax</span></span>

<span data-ttu-id="d5dd9-105">Используйте следующий синтаксис для вкладок:</span><span class="sxs-lookup"><span data-stu-id="d5dd9-105">The syntax for tabs is as follows:</span></span>

<span data-ttu-id="d5dd9-106">Одноуровневая вкладка:</span><span class="sxs-lookup"><span data-stu-id="d5dd9-106">Single level tab:</span></span>

`# [Tab Display Name](#tab/tab-id)`

<span data-ttu-id="d5dd9-107">Дополнительная зависимая вкладка:</span><span class="sxs-lookup"><span data-stu-id="d5dd9-107">Optional dependent tab:</span></span>

`# [Tab Display Name](#tab/tab-id/tab-condition)`

<span data-ttu-id="d5dd9-108">Пример раздела одноуровневых вкладок с двумя вкладками и разделителями группы вкладок (---):</span><span class="sxs-lookup"><span data-stu-id="d5dd9-108">Example of a single-level tab section with two tabs and the tab group terminator (---):</span></span>

```
# [Linux](#tab/linux)

Content for Linux...

# [Windows](#tab/windows)

Content for Windows...

---
```

<span data-ttu-id="d5dd9-109">Вкладки также могут включать вторичные, или зависимые вкладки.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-109">Tabs can optionally contain secondary tabs, or dependency tabs.</span></span> <span data-ttu-id="d5dd9-110">Эти вкладки зависят от выделенных элементов в другом наборе вкладок.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-110">This makes tabs dependent on the selection in another set of tabs.</span></span> <span data-ttu-id="d5dd9-111">Ниже приведен пример.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-111">Here's an example:</span></span>

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

<span data-ttu-id="d5dd9-112">К синтаксису вкладок применяются следующие проверки:</span><span class="sxs-lookup"><span data-stu-id="d5dd9-112">The following validations apply to tab syntax:</span></span>

- <span data-ttu-id="d5dd9-113">Синтаксис вкладок должен быть правильным.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-113">Tab syntax must be correct.</span></span>
- <span data-ttu-id="d5dd9-114">Зависимые вкладки должны быть определены в предыдущей группе вкладок.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-114">Dependent tabs must have been defined in a previous tab group.</span></span>
- <span data-ttu-id="d5dd9-115">Допускается использовать только один уровень зависимости.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-115">Only one level of dependency is allowed.</span></span>
- <span data-ttu-id="d5dd9-116">Минимально возможное число вкладок — две.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-116">No fewer than two tabs are allowed.</span></span>
- <span data-ttu-id="d5dd9-117">Максимально возможное число вкладок — четыре.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-117">No more than four tabs are allowed.</span></span>
- <span data-ttu-id="d5dd9-118">Вкладки должны быть добавлены в список разрешенных вкладок.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-118">Tabs must be whitelisted.</span></span>
- <span data-ttu-id="d5dd9-119">Пары вкладок и идентификаторов должны быть допустимыми.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-119">Tab/ID pairs must be valid.</span></span>
- <span data-ttu-id="d5dd9-120">Один и тот же идентификатор вкладки не может использоваться несколько раз в одной группе вкладок.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-120">Cannot have the same tab ID multiple times in one tab group.</span></span>

## <a name="tab-whitelist"></a><span data-ttu-id="d5dd9-121">Список разрешенных вкладок</span><span class="sxs-lookup"><span data-stu-id="d5dd9-121">Tab whitelist</span></span>

<span data-ttu-id="d5dd9-122">В список разрешенных вкладок включены следующие пары названий и идентификаторов вкладок.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-122">The following tab name/tab ID pairs are whitelisted.</span></span> <span data-ttu-id="d5dd9-123">Идентификаторы зависимых вкладок не сопоставляются, но должны быть допустимыми в соответствии с содержимым столбца идентификатора вкладки.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-123">Dependent tab IDs are not paired but must be valid per the Tab ID column.</span></span> <span data-ttu-id="d5dd9-124">Эти значения чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-124">The values are case-sensitive</span></span>

|<span data-ttu-id="d5dd9-125">Название вкладки</span><span class="sxs-lookup"><span data-stu-id="d5dd9-125">Tab name</span></span>              |<span data-ttu-id="d5dd9-126">Идентификатор вкладки</span><span class="sxs-lookup"><span data-stu-id="d5dd9-126">Tab ID</span></span>            |
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