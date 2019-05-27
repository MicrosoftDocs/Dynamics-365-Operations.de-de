---
title: Bestandswerte im Lagerort anpassen (grundlegendes Warehousing)
description: Diese Prozedur führt Sie durch die einzelnen Schritte der Erstellung und des Buchens einer Lagerregulierungserfassung, um Bestandswerte von Produkten im Lagerort anzupassen.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 330ebacf4a036b2df6ca22728477cae5b347354d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550092"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a><span data-ttu-id="75f8c-103">Bestandswerte im Lagerort anpassen (grundlegendes Warehousing)</span><span class="sxs-lookup"><span data-stu-id="75f8c-103">Adjust stock levels in the warehouse (basic warehousing)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="75f8c-104">Diese Prozedur führt Sie durch die einzelnen Schritte der Erstellung und des Buchens einer Lagerregulierungserfassung, um Bestandswerte von Produkten im Lagerort anzupassen.</span><span class="sxs-lookup"><span data-stu-id="75f8c-104">This procedure walks you through the process of creating and posting an inventory adjustment journal in order to adjust stock levels of products in the warehouse.</span></span> <span data-ttu-id="75f8c-105">Sie müssen einen Lagererfassungnamen für die Bestandsregulierungen haben, bevor Sie diese starten.</span><span class="sxs-lookup"><span data-stu-id="75f8c-105">You need to have an inventory journal name set up for inventory adjustments before you start this.</span></span> <span data-ttu-id="75f8c-106">Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="75f8c-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="75f8c-107">Diese Aufgaben werden normalerweise von einem Lagerortmitarbeiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75f8c-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-adjustment-journal"></a><span data-ttu-id="75f8c-108">Lagerregulierungserfassung erstellen</span><span class="sxs-lookup"><span data-stu-id="75f8c-108">Create an inventory adjustment journal</span></span>
1. <span data-ttu-id="75f8c-109">Wechseln Sie zu Lagerverwaltung > Journaleinträge > Artikel > Lagerregulierung.</span><span class="sxs-lookup"><span data-stu-id="75f8c-109">Go to Inventory management > Journal entries > Items > Inventory adjustment.</span></span>
2. <span data-ttu-id="75f8c-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="75f8c-110">Click New.</span></span>
3. <span data-ttu-id="75f8c-111">Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="75f8c-111">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="75f8c-112">Klicken Sie in der Liste auf den Lageregulierungserfassungsnamen, den Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="75f8c-112">In the list, click on the inventory adjustment journal name you want to use.</span></span>
    * <span data-ttu-id="75f8c-113">Einige andere Felder werden basierend auf den Einstellungen der Lagerregulierungserfassung ausgefüllt, die Sie auswählen.</span><span class="sxs-lookup"><span data-stu-id="75f8c-113">Some other fields will be populated based on the setup of the inventory adjustment journal name you select.</span></span>  
5. <span data-ttu-id="75f8c-114">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="75f8c-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="75f8c-115">Erfassungspositionen erstellen</span><span class="sxs-lookup"><span data-stu-id="75f8c-115">Create journal lines</span></span>
1. <span data-ttu-id="75f8c-116">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="75f8c-116">Click New.</span></span>
2. <span data-ttu-id="75f8c-117">Markieren Sie das Feld "Artikelnummer" in der Liste.</span><span class="sxs-lookup"><span data-stu-id="75f8c-117">In the list, mark the item number field.</span></span>
3. <span data-ttu-id="75f8c-118">Wählen Sie im Feld "Artikelnummer" einen Artikel aus.</span><span class="sxs-lookup"><span data-stu-id="75f8c-118">In the Item number field, Select an item.</span></span> <span data-ttu-id="75f8c-119">Wenn Sie das Demodatunternehmen USMF verwenden, geben Sie " D0001" ein.</span><span class="sxs-lookup"><span data-stu-id="75f8c-119">If you are using demo data company USMF, type 'D0001'.</span></span>
4. <span data-ttu-id="75f8c-120">Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="75f8c-120">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="75f8c-121">Wählen Sie in der Liste einen Lagerplatz aus.</span><span class="sxs-lookup"><span data-stu-id="75f8c-121">In the list, select a site.</span></span>
6. <span data-ttu-id="75f8c-122">Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="75f8c-122">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="75f8c-123">Wählen Sie in der Liste einen Lagerort aus.</span><span class="sxs-lookup"><span data-stu-id="75f8c-123">In the list, select a warehouse.</span></span>
    * <span data-ttu-id="75f8c-124">Wenn Sie einen Artikel mit Lagerplatz als obligatorische Dimension ausgewählt haben, müssen Sie den Lagerplatz hier festlegen.</span><span class="sxs-lookup"><span data-stu-id="75f8c-124">If you have selected an item with Location as a mandatory dimension, you would have to specify the location here.</span></span>  
8. <span data-ttu-id="75f8c-125">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="75f8c-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="75f8c-126">Der Einstandspreis legt die Kosten pro Einheit für Lagerzugänge fest.</span><span class="sxs-lookup"><span data-stu-id="75f8c-126">The cost price field specifies the cost per unit for inventory receipts.</span></span> <span data-ttu-id="75f8c-127">Wenn keine Kosten für die Artikelnummer angegeben sind oder diese manuell geändert werden sollen, geben Sie sie hier ein.</span><span class="sxs-lookup"><span data-stu-id="75f8c-127">If the cost is not specified for the item number or if you wanted to change it manually, you would do this here.</span></span>  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a><span data-ttu-id="75f8c-128">Lagerregulierungserfassung prüfen und buchen</span><span class="sxs-lookup"><span data-stu-id="75f8c-128">Validate and post the inventory adjustment journal</span></span>
1. <span data-ttu-id="75f8c-129">Klicken Sie auf "Überprüfen".</span><span class="sxs-lookup"><span data-stu-id="75f8c-129">Click Validate.</span></span>
2. <span data-ttu-id="75f8c-130">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="75f8c-130">Click OK.</span></span>
3. <span data-ttu-id="75f8c-131">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="75f8c-131">Click Post.</span></span>
    * <span data-ttu-id="75f8c-132">Beim Buchen dieser Art von Erfassung wird ein Lagerzugang oder -abgang gebucht, der Lagerbestand und der Lagerwert werden geändert, und Sachkontobuchungen werden generiert.</span><span class="sxs-lookup"><span data-stu-id="75f8c-132">When you post this kind of journal, an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
4. <span data-ttu-id="75f8c-133">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="75f8c-133">Click OK.</span></span>
5. <span data-ttu-id="75f8c-134">Schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="75f8c-134">Close the form.</span></span>
6. <span data-ttu-id="75f8c-135">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="75f8c-135">Close the page.</span></span>

