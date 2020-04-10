---
title: Bestandsnachverfolgungsinformationen korrigieren
description: Diese Prozedur führt Sie durch den einzelnen Schritte der Erstellung und des Buchens einer Umlagerungserfassung, um Lagerbestandsnachverfolgungsinformationen zu korrigieren.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5155ada23fe4f559c79964e6bd10d86712009d1d
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145770"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="8ebc6-103">Bestandsnachverfolgungsinformationen korrigieren</span><span class="sxs-lookup"><span data-stu-id="8ebc6-103">Correct inventory tracking information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8ebc6-104">Diese Prozedur führt Sie durch den einzelnen Schritte der Erstellung und des Buchens einer Umlagerungserfassung, um Lagerbestandsnachverfolgungsinformationen zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="8ebc6-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="8ebc6-105">In diesem Beispiel aktualisieren wir die Informationen für eine durch einen Artikel gesteuerte Charge, indem wir eine falsch erfasste Charge mit einer anderen Charge ersetzen.</span><span class="sxs-lookup"><span data-stu-id="8ebc6-105">In this example, we'll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="8ebc6-106">Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USPI durchführen oder können Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="8ebc6-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="8ebc6-107">Wenn Sie eigene Daten verwenden, müssen Sie einen Artikel haben, der für Chargen aktiviert ist, denn er darf nicht über den Lagerplatz gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="8ebc6-107">If you use your own data, you need to have an item that's batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="8ebc6-108">Sie müssen außerdem einen Namen der Lagererfassungen für die Umlagerungen haben.</span><span class="sxs-lookup"><span data-stu-id="8ebc6-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="8ebc6-109">Diese Aufgaben werden normalerweise von einem Lagerortmitarbeiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ebc6-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="8ebc6-110">Lagerumlagerungserfassung erstellen</span><span class="sxs-lookup"><span data-stu-id="8ebc6-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="8ebc6-111">Wechseln Sie zu "Umlagerung".</span><span class="sxs-lookup"><span data-stu-id="8ebc6-111">Go to Transfer.</span></span>
2. <span data-ttu-id="8ebc6-112">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="8ebc6-112">Click New.</span></span>
3. <span data-ttu-id="8ebc6-113">Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="8ebc6-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="8ebc6-114">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8ebc6-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="8ebc6-115">Erfassungspositionen erstellen</span><span class="sxs-lookup"><span data-stu-id="8ebc6-115">Create journal lines</span></span>
1. <span data-ttu-id="8ebc6-116">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="8ebc6-116">Click New.</span></span>
2. <span data-ttu-id="8ebc6-117">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="8ebc6-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="8ebc6-118">Wählen Sie USPI verwenden, wählten Sie Artikel M5003 aus.</span><span class="sxs-lookup"><span data-stu-id="8ebc6-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="8ebc6-119">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="8ebc6-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="8ebc6-120">Klicken Sie auf die Registerkarte "Lagerungsdimension".</span><span class="sxs-lookup"><span data-stu-id="8ebc6-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="8ebc6-121">Geben Sie im Feld "Chargennummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="8ebc6-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="8ebc6-122">Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="8ebc6-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="8ebc6-123">Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="8ebc6-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="8ebc6-124">Geben Sie im Feld "Chargennummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="8ebc6-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="8ebc6-125">Erfassung buchen</span><span class="sxs-lookup"><span data-stu-id="8ebc6-125">Post the journal</span></span>
1. <span data-ttu-id="8ebc6-126">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="8ebc6-126">Click Post.</span></span>
2. <span data-ttu-id="8ebc6-127">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8ebc6-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="8ebc6-128">Prüfen von Verfolgungsinformationen</span><span class="sxs-lookup"><span data-stu-id="8ebc6-128">Check tracing information</span></span>
1. <span data-ttu-id="8ebc6-129">Klicken Sie auf Lager.</span><span class="sxs-lookup"><span data-stu-id="8ebc6-129">Click Inventory.</span></span>
2. <span data-ttu-id="8ebc6-130">Klicken Sie auf "Verfolgen".</span><span class="sxs-lookup"><span data-stu-id="8ebc6-130">Click Trace.</span></span>
3. <span data-ttu-id="8ebc6-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8ebc6-131">Click OK.</span></span>
    * <span data-ttu-id="8ebc6-132">Bei Verwendung dieser Nachverfolgungsinformationen können Sie nachverfolgen, über welche Charge Sie den Bestand korrigieren.</span><span class="sxs-lookup"><span data-stu-id="8ebc6-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="8ebc6-133">Sie können die Seite "Artikelverfolgung" verwenden, um diese Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8ebc6-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="8ebc6-134">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8ebc6-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="8ebc6-135">Prüfen von Lagerbuchungen</span><span class="sxs-lookup"><span data-stu-id="8ebc6-135">Check inventory transactions</span></span>
1. <span data-ttu-id="8ebc6-136">Klicken Sie auf Lager.</span><span class="sxs-lookup"><span data-stu-id="8ebc6-136">Click Inventory.</span></span>
2. <span data-ttu-id="8ebc6-137">Klicken Sie auf "Transaktionen".</span><span class="sxs-lookup"><span data-stu-id="8ebc6-137">Click Transactions.</span></span>
    * <span data-ttu-id="8ebc6-138">Hier können Sie die Transaktionen anzeigen, die erstellt wurden, als Sie Ihre Erfassung gebucht haben.</span><span class="sxs-lookup"><span data-stu-id="8ebc6-138">Here you can see the transactions that were created when you posted your journal.</span></span>   

