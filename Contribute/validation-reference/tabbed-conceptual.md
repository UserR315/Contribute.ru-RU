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
# <a name="tabbed-conceptual"></a>Элемент с вкладками

> [!IMPORTANT]
> Синтаксис элемента с вкладками признан устаревшим, и добавлять новые вкладки больше не следует. Проверки, которые описаны в этой статье, применяются к наборам содержимого, в которых может использоваться элемент с вкладками, до тех пор, пока не будут реализованы функции для его замены.

## <a name="tab-syntax"></a>Синтаксис вкладок

Используйте следующий синтаксис для вкладок:

Одноуровневая вкладка:

`# [Tab Display Name](#tab/tab-id)`

Дополнительная зависимая вкладка:

`# [Tab Display Name](#tab/tab-id/tab-condition)`

Пример раздела одноуровневых вкладок с двумя вкладками и разделителями группы вкладок (---):

```markdown
# [Linux](#tab/linux)

Content for Linux...

# [Windows](#tab/windows)

Content for Windows...

---
```

Вкладки также могут включать вторичные, или зависимые вкладки. Эти вкладки зависят от выделенных элементов в другом наборе вкладок. Ниже приведен пример.

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

К синтаксису вкладок применяются следующие проверки:

- Синтаксис вкладок должен быть правильным.
- Зависимые вкладки должны быть определены в предыдущей группе вкладок.
- Допускается использовать только один уровень зависимости.
- Минимально возможное число вкладок — две.
- Максимально возможное число вкладок — четыре.
- Вкладки должны быть утверждены.
- Пары вкладок и идентификаторов должны быть допустимыми.
- Один и тот же идентификатор вкладки не может использоваться несколько раз в одной группе вкладок.

## <a name="approved-tabs"></a>Утвержденные вкладки

Следующие пары имени и идентификатора вкладок являются утвержденными. Идентификаторы зависимых вкладок не сопоставляются, но должны быть допустимыми в соответствии с содержимым столбца идентификатора вкладки. Эти значения чувствительны к регистру.

|Название вкладки              |Идентификатор вкладки            |
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