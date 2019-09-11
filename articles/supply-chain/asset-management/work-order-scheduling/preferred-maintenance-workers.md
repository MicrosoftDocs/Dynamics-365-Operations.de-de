---
title: Bevorzugte Wartungsarbeiter einrichten
description: In diesem Thema wird erläutert, wie Sie bevorzugte Wartungsmitarbeiter im Anlagenmanagement einrichten.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887410"
---
# <a name="preferred-maintenance-workers"></a><span data-ttu-id="f98cb-103">Bevorzugte Wartungsarbeiter</span><span class="sxs-lookup"><span data-stu-id="f98cb-103">Preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="f98cb-104">Sie können bei der Arbeitsvorbereitung einstellen, welche Wartungsmitarbeiter zu kompletten Arbeitsaufträgen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f98cb-104">You can make a preference regarding which maintenance workers are allocated to complete work orders during work order scheduling.</span></span> <span data-ttu-id="f98cb-105">Die Verwendung dieser Funktionalität ist optional, kann Ihnen aber helfen, sich für den am besten qualifizierten Wartungstechniker zu entscheiden, um einen Auftrag auszuführen, basierend auf den Fähigkeiten und Kompetenzen des Arbeiters.</span><span class="sxs-lookup"><span data-stu-id="f98cb-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="f98cb-106">Daher wird bei der Arbeitsauftragsplanung anhand des Einrichtens unter **Bevorzugte Wartungsmitarbeiter** festgelegt, ob ein bestimmter Wartungsmitarbeiter oder eine bestimmte Mitarbeitergruppe für einen Arbeitsauftrag geplant werden soll.</span><span class="sxs-lookup"><span data-stu-id="f98cb-106">Therefore, during work order scheduling, the setup in **Preferred maintenance workers** is used to determine if a specific maintenance worker or worker group should be scheduled for a work order.</span></span> <span data-ttu-id="f98cb-107">Es werden nur Wartungsmitarbeiter geplant, die zur Planungszeit verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f98cb-107">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="f98cb-108">Wenn eine bevorzugte Einrichtung eines Wartungsmitarbeiters bei der Terminierung mit einem Arbeitsauftrag übereinstimmt, der Wartungsmitarbeiter aber anderen Aufträgen zugeordnet ist, wird der Arbeitsauftrag einem anderen, verfügbaren Wartungsmitarbeiter zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="f98cb-108">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another, available, maintenance worker.</span></span>

<span data-ttu-id="f98cb-109">Bevor Sie bevorzugte Wartungsmitarbeiter einrichten können, müssen Sie zunächst die Wartungsmitarbeiter und Arbeitsgruppen einrichten, die zur Auswahl stehen sollen.</span><span class="sxs-lookup"><span data-stu-id="f98cb-109">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups that should be available for selection.</span></span> <span data-ttu-id="f98cb-110">Unter [Wartungspersonal und Arbeitsgruppen](../setup-for-objects/workers-and-worker-groups.md) finden Sie eine Beschreibung, wie Sie Wartungspersonal und Arbeitsgruppen einrichten können.</span><span class="sxs-lookup"><span data-stu-id="f98cb-110">Refer to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md) for a description on how to set up maintenance workers and worker groups.</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="f98cb-111">Einrichten von bevorzugten Mitarbeitern</span><span class="sxs-lookup"><span data-stu-id="f98cb-111">Set up preferred workers</span></span>

<span data-ttu-id="f98cb-112">Ein bevorzugter Wartungsmitarbeiter oder eine bevorzugte Mitarbeitergruppe kann mit einer bestimmten Person in Verbindung gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="f98cb-112">A preferred maintenance worker or worker group can be related to a specific</span></span>

- <span data-ttu-id="f98cb-113">Handel</span><span class="sxs-lookup"><span data-stu-id="f98cb-113">trade</span></span>  
- <span data-ttu-id="f98cb-114">Variante der Wartungsauftragsart</span><span class="sxs-lookup"><span data-stu-id="f98cb-114">maintenance job type variant</span></span>  
- <span data-ttu-id="f98cb-115">Wartungsauftragsart</span><span class="sxs-lookup"><span data-stu-id="f98cb-115">maintenance job type</span></span>  
- <span data-ttu-id="f98cb-116">Wartungsjobtyp Kategorie</span><span class="sxs-lookup"><span data-stu-id="f98cb-116">maintenance job type category</span></span>  
- <span data-ttu-id="f98cb-117">Anlage</span><span class="sxs-lookup"><span data-stu-id="f98cb-117">asset</span></span>  
- <span data-ttu-id="f98cb-118">Anlagenart</span><span class="sxs-lookup"><span data-stu-id="f98cb-118">asset type</span></span>  

