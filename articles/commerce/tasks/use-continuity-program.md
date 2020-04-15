---
title: Anschlussprogramme nutzen
description: Diese Verfahren zeigt den Verkauf eines Kontinuitätsprogramms und die Verarbeitung der zugehörigen Aufträge.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2baf0127a35cc62952fd78daaf8204d35ec8d2b3
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141152"
---
# <a name="using-continuity-program"></a><span data-ttu-id="61511-103">Anschlussprogramme nutzen</span><span class="sxs-lookup"><span data-stu-id="61511-103">Using continuity program</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61511-104">Diese Verfahren zeigt den Verkauf eines Kontinuitätsprogramms und die Verarbeitung der zugehörigen Aufträge.</span><span class="sxs-lookup"><span data-stu-id="61511-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="61511-105">Damit sie dieses Verfahren abschließen können, muss der Benutzer als Callcenterbenutzer eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="61511-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="61511-106">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="61511-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="61511-107">Navigieren Sie zu Retail und Commerce > Kunden > Kundendienst.</span><span class="sxs-lookup"><span data-stu-id="61511-107">Go to Retail and Commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="61511-108">Geben Sie im Suchtext-Feld "Karin" ein, und drücken Sie dann die TAB-Taste.</span><span class="sxs-lookup"><span data-stu-id="61511-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="61511-109">Das Dialogfeld für die erweiterte Suche wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="61511-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="61511-110">Wenn dies nicht der Fall ist, klicken Sie rechts neben diesem Feld auf Suchen.</span><span class="sxs-lookup"><span data-stu-id="61511-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="61511-111">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="61511-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="61511-112">Es darf nur eine Zeile mit "Karin Berg" geben.</span><span class="sxs-lookup"><span data-stu-id="61511-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="61511-113">Wählen Sie die Zeile aus, indem Sie auf die auf Häkchenspalte am linken äußeren Rand des Formulars klicken.</span><span class="sxs-lookup"><span data-stu-id="61511-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="61511-114">Klicken Sie auf Auswählen.</span><span class="sxs-lookup"><span data-stu-id="61511-114">Click Select.</span></span>
5. <span data-ttu-id="61511-115">Klicken Sie auf "Neuer Auftrag".</span><span class="sxs-lookup"><span data-stu-id="61511-115">Click New sales order.</span></span>
    * <span data-ttu-id="61511-116">Es empfiehlt sich, die Auftragsnummer zu notieren.</span><span class="sxs-lookup"><span data-stu-id="61511-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="61511-117">Sie benötigen Sie sie später in diesem Verfahren.</span><span class="sxs-lookup"><span data-stu-id="61511-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="61511-118">Geben Sie im Artikelnummer-Feld "88000" ein, und drücken Sie dann die TAB-Taste.</span><span class="sxs-lookup"><span data-stu-id="61511-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="61511-119">Dies ist ein Anschlussartikel in den USRT-Demodaten.</span><span class="sxs-lookup"><span data-stu-id="61511-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="61511-120">Klicken Sie auf "Abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="61511-120">Click Complete.</span></span>
8. <span data-ttu-id="61511-121">Geben Sie im Feld "Zahlungsmethode" "Visa" aus.</span><span class="sxs-lookup"><span data-stu-id="61511-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="61511-122">Klicken Sie auf "Kreditkarte hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="61511-122">Click Add credit card.</span></span>
    * <span data-ttu-id="61511-123">Geben Sie die erforderlichen Kreditkarteninformationen auf dieser Seite ein.</span><span class="sxs-lookup"><span data-stu-id="61511-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="61511-124">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="61511-124">Click OK.</span></span>
11. <span data-ttu-id="61511-125">Erweitern Sie den Abschnitt "Zahlung".</span><span class="sxs-lookup"><span data-stu-id="61511-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="61511-126">Um einen Callcenterauftrag zu senden, müssen die Zahlungen für den Auftrag eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="61511-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="61511-127">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="61511-127">Click OK.</span></span>
13. <span data-ttu-id="61511-128">Klicken Sie auf Absenden.</span><span class="sxs-lookup"><span data-stu-id="61511-128">Click Submit.</span></span>
    * <span data-ttu-id="61511-129">Sie haben einen neuen Anschlussauftrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="61511-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="61511-130">Als nächstes führen Sie zwei Stapelverarbeitungsvorgänge aus, die verwendet werden, um die Kontinuitätsaufträge zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="61511-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="61511-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="61511-131">Close the page.</span></span>
15. <span data-ttu-id="61511-132">Navigieren Sie zu Retail und Commerce > Anschluss > Anschlusszahlungen verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="61511-132">Go to Retail and Commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="61511-133">Geben Sie im Anschlussartikel-Feld "88000" ein, und drücken Sie dann die TAB-Taste.</span><span class="sxs-lookup"><span data-stu-id="61511-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="61511-134">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="61511-134">Click OK.</span></span>
18. <span data-ttu-id="61511-135">Navigieren Sie zu Retail und Commerce > Anschluss > Untergeordnete Anschlussaufträge erstellen.</span><span class="sxs-lookup"><span data-stu-id="61511-135">Go to Retail and Commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="61511-136">Dieser Prozess erstellt neue Aufträge auf Grundlage der Einstellungen der Kontinuitätsprogramme.</span><span class="sxs-lookup"><span data-stu-id="61511-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="61511-137">Geben Sie im Anschlussartikel-Feld "88000" ein, und drücken Sie dann die TAB-Taste.</span><span class="sxs-lookup"><span data-stu-id="61511-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="61511-138">Artikel '88000' ist ein Anschlussartikel in den USRT-Demodaten.</span><span class="sxs-lookup"><span data-stu-id="61511-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="61511-139">Geben Sie im Feld 'Auftrag' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="61511-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="61511-140">Geben Sie die Auftragsnummer ein, die Sie weiter oben in der Prozedur notiert haben.</span><span class="sxs-lookup"><span data-stu-id="61511-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="61511-141">So bleibt die Verarbeitungszeit für dieses Verfahren minimal.</span><span class="sxs-lookup"><span data-stu-id="61511-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="61511-142">Das Auftragsfeld ist optional. Sie können alle Aufträge für ein beliebiges Programm verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="61511-142">The Sales order field field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="61511-143">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="61511-143">Click OK.</span></span>

