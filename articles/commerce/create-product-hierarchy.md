---
title: Neue Produkthierarchie erstellen
description: In diesem Thema wird beschrieben, wie Sie eine neue Produkthierarchie in Microsoft Dynamics 365 Commerce erstellen.
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
ms.openlocfilehash: 8aef33a501f43105730eaa21a9159eb1398a1b36
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799564"
---
# <a name="create-a-new-product-hierarchy"></a><span data-ttu-id="1a348-103">Neue Produkthierarchie erstellen</span><span class="sxs-lookup"><span data-stu-id="1a348-103">Create a new product hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1a348-104">In diesem Thema wird beschrieben, wie Sie eine neue Produkthierarchie in Microsoft Dynamics 365 Commerce erstellen.</span><span class="sxs-lookup"><span data-stu-id="1a348-104">This topic describes how to create a new product hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1a348-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="1a348-105">Overview</span></span>

<span data-ttu-id="1a348-106">Dynamics 365 Commerce unterstützt mehrere Retail Channels.</span><span class="sxs-lookup"><span data-stu-id="1a348-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="1a348-107">Diese Vertriebskanäle umfassen Onlineshops, Callcenter und Einzelhandelsgeschäfte (auch physische Läden genannt).</span><span class="sxs-lookup"><span data-stu-id="1a348-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="1a348-108">Jeder Einzelhandelskanal kann seine eigenen Zahlungsmethoden, Preisgruppen, POS-Register, Ein- und Ausgabenkonten und Mitarbeiter einrichten.</span><span class="sxs-lookup"><span data-stu-id="1a348-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="1a348-109">Sie müssen alle Elemente einrichten, bevor Sie ein Ladengeschäftskanal erstellen können.</span><span class="sxs-lookup"><span data-stu-id="1a348-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="1a348-110">Es wird eine Commerce-Produkthierarchie verwendet, um die Gesamtprodukthierarchie für Ihre Organisation zu definieren.</span><span class="sxs-lookup"><span data-stu-id="1a348-110">A Commerce product hierarchy is used to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="1a348-111">Sie können eine Commerce-Produkthierarchie für den Verkauf, die Preisgestaltung und die verkaufsfördernden Maßnahmen, die Berichterstellung und die Sortimentsplanung verwenden.</span><span class="sxs-lookup"><span data-stu-id="1a348-111">You can use a Commerce product hierarchy for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="1a348-112">Pro Organisation kann nur eine Commerce-Produkthierarchie zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="1a348-112">Only one Commerce product hierarchy can be assigned per organization.</span></span>

## <a name="create-and-configure-a-product-hierarchy"></a><span data-ttu-id="1a348-113">Produkthierarchie erstellen und konfigurieren</span><span class="sxs-lookup"><span data-stu-id="1a348-113">Create and configure a product hierarchy</span></span>

<span data-ttu-id="1a348-114">Um eine Commerce-Produkthierarchie zu erstellen und zu konfigurieren, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="1a348-114">To create and configure a Commerce product hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="1a348-115">Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Produkte und Kategorien \> Commerce-Produkthierarchie**.</span><span class="sxs-lookup"><span data-stu-id="1a348-115">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
1. <span data-ttu-id="1a348-116">Wenn noch keine Hierarchie existiert, wählen Sie unter **Aktionsbereich** die Option **Neu**, um die Wurzel der Hierarchie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1a348-116">If no hierachy exists yet, on the **Action pane**, select **New** to create the root of the hierarchy.</span></span>
1. <span data-ttu-id="1a348-117">Unter **Allgemeines**:</span><span class="sxs-lookup"><span data-stu-id="1a348-117">Under **General**:</span></span>
    1. <span data-ttu-id="1a348-118">Geben Sie im Kästchen **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="1a348-118">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="1a348-119">Geben Sie im Kästchen **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="1a348-119">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="1a348-120">Geben Sie in das Feld **Anzeigename** einen Anzeigename ein.</span><span class="sxs-lookup"><span data-stu-id="1a348-120">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="1a348-121">Setzen Sie **Aktiv** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1a348-121">Set **Active** to **Yes**.</span></span>

