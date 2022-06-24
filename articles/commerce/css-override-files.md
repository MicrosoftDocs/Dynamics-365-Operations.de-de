---
title: Mit CSS-Überschreibungsdateien arbeiten
description: In diesem Artikel wird beschrieben, warum, wann und wie Cascading Style Sheets-Überschreibungsdateien (CSS) Dateien in Microsoft Dynamics 365 Commerce verwendet werden.
author: phinneyridge
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: eaeeee4c9de7293ba94cc836c4d7b62787eca81d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892859"
---
# <a name="work-with-css-override-files"></a>Mit CSS-Überschreibungsdateien arbeiten

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, warum, wann und wie Cascading Style Sheets-Überschreibungsdateien (CSS) Dateien in Microsoft Dynamics 365 Commerce verwendet werden.

Permanente Site-Stile sollten normalerweise über das Thema einer Site verwaltet werden. Designs bilden die grundlegenden CSS- und Stileinstellungen für die Module auf einer beliebigen Seite Ihrer Site. Designs werden mit dem Dynamics 365 Commerce Online Software Development Kit (SDK) erstellt, und sie werden mit Microsoft Dynamics Lifecycle Services (LCS) auf Ihren Websites bereitgestellt. Design-Debugging-Funktionen und Modulschnittstellenkonfigurationen im SDK helfen Site-Entwicklern, anpassbare und zusammenhängende Site-Design-Pakete zu erstellen. Wenn diese Entwurfspakete auf einer Website bereitgestellt werden, können sich die Website-Autoren auf das Erstellen, Bearbeiten und Veröffentlichen von Inhalten konzentrieren, anstatt die Website zu entwickeln.

Angesichts des üblichen Lebenszyklus eines Themas kann die Abhängigkeit von Entwicklern, Stiländerungen über die SDK- und LCS-Bereitstellungspipeline vorzunehmen, in einigen Szenarien untragbar sein. Site-Prototypen oder Hotfixes können mühsam erscheinen, wenn das SDK nicht konfiguriert ist oder Sie keine Zeit haben, auf eine LCS-Bereitstellung zu warten.

In diesen Szenarien können CSS-Überschreibungsdateien hilfreich sein. In den Commerce-Authoring-Tools können authentifizierte Benutzer eine CSS-Datei hochladen, sie in einer Vorschau anzeigen, und sie anschließend aktivieren, um das Design einer Site zu überschreiben. Der Overhead der SDK- oder LCS-Bereitstellung ist nicht erforderlich. Die in einer CSS-Überschreibungsdatei angegebenen Überschreibungen können so klein wie eine Änderung an einem einzelnen Textstil oder so umfangreich wie eine vollständige Markenüberholung sein.

Bevor Sie es CSS-Überschreibungsdateien verwenden, beachten Sie beim Überschreiben von Dateien die folgenden Einschränkungen:

- Nur eine CSS-Überschreibungsdatei kann gleichzeitig auf einer Site aktiv sein. Daher müssen alle aktiven Außerkraftsetzungen in einer einzigen Außerkraftsetzungsdatei vorhanden sein.
- Obwohl Sie eine Vorschau der Überschreibungen in den Commerce-Authoring-Tools anzeigen können, gibt es keine dedizierten Debugging-Funktionen, mit denen Sie die durch die Überschreibungen verursachten Fehler identifizieren können. Mit anderen Worten, verfügen Sie bei Verwendung von CSS-Überschreibungsdateien nicht über dasselbe Toolset, das das SDK für die Modul- und Autorenvalidierung bietet.

Dennoch bieten CSS-Überschreibungsdateien eine schnelle Möglichkeit, ein Design zu prototypisieren oder einen Hotfix zu implementieren, bevor ein vollständiges Design-Update entwickelt und bereitgestellt wird.

## <a name="create-a-css-override-file"></a>Erstellen einer CSS-Überschreibungsdatei

Beim Erstellen einer CSS-Überschreibungsdatei können Sie eine beliebige integrierte Entwicklungsumgebung (IDE), einen Texteditor oder einen Quellcode-Editor verwenden. Ein typischer Ansatz besteht darin, Standard-Web-Debugger in Ihrem Browser zu verwenden, um Stilselektoren, Eigenschaften und Werte auf Ihrer vorhandenen Site zu identifizieren. In den meisten Browsern können Sie Werte ändern und im Debugger eine Vorschau anzeigen. Nachdem Sie die gewünschten Änderungen identifiziert haben, können Sie sie in Ihrer eigenen CSS-Datei speichern.

## <a name="upload-a-css-override-file"></a>Eine CSS-Überschreibungsdatei hochladen

Gehen Sie folgendermaßen vor, um eine CSS-Datei zu Ihrer Site in Commerce hochzuladen.

