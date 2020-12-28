---
title: Eine Attribut-basierte Preiskalkulation für konfigurierbare Produkte einrichten
description: In diesem Thema wird erläutert, wie Sie eine attributive Preisgestaltung einrichten.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a75f3afcf4761ac6a9575eae9a620a1e9f01c8e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428552"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="42e5c-103">Eine Attribut-basierte Preiskalkulation für konfigurierbare Produkte einrichten</span><span class="sxs-lookup"><span data-stu-id="42e5c-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="42e5c-104">In diesem Thema wird erläutert, wie Sie eine attributive Preisgestaltung einrichten.</span><span class="sxs-lookup"><span data-stu-id="42e5c-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="42e5c-105">Als Voraussetzung müssen Sie ein Produktkonfigurationsmodell haben, das eine oder mehrere Komponenten und Attribute besitzt.</span><span class="sxs-lookup"><span data-stu-id="42e5c-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="42e5c-106">Dieses Beispiel verwendet das High-End-Lausprecherproduktmodell im Demodatenunternehmen USMF.</span><span class="sxs-lookup"><span data-stu-id="42e5c-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="42e5c-107">Normalerweise wird ein Produktmanager dieses Verfahren durchführen.</span><span class="sxs-lookup"><span data-stu-id="42e5c-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="42e5c-108">Erstellen eines neuen Preismodellkriteriums</span><span class="sxs-lookup"><span data-stu-id="42e5c-108">Create a new price model</span></span>
1. <span data-ttu-id="42e5c-109">Wählen Sie auf der Startseite **Produktvariantenmodelldefinition**.</span><span class="sxs-lookup"><span data-stu-id="42e5c-109">Select **Product variant model definition** on the home page.</span></span>
2. <span data-ttu-id="42e5c-110">Wählen Sie **Produktkonfigurationsmodelle** im Abschnitt **Links**.</span><span class="sxs-lookup"><span data-stu-id="42e5c-110">Select **Product configuration models** in the **links** section.</span></span>
3. <span data-ttu-id="42e5c-111">Wählen Sie in der Liste die Zeile **High-End-Lautsprecher**, aber nicht den Link für den Namen.</span><span class="sxs-lookup"><span data-stu-id="42e5c-111">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
4. <span data-ttu-id="42e5c-112">Wählen Sie im Aktionsbereich **Modell**.</span><span class="sxs-lookup"><span data-stu-id="42e5c-112">On the Action Pane, select **Model**.</span></span>
5. <span data-ttu-id="42e5c-113">Wählen Sie **Preismodelle**.</span><span class="sxs-lookup"><span data-stu-id="42e5c-113">Select **Price models**.</span></span>
6. <span data-ttu-id="42e5c-114">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="42e5c-114">Select **New**.</span></span>
7. <span data-ttu-id="42e5c-115">Geben Sie im Feld **Preismodellname** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="42e5c-115">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="42e5c-116">Verwenden Sie einen Namen, mit dem das Modell einfach zu identifizieren ist.</span><span class="sxs-lookup"><span data-stu-id="42e5c-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="42e5c-117">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="42e5c-117">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="42e5c-118">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="42e5c-118">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="42e5c-119">Hinzufügen von Preiselementen</span><span class="sxs-lookup"><span data-stu-id="42e5c-119">Add price elements</span></span>
1. <span data-ttu-id="42e5c-120">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="42e5c-120">Select **Edit**.</span></span> <span data-ttu-id="42e5c-121">Jede Komponente in einem Produktmodell kann ein Basispreiselement und eine beliebige Anzahl Preisausdrucksregeln haben.</span><span class="sxs-lookup"><span data-stu-id="42e5c-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="42e5c-122">Sie können die Preise in den verschiedenen Währungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="42e5c-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="42e5c-123">Geben Sie im Feld **Basispreisausdruck** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="42e5c-123">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="42e5c-124">Geben Sie beispielsweise "100" ein.</span><span class="sxs-lookup"><span data-stu-id="42e5c-124">For example, type 100.</span></span> <span data-ttu-id="42e5c-125">Ein Basispreisausdruck kann ein numerischer Wert sein, oder er kann aus einer arithmetischen Berechnung mit einem oder mehreren Attribute zusammensetzen.</span><span class="sxs-lookup"><span data-stu-id="42e5c-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="42e5c-126">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="42e5c-126">Select **Add**.</span></span>
4. <span data-ttu-id="42e5c-127">Geben Sie im Feld **Name** `Rosewood` ein.</span><span class="sxs-lookup"><span data-stu-id="42e5c-127">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="42e5c-128">Die Preisausdruckname erleichtert die Erkennung des Preiselements.</span><span class="sxs-lookup"><span data-stu-id="42e5c-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="42e5c-129">In diesem Beispiel wird ein Preiselement für die Rosenholzlautsprechergehäuse-Option erstellt.</span><span class="sxs-lookup"><span data-stu-id="42e5c-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="42e5c-130">Wählen Sie **Bedingung bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="42e5c-130">Select **Edit condition**.</span></span> <span data-ttu-id="42e5c-131">Eine Preisbedingung stellt sicher, dass ein Preisausdruckselement nur dann in den Verkaufspreis einbezogen wird, wenn eine bestimmte Kombination von Attributen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="42e5c-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="42e5c-132">Geben Sie im Feld **ConstraintBody** `CabinetFinish=="Rosewood"` ein.</span><span class="sxs-lookup"><span data-stu-id="42e5c-132">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="42e5c-133">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="42e5c-133">Select **OK**.</span></span>
8. <span data-ttu-id="42e5c-134">Geben Sie in das Feld **Ausdruck** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="42e5c-134">In the **Expression** field, type a value.</span></span> <span data-ttu-id="42e5c-135">Geben Sie z.B. `50` ein.</span><span class="sxs-lookup"><span data-stu-id="42e5c-135">For example, type `50`.</span></span> 
9. <span data-ttu-id="42e5c-136">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="42e5c-136">Close the page.</span></span>

