---
title: Problembehandlung bei Bestandsvorgängen
description: In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Bestandsvorgängen auftreten können.
author: sherry-zheng
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 24e41e35b3e810c509a16b91fffd1e796ab9d134
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832057"
---
# <a name="troubleshoot-inventory-operations"></a><span data-ttu-id="5035d-103">Problembehandlung bei Bestandsvorgängen</span><span class="sxs-lookup"><span data-stu-id="5035d-103">Troubleshoot inventory operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5035d-104">In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Bestandsvorgängen auftreten können.</span><span class="sxs-lookup"><span data-stu-id="5035d-104">This topic describes how to fix issues that you might encounter while you work with inventory operations.</span></span>

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a><span data-ttu-id="5035d-105">Ich kann das Dropdown-Dialogfeld „Workflow“ für Bestandserfassungen nicht finden.</span><span class="sxs-lookup"><span data-stu-id="5035d-105">I can't find the "Workflow" drop-down dialog box for inventory journals.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5035d-106">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="5035d-106">Issue description</span></span>

<span data-ttu-id="5035d-107">Sie können das Dropdown-Dialogfeld **Workflow** auf der Erfassungsseite nicht finden oder zugehörige Workflowvorgänge sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5035d-107">You can't find the **Workflow** drop-down dialog box on the journal page, or related workflow operations aren't available.</span></span>

<span data-ttu-id="5035d-108">Dieses Problem kann aus drei Gründen auftreten, wie in den folgenden Unterabschnitten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5035d-108">This issue can occur for three reasons, as described in the following subsections.</span></span>

### <a name="issue-resolution-1"></a><span data-ttu-id="5035d-109">Problemlösung 1</span><span class="sxs-lookup"><span data-stu-id="5035d-109">Issue resolution 1</span></span>

<span data-ttu-id="5035d-110">Wenn das Problem für alle Benutzer gilt, kann es auftreten, weil der Genehmigungsworkflow nicht dem Erfassungsnamen zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="5035d-110">If the issue applies to all users, it might be occurring because the approval workflow hasn't been assigned to the journal name.</span></span> <span data-ttu-id="5035d-111">Führen Sie folgende Schritte aus, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="5035d-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="5035d-112">Wechseln Sie zu **Bestandsverwaltung &gt; Einrichten &gt; Erfassungsnamen &gt; Bestand**.</span><span class="sxs-lookup"><span data-stu-id="5035d-112">Go to **Inventory Management &gt; Setup &gt; Journal names &gt; Inventory**.</span></span>
1. <span data-ttu-id="5035d-113">Wählen Sie im Listenbereich einen Erfassungsnamen aus, um seine Einstellungen zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5035d-113">In the list pane, select a journal name to open its settings.</span></span>
1. <span data-ttu-id="5035d-114">Legen Sie im Inforegister **Allgemein** die Option **Genehmigungsworkflow** auf *Ja* fest.</span><span class="sxs-lookup"><span data-stu-id="5035d-114">On the **General** FastTab, set the **Approval workflow** option to *Yes*.</span></span> <span data-ttu-id="5035d-115">Wählen Sie **Ja** aus, wenn Sie zum Bestätigen der Änderung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="5035d-115">If you're prompted to confirm the change, select **Yes**.</span></span>
1. <span data-ttu-id="5035d-116">Wählen Sie im Feld **Workflow** den Workflow aus, den Sie für den ausgewählten Erfassungsnamen verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="5035d-116">In the **Workflow** field, select the workflow that you want to use for the selected journal name.</span></span>

### <a name="issue-resolution-2"></a><span data-ttu-id="5035d-117">Problemlösung 2</span><span class="sxs-lookup"><span data-stu-id="5035d-117">Issue resolution 2</span></span>

<span data-ttu-id="5035d-118">Wenn Ihr Workflow benutzerdefinierten Code verwendet, können nach dem Upgrade des Systems Probleme auftreten.</span><span class="sxs-lookup"><span data-stu-id="5035d-118">If your workflow uses customized code, issues might occur after you upgrade the system.</span></span> <span data-ttu-id="5035d-119">Im Erfassungsworkflow wird beispielsweise eventuell die Schaltläche **Übermitteln** ausgegraut, sodass Sie sie nicht auswählen können, um eine Übermittlung zu genehmigen.</span><span class="sxs-lookup"><span data-stu-id="5035d-119">For example, in the journal workflow, the **Submit** button might be grayed out so you can't select it to approve a submission.</span></span>

