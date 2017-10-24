---
title: "Buchhaltungsverteilungen und Erfassungseinträge im untergeordneten Sachkonto für Kreditorenrechnungen"
description: "Mithilfe von Buchhaltungsverteilungen wird definiert, wie ein Betrag kalkuliert wird, beispielsweise wie Ausgaben, Steuern oder Zuschläge auf einer Kreditorenrechnung kalkuliert werden. Jeder Betrag, der kalkuliert werden muss, wenn die Kreditorenrechnung journalisiert wird, enthält eine oder mehrere Buchhaltungsverteilungen."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f8169c32dc47c1635f6d3d00852d14d677678868
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="accounting-distributions-and-subledger-journal-entries-for-vendor-invoices"></a><span data-ttu-id="a6aca-104">Buchhaltungsverteilungen und Erfassungseinträge im untergeordneten Sachkonto für Kreditorenrechnungen</span><span class="sxs-lookup"><span data-stu-id="a6aca-104">Accounting distributions and subledger journal entries for vendor invoices</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a6aca-105">Mithilfe von Buchhaltungsverteilungen wird definiert, wie ein Betrag kalkuliert wird, beispielsweise wie Ausgaben, Steuern oder Zuschläge auf einer Kreditorenrechnung kalkuliert werden.</span><span class="sxs-lookup"><span data-stu-id="a6aca-105">Accounting distributions are used to define how an amount will be accounted for, such as how the expense, tax, or charges will be accounted for on a vendor invoice.</span></span> <span data-ttu-id="a6aca-106">Jeder Betrag, der kalkuliert werden muss, wenn die Kreditorenrechnung journalisiert wird, enthält eine oder mehrere Buchhaltungsverteilungen.</span><span class="sxs-lookup"><span data-stu-id="a6aca-106">Every amount that must be accounted for when the vendor invoice is journalized will have one or more accounting distributions.</span></span> 

<a name="accounting-distributions"></a><span data-ttu-id="a6aca-107">Buchhaltungsverteilungen</span><span class="sxs-lookup"><span data-stu-id="a6aca-107">Accounting distributions</span></span> 
-------------------------

<span data-ttu-id="a6aca-108">Sie können die folgenden Schaltflächen auf der Seite "Kreditorenrechnung" verwenden, um die Buchhaltungsverteilungen für jeden Betrag auf der Kreditorenrechnung anzuzeigen und eventuell zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a6aca-108">You can use the following buttons in the Vendor invoice page to view, and possibly modify, the accounting distributions for each amount on the vendor invoice.</span></span>
-   <span data-ttu-id="a6aca-109">**Beträge verteilen** - Dient zum Anzeigen und Ändern der Buchhaltungsverteilungen für eine einzelne Position und alle untergeordneten Positionen wie Steuern oder Zuschläge.</span><span class="sxs-lookup"><span data-stu-id="a6aca-109">**Distribute amounts** – View and modify the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="a6aca-110">Sie können auch die Buchhaltungsverteilungen für die untergeordnete Position direkt von der Seite "Mehrwertsteuerbuchungen" oder der Seite "Belastungsbuchungen" aus anzeigen und ändern.</span><span class="sxs-lookup"><span data-stu-id="a6aca-110">You can also view and modify the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="a6aca-111">Ändern Sie Kopfzeilenbeträge von Kreditorenrechnungen wie Zuschläge oder Währungsrundungsbeträge.</span><span class="sxs-lookup"><span data-stu-id="a6aca-111">Modify vendor invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="a6aca-112">Ändern Sie Kreditorenrechnungspositionsbeträge.</span><span class="sxs-lookup"><span data-stu-id="a6aca-112">Modify vendor invoice line amounts.</span></span>
-   <span data-ttu-id="a6aca-113">**Verteilungen anzeigen** – Dient zum Anzeigen der Buchhaltungsverteilungen für alle Positionen im Dokument.</span><span class="sxs-lookup"><span data-stu-id="a6aca-113">**View distributions** – View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="a6aca-114">Sie können die Buchhaltungsverteilungen in dieser Ansicht nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="a6aca-114">You cannot modify the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="a6aca-115">Zeigen Sie die Kopfzeilen- und Positionsbeträge an.</span><span class="sxs-lookup"><span data-stu-id="a6aca-115">View header and line amounts.</span></span>

