---
title: EUR-00002 - Angeben einer Ladungsadresse für eine Innergemeinschaftliche Buchung
description: Dieses Verfahren zeigt, wie eine Ladungsadresse für eine innergemeinschaftliche Handelsbuchung festgelegt wird.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, TransportationDocument, LogisticsPostalAddress, SysLookupMultiSelectGrid,  VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, Intrastat, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e555d6791f596850ba1ed718aa5593ee3f88bed9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407731"
---
# <a name="eur-00002-specifying-a-lading-address-for-an-intra-community-transaction"></a><span data-ttu-id="20526-103">EUR-00002 - Angeben einer Ladungsadresse für eine Innergemeinschaftliche Buchung</span><span class="sxs-lookup"><span data-stu-id="20526-103">EUR-00002 Specifying a lading address for an intra-community transaction</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="20526-104">Dieses Verfahren zeigt, wie eine Ladungsadresse für eine innergemeinschaftliche Handelsbuchung festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="20526-104">This procedure shows how to specify a lading address for an intra-community trade transaction.</span></span> <span data-ttu-id="20526-105">Zum Beispiel ein deutsches Unternehmens bestellt Artikel von einem Kreditor mit einer deutschen Geschäftsadresse.</span><span class="sxs-lookup"><span data-stu-id="20526-105">For example, a Germany company orders items from a vendor with a German business address.</span></span> <span data-ttu-id="20526-106">Dieser Kreditor hat einen Lagerort in Italien und liefert die Artikel von dort.</span><span class="sxs-lookup"><span data-stu-id="20526-106">This vendor has a warehouse in Italy and ships the items from there.</span></span> <span data-ttu-id="20526-107">Die Lieferung muss in Intrastat gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="20526-107">This delivery must be reported in the Intrastat.</span></span> <span data-ttu-id="20526-108">Dasselbe Verhalten gilt für Debitorenrücklieferungen.</span><span class="sxs-lookup"><span data-stu-id="20526-108">The same behavior is valid for customer returns.</span></span>
<span data-ttu-id="20526-109">Diese Prozedur gilt für alle europäischen Länder/Regionen.</span><span class="sxs-lookup"><span data-stu-id="20526-109">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="20526-110">Diese Aufgabe wurde mithilfe des Demodatenunternehmens DEMF mit der primären Adresse in Deutschland erstellt.</span><span class="sxs-lookup"><span data-stu-id="20526-110">The task was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="20526-111">Bevor Sie dieses Verfahren ausführen können, müssen Sie Intrastat-Berichte konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="20526-111">Before you can complete this procedure, you must configure Intrastat reporting.</span></span> <span data-ttu-id="20526-112">Diese Prozedur ist für Buchhalter vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="20526-112">This procedure is intended for accountants.</span></span> <span data-ttu-id="20526-113">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="20526-113">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="20526-114">Wechseln Sie zu "Kreditoren" > "Bestellungen" > "Alle Bestellungen".</span><span class="sxs-lookup"><span data-stu-id="20526-114">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="20526-115">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="20526-115">Click New.</span></span>
3. <span data-ttu-id="20526-116">Wert eingeben oder auswählen</span><span class="sxs-lookup"><span data-stu-id="20526-116">Enter or select a value</span></span>
    * <span data-ttu-id="20526-117">Wählen Sie z. B. DE-001 aus.</span><span class="sxs-lookup"><span data-stu-id="20526-117">For example, select DE-001.</span></span> <span data-ttu-id="20526-118">Dieser Kreditor hat eine deutsche Geschäftsadresse.</span><span class="sxs-lookup"><span data-stu-id="20526-118">This vendor has a German business address.</span></span>  
4. <span data-ttu-id="20526-119">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="20526-119">Click OK.</span></span>
5. <span data-ttu-id="20526-120">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="20526-120">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="20526-121">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie den Wert "D0001" aus.</span><span class="sxs-lookup"><span data-stu-id="20526-121">In the Item number field, enter or select a value D0001.</span></span>
7. <span data-ttu-id="20526-122">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="20526-122">Click Save.</span></span>
8. <span data-ttu-id="20526-123">Klicken Sie im Aktivitätsbereich auf "Entgegennehmen".</span><span class="sxs-lookup"><span data-stu-id="20526-123">On the Action Pane, click Receive.</span></span>
9. <span data-ttu-id="20526-124">Klicken Sie auf Transportdetails.</span><span class="sxs-lookup"><span data-stu-id="20526-124">Click Transportation details.</span></span>
10. <span data-ttu-id="20526-125">Geben Sie im Feld "Beladungsdatum und -uhrzeit" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="20526-125">In the Loading date and time field, enter a date and time.</span></span>
11. <span data-ttu-id="20526-126">Klicken Sie auf "Adresse hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="20526-126">Click Add address.</span></span>
12. <span data-ttu-id="20526-127">Klicken Sie auf "Neu" und erstellen Sie eine neue Adresse mit dem Zweck "Beladen".</span><span class="sxs-lookup"><span data-stu-id="20526-127">Click New and create new address with purpose Lading.</span></span>
13. <span data-ttu-id="20526-128">Geben Sie im Feld "Name oder Beschreibung" "Italienisch" ein.</span><span class="sxs-lookup"><span data-stu-id="20526-128">In the Name or description field, type 'Italian'.</span></span>
14. <span data-ttu-id="20526-129">Wählen Sie "Beladung" als Wert aus.</span><span class="sxs-lookup"><span data-stu-id="20526-129">Select Lading as the value.</span></span>
    * <span data-ttu-id="20526-130">Beachten Sie, das der Adresszweck "Beladen" muss.</span><span class="sxs-lookup"><span data-stu-id="20526-130">Note that that address purpose must be Lading.</span></span>  
