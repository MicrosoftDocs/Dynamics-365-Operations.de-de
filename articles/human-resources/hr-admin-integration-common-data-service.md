---
title: Common Data Service-Integration konfigurieren
description: Sie können die Integration zwischen Common Data Service und einer Instanz von Microsoft Dynamics 365 Human Resources aktivieren und deaktivieren. Sie können auch die Synchronisierungsdetails anzeigen, Nachverfolgungsdaten löschen und eine Entität erneut synchronisieren, um Datenprobleme zwischen den beiden Umgebungen zu beheben.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 042daf3fdf7a906086af726472da050467d217e3
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009120"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="a225f-104">Common Data Service-Integration konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a225f-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="a225f-105">Sie können die Integration zwischen Common Data Service und einer Instanz von Microsoft Dynamics 365 Human Resources aktivieren und deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a225f-105">You can turn integration between Common Data Service and an instance of Microsoft Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="a225f-106">Sie können auch die Synchronisierungsdetails anzeigen, Nachverfolgungsdaten löschen und eine Entität erneut synchronisieren, um Datenprobleme zwischen den beiden Umgebungen zu beheben.</span><span class="sxs-lookup"><span data-stu-id="a225f-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="a225f-107">Wenn Sie die Integration deaktivieren, können Benutzer Änderungen in Human Resources oder Common Data Service vornehmen, diese Änderungen werden jedoch nicht zwischen den beiden Umgebungen synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="a225f-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="a225f-108">Standardmäßig ist die Integration zwischen Human Resources und Common Data Service entweder aktiviert oder deaktiviert, dies hängt vom Vorhandensein von Demo-Daten in den Umgebungen ab.</span><span class="sxs-lookup"><span data-stu-id="a225f-108">By default, integration between Human Resources and Common Data Service is turned either off or on, depending on the presence of demo data in the environments:</span></span>

- <span data-ttu-id="a225f-109">**Aus** bei neuen Umgebungen ohne Demo-Daten</span><span class="sxs-lookup"><span data-stu-id="a225f-109">**Off** for new environments that don't include demo data</span></span>
- <span data-ttu-id="a225f-110">**Ein** bei neuen Umgebungen mit Demo-Daten</span><span class="sxs-lookup"><span data-stu-id="a225f-110">**On** for new environments that include demo data</span></span>

<span data-ttu-id="a225f-111">Neue Umgebungen, die Demodaten enthalten, beginnen mit der Synchronisierung der Daten, wenn diese bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a225f-111">New environments that include demo data will start to sync data when they are provisioned.</span></span>

