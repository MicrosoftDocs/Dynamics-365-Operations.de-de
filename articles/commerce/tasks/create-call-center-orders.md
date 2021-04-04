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
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ecf6fe97287fcfb3c070215b563542878175789c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264283"
---
# <a name="create-call-center-orders"></a><span data-ttu-id="241b8-103"> Callcenteraufträge erstellen</span><span class="sxs-lookup"><span data-stu-id="241b8-103">Create call center orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="241b8-104">Diese Prozedur führt Sie Schritt für Schritt durch die Suche nach einem Debitor, das Erstellen eines neuen Auftrags, die Suche nach einem Produkt und das Einziehen einer Zahlung vom Debitor.</span><span class="sxs-lookup"><span data-stu-id="241b8-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="241b8-105">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet. Sie ist für den Auftragssachbearbeiter vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="241b8-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="241b8-106">Voraussetzungen: Die Benutzer, welche das Verfahren ausführen, sind als Callcenterbenutzer eingerichtet, und der halbjährliche Fabrikam-Katalog wird mit mindestens einem Quellcode veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="241b8-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="241b8-107">Navigieren Sie zu **Einzelhandel und Handel \> Kunden \> Kundendienst**.</span><span class="sxs-lookup"><span data-stu-id="241b8-107">Go to **Retail and Commerce \> Customers \> Customer service**.</span></span>
2. <span data-ttu-id="241b8-108">Geben Sie im Feld **SearchText** die Suchkriterien ein, um den Debitor zu suchen.</span><span class="sxs-lookup"><span data-stu-id="241b8-108">For **SearchText**, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="241b8-109">Für diese Beispielsprozedur geben Sie Karen ein und wählen **TAB**.</span><span class="sxs-lookup"><span data-stu-id="241b8-109">For this example procedure, enter "Karen" and select **Tab**.</span></span>  
3. <span data-ttu-id="241b8-110">Wählen Sie Suchen aus.</span><span class="sxs-lookup"><span data-stu-id="241b8-110">Select Search.</span></span>
    * <span data-ttu-id="241b8-111">Da nur ein Debitor namens Karen in den Demodaten vorhanden ist, wird das Ergebnis automatisch ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="241b8-111">Since there is only one customer named "Karen" in demo data, the result will be automatically selected.</span></span>  
4. <span data-ttu-id="241b8-112">**Neuen Auftrag** auswählen.</span><span class="sxs-lookup"><span data-stu-id="241b8-112">Select **New sales order**.</span></span>
5. <span data-ttu-id="241b8-113">Erweitern oder reduzieren Sie den Kopfbereich **Auftrag**.</span><span class="sxs-lookup"><span data-stu-id="241b8-113">Expand or collapse the **Sales order** header section.</span></span>
6. <span data-ttu-id="241b8-114">Wählen Sie den Quelltyp für den Katalog aus.</span><span class="sxs-lookup"><span data-stu-id="241b8-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="241b8-115">Wenn keine aktiven Quellcodes vorliegen, können Sie diesen Schritt überspringen.</span><span class="sxs-lookup"><span data-stu-id="241b8-115">If there are no active source codes you can skip this step.</span></span>  
7. <span data-ttu-id="241b8-116">Wählen Sie **Position hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="241b8-116">Select **Add line**.</span></span>
8. <span data-ttu-id="241b8-117">Geben Sie im Feld **Artikelnummer** den Artikelsuchbegriff ein.</span><span class="sxs-lookup"><span data-stu-id="241b8-117">For **Item number**, enter the item search term.</span></span>
    * <span data-ttu-id="241b8-118">Für diese Beispielprozedur geben Sie eine Artikelnummer 8111 ein und drücken Sie die Registerkarte. Durch diese Aktion wird das Artikelsuchfenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="241b8-118">For this sample procedure, enter a partial item number of '8111' and press tab. This action will bring up the item search window.</span></span>  
9. <span data-ttu-id="241b8-119">Wählen Sie das Produkt aus, das zum Auftrag hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="241b8-119">Select the product to add to the sales order.</span></span>
10. <span data-ttu-id="241b8-120">Geben Sie die Verkaufsmenge ein.</span><span class="sxs-lookup"><span data-stu-id="241b8-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="241b8-121">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="241b8-121">Select **Create**.</span></span>
12. <span data-ttu-id="241b8-122">Wählen Sie **Abschließen**, um die Debitorenzahlung aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="241b8-122">Select **Complete** to capture the customer payment.</span></span>
13. <span data-ttu-id="241b8-123">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="241b8-123">Select **Add**.</span></span>
    * <span data-ttu-id="241b8-124">Der Hinzufügen-Llink  ist die Registerkarte Zahlungen. Erweitern Sie die Registerkarte wenn sie verringert ist.</span><span class="sxs-lookup"><span data-stu-id="241b8-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="241b8-125">Wählen Sie die Zahlungsmethode aus.</span><span class="sxs-lookup"><span data-stu-id="241b8-125">Select the payment method.</span></span>
    * <span data-ttu-id="241b8-126">Für diese Prozedur wählen Sie die Bargeldzahlungsmethode aus.</span><span class="sxs-lookup"><span data-stu-id="241b8-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="241b8-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="241b8-127">Close the page.</span></span>
16. <span data-ttu-id="241b8-128">Geben Sie den Betrag ein.</span><span class="sxs-lookup"><span data-stu-id="241b8-128">Enter the amount.</span></span>
    * <span data-ttu-id="241b8-129">Für diese Prozedur geben Sie einen Betrag gleich dem Auftragssaldo ein, der in der Auftrags-Übersichtsseite auf der linken Seite des Betrag-Felds angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="241b8-129">For this procedure, enter an amount equal to the order balance that can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="241b8-130">Dies Aktion ermöglicht Ihnen, den Auftrag als vollständig bezahlt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="241b8-130">This action will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="241b8-131">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="241b8-131">Select **OK**.</span></span>
18. <span data-ttu-id="241b8-132">Wählen Sie **Senden**.</span><span class="sxs-lookup"><span data-stu-id="241b8-132">Select **Submit**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="241b8-133">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="241b8-133">Additional resources</span></span>

[<span data-ttu-id="241b8-134">Transaktions-E-Mails nach Lieferart anpassen</span><span class="sxs-lookup"><span data-stu-id="241b8-134">Customize transactional emails by mode of delivery</span></span>](../customize-email-delivery-mode.md)

[<span data-ttu-id="241b8-135">Lieferart in POS ändern</span><span class="sxs-lookup"><span data-stu-id="241b8-135">Change mode of delivery in POS</span></span>](../pos-change-delivery-mode.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]