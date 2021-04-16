---
title: Eine Kanalnavigationshierarchie erstellen
description: In diesem Thema wird beschrieben, wie eine Kanalnavigationshierarchie in Microsoft Dynamics 365 Commerce erstellt wird.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 358f3d40c7a21184c20da342d6b2bf72dd4e7bbd
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795834"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="75bd1-103">Eine Kanalnavigationshierarchie erstellen</span><span class="sxs-lookup"><span data-stu-id="75bd1-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="75bd1-104">In diesem Thema wird beschrieben, wie eine Kanalnavigationshierarchie in Microsoft Dynamics 365 Commerce erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="75bd1-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="75bd1-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="75bd1-105">Overview</span></span>

<span data-ttu-id="75bd1-106">Eine Kanalnavigationshierarchie dient zur Gruppierung und Organisierung von Produkten in Kategorien, sodass die Produkte online oder an einer Verkaufsstelle (POS) durchsucht werden können.</span><span class="sxs-lookup"><span data-stu-id="75bd1-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="75bd1-107">Eine Kanalnavigationshierarchie erstellen</span><span class="sxs-lookup"><span data-stu-id="75bd1-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="75bd1-108">Um eine Kanalnavigationshierarchie zu erstellen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="75bd1-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="75bd1-109">Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Produkte und Kategorien \> Kanalnavigationskategorien**.</span><span class="sxs-lookup"><span data-stu-id="75bd1-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="75bd1-110">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="75bd1-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="75bd1-111">Geben Sie im Kästchen **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="75bd1-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="75bd1-112">Geben Sie im Kästchen **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="75bd1-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="75bd1-113">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="75bd1-113">Select **Create**.</span></span>
1. <span data-ttu-id="75bd1-114">Wählen Sie im Aktionsbereich **Neuer Kategorieknoten**, um einen Stammknoten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="75bd1-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="75bd1-115">Geben Sie im Kästchen **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="75bd1-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="75bd1-116">Geben Sie im Kästchen **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="75bd1-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="75bd1-117">Geben Sie in das Feld **Anzeigename** einen Anzeigename ein.</span><span class="sxs-lookup"><span data-stu-id="75bd1-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="75bd1-118">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="75bd1-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="75bd1-119">Die folgende Abbildung zeigt einen beispielhaften Stammknoten.</span><span class="sxs-lookup"><span data-stu-id="75bd1-119">The following image shows a example root node.</span></span>

![Beispiel für einen Stammknoten](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="75bd1-121">Navigationskategorieknoten erstellen</span><span class="sxs-lookup"><span data-stu-id="75bd1-121">Create navigation category nodes</span></span>

<span data-ttu-id="75bd1-122">Gehen Sie folgendermaßen vor, um zusätzliche Navigationskategorieknoten zu erstellen, um die Produktkategorien auf dem Kanal darzustellen.</span><span class="sxs-lookup"><span data-stu-id="75bd1-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="75bd1-123">Wählen Sie im Navigationsbereich den übergeordneten Knoten aus, dem Sie eine Kategorie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="75bd1-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="75bd1-124">Klicken Sie im Aktivitätsbereich auf **Neuer Kategorieknoten**.</span><span class="sxs-lookup"><span data-stu-id="75bd1-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="75bd1-125">Geben Sie im Kästchen **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="75bd1-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="75bd1-126">Geben Sie im Kästchen **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="75bd1-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="75bd1-127">Geben Sie in das Feld **Anzeigename** einen Anzeigename ein.</span><span class="sxs-lookup"><span data-stu-id="75bd1-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="75bd1-128">Geben Sie im Feld **Anzeigereihenfolge** eine Anzeigereihenfolge ein (optional).</span><span class="sxs-lookup"><span data-stu-id="75bd1-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="75bd1-129">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="75bd1-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="75bd1-130">Das folgende Bild zeigt ein Beispiel einer vollständigen Kanalnavigationshierarchie.</span><span class="sxs-lookup"><span data-stu-id="75bd1-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![Beispiel einer Kanalhierarchie](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="75bd1-132">Produkte zu Kategorieknoten hinzufügen</span><span class="sxs-lookup"><span data-stu-id="75bd1-132">Add products to category nodes</span></span>

<span data-ttu-id="75bd1-133">Gehen Sie folgendermaßen vor, um Produkte zu Kategorieknoten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="75bd1-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="75bd1-134">Wählen Sie einen Kategorieknoten aus.</span><span class="sxs-lookup"><span data-stu-id="75bd1-134">Select a category node.</span></span>
1. <span data-ttu-id="75bd1-135">Wählen Sie unter **Produkte** die Option **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="75bd1-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="75bd1-136">Suchen Sie die neuen Produkte, die Sie hinzufügen möchten, anhand der Produktnummer oder des Produktnamens und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="75bd1-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="75bd1-137">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="75bd1-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="75bd1-138">Das Hinzufügen von Produkten zu einem Knoten in der Kanalnavigationshierarchie reicht nicht aus, damit die Produkte in einem ausgewählten Kanal angezeigt werden. Die Produkte müssen auch zu einem Produkt sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="75bd1-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a product.</span></span>

<span data-ttu-id="75bd1-139">Das folgende Bild zeigt einen Beispielknoten mit hinzugefügten Produkten.</span><span class="sxs-lookup"><span data-stu-id="75bd1-139">The following image shows an example node with products added.</span></span>

![Produkte zu einem Kategorieknoten hinzufügt](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="75bd1-141">Produktattributgruppen zu Kategorieknoten hinzufügen</span><span class="sxs-lookup"><span data-stu-id="75bd1-141">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="75bd1-142">Attributgruppen müssen erstellt werden, bevor Sie sie einem Knoten in der Kanalnavigationshierarchie hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="75bd1-142">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="75bd1-143">Befolgen Sie diese Schritte, um ein Produkt einer Attributgruppe zu einem Kategorieknoten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="75bd1-143">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="75bd1-144">Wählen Sie einen Kategorieknoten aus.</span><span class="sxs-lookup"><span data-stu-id="75bd1-144">Select a category node.</span></span>
1. <span data-ttu-id="75bd1-145">Wählen Sie unter **Produktattributgruppe** die Option **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="75bd1-145">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="75bd1-146">Suchen Sie die Attributgruppen, die Sie hinzufügen möchten, und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="75bd1-146">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="75bd1-147">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="75bd1-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="75bd1-148">Das folgende Bild zeigt einen Beispielknoten mit hinzugefügten Produktattributgruppen.</span><span class="sxs-lookup"><span data-stu-id="75bd1-148">The following image shows a sample node with product attribute groups added.</span></span>

![Produktattributgruppen auf einem Knoten](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="75bd1-150">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="75bd1-150">Additional resources</span></span>

[<span data-ttu-id="75bd1-151">Sortimente einrichten</span><span class="sxs-lookup"><span data-stu-id="75bd1-151">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="75bd1-152">Attribute und Attributgruppen verwalten</span><span class="sxs-lookup"><span data-stu-id="75bd1-152">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]