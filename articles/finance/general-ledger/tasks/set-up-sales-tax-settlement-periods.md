---
title: Mehrwertsteuer-Ausgleichsperioden einrichten
description: In diesem Abschnitt wird erläutert, wie Sie unter Dynamics 365 Finance Umsatzsteuerverrechnungsperioden einrichten.
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
ms.openlocfilehash: c17a0240c29dad58c958ab1ce844ee5d8384bd1f
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658928"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="29cb0-103">Mehrwertsteuer-Ausgleichsperioden einrichten</span><span class="sxs-lookup"><span data-stu-id="29cb0-103">Set up sales tax settlement periods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="29cb0-104">In diesem Abschnitt wird erläutert, wie Sie Umsatzsteuerverrechnungsperioden einrichten.</span><span class="sxs-lookup"><span data-stu-id="29cb0-104">This topic explains how to set up sales tax settlement periods.</span></span> <span data-ttu-id="29cb0-105">Mehrwertsteuer-Abrechnungszeiträume enthalten Informationen über die Periodenintervalle für die die Mehrwertsteuer gemeldet und abgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="29cb0-105">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="29cb0-106">Ein Abrechnungsprozess kann für einen Abrechnungszeitraum für ein bestimmtes Datumsintervall ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="29cb0-106">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="29cb0-107">Alle Steuercodes, die dem Abrechnungszeitraum zugeordnet sind, werden ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="29cb0-107">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="29cb0-108">Je nach den Einstellungen der zugehörigen "Mehrwertsteuerbehörde", werden die Steuerverbindlichkeiten entweder zu einem Kreditor oder auf ein "Hauptbuchkonto" gebucht.</span><span class="sxs-lookup"><span data-stu-id="29cb0-108">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>

<span data-ttu-id="29cb0-109">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="29cb0-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="29cb0-110">Gehen Sie im Navigationsbereich zu **Module > Steuer > Indirekte Steuern > Umsatzsteuer > Umsatzsteuer > Umsatzsteuerabrechnungsperioden**.</span><span class="sxs-lookup"><span data-stu-id="29cb0-110">In the navigation pane, go to **Modules > Tax > Indirect taxes > Sales tax > Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="29cb0-111">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="29cb0-111">Select **New**.</span></span>
3. <span data-ttu-id="29cb0-112">Geben Sie im Feld **Abrechnungszeitraum** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="29cb0-112">In the **Settlement period** field, type a value.</span></span>
4. <span data-ttu-id="29cb0-113">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="29cb0-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="29cb0-114">Wählen Sie im Feld **Berechtigung** die Umsatzsteuerbehörde, die die Berichte und die Zahlungen erhält, die für den Abrechnungszeitraum angelegt werden.</span><span class="sxs-lookup"><span data-stu-id="29cb0-114">In the **Authority** field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="29cb0-115">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="29cb0-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="29cb0-116">Wählen Sie im Feld **Zahlungsbedingungen** den gewünschten Datensatz im Dropdown-Menü aus.</span><span class="sxs-lookup"><span data-stu-id="29cb0-116">In the **Terms of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="29cb0-117">Die zugehörige Mehrwertsteuerbehörde kann als Kreditor eingerichtet werden und die "Mehrwertsteuerabrechnung" erstellt eine offene Kreditorenrechnung.</span><span class="sxs-lookup"><span data-stu-id="29cb0-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="29cb0-118">Die "Zahlungsbedingungen" definieren das "Fälligkeitsdatum" für die offene Kreditorenrechnung.</span><span class="sxs-lookup"><span data-stu-id="29cb0-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
8. <span data-ttu-id="29cb0-119">Wählen Sie einen Typ für die Abrechnungszeitraumintervalle aus.</span><span class="sxs-lookup"><span data-stu-id="29cb0-119">Select a type for the settlement period intervals.</span></span>
9. <span data-ttu-id="29cb0-120">Geben Sie die Anzahl der Periodenintervalleinheiten pro Periode ein.</span><span class="sxs-lookup"><span data-stu-id="29cb0-120">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="29cb0-121">So verfügt beispielsweise ein Quartal über 3 Monate.</span><span class="sxs-lookup"><span data-stu-id="29cb0-121">For example, a quarter has 3 months.</span></span>
10. <span data-ttu-id="29cb0-122">Aktivieren oder deaktivieren Sie das Kontrollkästchen **Batchverarbeitung für Umsatzsteuerabrechnung verwenden**.</span><span class="sxs-lookup"><span data-stu-id="29cb0-122">Select or clear the **Use batch processing for sales tax settlement** check box.</span></span> <span data-ttu-id="29cb0-123">Der Abrechnungsprozess für den Abrechnungszeitraum kann als Batchauftrag im Hintergrund verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="29cb0-123">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="29cb0-124">Das wird für eine große Zahl von Steuertransaktionen innerhalb eines Periodenintervalls empfohlen.</span><span class="sxs-lookup"><span data-stu-id="29cb0-124">This is recommended for a large number of tax transactions within a period interval.</span></span>  
    > [!NOTE]
    > <span data-ttu-id="29cb0-125">Derzeit wird dies in Spanien, Japan und den Niederlanden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="29cb0-125">Currently this is not supported in Spain, Japan, and the Netherlands.</span></span>
11. <span data-ttu-id="29cb0-126">Aktivieren oder deaktivieren Sie das Kontrollkästchen **Verrechnung von Steuertransaktionen verhindern**.</span><span class="sxs-lookup"><span data-stu-id="29cb0-126">Select or clear the **Prevent generating offset tax transactions** check box.</span></span> <span data-ttu-id="29cb0-127">Standardmäßig generiert das System Offsetsteuerbuchungen während des Ausgleichsprozesses, die  Performanceprobleme verursachen können,  wenn es viele Steuerbuchungen innerhalb eines Periodenintervalls gibt.</span><span class="sxs-lookup"><span data-stu-id="29cb0-127">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="29cb0-128">Aktivieren bzw. deaktivieren Sie dieses Kontrollkästchen, um Steuerausgleichsbuchungen erstellen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="29cb0-128">Select this check box to prevent generating offset tax transactions.</span></span>
12. <span data-ttu-id="29cb0-129">Erweitern Sie die Registerkarte **Periodenintervalle**.</span><span class="sxs-lookup"><span data-stu-id="29cb0-129">Expand the **Period intervals** tab.</span></span>
13. <span data-ttu-id="29cb0-130">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="29cb0-130">Select **Add**.</span></span>
14. <span data-ttu-id="29cb0-131">Geben Sie in der neuen Zeile im Feld **Ab Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="29cb0-131">In the **From date** field in the new row, enter a date.</span></span>
15. <span data-ttu-id="29cb0-132">Geben Sie im Feld **Bis Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="29cb0-132">In the **To date** field, enter a date.</span></span>
16. <span data-ttu-id="29cb0-133">Wählen Sie **Neues Periodenintervall**.</span><span class="sxs-lookup"><span data-stu-id="29cb0-133">Select **New period interval**.</span></span> <span data-ttu-id="29cb0-134">Sobald das erste Periodenintervall eingegeben wurde, können neue Perioden automatisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="29cb0-134">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="29cb0-135">Sie können nach Bedarf zurückkehren und neue Periodenintervalle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="29cb0-135">You can come back and add new period intervals as required.</span></span>  
17. <span data-ttu-id="29cb0-136">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="29cb0-136">Close the page.</span></span>

