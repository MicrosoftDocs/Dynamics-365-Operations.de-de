---
title: "Buchhaltungsverteilungen und Erfassungseinträge im untergeordneten Sachkonto für Freitextrechnungen"
description: "Mithilfe von Buchhaltungsverteilungen wird definiert, wie ein Betrag kalkuliert wird, beispielsweise wie Umsatzerlöse, Steuern oder Zuschläge auf einer Freitextrechnung kalkuliert werden. Jeder Betrag, der kalkuliert werden muss, wenn die Freitextrechnung journalisiert wird, enthält eine oder mehrere Buchhaltungsverteilungen."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ac321e34086e1861b3d8c539fb3ac5f360679d79
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="accounting-distributions-and-subledger-journal-entries-for-free-text-invoices"></a><span data-ttu-id="3cf9e-104">Buchhaltungsverteilungen und Erfassungseinträge im untergeordneten Sachkonto für Freitextrechnungen</span><span class="sxs-lookup"><span data-stu-id="3cf9e-104">Accounting distributions and subledger journal entries for free text invoices</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="3cf9e-105">Mithilfe von Buchhaltungsverteilungen wird definiert, wie ein Betrag kalkuliert wird, beispielsweise wie Umsatzerlöse, Steuern oder Zuschläge auf einer Freitextrechnung kalkuliert werden.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-105">Accounting distributions are used to define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span> <span data-ttu-id="3cf9e-106">Jeder Betrag, der kalkuliert werden muss, wenn die Freitextrechnung journalisiert wird, enthält eine oder mehrere Buchhaltungsverteilungen.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-106">Every amount that must be accounted for when the free text invoice is journalized will have one or more accounting distributions.</span></span>

<a name="accounting-distributions"></a><span data-ttu-id="3cf9e-107">Buchhaltungsverteilungen</span><span class="sxs-lookup"><span data-stu-id="3cf9e-107">Accounting distributions</span></span>
------------------------

<span data-ttu-id="3cf9e-108">Sie können die folgenden Schaltflächen auf der Seite "Freitextrechnung" verwenden, um die Buchhaltungsverteilungen für jeden Betrag auf der Freitextrechnung anzuzeigen und eventuell zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-108">You can use the following buttons in the Free text invoice page to view, and possibly change, the accounting distributions for each amount on the free text invoice.</span></span>

