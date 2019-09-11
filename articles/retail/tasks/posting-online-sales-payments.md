---
title: Buchen von Online-Verkäufen und -Zahlungen
description: Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und die Ausführung eines wiederkehrenden Batchauftrags zum Erstellen von Aufträgen und Zahlungen für Onlineshopbuchungen.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d42b585a61214628980cd45a859215443ed55b5
ms.sourcegitcommit: c461758290d7ddc19f0b60701368937c35ef78b0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864152"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="846da-103">Buchen von Online-Verkäufen und -Zahlungen</span><span class="sxs-lookup"><span data-stu-id="846da-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="846da-104">Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und die Ausführung eines wiederkehrenden Batchauftrags zum Erstellen von Aufträgen und Zahlungen für Onlineshopbuchungen.</span><span class="sxs-lookup"><span data-stu-id="846da-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="846da-105">Die Buchung von Online-Verkäufen und Zahlungen ist ein zweistufiger Prozess.</span><span class="sxs-lookup"><span data-stu-id="846da-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="846da-106">Abruf der Online-Retail-Transaktionsdaten in der Zentrale.</span><span class="sxs-lookup"><span data-stu-id="846da-106">Pulling the online retail transaction data in HQ.</span></span>
- <span data-ttu-id="846da-107">Synchronisieren von Aufträgen, um Kundenaufträge in der Zentrale anzulegen.</span><span class="sxs-lookup"><span data-stu-id="846da-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="846da-108">Das Abrufen der Online-Retail-Transaktionsdaten kann entweder durch manuelles Ausführen des P-Jobs oder durch Erstellen eines wiederkehrenden Batch-Jobs erfolgen.</span><span class="sxs-lookup"><span data-stu-id="846da-108">Pulling the online retail transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="846da-109">Manuelles Ausführen des P-Jobs</span><span class="sxs-lookup"><span data-stu-id="846da-109">Manually running the P-job</span></span>

1. <span data-ttu-id="846da-110">Gehen Sie zu Alle Arbeitsbereiche > Retail IT.</span><span class="sxs-lookup"><span data-stu-id="846da-110">Go to All workspaces > Retail IT.</span></span>
2. <span data-ttu-id="846da-111">Klicken Sie auf Verteilungsplan.</span><span class="sxs-lookup"><span data-stu-id="846da-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="846da-112">Wählen Sie P-0001.</span><span class="sxs-lookup"><span data-stu-id="846da-112">Select P-0001.</span></span>
4. <span data-ttu-id="846da-113">Passen Sie bei Bedarf die Gruppen der Kanaldatenbank an.</span><span class="sxs-lookup"><span data-stu-id="846da-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="846da-114">Klicken Sie auf Jetzt ausführen</span><span class="sxs-lookup"><span data-stu-id="846da-114">Click Run now.</span></span>
6. <span data-ttu-id="846da-115">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="846da-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="846da-116">Einplanen eines wiederkehrenden P-Jobs</span><span class="sxs-lookup"><span data-stu-id="846da-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="846da-117">Gehen Sie zu Alle Arbeitsbereiche > Retail IT.</span><span class="sxs-lookup"><span data-stu-id="846da-117">Go to All workspaces > Retail IT.</span></span>
2. <span data-ttu-id="846da-118">Klicken Sie auf Verteilungsplan.</span><span class="sxs-lookup"><span data-stu-id="846da-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="846da-119">Wählen Sie P-0001.</span><span class="sxs-lookup"><span data-stu-id="846da-119">Select P-0001.</span></span>
4. <span data-ttu-id="846da-120">Klicken Sie auf Batch-Job erstellen.</span><span class="sxs-lookup"><span data-stu-id="846da-120">Click Create batch job.</span></span>
5. <span data-ttu-id="846da-121">Klicken Sie im Hintergrund auf Ausführen.</span><span class="sxs-lookup"><span data-stu-id="846da-121">Click Run in the background.</span></span>
5. <span data-ttu-id="846da-122">Aktivieren Sie die Stapelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="846da-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="846da-123">Klicken Sie auf Wiederholung.</span><span class="sxs-lookup"><span data-stu-id="846da-123">Click Recurrence..</span></span>
7. <span data-ttu-id="846da-124">Wählen Sie die Option "Kein Enddatum" aus.</span><span class="sxs-lookup"><span data-stu-id="846da-124">Select the No end date option.</span></span>
8. <span data-ttu-id="846da-125">Geben Sie im Feld Zähler das Intervall zwischen den Läufen in Minuten ein.</span><span class="sxs-lookup"><span data-stu-id="846da-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="846da-126">Typischerweise wäre dies 5-10.</span><span class="sxs-lookup"><span data-stu-id="846da-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="846da-127">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="846da-127">Click OK.</span></span>
10. <span data-ttu-id="846da-128">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="846da-128">Click OK.</span></span>

<span data-ttu-id="846da-129">Aufträge können entweder durch manuelles Ausführen des Jobs „Aufträge synchronisieren“ oder durch Erstellen eines wiederkehrenden Batch-Jobs synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="846da-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="846da-130">Manuell laufende Auftragssynchronisation</span><span class="sxs-lookup"><span data-stu-id="846da-130">Manually running order synchronization</span></span> 