## <a name="add-hierarchy-nodes"></a><span data-ttu-id="1a348-122">Hierarchieknoten hinzufügen</span><span class="sxs-lookup"><span data-stu-id="1a348-122">Add hierarchy nodes</span></span>

<span data-ttu-id="1a348-123">Gehen Sie folgendermaßen vor, um Hierarchieknoten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1a348-123">To add hierarchy nodes, follow these steps.</span></span>

1. <span data-ttu-id="1a348-124">Klicken Sie im Aktivitätsbereich auf **Kategoriehierarchie bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="1a348-124">On the action pane, select **Edit category hierarchy**.</span></span>
1. <span data-ttu-id="1a348-125">Wählen Sie den übergeordneten Knoten aus, dem Sie einen neuen Knoten hinzufügen möchten, und wählen Sie dann **Neuer Kategorieknoten** aus.</span><span class="sxs-lookup"><span data-stu-id="1a348-125">Select the parent node you want to add a new node to, and then select **New category node**.</span></span>
1. <span data-ttu-id="1a348-126">Im Abschnitt **Allgemeines** geben Sie **Name**, **Beschreibung**, **Anzeigename** und **Schlüsselwörter** ein.</span><span class="sxs-lookup"><span data-stu-id="1a348-126">In the **General** section provide a **Name**, **Description**, **Friendly name** and **Keywords**.</span></span>
1. <span data-ttu-id="1a348-127">Unter **Allgemeines**:</span><span class="sxs-lookup"><span data-stu-id="1a348-127">Under **General**:</span></span>
    1. <span data-ttu-id="1a348-128">Geben Sie im Kästchen **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="1a348-128">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="1a348-129">Geben Sie im Kästchen **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="1a348-129">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="1a348-130">Geben Sie in das Feld **Anzeigename** einen Anzeigename ein.</span><span class="sxs-lookup"><span data-stu-id="1a348-130">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="1a348-131">Geben Sie im Feld **Schlüsselwörter** die relevanten Schlüsselwörter ein.</span><span class="sxs-lookup"><span data-stu-id="1a348-131">In the **Keywords** box, enter relevant keywords.</span></span>
    1. <span data-ttu-id="1a348-132">Geben Sie im Feld **Anzeigereihenfolge** eine Anzeigereihenfolge ein (optional).</span><span class="sxs-lookup"><span data-stu-id="1a348-132">In the **Display order** box, enter a number for the display order (optional).</span></span>
1. <span data-ttu-id="1a348-133">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="1a348-133">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="1a348-134">Wiederholen Sie die obigen Schritte, um weitere Knoten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1a348-134">Repeat the steps above to add additional nodes.</span></span>

<span data-ttu-id="1a348-135">Das folgende Bild zeigt die Erstellung eines neuen Produkthierarchieknotens an.</span><span class="sxs-lookup"><span data-stu-id="1a348-135">The following image shows the creation of a new product hierarchy node.</span></span>

![Produkthierarchie erstellen](media/create-product-hierarchy.png)

## <a name="other-settings"></a><span data-ttu-id="1a348-137">Andere Einstellungen</span><span class="sxs-lookup"><span data-stu-id="1a348-137">Other settings</span></span>

<span data-ttu-id="1a348-138">Bei Bedarf können jeder Gruppe auch Kategorieattributgruppen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="1a348-138">Category attribute groups can also be assigned to each group as required.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="1a348-139">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1a348-139">Additional resources</span></span>

[<span data-ttu-id="1a348-140">Hierarchien in Commerce</span><span class="sxs-lookup"><span data-stu-id="1a348-140">commerce hierarchies</span></span>](retail-hierarchies.md)

[<span data-ttu-id="1a348-141">Produktkategorien und Produkte verwalten </span><span class="sxs-lookup"><span data-stu-id="1a348-141">Manage product categories and products </span></span>](category-management-product-creation.md)

[<span data-ttu-id="1a348-142">Sortierreihenfolge für Verkaufsentitäten ändern</span><span class="sxs-lookup"><span data-stu-id="1a348-142">Change the sort order for merchandizing entities</span></span>](custom-order-categories-nav-retail-prod-hierarchy.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]