<span data-ttu-id="5035d-120">Wenn die Schaltfläche **Übermitteln** ausgegraut ist, wurde möglicherweise Ihr Workflow angepasst. Das bedeutet, dass die Methode des Workflows, `canSubmitToWorkflow()` in `FormDataUtil`, erweitert wurde.</span><span class="sxs-lookup"><span data-stu-id="5035d-120">If the **Submit** button is grayed out, your workflow might have been customized, which means the method of the workflow, `canSubmitToWorkflow()` in `FormDataUtil`, has been extended.</span></span> <span data-ttu-id="5035d-121">Um dieses Problem zu beheben, ändern Sie die Art und Weise, auf die Sie die Methode von `canSubmitToWorkflow()` erweitern, indem Sie die Struktur im folgenden Beispiel verwenden.</span><span class="sxs-lookup"><span data-stu-id="5035d-121">To fix this issue, change the way that you extend the method of the `canSubmitToWorkflow()` to use the structure in the following example.</span></span>

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

### <a name="issue-resolution-3"></a><span data-ttu-id="5035d-122">Problemlösung 3</span><span class="sxs-lookup"><span data-stu-id="5035d-122">Issue resolution 3</span></span>

<span data-ttu-id="5035d-123">Wenn das Problem nur für einige bestimmte Benutzer gilt, verfügen diese Benutzer möglicherweise nicht über die Sicherheitsrechte, die zum Ausführen von Workflowvorgängen für Bestandserfassungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="5035d-123">If the issue applies only to a few specific users, those users might not have the security privileges that are required to run workflow operations on inventory journals.</span></span> <span data-ttu-id="5035d-124">Stellen Sie sicher, dass jeder betroffene Benutzer über das Sicherheitsrecht *Workflow zur Bestandserfassung pflegen* verfügt.</span><span class="sxs-lookup"><span data-stu-id="5035d-124">Verify that each affected user has the *Maintain inventory journal workflow* security privilege.</span></span> <span data-ttu-id="5035d-125">Standardmäßig wird dieses Recht einer Pflicht mit demselben Namen zugewiesen und diese Pflicht wird auf die Rollen *Lagerortarbeitskraft* und *Lagerortleiter* angewendet.</span><span class="sxs-lookup"><span data-stu-id="5035d-125">By default, this privilege is assigned to a duty that has same name, and that duty is applied to the *Warehouse worker* and *Warehouse manager* roles.</span></span>

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a><span data-ttu-id="5035d-126">Meine Bestandserfassung behält den Status „System gesperrt“ bei und der Stapelauftrag für den Workflow funktioniert nicht.</span><span class="sxs-lookup"><span data-stu-id="5035d-126">My inventory journal remains in system-locked status, and the workflow batch job doesn't work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5035d-127">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="5035d-127">Issue description</span></span>

<span data-ttu-id="5035d-128">Eine Ihrer Bestandserassungen ist durch einen Vorgang gesperrt und wird nicht freigegeben.</span><span class="sxs-lookup"><span data-stu-id="5035d-128">One of your inventory journals is locked by some operation and isn't being released.</span></span> <span data-ttu-id="5035d-129">Wenn beispielsweise während der Buchung (einem Vorgang, bei dem das System gesperrt wird) ein unbekannter Fehler auftritt, bleibt die Erfassung möglicherweise im Status „System gesperrt“.</span><span class="sxs-lookup"><span data-stu-id="5035d-129">For example, if an unknown error occurs during posting (which is a system lock operation), the journal might remain in system-locked status.</span></span> <span data-ttu-id="5035d-130">In diesem Fall gibt der Handler für das Workflowarbeitselement einen Fehler aus, während er die Prüfung sperrt.</span><span class="sxs-lookup"><span data-stu-id="5035d-130">In this case, the workflow work item handler will throw an error while it does lock validation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5035d-131">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="5035d-131">Issue resolution</span></span>

<span data-ttu-id="5035d-132">Melden Sie sich bei der SQL Server-Instanz für Supply Chain Management an und prüfen Sie, ob **InventJournalTable.SystemBlocked** auf *1* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5035d-132">Sign in to the SQL Server instance for Supply Chain Management, and check whether **InventJournalTable.SystemBlocked** is set to *1*.</span></span> <span data-ttu-id="5035d-133">Wenn dies der Fall ist, stellen Sie sicher, dass die Erfassung nicht gesperrt ist, und setzen Sie **InventJournalTable.SystemBlocked** dann auf *0* zurück.</span><span class="sxs-lookup"><span data-stu-id="5035d-133">If it is, make sure that the journal should not be in locked status, and then reset **InventJournalTable.SystemBlocked** to *0*.</span></span>

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a><span data-ttu-id="5035d-134">Mein Workflow zur Bestandserfassung wird nie abgeschlossen und die Erfassung kann nicht bearbeitet oder gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="5035d-134">My inventory journal workflow is never completed, and the journal can't be edited or posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5035d-135">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="5035d-135">Issue description</span></span>

