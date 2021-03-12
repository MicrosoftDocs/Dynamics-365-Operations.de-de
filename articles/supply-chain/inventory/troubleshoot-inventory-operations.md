---
title: Problembehandlung bei Bestandsvorgängen
description: In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Bestandsvorgängen auftreten können.
author: sherry-zheng
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3a22229106753d265a90f0ef05f5ac82dc745bbd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967154"
---
# <a name="troubleshoot-inventory-operations"></a>Problembehandlung bei Bestandsvorgängen

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Bestandsvorgängen auftreten können.

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>Ich kann das Dropdown-Dialogfeld „Workflow“ für Bestandserfassungen nicht finden.

### <a name="issue-description"></a>Problembeschreibung

Sie können das Dropdown-Dialogfeld **Workflow** auf der Erfassungsseite nicht finden oder zugehörige Workflowvorgänge sind nicht verfügbar.

Dieses Problem kann aus drei Gründen auftreten, wie in den folgenden Unterabschnitten beschrieben.

### <a name="issue-resolution-1"></a>Problemlösung 1

Wenn das Problem für alle Benutzer gilt, kann es auftreten, weil der Genehmigungsworkflow nicht dem Erfassungsnamen zugewiesen wurde. Führen Sie folgende Schritte aus, um das Problem zu beheben.

1. Wechseln Sie zu **Bestandsverwaltung &gt; Einrichten &gt; Erfassungsnamen &gt; Bestand**.
1. Wählen Sie im Listenbereich einen Erfassungsnamen aus, um seine Einstellungen zu öffnen.
1. Legen Sie im Inforegister **Allgemein** die Option **Genehmigungsworkflow** auf *Ja* fest. Wählen Sie **Ja** aus, wenn Sie zum Bestätigen der Änderung aufgefordert werden.
1. Wählen Sie im Feld **Workflow** den Workflow aus, den Sie für den ausgewählten Erfassungsnamen verwenden möchten.

### <a name="issue-resolution-2"></a>Problemlösung 2

Wenn Ihr Workflow benutzerdefinierten Code verwendet, können nach dem Upgrade des Systems Probleme auftreten. Im Erfassungsworkflow wird beispielsweise eventuell die Schaltläche **Übermitteln** ausgegraut, sodass Sie sie nicht auswählen können, um eine Übermittlung zu genehmigen.

Wenn die Schaltfläche **Übermitteln** ausgegraut ist, wurde möglicherweise Ihr Workflow angepasst. Das bedeutet, dass die Methode des Workflows, `canSubmitToWorkflow()` in `FormDataUtil`, erweitert wurde. Um dieses Problem zu beheben, ändern Sie die Art und Weise, auf die Sie die Methode von `canSubmitToWorkflow()` erweitern, indem Sie die Struktur im folgenden Beispiel verwenden.

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a>Problemlösung 3

Wenn das Problem nur für einige bestimmte Benutzer gilt, verfügen diese Benutzer möglicherweise nicht über die Sicherheitsrechte, die zum Ausführen von Workflowvorgängen für Bestandserfassungen erforderlich sind. Stellen Sie sicher, dass jeder betroffene Benutzer über das Sicherheitsrecht *Workflow zur Bestandserfassung pflegen* verfügt. Standardmäßig wird dieses Recht einer Pflicht mit demselben Namen zugewiesen und diese Pflicht wird auf die Rollen *Lagerortarbeitskraft* und *Lagerortleiter* angewendet.

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a>Meine Bestandserfassung behält den Status „System gesperrt“ bei und der Stapelauftrag für den Workflow funktioniert nicht.

### <a name="issue-description"></a>Problembeschreibung

Eine Ihrer Bestandserassungen ist durch einen Vorgang gesperrt und wird nicht freigegeben. Wenn beispielsweise während der Buchung (einem Vorgang, bei dem das System gesperrt wird) ein unbekannter Fehler auftritt, bleibt die Erfassung möglicherweise im Status „System gesperrt“. In diesem Fall gibt der Handler für das Workflowarbeitselement einen Fehler aus, während er die Prüfung sperrt.

### <a name="issue-resolution"></a>Problemlösung

