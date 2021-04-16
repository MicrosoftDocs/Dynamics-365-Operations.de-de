---
title: Satzmaster einrichten
description: Dieses Verfahren zeigt Ihnen an, wie ein Satzmaster eingerichtet wird.
author: ShylaThompson
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cb25726e05f11420c7355c39f7e262abca5da62
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808989"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="7f2df-103">Satzmaster einrichten</span><span class="sxs-lookup"><span data-stu-id="7f2df-103">Set up rate masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7f2df-104">Dieses Verfahren zeigt Ihnen an, wie ein Satzmaster eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="7f2df-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="7f2df-105">Der Logistik-Manager legt normalerweise Satzmaster fest, abhängig von Verträgen mit den Spediteuren.</span><span class="sxs-lookup"><span data-stu-id="7f2df-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="7f2df-106">In diesem Szenario richten Sie einen Satzmaster für eine Luftfahrtgesellschaft ein.</span><span class="sxs-lookup"><span data-stu-id="7f2df-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="7f2df-107">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="7f2df-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-break-master"></a><span data-ttu-id="7f2df-108">Festlegen des Breakmasters</span><span class="sxs-lookup"><span data-stu-id="7f2df-108">Set up break master</span></span>

1. <span data-ttu-id="7f2df-109">Gehen Sie zu **Transportverwaltung > Einrichten > Bewertung > Breakmaster**.</span><span class="sxs-lookup"><span data-stu-id="7f2df-109">Go to **Transportation management > Setup > Rating > Break master**.</span></span> <span data-ttu-id="7f2df-110">Pausenmaster werden verwendet, um die Preisgestaltungsstruktur und die Breakpoints zu definieren.</span><span class="sxs-lookup"><span data-stu-id="7f2df-110">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="7f2df-111">Die Preisgestaltungsstruktur verwendet abgestufte Preisgestaltung auf Grundlage der physischen Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="7f2df-111">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
1. <span data-ttu-id="7f2df-112">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7f2df-112">Select **New**.</span></span>
1. <span data-ttu-id="7f2df-113">Geben Sie im Feld **Breakmaster** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7f2df-113">In the **Break master** field, enter a value.</span></span>
1. <span data-ttu-id="7f2df-114">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7f2df-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="7f2df-115">Wählen Sie im Feld **Datentyp** den Datentyp.</span><span class="sxs-lookup"><span data-stu-id="7f2df-115">In the **Data type** field, select the data type.</span></span>
1. <span data-ttu-id="7f2df-116">Geben Sie im Feld **Vergleich** die Art des gewünschten Vergleichs ein (mit Operatoren).</span><span class="sxs-lookup"><span data-stu-id="7f2df-116">In the **Comparison** field, enter the kind of comparison requested (using operators).</span></span>
1. <span data-ttu-id="7f2df-117">Geben Sie im Feld **Aufteilungseinheit** die Aufteilungseinheit ein.</span><span class="sxs-lookup"><span data-stu-id="7f2df-117">In the **Break unit** field, enter the break unit.</span></span>
1. <span data-ttu-id="7f2df-118">Erstellen Sie im Bereich **Details** so viele Breaks, wie für die Preisstruktur benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="7f2df-118">In the **Details** section, create as many breaks as needed for the pricing structure.</span></span>
1. <span data-ttu-id="7f2df-119">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="7f2df-119">Select **Save**.</span></span>

## <a name="set-up-rate-master"></a><span data-ttu-id="7f2df-120">Satzmaster einrichten</span><span class="sxs-lookup"><span data-stu-id="7f2df-120">Set up rate master</span></span>

1. <span data-ttu-id="7f2df-121">Gehen Sie zu **Transportverwaltung > Einrichten > Tarif > Tarifmaster**.</span><span class="sxs-lookup"><span data-stu-id="7f2df-121">Go to **Transportation management > Setup > Rating > Rate master**.</span></span>
1. <span data-ttu-id="7f2df-122">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7f2df-122">Select **New**.</span></span>
1. <span data-ttu-id="7f2df-123">Geben Sie im Feld **Ratemaster** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7f2df-123">In the **Rate master** field, type a value.</span></span>
1. <span data-ttu-id="7f2df-124">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7f2df-124">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="7f2df-125">Wählen Sie im Feld **Bewertungs-Metadaten-ID** die Dropdown-Schaltfläche, um den Lookup zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7f2df-125">In the **Rating metadata ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="7f2df-126">Die Rating-Metadaten-ID bestimmt die Daten, die für den Tarifmaster benötigt werden, da sie die Metadaten definiert, die von der Engine der Transportverwaltung erwartet werden, die diesen Tarifmaster verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f2df-126">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the transportation management engine using this rate master.</span></span>  
1. <span data-ttu-id="7f2df-127">Wählen Sie für dieses Beispiel die Option P2P.</span><span class="sxs-lookup"><span data-stu-id="7f2df-127">For this example, select the P2P option.</span></span> <span data-ttu-id="7f2df-128">Diese ist bereits in den Demodaten definiert.</span><span class="sxs-lookup"><span data-stu-id="7f2df-128">This is already defined in the demo data.</span></span>
1. <span data-ttu-id="7f2df-129">Wählen Sie in der Liste den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="7f2df-129">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="7f2df-130">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="7f2df-130">Select **Save**.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="7f2df-131">Satzbasis einrichten</span><span class="sxs-lookup"><span data-stu-id="7f2df-131">Set up rate base</span></span>

