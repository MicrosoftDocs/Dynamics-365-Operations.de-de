---
title: Geplantes Crossdocking
description: In diesem Thema wird das erweiterte geplante Crossdocking beschrieben, bei dem die für eine Bestellung erforderliche Lagerbestandsmenge direkt vom Eingang oder der Erstellung zum richtigen ausgehenden Dock oder Stagingbereich geleitet wird. Der gesamte verbleibende Lagerbestand aus der eingehenden Quelle wird durch den regulären Einlagerungsprozess an den richtigen Lagerort geleitet.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: c28639a4a575f5f356bf947ba8e0aee6bcd256b4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573032"
---
# <a name="planned-cross-docking"></a>Geplantes Crossdocking

[!include [banner](../includes/banner.md)]

In diesem Thema wird das erweiterte geplante Crossdocking beschrieben. Crossdocking ist ein Lagerortprozess, bei dem die für eine Bestellung erforderliche Lagerbestandsmenge direkt vom Eingang oder der Erstellung zum richtigen ausgehenden Dock oder Stagingbereich geleitet wird. Der gesamte verbleibende Lagerbestand aus der eingehenden Quelle wird durch den regulären Einlagerungsprozess an den richtigen Lagerort geleitet.

Durch Crossdocking können Mitarbeiter eingehende Einlagerungen und ausgehende Kommissionierungen vom Lagerbestand überspringen, der bereits für eine ausgehende Bestellung markiert ist. Daher wird die Häufigkeit, mit der der Lagerbestand berührt wird, nach Möglichkeit minimiert. Da weniger Interaktion mit dem System besteht, wird außerdem die Zeit- und Platzersparnis im Lagerortfertigungsbereich erhöht.

Bevor Sie Crossdocking ausführen können, müssen Sie eine neue Crossdocking-Vorlage konfigurieren, in der die Bezugsquelle und andere Anforderungen für das Crossdocking angegeben sind. Beim Erstellen der ausgehenden Bestellung muss die Position mit einer eingehenden Bestellung markiert werden, die denselben Artikel enthält. Sie können das Feld „Richtliniencode“ in der Crossdocking-Vorlage auswählen, ähnlich wie Sie Wiederbeschaffungen und Bestellungen einrichten.

Zum Zeitpunkt des Eingangs eingehender Bestellungen erkennt das Crossdocking-Setup automatisch den Bedarf an Crossdocking und erstellt die Bewegungsarbeit für die erforderliche Menge basierend auf dem Setup der Lagerplatzrichtlinie.

> [!NOTE]
> Lagerbuchungen sind *nicht* unregistriert, wenn Crossdocking-Arbeiten abgebrochen werden, auch wenn die Einstellung für diese Funktion in den Lagerortverwaltungsparametern aktiviert ist.

## <a name="turn-on-the-planned-cross-docking-features"></a>Schalten Sie die Funktionen für das geplante Cross Docking ein

Wenn Ihr System nicht bereits die in diesem Thema beschriebenen Funktionen enthält, gehen Sie zu [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) und schalten Sie die folgenden Funktionen in der folgenden Reihenfolge ein:

1. *Geplantes Crossdocking*
1. *Crossdockingvorlagen mit Lagerplatzrichtlinien*
    > [!NOTE]
    > Diese Funktion aktiviert das **Richtliniencode**, das in der Crossdocking-Vorlage angegeben werden soll, ähnlich wie Sie Wiederaufbauvorlagen einrichten. Durch Aktivieren dieser Funktion können Sie keinen Richtliniencode in die Crossdocking-Arbeitsvorlagenzeilen für die letzte *Einlagern*-Zeile. Dies stellt sicher, dass der endgültige Einlagerungsort während der Arbeitserstellung bestimmt werden kann, bevor Arbeitsvorlagen berücksichtigt werden.

## <a name="setup"></a>Einstellung

### <a name="regenerate-load-posting-methods"></a>Ladebuchungsmethoden erneut generieren

Das geplante Crossdocking wird als Ladebuchungsmethode implementiert. Nachdem Sie die Funktion aktiviert haben, müssen Sie die Methoden erneut generieren.

1. Gehen Sie zu **Lagerortverwaltung \> Einrichtung \> Ladebuchungsmethoden**.
1. Wählen Sie im Aktivitätsbereich **Methoden erneut generieren** aus.

    Wenn die Regeneration abgeschlossen ist, sollte eine Methode mit **Methodenname** im Wert von *planCrossDocking* angezeigt werden.

1. Schließen Sie die Seite.

### <a name="create-a-cross-docking-template"></a>Crossdocking-Vorlage erstellen

1. Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Arbeit \> Crossdocking-Vorlagen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Vorlage zu erstellen.
1. Legen Sie im Header die folgenden Werte fest:

    - **Sequenz:** *1*

        Dieses Feld definiert die Reihenfolge, in der Vorlagen ausgewertet werden.

    - **Crossdocking-Vorlagen-ID:** *51*
    - **Beschreibung:** *Lagerort 51*
    - **Richtlinien zur Bedarfsfreigabe:** *Vor dem Eingang der Lieferung*
    - **Lagerort:** *51*

1. Das Setup im Inforegister **Planung** steuert, wie die Vorlage funktioniert. Legen Sie die folgenden Werte fest:

    - **Bedarfsanforderungen:** *Keine*

        Dieses Feld definiert die Anforderungen des Bedarfslagerbestands. Wenn der Bedarf vor der Freigabe mit der Lieferung verknüpft werden muss, wählen Sie *Markierung* aus. Wenn der Bedarf vor der Freigabe gegen die Lieferung reserviert werden muss, wählen Sie *Auftragsreservierung* aus.

    - **Lagerplatztyp:** *Versandorte*

        In diesem Feld wird definiert, ob für die Crossdocking-Arbeit die Staging-/Ladeorte aus der Sendung oder ob Lagerplatzrichtlinien verwendet werden sollen, um eigene Staging-/Ladeorte zu finden.

    - **Arbeitsvorlage:** Lassen Sie dieses Feld leer.

        Dieses Feld definiert die Arbeitsvorlage, die beim Erstellen von Crossdocking-Arbeiten verwendet werden soll.

    - **Bei Eingang der Lieferung erneut validieren:** *Nein*

        Diese Option definiert, ob die Lieferung während des Eingangs erneut validiert werden soll. Wenn diese Option auf *Ja* festgelegt ist, werden sowohl das maximale Zeitfenster als auch der Ablauftagebereich überprüft.

    - **Richtliniencode:** Lassen Sie dieses Feld leer

        Diese Option wird durch die Funktion *Crossdockingvorlagen mit Lagerplatzrichtlinien* aktiviert. Das System benutzt Lagerplatzrichtlinien, um den besten Lagerplatz zu bestimmen, an den der Bestand beim Crossdocking gebracht werden soll. Sie können sie festlegen, indem Sie jeder relevanten Cross-Docking-Vorlage einen Richtliniencode zuweisen. Beachten Sie, dass bei festgelegtem Richtliniencode das System die Lagerplatzrichtlinie nach dem Richtliniencode sucht, wenn Arbeit erstellt wird. Auf diese Weise können Sie Lagerplatzrichtlinien einschränken, die für eine bestimmte Crossdockingvorlage verwendet werden.

    - **Zeitfenster validieren:** *Ja*

        Diese Option definiert, ob das maximale Zeitfenster ausgewertet werden soll, wenn eine Bezugsquelle ausgewählt wird. Wenn diese Option auf *Ja* festgelegt ist, werden die Felder verfügbar, die sich auf das maximale und minimale Zeitfenster beziehen.

    - **Maximales Zeitfenster:** *5*

        Dieses Feld definiert den maximalen Zeitraum, der zwischen Lieferungseingang und Bedarfsabgang zulässig ist.

    - **Maximale Zeitfenstereinheit:** *Tage*
    - **Minimales Zeitfenster:** *0*

        Dieses Feld definiert den minimalen Zeitraum, der zwischen Lieferungseingang und Bedarfsabgang zulässig ist.

    - **Minimale Zeitfenstereinheit:** *Tage*
    - **Ablauftagebereich:** *0*

        *First Expiry First Out (FEFO)-Kriterien:* Dieses Feld definiert die maximale Anzahl von Tagen zwischen dem Ablaufdatum der ersten ablaufenden Charge, die sich derzeit im Lagerort befindet, und der Charge, die empfangen wird.

1. Geben Sie im Inforegister **Bezugsquellen** die Liefertypen an, die für diese Vorlage gültig sind. Wählen Sie **Neu** aus, und legen Sie dann die folgenden Werte fest:

    - **Sequenznummer:** *1*
    - **Bezugsquelle:** *Bestellung*

