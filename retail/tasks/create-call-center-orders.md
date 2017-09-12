--- 
title: " Callcenteraufträge erstellen"
description: "Diese Prozedur führt Sie Schritt für Schritt durch die Suche nach einem Debitor, das Erstellen eines neuen Auftrags, die Suche nach einem Produkt und das Einziehen einer Zahlung vom Debitor."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 62f88cc2e28405a9d2eb43819fb09d83a64658b6
ms.contentlocale: de-de
ms.lasthandoff: 07/28/2017

---
# <a name="create-call-center-orders"></a><span data-ttu-id="d5569-103"> Callcenteraufträge erstellen</span><span class="sxs-lookup"><span data-stu-id="d5569-103">Create call center orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="d5569-104">Diese Prozedur führt Sie Schritt für Schritt durch die Suche nach einem Debitor, das Erstellen eines neuen Auftrags, die Suche nach einem Produkt und das Einziehen einer Zahlung vom Debitor.</span><span class="sxs-lookup"><span data-stu-id="d5569-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="d5569-105">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet. Sie ist für den Auftragssachbearbeiter vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="d5569-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="d5569-106">Voraussetzungen: Die Benutzer, welche das Verfahren ausführen, sind als Callcenterbenutzer eingerichtet, und der halbjährliche Fabrikam-Katalog wird mit mindestens einem Quellcode veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="d5569-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="d5569-107">Navigieren Sie zu Einzelhandel und Handel > Kunden > Kundendienst.</span><span class="sxs-lookup"><span data-stu-id="d5569-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="d5569-108">Geben Sie im SearchText-Feld die Suchkriterien ein, um den Debitor zu suchen.</span><span class="sxs-lookup"><span data-stu-id="d5569-108">In the SearchText field, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="d5569-109">Für diese Beispielsprozedur geben Sie "karen" ein und drücken Sie die Taste.</span><span class="sxs-lookup"><span data-stu-id="d5569-109">For this example procedure type in 'karen' and press tab.</span></span>  
3. <span data-ttu-id="d5569-110">Klicken Sie auf "Suchen".</span><span class="sxs-lookup"><span data-stu-id="d5569-110">Click Search.</span></span>
    * <span data-ttu-id="d5569-111">Da nur ein Debitor namens Karen in den Demodaten vorhanden ist, erfolgt die Auswahl automatisch.</span><span class="sxs-lookup"><span data-stu-id="d5569-111">Since there is only one customer named Karen in demo data they will be automatically selected.</span></span>  
4. <span data-ttu-id="d5569-112">Klicken Sie auf "Neuer Auftrag".</span><span class="sxs-lookup"><span data-stu-id="d5569-112">Click New sales order.</span></span>
5. <span data-ttu-id="d5569-113">Erweitern oder reduzieren Sie den Kopfbereich "Auftrag".</span><span class="sxs-lookup"><span data-stu-id="d5569-113">Expand or collapse the Sales order header section.</span></span>
6. <span data-ttu-id="d5569-114">Wählen Sie den Quelltyp für den Katalog aus.</span><span class="sxs-lookup"><span data-stu-id="d5569-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="d5569-115">Wenn keine aktiven Quellcodes vorliegen, können Sie das Quellfeld schließen und diesen Schritt überspringen.</span><span class="sxs-lookup"><span data-stu-id="d5569-115">If there are no active Source codes you can close the Source field and skip this step.</span></span>  
7. <span data-ttu-id="d5569-116">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="d5569-116">Click Add line.</span></span>
8. <span data-ttu-id="d5569-117">Geben Sie im Feld "Artikelnummer" den Artikelsuchbegriff ein.</span><span class="sxs-lookup"><span data-stu-id="d5569-117">In the Item number field, enter the item search term.</span></span>
    * <span data-ttu-id="d5569-118">Für diese Beispielprozedur geben Sie die Teil-Artikelnummer "8111" ein und drücken Sie die Taste.</span><span class="sxs-lookup"><span data-stu-id="d5569-118">For this sample procedure enter a partial item number of '8111' and press tab.</span></span> <span data-ttu-id="d5569-119">Dadurch wird das Artikelsuchfenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d5569-119">This will pop up the item search window.</span></span>  
9. <span data-ttu-id="d5569-120">Wählen Sie das Produkt aus, das zum Auftrag hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5569-120">Select the product to add to the sales order</span></span>
10. <span data-ttu-id="d5569-121">Geben Sie die Verkaufsmenge ein.</span><span class="sxs-lookup"><span data-stu-id="d5569-121">Enter the sales quantity.</span></span>
11. <span data-ttu-id="d5569-122">Klicken Sie auf Erstellen.</span><span class="sxs-lookup"><span data-stu-id="d5569-122">Click Create.</span></span>
12. <span data-ttu-id="d5569-123">Klicken Sie auf "Abschließen", um die Debitorenzahlung aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="d5569-123">Click Complete to capture the customer payment.</span></span>
13. <span data-ttu-id="d5569-124">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d5569-124">Click Add.</span></span>
    * <span data-ttu-id="d5569-125">Der Hinzufügen-Link ist auf der Registerkarte "Zahlungen".</span><span class="sxs-lookup"><span data-stu-id="d5569-125">The Add link is in the Payments tab.</span></span> <span data-ttu-id="d5569-126">Erweitern Sie die Registerkarte "Zahlungen", wenn sie reduziert ist.</span><span class="sxs-lookup"><span data-stu-id="d5569-126">Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="d5569-127">Wählen Sie die Zahlungsmethode aus.</span><span class="sxs-lookup"><span data-stu-id="d5569-127">Select the payment method.</span></span>
    * <span data-ttu-id="d5569-128">Für diese Prozedur wählen Sie die Bargeldzahlungsmethode aus.</span><span class="sxs-lookup"><span data-stu-id="d5569-128">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="d5569-129">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d5569-129">Close the page.</span></span>
16. <span data-ttu-id="d5569-130">Geben Sie den Betrag ein.</span><span class="sxs-lookup"><span data-stu-id="d5569-130">Enter the amount.</span></span>
    * <span data-ttu-id="d5569-131">Für diese Prozedur geben Sie einen Betrag gleich dem Auftragssaldo ein, der in der Auftrags-Übersichtsseite auf der linken Seite des Betrag-Felds angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d5569-131">For this procedure enter an amount equal to the order balance which can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="d5569-132">Dies ermöglicht Ihnen, den Auftrag als vollständig bezahlt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="d5569-132">This will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="d5569-133">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d5569-133">Click OK.</span></span>
18. <span data-ttu-id="d5569-134">Klicken Sie auf Absenden.</span><span class="sxs-lookup"><span data-stu-id="d5569-134">Click Submit.</span></span>


