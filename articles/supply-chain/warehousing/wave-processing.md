---
title: Wellen erstellen und verarbeiten
description: In diesem Thema wird beschrieben, wie eine Welle erstellt, verarbeitet und freigegeben wird, um Entnahmearbeit für eine Ladung, eine Lieferung, einen Produktionsauftrag oder einen Kanbanauftrag zu erstellen.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, WHSParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage, WHSProdWaveTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 76b11eaec0f22393e877c2837e2533a176018f2b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355481"
---
# <a name="wave-creation-and-processing"></a>Wellen erstellen und verarbeiten

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie eine Welle erstellt, verarbeitet und freigegeben wird, um Entnahmearbeit für eine Ladung, eine Lieferung, einen Produktionsauftrag oder einen Kanbanauftrag zu erstellen. Sie können für die folgenden Auftragsarten Wellen erstellen:

- **Aufträge** – Verwenden Sie Versandwellen, um Positionen aus Aufträgen einzubeziehen. Wenn ein Auftrag an den Lagerort freigegeben wird, können die Auftragspositionen in die Welle einbezogen werden.
- **Produktionsaufträge** – Verwenden Sie Produktionswellen, um Positionen aus der Stückliste (BOM) für ein Produkt einzubeziehen.
- **Kanbanaufträge** – Kanbanwellen enthalten Kommissionierlistenpositionen aus Kanbanaufträgen.

Bei Aufträgen und Kanbanaufträgen muss Lagerbestand reserviert werden, bevor der Auftrag an den Lagerort freigegeben wird. Andernfalls können die Artikel oder Verteilungspositionen nicht in einer Welle verarbeitet werden. Einige Produktionsaufträge sind jedoch etwas flexibler. Für Produktionsaufträge können Sie eine der folgenden Optionen auswählen:

- Anfordern, dass alle Materialien reserviert werden, bevor ein Auftrag für den Lagerort freigegeben werden kann.
- Zulassen, dass Produktionsaufträge für den Lagerort freigegeben werden, auch wenn nicht alle Materialien reserviert werden können. Wenn Sie diese Option auswählen, müssen Sie den Prozess der Freigabe für den Lagerort manuell wiederholen, wenn die zusätzlichen Materialien verfügbar werden. Dies ist beispielsweise hilfreich, wenn Sie die Materialien haben, die Sie zum Starten der Produktion benötigen, und warten können, bis die zusätzlichen Materialien verfügbar werden.

Sie können über das Feld **Anforderung für Materialreservierung** auf der Seite **Produktionssteuerungsparameter** festlegen, welche dieser Produktionsauftragsoptionen standardmäßig verwendet werden sollen. Sie können jedoch die Einstellungen für einen bestimmten Produktionsauftrag wie erforderlich ändern. Weitere Informationen finden Sie unter [Lagerortparameter für Wellenverarbeitung](wave-warehouse-parameters.md).

## <a name="create-and-process-a-wave"></a>Eine Welle erstellen und verarbeiten

Das folgende Diagramm zeigt, wie Versandwellen erstellt, verarbeitet und freigegeben werden. Die Zahlen entsprechen den Abschnitten weiter unten in diesem Abschnitt.

![Prozess zum Erstellen einer Welle.](media/wave-processing-diagram.png "Prozess zum Erstellen einer Welle")

### <a name="prerequisites"></a>Voraussetzungen

Bevor Sie beginnen, muss eine Wellenvorlage für den Wellentyp verfügbar sein, den Sie erstellen möchten (Versand, Produktion oder Kanban). Die Wellenvorlage legt viele Einstellungen dafür fest, wie die Welle generiert und verarbeitet wird, darunter auch, welche Schritte manuell und automatisch ausgeführt werden müssen. Weitere Informationen finden Sie unter [Wellenvorlagen](wave-templates.md).

### <a name="create-a-wave"></a>Welle erstellen

#### <a name="automatically-create-waves-based-on-warehouse-and-order-type"></a>Wellen basierend auf Lagerort und Auftragstyp automatisch erstellen

Um Wellen automatisch zu erstellen, richten Sie [Wellenvorlagen](wave-templates.md) ein, die für jede relevante Auftragsart und jeden Lagerort gelten. Stellen Sie sicher, dass bei jeder Vorlage die Option **Wellenerstellung automatisieren** auf *Ja* steht.

