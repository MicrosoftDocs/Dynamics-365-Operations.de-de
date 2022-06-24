---
title: Beschaffungsplan
description: Dieser Artikel enthält Informationen über die Seite „Beschaffungsplan“ und deren Funktionen.
author: t-benebo
ms.date: 9/3/2021
ms.topic: article
ms.search.form: ReqSupplyDemandSchedule, ReqSupplyDemandScheduleFilters, ReqSupplyDemandItemDetails, ReqTransFuturesActionsPart, ReqSupplyDemandOverviewLegendPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0e3937dd4cffc464f38b5770674364579bdb06d1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851738"
---
# <a name="supply-schedule"></a>Beschaffungsplan

[!include [banner](../includes/banner.md)]

Auf der Seite **Beschaffungsplan** wird eine umfassende Übersicht über Angebot und Nachfrage für ein Produkt oder eine Produktfamilie angezeigt. Die Informationen werden nach Standort, Produktprogrammplan und Zeiträumen gefiltert. Sie können die Seite auch verwenden, um neue Aufträge anzulegen, vorhandene Planaufträge zu ändern und die Produktprogrammplanung auszuführen.

## <a name="open-the-supply-schedule-page"></a>Öffnen Sie die Seite „Beschaffungsplan“

Sie können die Seite **Beschaffungsplan** auf eine der folgenden Arten öffnen:

- Gehen Sie zu **Produktprogrammplanung \> Gesamtplanung \> Beschaffungsplan**. Geben Sie im Dialogfeld **Filter ändern** den Plan oder das Produkt ein, das Sie suchen, indem Sie Filterwerte in die angegebenen Felder eingeben. (Im restlichen Teil dieses Artikels wird die von Ihnen eingegebene Sammlung von Filterwerten als „der Filter“ oder „der aktuelle Filter“ bezeichnet.) Wählen Sie **OK** aus, wenn Sie fertig sind.
- Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**. Wählen Sie ein Produkt aus oder öffnen Sie es. Klicken Sie dann im Aktivitätsbereich auf der Registerkarte **Planen** in der Gruppe **Anzeigen** auf **Bedarfsplan**.
- Gehen Sie zu **Produktprogrammplanung \> Einrichten \> Bedarfsplanung \> Artikelzuteilungsschlüssel**. Wählen Sie einen Artikelzuteilungsschlüssel aus, der als Produktfamilie verwendet wird. Wählen Sie dann im Aktionsbereich **Bedarfsplanung** aus.
- Gehen Sie zu **Produktprogrammplanung \> Gesamtplanung \> Geplante Aufträge**. Wählen oder öffnen Sie einen Planauftrag. Klicken Sie dann im Aktivitätsbereich auf der Registerkarte **Anzeigen** in der Gruppe **Anzeigen** auf **Bedarfsplan**.

> [!NOTE]
> Wenn Sie die Seite **Bedarfsplan** über ein Produkt, eine Produktfamilie oder einen geplanten Auftrag öffnen, müssen Sie keine Filterwerte eingeben. Das System verwendet die Standardperiodenvorlage.

## <a name="use-the-supply-schedule-page"></a>Die Seite „Beschaffungsplan“ verwenden

Die Seite **Beschaffungsplan** besteht aus einem oberen Abschnitt, dem Inforegister **Periodenendbestand**, einem zusätzlichen Inforegister, das basierend auf der im oberen Abschnitt ausgewählten Zeile angezeigt wird, und dem Infobox-Bereich. (Um den Infobox-Bereich zu öffnen und eine Infobox anzuzeigen, wählen Sie **Zugehörige Informationen** am rechten Seitenrand aus)

### <a name="upper-section"></a>Oberer Abschnitt

Der obere Abschnitt der Seite **Bedarfsplan** enthält ein Raster, das die folgenden Daten für ein Produkt oder eine Produktfamilie anzeigt. Diese Daten sind nach Zeiträumen gegliedert, die durch den Wert **Periodenvorlage** aus dem Filter definiert werden.

