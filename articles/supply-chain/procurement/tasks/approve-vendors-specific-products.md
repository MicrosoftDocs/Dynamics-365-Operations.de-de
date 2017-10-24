--- 
title: "Händler für bestimmte Produkte genehmigen"
description: "Diese Prozedur zeigt Ihnen an, wie Sie Händler für bestimmte Produkte genehmigen."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ffc58d2afe73fa2290e4e73a058d47ffd64b8d54
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="approve-vendors-for-specific-products"></a><span data-ttu-id="8813b-103">Händler für bestimmte Produkte genehmigen</span><span class="sxs-lookup"><span data-stu-id="8813b-103">Approve vendors for specific products</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8813b-104">Diese Prozedur zeigt Ihnen an, wie Sie Händler für bestimmte Produkte genehmigen.</span><span class="sxs-lookup"><span data-stu-id="8813b-104">This procedure shows you how to approve vendors for specific products.</span></span> <span data-ttu-id="8813b-105">Dies ermöglicht es Ihnen, zu steuern, welche Händler verwendet werden können, wenn das Produkt einer Bestellung hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="8813b-105">This allows you to control which vendors can be used when the product is added to a purchase order.</span></span> <span data-ttu-id="8813b-106">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="8813b-106">You can use this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="8813b-107">In der Regel wird diese Aufgabe von einem Einkaufsleiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8813b-107">This task would typically be carried out by a Purchasing manager.</span></span>

1. <span data-ttu-id="8813b-108">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="8813b-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="8813b-109">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8813b-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="8813b-110">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8813b-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8813b-111">Erweitern Sie den Abschnitt "Einkauf".</span><span class="sxs-lookup"><span data-stu-id="8813b-111">Expand the Purchase section.</span></span>
    * <span data-ttu-id="8813b-112">Wenn es einen primären Händler gibt, der im Feld "Händler" angezeigt wird, müssen Sie diesen Händler als genehmigten Kreditor in den folgenden Schritten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8813b-112">If there is a primary vendor shown in the Vendor field, then you need to add this vendor as an approved vendor in the following steps.</span></span> <span data-ttu-id="8813b-113">Notieren Sie die Kreditornummer, sofern sie angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8813b-113">Make a note of the vendor number, if one is shown.</span></span>  
5. <span data-ttu-id="8813b-114">Klicken Sie im Aktivitätsbereich auf "Einkauf".</span><span class="sxs-lookup"><span data-stu-id="8813b-114">On the Action Pane, click Purchase.</span></span>
6. <span data-ttu-id="8813b-115">Klicken Sie auf Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="8813b-115">Click Setup.</span></span>
7. <span data-ttu-id="8813b-116">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8813b-116">Click Add.</span></span>
8. <span data-ttu-id="8813b-117">Geben Sie im Feld "Händler" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="8813b-117">In the Vendor field, enter or select a value.</span></span>
    * <span data-ttu-id="8813b-118">Wählen Sie den genehmigten Kreditor aus.</span><span class="sxs-lookup"><span data-stu-id="8813b-118">Select the approved vendor.</span></span> <span data-ttu-id="8813b-119">Es muss mindestens eine der Positionen der primäre Händler sein, wenn sich einer im Produktdatensatz befand.</span><span class="sxs-lookup"><span data-stu-id="8813b-119">At least one of the lines has to be the primary vendor if there was one in the product record.</span></span> <span data-ttu-id="8813b-120">Wenn Sie zuvor die Händlernummer notierten, wählen Sie diese hier aus.</span><span class="sxs-lookup"><span data-stu-id="8813b-120">If you made a note of the vendor number earlier, select it here.</span></span>  