#### <a name="manually-create-waves"></a>Wellen manuell erstellen

Führen Sie folgende Schritte aus, um manuell eine Welle zu erstellen:

1. Stellen Sie sicher, dass die relevanten [Wellenvorlagen](wave-templates.md) nicht so eingestellt sind, dass eine Welle automatisch für den Lagerort und die Auftragstypen erstellt wird, für die Sie manuell Wellen erstellen wollen.
1. Abhängig vom Typ der Welle, die Sie erstellen möchten, gehen Sie wie folgt vor:

    - Gehen Sie zu **Lagerortverwaltung** \> **Allgemein** \> **Wellen** \> **Versandwellen** \> **Alle Wellen**. Wählen Sie im Aktivitätsbereich **Wellen** aus.
    - Gehen Sie zu **Lagerortverwaltung** \> **Allgemein** \> **Wellen** \> **Produktionswellen** \> **Alle Produktionswellen**. Wählen Sie im Aktivitätsbereich **Produktionswellen** aus.
    - Gehen Sie zu **Lagerortverwaltung** \> **Allgemein** \> **Wellen** \> **Kanbanwellen** \> **Alle Kanbanwellen**. Wählen Sie im Aktivitätsbereich **Welle erstellen** aus.

1. Geben Sie im Feld **Beschreibung** eine kurze Wellenbeschreibung ein. Sie sollte angeben, was Sie in der Welle verarbeiten.

1. Wählen Sie im Feld **Wellenvorlagennamen** die Wellenvorlage für den Typ der Welle aus, die erstellt werden soll. Die Wellenvorlage enthält die Wellenmethoden, die Aktivitäten wie das Erstellen der Arbeit für die Welle ausführen. Beispielsweise kann die Wellenvorlage für Versandwellen Methoden zum Erstellen von Ladungen, Zuweisen von Positionen an Wellen, zur Wiederbeschaffung und zum Erstellen der Entnahmearbeit für die Welle enthalten.

1. Wählen Sie die Attribute in den Feldern **Wellenattribute** aus, wenn Sie Wellenattribute als zusätzliche Abfragekriterien für die Welle verwenden möchten.

### <a name="specify-what-to-include-in-a-wave"></a>Festlegen, was in einer Welle enthalten sein soll

Nachdem eine Welle erstellt wurde, können Sie ihr Inhalte hinzufügen.

> [!NOTE]
> Solange sie noch nicht freigegeben wurde, können Sie einer Welle bei Bedarf Positionen hinzufügen, auch nachdem sie verarbeitet wurde.

#### <a name="automatically-specify-what-to-include-in-a-wave"></a>Automatisch festlegen, was in einer Welle enthalten sein soll

Um Wellen automatisch zu erstellen, richten Sie [Wellenvorlagen](wave-templates.md) ein, die für jede relevante Auftragsart und jeden Lagerort gelten. Stellen Sie sicher, dass bei jeder Vorlage die Option **Wellenerstellung automatisieren** auf *Ja* steht. Alternativ könnte Ihre Vorlage jeder qualifizierenden offenen Welle automatisch Positionen zuweisen, wenn die Option **Offenen Wellen zuweisen** auf *Ja* gesetzt ist.

#### <a name="manually-specify-what-to-include-in-a-wave"></a>Manuell festlegen, was in einer Welle enthalten sein soll

Wenn eine Welle erstellt, aber noch nicht freigegeben wurde, können Sie manuell angeben, was darin enthalten sein soll. So fügen Sie einer Welle manuell Positionen hinzu:

1. Abhängig vom Typ der Welle, zu der Positionen hinzugefügt werden sollen, nutzen Sie eine der folgenden Methoden:

    - Gehen Sie zu **Lagerortverwaltung** \> **Allgemein** \> **Wellen** \> **Versandwellen** \> **Alle Wellen**. Wählen Sie im Aktivitätsbereich **Wellen** aus.
    - Gehen Sie zu **Lagerortverwaltung** \> **Allgemein** \> **Wellen** \> **Produktionswellen** \> **Alle Produktionswellen**. Wählen Sie im Aktivitätsbereich **Produktionswellen** aus.
    - Gehen Sie zu **Lagerortverwaltung** \> **Allgemein** \> **Wellen** \> **Kanbanwellen** \> **Alle Kanbanwellen**. Wählen Sie im Aktivitätsbereich **Welle erstellen** aus.