> [!NOTE]
> Sie können eine Abfrage einrichten, um zu steuern, wann eine bestimmte Crossdocking-Vorlage verwendet wird. Die Abfrage nach Crossdocking-Vorlagen hat nur die (Artikel-)Tabelle *InventTable* und die innere verknüpfte (WHS-Artikel-)Tabelle *WHSInventTable*. Wenn Sie der Abfrage weitere Tabellen hinzufügen möchten, können Sie sie nur mit *Bestehende Verknüpfungen* oder *Nicht bestehende Verknüpfungen* verknüpfen. Wenn Sie nach den verknüpften Tabellen filtern, wird für jeden übereinstimmenden Datensatz in der verknüpften Tabelle ein Datensatz aus der Haupttabelle abgerufen. Wenn der Verknüpfungstyp *Verknüpfung besteht* ist, endet die Suche, nachdem die erste Übereinstimmung gefunden wurde. Wenn Sie beispielsweise die Auftragspositionstabelle mit der Artikeltabelle verknüpfen, validiert das System Artikel und gibt sie zurück, für die mindestens eine Kundenauftragsposition die definierte Bedingung aufweist. Im Wesentlichen werden die Daten aus der übergeordneten (Artikel-)Tabelle (Artikel) abgerufen, nicht aus der untergeordneten (Auftragspositions-)Tabelle. Daher ist das Filtern nach Quelldokumenten wie Auftragspositionen oder Debitoren nicht sofort möglich.

### <a name="create-a-work-class"></a>Eine Arbeitsklasse erstellen

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsklassen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Arbeitsklasse zu erstellen.
1. Legen Sie die folgenden Werte fest:

    - **Arbeitsklassen-ID:** *CrossDock*
    - **Beschreibung:** *Crossdocking*
    - **Arbeitsauftragstyp:** *Crossdocking*

### <a name="create-a-work-template"></a>Erstellen einer Arbeitsvorlage

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.
1. Legen Sie im Feld **Arbeitsauftragstyp** *Crossdocking* fest.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um auf der Registerkarte **Übersicht** eine Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Sequenznummer:** *1*
    - **Arbeitsvorlage:** *51 Crossdocking*
    - **Arbeitsvorlagenbeschreibung:** *51 Crossdocking*

1. Wählen Sie **Speichern** aus, um das Inforegister **Arbeitsvorlagendetails** verfügbar zu machen.
1. Wählen Sie im Inforegister **Arbeitsvorlagendetails** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Arbeitstyp:** *Entnahme*
    - **Arbeitsklassen-ID:** *CrossDock*

1. Wählen Sie **Neu** aus, um eine weitere Position hinzuzufügen, und legen Sie die folgenden Werte fest:

    - **Arbeitstyp:** *Einlagern*
    - **Arbeitsklassen-ID:** *CrossDock*

1. Wählen Sie **Speichern** aus, und bestätigen Sie, dass das Kontrollkästchen **Gültig** für die Vorlage *51 Crossdocking* ausgewählt ist.
1. Optional: Wählen Sie **Abfrage bearbeiten**, wenn Sie Kriterien festlegen möchten, um zu steuern, wann und wo die Arbeitsvorlage verwendet wird.

    Sie können eine Abfrage einrichten, um zu steuern, wann eine spezifische Arbeitsvorlage verwendet wird. Sie können beispielsweise festlegen, dass eine Vorlage nur für die Arbeit an einem bestimmten Lagerplatz verwendet werden kann. Wenn Sie möchten, dass die Crossdocking-Arbeitsvorlage an einem bestimmten Lagerplatz angewendet wird, müssen Sie nach dem Feld **Ausgangslagerplatz** nicht dem Feld **Lagerplatz** filtern, da die Arbeitserstellung für die eingehenden Prozesse (Kauf, Crossdocking und Wiederbeschaffung) von der Einlagerungsposition aus beginnt. Wenn Arbeit erstellt wird, legt die Lagerplatzrichtlinie das Feld **Lagerplatz** auf den Einlagerungslagerplatz festlegt. Der Entnahmelagerplatz wird jedoch im Feld **Ausgangslagerort** gespeichert.

> [!NOTE]
> Die Arbeitsklassen-IDs für die Arbeitstypen *Entnehmen* und *Einlagern* müssen gleich sein.

### <a name="create-location-directives"></a>Lagerplatzrichtlinien erstellen

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.
1. Legen Sie im linken Bereich im Feld **Arbeitsauftragstyp** *Crossdocking* fest.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, und legen Sie die folgenden Werte fest:

    - **Sequenznummer:** *1*
    - **Name:** *51 Crossdocking einlagern*
    - **Arbeitstyp:** *Einlagern*
    - **Standort:** *5*
    - **Lagerort:** *51*

1. Wählen Sie **Speichern** aus, um das Inforegister **Positionen** verfügbar zu machen.
1. Wählen Sie im Inforegister **Positionen** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Von Menge:** *1*
    - **Bis Menge:** *1000000*

