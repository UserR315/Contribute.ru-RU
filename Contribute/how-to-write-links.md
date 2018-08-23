---
title: Использование ссылок в документации
description: В этой статье содержатся инструкции по созданию ссылок на содержимое на сайте docs.microsoft.com.
ms.date: 06/29/2017
ms.openlocfilehash: dad0460cfb36594c17cef1b079c5fc14191f56f7
ms.sourcegitcommit: 886ca76086a302d1d6124967df12a5bcfe4fd4b5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/10/2018
ms.locfileid: "40251474"
---
# <a name="using-links-in-documentation"></a>Использование ссылок в документации
В этой статье описывается использование гиперссылок со страниц, размещенных на сайте docs.microsoft.com. Добавление ссылок в Markdown не представляет труда, но следует придерживаться ряда определенных правил. Ссылки могут указывать на содержимое на той же странице, на соседних страницах или вести на внешние сайты и URL-адреса.

В серверной части сайта docs.microsoft.com используются службы Open Publishing Services (OPS), которые поддерживают формат DocFX Flavored Markdown (DFM). DFM характеризуется высоким уровнем совместимости с форматом GitHub Flavored Markdown (GFM) и предоставляет дополнительные функции за счет применения расширений Markdown.

> [!IMPORTANT]
> Все ссылки должны быть безопасными (с протоколом `https` вместо `http`), если целевой объект поддерживает такой протокол (большинство целевых объектов поддерживают).

## <a name="link-text"></a>Текст ссылки

Фраза для ссылки должна быть понятной. Иными словами, это должен быть полноценный текст или название страницы, на которую указывает ссылка.

> [!IMPORTANT]
> Не используйте конструкцию "щелкните здесь". Она плохо сказывается на SEO-оптимизации и не дает адекватного представления о целевой странице.

**Правильно:**

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

**Неправильно:**

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a>Ссылки для перехода от одной статьи к другой

Чтобы добавить в статью, содержащую техническую документацию, встроенную ссылку на другую такую статью в том же docset, используйте следующий синтаксис.

- Для статьи в каталоге, в которую добавляется ссылка на другую статью в том же каталоге:

  `[link text](article-name.md)`

- Для статьи в подкаталоге, в которую добавляется ссылка на статью в корневом каталоге:

  `[link text](../article-name.md)`

- Для статьи в корневом каталоге, в которую добавляется ссылка на статью в подкаталоге:

  `[link text](./directory/article-name.md)`

- Для статьи в подкаталоге, в которую добавляется ссылка на статью в другом подкаталоге:

  `[link text](../directory/article-name.md)`

- Для статьи, ссылка на которую добавляется в разные docset (даже в рамках одного репозитория): `[link text](./directory/article-name)`

> [!IMPORTANT]
> Ни в одном из примеров выше `~/` не используется в качестве части ссылки. Если вы ссылаетесь на путь в корне репозитория, начните с `/`. Добавление `~/` приведет к формированию недопустимых ссылок при навигации по репозиториям исходного кода на GitHub. Если начать путь с `/`, разрешение происходит успешно.

## <a name="links-to-anchors"></a>Ссылки на привязки

Создавать привязки не требуется. Они автоматически генерируются для всех заголовков H2 во время публикации. Достаточно создать ссылки на разделы H2.

- Для ссылки на заголовок в той же статье:

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- Для ссылки на привязку в другой статье в том же подкаталоге:

  `[link text](article-name.md#anchor-name)`
  `[Configure your profile](media-services-create-account.md#configure-your-profile)`

- Для ссылки на привязку в другом подкаталоге службы:

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a>Ссылки во включаемых файлах

Включаемые файлы содержатся в другом каталоге, поэтому для них используются более длинные относительные пути. Чтобы добавить ссылку на статью во включаемый файл, используйте следующий формат:

    [link text](../articles/folder/article-name.md)

## <a name="links-in-selectors"></a>Ссылки в селекторах

Если во включаемый файл внедрены селекторы, как в документации Azure, используйте следующую структуру ссылки:

    > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
    - [(Text1 | Example1 )](../articles/folder/article-name1.md)
    - [(Text1 | Example2 )](../articles/folder/article-name2.md)
    - [(Text2 | Example3 )](../articles/folder/article-name3.md)
    - [(Text2 | Example4 )](../articles/folder/article-name4.md) -->

## <a name="reference-style-links"></a>Ссылки типа сносок

Ссылки типа сносок используются для того, чтобы пользователю было легче воспринимать содержимое источника. Для ссылок типа сносок синтаксис встроенной ссылки заменяется упрощенным вариантом, который позволяет переместить длинные URL-адреса в конец статьи. Ниже приведен пример от [Daring Fireball](https://daringfireball.net/projects/markdown/).

Встроенный текст:

    I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].