1. Wählen Sie die Welle aus. Wählen Sie im Aktivitätsbereich eine der folgenden Optionen aus:

      - **Lieferungen verwalten**
      - **Produktionen verwalten**
      - **Kanban-Einzelvorgangs-Kommissionierlisten**

1. Wählen Sie im oberen Teil des Fensters die Position aus, zu der die Welle hinzugefügt werden soll, und wählen Sie anschließend **Zur Welle hinzufügen**. Die Position wird in das Inforegister **Wellenpositionen** verschoben.

    Wiederholen Sie diesen Schritt für jede hinzuzufügende Position. Um alle Positionen hinzuzufügen, wählen Sie **Alle hinzufügen**.

    > [!TIP]
    > Für Versandwellen können Sie schnell einen spezifischen Auftrag suchen, indem Sie einen benutzerdefinierten Filter im Feld **Wellenfiltercode** auswählen. Wellenfiltercodes enthalten Abfragekriterien für Lieferungen, die im Formular **Wellenfilter** erstellt werden. Dieses Feld ist nicht für Produktionswellen oder Kanbanwellen verfügbar.
    > Ein grünes Häkchen in der Spalte **In Welle** gibt an, dass die Lieferung zur Welle hinzugefügt wurde.

### <a name="process-the-wave-to-create-the-picking-work"></a>Die Welle verarbeiten, um die Entnahmearbeit zu erstellen

Nachdem eine Welle erstellt wurde und alle erforderlichen Positionen hinzugefügt wurden, können Sie sie verarbeiten, um die entsprechende Entnahmearbeit zu erstellen.

#### <a name="automatically-process-a-wave"></a>Eine Welle automatisch verarbeiten

Um eine Welle automatisch zu verarbeiten, legen Sie in den entsprechenden [Wellenvorlagen](wave-templates.md) die erforderlichen automatischen Verarbeitungsoptionen fest.

#### <a name="manually-process-a-wave"></a>Eine Welle manuell verarbeiten

Sie können eine Welle nur verarbeiten, wenn der **Wellenstatus** *Erstellt* lautet. Nachdem Sie eine Welle verarbeitet haben, wird der **Wellenstatus** auf *Angehalten* geändert.

Gehen Sie folgendermaßen vor, um eine Welle mit dem gesamten erforderlichen Inhalt manuell zu verarbeiten:

1. Abhängig vom Typ der Welle, der verarbeitet werden soll, wählen Sie eine der folgenden Optionen:

    - Wechseln Sie zu **Lagerortverwaltung** \> **Allgemein** \> **Wellen** \> **Versandwellen** \> **Alle Wellen**. Wählen Sie im Aktivitätsbereich **Wellen** aus.
    - Wechseln Sie zu **Lagerortverwaltung** \> **Allgemein** \> **Wellen** \> **Produktionswellen** \> **Alle Produktionswellen**. Wählen Sie im Aktivitätsbereich **Produktionswellen** aus.
    - Wählen Sie **Lagerortverwaltung** \> **Allgemein** \> **Wellen** \> **Kanbanwellen** \> **Alle Kanbanwellen**. Wählen Sie im Aktivitätsbereich **Welle erstellen** aus.

1. Wählen Sie die Welle aus, die verarbeitet werden soll. Klicken Sie im Aktivitätsbereich auf **Verarbeiten**.

### <a name="release-the-wave-to-the-warehouse-to-start-picking-and-packing"></a>Die Welle für den Lagerort freigeben, um mit Entnahme und Verpackung zu beginnen

Eine Welle muss vor der Freigabe verarbeitet werden. Wenn Sie die Welle freigeben, ist die Entnahmearbeit am Lagerort verfügbar. Sie können eine Welle nach der Freigabe abbrechen und weitere Positionen hinzufügen, aber Sie können die Positionen nicht ändern.

#### <a name="automatically-release-a-wave"></a>Eine Welle automatisch freigeben

Um eine Welle automatisch zu verarbeiten, legen Sie in den entsprechenden [Wellenvorlagen](wave-templates.md) die erforderlichen automatischen Verarbeitungsoptionen fest.

#### <a name="manually-release-a-wave"></a>Eine Welle manuell freigeben

Führen Sie folgende Schritte aus, um eine Welle manuell freizugeben:

