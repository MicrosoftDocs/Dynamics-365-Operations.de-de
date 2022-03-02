---
title: Verankern
description: In diesem Thema wird erläutert, wie Sie die Verankerung aktivieren und verwenden.
author: GalynaFedorova
ms.date: 07/29/2021
ms.topic: article
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-29
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a17574cccbdf6f26f0453bda67eabaa16d559cd3
ms.sourcegitcommit: 99bde425ade701ef244c6bca6d411aef94a59b3c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/20/2021
ms.locfileid: "7505571"
---
# <a name="anchoring"></a>Verankern

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Details zum Verankerungsprozess. Es beschreibt die erforderliche Konfiguration und die Logik, die ausgeführt wird, wenn ein Lagerarbeiter entweder den Staging- oder den Ladungsplatz ändert.

Mit der Verankerungsfunktion können Sie den Staging- oder Ladungsplatz überschreiben. Alle offenen Einlagerungen werden dann an den neuen Bereitstellungs- oder Ladeort geleitet, den Sie angeben.

Diese Funktion kann den Arbeitern helfen, beim Versenden von Waren effizienter zu sein. Im Folgenden finden Sie einige Beispiele hierfür:

- Eine Arbeitskraft, die einen Artikel für Auftrag 1 in einen Staging-Lagerplatz bei Rampe 1 platzieren muss, diesen Vorgang jedoch nicht abschließen kann, da eine vorherige Ladung nicht vom Lagerplatz entfernt wurde. Anstatt auf den Staginglagerplatz des Docks 1 zu warten, kann die Arbeitskraft festlegen, dass sie den Staginglagerplatz Dock 2 verwendet. Daher wird die Arbeitskraft den vorgeschlagenen bereitgestellten Lagerplatz überschreiben. Der Einlagerungsort für alle verbleibenden Artikel für den Arbeitsauftrag wird dann auf den Staging-Lagerplatz für Rampe 2 aktualisiert.
- Ein Arbeiter, der mehrere Kommissionierungen für dieselbe Lieferung durchführen muss, kann sicher sein, dass alle eingelagerten Artikel am selben Ort montiert werden. Daher wird weniger Zeit benötigt, um die Artikel in den LKW zu laden.

Sie konfigurieren die Verankerung für Menüelemente auf Mobilgeräten, indem Sie die Option **Verankerung** verwenden. Wenn Sie diese Option auf *Ja* festlegen, können Sie das Feld **Verankerung nach** verwenden, um anzugeben, ob Sie nach Lieferung oder Ladung verankern möchten. Wenn Sie das Feld **Verankerung nach** auf *Lieferung* festlegen, werden nachfolgende offene Einlagerungen in den neuen Lagerort für diese Lieferung geändert. Wenn Sie es auf *Ladung* festlegen, werden nachfolgende offene Einlagerungen in den neuen Lagerort für diese Ladung geändert.

> [!IMPORTANT]
> Der Lagerort für nachfolgende offene Einlagerungen wird nur in den Arbeitszeilen geändert, die über dieselbe Arbeitsvorlagenzeile generiert werden. Mit anderen Worten, das System verankert die Einlagerungszeilen, die aus derselben Arbeitsvorlagenzeile stammen.

Dieses Thema enthält ein Szenario, das zeigt, wie die Verankerung funktioniert. Während des Szenarios erstellen Sie einen Satz von Kundenaufträgen und geben diese an das Lager frei. Sie überschreiben dann den vorgeschlagenen Staging-Lagerort und überprüfen, ob alle verbleibenden Einlagerungsarbeiten an den neuen Standort geleitet werden.

## <a name="scenario-prerequisite-make-demo-data-available"></a>Szenariovoraussetzung: Demodaten zur Verfügung stellen

Das Szenario in diesem Thema verweist auf Werte und Datensätze, die in den für Microsoft Dynamics 365 Supply Chain Management bereitgestellten Standarddemodaten enthalten sind. Wenn Sie die hier angegebenen Werte während der Übungen verwenden möchten, müssen Sie in einer Umgebung arbeiten, in der die Demodaten installiert sind, und die juristische Person auf *USMF* festlegen, bevor Sie beginnen.

