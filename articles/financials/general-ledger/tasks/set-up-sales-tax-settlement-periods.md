---
title: Mehrwertsteuer-Ausgleichsperioden einrichten
description: Mehrwertsteuer-Abrechnungszeiträume enthalten Informationen über die Periodenintervalle für die die Mehrwertsteuer gemeldet und abgeführt werden muss.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8304d9e8997a5d31740ee1203aa4bf0603014056
ms.sourcegitcommit: d0fa8d0140fa81029527edb317623c1a7737c593
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862987"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="febe4-103">Mehrwertsteuer-Ausgleichsperioden einrichten</span><span class="sxs-lookup"><span data-stu-id="febe4-103">Set up sales tax settlement periods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="febe4-104">Mehrwertsteuer-Abrechnungszeiträume enthalten Informationen über die Periodenintervalle für die die Mehrwertsteuer gemeldet und abgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="febe4-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="febe4-105">Ein Abrechnungsprozess kann für einen Abrechnungszeitraum für ein bestimmtes Datumsintervall ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="febe4-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="febe4-106">Alle Steuercodes, die dem Abrechnungszeitraum zugeordnet sind, werden ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="febe4-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="febe4-107">Je nach den Einstellungen der zugehörigen "Mehrwertsteuerbehörde", werden die Steuerverbindlichkeiten entweder zu einem Kreditor oder auf ein "Hauptbuchkonto" gebucht.</span><span class="sxs-lookup"><span data-stu-id="febe4-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="febe4-108">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="febe4-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="febe4-109">Wechseln Sie zu "Steuer" Wechseln Sie zu "Steuer" > "Indirekte Steuern" > "Mehrwertsteuer" > "Mehrwertsteuer-Abrechnungszeiträume".</span><span class="sxs-lookup"><span data-stu-id="febe4-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="febe4-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="febe4-110">Click New.</span></span>
3. <span data-ttu-id="febe4-111">Geben Sie im Feld "Abrechnungszeitraum" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="febe4-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="febe4-112">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="febe4-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="febe4-113">Wählen Sie im Feld "Behörde" die Mehrwertsteuerbehörde aus, die der Empfänger der Berichte und der Zahlungen in Verbindung mit dem Abrechnungszeitraum ist.</span><span class="sxs-lookup"><span data-stu-id="febe4-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="febe4-114">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="febe4-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="febe4-115">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="febe4-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="febe4-116">Klicken Sie im Feld "Zahlungsbedingungen" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="febe4-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="febe4-117">Die zugehörige Mehrwertsteuerbehörde kann als Kreditor eingerichtet werden und die "Mehrwertsteuerabrechnung" erstellt eine offene Kreditorenrechnung.</span><span class="sxs-lookup"><span data-stu-id="febe4-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="febe4-118">Die "Zahlungsbedingungen" definieren das "Fälligkeitsdatum" für die offene Kreditorenrechnung.</span><span class="sxs-lookup"><span data-stu-id="febe4-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="febe4-119">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="febe4-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="febe4-120">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="febe4-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="febe4-121">Wählen Sie einen Typ für die Abrechnungszeitraumintervalle aus.</span><span class="sxs-lookup"><span data-stu-id="febe4-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="febe4-122">Geben Sie die Anzahl der Periodenintervalleinheiten pro Periode ein.</span><span class="sxs-lookup"><span data-stu-id="febe4-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="febe4-123">So verfügt beispielsweise ein Quartal über 3 Monate.</span><span class="sxs-lookup"><span data-stu-id="febe4-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="febe4-124">Aktivieren oder deaktivieren Sie das Kontrollkästchen "Stapelverarbeitung für die Mehrwertsteuerabrechnung verwenden".</span><span class="sxs-lookup"><span data-stu-id="febe4-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="febe4-125">Der Abrechnungsprozess für den Abrechnungszeitraum kann als Batchauftrag im Hintergrund verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="febe4-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="febe4-126">Das wird für eine große Zahl von Steuertransaktionen innerhalb eines Periodenintervalls empfohlen.</span><span class="sxs-lookup"><span data-stu-id="febe4-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
    > [!NOTE]
    > <span data-ttu-id="febe4-127">Derzeit wird dies in Österreich, Belgien, Spanien, Italien, Japan und den Niederlanden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="febe4-127">Currently this is not supported in Austria, Belgium, Spain, Italy, Japan, and the Netherlands.</span></span>
14. <span data-ttu-id="febe4-128">Aktivieren bzw. deaktivieren Sie das Kontrollkästchen Generieren von Steuerausgleichsbuchungen verhindern.</span><span class="sxs-lookup"><span data-stu-id="febe4-128">Select or clear the Prevent generating offset tax transactions check box.</span></span>
    * <span data-ttu-id="febe4-129">Standardmäßig generiert das System Offsetsteuerbuchungen während des Ausgleichsprozesses, die  Performanceprobleme verursachen können,  wenn es viele Steuerbuchungen innerhalb eines Periodenintervalls gibt.</span><span class="sxs-lookup"><span data-stu-id="febe4-129">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="febe4-130">Aktivieren bzw. deaktivieren Sie dieses Kontrollkästchen, um Steuerausgleichsbuchungen erstellen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="febe4-130">Select this check box to prevent generating offset tax transactions.</span></span>
15. <span data-ttu-id="febe4-131">Erweitern Sie die Registerkarte "Periodenintervalle".</span><span class="sxs-lookup"><span data-stu-id="febe4-131">Expand the Period intervals tab.</span></span>
16. <span data-ttu-id="febe4-132">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="febe4-132">Click Add.</span></span>
17. <span data-ttu-id="febe4-133">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="febe4-133">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="febe4-134">Geben Sie in das Feld "Von Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="febe4-134">In the From date field, enter a date.</span></span>
19. <span data-ttu-id="febe4-135">Geben Sie in das Feld "Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="febe4-135">In the To date field, enter a date.</span></span>
20. <span data-ttu-id="febe4-136">Klicken Sie auf "Neues Periodenintervall".</span><span class="sxs-lookup"><span data-stu-id="febe4-136">Click New period interval.</span></span>
    * <span data-ttu-id="febe4-137">Sobald das erste Periodenintervall eingegeben wurde, können neue Perioden automatisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="febe4-137">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="febe4-138">Sie können nach Bedarf zurückkehren und neue Periodenintervalle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="febe4-138">You can come back and add new period intervals as required.</span></span>  
21. <span data-ttu-id="febe4-139">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="febe4-139">Close the page.</span></span>

