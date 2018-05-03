---
title: 'Рабочий процесс для участников GitHub: незначительные или эпизодические изменения'
description: В этой статье описан рабочий процесс по внесению незначительных изменений в статьи на сайте docs.microsoft.com.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 10/06/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 8bde44d502e1942b0870df9dd546a97705c2bb4f
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2018
---
# <a name="github-contribution-workflow-for-minor-or-infrequent-changes"></a>Рабочий процесс для участников GitHub: незначительные или эпизодические изменения

> [!IMPORTANT]
> При работе со всеми репозиториями, используемыми для публикации на сайте docs.microsoft.com, необходимо соблюдать [правила поведения для управляемых компанией Майкрософт сообществ разработки ПО с открытым кодом](https://opensource.microsoft.com/codeofconduct/) и [правила поведения от .NET Foundation](https://dotnetfoundation.org/code-of-conduct). Дополнительные сведения см. на странице с [часто задаваемыми вопросами о правилах поведения](https://opensource.microsoft.com/codeofconduct/faq/). С любыми вопросами и комментариями можно также обратиться по адресу [opencode@microsoft.com](mailto:opencode@microsoft.com) или [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org).<br>
>
> Порядок внесения незначительных изменений или уточнений в документацию и примеры кода из общедоступных репозиториев см. в [условиях использования на сайте docs.microsoft.com](https://docs.microsoft.com/legal/termsofuse). Если новые или значительные изменения вносят не сотрудники корпорации Майкрософт, в комментариях к запросу на вытягивание на сайте GitHub появится предложение принять условия лицензионного соглашения с участником (CLA). Вам нужно заполнить онлайн-форму, после чего мы сможем принять ваш запрос на вытягивание.

## <a name="overview"></a>Общие сведения

Этот рабочий процесс предназначен для внесения незначительных или эпизодических изменений с помощью веб-редактора Markdown editor на сайте GitHub. Возможности редактора GitHub ограничены, так как пользовательский интерфейс не поддерживает все операции и сценарии разработки Git. Если вам нужно внести значительные изменения или получить поддержку по расширенным возможностям Git (например, управление ветвлением или дополнительные варианты устранения конфликтов при слиянии), см. статью о [рабочем процессе по внесению значительных или времязатратных изменений на сайте GitHub](full-workflow.md).

## <a name="procedure-for-using-the-github-editor-to-propose-your-changes"></a>Пошаговые инструкции по предложению изменений с помощью редактора GitHub

1. Перейдите к репозиторию соответствующей статьи на сайте GitHub и файлу Markdown. Для этого можно использовать один из следующих методов:

   - Найдите статью, выполнив поиск по файлам Markdown, в соответствующем репозитории GitHub.
   - Откройте статью на сайте [docs.microsoft.com](https://docs.microsoft.com/), а затем щелкните ссылку **Изменить** в правом верхнем углу страницы.

     ![Расположение ссылки "Изменить"](./media/light-workflow/contributetogit.png)

2. Выберите значок карандаша **Edit this file** (Изменить файл), чтобы перейти в режим редактирования.

    ![Расположение значка карандаша](./media/light-workflow/editicon.png)

3. Внесите изменения на вкладке **Edit file** (Изменение файла), используя редактор Markdown editor, и просмотрите изменения на вкладке **Preview changes** (Просмотр изменений). Использование редактора не должно вызывать трудностей. Но если вам понадобится помощь, ознакомьтесь со следующими руководствами:

   - [Использование разметки Markdown](how-to-write-use-markdown.md)
   - [Creating files on GitHub](https://github.com/blog/1327-creating-files-on-github) (Создание файлов на сайте GitHub)
   - [Upload files to your repositories](https://github.com/blog/2105-upload-files-to-your-repositories) (Отправка файлов в репозитории)

4. Прокрутите страницу вниз, и вы увидите один из следующих элементов:

   - **Propose file change** (Предложить изменение файла). Отображается, если вам предоставлен доступ только на чтение в репозитории, например [Editing files in another user's repository](https://help.github.com/articles/editing-files-in-another-user-s-repository/) (Редактирование файлов в репозитории другого пользователя). В этом случае создается ветвь patch в вилке репозитория GitHub (и автоматически создается сама вилка, если она отсутствует). Щелкнув **Propose file change** (Предложить изменение файла), вы откроете страницу **Comparing changes** (Сравнение изменений), где можно просмотреть внесенные изменения. После этого нажмите кнопку **Create pull request** (Создать запрос на вытягивание), чтобы отправить изменения и поместить запрос на вытягивание в очередь, а затем перейдите к [следующему разделу](#pull-request-processing).

   - **Commit changes** (Внести изменения). Отображается, если вам предоставлены разрешения на запись в репозитории, например [Editing files in your own repository](https://help.github.com/articles/editing-files-in-your-repository/) (Редактирование файлов в собственном репозитории). В таком случае вы можете сохранить изменения на сайте GitHub одним из двух способов:

     - **Commit directly to the `<branch-name>` branch** (Внести изменения непосредственно в ветвь), где `<branch-name>` — это имя ветви, которая была открыта при нажатии кнопки **Edit** (Изменить). В этом случае изменения будут внесены непосредственно в эту ветвь вместо создания запроса на вытягивание. На этом этапе все готово.

     - **Create a new branch for this commit and start a pull request** (Создать новую ветвь для изменений и выполнить запрос на вытягивание) — создает запрос с именем по умолчанию на создание ветви. Щелкнув **Propose file change** (Предложить изменение файла), вы откроете страницу **Comparing changes** (Сравнение изменений), где можно просмотреть внесенные изменения. После этого нажмите кнопку **Create pull request** (Создать запрос на вытягивание), чтобы отправить изменения и поместить запрос на вытягивание в очередь, а затем перейдите к [следующему разделу](#pull-request-processing).

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>Дальнейшие действия

- Чтобы узнать больше о разметке Markdown и синтаксисе расширений Markdown, см. статьи об основных средствах создания документов.
