---
title: Artikelqualitätsgruppen
description: Dieses Thema beschreibt die Verwendung und das Erstellen von Element-Qualitätsgruppen, um Produkte logisch zu gruppieren, so dass sie Qualitätsverbänden für die automatische Generierung von Qualitätsprüfungsaufträgen zugewiesen werden können.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 272cb748e0a2722d9744fe6b357d767a1d6aeb26
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022251"
---
# <a name="item-quality-groups"></a><span data-ttu-id="be746-103">Artikelqualitätsgruppen</span><span class="sxs-lookup"><span data-stu-id="be746-103">Item quality groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be746-104">Eine Qualitätsgruppe gibt Aufschluss über allgemeine Testanforderungen für Artikel.</span><span class="sxs-lookup"><span data-stu-id="be746-104">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="be746-105">Dieses Thema beschreibt die Verwendung und das Erstellen von Element-Qualitätsgruppen, um Produkte logisch zu gruppieren, so dass sie Qualitätsverbänden für die automatische Generierung von Qualitätsprüfungsaufträgen zugewiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="be746-105">This topic describes how to use and create item quality groups to logically group products so that they can be assigned to quality associations for the automatic generation of quality orders.</span></span>

<span data-ttu-id="be746-106">Um die Elemente, die einer Qualitätsgruppe zugeordnet sind, oder die Qualitätsgruppen, die einem Element zugeordnet sind, einzurichten, zu bearbeiten und anzuzeigen, gehen Sie zu **Bestandsmanagement \> Einrichten \> Qualitätsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="be746-106">To set up, edit, and view the items that are assigned to a quality group, or the quality groups that are assigned to an item, go to **Inventory management \> Setup \> Quality groups**.</span></span> <span data-ttu-id="be746-107">Nachdem Sie die Testanforderungen auf der Seite **Testgruppen** definiert haben, können die Regeln für die automatische Generierung von Qualitätsprüfungsaufträgen definieren.</span><span class="sxs-lookup"><span data-stu-id="be746-107">After you define the test requirements on the **Test groups** page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="be746-108">Um den Prozess zu vereinfachen, definieren Sie keine Regeln für einzelne Elemente.</span><span class="sxs-lookup"><span data-stu-id="be746-108">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="be746-109">Stattdessen können Sie die Regeln für eine Qualitätsgruppe auf der Seite **Qualitätszuordnungen** definieren.</span><span class="sxs-lookup"><span data-stu-id="be746-109">Instead, you can define the rules for a quality group on the **Quality associations** page.</span></span>

## <a name="example-of-an-item-quality-group"></a><span data-ttu-id="be746-110">Beispiel für eine Element-Qualitätsgruppe</span><span class="sxs-lookup"><span data-stu-id="be746-110">Example of an item quality group</span></span>

<span data-ttu-id="be746-111">Ein Produktionsunternehmen erwirbt verschiedene Rohstoffe, bei denen die gleichen Testanforderungen zur Prüfung eingehender Waren gelten.</span><span class="sxs-lookup"><span data-stu-id="be746-111">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="be746-112">Daher definiert die Firma eine Qualitätsgruppe und ordnet dieser Gruppe dann die Elementnummern zu, die mit den Rohstoffen verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="be746-112">Therefore, the company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="be746-113">Später erwirbt das Unternehmen einen neuen Rohstofftyp, für den die gleichen Testanforderungen gelten.</span><span class="sxs-lookup"><span data-stu-id="be746-113">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="be746-114">Anstatt neue Testanforderungen für den neuen Rohstoff einzurichten, fügt das Unternehmen die Artikelnummer neuen Materials der vorhandenen Qualitätsgruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="be746-114">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span>

<span data-ttu-id="be746-115">Dieselbe Firma produziert auch Elemente, die die gleichen Anforderungen an die Produktionstests haben und versendet Elemente, die die gleichen Anforderungen an die Tests vor dem Versand haben.</span><span class="sxs-lookup"><span data-stu-id="be746-115">The same company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="be746-116">Daher definiert die Firma zwei weitere Qualitätsgruppen und ordnet dann jeder Gruppe die entsprechenden Element-Nummern zu.</span><span class="sxs-lookup"><span data-stu-id="be746-116">Therefore, the company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="be746-117">Eine Qualitätsgruppe erstellen</span><span class="sxs-lookup"><span data-stu-id="be746-117">Create a quality group</span></span>

<span data-ttu-id="be746-118">Um eine Qualitätsgruppe zu erstellen, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="be746-118">To create a quality group, follow these steps.</span></span>

