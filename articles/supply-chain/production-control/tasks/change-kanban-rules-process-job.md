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
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba77197f51b871f452c2aa94320aa2a68cf314df
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255372"
---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="4d976-103">Kanban-Regeln für einen Prozesseinzelvorgang ändern</span><span class="sxs-lookup"><span data-stu-id="4d976-103">Change kanban rules for a process job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4d976-104">Ziel dieser Prozedur ist es, die verwendete Kanban-Regel für einen angegebenen Kanban zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4d976-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="4d976-105">Dies ist hilfreich für Ebenenauslastungen von Recourcen oder im Falle der Aufschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="4d976-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="4d976-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="4d976-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="4d976-107">Diese Vorgehensweise ist für den Planer vorgesehen, der bei einem Lean Manufacturing-Unternehmen arbeitet, das für Wertstrom zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="4d976-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="4d976-108">Kanban-Regel kopieren</span><span class="sxs-lookup"><span data-stu-id="4d976-108">Copy kanban rule</span></span>
1. <span data-ttu-id="4d976-109">Wechseln Sie zu Kanban-Regeln.</span><span class="sxs-lookup"><span data-stu-id="4d976-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="4d976-110">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="4d976-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4d976-111">Wählen Sie die Ereignis-Kanban-Regel 000022 für L0001 aus.</span><span class="sxs-lookup"><span data-stu-id="4d976-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="4d976-112">Klicken Sie auf das Formular "Kanban-Regel duplizieren"</span><span class="sxs-lookup"><span data-stu-id="4d976-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="4d976-113">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4d976-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="4d976-114">Kanban-Regel ändern</span><span class="sxs-lookup"><span data-stu-id="4d976-114">Change kanban rule</span></span>
1. <span data-ttu-id="4d976-115">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4d976-115">Close the page.</span></span>
2. <span data-ttu-id="4d976-116">Wechseln Sie zu "Kanban-Feinterminierung".</span><span class="sxs-lookup"><span data-stu-id="4d976-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="4d976-117">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="4d976-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="4d976-118">Wählen Sie die Position mit Kanban 000177 aus.</span><span class="sxs-lookup"><span data-stu-id="4d976-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="4d976-119">Klicken Sie auf "Alternative Kanban-Regel verwenden".</span><span class="sxs-lookup"><span data-stu-id="4d976-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="4d976-120">Klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="4d976-120">Click Next.</span></span>
6. <span data-ttu-id="4d976-121">Geben Sie im Feld 'Kanban-Regel' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="4d976-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="4d976-122">Wählen Sie die Kanban-Regel aus, die Sie eben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="4d976-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="4d976-123">Dies ist die Kanban-Regel mit der höchsten Nummer.</span><span class="sxs-lookup"><span data-stu-id="4d976-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="4d976-124">Klicken Sie auf Fertig stellen.</span><span class="sxs-lookup"><span data-stu-id="4d976-124">Click Finish.</span></span>
    * <span data-ttu-id="4d976-125">Jetzt verwendet der Kanban-Einzelvorgang eine andere Kanban-Regel.</span><span class="sxs-lookup"><span data-stu-id="4d976-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="4d976-126">Dies kann hilfreich sein, um Arbeitsgruppen auf eine Ebene zu laden.</span><span class="sxs-lookup"><span data-stu-id="4d976-126">This can be useful to level load work cells.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]