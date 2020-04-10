---
title: Standardkosten für Arbeit und Ausgaben konfigurieren
description: Dieses Thema erläutert, wie Sie Standardkosten für Arbeit und Ausgaben für ein Projekt einrichten.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 51bbe52d70bae11cb0c95e9544f951f0fcc605f5
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140092"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="d0d69-103">Standardkosten für Arbeit und Ausgaben konfigurieren</span><span class="sxs-lookup"><span data-stu-id="d0d69-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d0d69-104">Dieses Thema erläutert, wie Sie Standardkosten für Arbeit und Ausgaben für ein Projekt einrichten.</span><span class="sxs-lookup"><span data-stu-id="d0d69-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="d0d69-105">Diese Aufgabe verwendet das USSI-Dataset.</span><span class="sxs-lookup"><span data-stu-id="d0d69-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="d0d69-106">Wechseln Sie im Navigationsbereich zu **Module > Projektverwaltung und -verrechnung > Einstellungen > Preise > Einstandspreis (Stunde)**.</span><span class="sxs-lookup"><span data-stu-id="d0d69-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="d0d69-107">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="d0d69-107">Select **New**.</span></span>
3. <span data-ttu-id="d0d69-108">Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="d0d69-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="d0d69-109">Geben Sie im Feld **Kostenpreis** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d0d69-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="d0d69-110">Sie können einen Standardeinstandspreis für die Projektkategorie oder einen Einstandspreis nach Arbeitskraftnummer, Projektnummer, Kategorie, Datum oder einer Kombination von ihnen einrichten.</span><span class="sxs-lookup"><span data-stu-id="d0d69-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="d0d69-111">Es wird jeweils der Einstandspreis mit der höchsten Genauigkeit angewendet.</span><span class="sxs-lookup"><span data-stu-id="d0d69-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="d0d69-112">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="d0d69-112">Select **Save**.</span></span>
6. <span data-ttu-id="d0d69-113">Wechseln Sie im Navigationsbereich zu **Module > Projektverwaltung und -verrechnung > Einstellungen > Preise > Verkaufspreis (Stunde)**.</span><span class="sxs-lookup"><span data-stu-id="d0d69-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="d0d69-114">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="d0d69-114">Select **New**.</span></span>
8. <span data-ttu-id="d0d69-115">Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="d0d69-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="d0d69-116">Wählen Sie im Feld **Gültig für** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="d0d69-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="d0d69-117">Geben Sie im Feld **Preisgestaltung** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d0d69-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="d0d69-118">Sie können einen Standardverkaufspreis für Stundenbuchungen oder für eine Projektkategorie einrichten.</span><span class="sxs-lookup"><span data-stu-id="d0d69-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="d0d69-119">Sie können auch Verkaufspreise nach Arbeitskraftnummer, Projektnummer, Kategorie, Buchungsdatum oder einer beliebigen Kombination dieser Angaben einrichten.</span><span class="sxs-lookup"><span data-stu-id="d0d69-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="d0d69-120">Der tatsächliche Verkaufspreis, der angewendet wird, wenn eine Arbeitskraft eine Buchung in die Stundenerfassung eingibt, ist der Verkaufspreis mit der höchsten Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="d0d69-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="d0d69-121">Wenn also z. B. ein allgemeiner und ein arbeitskraftspezifischer Verkaufspreis eingerichtet sind, wird der arbeitskraftspezifische Verkaufspreis verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0d69-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="d0d69-122">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="d0d69-122">Select **Save**.</span></span>
12. <span data-ttu-id="d0d69-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d0d69-123">Close the page.</span></span>
13. <span data-ttu-id="d0d69-124">Wechseln Sie im Navigationsbereich zu **Module > Projektverwaltung und -verrechnung > Einstellungen > Preise > Einstandspreis (Ausgaben)**.</span><span class="sxs-lookup"><span data-stu-id="d0d69-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="d0d69-125">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="d0d69-125">Select **New**.</span></span>
15. <span data-ttu-id="d0d69-126">Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="d0d69-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="d0d69-127">Geben Sie im Feld **Kostenpreis** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d0d69-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="d0d69-128">Mehrere können Felder ausgefüllt werden, dies ist jedoch das Minimum, das erforderlich ist, um den Datensatz zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d0d69-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="d0d69-129">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="d0d69-129">Select **Save**.</span></span>
18. <span data-ttu-id="d0d69-130">Wechseln Sie im Navigationsbereich zu **Module > Projektverwaltung und -verrechnung > Einstellungen > Preise > Verkaufspreis (Ausgaben)**.</span><span class="sxs-lookup"><span data-stu-id="d0d69-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="d0d69-131">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="d0d69-131">Select **New**.</span></span>
20. <span data-ttu-id="d0d69-132">Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="d0d69-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="d0d69-133">Wählen Sie im Feld **Gültig für** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="d0d69-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="d0d69-134">Geben Sie im Feld **Preisgestaltung** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d0d69-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="d0d69-135">Der tatsächliche Verkaufspreis, der dann angewendet wird, wenn eine Arbeitskraft Buchungen in eine Ausgabenerfassung eingibt, ist der Verkaufspreis mit der höchsten Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="d0d69-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="d0d69-136">Wenn also beispielsweise ein allgemeiner und ein arbeitskraftspezifischer Verkaufspreis eingerichtet sind, wird der arbeitskraftspezifische Verkaufspreis verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0d69-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="d0d69-137">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="d0d69-137">Select **Save**.</span></span>

