---
title: Mobiler Arbeitsbereich für Anlagenverwaltung
description: Dieses Thema enthält Informationen zum mobilen Arbeitsbereich „Anlageverwaltung“.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.dyn365.ops.version: 10.0.5
ms.search.validFrom: 2019-08-31
ms.openlocfilehash: 525f21d076027f1bf339e59fd0e346706044839c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428531"
---
# <a name="asset-management-mobile-workspace"></a>Mobiler Arbeitsbereich für Anlagenverwaltung

[!include [banner](../../includes/banner.md)]


Dieses Thema enthält Informationen zum mobilen Arbeitsbereich „Anlageverwaltung“. Mit dem Arbeitsbereich können Benutzer Wartungsanforderungen und Arbeitsaufträge anzeigen und erstellen. Benutzer können auch die zugeordneten Arbeitsauftragseinzelvorgänge in einer Listenansicht anzeigen. Anlagen und funktionale Standorte können auch angezeigt und gesucht werden.


## <a name="overview"></a>Übersicht

Anlagenverwaltung ist ein erweitertes Modul für die Verwaltung von Anlagen und Arbeitsauftragseinzelvorgänge in Dynamics 365 Supply Chain Management. Der mobile Arbeitsbereich **Asset-Management** ermöglicht Benutzern, zugewiesene Arbeitsauftragseinzelvorgänge schnell im mobilen Gerät ihrer Wahl anzuzeigen. Benutzer können auch Wartungsanfragen erstellen und verwalten, Lebenszyklusstatus aktualisieren, und Anlagen und funktionale Standortdetail mit ihrem mobilen Gerät anzeigen.

Insbesondere ermöglicht der mobile Arbeitsbereich für die **Anlagenverwaltung** den Benutzern, die folgenden Aufgaben auszuführen:

- Wartungsanfragen erstellen, anzeigen und bearbeiten, ein Foto machen oder ein vorhandenes Bild an die Wartungsanfrage anhängen, den Lebenszyklusstatus der Wartungsanfrage ändern 
- Arbeitsaufträge erstellen, anzeigen und bearbeiten, ein Foto machen oder ein vorhandenes Bild an den Wartungsauftrag anhängen, den Lebenszyklusstatus der Wartungsanfrage ändern, Wartungsauftragseinzelvorgänge anzeigen
- Zugewiesene Arbeitsauftrageinzelaufträge in einer Kalenderansicht anzeigen
- Arbeitsauftragseinzelvorgänge erstellen, anzeigen und bearbeiten, Anlagenzähler aktualisieren, Wartungsprüflisten anzeigen, Notizen zu Arbeitsauftrageinzelvorgängen anzeigen und bearbeiten, die erforderlichen Werkzeuge für den Arbeitsauftrageinzelvorgang anzeigen.
- Bestimmte Anlagen oder funktionale Standorte anzeigen oder suchen


## <a name="prerequisites"></a>Voraussetzungen

