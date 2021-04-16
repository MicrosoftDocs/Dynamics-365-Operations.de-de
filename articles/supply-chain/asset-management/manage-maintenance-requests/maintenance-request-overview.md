---
title: Wartungsanfragen
description: Dieses Thema bietet einen Überblick über die Verwaltung von Wartungsanfragen in Asset Management.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: dceb179d0a17d8025d88c5945b9571de65c86449
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838609"
---
# <a name="maintenance-requests"></a><span data-ttu-id="3b4ca-103">Wartungsanfragen</span><span class="sxs-lookup"><span data-stu-id="3b4ca-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="3b4ca-104">Wartungsanfragen sind Hinweise oder Erklärungen, die erstellt werden, um einen Manager oder Planer zu informieren, dass für eine Anlage möglicherweise ein Wartungs- oder Reparaturauftrag erforderlich ist, ohne dass jedoch ein Arbeitsauftrag erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3b4ca-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="3b4ca-105">Wenn den Inhalt einer Wartungsanfrage als gültig betrachtet wird, kann ein Arbeitsauftrag auf Basis der Wartungsanfrage erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3b4ca-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="3b4ca-106">Wartungsanfragen können für jede Anlage in Asset Management erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3b4ca-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="3b4ca-107">Unterschiedliche Arten von Wartungsanfragen können erstellt werden, je nachdem, wie das Unternehmen Wartungsanfragen verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b4ca-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="3b4ca-108">Nachfolgend finden Sie einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="3b4ca-108">Here are some examples:</span></span>

- <span data-ttu-id="3b4ca-109">Wartungsanfragen</span><span class="sxs-lookup"><span data-stu-id="3b4ca-109">Maintenance requests</span></span>
- <span data-ttu-id="3b4ca-110">Notizen</span><span class="sxs-lookup"><span data-stu-id="3b4ca-110">Notes</span></span>
- <span data-ttu-id="3b4ca-111">Korrekturen oder Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="3b4ca-111">Corrections or enhancements</span></span>
- <span data-ttu-id="3b4ca-112">Investitionen</span><span class="sxs-lookup"><span data-stu-id="3b4ca-112">Investments</span></span>
- <span data-ttu-id="3b4ca-113">Depotreparatur (Dieser Typ wird verwendet, wenn Sie Anlagen von einem anderen Standort erhalten, damit Sie einen Wartungs- oder Reparaturauftrag erledigen können. Anschließend geben Sie die Anlage zurück.)</span><span class="sxs-lookup"><span data-stu-id="3b4ca-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="3b4ca-114">Wartungsanfragen anzeigen</span><span class="sxs-lookup"><span data-stu-id="3b4ca-114">View maintenance requests</span></span>

