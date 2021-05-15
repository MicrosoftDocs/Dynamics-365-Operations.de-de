---
title: Mehrwertsteuer-Ausgleichsperioden einrichten
description: In diesem Abschnitt wird erläutert, wie Sie unter Dynamics 365 Finance Umsatzsteuerverrechnungsperioden einrichten.
author: twheeloc
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 83587df3963d215fec020150e6b707e431c1b6eb
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944776"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="c8bd7-103">Mehrwertsteuer-Ausgleichsperioden einrichten</span><span class="sxs-lookup"><span data-stu-id="c8bd7-103">Set up sales tax settlement periods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c8bd7-104">In diesem Abschnitt wird erläutert, wie Sie Umsatzsteuerverrechnungsperioden einrichten.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-104">This topic explains how to set up sales tax settlement periods.</span></span> <span data-ttu-id="c8bd7-105">Mehrwertsteuer-Abrechnungszeiträume enthalten Informationen über die Periodenintervalle für die die Mehrwertsteuer gemeldet und abgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-105">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="c8bd7-106">Ein Abrechnungsprozess kann für einen Abrechnungszeitraum für ein bestimmtes Datumsintervall ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-106">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="c8bd7-107">Alle Steuercodes, die dem Abrechnungszeitraum zugeordnet sind, werden ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-107">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="c8bd7-108">Je nach den Einstellungen der zugehörigen "Mehrwertsteuerbehörde", werden die Steuerverbindlichkeiten entweder zu einem Kreditor oder auf ein "Hauptbuchkonto" gebucht.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-108">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>

<span data-ttu-id="c8bd7-109">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="c8bd7-110">Gehen Sie im Navigationsbereich zu **Module > Steuer > Indirekte Steuern > Umsatzsteuer > Umsatzsteuer > Umsatzsteuerabrechnungsperioden**.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-110">In the navigation pane, go to **Modules > Tax > Indirect taxes > Sales tax > Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="c8bd7-111">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-111">Select **New**.</span></span>
3. <span data-ttu-id="c8bd7-112">Geben Sie im Feld **Abrechnungszeitraum** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-112">In the **Settlement period** field, type a value.</span></span>
4. <span data-ttu-id="c8bd7-113">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="c8bd7-114">Wählen Sie im Feld **Berechtigung** die Umsatzsteuerbehörde, die die Berichte und die Zahlungen erhält, die für den Abrechnungszeitraum angelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-114">In the **Authority** field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="c8bd7-115">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="c8bd7-116">Wählen Sie im Feld **Zahlungsbedingungen** den gewünschten Datensatz im Dropdown-Menü aus.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-116">In the **Terms of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="c8bd7-117">Die zugehörige Mehrwertsteuerbehörde kann als Kreditor eingerichtet werden und die "Mehrwertsteuerabrechnung" erstellt eine offene Kreditorenrechnung.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="c8bd7-118">Die "Zahlungsbedingungen" definieren das "Fälligkeitsdatum" für die offene Kreditorenrechnung.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
8. <span data-ttu-id="c8bd7-119">Wählen Sie einen Typ für die Abrechnungszeitraumintervalle aus.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-119">Select a type for the settlement period intervals.</span></span>
9. <span data-ttu-id="c8bd7-120">Geben Sie die Anzahl der Periodenintervalleinheiten pro Periode ein.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-120">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="c8bd7-121">So verfügt beispielsweise ein Quartal über 3 Monate.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-121">For example, a quarter has 3 months.</span></span>
10. <span data-ttu-id="c8bd7-122">Aktivieren oder deaktivieren Sie das Kontrollkästchen **Batchverarbeitung für Umsatzsteuerabrechnung verwenden**.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-122">Select or clear the **Use batch processing for sales tax settlement** check box.</span></span> <span data-ttu-id="c8bd7-123">Der Abrechnungsprozess für den Abrechnungszeitraum kann als Batchauftrag im Hintergrund verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-123">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="c8bd7-124">Das wird für eine große Zahl von Steuertransaktionen innerhalb eines Periodenintervalls empfohlen.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-124">This is recommended for a large number of tax transactions within a period interval.</span></span>
11. <span data-ttu-id="c8bd7-125">Aktivieren oder deaktivieren Sie das Kontrollkästchen **Verrechnung von Steuertransaktionen verhindern**.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-125">Select or clear the **Prevent generating offset tax transactions** check box.</span></span> <span data-ttu-id="c8bd7-126">Standardmäßig generiert das System Offsetsteuerbuchungen während des Ausgleichsprozesses, die  Performanceprobleme verursachen können,  wenn es viele Steuerbuchungen innerhalb eines Periodenintervalls gibt.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-126">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="c8bd7-127">Aktivieren bzw. deaktivieren Sie dieses Kontrollkästchen, um Steuerausgleichsbuchungen erstellen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-127">Select this check box to prevent generating offset tax transactions.</span></span>
12. <span data-ttu-id="c8bd7-128">Erweitern Sie die Registerkarte **Periodenintervalle**.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-128">Expand the **Period intervals** tab.</span></span>
13. <span data-ttu-id="c8bd7-129">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-129">Select **Add**.</span></span>
14. <span data-ttu-id="c8bd7-130">Geben Sie in der neuen Zeile im Feld **Ab Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-130">In the **From date** field in the new row, enter a date.</span></span>
15. <span data-ttu-id="c8bd7-131">Geben Sie im Feld **Bis Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-131">In the **To date** field, enter a date.</span></span>
16. <span data-ttu-id="c8bd7-132">Wählen Sie **Neues Periodenintervall**.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-132">Select **New period interval**.</span></span> <span data-ttu-id="c8bd7-133">Sobald das erste Periodenintervall eingegeben wurde, können neue Perioden automatisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-133">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="c8bd7-134">Sie können nach Bedarf zurückkehren und neue Periodenintervalle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-134">You can come back and add new period intervals as required.</span></span>  
17. <span data-ttu-id="c8bd7-135">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c8bd7-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
