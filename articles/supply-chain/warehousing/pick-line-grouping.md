---
title: Gruppierung von Kommissionierpositionen
description: In diesem Thema wird eine Übersicht über die Gruppierung von Kommissionierpositionen angezeigt.
author: Mirzaab
manager: AnnBe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 1b1d0135d450bc9be7b1303240a9ca70f95ae38e
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906267"
---
# <a name="pick-line-grouping"></a>Gruppierung von Kommissionierpositionen

[!include [banner](../includes/banner.md)]

Bei der Kommissionierliniengruppierung können mehrere Arbeitslinien mit demselben Artikel und demselben Standort zu einer einzigen Kommissionierlinie zusammengefasst werden, die dem Benutzer auf einem mobilen Gerät angezeigt wird. Daher können Lagerarbeiter die effizientesten Anweisungen erhalten, die möglich sind, aber die erforderliche Trennung der Arbeitslinien im System wird auch beibehalten (z. B. für verschiedene Container und Aufträge).

## <a name="set-up-pick-line-grouping"></a>Gruppierung von Kommissionierpositionen einrichten

### <a name="create-a-mobile-device-menu-item"></a>Erstellen eines Menüelements für ein mobiles Geräts

1. Navigieren Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüelemente für mobile Geräte**, und erstellen Sie ein neues Menüelement mit dem Namen **Entnahmepositionen für Warengruppe – Benutzergesteuert**.
2. Legen Sie unter **Menüoptionen für das mobile Gerät** die folgenden Werte fest:

    - Geben Sie im Feld **Menüelementname** die Option **Warenentnahme - Gruppenposition** ein.
    - Geben Sie im Feld **Titel** die Option **Warenentnahme - Gruppenposition** ein.
    - Wählen Sie im Feld **Modus** **Arbeit**.
    - Legen Sie die **Vorhandene Arbeit verwenden**-Option mit **Ja** fest.

3. Legen Sie auf dem Inforegister **Allgemein** die folgenden Werte fest:

    - Wählen Sie im Feld **Geleitet von** die Option **Benutzergesteuert** fest.
    - Legen Sie die Option **Ladungsträger generieren** auf **Ja** fest.
    - Legen Sie die Option **Gruppenentnahme** auf **Ja** fest.

4. Befolgen Sie im Inforegister **Arbeitsklassen** diese Schritte, um gültige Arbeitsklassen für den Menüpunkt für mobile Geräte zu konfigurieren:

    1. Wählen Sie **Neu** aus.
    2. Wählen Sie im Feld **Arbeitsklassenkennung** die Option **Verkäufe** oder **SO Entnahme** aus, je nachdem, welchen Lagerort Sie verwenden.
    3. Wählen Sie im Feld **Arbeitsauftragsart** **Arbeitsaufträge** aus.

### <a name="set-up-a-mobile-device-menu"></a>Menü des mobilen Geräts einrichten

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menü für mobiles Gerät**. 
1. Fügen Sie den soeben erstellten Menüeintrag zum gewünschten Menü hinzu.

### <a name="set-up-a-work-template"></a>Eine Arbeitsvorlage einrichten

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.
1. Suchen Sie die Arbeitsvorlage, die mit dieser Funktion verwendet werden soll. Wählen Sie für dieses Beispiel die standardmäßige Contoso-Arbeitsvorlage **51 Pick to stage** aus.
1. Wählen Sie im Menü **Abfrage bearbeiten** aus.
1. Wählen Sie auf der Registerkarte **Sortierung** die Option **Hinzufügen** aus, und legen Sie dann die folgenden Werte fest:

    - Wählen Sie im Feld **Tabelle** die Option **Temporäre Arbeitstransaktionen** aus.
    - Wählen Sie im Feld **Abgeleitete Tabelle** die Option **Temporäre Arbeitstransaktionen** aus.
    - Wählen Sie im Feld **Feld** die Option **Artikelnummer** aus.
    - Wählen Sie im Feld **Suchrichtung** die Option **Aufsteigend** aus.

> [!NOTE]
> Damit die Funktion zum Gruppieren von Auswahlzeilen funktioniert, müssen die Arbeitszeilen nach Artikel-ID sortiert sein. Wenn Zeilen mit denselben Elementen nicht nacheinander sequenziert werden, werden sie nicht gruppiert.

## <a name="example"></a>Beispiel

### <a name="create-picking-work"></a>Entnahmearbeit erstellen

