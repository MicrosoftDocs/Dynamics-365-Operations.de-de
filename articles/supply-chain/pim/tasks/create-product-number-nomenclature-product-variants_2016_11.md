---
title: Produktnummernbezeichnung für konfigurierte Produktvarianten erstellen
description: Diese Verfahren zeigt, wie eine Produktnummerenbezeichnung für konfigurierte Produktvarianten eingerichtet wird und sie einem konfigurierbaren Produktmaster zugeordnet werden kann.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ea30dc107213b1a2c6b2a109188066a6ea82159
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921010"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="5dfaf-103">Produktnummernbezeichnung für konfigurierte Produktvarianten erstellen</span><span class="sxs-lookup"><span data-stu-id="5dfaf-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5dfaf-104">Diese Verfahren zeigt, wie eine Produktnummerenbezeichnung für konfigurierte Produktvarianten eingerichtet wird und sie einem konfigurierbaren Produktmaster zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="5dfaf-105">Dieses Verfahren beschreibt auch, wie eine Konfigurationsbezeichnung für eine Produktkonfigurationsmodellkomponente erstellen wird.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="5dfaf-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5dfaf-107">Die neue Produktnummernbezeichnung wird dem Produktmaster D0004 zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="5dfaf-108">Diese Aufgabe erfolgt in der Regel durch einen Produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-108">This task would typically be done by a product designer.</span></span>

## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="5dfaf-109">Erstellen eine Produktnummerbezeichnung</span><span class="sxs-lookup"><span data-stu-id="5dfaf-109">Create a product number nomenclature</span></span>

1. <span data-ttu-id="5dfaf-110">Wechseln Sie zu **Produktinformationsmanagement \> Einrichten \> Produktbezeichnung**.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-110">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="5dfaf-111">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-111">Select **New**.</span></span>
1. <span data-ttu-id="5dfaf-112">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="5dfaf-113">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-113">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="5dfaf-114">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-114">Select **Add**.</span></span>
1. <span data-ttu-id="5dfaf-115">Wählen Sie **Produktstammnummer**.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-115">Select **Product master number**.</span></span>
1. <span data-ttu-id="5dfaf-116">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-116">Select **Add**.</span></span>
1. <span data-ttu-id="5dfaf-117">Wählen Sie **Textkonstante** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-117">Select **Text constant**.</span></span>
1. <span data-ttu-id="5dfaf-118">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-118">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5dfaf-119">Geben Sie im Feld **Text** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-119">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="5dfaf-120">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-120">Select **Add**.</span></span>
1. <span data-ttu-id="5dfaf-121">Wählen Sie **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-121">Select **Configuration**.</span></span>
1. <span data-ttu-id="5dfaf-122">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-122">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="5dfaf-123">Zuweisen der Produktnummernbezeichnung zu einem Produktmaster</span><span class="sxs-lookup"><span data-stu-id="5dfaf-123">Assign the product number nomenclature to a product master</span></span>

1. <span data-ttu-id="5dfaf-124">Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Produktmaster**.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-124">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="5dfaf-125">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5dfaf-126">Filtern Sie zum Beispiel auf das Feld **Produktnummer** mit dem Wert 'D'.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-126">For example, filter on the **Product number** field with a value of 'D'.</span></span>
1. <span data-ttu-id="5dfaf-127">Wählen Sie in der Liste den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-127">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="5dfaf-128">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-128">Select **Edit**.</span></span>
1. <span data-ttu-id="5dfaf-129">Wählen Sie *Ja* im Feld **Bezeichnungen verwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-129">Select *Yes* in the **Use nomenclature** field.</span></span>
1. <span data-ttu-id="5dfaf-130">Geben Sie im Feld **Produktvariantennummerbezeichnung** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-130">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
1. <span data-ttu-id="5dfaf-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-131">Close the page.</span></span>
1. <span data-ttu-id="5dfaf-132">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-132">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="5dfaf-133">Erstellen einer Bezeichnung für eine Produktkonfigurationsmodellkomponente</span><span class="sxs-lookup"><span data-stu-id="5dfaf-133">Create nomenclature for a product configuration model component</span></span>

