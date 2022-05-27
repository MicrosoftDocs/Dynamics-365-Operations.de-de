---
title: Für Lagerort freigeben
description: Dieses Thema enthält Details zur Freigabe an den Lagerprozess. Es beschreibt Entitäten, die erstellt werden, wenn Sie einen Auftrag an das Lager freigeben, und Optionen, die Sie verwenden können, um den Prozess einzuleiten.
author: Mirzaab
ms.date: 8/13/2021
ms.topic: article
ms.search.form: WHSReleaseToWarehouse, WHSReleaseToWarehouseSalesOrder, WHSReleaseToWarehouseTransferOrder, WHSLoadPlanningWorkbench, WHSWaveTemplateTable, WHSWorkTemplateTable, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8624db42e9d0f3d08ed3b582224ed7937d52f85d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678350"
---
# <a name="release-to-warehouse"></a>Für Lagerort freigeben

[!include [banner](../../includes/banner.md)]

Dieses Thema enthält Details zur Freigabe an den Lagerprozess. Es beschreibt Entitäten, die erstellt werden, wenn Sie einen Auftrag an das Lager freigeben, und Optionen, die Sie verwenden können, um den Prozess einzuleiten.

## <a name="release-to-warehouse-overview"></a>Freigabe an Lager – Übersicht

Die Freigabe an das Lager ist der Prozess der Bereitstellung des Bestands für die Versandabwicklung. Wenn Sie einen Auftrag an das Lager freigeben, erstellt das System Ladepositionen und Sendungen. Wenn eine automatische Wellenverarbeitung eingerichtet ist, werden auch Lasten und erforderliche Arbeiten erstellt. Die Konfiguration der beteiligten Entitäten hängt von den Systemeinstellungen ab. In diesem Abschnitt des Themas werden die Entitäten, die während des Freigabeprozesses für das Lager erstellt werden, und die Systemeinstellungen, die sie definieren, beschrieben.

Eine *Lieferung* ist eine Gruppe von Auftrags- oder Umlagerungsauftragspositionen für denselben Kunden oder dieselbe Lieferadresse.

Eine *Ladung* ist eine Gruppe von Auftrags- oder Umlagerungsauftragspositionen, die zusammen gruppiert sind und in der Regel auf einem einzigen LKW, Eisenbahnwaggon oder einem anderen Transportmittel verschickt werden. Eine Ladung kann eine oder mehrere Lieferungen enthalten. Sie können eine Ladung manuell erstellen, indem Sie einer neuen Ladung Auftragspositionen hinzufügen. In diesem Fall werden Auftragspositionen der Ladung zugewiesen, bevor der Freigabeprozess an das Lager eingeleitet wird, und sie können nur aus der Seite **Ladungsplanungs-Workbench** freigegeben werden.

Lagerhaus-*Arbeit* ist jeder Lagervorgang, der von einem Lagerarbeiter ausgeführt wird. In der Regel bestehen Lagerortarbeitsvorgänge aus mindestens zwei aufeinanderfolgenden Aktionen: Ein Lagerarbeiter entnimmt verfügbaren Lagerbestand an einem Lagerplatz und legt ihn anschließend an einem anderen Lagerplatz ab.

Wenn Aufträge an das Lager freigegeben werden, erstellt das System *Ladepositionen* und gruppiert sie in Sendungen. Der Sendungskonsolidierungsprozess ermöglicht eine automatisierte Sendungskonsolidierung während der Freigabe an den Lagerprozesses. Weitere Informationen finden Sie unter [Richtlinien für die Lieferungskonsolidierung](about-shipment-consolidation-policies.md).

Das System verwendet *Wellen*, um Kommissionierarbeiten und Ladungen für den Versand zu erstellen. Eine *Wellenvorlage* muss für den Wellentyp, den Sie erstellen möchten, und für das Lager der Auftragsposition verfügbar sein. Wellenvorlagen vom Typ *Versand* werden verwendet, um Artikel für Aufträge und Umlagerungsaufträge zu versenden.

