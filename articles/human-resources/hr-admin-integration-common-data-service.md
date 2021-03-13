---
title: Dataverse-Integration konfigurieren
description: Sie können die Integration zwischen Microsoft Dataverse und Dynamics 365 Human Resources aktivieren und deaktivieren. Sie können auch die Synchronisierungsdetails anzeigen, Nachverfolgungsdaten löschen und eine Tabelle erneut synchronisieren, um Datenprobleme zwischen den beiden Umgebungen zu beheben.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 38c42469e62bf5457d0281540325a6c56a5f930f
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112714"
---
# <a name="configure-dataverse-integration"></a><span data-ttu-id="6f7a2-104">Dataverse-Integration konfigurieren</span><span class="sxs-lookup"><span data-stu-id="6f7a2-104">Configure Dataverse integration</span></span>

<span data-ttu-id="6f7a2-105">Sie können die Integration zwischen Microsoft Dataverse und Dynamics 365 Human Resources aktivieren und deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-105">You can turn integration between Microsoft Dataverse and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="6f7a2-106">Sie können auch die Synchronisierungsdetails anzeigen, Nachverfolgungsdaten löschen und eine Tabelle erneut synchronisieren, um Datenprobleme zwischen den beiden Umgebungen zu beheben.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-106">You can also view the synchronization details, clear tracking data, and resync a table to help troubleshoot data issues between the two environments.</span></span>

