---
title: Systemgeleitete Clusterkommissionierung
description: Dieses Thema bietet einen Überblick über die systemgesteuerte Clusterauswahl in Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b7ac243a04309a41ab0e06c1b2d4843ae8ac0e22
ms.sourcegitcommit: 7c32e4739c07d825a8562564ea9e78922db2ce38
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2020
ms.locfileid: "3406380"
---
# <a name="system-directed-cluster-picking"></a>Systemgeleitete Clusterkommissionierung

[!include [banner](../includes/banner.md)]

Cluster-Kommissionierung ist ein Stückkommissionierungsprozess, bei dem Sie Artikel für mehrere Bestellungen gleichzeitig kommissionieren können, indem Sie sie zu Kommissionierclustern gruppieren. Sie müssen den Abholort dann nur einmal besuchen. In der Regel wird diese Funktion bei kleinen Kommissioniermengen oder Mengen verwendet, die unter den Fallmengen liegen.

Wenn die systemgesteuerte Cluster-Auswahl eingerichtet ist, können Sie Arbeitskopfzeilen basierend auf einem vom System generierten Cluster auswählen. Das System wählt die Aufträge im Cluster bis zu der Anzahl der Positionen aus, die im Clusterprofil angegeben sind. Daher können Sie mehrere Aufträge gleichzeitig auswählen, ohne manuell einen Cluster erstellen zu müssen.

Die systemgesteuerte Clusterauswahl bietet eine Alternative zur manuellen Clustererstellung, bei der ein Clusterprofil zum Erstellen eines Clusters verwendet wird. Im Cluster-Profil müssen mehrere Einrichtungsbezogene Zeilen definiert werden, bevor es verwendet wird:

- **Anzahl der Positionen** entspricht der Anzahl der Aufträge, die in einem Cluster abgelegt werden. Daher entspricht es der Anzahl der Behälter.
- **Cluster auflösen** legt fest, wann der Cluster aufgelöst werden soll.
- **Cluster-ID generieren** steuert, ob die Cluster-ID vom System generiert oder vom Benutzer eingegeben wird.
- **Prüfungstyp sortieren** bestimmt, ob eine Positionsüberprüfung erforderlich ist.

Ein neuer Menüpunkt für mobile Geräte wird für die systemgesteuerte Cluster-Auswahl verwendet. Die **Cluster-Profil-ID** muss für die Option **Geleitet von** angegeben werden. Darüber hinaus kann die systemgesteuerte Abfragereihenfolge Aufträge basierend auf unternehmensspezifischen Kriterien gruppieren. Daher können Sie die Zuordnung von Arbeitsaufträgen weiter optimieren, indem Sie benutzerdefinierte Sortierkriterien für die systemgesteuerte Abfragesequenz angeben.

Wenn eine systemgesteuerte Cluster-Kommissionierung aktiviert wird, wird den Lagerarbeitern ein Cluster angezeigt, in dem die Kommissionieraufträge den Cluster-Positionen zugewiesen wurden. Daher können Mitarbeiter beginnen, einen Artikel für mehrere Arbeitsaufträge zu kommissionieren, indem sie den Kommissionierort nur einmal besuchen. Der Auswahlprozess für die systemgesteuerte Clusterauswahl ist der gleiche wie für die benutzergesteuerte Clusterauswahl.

## <a name="enable-the-system-directed-cluster-picking-feature"></a>Aktivieren Sie die systemgesteuerte Clusterauswahlfunktion

