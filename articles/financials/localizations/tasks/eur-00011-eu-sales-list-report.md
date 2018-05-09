--- 
title: Bericht 'Zusammenfassende Meldung' generieren
description: "Diese Prozedur führt Sie durch das Generieren eines Berichts für zusammenfassende Meldungen."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 082a94fe3cab2cbdf7698683dec0da88f8554b6d
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---
# <a name="generate-an-eu-sales-list-report"></a><span data-ttu-id="1bbfc-103">Bericht 'Zusammenfassende Meldung' generieren</span><span class="sxs-lookup"><span data-stu-id="1bbfc-103">Generate an EU sales list report</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1bbfc-104">Diese Prozedur führt Sie durch das Generieren eines Berichts für zusammenfassende Meldungen.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-104">This procedure walks you through generating the EU sales list report.</span></span> <span data-ttu-id="1bbfc-105">Hierzu zählen das Übertragen von innergemeinschaftlichen Handelsbuchungen zur zusammenfassenden Meldung und das Ausführen des Berichts.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-105">This includes transferring intra-community trade transactions to the EU sales list and running the report.</span></span> <span data-ttu-id="1bbfc-106">Diese Prozedur umfasst auch das Erstellen einer innergemeinschaftlichen Handelsbuchung zu Demonstrationszwecken.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-106">This  procedure also includes creating an intra-community trade transaction for demo purposes.</span></span> <span data-ttu-id="1bbfc-107">Weitere Informationen über zusammenfassende Meldungen, einschließlich erforderliche Voraussetzungen, finden Sie in der Hilfe von Dynamics 365 for Finance and Operations Help.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-107">For more information about EU Sales list reporting, including required prerequisites, refer to the Dynamics 365 for Finance and Operations Help.</span></span>

<span data-ttu-id="1bbfc-108">Diese Prozedur gilt für alle europäischen Länder/Regionen.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-108">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="1bbfc-109">Die Prozedur wurde mithilfe des Demodatenunternehmens DEMF und somit mit Deutschland als Beispielland erstellt.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-109">The procedure was created using the demo data company DEMF and consequently Germany as an exemplar domestic country/region.</span></span> <span data-ttu-id="1bbfc-110">Die Prozedur verwendet ebenfalls Portugal als Beispielland.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-110">The procedure also uses Portugal as an exemplar EU country/region.</span></span> <span data-ttu-id="1bbfc-111">Bevor Sie dieses Verfahren ausführen können, müssen Sie zusammenfassende Meldungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-111">Before you can complete this procedure, you must configure EU sales list reporting.</span></span>

<span data-ttu-id="1bbfc-112">Diese Prozedur ist für Buchhalter vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-112">This procedure is intended for accountants.</span></span>


## <a name="create-an-intra-community-sales-transaction-for-demo-purposes"></a><span data-ttu-id="1bbfc-113">Erstellen einer innergemeinschaftlichen Verkaufsbuchung für Demonstrationszwecke</span><span class="sxs-lookup"><span data-stu-id="1bbfc-113">Create an intra-community sales transaction for demo purposes</span></span>
1. <span data-ttu-id="1bbfc-114">Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="1bbfc-114">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="1bbfc-115">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="1bbfc-115">Click New.</span></span>
3. <span data-ttu-id="1bbfc-116">Geben Sie im Feld "Debitorenkonto" den Wert 'PRT-001' ein.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-116">In the Customer account field, type 'PRT-001'.</span></span>
4. <span data-ttu-id="1bbfc-117">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1bbfc-117">Click OK.</span></span>
5. <span data-ttu-id="1bbfc-118">Geben Sie im Feld "Artikelnummer" die Zeichenfolge "D0001" ein.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-118">In the Item number field, type 'D0001'.</span></span>
6. <span data-ttu-id="1bbfc-119">Erweitern Sie den Abschnitt "Positionsdetails".</span><span class="sxs-lookup"><span data-stu-id="1bbfc-119">Expand the Line details section.</span></span>
7. <span data-ttu-id="1bbfc-120">Klicken Sie auf die Registerkarte Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-120">Click the Setup tab.</span></span>
8. <span data-ttu-id="1bbfc-121">Geben Sie im Feld "Artikel-Mehrwertsteuergruppe" einen Wert "Voll" ein.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-121">In the Item sales tax group field, type 'FULL'.</span></span>
9. <span data-ttu-id="1bbfc-122">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="1bbfc-122">Click Add line.</span></span>
10. <span data-ttu-id="1bbfc-123">Geben Sie im Feld "Artikelnummer" die Zeichenfolge "D0003" ein.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-123">In the Item number field, type 'D0003'.</span></span>
11. <span data-ttu-id="1bbfc-124">Geben Sie im Feld "Artikel-Mehrwertsteuergruppe" einen Wert "ROT" ein.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-124">In the Item sales tax group field, type 'RED'.</span></span>
12. <span data-ttu-id="1bbfc-125">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="1bbfc-125">Click Save.</span></span>
13. <span data-ttu-id="1bbfc-126">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="1bbfc-126">On the Action Pane, click Invoice.</span></span>
14. <span data-ttu-id="1bbfc-127">Klicken Sie auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="1bbfc-127">Click Invoice.</span></span>
15. <span data-ttu-id="1bbfc-128">Erweitern Sie den Abschnitt "Parameter".</span><span class="sxs-lookup"><span data-stu-id="1bbfc-128">Expand the Parameters section.</span></span>
16. <span data-ttu-id="1bbfc-129">Wählen Sie im Feld "Menge" die Option "Alle" aus.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-129">In the Quantity field, select 'All'.</span></span>
17. <span data-ttu-id="1bbfc-130">Erweitern Sie den Abschnitt 'Einstellungen'.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-130">Expand the Setup section.</span></span>
18. <span data-ttu-id="1bbfc-131">Legen Sie im Feld "Rechnungsdatum" das Datum "11.01.2016" fest.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-131">In the Invoice date field, set the date to '01/11/2016'.</span></span>
19. <span data-ttu-id="1bbfc-132">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1bbfc-132">Click OK.</span></span>
20. <span data-ttu-id="1bbfc-133">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1bbfc-133">Click OK.</span></span>

