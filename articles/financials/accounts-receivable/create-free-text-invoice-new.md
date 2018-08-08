--- 
title: Freitextrechnung erstellen
description: Dieser Artikel zeigt, wie eine Freitext-Debitorenrechnung erstellt wird.
author: mikefalkner
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e6f89a6d77ff8e1cd88632df0d9a72915086ee1e
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---

# <a name="create-a-free-text-invoice"></a><span data-ttu-id="56095-103">Freitextrechnung erstellen</span><span class="sxs-lookup"><span data-stu-id="56095-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56095-104">Dieser Artikel zeigt, wie eine Freitext-Debitorenrechnung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="56095-104">This article demonstrates how to create a free text invoice.</span></span> <span data-ttu-id="56095-105">Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="56095-105">For this procedure, use the USMF demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="56095-106">Freitextrechnung erstellen</span><span class="sxs-lookup"><span data-stu-id="56095-106">Create a free text invoice</span></span>

1. <span data-ttu-id="56095-107">Wechseln Sie zu "Debitoren" > "Rechnungen" > "Alle Freitextrechnungen".</span><span class="sxs-lookup"><span data-stu-id="56095-107">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="56095-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="56095-108">Click New.</span></span>
3. <span data-ttu-id="56095-109">Wählen Sie im Feld "Debitorenkonto" einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="56095-109">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="56095-110">Das Rechnungskonto wird standardmäßig auf dasselbe Konto festgelegt, das für das Debitorenkonto verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="56095-110">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="56095-111">Der Buchhaltungsstatus beginnt mit "In Bearbeitung", wenn die Rechnung nicht gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="56095-111">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="56095-112">Die Rechnungsnummer wird zugewiesen, wenn die Rechnung gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="56095-112">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="56095-113">Wenn Sie SEPA-Vollmachten verwenden, wird das Direkteinzugsmandat automatisch mit einer Vollmacht aufgefüllt, wenn Sie das Debitorenkonto auswählen.</span><span class="sxs-lookup"><span data-stu-id="56095-113">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="56095-114">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="56095-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="56095-115">Geben Sie im Feld "Hauptkonto" eine Kontonummer ohne Dimensionen an.</span><span class="sxs-lookup"><span data-stu-id="56095-115">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="56095-116">Sie können auch ein oder mehrere Zeichen für das Hauptkonto eingeben und die Suche verwenden, um Ihr Konto zu suchen.</span><span class="sxs-lookup"><span data-stu-id="56095-116">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="56095-117">Sie geben Dimensionen später in dieser Anleitung ein.</span><span class="sxs-lookup"><span data-stu-id="56095-117">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="56095-118">Erweitern Sie das Inforegister "Positionsdetails", sodass Sie Ihrem Hauptkonto Dimensionen hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="56095-118">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="56095-119">Klicken Sie auf die Registerkarte "Finanzdimensionsposition".</span><span class="sxs-lookup"><span data-stu-id="56095-119">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="56095-120">Die Dimensionen sind nur für die ausgewählte Position.</span><span class="sxs-lookup"><span data-stu-id="56095-120">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="56095-121">Die Mehrwertsteuergruppe wird vom Debitor aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="56095-121">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="56095-122">Wenn der Debitor keine Mehrwertsteuergruppe hat, wird die Mehrwertsteuergruppe aus dem Hauptkonto verwendet.</span><span class="sxs-lookup"><span data-stu-id="56095-122">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="56095-123">Die Artikel-Mehrwertsteuergruppe wird vom Hauptkonto aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="56095-123">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="56095-124">Wenn das Hauptkonto keine Artikel-Mehrwertsteuergruppe aufweist, wird die Artikel-Mehrwertsteuergruppe in den Mehrwertsteuerparametern für das Hauptbuch verwendet.</span><span class="sxs-lookup"><span data-stu-id="56095-124">If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="56095-125">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="56095-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="56095-126">Die Menge ist optional.</span><span class="sxs-lookup"><span data-stu-id="56095-126">The quantity is optional.</span></span>  
9. <span data-ttu-id="56095-127">Geben Sie im Feld "Preis je Einheit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="56095-127">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="56095-128">Der Preis je Einheit ist optional.</span><span class="sxs-lookup"><span data-stu-id="56095-128">The unit price is optional.</span></span>  
    * <span data-ttu-id="56095-129">Der Betrag wird als Menge mal Preis je Einheit berechnet.</span><span class="sxs-lookup"><span data-stu-id="56095-129">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="56095-130">Sie können diese Berechnung jedoch außer Kraft setzen und einen Betrag eingeben.</span><span class="sxs-lookup"><span data-stu-id="56095-130">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="56095-131">Klicken Sie auf "Mehrwertsteuer", um die Mehrwertsteuer anzuzeigen, die für Ihre Rechnung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="56095-131">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="56095-132">Zeigen Sie die Mehrwertsteuerbeträge auf dieser Seite an oder Sie können die Beträge auf der Registerkarte "Regulierung" überschreiben.</span><span class="sxs-lookup"><span data-stu-id="56095-132">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="56095-133">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="56095-133">Click OK.</span></span>