Bevor Sie diese Funktion nutzen können, müssen Sie diese auf Ihrem System aktivieren. Administratoren können die Seite [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um den Status der Funktion zu überprüfen und sie bei Bedarf zu aktivieren. Hier wird die Funktion als aufgeführt:

- **Module** ‑ Lagerortverwaltung
- **Funktionsname** – Aktivieren Sie die systemgesteuerte Clusterauswahlfunktion

Für diese Funktion muss auch eine abhängige Funktion aktiviert werden. Das abhängige Merkmal ist:

- **Module** ‑ Lagerortverwaltung
- **Funktionsname** – Organisationsweite systemgesteuerte Arbeitssequenzierung

## <a name="set-up-system-directed-cluster-picking"></a>Systemgeleitete Clusterkommissionierung einrichten

### <a name="create-cluster-profiles"></a>Clusterprofile erstellen

Clusterprofile steuern, wie das System die einzelnen Cluster erstellt. Wenn unterschiedliche Cluster erforderlich sind, sollte für jeden Menüpunkt für mobile Geräte ein anderes Clusterprofil erstellt werden.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Clusterprofile**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Cluster-Profil-ID** **2 Position** ein.
4. Geben Sie im Feld **Name** **2 Position** ein.
5. Geben Sie auf dem Inforegister **Allgemein** die folgenden Informationen ein:

    - **Cluster-ID generieren** – Wählen Sie **Ja**. Diese Option legt fest, ob die Cluster-ID automatisch vom System erstellt wird oder ob der Benutzer sie zu Beginn der Kommissionierung erstellt. 
    - **Positionen aktivieren** – Wählen Sie **Ja**. Diese Option legt fest, ob die Positionsnamen basierend auf der Einrichtung des Positionsnamens automatisch generiert werden. Wenn diese Option auf **Nein** festgelegt wird, wird die Ladungsträgerkennung für die Position verwendet.
    - **Maximale Anzahl an Positionen:** Wählen Sie **2**. Dieses Feld bestimmt die maximale Anzahl von Positionen, die der Cluster einnehmen kann (dh die maximale Anzahl von Feldern, Behältern usw.).
    - **Positionsname:** - Wählen Sie **Numerisch** aus, sodass Positionen durch fortlaufende Zahlen benannt werden. Wenn Sie **Alphabetisch** auswählen, sind die Positionen in alphabetischer Reihenfolge benannt.
    - **Cluster unterbrechen bei** - Wählen Sie **Einlagern** aus. Dieses Feld bestimmt, wann der Cluster unterbrochen wird. 
    - **Bestätigungsart sortieren** – Wählen Sie **Positionsscan** aus. In diesem Feld wird festgelegt, ob der Schritt „Positionieren“ überprüft wird.
        
6. Im Inforegister **Cluster-Sortierung** können Sie Sortierkriterien definieren, indem Sie eine neue Zeile erstellen und die folgenden Infornationen festlegen:

    - **Sequenznummer** - Wählen Sie **1**. Dieses Feld bestimmt die Reihenfolge, nach der das System sortiert. Ein Wert wird automatisch eingegeben, aber Sie können ihn nach Bedarf ändern.
    - **Dateiname** - Geben Sie **WMSLocationId** ein. Dieses Feld bestimmt das Feld, das die Zeile zum Sortieren von Kriterien verwendet.
    - **Sortierung** - Wählen Sie **Aufsteigend** aus. Dieses Feld definiert, ob die Sortierung in aufsteigender oder absteigender Reihenfolge erfolgt.

### <a name="create-a-mobile-device-menu-item"></a>Erstellen eines Menüelements für ein mobiles Geräts

Gehen Sie folgendermaßen vor, um ein neues Menüelement für mobile Geräte für die systemgesteuerte Clusterauswahl zu erstellen und die Clusterprofil-ID mit dem Menüelement für mobile Geräte zu verknüpfen.

1. Wechseln Sie zu **Lagerortverwaltung > Einstellungen > Mobiles Gerät > Menüoptionen für mobiles Gerät**.
1. Wählen Sie **Neu** aus.
1. Geben Sie im Bereich Kopfzeile die folgenden Informationen ein:
    - **Name des Menüelements** – SD-Cluster
    - **Titel** – SD-Cluster
    - **Modus** - Arbeit
    - **Vorhandene Arbeit verwenden** – Ja

1. Geben Sie auf dem Inforegister **Allgemein** die folgenden Informationen ein:
    - **Geleitet von** - Systemgeleitete Clusterkommissionierung
    - **Kennzeichen generieren**: - Ja
    - **Clusterprofil-ID** -  Wählen Sie 2 Position aus

1. Richten Sie im Inforegister **Arbeitsklassen** die gültige Arbeitsklasse für diesen Menüpunkt für mobile Geräte ein, indem Sie die folgenden Felder festlegen:
    - **Arbeitsklassenkennung** - Vertrieb
    - **Arbeitsauftragsart** – Kundenaufträge

1. In Aktionsbereich **Menüpunkte für mobile Geräte** wählen Sie **Systemgesteuerte Arbeitsablaufabfragen** und führen Sie die folgenden Schritte aus, um eine neue systemgesteuerte Arbeitssequenzabfrage anzugeben:
    - Wählen Sie **Neu** aus im Aktionsbereich.
    - **Sequenznummer** - 1
    - **Beschreibung** – Arbeitspriorität – Arbeits-ID

1. Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus
1. Wählen Sie die Registerkarte **Sortierung**
1. Wählen Sie **Hinzufügen**, um eine neue Zeile hinzuzufügen, geben Sie dann Folgendes ein:
    - **Tabelle** – Arbeit
    - **Abgeleitete Tabelle** - Arbeit
    - **Feld** - Arbeitspriorität
    - **Suchrichtigung** - Aufsteigend
1. Wählen Sie **Hinzufügen**, um eine zweite Zeile hinzuzufügen, geben Sie dann Folgendes ein:
    - **Tabelle** – Arbeit
    - **Abgeleitete Tabelle** - Arbeit
    - **Feld** - Arbeits-ID
    - **Suchrichtigung** - Aufsteigend

1. Das System sortiert nun die Arbeits-IDs im Cluster zunächst nach Arbeitspriorität und dann nach Arbeits-ID.

### <a name="set-up-a-mobile-device-menu"></a>Menü des mobilen Geräts einrichten

1. Wechseln Sie zu **Lagerortverwaltung > Einstellungen > Mobiles Gerät > Menü für mobiles Gerät**.
1. Fügen Sie das Menüelement **SD Cluster** hinzu, das Sie für ein mobiles Gerät erstellt haben.
1. Wählen Sie das Menü **Ausgehend**.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Scrollen Sie, bis Sie den **SD-Cluster** finden.
1. Wählen Sie **SD-Cluster** der Pfeil, der auf die **Menüstruktur** zeigt, wird aktiviert.
1. Wählen Sie die Schaltfläche **Pfeil** zum Verschieben der Menüpunkte **SD-Cluster** im Menü **Ausgehend**.
1. Wählen Sie **SD-Cluster** von der Liste **Menüstruktur**, wählen Sie dann die Pfeile **NACH OBEN** oder **NACH UNTEN**, um den Menüpunkt an die gewünschte Position im Menü des Mobilgeräts zu verschieben.

## <a name="scenario"></a>Szenario

### <a name="create-picking-work"></a>Entnahmearbeit erstellen

Bevor Sie die systemgesteuerte Cluster-Auswahl einrichten können, müssen Sie geeignete ausgehende Arbeiten erstellen. Das zuvor erstellte Clusterprofil gibt zwei Clusterpositionen an. Daher müssen Sie mindestens zwei Arbeitskennungen erstellen. In diesem Szenario erstellen Sie zwei Kundenaufträge, reservieren Inventar, geben die Kundenaufträge an das Lager frei und verarbeiten die Welle dann manuell.

1. Gehen Sie zu **Vertrieb und Marketing > Aufträge > Alle Aufträge**.
1. Wählen Sie **Neu** im Aktivitätsbereich, um den ersten Verkaufsauftrag zu erstellen.
    - Das Menü **Kundenauftrag erstellen** wird geöffnet, geben Sie folgende Informationen ein:
        - Im Inforegister **Kunde** geben Sie **Kundenkonto** - **US-004** ein.
        - Auf dem Inforegister **Allgemeines** geben Sie ein **Lagerort** - **62** ein.
        - Wählen Sie **OK** aus, um das Menü zu schließen und die Bestellung zu erstellen.
    - Auf dem Inforegister **Kundenauftragspositionen** wählen Sie **Zeile hinzufügen**, wenn eine neue Zeile nicht automatisch hinzugefügt wird, geben Sie Folgendes ein:
        - **Artikelnummer** - A0001
        - **Menge** - 1
        - Wählen Sie **Position hinzufügen** aus, um eine zweite Position hinzuzufügen.
        - **Artikelnummer** - A0002
        - **Menge** - 3
    - Reservieren Sie Bestand für beide Zeilen, die Sie gerade erstellt haben.
        - Wählen Sei **Zeile 1**.
        - Im Aktionsbereich unter **Bestellpositionszeile** wählen Sie **Bestand** und wählen dann **Reservierung** von der Liste aus.
        - Im Formular **Reservierung** wählen Sie **Reservierungs-Los** und reservieren Sie den Bestand.
        - Schließen Sie das Formular **Reservierung** wenn die Reservierung abgeschlossen ist.
        - Wiederholen Sie diese Schritte, um Bestand für **Zeile 2** zu reservieren.
1. Wählen Sie **Neu** im Aktivitätsbereich, um den zweiten Verkaufsauftrag zu erstellen
    - Das Menü **Kundenauftrag erstellen** wird geöffnet, geben Sie folgende Informationen ein:
        - Im Inforegister **Kunde** geben Sie **Kundenkonto** - **US-005** ein.
        - Auf dem Inforegister **Allgemeines** geben Sie ein **Lagerort** - **62** ein.
        - Wählen Sie **OK** aus, um das Menü zu schließen und die Bestellung zu erstellen
    - Auf dem Inforegister **Kundenauftragspositionen** wählen Sie **Zeile hinzufügen**, wenn eine neue Zeile nicht automatisch hinzugefügt wird, geben Sie folgende Informationen ein:
        - **Artikelnummer** - A0001
        - **Menge** - 4
        - Wählen Sie **Position hinzufügen** aus, um eine zweite Position hinzuzufügen.
        - **Artikelnummer** - A0002
        - **Menge** - 2
    - Reservieren Sie Bestand für beide Zeilen, die Sie gerade erstellt haben.
        - Wählen Sei **Zeile 1**.
        - Im Aktionsbereich unter **Bestellpositionszeile** wählen Sie **Bestand** und wählen dann **Reservierung** von der Liste aus.
        - Im Formular **Reservierung** wählen Sie **Reservierungs-Los** und reservieren Sie den Bestand.
        - Schließen Sie das Formular **Reservierung** wenn die Reservierung abgeschlossen ist.
        - Wiederholen Sie diese Schritte, um Bestand für **Zeile 2** zu reservieren.
    - Schließen Sie die Verkaufsaufträge und kehren Sie zur Seite mit der Liste **Alle Verkaufsaufträge** zurück.
1. Suchen Sie die beiden soeben erstellten Kundenaufträge (möglicherweise müssen Sie die Seite aktualisieren). Wählen Sie in der Tabelle beide Kundenaufträge mit dem Häkchen aus.
    - In dem Aktionsbereich **Alle Kundenaufträge** wählen Sie im Aktionsbereich die Option **Lagerort** aus.
    - In der Gruppe **Aktionen** wählen Sie **Freigabe für Lager**, um beide Verkaufsaufträge an das Lager freizugeben.
1. Wenn die Freigabe für den Lagerprozess abgeschlossen ist, wird eine Informationsmeldung angezeigt.
    - Für jeden Kundenauftrag werden Sendungen erstellt.
    - Eine Welle wird erstellt und beide Sendungen werden der Welle zugewiesen. Notieren Sie die **Wellen-ID**.
1. Wechseln Sie zu **Lagerortverwaltung > Ausgehende Wellen > Lieferungswellen > Alle Wellen**.
    - In der Liste **Alle Wellen** finden und wählen Sie die **Wellen-ID**, die Sie im vorherigen Schritt erstellt haben.
    - Aktivieren Sie im Aktivitätsbereich die Registerkarte **Welle**,
    - In der Gruppe **Welle** wählen Sie **Verarbeiten**, um die Welle zu verarbeiten und die **Arbeit** zu erstellen.
    - Nach Abschluss der Verarbeitung werden Informationsnachrichten generiert, die darauf hinweisen, dass die Arbeit erstellt und die Welle gebucht wurde.
1. **Optional**: Gehen Sie zu **Lagerverwaltung > Arbeit > Arbeitsdetails**, um die erstellte Arbeit anzuzeigen. Es werden zwei verschiedene Arbeitskennungen erstellt. Jede Arbeitskennung hat zwei Auswahlzeilen.

### <a name="run-the-mobile-device-flow"></a>Den Ablauf für mobile Geräte ausführen

1. Melden Sie sich beim mobilen Gerät für einen Benutzer im Lager **62** an.
1. Auf dem **Hauptmenü** wählen Sie **Ausgehend**.
1. Wählen Sie im Menü **Ausgehend** **SD-Cluster** aus, um die Auswahl zu initiieren.
    - Ein Cluster wird erstellt, und die beiden zuvor erstellten Arbeits-IDs werden angehängt. Wenn Sie mehr als zwei Arbeits-IDs erstellt haben, werden nur die ersten beiden zum Cluster hinzugefügt. Beachten Sie, dass die Arbeits-IDs in aufsteigender Reihenfolge zum Cluster hinzugefügt werden, wie Sie dies im Abfrage-Setup angegeben haben.

    > [!NOTE]
    > Der neue Cluster wird nur dann automatisch erstellt, wenn zuvor genügend zusätzliche Arbeits-IDs erstellt wurden. Andernfalls wird die folgende Meldung angezeigt: „Es wurde nicht genügend Arbeit für den Cluster gefunden.“

    - Nachdem Sie das Menü ausgewählt haben, wird der erste Auswahlbildschirm angezeigt. Das System aggregiert alle übereinstimmenden Kommissionierzeilen aus den beiden Arbeitskennungen und weist Sie an, den Kommissionierort einmal zu besuchen, damit Sie beide Aufträge mit einer Kommissionierung erfüllen können. Dieser Vorgang erfolgt auf die gleiche Weise wie der Vorgang für die benutzergesteuerte Cluster-Auswahl.

1. Bestätigen Sie den ersten Kommissionierort und Artikel durch Auswahl von **OK**.
    - Die Menge der Kommissionierung ist die Summe der Artikel, die in den Kundenaufträgen im Cluster angezeigt werden.
1. Geben Sie den Positionsnamen (numerisch oder alphabetisch) ein, um zu bestätigen, dass die für die Position ausgewählte Artikelmenge an der richtigen Position platziert wurde.
1. Wiederholen Sie diesen Vorgang, bis alle Mengen ausgewählt und in die richtige Position gebracht wurden.
1. Der letzte Schritt auf dem Mobilgerät besteht darin, den Cluster an den endgültigen Speicherort zu **verschieben**. Wählen Sie **OK**
    - Wenn dieser Einlagerungsvorgang bestätigt wird, wird das Cluster basierend auf dem Wert, den Sie für das Feld **Cluster aufteilen bei** festgelegt haben, geschlossen und aufgeteilt. Arbeitsausweise sind ebenfalls geschlossen.
1. Auf dem Mobilgerät wird die Meldung „Cluster abgeschlossen“ angezeigt.
