---
title: Besitz des Lagerbestands auf Grundlage des Produktionsbedarfs ändern
description: Dieses Verfahren zeigt, wie Sie den Eigentümer des Lieferungsbestandes vom Kreditor auf Ihre juristische Person ändern, wenn ein Bedarf für den Bestand in der Produktion vorhanden ist.
author: perlynne
manager: tfehr
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c50affa05b8df53d31660854f4d1ead6aeff820
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204239"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="84c57-103">Besitz des Lagerbestands auf Grundlage des Produktionsbedarfs ändern</span><span class="sxs-lookup"><span data-stu-id="84c57-103">Change the ownership of consignment inventory based on production demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="84c57-104">Dieses Verfahren zeigt, wie Sie den Eigentümer des Lieferungsbestandes vom Kreditor auf Ihre juristische Person ändern, wenn ein Bedarf für den Bestand in der Produktion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="84c57-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="84c57-105">Diese Besitzänderung wird ausgeführt, indem eine Bestandsbesitz-Änderungserfassung erstellt und gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="84c57-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="84c57-106">Die Besitzänderungs-Erfassungspositionen kann manuell erstellt werden, oder, wie in dieser Aufzeichnung, basierend auf einem vorhandenen Produktionsbedarf durchgeführt werden</span><span class="sxs-lookup"><span data-stu-id="84c57-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="84c57-107">Normalerweise wird diese Aufgabe von einem Fertigungsbereichsvorgesetzten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="84c57-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="84c57-108">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="84c57-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="84c57-109">Wenn Sie Ihren eigenen Daten nutzen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind: es wurden ein Lagererfassungsname für die Bestandsbesitzänderung, physisch erfasste verfügbare Artikel im Besitz des Kreditors und mindestens eine Produktionsauftragsposition für Rohstoff eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="84c57-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="84c57-110">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="84c57-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

> [!NOTE]
> <span data-ttu-id="84c57-111">Ausgehende Lieferungsprozesse werden standardmäßig nicht unterstützt und die automatische Besitzerfassungsverarbeitung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="84c57-111">Outbound consignment processes are not supported out-of-the-box and automatic ownership journal processing is not supported.</span></span>

## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="84c57-112">Erstellen einer Bestandsbesitz-Erfassung</span><span class="sxs-lookup"><span data-stu-id="84c57-112">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="84c57-113">Wechseln Sie zu "Lagerverwaltung" > "Journaleinträge" > "Artikel" > "Bestandseigentümeränderung".</span><span class="sxs-lookup"><span data-stu-id="84c57-113">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="84c57-114">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="84c57-114">Click New.</span></span>
    * <span data-ttu-id="84c57-115">Die Bestandseigentümer-Journaländerung wird verwendet, um den Eigentümer des Lieferungsbestandes vom Kreditor auf die aktuelle juristische Person zu ändern.</span><span class="sxs-lookup"><span data-stu-id="84c57-115">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="84c57-116">Diese Besitzänderung wird über die Freigabe des verfügbaren Lagerbestands im Besitz des Kreditors und den Empfang des Bestands in der aktuellen juristischen Person durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="84c57-116">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="84c57-117">Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="84c57-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="84c57-118">Sie können nur Lagerjournalnamen auswählen, die einen Erfassungstyp "Besitzänderung" haben.</span><span class="sxs-lookup"><span data-stu-id="84c57-118">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="84c57-119">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="84c57-119">Click OK.</span></span>
5. <span data-ttu-id="84c57-120">Klicken Sie auf Funktionen.</span><span class="sxs-lookup"><span data-stu-id="84c57-120">Click Functions.</span></span>
6. <span data-ttu-id="84c57-121">Klicken Sie auf "Erfassungspositionen aus Produktionsaufträgen erstellen".</span><span class="sxs-lookup"><span data-stu-id="84c57-121">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="84c57-122">Sie können den Eigentumsübertragungsprozess starten, indem Sie alle Produktionsauftragspositionen abfragen, die ggf. einen Verbrauch des Rohmaterials haben.</span><span class="sxs-lookup"><span data-stu-id="84c57-122">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="84c57-123">In den Lagerabgangstatus wählen Sie eine Option, um das Feld einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="84c57-123">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="84c57-124">Mit dieser Option können Sie nach dem Abgangsstatus von Lagerbuchungen filtern.</span><span class="sxs-lookup"><span data-stu-id="84c57-124">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="84c57-125">Beispielsweise können Sie Erfassungspositionen für Bestand erstellen, der den Status "Entnommen" und "Physisch reserviert" hat.</span><span class="sxs-lookup"><span data-stu-id="84c57-125">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="84c57-126">Erweitern Sie den Abschnitt "Einzuschließende Datensätze".</span><span class="sxs-lookup"><span data-stu-id="84c57-126">Expand the Records to include section.</span></span>
    * <span data-ttu-id="84c57-127">In diesem Abschnitt können Sie zusätzliche Filter anwenden.</span><span class="sxs-lookup"><span data-stu-id="84c57-127">This section lets you apply additional filtering.</span></span> <span data-ttu-id="84c57-128">So können z. B. ein bestimmtes Rohmaterialdatum auswählen.</span><span class="sxs-lookup"><span data-stu-id="84c57-128">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="84c57-129">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="84c57-129">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="84c57-130">Buchen der Bestandseigentümer-Journaländerung</span><span class="sxs-lookup"><span data-stu-id="84c57-130">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="84c57-131">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="84c57-131">Click Post.</span></span>
    * <span data-ttu-id="84c57-132">Wenn die Erfassung gebucht ist, wird der Bestand im Besitz des Kreditors über eine "Besitzänderungs"-Referenz freigegeben.</span><span class="sxs-lookup"><span data-stu-id="84c57-132">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="84c57-133">Anschließend wird der Bestand über eine Lagerbuchung als verfügbar empfangen, die mit einem Produktzugang für Bestellung aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="84c57-133">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="84c57-134">Beachten Sie, dass nur Buchungen, die der gebuchten Erfassung zugeordnet sind, erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="84c57-134">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="84c57-135">Es werden keine voraussichtlichen Lagerbuchung erstellt.</span><span class="sxs-lookup"><span data-stu-id="84c57-135">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="84c57-136">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="84c57-136">Click OK.</span></span>
3. <span data-ttu-id="84c57-137">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="84c57-137">Close the page.</span></span>