Ссылки типа сносок в конце статьи:

    <!--Reference links in article-->
    [1]: http://google.com/
    [2]: http://search.yahoo.com/
    [3]: http://search.msn.com/

Обязательно используйте пробел после двоеточия перед ссылкой. Если при добавлении ссылок на другие технические статьи вы забудете включить пробел, ссылка не будет работать в опубликованной статье.

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a>Ссылки на страницы, не являющиеся частью технической документации

Чтобы добавить ссылку на страницу корпорации Майкрософт другого характера (например, на страницу с ценами, страницу соглашения об уровне обслуживания или любую другую страницу, не являющуюся статьей документации), используйте абсолютный URL-адрес без указания языка. Такие ссылки работают на сайте GitHub и на отображаемом сайте:

    [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)

## <a name="links-to-third-party-sites"></a>Ссылки на сторонние сайты

Лучше избегать перенаправления пользователей на другие сайты. Но иногда это необходимо. При размещении ссылок на сторонние сайты руководствуйтесь следующей информацией:

- **Отслеживаемость**. Добавляйте ссылки на содержимое сторонних поставщиков, если именно к нему требуется предоставить общий доступ. Например, предоставлять описание того, как использовать средства разработчика Android, не входит в обязанности корпорации Майкрософт. Это задача Google. При необходимости мы можем объяснить, как использовать средства разработчика Android *с* Azure, но руководство по применению этих средств должна предоставить корпорация Google.
- **Утверждение руководителем проектов**. Запрашивайте в корпорации Майкрософт утверждение ссылок на содержимое сторонних поставщиков. Такие ссылки предполагают определенный уровень ответственности за надежность информации и выполнение инструкций пользователем.
- **Проверки актуальности**. Следите за актуальностью, правильностью и релевантностью информации. Регулярно проверяйте, не изменилась ли ссылка.
- **Информация о переходе на сайт стороннего поставщика**. Обязательно уведомляйте пользователей о том, что они переходят на другой сайт. Если это не следует из контекста, добавьте соответствующую фразу. Например, "Предварительные требования включают установку средств разработчика Android, которые вы можете скачать на сайте Android Studio".
- **Дальнейшие действия**. Неплохим решением будет добавить ссылку, скажем, на блог MVP, в разделе "Дальнейшие действия". Опять же, при этом пользователь должен понимать, что он покидает текущий сайт.
- **Юридическая информация**. Юридическая информация предоставляется в разделе **Ссылки на веб-сайты третьих лиц** на странице **условий использования**. Ссылка на нее размещена в нижнем колонтитуле каждой страницы ms.com.

## <a name="links-to-msdn-or-technet"></a>Ссылки на MSDN или TechNet

Если нужно добавить ссылку на MSDN или TechNet, используйте полную ссылку на статью, удалив указатель языка "en-us".

## <a name="links-to-azure-powershell-reference-content"></a>Ссылки на справочные материалы по Azure PowerShell

Справочные материалы по Azure PowerShell с ноября 2016 г. претерпели некоторые изменения. Выполните приведенные ниже инструкции, чтобы добавить ссылку на эти материалы в другие статьи на сайте docs.microsoft.com.

Структура URL-адреса:

* Для командлетов:
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* Для тематических статей:
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

Часть &lt;moniker-name&gt; является необязательной. Если ее исключить, пользователь будет направлен к последней версии содержимого. Для части &lt;service-name&gt; можно задать одно из значений в примерах базовых URL-адресов ниже:

- Содержимое Azure PowerShell (AzureRM): [https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)
- Содержимое Azure PowerShell (ASM) : [https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)
- Содержимое Azure PowerShell для Active Directory (AzureAD): [https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)
- PowerShell для Azure Service Fabric [https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)
- PowerShell для Azure Information Protection: [https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)
- PowerShell для заданий эластичной базы данных заданий Azure: [https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)

Если включить эти URL-адреса, пользователь будет перенаправлен к последней версии содержимого. В таком случае указывать моникер версии не требуется. Кроме того, вам не придется обновлять ссылки на тематические материалы при изменении версии.

Чтобы создать правильную ссылку на страницу, откройте ее в браузере и скопируйте URL-адрес.
Удалите https://docs.microsoft.com и сведения о языковом стандарте.

Если ссылка размещена в оглавлении, используйте полный URL-адрес без указателя языка.

Пример разметки Markdown:

```markdown
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](/powershell/azure/install-azurerm-ps)
```