## <a name="scenario-setup"></a>Szenarioeinrichtung

Bevor Sie das Beispielszenario durcharbeiten, müssen Sie die Verankerung für das entsprechende Menüelement des mobilen Geräts aktivieren.

### <a name="set-up-a-mobile-device-menu-item-to-enable-anchoring"></a>Eine Menüoption auf einem mobilen Gerät zum Aktivieren der Verankerung einrichten

Führen Sie diese Schritte aus, um die Verankerung für ein Menüelement eines mobilen Geräts zu aktivieren.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie im Listenbereich den Datensatz mit der Bezeichnung *Auftragskommissionierung*. Wenn kein Datensatz mit diesem Namen vorhanden ist, erstellen Sie ihn. Bestätigen Sie oder legen Sie die folgenden Werte für den Datensatz fest:

    - **Name des Menüelements:** *Auftragskommissionierung*
    - **Titel:** *Auftragskommissionierung*
    - **Modus:** *Arbeit*
    - **Vorhandene Arbeit verwenden:** *Ja*
    - **Geleitet von:** *Benutzergeleitet*
    - **Verankerung:** *Ja*

        Diese Einstellung bewirkt, dass das System während der Verkaufskommissionierung mehrere Arbeitsauftragspositionen miteinander verankert.

    - **Verankerung durch:** *Ladung*

        Diese Einstellung bewirkt, dass das System durch die Last verankert wird.

    - **Zielladungsträger überschreiben:** *Ja*
    - **Zielladungsträger während Einlagern überschreiben:** *Ja*
    - **Arbeit vom Benutzer gesperrt halten:** *Ja*
    - **Zu hohe Entnahme zulassen:** *Ja*

### <a name="set-up-a-work-template-to-enable-staging"></a>Eine Arbeitsvorlage einrichten, um das Staging zu aktivieren

Befolgen Sie diese Schritte, um eine Arbeitsvorlage zum Aktivieren des Staging zu konfigurieren. Diese Konfiguration unterstützt das Szenario, in dem eine Arbeitskraft Artikel für eine Bestellung an einem Staging-Lagerort einlagert.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.
1. Wählen Sie im Feld **Arbeitsauftragsart** *Arbeitsaufträge* aus.
1. Wählen Sie im Raster die Arbeitsvorlage **61 SO Stage** aus.
1. Stellen Sie im Abschnitt **Details zur Arbeitsvorlage** sicher, dass die folgenden Zeilen vorhanden sind und wie hier gezeigt konfiguriert sind:

    - Position 1:

        - **Arbeitstyp:** *Entnahme*
        - **Obligatorisch:** Ausgewählt (= *Ja*)
        - **Arbeitsklassen-ID:** *SO Kommissionierung*

    - Position 2:

        - **Arbeitstyp:** *Einlagern*
        - **Obligatorisch:** Ausgewählt (= *Ja*)
        - **Richtliniencode:** *Stage*
        - **Arbeitsklassen-ID:** *SO Kommissionierung*

    - Position 3:

        - **Arbeitstyp:** *Entnahme*
        - **Obligatorisch:** Ausgewählt (= *Ja*)
        - **Arbeit beenden:** *Ja*
        - **Arbeitsklassen-ID:** *SO Ladung*

    - Position 4:

        - **Arbeitstyp:** *Einlagern*
        - **Obligatorisch:** Ausgewählt (= *Ja*)
        - **Richtliniencode:** *Frachttür*
        - **Arbeitsklassen-ID:** *SO Ladung*

1. Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus, um den Abfrage-Editor zu öffnen.
1. Stellen Sie auf der Registerkarte **Bereich** sicher, dass die folgenden Zeilen vorhanden sind:

    - **Tabelle:** *Temporäre Arbeitstransaktionen*
    - **Abgeleitete Tabelle:** *Temporäre Arbeitstransaktionen*
    - **Feld:** *Lagerort*
    - **Kriterien:** *61*