<span data-ttu-id="a225f-112">Möglicherweise möchten Sie die Integration in den folgenden Situationen deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="a225f-112">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="a225f-113">Sie geben Daten über das Data Management Framework ein und müssen die Daten mehrmals importieren, um sie in einen korrekten Zustand zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="a225f-113">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="a225f-114">Es gibt Probleme mit Daten in Human Resources oder Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a225f-114">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="a225f-115">Wenn Sie die Integration deaktivieren, können Sie einen Datensatz in einer Umgebung löschen, ohne ihn in der anderen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="a225f-115">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="a225f-116">Wenn Sie die Integration wieder aktivieren, wird der Datensatz in der Umgebung, in der er nicht gelöscht wurde, wieder mit der Umgebung synchronisiert, in der er gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="a225f-116">When you turn integration back on, the record in the environment where it wasn't deleted will be synced back to the environment where it was deleted.</span></span> <span data-ttu-id="a225f-117">Die Synchronisierung beginnt erneut, wenn die **Common Data Service-Integration angeforderte Ausführungen von Batchaufträgen verpasst hat**.</span><span class="sxs-lookup"><span data-stu-id="a225f-117">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="a225f-118">Stellen Sie beim Deaktivieren der Datenintegration sicher, dass Sie nicht denselben Datensatz in beiden Umgebungen bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="a225f-118">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="a225f-119">Wenn Sie die Integration wieder aktivieren, wird der zuletzt bearbeitete Datensatz synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="a225f-119">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="a225f-120">Wenn Sie in beiden Umgebungen nicht dieselben Änderungen am Datensatz vorgenommen haben, kann dies zu Datenverlusten führen.</span><span class="sxs-lookup"><span data-stu-id="a225f-120">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="a225f-121">Zugreifen auf die Common Data Service-Integrationsseite</span><span class="sxs-lookup"><span data-stu-id="a225f-121">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="a225f-122">In der Human Resources-Instanz, in der Sie Einstellungen für die Integration mit Common Data Service anzeigen oder konfigurieren möchten, wählen Sie die Kachel **Systemverwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="a225f-122">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="a225f-123">[![Systemverwaltung-Kachel](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="a225f-123">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="a225f-124">Wählen Sie die Registerkarte **Links**.</span><span class="sxs-lookup"><span data-stu-id="a225f-124">Select the **Links** tab.</span></span>

    <span data-ttu-id="a225f-125">[![Registerkarte „Links“](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="a225f-125">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="a225f-126">Wählen Sie unter **Integrationen** **Common Data Service-Konfiguration** aus.</span><span class="sxs-lookup"><span data-stu-id="a225f-126">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="a225f-127">[![Common Data Service-Konfigurationslink](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="a225f-127">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="a225f-128">Aktivieren oder Deaktivieren der Integration zwischen Human Resources und Common Data Service</span><span class="sxs-lookup"><span data-stu-id="a225f-128">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="a225f-129">Um die Integration zu aktivieren, setzen Sie die Option für **Aktivieren der Integration in Common Data Service** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a225f-129">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a225f-130">Wenn Sie die Integration aktivieren, werden die Daten das nächsten Mal synchronisiert, wenn die **Common Data Service-Integration angeforderte Ausführungen von Batchaufträgen verpasst hat**.</span><span class="sxs-lookup"><span data-stu-id="a225f-130">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="a225f-131">Alle Daten sollten nach Abschluss des Batchauftrags verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="a225f-131">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="a225f-132">Um die Integration zu deaktivieren, setzen Sie die Option auf **Nein**.</span><span class="sxs-lookup"><span data-stu-id="a225f-132">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="a225f-133">[![Aktivieren/Deaktivieren der Common Data Service-Integration](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="a225f-133">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="a225f-134">Datenintegrationsdetails anzeigen</span><span class="sxs-lookup"><span data-stu-id="a225f-134">View data integration details</span></span>

<span data-ttu-id="a225f-135">Auf dem Inforegister **Verwaltung** der Seite **Common Data Service-Integration** können Sie sehen, wie Datensätze zwischen Human Resources und Common Data Service verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="a225f-135">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="a225f-136">Um die Datensätze für eine Entität anzuzeigen, wählen Sie die Entität im Feld **CDS-Entitätsname** aus.</span><span class="sxs-lookup"><span data-stu-id="a225f-136">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="a225f-137">Das Raster zeigt alle Datensätze an, die mit der ausgewählten Entität verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="a225f-137">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="a225f-138">[![Anzeigen der Datensätze für eine Entität](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="a225f-138">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="a225f-139">Nicht alle Common Data Service-Unternehmen sind derzeit aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a225f-139">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="a225f-140">Im Raster werden nur Entitäten angezeigt, die die Verwendung benutzerdefinierter Felder unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a225f-140">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="a225f-141">Durch fortlaufende Releases von Human Resources werden neue Entitäten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a225f-141">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="a225f-142">Das Raster enthält die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="a225f-142">The grid includes the following fields:</span></span>

- <span data-ttu-id="a225f-143">**CDS-Entitätsname** – Der Name der Entität in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a225f-143">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="a225f-144">**CDS-Entitätsreferenz** – Die Kennung, die Common Data Service verwendet, um einen Datensatz zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a225f-144">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="a225f-145">Dieser Wert entspricht einem **RecId**-Wert von Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a225f-145">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="a225f-146">Die Kennung finden Sie beim Öffnen der Common Data Service-Einheit in Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="a225f-146">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="a225f-147">**Name der Human Resources-Entität** – Die Entität, die zuletzt Daten mit dem Common Data Service synchronisiert hat.</span><span class="sxs-lookup"><span data-stu-id="a225f-147">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="a225f-148">Die Entität kann entweder das Common Data Service-Präfix oder ein anderes Präfix haben.</span><span class="sxs-lookup"><span data-stu-id="a225f-148">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="a225f-149">**Human Resources-Referenz** – Der **RecId**-Wert, der mit dem Datensatz in Human Resources verknüpft wird.</span><span class="sxs-lookup"><span data-stu-id="a225f-149">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="a225f-150">**Wurde aus CDS gelöscht** – Ein Wert, der angibt, ob der Datensatz aus Common Data Service gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="a225f-150">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="a225f-151">Entfernen der Zuordnung eines Datensatzes in Human Resources aus Common Data Service</span><span class="sxs-lookup"><span data-stu-id="a225f-151">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="a225f-152">Wenn bei der Datensynchronisierung zwischen Human Resources und Common Data Service Probleme auftreten, können Sie diese möglicherweise beheben, indem Sie die Nachverfolgung löschen und die Nachverfolgungstabelle erneut synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="a225f-152">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="a225f-153">Wenn Sie die Zuordnung entfernen und dann einen Datensatz in Common Data Service ändern oder löschen, werden die Änderungen nicht mit Human Resources synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="a225f-153">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="a225f-154">Wenn Sie Änderungen in Human Resources vornehmen, wird ein neuer Nachverfolgungsdatensatz erstellt und der Datensatz in Common Data Service aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a225f-154">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="a225f-155">Zum Entfernen der Zuordnung eines Datensatzes zwischen Human Resources und Common Data Service wählen Sie die Entität im Feld **CDS-Entitätsname** aus und klicken dann auf die Option für **Nachverfolgungsinformationen löschen**.</span><span class="sxs-lookup"><span data-stu-id="a225f-155">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="a225f-156">[![Nachverfolgungsinformationen löschen](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="a225f-156">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="a225f-157">Informationen zum Ausführen einer vollständigen Synchronisierung für die Entität nach dem Löschen der Nachverfolgung finden Sie in der nächsten beschriebenen Prozedur.</span><span class="sxs-lookup"><span data-stu-id="a225f-157">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="a225f-158">Synchronisieren einer Entität zwischen Human Resources und Common Data Service</span><span class="sxs-lookup"><span data-stu-id="a225f-158">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="a225f-159">Verwenden Sie diese Prozedur, wenn Änderungen von Common Data Service zu lange dauern, um in Human Resources angezeigt zu werden, oder wenn Sie nach dem Löschen der Nachverfolgung die Nachverfolgungstabelle aktualisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="a225f-159">Use this procedure if changes from Common Data Service are taking too long to appear in Human Resources, or if you must refresh the tracking table after you clear the tracking.</span></span>

- <span data-ttu-id="a225f-160">Zum Ausführen einer vollständigen Synchronisierung für eine Entität zwischen Human Resources und Common Data Service wählen Sie die Entität im Feld **CDS-Entitätsname** aus und klicken dann auf **Jetzt synchronisieren**.</span><span class="sxs-lookup"><span data-stu-id="a225f-160">To run a full synchronization on an entity between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Sync now**.</span></span>

<span data-ttu-id="a225f-161">[![Ausführen einer vollständigen Synchronisierung](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="a225f-161">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