Melden Sie sich bei der SQL Server-Instanz für Supply Chain Management an und prüfen Sie, ob **InventJournalTable.SystemBlocked** auf *1* festgelegt ist. Wenn dies der Fall ist, stellen Sie sicher, dass die Erfassung nicht gesperrt ist, und setzen Sie **InventJournalTable.SystemBlocked** dann auf *0* zurück.

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a>Mein Workflow zur Bestandserfassung wird nie abgeschlossen und die Erfassung kann nicht bearbeitet oder gebucht werden.

### <a name="issue-description"></a>Problembeschreibung

Nachdem Sie einen Workflow zur Genehmigung übermittelt haben, reagiert die Workflowverarbeitung nicht mehr und Sie können Ihre Erfassungen nicht mehr bearbeiten oder verarbeiten.

### <a name="issue-resolution"></a>Problemlösung

Es gibt mehrere Gründe, warum die Workflowverarbeitung möglicherweise nicht abgeschlossen wird. Überprüfen Sie, ob folgende Probleme vorliegen:

- Wechseln Sie zu **Bestandsverwaltung &gt; Einrichten &gt; Bestandsverwaltungsworkflows** und überprüfen Sie die Konfiguration des betroffenen Workflows. Weitere Informationen finden Sie unter [Workflows zur Genehmigung von Lagererfassungen](inventory-journal-workflow.md).
- Im Workflow ist möglicherweise eine Ausnahme oder ein Fehler aufgetreten. Überprüfen Sie für den betroffenen Workflow den Verlauf des Arbeitselements, um festzustellen, ob er einen Anwendungsfehler enthält, der den Workflow beendet.
- Die Bestandserfassung kann nur aktualisiert oder bearbeitet werden, wenn sie genehmigt wurde. Wenn ein Rückruf aktiv ist, können Sie versuchen, die Erfassung zurückzurufen. Die Ausführung des Stapelauftrags für den Workflow kann aus mehreren Gründen ausgesetzt werden. Einige dieser Gründe können durch das Problem mit dem Workflowframework verursacht werden.

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a>Die Workflowbedingungen für Bestandserfassungen gelten nur auf Erfassungsebene, nicht auf Positionsebene.

### <a name="issue-description"></a>Problembeschreibung

Dieses Problem kann auftreten, wenn Sie beispielsweise versuchen, eine Workflowbedingung für die Bestandserfassung für den Kostenbetrag einzurichten. Sie richten die Bedingung so ein, dass Schritt 1 nur ausgeführt wird, wenn der Kostenbetrag kleiner als 100 ist. Anschließend richten Sie eine weitere Bedingung so ein, dass Schritt 2 nur ausgeführt wird, wenn der Kostenbetrag größer als oder gleich 100 ist. Wenn der Workflow ausgeführt wird, zeigt die Workflowhistorie nur eine Position an und die erste Bedingung wird immer als *True* ausgewertet, unabhängig vom übermittelten Wert.

### <a name="issue-workaround"></a>Problemumgehung

Im aktuellen Release gelten die Workflowbedingungen für Bestandserfassungen nur auf Erfassungsebene, nicht auf Positionsebene. Dieses Verhalten ist beabsichtigt. Wir empfehlen, dass Sie Ihre Bedingungskriterien nur für Attribute auf Erfassungsebene festlegen.

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a>Der Filterbereich auf der Seite „Bestandsliste“ filtert die Ergebnisse nicht wie erwartet.

### <a name="issue-description"></a>Problembeschreibung

Die Filter im Filterbereich auf der Seite **Bestandsliste**  filtert die Ergebnisse nicht wie erwartet.

### <a name="issue-resolution"></a>Problemlösung

Dieses Verhalten ist beabsichtigt.

Die Seite  **Bestandsliste**  wird aus einer detaillierten Bestandstabelle zusammengestellt, die alle verfügbaren Dimensionen enthält. Die Liste auf dieser Seite ist jedoch eine Zusammenfassung. Daher können Zeilen aus der Quelltabelle kombiniert werden, indem Werte gemäß den angezeigten Dimensionen aggregiert werden.

