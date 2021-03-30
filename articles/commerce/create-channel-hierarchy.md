---
title: Eine Kanalnavigationshierarchie erstellen
description: In diesem Thema wird beschrieben, wie eine Kanalnavigationshierarchie in Microsoft Dynamics 365 Commerce erstellt wird.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 2e1462c10dfe1c858429e9f4cc5d720ca43df609
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221328"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="da662-103">Eine Kanalnavigationshierarchie erstellen</span><span class="sxs-lookup"><span data-stu-id="da662-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="da662-104">In diesem Thema wird beschrieben, wie eine Kanalnavigationshierarchie in Microsoft Dynamics 365 Commerce erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="da662-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="da662-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="da662-105">Overview</span></span>

<span data-ttu-id="da662-106">Eine Kanalnavigationshierarchie dient zur Gruppierung und Organisierung von Produkten in Kategorien, sodass die Produkte online oder an einer Verkaufsstelle (POS) durchsucht werden können.</span><span class="sxs-lookup"><span data-stu-id="da662-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="da662-107">Eine Kanalnavigationshierarchie erstellen</span><span class="sxs-lookup"><span data-stu-id="da662-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="da662-108">Um eine Kanalnavigationshierarchie zu erstellen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="da662-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="da662-109">Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Produkte und Kategorien \> Kanalnavigationskategorien**.</span><span class="sxs-lookup"><span data-stu-id="da662-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="da662-110">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="da662-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="da662-111">Geben Sie im Kästchen **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="da662-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="da662-112">Geben Sie im Kästchen **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="da662-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="da662-113">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="da662-113">Select **Create**.</span></span>
1. <span data-ttu-id="da662-114">Wählen Sie im Aktionsbereich **Neuer Kategorieknoten**, um einen Stammknoten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="da662-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="da662-115">Geben Sie im Kästchen **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="da662-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="da662-116">Geben Sie im Kästchen **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="da662-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="da662-117">Geben Sie in das Feld **Anzeigename** einen Anzeigename ein.</span><span class="sxs-lookup"><span data-stu-id="da662-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="da662-118">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="da662-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="da662-119">Die folgende Abbildung zeigt einen beispielhaften Stammknoten.</span><span class="sxs-lookup"><span data-stu-id="da662-119">The following image shows a example root node.</span></span>

![Beispiel für einen Stammknoten](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="da662-121">Navigationskategorieknoten erstellen</span><span class="sxs-lookup"><span data-stu-id="da662-121">Create navigation category nodes</span></span>

<span data-ttu-id="da662-122">Gehen Sie folgendermaßen vor, um zusätzliche Navigationskategorieknoten zu erstellen, um die Produktkategorien auf dem Kanal darzustellen.</span><span class="sxs-lookup"><span data-stu-id="da662-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="da662-123">Wählen Sie im Navigationsbereich den übergeordneten Knoten aus, dem Sie eine Kategorie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="da662-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="da662-124">Klicken Sie im Aktivitätsbereich auf **Neuer Kategorieknoten**.</span><span class="sxs-lookup"><span data-stu-id="da662-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="da662-125">Geben Sie im Kästchen **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="da662-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="da662-126">Geben Sie im Kästchen **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="da662-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="da662-127">Geben Sie in das Feld **Anzeigename** einen Anzeigename ein.</span><span class="sxs-lookup"><span data-stu-id="da662-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="da662-128">Geben Sie im Feld **Anzeigereihenfolge** eine Anzeigereihenfolge ein (optional).</span><span class="sxs-lookup"><span data-stu-id="da662-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="da662-129">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="da662-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="da662-130">Das folgende Bild zeigt ein Beispiel einer vollständigen Kanalnavigationshierarchie.</span><span class="sxs-lookup"><span data-stu-id="da662-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![Beispiel einer Kanalhierarchie](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="da662-132">Produkte zu Kategorieknoten hinzufügen</span><span class="sxs-lookup"><span data-stu-id="da662-132">Add products to category nodes</span></span>

<span data-ttu-id="da662-133">Gehen Sie folgendermaßen vor, um Produkte zu Kategorieknoten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="da662-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="da662-134">Wählen Sie einen Kategorieknoten aus.</span><span class="sxs-lookup"><span data-stu-id="da662-134">Select a category node.</span></span>
1. <span data-ttu-id="da662-135">Wählen Sie unter **Produkte** die Option **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="da662-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="da662-136">Suchen Sie die neuen Produkte, die Sie hinzufügen möchten, anhand der Produktnummer oder des Produktnamens und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="da662-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="da662-137">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="da662-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="da662-138">Das Hinzufügen von Produkten zu einem Knoten in der Kanalnavigationshierarchie reicht nicht aus, damit die Produkte in einem ausgewählten Kanal angezeigt werden. Die Produkte müssen auch zu einem Produkt sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="da662-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a product.</span></span>

<span data-ttu-id="da662-139">Das folgende Bild zeigt einen Beispielknoten mit hinzugefügten Produkten.</span><span class="sxs-lookup"><span data-stu-id="da662-139">The following image shows an example node with products added.</span></span>

![Produkte zu einem Kategorieknoten hinzufügt](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="da662-141">Produktattributgruppen zu Kategorieknoten hinzufügen</span><span class="sxs-lookup"><span data-stu-id="da662-141">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="da662-142">Attributgruppen müssen erstellt werden, bevor Sie sie einem Knoten in der Kanalnavigationshierarchie hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="da662-142">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="da662-143">Befolgen Sie diese Schritte, um ein Produkt einer Attributgruppe zu einem Kategorieknoten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="da662-143">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="da662-144">Wählen Sie einen Kategorieknoten aus.</span><span class="sxs-lookup"><span data-stu-id="da662-144">Select a category node.</span></span>
1. <span data-ttu-id="da662-145">Wählen Sie unter **Produktattributgruppe** die Option **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="da662-145">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="da662-146">Suchen Sie die Attributgruppen, die Sie hinzufügen möchten, und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="da662-146">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="da662-147">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="da662-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="da662-148">Das folgende Bild zeigt einen Beispielknoten mit hinzugefügten Produktattributgruppen.</span><span class="sxs-lookup"><span data-stu-id="da662-148">The following image shows a sample node with product attribute groups added.</span></span>

![Produktattributgruppen auf einem Knoten](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="da662-150">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="da662-150">Additional resources</span></span>

[<span data-ttu-id="da662-151">Sortimente einrichten</span><span class="sxs-lookup"><span data-stu-id="da662-151">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="da662-152">Attribute und Attributgruppen verwalten</span><span class="sxs-lookup"><span data-stu-id="da662-152">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]