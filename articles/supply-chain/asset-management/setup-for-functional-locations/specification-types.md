---
title: Wartungsattributtypen
description: In diesem Thema wird erläutert, wie Sie in Attributtypen in Asset Management erstellen.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c07f303b72f286c33979181fca1592b47efa1303
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571230"
---
# <a name="maintenance-attribute-types"></a><span data-ttu-id="b457c-103">Wartungsattributtypen</span><span class="sxs-lookup"><span data-stu-id="b457c-103">Maintenance attribute types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b457c-104">In diesem Thema wird erläutert, wie Sie in Attributtypen in Asset Management erstellen.</span><span class="sxs-lookup"><span data-stu-id="b457c-104">This topic explains how to create attribute types in Asset Management.</span></span> <span data-ttu-id="b457c-105">Attribute werden verwendet, um die Eigenschaften verschiedener Elemente zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b457c-105">Attributes are used to describe the properties of various elements.</span></span> <span data-ttu-id="b457c-106">Sie können Attribute für die folgenden Elemente einrichten:</span><span class="sxs-lookup"><span data-stu-id="b457c-106">You can set up attributes on the following elements:</span></span>

- [<span data-ttu-id="b457c-107">Funktionale Standorttypen</span><span class="sxs-lookup"><span data-stu-id="b457c-107">Functional location types</span></span>](../setup-for-functional-locations/functional-location-types.md)
- [<span data-ttu-id="b457c-108">Funktionale Standorte</span><span class="sxs-lookup"><span data-stu-id="b457c-108">Functional locations</span></span>](../functional-locations/create-functional-locations.md)
- [<span data-ttu-id="b457c-109">Anlagentypen</span><span class="sxs-lookup"><span data-stu-id="b457c-109">Asset types</span></span>](../setup-for-objects/object-types.md)
- <span data-ttu-id="b457c-110">Anlagen</span><span class="sxs-lookup"><span data-stu-id="b457c-110">Assets</span></span>

<span data-ttu-id="b457c-111">Die Attribute, die Sie einrichten können, variieren, je nach spezifischem Element.</span><span class="sxs-lookup"><span data-stu-id="b457c-111">The attributes that you can set up vary, depending on the element.</span></span> <span data-ttu-id="b457c-112">Für einen funktionalen Standort können Sie beispielsweise Attribute für die Konfiguration und physische Größe des Standorts einrichten.</span><span class="sxs-lookup"><span data-stu-id="b457c-112">For example, for a functional location, you can set up attributes for the configuration and physical size of the location.</span></span> <span data-ttu-id="b457c-113">Für einen Anlagentyp oder eine Anlage können Sie Attribute für Modulvolumen, Stromverbrauch und die maximale Ladungskapazität unter verschiedene Bedingungen einrichten.</span><span class="sxs-lookup"><span data-stu-id="b457c-113">For an asset type or an asset, you can set up attributes for engine volume, power consumption, and maximum load capacity under different conditions.</span></span>

## <a name="create-attribute-types"></a><span data-ttu-id="b457c-114">Erstellen von Attributtypen</span><span class="sxs-lookup"><span data-stu-id="b457c-114">Create attribute types</span></span>

<span data-ttu-id="b457c-115">Sie können eigene Attributtypen erstellen.</span><span class="sxs-lookup"><span data-stu-id="b457c-115">You can create your own attribute types.</span></span> <span data-ttu-id="b457c-116">Darüber hinaus können Sie Produktdimensionen auf die Seite **Attributtypen** übertragen.</span><span class="sxs-lookup"><span data-stu-id="b457c-116">Additionally, you can transfer product dimensions to the **Attribute types** page.</span></span>