Bevor Sie die Gruppierung von Kommissionierpositionen einrichten können, müssen Sie geeignete ausgehende Arbeiten erstellen.

1. Gehen Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
2. Wählen Sie **Neu** aus, um einen Auftrag zu erstellen. 
3. Wählen Sie im Feld **Debitorenkonto** einen Debitor aus. 
4. Wählen Sie auf dem Inforegister **Allgemein** im Feld **Lagerort** die Option **51** aus. Wählen Sie dann **OK** aus.
5. Fügen Sie unter **Auftragspositionen** die folgenden sechs Zeilen hinzu:

    - **Position 1:** Wählen Sie im Feld **Artikelnummer** die Option **M9200** aus. Geben Sie im Feld **Menge** den Wert **3** ein.
    - **Position 2:** Wählen Sie im Feld **Artikelnummer** die Option **M9201** aus. Geben Sie im Feld **Menge** den Wert **3** ein. 
    - **Position 3:** Wählen Sie im Feld **Artikelnummer** die Option **M9202** aus. Geben Sie im Feld **Menge** den Wert **2** ein. 
    - **Position 4:** Wählen Sie im Feld **Artikelnummer** die Option **M9200** aus. Geben Sie im Feld **Menge** den Wert **1** ein. 
    - **Position 5:** Wählen Sie im Feld **Artikelnummer** die Option **M9200** aus. Geben Sie im Feld **Menge** den Wert **3** ein.
    - **Position 6:** Wählen Sie im Feld **Artikelnummer** die Option **M9202** aus. Geben Sie im Feld **Menge** den Wert **7** ein. 

    Hier ist eine Zusammenfassung der Gesamtmengen für jeden Artikel:

    - **Artikel M9200:** 7 Stück
    - **Artikel M9201:** 3 Stück
    - **Artikel M9202:** 9 Stück

6. Bevor Sie die Bestellungen an das Lager freigeben, müssen Sie sicherstellen, dass die Kommissionierstellen über genügend Lagerbestand für alle Artikel in allen Bestellungen verfügen. Überprüfen Sie die Einstellung **Standortrichtlinie**, um zu bestimmen, welche Kommissionierorte für die Kundenauftragskommissionierung verwendet werden.
7. Reservieren Sie das Inventar und geben Sie es an das Lager frei. Eine Arbeitskennung mit sechs Zeilen wird erstellt. Die Zeilen sind nach Artikelnummer sortiert.

### <a name="run-the-mobile-device-flow"></a>Den Ablauf für mobile Geräte ausführen

1. Wählen Sie auf dem Mobilgerät das Menü aus, das den neuen Menüpunkt für das mobile Gerät enthält.
1. Wählen Sie das Menüelement **Warenentnahme – Gruppenposition** aus, und initiieren Sie die Entnahme.

    Nachdem Sie das Menü ausgewählt und die Arbeits-ID eingegeben haben, wird der Auswahlschritt angezeigt, in dem alle Auswahlzeilen für Artikel M9200 gruppiert sind. Sie erhalten die Anweisung, jeweils 7 von Artikel M9200 auszuwählen.

1. Bestätigen Sie den Entnahmeschritt. 
1. Gehen Sie zum Mandantenbild der Ware in Arbeit und stellen Sie fest, dass alle drei Kommissionierzeilen für Position M9200 gleichzeitig geschlossen wurden.

    Arbeitslinie 4 wird vorgestellt.

1. Bestätigen Sie den Entnahmeschritt.

    Der letzte Entnahmeschritt auf dem Mobilgerät fasst die letzten beiden Entnahmepositionen aus dem Arbeitsauftrag zusammen.

1. Führen Sie den Pick-Schritt für 9 Artikel M9202 durch.
1. Bestätigen Sie den Put-Schritt und alle weiteren Pick/Put-Paare, um die Arbeit abzuschließen.

> [!NOTE]
> - Arbeitszeilen können nur dann gruppiert werden, wenn sie der Reihe nach vorliegen.
> - Die folgende Funktionalität wird nicht unterstützt:
>
>    - Artikelgewichtsartikel. Wenn sich auf der Arbeit Catch-Weight-Artikel befinden, erhalten Sie eine Fehlermeldung, bevor Sie mit dem Kommissionieren beginnen.
>    - Stückentnahme.
>    - Arbeitspositionen, für die noch Wiederbeschaffungsarbeiten durchgeführt werden müssen.
>    - Zu hohe Entnahme.
