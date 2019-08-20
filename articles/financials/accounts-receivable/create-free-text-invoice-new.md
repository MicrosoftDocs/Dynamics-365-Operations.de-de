---
title: Freitextrechnungen erstellen
description: In diesem Thema wird erläutert, wie Freitextrechnungen erstellt werden.
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 4498f5c9ce0e3830ffe1857c0363ca962561fc59
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836771"
---
# <a name="create-free-text-invoices"></a><span data-ttu-id="96343-103">Freitextrechnungen erstellen</span><span class="sxs-lookup"><span data-stu-id="96343-103">Create free text invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96343-104">In diesem Thema wird erläutert, wie Freitextrechnungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="96343-104">This topic explains how to create free text invoices.</span></span> <span data-ttu-id="96343-105">Für diese Prozedur wird das Demo-Unternehmen **USMF** verwendet.</span><span class="sxs-lookup"><span data-stu-id="96343-105">For the procedure, use the **USMF** demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="96343-106">Freitextrechnung erstellen</span><span class="sxs-lookup"><span data-stu-id="96343-106">Create a free text invoice</span></span>

1. <span data-ttu-id="96343-107">Wechseln Sie zu **Debitoren \> Rechnungen \> Alle Freitextrechnungen**.</span><span class="sxs-lookup"><span data-stu-id="96343-107">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2. <span data-ttu-id="96343-108">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="96343-108">Select **New**.</span></span>
3. <span data-ttu-id="96343-109">Wählen Sie im Feld **Debitorenkonto** einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="96343-109">In the **Customer account** field, select a value.</span></span>

    * <span data-ttu-id="96343-110">Das Rechnungskonto wird standardmäßig auf dasselbe Konto festgelegt, das für das Rechnungskonto verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="96343-110">By default, the account that is selected as the customer account is used as the invoice account.</span></span>
    * <span data-ttu-id="96343-111">Der Buchhaltungsstatus beginnt mit **In Bearbeitung**, wenn die Rechnung nicht gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="96343-111">If the invoice isn't posted, the accounting status starts with **In process**.</span></span>
    * <span data-ttu-id="96343-112">Die Rechnungsnummer wird zugewiesen, wenn die Rechnung gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="96343-112">The invoice number will be assigned when the invoice is posted.</span></span>
    * <span data-ttu-id="96343-113">Wenn Sie einheitliche Euro-Zahlungsverkehrsraum-Vollmachten (SEPA) verwenden, wird das Direkteinzugsmandat automatisch mit einer Vollmacht aufgefüllt, wenn Sie das Debitorenkonto auswählen.</span><span class="sxs-lookup"><span data-stu-id="96343-113">If you're using Single Euro Payments Area (SEPA) mandates, the direct debit mandate is automatically entered when you select the customer account.</span></span>

4. <span data-ttu-id="96343-114">Geben Sie im Feld **Beschreibung** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="96343-114">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="96343-115">Geben Sie im Feld **Hauptkonto** eine Kontonummer ohne Dimensionen an.</span><span class="sxs-lookup"><span data-stu-id="96343-115">In the **Main account** field, specify an account number that doesn't have dimensions.</span></span> <span data-ttu-id="96343-116">Sie öffnen Finanzdimensionen weiter unten in diesem Handbuch.</span><span class="sxs-lookup"><span data-stu-id="96343-116">You will enter dimensions later in this topic.</span></span>

    <span data-ttu-id="96343-117">Sie können auch ein oder mehrere Zeichen für das Hauptkonto eingeben und die Suche verwenden, um Ihr Konto zu suchen.</span><span class="sxs-lookup"><span data-stu-id="96343-117">You can also enter one or more characters for the main account, and use the lookup to find the account.</span></span>