Die Voraussetzungen unterscheiden sich basierend auf der Version von Dynamics 365 Supply Chain Management, die für Ihre Organisation bereitgestellt wurde.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-supply-chain-management"></a>Voraussetzungen, wenn Sie Microsoft Dynamics 365 Supply Chain Management verwenden 
Wenn Microsoft Dynamics 365 Supply Chain Management für Ihre Organisation bereitgestellt wurde, muss der Systemadministrator den mobilen Arbeitsbereich **Anlagenverwaltung** veröffentlichen. Anweisungen finden Sie unter [Einen mobilen Arbeitsbereich veröffentlichen](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

## <a name="download-and-install-the-mobile-app"></a>Herunterladen und Installieren der mobilen App
Laden Sie die mobile App für Dynamics 365 for Unified Operations herunter und installieren Sie diese:

- [Für Android-Smartphones](https://go.microsoft.com/fwlink/?linkid=850662)
- [Für iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Bei der mobile App anmelden
1. Starten Sie die App auf Ihrem mobilen Gerät.

2. Geben Sie die URL Dynamics 365 ein.

3. Bei der erstmaligen Anwendung werden Sie nach Ihrem Benutzernamen und dem Kennwort gefragt. Geben Sie Ihre Anmeldeinformationen ein.

4. Nachdem Sie sich angemeldet haben, werden verfügbare Arbeitsbereiche für Ihr Unternehmen angezeigt. Beachten Sie, dass Sie, wenn Ihr Systemadministrator einen neuen Arbeitsbereich später veröffentlicht, die Liste der mobilen Arbeitsbereiche aktualisieren müssen.

![Abbildung 1](media/am-mobile-01.png)


## <a name="view-assigned-work-order-jobs-in-calendar-view"></a>Zugewiesene Arbeitsauftrageinzelaufträge in Kalenderansicht anzeigen

1. Öffnen Sie auf Ihrem mobilen Gerät den Arbeitsbereich für die **Anlagenverwaltung**.

2. Wählen Sie **Mein Arbeitsauftragseinzelvorgangskalender** aus.

3. Wählen Sie das Datum aus, für das Sie archivierte Arbeitsauftrageinzelvorgänge anzeigen möchten. In der Liste finden Sie die Anlagenkennung und die Kennung des funktionalen Standorts für jeden Arbeitsauftragseinzelvorgang.

4. Wählen Sie einen Arbeitsauftragseinzelvorgang in der Liste aus, um Detail zum Einzelvorgang anzuzeigen: Details zu Anlage und funktionalem Standort sowie andere Navigationslinks, um **Anhänge**, **Prüflisten**, **Tools**, **Anlagenzähler**, **Notizen**, **Erfassungen** anzuzeigen.

![Abbildung 2](media/am-mobile-02.png)


## <a name="create-a-work-order-job"></a>Arbeitsauftrageinzelvorgang erstellen

1. Öffnen Sie auf Ihrem mobilen Gerät den Arbeitsbereich für die **Anlagenverwaltung**.

2. Wählen Sie **Alle Wartungsarbeitsaufträge** aus.

3. Wählen Sie den Arbeitsauftrag aus, für den Sie einen neuen Arbeitsauftragseinzelvorgang erstellen möchten.

4. Wählen Sie die Schaltfläche **Position hinzufügen** aus.

5. Wählen Sie die **Anlage** aus, für die Sie einen Arbeitsauftragseinzelvorgang erstellen möchten.

6. Wählen Sie **Wartungsauftragstyp**, **Wartungsauftragsartenvariante** und **Art** aus.

7. Wählen Sie **Fertig**.

![Abbildung 3](media/am-mobile-03.png)


## <a name="add-attachment-to-a-work-order-job"></a>Einem Arbeitsauftragseinzelvorgang einen Anhang hinzufügen

1. Öffnen Sie auf Ihrem mobilen Gerät den Arbeitsbereich für die **Anlagenverwaltung**.

2. Wählen Sie **Alle Wartungsarbeitsaufträge** aus.

3. Wählen Sie den Arbeitsauftrag > Arbeitsauftragseinzelvorgang aus, dem Sie einen Anhang hinzufügen möchten.
    - Alternativ können Sie auch **Mein Arbeitsauftragseinzelvorgangskalender** oder **Eigene Arbeitsauftragseinzelvorgangsliste** auf der Startseite auswählen, um zur Seite **Arbeitsauftragseinzelvorgangsdetails** zu navigieren.

4. Wählen Sie **Anhänge** auf der Seite **Arbeitsauftragseinzelvorgangsdetails** aus.

5. Sie finden vorhandene Anhänge im Arbeitsauftragseinzelvorgang. Wählen Sie **Anhang hinzufügen** aus.

6. Geben Sie **Name** und **Notizen** für dien Anhang ein.

7. Wählen Sie **Bild auswählen** aus, um ein Foto aus der mobilen Galerie auszuwählen, oder **Foto aufnehmen**, um ein Foto zu machen.

8. Wählen Sie **Fertig**.

![Abbildung 4](media/am-mobile-04.png)


## <a name="view-maintenance-checklist-on-a-work-order-job"></a>Wartungsprüfliste zu einem Arbeitsauftragseinzelvorgang anzeigen

1. Öffnen Sie auf Ihrem mobilen Gerät den Arbeitsbereich für die **Anlagenverwaltung**.

2. Wählen Sie **Alle Wartungsarbeitsaufträge** aus.

3. Wählen Sie den Arbeitsauftrag > Arbeitsauftragseinzelvorgang aus, für den Sie Prüflisten anzeigen möchten.
    - Alternativ können Sie auch **Mein Arbeitsauftragseinzelvorgangskalender** oder **Eigene Arbeitsauftragseinzelvorgangsliste** auf der Startseite auswählen, um zur Seite **Arbeitsauftragseinzelvorgangsdetails** zu navigieren.

4. Wählen Sie **Prüflisten** auf der Seite **Arbeitsauftragseinzelvorgangsdetails** aus.

5. Es wird eine Liste der Prüflistenpositionen angezeigt, die dem Arbeitsauftragseinzelvorgang zugeordnet sind. Wählen Sie eine Prüflistenposition aus, um **Anweisungen** anzuzeigen und **Notizen** hinzuzufügen.

6. Klicken Sie auf die Zurück-Schaltfläche (**<**), um zur vorherigen Seite zurückzugelangen.

![Abbildung 5](media/am-mobile-05.png)


## <a name="view-and-update-asset-counters-on-a-work-order-job"></a>nlagenzähler zu einem Arbeitsauftragseinzelvorgang anzeigen und aktualisieren

1. Öffnen Sie auf Ihrem mobilen Gerät den Arbeitsbereich für die **Anlagenverwaltung**.

2. Wählen Sie **Alle Wartungsarbeitsaufträge** aus.

3. Wählen Sie den Arbeitsauftrag > Arbeitsauftragseinzelvorgang aus, für den Sie Anlagenzähler anzeigen möchten.
    - Alternativ können Sie auch **Mein Arbeitsauftragseinzelvorgangskalender** oder **Eigene Arbeitsauftragseinzelvorgangsliste** auf der Startseite auswählen, um zur Seite **Arbeitsauftragseinzelvorgangsdetails** zu navigieren.

4. Wählen Sie **Anlagenzähler** auf der Seite **Arbeitsauftragseinzelvorgangsdetails** aus.

5. Es wird eine Liste der Anlagenzähler angezeigt, die dem Arbeitsauftragseinzelvorgang zugeordnet sind. Wählen Sie das Bleistiftsymbol in einer Anlagenzählerposition aus, um den Gegenwert zu aktualisieren.

6. Geben Sie einen neuen Gegenwert ein, und wählen Sie **Fertig** aus.

![Abbildung 6](media/am-mobile-06.png)


## <a name="register-consumption-on-a-work-order-job"></a>Verbrauch in einem Arbeitsauftragseinzelvorgang erfassen

1. Öffnen Sie auf Ihrem mobilen Gerät den Arbeitsbereich für die **Anlagenverwaltung**.

2. Wählen Sie **Alle Wartungsarbeitsaufträge** aus.

3. Wählen Sie den Arbeitsauftrag > Arbeitsauftragseinzelvorgang aus, für den Sie Verbrauchserfassungen hinzufügen möchten.
    - Alternativ können Sie auch **Mein Arbeitsauftragseinzelvorgangskalender** oder **Eigene Arbeitsauftragseinzelvorgangsliste** auf der Startseite auswählen, um zur Seite **Arbeitsauftragseinzelvorgangsdetails** zu navigieren.

4. Wählen Sie **Erfassungen** auf der Seite **Arbeitsauftragseinzelvorgangsdetails** aus.

5. Wählen Sie **Stunden hinzufügen** aus, um Arbeitsstundenerfassungen zu erstellen.
    1. Wählen Sie aus der Suche die **Kategorie** aus.
    2. Geben Sie im Feld **Stunden** die Anzahl der Arbeitsstunden ein, die für den Arbeitsauftragseinzelvorgang aufgewendet wurden.
    3. Wählen Sie die geeignete **Positionseigenschaft** aus.
    4. Wählen Sie **Fertig**.

6. Wählen Sie **Artikel hinzufügen** aus, um Artikelerfassungen zu erstellen.
    1. Wählen Sie die **Artikelnummer** aus der Suche aus.
    2. Wählen Sie den **Standort** aus der Suche aus.
    3. Geben Sie die **Menge** der verbrauchten Artikel an.
    4. Wählen Sie **Fertig**.

7. Wählen Sie **Ausgaben hinzufügen** aus, um Ausgabenerfassungen zu erstellen.
    1. Wählen Sie aus der Suche die **Kategorie** aus.
    2. Geben Sie die Menge für die Ausgabenerfassung ein.
    3. Wählen Sie **Verkaufswährung** aus der Suche aus.
    4. Geben Sie den **Einstandspreis** für die Ausgabenerfassung ein.
    5. Wählen Sie **Fertig**.

![Abbildung 7](media/am-mobile-07.png)


## <a name="update-lifecycle-state-on-a-work-order"></a>Lebenszyklusstatus eines Arbeitsauftrags aktualisieren

1. Öffnen Sie auf Ihrem mobilen Gerät den Arbeitsbereich für die **Anlagenverwaltung**.

2. Wählen Sie **Alle Wartungsarbeitsaufträge** aus.

3. Wählen Sie den Arbeitsauftrag aus, für den Sie den Lebenszyklusstatus aktualisieren möchten.

4. Wählen Sie die Schaltfläche **Status aktualisieren** am unteren Bildschirmrand aus.

5. Wählen Sie einen neuen Lebenszyklusstatus aus der Liste aus.

6. Wählen Sie **Fertig**.

![Abbildung 8](media/am-mobile-08.png)


## <a name="create-a-maintenance-request"></a>Eine Wartungsanfrage erstellen

1. Öffnen Sie auf Ihrem mobilen Gerät den Arbeitsbereich für die **Anlagenverwaltung**.

2. Wählen Sie **Alle Wartungsanfragen** aus.

3. Wählen Sie am unteren Bildschirmrand **Aktivitäten** und dann **Wartungsanfrage erstellen** aus.

4. Wenn für Wartungsanfragen in **Anlagenverwaltung** Nummernkreis aktiviert ist, wird das Feld **Wartungsanfrage** ausgeblendet, da es automatisch aufgefüllt wird. Wenn das Feld **Wartungsanfrage** angezeigt wird, geben Sie eine Wartungsanfragenkennung ein.

5. Wählen Sie einen **Wartungsanfragetyp** aus.

6. Geben Sie eine **Beschreibung** für die Wartungsanfrage ein.

7. Wählen Sie die **Anlage** aus, für die Sie eine Anfrage erstellen möchten.

8. Wählen Sie die **Leistungsebene** für die Wartungsanfrage aus.

9. Wählen Sie **Fertig**.

![Abbildung 9](media/am-mobile-09.png)


## <a name="add-attachment-to-a-maintenance-request"></a>Einer Wartungsanforderung einen Anhang hinzufügen

1. Öffnen Sie auf Ihrem mobilen Gerät den Arbeitsbereich für die **Anlagenverwaltung**.

2. Wählen Sie **Alle Wartungsanfragen** aus.

3. Wählen Sie die Wartungsanfrage aus, der Sie einen Anhang hinzufügen möchten.

4. Wählen Sie **Anhänge** am unteren Bildschirmrand aus.

5. Wählen Sie **Anhänge hinzufügen** aus.

6. Geben Sie **Name** und **Notizen** für dien Anhang ein.

7. Wählen Sie **Bild auswählen** aus, um ein Foto aus der mobilen Galerie auszuwählen, oder **Foto aufnehmen**, um ein Foto zu machen.

8. Wählen Sie **Fertig**.

![Abbildung 10](media/am-mobile-10.png)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]