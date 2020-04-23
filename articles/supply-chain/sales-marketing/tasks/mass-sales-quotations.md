---
title: Massenerstellung von Verkaufsangeboten
description: Diese Verfahren zeigt, wie Sie Angebote, die eine Gruppe von Produkte oder Dienstleistungen enthalten und an mehrere Debitoren gesendet werden sollen, effizient erstellen.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1a9c7235f37ccdedc87ce70d3846443f645c0fe
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211881"
---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="1c8bb-103">Massenerstellung von Verkaufsangeboten</span><span class="sxs-lookup"><span data-stu-id="1c8bb-103">Mass create sales quotations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1c8bb-104">Diese Verfahren zeigt, wie Sie Angebote, die eine Gruppe von Produkte oder Dienstleistungen enthalten und an mehrere Debitoren gesendet werden sollen, effizient erstellen.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="1c8bb-105">Diese Massenangebotserstellung basiert auf Angebotsvorlagen.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="1c8bb-106">Sie können diese Prozedur in Ihrem eigenen Demodatenunternehmen oder in USMF ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="1c8bb-107">Erstellen einer Angebotsvorlage</span><span class="sxs-lookup"><span data-stu-id="1c8bb-107">Create a quotation template</span></span>
1. <span data-ttu-id="1c8bb-108">Wechseln Sie zu Vertrieb und Marketing > Einstellungen > Angebote > Vorlagengruppen.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="1c8bb-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="1c8bb-109">Click New.</span></span>
3. <span data-ttu-id="1c8bb-110">Geben Sie im Feld "Gruppenkennung" eine Kennung Ihrer Wahl ein.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="1c8bb-111">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1c8bb-112">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="1c8bb-112">Click Save.</span></span>
6. <span data-ttu-id="1c8bb-113">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-113">Close the page.</span></span>
7. <span data-ttu-id="1c8bb-114">Wechseln Sie zu "Vertrieb und Marketing" > "Verkaufsangebote" > "Alle Angebote".</span><span class="sxs-lookup"><span data-stu-id="1c8bb-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="1c8bb-115">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="1c8bb-115">Click New.</span></span>
9. <span data-ttu-id="1c8bb-116">Wählen Sie im Feld "Kontotyp" die Option "Debitor" aus.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="1c8bb-117">Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="1c8bb-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1c8bb-118">Click OK.</span></span>
    * <span data-ttu-id="1c8bb-119">Damit ein Angebot eine Vorlage wird, müssen Sie die Einrichtungsschritte im Angebotskopf ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="1c8bb-120">Dies muss ausgeführt werden, bevor Sie Positionen zum Angebot hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="1c8bb-121">Klicken Sie im Aktivitätsbereich auf "Optionen".</span><span class="sxs-lookup"><span data-stu-id="1c8bb-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="1c8bb-122">Klicken Sie auf "Ansicht ändern".</span><span class="sxs-lookup"><span data-stu-id="1c8bb-122">Click Change view.</span></span>
