--- 
title: "EU-Gelangensbestätigung ausstellen"
description: "Diese Prozedur läuft Sie durch das Aktivieren einer EU-Eintragsbescheinigung nach und konfiguriert ein Debitorenkonto, um Eintragsbescheinigungen zu verwenden und eine Bescheinigung auszustellen."
author: mrolecki
manager: AnnBe
ms.date: 02/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ff00ff0df3835ee2cbf21219ad6f07bfeba6e7ac
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="issue-an-eu-entry-certificate"></a><span data-ttu-id="632e1-103">EU-Gelangensbestätigung ausstellen</span><span class="sxs-lookup"><span data-stu-id="632e1-103">Issue an EU entry certificate</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="632e1-104">Diese Prozedur läuft Sie durch das Aktivieren einer EU-Eintragsbescheinigung nach und konfiguriert ein Debitorenkonto, um Eintragsbescheinigungen zu verwenden und eine Bescheinigung auszustellen.</span><span class="sxs-lookup"><span data-stu-id="632e1-104">This procedure walks you through enabling an EU entry certificate, configuring a customer account to use entry certificates and issue a certificate.</span></span> <span data-ttu-id="632e1-105">Diese Prozedur wurde mit dem Demodatenunternehmen DEMF erstellt.</span><span class="sxs-lookup"><span data-stu-id="632e1-105">This procedure was created using the demo data company DEMF.</span></span>


## <a name="enable-entry-certificate-management"></a><span data-ttu-id="632e1-106">Verwaltung der Gelangensbestätigung aktivieren</span><span class="sxs-lookup"><span data-stu-id="632e1-106">Enable entry certificate management</span></span>
1. <span data-ttu-id="632e1-107">Wechseln Sie zu "Kreditoren" > "Einstellung" > "Kreditorenparameter".</span><span class="sxs-lookup"><span data-stu-id="632e1-107">Go to Accounts receivable > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="632e1-108">Klicken Sie auf die Registerkarte ''.</span><span class="sxs-lookup"><span data-stu-id="632e1-108">Click the Shipments tab.</span></span>
3. <span data-ttu-id="632e1-109">Erweitern Sie den Eintragsbescheinigungsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="632e1-109">Expand the Entry certificate section.</span></span>
4. <span data-ttu-id="632e1-110">Aktivieren Sie dieses Kontrollkästchen, um die Verwaltung der Gelangensbestätigung zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="632e1-110">Select Yes in the Enable entry certificate management field.</span></span>
5. <span data-ttu-id="632e1-111">Aktivieren Sie dieses Kontrollkästchen, um die Verwaltung der Gelangensbestätigung zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="632e1-111">Select Yes in the Enable entry certificate issuing field.</span></span>
6. <span data-ttu-id="632e1-112">Klicken Sie auf die Registerkarte "Nummernkreis".</span><span class="sxs-lookup"><span data-stu-id="632e1-112">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="632e1-113">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="632e1-113">In the list, find and select Entry certificate row.</span></span>
8. <span data-ttu-id="632e1-114">Geben Sie im Feld "Ursprüngliche Rechnungsnummer" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="632e1-114">In the Number sequence code field, enter or select a value.</span></span>

## <a name="set-up-a-customer"></a><span data-ttu-id="632e1-115">Einrichten einer Debitorenvorauszahlung</span><span class="sxs-lookup"><span data-stu-id="632e1-115">Set up a customer</span></span>
1. <span data-ttu-id="632e1-116">Wechseln Sie zu "Debitoren" > "Debitoren" > "Alle Debitoren".</span><span class="sxs-lookup"><span data-stu-id="632e1-116">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="632e1-117">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="632e1-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="632e1-118">Filtern Sie beispielsweise im Feld "Konto" mit dem Wert "DE-015".</span><span class="sxs-lookup"><span data-stu-id="632e1-118">For example, filter on the Account field with a value of 'DE-015'.</span></span>
3. <span data-ttu-id="632e1-119">Die Details des Debitorenkontos öffnen.</span><span class="sxs-lookup"><span data-stu-id="632e1-119">Open customer account details.</span></span>
4. <span data-ttu-id="632e1-120">Klicken Sie auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="632e1-120">Click Edit.</span></span>
5. <span data-ttu-id="632e1-121">Erweitern Sie den Rechnungs- und Lieferungsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="632e1-121">Expand the Invoice and delivery section.</span></span>
6. <span data-ttu-id="632e1-122">Aktivieren Sie dieses Kontrollkästchen, um die Verwaltung der Gelangensbestätigung zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="632e1-122">Select Yes in the Entry certificate required field.</span></span>
7. <span data-ttu-id="632e1-123">Aktivieren Sie dieses Kontrollkästchen, um die Verwaltung der Gelangensbestätigung zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="632e1-123">Select Yes in the Issue entry certificate field.</span></span>
8. <span data-ttu-id="632e1-124">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="632e1-124">Click Save.</span></span>

