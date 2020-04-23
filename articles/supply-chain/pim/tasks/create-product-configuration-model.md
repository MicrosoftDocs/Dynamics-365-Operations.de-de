---
title: Produktkonfigurationsmodell erstellen
description: Im folgenden Verfahren wird gezeigt, wie ein Produktkonfigurationsmodell erstellt wird und grundlegende Informationen wie Attribute und Unterkomponenten eingegeben werden.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9577005fb4fc016670713c36e40263ff30030caf
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203756"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="9c573-103">Produktkonfigurationsmodell erstellen</span><span class="sxs-lookup"><span data-stu-id="9c573-103">Create a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9c573-104">Im folgenden Verfahren wird gezeigt, wie ein Produktkonfigurationsmodell erstellt wird und grundlegende Informationen wie Attribute und Unterkomponenten eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9c573-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="9c573-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="9c573-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="9c573-106">Erstellen eines Produktmodells</span><span class="sxs-lookup"><span data-stu-id="9c573-106">Create a product model</span></span>
1. <span data-ttu-id="9c573-107">Klicken Sie auf "Produktvariantenmodell-Definition".</span><span class="sxs-lookup"><span data-stu-id="9c573-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="9c573-108">Klicken Sie auf "Produktkonfigurationsmodelle".</span><span class="sxs-lookup"><span data-stu-id="9c573-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="9c573-109">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="9c573-109">Click New.</span></span>
4. <span data-ttu-id="9c573-110">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9c573-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9c573-111">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9c573-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="9c573-112">Wählen Sie im Feld "Solver-Strategie" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="9c573-112">In the Solver strategy field, select an option.</span></span>
    * <span data-ttu-id="9c573-113">Die Solver-Strategie bestimmt, wie die Einschränkungen in einem einschränkungsbasierten Produktkonfigurationsmodell verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="9c573-113">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="9c573-114">Diese Auswahl kann Auswirkungen auf die Leistung des Produktkonfigurationsmodells haben.</span><span class="sxs-lookup"><span data-stu-id="9c573-114">This selection can have an impact on the performance of the product configuration model.</span></span>  
7. <span data-ttu-id="9c573-115">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9c573-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="9c573-116">Die Stammkomponente stellt das Produktkonfigurationsmodell dar, kann jedoch auch in anderen Produktmodellen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9c573-116">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
8. <span data-ttu-id="9c573-117">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9c573-117">Click OK.</span></span>
9. <span data-ttu-id="9c573-118">Wählen Sie im Feld "Konfigurationen wiederverwenden" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="9c573-118">In the Reuse configurations field, select an option.</span></span>
    * <span data-ttu-id="9c573-119">Wenn der Parameter "Konfigurationen wiederverwenden" auf "Ja" festgelegt wird, prüft das System nach jeder Konfigurationssitzung auf identische Konfigurationen und verwendet sie erneut , wenn eine komplette Übereinstimmung gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="9c573-119">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="9c573-120">Attribute hinzufügen</span><span class="sxs-lookup"><span data-stu-id="9c573-120">Add attributes</span></span>
1. <span data-ttu-id="9c573-121">Erweitern Sie den Abschnitt "Attribute".</span><span class="sxs-lookup"><span data-stu-id="9c573-121">Expand the Attributes section.</span></span>
2. <span data-ttu-id="9c573-122">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9c573-122">Click Add.</span></span>
3. <span data-ttu-id="9c573-123">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="9c573-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="9c573-124">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9c573-124">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9c573-125">Geben Sie im Feld "Solver-Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9c573-125">In the Solver name field, type a value.</span></span>
    * <span data-ttu-id="9c573-126">Der Solver-Name wird vom Einschränkungswandler des Variantenkonfigurators verwendet.</span><span class="sxs-lookup"><span data-stu-id="9c573-126">The Solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="9c573-127">Er darf keine Leerzeichen oder Sonderzeichen mit Ausnahme von _ (Unterstrich) enthalten.</span><span class="sxs-lookup"><span data-stu-id="9c573-127">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="9c573-128">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9c573-128">In the Description field, type a value.</span></span>
    * <span data-ttu-id="9c573-129">Der Beschreibungstext wird dem Konfigurationsbenutzer angezeigt und kann somit als Hilfe im Auswählen des richtigen Attributwerts dienen.</span><span class="sxs-lookup"><span data-stu-id="9c573-129">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="9c573-130">Geben Sie im Feld "Attribut" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9c573-130">In the Attribute type field, enter or select a value.</span></span>
    * <span data-ttu-id="9c573-131">Der Attributtyp bestimmt, welche Werte für das Attribut verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="9c573-131">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="9c573-132">Wählen Sie das Kontrollkästchen "In Wiederverwendung einbeziehen".</span><span class="sxs-lookup"><span data-stu-id="9c573-132">Select the Include in reuse check box.</span></span>
    * <span data-ttu-id="9c573-133">Diese Option ist nur verfügbar, wenn die Option "Konfigurationen wiederverwenden" ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="9c573-133">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="9c573-134">Wenn Sie die Attribute für das Kontrollkästchen "In Wiederverwendung einbeziehen" aktivieren, wird dieses Attribut berücksichtigt, wenn das System nach einer kompletten Übereinstimmung sucht.</span><span class="sxs-lookup"><span data-stu-id="9c573-134">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="9c573-135">Unterkomponenten hinzufügen</span><span class="sxs-lookup"><span data-stu-id="9c573-135">Add subcomponents</span></span>
