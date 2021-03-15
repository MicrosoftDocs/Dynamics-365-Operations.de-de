---
title: Gruppierung von Kommissionierpositionen
description: In diesem Thema wird eine Übersicht über die Gruppierung von Kommissionierpositionen angezeigt.
author: Mirzaab
manager: tfehr
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: e70244d46ec2787fefdb097d0354af7910b55e9c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989717"
---
# <a name="pick-line-grouping"></a>Gruppierung von Kommissionierpositionen

[!include [banner](../includes/banner.md)]

Die Gruppierung von Entnahmepositionen ermöglicht das Zusammenfassen mehrerer Arbeitspositionen mit demselben Artikel und Lagerplatz zu einer einzigen Entnahmeposition, die dem Benutzer auf einem Mobilgerät angezeigt wird. Dadurch können Lagerarbeiter die effizientesten Anweisungen erhalten, wobei die erforderliche Trennung der Arbeitspositionen (für unterschiedliche Container, Aufträge usw.) weiterhin im System beibehalten werden kann.

## <a name="turn-on-the-pick-line-grouping-feature"></a>Einschalten der Gruppierungsfunktion für Entnahmepositionen

Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können den Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um den Status der Funktion zu prüfen und sie bei Bedarf einzuschalten. Dort wird die Funktion folgendermaßen aufgelistet:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Gruppierung von Entnahmepositionen*

## <a name="set-up-pick-line-grouping"></a>Gruppierung von Kommissionierpositionen einrichten

### <a name="create-a-mobile-device-menu-item"></a>Erstellen eines Menüelements für ein mobiles Geräts

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie im Feld **Menüelementname** den Text *Entnahmepositionen für Warengruppe* ein.
1. Geben Sie im Feld **Titel** den Text *Entnahmepositionen für Warengruppe* ein. Dieser Titel wird im Menü des Mobilgeräts angezeigt.
1. Wählen Sie im Feld **Modus** *Arbeit*.
1. Legen Sie die **Vorhandene Arbeit verwenden**-Option mit *Ja* fest.
1. Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:

    - Wählen Sie im Feld **Geleitet von** die Option *Benutzergesteuert* fest.
    - Legen Sie die Option **Ladungsträger generieren** auf *Ja* fest.
    - Legen Sie die Option **Gruppenentnahme** auf *Ja* fest.
    - Übernehmen Sie für alle verbleibenden Optionen die Standardwerte.

1. Befolgen Sie diese Schritte, um gültige Arbeitsklassen für den Menüpunkt für Mobilgeräte zu konfigurieren:

    1. Wählen Sie im Inforegister **Arbeitsklassen** die Option **Neu** aus.
    2. Wählen Sie im Feld **Arbeitsklassenkennung** entweder die Option *Verkäufe* oder *SO Entnahme* auswählen, je nachdem, welchen Lagerort Sie verwenden. Wählen Sie für dieses Szenario *SO Entnahme* aus.

        Das Feld **Arbeitsauftragstyp** wird automatisch auf *Auftrag* festgelegt.

### <a name="set-up-a-mobile-device-menu"></a>Menü des mobilen Geräts einrichten

Führen Sie die folgenden Schritte aus, um den soeben erstellten Menüpunkt zum Menü **Ausgehend** hinzuzufügen.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menü für mobiles Gerät**.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Im Listenbereich werden alle vorhandenen Menüs für Mobilgeräte angezeigt. Wählen Sie in der Liste *Ausgehend* aus.
1. Suchen Sie in der Liste **Verfügbare Menüs und Menüpunkte** den von Ihnen erstellten Menüpunkt *Entnahmepositionen für Warengruppe* aus.
1. Wählen Sie die Schaltfläche mit dem Pfeil nach rechts aus, um den Menüpunkt *Entnahmepositionen für Warengruppe* in die Liste **Menüstruktur** zu verschieben.
1. Verwenden Sie die Nach-oben- und Nach-unten-Pfeilschaltflächen, um den Menüpunkt an die gewünschte Position in der Menüstruktur zu verschieben.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

