---
title: Bevorzugte Wartungsarbeiter einrichten
description: In diesem Thema wird erläutert, wie Sie bevorzugte Wartungsmitarbeiter im Anlagenmanagement einrichten.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 327cda12a05ad54b310e472a652f1c822ad97142
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215331"
---
# <a name="set-up-preferred-maintenance-workers"></a><span data-ttu-id="42ba2-103">Bevorzugte Wartungsarbeiter einrichten</span><span class="sxs-lookup"><span data-stu-id="42ba2-103">Set up preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="42ba2-104">Während der Arbeitsauftragsplanung können Sie einstellen, welcher Wartungsmitarbeiter oder welche Arbeitskräftegruppe zugeordnet wird, um den Arbeitsauftrag fertig zu stellen.</span><span class="sxs-lookup"><span data-stu-id="42ba2-104">During work order scheduling, you can make a preference regarding which maintenance worker or worker group is allocated to complete the work order.</span></span> <span data-ttu-id="42ba2-105">Die Verwendung dieser Funktionalität ist optional, kann Ihnen aber helfen, sich für den am besten qualifizierten Wartungstechniker zu entscheiden, um einen Auftrag auszuführen, basierend auf den Fähigkeiten und Kompetenzen des Arbeiters.</span><span class="sxs-lookup"><span data-stu-id="42ba2-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="42ba2-106">Es werden nur Wartungsmitarbeiter geplant, die zur Planungszeit verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="42ba2-106">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="42ba2-107">Wenn eine bevorzugte Einrichtung eines Wartungsmitarbeiters bei der Terminierung mit einem Arbeitsauftrag übereinstimmt, der Wartungsmitarbeiter aber anderen Aufträgen zugeordnet ist, wird der Arbeitsauftrag einem anderen, verfügbaren Wartungsmitarbeiter zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="42ba2-107">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another available maintenance worker.</span></span>

<span data-ttu-id="42ba2-108">Bevor Sie bevorzugte Wartungsmitarbeiter einrichten können, müssen Sie die Wartungsmitarbeiter und Arbeitskräftegruppen zuerst einrichten.</span><span class="sxs-lookup"><span data-stu-id="42ba2-108">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups.</span></span> <span data-ttu-id="42ba2-109">Unter [Wartungsarbeiter und Arbeitskräftegruppen](../setup-for-objects/workers-and-worker-groups.md) finden Sie eine Beschreibung, wie Sie Wartungsarbeiter und Arbeitskräftegruppen einrichten können.</span><span class="sxs-lookup"><span data-stu-id="42ba2-109">For a description about how to set up maintenance workers and worker groups, see to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="42ba2-110">Einrichten von bevorzugten Mitarbeitern</span><span class="sxs-lookup"><span data-stu-id="42ba2-110">Set up preferred workers</span></span>

<span data-ttu-id="42ba2-111">Ein bevorzugter Wartungsmitarbeiter oder eine bevorzugte Mitarbeitergruppe kann mit folgenden Elementen in Verbindung gebracht werden:</span><span class="sxs-lookup"><span data-stu-id="42ba2-111">A preferred maintenance worker or worker group can be related to one or more of the following:</span></span>

- <span data-ttu-id="42ba2-112">Handel</span><span class="sxs-lookup"><span data-stu-id="42ba2-112">trade</span></span>  
- <span data-ttu-id="42ba2-113">Variante der Wartungsauftragsart</span><span class="sxs-lookup"><span data-stu-id="42ba2-113">maintenance job type variant</span></span>  
- <span data-ttu-id="42ba2-114">Wartungsauftragsart</span><span class="sxs-lookup"><span data-stu-id="42ba2-114">maintenance job type</span></span>  
- <span data-ttu-id="42ba2-115">Wartungsjobtyp Kategorie</span><span class="sxs-lookup"><span data-stu-id="42ba2-115">maintenance job type category</span></span>  
- <span data-ttu-id="42ba2-116">Anlage</span><span class="sxs-lookup"><span data-stu-id="42ba2-116">asset</span></span>  
- <span data-ttu-id="42ba2-117">Anlagenart</span><span class="sxs-lookup"><span data-stu-id="42ba2-117">asset type</span></span>  