Filter, die im Filterereich eingerichet werden, gelten für die Quelltabelle und nicht für die aggregierte Liste. Dieses Verhalten kann manchmal zu unerwarteten Ergebnissen führen, wie in [diesen Beispielen](inventory-on-hand-list.md#examples) zu sehen ist.

Die  [Filter, die im Raster bereitgestellt werden](inventory-on-hand-list.md#grid-filters) *, gelten*  jedoch für die aggregierte Liste. Diese Filter enthalten sowohl QuickFilter am oberen Rand des Rasters als auch den Filter für jede Spaltenüberschrift.

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>Die Einheit und die Stückzahl funktionieren in der Bestandserfassung nicht richtig.

### <a name="issue-description"></a>Problembeschreibung

Bei der Arbeit mit Einheiten und Mengen in einer Bestandserfassung können eines oder beide der folgenden Probleme auftreten:

- Sie sehen keine Einheiten oder Stückzahlen in der Bestandserfassung, obwohl eine Umrechnungseinheit für das freigegebene Produkt eingerichtet ist, und Sie können die Einheit in der Bestandserfassung nicht ändern.
- Sie sehen die Felder **Menge** und **Einheit** in der Bestandserfassung, das Feld **Stückzahl** aber nicht. Wenn Sie die Einheit ändern, eine Menge eingeben und die Erfassung buchen, zeigt die Erfassung weiterhin die ursprüngliche Messung für diese Menge an.

### <a name="issue-resolution"></a>Problemlösung

Führen Sie folgende Schritte aus, um dieses Problem zu beheben.

1. Stellen Sie im Arbeitsbereich **Funktionsverwaltung** sicher, dass die Funktion *Maßeinheit und Stückzahl in Bestandserfassungen* verwenden aktiviert ist. Diese Funktion fügt die Felder **Einheit** und **Stückzahl** zur Erfassung hinzu.
1. Verwenden Sie nach dem Einschalten der Funktion die Felder **Menge**, **Stückzahl** und **Einheit** wie folgt:

    - **Menge** – Geben Sie die Menge unter Verwendung der Standardeinheit an, die für das freigegebene Produkt definiert ist. Die Standardeinheit selbst wird hier jedoch nicht angezeigt. Wenn eine Umrechnung zwischen der Standardeinheit und der im Feld **Einheit** ausgewählten Einheit eingerichtet ist, wird das Feld **Menge** basierend auf der Auswahl in den Feldern **Stückzahl** und **Einheit** automatisch aktualisiert.
    - **Stückzahl** – Geben Sie die Menge unter Verwendung der Einheit an, die im Feld **Einheit** ausgewählt ist.
    - **Einheit** – Wählen Sie die Einheit aus, die auf den Wert im Feld **Stückzahl** angewendet werden soll.

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Ich erhalte die folgende Fehlermeldung: „Die maximale Anzahl von Dezimalstellen für die Lagermengeneinheit beträgt 0.“

### <a name="issue-description"></a>Problembeschreibung

Wenn Sie versuchen, eine Bestandstransaktion oder eine Bestandsreservierung zu buchen, wird die folgende Fehlermeldung angezeigt: „Die maximale Anzahl von Dezimalstellen für die Lagermengeneinheit beträgt 0.“

Dieses Problem tritt auf, wenn die Bestandstransaktionsmenge als Dezimalwert angegeben wird, der unter der vom Feld unterstützten Genauigkeit liegt. Beispiel: Für eine Bestandstransaktion wurde eine Menge von *0,5* angegeben, es werden jedoch nur ganzzahlige Mengen unterstützt. Daher sollte der Wert *1* statt *0,5* sein.

### <a name="issue-resolution"></a>Problemlösung

1. Führen Sie das folgende Skript auf Ihrer SQL Server-Instanz aus, um Mengen in den Bestandstransaktionen zu runden. Dieses Skript korrigiert Werte in der Tabelle **inventTrans**.

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. Führen Sie eine Konsistenzprüfung des verfügbaren Bestands durch, bei der die Option **Fehler beheben** aktiviert ist. Diese Überprüfung korrigiert Werte in der Tabelle **inventSum**.

> [!IMPORTANT]
> Wir empfehlen dringend, dass Sie das Skript entsprechend Ihrer Umgebung sorgfältig bearbeiten, es in einer Testumgebung testen und dann die resultierenden Daten überprüfen, bevor Sie das Skript in einer Produktionsumgebung ausführen.
