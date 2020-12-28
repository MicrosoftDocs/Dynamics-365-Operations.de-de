---
title: Einen Kanban-Bearbeitungseinzelvorgang vorbereiten, wenn Materialien für die Arbeitsgruppe verfügbar sind
description: Der Schwerpunkt dieser Aufgabe liegt auf dem Vorbereiten eines Kanban-Bearbeitungseinzelvorgangs, wenn alle Materialien für die Arbeitsgruppe verfügbar sind.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cd6d5add4d11c917a705e88d10b589e2c43fab89
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428513"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="ac34d-103">Einen Kanban-Bearbeitungseinzelvorgang vorbereiten, wenn Materialien für die Arbeitsgruppe verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="ac34d-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ac34d-104">Der Schwerpunkt dieser Aufgabe liegt auf dem Vorbereiten eines Kanban-Bearbeitungseinzelvorgangs, wenn alle Materialien für die Arbeitsgruppe verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ac34d-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="ac34d-105">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="ac34d-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="ac34d-106">Diese Aufgabe ist für den Maschinenbediener vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="ac34d-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="ac34d-107">Gehen Sie zu "Kanban Tafel für Prozesseinzelvorgänge".</span><span class="sxs-lookup"><span data-stu-id="ac34d-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="ac34d-108">Klicken Sie im Feld "Arbeitsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ac34d-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="ac34d-109">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="ac34d-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ac34d-110">Wählen Sie Arbeitsgruppe "1250" aus, und klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ac34d-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="ac34d-111">Wählen Sie in der Liste die Zeile "4" aus.</span><span class="sxs-lookup"><span data-stu-id="ac34d-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="ac34d-112">Im unveränderten Demounternehmen ist Kanban 000329 in Zeile 4 der erste Einzelvorgang, der noch nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="ac34d-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="ac34d-113">Schalten Sie die Erweiterung des Abschnitts "Kommissionierliste" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="ac34d-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="ac34d-114">Überprüfen Sie, ob der Beschaffungsstatus für alle Artikel in der Kommissionierliste verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ac34d-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="ac34d-115">Wenn mehrere Einzelvorgänge ausgewählt wurden, wird in der Kommissionierliste die Summe aller Artikel angezeigt, die für die ausgewählten Einzelvorgänge erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ac34d-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="ac34d-116">Klicken Sie auf "Vorbereiten".</span><span class="sxs-lookup"><span data-stu-id="ac34d-116">Click Prepare.</span></span>
    * <span data-ttu-id="ac34d-117">Der Vorbereitungsprozess ist nun abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="ac34d-117">The preparation process is now completed.</span></span> <span data-ttu-id="ac34d-118">Das aktivierte Kontrollkästchen für alle Zeilen in der Kommissionierliste gibt an, dass der Beschaffungsstatus entnommen wird.</span><span class="sxs-lookup"><span data-stu-id="ac34d-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  

