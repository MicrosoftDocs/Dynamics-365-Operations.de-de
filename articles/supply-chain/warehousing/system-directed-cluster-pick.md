---
title: Systemgeleitete Clusterkommissionierung
description: Dieses Thema bietet einen Überblick über die systemgesteuerte Clusterauswahl in Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
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
ms.openlocfilehash: 390e0a3379a6482e99a13f4f7835b5264e3747ac
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217240"
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

Ein neuer Menüpunkt für mobile Geräte wird für die systemgesteuerte Cluster-Auswahl verwendet. Die Cluster-Profil-ID muss für die Option **Geleitet von** angegeben werden. Darüber hinaus kann die systemgesteuerte Abfragereihenfolge Aufträge nach unternehmensspezifischen Kriterien gruppieren. Daher können Sie die Zuordnung von Arbeitsaufträgen weiter optimieren, indem Sie benutzerdefinierte Sortierkriterien für den systemgesteuerten Abfrageauftrag angeben.

Wenn eine systemgesteuerte Cluster-Kommissionierung durchgeführt wird, wird den Lagerarbeitern ein Cluster angezeigt, in dem die Kommissionieraufträge den Cluster-Positionen zugewiesen wurden. Daher können Mitarbeiter beginnen, einen Artikel für mehrere Arbeitsaufträge zu kommissionieren, indem sie den Kommissionierort nur einmal besuchen. Der Auswahlprozess für die systemgesteuerte Clusterauswahl ist der gleiche wie für die benutzergesteuerte Clusterauswahl.

## <a name="set-up-system-directed-cluster-picking"></a>Systemgeleitete Clusterkommissionierung einrichten

### <a name="create-cluster-profiles"></a>Clusterprofile erstellen

Clusterprofile steuern, wie das System die einzelnen Cluster erstellt. Wenn unterschiedliche Cluster erforderlich sind, sollte für jeden Menüpunkt für mobile Geräte ein anderes Clusterprofil erstellt werden.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Clusterprofile**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Cluster-Profil-ID** **2 Position** ein.
4. Geben Sie im Feld **Name** **2 Position** ein.
5. Legen Sie im Inforegister **Allgemein** die folgenden Felder fest:

    - **Cluster-ID generieren:** Legen Sie diese Option auf **Ja** fest. Diese Option legt fest, ob die Cluster-ID automatisch vom System erstellt wird oder ob der Benutzer sie zu Beginn der Kommissionierung erstellt.
    - **Positionen aktivieren:** Setzen Sie diese Option auf **Ja**. Diese Option legt fest, ob die Positionsnamen basierend auf der Einrichtung des Positionsnamens automatisch generiert werden. Wenn diese Option auf **Nein** festgelegt wird, wird die Ladungsträgerkennung für die Position verwendet.
    - **Maximale Anzahl an Positionen:** Geben Sie **2** ein. Dieses Feld bestimmt die maximale Anzahl von Positionen, die der Cluster einnehmen kann (dh die maximale Anzahl von Feldern, Behältern usw.).
    - **Positionsname:** Wählen Sie **Numerisch** aus, sodass Positionen durch fortlaufende Zahlen benannt werden. Wenn Sie **Alphabetisch** auswählen, sind die Positionen in alphabetischer Reihenfolge benannt.
    - **Cluster unterbrechen um:** Wählen Sie **Einlagern** aus. Dieses Feld bestimmt, wann der Cluster unterbrochen wird.
    - **Bestätigungsart sortieren:** Wählen Sie **Positionsscan** aus. In diesem Feld wird festgelegt, ob der Schritt „Positionieren“ überprüft wird.

