---
title: Produktkonfigurationsmodell erstellen
description: Im folgenden Verfahren wird gezeigt, wie ein Produktkonfigurationsmodell erstellt wird und grundlegende Informationen wie Attribute und Unterkomponenten eingegeben werden.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cb9e33d7bab6ca9cd378ec40baa796d1a933ece
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921364"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="53011-103">Produktkonfigurationsmodell erstellen</span><span class="sxs-lookup"><span data-stu-id="53011-103">Create a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="53011-104">Im folgenden Verfahren wird gezeigt, wie ein Produktkonfigurationsmodell erstellt wird und grundlegende Informationen wie Attribute und Unterkomponenten eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="53011-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="53011-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="53011-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="53011-106">Erstellen eines Produktmodells</span><span class="sxs-lookup"><span data-stu-id="53011-106">Create a product model</span></span>

1. <span data-ttu-id="53011-107">Wechseln Sie zu **Produktinformationsmanagement \> Produkte \> Produktkonfigurationsmodelle**.</span><span class="sxs-lookup"><span data-stu-id="53011-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="53011-108">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="53011-108">Select **New**.</span></span>
1. <span data-ttu-id="53011-109">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="53011-109">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="53011-110">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="53011-110">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="53011-111">Wählen Sie im Feld **Löserstrategie** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="53011-111">In the **Solver strategy** field, select an option.</span></span>
    * <span data-ttu-id="53011-112">Die Solver-Strategie bestimmt, wie die Einschränkungen in einem einschränkungsbasierten Produktkonfigurationsmodell verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="53011-112">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="53011-113">Diese Auswahl kann Auswirkungen auf die Leistung des Produktkonfigurationsmodells haben.</span><span class="sxs-lookup"><span data-stu-id="53011-113">This selection can have an impact on the performance of the product configuration model.</span></span>  
1. <span data-ttu-id="53011-114">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="53011-114">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="53011-115">Die Stammkomponente stellt das Produktkonfigurationsmodell dar, kann jedoch auch in anderen Produktmodellen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="53011-115">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
1. <span data-ttu-id="53011-116">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="53011-116">Select **OK**.</span></span>
1. <span data-ttu-id="53011-117">Wählen Sie im Feld **Konfigurationen wiederverwenden** eine Option.</span><span class="sxs-lookup"><span data-stu-id="53011-117">In the **Reuse configurations** field, select an option.</span></span>
    * <span data-ttu-id="53011-118">Wenn der Parameter "Konfigurationen wiederverwenden" auf "Ja" festgelegt wird, prüft das System nach jeder Konfigurationssitzung auf identische Konfigurationen und verwendet sie erneut , wenn eine komplette Übereinstimmung gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="53011-118">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="53011-119">Attribute hinzufügen</span><span class="sxs-lookup"><span data-stu-id="53011-119">Add attributes</span></span>

1. <span data-ttu-id="53011-120">Erweitern Sie den Abschnitt **Attribute**.</span><span class="sxs-lookup"><span data-stu-id="53011-120">Expand the **Attributes** section.</span></span>
2. <span data-ttu-id="53011-121">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="53011-121">Select **Add**.</span></span>
3. <span data-ttu-id="53011-122">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="53011-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="53011-123">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="53011-123">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="53011-124">Geben Sie in das Feld **Lösername** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="53011-124">In the **Solver name** field, type a value.</span></span>
    * <span data-ttu-id="53011-125">Der Solver-Name wird vom Constraint-Solver des Produktkonfigurators verwendet.</span><span class="sxs-lookup"><span data-stu-id="53011-125">The solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="53011-126">Er darf keine Leerzeichen oder Sonderzeichen mit Ausnahme von _ (Unterstrich) enthalten.</span><span class="sxs-lookup"><span data-stu-id="53011-126">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="53011-127">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="53011-127">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="53011-128">Der Beschreibungstext wird dem Konfigurationsbenutzer angezeigt und kann somit als Hilfe im Auswählen des richtigen Attributwerts dienen.</span><span class="sxs-lookup"><span data-stu-id="53011-128">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="53011-129">Geben Sie in das Feld **Attribut-Typ** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="53011-129">In the **Attribute type** field, enter or select a value.</span></span>
    * <span data-ttu-id="53011-130">Der Attributtyp bestimmt, welche Werte für das Attribut verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="53011-130">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="53011-131">Aktivieren Sie das Kontrollkästchen **Bei Wiederverwendung einbeziehen**.</span><span class="sxs-lookup"><span data-stu-id="53011-131">Select the **Include in reuse** check box.</span></span>
    * <span data-ttu-id="53011-132">Diese Option ist nur verfügbar, wenn die Option "Konfigurationen wiederverwenden" ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="53011-132">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="53011-133">Wenn Sie die Attribute für das Kontrollkästchen "In Wiederverwendung einbeziehen" aktivieren, wird dieses Attribut berücksichtigt, wenn das System nach einer kompletten Übereinstimmung sucht.</span><span class="sxs-lookup"><span data-stu-id="53011-133">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="53011-134">Unterkomponenten hinzufügen</span><span class="sxs-lookup"><span data-stu-id="53011-134">Add subcomponents</span></span>