<span data-ttu-id="a6aca-116">Wenn die Kreditorenrechnung sich auf eine Bestellung bezieht, können Sie die Buchhaltungsverteilungen für Positionen unterteilen und ändern, die einen Artikel enthalten, der nicht gelagert ist.</span><span class="sxs-lookup"><span data-stu-id="a6aca-116">If the vendor invoice references a purchase order, you can split and modify the accounting distributions for lines that contain an item that is not stocked.</span></span> <span data-ttu-id="a6aca-117">Wenn die Kreditorenrechnungsposition auf keine Bestellposition verweist, können Sie eine Buchhaltungsverteilung auch löschen.</span><span class="sxs-lookup"><span data-stu-id="a6aca-117">If the vendor invoice line does not reference a purchase order line, you can also delete an accounting distribution.</span></span> <span data-ttu-id="a6aca-118">Sie können Positionen für Belastungen, Steuern und Positionsrabatte nicht aufteilen oder löschen.</span><span class="sxs-lookup"><span data-stu-id="a6aca-118">You cannot split or delete lines for charges, taxes, and line discounts.</span></span> <span data-ttu-id="a6aca-119">Sie können das Sachkonto ändern, aber Sie können die Beträge oder Prozentsätze nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="a6aca-119">You can modify the ledger account, but you cannot change the amounts or percentages.</span></span>
> [!NOTE]                                                                                                                                 
> <span data-ttu-id="a6aca-120">Wenn die übergeordnete Position einen Artikel enthält, der nicht auf Lager ist, und die Buchhaltungsverteilungen aufgeteilt werden, wird die untergeordnete Position automatisch aufgeteilt, damit sie den Finanzdimensionen der übergeordneten Position entspricht.</span><span class="sxs-lookup"><span data-stu-id="a6aca-120">If the parent line contains an item that is not stocked and the accounting distributions are split, the child line will be split automatically to match the financial dimensions of the parent line.</span></span> <span data-ttu-id="a6aca-121">Die Buchhaltungsverteilungen für die untergeordnete Position können nicht zusätzlich aufgeteilt oder gelöscht werden. Je nach den Einstellungen der untergeordneten Position ist es jedoch eventuell möglich, das Sachkonto für die Buchhaltungsverteilungen der untergeordneten Position zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a6aca-121">The accounting distributions for the child line cannot be additionally split or deleted, but depending on the setup of the child line, you might be able to modify the ledger account for the accounting distributions of the child line.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="a6aca-122">Beträge verteilen</span><span class="sxs-lookup"><span data-stu-id="a6aca-122">Distributing amounts</span></span>
<span data-ttu-id="a6aca-123">Wenn Sie eine Kreditorenrechnung eingeben, wird jeder Betrag wie folgt verteilt.</span><span class="sxs-lookup"><span data-stu-id="a6aca-123">When you enter a vendor invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a6aca-124">Typ der Kreditorenrechnungsposition</span><span class="sxs-lookup"><span data-stu-id="a6aca-124">Type of vendor invoice line</span></span></th>
<th><span data-ttu-id="a6aca-125">Prioritätsreihenfolge, die bestimmt, von wo aus das Hauptkonto angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="a6aca-125">Order of priority that determines where the main account is displayed from</span></span></th>
<th><span data-ttu-id="a6aca-126">Prioritätsreihenfolge, die bestimmt, welche standardmäßige Finanzdimension angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="a6aca-126">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a6aca-127">Produkt auf Lager</span><span class="sxs-lookup"><span data-stu-id="a6aca-127">Stocked product</span></span></td>
<td><ol>
<li><span data-ttu-id="a6aca-128">Die Buchhaltungsverteilung für die Bestellposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-128">The accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="a6aca-129">Das Feld "Hauptkonto", wenn "Einkaufswendungen für Produkt" auf der Seite "Buchung" ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="a6aca-129">The Main account field when Purchase expenditure for product is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="a6aca-130">Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-130">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="a6aca-131">Verwenden Sie die standardmäßigen Finanzdimensionswerte in der Kreidtorenrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-131">Use the default financial dimension values on the vendor invoice.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6aca-132">Eine Beschaffungskategorie oder ein nicht gelagertes Produkt</span><span class="sxs-lookup"><span data-stu-id="a6aca-132">A procurement category or a product that is not stocked</span></span></td>
<td><ol>
<li><span data-ttu-id="a6aca-133">Die Buchhaltungsverteilung für die Bestellposition, wenn die Kreditorenrechnung auf eine Bestellposition verweist.</span><span class="sxs-lookup"><span data-stu-id="a6aca-133">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="a6aca-134">Das Feld "Hauptkonto", wenn "Einkaufsaufwendungen für Ausgaben" auf der Seite "Buchung" ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="a6aca-134">The Main account field when Purchase expenditure for expense is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="a6aca-135">Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-135">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="a6aca-136">Wenn das Hauptkonto ein Zuordnungskonto ist, verwenden Sie den Standardwert der Zuweisungskontodefinition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-136">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="a6aca-137">Verwenden Sie die standardmäßigen Finanzdimensionswerte in der Kreidtorenrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-137">Use the default financial dimension values on the vendor invoice.</span></span></li>
<li><span data-ttu-id="a6aca-138">Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-138">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="a6aca-139">Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite "Kontenplan".</span><span class="sxs-lookup"><span data-stu-id="a6aca-139">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6aca-140">Anlagen</span><span class="sxs-lookup"><span data-stu-id="a6aca-140">Fixed asset</span></span></td>
<td><ol>
<li><span data-ttu-id="a6aca-141">Die Buchhaltungsverteilung für die Bestellposition, wenn die Kreditorenrechnung auf eine Bestellposition verweist.</span><span class="sxs-lookup"><span data-stu-id="a6aca-141">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="a6aca-142">Wenn "Anschaffung" im Feld "Buchungsart" im Formular "Kreditorenrechnung" ausgewählt ist, das Feld "Hauptkonto", wenn "Anschaffung" auf der Seite "Anlagenbuchungsprofile" ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="a6aca-142">If Acquisition is selected in the Transaction type field in the Vendor invoice form, the Main account field when Acquisition is selected in the Fixed asset posting profiles page.</span></span></li>
<li><span data-ttu-id="a6aca-143">Wenn "Anschaffungsänderung" im Feld "Buchungsart" ausgewählt ist, das Feld "Hauptkonto", wenn "Anschaffungsänderung" auf der Seite "Anlagenbuchungsprofile" ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="a6aca-143">If Acquisition adjustment is selected in the Transaction type field, the Main account field when Acquisition adjustment is selected in the Fixed asset posting profiles page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="a6aca-144">Verwenden Sie die Buchhaltungsverteilung für die Bestellposition, wenn die Rechnungsposition auf eine Bestellposition verweist.</span><span class="sxs-lookup"><span data-stu-id="a6aca-144">Use the account distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="a6aca-145">Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-145">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="a6aca-146">Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite "Kontenplan".</span><span class="sxs-lookup"><span data-stu-id="a6aca-146">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6aca-147">Das Projekt, das in der Kreditorenrechnungsposition definiert ist</span><span class="sxs-lookup"><span data-stu-id="a6aca-147">Project defined on the vendor invoice line</span></span></td>
<td><ol>
<li><span data-ttu-id="a6aca-148">Die Buchhaltungsverteilung für die Bestellposition, wenn die Rechnungsposition auf eine Bestellposition verweist.</span><span class="sxs-lookup"><span data-stu-id="a6aca-148">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="a6aca-149">Wenn "Saldo" im Feld "Kosten buchen - Artikel" auf der Seite "Projektgruppen" ausgewählt ist, das Feld "Hauptkonto", wenn "Kosten" auf der Seite "Sachkontobuchungseinstellungen" ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="a6aca-149">If Balance is selected in the Post costs - item field in the Project groups page, the Main account field when Cost is selected in the Ledger posting setup page.</span></span></li>
<li><span data-ttu-id="a6aca-150">Wenn "Gewinn und Verlust" im Feld "Kosten buchen - Artikel" auf der Seite "Projektgruppen" ausgewählt ist, das Feld "Hauptkonto", wenn "Kosten - Artikel" auf der Seite "Sachkontobuchungseinstellungen" ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="a6aca-150">If Profit and loss is selected in the Post costs - item field in the Project groups page, the Main account field when Cost - item is selected in the Ledger posting setup page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="a6aca-151">Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-151">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6aca-152">Positionsrabatt</span><span class="sxs-lookup"><span data-stu-id="a6aca-152">Line discount</span></span></td>
<td><ol>
<li><span data-ttu-id="a6aca-153">Die Buchhaltungsverteilung für die Bestellposition, wenn die Rechnungsposition auf eine Bestellposition verweist.</span><span class="sxs-lookup"><span data-stu-id="a6aca-153">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="a6aca-154">Das Feld "Hauptkonto", wenn "Rabatt" auf der Seite "Buchung" ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="a6aca-154">The Main account field when Discount is selected in the Posting page.</span></span></li>
<li><span data-ttu-id="a6aca-155">Wenn ein Hauptkonto im Buchungsprofil nicht definiert ist, die Buchhaltungsverteilung des erweiterten Preises in der Bestellposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-155">If a main account for a discount is not defined on the posting profile, the accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="a6aca-156">Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-156">If the invoice line references a purchase order line, use the accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="a6aca-157">Verwenden Sie die Finanzdimensionen aus den Buchhaltungsverteilungen für den erweiterten Preis in der Kreditorenrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-157">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="a6aca-158">Verwenden Sie die Finanzdimensionswerte für die Kreditorenrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-158">Use the financial dimension values for the vendor invoice line.</span></span></li>
<li><span data-ttu-id="a6aca-159">Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite "Kontenplan".</span><span class="sxs-lookup"><span data-stu-id="a6aca-159">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6aca-160">"Einkaufskosten", das auf der Registerkarte "Preis und Rabatt" der Bestellposition eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="a6aca-160">Purchase charge, which is entered on the Price and discount tab of the purchase order line</span></span></td>
<td><ol>
<li><span data-ttu-id="a6aca-161">Die Buchhaltungsverteilung für die Bestellposition, wenn die Rechnungsposition auf eine Bestellposition verweist.</span><span class="sxs-lookup"><span data-stu-id="a6aca-161">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="a6aca-162">Die Buchhaltungsverteilung des erweiterten Preises in der Bestellposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-162">The accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="a6aca-163">Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-163">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="a6aca-164">Verwenden Sie die Finanzdimensionen aus den Buchhaltungsverteilungen für den erweiterten Preis in der Kreditorenrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-164">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6aca-165">Positionszuschlag</span><span class="sxs-lookup"><span data-stu-id="a6aca-165">Line charge</span></span></td>
<td><ol>
<li><span data-ttu-id="a6aca-166">Die Buchhaltungsverteilung für die Bestellposition, wenn die Rechnungsposition auf eine Bestellposition verweist.</span><span class="sxs-lookup"><span data-stu-id="a6aca-166">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="a6aca-167">Wenn "Sachkonto" im Feld "Solltyp" im Formular "Belastungscode" ausgewählt ist, das Feld "Sollkonto" auf der Seite "Belastungscode".</span><span class="sxs-lookup"><span data-stu-id="a6aca-167">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="a6aca-168">Wenn "Artikel" im Feld "Solltyp" im Formular "Belastungscode" ausgewählt ist, die Buchhaltungsverteilung für den erweiterten Preis in der Bestellposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-168">If Item is selected in the debit Type field in the Charges code form, the accounting distribution for the extended price on the purchase order line.</span></span></li>
<li><span data-ttu-id="a6aca-169">Wenn "Debitor/Kreditor" im Feld "Solltyp" im Formular "Belastungscode" ausgewählt ist, das Feld "Habenkonto" auf der Seite "Belastungscode".</span><span class="sxs-lookup"><span data-stu-id="a6aca-169">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="a6aca-170">Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-170">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="a6aca-171">Verwenden Sie die Finanzdimensionen aus den Buchhaltungsverteilungen für den erweiterten Preis in der Kreditorenrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-171">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="a6aca-172">Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-172">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="a6aca-173">Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite "Kontenplan".</span><span class="sxs-lookup"><span data-stu-id="a6aca-173">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6aca-174">Steuer, mit der folgenden Bedingung:</span><span class="sxs-lookup"><span data-stu-id="a6aca-174">Tax, with the following condition:</span></span>
<ul>
<li><span data-ttu-id="a6aca-175">Die Option "US-Steuerregeln anwenden" ist auf der Seite "Hauptbuchparameter" ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="a6aca-175">The Apply U.S. taxation rules option is selected in the General ledger parameters page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="a6aca-176">Die Buchhaltungsverteilung für die Bestellposition, wenn die Rechnungsposition auf eine Bestellposition verweist.</span><span class="sxs-lookup"><span data-stu-id="a6aca-176">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="a6aca-177">Die Buchhaltungsverteilungen für den erweiterten Preis oder die Belastung.</span><span class="sxs-lookup"><span data-stu-id="a6aca-177">The accounting distribution of the extended price or charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="a6aca-178">Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-178">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="a6aca-179">Verwenden Sie die Finanzdimensionen aus den Buchhaltungsverteilungen für den erweiterten Preis in der Kreditorenrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-179">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="a6aca-180">Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-180">Use the financial dimension values from the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6aca-181">Steuer, mit den folgenden Bedingungen:</span><span class="sxs-lookup"><span data-stu-id="a6aca-181">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="a6aca-182">Die Option "US-Steuerregeln anwenden" wird auf der Seite "Hauptbuchparameter" deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a6aca-182">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="a6aca-183">Das Feld "Verbrauchssteuer (USA)" für die Mehrwertsteuergruppe wird auf der Seite "Mehrwertsteuergruppen" deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a6aca-183">The Use tax field for the sales tax group is cleared in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="a6aca-184">Wenn der Steuerbetrag wiederherstellbar ist, das Feld "Vorsteuer" auf der Seite "Sachkontobuchungsgruppen".</span><span class="sxs-lookup"><span data-stu-id="a6aca-184">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="a6aca-185">Wenn der Steuerbetrag nicht erstattungsfähig ist, der erweiterte Preis oder die Buchhaltungsverteilung für die Belastung.</span><span class="sxs-lookup"><span data-stu-id="a6aca-185">If the tax amount is not recoverable, the extended price or the accounting distribution for the charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="a6aca-186">Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-186">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="a6aca-187">Verwenden Sie die Finanzdimensionen aus dem erweiterten Preis oder der Buchhaltungsverteilung für die Belastung in der Kreditorenrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-187">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="a6aca-188">Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-188">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="a6aca-189">Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite "Kontenplan".</span><span class="sxs-lookup"><span data-stu-id="a6aca-189">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6aca-190">Steuer, mit den folgenden Bedingungen:</span><span class="sxs-lookup"><span data-stu-id="a6aca-190">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="a6aca-191">Die Option "US-Steuerregeln anwenden" wird auf der Seite "Hauptbuchparameter" deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a6aca-191">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="a6aca-192">Das Feld "Verbrauchssteuer (USA)" für die Mehrwertsteuergruppe wird auf der Seite "Mehrwertsteuergruppen" ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="a6aca-192">The Use tax field for the sales tax group is selected in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="a6aca-193">Wenn der Steuerbetrag wiederherstellbar ist, das Feld "Vorsteuer" auf der Seite "Sachkontobuchungsgruppen".</span><span class="sxs-lookup"><span data-stu-id="a6aca-193">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="a6aca-194">Wenn der Steuerbetrag nicht wiederherstellbar ist, das Feld "Verbrauchssteuerausgaben (USA)" auf der Seite "Sachkontobuchungsgruppen".</span><span class="sxs-lookup"><span data-stu-id="a6aca-194">If the tax amount is not recoverable, the Use tax expense field in the Ledger posting groups page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="a6aca-195">Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-195">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="a6aca-196">Verwenden Sie die Finanzdimensionen aus dem erweiterten Preis oder der Buchhaltungsverteilung für die Belastung in der Kreditorenrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-196">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="a6aca-197">Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-197">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="a6aca-198">Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite "Kontenplan".</span><span class="sxs-lookup"><span data-stu-id="a6aca-198">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6aca-199">Kopfgebühr</span><span class="sxs-lookup"><span data-stu-id="a6aca-199">Header charge</span></span></td>
<td><ol>
<li><span data-ttu-id="a6aca-200">Wenn "Sachkonto" im Feld "Solltyp" im Formular "Belastungscode" ausgewählt ist, das Feld "Sollkonto" auf der Seite "Belastungscode".</span><span class="sxs-lookup"><span data-stu-id="a6aca-200">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="a6aca-201">Wenn "Debitor/Kreditor" im Feld "Solltyp" im Formular "Belastungscode" ausgewählt ist, das Feld "Habenkonto" auf der Seite "Belastungscode".</span><span class="sxs-lookup"><span data-stu-id="a6aca-201">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="a6aca-202">Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-202">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="a6aca-203">Wenn das Hauptkonto ein Zuordnungskonto ist, verwenden Sie den Standardwert der Zuweisungskontodefinition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-203">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="a6aca-204">Verwenden Sie die Finanzdimensionsstandardvorlagewerte aus dem Kreditorenrechnungskopf.</span><span class="sxs-lookup"><span data-stu-id="a6aca-204">Use the financial dimension default template values from the vendor invoice header.</span></span></li>
<li><span data-ttu-id="a6aca-205">Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-205">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="a6aca-206">Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite "Kontenplan".</span><span class="sxs-lookup"><span data-stu-id="a6aca-206">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6aca-207">Kopfrabatt</span><span class="sxs-lookup"><span data-stu-id="a6aca-207">Header discount</span></span></td>
<td><ol>
<li><span data-ttu-id="a6aca-208">Das Feld "Hauptkonto" für die Buchungsart "Kreditorenrechnungsrabatt" auf der Seite "Konten für automatische Buchungen".</span><span class="sxs-lookup"><span data-stu-id="a6aca-208">The Main account field for the Vendor invoice discount posting type in the Accounts for automatic transactions page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="a6aca-209">Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-209">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="a6aca-210">Verwenden Sie die Finanzdimensionen aus den Buchhaltungsverteilungen für den erweiterten Preis in der Kreditorenrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-210">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="a6aca-211">Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="a6aca-211">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="a6aca-212">Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite "Kontenplan".</span><span class="sxs-lookup"><span data-stu-id="a6aca-212">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

 
<a name="distributing-taxes"></a><span data-ttu-id="a6aca-213">Verteilen von Steuern</span><span class="sxs-lookup"><span data-stu-id="a6aca-213">Distributing taxes</span></span>
------------------