6. Im Inforegister **Cluster-Sortierung** können Sie Sortierkriterien definieren, indem Sie eine neue Zeile erstellen und die folgenden Felder festlegen:

    - **Sequenznummer:** Dieses Feld bestimmt die Reihenfolge, nach der das System sortiert. Ein Wert wird automatisch eingegeben, aber Sie können ihn nach Bedarf ändern.
    - **Dateiname:** Wählen Sie **WMSLocationId** aus. Dieses Feld bestimmt das Feld, das die Zeile zum Sortieren von Kriterien verwendet.
    - **Sortierung:** Wählen Sie **Aufsteigend** aus. Dieses Feld definiert, ob die Sortierung in aufsteigender oder absteigender Reihenfolge erfolgt.

### <a name="create-a-mobile-device-menu-item"></a>Erstellen eines Menüelements für ein mobiles Geräts

Gehen Sie folgendermaßen vor, um ein neues Menüelement für mobile Geräte für die systemgesteuerte Clusterauswahl zu erstellen und die Clusterprofil-ID mit dem Menüelement für mobile Geräte zu verknüpfen.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Name des Menüelements** die Option **SD-Cluster** ein.
4. Geben Sie im Feld **Titel** die Option **SD-Cluster** ein.
5. Wählen Sie im Feld **Modus** **Arbeit**.
6. Legen Sie die **Vorhandene Arbeit verwenden**-Option mit **Ja** fest.
7. Legen Sie im Inforegister **Allgemein** die folgenden Felder fest:

    - **Geleitet von:** Wählen Sie **Systemgeleitet** aus.
    - **Ladungsträger generieren:** Legen Sie diese Option auf **Ja** fest.
    - **Clusterprofil-ID:** Wählen Sie **2 Position** aus.

8. Richten Sie im Inforegister **Arbeitsklassen** die gültige Arbeitsklasse für diesen Menüpunkt für mobile Geräte ein, indem Sie die folgenden Felder festlegen:

    - **Arbeitsklassenkennung:** Stellen Sie sicher, dass **Umsatz** eingegeben wurde.
    - **Arbeitsauftragstyp:** Stellen Sie sicher, dass **Arbeitsauftrag** eingegeben wurde.

9. Führen Sie die folgenden Schritte aus, um eine neue systemgesteuerte Arbeitssequenzabfrage anzugeben:

    1. Wählen Sie **Neu** aus.
    2. Geben Sie im Feld **Laufende Nummer** den Wert **1** ein.
    3. Wählen Sie im Feld **Beschreibung** die Option **Arbeitspriorität – Arbeits-ID** aus.

10. Wählen Sie im Menü **Abfrage bearbeiten** aus.
11. Legen Sie auf der Registerkarte **Sortierung** die folgenden Felder fest:

    - **Tabelle:** Wählen Sie **Arbeit** aus.
    - **Abgeleitete Tabelle:** Wählen Sie **Arbeit** aus.
    - **Feld:** Wählen Sie **Arbeitspriorität** aus.
    - **Suchrichtigung:** Wählen Sie **Aufsteigend** aus.
    - **Tabelle:** Wählen Sie **Arbeit** aus.
    - **Abgeleitete Tabelle:** Wählen Sie **Arbeit** aus.
    - **Feld:** Wählen Sie **Arbeitskennung** aus.
    - **Suchrichtigung:** Wählen Sie **Aufsteigend** aus.

Das System sortiert nun die Arbeits-IDs im Cluster zunächst nach Arbeitspriorität und dann nach Arbeits-ID.

### <a name="set-up-a-mobile-device-menu"></a>Menü des mobilen Geräts einrichten

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menü für mobiles Gerät**.
2. Fügen Sie den soeben erstellten Menüeintrag zum gewünschten Menü hinzu.

## <a name="example"></a>Beispiel

### <a name="create-picking-work"></a>Entnahmearbeit erstellen

Bevor Sie die systemgesteuerte Cluster-Auswahl einrichten können, müssen Sie geeignete ausgehende Arbeiten erstellen. Das zuvor erstellte Clusterprofil gibt zwei Clusterpositionen an. Daher müssen Sie mindestens zwei Arbeitskennungen erstellen.

