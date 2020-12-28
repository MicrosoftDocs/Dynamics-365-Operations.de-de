---
title: " Callcenteraufträge erstellen"
description: Diese Prozedur führt Sie Schritt für Schritt durch die Suche nach einem Debitor, das Erstellen eines neuen Auftrags, die Suche nach einem Produkt und das Einziehen einer Zahlung vom Debitor.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c875eaa85d9da997b75b296ad9ace99ae1e91798
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594235"
---
# <a name="create-call-center-orders"></a><span data-ttu-id="18244-103"> Callcenteraufträge erstellen</span><span class="sxs-lookup"><span data-stu-id="18244-103">Create call center orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18244-104">Diese Prozedur führt Sie Schritt für Schritt durch die Suche nach einem Debitor, das Erstellen eines neuen Auftrags, die Suche nach einem Produkt und das Einziehen einer Zahlung vom Debitor.</span><span class="sxs-lookup"><span data-stu-id="18244-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="18244-105">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet. Sie ist für den Auftragssachbearbeiter vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="18244-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="18244-106">Voraussetzungen: Die Benutzer, welche das Verfahren ausführen, sind als Callcenterbenutzer eingerichtet, und der halbjährliche Fabrikam-Katalog wird mit mindestens einem Quellcode veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="18244-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="18244-107">Navigieren Sie zu **Retail und Commerce \> Kunden \> Kundendienst**.</span><span class="sxs-lookup"><span data-stu-id="18244-107">Go to **Retail and Commerce \> Customers \> Customer service**.</span></span>
2. <span data-ttu-id="18244-108">Geben Sie im Feld **SearchText** die Suchkriterien ein, um den Debitor zu suchen.</span><span class="sxs-lookup"><span data-stu-id="18244-108">For **SearchText**, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="18244-109">Für diese Beispielsprozedur geben Sie Karen ein und wählen **TAB**.</span><span class="sxs-lookup"><span data-stu-id="18244-109">For this example procedure, enter "Karen" and select **Tab**.</span></span>  
3. <span data-ttu-id="18244-110">Wählen Sie Suchen aus.</span><span class="sxs-lookup"><span data-stu-id="18244-110">Select Search.</span></span>
    * <span data-ttu-id="18244-111">Da nur ein Debitor namens Karen in den Demodaten vorhanden ist, wird das Ergebnis automatisch ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="18244-111">Since there is only one customer named "Karen" in demo data, the result will be automatically selected.</span></span>  
4. <span data-ttu-id="18244-112">**Neuen Auftrag** auswählen.</span><span class="sxs-lookup"><span data-stu-id="18244-112">Select **New sales order**.</span></span>
5. <span data-ttu-id="18244-113">Erweitern oder reduzieren Sie den Kopfbereich **Auftrag**.</span><span class="sxs-lookup"><span data-stu-id="18244-113">Expand or collapse the **Sales order** header section.</span></span>
6. <span data-ttu-id="18244-114">Wählen Sie den Quelltyp für den Katalog aus.</span><span class="sxs-lookup"><span data-stu-id="18244-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="18244-115">Wenn keine aktiven Quellcodes vorliegen, können Sie diesen Schritt überspringen.</span><span class="sxs-lookup"><span data-stu-id="18244-115">If there are no active source codes you can skip this step.</span></span>  
7. <span data-ttu-id="18244-116">Wählen Sie **Position hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="18244-116">Select **Add line**.</span></span>
8. <span data-ttu-id="18244-117">Geben Sie im Feld **Artikelnummer** den Artikelsuchbegriff ein.</span><span class="sxs-lookup"><span data-stu-id="18244-117">For **Item number**, enter the item search term.</span></span>
    * <span data-ttu-id="18244-118">Für diese Beispielprozedur geben Sie eine Artikelnummer 8111 ein und drücken Sie die Registerkarte. Durch diese Aktion wird das Artikelsuchfenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="18244-118">For this sample procedure, enter a partial item number of '8111' and press tab. This action will bring up the item search window.</span></span>  
9. <span data-ttu-id="18244-119">Wählen Sie das Produkt aus, das zum Auftrag hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="18244-119">Select the product to add to the sales order.</span></span>
10. <span data-ttu-id="18244-120">Geben Sie die Verkaufsmenge ein.</span><span class="sxs-lookup"><span data-stu-id="18244-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="18244-121">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="18244-121">Select **Create**.</span></span>
12. <span data-ttu-id="18244-122">Wählen Sie **Abschließen**, um die Debitorenzahlung aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="18244-122">Select **Complete** to capture the customer payment.</span></span>
13. <span data-ttu-id="18244-123">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="18244-123">Select **Add**.</span></span>
    * <span data-ttu-id="18244-124">Der Hinzufügen-Llink  ist die Registerkarte Zahlungen. Erweitern Sie die Registerkarte wenn sie verringert ist.</span><span class="sxs-lookup"><span data-stu-id="18244-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="18244-125">Wählen Sie die Zahlungsmethode aus.</span><span class="sxs-lookup"><span data-stu-id="18244-125">Select the payment method.</span></span>
    * <span data-ttu-id="18244-126">Für diese Prozedur wählen Sie die Bargeldzahlungsmethode aus.</span><span class="sxs-lookup"><span data-stu-id="18244-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="18244-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="18244-127">Close the page.</span></span>
16. <span data-ttu-id="18244-128">Geben Sie den Betrag ein.</span><span class="sxs-lookup"><span data-stu-id="18244-128">Enter the amount.</span></span>
    * <span data-ttu-id="18244-129">Für diese Prozedur geben Sie einen Betrag gleich dem Auftragssaldo ein, der in der Auftrags-Übersichtsseite auf der linken Seite des Betrag-Felds angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="18244-129">For this procedure, enter an amount equal to the order balance that can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="18244-130">Dies Aktion ermöglicht Ihnen, den Auftrag als vollständig bezahlt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="18244-130">This action will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="18244-131">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="18244-131">Select **OK**.</span></span>
18. <span data-ttu-id="18244-132">Wählen Sie **Senden**.</span><span class="sxs-lookup"><span data-stu-id="18244-132">Select **Submit**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18244-133">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="18244-133">Additional resources</span></span>

[<span data-ttu-id="18244-134">Transaktions-E-Mails nach Lieferart anpassen</span><span class="sxs-lookup"><span data-stu-id="18244-134">Customize transactional emails by mode of delivery</span></span>](../customize-email-delivery-mode.md)

[<span data-ttu-id="18244-135">Lieferart in POS ändern</span><span class="sxs-lookup"><span data-stu-id="18244-135">Change mode of delivery in POS</span></span>](../pos-change-delivery-mode.md)

