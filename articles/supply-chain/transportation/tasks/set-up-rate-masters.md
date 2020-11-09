---
title: Satzmaster einrichten
description: Dieses Verfahren zeigt Ihnen an, wie ein Satzmaster eingerichtet wird.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRouteWorkbench, TMSRateMaster, TMSRateBaseType
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72d71aa15f8cec532980f412ff1cb48e142c4cb1
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016469"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="759a8-103">Satzmaster einrichten</span><span class="sxs-lookup"><span data-stu-id="759a8-103">Set up rate masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="759a8-104">Dieses Verfahren zeigt Ihnen an, wie ein Satzmaster eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="759a8-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="759a8-105">Der Logistik-Manager legt normalerweise Satzmaster fest, abhängig von Verträgen mit den Spediteuren.</span><span class="sxs-lookup"><span data-stu-id="759a8-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="759a8-106">In diesem Szenario richten Sie einen Satzmaster für eine Luftfahrtgesellschaft ein.</span><span class="sxs-lookup"><span data-stu-id="759a8-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="759a8-107">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="759a8-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-rate-master"></a><span data-ttu-id="759a8-108">Satzmaster einrichten</span><span class="sxs-lookup"><span data-stu-id="759a8-108">Set up rate master</span></span>
1. <span data-ttu-id="759a8-109">Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Bewertung" > "Satzmaster".</span><span class="sxs-lookup"><span data-stu-id="759a8-109">Go to Transportation management > Setup > Rating > Rate master.</span></span>
2. <span data-ttu-id="759a8-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="759a8-110">Click New.</span></span>
3. <span data-ttu-id="759a8-111">Geben Sie im Feld "Satzmaster" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="759a8-111">In the Rate master field, type a value.</span></span>
4. <span data-ttu-id="759a8-112">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="759a8-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="759a8-113">Klicken Sie im Feld "Metadatenkennung bewerten" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="759a8-113">In the Rating metadata ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="759a8-114">Die Bewertungsmetadaten-Kennung bestimmt die Daten, die für den Satzmaster erforderlich sind, indem sie die Metadaten definiert, die über das TMS-Modul mithilfe dieses Satzmasters erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="759a8-114">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the TMS engine using this rate master.</span></span>  
6. <span data-ttu-id="759a8-115">Für dieses Beispiel die P2P-Option auswählen</span><span class="sxs-lookup"><span data-stu-id="759a8-115">For this example, select the P2P option</span></span>
7. <span data-ttu-id="759a8-116">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="759a8-116">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="759a8-117">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="759a8-117">Click Save.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="759a8-118">Satzbasis einrichten</span><span class="sxs-lookup"><span data-stu-id="759a8-118">Set up rate base</span></span>
1. <span data-ttu-id="759a8-119">Klicken Sie auf "Satzbasis".</span><span class="sxs-lookup"><span data-stu-id="759a8-119">Click Rate base.</span></span>
    * <span data-ttu-id="759a8-120">Die Satzbasis bestimmt den Satz des Spediteurs und kann verwendet werden, um eine Tarifstruktur einzurichten, da sie die Sätze in den Breakpoints strukturiert, die im Pausenmaster definiert werden.</span><span class="sxs-lookup"><span data-stu-id="759a8-120">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="759a8-121">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="759a8-121">Click New.</span></span>
