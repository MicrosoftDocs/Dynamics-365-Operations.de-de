---
title: Spediteur-Kraftstoffindex einrichten
description: Dieses Handbuch zeigt, wie eine Kraftstoffindex-Region, ein Kraftstoffindex und einen Spediteur-Kraftstoffindex erstellt wird.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 69bf6e3a896e560b1dbb96c8f997f6ee8dbb9ec1
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214917"
---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="78743-103">Spediteur-Kraftstoffindex einrichten</span><span class="sxs-lookup"><span data-stu-id="78743-103">Set up a carrier fuel index</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="78743-104">Dieses Handbuch zeigt, wie eine Kraftstoffindex-Region, ein Kraftstoffindex und einen Spediteur-Kraftstoffindex erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="78743-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="78743-105">Die Kraftstoffindex-Region gibt an, für welche Region der Kraftstoffindex gelten soll, und der Kraftstoffindex gibt einen Kraftstoffpreis für einen bestimmten Zeitraum an.</span><span class="sxs-lookup"><span data-stu-id="78743-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="78743-106">Um die Änderung der Kraftstoffpreise im Laufe der Zeit wiederzugeben, können Sie einem Spediteur mehrere Kraftstoffindizes zuordnen.</span><span class="sxs-lookup"><span data-stu-id="78743-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="78743-107">Diese Aufgaben werden in der Regel von einem Transportkoordinator durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="78743-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="78743-108">Sie können diese Prozedur im Demodatenunternehmen USMF oder mit eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="78743-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="78743-109">Erstellen einer Kraftstoffindex-Region</span><span class="sxs-lookup"><span data-stu-id="78743-109">Create a fuel index region</span></span>
1. <span data-ttu-id="78743-110">Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Kraftstoffindizes" > "Kraftstoffindex-Regionen".</span><span class="sxs-lookup"><span data-stu-id="78743-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="78743-111">Zunächst müssen Sie die verschiedenen Regionen erstellen, in denen Sie arbeiten, und verschiedene Benzinzuschläge berechnen.</span><span class="sxs-lookup"><span data-stu-id="78743-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="78743-112">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="78743-112">Click New.</span></span>
3. <span data-ttu-id="78743-113">Geben Sie im Feld "Region" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="78743-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="78743-114">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="78743-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="78743-115">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="78743-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="78743-116">Erstellen eines Kraftstoffindex</span><span class="sxs-lookup"><span data-stu-id="78743-116">Create a fuel index</span></span>
1. <span data-ttu-id="78743-117">Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Kraftstoffindizes" > "Kraftstoffindizes".</span><span class="sxs-lookup"><span data-stu-id="78743-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="78743-118">Für die eingerichteten Regionen müssen Sie die aktuellen Preise für den Kraftstoff eingeben.</span><span class="sxs-lookup"><span data-stu-id="78743-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="78743-119">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="78743-119">Click New.</span></span>
3. <span data-ttu-id="78743-120">Klicken Sie im Feld "Region" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="78743-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="78743-121">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="78743-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="78743-122">Geben Sie im Feld "Preis pro Liter" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="78743-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="78743-123">Geben Sie im Feld "Effektives Startdatum und -uhrzeit" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="78743-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="78743-124">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="78743-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="78743-125">Erstellen eines Spediteur-Kraftstoffindex</span><span class="sxs-lookup"><span data-stu-id="78743-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="78743-126">Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Kraftstoffindizes" > "Spediteur-Kraftstoffindizes".</span><span class="sxs-lookup"><span data-stu-id="78743-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="78743-127">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="78743-127">Click New.</span></span>
3. <span data-ttu-id="78743-128">Geben Sie einen Wert in das Feld "Spediteur-Kraftstoffindex" ein.</span><span class="sxs-lookup"><span data-stu-id="78743-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="78743-129">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="78743-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="78743-130">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="78743-130">Click New.</span></span>
6. <span data-ttu-id="78743-131">Geben Sie im Feld "Effektives Startdatum und -uhrzeit" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="78743-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="78743-132">Geben Sie im Feld "PPG von" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="78743-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="78743-133">In diesem Beispiel können Sie das Feld "PPG von" auf "1,95" festlegen.</span><span class="sxs-lookup"><span data-stu-id="78743-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="78743-134">Geben Sie im Feld "PPG bis" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="78743-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="78743-135">In diesem Beispiel können Sie das Feld "PPG bis" auf "2" festlegen.</span><span class="sxs-lookup"><span data-stu-id="78743-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="78743-136">Geben Sie im Feld "Prozentsatz" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="78743-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="78743-137">In diesem Beispiel können Sie "Prozentsatz" auf "3" festlegen.</span><span class="sxs-lookup"><span data-stu-id="78743-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="78743-138">Klicken Sie im Feld "Währung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="78743-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="78743-139">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="78743-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="78743-140">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="78743-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="78743-141">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="78743-141">Click Save.</span></span>

