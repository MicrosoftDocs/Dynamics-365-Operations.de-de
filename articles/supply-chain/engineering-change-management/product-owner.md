---
title: Produkteigentümer
description: Dieses Thema enthält Informationen über Produktbesitzer. Ein Produktbesitzer ist eine Gruppe von Benutzern, die für bestimmte Produkte verantwortlich sind. Nur Mitglieder der Gruppe können diese Produkte freigeben. Der Besitzer eines Produkts kann auch im Genehmigungs-Workflow verwendet werden.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 679712b2397f220e263da3df07ecd03c99bebf3f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842031"
---
# <a name="product-owners"></a><span data-ttu-id="c14e5-106">Produkteigentümer</span><span class="sxs-lookup"><span data-stu-id="c14e5-106">Product owners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c14e5-107">Der Produktbesitzer ist eine Gruppe von Benutzern, die für bestimmte Produkte verantwortlich sind.</span><span class="sxs-lookup"><span data-stu-id="c14e5-107">The product owner is a group of users who are responsible for specific products.</span></span> <span data-ttu-id="c14e5-108">Wenn eine Gruppe von Produktbesitzern einem Produkt zugewiesen ist, können nur die Mitglieder dieser Gruppe das Produkt freigeben.</span><span class="sxs-lookup"><span data-stu-id="c14e5-108">When a product owner group is assigned to a product, only the members of that group can release the product.</span></span> <span data-ttu-id="c14e5-109">Der Produktbesitzer kann auch im Genehmigungs-Workflow in der Verwaltung für technische Änderungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c14e5-109">The product owner can also be used in the approval workflow in engineering change management.</span></span>

<span data-ttu-id="c14e5-110">Produktbesitzer sind globale Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="c14e5-110">Product owners are global settings.</span></span> <span data-ttu-id="c14e5-111">Sie sind daher für alle juristischen Entitäten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c14e5-111">Therefore, they are available to all legal entities.</span></span>

## <a name="create-a-product-owner-group"></a><span data-ttu-id="c14e5-112">Erstellen einer Gruppe von Produktbesitzern</span><span class="sxs-lookup"><span data-stu-id="c14e5-112">Create a product owner group</span></span>

<span data-ttu-id="c14e5-113">Gehen Sie folgendermaßen vor, um eine Gruppe von Produktbesitzern zu erstellen und ihr Mitglieder hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c14e5-113">To create a product owner group and add members to it, follow these steps.</span></span>

1. <span data-ttu-id="c14e5-114">Gehen Sie zu **Verwaltung für technische Änderungen \> Einrichten \> Produktbesitzer**.</span><span class="sxs-lookup"><span data-stu-id="c14e5-114">Go to **Engineering change management \> Setup \> Product owners**.</span></span>
2. <span data-ttu-id="c14e5-115">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="c14e5-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="c14e5-116">Geben Sie in das Feld **Produktbesitzer** einen Namen für die Gruppe ein.</span><span class="sxs-lookup"><span data-stu-id="c14e5-116">In the **Product owner** field, enter a name for the group.</span></span>
4. <span data-ttu-id="c14e5-117">Geben Sie in das Feld **Name** eine Beschreibung für die Gruppe ein.</span><span class="sxs-lookup"><span data-stu-id="c14e5-117">In the **Name** field, enter a description of the group.</span></span>
5. <span data-ttu-id="c14e5-118">Fügen Sie auf dem Inforegister **Mitglieder** die Arbeitskräfte hinzu, die Mitglieder der Gruppe sein sollen.</span><span class="sxs-lookup"><span data-stu-id="c14e5-118">On the **Members** FastTab, add the workers who should be members of the group.</span></span>

## <a name="assign-a-product-owner-to-a-product"></a><span data-ttu-id="c14e5-119">Zuweisen eines Besitzers zu einem Produkt</span><span class="sxs-lookup"><span data-stu-id="c14e5-119">Assign a product owner to a product</span></span>

<span data-ttu-id="c14e5-120">Um einem Produkt einen Besitzer zuzuweisen, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="c14e5-120">To assign a product owner to a product, follow these steps.</span></span>

1. <span data-ttu-id="c14e5-121">Öffnen Sie die Seite **Produktdetails** für das betreffende Produkt oder den Produktstamm.</span><span class="sxs-lookup"><span data-stu-id="c14e5-121">Open the **Product details** page for the relevant product or product master.</span></span>
1. <span data-ttu-id="c14e5-122">Legen Sie auf dem Inforegister **Allgemein** das Feld **Produktbesitzer** auf den Namen der entsprechenden Gruppe von Produktbesitzern fest.</span><span class="sxs-lookup"><span data-stu-id="c14e5-122">On the **General** FastTab, set the **Product owner** field to the name of the relevant product owner group.</span></span>