1. <span data-ttu-id="b457c-117">Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Attributtypen** aus.</span><span class="sxs-lookup"><span data-stu-id="b457c-117">Select **Asset management** \> **Setup** \> **Attribute types**.</span></span>
2. <span data-ttu-id="b457c-118">Beim der erstmaligen Einrichtung von Attributtypen wählen Sie **Produktdimensionen erstellen** aus, um Standardproduktdimensionen automatisch zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="b457c-118">The first time that you set up attribute types, select **Create product dimensions** to automatically transfer standard product dimensions.</span></span>
3. <span data-ttu-id="b457c-119">Wählen Sie **Neu** aus, um einen neuen Attributtyp zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b457c-119">Select **New** to create a new attribute type.</span></span>
4. <span data-ttu-id="b457c-120">Geben Sie im Feld **Attributtyp** einen Namen für den Attributtyp ein.</span><span class="sxs-lookup"><span data-stu-id="b457c-120">In the **Attribute type** field, enter a name for the attribute type.</span></span>
5. <span data-ttu-id="b457c-121">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="b457c-121">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="b457c-122">Wählen Sie im Feld **Einheit** die benötigte Attributeinheit aus.</span><span class="sxs-lookup"><span data-stu-id="b457c-122">In the **Unit** field, select the relevant attribute unit, as required.</span></span>
7. <span data-ttu-id="b457c-123">Wählen Sie im Feld **Datentyp** einen Datentyp für die Einheit aus.</span><span class="sxs-lookup"><span data-stu-id="b457c-123">In the **Data type** field, select a data type for the unit.</span></span>
8. <span data-ttu-id="b457c-124">Wenn Sie **Zeichenfolge** als Datentyp ausgewählt haben, gehen Sie folgendermaßen vor, um Werte für den Attributtyp zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="b457c-124">If you selected **String** as the data type, follow these steps to create values for the attribute type:</span></span>

    1. <span data-ttu-id="b457c-125">Wählen Sie den Attributtyp und dann **Werte** aus.</span><span class="sxs-lookup"><span data-stu-id="b457c-125">Select the attribute type, and then select **Values**.</span></span>
    2. <span data-ttu-id="b457c-126">Wählen Sie im Feld **Attributwerte** die Option **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="b457c-126">In the **Attribute values** field, select **New**.</span></span>
    3. <span data-ttu-id="b457c-127">Wählen Sie im Feld **Attributtyp** einen Attributtyp (Dimension) aus.</span><span class="sxs-lookup"><span data-stu-id="b457c-127">In the **Attribute type** field, select an attribute type (dimension).</span></span>
    4. <span data-ttu-id="b457c-128">Geben Sie im Feld **Wert** einen zugehörigen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b457c-128">In the **Value** field, enter a related value.</span></span>
    5. <span data-ttu-id="b457c-129">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="b457c-129">In the **Description** field, enter a description.</span></span>
    6. <span data-ttu-id="b457c-130">Speichern Sie den Datensatz.</span><span class="sxs-lookup"><span data-stu-id="b457c-130">Save the record.</span></span>
    7. <span data-ttu-id="b457c-131">Kehren Sie zur Seite **Attributtypen** zurück.</span><span class="sxs-lookup"><span data-stu-id="b457c-131">Return to the **Attribute types** page.</span></span>

9. <span data-ttu-id="b457c-132">Speichern Sie den Datensatz.</span><span class="sxs-lookup"><span data-stu-id="b457c-132">Save the record.</span></span>

    <span data-ttu-id="b457c-133">Das Feld **Funktionale Standorttypen** zeigt die Anzahl der funktionalen Standorte an, die den Attributtyp verwenden.</span><span class="sxs-lookup"><span data-stu-id="b457c-133">The **Functional location types** field shows the number of functional locations that are using the attribute type.</span></span> <span data-ttu-id="b457c-134">Das Feld **Anlagentypen** zeigt die Anzahl von Anlagentypen an, die ihn verwenden.</span><span class="sxs-lookup"><span data-stu-id="b457c-134">The **Asset types** field shows the number of asset types that are using it.</span></span>