- **Periode – Anfangsbestand** – Diese Zeile zeigt den erwarteten Bestandssaldo zum Anfang der Periode, wenn alle Aufträge im System auftreten.
- **Lagerbestand am Ende der Periode** – Diese Zeile zeigt den erwarteten Bestandssaldo zum Ende der Periode, wenn alle Aufträge im System auftreten.
- **Bedarfsverursachender Bestand am Periodenende** – Diese Zeile zeigt die Bestandsmenge am Ende der Periode, die mit dem zukünftigen Bedarf verknüpft ist.
- **Periode – Nettobeschaffung** – Diese Zeile zeigt die Differenz zwischen Angebot und Nachfrage in der Periode.
- **Mindestbestand** – Dieser Knoten zeigt den Sicherheitslagerbestand für ein Produkt oder eine Produktfamilie. Um diesen Knoten zu erweitern oder zu reduzieren, wählen Sie ihn und dann **Erweitern** oder **Reduzieren** auf der Symbolleiste aus. Dieser Knoten wird nur angezeigt, wenn für das Produkt oder die Produktfamilie ein Sicherheitslagerbestand vorhanden ist.
- **Bedarf** – Dieser Knoten zeigt den Bedarf an einem Produkt oder einer Produktfamilie an. Der Bedarf wird nach Transaktionsart gruppiert. Um diesen Knoten zu erweitern oder zu reduzieren, wählen Sie ihn und dann **Erweitern** oder **Reduzieren** auf der Symbolleiste aus. Zu den Bedarfstransaktionstypen gehören Verkäufe, Umbuchungen und Bestandserfassungen. Dieser Knoten wird nur angezeigt, wenn für das Produkt oder die Produktfamilie ein Bedarf vorhanden ist.
- **Beschaffung** – Dieser Knoten zeigt die Beschaffung für ein Produkt oder eine Produktfamilie an. Die Beschaffung wird nach Transaktionsart gruppiert. Um diesen Knoten zu erweitern oder zu reduzieren, wählen Sie ihn und dann **Erweitern** oder **Reduzieren** auf der Symbolleiste aus. Zu den Angebotstransaktionsarten gehören Produktion, Einkauf und Umlagerungen. Dieser Knoten wird nur angezeigt, wenn für das Produkt oder die Produktfamilie eine Beschaffung vorhanden ist.

Viele der verfügbaren Symbolleistenschaltflächen sowie Infobox- und Inforegister-Anzeigen hängen von Ihrer Auswahl im oberen Abschnitt ab. Normalerweise wählen Sie einen Transaktionstyp aus, indem Sie eine der Zeilen unter dem Knoten **Beschaffung** oder **Bedarf** auswählen. Sie wählen dann einen Zeitraum aus, indem Sie eine bestimmte Spalte für die ausgewählte Zeile auswählen.

Die Symbolleiste über dem Raster im oberen Bereich der Seite **Beschaffungsplan** bietet die folgenden Schaltflächen:

- **Erweitern/reduzieren** – Erweitern oder reduzieren Sie einen ausgewählten Knoten, z. B. den Knoten **Bedarf**, den Knoten **Beschaffung** und deren Unterknoten. (Knoten zeigen das Präfix **\[+\]** oder **\[-\]** an, um anzugeben, ob sie derzeit reduziert oder erweitert sind.)
- **Neu** – Öffnet ein neues Menü, in dem jeder Befehl wiederum ein Dialogfeld oder eine Seite öffnet, auf der Sie einen bestimmten Elementtyp zur Auswahl hinzufügen können Verfügbare Befehle umfassen **Planungseinkauf**, **Geplanter Auftrag**, **Geplantes Kanban**, **Neuer Produktionsauftrag**, **Bestellung** und **Umlagerungsauftrag**.
- **Produktprogrammplanung** – Führen Sie eine Produktprogrammplanung durch. Ein Dialogfeld wird angezeigt, in dem Sie den auszuführenden Plan angeben können. Standardmäßig wird das Feld **Produktprogrammplanung** so festgelegt, dass es dem aktuellen Filter entspricht.
- **Retrograd nach Lagermengen** – Öffnet die Seite **Retrograd nach Lagermengen** für das Produkt, das im aktuellen Filter definiert ist.
- **Bestellvorschläge aktualisieren** – Öffnet die Seite **Bestellvorschläge**, die Bestellvorschläge für das im aktuellen Filter definierte Produkt oder die Produktfamilie anzeigt.
- **Ebene** – Verteilt die Bestellvorschläge gemäß den Einstellungen aus dem angezeigten Dialogfeld.
- **Materialplanrichtlinie nach Lagerplatz** – Öffnet die Seite **Artikelabdeckung** für das im aktuellen Filter definierte Produkt.
- **Kanban-Regel** – Öffnet die Seite **Kanban-Regeln** für das Produkt, das im aktuellen Filter definiert ist.

