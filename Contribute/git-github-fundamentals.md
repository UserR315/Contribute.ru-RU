---
title: Основные сведения о Git и GitHub для создания документации
description: В этой статье приводятся общие сведения о репозиториях Git в GitHub, принципах организации содержимого и правилах именования, используемых для сайта docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 06/30/2017
ms.openlocfilehash: 5154b80102069f1d5526b744637f8ba854f1fe3f
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288442"
---
# <a name="git-and-github-essentials-for-docs"></a>Основные сведения о Git и GitHub для создания документации

## <a name="overview"></a>Общие сведения

Как участник проекта по созданию документации вы будете использовать ряд инструментов и процессов. Вы будете работать параллельно с другими участниками над одним и тем же проектом, иногда над тем же содержимым и в то же время. Все это возможно благодаря программному обеспечению Git и GitHub.

Git — это система управления версиями с открытым исходным кодом. Она упрощает совместную работу над проектами такого типа с помощью *распределенной системы управления версиями* файлов, которые хранятся в *репозиториях*. По сути, Git позволяет интегрировать в определенный репозиторий потоки работы, выполненные несколькими участниками в течение определенного времени.

GitHub — это служба размещения в Интернете репозиториев Git, которые используются для хранения содержимого [docs.microsoft.com](https://docs.microsoft.com). В GitHub размещается основной репозиторий всех проектов. Из этого репозитория участники копируют свою работу.

## <a name="git"></a>Git

Если вы знакомы с централизованными системами управления версиями (например, Team Foundation Server, SharePoint или Visual SourceSafe), вы заметите, что Git использует уникальный рабочий процесс и специальную терминологию для поддержки распределенной модели. Например, в Git не блокируются файлы, как это обычно бывает, когда файл берут на редактирование или возвращают после редактирования. На самом деле Git учитывает изменения на более тонком уровне, сравнивая файлы байт за байтом.

Git также использует многоуровневую структуру для хранения содержимого проекта и управления им.

- *Репозиторий* — это *единица хранения* самого высокого уровня. Репозиторий содержит одну или несколько ветвей.
- *Ветвь* представляет собой единицу хранения, содержащую текущие файлы и папки, которые формируют содержимое проекта. Ветви используются для разделения потоков работы (обычно они называются версиями). Участники всегда вносят изменения в содержимое в определенной ветви, и эти изменения привязаны к соответствующей ветви. Все репозитории содержат ветвь по умолчанию (обычно она называется главной) и одну или несколько ветвей, предназначенных для объединения с главной ветвью. Главная ветвь является текущей версией и единственным источником достоверных сведений для определенного проекта. Из этой родительской ветви создаются все остальные ветви в репозитории.

Участники взаимодействуют с Git, чтобы обновлять репозитории и управлять ими локально и на уровне GitHub.

- Для локального взаимодействия участники используют такие инструменты, как консоль Git Bash, которая поддерживает команды Git для управления локальными репозиториями и обмена данными с репозиториями GitHub.
- Кроме того, участники используют сайт [www.github.com](https://www.github.com) с интегрированной системой Git для управления согласованием изменений, возвращаемых обратно в основной репозиторий.

## <a name="github"></a>GitHub

> [!NOTE]
> Хотя управление проекта Docs основано на использовании GitHub, некоторые команды используют Visual Studio Team Services для размещения репозиториев Git. Клиент Visual Studio Team Explorer — это графический интерфейс для взаимодействия с репозиториями Team Services. Этот интерфейс является альтернативой использованию команд Git в командной строке.
> </br>
> Кроме того, многие приведенные руководства разработаны в качестве рекомендаций, которые появились в результате многолетнего размещения содержимого службы Azure в GitHub. Они могут понадобиться для работы с некоторыми репозиториями Docs.

Все рабочие процессы начинаются и заканчиваются на уровне GitHub, где хранится основной репозиторий любого проекта Docs. Копии, создаваемые участниками для собственного использования, распространяются на нескольких компьютерах. В итоге они согласовываются в основном репозитории GitHub проекта.

### <a name="directory-organization"></a>Организация каталогов

Как упоминалось ранее, стандартная или главная ветвь проекта является текущей версией содержимого проекта. Содержимое главной ветви (и ветвей, созданных из нее) приблизительно согласовано с организацией статей на соответствующих страницах проекта Docs. Подкаталоги используются для разделения содержимого (например, служб), мультимедийного содержимого (например, файлов изображений) и файлов include, которые позволяют повторно использовать содержимое.

Основной каталог `articles` обычно находится в корне репозитория. Этот каталог статей содержит набор подкаталогов. Статьи в подкаталогах имеют формат файлов Markdown с расширением *.md*. Некоторые репозитории, которые поддерживают несколько служб, например репозиторий [Azure-Docs](https://github.com/MicrosoftDocs/Azure-Docs), используют универсальный подкаталог `/articles`. Другие репозитории, например [IntuneDocs](https://github.com/MicrosoftDocs/IntuneDocs), используют подкаталог, который называется как служба: `/IntuneDocs`.

В корне этого каталога находятся общие статьи, которые описывают службу или продукт в целом. Как правило, каталог содержит еще одну серию подкаталогов, которые соответствуют функциям и службам или распространенным сценариям. Например, статьи, которые описывают службу виртуальных машин Azure, находятся в подкаталоге `/virtual-machines`, статьи "Изучение вопроса" службы Intune размещены в подкаталоге `/understand-explore`.

### <a name="media-subdirectory"></a>Подкаталог Media

В каждом каталоге находится подкаталог `/media` для соответствующих файлов мультимедиа. Файлы мультимедиа содержат изображения, используемые в статьях со ссылками на изображения.

### <a name="includes-subdirectory"></a>Подкаталог includes

Содержимое для многократного использования, которое является общим для двух или нескольких статей, помещается в подкаталог `/includes` основного каталога `articles`. В файле Markdown, где используется включаемый файл, соответствующее расширение Markdown include помещается в расположение, на которое должна указывать ссылка на включаемый файл.

Дополнительные инструкции см. в разделе [Включаемые файлы](how-to-write-use-markdown.md#include-files).

### <a name="markdown-file-template"></a>Шаблон файла Markdown

Для удобства в корневом каталоге каждого репозитория обычно находится файл шаблона Markdown с именем `template.md`. Его можно использовать как начальный файл для создания статьи с последующей отправкой в репозиторий. Файл содержит следующие компоненты.

- **Заголовок метаданных** в верхней части файла, разделенный двумя строками с тремя дефисами. Он содержит различные теги, используемые для отслеживания информации, относящейся к статье. Метаданные статьи обеспечивают дополнительные возможности. Например, можно указать ссылки на автора и участника, настроить строку навигации, добавить описание статьи. Они также обеспечивают оптимизации поисковых систем и позволяют Майкрософт оценивать качество содержимого. Как видите, метаданные имеют большое значение.
- **Раздел метаданных** с описанием различных тегов и значений метаданных. Если вы не знаете, какие значения нужно использовать для раздела метаданных, их можно оставить пустыми или закомментировать с помощью начального хэштега (#). Так рецензент запроса на вытягивание в репозитории сможет проверить или заполнить их.
- Различные **примеры использования разметки Markdown** для форматирования элементов статьи.
- Общие **инструкции по использованию расширений разметки Markdown**, которые можно применять для различных типов оповещений.
- Примеры **встраивания видео** с помощью iframe.
- Общие **инструкции по использованию расширений docs.microsoft.com**, которые можно применять для специальных элементов управления, таких как кнопки и селекторы.

## <a name="pull-requests"></a>Запросы на вытягивание

*Запрос на вытягивание* — используя этот удобный способ, участник предлагает набор изменений для внесения в стандартную ветвь. Изменения (они также называются *фиксациями*) хранятся в ветви участника. GitHub использует их для моделирования результатов их *объединения* со стандартной ветвью. Запрос на вытягивание также служит механизмом для предоставления участнику отзыва рецензента запроса. Рецензент отправляет участнику отзыв после процесса сборки и проверки, чтобы решить потенциальные проблемы или вопросы до того, как изменения будут объединены в стандартной ветви.

В зависимости от размера предлагаемых изменений можно воспользоваться двумя способами размещения материалов с помощью запроса на вытягивание. Дополнительные сведения см. в статье [Рабочий процесс для участников GitHub: незначительные или эпизодические изменения](how-to-write-workflows-major.md).

<!---- Reference links for Docs landing pages, associated GitHub repositories, and related Forums matrix. ------------------>
<!---- PLEASE INSERT URLS IN ASCENDING SORT ORDER, AND REMOVE LOCALE SEGMENT FROM URLS (that is, en-us) FOR LOCALIZED FORUMS! -->
<!---- NOTE: these links are saved for future use in another/new article; no longer used above in this article --->
[Visual-Studio-Page]:(https://docs.microsoft.com/en-us/visualstudio/index)
[Visual-Studio-Repo-Internal]:(https://github.com/Microsoft/vsdocs)
[Visual-Studio-Repo-External]:(https://github.com/Microsoft/visualstudio-docs)
[Visual-Studio-SO]: (https://stackoverflow.com/search?q=Visual+Studio+2017)
[Dotnet-Page]: https://docs.microsoft.com/dotnet
[Dotnet-Core-Page]: https://docs.microsoft.com/dotnet/articles/welcome
[Dotnet-Core-Repo]: https://github.com/dotnet/docs
[EM-ATA-Land]: https://docs.microsoft.com/advanced-threat-analytics/
[EM-ATA-Repo]: https://github.com/Microsoft/ATADocs
[EM-AzureAD-Land]: https://docs.microsoft.com/active-directory/
[EM-AzureAD-Repo]: https://github.com/Azure/azure-content/tree/master/articles/active-directory/
[EM-AzureRMS-Land]: https://docs.microsoft.com/rights-management/
[EM-AzureRMS-Repo]: https://github.com/Microsoft/Azure-RMSDocs
[EM-Intune-Land]: https://docs.microsoft.com/intune/
[EM-Intune-Repo]: https://github.com/microsoft/intuneDocs
[EM-Land-Page]: https://docs.microsoft.com/enterprise-mobility/
[EM-Land-Repo]: https://github.com/Microsoft/EMDocs/
[EM-MFA-Land]: https://docs.microsoft.com/multi-factor-authentication/
[EM-MFA-Repo]: https://github.com/Azure/azure-content/tree/master/articles/multi-factor-authentication
[EM-MIM-Land]: https://docs.microsoft.com/microsoft-identity-manager/
[EM-MIM-Repo]: https://github.com/Microsoft/MIMDocs
[EM-RemoteApp-Land]: https://docs.microsoft.com/en-us/remoteapp/
[EM-RemoteApp-Repo]: https://github.com/Azure/azure-content/tree/master/articles/remoteapp
[Forum-MSDN-ATA]: https://social.technet.microsoft.com/Forums/en-US/home?forum=mata
[Forum-MSDN-AzureAD]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=WindowsAzureAD
[Forum-MSDN-AzureRMS]: https://social.technet.microsoft.com/Forums/en-US/home?forum=rmsapps%2Crmscloud&filter=alltypes&sort=lastpostdesc
[Forum-MSDN-EM]: https://social.technet.microsoft.com/Forums/en-US/home?sort=relevancedesc&brandIgnore=True&searchTerm=Enterprise+Mobility
[Forum-MSDN-Intune]: https://social.technet.microsoft.com/Forums/en-us/home?category=microsoftintune
[Forum-MSDN-Main]: https://social.msdn.microsoft.com/Forums/home
[Forum-MSDN-MFA]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=windowsazureactiveauthentication
[Forum-MSDN-MIM]: https://social.technet.microsoft.com/Forums/en-US/home?category=identitymanagement
[Forum-MSDN-RemoteApp]: https://social.technet.microsoft.com/Forums/en-US/home?filter=alltypes&brandIgnore=True&sort=relevancedesc&searchTerm=Azure+Remote+or+RemoteApp
[Forum-SO-AzureAD]: https://stackoverflow.com/questions/tagged/azure-active-directory
[Forum-SO-AzureRMS]: https://stackoverflow.com/questions/tagged/rights-management
[Forum-SO-Dotnet]: https://stackoverflow.com/questions/tagged/.net
[Forum-SO-Dotnet-Core]: https://stackoverflow.com/questions/tagged/.net-core
[Forum-SO-Main]: https://stackoverflow.com/tags
[Forum-SO-Intune]: https://stackoverflow.com/questions/tagged/intune
[Forum-SO-MFA]: https://stackoverflow.com/search?q=%5Bazure%5D+multi-factor
[Forum-SO-MIM]: https://stackoverflow.com/search?q=Microsoft+Identity+Manager
[Forum-SO-RemoteApp]: https://stackoverflow.com/questions/tagged/remoteapp
[Forum-TechNet-Main]: https://social.technet.microsoft.com/Forums/home
[Forum-Yammer-AzureRMS]: https://www.yammer.com/AskIPTeam
[Forum-Yammer-Main]: https://www.yammer.com/
