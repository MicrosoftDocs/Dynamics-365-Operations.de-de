---
title: Eingang von Kreditorenrechnungen erfassen und mit dem Wareneingang abgleichen
description: Wenn Sie von einem Kreditor eine Rechnung für die Waren oder Dienstleistungen einer Bestellung erhalten, muss gemäß den Unternehmensrichtlinien möglicherweise zunächst der Eingang der Waren bzw. die Erbringung der Dienstleistungen stattfinden, bevor die Bezahlung der Rechnung genehmigt wird.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 66d84f497775ce4f988242dd2b327bf4854faef5
ms.sourcegitcommit: ba1c76497acc9afba85257976f0d4e96836871d1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/04/2019
ms.locfileid: "2890418"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a><span data-ttu-id="6416e-103">Eingang von Kreditorenrechnungen erfassen und mit dem Wareneingang abgleichen</span><span class="sxs-lookup"><span data-stu-id="6416e-103">Record vendor invoice and match against received quantity</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6416e-104">Wenn Sie von einem Kreditor eine Rechnung für die Waren oder Dienstleistungen einer Bestellung erhalten, muss gemäß den Unternehmensrichtlinien möglicherweise zunächst der Eingang der Waren bzw. die Erbringung der Dienstleistungen stattfinden, bevor die Bezahlung der Rechnung genehmigt wird.</span><span class="sxs-lookup"><span data-stu-id="6416e-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="6416e-105">Stellen Sie zu Beginn sicher, dass der Konfigurationsschlüssel "Rechnungsabgleich" ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="6416e-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="6416e-106">Stellen Sie auf der Seite "Kreditorenparameter" sicher, dass die Option "Rechnungsabgleichüberprüfung aktivieren" ausgewählt ist, dass das Feld "Rechnung mit Abweichungen buchen" auf "Genehmigung anfordern" fesgelegt ist und das Feld "Positionsabgleichsrichtlinie" auf "Dreiseitiger Abgleich" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6416e-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="6416e-107">Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="6416e-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="6416e-108">Die Kreditorenleiter- oder Buchhaltungsleiterrolle würde diese Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="6416e-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="6416e-109">Eine Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="6416e-109">Create a purchase order</span></span>
1. <span data-ttu-id="6416e-110">Wechseln Sie zu "Alle Bestellungen".</span><span class="sxs-lookup"><span data-stu-id="6416e-110">Go to All purchase orders.</span></span>
2. <span data-ttu-id="6416e-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="6416e-111">Click New.</span></span>
3. <span data-ttu-id="6416e-112">Klicken Sie im Feld "Kreditorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6416e-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6416e-113">Geben Sie im Feld "Kreditorenkonto" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6416e-113">In the Vendor account field, type a value.</span></span>
5. <span data-ttu-id="6416e-114">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="6416e-114">Click OK.</span></span>
6. <span data-ttu-id="6416e-115">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="6416e-115">Click Add line.</span></span>
7. <span data-ttu-id="6416e-116">Geben Sie im Feld "Artikelnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6416e-116">In the Item number field, type a value.</span></span>
8. <span data-ttu-id="6416e-117">Klicken Sie im Aktivitätsbereich auf "Einkauf".</span><span class="sxs-lookup"><span data-stu-id="6416e-117">On the Action Pane, click Purchase.</span></span>
9. <span data-ttu-id="6416e-118">Klicken Sie auf "Bestätigen".</span><span class="sxs-lookup"><span data-stu-id="6416e-118">Click Confirm.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="6416e-119">Einen Produktzugang buchen</span><span class="sxs-lookup"><span data-stu-id="6416e-119">Post a product receipt</span></span>
1. <span data-ttu-id="6416e-120">Klicken Sie im Aktivitätsbereich auf "Empfangen".</span><span class="sxs-lookup"><span data-stu-id="6416e-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="6416e-121">Klicken Sie auf "Produktzugang".</span><span class="sxs-lookup"><span data-stu-id="6416e-121">Click Product receipt.</span></span>
3. <span data-ttu-id="6416e-122">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="6416e-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="6416e-123">Geben Sie im Feld "Produktzugang" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6416e-123">In the Product receipt field, type a value.</span></span>
5. <span data-ttu-id="6416e-124">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="6416e-124">Click OK.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="6416e-125">Eine Kreditorenrechnung erfassen und einem Produktzugang zuordnen</span><span class="sxs-lookup"><span data-stu-id="6416e-125">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="6416e-126">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="6416e-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="6416e-127">Klicken Sie auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="6416e-127">Click Invoice.</span></span>
3. <span data-ttu-id="6416e-128">Geben Sie im Feld "Zahl" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6416e-128">In the Number field, type a value.</span></span>
4. <span data-ttu-id="6416e-129">Klicken Sie auf "Standard" aus: "Bestellte Menge" um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6416e-129">Click Default from: Ordered quantity to open the drop dialog.</span></span>
5. <span data-ttu-id="6416e-130">Wählen Sie im Feld "Standardmenge für Positionen" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="6416e-130">In the Default quantity for lines field, select an option.</span></span>
6. <span data-ttu-id="6416e-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="6416e-131">Click OK.</span></span>
7. <span data-ttu-id="6416e-132">Klicken Sie auf „Ja“.</span><span class="sxs-lookup"><span data-stu-id="6416e-132">Click Yes.</span></span>
8. <span data-ttu-id="6416e-133">Klicken Sie auf "Produktzugänge abgleichen".</span><span class="sxs-lookup"><span data-stu-id="6416e-133">Click Match product receipts.</span></span>
9. <span data-ttu-id="6416e-134">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="6416e-134">Click OK.</span></span>
10. <span data-ttu-id="6416e-135">Klicken Sie im Aktivitätsbereich auf "Überprüfen".</span><span class="sxs-lookup"><span data-stu-id="6416e-135">On the Action Pane, click Review.</span></span>
11. <span data-ttu-id="6416e-136">Klicken Sie auf "Detailabgleich".</span><span class="sxs-lookup"><span data-stu-id="6416e-136">Click Matching details.</span></span>