1. <span data-ttu-id="be746-119">Wechseln Sie zu **Inventarverwaltung \> Einrichten \> Qualitätskontrolle \> Qualitätsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="be746-119">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="be746-120">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="be746-120">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="be746-121">Legen Sie für die neue Zeile die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="be746-121">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="be746-122">**Qualitätsgruppe** – Geben Sie eine eindeutige ID oder einen Namen für die Qualitätsgruppe ein.</span><span class="sxs-lookup"><span data-stu-id="be746-122">**Quality group** – Enter a unique ID or name for the quality group.</span></span>
    - <span data-ttu-id="be746-123">**Beschreibung** – Geben Sie eine detaillierte Beschreibung der Qualitätsgruppe ein.</span><span class="sxs-lookup"><span data-stu-id="be746-123">**Description** – Enter a detailed description of the quality group.</span></span>

1. <span data-ttu-id="be746-124">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="be746-124">Close the page.</span></span>

## <a name="manually-add-items-to-a-quality-group"></a><span data-ttu-id="be746-125">Manuelles Hinzufügen von Elementen zu einer Qualitätsgruppe</span><span class="sxs-lookup"><span data-stu-id="be746-125">Manually add items to a quality group</span></span>

<span data-ttu-id="be746-126">Um Elemente manuell zu einer Qualitätsgruppe hinzuzufügen, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="be746-126">To manually add items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="be746-127">Wechseln Sie zu **Inventarverwaltung \> Einrichten \> Qualitätskontrolle \> Qualitätsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="be746-127">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="be746-128">Wählen Sie die Qualitätsgruppe aus, der Sie Elemente hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="be746-128">Select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="be746-129">Klicken Sie im Aktivitätsbereich auf **Artikel**.</span><span class="sxs-lookup"><span data-stu-id="be746-129">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="be746-130">Wählen Sie auf der Seite **Elemente in Qualitätsgruppen** im Aktivitätsbereich **Neu**, um dem Raster eine Zeile hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="be746-130">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="be746-131">Legen Sie dann für die neue Zeile das Feld **Artikelnummer** auf die Artikelnummer fest, die Sie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="be746-131">Then, for the new row, set the **Item number** field to the item number that you want to add.</span></span>
1. <span data-ttu-id="be746-132">Wiederholen Sie den vorherigen Schritt für jedes zusätzliche Element, das hinzugefügt werden muss.</span><span class="sxs-lookup"><span data-stu-id="be746-132">Repeat the previous step for each additional item that must be added.</span></span>
1. <span data-ttu-id="be746-133">Schließen Sie die Seiten.</span><span class="sxs-lookup"><span data-stu-id="be746-133">Close the pages.</span></span>

## <a name="add-multiple-items-to-a-quality-group"></a><span data-ttu-id="be746-134">Hinzufügen mehrerer Elemente zu einer Qualitätsgruppe</span><span class="sxs-lookup"><span data-stu-id="be746-134">Add multiple items to a quality group</span></span>

<span data-ttu-id="be746-135">Um mehrere Elemente zu einer Qualitätsgruppe hinzuzufügen, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="be746-135">To add multiple items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="be746-136">Wechseln Sie zu **Inventarverwaltung \> Einrichten \> Qualitätskontrolle \> Qualitätsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="be746-136">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="be746-137">Erstellen oder wählen Sie die Qualitätsgruppe, zu der Sie Elemente hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="be746-137">Create or select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="be746-138">Klicken Sie im Aktivitätsbereich auf **Artikel hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="be746-138">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="be746-139">Geben Sie im Dialogfeld **Abfrage** die Filterkriterien für die Elemente ein, die Sie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="be746-139">In the **Inquiry** dialog box, enter the filter criteria for the items that you want to add.</span></span> <span data-ttu-id="be746-140">Sie könnten z. B. nach allen Elementen in einer bestimmten Elementgruppe filtern.</span><span class="sxs-lookup"><span data-stu-id="be746-140">For example, you might filter for all items in a specific item group.</span></span>
1. <span data-ttu-id="be746-141">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="be746-141">Select **OK**.</span></span>
1. <span data-ttu-id="be746-142">Im Dialogfeld **Elemente hinzufügen** werden in einem Raster alle Elemente angezeigt, die Ihrer Abfrage entsprechen.</span><span class="sxs-lookup"><span data-stu-id="be746-142">In the **Add items** dialog box, a grid shows all the items that match your query.</span></span> <span data-ttu-id="be746-143">Überprüfen Sie die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="be746-143">Review the results.</span></span>

    <span data-ttu-id="be746-144">Wenn Änderungen erforderlich sind, wählen Sie **Auswählen**, um zum Dialogfeld **Abfrage** zurückzukehren, und passen Sie Ihre Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="be746-144">If any changes are required, select **Select** to return to the **Inquiry** dialog box, and adjust your query.</span></span>