<span data-ttu-id="3b4ca-115">Um Wartungsanfragen anzuzeigen, wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Wartungsanfragen** \> **Alle Wartungsanfragen**, **Aktive Wartungsanfragen** oder **Meine Wartungsanfragen für funktionale Standorte** aus.</span><span class="sxs-lookup"><span data-stu-id="3b4ca-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="3b4ca-116">Jede Listenseite zeigt einige der Informationen an, die sich auf eine Wartungsanfrage bezieht.</span><span class="sxs-lookup"><span data-stu-id="3b4ca-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![Wartungsanfragen anzeigen](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="3b4ca-118">Verwenden Sie die Listenseite **Meine Wartungsanfragen für funktionale Standorte**, um eine Liste der Wartungsanfragen anzuzeigen, die entweder funktionalen Standorte enthalten, denen Sie als Arbeitskraft zugeordnet sind, oder Anlagen, die an funktionalen Standorten eingerichtet sind, denen Sie als Arbeitskraft zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3b4ca-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="3b4ca-119">(Informationen darüber, wie Sie funktionale Standorte für Wartungsarbeiter einrichten, finden Sie unter [Wartungsarbeiter und Arbeitskräftegruppen](../setup-for-objects/workers-and-worker-groups.md).)</span><span class="sxs-lookup"><span data-stu-id="3b4ca-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="3b4ca-120">Obwohl Informationen zu Kundenkonten in Asset Service Management (externe Wartung) verfügbar sind, sind diese nicht in Asset Management verfügbar (interne Wartung).</span><span class="sxs-lookup"><span data-stu-id="3b4ca-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="3b4ca-121">Um die Detailansicht eines Datensatzes zu öffnen, wählen Sie auf der Listenseite **Alle Wartungsanfragen** in der Rasteransicht eine Verknüpfung in der Spalte **Wartungsanfrage** aus.</span><span class="sxs-lookup"><span data-stu-id="3b4ca-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![Details der Wartungsanfrage anzeigen](media/02-manage-maintenance-requests.png)

<span data-ttu-id="3b4ca-123">Die Schaltflächen im Aktivitätsbereich sind auf Registerkarten zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="3b4ca-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="3b4ca-124">Die folgende Tabelle beschreibt kurz die Schaltflächen, die sich auf Anlagenmanagement beziehen.</span><span class="sxs-lookup"><span data-stu-id="3b4ca-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="3b4ca-125">Name der Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="3b4ca-125">Button name</span></span>                      | <span data-ttu-id="3b4ca-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b4ca-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="3b4ca-127">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="3b4ca-127">Edit</span></span>                             | <span data-ttu-id="3b4ca-128">Dient zum Bearbeiten der ausgewählten Wartungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="3b4ca-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="3b4ca-129">Neue</span><span class="sxs-lookup"><span data-stu-id="3b4ca-129">New</span></span>                              | <span data-ttu-id="3b4ca-130">Erstellt eine neue Wartungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="3b4ca-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="3b4ca-131">Löschen</span><span class="sxs-lookup"><span data-stu-id="3b4ca-131">Delete</span></span>                           | <span data-ttu-id="3b4ca-132">Löscht die ausgewählte Wartungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="3b4ca-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="3b4ca-133">Arbeitsauftragspool</span><span class="sxs-lookup"><span data-stu-id="3b4ca-133">Work order pool</span></span>                  | <span data-ttu-id="3b4ca-134">Verbindet die ausgewählte Wartungsanfrage mit einem Arbeitsauftragspool.</span><span class="sxs-lookup"><span data-stu-id="3b4ca-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="3b4ca-135">Arbeitsauftrag</span><span class="sxs-lookup"><span data-stu-id="3b4ca-135">Work order</span></span>                       | <span data-ttu-id="3b4ca-136">Erstellt einen Arbeitsauftrag basierend auf der ausgewählten Wartungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="3b4ca-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="3b4ca-137">Anlagenfehler</span><span class="sxs-lookup"><span data-stu-id="3b4ca-137">Asset fault</span></span>                      | <span data-ttu-id="3b4ca-138">Klicken Sie auf **Anlagenfehler**, wo Sie eine Fehlererfassung für die ausgewählte Wartungsanfrage erstellen können.</span><span class="sxs-lookup"><span data-stu-id="3b4ca-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="3b4ca-139">Arbeitsaufträge</span><span class="sxs-lookup"><span data-stu-id="3b4ca-139">Work orders</span></span>                      | <span data-ttu-id="3b4ca-140">Hier wird eine Liste aller Arbeitsaufträge angezeigt, die mit der ausgewählten Wartungsanfrage verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="3b4ca-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="3b4ca-141">Wartungsanfragenstatus aktualisieren</span><span class="sxs-lookup"><span data-stu-id="3b4ca-141">Update maintenance request state</span></span> | <span data-ttu-id="3b4ca-142">Aktualisiert den Status der Wartungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="3b4ca-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="3b4ca-143">Lebenszyklusstatusprotokoll</span><span class="sxs-lookup"><span data-stu-id="3b4ca-143">Lifecycle state log</span></span>              | <span data-ttu-id="3b4ca-144">Hiermit wird ein Protokoll angezeigt, das den Lebenszyklusstatus der ausgewählten Wartungsanfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="3b4ca-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="3b4ca-145">Wartungsanfragedetails</span><span class="sxs-lookup"><span data-stu-id="3b4ca-145">Maintenance request details</span></span>      | <span data-ttu-id="3b4ca-146">Dient zum Drucken eines Berichts, der Details der ausgewählten Wartungsanfrage anzeigt.</span><span class="sxs-lookup"><span data-stu-id="3b4ca-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="3b4ca-147">Anlagenausleihe senden</span><span class="sxs-lookup"><span data-stu-id="3b4ca-147">Send loan asset</span></span>                  | <span data-ttu-id="3b4ca-148">Wählen Sie eine Anlagenausleihe aus, die als temporäre Ersetzung der Anlage dienen soll, die in der ausgewählten Wartungsanfrage ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="3b4ca-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="3b4ca-149">Anlagenausleiche zurückgeben</span><span class="sxs-lookup"><span data-stu-id="3b4ca-149">Return loan asset</span></span>                | <span data-ttu-id="3b4ca-150">Erfassen Sie die Anlagenausleihe als zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3b4ca-150">Register the loan asset as returned.</span></span> |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]