## <a name="transfer-intra-community-trade-transactions-to-the-eu-sales-list"></a><span data-ttu-id="1bbfc-134">Übertragen von innergemeinschaftlichen Verkaufsbuchungen zur zusammenfassenden Meldung</span><span class="sxs-lookup"><span data-stu-id="1bbfc-134">Transfer intra-community trade transactions to the EU sales list</span></span>
1. <span data-ttu-id="1bbfc-135">Wechseln Sie zu "Steuer" > "Meldungen" > "Außenhandel" > "Zusammenfassende Meldung".</span><span class="sxs-lookup"><span data-stu-id="1bbfc-135">Go to Tax > Declarations > Foreign trade > EU sales list.</span></span>
2. <span data-ttu-id="1bbfc-136">Klicken Sie auf Übertragen.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-136">Click Transfer.</span></span>
3. <span data-ttu-id="1bbfc-137">Wählen Sie "Ja" im Feld "Artikel", um Artikelbuchungen zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-137">Select Yes in the Item field to transfer item transactions.</span></span>
4. <span data-ttu-id="1bbfc-138">Wählen Sie "Ja" im Feld "Leistung", um Leistungsbuchungen zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-138">Select Yes in the Service field to transfer service transactions.</span></span>
    * <span data-ttu-id="1bbfc-139">Sie können zusätzliche Filter auf zu übertragende innergemeinschaftliche Handelsbuchung anwenden.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-139">You can also specify additional filters on intra-community trade transactions to transfer.</span></span>  
5. <span data-ttu-id="1bbfc-140">Klicken Sie auf Übertragen.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-140">Click Transfer.</span></span>
    * <span data-ttu-id="1bbfc-141">Überprüfen Sie, ob die innergemeinschaftlichen Handelsbuchung erfolgreich in die zusammenfassende Meldung übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-141">Verify that the intra-community sales transaction is successfully transferred to the EU sales list.</span></span>  

## <a name="generate-the-eu-sales-list-report"></a><span data-ttu-id="1bbfc-142">Erstellen des Berichts für die zusammenfassende Meldung</span><span class="sxs-lookup"><span data-stu-id="1bbfc-142">Generate the EU sales list report</span></span>
1. <span data-ttu-id="1bbfc-143">Klicken Sie auf "Berichterstellung".</span><span class="sxs-lookup"><span data-stu-id="1bbfc-143">Click Reporting.</span></span>
2. <span data-ttu-id="1bbfc-144">Wählen Sie im Feld "Berichtszeitraum" "Monatlich" aus.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-144">In the Reporting period field, select 'Monthly'.</span></span>
3. <span data-ttu-id="1bbfc-145">Legen Sie das Von-Datum auf "01.01.2016" fest.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-145">In the From date field, set the date to '01/01/2016'.</span></span>
4. <span data-ttu-id="1bbfc-146">Wählen Sie "Ja" im Feld "Datei generieren" aus.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-146">Select Yes in the Generate file field.</span></span>
5. <span data-ttu-id="1bbfc-147">Wählen Sie "Ja" im Feld "Bericht erzeugen" aus.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-147">Select Yes in the Generate report field.</span></span>
6. <span data-ttu-id="1bbfc-148">Geben Sie im Feld "Dateiname" "EUSalesList" ein.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-148">In the File name field, type 'EUSalesList'.</span></span>
7. <span data-ttu-id="1bbfc-149">Geben Sie im Feld "Berichtdatei" "EUSalesList" ein.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-149">In the Report file name field, type 'EUSalesList'.</span></span>
8. <span data-ttu-id="1bbfc-150">Geben Sie im Feld "Registrierungs-ID Zusammenfassende Meldung" "123" ein.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-150">In the EU Sales List Registration ID field, type '123'.</span></span>
    * <span data-ttu-id="1bbfc-151">Dieses Feld ist für Deutschland verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-151">This field is only available for Germany.</span></span>  
    * <span data-ttu-id="1bbfc-152">Sie können zusätzliche Filter auf die im Bericht angezeigte innergemeinschaftliche Handelsbuchung anwenden.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-152">You can also specify additional filters on intra-community trade transactions to include in the report.</span></span>  