<span data-ttu-id="a6aca-214">Buchhaltungsverteilungen für Steuern können erst erstellt werden, nachdem Steuern berechnet wurden.</span><span class="sxs-lookup"><span data-stu-id="a6aca-214">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="a6aca-215">Zum Berechnen der Mehrwertsteuer müssen Sie auf der Seite "Kreditorenrechnung" eine der folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="a6aca-215">To calculate sales taxes, you must complete one of the following tasks in the Vendor invoice page:</span></span>
-   <span data-ttu-id="a6aca-216">Zeigen Sie die Rechnungssumme an.</span><span class="sxs-lookup"><span data-stu-id="a6aca-216">View the invoice total.</span></span>
-   <span data-ttu-id="a6aca-217">Zeigen Sie den Mehrwertsteuercode an.</span><span class="sxs-lookup"><span data-stu-id="a6aca-217">View the sales tax.</span></span>
-   <span data-ttu-id="a6aca-218">Zeigen Sie die Erfassung im untergeordneten Sachkonto an.</span><span class="sxs-lookup"><span data-stu-id="a6aca-218">View the subledger journal.</span></span>
-   <span data-ttu-id="a6aca-219">Zeigen Sie die Ansichtsbuchhaltungsverteilungen für die vollständige Kreditorenrechnung an.</span><span class="sxs-lookup"><span data-stu-id="a6aca-219">View accounting distributions for the complete vendor invoice.</span></span>
-   <span data-ttu-id="a6aca-220">Sperren Sie die Kreditorenrechnung.</span><span class="sxs-lookup"><span data-stu-id="a6aca-220">Place the vendor invoice on hold.</span></span>
-   <span data-ttu-id="a6aca-221">Buchen Sie die Kreditorenrechnung.</span><span class="sxs-lookup"><span data-stu-id="a6aca-221">Post the vendor invoice.</span></span>

