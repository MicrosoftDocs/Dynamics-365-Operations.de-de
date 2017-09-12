--- 
title: "Eine vorhandene Aktivität zu einer Produktionsflussversion hinzufügen"
description: "Wenn Sie neue Versionen von Produktionsflüssen erstellen, können Sie Aktivitäten hinzuzufügen, die für die Vorgängerversionen der neuen Version erstellt werden."
author: cvocph
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 262fa70f0fa3c294059b3379c179be62100ea5a8
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a><span data-ttu-id="4495e-103">Eine vorhandene Aktivität zu einer Produktionsflussversion hinzufügen</span><span class="sxs-lookup"><span data-stu-id="4495e-103">Add an existing activity to a production flow version</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4495e-104">Wenn Sie neue Versionen von Produktionsflüssen erstellen, können Sie Aktivitäten hinzuzufügen, die für die Vorgängerversionen der neuen Version erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4495e-104">When creating new versions of production flows, you can choose to add activities created for the older versions, to the new version.</span></span> <span data-ttu-id="4495e-105">Dieses Verfahren zeigt, wie Sie eine neue Version für einen vorhandenen Produktionsfluss erstellen, ohne die Aktivitäten zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="4495e-105">This procedure shows how a new version is created for an existing production flow, without copying the activities.</span></span> <span data-ttu-id="4495e-106">Im nächsten Schritt wird einer vorhandenen Aktivität der neuen Version hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4495e-106">In the next step, an existing activity is added to the new version.</span></span> 

<span data-ttu-id="4495e-107">Diese Aufgabe erfordert einen Produktionsfluss mit der Version und Aktivitäten, die bereits erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4495e-107">This task requires production flow with version and activities already created.</span></span>


## <a name="create-a-new-production-flow-version"></a><span data-ttu-id="4495e-108">Neue Produktionsflussversion erstellen</span><span class="sxs-lookup"><span data-stu-id="4495e-108">Create a new production flow version</span></span>
1. <span data-ttu-id="4495e-109">Wechseln Sie zu "Produktionssteuerung" > "Einrichten" > "Lean-Produktionsfluss" > "Produktionsflüsse".</span><span class="sxs-lookup"><span data-stu-id="4495e-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="4495e-110">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="4495e-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="4495e-111">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="4495e-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="4495e-112">Klicken Sie auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="4495e-112">Click Edit.</span></span>
5. <span data-ttu-id="4495e-113">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="4495e-113">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="4495e-114">Geben Sie im Feld "Ablaufdatum" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="4495e-114">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="4495e-115">Prüfen Sie das Ablaufdatum und der Ablaufuhrzeit der aktiven Version bevor Sie eine neue Produktionsflussversion erstellen.</span><span class="sxs-lookup"><span data-stu-id="4495e-115">Note that before you create a new production flow version, make sure to check the expiration date and time of the active version.</span></span> <span data-ttu-id="4495e-116">Die neue Version wird mit einem effektiven Startdatum erstellt, das zum Ablaufdatum der ausgewählten Version passt.</span><span class="sxs-lookup"><span data-stu-id="4495e-116">The new version will be created with an effective start date, which connects to the expiry date of the selected version.</span></span>  
7. <span data-ttu-id="4495e-117">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4495e-117">Click Add.</span></span>
8. <span data-ttu-id="4495e-118">Wählen Sie "Nein" im Feld "Von Version kopieren" aus.</span><span class="sxs-lookup"><span data-stu-id="4495e-118">Select No in the Copy from version field.</span></span>
    * <span data-ttu-id="4495e-119">Wählen Sie auf "Nein" aus, um ohne Version zu starten, wenn die Mehrheit der Aktivitäten die kopierte Version nach neue Aktivitäten ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="4495e-119">Select No to start with an empty version if most of the activities of the copied version will be replaced by new activities.</span></span> <span data-ttu-id="4495e-120">Fügen Sie den unveränderten Aktivitäten zur "Vorhandenes Element hinzufügen"-Funktion im Aktivitätsformular manuell hinzu.</span><span class="sxs-lookup"><span data-stu-id="4495e-120">Add the unchanged activities to the Add existing function in the activity form manually.</span></span>  
9. <span data-ttu-id="4495e-121">Wählen Sie "Nein" im Feld "Kanban-Regeln duplizieren" aus.</span><span class="sxs-lookup"><span data-stu-id="4495e-121">Select No in the Duplicate kanban rules field.</span></span>
    * <span data-ttu-id="4495e-122">Werden die Aktivitäten nicht in die neue Version kopiert werden, ist es nicht möglich Kanban-Regeln zum Zeitpunkt der Erstellung der neuen Version zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="4495e-122">When the activities are not copied to the new version, it is not possible to copy the kanban rules at the time of creation of the new version.</span></span>   <span data-ttu-id="4495e-123">Verwenden Sie stattdessen die "Kanban-Ersetzung"-Funktion später im Kanban-Regel-Formular, um die Kanban-Regeln der alten Produktionsflussversion durch Kanban-Regeln mit der Aktivitäten der neuen Version zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="4495e-123">Instead you will use the create replacement kanban function later in the kanban rule form, to replace kanban rules of the old production flow version with kanban rules using the activities of the new version.</span></span>  
10. <span data-ttu-id="4495e-124">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4495e-124">Click OK.</span></span>
11. <span data-ttu-id="4495e-125">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="4495e-125">In the list, find and select the desired record.</span></span>

## <a name="add-an-existing-activity"></a><span data-ttu-id="4495e-126">Vorhandene Aktivität hinzufügen</span><span class="sxs-lookup"><span data-stu-id="4495e-126">Add an existing activity</span></span>
1. <span data-ttu-id="4495e-127">Klicken Sie auf "Aktivitäten".</span><span class="sxs-lookup"><span data-stu-id="4495e-127">Click Activities.</span></span>
2. <span data-ttu-id="4495e-128">Klicken Sie auf "Vorhandenes Element hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4495e-128">Click Add existing to open the drop dialog.</span></span>
    * <span data-ttu-id="4495e-129">Suchen Sie eine bestehende Aktivität aus, die der neuen Produktionsflussversion hinzugefügt werden soll und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="4495e-129">Find and select an existing activity to be added to the new production flow version.</span></span>  <span data-ttu-id="4495e-130">Beachten Sie, dass die Liste alle Aktivitäten anzeigt, die für den Produktionsfluss für alle vorherigen Versionen Datenfluss erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="4495e-130">Note that the list shows all activities that have been created for this production flow for all previous versions of the flow.</span></span>  
3. <span data-ttu-id="4495e-131">Geben Sie im Feld 'Aktivität' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="4495e-131">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="4495e-132">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4495e-132">Click OK.</span></span>