15. <span data-ttu-id="20526-131">Wählen Sie im Feld Name/Region "ITA" aus oder geben Sie einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="20526-131">In the Country/region field, enter or select a value ITA.</span></span>
16. <span data-ttu-id="20526-132">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="20526-132">Click Save.</span></span>
17. <span data-ttu-id="20526-133">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="20526-133">Close the page.</span></span>
18. <span data-ttu-id="20526-134">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="20526-134">Click Save.</span></span>
    * <span data-ttu-id="20526-135">Überprüfen Sie, ob die Beladungsadresse korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="20526-135">Verify that the lading address is correct.</span></span>  
19. <span data-ttu-id="20526-136">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="20526-136">Close the page.</span></span>
20. <span data-ttu-id="20526-137">Klicken Sie im Aktivitätsbereich auf "Einkauf".</span><span class="sxs-lookup"><span data-stu-id="20526-137">On the Action Pane, click Purchase.</span></span>
21. <span data-ttu-id="20526-138">Klicken Sie auf "Bestätigen".</span><span class="sxs-lookup"><span data-stu-id="20526-138">Click Confirm.</span></span>
22. <span data-ttu-id="20526-139">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="20526-139">On the Action Pane, click Invoice.</span></span>
23. <span data-ttu-id="20526-140">Klicken Sie auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="20526-140">Click Invoice.</span></span>
24. <span data-ttu-id="20526-141">Geben Sie im Feld "Zahl" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="20526-141">In the Number field, type a value.</span></span>
25. <span data-ttu-id="20526-142">Geben Sie in das Feld "Rechnungsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="20526-142">In the Invoice date field, enter a date.</span></span>
26. <span data-ttu-id="20526-143">Klicken Sie auf "Standard von: Menge im Produktzugang", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="20526-143">Click Default from: Product receipt quantity to open the drop dialog.</span></span>
27. <span data-ttu-id="20526-144">Wählen Sie im Feld "Standardmenge für Positionen" "Menge im Produktzugang" aus.</span><span class="sxs-lookup"><span data-stu-id="20526-144">In the Default quantity for lines field, select 'Ordered quantity'.</span></span>
28. <span data-ttu-id="20526-145">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="20526-145">Click OK.</span></span>
29. <span data-ttu-id="20526-146">Klicken Sie auf Transportdetails.</span><span class="sxs-lookup"><span data-stu-id="20526-146">Click Transportation details.</span></span>
    * <span data-ttu-id="20526-147">Überprüfen Sie, dass Waren aus Italien versendet wurden.</span><span class="sxs-lookup"><span data-stu-id="20526-147">Verify that goods were shipped from Italy.</span></span> <span data-ttu-id="20526-148">Bei Bedarf können Sie die Ladungsdetails bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="20526-148">If necessary, you can edit the lading details.</span></span>  
30. <span data-ttu-id="20526-149">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="20526-149">Close the page.</span></span>
31. <span data-ttu-id="20526-150">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="20526-150">Click Post.</span></span>
32. <span data-ttu-id="20526-151">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="20526-151">Close the page.</span></span>
33. <span data-ttu-id="20526-152">Wechseln Sie zu "Steuer" > "Meldungen" > "Außenhandel" > "Intrastat".</span><span class="sxs-lookup"><span data-stu-id="20526-152">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
34. <span data-ttu-id="20526-153">Klicken Sie auf Übertragen.</span><span class="sxs-lookup"><span data-stu-id="20526-153">Click Transfer.</span></span>
35. <span data-ttu-id="20526-154">Wählen Sie "Ja" im Feld "Kreditorenrechnung" aus.</span><span class="sxs-lookup"><span data-stu-id="20526-154">Select Yes in the Vendor invoice field.</span></span>
36. <span data-ttu-id="20526-155">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="20526-155">Click OK.</span></span>
37. <span data-ttu-id="20526-156">Klicken Sie auf die Registerkarte "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="20526-156">Click the General tab.</span></span>
    * <span data-ttu-id="20526-157">Suchen Sie eine neu erstellte Position und vergewissern Sie sich, dass der Absender die Waren aus Italien liefert.</span><span class="sxs-lookup"><span data-stu-id="20526-157">Find a newly created line and verify that the sender shipped the goods from Italy.</span></span>  