### <a name="set-up-a-work-template"></a>Eine Arbeitsvorlage einrichten

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.
1. Wählen Sie im Feld **Arbeitsauftragsart** *Arbeitsaufträge* aus.
1. Suchen Sie im Raster **Übersicht** nach der mit dieser Funktion zu verwendenden Arbeitsvorlage und wählen Sie sie aus. Wählen Sie für dieses Szenario die Vorlage *51 Entnahme zu Plattform* aus.
1. Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.
1. Wählen Sie im Abfrage-Editor-Dialogfeld auf der Registerkarte **Sortierung** die Option **Hinzufügen** aus und legen Sie dann für die neue Zeile die folgenden Werte fest:

    - Wählen Sie in der Spalte **Tabelle** die Option *Temporäre Arbeitstransaktionen* aus.
    - Wählen Sie in der Spalte **Abgeleitete Tabelle** die Option *Temporäre Arbeitstransaktionen* aus.
    - Wählen Sie in der Spalte *Feld* die Option **Artikelnummer** aus.
    - Wählen Sie in der Spalte **Suchrichtung** die Option *Aufsteigend* aus.

1. Wählen Sie **OK** aus, um das Dialogfeld zu schließen und Ihre Auswahl zu speichern.
1. Die folgende Meldung wird angezeigt: „Gruppierung wird zurückgesetzt, fortfahren?“ Wählen Sie **Ja** aus, um fortzufahren.

> [!IMPORTANT]
> Damit die Funktion zum Gruppieren von Auswahlzeilen funktioniert, müssen die Arbeitszeilen nach Artikel-ID sortiert sein. Wenn Zeilen mit denselben Elementen nicht nacheinander sequenziert werden, werden sie nicht gruppiert.

## <a name="example"></a>Beispiel

### <a name="create-picking-work"></a>Entnahmearbeit erstellen

Bevor Sie die Gruppierung von Kommissionierpositionen einrichten können, müssen Sie geeignete ausgehende Arbeiten erstellen.

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie **Neu** aus, um einen Auftrag zu erstellen.
1. Wählen Sie im Feld **Kundenkonto** die Option *US-004* aus.
1. Wählen Sie auf dem Inforegister **Allgemein** im Feld **Lagerort** die Option *51* aus.
1. Wählen Sie **OK**.
1. Fügen Sie im Inforegister **Auftragspositionen** die folgenden sechs Positionen hinzu:

    - **Position 1:** Wählen Sie im Feld **Artikelnummer** die Option *M9200* aus. Geben Sie im Feld **Menge** den Wert *3* ein.
    - **Position 2:** Wählen Sie im Feld **Artikelnummer** die Option *M9201* aus. Geben Sie im Feld **Menge** den Wert *3* ein.
    - **Position 3:** Wählen Sie im Feld **Artikelnummer** die Option *M9202* aus. Geben Sie im Feld **Menge** den Wert *2* ein.
    - **Position 4:** Wählen Sie im Feld **Artikelnummer** die Option *M9200* aus. Geben Sie im Feld **Menge** den Wert *1* ein.
    - **Position 5:** Wählen Sie im Feld **Artikelnummer** die Option *M9200* aus. Geben Sie im Feld **Menge** den Wert *3* ein.
    - **Position 6:** Wählen Sie im Feld **Artikelnummer** die Option *M9202* aus. Geben Sie im Feld **Menge** den Wert *7* ein.

    Hier ist eine Zusammenfassung der Gesamtmengen für jeden Artikel:

    - **Artikel M9200:** *7* Stück
    - **Artikel M9201:** *3* Stück
    - **Artikel M9202:** *9* Stück

1. Bevor Sie die Bestellungen an das Lager freigeben, müssen Sie sicherstellen, dass die Kommissionierstellen über genügend Lagerbestand für alle Artikel in allen Bestellungen verfügen. Überprüfen Sie die Einstellung **Standortrichtlinie**, um zu bestimmen, welche Kommissionierorte für die Kundenauftragskommissionierung verwendet werden. Wenn Sie die Contoso-Demodatenumgebung für Lagerort *51* verwenden, bestätigen Sie, dass Bestand verfügbar ist.

    Sie müssen jetzt den Bestand für jede Position reservieren.

