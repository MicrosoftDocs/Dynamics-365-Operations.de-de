---
title: "Besitz des Lagerbestands auf Grundlage des Produktionsbedarfs ändern"
description: "Dieses Verfahren zeigt, wie Sie den Eigentümer des Lieferungsbestandes vom Kreditor auf Ihre juristische Person ändern, wenn ein Bedarf für den Bestand in der Produktion vorhanden ist."
author: perlynne
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: f02e37a21e2417d46c5ad990e165c2eff5a70811
ms.contentlocale: de-de
ms.lasthandoff: 01/17/2018

---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="292b7-103">Besitz des Lagerbestands auf Grundlage des Produktionsbedarfs ändern</span><span class="sxs-lookup"><span data-stu-id="292b7-103">Change the ownership of consignment inventory based on production demand</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="292b7-104">Dieses Verfahren zeigt, wie Sie den Eigentümer des Lieferungsbestandes vom Kreditor auf Ihre juristische Person ändern, wenn ein Bedarf für den Bestand in der Produktion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="292b7-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="292b7-105">Diese Besitzänderung wird ausgeführt, indem eine Bestandsbesitz-Änderungserfassung erstellt und gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="292b7-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="292b7-106">Die Besitzänderungs-Erfassungspositionen kann manuell erstellt werden, oder, wie in dieser Aufzeichnung, basierend auf einem vorhandenen Produktionsbedarf durchgeführt werden</span><span class="sxs-lookup"><span data-stu-id="292b7-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="292b7-107">Normalerweise wird diese Aufgabe von einem Fertigungsbereichsvorgesetzten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="292b7-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="292b7-108">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="292b7-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="292b7-109">Wenn Sie Ihren eigenen Daten nutzen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind: es wurden ein Lagererfassungsname für die Bestandsbesitzänderung, physisch erfasste verfügbare Artikel im Besitz des Kreditors und mindestens eine Produktionsauftragsposition für Rohstoff eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="292b7-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="292b7-110">Diese Prozedur ist für eine Funktion gedacht, die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="292b7-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="292b7-111">Erstellen einer Bestandsbesitz-Erfassung</span><span class="sxs-lookup"><span data-stu-id="292b7-111">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="292b7-112">Wechseln Sie zu "Lagerverwaltung" > "Journaleinträge" > "Artikel" > "Bestandseigentümeränderung".</span><span class="sxs-lookup"><span data-stu-id="292b7-112">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="292b7-113">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="292b7-113">Click New.</span></span>
    * <span data-ttu-id="292b7-114">Die Bestandseigentümer-Journaländerung wird verwendet, um den Eigentümer des Lieferungsbestandes vom Kreditor auf die aktuelle juristische Person zu ändern.</span><span class="sxs-lookup"><span data-stu-id="292b7-114">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="292b7-115">Diese Besitzänderung wird über die Freigabe des verfügbaren Lagerbestands im Besitz des Kreditors und den Empfang des Bestands in der aktuellen juristischen Person durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="292b7-115">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="292b7-116">Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="292b7-116">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="292b7-117">Sie können nur Lagerjournalnamen auswählen, die einen Erfassungstyp "Besitzänderung" haben.</span><span class="sxs-lookup"><span data-stu-id="292b7-117">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="292b7-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="292b7-118">Click OK.</span></span>
5. <span data-ttu-id="292b7-119">Klicken Sie auf Funktionen.</span><span class="sxs-lookup"><span data-stu-id="292b7-119">Click Functions.</span></span>
6. <span data-ttu-id="292b7-120">Klicken Sie auf "Erfassungspositionen aus Produktionsaufträgen erstellen".</span><span class="sxs-lookup"><span data-stu-id="292b7-120">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="292b7-121">Sie können den Eigentumsübertragungsprozess starten, indem Sie alle Produktionsauftragspositionen abfragen, die ggf. einen Verbrauch des Rohmaterials haben.</span><span class="sxs-lookup"><span data-stu-id="292b7-121">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="292b7-122">In den Lagerabgangstatus wählen Sie eine Option, um das Feld einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="292b7-122">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="292b7-123">Mit dieser Option können Sie nach dem Abgangsstatus von Lagerbuchungen filtern.</span><span class="sxs-lookup"><span data-stu-id="292b7-123">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="292b7-124">Beispielsweise können Sie Erfassungspositionen für Bestand erstellen, der den Status "Entnommen" und "Physisch reserviert" hat.</span><span class="sxs-lookup"><span data-stu-id="292b7-124">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="292b7-125">Erweitern Sie den Abschnitt "Einzuschließende Datensätze".</span><span class="sxs-lookup"><span data-stu-id="292b7-125">Expand the Records to include section.</span></span>
    * <span data-ttu-id="292b7-126">In diesem Abschnitt können Sie zusätzliche Filter anwenden.</span><span class="sxs-lookup"><span data-stu-id="292b7-126">This section lets you apply additional filtering.</span></span> <span data-ttu-id="292b7-127">So können z. B. ein bestimmtes Rohmaterialdatum auswählen.</span><span class="sxs-lookup"><span data-stu-id="292b7-127">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="292b7-128">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="292b7-128">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="292b7-129">Buchen der Bestandseigentümer-Journaländerung</span><span class="sxs-lookup"><span data-stu-id="292b7-129">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="292b7-130">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="292b7-130">Click Post.</span></span>
    * <span data-ttu-id="292b7-131">Wenn die Erfassung gebucht ist, wird der Bestand im Besitz des Kreditors über eine "Besitzänderungs"-Referenz freigegeben.</span><span class="sxs-lookup"><span data-stu-id="292b7-131">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="292b7-132">Anschließend wird der Bestand über eine Lagerbuchung als verfügbar empfangen, die mit einem Produktzugang für Bestellung aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="292b7-132">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="292b7-133">Beachten Sie, dass nur Buchungen, die der gebuchten Erfassung zugeordnet sind, erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="292b7-133">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="292b7-134">Es werden keine voraussichtlichen Lagerbuchung erstellt.</span><span class="sxs-lookup"><span data-stu-id="292b7-134">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="292b7-135">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="292b7-135">Click OK.</span></span>
3. <span data-ttu-id="292b7-136">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="292b7-136">Close the page.</span></span>