9. <span data-ttu-id="8813b-121">Geben Sie im Feld "Ablauf" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="8813b-121">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="8813b-122">Wählen Sie ein Datum aus, das mehrere Monate in der Zukunft liegt.</span><span class="sxs-lookup"><span data-stu-id="8813b-122">Choose a date a that is a few months ahead.</span></span>  
10. <span data-ttu-id="8813b-123">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8813b-123">Click Add.</span></span>
11. <span data-ttu-id="8813b-124">Geben Sie im Feld "Händler" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="8813b-124">In the Vendor field, enter or select a value.</span></span>
12. <span data-ttu-id="8813b-125">Geben Sie im Feld "Ablauf" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="8813b-125">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="8813b-126">Wählen Sie ein Datum aus, das sich vom vorherigen Ablaufdatum unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="8813b-126">Choose a date that is different than the previous expiration date.</span></span>  
13. <span data-ttu-id="8813b-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8813b-127">Close the page.</span></span>
14. <span data-ttu-id="8813b-128">Klicken Sie auf "Genehmigte Kreditoren".</span><span class="sxs-lookup"><span data-stu-id="8813b-128">Click Approved vendors.</span></span>
15. <span data-ttu-id="8813b-129">Geben Sie im Feld "Ablauf" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="8813b-129">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="8813b-130">Dieses Datum dient als ein Filter, damit Sie sehen können, wer bis zu einem bestimmten Datum die genehmigten Kreditoren sind.</span><span class="sxs-lookup"><span data-stu-id="8813b-130">This date acts as a filter so you can see who the approved vendors are, up to a certain date.</span></span>  
16. <span data-ttu-id="8813b-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8813b-131">Close the page.</span></span>
17. <span data-ttu-id="8813b-132">Klicken Sei auf "Effektive Periode".</span><span class="sxs-lookup"><span data-stu-id="8813b-132">Click Effective period.</span></span>
18. <span data-ttu-id="8813b-133">Geben Sie im Feld "Abgelaufene Händler am" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="8813b-133">In the Show vendors expired by field, enter a date.</span></span>
    * <span data-ttu-id="8813b-134">Sie können diese Seite verwenden, um Händler identifizieren, bei denen der Genehmigungsstatus nach einem bestimmten Datum abläuft.</span><span class="sxs-lookup"><span data-stu-id="8813b-134">You can use this page to identify vendors where the approval status will expire after a certain date.</span></span>  
19. <span data-ttu-id="8813b-135">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8813b-135">Close the page.</span></span>
20. <span data-ttu-id="8813b-136">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="8813b-136">Click Edit.</span></span>
21. <span data-ttu-id="8813b-137">Wählen Sie im Feld "Überprüfung genehmigter Kreditoren" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="8813b-137">In the Approved vendor check method field, select an option.</span></span>
    * <span data-ttu-id="8813b-138">In diesem Feld können Sie die Richtlinie auswählen, die bestimmt, was geschehen soll, wenn das Produkt einer Bestellpostion hinzugefügt wird, wobei der Händler kein genehmigter Kreditor ist.</span><span class="sxs-lookup"><span data-stu-id="8813b-138">This field allows you to select the policy for what should happen if the product is added to a purchase order line where the vendor is not an approved vendor.</span></span>  
22. <span data-ttu-id="8813b-139">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8813b-139">Click Save.</span></span>
23. <span data-ttu-id="8813b-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8813b-140">Close the page.</span></span>
24. <span data-ttu-id="8813b-141">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8813b-141">Close the page.</span></span>
25. <span data-ttu-id="8813b-142">Wechseln Sie zu "Beschaffung" > "Händler" > "Kreditor-/Artikelbeziehungen" > "Übersicht genehmigter Kreditoren nach Artikel".</span><span class="sxs-lookup"><span data-stu-id="8813b-142">Go to Procurement and sourcing > Vendors > Vendor/item relations > Approved vendor list by item.</span></span>
    * <span data-ttu-id="8813b-143">Diese Seite enthält einen Überblick über alle Produkte und die genehmigten Kreditoren.</span><span class="sxs-lookup"><span data-stu-id="8813b-143">This page gives you an overview of all products and the approved vendors.</span></span>  
26. <span data-ttu-id="8813b-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8813b-144">Close the page.</span></span>
27. <span data-ttu-id="8813b-145">Klicken Sie auf "Beschaffung" > "Kreditoren" > "Alle Kreditoren".</span><span class="sxs-lookup"><span data-stu-id="8813b-145">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
    * <span data-ttu-id="8813b-146">Sie können von einem Händler aus beginnen und dann zur Liste der genehmigten Produkten für dieses Kreditorenkonto wechseln.</span><span class="sxs-lookup"><span data-stu-id="8813b-146">You can also start from a vendor and then go to the list of approved products for that vendor account.</span></span>  
28. <span data-ttu-id="8813b-147">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8813b-147">In the list, find and select the desired record.</span></span>
29. <span data-ttu-id="8813b-148">Klicken Sie im Aktivitätsbereich auf "Beschaffung".</span><span class="sxs-lookup"><span data-stu-id="8813b-148">On the Action Pane, click Procurement.</span></span>
30. <span data-ttu-id="8813b-149">Klicken Sie auf "Übersicht genehmigter Kreditoren 'nach Kreditoren'".</span><span class="sxs-lookup"><span data-stu-id="8813b-149">Click Approved vendor list by vendor.</span></span>
31. <span data-ttu-id="8813b-150">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8813b-150">Close the page.</span></span>
32. <span data-ttu-id="8813b-151">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8813b-151">Close the page.</span></span>


