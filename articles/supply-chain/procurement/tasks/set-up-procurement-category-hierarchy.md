---
title: Einrichten einer Beschaffungskategoriehierarchie
description: Dieses Verfahren zeigt Ihnen an, wie neue Knoten in einer Beschaffungskategorie-Hierarchie erstellt und das Einrichten einer in konfiguriert einem Beschaffungsprozess zu verwendende Beschaffungskategorie.
author: mkirknel
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7010fb702d16dc276bfee397066ccf95bf5d25a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147272"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="c984b-103">Einrichten einer Beschaffungskategoriehierarchie</span><span class="sxs-lookup"><span data-stu-id="c984b-103">Set up a procurement category hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c984b-104">Dieses Verfahren zeigt Ihnen an, wie neue Knoten in einer Beschaffungskategorie-Hierarchie erstellt und das Einrichten einer in konfiguriert einem Beschaffungsprozess zu verwendende Beschaffungskategorie.</span><span class="sxs-lookup"><span data-stu-id="c984b-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="c984b-105">Diese Aufgaben werden normalerweise von einem Einkaufsleiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c984b-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="c984b-106">Überprüfen Sie zunächst können, muss es eine Kategoriehierarchie vom Typ Beschaffung geben.</span><span class="sxs-lookup"><span data-stu-id="c984b-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="c984b-107">Wenn Sie ein Demodatunternehmen verwenden, können Sie diese Prozedur im USMF-Unternehmen ausführen.</span><span class="sxs-lookup"><span data-stu-id="c984b-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="c984b-108">Neue Beschaffungskategorie hinzufügen</span><span class="sxs-lookup"><span data-stu-id="c984b-108">Add a new procurement category</span></span>
1. <span data-ttu-id="c984b-109">Wechseln Sie zu **Navigationsbereich > Module > Beschaffung > Sendung > Beschaffungskategorien**.</span><span class="sxs-lookup"><span data-stu-id="c984b-109">Go to **Navigation pane > Modules > Procurement and sourcing > Consignment > Procurement categories**.</span></span>
2. <span data-ttu-id="c984b-110">Klicken Sie im Aktivitätsbereich auf **Kategoriehierarchie bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="c984b-110">On the action pane, select **Edit category hierarchy**.</span></span> <span data-ttu-id="c984b-111">Die aktuelle Beschaffungskategorie-Hierarchie wird in der linken Seite der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c984b-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="c984b-112">Sie sind dabei, die Hierarchie zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c984b-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="c984b-113">Klicken Sie im Aktivitätsbereich auf **Neuer Kategorieknoten**.</span><span class="sxs-lookup"><span data-stu-id="c984b-113">On the action pane, select **New category node**.</span></span> <span data-ttu-id="c984b-114">Das System wählt den obersten Knoten standardmäßig aus.</span><span class="sxs-lookup"><span data-stu-id="c984b-114">The system selects the top node by default.</span></span> <span data-ttu-id="c984b-115">Wenn Sie dieses Verfahren ausführen, während ein Aufgabenhandbuch, Sie auf die Schaltfläche Entsperren klicken und einen anderen übergeordneten Knoten auswählen kann, um den neuen Knoten in einzufügen.</span><span class="sxs-lookup"><span data-stu-id="c984b-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="c984b-116">Sobald das getan haben, sperren Sie das Aufgabenhandbuch erneut und klicken Sie anschließend auf Neues Kategorie Knoten.</span><span class="sxs-lookup"><span data-stu-id="c984b-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="c984b-117">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c984b-117">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="c984b-118">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c984b-118">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="c984b-119">Geben Sie im Feld **Anzeigename** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c984b-119">In the **Friendly name** field, type a value.</span></span> <span data-ttu-id="c984b-120">Der Anzeigename ist optional.</span><span class="sxs-lookup"><span data-stu-id="c984b-120">The friendly name is optional.</span></span> <span data-ttu-id="c984b-121">Er wird in den Kategoriesuchen zusammen mit dem Kategorienamen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c984b-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="c984b-122">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="c984b-122">Select **Save**.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="c984b-123">Hinzufügen von Produkten zu Ihrer neuen Beschaffungskategorie</span><span class="sxs-lookup"><span data-stu-id="c984b-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="c984b-124">Klicken Sie auf **Beschaffung > Sendung > Beschaffungskategorien**.</span><span class="sxs-lookup"><span data-stu-id="c984b-124">Go to **Procurement and sourcing > Consignment > Procurement categories**.</span></span> <span data-ttu-id="c984b-125">Wählen Sie den Knoten aus, den Sie soeben gelegt haben.</span><span class="sxs-lookup"><span data-stu-id="c984b-125">Select the node you just added.</span></span> <span data-ttu-id="c984b-126">Wenn Sie die Prozedur wie ein Aufgabenhandbuch ausführen, müssen Sie möglicherweise auf die Schaltfläche „Entsperren“ klicken, bevor Sie den Knoten auswählen können.</span><span class="sxs-lookup"><span data-stu-id="c984b-126">If you're running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="c984b-127">Schalten Sie die Erweiterung des **Produkt**-Abschnitts ein/aus.</span><span class="sxs-lookup"><span data-stu-id="c984b-127">Toggle the expansion of the **Products** section.</span></span>
3. <span data-ttu-id="c984b-128">Wählen Sie **Hinzufügen**, um Produkte mit der Beschaffungskategorie zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="c984b-128">Select **Add** to associate products with the procurement category.</span></span>
4. <span data-ttu-id="c984b-129">Wählen Sie Produkte aus, die Sie der Beschaffungskategorie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="c984b-129">Select the products you want to add to the procurement category.</span></span>
5. <span data-ttu-id="c984b-130">Klicken Sie auf den Pfeil, um die Produkte zur Tabelle **Ausgewählt** hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c984b-130">Select the arrow to add the products to the **Selected** table.</span></span>
6. <span data-ttu-id="c984b-131">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="c984b-131">Select **OK**.</span></span>