<span data-ttu-id="42ba2-118">Je mehr Auswahlen Sie für den gleichen Datensatz treffen, desto spezifischer wird Ihr Setup sein.</span><span class="sxs-lookup"><span data-stu-id="42ba2-118">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="42ba2-119">Klicken Sie auf **Anlagenmanagement** > **Einrichtung** > **Arbeiter** > **Bevorzugte Wartungsmitarbeiter**.</span><span class="sxs-lookup"><span data-stu-id="42ba2-119">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="42ba2-120">Klicken Sie auf **Neu**, um einen neuen Datensatz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="42ba2-120">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="42ba2-121">Starten Sie, indem Sie einen standardmäßigen Wartungsarbeiter oder einer standardmäßige Arbeitskräftegruppe erstellen.</span><span class="sxs-lookup"><span data-stu-id="42ba2-121">Start by creating a "default" maintenance worker or worker group.</span></span> <span data-ttu-id="42ba2-122">D.h. Sie treffen nur eine Auswahl im Feld **Bevorzugte Wartungsmitarbeitergruppe** oder im Feld **Bevorzugte Wartungsmitarbeiter**.</span><span class="sxs-lookup"><span data-stu-id="42ba2-122">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="42ba2-123">Im folgenden Screenshot sehen Sie ein Beispiel im ersten Datensatz, in dem „Anfragen“ als **Bevorzugte Wartungsarbeitergruppe** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="42ba2-123">In the screenshot below, you see an example in the first record in which "Requests" is selected as **Preferred maintenance worker group**.</span></span>

    [!NOTE] <span data-ttu-id="42ba2-124">Die Standardkonfiguration wird während der Arbeitsauftragsplanung verwendet, wenn keine andere, spezifischere Kombination dem Inhalt des Arbeitsauftrags entspricht.</span><span class="sxs-lookup"><span data-stu-id="42ba2-124">The default setup will be used during work order scheduling if no other, more specific, combination matches the contents of the work order.</span></span>

4. <span data-ttu-id="42ba2-125">Wiederholen Sie Schritt 2, um einen neuen Datensatz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="42ba2-125">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="42ba2-126">Nehmen Sie die erforderlichen Einstellungen vor, je nach Detaillierungsgrad des bevorzugten Mitarbeiters oder der bevorzugten Mitarbeitergruppe.</span><span class="sxs-lookup"><span data-stu-id="42ba2-126">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> 

    <span data-ttu-id="42ba2-127">*Beispiel:* Im folgenden Screenshot, im sechsten Datensatz, wird der Wartungsarbeiter Shawn Richardson als bevorzugter Arbeiter ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="42ba2-127">*Example:* In the screenshot below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="42ba2-128">Er wird automatisch bei der Terminierung eines Arbeitsauftrags ausgewählt, der die Anlage „CH-BP1-03-02“ und die Auftragsart „Anlagenbewertung“ beinhaltet, wenn er zum geplanten Zeitpunkt verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="42ba2-128">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintenance job type "Facility assessment", if he is available at the scheduled time.</span></span>

    [!NOTE] <span data-ttu-id="42ba2-129">Im Allgemeinen, wenn ein bevorzugter Wartungsmitarbeiter während der Arbeitsauftragsplanung ausgewählt wird, durchläuft das Asset Management alle **Bevorzugter Mitarbeiter** Datensätze, um nach einer möglichen Übereinstimmung zu suchen, wobei immer zuerst die spezifischste Kombination geprüft wird.</span><span class="sxs-lookup"><span data-stu-id="42ba2-129">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="42ba2-130">Wenn keine Übereinstimmung gefunden wird, wird der „Standarddatensatz“ mit einer Auswahl entweder im Feld **Bevorzugte Wartungspersonengruppe** oder im Feld **Bevorzugte Wartungsperson** verwendet.</span><span class="sxs-lookup"><span data-stu-id="42ba2-130">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>

![Abbildung 1](media/02-work-order-scheduling.png)

<span data-ttu-id="42ba2-132">Sie können auch *verantwortliche* Instandhaltungsmitarbeiter einrichten, die beim Anlegen einer Wartungsanforderung oder eines Arbeitsauftrags ausgewählt werden können.</span><span class="sxs-lookup"><span data-stu-id="42ba2-132">You can also set up *responsible* maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="42ba2-133">Unter **Alle Arbeitsaufträge** und **Alle Wartungsanforderungen** können Sie die Auswahl bei Bedarf bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="42ba2-133">You can edit the selection in **All work orders** and **All maintenance requests**, if required.</span></span> <span data-ttu-id="42ba2-134">Weitere Informationen finden Sie unter [Verantwortliche Wartungsmitarbeiter](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="42ba2-134">For more information, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

<span data-ttu-id="42ba2-135">Bei der Arbeitsauftragsplanung werden verschiedene Werten berechnet, um festzustellen, welche Mitarbeiter die mit einem Arbeitsauftrag zusammenhängenden Aufgaben erledigen sollen (diese Noten werden in **Anlagenmanagementparameter** > **Auftragsplanung**Link eingerichtet).</span><span class="sxs-lookup"><span data-stu-id="42ba2-135">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="42ba2-136">Wenn zwei oder mehr bevorzugte Wartungsmitarbeiter oder verantwortliche Wartungsmitarbeiter bei der Arbeitsauftragsplanung die gleiche Punktzahl erhalten, wird ein Mitarbeiter zufällig ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="42ba2-136">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="42ba2-137">Andernfalls ist es immer der Mitarbeiter mit der höchsten Punktzahl, der für die Erledigung eines Arbeitsauftrags vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="42ba2-137">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

