---
title: Physischen Bestand im Lagerort übertragen
description: Diese Prozedur führt Sie durch den Prozess der Erstellung und des Buchens einer Umlagerungserfassung, um Artikelbewegungen von einem Lagerplatz eines Lagerorts an einen anderen zu erfassen.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 540ba2266ea74c36babce57670f84159c89018f1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428956"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="9ca24-103">Physischen Bestand im Lagerort übertragen</span><span class="sxs-lookup"><span data-stu-id="9ca24-103">Transfer physical inventory within the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9ca24-104">Diese Prozedur führt Sie durch den Prozess der Erstellung und des Buchens einer Umlagerungserfassung, um Artikelbewegungen von einem Lagerplatz eines Lagerorts an einen anderen zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="9ca24-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="9ca24-105">Sie müssen einen Namen der Lagererfassungen für die Umlagerungen haben, bevor Sie diese starten.</span><span class="sxs-lookup"><span data-stu-id="9ca24-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="9ca24-106">Sie können diese Prozedur im Demodatunternehmen USMF mithilfe der angezeigten Beispielswerte ausführen, oder eigene Daten verwenden, wenn Sie bereits Produkte und Lagerplätze eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="9ca24-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="9ca24-107">Diese Aufgaben werden normalerweise von einem Lagerortmitarbeiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ca24-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="9ca24-108">Lagerumlagerungserfassung erstellen</span><span class="sxs-lookup"><span data-stu-id="9ca24-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="9ca24-109">Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Bestandsverwaltung > Journalbuchungen > Positionen > Transfer**.</span><span class="sxs-lookup"><span data-stu-id="9ca24-109">In the **Navigation pane**, go to **Inventory management > Journal entries > Items > Transfer**.</span></span>
2. <span data-ttu-id="9ca24-110">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="9ca24-110">Click **New**.</span></span>
3. <span data-ttu-id="9ca24-111">Geben Sie im Feld **Name** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9ca24-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="9ca24-112">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="9ca24-112">Click **OK**.</span></span> <span data-ttu-id="9ca24-113">Es gibt die Option, "Von"- und "Bis"-Dimensionen für jede Erfassungsposition anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9ca24-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="9ca24-114">Dies ist für diesen Erfassungstyp wesentlich.</span><span class="sxs-lookup"><span data-stu-id="9ca24-114">These are essential for this journal type.</span></span> <span data-ttu-id="9ca24-115">Sie können Artikel unter Verwendung der verschiedenen Regeln an andere Lagerplätze umlagern.</span><span class="sxs-lookup"><span data-stu-id="9ca24-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="9ca24-116">In diesem Beispiel lagern Sie einen Artikel innerhalb des gleichen Lagerorts von einem Ladungsträger gesteuerten Lagerplatz zu einem Lagerplatz, der nicht von einem Ladungsträger gesteuert wird, um.</span><span class="sxs-lookup"><span data-stu-id="9ca24-116">In this example we'll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="9ca24-117">Erfassungspositionen erstellen</span><span class="sxs-lookup"><span data-stu-id="9ca24-117">Create journal lines</span></span>
1. <span data-ttu-id="9ca24-118">In den **Journalzeilen fastTab**, klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="9ca24-118">Int the **Journal lines fastTab**, click **New**.</span></span>
2. <span data-ttu-id="9ca24-119">Geben Sie im Feld **Artikelnummer** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9ca24-119">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="9ca24-120">Wenn Sie USMF verwenden, können Sie A0001 auswählen.</span><span class="sxs-lookup"><span data-stu-id="9ca24-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="9ca24-121">Geben Sie im Feld **Vom Standort** einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9ca24-121">In the **From site** field, enter or select a value.</span></span> <span data-ttu-id="9ca24-122">Wenn Sie USMF verwenden, können Sie "2" auswählen.</span><span class="sxs-lookup"><span data-stu-id="9ca24-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="9ca24-123">Geben Sie im Feld **Zu Standort** einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9ca24-123">In the **To site** field, enter or select a value.</span></span> <span data-ttu-id="9ca24-124">Wenn Sie USMF verwenden, können Sie "2" auswählen.</span><span class="sxs-lookup"><span data-stu-id="9ca24-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="9ca24-125">Geben Sie im Feld **Ab Lager** einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9ca24-125">In the **From warehouse** field, enter or select a value.</span></span> <span data-ttu-id="9ca24-126">Wenn Sie USMF verwenden, können Sie "24" auswählen.</span><span class="sxs-lookup"><span data-stu-id="9ca24-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="9ca24-127">Geben Sie im Feld **Zu Lager** einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9ca24-127">In the **To warehouse** field, enter or select a value.</span></span> <span data-ttu-id="9ca24-128">Wenn Sie USMF verwenden, können Sie "24" auswählen.</span><span class="sxs-lookup"><span data-stu-id="9ca24-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="9ca24-129">Geben Sie im Feld **Ab Standort** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9ca24-129">In the **From location** field, enter or select a value.</span></span> <span data-ttu-id="9ca24-130">Wenn Sie USMF verwenden, können Sie "FL-001" auswählen.</span><span class="sxs-lookup"><span data-stu-id="9ca24-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="9ca24-131">Geben Sie im Feld **Zur Position** einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9ca24-131">In the **To location** field, enter or select a value.</span></span> <span data-ttu-id="9ca24-132">Wenn Sie USMF verwenden, können Sie "BULK-001" auswählen.</span><span class="sxs-lookup"><span data-stu-id="9ca24-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="9ca24-133">Geben Sie im Feld **Menge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="9ca24-133">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="9ca24-134">Klicken Sie in der Registerkarte **Liniendetails** fastTab auf die Registerkarte **Bestandsmaße**.</span><span class="sxs-lookup"><span data-stu-id="9ca24-134">In the **Line details** fastTab, click the **Inventory dimensions** tab.</span></span>
11. <span data-ttu-id="9ca24-135">Geben Sie unter **Aus Bestandsdimensionen** im Feld **Lizenzplatte** einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9ca24-135">In **From inventory dimensions**, in the **License plate** field, enter or select a value.</span></span> <span data-ttu-id="9ca24-136">Wenn Sie USMF verwenden, können Sie "24" auswählen.</span><span class="sxs-lookup"><span data-stu-id="9ca24-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="9ca24-137">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="9ca24-137">Click **Save**.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="9ca24-138">Umlagerungserfassung buchen</span><span class="sxs-lookup"><span data-stu-id="9ca24-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="9ca24-139">Klicken Sie im **Aktivitätsbereich** auf **Buchen**.</span><span class="sxs-lookup"><span data-stu-id="9ca24-139">On the **Action Pane**, click **Post**.</span></span>
2. <span data-ttu-id="9ca24-140">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="9ca24-140">Click **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="9ca24-141">Lagerbuchungen anzeigen</span><span class="sxs-lookup"><span data-stu-id="9ca24-141">View inventory transactions</span></span>
1. <span data-ttu-id="9ca24-142">Klicken Sie auf **Bestand**.</span><span class="sxs-lookup"><span data-stu-id="9ca24-142">Click **Inventory**.</span></span>
2. <span data-ttu-id="9ca24-143">Klicken Sie auf **Transaktionen**.</span><span class="sxs-lookup"><span data-stu-id="9ca24-143">Click **Transactions**.</span></span> <span data-ttu-id="9ca24-144">Hier können Sie die Transaktionen anzeigen, die erstellt wurden, als Sie Ihre Erfassung gebucht haben.</span><span class="sxs-lookup"><span data-stu-id="9ca24-144">Here you can see the transactions that were created when you posted your journal.</span></span>  