<span data-ttu-id="5035d-136">Nachdem Sie einen Workflow zur Genehmigung übermittelt haben, reagiert die Workflowverarbeitung nicht mehr und Sie können Ihre Erfassungen nicht mehr bearbeiten oder verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="5035d-136">After you submit a journal approval workflow, workflow processing stops responding, and you can't edit or process your journals.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5035d-137">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="5035d-137">Issue resolution</span></span>

<span data-ttu-id="5035d-138">Es gibt mehrere Gründe, warum die Workflowverarbeitung möglicherweise nicht abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="5035d-138">There are several reasons why workflow processing might not be completed.</span></span> <span data-ttu-id="5035d-139">Überprüfen Sie, ob folgende Probleme vorliegen:</span><span class="sxs-lookup"><span data-stu-id="5035d-139">Check for the following issues:</span></span>

- <span data-ttu-id="5035d-140">Wechseln Sie zu **Bestandsverwaltung &gt; Einrichten &gt; Bestandsverwaltungsworkflows** und überprüfen Sie die Konfiguration des betroffenen Workflows.</span><span class="sxs-lookup"><span data-stu-id="5035d-140">Go to **Inventory management &gt; Setup &gt; Inventory management workflows**, and review the configuration of the affected workflow.</span></span> <span data-ttu-id="5035d-141">Weitere Informationen finden Sie unter [Workflows zur Genehmigung von Lagererfassungen](inventory-journal-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="5035d-141">For more information, see [Inventory journal approval workflows](inventory-journal-workflow.md).</span></span>
- <span data-ttu-id="5035d-142">Im Workflow ist möglicherweise eine Ausnahme oder ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="5035d-142">The workflow might be encountering an exception or error.</span></span> <span data-ttu-id="5035d-143">Überprüfen Sie für den betroffenen Workflow den Verlauf des Arbeitselements, um festzustellen, ob er einen Anwendungsfehler enthält, der den Workflow beendet.</span><span class="sxs-lookup"><span data-stu-id="5035d-143">Review the work item history of the affected workflow to see whether it includes an application error that terminates the workflow.</span></span>
- <span data-ttu-id="5035d-144">Die Bestandserfassung kann nur aktualisiert oder bearbeitet werden, wenn sie genehmigt wurde.</span><span class="sxs-lookup"><span data-stu-id="5035d-144">The inventory journal can be updated or edited only if it's approved.</span></span> <span data-ttu-id="5035d-145">Wenn ein Rückruf aktiv ist, können Sie versuchen, die Erfassung zurückzurufen.</span><span class="sxs-lookup"><span data-stu-id="5035d-145">If recall is active, you can try to recall the journal.</span></span> <span data-ttu-id="5035d-146">Die Ausführung des Stapelauftrags für den Workflow kann aus mehreren Gründen ausgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="5035d-146">Execution of the workflow batch job might be suspended for multiple reasons.</span></span> <span data-ttu-id="5035d-147">Einige dieser Gründe können durch das Problem mit dem Workflowframework verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="5035d-147">Some of these reasons might be caused by the workflow framework issue.</span></span>

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a><span data-ttu-id="5035d-148">Die Workflowbedingungen für Bestandserfassungen gelten nur auf Erfassungsebene, nicht auf Positionsebene.</span><span class="sxs-lookup"><span data-stu-id="5035d-148">Inventory journal workflow conditions apply only at the journal level, not at the line level</span></span>

### <a name="issue-description"></a><span data-ttu-id="5035d-149">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="5035d-149">Issue description</span></span>

<span data-ttu-id="5035d-150">Dieses Problem kann auftreten, wenn Sie beispielsweise versuchen, eine Workflowbedingung für die Bestandserfassung für den Kostenbetrag einzurichten.</span><span class="sxs-lookup"><span data-stu-id="5035d-150">You might experience this issue if, for example, you try to set up an inventory journal workflow condition on the cost amount.</span></span> <span data-ttu-id="5035d-151">Sie richten die Bedingung so ein, dass Schritt 1 nur ausgeführt wird, wenn der Kostenbetrag kleiner als 100 ist.</span><span class="sxs-lookup"><span data-stu-id="5035d-151">You set up the condition so that step 1 is run only when the cost amount is less than 100.</span></span> <span data-ttu-id="5035d-152">Anschließend richten Sie eine weitere Bedingung so ein, dass Schritt 2 nur ausgeführt wird, wenn der Kostenbetrag größer als oder gleich 100 ist.</span><span class="sxs-lookup"><span data-stu-id="5035d-152">You then set up another condition so that step 2 is run only when the cost amount is more than or equal to 100.</span></span> <span data-ttu-id="5035d-153">Wenn der Workflow ausgeführt wird, zeigt die Workflowhistorie nur eine Position an und die erste Bedingung wird immer als *True* ausgewertet, unabhängig vom übermittelten Wert.</span><span class="sxs-lookup"><span data-stu-id="5035d-153">Then, when the workflow is run, the workflow history shows only one line, and the first condition is always evaluated as *true*, regardless of the value that is submitted.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="5035d-154">Problemumgehung</span><span class="sxs-lookup"><span data-stu-id="5035d-154">Issue workaround</span></span>

<span data-ttu-id="5035d-155">Im aktuellen Release gelten die Workflowbedingungen für Bestandserfassungen nur auf Erfassungsebene, nicht auf Positionsebene.</span><span class="sxs-lookup"><span data-stu-id="5035d-155">In the current release, inventory workflow conditions apply only at the journal level, not at the line level.</span></span> <span data-ttu-id="5035d-156">Dieses Verhalten ist beabsichtigt.</span><span class="sxs-lookup"><span data-stu-id="5035d-156">This behavior is by design.</span></span> <span data-ttu-id="5035d-157">Wir empfehlen, dass Sie Ihre Bedingungskriterien nur für Attribute auf Erfassungsebene festlegen.</span><span class="sxs-lookup"><span data-stu-id="5035d-157">We recommend that you set your condition criteria only on journal-level attributes.</span></span>

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a><span data-ttu-id="5035d-158">Der Filterbereich auf der Seite „Bestandsliste“ filtert die Ergebnisse nicht wie erwartet.</span><span class="sxs-lookup"><span data-stu-id="5035d-158">The filter pane on the On-hand list page doesn't filter results as I expect.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5035d-159">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="5035d-159">Issue description</span></span>

<span data-ttu-id="5035d-160">Die Filter im Filterbereich auf der Seite **Bestandsliste**  filtert die Ergebnisse nicht wie erwartet.</span><span class="sxs-lookup"><span data-stu-id="5035d-160">The filters in the filter pane on the **On-hand list** page don't filter results as you expect.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5035d-161">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="5035d-161">Issue resolution</span></span>

<span data-ttu-id="5035d-162">Dieses Verhalten ist beabsichtigt.</span><span class="sxs-lookup"><span data-stu-id="5035d-162">This behavior is by design.</span></span>

<span data-ttu-id="5035d-163">Die Seite  **Bestandsliste**  wird aus einer detaillierten Bestandstabelle zusammengestellt, die alle verfügbaren Dimensionen enthält.</span><span class="sxs-lookup"><span data-stu-id="5035d-163">The **On-hand list** page is assembled from a detailed on-hand inventory table that includes all available dimensions.</span></span> <span data-ttu-id="5035d-164">Die Liste auf dieser Seite ist jedoch eine Zusammenfassung.</span><span class="sxs-lookup"><span data-stu-id="5035d-164">However, the list on this page is a summary.</span></span> <span data-ttu-id="5035d-165">Daher können Zeilen aus der Quelltabelle kombiniert werden, indem Werte gemäß den angezeigten Dimensionen aggregiert werden.</span><span class="sxs-lookup"><span data-stu-id="5035d-165">Therefore, it might combine rows from the source table by aggregating values according to the dimensions that are shown.</span></span>

<span data-ttu-id="5035d-166">Filter, die im Filterereich eingerichet werden, gelten für die Quelltabelle und nicht für die aggregierte Liste.</span><span class="sxs-lookup"><span data-stu-id="5035d-166">Filters that are set up in the filter pane apply to the source table, not to the aggregated list.</span></span> <span data-ttu-id="5035d-167">Dieses Verhalten kann manchmal zu unerwarteten Ergebnissen führen, wie in [diesen Beispielen](inventory-on-hand-list.md#examples) zu sehen ist.</span><span class="sxs-lookup"><span data-stu-id="5035d-167">This behavior can sometimes produce unexpected results, as shown in [these examples](inventory-on-hand-list.md#examples).</span></span>

<span data-ttu-id="5035d-168">Die  [Filter, die im Raster bereitgestellt werden](inventory-on-hand-list.md#grid-filters) *, gelten*  jedoch für die aggregierte Liste.</span><span class="sxs-lookup"><span data-stu-id="5035d-168">However, the [filters that are provided in the grid](inventory-on-hand-list.md#grid-filters) *do* apply to the aggregated list.</span></span> <span data-ttu-id="5035d-169">Diese Filter enthalten sowohl QuickFilter am oberen Rand des Rasters als auch den Filter für jede Spaltenüberschrift.</span><span class="sxs-lookup"><span data-stu-id="5035d-169">These filters include both the QuickFilter at the top of the grid and the filter for each column heading.</span></span>

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a><span data-ttu-id="5035d-170">Die Einheit und die Stückzahl funktionieren in der Bestandserfassung nicht richtig.</span><span class="sxs-lookup"><span data-stu-id="5035d-170">The unit and unit quantity aren't working correctly in the inventory journal.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5035d-171">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="5035d-171">Issue description</span></span>

<span data-ttu-id="5035d-172">Bei der Arbeit mit Einheiten und Mengen in einer Bestandserfassung können eines oder beide der folgenden Probleme auftreten:</span><span class="sxs-lookup"><span data-stu-id="5035d-172">You might encounter one or both of the following issues when you work with units and quantities in an inventory journal:</span></span>

- <span data-ttu-id="5035d-173">Sie sehen keine Einheiten oder Stückzahlen in der Bestandserfassung, obwohl eine Umrechnungseinheit für das freigegebene Produkt eingerichtet ist, und Sie können die Einheit in der Bestandserfassung nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="5035d-173">You don't see units or unit quantities in the inventory journal while a unit of conversion is set up for the released product, and you can't change the unit in the inventory journal.</span></span>
- <span data-ttu-id="5035d-174">Sie sehen die Felder **Menge** und **Einheit** in der Bestandserfassung, das Feld **Stückzahl** aber nicht.</span><span class="sxs-lookup"><span data-stu-id="5035d-174">You see the **Quantity** and **Unit** fields in the inventory journal, but you don't see the **Unit quantity** field.</span></span> <span data-ttu-id="5035d-175">Wenn Sie die Einheit ändern, eine Menge eingeben und die Erfassung buchen, zeigt die Erfassung weiterhin die ursprüngliche Messung für diese Menge an.</span><span class="sxs-lookup"><span data-stu-id="5035d-175">If you change the unit, enter a quantity, and post the journal, the journal still shows the original unit of measurement for that quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5035d-176">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="5035d-176">Issue resolution</span></span>

<span data-ttu-id="5035d-177">Führen Sie folgende Schritte aus, um dieses Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="5035d-177">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="5035d-178">Stellen Sie im Arbeitsbereich **Funktionsverwaltung** sicher, dass die Funktion *Maßeinheit und Stückzahl in Bestandserfassungen* verwenden aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5035d-178">In the **Feature management** workspace, make sure that the *Using unit of measure and unit quantity in inventory journals* feature is turned on.</span></span> <span data-ttu-id="5035d-179">Diese Funktion fügt die Felder **Einheit** und **Stückzahl** zur Erfassung hinzu.</span><span class="sxs-lookup"><span data-stu-id="5035d-179">This feature adds the **Unit** and **Unit quantity** fields to the journal.</span></span>
1. <span data-ttu-id="5035d-180">Verwenden Sie nach dem Einschalten der Funktion die Felder **Menge**, **Stückzahl** und **Einheit** wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5035d-180">After the feature is turned on, use the **Quantity**, **Unit quantity**, and **Unit** fields in the following way:</span></span>

    - <span data-ttu-id="5035d-181">**Menge** – Geben Sie die Menge unter Verwendung der Standardeinheit an, die für das freigegebene Produkt definiert ist.</span><span class="sxs-lookup"><span data-stu-id="5035d-181">**Quantity** – Specify the quantity by using the default unit that is defined for the released product.</span></span> <span data-ttu-id="5035d-182">Die Standardeinheit selbst wird hier jedoch nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5035d-182">However, the default unit itself isn't shown here.</span></span> <span data-ttu-id="5035d-183">Wenn eine Umrechnung zwischen der Standardeinheit und der im Feld **Einheit** ausgewählten Einheit eingerichtet ist, wird das Feld **Menge** basierend auf der Auswahl in den Feldern **Stückzahl** und **Einheit** automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5035d-183">If a conversion is set up between the default unit and the unit that is selected in the **Unit** field, the **Quantity** field is automatically updated, based on the selections in the **Unit quantity** and **Unit** fields.</span></span>
    - <span data-ttu-id="5035d-184">**Stückzahl** – Geben Sie die Menge unter Verwendung der Einheit an, die im Feld **Einheit** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="5035d-184">**Unit quantity** – Specify the quantity by using the unit that is selected in the **Unit** field.</span></span>
    - <span data-ttu-id="5035d-185">**Einheit** – Wählen Sie die Einheit aus, die auf den Wert im Feld **Stückzahl** angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5035d-185">**Unit** – Select the unit to apply to the value in the **Unit quantity** field.</span></span>

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a><span data-ttu-id="5035d-186">Ich erhalte die folgende Fehlermeldung: „Die maximale Anzahl von Dezimalstellen für die Lagermengeneinheit beträgt 0.“</span><span class="sxs-lookup"><span data-stu-id="5035d-186">I receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

### <a name="issue-description"></a><span data-ttu-id="5035d-187">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="5035d-187">Issue description</span></span>

<span data-ttu-id="5035d-188">Wenn Sie versuchen, eine Bestandstransaktion oder eine Bestandsreservierung zu buchen, wird die folgende Fehlermeldung angezeigt: „Die maximale Anzahl von Dezimalstellen für die Lagermengeneinheit beträgt 0.“</span><span class="sxs-lookup"><span data-stu-id="5035d-188">When you try to post an inventory transaction or an inventory reservation, you receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

<span data-ttu-id="5035d-189">Dieses Problem tritt auf, wenn die Bestandstransaktionsmenge als Dezimalwert angegeben wird, der unter der vom Feld unterstützten Genauigkeit liegt.</span><span class="sxs-lookup"><span data-stu-id="5035d-189">This issue occurs when the inventory transaction quantity is specified as a decimal value that is below the level of precision that the field supports.</span></span> <span data-ttu-id="5035d-190">Beispiel: Für eine Bestandstransaktion wurde eine Menge von *0,5* angegeben, es werden jedoch nur ganzzahlige Mengen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5035d-190">For example, a quantity of *0.5* has been specified for an inventory transaction, but only integer quantities are supported.</span></span> <span data-ttu-id="5035d-191">Daher sollte der Wert *1* statt *0,5* sein.</span><span class="sxs-lookup"><span data-stu-id="5035d-191">Therefore, the value should be *1* instead of *0.5*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5035d-192">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="5035d-192">Issue resolution</span></span>

1. <span data-ttu-id="5035d-193">Führen Sie das folgende Skript auf Ihrer SQL Server-Instanz aus, um Mengen in den Bestandstransaktionen zu runden.</span><span class="sxs-lookup"><span data-stu-id="5035d-193">Run the following script on your SQL Server instance to round quantities in the inventory transactions.</span></span> <span data-ttu-id="5035d-194">Dieses Skript korrigiert Werte in der Tabelle **inventTrans**.</span><span class="sxs-lookup"><span data-stu-id="5035d-194">This script will correct values in the **inventTrans** table.</span></span>

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. <span data-ttu-id="5035d-195">Führen Sie eine Konsistenzprüfung des verfügbaren Bestands durch, bei der die Option **Fehler beheben** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5035d-195">Run an on-hand consistency check where the **fix error** option is turned on.</span></span> <span data-ttu-id="5035d-196">Diese Überprüfung korrigiert Werte in der Tabelle **inventSum**.</span><span class="sxs-lookup"><span data-stu-id="5035d-196">This check will correct values in the **inventSum** table.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5035d-197">Wir empfehlen dringend, dass Sie das Skript entsprechend Ihrer Umgebung sorgfältig bearbeiten, es in einer Testumgebung testen und dann die resultierenden Daten überprüfen, bevor Sie das Skript in einer Produktionsumgebung ausführen.</span><span class="sxs-lookup"><span data-stu-id="5035d-197">We strongly recommend that you carefully edit the script as required for your environment, test it in a test environment, and then check the resulting data before you run the script in a production environment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]