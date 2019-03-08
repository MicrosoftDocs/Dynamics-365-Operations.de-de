---
title: Intercompany-Projektrechnungsstellung konfigurieren
description: Diese Prozedur zeigt, wie die Projektfakturierung zwischen zwei Unternehmen in Ihrer Organisation eingerichtet wird.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2fe06978d3a1c41a1133a568cca61df05b49d235
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "352757"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="f6890-103">Intercompany-Projektrechnungsstellung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="f6890-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f6890-104">Diese Prozedur zeigt, wie die Projektfakturierung zwischen zwei Unternehmen in Ihrer Organisation eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="f6890-104">This procedure shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="f6890-105">Diese Aufgabe verwendet das USSI-Dataset.</span><span class="sxs-lookup"><span data-stu-id="f6890-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="f6890-106">Gehen Sie zu "Kreditoren" > "Händler" > "Alle Händler".</span><span class="sxs-lookup"><span data-stu-id="f6890-106">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="f6890-107">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f6890-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f6890-108">Klicken Sie im Aktivitätsbereich auf Allgemein.</span><span class="sxs-lookup"><span data-stu-id="f6890-108">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="f6890-109">Klicken Sie auf „Intercompany”.</span><span class="sxs-lookup"><span data-stu-id="f6890-109">Click Intercompany.</span></span>
5. <span data-ttu-id="f6890-110">Legen Sie „Aktiv” auf „Ja” fest, um den Intercompanyhandel zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f6890-110">Set Active to Yes to enable intercompany trading.</span></span>
6. <span data-ttu-id="f6890-111">Geben Sie im Feld „Debitorenunternehmen” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f6890-111">In the Customer company field, enter or select a value.</span></span>
7. <span data-ttu-id="f6890-112">Geben Sie im Feld „Mein Konto” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f6890-112">In the My account field, enter or select a value.</span></span>
8. <span data-ttu-id="f6890-113">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f6890-113">Click Save.</span></span>
9. <span data-ttu-id="f6890-114">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f6890-114">Close the page.</span></span>
10. <span data-ttu-id="f6890-115">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f6890-115">Close the page.</span></span>
11. <span data-ttu-id="f6890-116">Wechseln Sie zu „Projektverwaltung und -buchhaltung” > „Setup”  „Projektverwaltungs- und -buchhaltungsparameter”.</span><span class="sxs-lookup"><span data-stu-id="f6890-116">Go to Project management and accounting > Setup > Project management and accounting parameters.</span></span>
12. <span data-ttu-id="f6890-117">Klicken Sie auf die Registerkarte „Intercompany”.</span><span class="sxs-lookup"><span data-stu-id="f6890-117">Click the Intercompany tab.</span></span>
13. <span data-ttu-id="f6890-118">Bewegen Sie den Schieberegler auf „Ja”, um die Intercompany-Ressourcenplanung und -Arbeitszeittabellen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f6890-118">Move the slider to Yes to enable intercompany resource scheduling and timesheets.</span></span>
14. <span data-ttu-id="f6890-119">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="f6890-119">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="f6890-120">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f6890-120">Click New.</span></span>
16. <span data-ttu-id="f6890-121">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="f6890-121">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="f6890-122">Geben Sie im Feld „Leihende juristische Person” einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f6890-122">In the Borrowing legal entity field, enter or select a value.</span></span>
18. <span data-ttu-id="f6890-123">Aktivieren Sie das Kontrollkästchen „Umsatzerlös antizipieren”.</span><span class="sxs-lookup"><span data-stu-id="f6890-123">Select the Accrue revenue check box.</span></span>
19. <span data-ttu-id="f6890-124">Geben Sie im Feld „Standard-Arbeitszeittabellenkategorie” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f6890-124">In the Default timesheet category field, enter or select a value.</span></span>
20. <span data-ttu-id="f6890-125">Geben Sie im Feld „Standard-Ausgabenkategorie” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f6890-125">In the Default expense category field, enter or select a value.</span></span>
21. <span data-ttu-id="f6890-126">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f6890-126">Click Save.</span></span>
22. <span data-ttu-id="f6890-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f6890-127">Close the page.</span></span>
23. <span data-ttu-id="f6890-128">Wechseln Sie zu „Projektverwaltung und -buchhaltung” > „Setup” > „Buchung” > „Sachkontobuchungseinstellungen”.</span><span class="sxs-lookup"><span data-stu-id="f6890-128">Go to Project management and accounting > Setup > Posting > Ledger posting setup.</span></span>
24. <span data-ttu-id="f6890-129">Wählen Sie im Feld „Sachkontotypen” eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="f6890-129">In the Ledger account types field, select an option.</span></span>
25. <span data-ttu-id="f6890-130">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f6890-130">Click New.</span></span>
26. <span data-ttu-id="f6890-131">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="f6890-131">In the list, mark the selected row.</span></span>
27. <span data-ttu-id="f6890-132">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="f6890-132">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="f6890-133">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="f6890-133">In the Main account field, specify the desired values.</span></span>
29. <span data-ttu-id="f6890-134">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f6890-134">Click Save.</span></span>
30. <span data-ttu-id="f6890-135">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f6890-135">Close the page.</span></span>
31. <span data-ttu-id="f6890-136">Wechseln Sie zu „Projektverwaltung und -buchhaltung” > „Setup” > „Preise” > „Verrechnungspreis”.</span><span class="sxs-lookup"><span data-stu-id="f6890-136">Go to Project management and accounting > Setup > Prices > Transfer price.</span></span>
32. <span data-ttu-id="f6890-137">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f6890-137">Click New.</span></span>
33. <span data-ttu-id="f6890-138">Geben Sie im Feld "Gültigkeitsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="f6890-138">In the Effective date field, enter a date.</span></span>
34. <span data-ttu-id="f6890-139">Geben Sie im Feld „Leihende juristische Person” einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f6890-139">In the Borrowing legal entity field, enter or select a value.</span></span>
35. <span data-ttu-id="f6890-140">Wählen Sie im Feld „Verrechnungspreismodell” eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="f6890-140">In the Transfer price model field, select an option.</span></span>
36. <span data-ttu-id="f6890-141">Geben Sie im Feld „Preisgestaltung” eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f6890-141">In the Pricing field, enter a number.</span></span>
37. <span data-ttu-id="f6890-142">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f6890-142">Click Save.</span></span>