Jede Wellenvorlage enthält *Wellenmethoden*. Wellenmethoden führen Aktionen wie das Erstellen von Arbeit für die Welle oder das Erstellen von Ladungen aus. Beispielsweise kann eine Wellenvorlage für Versandwellen Methoden zum Erstellen von Ladungen, Zuweisen von Positionen an Wellen, zur Wiederbeschaffung und zum Erstellen der Entnahmearbeit für die Welle enthalten. Die Wellenvorlage legt viele Einstellungen fest, die definieren, wie die Welle generiert und verarbeitet wird, darunter auch, welche Schritte manuell und welche Schritte automatisch ausgeführt werden müssen. Weitere Informationen finden Sie unter [Wellenvorlagen](wave-templates.md). Daher wird abhängig von der Konfiguration Ihrer Wellenvorlage entweder automatisch eine Welle erstellt, verarbeitet und freigegeben, wenn Sie einen Auftrag an das Lager freigeben, oder einige oder alle dieser Aktionen werden nach der Freigabe an das Lager manuell ausgeführt.

Wenn eine Welle verarbeitet wird, erstellt das System Kommissionierarbeit, basierend auf einer geeigneten *Arbeitsvorlage* und *Standortrichtlinie*, und macht diese Arbeit auf mobilen Geräten verfügbar. Die Arbeitsvorlage bestimmt, wie die Arbeit für jeden Lagerprozess ausgeführt wird, und die Lagerplatzdirektive gibt die Entnahme- und Abhollagerplätze für die Bestandsbewegung an. (Weitere Informationen finden Sie unter [Steuern von Lagerarbeit mithilfe von Arbeitsvorlagen und Lagerplatzrichtlinien](control-warehouse-location-directives.md).)

> [!NOTE]
> Standardmäßig werden Wellen im Stapelmodus verarbeitet.

Während der Wellenverarbeitung erstellt das System normalerweise eine neue Ladung für jede Lieferung, der keine Ladung zugewiesen ist. Wenn Sie möchten, dass das System stattdessen nicht zugeordneten Sendungen vorhandenen Ladungen zuordnet, können Sie die erweiterte Funktion zum Erstellen von Wellenladungen verwenden. Weitere Informationen finden Sie unter [Erweiterter Ladungserstellung während einer Welle](advanced-load-building-during-wave.md) .

Auf den Seiten **Aufträge** und **Umlagerungsaufträge** können Sie die Entitäten überprüfen, die während des Freigabeprozesses für das Lager für Auftragspositionen erstellt werden.

- Seite **Aufträge**:

    - Wählen Sie im Inforegister **Auftragspositionen** die Option **Lager** und dann im Menü **Versanddetails** aus, um verknüpfte Lieferungen zu öffnen, **Ladungsdetails**, um zugehörige Ladungen zu öffnen, oder **Arbeitsdetails**, um zugehörige Arbeitsdetails zu öffnen.
    - Wählen Sie im Inforegister **Positionsdetails** die Registerkarte **Ladung**, um die zugehörigen Ladungen zu prüfen.

- Seite **Umlagerungsaufträge**:

    - Wählen Sie im Aktionsbereich auf der Registerkarte **Senden** die Option **Versanddetails** aus, um zugehörige Lieferungen zu öffnen, oder **Ladungsdetails**, um zugehörige Ladungen zu öffnen.
    - Wählen Sie im Inforegister **Umlagerungsauftragspositionen** die Option **Arbeitsdetails** aus, um zugehörige Arbeitsdetails zu öffnen.

Zusammenfassend lässt sich sagen, dass bei der Freigabe einer Bestellung an das Lager der am stärksten automatisierte Ablauf wie folgt funktioniert:

1. Das System legt eine Lieferung zum Auftrag und eine Welle an.
1. Die Welle wird verarbeitet.
1. Das System erstellt eine Ladung und eine Arbeits-ID.

Abhängig von den Einstellungen für Wave-Vorlagen, Arbeitsvorlagen und Standortanweisungen werden einige Schritte in diesem Ablauf möglicherweise manuell. Der Gesamtfluss bleibt jedoch gleich.

Sie haben mehrere Möglichkeiten, wie Sie eine Bestellung an das Lager freigeben. Sie können den Vorgang manuell ausführen oder einen Batchauftrag einrichten. In den verbleibenden Abschnitten dieses Themas werden die verschiedenen Möglichkeiten beschrieben, wie Sie eine Freigabe für den Lagervorgang durchführen können.

## <a name="manual-release-to-the-warehouse-from-the-sales-orders-and-transfer-orders-pages"></a>Manuelle Freigabe an das Lager über die Seiten Kundenaufträge und Umlagerungsaufträge

Sie können eine Bestellung direkt über die Seite **Aufträge** oder **Umlagerungsaufträge** an das Lager freigeben, indem Sie **Freigabe an Lager** auswählen.