## <a name="create-an-eu-entry-certificate-automatically"></a><span data-ttu-id="632e1-125">Erhalt einer EU-Gelangensbestätigung</span><span class="sxs-lookup"><span data-stu-id="632e1-125">Create an EU entry certificate automatically</span></span>
1. <span data-ttu-id="632e1-126">Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="632e1-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="632e1-127">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="632e1-127">Click New.</span></span>
3. <span data-ttu-id="632e1-128">Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="632e1-128">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="632e1-129">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="632e1-129">Click OK.</span></span>
5. <span data-ttu-id="632e1-130">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="632e1-130">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="632e1-131">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="632e1-131">Click Save.</span></span>
7. <span data-ttu-id="632e1-132">Klicken Sie im Aktivitätsbereich auf "Entnehmen und verpacken".</span><span class="sxs-lookup"><span data-stu-id="632e1-132">On the Action Pane, click Pick and pack.</span></span>
8. <span data-ttu-id="632e1-133">Klicken Sie auf "Lieferschein buchen".</span><span class="sxs-lookup"><span data-stu-id="632e1-133">Click Post packing slip.</span></span>
9. <span data-ttu-id="632e1-134">Erweitern Sie den Abschnitt "Parameter".</span><span class="sxs-lookup"><span data-stu-id="632e1-134">Expand the Parameters section.</span></span>
10. <span data-ttu-id="632e1-135">Wählen Sie im Feld "Menge" die Option "Alle" aus.</span><span class="sxs-lookup"><span data-stu-id="632e1-135">In the Quantity field, select 'All'.</span></span>
11. <span data-ttu-id="632e1-136">Aktivieren Sie dieses Kontrollkästchen, um Gelangensbestätigungen auszustellen</span><span class="sxs-lookup"><span data-stu-id="632e1-136">Clear the Issue entry certificate check box.</span></span>
    * <span data-ttu-id="632e1-137">Eine Eintragsbescheinigung kann während der Lieferscheinbuchung oder während der Auftragsrechnungsstellung ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="632e1-137">An entry certificate can be issued during packing slip posting or during order invoicing.</span></span> <span data-ttu-id="632e1-138">Verlassen Sie das Abgangseintrags-Bescheinigungskontrollkästchen deaktiviert, um ihn später auszugeben.</span><span class="sxs-lookup"><span data-stu-id="632e1-138">Leave the Issue entry certificate checkbox unchecked to issue it later.</span></span>  
12. <span data-ttu-id="632e1-139">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="632e1-139">Click OK.</span></span>
13. <span data-ttu-id="632e1-140">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="632e1-140">Click OK.</span></span>
14. <span data-ttu-id="632e1-141">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="632e1-141">On the Action Pane, click Invoice.</span></span>
15. <span data-ttu-id="632e1-142">Klicken Sie auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="632e1-142">Click Invoice.</span></span>
    * <span data-ttu-id="632e1-143">Überprüfen Sie, ob die Eintragsbescheinigung Buchungszeitpunkt und Abgangseintrags-Bescheinigungskontrollkästchen im Überblicksabschnitt markiert sind.</span><span class="sxs-lookup"><span data-stu-id="632e1-143">Verify that the Entry certificate required and Issue entry certificate checkboxes in the Overview section are marked.</span></span>  <span data-ttu-id="632e1-144">Sie können das Druckseintrags-Bescheinigungskontrollkästchen auch auswählen, um das Drucken der Bescheinigung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="632e1-144">You can also select the Print entry certificate check box to allow printing of the certificate.</span></span>  
16. <span data-ttu-id="632e1-145">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="632e1-145">Click OK.</span></span>
17. <span data-ttu-id="632e1-146">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="632e1-146">Click OK.</span></span>
18. <span data-ttu-id="632e1-147">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="632e1-147">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="632e1-148">Klicken Sie auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="632e1-148">Click Invoice.</span></span>
20. <span data-ttu-id="632e1-149">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="632e1-149">On the Action Pane, click Invoice.</span></span>
21. <span data-ttu-id="632e1-150">Ausgestellte Gelangensbestätigungen anzeigen</span><span class="sxs-lookup"><span data-stu-id="632e1-150">Click View issued entry certificates.</span></span>
22. <span data-ttu-id="632e1-151">Klicken Sie auf Drucken.</span><span class="sxs-lookup"><span data-stu-id="632e1-151">Click Print.</span></span>
23. <span data-ttu-id="632e1-152">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="632e1-152">Close the page.</span></span>
24. <span data-ttu-id="632e1-153">Klicken Sie auf "Status ändern".</span><span class="sxs-lookup"><span data-stu-id="632e1-153">Click Change status.</span></span>
25. <span data-ttu-id="632e1-154">Wählen Sie im Feld Status eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="632e1-154">In the New status field, select an option.</span></span>
26. <span data-ttu-id="632e1-155">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="632e1-155">Click OK.</span></span>
27. <span data-ttu-id="632e1-156">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="632e1-156">Close the page.</span></span>

## <a name="create-an-eu-entry-certificate-manually"></a><span data-ttu-id="632e1-157">Erhalt einer EU-Gelangensbestätigung</span><span class="sxs-lookup"><span data-stu-id="632e1-157">Create an EU entry certificate manually</span></span>
1. <span data-ttu-id="632e1-158">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="632e1-158">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="632e1-159">Gelangensbestätigung erstellen</span><span class="sxs-lookup"><span data-stu-id="632e1-159">Click Create entry certificate.</span></span>
3. <span data-ttu-id="632e1-160">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="632e1-160">Click OK.</span></span>
4. <span data-ttu-id="632e1-161">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="632e1-161">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="632e1-162">Ausgestellte Gelangensbestätigungen anzeigen</span><span class="sxs-lookup"><span data-stu-id="632e1-162">Click View issued entry certificates.</span></span>


