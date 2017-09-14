--- 
title: "Eine Attribut-basierte Preiskalkulation für konfigurierbare Produkte einrichten"
description: Dieses Verfahren zeigt Ihnen, wie Sie attributbasierte Preis einrichten.
author: YuyuScheller
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: 88402bef6fd5dad38a74795cd31a4046085d6db7
ms.contentlocale: de-de
ms.lasthandoff: 09/14/2017

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="595db-103">Eine Attribut-basierte Preiskalkulation für konfigurierbare Produkte einrichten</span><span class="sxs-lookup"><span data-stu-id="595db-103">Set up attribute-based pricing for configurable products</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="595db-104">Dieses Verfahren zeigt Ihnen, wie Sie attributbasierte Preis einrichten.</span><span class="sxs-lookup"><span data-stu-id="595db-104">This procedure shows how to set up attribute-based pricing.</span></span> <span data-ttu-id="595db-105">Als Voraussetzung müssen Sie ein Produktkonfigurationsmodell haben, das eine oder mehrere Komponenten und Attribute besitzt.</span><span class="sxs-lookup"><span data-stu-id="595db-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="595db-106">Dieses Beispiel verwendet das High-End-Lausprecherproduktmodell im Demodatenunternehmen USMF.</span><span class="sxs-lookup"><span data-stu-id="595db-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="595db-107">Normalerweise wird ein Produktmanager dieses Verfahren durchführen.</span><span class="sxs-lookup"><span data-stu-id="595db-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="595db-108">Erstellen eines neuen Preismodellkriteriums</span><span class="sxs-lookup"><span data-stu-id="595db-108">Create a new price model</span></span>
1. <span data-ttu-id="595db-109">Klicken Sie auf "Produktvariantenmodell-Definition".</span><span class="sxs-lookup"><span data-stu-id="595db-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="595db-110">Klicken Sie auf "Produktkonfigurationsmodelle".</span><span class="sxs-lookup"><span data-stu-id="595db-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="595db-111">Wählen Sie in der Liste die Position "High-End-Lautsprecher" aus, aber klicken Sie nicht auf den Link für den Namen.</span><span class="sxs-lookup"><span data-stu-id="595db-111">In the list, select the High End Speaker line, but don’t click the link for the name.</span></span>
4. <span data-ttu-id="595db-112">Klicken Sie im Aktivitätsbereich auf "Modell".</span><span class="sxs-lookup"><span data-stu-id="595db-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="595db-113">Klicken Sie auf Preismodelle.</span><span class="sxs-lookup"><span data-stu-id="595db-113">Click Price models.</span></span>
6. <span data-ttu-id="595db-114">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="595db-114">Click New.</span></span>
7. <span data-ttu-id="595db-115">Geben Sie im Feld "Preismodellname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="595db-115">In the Price model name field, type a value.</span></span>
    * <span data-ttu-id="595db-116">Verwenden Sie einen Namen, mit dem das Modell einfach zu identifizieren ist.</span><span class="sxs-lookup"><span data-stu-id="595db-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="595db-117">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="595db-117">In the Description field, type a value.</span></span>
9. <span data-ttu-id="595db-118">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="595db-118">Click Save.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="595db-119">Hinzufügen von Preiselementen</span><span class="sxs-lookup"><span data-stu-id="595db-119">Add price elements</span></span>
1. <span data-ttu-id="595db-120">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="595db-120">Click Edit.</span></span>
    * <span data-ttu-id="595db-121">Jede Komponente in einem Produktmodell kann ein Basispreiselement und eine beliebige Anzahl Preisausdrucksregeln haben.</span><span class="sxs-lookup"><span data-stu-id="595db-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="595db-122">Sie können die Preise in den verschiedenen Währungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="595db-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="595db-123">Geben Sie im Feld "Basispreisausdruck" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="595db-123">In the Base price expression field, type a value.</span></span>
    * <span data-ttu-id="595db-124">Geben Sie beispielsweise "100" ein.</span><span class="sxs-lookup"><span data-stu-id="595db-124">For example, type 100.</span></span>   <span data-ttu-id="595db-125">Ein Basispreisausdruck kann ein numerischer Wert sein, oder er kann aus einer arithmetischen Berechnung mit einem oder mehreren Attribute zusammensetzen.</span><span class="sxs-lookup"><span data-stu-id="595db-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="595db-126">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="595db-126">Click Add.</span></span>
4. <span data-ttu-id="595db-127">Geben Sie im Feld "Name" 'Rosenholz' ein.</span><span class="sxs-lookup"><span data-stu-id="595db-127">In the Name field, type ‘Rosewood’.</span></span>
    * <span data-ttu-id="595db-128">Die Preisausdruckname erleichtert die Erkennung des Preiselements.</span><span class="sxs-lookup"><span data-stu-id="595db-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="595db-129">In diesem Beispiel wird ein Preiselement für die Rosenholzlautsprechergehäuse-Option erstellt.</span><span class="sxs-lookup"><span data-stu-id="595db-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="595db-130">Klicken Sie auf "Bedingung bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="595db-130">Click Edit condition.</span></span>
    * <span data-ttu-id="595db-131">Eine Preisbedingung stellt sicher, dass ein Preisausdruckselement nur dann in den Verkaufspreis einbezogen wird, wenn eine bestimmte Kombination von Attributen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="595db-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="595db-132">Geben Sie im Feld "ConstraintBody" "CabinetFinish=="Rosenholz"" ein.</span><span class="sxs-lookup"><span data-stu-id="595db-132">In the ConstraintBody field, enter 'CabinetFinish=="Rosewood"'.</span></span>
7. <span data-ttu-id="595db-133">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="595db-133">Click OK.</span></span>
8. <span data-ttu-id="595db-134">Geben Sie im Feld 'Ausdruck' einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="595db-134">In the Expression field, type a value.</span></span>
    * <span data-ttu-id="595db-135">Geben Sie beispielsweise "50" ein.</span><span class="sxs-lookup"><span data-stu-id="595db-135">For example, type 50.</span></span>  
9. <span data-ttu-id="595db-136">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="595db-136">Close the page.</span></span>
10. <span data-ttu-id="595db-137">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="595db-137">Close the page.</span></span>


