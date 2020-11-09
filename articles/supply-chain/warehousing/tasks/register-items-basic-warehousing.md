---
title: Erfassen von Artikeln für einen grundlegendes Warehousing aktivierten Artikel mithilfe eines Artikels eine Wareneingangserfassung
description: Dieses Verfahren zeigt Ihnen an, wie Artikel mithilfe der Wareneingangserfassung erfasst werden, wenn Sie grundlegendes Warehousing im Inventurverwaltungsmodul verwenden.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 940fa33b10c5f60f469187b11dd066091581996f
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018467"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a><span data-ttu-id="e7a16-103">Erfassen von Artikeln für einen grundlegendes Warehousing aktivierten Artikel mithilfe eines Artikels eine Wareneingangserfassung</span><span class="sxs-lookup"><span data-stu-id="e7a16-103">Register items for a basic warehousing enabled item using an item an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e7a16-104">Dieses Verfahren zeigt Ihnen an, wie Artikel mithilfe der Wareneingangserfassung erfasst werden, wenn Sie grundlegendes Warehousing im Inventurverwaltungsmodul verwenden.</span><span class="sxs-lookup"><span data-stu-id="e7a16-104">This procedure shows you how to register items using the item arrival journal when you are using "basic warehousing" in the Inventory management module.</span></span> <span data-ttu-id="e7a16-105">Dies wird in der Regel von einem Sachbearbeiter für Zugänge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7a16-105">This would usually be done by a receiving clerk.</span></span> <span data-ttu-id="e7a16-106">Sie können diese Prozedur im Demodatenunternehmen USMF mit den Beispielswerten ausführen, die angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e7a16-106">You can run this procedure in demo data company USMF with the example values that are shown.</span></span>  <span data-ttu-id="e7a16-107">Wenn Sie nicht USMF verwenden, müssen Sie eine bestätigte Bestellung mit einer offenen Bestellposition haben, bevor Sie dieses Handbuch starten.</span><span class="sxs-lookup"><span data-stu-id="e7a16-107">If you are not using USMF, you need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="e7a16-108">Der Artikel für die Position muss gelagert sein.</span><span class="sxs-lookup"><span data-stu-id="e7a16-108">The item on the line must be stocked.</span></span> <span data-ttu-id="e7a16-109">Der Artikel muss außerdem einer Lagerdimensionsgruppe zugeordnet werden, in der Standort und Lagerort aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="e7a16-109">And the item needs to be associated with a storage dimension group, where site and warehouse are active.</span></span>


## <a name="create-item-arrival-journal-header"></a><span data-ttu-id="e7a16-110">Wareneingangserfassungs-Kopfzeile erstellen</span><span class="sxs-lookup"><span data-stu-id="e7a16-110">Create item arrival journal header</span></span>
1. <span data-ttu-id="e7a16-111">Wechseln Sie zu "Lagerverwaltung" > "Journaleinträge" > "Wareneingang" > "Wareneingang".</span><span class="sxs-lookup"><span data-stu-id="e7a16-111">Go to Inventory management > Journal entries > Item arrival > Item arrival.</span></span>
2. <span data-ttu-id="e7a16-112">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="e7a16-112">Click New.</span></span>
3. <span data-ttu-id="e7a16-113">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e7a16-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="e7a16-114">Wenn Sie USMF verwenden, können Sie WHS eingeben.</span><span class="sxs-lookup"><span data-stu-id="e7a16-114">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="e7a16-115">Wenn Sie andere Daten verwenden, muss die Erfassung, deren Namen Sie auswählen, die folgenden Eigenschaften haben: „Entnahmeort prüfen“ muss auf „Kein“ festgelegt werden, und „Quarantäneverwaltung“ muss auf „Nein“ festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e7a16-115">If you're using other data, the journal whose name you choose has to have the following properties: cheque picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="e7a16-116">Geben Sie im Feld "Lieferschein" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e7a16-116">In the Packing slip field, type a value.</span></span>
    * <span data-ttu-id="e7a16-117">Dies ist die Lieferscheinkennung des Lieferscheins, der vom Kreditor ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e7a16-117">This is the packing slip ID from the packing slip issued by the vendor.</span></span> <span data-ttu-id="e7a16-118">Eindeutige Nummer hinzufügen</span><span class="sxs-lookup"><span data-stu-id="e7a16-118">Add a unique number.</span></span>  
5. <span data-ttu-id="e7a16-119">Wählen Sie im Feld "Nummer" die Bestellung aus.</span><span class="sxs-lookup"><span data-stu-id="e7a16-119">In the Number field, In the Number field, select the purchase order..</span></span>
6. <span data-ttu-id="e7a16-120">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="e7a16-120">Click OK.</span></span>

## <a name="add-lines-to-item-arrival-journal"></a><span data-ttu-id="e7a16-121">Positionen zur Wareneingangserfassung hinzufügen</span><span class="sxs-lookup"><span data-stu-id="e7a16-121">Add lines to item arrival journal</span></span>
1. <span data-ttu-id="e7a16-122">Klicken Sie auf Funktionen.</span><span class="sxs-lookup"><span data-stu-id="e7a16-122">Click Functions.</span></span>
2. <span data-ttu-id="e7a16-123">Klicken Sie auf "Positionen erstellen".</span><span class="sxs-lookup"><span data-stu-id="e7a16-123">Click Create lines.</span></span>
    * <span data-ttu-id="e7a16-124">Die Positionen können in diese Erfassung manuell eingegeben oder automatisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e7a16-124">The lines can be entered manually into this journal or created automatically.</span></span> <span data-ttu-id="e7a16-125">Dies zeigt Ihnen an, wie dies automatisch erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e7a16-125">This will show you how to create this automatically.</span></span>  
3. <span data-ttu-id="e7a16-126">Aktivieren oder deaktivieren Sie das Kontrollkästchen "Menge initialisieren".</span><span class="sxs-lookup"><span data-stu-id="e7a16-126">Check or uncheck the Initialize quantity checkbox.</span></span>
    * <span data-ttu-id="e7a16-127">Dies initialisiert die Menge in den Erfassungspositionen mit der Menge, die nicht aus der Bestellposition erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="e7a16-127">This will initialize the quantity on the journal lines with the quantity not registered from the purchase order line.</span></span>  
4. <span data-ttu-id="e7a16-128">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="e7a16-128">Click OK.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="e7a16-129">Erfassung buchen</span><span class="sxs-lookup"><span data-stu-id="e7a16-129">Post the journal</span></span>
1. <span data-ttu-id="e7a16-130">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="e7a16-130">Click Post.</span></span>
2. <span data-ttu-id="e7a16-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="e7a16-131">Click OK.</span></span>

## <a name="generate-the-product-receipt"></a><span data-ttu-id="e7a16-132">Produktzugang generieren</span><span class="sxs-lookup"><span data-stu-id="e7a16-132">Generate the product receipt</span></span>
1. <span data-ttu-id="e7a16-133">Klicken Sie auf Funktionen.</span><span class="sxs-lookup"><span data-stu-id="e7a16-133">Click Functions.</span></span>
2. <span data-ttu-id="e7a16-134">Klicken Sie auf "Produktzugang".</span><span class="sxs-lookup"><span data-stu-id="e7a16-134">Click Product receipt.</span></span>
3. <span data-ttu-id="e7a16-135">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="e7a16-135">Click OK.</span></span>

