--- 
title: "Arbeitsplan für ein Produktmodell verwalten"
description: "Die Ausführung dieser Prozedur erfordert ein vorhandenes Produktkonfigurationsmodell."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
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
ms.openlocfilehash: 25d9530fc137b443b99a183b9d10886585c7b65f
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---
# <a name="maintain-a-route-for-a-product-model"></a><span data-ttu-id="ed76f-103">Arbeitsplan für ein Produktmodell verwalten</span><span class="sxs-lookup"><span data-stu-id="ed76f-103">Maintain a route for a product model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ed76f-104">Die Ausführung dieser Prozedur erfordert ein vorhandenes Produktkonfigurationsmodell.</span><span class="sxs-lookup"><span data-stu-id="ed76f-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="ed76f-105">Bei diesem Verfahren wird das Spitzenlautsprechermodell im Vorführungsunternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed76f-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="ed76f-106">Hinzufügen eines Arbeitsplanarbeitsgangs</span><span class="sxs-lookup"><span data-stu-id="ed76f-106">Add a route operation</span></span>
1. <span data-ttu-id="ed76f-107">Klicken Sie auf "Produktvariantenmodell-Definition".</span><span class="sxs-lookup"><span data-stu-id="ed76f-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="ed76f-108">Klicken Sie auf "Produktkonfigurationsmodelle".</span><span class="sxs-lookup"><span data-stu-id="ed76f-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="ed76f-109">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="ed76f-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ed76f-110">Wählen Sie den Spitzenlautsprecher für diese Aufgabe aus.</span><span class="sxs-lookup"><span data-stu-id="ed76f-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="ed76f-111">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="ed76f-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ed76f-112">Erweitern Sie den Abschnitt "Arbeitsgänge".</span><span class="sxs-lookup"><span data-stu-id="ed76f-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="ed76f-113">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ed76f-113">Click Add.</span></span>
7. <span data-ttu-id="ed76f-114">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ed76f-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="ed76f-115">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ed76f-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="ed76f-116">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ed76f-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="ed76f-117">Eingeben von Arbeitsplanarbeitsgangdetails</span><span class="sxs-lookup"><span data-stu-id="ed76f-117">Enter route operation details</span></span>
1. <span data-ttu-id="ed76f-118">Klicken Sie auf "Details zum Arbeitsplanarbeitsgang"</span><span class="sxs-lookup"><span data-stu-id="ed76f-118">Click Route operation details.</span></span>
2. <span data-ttu-id="ed76f-119">Geben Sie im Feld 'Arbeitsgang' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="ed76f-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="ed76f-120">Geben Sie im Feld Arbeitsgang-</span><span class="sxs-lookup"><span data-stu-id="ed76f-120">In the Oper.</span></span> <span data-ttu-id="ed76f-121">Nr.</span><span class="sxs-lookup"><span data-stu-id="ed76f-121">No.</span></span> <span data-ttu-id="ed76f-122">eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="ed76f-122">field, enter a number.</span></span>
    * <span data-ttu-id="ed76f-123">Vorgangsnummer legen die Arbeitsplansequenz fest.</span><span class="sxs-lookup"><span data-stu-id="ed76f-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="ed76f-124">Jede Eigenschaft eines Arbeitsplanvorgang kann einen statischen Wert enthalten oder einem Attribut zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="ed76f-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="ed76f-125">Die Zuordnung zu einem Attribut arbeitet mit dem Wert, die als Teil der Konfiguration festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ed76f-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="ed76f-126">Geben Sie im Feld "Arbeitsplangruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="ed76f-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="ed76f-127">Die Arbeitsgangsteuerungsgruppe bestimmt das grundlegende Verhalten der Nachkalkulation, des Verbrauch und der Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="ed76f-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="ed76f-128">Klicken Sie auf die Registerkarte "Einstellungen".</span><span class="sxs-lookup"><span data-stu-id="ed76f-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="ed76f-129">Klicken Sie auf die Registerkarte 'Zeiten'.</span><span class="sxs-lookup"><span data-stu-id="ed76f-129">Click the Times tab.</span></span>
7. <span data-ttu-id="ed76f-130">Geben Sie im Feld Prozessmenge eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="ed76f-130">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="ed76f-131">Bestimmen Sie, wie viele während eines Arbeitsgangs verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="ed76f-131">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="ed76f-132">Geben Sie im Feld "Stunden/Zeit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="ed76f-132">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="ed76f-133">Geben Sie einen Zeitanteil ein.</span><span class="sxs-lookup"><span data-stu-id="ed76f-133">Enter the time ratio.</span></span>  
9. <span data-ttu-id="ed76f-134">Wählen Sie das Kontrollkästchen "Festlegen" aus.</span><span class="sxs-lookup"><span data-stu-id="ed76f-134">Select the Set check box.</span></span>
10. <span data-ttu-id="ed76f-135">Geben Sie im Feld "Laufzeit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="ed76f-135">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="ed76f-136">Bestimmen Sie die Bearbeitungszeit zur Menge, die Sie angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="ed76f-136">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="ed76f-137">Klicken Sie auf die Ressourcenanforderungsregisterkarte.</span><span class="sxs-lookup"><span data-stu-id="ed76f-137">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="ed76f-138">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ed76f-138">Click Add.</span></span>
13. <span data-ttu-id="ed76f-139">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="ed76f-139">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="ed76f-140">Wählen Sie im Feld "Anforderungstyp" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="ed76f-140">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="ed76f-141">Entscheiden Sie, ob spezifische Ressourcen oder Funktionen vorhanden sein müssen.</span><span class="sxs-lookup"><span data-stu-id="ed76f-141">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="ed76f-142">Geben Sie im Feld 'Anforderung' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="ed76f-142">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="ed76f-143">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ed76f-143">Click OK.</span></span>