## <a name="subledger-journals-for-vendor-invoices"></a><span data-ttu-id="a6aca-222">Untergeordnete Sachkonten für Kreditorenrechnungen</span><span class="sxs-lookup"><span data-stu-id="a6aca-222">Subledger journals for vendor invoices</span></span>
<span data-ttu-id="a6aca-223">Bevor Sie eine Kreditorenrechnung buchen, können Sie den vollständigen Buchhaltungseintrag der Rechnung anzeigen, der Soll- und Habenbeträge enthält, um sicherzustellen, dass die Rechnung auf die richtigen Konten gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="a6aca-223">Before you post a vendor invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="a6aca-224">Diese Ansicht des vollständigen Buchhaltungseintrags wird als Erfassung im untergeordneten Sachkonto bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a6aca-224">This view of the full accounting entry is called a subledger journal.</span></span> 

<span data-ttu-id="a6aca-225">Wenn der Erfassungseintrag im untergeordneten Sachkonto falsch ist, wenn Sie ihn in der Vorschau anzeigen, bevor Sie die Kreditorenrechnung journalisieren, können Sie den Erfassungseintrag im untergeordneten Sachkonto nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="a6aca-225">If the subledger journal entry is incorrect when you preview it before you journalize the vendor invoice, you cannot modify the subledger journal entry.</span></span> <span data-ttu-id="a6aca-226">Stattdessen müssen Sie die Buchhaltungsverteilungen oder das Buchungsprofil ändern.</span><span class="sxs-lookup"><span data-stu-id="a6aca-226">Instead, you must modify the accounting distributions or the posting profile.</span></span> <span data-ttu-id="a6aca-227">Die Buchhaltungsverteilungen dienen dazu, eine Seite des Buchhaltungseintrags, der Soll- oder Habenbetrag, zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a6aca-227">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="a6aca-228">Der Ausgleichskontoeintrag in der Erfassung im untergeordneten Sachkonto wird aus den Buchungsprofilen erstellt, beispielsweise aus dem Kreditorenkonto oder der Steuer.</span><span class="sxs-lookup"><span data-stu-id="a6aca-228">The offsetting subledger journal account entry is created by using the posting profiles, such as from the vendor account or tax.</span></span>






