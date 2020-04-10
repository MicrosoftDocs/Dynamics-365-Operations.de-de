---
title: Spediteur-Kraftstoffindex einrichten
description: Dieses Handbuch zeigt, wie eine Kraftstoffindex-Region, ein Kraftstoffindex und einen Spediteur-Kraftstoffindex erstellt wird.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 73336c6803f28239ff8ca78dcff5ea8db0835e32
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146248"
---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="8af2c-103">Spediteur-Kraftstoffindex einrichten</span><span class="sxs-lookup"><span data-stu-id="8af2c-103">Set up a carrier fuel index</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8af2c-104">Dieses Handbuch zeigt, wie eine Kraftstoffindex-Region, ein Kraftstoffindex und einen Spediteur-Kraftstoffindex erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8af2c-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="8af2c-105">Die Kraftstoffindex-Region gibt an, für welche Region der Kraftstoffindex gelten soll, und der Kraftstoffindex gibt einen Kraftstoffpreis für einen bestimmten Zeitraum an.</span><span class="sxs-lookup"><span data-stu-id="8af2c-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="8af2c-106">Um die Änderung der Kraftstoffpreise im Laufe der Zeit wiederzugeben, können Sie einem Spediteur mehrere Kraftstoffindizes zuordnen.</span><span class="sxs-lookup"><span data-stu-id="8af2c-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="8af2c-107">Diese Aufgaben werden in der Regel von einem Transportkoordinator durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="8af2c-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="8af2c-108">Sie können diese Prozedur im Demodatenunternehmen USMF oder mit eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="8af2c-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="8af2c-109">Erstellen einer Kraftstoffindex-Region</span><span class="sxs-lookup"><span data-stu-id="8af2c-109">Create a fuel index region</span></span>
1. <span data-ttu-id="8af2c-110">Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Kraftstoffindizes" > "Kraftstoffindex-Regionen".</span><span class="sxs-lookup"><span data-stu-id="8af2c-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="8af2c-111">Zunächst müssen Sie die verschiedenen Regionen erstellen, in denen Sie arbeiten, und verschiedene Benzinzuschläge berechnen.</span><span class="sxs-lookup"><span data-stu-id="8af2c-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="8af2c-112">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="8af2c-112">Click New.</span></span>
3. <span data-ttu-id="8af2c-113">Geben Sie im Feld "Region" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8af2c-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="8af2c-114">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8af2c-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="8af2c-115">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8af2c-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="8af2c-116">Erstellen eines Kraftstoffindex</span><span class="sxs-lookup"><span data-stu-id="8af2c-116">Create a fuel index</span></span>
1. <span data-ttu-id="8af2c-117">Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Kraftstoffindizes" > "Kraftstoffindizes".</span><span class="sxs-lookup"><span data-stu-id="8af2c-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="8af2c-118">Für die eingerichteten Regionen müssen Sie die aktuellen Preise für den Kraftstoff eingeben.</span><span class="sxs-lookup"><span data-stu-id="8af2c-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="8af2c-119">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="8af2c-119">Click New.</span></span>
3. <span data-ttu-id="8af2c-120">Klicken Sie im Feld "Region" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8af2c-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8af2c-121">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8af2c-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="8af2c-122">Geben Sie im Feld "Preis pro Liter" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="8af2c-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="8af2c-123">Geben Sie im Feld "Effektives Startdatum und -uhrzeit" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="8af2c-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="8af2c-124">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8af2c-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="8af2c-125">Erstellen eines Spediteur-Kraftstoffindex</span><span class="sxs-lookup"><span data-stu-id="8af2c-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="8af2c-126">Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Kraftstoffindizes" > "Spediteur-Kraftstoffindizes".</span><span class="sxs-lookup"><span data-stu-id="8af2c-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="8af2c-127">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="8af2c-127">Click New.</span></span>
3. <span data-ttu-id="8af2c-128">Geben Sie einen Wert in das Feld "Spediteur-Kraftstoffindex" ein.</span><span class="sxs-lookup"><span data-stu-id="8af2c-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="8af2c-129">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8af2c-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8af2c-130">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="8af2c-130">Click New.</span></span>
6. <span data-ttu-id="8af2c-131">Geben Sie im Feld "Effektives Startdatum und -uhrzeit" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="8af2c-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="8af2c-132">Geben Sie im Feld "PPG von" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="8af2c-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="8af2c-133">In diesem Beispiel können Sie das Feld "PPG von" auf "1,95" festlegen.</span><span class="sxs-lookup"><span data-stu-id="8af2c-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="8af2c-134">Geben Sie im Feld "PPG bis" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="8af2c-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="8af2c-135">In diesem Beispiel können Sie das Feld "PPG bis" auf "2" festlegen.</span><span class="sxs-lookup"><span data-stu-id="8af2c-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="8af2c-136">Geben Sie im Feld "Prozentsatz" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="8af2c-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="8af2c-137">In diesem Beispiel können Sie "Prozentsatz" auf "3" festlegen.</span><span class="sxs-lookup"><span data-stu-id="8af2c-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="8af2c-138">Klicken Sie im Feld "Währung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8af2c-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="8af2c-139">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8af2c-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="8af2c-140">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8af2c-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="8af2c-141">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8af2c-141">Click Save.</span></span>

