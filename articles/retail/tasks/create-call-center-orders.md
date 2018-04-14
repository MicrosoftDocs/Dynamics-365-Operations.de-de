--- 
title: " Callcenteraufträge erstellen"
description: "Diese Prozedur führt Sie Schritt für Schritt durch die Suche nach einem Debitor, das Erstellen eines neuen Auftrags, die Suche nach einem Produkt und das Einziehen einer Zahlung vom Debitor."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d46e5382c4808ecb01012800caf85209b173901a
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="create-call-center-orders"></a><span data-ttu-id="e4988-103"> Callcenteraufträge erstellen</span><span class="sxs-lookup"><span data-stu-id="e4988-103">Create call center orders</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e4988-104">Diese Prozedur führt Sie Schritt für Schritt durch die Suche nach einem Debitor, das Erstellen eines neuen Auftrags, die Suche nach einem Produkt und das Einziehen einer Zahlung vom Debitor.</span><span class="sxs-lookup"><span data-stu-id="e4988-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="e4988-105">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet. Sie ist für den Auftragssachbearbeiter vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="e4988-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="e4988-106">Voraussetzungen: Die Benutzer, welche das Verfahren ausführen, sind als Callcenterbenutzer eingerichtet, und der halbjährliche Fabrikam-Katalog wird mit mindestens einem Quellcode veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="e4988-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="e4988-107">Navigieren Sie zu Einzelhandel und Handel > Kunden > Kundendienst.</span><span class="sxs-lookup"><span data-stu-id="e4988-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="e4988-108">Geben Sie im SearchText-Feld die Suchkriterien ein, um den Debitor zu suchen.</span><span class="sxs-lookup"><span data-stu-id="e4988-108">In the SearchText field, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="e4988-109">Für diese Beispielsprozedur geben Sie "karen" ein und drücken Sie die Taste.</span><span class="sxs-lookup"><span data-stu-id="e4988-109">For this example procedure type in 'karen' and press tab.</span></span>  
3. <span data-ttu-id="e4988-110">Klicken Sie auf "Suchen".</span><span class="sxs-lookup"><span data-stu-id="e4988-110">Click Search.</span></span>
    * <span data-ttu-id="e4988-111">Da nur ein Debitor namens Karen in den Demodaten vorhanden ist, erfolgt die Auswahl automatisch.</span><span class="sxs-lookup"><span data-stu-id="e4988-111">Since there is only one customer named Karen in demo data they will be automatically selected.</span></span>  
4. <span data-ttu-id="e4988-112">Klicken Sie auf "Neuer Auftrag".</span><span class="sxs-lookup"><span data-stu-id="e4988-112">Click New sales order.</span></span>
5. <span data-ttu-id="e4988-113">Erweitern oder reduzieren Sie den Kopfbereich "Auftrag".</span><span class="sxs-lookup"><span data-stu-id="e4988-113">Expand or collapse the Sales order header section.</span></span>
6. <span data-ttu-id="e4988-114">Wählen Sie den Quelltyp für den Katalog aus.</span><span class="sxs-lookup"><span data-stu-id="e4988-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="e4988-115">Wenn keine aktiven Quellcodes vorliegen, können Sie das Quellfeld schließen und diesen Schritt überspringen.</span><span class="sxs-lookup"><span data-stu-id="e4988-115">If there are no active Source codes you can close the Source field and skip this step.</span></span>  
7. <span data-ttu-id="e4988-116">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="e4988-116">Click Add line.</span></span>
8. <span data-ttu-id="e4988-117">Geben Sie im Feld "Artikelnummer" den Artikelsuchbegriff ein.</span><span class="sxs-lookup"><span data-stu-id="e4988-117">In the Item number field, enter the item search term.</span></span>
    * <span data-ttu-id="e4988-118">Für diese Beispielprozedur geben Sie eine Artikelnummer " 8111 "ein und drücken Sie die Registerkarte. Dadurch wird das Artikelsuchfenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e4988-118">For this sample procedure enter a partial item number of '8111' and press tab. This will pop up the item search window.</span></span>  
9. <span data-ttu-id="e4988-119">Wählen Sie das Produkt aus, das zum Auftrag hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e4988-119">Select the product to add to the sales order</span></span>
10. <span data-ttu-id="e4988-120">Geben Sie die Verkaufsmenge ein.</span><span class="sxs-lookup"><span data-stu-id="e4988-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="e4988-121">Klicken Sie auf Erstellen.</span><span class="sxs-lookup"><span data-stu-id="e4988-121">Click Create.</span></span>
12. <span data-ttu-id="e4988-122">Klicken Sie auf "Abschließen", um die Debitorenzahlung aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="e4988-122">Click Complete to capture the customer payment.</span></span>
13. <span data-ttu-id="e4988-123">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e4988-123">Click Add.</span></span>
    * <span data-ttu-id="e4988-124">Der Hinzufügen-Llink  ist die Registerkarte Zahlungen. Erweitern Sie die Registerkarte wenn sie verringert ist.</span><span class="sxs-lookup"><span data-stu-id="e4988-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="e4988-125">Wählen Sie die Zahlungsmethode aus.</span><span class="sxs-lookup"><span data-stu-id="e4988-125">Select the payment method.</span></span>
    * <span data-ttu-id="e4988-126">Für diese Prozedur wählen Sie die Bargeldzahlungsmethode aus.</span><span class="sxs-lookup"><span data-stu-id="e4988-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="e4988-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e4988-127">Close the page.</span></span>
16. <span data-ttu-id="e4988-128">Geben Sie den Betrag ein.</span><span class="sxs-lookup"><span data-stu-id="e4988-128">Enter the amount.</span></span>
    * <span data-ttu-id="e4988-129">Für diese Prozedur geben Sie einen Betrag gleich dem Auftragssaldo ein, der in der Auftrags-Übersichtsseite auf der linken Seite des Betrag-Felds angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e4988-129">For this procedure enter an amount equal to the order balance which can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="e4988-130">Dies ermöglicht Ihnen, den Auftrag als vollständig bezahlt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="e4988-130">This will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="e4988-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="e4988-131">Click OK.</span></span>
18. <span data-ttu-id="e4988-132">Klicken Sie auf Absenden.</span><span class="sxs-lookup"><span data-stu-id="e4988-132">Click Submit.</span></span>