12. <span data-ttu-id="56095-134">Klicken Sie auf "Belastungen", um der Rechnung eine Belastung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="56095-134">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="56095-135">Geben Sie im Feld "Belastungen" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="56095-135">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="56095-136">Geben Sie im Feld "Wert der Belastungen" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="56095-136">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="56095-137">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="56095-137">Close the page.</span></span>
16. <span data-ttu-id="56095-138">Klicken Sie auf "Summen", um die zusammengefassten Rechnungsdetails und Summen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="56095-138">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="56095-139">Klicken Sie auf "Schließen".</span><span class="sxs-lookup"><span data-stu-id="56095-139">Click Close.</span></span>
18. <span data-ttu-id="56095-140">Klicken Sie zum Buchen der Rechnung auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="56095-140">Click Post to post the invoice.</span></span> <span data-ttu-id="56095-141">Sie können den Vorgang vor dem Buchen abbrechen.</span><span class="sxs-lookup"><span data-stu-id="56095-141">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="56095-142">So ändern Sie den Zeitpunkt für das Drucken von Rechnungen: Wählen Sie "Aktuell" aus, um jede Rechnung zu drucken, wenn sie aktualisiert wird, oder wählen Sie "Danach" aus, um zu drucken, nachdem alle Rechnungen aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="56095-142">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="56095-143">Wenn Sie ändern möchten, wie das Kreditlimit des Debitors vor dem Buchen überprüft wird, ändern Sie den Kreditlimittyp.</span><span class="sxs-lookup"><span data-stu-id="56095-143">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="56095-144">Wenn Sie die Rechnung drucken möchten, wählen Sie "Ja" aus.</span><span class="sxs-lookup"><span data-stu-id="56095-144">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="56095-145">Wenn Sie die Rechnung buchen möchten, wählen Sie "Ja" aus.</span><span class="sxs-lookup"><span data-stu-id="56095-145">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="56095-146">Sie können die Rechnung ohne Buchen drucken.</span><span class="sxs-lookup"><span data-stu-id="56095-146">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="56095-147">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="56095-147">Click OK.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="56095-148">Positionen kopieren</span><span class="sxs-lookup"><span data-stu-id="56095-148">Copy lines</span></span>
<span data-ttu-id="56095-149">Um die Positionen auf der Freitextrechnung zu kopieren, wählen Sie eine oder mehrere Positionen aus und gehen anschließend auf ausgewählte Positionen kopieren.</span><span class="sxs-lookup"><span data-stu-id="56095-149">To copy lines on the free text invoice, select one or more lines and then click Copy selected lines.</span></span> <span data-ttu-id="56095-150">Sie können die Anzahl von Kopien angeben, die Sie erstellen möchten, und Sie können Hinweise und Anhänge kopieren.</span><span class="sxs-lookup"><span data-stu-id="56095-150">You can specify the number of copies that you want to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="56095-151">Sie können die Verteilungen kopieren oder zulassen, dass sie neu erstellt werden, wenn Sie buchen.</span><span class="sxs-lookup"><span data-stu-id="56095-151">You can copy the distributions or allow them to be recreated when you post.</span></span> <span data-ttu-id="56095-152">Anschließend können Sie die Informationen nach Bedarf bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="56095-152">Once you copy the lines, you can edit the information as needed.</span></span> 

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="56095-153">Erstellen einer Vorlage für Freitext-Serienrechnungen</span><span class="sxs-lookup"><span data-stu-id="56095-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="56095-154">Sie können eine Freitext-Rechnung von einer Vorlage erstellen.</span><span class="sxs-lookup"><span data-stu-id="56095-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="56095-155">Wenn Sie Neu von Vorlage aus der Rechnungsregisterkarte auswählen, können Sie einen Vorlagennamen auswählen und der Debitor für die neue Freitextrechnung.</span><span class="sxs-lookup"><span data-stu-id="56095-155">When you select New from template from the Invoice tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="56095-156">Sie können die Standardwerte wie die Zahlungsbedingungen und die Zahlungsmethode der Zahlung auch auswählen oder die Werte verwenden, , die mit der Vorlage gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="56095-156">You can also choose to default values such as the terms of payment and method of payment from the customer or use the values that were saved with the template.</span></span> <span data-ttu-id="56095-157">Eine neue Freitextrechnung wird erstellt und die Werte in dieser Rechnung bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="56095-157">A new free text invoice will be created and you can edit the values in that invoice.</span></span> 