14. <span data-ttu-id="1c8bb-123">Klicken Sie auf die Kopfzeilenansicht.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-123">Click Header view.</span></span>
15. <span data-ttu-id="1c8bb-124">Erweitern Sie den Abschnitt 'Einstellungen'.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="1c8bb-125">Geben Sie im Feld "Gruppenkennung" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="1c8bb-126">Geben Sie im Feld "Vorlage" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="1c8bb-127">Wählen Sie "Ja" im Feld "Aktiv".</span><span class="sxs-lookup"><span data-stu-id="1c8bb-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="1c8bb-128">Nur aktive Vorlagen können verwendet werden wenn Sie eine Vorlage auf ein neues Verkaufsangebot anwenden.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="1c8bb-129">Klicken Sie im Aktivitätsbereich auf "Optionen".</span><span class="sxs-lookup"><span data-stu-id="1c8bb-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="1c8bb-130">Klicken Sie auf "Ansicht ändern".</span><span class="sxs-lookup"><span data-stu-id="1c8bb-130">Click Change view.</span></span>
21. <span data-ttu-id="1c8bb-131">Klicken Sie auf Positionsansicht.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-131">Click Line view.</span></span>
22. <span data-ttu-id="1c8bb-132">Geben Sie im Feld 'Artikel' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="1c8bb-133">Geben Sie im Feld "Artikel einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="1c8bb-134">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-134">Close the page.</span></span>
25. <span data-ttu-id="1c8bb-135">Geben Sie im Feld "Rabatt in Prozent" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="1c8bb-136">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="1c8bb-136">Click Add line.</span></span>
27. <span data-ttu-id="1c8bb-137">Geben Sie im Feld 'Artikel' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="1c8bb-138">Geben Sie im Feld "Artikel einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="1c8bb-139">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-139">Close the page.</span></span>
30. <span data-ttu-id="1c8bb-140">Geben Sie im Feld "Preis je Einheit" einen neuen Preis ein oder ändern Sie den aktuellen.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="1c8bb-141">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="1c8bb-141">Click Add line.</span></span>
32. <span data-ttu-id="1c8bb-142">Geben Sie im Feld 'Artikel' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="1c8bb-143">Geben Sie im Feld "Artikel einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="1c8bb-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-144">Close the page.</span></span>
35. <span data-ttu-id="1c8bb-145">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="1c8bb-146">Geben Sie im Feld "Rabatt" einen Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="1c8bb-147">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="1c8bb-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="1c8bb-148">Anwenden der Vorlage, um ein einzelnes Angebot zu erstellen</span><span class="sxs-lookup"><span data-stu-id="1c8bb-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="1c8bb-149">Wechseln Sie zu "Vertrieb und Marketing" > "Verkaufsangebote" > "Alle Angebote".</span><span class="sxs-lookup"><span data-stu-id="1c8bb-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="1c8bb-150">Beachten Sie, dass das Angebot, das Sie soeben erstellt haben, als Vorlage markiert ist.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="1c8bb-151">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="1c8bb-151">Click New.</span></span>
3. <span data-ttu-id="1c8bb-152">Wählen Sie im Feld "Kontotyp" die Option "Debitor" aus.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="1c8bb-153">Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="1c8bb-154">Erweitern Sie den Abschnitt "Vorlage".</span><span class="sxs-lookup"><span data-stu-id="1c8bb-154">Expand the Template section.</span></span>
6. <span data-ttu-id="1c8bb-155">Geben Sie im Feld "Gruppenkennung" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="1c8bb-156">Geben Sie im Feld "Vorlagenname" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="1c8bb-157">Wählen Sie im Feld "Berechnungsmethode" "Basierend auf Vorlagenwerten" aus.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="1c8bb-158">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1c8bb-158">Click OK.</span></span>
    * <span data-ttu-id="1c8bb-159">Das neue Angebot ist jetzt basierend auf den Daten und den Bedingungen der Vorlage erstellt.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="1c8bb-160">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-160">Close the page.</span></span>
11. <span data-ttu-id="1c8bb-161">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="1c8bb-162">Anwenden der Vorlage zur Massenerstellung von Angeboten</span><span class="sxs-lookup"><span data-stu-id="1c8bb-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="1c8bb-163">Wechseln Sie zu Vertrieb und Marketing > Verkaufsangebote > Angebotsaktualisierung > Massenerstellung von Angeboten.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="1c8bb-164">Wählen Sie im Feld "Kontotyp" die Option "Debitor" aus.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="1c8bb-165">Geben Sie im Feld "Gruppenkennung" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="1c8bb-166">Geben Sie im Feld "Vorlagenname" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="1c8bb-167">Wählen Sie im Feld "Berechnungsmethode" "Basierend auf Vorlagenwerten" aus.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="1c8bb-168">Erweitern Sie den Abschnitt "Einzuschließende Datensätze".</span><span class="sxs-lookup"><span data-stu-id="1c8bb-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="1c8bb-169">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="1c8bb-169">Click Filter.</span></span>
8. <span data-ttu-id="1c8bb-170">Lesen Sie im Feld "Kriterien" den Filter fest, um den Bereich von Debitoren abzudecken, die Sie in diese Massen-Angebotserstellung einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="1c8bb-171">Verwenden Sie das folgende Format: "Kunde1..KundeN."</span><span class="sxs-lookup"><span data-stu-id="1c8bb-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="1c8bb-172">So können Sie beispielsweise den folgenden Filter festlegen: US-001..US-004</span><span class="sxs-lookup"><span data-stu-id="1c8bb-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="1c8bb-173">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1c8bb-173">Click OK.</span></span>
10. <span data-ttu-id="1c8bb-174">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1c8bb-174">Click OK.</span></span>
11. <span data-ttu-id="1c8bb-175">Wechseln Sie zu "Vertrieb und Marketing" > "Verkaufsangebote" > "Alle Angebote".</span><span class="sxs-lookup"><span data-stu-id="1c8bb-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="1c8bb-176">Überprüfen Sie, ob Angebote für alle Debitoren erstellt wurden, die in der Massenaktualisierungsroutine angeben sind.</span><span class="sxs-lookup"><span data-stu-id="1c8bb-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  