1. Abhängig vom Typ der Welle, der freigegeben werden soll, wählen Sie eine der folgenden Optionen:

      - Wechseln Sie zu **Lagerortverwaltung** \> **Allgemein** \> **Wellen** \> **Versandwellen** \> **Alle Wellen**. Wählen Sie im Aktivitätsbereich **Wellen** aus.
      - Wechseln Sie zu **Lagerortverwaltung** \> **Allgemein** \> **Wellen** \> **Produktionswellen** \> **Alle Produktionswellen**. Wählen Sie im Aktivitätsbereich **Produktionswellen** aus.
      - Wählen Sie **Lagerortverwaltung** \> **Allgemein** \> **Wellen** \> **Kanbanwellen** \> **Alle Kanbanwellen**. Wählen Sie im Aktivitätsbereich **Welle erstellen** aus.

1. Wählen Sie die Welle aus, die freigegeben werden soll. Wählen Sie im Aktivitätsbereich **Welle freigeben** aus.

## <a name="containerize-a-wave"></a>Eine Welle containerisieren

Die automatisierte Containerisierung erstellt Container und die Entnahmearbeit für Lieferungen, wenn eine Welle verarbeitet wird. Einzelheiten zum Einrichten finden Sie unter [Containerisierung](wave-containerization.md).

## <a name="work-with-the-scheduled-work-creation"></a>Mit der geplanten Arbeitserstellung arbeiten

Wenn die Funktion *Arbeitserstellung planen* aktiviert ist, erstellt die Wellenverarbeitung geplante Arbeiten, die schließlich vom neuen Arbeitserstellungsprozess verwendet werden. Während der Arbeitserstellung wird die Arbeit mit der Funktion *Organisationsweite Arbeitssperre* gesperrt. Weitere Informationen finden Sie unter [Planen der Arbeitserstellung während der Welle](configure-wave-schedule-work-creation.md).

Das folgende Flussdiagramm zeigt, wie geplante Arbeiten während der Wellenverarbeitung erstellt werden.

