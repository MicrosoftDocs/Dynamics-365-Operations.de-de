--- 
title: Mehrwertsteuer-Ausgleichsperioden einrichten
description: "Mehrwertsteuer-Abrechnungszeiträume enthalten Informationen über die Periodenintervalle für die die Mehrwertsteuer gemeldet und abgeführt werden muss."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: ab7d3a00a327f42a9f70c954d9b64a360a7f9163
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="0022c-103">Mehrwertsteuer-Ausgleichsperioden einrichten</span><span class="sxs-lookup"><span data-stu-id="0022c-103">Set up sales tax settlement periods</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0022c-104">Mehrwertsteuer-Abrechnungszeiträume enthalten Informationen über die Periodenintervalle für die die Mehrwertsteuer gemeldet und abgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="0022c-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="0022c-105">Ein Abrechnungsprozess kann für einen Abrechnungszeitraum für ein bestimmtes Datumsintervall ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0022c-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="0022c-106">Alle Steuercodes, die dem Abrechnungszeitraum zugeordnet sind, werden ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="0022c-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="0022c-107">Je nach den Einstellungen der zugehörigen "Mehrwertsteuerbehörde", werden die Steuerverbindlichkeiten entweder zu einem Kreditor oder auf ein "Hauptbuchkonto" gebucht.</span><span class="sxs-lookup"><span data-stu-id="0022c-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="0022c-108">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="0022c-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="0022c-109">Wechseln Sie zu "Steuer" Wechseln Sie zu "Steuer" > "Indirekte Steuern" > "Mehrwertsteuer" > "Mehrwertsteuer-Abrechnungszeiträume".</span><span class="sxs-lookup"><span data-stu-id="0022c-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="0022c-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0022c-110">Click New.</span></span>
3. <span data-ttu-id="0022c-111">Geben Sie im Feld "Abrechnungszeitraum" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0022c-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="0022c-112">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0022c-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0022c-113">Wählen Sie im Feld "Behörde" die Mehrwertsteuerbehörde aus, die der Empfänger der Berichte und der Zahlungen in Verbindung mit dem Abrechnungszeitraum ist.</span><span class="sxs-lookup"><span data-stu-id="0022c-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="0022c-114">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="0022c-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="0022c-115">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="0022c-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="0022c-116">Klicken Sie im Feld "Zahlungsbedingungen" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0022c-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="0022c-117">Die zugehörige Mehrwertsteuerbehörde kann als Kreditor eingerichtet werden und die "Mehrwertsteuerabrechnung" erstellt eine offene Kreditorenrechnung.</span><span class="sxs-lookup"><span data-stu-id="0022c-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="0022c-118">Die "Zahlungsbedingungen" definieren das "Fälligkeitsdatum" für die offene Kreditorenrechnung.</span><span class="sxs-lookup"><span data-stu-id="0022c-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="0022c-119">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="0022c-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="0022c-120">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="0022c-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="0022c-121">Wählen Sie einen Typ für die Abrechnungszeitraumintervalle aus.</span><span class="sxs-lookup"><span data-stu-id="0022c-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="0022c-122">Geben Sie die Anzahl der Periodenintervalleinheiten pro Periode ein.</span><span class="sxs-lookup"><span data-stu-id="0022c-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="0022c-123">So verfügt beispielsweise ein Quartal über 3 Monate.</span><span class="sxs-lookup"><span data-stu-id="0022c-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="0022c-124">Aktivieren oder deaktivieren Sie das Kontrollkästchen "Stapelverarbeitung für die Mehrwertsteuerabrechnung verwenden".</span><span class="sxs-lookup"><span data-stu-id="0022c-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="0022c-125">Der Abrechnungsprozess für den Abrechnungszeitraum kann als Batchauftrag im Hintergrund verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="0022c-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="0022c-126">Das wird für eine große Zahl von Steuertransaktionen innerhalb eines Periodenintervalls empfohlen.</span><span class="sxs-lookup"><span data-stu-id="0022c-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
14. <span data-ttu-id="0022c-127">Erweitern Sie die Registerkarte "Periodenintervalle".</span><span class="sxs-lookup"><span data-stu-id="0022c-127">Expand the Period intervals tab.</span></span>
15. <span data-ttu-id="0022c-128">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0022c-128">Click Add.</span></span>
16. <span data-ttu-id="0022c-129">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="0022c-129">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="0022c-130">Geben Sie in das Feld "Von Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="0022c-130">In the From date field, enter a date.</span></span>
18. <span data-ttu-id="0022c-131">Geben Sie in das Feld "Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="0022c-131">In the To date field, enter a date.</span></span>
19. <span data-ttu-id="0022c-132">Klicken Sie auf "Neues Periodenintervall".</span><span class="sxs-lookup"><span data-stu-id="0022c-132">Click New period interval.</span></span>
    * <span data-ttu-id="0022c-133">Sobald das erste Periodenintervall eingegeben wurde, können neue Perioden automatisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0022c-133">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="0022c-134">Sie können nach Bedarf zurückkehren und neue Periodenintervalle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0022c-134">You can come back and add new period intervals as required.</span></span>  
20. <span data-ttu-id="0022c-135">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0022c-135">Close the page.</span></span>