6. <span data-ttu-id="96343-118">Erweitern Sie das Inforegister **Positionsdetails**, sodass Sie Ihrem Hauptkonto Dimensionen hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="96343-118">Select the **Line details** FastTab to add dimensions to the main account.</span></span>
7. <span data-ttu-id="96343-119">Klicken Sie auf die Registerkarte **Finanzdimensionsposition**.</span><span class="sxs-lookup"><span data-stu-id="96343-119">Select the **Financial dimensions line** tab.</span></span>

    * <span data-ttu-id="96343-120">Die Dimensionen sind nur für die ausgewählte Position.</span><span class="sxs-lookup"><span data-stu-id="96343-120">The dimensions are for the selected line only.</span></span>
    * <span data-ttu-id="96343-121">Die Mehrwertsteuergruppe wird standardmäßig aus dem Debitorendatensatz übernommen.</span><span class="sxs-lookup"><span data-stu-id="96343-121">The sales tax group is filled in from the customer.</span></span> <span data-ttu-id="96343-122">Wenn der Debitor keine Mehrwertsteuergruppe aufweist, wird die Mehrwertsteuergruppe aus dem Hauptkonto verwendet.</span><span class="sxs-lookup"><span data-stu-id="96343-122">If the customer doesn't have a sales tax group, the sales tax group from the main account is used.</span></span>
    * <span data-ttu-id="96343-123">Die Artikel-Mehrwertsteuergruppe wird vom Hauptkonto aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="96343-123">The items sales tax group is filled in from the main account.</span></span> <span data-ttu-id="96343-124">Wenn das Hauptkonto keine Artikel-Mehrwertsteuergruppe aufweist, wird die Artikel-Mehrwertsteuergruppe in den Mehrwertsteuerparametern für das Hauptbuch verwendet.</span><span class="sxs-lookup"><span data-stu-id="96343-124">If the main account doesn't have an item sales tax group, the item sales tax group that is specified in the sales tax parameters in General ledger is used.</span></span>

8. <span data-ttu-id="96343-125">Optional: Geben Sie im Feld **Menge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="96343-125">Optional: In the **Quantity** field, enter a number.</span></span>
9. <span data-ttu-id="96343-126">Optional: Geben Sie im Feld **Einheitspreis** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="96343-126">Optional: In the **Unit price** field, enter a number.</span></span>

    <span data-ttu-id="96343-127">Der Betrag wird als Menge mal Preis je Einheit berechnet.</span><span class="sxs-lookup"><span data-stu-id="96343-127">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="96343-128">Sie können diese Berechnung jedoch außer Kraft setzen und einen Betrag eingeben.</span><span class="sxs-lookup"><span data-stu-id="96343-128">However, you can override that calculation by entering an amount.</span></span>

10. <span data-ttu-id="96343-129">Klicken Sie auf **Mehrwertsteuer**, um die Mehrwertsteuer anzuzeigen, die für Ihre Rechnung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="96343-129">Select **Sales tax** to view the sales tax that is calculated for the invoice.</span></span>

    <span data-ttu-id="96343-130">Zeigen Sie die Mehrwertsteuerbeträge auf dieser Seite an oder Sie können die Beträge auf der Registerkarte **Regulierung** überschreiben.</span><span class="sxs-lookup"><span data-stu-id="96343-130">You can view the sales tax amounts on this page, or you can override the amounts on the **Adjustment** tab.</span></span>