1. <span data-ttu-id="9c573-136">Erweitern Sie den Abschnitt "Unterkomponenten".</span><span class="sxs-lookup"><span data-stu-id="9c573-136">Expand the Subcomponents section.</span></span>
2. <span data-ttu-id="9c573-137">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9c573-137">Click Add.</span></span>
3. <span data-ttu-id="9c573-138">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="9c573-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="9c573-139">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9c573-139">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9c573-140">Geben Sie im Feld "Solver-Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9c573-140">In the Solver name field, type a value.</span></span>
6. <span data-ttu-id="9c573-141">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9c573-141">In the Description field, type a value.</span></span>
7. <span data-ttu-id="9c573-142">Geben Sie im Feld ''Komponente" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9c573-142">In the Component field, enter or select a value.</span></span>
    * <span data-ttu-id="9c573-143">Jede Unterkomponente muss auf eine Komponentendefinition verweisen.</span><span class="sxs-lookup"><span data-stu-id="9c573-143">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="9c573-144">Dieser Entwurf unterstützt wiederverwendbare Komponenten und stellt sicher, dass eine Komponente, nachdem sie einmal definiert wurde, in vielen Produktmodellen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9c573-144">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="9c573-145">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="9c573-145">Click Save.</span></span>
9. <span data-ttu-id="9c573-146">Klicken Sie auf "Stücklistenpositionsdetails".</span><span class="sxs-lookup"><span data-stu-id="9c573-146">Click BOM line details.</span></span>
    * <span data-ttu-id="9c573-147">Das Formular "Stücklistenpositionsdetail"ermöglicht dem Benutzer, die erforderlichen Eigenschaften für die Unterkomponente auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="9c573-147">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="9c573-148">Jeder Eigenschaft kann ein fester Wert oder ein Attribute zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="9c573-148">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="9c573-149">Die Zuordnung zu einem Attribut führt dazu, dass der Stücklistenabrechnungscode, verschiedene Werte abhängig von der Konfigurationsauswahl abruft.</span><span class="sxs-lookup"><span data-stu-id="9c573-149">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="9c573-150">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9c573-150">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="9c573-151">Jede Unterkomponente stellt einen konfigurierbaren Produktmaster mit einschränkungsbasierten Konfigurationtechnologie dar.</span><span class="sxs-lookup"><span data-stu-id="9c573-151">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="9c573-152">Die Referenz wird durch die Artikelnummer vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="9c573-152">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="9c573-153">Wählen Sie das Kontrollkästchen "Festlegen" aus.</span><span class="sxs-lookup"><span data-stu-id="9c573-153">Select the Set check box.</span></span>
12. <span data-ttu-id="9c573-154">Wählen Sie "Ja" im Feld "Berechnung" aus.</span><span class="sxs-lookup"><span data-stu-id="9c573-154">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="9c573-155">Das Festlegen der Berechnungsoption stellt sicher, dass das Produkt enthalten ist, wenn eine Kostenberechnung für das Produkt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9c573-155">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="9c573-156">Klicken Sie auf die Registerkarte "Einstellungen".</span><span class="sxs-lookup"><span data-stu-id="9c573-156">Click the Setup tab.</span></span>
14. <span data-ttu-id="9c573-157">Wählen Sie das Kontrollkästchen "Festlegen" aus.</span><span class="sxs-lookup"><span data-stu-id="9c573-157">Select the Set check box.</span></span>
15. <span data-ttu-id="9c573-158">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="9c573-158">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="9c573-159">Das Feld "Menge" bestimmt, wie viel von diesem Produkt im konfigurierten Produkt verbraucht wird.</span><span class="sxs-lookup"><span data-stu-id="9c573-159">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="9c573-160">Wählen Sie das Kontrollkästchen "Festlegen" aus.</span><span class="sxs-lookup"><span data-stu-id="9c573-160">Select the Set check box.</span></span>
17. <span data-ttu-id="9c573-161">Geben Sie im Feld "Pro Serie" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="9c573-161">In the Per series field, enter a number.</span></span>
18. <span data-ttu-id="9c573-162">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9c573-162">Click OK.</span></span>

