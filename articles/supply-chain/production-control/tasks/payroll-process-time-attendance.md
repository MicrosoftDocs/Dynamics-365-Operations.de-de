---
title: "Lohnprozess für Zeit und Anwesenheit aktivieren"
description: "Diese Prozedur zeigt, wie der Lohnprozess für Zeit und Anwesenheit aktiviert wird."
author: johanhoffmann
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 020bcb71d9b8495e61f3cf83c073771d6f2b2f26
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="62627-103">Lohnprozess für Zeit und Anwesenheit aktivieren</span><span class="sxs-lookup"><span data-stu-id="62627-103">Enable the payroll process for time and attendance</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="62627-104">Diese Prozedur zeigt, wie der Lohnprozess für Zeit und Anwesenheit aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="62627-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="62627-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="62627-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="62627-106">Lohnart mit einem zugehörigen Lohnsatz erstellen</span><span class="sxs-lookup"><span data-stu-id="62627-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="62627-107">"Zeit und Anwesenheit" > "Einstellungen" > "Lohn" > "Lohnarten"</span><span class="sxs-lookup"><span data-stu-id="62627-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="62627-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="62627-108">Click New.</span></span>
3. <span data-ttu-id="62627-109">Geben Sie im Feld "Lohnart" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="62627-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="62627-110">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="62627-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="62627-111">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="62627-111">Click Save.</span></span>
6. <span data-ttu-id="62627-112">Klicken Sie auf "Sätze".</span><span class="sxs-lookup"><span data-stu-id="62627-112">Click Rates.</span></span>
    * <span data-ttu-id="62627-113">Sätze für Lohnarten werden für bestimmte Zeitintervalle eingerichtet, wobei für Arbeitskräfte individuelle Sätze erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="62627-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="62627-114">Es ist nicht immer erforderlich, Sätze unter "Zeit und Anwesenheit" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="62627-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="62627-115">Diese Informationen wurden möglicherweise bereits in dem Lohnabrechnungssystem angelegt, das zum Generieren von Löhnen und Gehältern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="62627-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="62627-116">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="62627-116">Click New.</span></span>
8. <span data-ttu-id="62627-117">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="62627-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="62627-118">Geben Sie im Feld "Satz" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="62627-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="62627-119">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="62627-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="62627-120">Erstellen einer Lohnvereinbarung</span><span class="sxs-lookup"><span data-stu-id="62627-120">Create a pay agreement</span></span>
1. <span data-ttu-id="62627-121">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="62627-121">Close the page.</span></span>
2. <span data-ttu-id="62627-122">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="62627-122">Close the page.</span></span>
3. <span data-ttu-id="62627-123">Wechseln Sie zu "Lohnvereinbarungen".</span><span class="sxs-lookup"><span data-stu-id="62627-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="62627-124">"Zeit und Anwesenheit" > "Einstellungen" > "Lohnvereinbarungen"</span><span class="sxs-lookup"><span data-stu-id="62627-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="62627-125">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="62627-125">Click New.</span></span>
5. <span data-ttu-id="62627-126">Geben Sie im Feld "Lohnvereinbarung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="62627-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="62627-127">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="62627-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="62627-128">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="62627-128">Click Save.</span></span>
8. <span data-ttu-id="62627-129">Klicken Sie auf "Vereinbarungspositionen".</span><span class="sxs-lookup"><span data-stu-id="62627-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="62627-130">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="62627-130">Click New.</span></span>
10. <span data-ttu-id="62627-131">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="62627-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="62627-132">Geben Sie im Feld "Profiltyp" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="62627-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="62627-133">Geben Sie im Feld "Lohnart" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="62627-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="62627-134">Lohnvereinbarung für Zeit- und Erfassungsarbeitskraft einrichten</span><span class="sxs-lookup"><span data-stu-id="62627-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="62627-135">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="62627-135">Close the page.</span></span>
2. <span data-ttu-id="62627-136">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="62627-136">Close the page.</span></span>
3. <span data-ttu-id="62627-137">Wechseln Sie zu "Zeiterfassung für Arbeitskräfte".</span><span class="sxs-lookup"><span data-stu-id="62627-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="62627-138">"Zeit und Anwesenheit" > "Einstellungen" > "Zeiterfassung für Arbeitskräfte"</span><span class="sxs-lookup"><span data-stu-id="62627-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="62627-139">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="62627-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="62627-140">Klicken Sie auf die Registerkarte "Anstellung".</span><span class="sxs-lookup"><span data-stu-id="62627-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="62627-141">Erweitern Sie den Abschnitt "Zeiterfassung".</span><span class="sxs-lookup"><span data-stu-id="62627-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="62627-142">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="62627-142">Click Edit.</span></span>
8. <span data-ttu-id="62627-143">Geben Sie im Feld "Lohnvereinbarung" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="62627-143">In the Pay agreement field, enter or select a value.</span></span>

