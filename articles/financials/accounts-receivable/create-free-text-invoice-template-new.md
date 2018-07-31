--- 
title: "Eine Vorlage für Freitextrechnungen erstellen"
description: "Verwenden Sie die folgende Prozedur, um eine Vorlage für Freitext-Serienrechnungen zu erstellen."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f69505f0c6137121cae92d42d052b244326c8436
ms.openlocfilehash: 9b7ce8ba180f67c4a52439f4e03b59f07a71323d
ms.contentlocale: de-de
ms.lasthandoff: 06/28/2018

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="7b68f-103">Eine Vorlage für Freitextrechnungen erstellen</span><span class="sxs-lookup"><span data-stu-id="7b68f-103">Create a free text invoice template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b68f-104">Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="7b68f-104">For this walkthrough, use the USMF demo company.</span></span> <span data-ttu-id="7b68f-105">Die Erfassung ist für den Benutzer bestimmt, der für die Verwaltung und für die Verarbeitung von Debitorenrechnungen zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="7b68f-105">This procedure is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="7b68f-106">Eine Vorlage erstellen</span><span class="sxs-lookup"><span data-stu-id="7b68f-106">Create a template</span></span>

1. <span data-ttu-id="7b68f-107">Wechseln Sie zu "Debitoren" Wechseln Sie zu Debitoren > Rechnungen > Wiederkehrende Rechnungen > Vorlage für Freitextrechnungen.</span><span class="sxs-lookup"><span data-stu-id="7b68f-107">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="7b68f-108">Mithilfe dieses Formulars können Sie Freitext-Rechnungsvorlagen erstellen, die Rechnungspositionen, Belastungen, eine Buchhaltungsverteilungsvorlage und Sachkontoinformationen enthalten können.</span><span class="sxs-lookup"><span data-stu-id="7b68f-108">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="7b68f-109">Klicken Sie auf "Neu", um eine neue Vorlage für Freitextrechnungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7b68f-109">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="7b68f-110">Geben Sie im Feld "Vorlage" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7b68f-110">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="7b68f-111">"Vorlagenname" bezeichnet eindeutig eine Freitext-Rechnungsvorlage.</span><span class="sxs-lookup"><span data-stu-id="7b68f-111">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="7b68f-112">Keine zwei Vorlagen können den gleichen "Vorlagennamen" haben.</span><span class="sxs-lookup"><span data-stu-id="7b68f-112">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="7b68f-113">Geben Sie im Feld "Beschreibung" eine Beschreibung für die Vorlage ein.</span><span class="sxs-lookup"><span data-stu-id="7b68f-113">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="7b68f-114">Erweitern Sie die Registerkarte "Rechnungspositionen".</span><span class="sxs-lookup"><span data-stu-id="7b68f-114">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="7b68f-115">Geben Sie im Feld "Beschreibung" eine Beschreibung der Rechnungsposition ein.</span><span class="sxs-lookup"><span data-stu-id="7b68f-115">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="7b68f-116">Wählen Sie im Feld "Hauptkonto" ein Umsatzerlöskonto aus.</span><span class="sxs-lookup"><span data-stu-id="7b68f-116">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="7b68f-117">Sie können das Gegenbuchungskonto eines Debitorenkredits für den Gesamtrechnungsbetrag auf der Seite "Kundenbuchungsprofile" auswählen.</span><span class="sxs-lookup"><span data-stu-id="7b68f-117">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="7b68f-118">Klicken Sie im Feld "Mehrwertsteuergruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7b68f-118">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7b68f-119">Die Mehrwertsteuergruppe für die aktuelle Rechnungsposition ist die standardmäßige Mehrwertsteuergruppe für das Debitorenkonto.</span><span class="sxs-lookup"><span data-stu-id="7b68f-119">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="7b68f-120">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="7b68f-120">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="7b68f-121">Wählen Sie im Feld "Artikel-Mehrwertsteuergruppe" die Artikel-Mehrwertsteuergruppe für die aktuelle Rechnungsposition aus.</span><span class="sxs-lookup"><span data-stu-id="7b68f-121">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="7b68f-122">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="7b68f-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="7b68f-123">Geben Sie im Feld "Einzelpreis" den Preis pro Einheit für die Rechnungsposition ein oder zeigen ihn an.</span><span class="sxs-lookup"><span data-stu-id="7b68f-123">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="7b68f-124">Dieser Betrag wird mit dem Feld "Menge" multipliziert, um den Betrag der Rechnungsposition zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="7b68f-124">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="7b68f-125">Fügen Sie der Vorlage für Freitextrechnungen eine neue Position hinzu.</span><span class="sxs-lookup"><span data-stu-id="7b68f-125">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="7b68f-126">Geben Sie im Feld "Beschreibung" eine Beschreibung der Rechnungsposition ein.</span><span class="sxs-lookup"><span data-stu-id="7b68f-126">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="7b68f-127">Wählen Sie im Feld "Hauptkonto" ein Umsatzerlöskonto aus.</span><span class="sxs-lookup"><span data-stu-id="7b68f-127">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="7b68f-128">Sie können das Gegenbuchungskonto eines Debitorenkredits für den Gesamtrechnungsbetrag auf der Seite "Kundenbuchungsprofile" auswählen.</span><span class="sxs-lookup"><span data-stu-id="7b68f-128">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="7b68f-129">Klicken Sie im Feld "Mehrwertsteuergruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7b68f-129">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7b68f-130">Die Mehrwertsteuergruppe für die aktuelle Rechnungsposition ist die standardmäßige Mehrwertsteuergruppe für das Debitorenkonto.</span><span class="sxs-lookup"><span data-stu-id="7b68f-130">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="7b68f-131">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="7b68f-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="7b68f-132">Klicken Sie im Feld "Mehrwertsteuergruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7b68f-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7b68f-133">Die Artikel-Mehrwertsteuergruppe für die aktuelle Rechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="7b68f-133">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="7b68f-134">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="7b68f-134">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="7b68f-135">Die Anzahl von Einheiten für die Rechnungsposition eingeben oder anzeigen</span><span class="sxs-lookup"><span data-stu-id="7b68f-135">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="7b68f-136">Diese Zahl wird mit dem Wert im Feld "Einzelpreis" multipliziert, um den Betrag der Rechnungsposition zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="7b68f-136">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="7b68f-137">Dient zum Eingeben oder Anzeigen des Preises je Einheit für die Rechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="7b68f-137">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="7b68f-138">Dieser Betrag wird mit dem Wert im Feld "Menge" multipliziert, um den Betrag der Rechnungsposition zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="7b68f-138">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="7b68f-139">Zeigen Sie die Buchhaltungsverteilungen für eine einzelne Position und alle untergeordneten Positionen an und ändern Sie diese.</span><span class="sxs-lookup"><span data-stu-id="7b68f-139">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="7b68f-140">Buchhaltungsverteilungen definieren, wie ein Betrag kalkuliert wird, beispielsweise wie Umsatzerlöse, Steuern oder Zuschläge auf einer Freitextrechnung kalkuliert werden.</span><span class="sxs-lookup"><span data-stu-id="7b68f-140">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="7b68f-141">Aktualisieren Sie die Buchhaltungsverteilungen für die ausgewählte Rechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="7b68f-141">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="7b68f-142">Klicken Sie auf "Schließen".</span><span class="sxs-lookup"><span data-stu-id="7b68f-142">Click Close.</span></span>

## <a name="save-a-free-text-invoice-as-a-template"></a><span data-ttu-id="7b68f-143">Eine Vorlage für Freitextrechnungen erstellen</span><span class="sxs-lookup"><span data-stu-id="7b68f-143">Save a free text invoice as a template</span></span>
<span data-ttu-id="7b68f-144">Sie können eine vorhandene Freitextrechnung als Vorlage auch speichern.</span><span class="sxs-lookup"><span data-stu-id="7b68f-144">You can also save an existing free text invoice as a template.</span></span> <span data-ttu-id="7b68f-145">Wenn Sie aus der Rechnungsregisterkarte Speichern in Vorlage auswählen, geben Sie einen Namen und eine Beschreibung für die Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="7b68f-145">When you select Save to template from the Invoice tab, provide a name and a description for the template.</span></span> <span data-ttu-id="7b68f-146">Wenn eine Vorlage mit dem Namen bereits vorhanden ist, sehen Sie eine Benachrichtigung, dass eine Vorlage mit diesem Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7b68f-146">If a template with the name already exists, you will see a notification that a template with that name already exists.</span></span> <span data-ttu-id="7b68f-147">Sie können immer noch auf OK klicken, um es zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="7b68f-147">You can still click on Ok to replace it.</span></span> 