- Auf der Seite **Aufträge** befindet sich die Schaltfläche auf der Registerkarte **Lagerort** des Aktivitätsbereichs.
- Auf der Seite **Umlagerungsaufträge** befindet sich die Schaltfläche auf der Registerkarte **Senden** des Aktivitätsbereichs.

Von der Seite **Aufträge** können Sie mehrere Aufträge gleichzeitig freigeben.

## <a name="manual-release-to-the-warehouse-from-the-release-to-warehouse-pages"></a>Manuelle Freigabe an das Lager von den Seiten „Freigabe an Lager“

Das System bietet derzeit drei Seiten, auf denen Sie Positionen für mehrere Bestellungen überprüfen und an das Lager freigeben können:

- **Freigabe an Lager** (**Lagerortverwaltung \> Freigabe an Lager \> Freigabe an Lager**) – Auf dieser Seite können Sie sowohl mit Aufträgen als auch mit Umlagerungsaufträgen arbeiten. Es bietet jedoch eine langsamere Leistung als die anderen beiden Seiten. Diese Seite wird in Kürze eingestellt.
- **Aufträge an Lager freigeben** (**Lagerortverwaltung \> Freigabe an Lager \> Aufträge an Lager freigeben**) – Auf dieser Seite können Sie nur mit Aufträgen arbeiten. Es bietet jedoch eine bessere Leistung als die Seite **Freigabe an Lager**.
- **Umlagerungsaufträge an Lager freigeben** (**Lagerortverwaltung \> Freigabe an Lager \> Umlagerungsaufträge an Lager freigeben**) – Auf dieser Seite können Sie nur mit Umlagerungsaufträgen arbeiten. Es bietet jedoch eine bessere Leistung als die Seite **Freigabe an Lager**.

Alle drei Seiten bieten ähnliche Funktionen, wie im Rest dieses Abschnitts beschrieben. Bei allen können Sie Auftragspositionen oder ganze Aufträge auswählen und diese dann an das Lager freigeben.

Jede der Seiten besteht aus einem oberen Abschnitt, in dem Sie Auftragspositionen auswählen können, und einem unteren Abschnitt, in dem Sie den Freigabeprozess an das Lager einleiten können. Sie können im oberen Bereich Filter verwenden, um nach den Auftragspositionen zu suchen, die Sie freigeben möchten. Die Seite **Freigabe an Lager** bietet im oberen Bereich eine separate Registerkarte für Aufträge und Umlagerungsaufträge, während auf den beiden anderen Seiten jeweils nur eine Auftragsart angezeigt wird.

Die Symbolleiste im oberen Bereich enthält die folgenden Schaltflächen, mit denen Sie Auftragspositionen zur Freigabe an das Lager auswählen können:

- **Hinzufügen** – Wählen Sie im oberen Abschnitt eine oder mehrere Auftragspositionen aus und wählen Sie dann diese Schaltfläche, um diese Zeilen in den unteren Abschnitt zu bringen.
- **Alle hinzufügen** – Fügen Sie alle Zeilen vom oberen Abschnitt zum unteren Abschnitt hinzu.
- **Auftrag hinzufügen** – Wählen Sie einen Auftrag aus und wählen Sie dann diese Schaltfläche, um alle Positionen aus diesem Auftrag zum unteren Abschnitt hinzuzufügen.

Nachdem Sie das Hinzufügen von Positionen zum unteren Abschnitt abgeschlossen haben, markieren Sie jede Zeile, die Sie freigeben möchten. Wählen Sie dann **Freigabe an Lager** auf der Symbolleiste, um diese Positionen für das Lager freizugeben.

## <a name="manual-release-to-the-warehouse-from-the-load-planning-workbench-page"></a>Manuelle Freigabe an das Lager über die Seite „Ladungsplanungs-Workbench“

Sie können Aufträge auch manuell an das Lager freigeben, indem Sie die Seite **Ladungsplanungs-Workbench** verwenden. Auf dieser Seite können Sie Auftragspositionen in Ladungen organisieren und diese Ladungen dann an das Lager freigeben.

Öffnen Sie die Seite **Ladungsplanungs-Workbench** über **Lagerortverwaltung \> Ladungen**. Sie können sie auch über die Seiten **Aufträge** und **Umlagerungsaufträge** öffnen. Im oberen Bereich der Seite können Sie Auftragspositionen auf der Registerkarte **Verkaufspositionen** auswählen und Auftragspositionen auf die Registerkarte **Umlagerungspositionen** übertragen, und diese Leitungen dann zu einer neuen oder vorhandenen Ladung hinzufügen.

