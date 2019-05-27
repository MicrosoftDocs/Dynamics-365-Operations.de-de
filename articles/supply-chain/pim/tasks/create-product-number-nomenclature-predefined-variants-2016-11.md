---
title: Produktnummernbezeichnung für vordefinierte Produktvarianten erstellen
description: Diese Verfahren zeigt, wie eine Produktnummerenbezeichnung für vordefinierte Produktvarianten eingerichtet wird und sie der passenden Produktdimensionsgruppe zugeordnet werden kann.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b49e96677b94d5f669ea41861f64e62e118938c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550582"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="aabc8-103">Produktnummernbezeichnung für vordefinierte Produktvarianten erstellen</span><span class="sxs-lookup"><span data-stu-id="aabc8-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aabc8-104">Diese Verfahren zeigt, wie eine Produktnummerenbezeichnung für vordefinierte Produktvarianten eingerichtet wird und sie der passenden Produktdimensionsgruppe zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="aabc8-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="aabc8-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="aabc8-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="aabc8-106">Die neue Produktnummernnomenklatur wird der Produktdimensionsgruppe Farbe und Größe zuweisen.</span><span class="sxs-lookup"><span data-stu-id="aabc8-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="aabc8-107">Diese Aufgabe erfolgt in der Regel durch einen Produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="aabc8-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="aabc8-108">Erstellen eine Produktnummerbezeichnung</span><span class="sxs-lookup"><span data-stu-id="aabc8-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="aabc8-109">Klicken Sie auf "Produktvariantenmodell-Definition".</span><span class="sxs-lookup"><span data-stu-id="aabc8-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="aabc8-110">Klicken Sie auf "Produktbezeichnung".</span><span class="sxs-lookup"><span data-stu-id="aabc8-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="aabc8-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="aabc8-111">Click New.</span></span>
4. <span data-ttu-id="aabc8-112">Geben Sie im Feld Name einen Nomenklaturnamen ein, der die Zielproduktdimensionsgruppe identifiziert (beispielsweise ColorSize).</span><span class="sxs-lookup"><span data-stu-id="aabc8-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize..</span></span>
5. <span data-ttu-id="aabc8-113">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="aabc8-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="aabc8-114">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="aabc8-114">Click Add.</span></span>
7. <span data-ttu-id="aabc8-115">Klicken Sie auf "Produktmasternummer".</span><span class="sxs-lookup"><span data-stu-id="aabc8-115">Click Product master number.</span></span>
8. <span data-ttu-id="aabc8-116">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="aabc8-116">Click Add.</span></span>
9. <span data-ttu-id="aabc8-117">Klicken Sie auf Textkonstante.</span><span class="sxs-lookup"><span data-stu-id="aabc8-117">Click Text constant.</span></span>
10. <span data-ttu-id="aabc8-118">Geben Sie im Feld "Text" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="aabc8-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="aabc8-119">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="aabc8-119">Click Add.</span></span>
12. <span data-ttu-id="aabc8-120">Klicken Sie auf "Farbe".</span><span class="sxs-lookup"><span data-stu-id="aabc8-120">Click Color.</span></span>
13. <span data-ttu-id="aabc8-121">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="aabc8-121">Click Add.</span></span>
14. <span data-ttu-id="aabc8-122">Klicken Sie auf Textkonstante.</span><span class="sxs-lookup"><span data-stu-id="aabc8-122">Click Text constant.</span></span>
15. <span data-ttu-id="aabc8-123">Geben Sie im Feld "Text" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="aabc8-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="aabc8-124">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="aabc8-124">Click Add.</span></span>
17. <span data-ttu-id="aabc8-125">Klicken Sie auf Größe.</span><span class="sxs-lookup"><span data-stu-id="aabc8-125">Click Size.</span></span>
18. <span data-ttu-id="aabc8-126">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="aabc8-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="aabc8-127">Zuweisen der Nomenklatur zu einem Produktmaster</span><span class="sxs-lookup"><span data-stu-id="aabc8-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="aabc8-128">Klicken Sie auf "Produktdimensionsgruppen".</span><span class="sxs-lookup"><span data-stu-id="aabc8-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="aabc8-129">Wählen Sie die Dimensionsgruppe "SizeCol".</span><span class="sxs-lookup"><span data-stu-id="aabc8-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="aabc8-130">Klicken Sie auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="aabc8-130">Click Edit.</span></span>
4. <span data-ttu-id="aabc8-131">Wählen Sie "Ja" im Feld "Bezeichnungen verwenden".</span><span class="sxs-lookup"><span data-stu-id="aabc8-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="aabc8-132">Geben Sie im Feld "Produktvariantennummerbezeichnung" eine Bezeichnung ein oder wählen Sie eine aus.</span><span class="sxs-lookup"><span data-stu-id="aabc8-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="aabc8-133">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="aabc8-133">Close the page.</span></span>

