---
title: Anlagenbudgetbuchungsoptione
description: "In diesem Artikel werden die unterschiedlichen, verfügbaren Methoden beschrieben, um Transaktionen für Anlagen zu erstellen."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 18352ad921c2e2d110a7535f979272685105662f
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="fixed-asset-transaction-options"></a><span data-ttu-id="0ea92-103">Anlagenbudgetbuchungsoptione</span><span class="sxs-lookup"><span data-stu-id="0ea92-103">Fixed asset transaction options</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0ea92-104">In diesem Artikel werden die unterschiedlichen, verfügbaren Methoden beschrieben, um Transaktionen für Anlagen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0ea92-104">This article describes the different methods available to create fixed asset transactions.</span></span>

<span data-ttu-id="0ea92-105">Sie können Anlagen für die Integration in Kreditoren, Debitoren, Beschaffung und Hauptbuch einrichten.</span><span class="sxs-lookup"><span data-stu-id="0ea92-105">You can set up Fixed assets for integration with Accounts payable, Accounts receivable, Procurement and sourcing, and General ledger.</span></span> <span data-ttu-id="0ea92-106">Sie können außerdem Artikel in der Lagerverwaltung in Anlagen übertragen, wenn Sie diese Artikel intern verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="0ea92-106">You can also transfer items in Inventory management to Fixed assets if you want to use those items internally.</span></span>

## <a name="accounts-payable"></a><span data-ttu-id="0ea92-107">Kreditorenkonten</span><span class="sxs-lookup"><span data-stu-id="0ea92-107">Accounts payable</span></span>
<span data-ttu-id="0ea92-108">Sie können Anlagenbuchungen auf der Seite "Alle Journale" eingeben.</span><span class="sxs-lookup"><span data-stu-id="0ea92-108">You can enter Fixed assets transactions in the Journal voucher page.</span></span> <span data-ttu-id="0ea92-109">Diese Seite kann über die Seite "Rechnungserfassung" geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="0ea92-109">This page can be opened from the Invoice journal page.</span></span> <span data-ttu-id="0ea92-110">Sie können die Erfassungsbelegseite aus der Rechnungsgenehmigungserfassungsseite öffnen.</span><span class="sxs-lookup"><span data-stu-id="0ea92-110">You can also open the Journal voucher page from the Invoice approval journal page.</span></span> <span data-ttu-id="0ea92-111">Wählen Sie im Feld "Gegenkontenart" "Anlagen" aus.</span><span class="sxs-lookup"><span data-stu-id="0ea92-111">In the Offset account type field, select Fixed assets.</span></span> <span data-ttu-id="0ea92-112">Wählen Sie dann im Feld "Gegenkonto" eine Anlagennummer aus.</span><span class="sxs-lookup"><span data-stu-id="0ea92-112">Then, in the Offset account field, select a fixed asset number.</span></span> <span data-ttu-id="0ea92-113">Geben Sie auf der Registerkarte "Anlagen" die Werte in den Feldern "Transaktionstyp" und "Buch" ein.</span><span class="sxs-lookup"><span data-stu-id="0ea92-113">On the Fixed assets tab, enter values in the Transaction type and Book fields.</span></span>

## <a name="accounts-receivable"></a><span data-ttu-id="0ea92-114">Debitorenkonten</span><span class="sxs-lookup"><span data-stu-id="0ea92-114">Accounts receivable</span></span>
<span data-ttu-id="0ea92-115">Sie können Anlagenbuchungen auf der Seite "Freitextrechung" eingeben.</span><span class="sxs-lookup"><span data-stu-id="0ea92-115">You can enter Fixed assets transactions in the Free text invoice page.</span></span>  <span data-ttu-id="0ea92-116">In der Freitextrechnungsseite im Rechnungspositionsraster, wählen Sie eine Position aus.</span><span class="sxs-lookup"><span data-stu-id="0ea92-116">In the Free text invoice page, in the Invoice lines grid, select a line item.</span></span> <span data-ttu-id="0ea92-117">Klicken Sie auf das Inforegister "Positionsdetails".</span><span class="sxs-lookup"><span data-stu-id="0ea92-117">Click the Line details FastTab.</span></span> <span data-ttu-id="0ea92-118">Geben Sie die Anlagennummer das Buch für die Abgangsbuchung ein.</span><span class="sxs-lookup"><span data-stu-id="0ea92-118">Enter the fixed asset number and book for the disposal transaction.</span></span> <span data-ttu-id="0ea92-119">Bei Freitextrechnungen lautet die Anlagenbuchungsart stets "Veräußerung".</span><span class="sxs-lookup"><span data-stu-id="0ea92-119">For free text invoices, the fixed asset transaction type is always Disposal - sale.</span></span>

