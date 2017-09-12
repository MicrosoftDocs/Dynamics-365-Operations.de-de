--- 
title: "Arbeitsplan für ein Produktmodell verwalten"
description: "Die Ausführung dieser Prozedur erfordert ein vorhandenes Produktkonfigurationsmodell."
author: BibiSp
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 3f6bacc54664c32a7d42f2befc51c420e29ada56
ms.contentlocale: de-de
ms.lasthandoff: 07/28/2017

---
# <a name="maintain-a-route-for-a-product-model"></a><span data-ttu-id="989c0-103">Arbeitsplan für ein Produktmodell verwalten</span><span class="sxs-lookup"><span data-stu-id="989c0-103">Maintain a route for a product model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="989c0-104">Die Ausführung dieser Prozedur erfordert ein vorhandenes Produktkonfigurationsmodell.</span><span class="sxs-lookup"><span data-stu-id="989c0-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="989c0-105">Bei diesem Verfahren wird das Spitzenlautsprechermodell im Vorführungsunternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="989c0-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="989c0-106">Hinzufügen eines Arbeitsplanarbeitsgangs</span><span class="sxs-lookup"><span data-stu-id="989c0-106">Add a route operation</span></span>
1. <span data-ttu-id="989c0-107">Klicken Sie auf "Produktvariantenmodell-Definition".</span><span class="sxs-lookup"><span data-stu-id="989c0-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="989c0-108">Klicken Sie auf "Produktkonfigurationsmodelle".</span><span class="sxs-lookup"><span data-stu-id="989c0-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="989c0-109">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="989c0-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="989c0-110">Wählen Sie den Spitzenlautsprecher für diese Aufgabe aus.</span><span class="sxs-lookup"><span data-stu-id="989c0-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="989c0-111">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="989c0-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="989c0-112">Erweitern Sie den Abschnitt "Arbeitsgänge".</span><span class="sxs-lookup"><span data-stu-id="989c0-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="989c0-113">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="989c0-113">Click Add.</span></span>
7. <span data-ttu-id="989c0-114">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="989c0-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="989c0-115">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="989c0-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="989c0-116">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="989c0-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="989c0-117">Eingeben von Arbeitsplanarbeitsgangdetails</span><span class="sxs-lookup"><span data-stu-id="989c0-117">Enter route operation details</span></span>
1. <span data-ttu-id="989c0-118">Klicken Sie auf "Details zum Arbeitsplanarbeitsgang"</span><span class="sxs-lookup"><span data-stu-id="989c0-118">Click Route operation details.</span></span>
2. <span data-ttu-id="989c0-119">Geben Sie im Feld 'Arbeitsgang' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="989c0-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="989c0-120">Geben Sie im Feld Arbeitsgang-</span><span class="sxs-lookup"><span data-stu-id="989c0-120">In the Oper.</span></span> <span data-ttu-id="989c0-121">Nr.</span><span class="sxs-lookup"><span data-stu-id="989c0-121">No.</span></span> <span data-ttu-id="989c0-122">eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="989c0-122">field, enter a number.</span></span>
    * <span data-ttu-id="989c0-123">Vorgangsnummer legen die Arbeitsplansequenz fest.</span><span class="sxs-lookup"><span data-stu-id="989c0-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="989c0-124">Jede Eigenschaft eines Arbeitsplanvorgang kann einen statischen Wert enthalten oder einem Attribut zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="989c0-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="989c0-125">Die Zuordnung zu einem Attribut arbeitet mit dem Wert, die als Teil der Konfiguration festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="989c0-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="989c0-126">Geben Sie im Feld "Arbeitsplangruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="989c0-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="989c0-127">Die Arbeitsgangsteuerungsgruppe bestimmt das grundlegende Verhalten der Nachkalkulation, des Verbrauch und der Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="989c0-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="989c0-128">Klicken Sie auf die Registerkarte "Einstellungen".</span><span class="sxs-lookup"><span data-stu-id="989c0-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="989c0-129">Klicken Sie auf die Registerkarte 'Zeiten'.</span><span class="sxs-lookup"><span data-stu-id="989c0-129">Click the Times tab.</span></span>
7. <span data-ttu-id="989c0-130">Geben Sie im Feld "Bearb. Menge"</span><span class="sxs-lookup"><span data-stu-id="989c0-130">In the Process qty.</span></span> <span data-ttu-id="989c0-131">eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="989c0-131">field, enter a number.</span></span>
    * <span data-ttu-id="989c0-132">Bestimmen Sie, wie viele während eines Arbeitsgangs verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="989c0-132">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="989c0-133">Geben Sie im Feld "Stunden/Zeit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="989c0-133">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="989c0-134">Geben Sie einen Zeitanteil ein.</span><span class="sxs-lookup"><span data-stu-id="989c0-134">Enter the time ratio.</span></span>  
9. <span data-ttu-id="989c0-135">Wählen Sie das Kontrollkästchen "Festlegen" aus.</span><span class="sxs-lookup"><span data-stu-id="989c0-135">Select the Set check box.</span></span>
10. <span data-ttu-id="989c0-136">Geben Sie im Feld "Laufzeit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="989c0-136">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="989c0-137">Bestimmen Sie die Bearbeitungszeit zur Menge, die Sie angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="989c0-137">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="989c0-138">Klicken Sie auf die Ressourcenanforderungsregisterkarte.</span><span class="sxs-lookup"><span data-stu-id="989c0-138">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="989c0-139">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="989c0-139">Click Add.</span></span>
13. <span data-ttu-id="989c0-140">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="989c0-140">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="989c0-141">Wählen Sie im Feld "Anforderungstyp" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="989c0-141">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="989c0-142">Entscheiden Sie, ob spezifische Ressourcen oder Funktionen vorhanden sein müssen.</span><span class="sxs-lookup"><span data-stu-id="989c0-142">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="989c0-143">Geben Sie im Feld 'Anforderung' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="989c0-143">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="989c0-144">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="989c0-144">Click OK.</span></span>