<span data-ttu-id="c14e5-123">Während ein Produktbesitzer einem Produkt zugewiesen ist, können nur die Mitglieder der Produktbesitzer-Gruppe die Einstellung **Produktbesitzer** bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="c14e5-123">While a product owner is assigned to a product, only the members of the product owner group can edit the **Product owner** setting.</span></span>

<span data-ttu-id="c14e5-124">Der Besitzer des Produkts ist auch auf der Seite **Freigegebene Produkte** sichtbar.</span><span class="sxs-lookup"><span data-stu-id="c14e5-124">The product owner is also visible on the **Released products** page.</span></span>

## <a name="product-owners-and-product-releases"></a><span data-ttu-id="c14e5-125">Produktbesitzer und Produktfreigaben</span><span class="sxs-lookup"><span data-stu-id="c14e5-125">Product owners and product releases</span></span>

<span data-ttu-id="c14e5-126">Nur Benutzer aus der Gruppe der Besitzer eines Produkts können dieses Produkt freigeben.</span><span class="sxs-lookup"><span data-stu-id="c14e5-126">Only users from a product's product owner group can release that product.</span></span> <span data-ttu-id="c14e5-127">Es gibt jedoch eine Ausnahme, wenn das Produkt ein untergeordnetes Element ist und sein übergeordnetes Element vom Besitzer des übergeordneten Elements freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c14e5-127">However, there is an exception when the product is a child item, and its parent is released by the parent's owner.</span></span> <span data-ttu-id="c14e5-128">Mit anderen Worten: Wenn das Produkt Teil der Stückliste eines anderen Produkts ist, prüft das System nicht den Besitzer jedes Elements in der Stückliste.</span><span class="sxs-lookup"><span data-stu-id="c14e5-128">In other words, if the product is part of the BOM of another product, the system doesn't check the product owner of each item in the BOM.</span></span> <span data-ttu-id="c14e5-129">Es prüft nur den Besitzer des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="c14e5-129">It checks only the product owner of the parent item.</span></span>

<span data-ttu-id="c14e5-130">Beispiel: Produkt X ist der Eigentümergruppe *Designschränke* zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c14e5-130">For example, product X is assigned to the *Design cabinets* product owner group.</span></span> <span data-ttu-id="c14e5-131">Produkt X ist auch Teil der Stückliste von Produkt Y, das der Produktbesitzer-Gruppe *Design Speakers* zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c14e5-131">Product X is also part of the BOM of product Y, which is assigned to the *Design Speakers* product owner group.</span></span> <span data-ttu-id="c14e5-132">Wenn ein Benutzer aus der Produktbesitzer-Gruppe *Design Speakers* das Produkt Y und dessen Stückliste freigibt, wird das Produkt X zusammen mit dem Produkt Y freigegeben.</span><span class="sxs-lookup"><span data-stu-id="c14e5-132">If a user from the *Design Speakers* product owner group releases product Y and its BOM, product X will be released together with product Y.</span></span>

## <a name="product-owners-and-approvals"></a><span data-ttu-id="c14e5-133">Produktbesitzer und Freigaben</span><span class="sxs-lookup"><span data-stu-id="c14e5-133">Product owners and approvals</span></span>

<span data-ttu-id="c14e5-134">Da die Besitzer der Produkte wissen, ob bestimmte technische Änderungen für ihre Produkte von Vorteil sind, ist es oft sinnvoll, sie als Teil des Genehmigungsprozesses in die Verwaltung für technische Änderungen einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="c14e5-134">Because product owners know whether specific engineering changes will benefit their products, it often makes sense to include them as part of the approval process in engineering change management.</span></span> <span data-ttu-id="c14e5-135">Sie können diesen Ansatz implementieren, indem Sie die Besitzer der Produkte als Teilnehmer in den Workflows festlegen, die für die Verwaltung für technische Änderungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c14e5-135">You can implement this approach by setting up the product owners as participant providers in the workflows that are used for engineering change management.</span></span> <span data-ttu-id="c14e5-136">Das System weist dann Genehmigungsaufgaben in den Workflows zu, basierend auf den Produkten, die in Änderungsanträgen und Änderungsaufträgen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c14e5-136">The system will then assign approval tasks in the workflows, based on the products that are in engineering change requests and engineering change orders.</span></span> <span data-ttu-id="c14e5-137">Weitere Informationen finden Sie unter [Verwalten von Änderungen an Engineering-Produkten](engineering-change-management.md).</span><span class="sxs-lookup"><span data-stu-id="c14e5-137">For more information, see [Manage changes to engineering products](engineering-change-management.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]