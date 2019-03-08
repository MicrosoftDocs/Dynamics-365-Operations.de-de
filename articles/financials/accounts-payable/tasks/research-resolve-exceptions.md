---
title: Ausnahmen untersuchen/auflösen
description: Kreditorenrechnungsrichtlinien werden ausgeführt, wenn Sie mit der Seite "Kreditorenrechnung" eine Kreditorenrechnung buchen und wenn Sie die Seite "Richtlinienverstöße" der Kreditorenrechnung öffnen.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c6f8c8dcf7a301c7fb2d095658ac96cd4a24dff
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "365154"
---
# <a name="researchresolve-exceptions"></a><span data-ttu-id="ffacf-103">Ausnahmen untersuchen/auflösen</span><span class="sxs-lookup"><span data-stu-id="ffacf-103">Research/Resolve exceptions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ffacf-104">Kreditorenrechnungsrichtlinien werden ausgeführt, wenn Sie mit der Seite "Kreditorenrechnung" eine Kreditorenrechnung buchen und wenn Sie die Seite "Richtlinienverstöße" der Kreditorenrechnung öffnen.</span><span class="sxs-lookup"><span data-stu-id="ffacf-104">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="ffacf-105">Sie können auch den Workflow für Kreditorenrechnungen konfigurieren, sodass Kreditorenrechnungsrichtlinien immer ausgeführt werden, wenn eine Rechnung an den Workflow übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="ffacf-105">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

<span data-ttu-id="ffacf-106">Kreditorenrechnungsrichtlinien werden nicht auf Rechnungen angewendet, die im Rechnungsbuch oder in einer Rechnungserfassung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ffacf-106">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span> 

<span data-ttu-id="ffacf-107">Für die Rechnungsabgleichüberprüfung werden keine Kreditorenrechnungsrichtlinien verwendet. Stattdessen wird die Prüfung auf der Seite "Kreditorenkontenparameter" eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="ffacf-107">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>

