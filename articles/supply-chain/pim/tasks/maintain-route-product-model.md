---
title: Arbeitsplan für ein Produktmodell verwalten
description: Die Ausführung dieser Prozedur erfordert ein vorhandenes Produktkonfigurationsmodell.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3cc8b8137fb043dab3910ebea92e0a4152c80c97
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149917"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="461d6-103">Arbeitsplan für ein Produktmodell verwalten</span><span class="sxs-lookup"><span data-stu-id="461d6-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="461d6-104">Die Ausführung dieser Prozedur erfordert ein vorhandenes Produktkonfigurationsmodell.</span><span class="sxs-lookup"><span data-stu-id="461d6-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="461d6-105">Bei diesem Verfahren wird das Spitzenlautsprechermodell im Vorführungsunternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="461d6-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="461d6-106">Hinzufügen eines Arbeitsplanarbeitsgangs</span><span class="sxs-lookup"><span data-stu-id="461d6-106">Add a route operation</span></span>
1. <span data-ttu-id="461d6-107">Klicken Sie auf "Produktvariantenmodell-Definition".</span><span class="sxs-lookup"><span data-stu-id="461d6-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="461d6-108">Klicken Sie auf "Produktkonfigurationsmodelle".</span><span class="sxs-lookup"><span data-stu-id="461d6-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="461d6-109">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="461d6-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="461d6-110">Wählen Sie den Spitzenlautsprecher für diese Aufgabe aus.</span><span class="sxs-lookup"><span data-stu-id="461d6-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="461d6-111">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="461d6-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="461d6-112">Erweitern Sie den Abschnitt "Arbeitsgänge".</span><span class="sxs-lookup"><span data-stu-id="461d6-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="461d6-113">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="461d6-113">Click Add.</span></span>
7. <span data-ttu-id="461d6-114">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="461d6-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="461d6-115">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="461d6-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="461d6-116">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="461d6-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="461d6-117">Eingeben von Arbeitsplanarbeitsgangdetails</span><span class="sxs-lookup"><span data-stu-id="461d6-117">Enter route operation details</span></span>
1. <span data-ttu-id="461d6-118">Klicken Sie auf "Details zum Arbeitsplanarbeitsgang"</span><span class="sxs-lookup"><span data-stu-id="461d6-118">Click Route operation details.</span></span>
2. <span data-ttu-id="461d6-119">Geben Sie im Feld 'Arbeitsgang' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="461d6-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="461d6-120">Geben Sie im Feld Arbeitsgang-</span><span class="sxs-lookup"><span data-stu-id="461d6-120">In the Oper.</span></span> <span data-ttu-id="461d6-121">Nr.</span><span class="sxs-lookup"><span data-stu-id="461d6-121">No.</span></span> <span data-ttu-id="461d6-122">eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="461d6-122">field, enter a number.</span></span>
    * <span data-ttu-id="461d6-123">Vorgangsnummer legen die Arbeitsplansequenz fest.</span><span class="sxs-lookup"><span data-stu-id="461d6-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="461d6-124">Jede Eigenschaft eines Arbeitsplanvorgang kann einen statischen Wert enthalten oder einem Attribut zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="461d6-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="461d6-125">Die Zuordnung zu einem Attribut arbeitet mit dem Wert, die als Teil der Konfiguration festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="461d6-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="461d6-126">Geben Sie im Feld "Arbeitsplangruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="461d6-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="461d6-127">Die Arbeitsgangsteuerungsgruppe bestimmt das grundlegende Verhalten der Nachkalkulation, des Verbrauch und der Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="461d6-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="461d6-128">Klicken Sie auf die Registerkarte "Einstellungen".</span><span class="sxs-lookup"><span data-stu-id="461d6-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="461d6-129">Klicken Sie auf die Registerkarte 'Zeiten'.</span><span class="sxs-lookup"><span data-stu-id="461d6-129">Click the Times tab.</span></span>
7. <span data-ttu-id="461d6-130">Geben Sie im Feld Prozessmenge eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="461d6-130">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="461d6-131">Bestimmen Sie, wie viele während eines Arbeitsgangs verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="461d6-131">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="461d6-132">Geben Sie im Feld "Stunden/Zeit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="461d6-132">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="461d6-133">Geben Sie einen Zeitanteil ein.</span><span class="sxs-lookup"><span data-stu-id="461d6-133">Enter the time ratio.</span></span>  
9. <span data-ttu-id="461d6-134">Wählen Sie das Kontrollkästchen "Festlegen" aus.</span><span class="sxs-lookup"><span data-stu-id="461d6-134">Select the Set check box.</span></span>
10. <span data-ttu-id="461d6-135">Geben Sie im Feld "Laufzeit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="461d6-135">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="461d6-136">Bestimmen Sie die Bearbeitungszeit zur Menge, die Sie angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="461d6-136">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="461d6-137">Klicken Sie auf die Ressourcenanforderungsregisterkarte.</span><span class="sxs-lookup"><span data-stu-id="461d6-137">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="461d6-138">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="461d6-138">Click Add.</span></span>
13. <span data-ttu-id="461d6-139">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="461d6-139">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="461d6-140">Wählen Sie im Feld "Anforderungstyp" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="461d6-140">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="461d6-141">Entscheiden Sie, ob spezifische Ressourcen oder Funktionen vorhanden sein müssen.</span><span class="sxs-lookup"><span data-stu-id="461d6-141">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="461d6-142">Geben Sie im Feld 'Anforderung' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="461d6-142">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="461d6-143">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="461d6-143">Click OK.</span></span>