1. Wählen Sie **Speichern** aus, um das Inforegister **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.
1. Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Name:** *Ladebereichstor*
    - **Feste Standortnutzung:** *Feste und nicht feste Lagerplätze*

1. Wählen Sie **Speichern** aus, um die Schaltfläche **Abfrage bearbeiten** in der Symbolleiste **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.
1. Wählen Sie **Abfrage bearbeiten** aus, um den Abfrageeditor zu öffnen.
1. Stellen Sie auf der Registerkarte **Bereich** sicher, dass die folgenden zwei Positionen konfiguriert sind:

    - Position 1:

        - **Tabelle:** *Lagerorte*
        - **Abgeleitete Tabelle:** *Lagerorte*
        - **Feld:** *Lagerort*
        - **Kriterien:** *51*

    - Position 2:

        - **Tabelle:** *Lagerorte*
        - **Abgeleitete Tabelle:** *Lagerorte*
        - **Feld:** *Lagerplatz*
        - **Kriterien:** *Ladebereichstor*

1. Wählen Sie **OK** aus, um den Abfrageeditor zu schließen.

### <a name="create-a-mobile-device-menu-item"></a>Erstellen eines Menüelements für ein mobiles Geräts

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie in der Liste der Menüpunkte im linken Bereich die Option **Kaufeinlagerung** aus.
1. Wählen Sie **Bearbeiten** aus.
1. Wählen Sie im Inforegister **Arbeitsklassen** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Arbeitsklassen-ID:** *CrossDock*
    - **Arbeitsauftragstyp:** *Crossdocking*

1. Wählen Sie **Speichern** aus.

## <a name="scenario"></a>Szenario

### <a name="create-a-purchase-order"></a>Eine Bestellung erstellen

Befolgen Sie diese Schritte, um eine Bestellung als Bezugsquelle zu erstellen.

1. Wechseln Sie zu **Beschaffung \> Bestellungen \> Alle Bestellungen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Dialogfeld **Bestellung erstellen** die folgenden Werte fest:

    - **Kreditorenkonto:** *104*
    - **Lagerort:** *51*

1. Wählen Sie **OK** aus, und notieren Sie sich die Bestellnummer.
1. Im Inforegister **Bestellpositionen** wird eine neue Position hinzugefügt. Legen Sie die folgenden Werte für diese Position fest:

    - **Artikelnummer** *A001*
    - **Menge** *5*

### <a name="create-a-sales-order"></a>Auftrag erstellen

Befolgen Sie diese Schritte, um einen Auftrag als Bedarfsquelle zu erstellen.

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - **Debitorenkonto:** *US-002*
    - **Lagerort:** *51*

1. Wählen Sie **OK**.
1. Im Inforegister **Auftragspositionen** wird eine neue Position hinzugefügt. Legen Sie die folgenden Werte für diese Position fest:

    - **Artikelnummer** *A001*
    - **Menge** *3*

### <a name="create-planned-cross-docking"></a>Geplantes Crossdocking erstellen

Befolgen Sie diese Schritte, um das geplante Crossdocking aus dem Auftrag zu erstellen.

1. Wählen Sie auf der Seite **Auftragsdetails** für den Auftrag, den Sie gerade erstellt haben, im Aktivitätsbereich auf der Registerkarte **Lagerort** in der Gruppe **Aktivitäten** die Option **An Lager freigeben** aus.

    Die Aktivität „An Lager freigeben“ erstellt eine Versand- und Ladeposition für die Auftragsposition und versucht, Lagerbestand zuzuordnen.
    
    Es wird eine Informationsnachricht angezeigt. Sie erhalten außerdem die folgende Warnmeldung: „Für Welle XXXX wurde keine Arbeit erstellt. Weitere Informationen finden Sie im Protokoll zum Arbeitserstellungsverlauf.“ Dieses Verhalten wird erwartet, da sich kein Lagerbestand im Lagerort befindet.

1. Wählen Sie im Inforegister **Auftragspositionen** im Menü **Lagerort** die Option **Lieferdetails** aus.

    Die Seite **Lieferdetails** wird angezeigt und zeigt die Lieferung, die für den Auftrag erstellt wurde.

1. Überprüfen Sie, ob im Inforegister **Ladungspositionen** das Feld **Geplante Crossdocking-Menge** auf *3* festgelegt ist. Da im Lagerort kein Lagerbestand verfügbar war, aber innerhalb des in der Crossdocking-Vorlage definierten Zeitfensters eine gültige Bezugsquelle eintrifft, wurde die Crossdocking-Menge erstellt.
1. Wählen Sie im Inforegister **Ladungspositionen** die Option **Geplantes Crossdocking** aus, um die Details des erstellten Crossdocking anzuzeigen.