-   <span data-ttu-id="3cf9e-109">**Beträge verteilen**– Dient zum Anzeigen und Ändern der Buchhaltungsverteilungen für eine einzelne Position und alle untergeordneten Positionen wie Steuern oder Belastungen.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-109">**Distribute amounts**—View and change the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="3cf9e-110">Sie können auch die Buchhaltungsverteilungen für die untergeordnete Position direkt von der Seite "Mehrwertsteuerbuchungen" oder der Seite "Belastungsbuchungen" aus anzeigen und ändern.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-110">You can also view and change the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="3cf9e-111">Ändern Sie Kopfzeilenbeträge von Freitextrechnungen wie Zuschläge oder Währungsrundungsbeträge.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-111">Change free text invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="3cf9e-112">Ändern von Freitextrechnungpositionsbeträgen.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-112">Change free text invoice line amounts.</span></span>
-   <span data-ttu-id="3cf9e-113">**Verteilungen anzeigen** – Dient zum Anzeigen der Buchhaltungsverteilungen für alle Positionen im Dokument.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-113">**View distributions**—View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="3cf9e-114">Sie können die Buchhaltungsverteilungen in dieser Ansicht nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-114">You can't change the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="3cf9e-115">Zeigen Sie die Kopfzeilen- und Positionsbeträge an.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-115">View header and line amounts.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="3cf9e-116">Beträge verteilen</span><span class="sxs-lookup"><span data-stu-id="3cf9e-116">Distributing amounts</span></span>
<span data-ttu-id="3cf9e-117">Wenn Sie eine Freitextrechnung eingeben, wird jeder Betrag wie folgt verteilt.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-117">When you enter a free text invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3cf9e-118">Typ des Geldbetrags</span><span class="sxs-lookup"><span data-stu-id="3cf9e-118">Type of monetary amount</span></span></th>
<th><span data-ttu-id="3cf9e-119">Wo das Hauptkonto angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="3cf9e-119">Where the main account is displayed from</span></span></th>
<th><span data-ttu-id="3cf9e-120">Prioritätsreihenfolge, die bestimmt, welche standardmäßige Finanzdimension angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="3cf9e-120">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3cf9e-121">Freitextrechnungsposition</span><span class="sxs-lookup"><span data-stu-id="3cf9e-121">Free text invoice line</span></span></td>
<td><span data-ttu-id="3cf9e-122">Das Sachkonto in der Freitextrechnungsposition</span><span class="sxs-lookup"><span data-stu-id="3cf9e-122">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="3cf9e-123">Wenn das Hauptkonto ein Zuordnungskonto ist, verwenden Sie den Standardwert der Zuweisungskontodefinition.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-123">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="3cf9e-124">Wenn das Hauptkonto kein Zuweisungskonto ist, verwenden Sie die Standardvorlage für Finanzdimensionen in der Freitextrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-124">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="3cf9e-125">Verwenden Sie die standardmäßigen Finanzdimensionswerte in der Freitextrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-125">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="3cf9e-126">Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Sachkonto auf der Seite "Kontenplan".</span><span class="sxs-lookup"><span data-stu-id="3cf9e-126">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cf9e-127">Freitextrechnungsposition für eine Kombination aus Anlagennummer und Wertmodell</span><span class="sxs-lookup"><span data-stu-id="3cf9e-127">Free text invoice line for a fixed asset number and value model combination</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3cf9e-128"><strong>Hinweis </strong></span><span class="sxs-lookup"><span data-stu-id="3cf9e-128"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3cf9e-129">Das Hauptkonto in der Freitextrechnungsposition ist das Anlagenveräußerungskonto.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-129">The main account on the free text invoice line will be the fixed asset disposal account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
<td><span data-ttu-id="3cf9e-130">Das Sachkonto in der Freitextrechnungsposition</span><span class="sxs-lookup"><span data-stu-id="3cf9e-130">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="3cf9e-131">Verwenden Sie die standardmäßigen Finanzdimensionswerte in der Freitextrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-131">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="3cf9e-132">Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Sachkonto auf der Seite "Kontenplan".</span><span class="sxs-lookup"><span data-stu-id="3cf9e-132">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3cf9e-133">Rabattbetrag der Freitextrechnung</span><span class="sxs-lookup"><span data-stu-id="3cf9e-133">Free text invoice discount amount</span></span></td>
<td><span data-ttu-id="3cf9e-134">Das Feld "Hauptkonto für Debitorenrabatte" auf der Skonti Seite.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-134">The Main account for customer discounts field in the Cash discounts page.</span></span></td>
<td><ol>
<li><span data-ttu-id="3cf9e-135">Wenn das Hauptkonto ein Zuordnungskonto ist, verwenden Sie den Standardwert der Zuweisungskontodefinition.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-135">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="3cf9e-136">Wenn das Hauptkonto kein Zuweisungskonto ist, verwenden Sie die Standardvorlage für Finanzdimensionen in der Freitextrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-136">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="3cf9e-137">Verwenden Sie die standardmäßigen Finanzdimensionswerte in der Freitextrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-137">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="3cf9e-138">Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Sachkonto auf der Seite "Kontenplan".</span><span class="sxs-lookup"><span data-stu-id="3cf9e-138">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cf9e-139">Mehrwertsteuerbetrag der Freitextrechnung</span><span class="sxs-lookup"><span data-stu-id="3cf9e-139">Free text invoice sales tax amount</span></span></td>
<td><span data-ttu-id="3cf9e-140">Das Feld Mehrwertsteuer in der Sachkontobuchungsgruppenseite.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-140">The Sales tax payable field in the Ledger posting groups page.</span></span></td>
<td><ol>
<li><span data-ttu-id="3cf9e-141">Verwenden Sie die Finanzdimensionen, die im Freitextrechnungspositionsbetrag oder den Verteilungen für den Positionsbetrag der Zuschläge definiert sind.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-141">Use the financial dimensions that are defined on the free text invoice line amount or the distributions for the charge line amount.</span></span></li>
<li><span data-ttu-id="3cf9e-142">Verwenden Sie die standardmäßigen Finanzdimensionswerte in der Freitextrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-142">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="3cf9e-143">Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Sachkonto auf der Seite "Kontenplan".</span><span class="sxs-lookup"><span data-stu-id="3cf9e-143">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3cf9e-144">Positionsbetrag der Zuschläge der Freitextrechnung</span><span class="sxs-lookup"><span data-stu-id="3cf9e-144">Free text invoice charge line amount</span></span></td>
<td><span data-ttu-id="3cf9e-145">Das Habenkontofeld in der Belastungscodeseite.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-145">The Credit account field in the Charges code page.</span></span></td>
<td><ol>
<li><span data-ttu-id="3cf9e-146">Wenn das Hauptkonto ein Zuordnungskonto ist, verwenden Sie den Standardwert der Zuweisungskontodefinition.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-146">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="3cf9e-147">Wenn das Hauptkonto kein Zuweisungskonto ist, verwenden Sie die Standardvorlage für Finanzdimensionen in der Freitextrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-147">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="3cf9e-148">Verwenden Sie die standardmäßigen Finanzdimensionswerte in der Freitextrechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-148">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="3cf9e-149">Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Sachkonto auf der Seite "Kontenplan".</span><span class="sxs-lookup"><span data-stu-id="3cf9e-149">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a><span data-ttu-id="3cf9e-150">Verteilen von Steuern</span><span class="sxs-lookup"><span data-stu-id="3cf9e-150">Distributing taxes</span></span>
<span data-ttu-id="3cf9e-151">Buchhaltungsverteilungen für Steuern können erst erstellt werden, nachdem Steuern berechnet wurden.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-151">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="3cf9e-152">Zum Berechnen der Mehrwertsteuer müssen Sie auf der Seite "Freitextrechnung" eine der folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="3cf9e-152">To calculate sales taxes, you must complete one of the following tasks in the Free text invoice form:</span></span>
-   <span data-ttu-id="3cf9e-153">Zeigen Sie den Mehrwertsteuercode an.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-153">View the sales tax.</span></span>
-   <span data-ttu-id="3cf9e-154">Zeigen Sie die Rechnungssumme an.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-154">View the invoice total.</span></span>
-   <span data-ttu-id="3cf9e-155">Zeigen Sie den Cashflow an.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-155">View the cash flow.</span></span>
-   <span data-ttu-id="3cf9e-156">Zeigen Sie die Buchhaltungsverteilungen für die gesamte Freitextrechnung an.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-156">View accounting distributions for the whole free text invoice.</span></span>
-   <span data-ttu-id="3cf9e-157">Zeigen Sie die Erfassung im untergeordneten Sachkonto an.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-157">View the subledger journal.</span></span>