## <a name="procurement-and-sourcing"></a><span data-ttu-id="0ea92-120">Beschaffung</span><span class="sxs-lookup"><span data-stu-id="0ea92-120">Procurement and sourcing</span></span>
<span data-ttu-id="0ea92-121">Sie können Anlagenbuchungen auf der Seite "Bestellung" eingeben.</span><span class="sxs-lookup"><span data-stu-id="0ea92-121">You can enter Fixed assets transactions in the Purchase order page.</span></span> <span data-ttu-id="0ea92-122">Geben Sie die erforderlichen Informationen zum Erstellen einer Bestellung ein, und klicken Sie anschließend auf OK.</span><span class="sxs-lookup"><span data-stu-id="0ea92-122">Enter the required information to create a purchase order, and then click OK.</span></span> <span data-ttu-id="0ea92-123">In der Bestellungsseite klicken Sie auf das Positionsdetail-Inforegister.</span><span class="sxs-lookup"><span data-stu-id="0ea92-123">In the Purchase order page, click the Line details FastTab.</span></span> <span data-ttu-id="0ea92-124">Geben Sie danach auf der Registerkarte "Anlagen" Informationen zur Anlage ein.</span><span class="sxs-lookup"><span data-stu-id="0ea92-124">Then, on the Fixed assets tab, enter information about the fixed asset.</span></span> 

<span data-ttu-id="0ea92-125">Um eine Anschaffungsbuchung für eine vorhandene Anlage zu buchen, geben Sie die Anlagennummer, das Wertmodell und die Buchungsart an.</span><span class="sxs-lookup"><span data-stu-id="0ea92-125">To post an acquisition transaction for an existing fixed asset, specify the fixed asset number, book, and transaction type.</span></span> <span data-ttu-id="0ea92-126">Die Anlage kann nicht gebucht werden, wenn diese Informationen nicht vollständig sind.</span><span class="sxs-lookup"><span data-stu-id="0ea92-126">The fixed asset cannot be posted if any of this information is missing.</span></span> <span data-ttu-id="0ea92-127">Um eine Anschaffungsbuchung für eine neue Anlage zu buchen, aktivieren Sie das Kontrollkästchen "Neue Anlage?", und wählen Sie dann die Anlagengruppe aus, der die neue Anlage zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0ea92-127">To post an acquisition transaction for a new fixed asset, select the New fixed asset? option, and then select the fixed asset group to assign the new asset to.</span></span> <span data-ttu-id="0ea92-128">Für eine Position stehen jedoch keine Anlagenfelder zur Verfügung, wenn die Position in einer Lagersteuerungsgruppe enthalten ist, die ein Lagermodell für Standardkosten verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ea92-128">However, no fixed asset fields are available for a line if the item is in an inventory model group that uses a standard cost inventory model.</span></span> <span data-ttu-id="0ea92-129">Darüber hinaus bestimmen die Optionen, die auf der Seite "Anlagenparameter" definiert werden, ob Sie Anschaffungsbuchungen in den Einkaufsmodulen buchen können.</span><span class="sxs-lookup"><span data-stu-id="0ea92-129">Additionally, the options that are defined in the Fixed assets parameters page determine whether you can post acquisition transactions from the purchasing modules.</span></span> 

<span data-ttu-id="0ea92-130">Wird für die Anschaffung von Anlagen die Bestellungserfassung oder die Erfassung "Lager an Anlagen" verwendet, wirkt sich dies auf den Lagerwert aus.</span><span class="sxs-lookup"><span data-stu-id="0ea92-130">When a purchase order or the Inventory to fixed assets journal is used to acquire fixed assets, the inventory value is affected.</span></span>

## <a name="general-ledger"></a><span data-ttu-id="0ea92-131">Hauptbuch</span><span class="sxs-lookup"><span data-stu-id="0ea92-131">General ledger</span></span>
<span data-ttu-id="0ea92-132">Jede Anlagenbuchungsart kann auf der Seite "Allgemeine Erfassung" gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="0ea92-132">Any fixed asset transaction type can be posted in the General journal page.</span></span> <span data-ttu-id="0ea92-133">Sie können auch Erfassungen in Anlagen verwenden, um Anlagenbuchungen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="0ea92-133">You can also use journals in Fixed assets to post fixed asset transactions.</span></span>

## <a name="options-for-entering-fixed-asset-transaction-types"></a><span data-ttu-id="0ea92-134">Eingabeoptionen für Anlagenbuchungsarten</span><span class="sxs-lookup"><span data-stu-id="0ea92-134">Options for entering fixed asset transaction types</span></span>


