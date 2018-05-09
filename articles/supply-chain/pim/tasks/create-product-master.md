--- 
title: Produktmaster erstellen
description: "Erstellen eines Produktmasters für vordefinierte Varianten."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fa2ea0f36f059b582b5e8658ffacde527425fcba
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-product-master"></a><span data-ttu-id="c2f95-103">Produktmaster erstellen</span><span class="sxs-lookup"><span data-stu-id="c2f95-103">Create a product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c2f95-104">Erstellen eines Produktmasters für vordefinierte Varianten.</span><span class="sxs-lookup"><span data-stu-id="c2f95-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="c2f95-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="c2f95-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c2f95-106">Diese Prozedur ist für den Produktionsplaner vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="c2f95-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="c2f95-107">Neuen Produktmaster erstellen</span><span class="sxs-lookup"><span data-stu-id="c2f95-107">Create a new product master</span></span>
1. <span data-ttu-id="c2f95-108">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Produktmaster".</span><span class="sxs-lookup"><span data-stu-id="c2f95-108">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="c2f95-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="c2f95-109">Click New.</span></span>
3. <span data-ttu-id="c2f95-110">Geben Sie im Feld "Produktnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c2f95-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="c2f95-111">Die Nummer muss eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="c2f95-111">The number must be unique.</span></span> <span data-ttu-id="c2f95-112">Ein Nummernkreis kann im Feld "Produktnummer" eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c2f95-112">A number sequence can be set for the Product number field.</span></span> <span data-ttu-id="c2f95-113">In diesem Fall muss der Benutzer keinen Wert eingeben.</span><span class="sxs-lookup"><span data-stu-id="c2f95-113">In this case, the user doesn't have to enter a value.</span></span>  
4. <span data-ttu-id="c2f95-114">Geben Sie im Feld "Produktname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c2f95-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="c2f95-115">Geben Sie einen beschreibenden Namen des Produkts ein.</span><span class="sxs-lookup"><span data-stu-id="c2f95-115">Enter a descriptive product name.</span></span> <span data-ttu-id="c2f95-116">Der Wert ist standardmäßig der Suchname, er kann jedoch auch vom Benutzer geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c2f95-116">The value defaults to the search name, but this can be changed by the user.</span></span>  
5. <span data-ttu-id="c2f95-117">Klicken Sie im Feld "Produktdimensionsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c2f95-117">In the Product dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c2f95-118">Die Produktdimensionsgruppe legt fest, welche der 4 Produktdimensionen für die Erstellung der Produktvarianten verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c2f95-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="c2f95-119">In diesem Beispiel wird eine Gruppe mit Farbe und Größe verwendet.</span><span class="sxs-lookup"><span data-stu-id="c2f95-119">This example uses a group with color and size.</span></span>  
6. <span data-ttu-id="c2f95-120">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="c2f95-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="c2f95-121">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c2f95-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c2f95-122">Die Standardkonfigurationstechnologie ist die vordefinierte Variante.</span><span class="sxs-lookup"><span data-stu-id="c2f95-122">The default configuration technology is Predefined variant.</span></span> <span data-ttu-id="c2f95-123">Diese wird für dieses Beispiel verwendet.</span><span class="sxs-lookup"><span data-stu-id="c2f95-123">This will be used for this example.</span></span>  
8. <span data-ttu-id="c2f95-124">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c2f95-124">Click OK.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="c2f95-125">Produktdimensionsgruppen auswählen</span><span class="sxs-lookup"><span data-stu-id="c2f95-125">Select product dimension groups</span></span>
1. <span data-ttu-id="c2f95-126">Klicken Sie im Feld "Farbgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c2f95-126">In the Color group field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="c2f95-127">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="c2f95-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c2f95-128">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c2f95-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c2f95-129">Klicken Sie im Feld "Größengruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c2f95-129">In the Size group field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c2f95-130">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="c2f95-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="c2f95-131">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c2f95-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="c2f95-132">Dimensionsgruppen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="c2f95-132">Add dimension groups</span></span>
1. <span data-ttu-id="c2f95-133">Klicken Sie im Aktivitätsbereich auf "Produkt".</span><span class="sxs-lookup"><span data-stu-id="c2f95-133">On the Action Pane, click Product.</span></span>
2. <span data-ttu-id="c2f95-134">Klicken Sie auf "Dimensionsgruppen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c2f95-134">Click Dimension groups to open the drop dialog.</span></span>
3. <span data-ttu-id="c2f95-135">Klicken Sie im Feld "Lagerdimensionsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c2f95-135">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c2f95-136">Mit Lagerdimensionsgruppen kann gesteuert werden, wie Artikel im Lagerbestand gespeichert und aus dem Lagerbestand entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="c2f95-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="c2f95-137">So kann eine Lagerdimension Standort und Lagerort enthalten.</span><span class="sxs-lookup"><span data-stu-id="c2f95-137">For example, a storage dimension can include Site and Warehouse.</span></span>  
4. <span data-ttu-id="c2f95-138">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="c2f95-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c2f95-139">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c2f95-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c2f95-140">Klicken Sie im Feld "Rückverfolgungsangaben-Gruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c2f95-140">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c2f95-141">Die Rückverfolgungsangabengruppe bestimmt, welche Rückverfolgungsangaben Sie einem Produkt hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="c2f95-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="c2f95-142">Die Chargennummer und die Seriennummer können z. B. zum Nachverfolgen von Lagerartikeln verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2f95-142">For example, the batch number and serial number are used to track inventory items.</span></span>  
7. <span data-ttu-id="c2f95-143">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="c2f95-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="c2f95-144">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c2f95-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c2f95-145">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c2f95-145">Click OK.</span></span>
10. <span data-ttu-id="c2f95-146">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="c2f95-146">Click Save.</span></span>
11. <span data-ttu-id="c2f95-147">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c2f95-147">Close the page.</span></span>


