---
title: Bestandswerte im Lagerort initialisieren
description: Dieses Verfahren zeigt Ihnen, wie der verfügbare Lagerbestand manuell mithilfe einer Lagerverlagerungserfassung aktualisiert wird.
author: perlynne
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0746b799c701c569f0ae5c657ac3302ab6626287
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823480"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a><span data-ttu-id="58351-103">Bestandswerte im Lagerort initialisieren</span><span class="sxs-lookup"><span data-stu-id="58351-103">Initialize stock levels in the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="58351-104">Dieses Verfahren zeigt Ihnen, wie der verfügbare Lagerbestand manuell mithilfe einer Lagerverlagerungserfassung aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="58351-104">This procedure shows you how to get the on-hand inventory updated manually using an Inventory movement journal.</span></span> <span data-ttu-id="58351-105">(Es ist auch möglich den verfügbaren Lagerbestand zu aktualisieren, indem Sie Buchungen in Datenentitäten importieren.) Sie können dieses Handbuch im Demodatenunternehmen USMF ausführen, in dem alle Voraussetzungen wie Erfassungen, Artikeleinstellungen, Buchungsprofile und Konten verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="58351-105">(It's also possible to update on-hand inventory by importing transactions in data entities.) You can run this guide in demo data company USMF where all the prerequisites like journal name, item setup, posting profiles, and accounts are available.</span></span> <span data-ttu-id="58351-106">Das Handbuch schlägt bestimmte Werte für den Artikel und die Dimensionen vor, die verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58351-106">The guide suggests specific values for the item and dimensions that are used.</span></span> <span data-ttu-id="58351-107">Wenn Sie einen anderen Artikel auswählen, müssen Sie ggf. Werte für verschiedene Dimensionen eingeben.</span><span class="sxs-lookup"><span data-stu-id="58351-107">If you choose a different item, you may need to enter values for different dimensions.</span></span>

1. <span data-ttu-id="58351-108">Wechseln Sie zu Lagerverwaltung > Journaleinträge > Artikel > Bewegung.</span><span class="sxs-lookup"><span data-stu-id="58351-108">Go to Inventory management > Journal entries > Items > Movement.</span></span>
2. <span data-ttu-id="58351-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="58351-109">Click New.</span></span>
3. <span data-ttu-id="58351-110">Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="58351-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="58351-111">Wählen Sie IMov.</span><span class="sxs-lookup"><span data-stu-id="58351-111">Select IMov.</span></span>
    * <span data-ttu-id="58351-112">Es empfiehlt sich, verschiedene Erfassungsvorlagen für verschiedene Geschäftszwecke zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="58351-112">It's a good practice to use different journal name templates for the different business purposes.</span></span>  
5. <span data-ttu-id="58351-113">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="58351-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="58351-114">Geben Sie im Feld "Gegenkonto" den Wert "140200" an.</span><span class="sxs-lookup"><span data-stu-id="58351-114">In the Offset account field, specify the values '140200'.</span></span>
    * <span data-ttu-id="58351-115">Hierbei handelt es sich um das in Erfassungspositionen als Standardkonto verwendete Gegenkonto.</span><span class="sxs-lookup"><span data-stu-id="58351-115">This is the offset account that will be the default account on the journal lines.</span></span> <span data-ttu-id="58351-116">Es ist möglich, die Standardeinstellung zu überschreiben, um verschiedene Gegenkontos pro Position zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="58351-116">It's possible to override the default to assign different offset accounts per line.</span></span>  
7. <span data-ttu-id="58351-117">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="58351-117">Click OK.</span></span>
8. <span data-ttu-id="58351-118">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="58351-118">Click New.</span></span>
9. <span data-ttu-id="58351-119">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="58351-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="58351-120">Artikel A0001 auswählen.</span><span class="sxs-lookup"><span data-stu-id="58351-120">Select item A0001.</span></span>
11. <span data-ttu-id="58351-121">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="58351-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="58351-122">Klicken Sie auf die Registerkarte "Lagerungsdimension".</span><span class="sxs-lookup"><span data-stu-id="58351-122">Click the Inventory dimensions tab.</span></span>
13. <span data-ttu-id="58351-123">Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="58351-123">In the Site field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="58351-124">Wählen Sie Standort 1.</span><span class="sxs-lookup"><span data-stu-id="58351-124">Select site 1.</span></span>
15. <span data-ttu-id="58351-125">Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="58351-125">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="58351-126">Wählen Sie Lagerort 13.</span><span class="sxs-lookup"><span data-stu-id="58351-126">Select warehouse 13.</span></span>
17. <span data-ttu-id="58351-127">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="58351-127">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="58351-128">Klicken Sie im Feld "Lagerplatz" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="58351-128">In the Location field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="58351-129">Wählen Sie Lagerplatz 13.</span><span class="sxs-lookup"><span data-stu-id="58351-129">Select location 13.</span></span>
20. <span data-ttu-id="58351-130">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="58351-130">In the Quantity field, enter a number.</span></span>
21. <span data-ttu-id="58351-131">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="58351-131">Click Save.</span></span>
22. <span data-ttu-id="58351-132">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="58351-132">Click Post.</span></span>
23. <span data-ttu-id="58351-133">Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Alle Buchungsfehler in eine neue Erfassung übertragen".</span><span class="sxs-lookup"><span data-stu-id="58351-133">Check or uncheck the Transfer all posting errors to a new journal check box.</span></span>
    * <span data-ttu-id="58351-134">Wenn Sie diese Option aktivieren, werden alle Positionen, die nicht gebucht werden können, in eine neue Erfassung kopiert.</span><span class="sxs-lookup"><span data-stu-id="58351-134">If you enable this option, any lines that fail to post will be copied to a new journal.</span></span> <span data-ttu-id="58351-135">Sie können die Informationen im Protokoll verwenden, um Probleme zu korrigieren und anschließend die Positionen erneut zu buchen.</span><span class="sxs-lookup"><span data-stu-id="58351-135">You can use the information in the log to correct the issues and then re-post the lines.</span></span>  
24. <span data-ttu-id="58351-136">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="58351-136">Click OK.</span></span>
25. <span data-ttu-id="58351-137">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="58351-137">Close the page.</span></span>
26. <span data-ttu-id="58351-138">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="58351-138">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]