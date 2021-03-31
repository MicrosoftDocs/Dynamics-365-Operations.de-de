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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59631148dbd2ad27ce2bb5c268d78e625daef6bb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224450"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="8f613-103">Eine Hierarchie zur Produktklassifizierung erstellen</span><span class="sxs-lookup"><span data-stu-id="8f613-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8f613-104">Im folgenden Verfahren, wie eine neue Kategoriehierarchie erstellt und einen Warencodehierarchietyp zuweist.</span><span class="sxs-lookup"><span data-stu-id="8f613-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="8f613-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="8f613-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8f613-106">Diese Prozedur ist für die Kategorie-Lagerverwaltung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="8f613-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="8f613-107">Neue Kategoriehierarchie erstellen</span><span class="sxs-lookup"><span data-stu-id="8f613-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="8f613-108">Wechseln Sie zu **Navigationsbereich > Module > Produktinformationsverwaltung > Einstellungen > Kategorien und Attribute > Kategoriehierarchien**.</span><span class="sxs-lookup"><span data-stu-id="8f613-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="8f613-109">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="8f613-109">Click **New**.</span></span>
3. <span data-ttu-id="8f613-110">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8f613-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="8f613-111">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8f613-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="8f613-112">Klicken Sie auf **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="8f613-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="8f613-113">Erstellen Sie die Hierarchie an</span><span class="sxs-lookup"><span data-stu-id="8f613-113">Build the hierarchy</span></span>
1. <span data-ttu-id="8f613-114">Klicken Sie auf **Neuer Kategorieknoten**.</span><span class="sxs-lookup"><span data-stu-id="8f613-114">Click **New** category node.</span></span>
2. <span data-ttu-id="8f613-115">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8f613-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="8f613-116">Geben Sie im Feld **Code** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8f613-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="8f613-117">Geben Sie im Feld **Anzeigename** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8f613-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="8f613-118">Klicken Sie auf **Neuer Kategorieknoten**.</span><span class="sxs-lookup"><span data-stu-id="8f613-118">Click **New** category node.</span></span>
6. <span data-ttu-id="8f613-119">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8f613-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="8f613-120">Geben Sie im Feld **Code** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8f613-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="8f613-121">Geben Sie im Feld **Anzeigename** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8f613-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="8f613-122">Klicken Sie auf **Neuer Kategorieknoten**.</span><span class="sxs-lookup"><span data-stu-id="8f613-122">Click **New** category node.</span></span>
10. <span data-ttu-id="8f613-123">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8f613-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="8f613-124">Geben Sie im Feld **Code** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8f613-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="8f613-125">Geben Sie im Feld **Anzeigename** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8f613-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="8f613-126">Klicken Sie auf **Neuer Kategorieknoten**.</span><span class="sxs-lookup"><span data-stu-id="8f613-126">Click **New** category node.</span></span>
14. <span data-ttu-id="8f613-127">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8f613-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="8f613-128">Geben Sie im Feld **Code** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8f613-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="8f613-129">Geben Sie im Feld **Anzeigename** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8f613-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="8f613-130">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8f613-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="8f613-131">Klassifizieren Sie die Hierarchie</span><span class="sxs-lookup"><span data-stu-id="8f613-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="8f613-132">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8f613-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="8f613-133">Klicken Sie im **Aktivitätsbereich** auf **Kategoriehierarchie**.</span><span class="sxs-lookup"><span data-stu-id="8f613-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="8f613-134">Klicken Sie auf **Hierarchietyp zuordnen**.</span><span class="sxs-lookup"><span data-stu-id="8f613-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="8f613-135">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="8f613-135">Click **New**.</span></span>
5. <span data-ttu-id="8f613-136">Wählen Sie im Feld **Kategoriehierarchietyp** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="8f613-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="8f613-137">Wählen Sie den **Warencodekategoriehierarchietyp für Produktklassifizierung** aus.</span><span class="sxs-lookup"><span data-stu-id="8f613-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="8f613-138">Klicken Sie im Feld **Kategoriehierarchie** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8f613-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8f613-139">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8f613-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="8f613-140">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8f613-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="8f613-141">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8f613-141">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]