1. <span data-ttu-id="7f2df-132">Wählen Sie **Tarifbasis**.</span><span class="sxs-lookup"><span data-stu-id="7f2df-132">Select **Rate base**.</span></span>
    * <span data-ttu-id="7f2df-133">Die Satzbasis bestimmt den Satz des Spediteurs und kann verwendet werden, um eine Tarifstruktur einzurichten, da sie die Sätze in den Breakpoints strukturiert, die im Pausenmaster definiert werden.</span><span class="sxs-lookup"><span data-stu-id="7f2df-133">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="7f2df-134">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7f2df-134">Select **New**.</span></span>
3. <span data-ttu-id="7f2df-135">Geben Sie in das Feld **Tarifbasis** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7f2df-135">In the **Rate base** field, type a value.</span></span>
4. <span data-ttu-id="7f2df-136">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7f2df-136">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="7f2df-137">Wählen Sie im Feld **Breakmaster** die Dropdown-Schaltfläche, um das Lookup zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7f2df-137">In the **Break master** field, select the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7f2df-138">Pausenmaster werden verwendet, um die Preisgestaltungsstruktur und die Breakpoints zu definieren.</span><span class="sxs-lookup"><span data-stu-id="7f2df-138">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="7f2df-139">Die Preisgestaltungsstruktur verwendet abgestufte Preisgestaltung auf Grundlage der physischen Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="7f2df-139">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="7f2df-140">Verwenden Sie für dieses Beispiel Gewicht.</span><span class="sxs-lookup"><span data-stu-id="7f2df-140">For this example, use weight.</span></span> <span data-ttu-id="7f2df-141">Diese ist bereits in den Demodaten definiert.</span><span class="sxs-lookup"><span data-stu-id="7f2df-141">This is already defined in the demo data.</span></span>
7. <span data-ttu-id="7f2df-142">Wählen Sie in der Liste die Verknüpfung in der markierten Zeile.</span><span class="sxs-lookup"><span data-stu-id="7f2df-142">In the list, select the link in the highlighted row.</span></span>
8. <span data-ttu-id="7f2df-143">Erweitern Sie den Bereich **Details**.</span><span class="sxs-lookup"><span data-stu-id="7f2df-143">Expand the **Details** section.</span></span>
9. <span data-ttu-id="7f2df-144">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7f2df-144">Select **New**.</span></span>
10. <span data-ttu-id="7f2df-145">Geben Sie in das Feld **Lieferungs-Postleitzahl von** „30301“ ein.</span><span class="sxs-lookup"><span data-stu-id="7f2df-145">In the **Drop-off Postal Code From** field, type "30301".</span></span>
11. <span data-ttu-id="7f2df-146">Geben Sie in das Feld **Lieferungs-Postleitzahl bis** „30318“ ein.</span><span class="sxs-lookup"><span data-stu-id="7f2df-146">In the **Drop-off Postal Code To** field, type "30318".</span></span>
12. <span data-ttu-id="7f2df-147">Geben Sie in das Feld **Lieferungsland Region** „USA“ ein.</span><span class="sxs-lookup"><span data-stu-id="7f2df-147">In the **Drop-off Country Region** field, type "USA".</span></span>
13. <span data-ttu-id="7f2df-148">Geben Sie in das Feld **<1,00 kg** „100“ ein.</span><span class="sxs-lookup"><span data-stu-id="7f2df-148">In the **<1.00 Lbs** field, type "100".</span></span>
    * <span data-ttu-id="7f2df-149">Geben Sie den Satz pro Kilogramm ein, wenn das Gesamtgewicht der Ladung weniger als 1 Kilogramm beträgt.</span><span class="sxs-lookup"><span data-stu-id="7f2df-149">Insert the rate per pounds if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="7f2df-150">Geben Sie in das Feld **<5,00 kg** „300“ ein.</span><span class="sxs-lookup"><span data-stu-id="7f2df-150">In the **<5.00 Lbs** field, type "300".</span></span>
    * <span data-ttu-id="7f2df-151">Geben Sie den Satz pro Kilogramm ein, wenn das Gesamtgewicht der Ladung weniger als 5 Kilogramm beträgt.</span><span class="sxs-lookup"><span data-stu-id="7f2df-151">Insert the rate per pounds if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="7f2df-152">Geben Sie in das Feld **<20,00 kg** „500“ ein.</span><span class="sxs-lookup"><span data-stu-id="7f2df-152">In the **<20.00 Lbs** field, type "500".</span></span>
    * <span data-ttu-id="7f2df-153">Geben Sie den Satz pro Kilogramm ein, wenn das Gesamtgewicht der Ladung weniger als 20 Kilogramm beträgt.</span><span class="sxs-lookup"><span data-stu-id="7f2df-153">Insert the rate per pounds if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="7f2df-154">Geben Sie in das Feld **<100,00 kg** „1000“ ein.</span><span class="sxs-lookup"><span data-stu-id="7f2df-154">In the **<100.00 Lbs** field, type "1000".</span></span>
    * <span data-ttu-id="7f2df-155">Geben Sie den Satz pro Kilogramm ein, wenn das Gesamtgewicht der Ladung weniger als 100 Kilogramm beträgt.</span><span class="sxs-lookup"><span data-stu-id="7f2df-155">Insert the rate per pounds if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="7f2df-156">Geben Sie in das Feld **<1.000,00 kg** „3000“ ein.</span><span class="sxs-lookup"><span data-stu-id="7f2df-156">In the **<1,000.00 Lbs** field, type "3000".</span></span>
    * <span data-ttu-id="7f2df-157">Geben Sie den Satz pro Kilogramm ein, wenn das Gesamtgewicht der Ladung weniger als 1000 Kilogramm beträgt.</span><span class="sxs-lookup"><span data-stu-id="7f2df-157">Insert the rate per pounds if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="7f2df-158">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="7f2df-158">Select **Save**.</span></span>