<span data-ttu-id="846da-131">Führen Sie diese Schritte aus, um den Job „Aufträge synchronisieren“ einmal manuell auszuführen.</span><span class="sxs-lookup"><span data-stu-id="846da-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="846da-132">Wechseln Sie zu Alle Arbeitsbereiche > Finanzdaten für den Einzelhandelsshop.</span><span class="sxs-lookup"><span data-stu-id="846da-132">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="846da-133">Klicken Sie auf "Aufträge synchronisieren".</span><span class="sxs-lookup"><span data-stu-id="846da-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="846da-134">Wählen Sie im Organisationshierarchie-Feld "Einzelhandelsgeschäfte nach Region" aus.</span><span class="sxs-lookup"><span data-stu-id="846da-134">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="846da-135">Wählen Sie entweder einen bestimmten Online-Shop oder einen Knoten aus, wenn Sie den Batchauftrag für eine Gruppe von Shops erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="846da-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="846da-136">Klicken Sie auf den Pfeil, um die Auswahl hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="846da-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="846da-137">Klicken Sie auf die Registerkarte "Im Hintergrund ausführen".</span><span class="sxs-lookup"><span data-stu-id="846da-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="846da-138">Stapelverarbeitung deaktivieren</span><span class="sxs-lookup"><span data-stu-id="846da-138">Disable Batch processing</span></span>
6. <span data-ttu-id="846da-139">Klicken Sie auf "Wiederholung".</span><span class="sxs-lookup"><span data-stu-id="846da-139">Click Recurrence.</span></span>
7. <span data-ttu-id="846da-140">Wählen Sie die Option Ende nach</span><span class="sxs-lookup"><span data-stu-id="846da-140">Select End After option</span></span>
8. <span data-ttu-id="846da-141">Geben Sie im Feld Ende nach 1 ein.</span><span class="sxs-lookup"><span data-stu-id="846da-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="846da-142">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="846da-142">Click OK.</span></span>
10. <span data-ttu-id="846da-143">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="846da-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="846da-144">Terminierung der Synchronisation wiederkehrender Aufträge</span><span class="sxs-lookup"><span data-stu-id="846da-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="846da-145">Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und die Ausführung eines wiederkehrenden Batchauftrags zum Erstellen von Aufträgen und Zahlungen für Onlineshopbuchungen.</span><span class="sxs-lookup"><span data-stu-id="846da-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="846da-146">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="846da-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="846da-147">Wechseln Sie zu Alle Arbeitsbereiche > Finanzdaten für den Einzelhandelsshop.</span><span class="sxs-lookup"><span data-stu-id="846da-147">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="846da-148">Klicken Sie auf "Aufträge synchronisieren".</span><span class="sxs-lookup"><span data-stu-id="846da-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="846da-149">Wählen Sie im Organisationshierarchie-Feld "Einzelhandelsgeschäfte nach Region" aus.</span><span class="sxs-lookup"><span data-stu-id="846da-149">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="846da-150">Wählen Sie entweder einen bestimmten Online-Shop oder einen Knoten aus, wenn Sie den Batchauftrag für eine Gruppe von Shops erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="846da-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="846da-151">Klicken Sie auf den Pfeil, um die Auswahl hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="846da-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="846da-152">Klicken Sie auf die Registerkarte "Im Hintergrund ausführen".</span><span class="sxs-lookup"><span data-stu-id="846da-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="846da-153">Batch-Verarbeitung aktivieren</span><span class="sxs-lookup"><span data-stu-id="846da-153">Enable Batch processing</span></span>
6. <span data-ttu-id="846da-154">Klicken Sie auf "Wiederholung".</span><span class="sxs-lookup"><span data-stu-id="846da-154">Click Recurrence.</span></span>
7. <span data-ttu-id="846da-155">Wählen Sie die Option "Kein Enddatum" aus.</span><span class="sxs-lookup"><span data-stu-id="846da-155">Select the No end date option.</span></span>
8. <span data-ttu-id="846da-156">Geben Sie im Feld Zähler das Intervall zwischen den Läufen in Minuten ein.</span><span class="sxs-lookup"><span data-stu-id="846da-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="846da-157">Typischerweise wäre dies 2-20.</span><span class="sxs-lookup"><span data-stu-id="846da-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="846da-158">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="846da-158">Click OK.</span></span>
10. <span data-ttu-id="846da-159">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="846da-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="846da-160">Am Prozess beteiligte Dateneinheiten</span><span class="sxs-lookup"><span data-stu-id="846da-160">Data entities involved in the process</span></span>

- <span data-ttu-id="846da-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="846da-161">RetailTransactionTable</span></span>
- <span data-ttu-id="846da-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="846da-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="846da-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="846da-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="846da-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="846da-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="846da-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="846da-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="846da-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="846da-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="846da-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="846da-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="846da-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="846da-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="846da-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="846da-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="846da-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="846da-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="846da-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="846da-171">RetailTransactionAttributeTrans</span></span>
