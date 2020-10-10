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
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm, SalesQuickQuote
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1bbe96e8e8fc2b7139c5d3064825f6ab527fc67e
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830306"
---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="3f3ba-103">Massenerstellung von Verkaufsangeboten</span><span class="sxs-lookup"><span data-stu-id="3f3ba-103">Mass create sales quotations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3f3ba-104">Diese Verfahren zeigt, wie Sie Angebote, die eine Gruppe von Produkte oder Dienstleistungen enthalten und an mehrere Debitoren gesendet werden sollen, effizient erstellen.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="3f3ba-105">Diese Massenangebotserstellung basiert auf Angebotsvorlagen.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="3f3ba-106">Sie können diese Prozedur in Ihrem eigenen Demodatenunternehmen oder in USMF ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="3f3ba-107">Erstellen einer Angebotsvorlage</span><span class="sxs-lookup"><span data-stu-id="3f3ba-107">Create a quotation template</span></span>
1. <span data-ttu-id="3f3ba-108">Wechseln Sie zu Vertrieb und Marketing > Einstellungen > Angebote > Vorlagengruppen.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="3f3ba-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="3f3ba-109">Click New.</span></span>
3. <span data-ttu-id="3f3ba-110">Geben Sie im Feld "Gruppenkennung" eine Kennung Ihrer Wahl ein.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="3f3ba-111">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3f3ba-112">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="3f3ba-112">Click Save.</span></span>
6. <span data-ttu-id="3f3ba-113">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-113">Close the page.</span></span>
7. <span data-ttu-id="3f3ba-114">Wechseln Sie zu "Vertrieb und Marketing" > "Verkaufsangebote" > "Alle Angebote".</span><span class="sxs-lookup"><span data-stu-id="3f3ba-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="3f3ba-115">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="3f3ba-115">Click New.</span></span>
9. <span data-ttu-id="3f3ba-116">Wählen Sie im Feld "Kontotyp" die Option "Debitor" aus.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="3f3ba-117">Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="3f3ba-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3f3ba-118">Click OK.</span></span>
    * <span data-ttu-id="3f3ba-119">Damit ein Angebot eine Vorlage wird, müssen Sie die Einrichtungsschritte im Angebotskopf ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="3f3ba-120">Dies muss ausgeführt werden, bevor Sie Positionen zum Angebot hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="3f3ba-121">Klicken Sie im Aktivitätsbereich auf "Optionen".</span><span class="sxs-lookup"><span data-stu-id="3f3ba-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="3f3ba-122">Klicken Sie auf "Ansicht ändern".</span><span class="sxs-lookup"><span data-stu-id="3f3ba-122">Click Change view.</span></span>