> [!NOTE]
> <span data-ttu-id="6f7a2-107">Weitere Informationen zu Dataverse (früher Common Data Service) und Terminologie-Updates finden Sie unter [Was ist Microsoft Dataverse ?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="6f7a2-107">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="6f7a2-108">Wenn Sie die Integration deaktivieren, können Benutzer Änderungen in Human Resources oder Dataverse vornehmen, diese Änderungen werden jedoch nicht zwischen den beiden Umgebungen synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-108">When you turn off integration, users can make changes in Human Resources or Dataverse, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="6f7a2-109">Standardmäßig ist die Integration zwischen Human Resources und Dataverse deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-109">By default, integration between Human Resources and Dataverse is turned off.</span></span>

<span data-ttu-id="6f7a2-110">Möglicherweise möchten Sie die Integration in den folgenden Situationen deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="6f7a2-110">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="6f7a2-111">Sie geben Daten über das Data Management Framework ein und müssen die Daten mehrmals importieren, um sie in einen korrekten Zustand zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-111">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="6f7a2-112">Es gibt Probleme mit Daten in Human Resources oder Dataverse.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-112">There are issues with data in either Human Resources or Dataverse.</span></span> <span data-ttu-id="6f7a2-113">Wenn Sie die Integration deaktivieren, können Sie einen Datensatz in einer Umgebung löschen, ohne ihn in der anderen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-113">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="6f7a2-114">Wenn Sie die Integration wieder aktivieren, wird der Datensatz in der Umgebung, in der er nicht gelöscht wurde, wieder mit der Umgebung synchronisiert, in der er gelöscht worden ist.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-114">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="6f7a2-115">Die Synchronisierung beginnt erneut, wenn die **Dataverse-Integration angeforderte Ausführungen von Batchaufträgen verpasst hat**.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-115">Synchronization begins the next time the **Dataverse integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="6f7a2-116">Stellen Sie beim Deaktivieren der Datenintegration sicher, dass Sie nicht denselben Datensatz in beiden Umgebungen bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-116">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="6f7a2-117">Wenn Sie die Integration wieder aktivieren, wird der zuletzt bearbeitete Datensatz synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-117">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="6f7a2-118">Wenn Sie in beiden Umgebungen nicht dieselben Änderungen am Datensatz vorgenommen haben, kann dies zu Datenverlusten führen.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-118">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-dataverse-integration-page"></a><span data-ttu-id="6f7a2-119">Zugreifen auf die Dataverse-Integrationsseite</span><span class="sxs-lookup"><span data-stu-id="6f7a2-119">Access the Dataverse integration page</span></span>

1. <span data-ttu-id="6f7a2-120">In der Human Resources-Instanz, in der Sie Einstellungen für die Integration mit Dataverse anzeigen oder konfigurieren möchten, wählen Sie die Kachel **Systemverwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-120">In the Human Resources instance where you want to view or configure settings for the integration with Dataverse, select the **System administration** tile.</span></span>

    <span data-ttu-id="6f7a2-121">[![Systemverwaltung-Kachel](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="6f7a2-121">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="6f7a2-122">Wählen Sie die Registerkarte **Links**.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-122">Select the **Links** tab.</span></span>

    <span data-ttu-id="6f7a2-123">[![Registerkarte „Links“](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="6f7a2-123">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="6f7a2-124">Wählen Sie unter **Integrationen** **Dataverse-Konfiguration** aus.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-124">Under **Integrations**, select **Dataverse configuration**.</span></span>

    <span data-ttu-id="6f7a2-125">[![Dataverse-Konfigurationslink](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span><span class="sxs-lookup"><span data-stu-id="6f7a2-125">[![Dataverse configuration link](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a><span data-ttu-id="6f7a2-126">Aktivieren oder Deaktivieren der Integration zwischen Human Resources und Dataverse</span><span class="sxs-lookup"><span data-stu-id="6f7a2-126">Turn data integration between Human Resources and Dataverse on or off</span></span>

- <span data-ttu-id="6f7a2-127">Um die Integration zu aktivieren, setzen Sie die Option **Dataverse aktivieren** auf der Seite **Microsoft Dataverse-Integration** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-127">To turn on integration, set the **Enable Dataverse integration** option to **Yes** on the **Microsoft Dataverse integration** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f7a2-128">Wenn Sie die Integration aktivieren, werden die Daten das nächsten Mal synchronisiert, wenn die **Dataverse-Integration angeforderte Ausführungen von Batchaufträgen verpasst hat**.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-128">When you turn on integration, data will be synced the next time that the **Dataverse integration missed request sync** batch job runs.</span></span> <span data-ttu-id="6f7a2-129">Alle Daten sollten nach Abschluss des Batchauftrags verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-129">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="6f7a2-130">Um die Integration zu deaktivieren, setzen Sie die Option auf **Nein**.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-130">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="6f7a2-131">[![Aktivieren/Deaktivieren der Dataverse-Integration](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span><span class="sxs-lookup"><span data-stu-id="6f7a2-131">[![Turning the Dataverse integration on or off](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span></span>

> [!WARNING]
> <span data-ttu-id="6f7a2-132">Wir empfehlen dringend, die Dataverse Integration während Datenmigrationsaufgaben auszuschalten.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-132">We strongly recommend turning off Dataverse integration while performing data migration tasks.</span></span> <span data-ttu-id="6f7a2-133">Das Hochladen großer Datenmengen kann die Leistung erheblich beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-133">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="6f7a2-134">Das Hochladen von 2.000 Mitarbeitern kann beispielsweise mehrere Stunden dauern, wenn die Integration aktiviert ist, aber weniger als eine Stunde, wenn sie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-134">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="6f7a2-135">Die in diesem Beispiel angegebenen Zahlen dienen nur zu Demonstrationszwecken.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-135">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="6f7a2-136">Die genaue Zeit, die zum Importieren von Datensätzen benötigt wird, kann aufgrund vieler Faktoren stark variieren.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-136">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="6f7a2-137">Datenintegrationsdetails anzeigen</span><span class="sxs-lookup"><span data-stu-id="6f7a2-137">View data integration details</span></span>

<span data-ttu-id="6f7a2-138">Auf dem Inforegister **Verwaltung** der Seite **Microsoft Dataverse-Integration** können Sie sehen, wie Zeilen zwischen Human Resources und Dataverse verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-138">On the **Administration** FastTab of the **Microsoft Dataverse integration** page, you can see how rows are linked together between Human Resources and Dataverse.</span></span>

- <span data-ttu-id="6f7a2-139">Um die Zeilen für eine Tabelle anzuzeigen, wählen Sie die Tabelle im Feld **Dataverse-Tabelle**.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-139">To view the rows for a table, select the table in the **Dataverse table** field.</span></span> <span data-ttu-id="6f7a2-140">Das Raster zeigt alle Zeilen an, die mit der ausgewählten Tabelle verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-140">The grid shows all the rows that are linked to the selected table.</span></span>

> [!NOTE]
> <span data-ttu-id="6f7a2-141">Nicht alle Dataverse-Tabellen sind derzeit aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-141">Not all Dataverse tables are currently listed.</span></span> <span data-ttu-id="6f7a2-142">Im Raster werden nur Tabellen angezeigt, die die Verwendung benutzerdefinierter Felder unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-142">Only tables that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="6f7a2-143">Durch fortlaufende Releases von Human Resources werden neue Tabellen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-143">New tables become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="6f7a2-144">Das Raster enthält die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="6f7a2-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="6f7a2-145">**Dataverse-Tabelle** – Der Name der Tabelle in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-145">**Dataverse table** – The name of the table in Dataverse.</span></span>
- <span data-ttu-id="6f7a2-146">**Dataverse-Tabellenreferenz** – Der Bezeichner, den Dataverse verwendet, um einen Datensatz zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-146">**Dataverse table reference** – The identifier that Dataverse uses to identify a record.</span></span> <span data-ttu-id="6f7a2-147">Dieser Wert entspricht einem **RecId**-Wert von Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="6f7a2-148">Den Bezeichner finden Sie beim Öffnen der Dataverse-Tabelle in Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-148">You can find the identifier when you open the Dataverse table in Microsoft Excel.</span></span>
- <span data-ttu-id="6f7a2-149">**Name der Human Resources-Entität** – Die Human Resources-Entität, die zuletzt Daten mit dem Dataverse synchronisiert hat.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-149">**Human Resources entity name** – The Human Resources entity that last synced data to Dataverse.</span></span> <span data-ttu-id="6f7a2-150">Die Entität kann entweder das Dataverse-Präfix oder ein anderes Präfix haben.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-150">The entity can have either the Dataverse prefix or another prefix.</span></span>
- <span data-ttu-id="6f7a2-151">**Human Resources-Referenz** – Der **RecId**-Wert, der mit dem Datensatz in Human Resources verknüpft wird.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="6f7a2-152">**Aus Dataverse gelöscht** – Ein Wert, der angibt, ob die Zeile aus Dataverse gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-152">**Deleted from Dataverse** – A value that indicates whether the row was deleted from Dataverse.</span></span>

> [!NOTE]
> <span data-ttu-id="6f7a2-153">Datensätze in der Human Resources entsprechen den Zeilen in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-153">Records in Human Resources correspond to rows in Dataverse.</span></span>

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a><span data-ttu-id="6f7a2-154">Entfernen der Zuordnung eines Human Resources-Datensatzes aus einer Dataverse-Zeile</span><span class="sxs-lookup"><span data-stu-id="6f7a2-154">Remove the association of a Human Resources record from a Dataverse row</span></span>

<span data-ttu-id="6f7a2-155">Wenn bei der Datensynchronisierung zwischen Human Resources und Dataverse Probleme auftreten, können Sie diese möglicherweise beheben, indem Sie die Nachverfolgung löschen und die Nachverfolgungstabelle erneut synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-155">If you experience issues during data synchronization between Human Resources and Dataverse, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="6f7a2-156">Wenn Sie die Zuordnung entfernen und dann eine Zeile in Dataverse ändern oder löschen, werden die Änderungen nicht mit Human Resources synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-156">If you remove the association, and then change or delete a row in Dataverse, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="6f7a2-157">Wenn Sie Änderungen in Human Resources vornehmen, wird ein neuer Nachverfolgungsdatensatz erstellt und die Zeile in Dataverse aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-157">If you make changes in Human Resources, a new tracking record is created, and the row is updated in Dataverse.</span></span>

- <span data-ttu-id="6f7a2-158">Zum Entfernen der Zuordnung eines Human Resources-Datensatzes und einer Dataverse-Zeile wählen Sie die Tabelle im **Dataverse-Tabelle**-Feld aus und klicken dann auf die Option **Nachverfolgungsinformationen löschen**.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-158">To remove the association of a Human Resources record and a Dataverse row, select the table in the **Dataverse table** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="6f7a2-159">[![Nachverfolgungsinformationen löschen](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="6f7a2-159">[![Clearing tracking information](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span></span>

<span data-ttu-id="6f7a2-160">Informationen zum Ausführen einer vollständigen Synchronisierung für die Tabelle nach dem Löschen der Nachverfolgung finden Sie in der nächsten beschriebenen Prozedur.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-160">To run a full synchronization on the table after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-a-table-between-human-resources-and-dataverse"></a><span data-ttu-id="6f7a2-161">Synchronisieren einer Tabelle zwischen Human Resources und Dataverse</span><span class="sxs-lookup"><span data-stu-id="6f7a2-161">Sync a table between Human Resources and Dataverse</span></span>

<span data-ttu-id="6f7a2-162">Verwenden Sie dieses Verfahren, wenn:</span><span class="sxs-lookup"><span data-stu-id="6f7a2-162">Use this procedure when:</span></span>

- <span data-ttu-id="6f7a2-163">Änderungen von Dataverse dauern zu lange, um in der Personalabteilung zu erscheinen.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-163">Changes from Dataverse take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="6f7a2-164">Sie müssen die Tracking-Tabelle aktualisieren, nachdem Sie das Tracking gelöscht haben.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-164">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="6f7a2-165">So führen Sie eine vollständige Synchronisierung für eine Tabelle zwischen Human Resources und Dataverse ::</span><span class="sxs-lookup"><span data-stu-id="6f7a2-165">To run a full synchronization on a table between Human Resources and Dataverse:</span></span>

1. <span data-ttu-id="6f7a2-166">Wählen Sie im **Dataverse-Tabelle**-Feld die Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-166">Select the table in the **Dataverse table** field.</span></span>

2. <span data-ttu-id="6f7a2-167">Wählen **Jetzt synchronisieren**.</span><span class="sxs-lookup"><span data-stu-id="6f7a2-167">Select **Sync now**.</span></span>

<span data-ttu-id="6f7a2-168">[![Ausführen einer vollständigen Synchronisierung](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="6f7a2-168">[![Running a full synchronization](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="6f7a2-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f7a2-169">See also</span></span>

[<span data-ttu-id="6f7a2-170">Dataverse-Tabellen</span><span class="sxs-lookup"><span data-stu-id="6f7a2-170">Dataverse tables</span></span>](hr-developer-entities.md)<br>
[<span data-ttu-id="6f7a2-171">Virtuelle Dataverse-Tabellen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="6f7a2-171">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="6f7a2-172">FAQ zu virtuellen Tabellen für Human Resources</span><span class="sxs-lookup"><span data-stu-id="6f7a2-172">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="6f7a2-173">Was ist Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="6f7a2-173">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="6f7a2-174">Terminologie-Updates</span><span class="sxs-lookup"><span data-stu-id="6f7a2-174">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)