## <a name="process-the-cross-docking"></a>Crossdocking verarbeiten

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a>Bestelleingang mit der Warehouse Mobile App

Das System erhält die Menge von 5 aus der Bestellung an den Empfangsort und erstellt zwei Arbeiten.

Die erste Arbeits-ID, die erstellt wird, hat einen **Arbeitsauftragstyp** im Wert von *Crossdocking* und ist mit dem Auftrag verknüpft. Sie hat eine Menge von 3 und wird zum endgültigen Versandort geleitet, damit sie sofort versendet werden kann.

Die zweite Arbeits-ID, die erstellt wird, hat einen **Arbeitsauftragstyp** im Wert von *Bestellungen* und ist mit der Bestellung verknüpft. Sie hat die verbleibende Menge von 2, für die das Crossdocking nicht durchgeführt wurde und zur Einlagerung bestimmt ist.

1. Melden Sie sich beim mobilen Gerät als ein Benutzer im Lagerort *51* an.
1. Gehen Sie zu **Eingehend \> Kaufempfang**.
1. Geben Sie im Feld **PONum** Ihre Bestellnummer ein.
1. Geben Sie im Feld **Menge** den Wert *5* ein.
1. Wählen Sie **OK**.
1. Legen Sie auf der nächsten Seite im Feld **Artikel** *A0001* fest.
1. Wählen Sie **OK**.
1. Bestätigen Sie auf der nächsten Seite die Werte **PONum**, **Artikel** und **Menge**, indem Sie **OK** auswählen.

    Sie erhalten die Nachricht „Arbeit abgeschlossen“.

1. Wählen Sie **Abbrechen** aus, um zu beenden.

### <a name="put-away-to-cross-docking-and-bulk"></a>Einlagerung zu Crossdocking und Bulk

Derzeit haben beide Arbeits-IDs das gleiche Zielkennzeichen. Um die nächsten Schritte ausführen zu können, müssen Sie die Arbeits-ID und die Zielkennzeichen-ID erhalten. Sie können diese Informationen aus den Arbeitsdetails für die Bestellposition und die Auftragsposition abrufen. Alternativ können Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsdetails** gehen und nach Arbeit filtern, wo der Wert von **Lagerort** *51* ist.

1. Gehen Sie auf dem mobilen Gerät zu **Eingehend \> Kaufeinlagerung**, und geben Sie das Zielkennzeichen von der Arbeit ein.
1. Geben Sie im Feld **ID** die Zielkennzeichen-ID aus den Arbeitsdetails ein.

    Die Crossdocking-Auswahlseite zeigt den Kommissionierort (*RECV*), das Zielkennzeichen (*Kennzeichen*), den Artikel (*A0001*) und die Menge (*3*).

1. Wählen Sie **OK**.
1. Geben Sie im Feld **Ziel-LP** ein Zielkennzeichen für die Kennzeichen-ID ein, die am Versandort eingelagert (Crossdocking) werden soll. Sie können eine beliebige Kennzeichen-ID Ihrer Wahl auswählen.
1. Wählen Sie **OK**.
1. Geben Sie auf der nächsten Seite im Feld **ID** die Zielkennzeichen-ID ein.
1. Wählen Sie **OK**.
1. Bestätigen Sie die Arbeit zur Auswahl der verbleibenden Menge von 2, und wählen Sie dann **OK** aus.
1. Wählen Sie auf der nächsten Seite **Fertig** aus, um den Kommissioniervorgang zu beenden und den Einlagerungsprozess zu beginnen.

    Die mobile App zeigt Ihnen den Lagerplatz und das Kennzeichen an, an dem Sie den Artikel ablegen möchten.

1. Bestätigen Sie den Bulk-Lagerplatz **Einlagern**, indem Sie **OK** auswählen.
1. Bestätigen Sie auf der nächsten Seite das Crossdocking **Einlagern**, indem Sie **OK** auswählen.

    Sie erhalten die Nachricht „Arbeit abgeschlossen“.

1. Wählen Sie **Abbrechen** aus, um zu beenden.

Die folgende Abbildung zeigt, wie die abgeschlossene Crossdocking-Arbeit in Microsoft Dynamics 365 Supply Chain Management aussehen könnte.

![Crossdocking-Arbeit abgeschlossen.](media/PlannedCrossDockingWork.png "Crossdocking-Arbeit abgeschlossen")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