1. Stellen Sie auf der Registerkarte **Sortierung** sicher, dass die folgenden Zeilen vorhanden sind:

    - **Tabelle:** *Temporäre Arbeitstransaktionen*
    - **Abgeleitete Tabelle:** *Temporäre Arbeitstransaktionen*
    - **Feld:** *Lieferungs-ID*
    - **Suchrichtigung:** *Aufsteigend*

1. Wählen Sie **OK** aus, um Ihre Einstellungen zu übernehmen und den Abfrage-Editor zu schließen. Akzeptieren Sie die Änderungen, wenn Sie dazu aufgefordert werden.
1. Wählen Sie im Aktivitätsbereich **Arbeitskopfzeilenumbrüche** aus.
1. Stellen Sie in der Position, in der das Feld **Feldname** auf *Lieferungs-ID* gesetzt ist, sicher, dass das Kontrollkästchen **Nach diesem Feld gruppieren** aktiviert ist.

### <a name="set-up-license-plates-locations-and-inventory"></a>Kennzeichen, Lagerorte und Bestand einrichten

Bevor Sie Kundenaufträge und Lieferungen erstellen, müssen Sie sicherstellen, dass die erforderlichen Lagerorte, Kennzeichen und Bestände vorhanden sind.

1. Navigieren Sie zu **Lagerverwaltung \> Einstellungen \> Lagerort \> Kennzeichen**, und erstellen Sie zwei Kennzeichen:

    - MyLP1
    - MyLP2

1. Navigieren Sie zu **Lagerverwaltung \> Einstellungen \> Lagerort \> Orte**, und erstellen Sie die folgenden Orte, falls sie noch nicht vorhanden sind.

    | Lagerhaus | Speicherort   | Lagerplatz-Profilkennung | Zonenkennung   |
    |-----------|------------|---------------------|-----------|
    | 61        | 06A01R2S1B | PICK-06             | FLOOR     |
    | 61        | 06A01R3S1B | PICK-06             | FLOOR     |
    | 61        | STAGE01    | STAGE               | *(Leer)* |
    | 61        | STAGE02    | STAGE               | *(Leer)* |
    | 61        | STAGE03    | STAGE               | *(Leer)* |
    | 61        | STAGE04    | STAGE               | *(Leer)* |

1. Stellen Sie sicher, dass der folgende Bestand verfügbar ist. Wenn Sie den Lagerbestand anpassen müssen, können Sie manuelle Bewegungen erstellen, Wiederbeschaffung verwenden oder einen anderen Flow verwenden.

    | Artikelnummer | Menge | Lagerhaus | Speicherort   | Ladungsträger |
    |-------------|----------|-----------|------------|---------------|
    | A0001       | 100      | 61        | 06A01R2S1B | MyLP1         |
    | A0002       | 100      | 61        | 06A01R3S1B | MyLP2         |

### <a name="create-demand"></a>Bedarf erstellen

Bevor Sie die Verankerungsfunktion testen können, müssen Sie einen Bedarf erstellen. Für dieses Szenario erstellen Sie drei Kundenaufträge für denselben Kunden.

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie **Neu** aus, um den ersten Auftrag zu erstellen.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - **Debitorenkonto:** *US-001*
    - **Lagerort:** *61*

1. Wählen Sie **OK** aus.
1. Der neue Auftrag wird geöffnet. Er enthält eine leere Position im Inforegister **Auftragspositionen**. Stellen Sie die folgenden Werte für diese Zeile ein:

    - **Artikelnummer** *A001*
    - **Menge** *1*

1. Wählen Sie auf der Symbolleiste **Position hinzufügen** aus, um eine zweite Auftragszeile hinzuzufügen, und legen Sie dafür die folgenden Werte fest:

    - **Artikelnummer:** *A0002*
    - **Menge** *1*

