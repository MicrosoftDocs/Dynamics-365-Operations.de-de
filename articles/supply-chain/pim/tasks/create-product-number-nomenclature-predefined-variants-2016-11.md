---
title: Produktnummernbezeichnung für vordefinierte Produktvarianten erstellen
description: Dieses Thema erklärt, wie eine Produktnummernbezeichnung für vordefinierte Produktvarianten eingerichtet wird und der passenden Produktdimensionsgruppe zugeordnet werden kann.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bb73854f52525c0722683086d1b4f1dd7173306
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920656"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="54c7d-103">Produktnummernbezeichnung für vordefinierte Produktvarianten erstellen</span><span class="sxs-lookup"><span data-stu-id="54c7d-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="54c7d-104">Dieses Thema erklärt, wie eine Produktnummernbezeichnung für vordefinierte Produktvarianten eingerichtet wird und der passenden Produktdimensionsgruppe zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="54c7d-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="54c7d-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="54c7d-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="54c7d-106">Die neue Produktnummernnomenklatur wird der Produktdimensionsgruppe Farbe und Größe zuweisen.</span><span class="sxs-lookup"><span data-stu-id="54c7d-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="54c7d-107">Diese Aufgabe erfolgt in der Regel durch einen Produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="54c7d-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="54c7d-108">Erstellen eine Produktnummerbezeichnung</span><span class="sxs-lookup"><span data-stu-id="54c7d-108">Create a product number nomenclature</span></span>

1. <span data-ttu-id="54c7d-109">Wechseln Sie zu **Produktinformationsmanagement \> Einrichten \> Produktbezeichnung**.</span><span class="sxs-lookup"><span data-stu-id="54c7d-109">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="54c7d-110">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="54c7d-110">Select **New**.</span></span>
1. <span data-ttu-id="54c7d-111">Geben Sie im Feld **Name** einen Bezeichnungsnamen ein, der die Zielproduktdimensionsgruppe identifiziert (beispielsweise `ColorSize`).</span><span class="sxs-lookup"><span data-stu-id="54c7d-111">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
1. <span data-ttu-id="54c7d-112">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="54c7d-112">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="54c7d-113">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="54c7d-113">Select **Add**.</span></span>
1. <span data-ttu-id="54c7d-114">Wählen Sie **Produktmaster**-Nummer aus.</span><span class="sxs-lookup"><span data-stu-id="54c7d-114">Select **Product master** number.</span></span>
1. <span data-ttu-id="54c7d-115">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="54c7d-115">Select **Add**.</span></span>
1. <span data-ttu-id="54c7d-116">Wählen Sie **Textkonstante** aus.</span><span class="sxs-lookup"><span data-stu-id="54c7d-116">Select **Text constant**.</span></span>
1. <span data-ttu-id="54c7d-117">Geben Sie im Feld **Text** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="54c7d-117">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="54c7d-118">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="54c7d-118">Select **Add**.</span></span>
1. <span data-ttu-id="54c7d-119">Wählen Sie **Farbe** aus.</span><span class="sxs-lookup"><span data-stu-id="54c7d-119">Select **Color**.</span></span>
1. <span data-ttu-id="54c7d-120">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="54c7d-120">Select **Add**.</span></span>
1. <span data-ttu-id="54c7d-121">Wählen Sie **Textkonstante** aus.</span><span class="sxs-lookup"><span data-stu-id="54c7d-121">Select **Text constant**.</span></span>
1. <span data-ttu-id="54c7d-122">Geben Sie im Feld **Text** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="54c7d-122">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="54c7d-123">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="54c7d-123">Select **Add**.</span></span>
1. <span data-ttu-id="54c7d-124">Wählen Sie **Größe** aus.</span><span class="sxs-lookup"><span data-stu-id="54c7d-124">Select **Size**.</span></span>
1. <span data-ttu-id="54c7d-125">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="54c7d-125">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="54c7d-126">Zuweisen der Nomenklatur zu einem Produktmaster</span><span class="sxs-lookup"><span data-stu-id="54c7d-126">Assign the nomenclature to a product master</span></span>

1. <span data-ttu-id="54c7d-127">Wählen Sie **Produktdimensionsgruppen** aus.</span><span class="sxs-lookup"><span data-stu-id="54c7d-127">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="54c7d-128">Wählen Sie die Gruppe **SizeCol-Produktdimension** aus.</span><span class="sxs-lookup"><span data-stu-id="54c7d-128">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="54c7d-129">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="54c7d-129">Select **Edit**.</span></span>
4. <span data-ttu-id="54c7d-130">Wählen Sie **Ja** im Feld **Bezeichnungen verwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="54c7d-130">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="54c7d-131">Geben Sie im Feld **Produktvariantennummerbezeichnung** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="54c7d-131">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="54c7d-132">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="54c7d-132">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]