<span data-ttu-id="ffacf-108">Für diese Erfassung wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="ffacf-108">This recording uses the USMF demo company.</span></span> <span data-ttu-id="ffacf-109">Die Kreditorenleiter- oder Buchhaltungsleiterrolle würde diese Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="ffacf-109">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="ffacf-110">Stellen Sie zu Beginn sicher, dass der Konfigurationsschlüssel "Rechnungsabgleich" ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="ffacf-110">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="ffacf-111">Vorbereitung zum Erstellen von Kreditorenrechnungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="ffacf-111">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="ffacf-112">Wechseln Sie zu Kreditoren > Einstellung > Kreditorenparameter.</span><span class="sxs-lookup"><span data-stu-id="ffacf-112">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="ffacf-113">Klicken Sie auf die Registerkarte "Rechnungsprüfung".</span><span class="sxs-lookup"><span data-stu-id="ffacf-113">Click the Invoice validation tab.</span></span>
3. <span data-ttu-id="ffacf-114">Aktivieren oder deaktivieren Sie das Kontrollkästchen "Rechnungskopfstatus automatisch aktualisieren".</span><span class="sxs-lookup"><span data-stu-id="ffacf-114">Select or clear the Automatically update invoice header status check box.</span></span>
4. <span data-ttu-id="ffacf-115">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ffacf-115">Click OK.</span></span>
5. <span data-ttu-id="ffacf-116">Wählen Sie im Feld "Rechnung mit Abweichungen buchen" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="ffacf-116">In the Post invoice with discrepancies field, select an option.</span></span>
6. <span data-ttu-id="ffacf-117">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ffacf-117">Close the page.</span></span>
7. <span data-ttu-id="ffacf-118">Wechseln Sie zu "Kreditoren" > "Richtlinieneinstellung" > "Kreditorenrechnungsrichtlinien".</span><span class="sxs-lookup"><span data-stu-id="ffacf-118">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
8. <span data-ttu-id="ffacf-119">Klicken Sie auf "Parameter".</span><span class="sxs-lookup"><span data-stu-id="ffacf-119">Click Parameters.</span></span>
9. <span data-ttu-id="ffacf-120">Klicken Sie auf die Schaltfläche "Hinzufügen."</span><span class="sxs-lookup"><span data-stu-id="ffacf-120">Click btnAdd.</span></span>
10. <span data-ttu-id="ffacf-121">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ffacf-121">Close the page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="ffacf-122">Erstellen von Richtlinienregeltypen für Kreditorenrechnungen</span><span class="sxs-lookup"><span data-stu-id="ffacf-122">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="ffacf-123">Wechseln Sie zu "Kreditoren" > "Richtlinieneinstellung" > "Kreditorenrechnungs-Richtlinienregeltypen".</span><span class="sxs-lookup"><span data-stu-id="ffacf-123">Go to Accounts payable > Policy setup > Vendor invoice policy rule types.</span></span>
2. <span data-ttu-id="ffacf-124">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="ffacf-124">Click New.</span></span>
3. <span data-ttu-id="ffacf-125">Geben Sie im Feld "Regelname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ffacf-125">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="ffacf-126">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ffacf-126">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ffacf-127">Klicken Sie im Feld "Abfragename" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ffacf-127">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ffacf-128">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="ffacf-128">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ffacf-129">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="ffacf-129">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ffacf-130">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ffacf-130">Click Save.</span></span>
9. <span data-ttu-id="ffacf-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ffacf-131">Close the page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="ffacf-132">Definieren einer Kreditorenrechnungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="ffacf-132">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="ffacf-133">Wechseln Sie zu "Kreditoren" > "Richtlinieneinstellung" > "Kreditorenrechnungsrichtlinien".</span><span class="sxs-lookup"><span data-stu-id="ffacf-133">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
2. <span data-ttu-id="ffacf-134">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="ffacf-134">Click New.</span></span>
3. <span data-ttu-id="ffacf-135">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ffacf-135">In the Name field, type a value.</span></span>
4. <span data-ttu-id="ffacf-136">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ffacf-136">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ffacf-137">Erweitern oder reduzieren Sie den Abschnitt "Richtlinienorganisationen".</span><span class="sxs-lookup"><span data-stu-id="ffacf-137">Expand or collapse the Policy organizations section.</span></span>
6. <span data-ttu-id="ffacf-138">Wählen Sie in der Struktur "Contoso Unterhaltungsanlagen USA" aus.</span><span class="sxs-lookup"><span data-stu-id="ffacf-138">In the tree, select 'Contoso Entertainment System USA'.</span></span>
7. <span data-ttu-id="ffacf-139">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ffacf-139">Click Add.</span></span>
8. <span data-ttu-id="ffacf-140">Erweitern oder reduzieren Sie den Abschnitt "Richtlinienregeln".</span><span class="sxs-lookup"><span data-stu-id="ffacf-140">Expand or collapse the Policy rules section.</span></span>
9. <span data-ttu-id="ffacf-141">Klicken Sie auf "Richtlinienregel erstellen".</span><span class="sxs-lookup"><span data-stu-id="ffacf-141">Click Create policy rule.</span></span>
10. <span data-ttu-id="ffacf-142">Geben Sie im Feld "Richtlinienregel" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ffacf-142">In the Policy rule description field, type a value.</span></span>
11. <span data-ttu-id="ffacf-143">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="ffacf-143">Click Filter.</span></span>
12. <span data-ttu-id="ffacf-144">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ffacf-144">Click Add.</span></span>
13. <span data-ttu-id="ffacf-145">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="ffacf-145">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="ffacf-146">Klicken Sie im Feld "Tabelle" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ffacf-146">In the Table field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="ffacf-147">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="ffacf-147">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="ffacf-148">Klicken Sie im Feld "Abgeleitete Tabelle" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ffacf-148">In the Derived table field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="ffacf-149">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="ffacf-149">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="ffacf-150">Klicken Sie im Feld "Feld" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ffacf-150">In the Field field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="ffacf-151">Geben Sie im Feld "Feld" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ffacf-151">In the Field field, type a value.</span></span>
20. <span data-ttu-id="ffacf-152">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ffacf-152">Close the page.</span></span>
21. <span data-ttu-id="ffacf-153">Geben Sie im Feld "Kriterien" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ffacf-153">In the Criteria field, type a value.</span></span>
22. <span data-ttu-id="ffacf-154">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ffacf-154">Click OK.</span></span>
23. <span data-ttu-id="ffacf-155">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ffacf-155">Click OK.</span></span>
24. <span data-ttu-id="ffacf-156">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ffacf-156">Close the page.</span></span>
25. <span data-ttu-id="ffacf-157">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ffacf-157">Close the page.</span></span>