1. Befolgen Sie diese Schritte für jede Verkaufsposition in der Bestellung, um Bestand dafür zu reservieren:

    1. Wählen Sie auf dem Inforegister **Verkaufsauftragszeilen** eine Auftragszeile aus.
    1. Wählen Sie auf der Symbolleiste **Bestand \> Reservierung** aus.
    1. Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus, und schließen Sie dann die Seite.
    1. Wählen Sie im Aktionsbereich **Speichern** aus.

1. Wiederholen Sie die Schritte 2 bis 6, um einen zweiten Auftrag zu erstellen. Stellen Sie dafür die folgenden Werte ein:

    - Im Dialogfeld **Kundenauftrag erstellen**:

        - **Debitorenkonto:** *US-001*
        - **Lagerort:** *61*

    - In Auftragsposition 1:

        - **Artikelnummer** *A001*
        - **Menge** *2*

    - In Auftragsposition 2:

        - **Artikelnummer:** *A0002*
        - **Menge** *2*

1. Wiederholen Sie Schritt 7, um jede Position in Kundenauftrag 2 zu reservieren.
1. Wiederholen Sie die Schritte 2 bis 6, um einen dritten Auftrag zu erstellen. Stellen Sie dafür die folgenden Werte ein:

    - Im Dialogfeld **Kundenauftrag erstellen**:

        - **Debitorenkonto:** *US-001*
        - **Lagerort:** *61*

    - In Auftragsposition 1:

        - **Artikelnummer** *A001*
        - **Menge** *3*

    - In Auftragsposition 2:

        - **Artikelnummer:** *A0002*
        - **Menge** *3*

1. Wiederholen Sie Schritt 7, um jede Position in Kundenauftrag 3 zu reservieren.

### <a name="use-the-load-planning-workbench-to-create-a-load-and-release-it-to-the-warehouse"></a>Verwenden Sie die Ladungsplanungs-Workbench, um eine Ladung zu erstellen und an das Lager freizugeben.

Befolgen Sie diese Schritte, um eine Ladung für die Aufträge zu erstellen, die Sie für dieses Szenario erstellt haben, und geben Sie sie dann an den Lagerort frei.

1. Wechseln Sie zu **Transportverwaltung \> Planung \> Ladungsplanungsworkbench**.
1. Suchen Sie auf der Registerkarte **Vertriebszeilen** alle Auftragszeilen für Auftrag 1 und Auftrag 2 und wählen Sie sie aus.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Angebot und Nachfrage** in der Gruppe **Hinzufügen** die Option **Zu neuer Ladung** aus.
1. Wählen Sie im Dialogfeld **Vorlagenzuordnung** im Feld **Ladungsvorlagen-ID** eine Ladevorlage aus, wie z. B. *Standardladungsvorlage*.
1. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.
1. Suchen Sie im Abschnitt **Ladungen** die Ladung, die Sie erstellt haben, und wählen Sie sie aus.
1. Wählen Sie auf der Symbolleiste **Freigabe \> Freigabe an Lagerort** aus.
1. Wählen Sie im Dialogfeld **Ladung an Lager freigeben** die Option **OK** aus, um die ausgewählte Ladung an den Lagerort freizugeben.
1. Wechseln Sie zu **Lagerverwaltung \> Arbeit \> Alle Arbeit**, um die erstellte Arbeit anzuzeigen. Sie sollten zwei neue Arbeits-IDs finden, eine für jede Lieferung. Jede Arbeits-ID verfügt über Kommissionierungs- und Einlagerungsorte, die Inventar von den Kommissionierorten zum Staging-Lagerort und vom Staging-Lagerort zur Frachttür bringen. Notieren Sie sich den Wert von **Arbeitskennung** für die erste Lieferung, da Sie ihn in der nächsten Prodzedur benötigen werden.

### <a name="sales-order-picking-to-the-staging-location-for-the-first-shipment"></a>Kommissionierung von Kundenaufträgen zum Staging-Lagerort für die erste Lieferung

