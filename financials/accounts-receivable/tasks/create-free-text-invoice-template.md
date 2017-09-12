--- 
title: "Eine Vorlage für Freitextrechnungen erstellen"
description: "Für diese Erfassung wird das Demo-Unternehmen USMF verwendet."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e9c9811b348d81cd735c5b75ca48e0a56a8d52be
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="62344-103">Eine Vorlage für Freitextrechnungen erstellen</span><span class="sxs-lookup"><span data-stu-id="62344-103">Create a free text invoice template</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="62344-104">Für diese Erfassung wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="62344-104">This recording uses the USMF demo company.</span></span> <span data-ttu-id="62344-105">Die Erfassung ist für den Benutzer bestimmt, der für die Verwaltung und für die Verarbeitung von Debitorenrechnungen zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="62344-105">The recording is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="62344-106">Wechseln Sie zu "Debitoren" Wechseln Sie zu Debitoren > Rechnungen > Wiederkehrende Rechnungen > Vorlage für Freitextrechnungen.</span><span class="sxs-lookup"><span data-stu-id="62344-106">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="62344-107">Mithilfe dieses Formulars können Sie Freitext-Rechnungsvorlagen erstellen, die Rechnungspositionen, Belastungen, eine Buchhaltungsverteilungsvorlage und Sachkontoinformationen enthalten können.</span><span class="sxs-lookup"><span data-stu-id="62344-107">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="62344-108">Klicken Sie auf "Neu", um eine neue Vorlage für Freitextrechnungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="62344-108">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="62344-109">Geben Sie im Feld "Vorlage" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="62344-109">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="62344-110">"Vorlagenname" bezeichnet eindeutig eine Freitext-Rechnungsvorlage.</span><span class="sxs-lookup"><span data-stu-id="62344-110">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="62344-111">Keine zwei Vorlagen können den gleichen "Vorlagennamen" haben.</span><span class="sxs-lookup"><span data-stu-id="62344-111">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="62344-112">Geben Sie im Feld "Beschreibung" eine Beschreibung für die Vorlage ein.</span><span class="sxs-lookup"><span data-stu-id="62344-112">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="62344-113">Erweitern Sie die Registerkarte "Rechnungspositionen".</span><span class="sxs-lookup"><span data-stu-id="62344-113">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="62344-114">Geben Sie im Feld "Beschreibung" eine Beschreibung der Rechnungsposition ein.</span><span class="sxs-lookup"><span data-stu-id="62344-114">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="62344-115">Wählen Sie im Feld "Hauptkonto" ein Umsatzerlöskonto aus.</span><span class="sxs-lookup"><span data-stu-id="62344-115">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="62344-116">Sie können das Gegenbuchungskonto eines Debitorenkredits für den Gesamtrechnungsbetrag auf der Seite "Kundenbuchungsprofile" auswählen.</span><span class="sxs-lookup"><span data-stu-id="62344-116">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="62344-117">Klicken Sie im Feld "Mehrwertsteuergruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="62344-117">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="62344-118">Die Mehrwertsteuergruppe für die aktuelle Rechnungsposition ist die standardmäßige Mehrwertsteuergruppe für das Debitorenkonto.</span><span class="sxs-lookup"><span data-stu-id="62344-118">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="62344-119">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="62344-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="62344-120">Wählen Sie im Feld "Artikel-Mehrwertsteuergruppe" die Artikel-Mehrwertsteuergruppe für die aktuelle Rechnungsposition aus.</span><span class="sxs-lookup"><span data-stu-id="62344-120">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="62344-121">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="62344-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="62344-122">Geben Sie im Feld "Einzelpreis" den Preis pro Einheit für die Rechnungsposition ein oder zeigen ihn an.</span><span class="sxs-lookup"><span data-stu-id="62344-122">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="62344-123">Dieser Betrag wird mit dem Feld "Menge" multipliziert, um den Betrag der Rechnungsposition zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="62344-123">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="62344-124">Fügen Sie der Vorlage für Freitextrechnungen eine neue Position hinzu.</span><span class="sxs-lookup"><span data-stu-id="62344-124">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="62344-125">Geben Sie im Feld "Beschreibung" eine Beschreibung der Rechnungsposition ein.</span><span class="sxs-lookup"><span data-stu-id="62344-125">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="62344-126">Wählen Sie im Feld "Hauptkonto" ein Umsatzerlöskonto aus.</span><span class="sxs-lookup"><span data-stu-id="62344-126">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="62344-127">Sie können das Gegenbuchungskonto eines Debitorenkredits für den Gesamtrechnungsbetrag auf der Seite "Kundenbuchungsprofile" auswählen.</span><span class="sxs-lookup"><span data-stu-id="62344-127">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="62344-128">Klicken Sie im Feld "Mehrwertsteuergruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="62344-128">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="62344-129">Die Mehrwertsteuergruppe für die aktuelle Rechnungsposition ist die standardmäßige Mehrwertsteuergruppe für das Debitorenkonto.</span><span class="sxs-lookup"><span data-stu-id="62344-129">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="62344-130">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="62344-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="62344-131">Klicken Sie im Feld "Mehrwertsteuergruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="62344-131">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="62344-132">Die Artikel-Mehrwertsteuergruppe für die aktuelle Rechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="62344-132">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="62344-133">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="62344-133">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="62344-134">Die Anzahl von Einheiten für die Rechnungsposition eingeben oder anzeigen</span><span class="sxs-lookup"><span data-stu-id="62344-134">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="62344-135">Diese Zahl wird mit dem Wert im Feld "Einzelpreis" multipliziert, um den Betrag der Rechnungsposition zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="62344-135">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="62344-136">Dient zum Eingeben oder Anzeigen des Preises je Einheit für die Rechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="62344-136">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="62344-137">Dieser Betrag wird mit dem Wert im Feld "Menge" multipliziert, um den Betrag der Rechnungsposition zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="62344-137">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="62344-138">Zeigen Sie die Buchhaltungsverteilungen für eine einzelne Position und alle untergeordneten Positionen an und ändern Sie diese.</span><span class="sxs-lookup"><span data-stu-id="62344-138">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="62344-139">Buchhaltungsverteilungen definieren, wie ein Betrag kalkuliert wird, beispielsweise wie Umsatzerlöse, Steuern oder Zuschläge auf einer Freitextrechnung kalkuliert werden.</span><span class="sxs-lookup"><span data-stu-id="62344-139">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="62344-140">Aktualisieren Sie die Buchhaltungsverteilungen für die ausgewählte Rechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="62344-140">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="62344-141">Klicken Sie auf "Schließen".</span><span class="sxs-lookup"><span data-stu-id="62344-141">Click Close.</span></span>