11. <span data-ttu-id="96343-131">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="96343-131">Select **OK**.</span></span>
12. <span data-ttu-id="96343-132">Klicken Sie auf **Belastungen**, um der Rechnung eine Belastung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="96343-132">Select **Charges** to add a charge to the invoice.</span></span>
13. <span data-ttu-id="96343-133">Geben Sie im Feld **Belastungen** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="96343-133">In the **Charges code** field, enter a value.</span></span>
14. <span data-ttu-id="96343-134">Geben Sie im Feld **Wert der Belastungen** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="96343-134">In the **Charges value** field, enter a number.</span></span>
15. <span data-ttu-id="96343-135">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="96343-135">Close the page.</span></span>
16. <span data-ttu-id="96343-136">Klicken Sie auf **Summen**, um die zusammengefassten Rechnungsdetails und Summen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="96343-136">Select **Totals** to view a summary of the invoice details and totals.</span></span>
17. <span data-ttu-id="96343-137">Wählen Sie **Schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="96343-137">Select **Close**.</span></span>
18. <span data-ttu-id="96343-138">Wählen Sie **Buchen** aus, um die Rechnung zu buchen.</span><span class="sxs-lookup"><span data-stu-id="96343-138">Select **Post** to post the invoice.</span></span> <span data-ttu-id="96343-139">Sie haben noch eine Verkaufschance zu stornieren, bevor Sie buchen.</span><span class="sxs-lookup"><span data-stu-id="96343-139">You will still have an opportunity to cancel before you actually post.</span></span>

    * <span data-ttu-id="96343-140">Sie können die Zeit des Rechnungsdruckes zu ändern.</span><span class="sxs-lookup"><span data-stu-id="96343-140">You can change the timing of invoice printing.</span></span> <span data-ttu-id="96343-141">Wählen sie **Aktuell** um jede Rechnung zu drucken, wenn diese aktualisiert wird</span><span class="sxs-lookup"><span data-stu-id="96343-141">Select **Current** to print each invoice as it's updated.</span></span> <span data-ttu-id="96343-142">Wählen Sie **Später**, um alle Rechnungen zu drucken, die aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="96343-142">Select **After** to print after all invoices have been updated.</span></span>
    * <span data-ttu-id="96343-143">Um zu ändern wie die Kreditlimite geprüft wird, bevor die Rechnung gebucht wird, ändern Sie den Wert im Feld **Kreditlimit-Typ**.</span><span class="sxs-lookup"><span data-stu-id="96343-143">To change how the customer's credit limit is verified before the invoice is posted, change the value in the **Credit limit type** field.</span></span>
    * <span data-ttu-id="96343-144">Aktivieren Sie diese Option auf **Ja**, um die Rechnung zu drucken.</span><span class="sxs-lookup"><span data-stu-id="96343-144">To print the invoice, set the option to **Yes**.</span></span>
    * <span data-ttu-id="96343-145">Aktivieren Sie diese Option auf **Ja**, um die Rechnung zu buchen.</span><span class="sxs-lookup"><span data-stu-id="96343-145">To post the invoice, set the option to **Yes**.</span></span> <span data-ttu-id="96343-146">Sie können die Rechnung ohne Buchen drucken.</span><span class="sxs-lookup"><span data-stu-id="96343-146">You can print the invoice without posting it.</span></span>

19. <span data-ttu-id="96343-147">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="96343-147">Select **OK**.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="96343-148">Positionen kopieren</span><span class="sxs-lookup"><span data-stu-id="96343-148">Copy lines</span></span>
<span data-ttu-id="96343-149">Um die Positionen auf der Freitextrechnung zu kopieren, wählen Sie eine oder mehrere Positionen aus und gehen anschließend auf **ausgewählte Positionen kopieren**.</span><span class="sxs-lookup"><span data-stu-id="96343-149">To copy lines on a free text invoice, select one or more lines, and then select **Copy selected lines**.</span></span> <span data-ttu-id="96343-150">Sie können die Anzahl von Kopien angeben, die Sie erstellen möchten, und Sie können Hinweise und Anhänge kopieren.</span><span class="sxs-lookup"><span data-stu-id="96343-150">You can specify the number of copies to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="96343-151">Sie können die Verteilungen kopieren oder zulassen, dass sie neu erstellt werden, wenn Sie buchen.</span><span class="sxs-lookup"><span data-stu-id="96343-151">You can either copy the distributions or let them be re-created when you post.</span></span>

<span data-ttu-id="96343-152">Anschließend können Sie die Informationen nach Bedarf bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="96343-152">After you copy lines, you can edit the information as you require.</span></span>

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="96343-153">Erstellen einer Vorlage für Freitext-Serienrechnungen</span><span class="sxs-lookup"><span data-stu-id="96343-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="96343-154">Sie können eine Freitext-Rechnung von einer Vorlage erstellen.</span><span class="sxs-lookup"><span data-stu-id="96343-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="96343-155">Wenn Sie **Neu von Vorlage** aus der **Rechnungs**registerkarte auswählen, können Sie einen Vorlagennamen gür die neue Freitextrechnung auswählen.</span><span class="sxs-lookup"><span data-stu-id="96343-155">When you select **New from template** on the **Invoice** tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="96343-156">Sie können die Standardwerte wie die Zahlungsbedingungen und die Zahlungsmethode der Zahlung auch auswählen oder die Werte verwenden, , die mit der Vorlage gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="96343-156">Default values, such as the terms of payment and method of payment, can be automatically filled in from the customer, or you can use the values that were saved in the template.</span></span>

<span data-ttu-id="96343-157">Eine neue Freitextrechnung wird erstellt und Sie können die Werte in dieser Rechnung bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="96343-157">A new free text invoice is created, and you can edit the values as you require.</span></span>