1. Melden Sie sich bei der Warehouse Management Mobile App als Arbeitskraft im Lagerort *61* an. (Sie können sich bei den Standard-Demo-Daten mit _61_ als Benutzer-ID und _1_ als Kennwort anmelden.)
1. Auf dem Hauptmenü wählen Sie **Ausgehend**.
1. Auf dem Menü **Ausgehend** wählen Sie **Verkaufsauswahl**.
1. Wählen Sie das Feld **ID** aus, und geben Sie dann die Arbeits-ID für die erste Ladung ein.
1. Bestätigen Sie Ihre Eingabe.
1. Geben Sie im Feld **LP** eine Kennzeichnung für den ersten Artikel ein (*MyLP1*).
1. Bestätigen Sie Ihre Eingabe.
1. Geben Sie im Feld **Ziel-LP** eine Zahl ein (die Zielkennung muss nicht bereits vorhanden sein).

    Sie wählen alle Positionen, die aus dem verarbeiteten Zyklus erstellt wurden, auf demselben Zielkennzeichen aus.

1. Bestätigen Sie Ihre Eingabe.
1. Geben Sie im Feld **LP** eine Kennzeichnung für den zweiten Artikel ein (*MyLP2*).
1. Bestätigen Sie Ihre Eingabe.

    Stellen Sie sich vor, die Arbeitskraft hat jetzt die Bestellung abgeholt, aber wenn sie den in der Arbeit angegebenen Staging-Lagerort erreicht, stellt sie fest, dass der Platz bereits belegt ist. Der Mitarbeiter kann jedoch sehen, dass ein anderer Lagerort in der Nähe (*STAGE03*) verfügbar ist. Daher fordert er eine Änderung des Staging-Lagerorts an. Da die Verankerungsfunktion aktiviert ist, aktualisiert das System dann automatisch den Staging-Lagerort für diese und alle damit verbundenen Arbeiten.

1. Wählen Sie **Lagerplatz überschreiben** aus, um den vorgeschlagenen Staging-Lagerort zu überschreiben.
1. Geben Sie im Feld **Arbeitsausnahmen** die Angabe *Staging-Bahn geändert*.
1. Geben Sie im Feld **Lagerort** einen neuen Staging-Lagerort (*STAGE03*) ein.
1. Bestätigen Sie Ihre Eingabe. Sie erhalten die Nachricht „Arbeit abgeschlossen“.
1. Gehen Sie zu **Lagerortverwaltung \> Arbeit \> Alle Arbeiten**.
1. Öffnen Sie die Arbeits-ID für die erste Lieferung. Stellen Sie sicher, dass der Staging-Lagerort auf den neuen Lagerort aktualisiert wurde (*STUFE03*), der mithilfe des mobilen Geräts definiert wurde.
1. Öffnen Sie die Arbeits-ID für die zweite Lieferung. Stellen Sie sicher, dass der Staging-Lagerort auf den neuen Staging-Lagerort (*STUFE03*) aufgrund der Verankerungseinrichtung aktualisiert wurde.

> [!NOTE]
> Der Lagerort für alle verbleibenden offenen Arbeitszeilen, die denselben Staging-Lagerort haben und aus derselben Arbeitsvorlagenzeile generiert wurden, wird auf den neuen Lagerort aktualisiert.

### <a name="use-the-load-planning-workbench-to-add-the-new-sales-order-to-the-existing-load"></a>Die Ladungsplanung-Workbench zum Hinzufügen neuer Aufträge zur vorhandenen Ladung verwenden

Führen Sie diese Schritte aus, um der Ladung einen Auftrag hinzuzufügen und ihn dann an das Lager freizugeben.