1. Wählen Sie im Inforegister **Auftragspositionen** eine der Positionen aus, die reserviert werden müssen.
1. Wählen Sie im Menü **Lagerbestand** über dem Raster die Option **Reservierung** aus.
1. Wählen Sie auf der Seite **Reservierung** im Aktionsbereich die Option **Los reservieren** aus, um die Reservierung anzuwenden. Schließen Sie nun die Seite.
1. Wiederholen Sie die Schritte 8 bis 10 für die verbleibenden Positionen, die reserviert werden müssen.

    Jetzt müssen Sie den Auftrag für den Lagerort freigeben.

1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.

    Sie erhalten eine Nachricht, die besagt, dass eine Lieferung und eine Welle erstellt wurden und die Welle zur Ausführung in einem Stapel gesendet wurde.

    Wenn die Welle und alle nachgelagerten Einzelvorgänge abgeschlossen wurden, wird für Arbeit mit sechs Positionen eine Arbeitskennung erstellt. Die Zeilen sind nach Artikelnummer sortiert.

1. Wechseln Sie zu **Lagerverwaltung \> Arbeit \> Alle Arbeit**, um die erstellte Arbeit anzuzeigen. Notieren Sie sich den Wert von **Arbeitskennung**, da Sie ihn in der nächsten Prodzedur benötigen werden..

### <a name="initiate-picking-from-the-mobile-device"></a>Initiieren einer Entnahme vom Mobilgerät aus

1. Melden Sie sich beim mobilen Gerät als Benutzer an, der für den Lagerort *51* eingerichtet ist.
1. Wählen Sie auf dem Mobilgerät das Menü aus, das den neuen Menüpunkt für das mobile Gerät enthält. Wählen Sie für dieses Szenario **Ausgehend** aus.
1. Wählen Sie das Menüelement **Entnahmepositionen für Warengruppe** aus, um die Entnahme zu initiieren.
1. Geben Sie den Wert für **Arbeitskennung** ein, den Sie in der vorherigen Prozedur notiert haben.

    Sie sollten einen Entnahmeschritt sehen, in dem alle Entnahmepositionen für den Artikel *M9200* gruppiert sind. Außerdem sollten Sie eine Anweisung zur Entnahme von *7* Stück von Artikel *M9200* erhalten.

    > [!IMPORTANT]
    > Auf dem Mobilgerät wurde die Entnahmearbeit für die drei Entnahmearbeitspositionen zu einem Entnahmeschritt für den Anwender zusammengefasst.

1. Bestätigen Sie den Entnahmeschritt.
1. Wechseln Sie zur Arbeitsseite für die Arbeitskennung. Sie werden feststellen, dass alle drei Entnahmepositionen für Artikel *M9200* gleichzeitig geschlossen wurden.
1. Wechseln Sie zurück zum Mobilgerät und fahren Sie mit der Entnahme fort. Arbeitsposition 4 für Artikel *M9201* sollte angezeigt werden. Da der Auftrag nur eine Arbeitsposition enthielt, gibt es nichts zu aggregieren.
1. Bestätigen Sie den Entnahmeschritt.
1. Der letzte Entnahmeschritt auf dem Mobilgerät fasst die letzten beiden Entnahmepositionen aus dem Arbeitsauftrag zusammen.
1. Führen Sie den Entnahmeschritt für *9* Stück von Artikel *M9202* durch.
1. Bestätigen Sie den Put-Schritt und alle weiteren Pick/Put-Paare, um die Arbeit abzuschließen.

> [!IMPORTANT]
>
> - Arbeitszeilen können nur dann gruppiert werden, wenn sie der Reihe nach vorliegen.
> - Die folgende Funktionalität wird nicht unterstützt:
>
>   - Artikelgewichtsartikel
>
>    Wenn sich auf der Arbeit Catch-Weight-Artikel befinden, erhalten Sie eine Fehlermeldung, bevor Sie mit dem Kommissionieren beginnen.
>
>   - Stückentnahme
>   - Arbeitspositionen mit noch nicht abgeschlossenen Wiederbeschaffungsarbeiten
>   - Zu hohe Entnahme
>   - Artikelneuzuordnung für Entnahme mit unzureichender Menge


[!INCLUDE[footer-include](../../includes/footer-banner.md)]