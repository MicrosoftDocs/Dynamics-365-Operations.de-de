--- 
title: "Stückliste für ein Produktkonfigurationsmodell verwalten"
description: "Die Ausführung dieser Prozedur erfordert ein vorhandenes Produktkonfigurationsmodell."
author: BibiSp
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 380e902f9c8266f583e44fa7ea643dc5d5ab52d3
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="74d00-103">Stückliste für ein Produktkonfigurationsmodell verwalten</span><span class="sxs-lookup"><span data-stu-id="74d00-103">Maintain BOM for a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="74d00-104">Die Ausführung dieser Prozedur erfordert ein vorhandenes Produktkonfigurationsmodell.</span><span class="sxs-lookup"><span data-stu-id="74d00-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="74d00-105">Das Spitzenlautsprechermodell im Vorführungsunternehmen USMF wird verwendet, um diese Prozedur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="74d00-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="74d00-106">Hinzufügen einer Stücklistenposition</span><span class="sxs-lookup"><span data-stu-id="74d00-106">Add a BOM line</span></span>
1. <span data-ttu-id="74d00-107">Klicken Sie auf "Produktvariantenmodell-Definition".</span><span class="sxs-lookup"><span data-stu-id="74d00-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="74d00-108">Klicken Sie auf "Produktkonfigurationsmodelle".</span><span class="sxs-lookup"><span data-stu-id="74d00-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="74d00-109">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="74d00-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="74d00-110">Wählen Sie den Spitzenlautsprecher für diese Prozedur aus.</span><span class="sxs-lookup"><span data-stu-id="74d00-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="74d00-111">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="74d00-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="74d00-112">Erweitern Sie den Abschnitt "Stücklistenpositionen".</span><span class="sxs-lookup"><span data-stu-id="74d00-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="74d00-113">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="74d00-113">Click Add.</span></span>
7. <span data-ttu-id="74d00-114">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="74d00-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="74d00-115">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="74d00-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="74d00-116">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="74d00-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="74d00-117">Hinzufügen von Stücklistenpositionsdetails</span><span class="sxs-lookup"><span data-stu-id="74d00-117">Add BOM line details</span></span>
1. <span data-ttu-id="74d00-118">Klicken Sie auf "Stücklistenpositionsdetails".</span><span class="sxs-lookup"><span data-stu-id="74d00-118">Click BOM line details.</span></span>
2. <span data-ttu-id="74d00-119">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="74d00-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="74d00-120">Sie können beispielsweise Artikel "M0055" auswählen.</span><span class="sxs-lookup"><span data-stu-id="74d00-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="74d00-121">Für jede Stücklistenpositionseigenschaft können Sie festlegen, ob ein fester Wert oder ein Attribut zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="74d00-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="74d00-122">Wählen Sie das Kontrollkästchen "Festlegen" aus.</span><span class="sxs-lookup"><span data-stu-id="74d00-122">Select the Set check box.</span></span>
4. <span data-ttu-id="74d00-123">Wählen Sie "Ja" im Feld "Berechnung" aus.</span><span class="sxs-lookup"><span data-stu-id="74d00-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="74d00-124">Das Festlegen der Berechnungseigenschaft auf "Ja" gewährleistet, dass die Stücklistenposition in die Kostenberechnungen einbezogen ist.</span><span class="sxs-lookup"><span data-stu-id="74d00-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="74d00-125">Klicken Sie auf die Registerkarte "Einstellungen".</span><span class="sxs-lookup"><span data-stu-id="74d00-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="74d00-126">Wählen Sie das Kontrollkästchen "Festlegen" aus.</span><span class="sxs-lookup"><span data-stu-id="74d00-126">Select the Set check box.</span></span>
7. <span data-ttu-id="74d00-127">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="74d00-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="74d00-128">Das Feld "Menge" bestimmt die Menge des Artikels, der in der Stückliste enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="74d00-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="74d00-129">Dieser könnte ein offensichtlicher Kandidat für eine Attributzuordnung sein.</span><span class="sxs-lookup"><span data-stu-id="74d00-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="74d00-130">Klicken Sie auf die Registerkarte 'Dimensionen'.</span><span class="sxs-lookup"><span data-stu-id="74d00-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="74d00-131">Überprüfen Sie, ob vorhandene Produktdimensionen aktiv sind und daher ein Wert oder ein Attribut zugewiesen sein muss..</span><span class="sxs-lookup"><span data-stu-id="74d00-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="74d00-132">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="74d00-132">Click OK.</span></span>