![Arbeitserstellung planen.](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>Geplante Arbeit

Die Seite **Details der geplanten Arbeit** (**Lagerort verwaltung \> Arbeit \> Details der geplanten Arbeit**) zeigt Informationen über die geplante Arbeit an, die anfänglich während der Wellenverarbeitung erstellt werden. Die folgenden **Prozessstatus**-Werte sind verfügbar:

- **In Warteschlange** – Die geplante Arbeit wartet darauf, zur Erstellung von Arbeit verwendet zu werden.
- **Abgeschlossen** – Die geplante Arbeit wurde verwendet, um Arbeit zu erstellen.
- **Fehlgeschlagen** – Die Wellenverarbeitung ist fehlgeschlagen. Beachten Sie, dass die geplante Arbeit mit oder ohne zugehörige tatsächliche Arbeit in einem Status **Fehlgeschlagen** sein kann. Wenn der eigentliche Arbeitserstellungsprozess fehlschlägt, bleibt die eigentliche Arbeit im Status *Storniert*.

### <a name="batch-job-for-the-work-creation-process"></a>Stapelverarbeitungsauftrag für den Arbeitserstellungsprozess

Um die Stapelverarbeitungsaufträge für die Verarbeitung von Wellen anzuzeigen, wählen Sie **Stapelverarbeitungsaufträge** im Aktionsbereich auf der Seite **Alle Wellen** aus.

Von hier aus können Sie alle Details der Stapelverarbeitungsaufgabe für jede der Stapelverarbeitungsauftrags-IDs anzeigen.

## <a name="cancel-a-wave"></a>Eine Welle abbrechen

Bei Bedarf können Sie eine Welle abbrechen, die verarbeitet wurde. Um eine Welle und die Entnahmearbeit, die erstellt wurde, abzubrechen, führen Sie folgende Schritte aus:

1. Abhängig vom Typ der Welle, der abgebrochen werden soll, wählen Sie eine der folgenden Optionen:

      - Gehen Sie zu **Lagerortverwaltung** \> **Allgemein** \> **Wellen** \> **Versandwellen** \> **Alle Wellen**.
      - Gehen Sie zu **Lagerortverwaltung** \> **Allgemein** \> **Wellen** \> **Produktionswellen** \> **Alle Produktionswellen**.
      - Gehen Sie zu **Lagerortverwaltung** \> **Allgemein** \> **Wellen** \> **Kanbanwellen** \> **Alle Kanbanwellen**.

1. Wählen Sie die Welle aus, die abgebrochen werden soll. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Arbeit** die Option **Abbrechen** aus.

## <a name="review-wave-batch-job-details"></a>Wellenstapelverarbeitungsdetails überprüfen

Verwenden Sie die Seite **Wellenstapelverarbeitungsdetails**, um Stapelverarbeitungen und die dazugehörigen Aufgaben zu überprüfen, die mit einer Welle verbunden sind. Dies ist besonders für die Problembehandlung bei einer fehlgeschlagenen Welle nützlich. Ohne diese Funktion haben normalerweise nur Administratoren Zugriff auf Stapelverarbeitungsdetails. Die Seite **Stapelverarbeitungsdetails** kann Nicht-Administratoren zur Verfügung gestellt werden und bietet eine schreibgeschützte Ansicht von Stapelverarbeitungen und den dazugehörigen Aufgaben.

### <a name="enable-the-wave-batch-job-details-page"></a>Seite „Wellenstapelverarbeitungsdetails“ aktivieren

Wenn Ihr System die Seite **Wellenstapelverarbeitungsdetails** noch nicht enthält, gehen Sie zu [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) und schalten Sie die Funktion *Wellenstapelverarbeitungsdetails* an.

### <a name="use-the-wave-batch-job-details-page"></a>Seite „Stapelverarbeitungsdetails“ verwenden

Die Seite **Wellenstapelverarbeitungsdetails** verbindet Stapelverarbeitungen und Stapelverarbeitungsaufgaben, sodass Sie alle Wellenschritte untersuchen können, ohne zwischen einer einzelnen Stapelverarbeitung und einzelnen Stapelverarbeitungsaufgaben hin- und herwechseln zu müssen. Die Seite bietet auch Zugriff auf das Stapelverarbeitungsprotokoll und, wenn Sie über die erforderlichen Berechtigungen verfügen, einen Link zur Seite **Stapelverarbeitungen**.

Um diese Seite zu öffnen, wählen Sie eine Welle auf einer von mehreren verschiedenen Wellenseiten und dann **Wellenstapelverarbeitungsdetails** aus dem Aktivitätsbereich aus.

## <a name="review-load-validation-and-error-messages"></a>Ladungsvalidierungen und Fehlermeldungen überprüfen

Während der Wellenverarbeitung validiert das System den Status für jede Ladungsposition in der Welle und zeigt ihn an. Wenn keine Warnungen auftreten, wird mit dem nächsten Wellenschritt fortgefahren. Wenn Warnungen auftreten, wird stattdessen der folgende Fehler angezeigt, nachdem die Validierung der gesamten Welle abgeschlossen ist:

> In der Welle wurde eine ungültige Ladungsposition gefunden. Bitte entfernen Sie die ungültigen Ladungspositionen.

Sie können dann den endgültigen Status jeder Ladungsposition in der Welle überprüfen und alle Warnungen korrigieren, bevor Sie es erneut versuchen. Auf diese Weise können Sie alle Warnungen gleichzeitig beheben, bevor Sie die Welle erneut verarbeiten. (In früheren Versionen hat das System die Verarbeitung der Welle nach der ersten Warnung gestoppt, sodass Sie Warnungen nur einzeln beheben konnten.)

Wie das System Ihre Wellenverarbeitungsstatusmeldungen anzeigt, hängt davon ab, welche Einstellung Sie bei der Option **Protokoll zum Wellenverarbeitungsverlauf erstellen** auf der Seite **Lagerortverwaltungsparameter** vorgenommen haben.

- Wenn **Protokoll für Wellenverarbeitungsverlauf** auf *Nein* steht, werden die Statusmeldungen der Ladungspositionen im **Infolog** angezeigt.
- Wenn **Protokoll für Wellenverarbeitungsverlauf** auf *Ja* steht, werden die Statusmeldungen der Ladungspositionen auf der Seite **Protokoll für Wellenverarbeitungsverlauf** angezeigt. Um das Protokoll anzuzeigen, gehen Sie zu **Lagerortverwaltung \> Ausgehende Wellen \> Protokoll für Wellenverarbeitungsablauf**.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Wellenverarbeitung konfigurieren – Beispiel](tasks/configure-wave-processing.md)
- [Wellenvorlagen](wave-templates.md)
- [Containerisierung](wave-containerization.md)