14. <span data-ttu-id="3f3ba-123">Klicken Sie auf die Kopfzeilenansicht.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-123">Click Header view.</span></span>
15. <span data-ttu-id="3f3ba-124">Erweitern Sie den Abschnitt 'Einstellungen'.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="3f3ba-125">Geben Sie im Feld "Gruppenkennung" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="3f3ba-126">Geben Sie im Feld "Vorlage" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="3f3ba-127">Wählen Sie "Ja" im Feld "Aktiv".</span><span class="sxs-lookup"><span data-stu-id="3f3ba-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="3f3ba-128">Nur aktive Vorlagen können verwendet werden wenn Sie eine Vorlage auf ein neues Verkaufsangebot anwenden.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="3f3ba-129">Klicken Sie im Aktivitätsbereich auf "Optionen".</span><span class="sxs-lookup"><span data-stu-id="3f3ba-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="3f3ba-130">Klicken Sie auf "Ansicht ändern".</span><span class="sxs-lookup"><span data-stu-id="3f3ba-130">Click Change view.</span></span>
21. <span data-ttu-id="3f3ba-131">Klicken Sie auf Positionsansicht.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-131">Click Line view.</span></span>
22. <span data-ttu-id="3f3ba-132">Geben Sie im Feld 'Artikel' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="3f3ba-133">Geben Sie im Feld "Artikel einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="3f3ba-134">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-134">Close the page.</span></span>
25. <span data-ttu-id="3f3ba-135">Geben Sie im Feld "Rabatt in Prozent" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="3f3ba-136">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3f3ba-136">Click Add line.</span></span>
27. <span data-ttu-id="3f3ba-137">Geben Sie im Feld 'Artikel' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="3f3ba-138">Geben Sie im Feld "Artikel einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="3f3ba-139">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-139">Close the page.</span></span>
30. <span data-ttu-id="3f3ba-140">Geben Sie im Feld "Preis je Einheit" einen neuen Preis ein oder ändern Sie den aktuellen.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="3f3ba-141">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3f3ba-141">Click Add line.</span></span>
32. <span data-ttu-id="3f3ba-142">Geben Sie im Feld 'Artikel' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="3f3ba-143">Geben Sie im Feld "Artikel einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="3f3ba-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-144">Close the page.</span></span>
35. <span data-ttu-id="3f3ba-145">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="3f3ba-146">Geben Sie im Feld "Rabatt" einen Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="3f3ba-147">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="3f3ba-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="3f3ba-148">Anwenden der Vorlage, um ein einzelnes Angebot zu erstellen</span><span class="sxs-lookup"><span data-stu-id="3f3ba-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="3f3ba-149">Wechseln Sie zu "Vertrieb und Marketing" > "Verkaufsangebote" > "Alle Angebote".</span><span class="sxs-lookup"><span data-stu-id="3f3ba-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="3f3ba-150">Beachten Sie, dass das Angebot, das Sie soeben erstellt haben, als Vorlage markiert ist.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="3f3ba-151">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="3f3ba-151">Click New.</span></span>
3. <span data-ttu-id="3f3ba-152">Wählen Sie im Feld "Kontotyp" die Option "Debitor" aus.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="3f3ba-153">Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="3f3ba-154">Erweitern Sie den Abschnitt "Vorlage".</span><span class="sxs-lookup"><span data-stu-id="3f3ba-154">Expand the Template section.</span></span>
6. <span data-ttu-id="3f3ba-155">Geben Sie im Feld "Gruppenkennung" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="3f3ba-156">Geben Sie im Feld "Vorlagenname" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="3f3ba-157">Wählen Sie im Feld "Berechnungsmethode" "Basierend auf Vorlagenwerten" aus.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="3f3ba-158">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3f3ba-158">Click OK.</span></span>
    * <span data-ttu-id="3f3ba-159">Das neue Angebot ist jetzt basierend auf den Daten und den Bedingungen der Vorlage erstellt.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="3f3ba-160">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-160">Close the page.</span></span>
11. <span data-ttu-id="3f3ba-161">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="3f3ba-162">Anwenden der Vorlage zur Massenerstellung von Angeboten</span><span class="sxs-lookup"><span data-stu-id="3f3ba-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="3f3ba-163">Wechseln Sie zu Vertrieb und Marketing > Verkaufsangebote > Angebotsaktualisierung > Massenerstellung von Angeboten.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="3f3ba-164">Wählen Sie im Feld "Kontotyp" die Option "Debitor" aus.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="3f3ba-165">Geben Sie im Feld "Gruppenkennung" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="3f3ba-166">Geben Sie im Feld "Vorlagenname" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="3f3ba-167">Wählen Sie im Feld "Berechnungsmethode" "Basierend auf Vorlagenwerten" aus.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="3f3ba-168">Erweitern Sie den Abschnitt "Einzuschließende Datensätze".</span><span class="sxs-lookup"><span data-stu-id="3f3ba-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="3f3ba-169">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="3f3ba-169">Click Filter.</span></span>
8. <span data-ttu-id="3f3ba-170">Lesen Sie im Feld "Kriterien" den Filter fest, um den Bereich von Debitoren abzudecken, die Sie in diese Massen-Angebotserstellung einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="3f3ba-171">Verwenden Sie das folgende Format: "Kunde1..KundeN."</span><span class="sxs-lookup"><span data-stu-id="3f3ba-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="3f3ba-172">So können Sie beispielsweise den folgenden Filter festlegen: US-001..US-004</span><span class="sxs-lookup"><span data-stu-id="3f3ba-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="3f3ba-173">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3f3ba-173">Click OK.</span></span>
10. <span data-ttu-id="3f3ba-174">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3f3ba-174">Click OK.</span></span>
11. <span data-ttu-id="3f3ba-175">Wechseln Sie zu "Vertrieb und Marketing" > "Verkaufsangebote" > "Alle Angebote".</span><span class="sxs-lookup"><span data-stu-id="3f3ba-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="3f3ba-176">Überprüfen Sie, ob Angebote für alle Debitoren erstellt wurden, die in der Massenaktualisierungsroutine angeben sind.</span><span class="sxs-lookup"><span data-stu-id="3f3ba-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  

