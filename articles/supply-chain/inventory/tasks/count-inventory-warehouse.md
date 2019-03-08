---
title: Bestand an einem Lagerort zählen
description: Diese Prozedur führt Sie durch die einzelnen Schritte der Erstellung und des Buchens einer Lagerinventurerfassung, um einen bestimmten Artikel in einem Lagerplatz am Lagerort zu zählen.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c0bbfe8f86d27f81b0d577ed89dfa34ebcf3f18
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "353470"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="f9d86-103">Bestand an einem Lagerort zählen</span><span class="sxs-lookup"><span data-stu-id="f9d86-103">Count inventory in a warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f9d86-104">Diese Prozedur führt Sie durch die einzelnen Schritte der Erstellung und des Buchens einer Lagerinventurerfassung, um einen bestimmten Artikel in einem Lagerplatz am Lagerort zu zählen.</span><span class="sxs-lookup"><span data-stu-id="f9d86-104">This procedure walks you through the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="f9d86-105">Die Prozedur ist auf die Funktion "Grundlegendes Warehousing", die sich im Inventurverwaltungsmodul befindet, anwendbar. Jedoch nicht auf die Warehousing-Funktion, die im Lagerortverwaltungsmodul verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f9d86-105">The procedure applies to “basic warehousing” functionality, available in the Inventory management module, not to the warehousing functionality that’s available in the Warehouse management module.</span></span> <span data-ttu-id="f9d86-106">Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9d86-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="f9d86-107">Wenn Sie eigene Daten verwenden, sollten Sie sicherstellen, dass Sie Produkte und Lagerplatzeinstellung eingerichtet haben und dass Sie eine Lagererfassung für Inventurerfassungen erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="f9d86-107">If you’re using your own data, make sure that you have products and locations set up, and that you’ve created an inventory journal name for counting journals.</span></span> <span data-ttu-id="f9d86-108">Die Lagerinventur wird in der Regel von einem Lagerortmitarbeiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9d86-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="f9d86-109">Lagerinventurerfassung erstellen</span><span class="sxs-lookup"><span data-stu-id="f9d86-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="f9d86-110">Wechseln Sie zu "Lagerverwaltung" Wechseln Sie zu "Lagerverwaltung" > "Erfassungseinträge" > "Artikelinventur" > "Artikel"</span><span class="sxs-lookup"><span data-stu-id="f9d86-110">Go to Inventory management > Journal entries > Item counting > Counting.</span></span>
2. <span data-ttu-id="f9d86-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f9d86-111">Click New.</span></span>
3. <span data-ttu-id="f9d86-112">Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f9d86-112">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f9d86-113">Klicken Sie in der Liste auf die Lagerinventurerfassung, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="f9d86-113">In the list, click on the inventory counting journal name you want to use</span></span>
    * <span data-ttu-id="f9d86-114">Einige andere Felder werden basierend auf den Einstellungen der Lagerinventurerfassung ausgefüllt, die Sie auswählen.</span><span class="sxs-lookup"><span data-stu-id="f9d86-114">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
5. <span data-ttu-id="f9d86-115">Klicken Sie im Feld "Arbeitskraft" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f9d86-115">In the Worker field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f9d86-116">Wählen Sie in der Liste die Arbeitskraft aus, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="f9d86-116">In the list, select the worker you want to use.</span></span>
7. <span data-ttu-id="f9d86-117">Klicken Sie auf Auswählen.</span><span class="sxs-lookup"><span data-stu-id="f9d86-117">Click Select.</span></span>
8. <span data-ttu-id="f9d86-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f9d86-118">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="f9d86-119">Erfassungspositionen erstellen</span><span class="sxs-lookup"><span data-stu-id="f9d86-119">Create journal lines</span></span>
1. <span data-ttu-id="f9d86-120">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f9d86-120">Click New.</span></span>
2. <span data-ttu-id="f9d86-121">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f9d86-121">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="f9d86-122">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f9d86-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f9d86-123">Wenn Sie das Demodatenunternehmen USMF verwenden, geben Sie "A0001" ein.</span><span class="sxs-lookup"><span data-stu-id="f9d86-123">If you are using demo data company USMF, select 'A0001'.</span></span>  
4. <span data-ttu-id="f9d86-124">Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f9d86-124">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f9d86-125">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f9d86-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f9d86-126">Wenn Sie das Demodatenunternehmen USMF verwenden, geben Sie den Standort "2" ein.</span><span class="sxs-lookup"><span data-stu-id="f9d86-126">If you are using demo data company USMF, select site '2'.</span></span>  
6. <span data-ttu-id="f9d86-127">Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f9d86-127">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f9d86-128">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f9d86-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f9d86-129">Wenn Sie das Demodatenunternehmen USMF verwenden, geben Sie den Lagerort "24" ein.</span><span class="sxs-lookup"><span data-stu-id="f9d86-129">If you are using demo data company USMF, select warehouse '24'.</span></span>  
8. <span data-ttu-id="f9d86-130">Klicken Sie im Feld "Lagerplatz" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f9d86-130">In the Location field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="f9d86-131">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f9d86-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f9d86-132">Wenn Sie das Demodatenunternehmen USMF verwenden, geben Sie den Lagerplatz "BULK-001" ein.</span><span class="sxs-lookup"><span data-stu-id="f9d86-132">If you are using demo data company USMF, select location 'BULK-001'</span></span>  
10. <span data-ttu-id="f9d86-133">Geben Sie im Feld "Gezählt" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f9d86-133">In the Counted field, enter a number.</span></span>
    * <span data-ttu-id="f9d86-134">Wenn Sie eine Anzahl eingeben, die von der Zahl im Feld "Am Lager" angezeigt wird, wird das Mengenfeld aktualisiert, um die Abweichung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f9d86-134">If you enter a counted number that’s different to the number shown in the On-hand field, the Quantity field is updated to show the discrepancy.</span></span>  
11. <span data-ttu-id="f9d86-135">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f9d86-135">Click Save.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="f9d86-136">Lagerinventurerfassung buchen</span><span class="sxs-lookup"><span data-stu-id="f9d86-136">Post the inventory counting journal</span></span>
1. <span data-ttu-id="f9d86-137">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="f9d86-137">Click Post.</span></span>
    * <span data-ttu-id="f9d86-138">Wenn Sie eine Lagerinventurerfassung buchen und der gezählte Betrag unterscheidet sich vom Betrag, der im Feld "Am Lager" gemeldet ist, wird ein Lagerzugang oder Abgang gebucht, der Lagerbestand und der Lagerwert werden geändert, und Sachkontobuchungen werden generiert.</span><span class="sxs-lookup"><span data-stu-id="f9d86-138">When you post an inventory counting journal, if the counted amount differs from amount that’s reported in the On-hand field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
2. <span data-ttu-id="f9d86-139">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f9d86-139">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="f9d86-140">Lagerbuchungen anzeigen</span><span class="sxs-lookup"><span data-stu-id="f9d86-140">View inventory transactions</span></span>
1. <span data-ttu-id="f9d86-141">Klicken Sie auf Lager.</span><span class="sxs-lookup"><span data-stu-id="f9d86-141">Click Inventory.</span></span>
2. <span data-ttu-id="f9d86-142">Klicken Sie auf "Transaktionen".</span><span class="sxs-lookup"><span data-stu-id="f9d86-142">Click Transactions.</span></span>
    * <span data-ttu-id="f9d86-143">Hier können Sie alle zugehörigen Transaktionen finden, die erstellt werden, wenn Sie die Lagerinventurerfassung buchen.</span><span class="sxs-lookup"><span data-stu-id="f9d86-143">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

