---
title: Hinzufügen eines Favicons
description: In diesem Thema wird erläutert, wie ein favicon der Site hinzufügt wird.
author: bicyclingfool
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 58cb6c592351a96876532ef53d5d477ff93fafa1
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696990"
---
# <a name="add-a-favicon"></a>Hinzufügen eines Favicons

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie ein favicon der Site hinzufügt wird.

## <a name="overview"></a>Übersicht

Ein favicon ist eine kleine Grafikdatei, die auf einer Webbrowserregisterkarte im Browserverlauf der Adressleiste sowie in Lesezeichen oder in den Favoriten angezeigt wird. Es wird empfohlen, ein favicon dem Standort hinzufügen, da es Ihre Marke darstellt und verstärkt und hilft, den Standort von anderen Websites, die Ihre Kunden suchen, zu unterscheiden.

Zwar können Sie mehrere favicons von verschiedenen Größen und Dateitypen Ihrem Standort hinzufügen, dieses Thema behandelt lediglich das Hinzufügen von einem einzelnen favicon. Allerdings werden der gleiche Prozess und Ort verwendet, um weitere favicons hinzuzufügen.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Laden Sie ein favicon in die Anlagensammlung Ihrer Site hoch

Um ein favicon aus der Anlagensammlung zu entfernen, folgen Sie diesen Schritten.

1. Gehen Sie zu **Anlagen \> Hochladen \> Anlagen hochladen**.
1. Suchen und wählen Sie das favicon auf dem lokalen Dateisystem aus.
1. Geben Sie einen Betreff ein, und wählen Sie dann **OK** aus. 
1. Im Eigenschaftenbereich auf der rechten Seite, kopieren Sie die öffentliche URL des favicon.

> [!NOTE]
> Wenn Sie **Anlagen nach den Hochladen veröffentlichen** auswählen, müssen Sie auf die Seite **Anlagen** zurückkehren und das favicon später manuell veröffentlichen.

## <a name="create-the-html-for-the-favicon"></a>Erstellen Sie das HTML für das favicon

Um das HTML für das favicon zu erstellen, verwenden Sie den folgenden HTML-Ausschnitt. Für **href** ersetzen Sie das Attribut **„Öffentliche\_URL\_für\_Ihr\_favicon“** durch die öffentliche URL, die Sie eben kopierten.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a>Fügen Sie die HTML für das favicon dem \<Kopf\>-Element der Seiten hinzu

Um einen favicon dem Standort hinzuzufügen, nutzen Sie dasselbe Verfahren, das verwendet wird, um einen Typ HTML- oder Skriptelement dem **\<Kopf\>** der Standortsseiten hinzuzufügen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Hinzufügen eines Logos](add-logo.md)

[Auswählen eines Sitedesigns](select-site-theme.md)

[Hinzufügen einer Begrüßungsnachricht](add-welcome-message.md)

[Hinzufügen eines Urheberrechtshinweises](add-copyright-notice.md)

[Hinzufügen von Sprachen zu Ihrer Website](add-languages-to-site.md)

[Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie](add-telemetry.md)

