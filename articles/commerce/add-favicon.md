---
title: Hinzufügen eines Favicons
description: In diesem Thema wird erläutert, wie ein favicon der Site hinzufügt wird.
author: bicyclingfool
manager: annbe
ms.date: 04/27/2020
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
ms.openlocfilehash: 2d95e8b799c3b89418657342868e0ec7e94a86f9
ms.sourcegitcommit: ce79fb570e299a26a644e29da7ceb5a57a1374e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2020
ms.locfileid: "3295079"
---
# <a name="add-a-favicon"></a>Hinzufügen eines Favicons

[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie ein favicon der Site hinzufügt wird.

## <a name="overview"></a>Übersicht

Ein favicon ist eine kleine Grafikdatei, die auf einer Webbrowserregisterkarte im Browserverlauf der Adressleiste sowie in Lesezeichen oder in den Favoriten angezeigt wird. Es wird empfohlen, ein favicon dem Standort hinzufügen, da es Ihre Marke darstellt und verstärkt und hilft, den Standort von anderen Websites, die Ihre Kunden suchen, zu unterscheiden.

Zwar können Sie mehrere favicons von verschiedenen Größen und Dateitypen Ihrem Standort hinzufügen, dieses Thema behandelt lediglich das Hinzufügen von einem einzelnen favicon. Allerdings werden der gleiche Prozess und Ort verwendet, um weitere favicons hinzuzufügen.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Laden Sie ein favicon in die Anlagensammlung Ihrer Site hoch

Um ein favicon aus der Anlagensammlung zu entfernen, folgen Sie diesen Schritten.

1. Wählen Sie im linken Navigationsbereich **Medienbibliothek**.
1. Wählen Sie in der Befehlsleiste **Hochladen \> Medienelemente hochladen**.
1. Navigieren Sie im Fenster „Datei-Explorer“ zu der Favicon-Bilddatei, die Sie hochladen möchten, wählen Sie sie aus und wählen Sie sie **Öffnen** aus.
1. Geben Sie im Dialogfenster **Medienelement hochladen** den gewünschten Titel und den Alt-Text ein.
1. Wenn Sie das Bild unmittelbar nach dem Hochladen veröffentlichen möchten, markieren Sie das Kontrollkästchen **Medienelemente nach dem Upload veröffentlichen**.

    > [!NOTE]
    > Wenn Sie das Kontrollkästchen **Medienelemente nach dem Hochladen veröffentlichen** aktivieren, müssen Sie auf die Seite **Medienelemente** zurückkehren und das Favicon später manuell veröffentlichen.

1. Wählen Sie **OK**.
1. Im Eigenschaftenbereich auf der rechten Seite, kopieren Sie die öffentliche URL des favicon. Sie werden diese URL später verwenden.

## <a name="create-the-html-for-your-favicon"></a>Erstellen Sie das HTML für Ihr Favicon

Um das HTML für das Favicon zu erstellen, verwenden Sie die folgende HTML-Zeichenfolge. Für das Attribut **href** ersetzen Sie **Öffentliche\_URL\_für\_Ihr\_Favicon** durch die öffentliche URL, die Sie zuvor kopierten.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-page-fragment-that-contains-a-metatag-for-your-favicon"></a>Erstellen Sie ein Seitenfragment, das ein Metatag für Ihr Favicon enthält

Um ein Seitenfragment zu erstellen, das ein Metatag für Ihr Favicon enthält, folgen Sie diesen Schritten.

1. Wechseln Sie zu **Seitenfragmente**, und wählen Sie **Neu** aus.
1. Im Dialogfeld **Neues Seitenfragment** wählen Sie **Metatags** als das das Modul aus, auf dem das Seitenfragment basiert.
1. Geben Sie einen Namen für das Seitenfragment ein, und wählen Sie dann **OK** aus.
1. Wählen Sie in der Fragmenthierarchiestruktur das untergeordnete Element **Standard-Metatags** aus.
1. Im rechten Bereich unter **Metatags** wählen Sie **Hinzufügen** aus, und geben Sie dann die HTML-Zeichenfolge ein, die Sie zuvor für das Favicon erstellt haben. 
1. Wählen Sie **Bearbeiten beenden** aus, und wählen Sie dann **Veröffentlichen** aus, um das Seitenfragment zu veröffentlichen.

## <a name="add-the-metatag-page-fragment-to-the-html-head-section-of-your-pages"></a>Fügen Sie das Metatag-Seitenfragment zum HTML-Kopfbereich Ihrer Seiten hinzu

Um das Metatag-Seitenfragment zum HTML-**Kopf**-Bereich Ihrer Seiten hinzuzufügen, folgen Sie diesen Schritten.

1. Gehen Sie zu **Vorlagen**, öffnen Sie die Vorlage für die Seiten, denen Sie Ihr Favicon hinzufügen möchten, und wählen Sie dann **Bearbeiten** aus.
1. Wählen Sie in der Vorlagenhierarchiestruktur die Auslassungspunkte (**...**)-Schaltfläche rechts neben dem **HTML-Kopf**-Container aus, und wählen Sie dann **Seitenfragment hinzufügen** aus.
1. Im Dialogfeld **Seitenfragment auswählen** wählen Sie das Metatag-Seitenfragment aus, das Sie zuvor erstellt haben, und wählen Sie dann **OK** aus.
1. Wählen Sie **Bearbeiten beenden** aus, und wählen Sie dann **Veröffentlichen** aus, um die Vorlage zu veröffentlichen.

> [!NOTE]
> Wenn Ihre Site mehr als eine Vorlage verwendet, müssen Sie allen das Metatags-Seitenfragment hinzufügen.

Wenn Sie Seiten in der Vorschau anzeigen, die auf der Vorlage basieren, der Sie das Metatags-Seitenfragment hinzugefügt haben, sollten Sie jetzt das Favicon in der Browser-Registerkarte sehen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Hinzufügen eines Logos](add-logo.md)

[Auswählen eines Sitedesigns](select-site-theme.md)

[Arbeiten mit CSS-Überschreibungsdateien](css-override-files.md)

[Hinzufügen einer Begrüßungsnachricht](add-welcome-message.md)

[Hinzufügen eines Urheberrechtshinweises](add-copyright-notice.md)

[Hinzufügen von Sprachen zu Ihrer Website](add-languages-to-site.md)

[Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie](add-telemetry.md)

