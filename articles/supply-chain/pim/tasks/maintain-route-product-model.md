---
title: Arbeitsplan für ein Produktmodell verwalten
description: Die Ausführung dieser Prozedur erfordert ein vorhandenes Produktkonfigurationsmodell.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45c6b1e6e75645bb17ce4defa0bca0e6d2131b6e
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921264"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="27512-103">Arbeitsplan für ein Produktmodell verwalten</span><span class="sxs-lookup"><span data-stu-id="27512-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="27512-104">Die Ausführung dieser Prozedur erfordert ein vorhandenes Produktkonfigurationsmodell.</span><span class="sxs-lookup"><span data-stu-id="27512-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="27512-105">Bei diesem Verfahren wird das Spitzenlautsprechermodell im Vorführungsunternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="27512-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>

## <a name="add-a-route-operation"></a><span data-ttu-id="27512-106">Hinzufügen eines Arbeitsplanarbeitsgangs</span><span class="sxs-lookup"><span data-stu-id="27512-106">Add a route operation</span></span>

1. <span data-ttu-id="27512-107">Wechseln Sie zu **Produktinformationsmanagement \> Produkte \> Produktkonfigurationsmodelle**.</span><span class="sxs-lookup"><span data-stu-id="27512-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="27512-108">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="27512-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="27512-109">Wählen Sie den Spitzenlautsprecher für diese Aufgabe aus.</span><span class="sxs-lookup"><span data-stu-id="27512-109">Select the High end speaker model for this exercise.</span></span>  
1. <span data-ttu-id="27512-110">Wählen Sie in der Liste den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="27512-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="27512-111">Erweitern Sie den Abschnitt **Arbeitsplanvorgänge**.</span><span class="sxs-lookup"><span data-stu-id="27512-111">Expand the **Route operations** section.</span></span>
1. <span data-ttu-id="27512-112">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="27512-112">Select **Add**.</span></span>
1. <span data-ttu-id="27512-113">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="27512-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="27512-114">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="27512-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="27512-115">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="27512-115">Select **Save**.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="27512-116">Eingeben von Arbeitsplanarbeitsgangdetails</span><span class="sxs-lookup"><span data-stu-id="27512-116">Enter route operation details</span></span>

1. <span data-ttu-id="27512-117">Wählen Sie **Details zum Arbeitsplanvorgang**.</span><span class="sxs-lookup"><span data-stu-id="27512-117">Select **Route operation details**.</span></span>
1. <span data-ttu-id="27512-118">Geben Sie im Feld **Vorgang** einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="27512-118">In the **Operation** field, enter or select a value.</span></span>
1. <span data-ttu-id="27512-119">In dem **Vorgang. Nr.**</span><span class="sxs-lookup"><span data-stu-id="27512-119">In the **Oper. No.**</span></span> <span data-ttu-id="27512-120">eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="27512-120">field, enter a number.</span></span>
    * <span data-ttu-id="27512-121">Vorgangsnummer legen die Arbeitsplansequenz fest.</span><span class="sxs-lookup"><span data-stu-id="27512-121">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="27512-122">Jede Eigenschaft eines Arbeitsplanvorgang kann einen statischen Wert enthalten oder einem Attribut zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="27512-122">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="27512-123">Die Zuordnung zu einem Attribut arbeitet mit dem Wert, die als Teil der Konfiguration festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="27512-123">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
1. <span data-ttu-id="27512-124">Geben Sie im Feld **Arbeitsplan-Gruppe** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="27512-124">In the **Route group** field, enter or select a value.</span></span>
    * <span data-ttu-id="27512-125">Die Arbeitsgangsteuerungsgruppe bestimmt das grundlegende Verhalten der Nachkalkulation, des Verbrauch und der Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="27512-125">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
1. <span data-ttu-id="27512-126">Wählen Sie die Registerkarte **Einrichten**.</span><span class="sxs-lookup"><span data-stu-id="27512-126">Select the **Setup** tab.</span></span>
1. <span data-ttu-id="27512-127">Wählen Sie die Registerkarte **Zeiten**.</span><span class="sxs-lookup"><span data-stu-id="27512-127">Select the **Times** tab.</span></span>
1. <span data-ttu-id="27512-128">Geben Sie im Feld **Anzahl verarbeiten** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="27512-128">In the **Process qty.** field, enter a number.</span></span>
    * <span data-ttu-id="27512-129">Bestimmen Sie, wie viele während eines Arbeitsgangs verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="27512-129">Determine how many will be processed during one operation.</span></span>  
1. <span data-ttu-id="27512-130">Geben Sie im Feld **Stunden/Zeit** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="27512-130">In the **Hours/time** field, enter a number.</span></span>
    * <span data-ttu-id="27512-131">Geben Sie einen Zeitanteil ein.</span><span class="sxs-lookup"><span data-stu-id="27512-131">Enter the time ratio.</span></span>  
1. <span data-ttu-id="27512-132">Aktivieren Sie das Kontrollkästchen **Setzen**.</span><span class="sxs-lookup"><span data-stu-id="27512-132">Select the **Set** check box.</span></span>
1. <span data-ttu-id="27512-133">Geben Sie im Feld **Laufzeit** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="27512-133">In the **Run time** field, enter a number.</span></span>
    * <span data-ttu-id="27512-134">Bestimmen Sie die Bearbeitungszeit zur Menge, die Sie angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="27512-134">Determine the processing time for the quantity that you have specified.</span></span>  
1. <span data-ttu-id="27512-135">Wählen Sie die Registerkarte **Ressourcenanforderung**.</span><span class="sxs-lookup"><span data-stu-id="27512-135">Select the **Resource requirements** tab.</span></span>
1. <span data-ttu-id="27512-136">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="27512-136">Select **Add**.</span></span>
1. <span data-ttu-id="27512-137">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="27512-137">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="27512-138">Wählen Sie im Feld **Bedarfstyp** eine Option.</span><span class="sxs-lookup"><span data-stu-id="27512-138">In the **Requirement type** field, select an option.</span></span>
    * <span data-ttu-id="27512-139">Entscheiden Sie, ob spezifische Ressourcen oder Funktionen vorhanden sein müssen.</span><span class="sxs-lookup"><span data-stu-id="27512-139">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
1. <span data-ttu-id="27512-140">Geben Sie im Feld **Anforderung** einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="27512-140">In the **Requirement** field, enter or select a value.</span></span>
1. <span data-ttu-id="27512-141">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="27512-141">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]