---
title: Kanban-Regeln für einen Prozesseinzelvorgang ändern
description: Ziel dieser Prozedur ist es, die verwendete Kanban-Regel für einen angegebenen Kanban zu ändern.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d4c8fd8251aca2cc53e59afe4c104f2e5198426
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210961"
---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="66903-103">Kanban-Regeln für einen Prozesseinzelvorgang ändern</span><span class="sxs-lookup"><span data-stu-id="66903-103">Change kanban rules for a process job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="66903-104">Ziel dieser Prozedur ist es, die verwendete Kanban-Regel für einen angegebenen Kanban zu ändern.</span><span class="sxs-lookup"><span data-stu-id="66903-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="66903-105">Dies ist hilfreich für Ebenenauslastungen von Recourcen oder im Falle der Aufschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="66903-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="66903-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="66903-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="66903-107">Diese Vorgehensweise ist für den Planer vorgesehen, der bei einem Lean Manufacturing-Unternehmen arbeitet, das für Wertstrom zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="66903-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="66903-108">Kanban-Regel kopieren</span><span class="sxs-lookup"><span data-stu-id="66903-108">Copy kanban rule</span></span>
1. <span data-ttu-id="66903-109">Wechseln Sie zu Kanban-Regeln.</span><span class="sxs-lookup"><span data-stu-id="66903-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="66903-110">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="66903-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="66903-111">Wählen Sie die Ereignis-Kanban-Regel 000022 für L0001 aus.</span><span class="sxs-lookup"><span data-stu-id="66903-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="66903-112">Klicken Sie auf das Formular "Kanban-Regel duplizieren"</span><span class="sxs-lookup"><span data-stu-id="66903-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="66903-113">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="66903-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="66903-114">Kanban-Regel ändern</span><span class="sxs-lookup"><span data-stu-id="66903-114">Change kanban rule</span></span>
1. <span data-ttu-id="66903-115">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="66903-115">Close the page.</span></span>
2. <span data-ttu-id="66903-116">Wechseln Sie zu "Kanban-Feinterminierung".</span><span class="sxs-lookup"><span data-stu-id="66903-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="66903-117">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="66903-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="66903-118">Wählen Sie die Position mit Kanban 000177 aus.</span><span class="sxs-lookup"><span data-stu-id="66903-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="66903-119">Klicken Sie auf "Alternative Kanban-Regel verwenden".</span><span class="sxs-lookup"><span data-stu-id="66903-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="66903-120">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="66903-120">Click Next.</span></span>
6. <span data-ttu-id="66903-121">Geben Sie im Feld 'Kanban-Regel' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="66903-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="66903-122">Wählen Sie die Kanban-Regel aus, die Sie eben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="66903-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="66903-123">Dies ist die Kanban-Regel mit der höchsten Nummer.</span><span class="sxs-lookup"><span data-stu-id="66903-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="66903-124">Klicken Sie auf Fertig stellen.</span><span class="sxs-lookup"><span data-stu-id="66903-124">Click Finish.</span></span>
    * <span data-ttu-id="66903-125">Jetzt verwendet der Kanban-Einzelvorgang eine andere Kanban-Regel.</span><span class="sxs-lookup"><span data-stu-id="66903-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="66903-126">Dies kann hilfreich sein, um Arbeitsgruppen auf eine Ebene zu laden.</span><span class="sxs-lookup"><span data-stu-id="66903-126">This can be useful to level load work cells.</span></span>  