1. <span data-ttu-id="be746-145">Wenn die Ergebnisse alle Elemente enthalten, die Sie hinzufügen möchten, wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="be746-145">When the results include all the items that you want to add, select **OK**.</span></span>
1. <span data-ttu-id="be746-146">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="be746-146">Close the page.</span></span>

## <a name="manually-associate-an-item-with-a-quality-group"></a><span data-ttu-id="be746-147">Manuelles Zuordnen eines Elements zu einer Qualitätsgruppe</span><span class="sxs-lookup"><span data-stu-id="be746-147">Manually associate an item with a quality group</span></span>

<span data-ttu-id="be746-148">Um ein Element manuell mit einer Qualitätsgruppe zu verknüpfen, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="be746-148">To manually associate an item with a quality group, follow these steps.</span></span>

1. <span data-ttu-id="be746-149">Gehen Sie zu **Bestandsverwaltung \> Einrichten \> Qualitätskontrolle \> Element-Qualitätsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="be746-149">Go to **Inventory management \> Setup \> Quality control \> Item quality groups**.</span></span>
1. <span data-ttu-id="be746-150">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="be746-150">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="be746-151">Legen Sie für die neue Zeile die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="be746-151">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="be746-152">**Elementnummer** – Wählen Sie die Elementnummer, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="be746-152">**Item number** – Select the item number to add.</span></span>
    - <span data-ttu-id="be746-153">**Qualitätsgruppe** – Wählen Sie die Qualitätsgruppe, die dem Element zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="be746-153">**Quality group** – Select the quality group to assign to the item.</span></span>

1. <span data-ttu-id="be746-154">Wiederholen Sie den vorherigen Schritt für jede zusätzliche Kombination aus einem Element und einer Qualitätsgruppe, die hinzugefügt werden muss.</span><span class="sxs-lookup"><span data-stu-id="be746-154">Repeat the previous step for each additional combination of an item and a quality group that must be added.</span></span>
1. <span data-ttu-id="be746-155">Schließen Sie die Seiten.</span><span class="sxs-lookup"><span data-stu-id="be746-155">Close the pages.</span></span>

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a><span data-ttu-id="be746-156">Manuelles Hinzufügen einer Qualitätsgruppe über die Seite Freigegebene Produkte</span><span class="sxs-lookup"><span data-stu-id="be746-156">Manually add a quality group from the Released products page</span></span>

<span data-ttu-id="be746-157">Um eine Qualitätsgruppe manuell von der Seite **Freigegebene Produkte** hinzuzufügen, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="be746-157">To manually add a quality group from the **Released products** page, follow these steps.</span></span>

1. <span data-ttu-id="be746-158">Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="be746-158">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="be746-159">Wählen Sie das Produkt, dem Sie eine Qualitätsgruppe zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="be746-159">Select the product that you want to assign a quality group to.</span></span>
1. <span data-ttu-id="be746-160">Im Aktivitätsbereich, auf der Registerkarte **Lagerbestand verwalten**, in der Gruppe **Qualität**, wählen Sie **Qualitätsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="be746-160">On the Action Pane, on the **Manage inventory** tab, in the **Quality** group, select **Item quality groups**.</span></span>
1. <span data-ttu-id="be746-161">Wählen Sie auf der Seite **Elemente in Qualitätsgruppen** im Aktivitätsbereich **Neu**, um dem Raster eine Zeile hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="be746-161">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="be746-162">Legen Sie dann für die neue Zeile das Feld **Qualitätsgruppe** auf die Qualitätsgruppe fest, die Sie dem Produkt zuweisen wollen.</span><span class="sxs-lookup"><span data-stu-id="be746-162">Then, for the new row, set the **Quality group** field to the quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="be746-163">Wiederholen Sie den vorherigen Schritt für jede zusätzliche Qualitätsgruppe, die Sie dem Produkt zuweisen wollen.</span><span class="sxs-lookup"><span data-stu-id="be746-163">Repeat the previous step for each additional quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="be746-164">Schließen Sie die Seiten.</span><span class="sxs-lookup"><span data-stu-id="be746-164">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be746-165">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="be746-165">Additional resources</span></span>

- [<span data-ttu-id="be746-166">Qualitätsmanagement Testinstrumente</span><span class="sxs-lookup"><span data-stu-id="be746-166">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="be746-167">Qualitätsmanagement-Tests</span><span class="sxs-lookup"><span data-stu-id="be746-167">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="be746-168">Qualitätsmanagement Testgruppen</span><span class="sxs-lookup"><span data-stu-id="be746-168">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="be746-169">Qualitätsmanagement-Testvariablen</span><span class="sxs-lookup"><span data-stu-id="be746-169">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="be746-170">Qualitätszuordnungen</span><span class="sxs-lookup"><span data-stu-id="be746-170">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
