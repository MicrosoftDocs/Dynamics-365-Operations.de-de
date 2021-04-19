---
title: EUR-00012 Ausstellen einer EU-Gelangensbestätigung
description: Diese Prozedur läuft Sie durch das Aktivieren einer EU-Eintragsbescheinigung nach und konfiguriert ein Debitorenkonto, um Eintragsbescheinigungen zu verwenden und eine Bescheinigung auszustellen.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters, CustTable, SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CustEntryCertificateJour_W, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 98a6566d37e77415e01c38055dc16aec35c5ce7e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821817"
---
# <a name="eur-00012-issue-an-eu-entry-certificate"></a><span data-ttu-id="7c3e4-103">EUR-00012 Ausstellen einer EU-Gelangensbestätigung</span><span class="sxs-lookup"><span data-stu-id="7c3e4-103">EUR-00012 Issue an EU entry certificate</span></span>

[!include [banner](../../includes/banner.md)]
<span data-ttu-id="7c3e4-104">Diese Prozedur läuft Sie durch das Aktivieren einer EU-Eintragsbescheinigung nach und konfiguriert ein Debitorenkonto, um Eintragsbescheinigungen zu verwenden und eine Bescheinigung auszustellen.</span><span class="sxs-lookup"><span data-stu-id="7c3e4-104">This procedure walks you through enabling an EU entry certificate, configuring a customer account to use entry certificates and issue a certificate.</span></span> <span data-ttu-id="7c3e4-105">Diese Prozedur wurde mit dem Demodatenunternehmen DEMF erstellt.</span><span class="sxs-lookup"><span data-stu-id="7c3e4-105">This procedure was created using the demo data company DEMF.</span></span>


## <a name="enable-entry-certificate-management"></a><span data-ttu-id="7c3e4-106">Verwaltung der Gelangensbestätigung aktivieren</span><span class="sxs-lookup"><span data-stu-id="7c3e4-106">Enable entry certificate management</span></span>
1. <span data-ttu-id="7c3e4-107">Wechseln Sie zu "Kreditoren" > "Einstellung" > "Kreditorenparameter".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-107">Go to Accounts receivable > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="7c3e4-108">Klicken Sie auf die Registerkarte ''.</span><span class="sxs-lookup"><span data-stu-id="7c3e4-108">Click the Shipments tab.</span></span>
3. <span data-ttu-id="7c3e4-109">Erweitern Sie den Eintragsbescheinigungsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="7c3e4-109">Expand the Entry certificate section.</span></span>
4. <span data-ttu-id="7c3e4-110">Aktivieren Sie dieses Kontrollkästchen, um die Verwaltung der Gelangensbestätigung zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="7c3e4-110">Select Yes in the Enable entry certificate management field.</span></span>
5. <span data-ttu-id="7c3e4-111">Aktivieren Sie dieses Kontrollkästchen, um die Verwaltung der Gelangensbestätigung zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="7c3e4-111">Select Yes in the Enable entry certificate issuing field.</span></span>
6. <span data-ttu-id="7c3e4-112">Klicken Sie auf die Registerkarte "Nummernkreis".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-112">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="7c3e4-113">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="7c3e4-113">In the list, find and select Entry certificate row.</span></span>
8. <span data-ttu-id="7c3e4-114">Geben Sie im Feld "Ursprüngliche Rechnungsnummer" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7c3e4-114">In the Number sequence code field, enter or select a value.</span></span>

## <a name="set-up-a-customer"></a><span data-ttu-id="7c3e4-115">Einrichten einer Debitorenvorauszahlung</span><span class="sxs-lookup"><span data-stu-id="7c3e4-115">Set up a customer</span></span>
1. <span data-ttu-id="7c3e4-116">Wechseln Sie zu "Debitoren" > "Debitoren" > "Alle Debitoren".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-116">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="7c3e4-117">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="7c3e4-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="7c3e4-118">Filtern Sie beispielsweise im Feld "Konto" mit dem Wert "DE-015".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-118">For example, filter on the Account field with a value of 'DE-015'.</span></span>
3. <span data-ttu-id="7c3e4-119">Die Details des Debitorenkontos öffnen.</span><span class="sxs-lookup"><span data-stu-id="7c3e4-119">Open customer account details.</span></span>
4. <span data-ttu-id="7c3e4-120">Klicken Sie auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="7c3e4-120">Click Edit.</span></span>
5. <span data-ttu-id="7c3e4-121">Erweitern Sie den Rechnungs- und Lieferungsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="7c3e4-121">Expand the Invoice and delivery section.</span></span>
6. <span data-ttu-id="7c3e4-122">Aktivieren Sie dieses Kontrollkästchen, um die Verwaltung der Gelangensbestätigung zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="7c3e4-122">Select Yes in the Entry certificate required field.</span></span>
7. <span data-ttu-id="7c3e4-123">Aktivieren Sie dieses Kontrollkästchen, um die Verwaltung der Gelangensbestätigung zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="7c3e4-123">Select Yes in the Issue entry certificate field.</span></span>
8. <span data-ttu-id="7c3e4-124">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-124">Click Save.</span></span>