### <a name="fasttabs"></a>Inforegister

Die Seite **Beschaffungsplan** kann folgende Inforegister enthalten:

- **Lagerbestand am Ende der Periode** – Dieses Inforegister zeigt die Bestandsdaten zum Periodenende in einem grafischen Format an.
- **Beschaffungsprofil** – Dieses Inforegister zeigt die Beschaffungsdaten in einem grafischen Format an. Es wird angezeigt, wenn Sie den Knoten **Beschaffung** oder eine Zeile darunter im oberen Bereich auswählen.
- **Zusammenfassung** – Dieses Inforegister zeigt zusammenfassende Details, die sich auf die Transaktionsart beziehen, die Sie im oberen Abschnitt ausgewählt haben. Wenn Sie beispielsweise **Verkauf** unter dem Knoten **Bedarf** auswählen, zeigt dieses Inforegister Felder an, die sich auf Kundenaufträge beziehen, wie **Angeforderte Auftragspositionen** oder **Gesamtsumme**. Wenn Sie **Produktionsaufträge** im Unterknoten **Produktion** des Knotens **Beschaffung** auswählen, zeigt dieses Inforegister Felder an, die sich auf Produktionsaufträge wie **Geplante Produktionsaufträge** oder **Insgesamt geplant** beziehen. Die Feldwerte hängen von dem Zeitraum ab, den Sie im oberen Abschnitt ausgewählt haben. 
- **\[Transaktionstyp\] - \[Zeitraum\]** – Dieses Inforegister zeigt Aufträge für die Transaktionsart und den Zeitraum an, die Sie im oberen Bereich ausgewählt haben. Der Name des Inforegisters spiegelt diese Auswahl wider. Zum Beispiel könnte es **Kundenaufträge – Rückstand** oder **Produktionsaufträge – Woche 37** heißen.

### <a name="action-pane"></a>Aktivitätsbereich

Die folgenden Schaltflächen sind im Aktivitätsbereich verfügbar:

- **Filter ändern** – Öffnet das Dialogfeld **Filter ändern**, in dem Sie die Filterwerte aktualisieren und dann erneut die Seite **Beschaffung** öffnen, die die aktualisierten Filtereinstellungen widerspiegelt
- **Verzögerungen anzeigen** – Markiert die entsprechenden Zeilen im oberen Bereich, wenn eine verzögerte Bestellung dieser Transaktionsart vorliegt

### <a name="factbox-pane"></a>Infobox-Bereich

Um den Infobox-Bereich zu öffnen und eine Infobox anzuzeigen, wählen Sie **Zugehörige Informationen** am rechten Seitenrand aus. Die folgenden Infoboxen sind auf der Seite **Beschaffungsplan** verfügbar:

- **Artikeldetails** – Diese Infobox zeigt grundlegende Informationen zu dem Produkt, das im aktuellen Filter definiert ist. Es ist leer, wenn Sie im Filter eine Produktfamilie definiert haben.
- **Aktionen** – Diese Infobox zeigt Aktionen für die Aufträge des im oberen Abschnitt ausgewählten Transaktionstyps an.
- **Verzögerungen** – Diese Infobox zeigt Verzögerungen für die Aufträge des im oberen Abschnitt ausgewählten Transaktionstyps an.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
