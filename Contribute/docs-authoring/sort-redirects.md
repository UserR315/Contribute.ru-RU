---
title: Сортировка перенаправлений — Docs Authoring Pack
description: Узнайте, как сортировать перенаправления с помощью Docs Authoring Pack — расширения Visual Studio Code.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4924c631c8720743c283083e53b3a1e9af86b00a
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336688"
---
# <a name="sort-redirects"></a>Сортировка перенаправлений

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Сводка

В результате развития набора документации docs.microsoft.com некоторые файлы Markdown в конечном итоге будут удалены. При удалении файла Markdown необходимо предоставить перенаправление, чтобы любая ссылка на удаленную статью правильно разрешалась через перенаправление. Перенаправления указываются в файле *.openpublishing.redirection.json*.

1. Откройте палитру команд, нажмите клавишу <kbd>F1</kbd> (или <kbd>⇧⌘P</kbd> на macOS).
1. Тип: **Документация. Сортировка главного файла перенаправления**
1. Выберите команду для выполнения
1. Обратите внимание на изменения в файле *.openpublishing.redirection.json*

## <a name="considerations"></a>Рекомендации

Файл *.openpublishing.redirection.json* был создан по принципу гирляндной цепи. Со временем файлы, добавленные в качестве перенаправления, будут устаревать. Это происходит, когда файл A удаляется и ему требуется перенаправление на файл Б, затем файл Б удаляется и перенаправляется на файл В. В идеале обе записи будут указывать на В, чтобы существовало перенаправление на файл В из файлов А и Б. Это незначительное увеличение производительности, и эта функция активно разрабатывается.

## <a name="in-action"></a>В действии

Ниже приведена краткая демонстрация этой функции.

[![Демонстрация сортировки перенаправлений](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)