19. <span data-ttu-id="7f2df-159">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="7f2df-159">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="7f2df-160">Satzbasis zuweisen</span><span class="sxs-lookup"><span data-stu-id="7f2df-160">Assign rate base</span></span>

1. <span data-ttu-id="7f2df-161">Erweitern Sie den Abschnitt **Satz-Basis-Zuweisungen**.</span><span class="sxs-lookup"><span data-stu-id="7f2df-161">Expand the **Rate base assignments** section.</span></span>
2. <span data-ttu-id="7f2df-162">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7f2df-162">Select **New**.</span></span>
    * <span data-ttu-id="7f2df-163">Sie können mehrere Satzbasiszuweisungen für jeden Satzmaster haben.</span><span class="sxs-lookup"><span data-stu-id="7f2df-163">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="7f2df-164">Auf diese Weise ist es möglich, mehrere verschiedene Preispunkte für jeden Spediteur abhängig von Zielen, Dienstleistungen oder unterschiedlichen Satzbasen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7f2df-164">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="7f2df-165">In diesem Verfahren erstellen Sie nur eine Satzbasiszuweisung.</span><span class="sxs-lookup"><span data-stu-id="7f2df-165">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="7f2df-166">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7f2df-166">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="7f2df-167">Wählen Sie im Feld **Tarifbasis** die Dropdown-Schaltfläche, um das Nachschlagefeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7f2df-167">In the **Rate base** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="7f2df-168">Wählen Sie in der Liste die Verknüpfung in der markierten Zeile.</span><span class="sxs-lookup"><span data-stu-id="7f2df-168">In the list, select the link in the highlighted row.</span></span>
6. <span data-ttu-id="7f2df-169">Wählen Sie im Feld **Service** die Dropdown-Schaltfläche, um das Nachschlagefeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7f2df-169">In the **Service** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="7f2df-170">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="7f2df-170">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="7f2df-171">Wählen Sie in der Liste die Verknüpfung in der markierten Zeile.</span><span class="sxs-lookup"><span data-stu-id="7f2df-171">In the list, select the link in the highlighted row.</span></span>
9. <span data-ttu-id="7f2df-172">Geben Sie in das Feld **Postleitzahl entnehmen** „98052“ ein.</span><span class="sxs-lookup"><span data-stu-id="7f2df-172">In the **Pick-up Postal Code** field, type "98052".</span></span>
    * <span data-ttu-id="7f2df-173">Geben Sie an, für welche Postleitzahl diese Satzbasiszuweisung gültig sein soll aus.</span><span class="sxs-lookup"><span data-stu-id="7f2df-173">Specify which postal code this rate base assignment should be valid from.</span></span>
10. <span data-ttu-id="7f2df-174">Geben Sie in das Feld **Land Region** „USA“ ein.</span><span class="sxs-lookup"><span data-stu-id="7f2df-174">In the **Pick-up Country Region** field, type "USA".</span></span>
11. <span data-ttu-id="7f2df-175">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="7f2df-175">Select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]