1. <span data-ttu-id="53011-135">Erweitern Sie den Abschnitt **Unterkomponenten**.</span><span class="sxs-lookup"><span data-stu-id="53011-135">Expand the **Subcomponents** section.</span></span>
2. <span data-ttu-id="53011-136">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="53011-136">Select **Add**.</span></span>
3. <span data-ttu-id="53011-137">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="53011-137">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="53011-138">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="53011-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="53011-139">Geben Sie in das Feld **Lösername** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="53011-139">In the **Solver name** field, type a value.</span></span>
6. <span data-ttu-id="53011-140">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="53011-140">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="53011-141">Geben Sie im Feld **Komponente** einen Wert ein oder wählen Sie einen aus.</span><span class="sxs-lookup"><span data-stu-id="53011-141">In the **Component** field, enter or select a value.</span></span>
    * <span data-ttu-id="53011-142">Jede Unterkomponente muss auf eine Komponentendefinition verweisen.</span><span class="sxs-lookup"><span data-stu-id="53011-142">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="53011-143">Dieser Entwurf unterstützt wiederverwendbare Komponenten und stellt sicher, dass eine Komponente, nachdem sie einmal definiert wurde, in vielen Produktmodellen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="53011-143">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="53011-144">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="53011-144">Select **Save**.</span></span>
9. <span data-ttu-id="53011-145">Wählen Sie **Stücklisten-Zeilen-Details**.</span><span class="sxs-lookup"><span data-stu-id="53011-145">Select **BOM line details**.</span></span>
    * <span data-ttu-id="53011-146">Das Formular "Stücklistenpositionsdetail"ermöglicht dem Benutzer, die erforderlichen Eigenschaften für die Unterkomponente auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="53011-146">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="53011-147">Jeder Eigenschaft kann ein fester Wert oder ein Attribute zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="53011-147">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="53011-148">Die Zuordnung zu einem Attribut führt dazu, dass der Stücklistenabrechnungscode, verschiedene Werte abhängig von der Konfigurationsauswahl abruft.</span><span class="sxs-lookup"><span data-stu-id="53011-148">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="53011-149">Geben Sie im Feld **Artikelnummer** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="53011-149">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="53011-150">Jede Unterkomponente stellt einen konfigurierbaren Produktmaster mit einschränkungsbasierten Konfigurationtechnologie dar.</span><span class="sxs-lookup"><span data-stu-id="53011-150">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="53011-151">Die Referenz wird durch die Artikelnummer vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="53011-151">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="53011-152">Aktivieren Sie das Kontrollkästchen **Setzen**.</span><span class="sxs-lookup"><span data-stu-id="53011-152">Select the **Set** check box.</span></span>
12. <span data-ttu-id="53011-153">Wählen Sie **Ja** im Feld **Berechnung**.</span><span class="sxs-lookup"><span data-stu-id="53011-153">Select **Yes** in the **Calculation** field.</span></span>
    * <span data-ttu-id="53011-154">Das Festlegen der Berechnungsoption stellt sicher, dass das Produkt enthalten ist, wenn eine Kostenberechnung für das Produkt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="53011-154">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="53011-155">Wählen Sie die Registerkarte **Einrichten**.</span><span class="sxs-lookup"><span data-stu-id="53011-155">Select the **Setup** tab.</span></span>
14. <span data-ttu-id="53011-156">Aktivieren Sie das Kontrollkästchen **Setzen**.</span><span class="sxs-lookup"><span data-stu-id="53011-156">Select the **Set** check box.</span></span>
15. <span data-ttu-id="53011-157">Geben Sie im Feld **Menge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="53011-157">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="53011-158">Das Feld "Menge" bestimmt, wie viel von diesem Produkt im konfigurierten Produkt verbraucht wird.</span><span class="sxs-lookup"><span data-stu-id="53011-158">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="53011-159">Aktivieren Sie das Kontrollkästchen **Setzen**.</span><span class="sxs-lookup"><span data-stu-id="53011-159">Select the **Set** check box.</span></span>
17. <span data-ttu-id="53011-160">Geben Sie in das Feld **Per Serie** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="53011-160">In the **Per series** field, enter a number.</span></span>
18. <span data-ttu-id="53011-161">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="53011-161">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]