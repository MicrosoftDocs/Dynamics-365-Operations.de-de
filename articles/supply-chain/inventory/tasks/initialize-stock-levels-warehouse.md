---
title: Bestandswerte im Lagerort initialisieren
description: "Dieses Verfahren zeigt Ihnen, wie der verfügbare Lagerbestand manuell mithilfe einer Lagerverlagerungserfassung aktualisiert wird."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 4ad9ab54fbe84c8ec47aa2bebcca44656124a73e
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="initialize-stock-levels-in-the-warehouse"></a><span data-ttu-id="1686d-103">Bestandswerte im Lagerort initialisieren</span><span class="sxs-lookup"><span data-stu-id="1686d-103">Initialize stock levels in the warehouse</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1686d-104">Dieses Verfahren zeigt Ihnen, wie der verfügbare Lagerbestand manuell mithilfe einer Lagerverlagerungserfassung aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="1686d-104">This procedure shows you how to get the on-hand inventory updated manually using an Inventory movement journal.</span></span> <span data-ttu-id="1686d-105">(Es ist auch möglich den verfügbaren Lagerbestand zu aktualisieren, indem Sie Buchungen in Datenentitäten importieren.) Sie können dieses Handbuch im Demodatenunternehmen USMF ausführen, in dem alle Voraussetzungen wie Erfassungen, Artikeleinstellungen, Buchungsprofile und Konten verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="1686d-105">(It’s also possible to update on-hand inventory by importing transactions in data entities.) You can run this guide in demo data company USMF where all the prerequisites like journal name, item setup, posting profiles, and accounts are available.</span></span> <span data-ttu-id="1686d-106">Das Handbuch schlägt bestimmte Werte für den Artikel und die Dimensionen vor, die verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1686d-106">The guide suggests specific values for the item and dimensions that are used.</span></span> <span data-ttu-id="1686d-107">Wenn Sie einen anderen Artikel auswählen, müssen Sie ggf. Werte für verschiedene Dimensionen eingeben.</span><span class="sxs-lookup"><span data-stu-id="1686d-107">If you choose a different item, you may need to enter values for different dimensions.</span></span>

1. <span data-ttu-id="1686d-108">Wechseln Sie zu Lagerverwaltung > Journaleinträge > Artikel > Bewegung.</span><span class="sxs-lookup"><span data-stu-id="1686d-108">Go to Inventory management > Journal entries > Items > Movement.</span></span>
2. <span data-ttu-id="1686d-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="1686d-109">Click New.</span></span>
3. <span data-ttu-id="1686d-110">Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1686d-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="1686d-111">Wählen Sie IMov.</span><span class="sxs-lookup"><span data-stu-id="1686d-111">Select IMov.</span></span>
    * <span data-ttu-id="1686d-112">Es empfiehlt sich, verschiedene Erfassungsvorlagen für verschiedene Geschäftszwecke zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1686d-112">It’s a good practice to use different journal name templates for the different business purposes.</span></span>  
5. <span data-ttu-id="1686d-113">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="1686d-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="1686d-114">Geben Sie im Feld "Gegenkonto" den Wert "140200" an.</span><span class="sxs-lookup"><span data-stu-id="1686d-114">In the Offset account field, specify the values '140200'.</span></span>
    * <span data-ttu-id="1686d-115">Hierbei handelt es sich um das in Erfassungspositionen als Standardkonto verwendete Gegenkonto.</span><span class="sxs-lookup"><span data-stu-id="1686d-115">This is the offset account that will be the default account on the journal lines.</span></span> <span data-ttu-id="1686d-116">Es ist möglich, die Standardeinstellung zu überschreiben, um verschiedene Gegenkontos pro Position zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="1686d-116">It’s possible to override the default to assign different offset accounts per line.</span></span>  
7. <span data-ttu-id="1686d-117">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1686d-117">Click OK.</span></span>
8. <span data-ttu-id="1686d-118">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="1686d-118">Click New.</span></span>
9. <span data-ttu-id="1686d-119">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1686d-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="1686d-120">Artikel A0001 auswählen.</span><span class="sxs-lookup"><span data-stu-id="1686d-120">Select item A0001.</span></span>
11. <span data-ttu-id="1686d-121">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="1686d-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="1686d-122">Klicken Sie auf die Registerkarte "Lagerungsdimension".</span><span class="sxs-lookup"><span data-stu-id="1686d-122">Click the Inventory dimensions tab.</span></span>
13. <span data-ttu-id="1686d-123">Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1686d-123">In the Site field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="1686d-124">Wählen Sie Standort 1.</span><span class="sxs-lookup"><span data-stu-id="1686d-124">Select site 1.</span></span>
15. <span data-ttu-id="1686d-125">Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1686d-125">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="1686d-126">Wählen Sie Lagerort 13.</span><span class="sxs-lookup"><span data-stu-id="1686d-126">Select warehouse 13.</span></span>
17. <span data-ttu-id="1686d-127">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="1686d-127">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="1686d-128">Klicken Sie im Feld "Lagerplatz" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1686d-128">In the Location field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="1686d-129">Wählen Sie Lagerplatz 13.</span><span class="sxs-lookup"><span data-stu-id="1686d-129">Select location 13.</span></span>
20. <span data-ttu-id="1686d-130">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="1686d-130">In the Quantity field, enter a number.</span></span>
21. <span data-ttu-id="1686d-131">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="1686d-131">Click Save.</span></span>
22. <span data-ttu-id="1686d-132">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="1686d-132">Click Post.</span></span>
23. <span data-ttu-id="1686d-133">Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Alle Buchungsfehler in eine neue Erfassung übertragen".</span><span class="sxs-lookup"><span data-stu-id="1686d-133">Check or uncheck the Transfer all posting errors to a new journal check box.</span></span>
    * <span data-ttu-id="1686d-134">Wenn Sie diese Option aktivieren, werden alle Positionen, die nicht gebucht werden können, in eine neue Erfassung kopiert.</span><span class="sxs-lookup"><span data-stu-id="1686d-134">If you enable this option, any lines that fail to post will be copied to a new journal.</span></span> <span data-ttu-id="1686d-135">Sie können die Informationen im Protokoll verwenden, um Probleme zu korrigieren und anschließend die Positionen erneut zu buchen.</span><span class="sxs-lookup"><span data-stu-id="1686d-135">You can use the information in the log to correct the issues and then re-post the lines.</span></span>  
24. <span data-ttu-id="1686d-136">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1686d-136">Click OK.</span></span>
25. <span data-ttu-id="1686d-137">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1686d-137">Close the page.</span></span>
26. <span data-ttu-id="1686d-138">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1686d-138">Close the page.</span></span>

