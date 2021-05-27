---
title: Fest geplante Aufträge
description: Dieses Thema erklärt, wie Sie geplanter Aufträge umwandeln können. Wenn geplante Aufträge umgewandelt werden, werden sie zu tatsächlichen Kaufbestellungen, Transportaufträgen oder Produktionsaufträgen.
author: ChristianRytt
ms.date: 04/22/2021
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a4f882f1abc9f758aca77b137b28aa973f925ea9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019493"
---
# <a name="firm-planned-orders"></a>Fest geplante Aufträge

[!include [banner](../../includes/banner.md)]

Geplante Aufträge müssen im Rahmen der Produktprogrammplanung *bestätigt* (d.h. freigegeben) werden. Wenn geplante Aufträge umgewandelt werden, werden sie zu tatsächlichen Kaufbestellungen, Transportaufträgen oder Produktionsaufträgen. Diese Aufträge werden auch als *Freigegebene Aufträge* oder *offene Aufträge* bezeichnet.

Es gibt drei Methoden zur Umwandlung geplanter Aufträge:

- **Manuelle Umwandlung** – Wählen Sie bestimmte geplante Aufträge in einer Liste aus und starten Sie den Prozess dann manuell.
- **Automatische Umwandlung** – Definieren Sie einen standardmäßigen Zeitrahmen für die Umwandlung für Erfassungsgruppen, einzelne Elemente und Kombinationen von Elementen und Produktprogrammplanungen. Dann werden bei der Produktprogrammplanung die geplanten Aufträge automatisch fixiert, wenn das Auftragsdatum innerhalb des angegebenen Zeitfensters für die Fixierung liegt.
- **Query-basierte Umwandlung** – Definieren Sie eine Abfrage, um geplanter Aufträge basierend auf ihren Eigenschaften auszuwählen. Sie können einen Batchauftrag festlegen, um die Abfrage auszuführen und übereinstimmende Aufträge nach einem regelmäßigen Zeitplan festzulegen.

Dieses Thema beschreibt jede Methode im Detail.

## <a name="enable-the-features-that-are-described-in-this-topic"></a><a name="enable-features"></a>Aktivieren Sie die Funktionen, die in diesem Thema beschrieben werden

Die meisten Funktionen für geplante Aufträge sind in allen Standardinstallationen von Microsoft Dynamics 365 Supply Chain Management verfügbar, die die Planungsoptimierung verwenden. Einige der Funktionen, die in diesem Thema beschrieben werden, müssen jedoch in der Funktionsverwaltung eingeschaltet werden, bevor Sie sie verwenden können.

### <a name="enable-parallelized-firming-of-planned-orders"></a>Parallelisierte Umwandlung geplanter Aufträge ermöglichen

Die Parallelisierung der Firmung hilft, den Umwandlungsprozess zu beschleunigen, indem er über mehrere Threads parallelisiert wird. Diese Vorgehensweise kann sinnvoll sein, wenn viele geplante Aufträge umgewandelt werden.

Um diese Funktion in Ihrem System verfügbar zu machen, gehen Sie zu [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), und schalten Sie die Funktion *Parallele Umwandlung geplanter Aufträge* ein.

### <a name="enable-planned-order-firming-with-filtering"></a>Ermöglicht das Umwandeln geplanter Aufträge mit Filterung

Bei der Umwandlung geplanter Aufträge mit Filterung können Sie logische Kriterien für die Auswahl der zu wandelnden geplanten Aufträge definieren. Sie können auch eine Vorschau anzeigen, welche geplanten Aufträge ausgewählt wurden, den Prozess im Hintergrund ausführen und/oder ihn als Batchauftrag einplanen.

Um diese Funktion in Ihrem System verfügbar zu machen, gehen Sie zu [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), und schalten Sie die Funktion *Geplante Aufträge umwandeln mit Filterung* ein.

