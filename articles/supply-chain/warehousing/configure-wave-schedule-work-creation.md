---
title: Planen Sie der Arbeitserstellung während der Welle
description: In diesem Thema wird beschrieben, wie Sie die Wellenverarbeitungsmethode „Arbeitserstellung planen“ einrichten und verwenden.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 36a450f78695f617056875f8d236fe46bc66aaaf
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501221"
---
# <a name="schedule-work-creation-during-wave"></a><span data-ttu-id="7e40a-103">Planen Sie der Arbeitserstellung während der Welle</span><span class="sxs-lookup"><span data-stu-id="7e40a-103">Schedule work creation during wave</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="7e40a-104">Verwenden Sie die Funktion *Arbeitserstellung planen* als Teil Ihres Wellenprozesses, um den Wellenverarbeitungsdurchsatz zu erhöhen, indem das System Arbeit mit paralleler Verarbeitung erstellt.</span><span class="sxs-lookup"><span data-stu-id="7e40a-104">Use the *Schedule work creation* feature as part of your waving process to help increase wave processing throughput by having the system create work using parallel processing.</span></span>

<span data-ttu-id="7e40a-105">Wenn die Funktionalität aktiviert ist, werden geplante Arbeiten automatisch erstellt, die das System schließlich verarbeitet, um tatsächliche Arbeiten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7e40a-105">When the functionality is enabled, planned work will automatically get created, which the system will eventually process to create actual work.</span></span> <span data-ttu-id="7e40a-106">Wenn die Anzahl der Wellenladungspositionen einen vorgegebenen Schwellenwert erreicht, erstellt das System durch parallele asynchrone Verarbeitung schneller tatsächliche Arbeit.</span><span class="sxs-lookup"><span data-stu-id="7e40a-106">If the number of wave load lines reaches a predetermined threshold, the system will create actual work more quickly by applying parallel, asynchronous processing.</span></span>

## <a name="enable-the-schedule-work-creation-feature"></a><span data-ttu-id="7e40a-107">Aktivieren der Funktion zum Erstellen von Arbeit</span><span class="sxs-lookup"><span data-stu-id="7e40a-107">Enable the Schedule work creation feature</span></span>

### <a name="enable-the-feature-in-feature-management"></a><span data-ttu-id="7e40a-108">Aktivieren der Funktion in der Funktionsverwaltung</span><span class="sxs-lookup"><span data-stu-id="7e40a-108">Enable the feature in feature management</span></span>

