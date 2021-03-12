---
title: Einen Kanban-Bearbeitungseinzelvorgang vorbereiten, wenn keine Materialien für die Arbeitsgruppe verfügbar sind
description: In dieser Prozedur liegt der Schwerpunkt auf dem Vorbereiten eines Kanban-Bearbeitungseinzelvorgangs, wenn einige Materialien nicht für die Arbeitsgruppe verfügbar sind und es daher erforderlich ist, Materialien aus dem Lagerort zu entnehmen.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: df0396a1d00e61ad82e52fc07779e239cd811ab8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994090"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="cb0e8-103">Einen Kanban-Bearbeitungseinzelvorgang vorbereiten, wenn keine Materialien für die Arbeitsgruppe verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="cb0e8-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cb0e8-104">In dieser Prozedur liegt der Schwerpunkt auf dem Vorbereiten eines Kanban-Bearbeitungseinzelvorgangs, wenn einige Materialien nicht für die Arbeitsgruppe verfügbar sind und es daher erforderlich ist, Materialien aus dem Lagerort zu entnehmen.</span><span class="sxs-lookup"><span data-stu-id="cb0e8-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="cb0e8-105">Das Verfahren "Bereiten Sie einen Kanban-Bearbeitungseinzelvorgang vor, wenn Materialien für die Arbeitsgruppe verfügbar sind" ist für dieses Verfahren vorausgesetzt.</span><span class="sxs-lookup"><span data-stu-id="cb0e8-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="cb0e8-106">Diese Prozedur ist für den Maschinenbediener vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="cb0e8-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="cb0e8-107">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="cb0e8-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="cb0e8-108">Wechseln Sie zu "Produktionssteuerung" > "Kanban" > "Kanban-Übersicht für Prozesseinzelvorgänge".</span><span class="sxs-lookup"><span data-stu-id="cb0e8-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="cb0e8-109">Klicken Sie im Feld "Arbeitsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cb0e8-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="cb0e8-110">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="cb0e8-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cb0e8-111">Wählen Sie die Arbeitsgruppe 1250 aus.</span><span class="sxs-lookup"><span data-stu-id="cb0e8-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="cb0e8-112">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="cb0e8-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cb0e8-113">Wählen Sie "Kanban 000356" aus.</span><span class="sxs-lookup"><span data-stu-id="cb0e8-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="cb0e8-114">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="cb0e8-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cb0e8-115">Wählen Sie in der Liste die Zeile 4 ab.</span><span class="sxs-lookup"><span data-stu-id="cb0e8-115">In the list, deselect row 4.</span></span> <span data-ttu-id="cb0e8-116">Heben Sie in der Liste die Auswahl von Zeile 4 auf, oder wählen Sie Zeile 4 aus, wenn Sie die Aufgabe "Bereiten Sie einen Kanban-Bearbeitungseinzelvorgang vor, wenn Material vorhanden ist" noch nicht abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="cb0e8-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="cb0e8-117">Schalten Sie die Erweiterung des Abschnitts "Kommissionierliste" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="cb0e8-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="cb0e8-118">Das Symbol "Kein Eintrag" im Beschaffungsstatus gibt an, dass 48 EA des Artikels P0002 für die Arbeitsgruppe fehlen.</span><span class="sxs-lookup"><span data-stu-id="cb0e8-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="cb0e8-119">Übertragen von Materialien zur Arbeitsgruppe</span><span class="sxs-lookup"><span data-stu-id="cb0e8-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="cb0e8-120">Schalten Sie die Erweiterung des Abschnitts "Umlagerungseinzelvorgänge" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="cb0e8-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="cb0e8-121">Verwenden Sie den Schnellfilter, um im Feld "Artikelnummer" nach dem Wert "P0002" zu filtern.</span><span class="sxs-lookup"><span data-stu-id="cb0e8-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="cb0e8-122">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="cb0e8-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="cb0e8-123">Klicken Sie auf "Start".</span><span class="sxs-lookup"><span data-stu-id="cb0e8-123">Click Start.</span></span>
    * <span data-ttu-id="cb0e8-124">Übertragung läuft.</span><span class="sxs-lookup"><span data-stu-id="cb0e8-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="cb0e8-125">Klicken Sie auf "Abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="cb0e8-125">Click Complete.</span></span>
    * <span data-ttu-id="cb0e8-126">Artikel P0002 ist nun in der Kommissionierliste für den Kanban-Einzelvorgang verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cb0e8-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="cb0e8-127">Das bedeutet, dass wir das Kanban mit allen obligatorischen Materialien vorbereiten können.</span><span class="sxs-lookup"><span data-stu-id="cb0e8-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="cb0e8-128">Klicken Sie auf "Vorbereiten".</span><span class="sxs-lookup"><span data-stu-id="cb0e8-128">Click Prepare.</span></span>
    * <span data-ttu-id="cb0e8-129">Beachten Sie, dass ein Symbol im Einzelvorgangsstatus angibt, dass der Einzelvorgang nun bereit ist.</span><span class="sxs-lookup"><span data-stu-id="cb0e8-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  

