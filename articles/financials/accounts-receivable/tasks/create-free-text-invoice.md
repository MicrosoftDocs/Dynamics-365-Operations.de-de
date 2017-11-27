--- 
title: Freitextrechnung erstellen
description: Diese Aufgabenanleitung veranschaulicht das Erstellen einer Freitextrechnung.
author: mikefalkner
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ef3cad6538d9efbd1c1881f4b7d771382d9b1ba8
ms.openlocfilehash: 87e293008fd748aa0dcc6b3caa94a4889bed35de
ms.contentlocale: de-de
ms.lasthandoff: 10/26/2017

---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="f2d2b-103">Freitextrechnung erstellen</span><span class="sxs-lookup"><span data-stu-id="f2d2b-103">Create a free text invoice</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2d2b-104">Diese Aufgabenanleitung veranschaulicht das Erstellen einer Freitextrechnung.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-104">This task guide demonstrates creating a free text invoice.</span></span> <span data-ttu-id="f2d2b-105">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="f2d2b-106">Wechseln Sie zu "Debitoren" > "Rechnungen" > "Alle Freitextrechnungen".</span><span class="sxs-lookup"><span data-stu-id="f2d2b-106">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="f2d2b-107">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f2d2b-107">Click New.</span></span>
3. <span data-ttu-id="f2d2b-108">Wählen Sie im Feld "Debitorenkonto" einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-108">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="f2d2b-109">Das Rechnungskonto wird standardmäßig auf dasselbe Konto festgelegt, das für das Debitorenkonto verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-109">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="f2d2b-110">Der Buchhaltungsstatus beginnt mit "In Bearbeitung", wenn die Rechnung nicht gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-110">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="f2d2b-111">Die Rechnungsnummer wird zugewiesen, wenn die Rechnung gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-111">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="f2d2b-112">Wenn Sie SEPA-Vollmachten verwenden, wird das Direkteinzugsmandat automatisch mit einer Vollmacht aufgefüllt, wenn Sie das Debitorenkonto auswählen.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-112">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="f2d2b-113">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f2d2b-114">Geben Sie im Feld "Hauptkonto" eine Kontonummer ohne Dimensionen an.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-114">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="f2d2b-115">Sie können auch ein oder mehrere Zeichen für das Hauptkonto eingeben und die Suche verwenden, um Ihr Konto zu suchen.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-115">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="f2d2b-116">Sie geben Dimensionen später in dieser Anleitung ein.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-116">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="f2d2b-117">Erweitern Sie das Inforegister "Positionsdetails", sodass Sie Ihrem Hauptkonto Dimensionen hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-117">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="f2d2b-118">Klicken Sie auf die Registerkarte "Finanzdimensionsposition".</span><span class="sxs-lookup"><span data-stu-id="f2d2b-118">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="f2d2b-119">Die Dimensionen sind nur für die ausgewählte Position.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-119">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="f2d2b-120">Die Mehrwertsteuergruppe wird vom Debitor aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-120">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="f2d2b-121">Wenn der Debitor keine Mehrwertsteuergruppe hat, wird die Mehrwertsteuergruppe aus dem Hauptkonto verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-121">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="f2d2b-122">Die Artikel-Mehrwertsteuergruppe wird vom Hauptkonto aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-122">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="f2d2b-123">Wenn das Hauptkonto keine Artikel-Mehrwertsteuergruppe aufweist, wird die Artikel-Mehrwertsteuergruppe in den Mehrwertsteuerparametern für das Hauptbuch verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-123">If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="f2d2b-124">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-124">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="f2d2b-125">Die Menge ist optional.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-125">The quantity is optional.</span></span>  
9. <span data-ttu-id="f2d2b-126">Geben Sie im Feld "Preis je Einheit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-126">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="f2d2b-127">Der Preis je Einheit ist optional.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-127">The unit price is optional.</span></span>  
    * <span data-ttu-id="f2d2b-128">Der Betrag wird als Menge mal Preis je Einheit berechnet.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-128">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="f2d2b-129">Sie können diese Berechnung jedoch außer Kraft setzen und einen Betrag eingeben.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-129">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="f2d2b-130">Klicken Sie auf "Mehrwertsteuer", um die Mehrwertsteuer anzuzeigen, die für Ihre Rechnung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-130">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="f2d2b-131">Zeigen Sie die Mehrwertsteuerbeträge auf dieser Seite an oder Sie können die Beträge auf der Registerkarte "Regulierung" überschreiben.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-131">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="f2d2b-132">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f2d2b-132">Click OK.</span></span>
12. <span data-ttu-id="f2d2b-133">Klicken Sie auf "Belastungen", um der Rechnung eine Belastung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-133">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="f2d2b-134">Geben Sie im Feld "Belastungen" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-134">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="f2d2b-135">Geben Sie im Feld "Wert der Belastungen" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-135">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="f2d2b-136">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-136">Close the page.</span></span>
16. <span data-ttu-id="f2d2b-137">Klicken Sie auf "Summen", um die zusammengefassten Rechnungsdetails und Summen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-137">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="f2d2b-138">Klicken Sie auf "Schließen".</span><span class="sxs-lookup"><span data-stu-id="f2d2b-138">Click Close.</span></span>
18. <span data-ttu-id="f2d2b-139">Klicken Sie zum Buchen der Rechnung auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="f2d2b-139">Click Post to post the invoice.</span></span> <span data-ttu-id="f2d2b-140">Sie können den Vorgang vor dem Buchen abbrechen.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-140">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="f2d2b-141">So ändern Sie den Zeitpunkt für das Drucken von Rechnungen: Wählen Sie "Aktuell" aus, um jede Rechnung zu drucken, wenn sie aktualisiert wird, oder wählen Sie "Danach" aus, um zu drucken, nachdem alle Rechnungen aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-141">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="f2d2b-142">Wenn Sie ändern möchten, wie das Kreditlimit des Debitors vor dem Buchen überprüft wird, ändern Sie den Kreditlimittyp.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-142">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="f2d2b-143">Wenn Sie die Rechnung drucken möchten, wählen Sie "Ja" aus.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-143">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="f2d2b-144">Wenn Sie die Rechnung buchen möchten, wählen Sie "Ja" aus.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-144">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="f2d2b-145">Sie können die Rechnung ohne Buchen drucken.</span><span class="sxs-lookup"><span data-stu-id="f2d2b-145">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="f2d2b-146">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f2d2b-146">Click OK.</span></span>


