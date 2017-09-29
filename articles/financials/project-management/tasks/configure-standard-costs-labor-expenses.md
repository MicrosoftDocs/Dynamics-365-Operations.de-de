--- 
title: "Standardkosten für Arbeit und Ausgaben konfigurieren"
description: "Diese Prozedur zeigt, wie Sie Standardkosten für Arbeit und Ausgaben für ein Projekt einrichten."
author: KimANelson
manager: AnnBe
ms.date: 02/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 432b5b195b29fb03786cb0560e277735b531b7d7
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="221a6-103">Standardkosten für Arbeit und Ausgaben konfigurieren</span><span class="sxs-lookup"><span data-stu-id="221a6-103">Configure standard costs for labor and expenses</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="221a6-104">Diese Prozedur zeigt, wie Sie Standardkosten für Arbeit und Ausgaben für ein Projekt einrichten.</span><span class="sxs-lookup"><span data-stu-id="221a6-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="221a6-105">Diese Aufgabe verwendet das USSI-Dataset.</span><span class="sxs-lookup"><span data-stu-id="221a6-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="221a6-106">Wechseln Sie zu „Projektverwaltung und -buchhaltung” > „Setup” > „Preise” > „Einstandspreis (Stunde)”.</span><span class="sxs-lookup"><span data-stu-id="221a6-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="221a6-107">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="221a6-107">Click New.</span></span>
3. <span data-ttu-id="221a6-108">Geben Sie im Feld "Gültigkeitsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="221a6-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="221a6-109">Geben Sie im Feld "Kostenpreis" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="221a6-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="221a6-110">Sie können einen Standardeinstandspreis für die Projektkategorie oder einen Einstandspreis nach Arbeitskraftnummer, Projektnummer, Kategorie, Datum oder einer Kombination von ihnen einrichten.</span><span class="sxs-lookup"><span data-stu-id="221a6-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="221a6-111">Es wird jeweils der Einstandspreis mit der höchsten Genauigkeit angewendet.</span><span class="sxs-lookup"><span data-stu-id="221a6-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="221a6-112">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="221a6-112">Click Save.</span></span>
6. <span data-ttu-id="221a6-113">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="221a6-113">Close the page.</span></span>
7. <span data-ttu-id="221a6-114">Wechseln Sie zu „Projektverwaltung und -buchhaltung” > „Setup” > „Preise” > „Verkaufspreis (Stunde)”.</span><span class="sxs-lookup"><span data-stu-id="221a6-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="221a6-115">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="221a6-115">Click New.</span></span>
9. <span data-ttu-id="221a6-116">Geben Sie im Feld "Gültigkeitsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="221a6-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="221a6-117">Wählen Sie im Feld "Gültig für" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="221a6-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="221a6-118">Geben Sie im Feld „Preisgestaltung” eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="221a6-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="221a6-119">Sie können einen Standardverkaufspreis für Stundenbuchungen oder für eine Projektkategorie einrichten.</span><span class="sxs-lookup"><span data-stu-id="221a6-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="221a6-120">Sie können auch Verkaufspreise nach Arbeitskraftnummer, Projektnummer, Kategorie, Buchungsdatum oder einer beliebigen Kombination dieser Angaben einrichten.</span><span class="sxs-lookup"><span data-stu-id="221a6-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="221a6-121">Der tatsächliche Verkaufspreis, der angewendet wird, wenn eine Arbeitskraft eine Buchung in die Stundenerfassung eingibt, ist der Verkaufspreis mit der höchsten Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="221a6-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="221a6-122">Wenn also z. B. ein allgemeiner und ein arbeitskraftspezifischer Verkaufspreis eingerichtet sind, wird der arbeitskraftspezifische Verkaufspreis verwendet.</span><span class="sxs-lookup"><span data-stu-id="221a6-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="221a6-123">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="221a6-123">Click Save.</span></span>
13. <span data-ttu-id="221a6-124">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="221a6-124">Close the page.</span></span>
14. <span data-ttu-id="221a6-125">Wechseln Sie zu „Projektverwaltung und -buchhaltung” > „Setup” > „Preise” > „Einstandspreis (Ausgaben)”.</span><span class="sxs-lookup"><span data-stu-id="221a6-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="221a6-126">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="221a6-126">Click New.</span></span>
16. <span data-ttu-id="221a6-127">Geben Sie im Feld "Gültigkeitsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="221a6-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="221a6-128">Geben Sie im Feld "Kostenpreis" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="221a6-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="221a6-129">Mehrere können Felder ausgefüllt werden, dies ist jedoch das Minimum, das erforderlich ist, um den Datensatz zu speichern.</span><span class="sxs-lookup"><span data-stu-id="221a6-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="221a6-130">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="221a6-130">Click Save.</span></span>
19. <span data-ttu-id="221a6-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="221a6-131">Close the page.</span></span>
20. <span data-ttu-id="221a6-132">Wechseln Sie zu „Projektverwaltung und -buchhaltung” > „Setup” > „Preise” > „Verkaufspreis (Ausgaben)”.</span><span class="sxs-lookup"><span data-stu-id="221a6-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="221a6-133">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="221a6-133">Click New.</span></span>
22. <span data-ttu-id="221a6-134">Geben Sie im Feld "Gültigkeitsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="221a6-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="221a6-135">Wählen Sie im Feld "Gültig für" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="221a6-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="221a6-136">Geben Sie im Feld „Preisgestaltung” eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="221a6-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="221a6-137">Der tatsächliche Verkaufspreis, der dann angewendet wird, wenn eine Arbeitskraft Buchungen in eine Ausgabenerfassung eingibt, ist der Verkaufspreis mit der höchsten Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="221a6-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="221a6-138">Wenn also beispielsweise ein allgemeiner und ein arbeitskraftspezifischer Verkaufspreis eingerichtet sind, wird der arbeitskraftspezifische Verkaufspreis verwendet.</span><span class="sxs-lookup"><span data-stu-id="221a6-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="221a6-139">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="221a6-139">Click Save.</span></span>