| <span data-ttu-id="0ea92-135">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="0ea92-135">Transaction type</span></span>                    | <span data-ttu-id="0ea92-136">Modul</span><span class="sxs-lookup"><span data-stu-id="0ea92-136">Module</span></span>                   | <span data-ttu-id="0ea92-137">Optionen</span><span class="sxs-lookup"><span data-stu-id="0ea92-137">Options</span></span>                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| <span data-ttu-id="0ea92-138">Anschaffung, Anschaffungsregulierung</span><span class="sxs-lookup"><span data-stu-id="0ea92-138">Acquisition, Acquisition adjustment</span></span> | <span data-ttu-id="0ea92-139">Feststehende Inhaltsteile</span><span class="sxs-lookup"><span data-stu-id="0ea92-139">Fixed assets</span></span>             | <span data-ttu-id="0ea92-140">Anlagen, Bestand für Anlagen</span><span class="sxs-lookup"><span data-stu-id="0ea92-140">Fixed assets, Inventory to fixed assets</span></span>   |
|                                     | <span data-ttu-id="0ea92-141">Hauptbuch</span><span class="sxs-lookup"><span data-stu-id="0ea92-141">General ledger</span></span>           | <span data-ttu-id="0ea92-142">Allgemeine Erfassung</span><span class="sxs-lookup"><span data-stu-id="0ea92-142">General journal</span></span>                           |
|                                     | <span data-ttu-id="0ea92-143">Kreditorenkonten</span><span class="sxs-lookup"><span data-stu-id="0ea92-143">Accounts payable</span></span>         | <span data-ttu-id="0ea92-144">Rechnungserfassung und Rechnungsgenehmigungserfassung</span><span class="sxs-lookup"><span data-stu-id="0ea92-144">Invoice journal, Invoice approval journal</span></span> |
|                                     | <span data-ttu-id="0ea92-145">Beschaffung</span><span class="sxs-lookup"><span data-stu-id="0ea92-145">Procurement and sourcing</span></span> | <span data-ttu-id="0ea92-146">Bestellung</span><span class="sxs-lookup"><span data-stu-id="0ea92-146">Purchase order</span></span>                            |
| <span data-ttu-id="0ea92-147">Abschreibung</span><span class="sxs-lookup"><span data-stu-id="0ea92-147">Depreciation</span></span>                        | <span data-ttu-id="0ea92-148">Feststehende Inhaltsteile</span><span class="sxs-lookup"><span data-stu-id="0ea92-148">Fixed assets</span></span>             | <span data-ttu-id="0ea92-149">Feststehende Inhaltsteile</span><span class="sxs-lookup"><span data-stu-id="0ea92-149">Fixed assets</span></span>                              |
|                                     | <span data-ttu-id="0ea92-150">Hauptbuch</span><span class="sxs-lookup"><span data-stu-id="0ea92-150">General ledger</span></span>           | <span data-ttu-id="0ea92-151">Allgemeine Erfassung</span><span class="sxs-lookup"><span data-stu-id="0ea92-151">General journal</span></span>                           |
| <span data-ttu-id="0ea92-152">Abgang</span><span class="sxs-lookup"><span data-stu-id="0ea92-152">Disposal</span></span>                            | <span data-ttu-id="0ea92-153">Anlagevermögen</span><span class="sxs-lookup"><span data-stu-id="0ea92-153">Fixed assets</span></span>             | <span data-ttu-id="0ea92-154">Anlagevermögen</span><span class="sxs-lookup"><span data-stu-id="0ea92-154">Fixed assets</span></span>                              |
| <span data-ttu-id="0ea92-155">** **</span><span class="sxs-lookup"><span data-stu-id="0ea92-155">** **</span></span>                               | <span data-ttu-id="0ea92-156">Hauptbuch</span><span class="sxs-lookup"><span data-stu-id="0ea92-156">General ledger</span></span>           | <span data-ttu-id="0ea92-157">Allgemeine Erfassung</span><span class="sxs-lookup"><span data-stu-id="0ea92-157">General journal</span></span>                           |
| <span data-ttu-id="0ea92-158">** **</span><span class="sxs-lookup"><span data-stu-id="0ea92-158">** **</span></span>                               | <span data-ttu-id="0ea92-159">Debitorenkonten</span><span class="sxs-lookup"><span data-stu-id="0ea92-159">Accounts receivable</span></span>      | <span data-ttu-id="0ea92-160">Freitextrechnung</span><span class="sxs-lookup"><span data-stu-id="0ea92-160">Free text invoice</span></span>                         |



<span data-ttu-id="0ea92-161">Weitere Informationen finden Sie unter [Anlage-Integration](fixed-asset-integration.md).</span><span class="sxs-lookup"><span data-stu-id="0ea92-161">For more information, see [Fixed assets integration](fixed-asset-integration.md).</span></span>