3. <span data-ttu-id="759a8-122">Geben Sie im Feld "Satzbasis" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="759a8-122">In the Rate base field, type a value.</span></span>
4. <span data-ttu-id="759a8-123">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="759a8-123">In the Name field, type a value.</span></span>
5. <span data-ttu-id="759a8-124">Klicken Sie im Feld "Umbruchmaster" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="759a8-124">In the Break master field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="759a8-125">Pausenmaster werden verwendet, um die Preisgestaltungsstruktur und die Breakpoints zu definieren.</span><span class="sxs-lookup"><span data-stu-id="759a8-125">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="759a8-126">Die Preisgestaltungsstruktur verwendet abgestufte Preisgestaltung auf Grundlage der physischen Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="759a8-126">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="759a8-127">Für dieses Beispiel verwenden Sie Gewicht</span><span class="sxs-lookup"><span data-stu-id="759a8-127">For this example, use weight</span></span>
7. <span data-ttu-id="759a8-128">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="759a8-128">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="759a8-129">Schalten Sie die Erweiterung des Abschnitts "Details" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="759a8-129">Toggle the expansion of the Details section.</span></span>
9. <span data-ttu-id="759a8-130">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="759a8-130">Click New.</span></span>
10. <span data-ttu-id="759a8-131">Geben Sie im Feld "Postleitzahl der Lieferung ab" "30301 "ein.</span><span class="sxs-lookup"><span data-stu-id="759a8-131">In the Drop-off Postal Code From field, type '30301'.</span></span>
11. <span data-ttu-id="759a8-132">Geben Sie im Feld "Postleitzahl der Lieferung bis" "30318 "ein.</span><span class="sxs-lookup"><span data-stu-id="759a8-132">In the Drop-off Postal Code To field, type '30318'.</span></span>
12. <span data-ttu-id="759a8-133">Geben Sie im Feld "Land/Region für Einlieferung" "USA" ein.</span><span class="sxs-lookup"><span data-stu-id="759a8-133">In the Drop-off Country Region field, type 'USA'.</span></span>
13. <span data-ttu-id="759a8-134">Geben Sie im Feld "<1,00 kg" "100" ein.</span><span class="sxs-lookup"><span data-stu-id="759a8-134">In the <1.00 Lbs field, type '100'.</span></span>
    * <span data-ttu-id="759a8-135">Fügen Sie den Preis pro Kilogramm ein, wenn das Gesamtgewicht der Auslastung kleiner als 1 Pfund ist.</span><span class="sxs-lookup"><span data-stu-id="759a8-135">Insert the rate per lbs if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="759a8-136">Geben Sie im Feld <"5.00 kg" "300" ein.</span><span class="sxs-lookup"><span data-stu-id="759a8-136">In the <5.00 Lbs field, type '300'.</span></span>
    * <span data-ttu-id="759a8-137">Fügen Sie den Preis pro Kilogramm ein, wenn das Gesamtgewicht der Auslastung kleiner als 5 Pfund ist.</span><span class="sxs-lookup"><span data-stu-id="759a8-137">Insert the rate per lbs if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="759a8-138">Geben Sie im Feld <"20.00 kg" "500" ein.</span><span class="sxs-lookup"><span data-stu-id="759a8-138">In the <20.00 Lbs field, type '500'.</span></span>
    * <span data-ttu-id="759a8-139">Fügen Sie den Preis pro Kilogramm ein, wenn das Gesamtgewicht der Auslastung kleiner als 20 Pfund ist.</span><span class="sxs-lookup"><span data-stu-id="759a8-139">Insert the rate per lbs if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="759a8-140">Geben Sie im Feld <"100.00 kg" "1000" ein.</span><span class="sxs-lookup"><span data-stu-id="759a8-140">In the <100.00 Lbs field, type '1000'.</span></span>
    * <span data-ttu-id="759a8-141">Fügen Sie den Preis pro Kilogramm ein, wenn das Gesamtgewicht der Auslastung kleiner als 100 Pfund ist.</span><span class="sxs-lookup"><span data-stu-id="759a8-141">Insert the rate per lbs if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="759a8-142">Geben Sie im Feld <"1,000.00 kg" "3000" ein.</span><span class="sxs-lookup"><span data-stu-id="759a8-142">In the <1,000.00 Lbs field, type '3000'.</span></span>
    * <span data-ttu-id="759a8-143">Fügen Sie den Preis pro Kilogramm ein, wenn das Gesamtgewicht der Auslastung kleiner als 1000 Pfund ist.</span><span class="sxs-lookup"><span data-stu-id="759a8-143">Insert the rate per lbs if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="759a8-144">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="759a8-144">Click Save.</span></span>
19. <span data-ttu-id="759a8-145">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="759a8-145">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="759a8-146">Satzbasis zuweisen</span><span class="sxs-lookup"><span data-stu-id="759a8-146">Assign rate base</span></span>
1. <span data-ttu-id="759a8-147">Schalten Sie die Erweiterung des Satzbasiszuweisungs-Abschnitts ein/aus.</span><span class="sxs-lookup"><span data-stu-id="759a8-147">Toggle the expansion of the Rate base assignments section.</span></span>
2. <span data-ttu-id="759a8-148">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="759a8-148">Click New.</span></span>
    * <span data-ttu-id="759a8-149">Sie können mehrere Satzbasiszuweisungen für jeden Satzmaster haben.</span><span class="sxs-lookup"><span data-stu-id="759a8-149">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="759a8-150">Auf diese Weise ist es möglich, mehrere verschiedene Preispunkte für jeden Spediteur abhängig von Zielen, Dienstleistungen oder unterschiedlichen Satzbasen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="759a8-150">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="759a8-151">In diesem Verfahren erstellen Sie nur eine Satzbasiszuweisung.</span><span class="sxs-lookup"><span data-stu-id="759a8-151">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="759a8-152">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="759a8-152">In the Name field, type a value.</span></span>
4. <span data-ttu-id="759a8-153">Klicken Sie im Feld "Satzbasis" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="759a8-153">In the Rate base field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="759a8-154">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="759a8-154">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="759a8-155">Klicken Sie im Feld "Dienstleistung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="759a8-155">In the Service field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="759a8-156">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="759a8-156">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="759a8-157">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="759a8-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="759a8-158">Geben Sie im Feld "Postleitzahl für Abholung" "98052" ein.</span><span class="sxs-lookup"><span data-stu-id="759a8-158">In the Pick-up Postal Code field, type '98052'.</span></span>
    * <span data-ttu-id="759a8-159">Geben Sie an, für welche Postleitzahl diese Satzbasiszuweisung gültig sein soll aus.</span><span class="sxs-lookup"><span data-stu-id="759a8-159">Specify which postal code this rate base assignment should be valid from.</span></span>    
10. <span data-ttu-id="759a8-160">Geben Sie im Feld "Land/Region für Abholung" "USA" ein.</span><span class="sxs-lookup"><span data-stu-id="759a8-160">In the Pick-up Country Region field, type 'USA'.</span></span>
11. <span data-ttu-id="759a8-161">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="759a8-161">Click Save.</span></span>