<span data-ttu-id="7e40a-109">Bevor Sie die Funktion *Arbeitserstellung planen* verwenden können, muss sie in Ihrem System eingeschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="7e40a-109">Before you can use the *Schedule work creation* feature, it must be turned on in your system.</span></span> <span data-ttu-id="7e40a-110">Administratoren können mit der Einstellung [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7e40a-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="7e40a-111">Dort wird die Funktion folgendermaßen aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="7e40a-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="7e40a-112">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="7e40a-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="7e40a-113">**Funktionsname:** *Arbeitserstellung planen*</span><span class="sxs-lookup"><span data-stu-id="7e40a-113">**Feature name:** *Schedule work creation*</span></span>

> [!NOTE]
> <span data-ttu-id="7e40a-114">Die Funktion *Organisationsweite Arbeitssperre* muss aktiviert sein, bevor Sie *Arbeitserstellung planen* aktivieren können.</span><span class="sxs-lookup"><span data-stu-id="7e40a-114">The *Organization-wide work blocking* feature must be enabled before you can enable *Schedule work creation*.</span></span>

### <a name="manually-enable-batch-processing-of-waves"></a><span data-ttu-id="7e40a-115">Die Stapelverarbeitung von Wellen manuell aktivieren</span><span class="sxs-lookup"><span data-stu-id="7e40a-115">Manually enable batch processing of waves</span></span>

<span data-ttu-id="7e40a-116">Um eine parallele asynchrone Methode zum Erstellen von Lagerarbeiten nutzen zu können, muss Ihr Wellenprozess im Stapel ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7e40a-116">To take advantage of a parallel asynchronous method to create warehouse work, your wave process must be running in batch.</span></span> <span data-ttu-id="7e40a-117">So richten Sie dies ein:</span><span class="sxs-lookup"><span data-stu-id="7e40a-117">To set this up:</span></span>

1. <span data-ttu-id="7e40a-118">Wechseln Sie zu  **Lagerortverwaltung \>  Einstellungen \> Lagerortverwaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="7e40a-118">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>

1. <span data-ttu-id="7e40a-119">Setzen Sie auf der Registerkarte **Allgemein** die Option **Wellen in einem Stapel verarbeiten** auf *Ja*.</span><span class="sxs-lookup"><span data-stu-id="7e40a-119">On the **General** tab, set **Process waves in batch** to *Yes*.</span></span> <span data-ttu-id="7e40a-120">Optional können Sie auch eine dedizierte **Stapelverarbeitungsgruppe Wellenverarbeitung** auswählen, um zu verhindern, dass Ihre Stapelwarteschlangenverarbeitung gleichzeitig mit anderen Prozessen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7e40a-120">Optionally, you can also select a dedicated **Wave processing batch group** to prevent your batch queue processing from running at the same time as other processes.</span></span>

1. <span data-ttu-id="7e40a-121">Stellen Sie die Zeit von **Auf Sperre warten (ms)** ein, die gilt, wenn das System mehrere Wellen gleichzeitig verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="7e40a-121">Set the **Wait for lock (ms) time**, which applies when the system is processing several waves at the same time.</span></span> <span data-ttu-id="7e40a-122">Für die meisten größeren Wellenprozesse empfehlen wir einen Wert von *60000*.</span><span class="sxs-lookup"><span data-stu-id="7e40a-122">For most larger waving processes, we recommend a value of *60000*.</span></span>

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a><span data-ttu-id="7e40a-123">Manuelles Aktivieren der neuen Wellenschrittmethode für vorhandene Wellenvorlagen</span><span class="sxs-lookup"><span data-stu-id="7e40a-123">Manually enable the new wave step method for existing wave templates</span></span>

<span data-ttu-id="7e40a-124">Erstellen Sie zunächst die neue Wellenschrittmethode, und aktivieren Sie sie für die parallele asynchrone Aufgabenverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="7e40a-124">Start by creating the new wave step method and enabling it for parallel asynchronous task processing.</span></span>

1. <span data-ttu-id="7e40a-125">Wechseln Sie zu  **Lagerortverwaltung \> Setup \> Wellen \> Wellenverarbeitungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="7e40a-125">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>

1. <span data-ttu-id="7e40a-126">Wählen Sie  **Methode erneut generieren** aus, und beachten Sie, dass *WHSScheduleWorkCreationWaveStepMethod* der Liste der Wellenprozessmethoden hinzugefügt wurde, die Sie in Ihren Versandwellenvorlagen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="7e40a-126">Select  **Regenerate method** and note that *WHSScheduleWorkCreationWaveStepMethod* has been added to the list of wave process methods you can use in your shipping wave templates.</span></span>

1. <span data-ttu-id="7e40a-127">Wählen Sie den Datensatz mit dem **Methodennamen** *WHSScheduleWorkCreationWaveStepMethod* und dann **Aufgabenkonfiguration** aus.</span><span class="sxs-lookup"><span data-stu-id="7e40a-127">Select the record with the **Method name** *WHSScheduleWorkCreationWaveStepMethod* and select **Task configuration**.</span></span>

1. <span data-ttu-id="7e40a-128">Wählen Sie im Aktivitätsbereich **Neu** aus, um dem Raster eine Zeile hinzuzufügen, und verwenden Sie die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="7e40a-128">To add a new row to the grid, select **New** on the Action Pane and use the following settings:</span></span>

    - <span data-ttu-id="7e40a-129">**Lagerort** – Wählen Sie das Lager aus, in dem Sie die Verarbeitung der Arbeitserstellung planen möchten.</span><span class="sxs-lookup"><span data-stu-id="7e40a-129">**Warehouse** - Select the warehouse you will use to schedule work creation processing.</span></span>

    - <span data-ttu-id="7e40a-130">**Maximale Anzahl an Stapelverarbeitungsaufgaben** – Geben Sie eine maximale Anzahl von Stapelverarbeitungsaufgaben an.</span><span class="sxs-lookup"><span data-stu-id="7e40a-130">**Maximum number of batch tasks** - Specify a maximum number of batch tasks.</span></span> <span data-ttu-id="7e40a-131">In den meisten Fällen sollte dieser Wert im Bereich von 8 bis 16 liegen. Wir empfehlen jedoch, mit der optimalen Einstellung basierend auf Ihren Szenarien zu experimentieren.</span><span class="sxs-lookup"><span data-stu-id="7e40a-131">In most cases, this value should be in the range from 8-16, however we recommend that you experiment with the optimal setting based on your scenarios.</span></span>

    - <span data-ttu-id="7e40a-132">**Stapelverarbeitungsgruppe Wellenverarbeitung** – Wählen Sie eine dedizierte Stapelverarbeitungsgruppe der Wellenverarbeitung aus, um die Verarbeitung Ihrer Stapelverarbeitungswarteschlange zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="7e40a-132">**Wave processing batch group** - Select a dedicated wave processing batch group to optimize your batch queue processing.</span></span>

<span data-ttu-id="7e40a-133">Jetzt können Sie eine vorhandene Wellenvorlage aktualisieren (oder eine neue erstellen), um die Wellenverarbeitungsmethode *Arbeitserstellung planen* zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7e40a-133">Now you are ready to update an existing wave template (or create a new one) to use the *Schedule work creation* wave processing method.</span></span>

1. <span data-ttu-id="7e40a-134">Wechseln Sie zu  **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="7e40a-134">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>

1. <span data-ttu-id="7e40a-135">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="7e40a-135">Select **Edit** on the Action Pane.</span></span>

1. <span data-ttu-id="7e40a-136">Wählen Sie im Listenbereich die Wellenvorlage aus, die Sie aktualisieren möchten (wenn Sie mit Demodaten testen, können Sie *Standard-24-Lieferung* verwenden).</span><span class="sxs-lookup"><span data-stu-id="7e40a-136">In the list pane, select the wave template you would like to update (if you are testing using demo data, then you could use *24 Shipping default*).</span></span>

1. <span data-ttu-id="7e40a-137">Erweitern Sie das Inforegister **Methoden**, und wählen Sie die Zeile mit dem **Namen** *Arbeitserstellung planen* im Raster **Verbleibende Methoden** aus.</span><span class="sxs-lookup"><span data-stu-id="7e40a-137">Expand the **Methods** FastTab and select the row with the **Name** *Schedule work creation* in the **Remaining methods** grid.</span></span>

1. <span data-ttu-id="7e40a-138">Wählen Sie den Pfeil aus, der auf die Spalte **Ausgewählte Methoden** zeigt, um die ausgewählte Zeile in diese Spalte zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="7e40a-138">Select the arrow pointing to the **Selected methods** column to move the selected row to that column.</span></span> <span data-ttu-id="7e40a-139">(Sie können jeweils nur eine ausgewählte Methode haben, die entweder *WHSScheduleWorkCreationWaveStepMethod* oder *createWork* verwendet, sodass die vorhandene Zeile mit **Methodenname** *createWork* automatisch in das Raster **Verbleibende Methoden** verschoben wird.)</span><span class="sxs-lookup"><span data-stu-id="7e40a-139">(You can only have one selected method at a time that uses either *WHSScheduleWorkCreationWaveStepMethod* or *createWork*, so the existing row with **Method name** *createWork* is automatically moved to the **Remaining methods** grid.)</span></span>

## <a name="set-wave-task-processing-threshold-data"></a><span data-ttu-id="7e40a-140">Festlegen der Schwellenwertdaten für die Verarbeitung von Wellenaufgaben</span><span class="sxs-lookup"><span data-stu-id="7e40a-140">Set wave task processing threshold data</span></span>

<span data-ttu-id="7e40a-141">Das System erstellt beim ersten Ausführen eines Wellenprozesses mit einer aufgabenbasierten Verarbeitung Standardschwellenwertdaten für die Verarbeitung von Wellenaufgaben.</span><span class="sxs-lookup"><span data-stu-id="7e40a-141">The system will create default wave task processing threshold data the first time a wave process runs using any task-based processing.</span></span> <span data-ttu-id="7e40a-142">Die Daten werden verwendet, um zu steuern, wann die Wellenverarbeitung asynchron ausgeführt wird und aufgabenbasiert ist, wodurch Arbeit parallel verarbeitet und erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7e40a-142">The data is used to control when wave processing will run asynchronously and be task-based, which enables it to process and create work in parallel.</span></span>

<span data-ttu-id="7e40a-143">Die Standarddaten verwenden zunächst einen Schwellenwert von 15 für die Mindestanzahl von Ladungspositionen (MINIMUMWAVELOADLINES).</span><span class="sxs-lookup"><span data-stu-id="7e40a-143">The default data will initially use a threshold value of 15 for the minimum number of load lines (MINIMUMWAVELOADLINES).</span></span> <span data-ttu-id="7e40a-144">Dies bedeutet, dass das System bei der Verarbeitung einer Welle mit mehr als 15 Ladungspositionen die asynchrone Aufgabenverarbeitung verwendet.</span><span class="sxs-lookup"><span data-stu-id="7e40a-144">This means that when the system processes a wave with more than 15 loads lines, it will use asynchronous task processing.</span></span> <span data-ttu-id="7e40a-145">Sie können diese Daten manuell in die Tabelle **WHSWaveTaskProcessingThresholdParameters** in Ihren Testumgebungen einfügen oder dort aktualisieren. Wenn Sie diese Einstellung jedoch in einer Produktionsumgebung ändern müssen, müssen Sie sich an den Microsoft-Support wenden, um die Aktualisierung anzufordern.</span><span class="sxs-lookup"><span data-stu-id="7e40a-145">You can manually insert/update this data in the **WHSWaveTaskProcessingThresholdParameters** table in your test environments, but if you need to change this setting in a production environment, you must contact Microsoft Support to request the update.</span></span>

## <a name="work-with-the-feature"></a><span data-ttu-id="7e40a-146">Arbeiten mit der Funktion</span><span class="sxs-lookup"><span data-stu-id="7e40a-146">Work with the feature</span></span>

<span data-ttu-id="7e40a-147">Wenn die Funktion *Arbeitserstellung planen* aktiviert ist, erstellt die Wellenverarbeitung geplante Arbeiten, die schließlich vom neuen Arbeitserstellungsprozess verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e40a-147">When the *Schedule work creation* functionality is enabled, wave processing will create planned work, which will eventually be used by the new work creation process.</span></span> <span data-ttu-id="7e40a-148">Während der Arbeitserstellung wird die Arbeit mit der Funktion *Organisationsweite Arbeitssperre* gesperrt.</span><span class="sxs-lookup"><span data-stu-id="7e40a-148">During work creation, the work will be blocked using the *Organization-wide work blocking* feature.</span></span>

<span data-ttu-id="7e40a-149">Das folgende Flussdiagramm zeigt, wie geplante Arbeiten während der Wellenverarbeitung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7e40a-149">The following flowchart shows how planned work is created during wave processing.</span></span>

![Arbeitserstellung planen](media/schedule-work-creation-process.png)

### <a name="planned-work"></a><span data-ttu-id="7e40a-151">Geplante Arbeit</span><span class="sxs-lookup"><span data-stu-id="7e40a-151">Planned work</span></span>

<span data-ttu-id="7e40a-152">Die Seite **Details der geplanten Arbeit** (**Lagerort verwaltung \> Arbeit \> Details der geplanten Arbeit**) zeigt Informationen über die geplante Arbeit an, die anfänglich während der Wellenverarbeitung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7e40a-152">The **Planned work details** page (**Warehouse management \> Work \> Planned work details**) shows information about the planned work, which is initially created during wave processing.</span></span> <span data-ttu-id="7e40a-153">Die folgenden **Prozessstatus**-Werte sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="7e40a-153">The following **Process status** values are available:</span></span>

- <span data-ttu-id="7e40a-154">**In Warteschlange** – Die geplante Arbeit wartet darauf, zur Erstellung von Arbeit verwendet zu werden.</span><span class="sxs-lookup"><span data-stu-id="7e40a-154">**Queued** - The planned work is waiting to be used to create work.</span></span>
- <span data-ttu-id="7e40a-155">**Abgeschlossen** – Die geplante Arbeit wurde verwendet, um Arbeit zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7e40a-155">**Completed** - The planned work has been used to create work.</span></span>
- <span data-ttu-id="7e40a-156">**Fehlgeschlagen** – Die Wellenverarbeitung ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="7e40a-156">**Failed** – The wave processing has failed.</span></span> <span data-ttu-id="7e40a-157">Beachten Sie, dass die geplante Arbeit mit oder ohne zugehörige tatsächliche Arbeit in einem Status **Fehlgeschlagen** sein kann.</span><span class="sxs-lookup"><span data-stu-id="7e40a-157">Note that the planned work can be in a **Failed** state with or without related actual work.</span></span> <span data-ttu-id="7e40a-158">Wenn der eigentliche Arbeitserstellungsprozess fehlschlägt, bleibt die eigentliche Arbeit im Status *Storniert*.</span><span class="sxs-lookup"><span data-stu-id="7e40a-158">When the actual work creation process fails, the actual work remains in status *Cancelled*.</span></span>

### <a name="batch-job-for-the-work-creation-process"></a><span data-ttu-id="7e40a-159">Stapelverarbeitungsauftrag für den Arbeitserstellungsprozess</span><span class="sxs-lookup"><span data-stu-id="7e40a-159">Batch job for the work creation process</span></span>

<span data-ttu-id="7e40a-160">Um die Stapelverarbeitungsaufträge für die Verarbeitung von Wellen anzuzeigen, wählen Sie **Stapelverarbeitungsaufträge** im Aktionsbereich auf der Seite **Alle Wellen** aus.</span><span class="sxs-lookup"><span data-stu-id="7e40a-160">To view the batch jobs for processing waves, select **Batch jobs** on the Action Pane on the **All waves** page.</span></span>

<span data-ttu-id="7e40a-161">Von hier aus können Sie alle Details der Stapelverarbeitungsaufgabe für jede der Stapelverarbeitungsauftrags-IDs anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7e40a-161">From here, you can view all the batch task details for each of the batch job IDs.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]