9. <span data-ttu-id="1bbfc-153">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1bbfc-153">Click OK.</span></span>
    * <span data-ttu-id="1bbfc-154">Überprüfen Sie, ob Popupfenster für das Herunterladen der die Datei und des Kontrollberichts erscheinen.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-154">Verify that pop-up windows appear to confirm that the file and the control report are being downloaded.</span></span>  

## <a name="mark-eu-sales-list-lines-as-reported"></a><span data-ttu-id="1bbfc-155">Markieren der zusammenfassenden Meldung als "Berichtet"</span><span class="sxs-lookup"><span data-stu-id="1bbfc-155">Mark EU sales list lines as Reported</span></span>
1. <span data-ttu-id="1bbfc-156">Klicken Sie auf "Markieren".</span><span class="sxs-lookup"><span data-stu-id="1bbfc-156">Click Mark.</span></span>
2. <span data-ttu-id="1bbfc-157">Klicken Sie auf "Als berichtet markieren".</span><span class="sxs-lookup"><span data-stu-id="1bbfc-157">Click Mark as reported.</span></span>
3. <span data-ttu-id="1bbfc-158">In der Liste wählen Sie die Zeile für das Feld "Rechnungsdatum" aus.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-158">In the list, select the row for the Invoice date field.</span></span>
4. <span data-ttu-id="1bbfc-159">Geben Sie im Feld "Kriterien" den Wert "01.01.2016..31.01.2016" ein.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-159">In the Criteria field, type '01/01/2016..01/31/2016'.</span></span>
5. <span data-ttu-id="1bbfc-160">In der Liste wählen Sie die Zeile für das Feld "Berichtsstatus" aus.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-160">In the list, select the row for the Reporting status field.</span></span>
6. <span data-ttu-id="1bbfc-161">Wählen Sie im Feld "Kriterien" den Wert "Enthalten" aus.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-161">In the Criteria field, select 'Included'.</span></span>
    * <span data-ttu-id="1bbfc-162">Sie können zusätzliche Filter auf die als "Berichtet" angezeigten innergemeinschaftlichen Handelsbuchungen anwenden.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-162">You can also specify additional filters on intra-community trade transactions to mark as Reported.</span></span>  
7. <span data-ttu-id="1bbfc-163">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1bbfc-163">Click OK.</span></span>
8. <span data-ttu-id="1bbfc-164">Wählen Sie im Feld "Abschnitt" "Berichtet" aus.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-164">In the Selection field, select 'Reported'.</span></span>

## <a name="mark-eu-sales-list-lines-as-closed"></a><span data-ttu-id="1bbfc-165">Markieren der zusammenfassenden Meldung als "Abgeschlossen"</span><span class="sxs-lookup"><span data-stu-id="1bbfc-165">Mark EU sales list lines as Closed</span></span>
1. <span data-ttu-id="1bbfc-166">Klicken Sie auf "Markieren".</span><span class="sxs-lookup"><span data-stu-id="1bbfc-166">Click Mark.</span></span>
2. <span data-ttu-id="1bbfc-167">Klicken Sie auf "Als geschlossen markieren".</span><span class="sxs-lookup"><span data-stu-id="1bbfc-167">Click Mark as closed.</span></span>
3. <span data-ttu-id="1bbfc-168">In der Liste markieren Sie die Zeile für das Feld "Rechnungsdatum" aus.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-168">In the list, mark the row for the Invoice date field.</span></span>
4. <span data-ttu-id="1bbfc-169">Geben Sie im Feld "Kriterien" den Wert "01.01.2016..31.01.2016" ein.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-169">In the Criteria field, type '01/01/2016..01/31/2016'.</span></span>
5. <span data-ttu-id="1bbfc-170">In der Liste markieren Sie die Zeile für das Feld "Berichtstatus" aus.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-170">In the list, mark the row for the Reporting status field.</span></span>
6. <span data-ttu-id="1bbfc-171">Wählen Sie im Feld "Kriterien" den Wert "Berichtet" aus.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-171">In the Criteria field, select ‘Reported’.</span></span>
    * <span data-ttu-id="1bbfc-172">Sie können zusätzliche Filter auf als "Abgeschlossen" markieren innergemeinschaftlichen Handelsbuchungn anwenden.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-172">You can also specify additional filters on intra-community trade transactions to mark as Closed.</span></span>  
7. <span data-ttu-id="1bbfc-173">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1bbfc-173">Click OK.</span></span>
8. <span data-ttu-id="1bbfc-174">Wählen Sie im Feld "Abschnitt" "Abgeschlossen" aus.</span><span class="sxs-lookup"><span data-stu-id="1bbfc-174">In the Selection field, select 'Closed'.</span></span>