Die Registerkarte **Angebot und Nachfrage** im Aktivitätsbereich enthält die folgenden Schaltflächen, mit denen Sie Auftragspositionen im oberen Abschnitt zu einer Ladung hinzufügen können:

- **Zu neuer Ladung** – Wählen Sie im oberen Abschnitt eine oder mehrere Auftragspositionen aus und wählen Sie dann diese Schaltfläche, um eine neue Ladung zu erstellen und diese Positionen hinzuzufügen.
- **Zu bestehender Ladung** – Wählen Sie im oberen Abschnitt eine oder mehrere Auftragspositionen aus und wählen Sie dann diese Schaltfläche, um diese Positionen zu einer bestehenden Ladung hinzuzufügen.
- **Gesamter Auftrag zu neuer Ladung** – Wählen Sie Aufträge aus und wählen Sie dann diese Schaltfläche, um eine neue Ladung zu erstellen und alle Positionen aus diesen Aufträgen hinzuzufügen.
- **Gesamter Auftrag zu bestehender Ladung** – Wählen Sie einen Auftrag aus und wählen Sie dann diese Schaltfläche, um alle Positionen aus diesen Aufträgen zu einer bestehenden Ladung hinzuzufügen.

Im unteren Bereich können Sie die angelegten Ladungen überprüfen. Um Ladungen an das Lager freizugeben, wählen Sie sie aus und wählen Sie dann **Freigabe \> Freigabe an Lager** in der Symbolleiste. Wenn Sie die automatische Wellenverarbeitung verwenden, erstellt das System Sendungen und Arbeits-IDs, wenn die Freigabe an den Lagervorgang ausgeführt wird, da den Auftragspositionen bereits Ladungen zugewiesen sind.

## <a name="automatic-release-to-the-warehouse"></a>Automatische Freigabe an das Lager

Um Bestellungen automatisch an das Lager freizugeben, verwenden Sie die Einzelvorgänge **Automatische Freigabe von Aufträgen** und **Automatische Freigabe von Umlagerungsaufträgen**.

Zum Einrichten des Batchauftrage, der Aufträge freigibt, folgen Sie diesen Schritten.

1. Wechseln Sie zu **Lagerortverwaltung \> An Lager freigeben \> Automatische Freigabe von Aufträgen für den Lagerort**.
1. Legen Sie im Dialogfeld **Automatische Freigabe von Aufträgen** auf dem Inforegister **Parameter** die folgenden Felder fest:

    - **Freizugebende Menge** – Wählen Sie aus, ob die gesamte Menge oder nur die physisch reservierte Menge an das Lager freigegeben werden sollen.
    - **Freigabe von teilweise freigegebenen Aufträgen zulassen** – Geben Sie an, ob Restmengen für teilfreigegebene Aufträge an das Lager freigegeben werden sollen.
    - **Reservierungen bei fehlgeschlagener Freigabe behalten** – Geben Sie an, ob Mengen, die automatisch für einen Auftrag reserviert wurden, reserviert bleiben sollen, wenn die Freigabe an das Lager fehlschlägt.
    - **Freigaben nach Kunden gruppieren** - Legen Sie fest, ob das System die Freigabe für Vorgänge im Lager für jeden Kunden separat verarbeiten oder alle Verkaufsaufträge gleichzeitig freigeben soll. Wenn diese Option auf *Ja* festgelegt ist, sammelt das System alle Verkaufsauftragszeilen für einen ausgewählten Kunden, gibt diese Aufträge für das Lager frei und verarbeitet dann den nächsten Kunden. Wenn diese Option auf *Nein* festgelegt ist, gibt das System alle verfügbaren Verkaufsauftragszeilen in einer einzigen Freigabe für den Lagervorgang frei. Durch die Aktivierung dieser Option können Sie dazu beitragen, die Leistung und Ausfallsicherheit des Release-to-Warehouse-Prozesses zu verbessern. Seien Sie jedoch vorsichtig, wenn Sie diese Option zusammen mit Wellenvorlagen verwenden, die so konfiguriert sind, dass sie Wellen bei der Freigabe an das Lager verarbeiten, denn diese Kombination könnte viele Wellen für einen einzelnen Kunden erzeugen, von denen jede einzelne Arbeit enthält, die nur für diesen Kunden erstellt wurde. Wenn Sie Arbeiten generieren möchten, bei denen Sendungen für mehrere Kunden zusammengefasst werden, sollten Sie entweder die Option *Freigaben nach Kunden gruppieren* deaktivieren oder Ihre Konfigurationsvorlagen so konfigurieren, dass sie die aufgeschobene Verarbeitung verwenden.
    - **Gesperrte Auftragsabwicklung** – Wählen Sie aus, wie das System Aufträge behandeln soll, die derzeit gesperrt sind, weil sie von anderen Benutzern oder Prozessen bearbeitet werden:

        - *Warten, bis die Bestellungen entsperrt werden* – Das System sollte warten, bis die Bestellungen entsperrt sind, bevor es sie an das Lager freigibt. In diesem Fall kann der Prozess der Freigabe an das Lager länger dauern.
        - *Gesperrte Bestellungen überspringen* – Das System soll gesperrte Aufträge überspringen.

    - **Gültige Auftragsarten** – Wählen Sie die Auftragstypen aus, die in den Stapel aufgenommen werden sollen.
    - **Kreditlimitart** – Wählen Sie aus, ob Kreditlimitprüfungen während des Freigabeprozesses an das Lager durchgeführt werden sollen, und, falls die Prüfungen durchgeführt werden sollen, die Transaktionsinformationen, die darin enthalten sein sollen.