### <a name="enable-auto-firming-for-planning-optimization"></a>Aktivieren Sie die automatische Umwandlung für die Planungsoptimierung

Mit der automatischen Fixierung können Sie geplanter Aufträge als Teil der Produktprogrammplanung während des Fixierungszeitfensters fixieren. Die automatische Umwandlung wird immer für die in Supply Chain Management eingebaute Planungs-Engine unterstützt. Um sie jedoch auch mit der Planungsoptimierung zu verwenden, müssen Sie die Funktion einschalten.

Um diese Funktion in Ihrem System verfügbar zu machen, gehen Sie zu [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) und schalten Sie die Funktion *Automatische Umwandlung für Planungsoptimierung* ein.

## <a name="manually-firm-planned-orders"></a>Geplante Aufträge manuell umwandeln

Um geplanter Aufträge manuell zu fixieren, suchen Sie die geplanter Aufträge, die Sie fixieren möchten, und wählen diese aus, und starten dann manuell die Umwandlung.

1. [Öffnen Sie eine beliebige Listenseite für geplante Aufträge](approved-planned-order.md#view-planned-orders).
1. Verwenden Sie das Feld **Filter**, das Feld **Plan** und die Spaltenüberschriften, um die Liste zu filtern und zu sortieren, damit Sie die geplanten Aufträge finden, nach denen Sie suchen.
1. Aktivieren Sie das Kontrollkästchen für jeden geplanten Auftrag, den Sie umwandeln möchten. Wenn Sie alle geplanten Aufträge fixieren wollen, die derzeit auf der Seite aufgelistet sind (basierend auf den Filtern, die Sie angewendet haben), überspringen Sie diesen Schritt.
1. Wählen Sie im Aktivitätsbereich eine der folgenden Schaltflächen:

    - **Festschreiben** – Nur die ausgewählten geplanten Aufträge festschreiben.
    - **Alle umwandeln** – Wandelt alle geplanter Aufträge um, die aktuell auf der Seite aufgelistet sind (basierend auf den Filtern, die Sie angewendet haben), unabhängig von den ausgewählten Kontrollkästchen. Diese Option kann nützlich sein, wenn Sie viele geplante Aufträge umwandeln.

1. Legen Sie im Dialogfeld **Umwandlung** auf dem Inforegister **Parameter** die folgenden Felder fest. (Viele dieser Felder übernehmen ihre Standardwerte von der Registerkarte **Standardaktualisierung** auf der Seite **Parameter der Produktprogrammplanung**.)

    - **Markierung aktualisieren** – Wählen Sie die Richtlinie für die Bestandsmarkierung, die verwendet werden soll, wenn geplanter Aufträge umgewandelt werden.
    - **Fixierung stoppen, wenn ein Fehler auftritt** – Legen Sie diese Option auf *Ja* fest, um die Umwandlung aller ausgewählten geplanten Aufträge zu stoppen, wenn ein Fehler in einem von ihnen auftritt. Diese Option muss auf *Nein* festgelegt werden, wenn die Option **Parallelisierung der Umwandlung** auf *Ja* festgelegt ist.
    - **Parallele Umwandlung** – Diese Option ist nur verfügbar, wenn die Funktion [*Parallele Umwandlung geplanter Aufträge* in Ihrem System eingeschaltet ist](#enable-features) und wenn Sie zwei oder mehr geplante Aufträge zur Umwandlung ausgewählt haben. Legen Sie es auf *Ja* fest, um die Umwandlungen parallel auszuführen. Die parallele Umwandlung kann zu einer Leistungssteigerung beitragen.
    -  **Anzahl der Threads** – Diese Option ist nur verfügbar, wenn die [Funktion *Parallele Umwandlung geplanter Aufträge*](#enable-features) in Ihrem System eingeschaltet ist und wenn Sie die Option **Parallele Umwandlung** auf *Ja* festgelegt haben. Geben Sie die Anzahl der Threads ein, die zur Parallelisierung der Umwandlung verwendet werden sollen. Hinweise zur Verwendung dieser Option in der Produktprogrammplanung finden Sie unter [Verbessern der Leistung der Produktprogrammplanung](../master-planning-performance.md#number-of-threads).

        > [!NOTE]
        > Ein Wert von *0* (Null) für das Feld **Anzahl der Threads** erhöht die Laufzeit der Produktprogrammplanung. Wir empfehlen daher, dieses Feld immer auf einen Wert größer als 0 festzulegen.

    - **Gruppieren nach Lieferant** – Legen Sie diese Option auf *Ja* fest, um geplante Aufträge zu gruppieren und eine Einkaufsbestellung pro Lieferant während der Umwandlung zu erstellen. Alternativ können Sie eine Einkaufsbestellung erstellen, die für jeden geplanten Auftrag eine Zeile enthält.
    - **Gruppieren nach Käufergruppe** – Legen Sie diese Option auf *Ja* fest, um geplante Aufträge zu gruppieren und eine Einkaufsbestellung zu erstellen, die den Lieferanten und die Käufergruppe kombiniert. Um diese Option zu verwenden, müssen Sie auch die Option **Gruppieren nach Kreditor** auf *Ja* festlegen.
    - **Gruppieren nach Periode** (im Abschnitt **Einkaufsbestellungen**) – Wählen Sie die Periode, nach der geplante Aufträge gruppiert werden sollen. Um diese Option zu verwenden, müssen Sie auch die Option **Gruppieren nach Kreditor** aktivieren.
    - **Gruppieren nach Periode** (im Bereich **Umlagerungsaufträge**) – Wählen Sie die Periode aus, nach der geplante Umlagerungsaufträge gruppiert werden sollen. Die Aufträge werden anhand der Werte **Vom Lagerort** und **Zum Lagerort** gruppiert.

    ![Parameter Inforegister im Dialogfenster für die Umwandlung](./media/manual-firming.png "Parameter Inforegister in der Dialogbox Umwandlung")

1. Auf der Registerkarte **Im Hintergrund laufen lassen** Inforegister legen Sie den Job so fest, dass er im Batch-Modus ausgeführt wird. Es macht jedoch keinen Sinn, einen wiederkehrenden Zeitplan festzulegen, wenn Sie eine manuelle Umwandlung durchführen. Die Felder funktionieren genauso wie bei anderen Arten von [Hintergrund-Jobs](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) im Supply Chain Management. Bei der manuellen Umwandlung verarbeitet der Batchauftrag jedoch nur die aktuell ausgewählten geplanter Aufträge. Es werden keine Bestellungen verarbeitet, die den Filtern entsprechen, die derzeit auf der Seite angewendet werden.
1. Wählen Sie **OK**, um Ihre Einstellungen zu übernehmen und die umgewandelten Aufträge zu generieren.

## <a name="auto-firm-planned-orders"></a>Automatische Umwandlung geplanter Aufträge

Mit der automatischen Fixierung können Sie geplanter Aufträge als Teil der Produktprogrammplanung fixieren. Sie können einen Zeitrahmen für die Umwandlung von Deckungsgruppen, einzelnen Elementen und Kombinationen von Elementen und Produktprogrammplanungen definieren. Dann werden bei der Produktprogrammplanung die geplanten Aufträge automatisch fixiert, wenn das Auftragsdatum innerhalb des angegebenen Zeitfensters für die Fixierung liegt. Geplante Aufträge, die von der Planungsoptimierung und dem integrierten Vorgang der Produktprogrammplanung erzeugt werden, behandeln das Auftragsdatum (d. h. den Starttermin) unterschiedlich.

> [!NOTE]
> Die automatische Umwandlung von geplanten Aufträgen kann nur für Elemente erfolgen, die mit einem Lieferanten verbunden sind.
> 
> Abgeleitete Aufträge (d.h. Einkaufsbestellungen von Unterlieferanten), die umgewandelt werden, haben den Status *In-Prüfung*, wenn die Änderungsverfolgung eingeschaltet ist.

> [!IMPORTANT]
> Bevor die in diesem Abschnitt beschriebene Funktion mit der Planungsoptimierung verwendet werden kann, muss die [Funktion *Automatische Umwandlung für Planungsoptimierung*](#enable-features) in Ihrem System aktiviert sein, wie am Anfang dieses Themas beschrieben. Die automatische Umwandlung kann immer mit der integrierten Produktprogrammplanung verwendet werden.

### <a name="auto-firming-with-planning-optimization-vs-the-built-in-planning-engine"></a>Automatische Umwandlung mit Planungsoptimierung vs. die integrierte Planungs-Engine

Sowohl die Planungsoptimierung als auch die integrierte Planungs-Engine können zur automatischen Umwandlung geplanter Aufträge verwendet werden. Jedoch gibt es mehrere wichtige Unterschiede. Die Planungsoptimierung verwendet z. B. das Auftragsdatum (d. h. das Startdatum), um zu bestimmen, welche geplanter Aufträge fixiert werden sollen, während die integrierte Planungs-Engine das Bedarfsdatum (d. h. das Enddatum) verwendet. In der folgenden Tabelle sind die Unterschiede zusammengefasst.

| | Planungsoptimierung | Integrierte Planungs-Engine |
|---|---|---|
| **Datumsbasis** | Die automatische Bestätigung basiert auf dem Bestelldatum (Startdatum). | Die automatische Bestätigung basiert auf dem Bedarfstermin (Enddatum). |
| **Vorlaufzeit** | Da das Auftragsdatum (Startdatum) die Fixierung auslöst, müssen Sie die Durchlaufzeit nicht als Teil des Fixierungszeitfensters betrachten. | Um zu gewährleisten, dass Aufträge rechtzeitig umgewandelt werden, muss der Zeitrahmen für die Umwandlung länger sein als die Vorlaufzeit. |
| **Aufträge für die aktuelle Woche** | Um alle Aufträge zu fixieren, die in der aktuellen Woche beginnen müssen, muss der Fixierungszeitrahmen eine Woche betragen. | Um alle Aufträge zu fixieren, die in der aktuellen Woche beginnen müssen, muss der Fixierungszeitraum die Vorlaufzeit plus eine Woche betragen. |

### <a name="set-up-auto-firming-and-the-firming-time-fence"></a>Automatische Umwandlung und den Festschreibezeit-Zaun festlegen

Sie schalten die automatische Umwandlung ein, indem Sie der entsprechenden Einrichtung der Abdeckung einen automatischen Umwandlungszeitpunkt zuweisen, wie später in diesem Abschnitt beschrieben. Wenn die automatische Umwandlung für kein Deckungs-Setup eingeschaltet ist oder wenn die Planung von einer bestimmten Seite aus gestartet wird, z. B. von der Seite **Netzanforderungen** für ein freigegebenes Produkt, wird die automatische Umwandlung übersprungen.

Gruppierungs- und Markierungsoptionen für die automatische Umwandlung beziehen ihre Werte aus der Registerkarte **Standardaktualisierung** auf der Seite **Parameter der Produktprogrammplanung**.

Die automatische Umwandlung wird durch die Anzahl der Tage definiert, die Sie für die entsprechende Einrichtung der Abdeckung eingeben. Sie können die automatische Umwandlung einschalten und das Steuerelement für den Zeitrahmen der Umwandlung wie folgt steuern:

- Um den Standard-Fixierzeitzaun für eine Abdeckungsgruppe zu definieren, gehen Sie zu **Produktprogrammplanung \> Einrichten \> Abdeckung \> Abdeckungsgruppen**, und wählen Sie eine Abdeckungsgruppe. Geben Sie dann auf der Registerkarte **Anderes** Inforegister im Feld **Automatischer Fixierungszeitrahmen (Tage)** die Anzahl der Tage ein.
- Um den für die Abdeckungsgruppe definierten Fixierungszeit-Zaun für ein bestimmtes Element zu überschreiben, gehen Sie zu **Produktinformationsverwaltung \> Freigegebene Produkte**. Wählen Sie im Aktivitätsbereich **Plan** und wählen Sie dann **Elementabdeckung**. Wählen Sie auf der Registerkarte **Allgemein** die Option **Zeitzaun außer Kraft setzen**, und geben Sie dann im Feld **Automatische Umwandlung Zeitzaun (Tage)** die Anzahl der Tage ein.
- Um den Umwandlungszeit-Zaun zu überschreiben, der für die Abdeckungsgruppe und die Elementabdeckung für einen bestimmten Masterplan definiert ist, gehen Sie zu **Produktprogrammplanung \> Einrichten \> Masterpläne**, und wählen Sie einen Masterplan aus. Legen Sie dann auf dem Inforegister **Zeitfenster in Tagen** die Option **Umwandlung** auf *Ja* fest und geben Sie die Anzahl der Tage ein.

Wenn Sie alle zuvor erwähnten Zeitzäune auf *0* (Null) festlegen, ist die automatische Umwandlung für die betreffenden abgedeckten Elemente effektiv deaktiviert.

## <a name="firm-planned-orders-by-using-a-query"></a>Geplante Aufträge umwandeln mit Hilfe einer Abfrage

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

Mit der abfragebasierten Umwandlung können Sie die Umwandlung auf der Basis von Kriterien planen, die im Voraus definiert wurden. Im Gegensatz zur automatischen Umwandlung lässt die abfragebasierte Umwandlung die automatische Umwandlung verschiedener Teilmengen von Aufträgen zu verschiedenen Zeitpunkten zu. Zusätzlich können Sie entweder manuelle oder automatisierte Vorgänge verwenden, um verschiedene Arten von geplanten Aufträgen zu fixieren. Sie können auch eine Vorschau anzeigen, welche umgewandelten Aufträge auf der Grundlage Ihrer Einstellungen ausgewählt wurden. So können Sie bestätigen, dass die Auswahl Ihren Erwartungen entspricht.

Sie können die automatische Umwandlung mit der abfragebasierten Umwandlung kombinieren. Zum Beispiel hat ein abfragebasierter Umwandlungsauftrag einen Forward Time Fence, der länger ist als der Time Fence für eine passende Konfiguration der automatischen Umwandlung. Daher wird der abfragebasierte Umwandlungsauftrag seine geplanten Aufträge verarbeiten, bevor die automatische Umwandlung ausgelöst wird. Sie können dieses Verhalten nutzen, um Aufträge für bestimmte Kreditor anders zu planen als Aufträge für ähnliche Produkte von anderen Kreditor.

> [!IMPORTANT]
> Bevor die in diesem Abschnitt beschriebene Funktion verwendet werden kann, muss die [Funktion *Geplante Aufträge umwandeln mit Filterung*](#enable-features) in Ihrem System eingeschaltet sein, wie zu Beginn dieses Themas beschrieben.

Um einen geplanten Auftrag mit Hilfe der abfragebasierten Umwandlung zu fixieren, gehen Sie wie folgt vor.

1. Gehen Sie zu **Produktprogrammplanung \> Masterplanung \> Ausführen \> Geplanter Auftrag umwandeln**.
1. Legen Sie im Dialogfeld **Geplante Auftrag-Umwandlung** auf dem Inforegister **Parameter** die grundlegenden Verarbeitungs-, Markierungs- und Gruppierungsoptionen fest. Diese Optionen funktionieren genauso wie im Dialogfeld **Umwandlung**. (Beschreibungen finden Sie im vorherigen Abschnitt.) Legen Sie dann im Abschnitt **Plan** die folgenden Felder fest, die nur im Dialogfeld **Geplanter Auftrag umwandeln** vorkommen:

    - **Plan** – Wählen Sie den Masterplan, der bei der Umwandlung der geplanter Aufträge, die durch diese Abfrage gefunden werden, angewendet werden soll.
    - **Umwandlungszeitzaun Tage vorwärts** – Wählen Sie, wie weit in der Zukunft die verschiedenen Bedarfe und andere Überlegungen von der Produktprogrammplanung berechnet werden müssen.
    - **Umwandlung time fence days backward** – Wählen Sie, wie weit in die Vergangenheit die verschiedenen Bedarfe und andere Überlegungen von der Produktprogrammplanung berechnet werden müssen.

    ![Parameter Inforegister im Dialogfenster „Geplanter Auftrag umwandeln“](./media/planned-order-firming-main-1.png "Parameter Inforegister im Dialogfenster „Geplanter Auftrag umwandeln“")

1. Um festzulegen, welche Datensätze in die Bestellung aufgenommen werden sollen, wählen Sie die Schaltfläche **Filter** auf dem Inforegister **Einzuschließende Datensätze**. Ein Standard-Abfragedialog wird angezeigt, in dem Sie Auswahlkriterien, Sortierkriterien und Joins definieren können. Die Felder funktionieren genauso wie bei anderen Arten von Abfragen im Supply Chain Management. Die Felder hier sind schreibgeschützt und zeigen Werte an, die mit Ihrer Abfrage in Zusammenhang stehen.

    ![Datensätze, die in das Inforegister des Dialogs „Geplanter Auftrag umwandeln“ aufgenommen werden sollen](./media/planned-order-firming-main-2.png "Datensätze zum Einbinden von Inforegister in das Dialogfeld Geplanter Auftrag umwandeln")

1. Wählen Sie **Vorschau**, um eine Vorschau des Inhalts Ihres umgewandelten Auftrags zu erhalten, basierend auf Ihren bisherigen Einstellungen. Die Liste der geplanten Aufträge, die umgewandelt werden sollen, wird als Nachricht angezeigt. Sie können dann Ihre Einstellungen nach Bedarf anpassen, bis die Vorschau den umgewandelten Auftrag so anzeigt, wie Sie ihn beabsichtigen.

    ![Beispiel für eine Vorschau auf einen umgewandelten Auftrag](./media/planned-order-firming-preview.png "Beispiel für eine Vorschau eines umgewandelten Auftrags")

    > [!WARNING]
    > Diese Funktion fixiert alle geplanter Aufträge, die den Filterkriterien entsprechen. Unkritische Umwandlung von geplanten Aufträgen kann dazu führen, dass massenhaft unerwünschte Kauf-, Transport- und Produktionsaufträge erstellt werden. Bevor Sie fortfahren, verwenden Sie immer die Schaltfläche **Vorschau**, um die Datensätze zu überprüfen, die einbezogen werden sollen.

1. Auf der Seite **Im Hintergrund ausführen** Inforegister legen Sie den Auftrag so fest, dass er im Batch-Modus ausgeführt wird, und/oder richten einen wiederkehrenden Zeitplan ein. Die Felder funktionieren genauso wie bei anderen Arten von [Hintergrund-Jobs](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) im Supply Chain Management.
1. Wählen Sie **OK**, um Ihre Einstellungen zu übernehmen und die umgewandelten Aufträge zu generieren.

## <a name="track-firmed-orders"></a>Umgewandelte Aufträge verfolgen

Um einen geplanter Auftrag zu verfolgen, der umgewandelt wurde, befolgen Sie diese Schritte.

1. [Öffnen Sie eine beliebige Listenseite für geplante Aufträge](approved-planned-order.md#view-planned-orders).
1. Öffnen oder wählen Sie den geplanten Auftrag, den Sie verfolgen möchten.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Ansicht** in der Gruppe **Ansicht** den Eintrag **Umwandlungsverlauf**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