1. <span data-ttu-id="5dfaf-134">Wechseln Sie zu **Produktinformationsmanagement \> Produkte \> Produktkonfigurationsmodelle**.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-134">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="5dfaf-135">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-135">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="5dfaf-136">Wählen Sie in der Liste den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-136">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="5dfaf-137">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-137">Select **Edit**.</span></span>
1. <span data-ttu-id="5dfaf-138">Wählen Sie *Ja* im Feld **Konfigurationsnomenklatur verwenden**.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-138">Select *Yes* in the **Use configuration nomenclature** field.</span></span>
1. <span data-ttu-id="5dfaf-139">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-139">Select **Add**.</span></span>
1. <span data-ttu-id="5dfaf-140">Wählen Sie **Attributwert**.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-140">Select **Attribute value**.</span></span>
1. <span data-ttu-id="5dfaf-141">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-141">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5dfaf-142">Geben Sie im Feld **Attribut** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-142">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="5dfaf-143">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-143">Select **Add**.</span></span>
1. <span data-ttu-id="5dfaf-144">Wählen Sie **Textkonstante** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-144">Select **Text constant**.</span></span>
1. <span data-ttu-id="5dfaf-145">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-145">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5dfaf-146">Geben Sie im Feld **Text** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-146">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="5dfaf-147">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-147">Select **Add**.</span></span>
1. <span data-ttu-id="5dfaf-148">Wählen Sie **Attributwert**.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-148">Select **Attribute value**.</span></span>
1. <span data-ttu-id="5dfaf-149">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-149">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5dfaf-150">Geben Sie im Feld **Attribut** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-150">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="5dfaf-151">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-151">Select **Add**.</span></span>
1. <span data-ttu-id="5dfaf-152">Wählen Sie **Textkonstante** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-152">Select **Text constant**.</span></span>
1. <span data-ttu-id="5dfaf-153">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-153">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5dfaf-154">Geben Sie im Feld **Text** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-154">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="5dfaf-155">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-155">Select **Add**.</span></span>
1. <span data-ttu-id="5dfaf-156">Wählen Sie **Attributwert**.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-156">Select **Attribute value**.</span></span>
1. <span data-ttu-id="5dfaf-157">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-157">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5dfaf-158">Geben Sie im Feld **Attribut** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-158">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="5dfaf-159">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-159">Select **Add**.</span></span>
1. <span data-ttu-id="5dfaf-160">Wählen Sie **Textkonstante** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-160">Select **Text constant**.</span></span>
1. <span data-ttu-id="5dfaf-161">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-161">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5dfaf-162">Geben Sie im Feld **Text** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-162">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="5dfaf-163">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-163">Select **Add**.</span></span>
1. <span data-ttu-id="5dfaf-164">Wählen Sie **Attributwert**.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-164">Select **Attribute value**.</span></span>
1. <span data-ttu-id="5dfaf-165">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-165">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5dfaf-166">Geben Sie im Feld **Attribut** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-166">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="5dfaf-167">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-167">Select **Add**.</span></span>
1. <span data-ttu-id="5dfaf-168">Wählen Sie **Textkonstante** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-168">Select **Text constant**.</span></span>
1. <span data-ttu-id="5dfaf-169">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-169">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5dfaf-170">Geben Sie im Feld **Text** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-170">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="5dfaf-171">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-171">Select **Add**.</span></span>
1. <span data-ttu-id="5dfaf-172">Wählen Sie **Nummernkreis Wert**.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-172">Select **Number sequence value**.</span></span>
1. <span data-ttu-id="5dfaf-173">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-173">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5dfaf-174">Geben Sie im Feld **Nummernkreis** einen Wert ein oder wählen Sie einen aus.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-174">In the **Number sequence** field, enter or select a value.</span></span>
1. <span data-ttu-id="5dfaf-175">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-175">Close the page.</span></span>
1. <span data-ttu-id="5dfaf-176">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-176">Close the page.</span></span>
1. <span data-ttu-id="5dfaf-177">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-177">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]