1. Wechseln Sie zu **Transportverwaltung \> Planung \> Ladungsplanungsworkbench**.
1. Suchen Sie auf der Registerkarte **Vertriebszeilen** alle Auftragszeilen für Auftrag 3 und wählen Sie sie aus.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Angebot und Nachfrage** in der Gruppe **Hinzufügen** die Option **Zur vorhandenen Ladung** aus, um die ausgewählten Auftragszeilen einer vorhandenen Ladung hinzuzufügen.
1. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.
1. Suchen Sie im Abschnitt **Ladungen** die Ladung aus dem vorherigen Schritt und wählen Sie sie aus.
1. Wählen Sie **Freigabe \> Freigabe an Lagerort**.
1. Wählen Sie im Dialogfeld **Ladung an Lager freigeben** die Option **OK** aus, um die ausgewählte Ladung an den Lagerort freizugeben.
1. Wechseln Sie zu **Lagerverwaltung \> Arbeit \> Alle Arbeit**, um die erstellte Arbeit anzuzeigen. Notieren Sie sich den Wert von **Arbeitskennung**, da Sie ihn in der nächsten Prodzedur benötigen werden..

### <a name="sales-order-picking-to-the-staging-location-for-the-third-shipment"></a>Kommissionierung von Kundenaufträgen zum Staging-Lagerort für die dritte Lieferung

1. Melden Sie sich bei der mobilen App als eine Arbeitskraft im Lagerort *61* an.
1. Auf dem Hauptmenü wählen Sie **Ausgehend**.
1. Auf dem Menü **Ausgehend** wählen Sie **Verkaufsauswahl**.
1. Wählen Sie das Feld **ID** aus, und geben Sie dann die Arbeits-ID für die dritte Ladung ein.
1. Bestätigen Sie Ihre Eingabe.
1. Geben Sie im Feld **LP** eine Kennzeichnung für den ersten Artikel ein (*MyLP1*).
1. Bestätigen Sie Ihre Eingabe.
1. Geben Sie im Feld **Ziel-LP** eine Zahl ein (die Zielkennung muss nicht bereits vorhanden sein).
1. Bestätigen Sie Ihre Eingabe.
1. Geben Sie im Feld **LP** eine Kennzeichnung für den zweiten Artikel ein (*MyLP2*).
1. Bestätigen Sie Ihre Eingabe.

    Stellen Sie sich bei der ersten Ladung vor, dass die Arbeitskraft feststellt, dass der angegebene Staging-Lagerort nicht verfügbar ist. Daher möchte sie einen anderen Staging-Lagerort verwenden (*STAGE04*).

1. Wählen Sie **Lagerplatz überschreiben** aus, um den vorgeschlagenen Staging-Lagerort zu überschreiben.
1. Geben Sie im Feld **Arbeitsausnahmen** die Angabe *Staging-Bahn geändert*.
1. Geben Sie im Feld **Lagerort** einen neuen Staging-Lagerort (*STAGE04*) ein.
1. Bestätigen Sie Ihre Eingabe. Sie erhalten die Nachricht „Arbeit abgeschlossen“.
1. Gehen Sie zu **Lagerortverwaltung \> Arbeit \> Alle Arbeiten**.
1. Öffnen Sie die Arbeits-ID für die erste Lieferung. Stellen Sie sicher, dass der Staging-Lagerort nicht auf den neuen Staging-Lagerort aktualisiert wurde (*STAGE04*), da die verbleibende offene Einlagerungszeile nicht der Arbeitsvorlagenzeile der abgeschlossenen Einlagerungszeile entspricht.
1. Öffnen Sie die Arbeits-ID für die zweite Lieferung. Überprüfen Sie, dass der Staging-Lagerort nicht auf den neuen Staging-Lagerort aktualisiert wurde (*STAGE04*), da der Staging-Lagerort nicht mit dem Staging-Lagerort der abgeschlossenen Einlagerungszeile übereinstimmt. Mit anderen Worten, die abgeschlossene Arbeitszeile und die verbleibende offene Arbeitszeile haben unterschiedliche Staging-Lagerorte, und in diesem Fall werden nur Zeilen aktualisiert, die dieselben Staging-Lagerorte haben.
1. Öffnen Sie die Arbeits-ID für die dritte Lieferung. Stellen Sie sicher, dass der Staging-Lagerort auf den neuen Staging-Lagerort (*STAGE04*) aktualisiert wurde.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