## <a name="subledger-journals-for-free-text-invoices"></a><span data-ttu-id="3cf9e-158">Erfassungen im untergeordneten Sachkonto für Freitextrechnungen</span><span class="sxs-lookup"><span data-stu-id="3cf9e-158">Subledger journals for free text invoices</span></span>
<span data-ttu-id="3cf9e-159">Bevor Sie eine Freitextrechnung buchen, können Sie den vollständigen Buchhaltungseintrag der Rechnung anzeigen, der Soll- und Habenbeträge enthält, um sicherzustellen, dass die Rechnung auf die richtigen Konten gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-159">Before you post a free text invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="3cf9e-160">Diese Ansicht des vollständigen Buchhaltungseintrags wird als Erfassung im untergeordneten Sachkonto bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-160">This view of the full accounting entry is called a subledger journal.</span></span> <span data-ttu-id="3cf9e-161">Wenn der Erfassungseintrag im untergeordneten Sachkonto falsch ist, wenn Sie ihn in der Vorschau anzeigen, bevor Sie die Freitextrechnung journalisieren, können Sie den Erfassungseintrag im untergeordneten Sachkonto nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-161">If the subledger journal entry is incorrect when you preview it before you journalize the free text invoice, you can't change the subledger journal entry.</span></span> <span data-ttu-id="3cf9e-162">Stattdessen müssen Sie die Buchhaltungsverteilungen oder das Buchungsprofil ändern.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-162">Instead, you must change the accounting distributions or the posting profile.</span></span> <span data-ttu-id="3cf9e-163">Die Buchhaltungsverteilungen dienen dazu, eine Seite des Buchhaltungseintrags, der Soll- oder Habenbetrag, zu definieren.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-163">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="3cf9e-164">Der Ausgleichskontoeintrag in der Erfassung im untergeordneten Sachkonto wird aus den Buchungsprofilen erstellt, beispielsweise aus dem Debitorenkonto oder der Steuer.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-164">The offsetting subledger journal account entry is created from the posting profiles, such as from the customer account or the tax.</span></span>