1. Gehen Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
2. Wählen Sie **Neu** aus, um einen Auftrag zu erstellen.
3. Wählen Sie im Feld **Debitorenkonto** einen Debitor aus.
4. Wählen Sie auf dem Inforegister **Allgemein** im Feld **Lagerort** den Lagerort **62** aus.
5. Wählen Sie **OK**.
6. Wählen Sie im Inforegister **Auftragspositionen** die Option **Position hinzufügen** aus.
7. Wählen Sie im Feld **Artikelnummer** die Option **A0001** aus.
8. Geben Sie im Feld **Menge** den Wert **1** ein.
9. Wählen Sie **Position hinzufügen** aus, um eine zweite Position hinzuzufügen.
10. Wählen Sie im Feld **Artikelnummer** die Option **A0002** aus.
11. Geben Sie im Feld **Menge** den Wert **3** ein.
12. Wiederholen Sie die Schritte 2 bis 6.
13. Wählen Sie im Feld **Artikelnummer** die Option **A0001** aus.
14. Geben Sie im Feld **Menge** den Wert **4** ein.
15. Wählen Sie **Position hinzufügen** aus, um eine zweite Position hinzuzufügen.
16. Wählen Sie im Feld **Artikelnummer** die Option **A0002** aus.
17. Geben Sie im Feld **Menge** den Wert **2** ein.

Reservieren Sie das Inventar und geben Sie es an das Lager frei. Es werden zwei verschiedene Arbeitskennungen erstellt. Jede Arbeitskennung hat zwei Auswahlzeilen.

### <a name="run-the-mobile-device-flow"></a>Den Ablauf für mobile Geräte ausführen

1. Wählen Sie auf dem Mobilgerät das Menü aus, das den neuen Menüpunkt für das mobile Gerät enthält.
2. Wählen Sie den Menüpunkt **SD-Cluster** aus, und initiieren Sie die Entnahme. Ein Cluster wird erstellt, und die beiden zuvor erstellten Arbeits-IDs werden angehängt. Wenn Sie mehr als zwei Arbeits-IDs erstellt haben, werden nur die ersten beiden zum Cluster hinzugefügt. Beachten Sie, dass die Arbeits-IDs in aufsteigender Reihenfolge zum Cluster hinzugefügt werden, wie Sie dies im Abfrage-Setup angegeben haben.

    > [!NOTE]
    > Der neue Cluster wird nur dann automatisch erstellt, wenn zuvor genügend zusätzliche Arbeits-IDs erstellt wurden. Andernfalls wird die folgende Meldung angezeigt: „Es wurde nicht genügend Arbeit für den Cluster gefunden.“

    Nachdem Sie das Menü ausgewählt haben, wird der erste Auswahlbildschirm angezeigt. Das System aggregiert alle übereinstimmenden Kommissionierzeilen aus den beiden Arbeitskennungen und weist Sie an, den Kommissionierort einmal zu besuchen, damit Sie beide Aufträge mit einer Kommissionierung erfüllen können. Dieser Vorgang erfolgt auf die gleiche Weise wie der Vorgang für die benutzergesteuerte Cluster-Auswahl.

3. Bestätigen Sie die erste Auswahl. Anschließend müssen Sie den Positionsnamen eingeben, um zu bestätigen, dass die Elemente an die richtige Position gebracht wurden.
4. Wiederholen Sie diesen Vorgang, bis alle Artikel kommissioniert und in die richtige Position gebracht wurden.
5. Der letzte Schritt auf dem Mobilgerät besteht darin, den Cluster an den endgültigen Speicherort zu verschieben. Wenn dieser Einlagerungsvorgang bestätigt wird, wird das Cluster basierend auf dem Wert, den Sie für das Feld **Cluster aufteilen bei** festgelegt haben, geschlossen und beschädigt. Arbeitsausweise sind ebenfalls geschlossen.
6. Auf dem Mobilgerät wird die Meldung „Cluster abgeschlossen“ angezeigt.
