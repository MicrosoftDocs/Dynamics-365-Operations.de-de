---
title: Bestandsnachverfolgungsinformationen korrigieren
description: Diese Prozedur führt Sie durch den einzelnen Schritte der Erstellung und des Buchens einer Umlagerungserfassung, um Lagerbestandsnachverfolgungsinformationen zu korrigieren.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a8a488d4c30923445b3ebc2626a79b8fa45012c7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204193"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="c61da-103">Bestandsnachverfolgungsinformationen korrigieren</span><span class="sxs-lookup"><span data-stu-id="c61da-103">Correct inventory tracking information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c61da-104">Diese Prozedur führt Sie durch den einzelnen Schritte der Erstellung und des Buchens einer Umlagerungserfassung, um Lagerbestandsnachverfolgungsinformationen zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="c61da-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="c61da-105">In diesem Beispiel aktualisieren wir die Informationen für eine durch einen Artikel gesteuerte Charge, indem wir eine falsch erfasste Charge mit einer anderen Charge ersetzen.</span><span class="sxs-lookup"><span data-stu-id="c61da-105">In this example, we'll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="c61da-106">Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USPI durchführen oder können Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="c61da-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="c61da-107">Wenn Sie eigene Daten verwenden, müssen Sie einen Artikel haben, der für Chargen aktiviert ist, denn er darf nicht über den Lagerplatz gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="c61da-107">If you use your own data, you need to have an item that's batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="c61da-108">Sie müssen außerdem einen Namen der Lagererfassungen für die Umlagerungen haben.</span><span class="sxs-lookup"><span data-stu-id="c61da-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="c61da-109">Diese Aufgaben werden normalerweise von einem Lagerortmitarbeiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c61da-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="c61da-110">Lagerumlagerungserfassung erstellen</span><span class="sxs-lookup"><span data-stu-id="c61da-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="c61da-111">Wechseln Sie zu "Umlagerung".</span><span class="sxs-lookup"><span data-stu-id="c61da-111">Go to Transfer.</span></span>
2. <span data-ttu-id="c61da-112">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="c61da-112">Click New.</span></span>
3. <span data-ttu-id="c61da-113">Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c61da-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="c61da-114">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c61da-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="c61da-115">Erfassungspositionen erstellen</span><span class="sxs-lookup"><span data-stu-id="c61da-115">Create journal lines</span></span>
1. <span data-ttu-id="c61da-116">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="c61da-116">Click New.</span></span>
2. <span data-ttu-id="c61da-117">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c61da-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="c61da-118">Wählen Sie USPI verwenden, wählten Sie Artikel M5003 aus.</span><span class="sxs-lookup"><span data-stu-id="c61da-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="c61da-119">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="c61da-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="c61da-120">Klicken Sie auf die Registerkarte "Lagerungsdimension".</span><span class="sxs-lookup"><span data-stu-id="c61da-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="c61da-121">Geben Sie im Feld "Chargennummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c61da-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="c61da-122">Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c61da-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="c61da-123">Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c61da-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="c61da-124">Geben Sie im Feld "Chargennummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c61da-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="c61da-125">Erfassung buchen</span><span class="sxs-lookup"><span data-stu-id="c61da-125">Post the journal</span></span>
1. <span data-ttu-id="c61da-126">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="c61da-126">Click Post.</span></span>
2. <span data-ttu-id="c61da-127">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c61da-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="c61da-128">Prüfen von Verfolgungsinformationen</span><span class="sxs-lookup"><span data-stu-id="c61da-128">Check tracing information</span></span>
1. <span data-ttu-id="c61da-129">Klicken Sie auf Lager.</span><span class="sxs-lookup"><span data-stu-id="c61da-129">Click Inventory.</span></span>
2. <span data-ttu-id="c61da-130">Klicken Sie auf "Verfolgen".</span><span class="sxs-lookup"><span data-stu-id="c61da-130">Click Trace.</span></span>
3. <span data-ttu-id="c61da-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c61da-131">Click OK.</span></span>
    * <span data-ttu-id="c61da-132">Bei Verwendung dieser Nachverfolgungsinformationen können Sie nachverfolgen, über welche Charge Sie den Bestand korrigieren.</span><span class="sxs-lookup"><span data-stu-id="c61da-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="c61da-133">Sie können die Seite "Artikelverfolgung" verwenden, um diese Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c61da-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="c61da-134">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c61da-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="c61da-135">Prüfen von Lagerbuchungen</span><span class="sxs-lookup"><span data-stu-id="c61da-135">Check inventory transactions</span></span>
1. <span data-ttu-id="c61da-136">Klicken Sie auf Lager.</span><span class="sxs-lookup"><span data-stu-id="c61da-136">Click Inventory.</span></span>
2. <span data-ttu-id="c61da-137">Klicken Sie auf "Transaktionen".</span><span class="sxs-lookup"><span data-stu-id="c61da-137">Click Transactions.</span></span>
    * <span data-ttu-id="c61da-138">Hier können Sie die Transaktionen anzeigen, die erstellt wurden, als Sie Ihre Erfassung gebucht haben.</span><span class="sxs-lookup"><span data-stu-id="c61da-138">Here you can see the transactions that were created when you posted your journal.</span></span>   

