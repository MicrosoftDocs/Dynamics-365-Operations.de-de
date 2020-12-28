---
title: Bestand an einem Lagerort zählen
description: In diesem Thema wird der Prozess der Erstellung und Buchung einer Lagerinventurerfassung beschrieben, um einen bestimmten Artikel in einem Lagerplatz am Lagerort zu zählen.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 34013783bab79d80f1dac9a7806042608635e617
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428970"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="71a0c-103">Bestand an einem Lagerort zählen</span><span class="sxs-lookup"><span data-stu-id="71a0c-103">Count inventory in a warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="71a0c-104">In diesem Thema wird der Prozess der Erstellung und Buchung einer Lagerinventurerfassung beschrieben, um einen bestimmten Artikel in einem Lagerplatz am Lagerort zu zählen.</span><span class="sxs-lookup"><span data-stu-id="71a0c-104">This topic describes the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="71a0c-105">Die Prozedur ist auf die Funktion Grundlegendes Warehousing ausgelegt, die sich im Inventurverwaltungsmodul befindet, jedoch nicht auf die Warehousing-Funktion, die im Lagerortverwaltungsmodul verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="71a0c-105">The procedure applies to "basic warehousing" functionality, available in the Inventory management module, not to the warehousing functionality that's available in the Warehouse management module.</span></span> <span data-ttu-id="71a0c-106">Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="71a0c-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="71a0c-107">Wenn Sie eigene Daten verwenden, sollten Sie sicherstellen, dass Sie die Produkte und Lagerplatzeinstellung eingerichtet haben und dass Sie eine Lagererfassung für Inventurerfassungen erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="71a0c-107">If you're using your own data, make sure that you have products and locations set up, and that you've created an inventory journal name for counting journals.</span></span> <span data-ttu-id="71a0c-108">Die Lagerinventur wird in der Regel von einem Lagerortmitarbeiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71a0c-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="71a0c-109">Lagerinventurerfassung erstellen</span><span class="sxs-lookup"><span data-stu-id="71a0c-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="71a0c-110">Wechseln Sie zu **Navigationsbereich > Module > Lagerverwaltung > Journaleinträge > Artikelinventur > Inventur**.</span><span class="sxs-lookup"><span data-stu-id="71a0c-110">Go to **Navigation pane > Modules > Inventory management > Journal entries > Item counting > Counting**.</span></span>
2. <span data-ttu-id="71a0c-111">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="71a0c-111">Select **New**.</span></span>
3. <span data-ttu-id="71a0c-112">Wählen Sie im Feld **Name** aus der Dropdownliste den Namen der Lagerinventurerfassung aus, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="71a0c-112">In the **Name** field, select the inventory counting journal name you want to use from the drop-down list.</span></span> <span data-ttu-id="71a0c-113">Einige andere Felder werden basierend auf den Einstellungen der Lagerinventurerfassung ausgefüllt, die Sie auswählen.</span><span class="sxs-lookup"><span data-stu-id="71a0c-113">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
4. <span data-ttu-id="71a0c-114">Klicken Sie im Feld **Arbeitskraft** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="71a0c-114">In the **Worker** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="71a0c-115">**Wählen Sie** in der Liste die Arbeitskraft aus, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="71a0c-115">In the list, **Select** the worker you want to use.</span></span>
6. <span data-ttu-id="71a0c-116">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="71a0c-116">Select **OK**.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="71a0c-117">Erfassungspositionen erstellen</span><span class="sxs-lookup"><span data-stu-id="71a0c-117">Create journal lines</span></span>
1. <span data-ttu-id="71a0c-118">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="71a0c-118">Select **New**.</span></span>
2. <span data-ttu-id="71a0c-119">Wählen Sie im Feld **Artikelnummer** den gewünschten Datensatz aus der Dropdown-Liste aus.</span><span class="sxs-lookup"><span data-stu-id="71a0c-119">In the **Item number** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="71a0c-120">Wenn Sie das Demodatenunternehmen USMF verwenden, wählen Sie **A0001** aus.</span><span class="sxs-lookup"><span data-stu-id="71a0c-120">If you are using demo data company USMF, select **A0001**.</span></span>  
3. <span data-ttu-id="71a0c-121">Wählen Sie im Feld **Standort** den gewünschten Datensatz aus der Dropdown-Liste aus.</span><span class="sxs-lookup"><span data-stu-id="71a0c-121">In the **Site** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="71a0c-122">Wenn Sie das Demodatenunternehmen USMF verwenden, wählen Sie den Standort **2** aus.</span><span class="sxs-lookup"><span data-stu-id="71a0c-122">If you are using demo data company USMF, select site **2**.</span></span>
4. <span data-ttu-id="71a0c-123">Wählen Sie im Feld **Lagerort** den gewünschten Datensatz aus der Dropdown-Liste aus.</span><span class="sxs-lookup"><span data-stu-id="71a0c-123">In the **Warehouse** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="71a0c-124">Wenn Sie das Demodatenunternehmen USMF verwenden, wählen Sie den Lagerort **24** aus.</span><span class="sxs-lookup"><span data-stu-id="71a0c-124">If you are using demo data company USMF, select warehouse **24**.</span></span>  
5. <span data-ttu-id="71a0c-125">Wählen Sie im Feld **Standort** den gewünschten Datensatz aus der Dropdown-Liste aus.</span><span class="sxs-lookup"><span data-stu-id="71a0c-125">In the **Location** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="71a0c-126">Wenn Sie das Demodatenunternehmen USMF verwenden, wählen Sie den Standort **BULK-001** aus.</span><span class="sxs-lookup"><span data-stu-id="71a0c-126">If you are using demo data company USMF, select location **BULK-001**.</span></span>  
6. <span data-ttu-id="71a0c-127">Geben Sie im Feld "Gezählt" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="71a0c-127">In the Counted field, enter a number.</span></span> <span data-ttu-id="71a0c-128">Wenn Sie eine Anzahl eingeben, die von der Zahl im Feld **An Lager** abweicht, wird das Feld **Menge** aktualisiert, um die Abweichung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="71a0c-128">If you enter a counted number that's different to the number shown in the **On-hand** field, the **Quantity** field is updated to show the discrepancy.</span></span>  
7. <span data-ttu-id="71a0c-129">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="71a0c-129">Select **Save**.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="71a0c-130">Lagerinventurerfassung buchen</span><span class="sxs-lookup"><span data-stu-id="71a0c-130">Post the inventory counting journal</span></span>
1. <span data-ttu-id="71a0c-131">Wählen Sie **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="71a0c-131">Select **Post**.</span></span> <span data-ttu-id="71a0c-132">Wenn Sie eine Lagerinventurerfassung buchen und die gezählte Menge sich von der Menge unterscheidet, die im Feld **An Lager** gemeldet ist, wird ein Lagerzugang oder -abgang gebucht, der Lagerbestand und der Lagerwert werden geändert, und Sachkontobuchungen werden generiert.</span><span class="sxs-lookup"><span data-stu-id="71a0c-132">When you post an inventory counting journal, if the counted amount differs from amount that's reported in the **On-hand** field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>
2. <span data-ttu-id="71a0c-133">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="71a0c-133">Select **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="71a0c-134">Lagerbuchungen anzeigen</span><span class="sxs-lookup"><span data-stu-id="71a0c-134">View inventory transactions</span></span>
1. <span data-ttu-id="71a0c-135">Wählen Sie **Bestand** aus.</span><span class="sxs-lookup"><span data-stu-id="71a0c-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="71a0c-136">Wählen Sie **Buchungen** aus.</span><span class="sxs-lookup"><span data-stu-id="71a0c-136">Select **Transactions**.</span></span> <span data-ttu-id="71a0c-137">Hier können Sie alle zugehörigen Transaktionen finden, die erstellt werden, wenn Sie die Lagerinventurerfassung buchen.</span><span class="sxs-lookup"><span data-stu-id="71a0c-137">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

