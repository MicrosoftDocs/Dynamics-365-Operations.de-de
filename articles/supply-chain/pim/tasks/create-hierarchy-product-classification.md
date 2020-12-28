---
title: Eine Hierarchie zur Produktklassifizierung erstellen
description: Im folgenden Verfahren, wie eine neue Kategoriehierarchie erstellt und einen Warencodehierarchietyp zuweist.
author: ShylaThompson
manager: tfehr
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole, EcoResProductCategory, EcoResCategorySearchList, EcoResCategoryHierarchyFactbox, EcoResCategoryFriendlyName, EcoResCategoryAddProduct
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 439df63a4f8f0cc1c030554d18f80e9934c88b00
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428705"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="b2296-103">Eine Hierarchie zur Produktklassifizierung erstellen</span><span class="sxs-lookup"><span data-stu-id="b2296-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b2296-104">Im folgenden Verfahren, wie eine neue Kategoriehierarchie erstellt und einen Warencodehierarchietyp zuweist.</span><span class="sxs-lookup"><span data-stu-id="b2296-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="b2296-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="b2296-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b2296-106">Diese Prozedur ist für die Kategorie-Lagerverwaltung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="b2296-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="b2296-107">Neue Kategoriehierarchie erstellen</span><span class="sxs-lookup"><span data-stu-id="b2296-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="b2296-108">Wechseln Sie zu **Navigationsbereich > Module > Produktinformationsverwaltung > Einstellungen > Kategorien und Attribute > Kategoriehierarchien**.</span><span class="sxs-lookup"><span data-stu-id="b2296-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="b2296-109">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="b2296-109">Click **New**.</span></span>
3. <span data-ttu-id="b2296-110">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b2296-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="b2296-111">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b2296-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="b2296-112">Klicken Sie auf **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="b2296-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="b2296-113">Erstellen Sie die Hierarchie an</span><span class="sxs-lookup"><span data-stu-id="b2296-113">Build the hierarchy</span></span>
1. <span data-ttu-id="b2296-114">Klicken Sie auf **Neuer Kategorieknoten**.</span><span class="sxs-lookup"><span data-stu-id="b2296-114">Click **New** category node.</span></span>
2. <span data-ttu-id="b2296-115">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b2296-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="b2296-116">Geben Sie im Feld **Code** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b2296-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="b2296-117">Geben Sie im Feld **Anzeigename** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b2296-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="b2296-118">Klicken Sie auf **Neuer Kategorieknoten**.</span><span class="sxs-lookup"><span data-stu-id="b2296-118">Click **New** category node.</span></span>
6. <span data-ttu-id="b2296-119">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b2296-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="b2296-120">Geben Sie im Feld **Code** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b2296-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="b2296-121">Geben Sie im Feld **Anzeigename** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b2296-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="b2296-122">Klicken Sie auf **Neuer Kategorieknoten**.</span><span class="sxs-lookup"><span data-stu-id="b2296-122">Click **New** category node.</span></span>
10. <span data-ttu-id="b2296-123">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b2296-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="b2296-124">Geben Sie im Feld **Code** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b2296-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="b2296-125">Geben Sie im Feld **Anzeigename** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b2296-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="b2296-126">Klicken Sie auf **Neuer Kategorieknoten**.</span><span class="sxs-lookup"><span data-stu-id="b2296-126">Click **New** category node.</span></span>
14. <span data-ttu-id="b2296-127">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b2296-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="b2296-128">Geben Sie im Feld **Code** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b2296-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="b2296-129">Geben Sie im Feld **Anzeigename** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b2296-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="b2296-130">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="b2296-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="b2296-131">Klassifizieren Sie die Hierarchie</span><span class="sxs-lookup"><span data-stu-id="b2296-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="b2296-132">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="b2296-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="b2296-133">Klicken Sie im **Aktivitätsbereich** auf **Kategoriehierarchie**.</span><span class="sxs-lookup"><span data-stu-id="b2296-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="b2296-134">Klicken Sie auf **Hierarchietyp zuordnen**.</span><span class="sxs-lookup"><span data-stu-id="b2296-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="b2296-135">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="b2296-135">Click **New**.</span></span>
5. <span data-ttu-id="b2296-136">Wählen Sie im Feld **Kategoriehierarchietyp** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="b2296-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="b2296-137">Wählen Sie den **Warencodekategoriehierarchietyp für Produktklassifizierung** aus.</span><span class="sxs-lookup"><span data-stu-id="b2296-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="b2296-138">Klicken Sie im Feld **Kategoriehierarchie** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b2296-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="b2296-139">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="b2296-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="b2296-140">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="b2296-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="b2296-141">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="b2296-141">Close the page.</span></span>

