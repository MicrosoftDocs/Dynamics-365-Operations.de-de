---
title: Produktnummernbezeichnung für vordefinierte Produktvarianten erstellen
description: Dieses Thema erklärt, wie eine Produktnummernbezeichnung für vordefinierte Produktvarianten eingerichtet wird und der passenden Produktdimensionsgruppe zugeordnet werden kann.
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 073b680c48855b2a8902c19cedfbf98cdbfdf17d
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150048"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="62389-103">Produktnummernbezeichnung für vordefinierte Produktvarianten erstellen</span><span class="sxs-lookup"><span data-stu-id="62389-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="62389-104">Dieses Thema erklärt, wie eine Produktnummernbezeichnung für vordefinierte Produktvarianten eingerichtet wird und der passenden Produktdimensionsgruppe zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="62389-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="62389-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="62389-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="62389-106">Die neue Produktnummernnomenklatur wird der Produktdimensionsgruppe Farbe und Größe zuweisen.</span><span class="sxs-lookup"><span data-stu-id="62389-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="62389-107">Diese Aufgabe erfolgt in der Regel durch einen Produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="62389-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="62389-108">Erstellen eine Produktnummerbezeichnung</span><span class="sxs-lookup"><span data-stu-id="62389-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="62389-109">Wählen Sie **Produktvariantenmodell-Definition** aus.</span><span class="sxs-lookup"><span data-stu-id="62389-109">Select **Product variant model definition**.</span></span>
2. <span data-ttu-id="62389-110">Wählen Sie **Produktbezeichnung** aus.</span><span class="sxs-lookup"><span data-stu-id="62389-110">Select **Product nomenclature**.</span></span>
3. <span data-ttu-id="62389-111">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="62389-111">Select **New**.</span></span>
4. <span data-ttu-id="62389-112">Geben Sie im Feld **Name** einen Bezeichnungsnamen ein, der die Zielproduktdimensionsgruppe identifiziert (beispielsweise `ColorSize`).</span><span class="sxs-lookup"><span data-stu-id="62389-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="62389-113">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="62389-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="62389-114">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="62389-114">Select **Add**.</span></span>
7. <span data-ttu-id="62389-115">Wählen Sie **Produktmaster**-Nummer aus.</span><span class="sxs-lookup"><span data-stu-id="62389-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="62389-116">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="62389-116">Select **Add**.</span></span>
9. <span data-ttu-id="62389-117">Wählen Sie **Textkonstante** aus.</span><span class="sxs-lookup"><span data-stu-id="62389-117">Select **Text constant**.</span></span>
10. <span data-ttu-id="62389-118">Geben Sie im Feld **Text** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="62389-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="62389-119">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="62389-119">Select **Add**.</span></span>
12. <span data-ttu-id="62389-120">Wählen Sie **Farbe** aus.</span><span class="sxs-lookup"><span data-stu-id="62389-120">Select **Color**.</span></span>
13. <span data-ttu-id="62389-121">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="62389-121">Select **Add**.</span></span>
14. <span data-ttu-id="62389-122">Wählen Sie **Textkonstante** aus.</span><span class="sxs-lookup"><span data-stu-id="62389-122">Select **Text constant**.</span></span>
15. <span data-ttu-id="62389-123">Geben Sie im Feld **Text** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="62389-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="62389-124">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="62389-124">Select **Add**.</span></span>
17. <span data-ttu-id="62389-125">Wählen Sie **Größe** aus.</span><span class="sxs-lookup"><span data-stu-id="62389-125">Select **Size**.</span></span>
18. <span data-ttu-id="62389-126">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="62389-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="62389-127">Zuweisen der Nomenklatur zu einem Produktmaster</span><span class="sxs-lookup"><span data-stu-id="62389-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="62389-128">Wählen Sie **Produktdimensionsgruppen** aus.</span><span class="sxs-lookup"><span data-stu-id="62389-128">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="62389-129">Wählen Sie die Gruppe **SizeCol-Produktdimension** aus.</span><span class="sxs-lookup"><span data-stu-id="62389-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="62389-130">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="62389-130">Select **Edit**.</span></span>
4. <span data-ttu-id="62389-131">Wählen Sie **Ja** im Feld **Bezeichnungen verwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="62389-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="62389-132">Geben Sie im Feld **Produktvariantennummerbezeichnung** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="62389-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="62389-133">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="62389-133">Close the page.</span></span>