<span data-ttu-id="f98cb-119">oder eine Kombination dieser Auswahlmöglichkeiten.</span><span class="sxs-lookup"><span data-stu-id="f98cb-119">or a combination of those selections.</span></span> <span data-ttu-id="f98cb-120">Je mehr Auswahlen Sie für den gleichen Datensatz treffen, desto spezifischer wird Ihr Setup sein.</span><span class="sxs-lookup"><span data-stu-id="f98cb-120">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="f98cb-121">Klicken Sie auf **Anlagenmanagement** > **Einrichtung** > **Arbeiter** > **Bevorzugte Wartungsmitarbeiter**.</span><span class="sxs-lookup"><span data-stu-id="f98cb-121">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="f98cb-122">Klicken Sie auf **Neu**, um einen neuen Datensatz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f98cb-122">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="f98cb-123">Beginnen Sie mit der Erstellung eines „standardmäßigen“ Wartungsmitarbeiters oder einer Arbeitsgruppeneinrichtung, die keine Auswahl in den Feldern der obigen Aufzählungsliste hat.</span><span class="sxs-lookup"><span data-stu-id="f98cb-123">Start by creating a "default" maintenance worker or worker group setup that has no selections in the fields shown in the bullet list above.</span></span> <span data-ttu-id="f98cb-124">D.h. Sie treffen nur eine Auswahl im Feld **Bevorzugte Wartungsmitarbeitergruppe** oder im Feld **Bevorzugte Wartungsmitarbeiter**.</span><span class="sxs-lookup"><span data-stu-id="f98cb-124">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="f98cb-125">In der folgenden Abbildung sehen Sie ein Beispiel im ersten Datensatz, in dem „Anfragen“ als bevorzugte Wartungsmitarbeitergruppe ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="f98cb-125">In the figure below, you see an example in the first record in which "Requests" is selected as preferred maintenance worker group.</span></span>

>[!NOTE]
><span data-ttu-id="f98cb-126">Die Standardeinstellung wird bei der Arbeitsauftragsplanung verwendet, falls keine andere, spezifischere Kombination mit dem Inhalt des Arbeitsauftrags bei der Arbeitsauftragsplanung übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="f98cb-126">The default setup will be used during work order scheduling in case no other, more specific, combination matches the contents of the work order during work order scheduling.</span></span>

4. <span data-ttu-id="f98cb-127">Wiederholen Sie Schritt 2, um einen neuen Datensatz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f98cb-127">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="f98cb-128">Nehmen Sie die erforderlichen Einstellungen vor, je nach Detaillierungsgrad des bevorzugten Mitarbeiters oder der bevorzugten Mitarbeitergruppe.</span><span class="sxs-lookup"><span data-stu-id="f98cb-128">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> <span data-ttu-id="f98cb-129">*Beispiel:* In der folgenden Abbildung, im sechsten Datensatz, wird der Wartungsarbeiter Shawn Richardson als bevorzugter Arbeiter ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="f98cb-129">*Example:* In the figure below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="f98cb-130">Er wird automatisch bei der Terminierung eines Arbeitsauftrags ausgewählt, der die Anlage „CH-BP1-03-02“ und die Auftragsart „Anlagenbewertung“ beinhaltet, wenn er zum geplanten Zeitpunkt verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f98cb-130">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintennace job type "Facility assessment", if he is available at the scheduled time.</span></span>

>[!NOTE]
><span data-ttu-id="f98cb-131">Im Allgemeinen, wenn ein bevorzugter Wartungsmitarbeiter während der Arbeitsauftragsplanung ausgewählt wird, durchläuft das Asset Management alle **Bevorzugter Mitarbeiter** Datensätze, um nach einer möglichen Übereinstimmung zu suchen, wobei immer zuerst die spezifischste Kombination geprüft wird.</span><span class="sxs-lookup"><span data-stu-id="f98cb-131">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="f98cb-132">Wenn keine Übereinstimmung gefunden wird, wird der „Standarddatensatz“ mit einer Auswahl entweder im Feld **Bevorzugte Wartungspersonengruppe** oder im Feld **Bevorzugte Wartungsperson** verwendet.</span><span class="sxs-lookup"><span data-stu-id="f98cb-132">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>


![Abbildung 1](media/02-work-order-scheduling.png)

<span data-ttu-id="f98cb-134">Sie können auch verantwortliche Instandhaltungsmitarbeiter einrichten, die beim Anlegen einer Wartungsanforderung oder eines Arbeitsauftrags ausgewählt werden können.</span><span class="sxs-lookup"><span data-stu-id="f98cb-134">You can also set up responsible maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="f98cb-135">Unter **Alle Arbeitsaufträge** und **Alle Wartungsanforderungen** können Sie die Auswahl bei Bedarf bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="f98cb-135">In **All work orders** and **All maintenance requests**, you can edit the selection, if required.</span></span> <span data-ttu-id="f98cb-136">Weitere Informationen finden Sie unter [Verantwortliche Wartungsmitarbeiter](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="f98cb-136">Refer to [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md) for more information.</span></span>

<span data-ttu-id="f98cb-137">Bei der Arbeitsauftragsplanung werden verschiedene Werten berechnet, um festzustellen, welche Mitarbeiter die mit einem Arbeitsauftrag zusammenhängenden Aufgaben erledigen sollen (diese Noten werden in **Anlagenmanagementparameter** > **Auftragsplanung**Link eingerichtet).</span><span class="sxs-lookup"><span data-stu-id="f98cb-137">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="f98cb-138">Wenn zwei oder mehr bevorzugte Wartungsmitarbeiter oder verantwortliche Wartungsmitarbeiter bei der Arbeitsauftragsplanung die gleiche Punktzahl erhalten, wird ein Mitarbeiter zufällig ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="f98cb-138">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="f98cb-139">Andernfalls ist es immer der Mitarbeiter mit der höchsten Punktzahl, der für die Erledigung eines Arbeitsauftrags vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="f98cb-139">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

