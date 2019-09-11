---
title: Intercompany-Projektrechnungsstellung konfigurieren
description: Dieses Thema zeigt, wie die Projektfakturierung zwischen zwei Unternehmen in Ihrer Organisation eingerichtet wird.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c89b17c09a4f145b5a4ca9cdd127b4e635447d4b
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867318"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="98560-103">Intercompany-Projektrechnungsstellung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="98560-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="98560-104">Dieses Thema zeigt, wie die Projektfakturierung zwischen zwei Unternehmen in Ihrer Organisation eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="98560-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="98560-105">Diese Aufgabe verwendet das USSI-Dataset.</span><span class="sxs-lookup"><span data-stu-id="98560-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="98560-106">Wechseln Sie im Navigationsbereich zu **Module > Kreditorenkonten > Kreditoren > Alle Kreditoren**.</span><span class="sxs-lookup"><span data-stu-id="98560-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="98560-107">In der Liste **Alle Kreditoren** suchen Sie den gewünschten Datensatz und wählen ihn aus.</span><span class="sxs-lookup"><span data-stu-id="98560-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="98560-108">Wählen Sie im Aktivitätsbereich **Allgemein** aus.</span><span class="sxs-lookup"><span data-stu-id="98560-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="98560-109">Wählen Sie **Intercompany** aus.</span><span class="sxs-lookup"><span data-stu-id="98560-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="98560-110">Legen Sie **Aktiv** auf **Ja** fest, um den Intercompanyhandel zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="98560-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="98560-111">Geben Sie im Feld **Debitorenunternehmen** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="98560-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="98560-112">Geben Sie im Feld **Mein Konto** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="98560-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="98560-113">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="98560-113">Select **Save**.</span></span>
9. <span data-ttu-id="98560-114">Schließen Sie die Seiten, um zur Startseite zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="98560-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="98560-115">Gehen Sie im Navigationsbereich zu **Module > Projektverwaltung und -verrechnung > Einrichtung > Projektverwaltungs- und -verrechnungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="98560-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="98560-116">Wählen Sie die Registerkarte **Intercompany** aus.</span><span class="sxs-lookup"><span data-stu-id="98560-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="98560-117">Bewegen Sie den Schieberegler auf **Ja**, um die Intercompany-Ressourcenplanung und -Arbeitszeittabellen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="98560-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="98560-118">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="98560-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="98560-119">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="98560-119">Select **New**.</span></span>
15. <span data-ttu-id="98560-120">Geben Sie im Feld **Leihende juristische Person** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="98560-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="98560-121">Aktivieren Sie das Kontrollkästchen **Umsatzerlös antizipieren**.</span><span class="sxs-lookup"><span data-stu-id="98560-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="98560-122">Geben Sie im Feld **Standard-Arbeitszeittabellenkategorie** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="98560-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="98560-123">Geben Sie im Feld **Standard-Ausgabenkategorie** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="98560-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="98560-124">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="98560-124">Select **Save**.</span></span>
20. <span data-ttu-id="98560-125">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="98560-125">Close the page.</span></span>
21. <span data-ttu-id="98560-126">Wechseln Sie im Navigationsbereich zu **Module > Projektverwaltung und -verrechnung > Einstellungen > Buchung > Sachkontobuchungseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="98560-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="98560-127">Wählen Sie im Feld **Sachkontotypen** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="98560-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="98560-128">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="98560-128">Select **New**.</span></span>
24. <span data-ttu-id="98560-129">Geben Sie im Feld **Hauptkonto** der neuen Zeile die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="98560-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="98560-130">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="98560-130">Select **Save**.</span></span>
26. <span data-ttu-id="98560-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="98560-131">Close the page.</span></span>
27. <span data-ttu-id="98560-132">Wechseln Sie im Navigationsbereich zu **Module > Projektverwaltung und -verrechnung > Einstellungen > Preise > Interner Verrechnungspreis**.</span><span class="sxs-lookup"><span data-stu-id="98560-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="98560-133">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="98560-133">Select **New**.</span></span>
29. <span data-ttu-id="98560-134">Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="98560-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="98560-135">Geben Sie im Feld **Leihende juristische Person** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="98560-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="98560-136">Wählen Sie im Feld **Verrechnungspreismodell** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="98560-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="98560-137">Geben Sie im Feld **Preisgestaltung** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="98560-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="98560-138">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="98560-138">Select **Save**.</span></span>