1. Um zu kontrollieren, welche Bestellungen verarbeitet werden sollen, wählen Sie im Inforegister **Einzuschließende Aufzeichnungen** die Option **Filter** aus. Ein Standard-Abfragedialog wird angezeigt, in dem Sie Auswahlkriterien, Sortierkriterien und Joins definieren können. Die Felder funktionieren genauso wie bei anderen Arten von Abfragen im Microsoft Dynamics 365 Supply Chain Management.
1. Im Inforegister **Im Hintergrund ausführen** wählen Sie aus, ob der Auftrag im Batch-Modus ausgeführt wird, und/oder richten einen wiederkehrenden Zeitplan ein. Die Felder funktionieren genauso wie bei anderen Arten von [Hintergrund-Jobs](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) im Supply Chain Management.
1. Wählen Sie **OK** um Ihre Einstellungen zu übernehmen und die Freigabe an den Lagerprozess anzustoßen.

Zum Einrichten des Batchauftrags, der Umlagerungsaufträge freigibt, folgen Sie den Schritten.

1. Wechseln Sie zu **Lagerortverwaltung \> An Lager freigeben \> Automatische Freigabe von Umlagerungsaufträgen**.
1. Legen Sie im Dialogfeld **Automatische Freigabe von Umlagerungsaufträgen** auf dem Inforegister **Parameter** die folgenden Felder fest:

    - **Freizugebende Menge** – Wählen Sie aus, ob die gesamte Menge oder nur die physisch reservierte Menge an das Lager freigegeben werden sollen.
    - **Freigabe von teilweise freigegebenen Aufträgen zulassen** – Geben Sie an, ob Restmengen für teilfreigegebene Aufträge an das Lager freigegeben werden sollen.
    - **Gruppenfreigaben nach Ziellager** – Geben Sie an, ob das System alle Umlagerungsaufträge gleichzeitig freigeben soll oder ob es Umlagerungsauftragspositionen nach Ziellager gruppieren und dann jede Gruppe separat an das Lager freigeben soll.

1. Um zu kontrollieren, welche Bestellungen verarbeitet werden sollen, wählen Sie im Inforegister **Einzuschließende Aufzeichnungen** die Option **Filter** aus. Ein Standard-Abfragedialog wird angezeigt, in dem Sie Auswahlkriterien, Sortierkriterien und Joins definieren können. Die Felder funktionieren genauso wie bei anderen Arten von Abfragen im Supply Chain Management.
1. Im Inforegister **Im Hintergrund ausführen** wählen Sie aus, ob der Auftrag im Batch-Modus ausgeführt wird, und/oder richten einen wiederkehrenden Zeitplan ein. Die Felder funktionieren genauso wie bei anderen Arten von [Hintergrund-Jobs](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) im Supply Chain Management.
1. Wählen Sie **OK** um Ihre Einstellungen zu übernehmen und die Freigabe an den Lagerprozess anzustoßen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
