---
title: Rechnungen und Schlüsseldaten im Kreditorsystem überwachen
description: In diesem Thema wird gezeigt, wie Rechnungen und Schlüsseldaten in Kreditorenkonten geprüft werden.
author: saraschi2
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
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5bb89f0adce41b045b1f573c4c0e841f78b2248c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443458"
---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a><span data-ttu-id="90aaa-103">Rechnungen und Schlüsseldaten im Kreditorsystem überwachen</span><span class="sxs-lookup"><span data-stu-id="90aaa-103">Audit invoices and key data in accounts payable</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="90aaa-104">Wenn Sie von einem Kreditor eine Rechnung für die Waren oder Dienstleistungen einer Bestellung erhalten, muss gemäß den Unternehmensrichtlinien möglicherweise zunächst der Eingang der Waren bzw. die Erbringung der Dienstleistungen stattfinden, bevor die Bezahlung der Rechnung genehmigt wird.</span><span class="sxs-lookup"><span data-stu-id="90aaa-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="90aaa-105">Stellen Sie zu Beginn sicher, dass der Konfigurationsschlüssel "Rechnungsabgleich" ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="90aaa-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="90aaa-106">Stellen Sie auf der Seite **Kreditorenparameter** sicher, dass die Option „Rechnungsabgleichüberprüfung aktivieren“ ausgewählt ist, dass das Feld **Rechnung mit Abweichungen buchen** auf **Genehmigung anfordern** festgelegt ist und das Feld **Positionsabgleichsrichtlinie** auf **Dreiseitiger Abgleich** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="90aaa-106">In the **Accounts payable parameters** page, ensure that the Enable invoice matching validation option is selected, the **Post invoice with discrepancies** field is set to **Require approval**, and the **Line matching policy** field is set to **Three-way matching**.</span></span>

<span data-ttu-id="90aaa-107">Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="90aaa-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="90aaa-108">Die Kreditorenleiter- oder Buchhaltungsleiterrolle würde diese Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="90aaa-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="90aaa-109">Eine Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="90aaa-109">Create a purchase order</span></span>
1. <span data-ttu-id="90aaa-110">Wechseln Sie zu **Alle Bestellungen**.</span><span class="sxs-lookup"><span data-stu-id="90aaa-110">Go to **All purchase orders**.</span></span>
2. <span data-ttu-id="90aaa-111">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="90aaa-111">Click **New**.</span></span>
3. <span data-ttu-id="90aaa-112">Geben Sie im Feld **Lieferantenkonto** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="90aaa-112">In the **Vendor account** field, type a value.</span></span>
4. <span data-ttu-id="90aaa-113">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="90aaa-113">Click **OK**.</span></span>
5. <span data-ttu-id="90aaa-114">Klicken Sie auf **Position hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="90aaa-114">Click **Add line**.</span></span>
6. <span data-ttu-id="90aaa-115">Geben Sie im Feld **Artikelnummer** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="90aaa-115">In the **Item number** field, type a value.</span></span>
7. <span data-ttu-id="90aaa-116">Klicken Sie im Aktionsbereich auf **Einkauf**.</span><span class="sxs-lookup"><span data-stu-id="90aaa-116">On the Action Pane, click **Purchase**.</span></span>
8. <span data-ttu-id="90aaa-117">Klicken Sie auf **Bestätigen**.</span><span class="sxs-lookup"><span data-stu-id="90aaa-117">Click **Confirm**.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="90aaa-118">Einen Produktzugang buchen</span><span class="sxs-lookup"><span data-stu-id="90aaa-118">Post a product receipt</span></span>
1. <span data-ttu-id="90aaa-119">Klicken Sie im Aktionsbereich auf **Empfangen**.</span><span class="sxs-lookup"><span data-stu-id="90aaa-119">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="90aaa-120">Klicken Sie auf **Produktzugang**.</span><span class="sxs-lookup"><span data-stu-id="90aaa-120">Click **Product receipt**.</span></span>
3. <span data-ttu-id="90aaa-121">Geben Sie im Feld **Produktzugang** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="90aaa-121">In the **Product receipt** field, type a value.</span></span>
4. <span data-ttu-id="90aaa-122">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="90aaa-122">Click **OK**.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="90aaa-123">Eine Kreditorenrechnung erfassen und einem Produktzugang zuordnen</span><span class="sxs-lookup"><span data-stu-id="90aaa-123">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="90aaa-124">Klicken Sie im Aktionsbereich auf **Rechnung > Rechnung**.</span><span class="sxs-lookup"><span data-stu-id="90aaa-124">On the Action Pane, click **Invoice > Invoice**.</span></span>
2. <span data-ttu-id="90aaa-125">Geben Sie im Feld **Zahl** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="90aaa-125">In the **Number** field, type a value.</span></span>
3. <span data-ttu-id="90aaa-126">Klicken Sie auf **Standard aus: Bestellte Menge** um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="90aaa-126">Click **Default from: Ordered quantity** to open the drop dialog.</span></span>
4. <span data-ttu-id="90aaa-127">Wählen Sie im Feld **Standardmenge für Positionen** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="90aaa-127">In the **Default quantity for lines** field, select an option.</span></span>
5. <span data-ttu-id="90aaa-128">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="90aaa-128">Click **OK**.</span></span>
6. <span data-ttu-id="90aaa-129">Klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="90aaa-129">Click **Yes**.</span></span>
7. <span data-ttu-id="90aaa-130">Klicken Sie auf **Produktzugänge abgleichen**.</span><span class="sxs-lookup"><span data-stu-id="90aaa-130">Click **Match product receipts**.</span></span>
8. <span data-ttu-id="90aaa-131">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="90aaa-131">Click **OK**.</span></span>
9. <span data-ttu-id="90aaa-132">Klicken Sie im Aktionsbereich auf **Überprüfen**.</span><span class="sxs-lookup"><span data-stu-id="90aaa-132">On the Action Pane, click **Review**.</span></span>
10. <span data-ttu-id="90aaa-133">Klicken Sie auf **Detailabgleich**.</span><span class="sxs-lookup"><span data-stu-id="90aaa-133">Click **Matching details**.</span></span>