## <a name="create-an-eu-entry-certificate-automatically"></a><span data-ttu-id="7c3e4-125">Erhalt einer EU-Gelangensbestätigung</span><span class="sxs-lookup"><span data-stu-id="7c3e4-125">Create an EU entry certificate automatically</span></span>
1. <span data-ttu-id="7c3e4-126">Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="7c3e4-127">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-127">Click New.</span></span>
3. <span data-ttu-id="7c3e4-128">Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7c3e4-128">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="7c3e4-129">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-129">Click OK.</span></span>
5. <span data-ttu-id="7c3e4-130">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7c3e4-130">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="7c3e4-131">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-131">Click Save.</span></span>
7. <span data-ttu-id="7c3e4-132">Klicken Sie im Aktivitätsbereich auf "Entnehmen und verpacken".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-132">On the Action Pane, click Pick and pack.</span></span>
8. <span data-ttu-id="7c3e4-133">Klicken Sie auf "Lieferschein buchen".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-133">Click Post packing slip.</span></span>
9. <span data-ttu-id="7c3e4-134">Erweitern Sie den Abschnitt "Parameter".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-134">Expand the Parameters section.</span></span>
10. <span data-ttu-id="7c3e4-135">Wählen Sie im Feld "Menge" die Option "Alle" aus.</span><span class="sxs-lookup"><span data-stu-id="7c3e4-135">In the Quantity field, select 'All'.</span></span>
11. <span data-ttu-id="7c3e4-136">Aktivieren Sie dieses Kontrollkästchen, um Gelangensbestätigungen auszustellen</span><span class="sxs-lookup"><span data-stu-id="7c3e4-136">Clear the Issue entry certificate check box.</span></span>
    * <span data-ttu-id="7c3e4-137">Eine Eintragsbescheinigung kann während der Lieferscheinbuchung oder während der Auftragsrechnungsstellung ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7c3e4-137">An entry certificate can be issued during packing slip posting or during order invoicing.</span></span> <span data-ttu-id="7c3e4-138">Verlassen Sie das Abgangseintrags-Bescheinigungskontrollkästchen deaktiviert, um ihn später auszugeben.</span><span class="sxs-lookup"><span data-stu-id="7c3e4-138">Leave the Issue entry certificate checkbox unchecked to issue it later.</span></span>  
12. <span data-ttu-id="7c3e4-139">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-139">Click OK.</span></span>
13. <span data-ttu-id="7c3e4-140">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-140">Click OK.</span></span>
14. <span data-ttu-id="7c3e4-141">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-141">On the Action Pane, click Invoice.</span></span>
15. <span data-ttu-id="7c3e4-142">Klicken Sie auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-142">Click Invoice.</span></span>
    * <span data-ttu-id="7c3e4-143">Überprüfen Sie, ob die Eintragsbescheinigung Buchungszeitpunkt und Abgangseintrags-Bescheinigungskontrollkästchen im Überblicksabschnitt markiert sind.</span><span class="sxs-lookup"><span data-stu-id="7c3e4-143">Verify that the Entry certificate required and Issue entry certificate checkboxes in the Overview section are marked.</span></span>  <span data-ttu-id="7c3e4-144">Sie können das Druckseintrags-Bescheinigungskontrollkästchen auch auswählen, um das Drucken der Bescheinigung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7c3e4-144">You can also select the Print entry certificate check box to allow printing of the certificate.</span></span>  
16. <span data-ttu-id="7c3e4-145">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-145">Click OK.</span></span>
17. <span data-ttu-id="7c3e4-146">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-146">Click OK.</span></span>
18. <span data-ttu-id="7c3e4-147">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-147">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="7c3e4-148">Klicken Sie auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-148">Click Invoice.</span></span>
20. <span data-ttu-id="7c3e4-149">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-149">On the Action Pane, click Invoice.</span></span>
21. <span data-ttu-id="7c3e4-150">Ausgestellte Gelangensbestätigungen anzeigen</span><span class="sxs-lookup"><span data-stu-id="7c3e4-150">Click View issued entry certificates.</span></span>
22. <span data-ttu-id="7c3e4-151">Klicken Sie auf Drucken.</span><span class="sxs-lookup"><span data-stu-id="7c3e4-151">Click Print.</span></span>
23. <span data-ttu-id="7c3e4-152">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="7c3e4-152">Close the page.</span></span>
24. <span data-ttu-id="7c3e4-153">Klicken Sie auf "Status ändern".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-153">Click Change status.</span></span>
25. <span data-ttu-id="7c3e4-154">Wählen Sie im Feld Status eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="7c3e4-154">In the New status field, select an option.</span></span>
26. <span data-ttu-id="7c3e4-155">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-155">Click OK.</span></span>
27. <span data-ttu-id="7c3e4-156">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="7c3e4-156">Close the page.</span></span>

## <a name="create-an-eu-entry-certificate-manually"></a><span data-ttu-id="7c3e4-157">Erhalt einer EU-Gelangensbestätigung</span><span class="sxs-lookup"><span data-stu-id="7c3e4-157">Create an EU entry certificate manually</span></span>
1. <span data-ttu-id="7c3e4-158">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-158">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="7c3e4-159">Gelangensbestätigung erstellen</span><span class="sxs-lookup"><span data-stu-id="7c3e4-159">Click Create entry certificate.</span></span>
3. <span data-ttu-id="7c3e4-160">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-160">Click OK.</span></span>
4. <span data-ttu-id="7c3e4-161">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="7c3e4-161">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="7c3e4-162">Ausgestellte Gelangensbestätigungen anzeigen</span><span class="sxs-lookup"><span data-stu-id="7c3e4-162">Click View issued entry certificates.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]