1. Gehen Sie in den Erstellungstools zu Ihrer Site.
1. Wählen Sie im linken Navigationsbereich **Design** aus.

    > [!NOTE]
    > Abhängig von der Version der verwendeten Commerce-Authoring-Tools müssen Sie möglicherweise **Einstellungen** im Navigationsbereich erweitern, bevor Sie **Design** auswählen können.

1. Wählen Sie oben im Hauptdesignfenster die Registerkarte **CSS überschreiben** aus, soweit noch nicht geschehen.
1. Wählen Sie unter **Verfügbare CSS-Überschreibungen** die Option **CSS-Datei hochladen** aus. Ein Dateiexplorerfenster wird angezeigt.
1. Suchen Sie im Dateiexplorer eine CSS-Datei und wählen Sie sie aus. Klicken Sie dann auf **Öffnen**. Die hochgeladene CSS-Datei erscheint jetzt unter **Verfügbare CSS-Überschreibungen**.

## <a name="preview-a-css-override-file"></a>Vorschau einer CSS-Überschreibungsdatei

Um eine Vorschau einer CSS-Überschreibungsdatei anzuzeigen, bevor Sie diese aktivieren, gehen Sie folgendermaßen vor.

1. Wählen Sie im Navigationsbereich links **Design** aus, und suchen Sie dann auf der Registerkarte **CSS überschreiben** unter **Verfügbare CSS-Überschreibungen** die CSS-Datei, die Sie in der Vorschau anzeigen möchten.
1. Wählen Sie neben dem CSS-Dateinamen die Option **Vorschau der Site**.
1. Wählen Sie im Dialogfeld **URL auswählen** die URL der Site, auf die die Überschreibung angewendet werden soll, und dann **OK** aus.
1. Wenn es verschiedene Varianten für die ausgewählte URL gibt, wählen Sie die gewünschte Variante im Dialogfeld **Vorschau der Variationen** aus, das angezeigt wird.

Ein neuer Browser-Tab oder ein neues Browser-Fenster wird geöffnet, in dem Sie Ihre Stilüberschreibungen für Ihre Site validieren können. Anschließend können Sie die URL für andere authentifizierte Commerce-Benutzer zur Überprüfung und für Feedback freigeben.

## <a name="activate-a-css-override-file-on-your-live-site"></a>Aktivieren einer CSS-Überschreibungsdatei auf Ihrer Live-Site

Nachdem Sie die CSS-Überschreibungsdatei als Vorschau angezeigt und genehmigt haben, können Sie sie auf Ihrer Live-Site aktivieren.

> [!NOTE]
> Nur eine CSS-Überschreibungsdatei kann gleichzeitig auf Ihrer Site aktiv sein. Wenn Sie eine neue Überschreibungsdatei aktivieren, wird die vorherige Überschreibungsdatei deaktiviert. Stellen Sie daher sicher, dass alle erforderlichen Überschreibungen in einer einzigen CSS-Überschreibungsdatei vorhanden sind.

Um eine CSS-Überschreibungsdatei zu aktivieren, gehen Sie folgendermaßen vor.

1. Wählen Sie im Navigationsbereich links **Design** aus, und suchen Sie dann auf der Registerkarte **CSS überschreiben** unter **Verfügbare CSS-Überschreibungen** die CSS-Datei, die Sie aktivieren möchten.
1. Wählen Sie unter dem CSS-Dateinamen die Option **Aktivieren** aus. Die Überschreibungsdatei wird sofort auf Ihrer Live-Site aktiv.

## <a name="deactivate-a-css-override-file-on-your-live-site"></a>Deaktivieren einer CSS-Überschreibungsdatei auf Ihrer Live-Site

Um eine CSS-Überschreibungsdatei auf Ihrer Site zu deaktivieren, gehen Sie folgendermaßen vor.

1. Wählen Sie im Navigationsbereich links **Design** aus, und suchen Sie dann auf der Registerkarte **CSS überschreiben** unter **Verfügbare CSS-Überschreibungen** die CSS-Datei, die Sie deaktivieren möchten.
1. Wählen Sie unter dem CSS-Dateinamen die Option **Deaktivieren** aus. Die Überschreibungsdatei wird sofort auf Ihrer Live-Site inaktiv.

> [!TIP]
> Wählen Sie zum Zugriff auf weitere Optionen für CSS-Überschreibungsdateien die Auslassungspunkte (**...**) neben dem CSS-Dateinamen aus. Die Optionen **Herunterladen**, **Umbenennen** und **Ersetzen** sind nützlich für schnelle Änderungen an vorhandenen CSS-Überschreibungsdateien.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Hinzufügen eines Logos](add-logo.md)

[Sitedesign auswählen](select-site-theme.md)

[Arbeiten Sie mit Stilvoreinstellungen](style-presets.md)

[Hinzufügen eines Favicons](add-favicon.md)

[Hinzufügen eines Urheberrechtshinweises](add-copyright-notice.md)

[Hinzufügen von Sprachen zu Ihrer Website](add-languages-to-site.md)

[Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
