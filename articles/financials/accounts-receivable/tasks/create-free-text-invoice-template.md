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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 519d0b0ef8153283aa63bc7fa00b4f4b5283fbc1
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="2bf67-103">Eine Vorlage für Freitextrechnungen erstellen</span><span class="sxs-lookup"><span data-stu-id="2bf67-103">Create a free text invoice template</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2bf67-104">Für diese Erfassung wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="2bf67-104">This recording uses the USMF demo company.</span></span> <span data-ttu-id="2bf67-105">Die Erfassung ist für den Benutzer bestimmt, der für die Verwaltung und für die Verarbeitung von Debitorenrechnungen zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="2bf67-105">The recording is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="2bf67-106">Wechseln Sie zu "Debitoren" Wechseln Sie zu Debitoren > Rechnungen > Wiederkehrende Rechnungen > Vorlage für Freitextrechnungen.</span><span class="sxs-lookup"><span data-stu-id="2bf67-106">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="2bf67-107">Mithilfe dieses Formulars können Sie Freitext-Rechnungsvorlagen erstellen, die Rechnungspositionen, Belastungen, eine Buchhaltungsverteilungsvorlage und Sachkontoinformationen enthalten können.</span><span class="sxs-lookup"><span data-stu-id="2bf67-107">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="2bf67-108">Klicken Sie auf "Neu", um eine neue Vorlage für Freitextrechnungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2bf67-108">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="2bf67-109">Geben Sie im Feld "Vorlage" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="2bf67-109">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="2bf67-110">"Vorlagenname" bezeichnet eindeutig eine Freitext-Rechnungsvorlage.</span><span class="sxs-lookup"><span data-stu-id="2bf67-110">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="2bf67-111">Keine zwei Vorlagen können den gleichen "Vorlagennamen" haben.</span><span class="sxs-lookup"><span data-stu-id="2bf67-111">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="2bf67-112">Geben Sie im Feld "Beschreibung" eine Beschreibung für die Vorlage ein.</span><span class="sxs-lookup"><span data-stu-id="2bf67-112">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="2bf67-113">Erweitern Sie die Registerkarte "Rechnungspositionen".</span><span class="sxs-lookup"><span data-stu-id="2bf67-113">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="2bf67-114">Geben Sie im Feld "Beschreibung" eine Beschreibung der Rechnungsposition ein.</span><span class="sxs-lookup"><span data-stu-id="2bf67-114">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="2bf67-115">Wählen Sie im Feld "Hauptkonto" ein Umsatzerlöskonto aus.</span><span class="sxs-lookup"><span data-stu-id="2bf67-115">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="2bf67-116">Sie können das Gegenbuchungskonto eines Debitorenkredits für den Gesamtrechnungsbetrag auf der Seite "Kundenbuchungsprofile" auswählen.</span><span class="sxs-lookup"><span data-stu-id="2bf67-116">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="2bf67-117">Klicken Sie im Feld "Mehrwertsteuergruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2bf67-117">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2bf67-118">Die Mehrwertsteuergruppe für die aktuelle Rechnungsposition ist die standardmäßige Mehrwertsteuergruppe für das Debitorenkonto.</span><span class="sxs-lookup"><span data-stu-id="2bf67-118">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="2bf67-119">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="2bf67-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="2bf67-120">Wählen Sie im Feld "Artikel-Mehrwertsteuergruppe" die Artikel-Mehrwertsteuergruppe für die aktuelle Rechnungsposition aus.</span><span class="sxs-lookup"><span data-stu-id="2bf67-120">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="2bf67-121">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="2bf67-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="2bf67-122">Geben Sie im Feld "Einzelpreis" den Preis pro Einheit für die Rechnungsposition ein oder zeigen ihn an.</span><span class="sxs-lookup"><span data-stu-id="2bf67-122">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="2bf67-123">Dieser Betrag wird mit dem Feld "Menge" multipliziert, um den Betrag der Rechnungsposition zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="2bf67-123">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="2bf67-124">Fügen Sie der Vorlage für Freitextrechnungen eine neue Position hinzu.</span><span class="sxs-lookup"><span data-stu-id="2bf67-124">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="2bf67-125">Geben Sie im Feld "Beschreibung" eine Beschreibung der Rechnungsposition ein.</span><span class="sxs-lookup"><span data-stu-id="2bf67-125">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="2bf67-126">Wählen Sie im Feld "Hauptkonto" ein Umsatzerlöskonto aus.</span><span class="sxs-lookup"><span data-stu-id="2bf67-126">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="2bf67-127">Sie können das Gegenbuchungskonto eines Debitorenkredits für den Gesamtrechnungsbetrag auf der Seite "Kundenbuchungsprofile" auswählen.</span><span class="sxs-lookup"><span data-stu-id="2bf67-127">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="2bf67-128">Klicken Sie im Feld "Mehrwertsteuergruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2bf67-128">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2bf67-129">Die Mehrwertsteuergruppe für die aktuelle Rechnungsposition ist die standardmäßige Mehrwertsteuergruppe für das Debitorenkonto.</span><span class="sxs-lookup"><span data-stu-id="2bf67-129">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="2bf67-130">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="2bf67-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="2bf67-131">Klicken Sie im Feld "Mehrwertsteuergruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2bf67-131">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2bf67-132">Die Artikel-Mehrwertsteuergruppe für die aktuelle Rechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="2bf67-132">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="2bf67-133">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="2bf67-133">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="2bf67-134">Die Anzahl von Einheiten für die Rechnungsposition eingeben oder anzeigen</span><span class="sxs-lookup"><span data-stu-id="2bf67-134">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="2bf67-135">Diese Zahl wird mit dem Wert im Feld "Einzelpreis" multipliziert, um den Betrag der Rechnungsposition zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="2bf67-135">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="2bf67-136">Dient zum Eingeben oder Anzeigen des Preises je Einheit für die Rechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="2bf67-136">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="2bf67-137">Dieser Betrag wird mit dem Wert im Feld "Menge" multipliziert, um den Betrag der Rechnungsposition zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="2bf67-137">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="2bf67-138">Zeigen Sie die Buchhaltungsverteilungen für eine einzelne Position und alle untergeordneten Positionen an und ändern Sie diese.</span><span class="sxs-lookup"><span data-stu-id="2bf67-138">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="2bf67-139">Buchhaltungsverteilungen definieren, wie ein Betrag kalkuliert wird, beispielsweise wie Umsatzerlöse, Steuern oder Zuschläge auf einer Freitextrechnung kalkuliert werden.</span><span class="sxs-lookup"><span data-stu-id="2bf67-139">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="2bf67-140">Aktualisieren Sie die Buchhaltungsverteilungen für die ausgewählte Rechnungsposition.</span><span class="sxs-lookup"><span data-stu-id="2bf67-140">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="2bf67-141">Klicken Sie auf "Schließen".</span><span class="sxs-lookup"><span data-stu-id="2bf67-141">Click Close.</span></span>


