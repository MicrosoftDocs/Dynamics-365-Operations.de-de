---
title: Kanban-Status aktualisieren
description: Wenn ein Kanban versehentlich geleert wird, oder ein empfangener Kanban geleert werden muss, müssen Sie den Kanbanstatus aktualisieren.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48dd5c3a878efb7413f461e76fde086030015b60
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146674"
---
# <a name="update-kanban-status"></a><span data-ttu-id="27208-103">Kanban-Status aktualisieren</span><span class="sxs-lookup"><span data-stu-id="27208-103">Update kanban status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="27208-104">Wenn ein Kanban versehentlich geleert wird, oder ein empfangener Kanban geleert werden muss, müssen Sie den Kanbanstatus aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="27208-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="27208-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="27208-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="27208-106">Diese Prozedur ist für den Filialleiter vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="27208-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="27208-107">Suchen Sie den Kanban.</span><span class="sxs-lookup"><span data-stu-id="27208-107">Find the kanban.</span></span>
1. <span data-ttu-id="27208-108">Wechseln Sie zu "Produktionssteuerung" > "Kanban" > "Kanbans".</span><span class="sxs-lookup"><span data-stu-id="27208-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="27208-109">Öffnen Sie den Spaltenfilter "Status der Handhabungseinheit".</span><span class="sxs-lookup"><span data-stu-id="27208-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="27208-110">Auf 'Löschen' klicken</span><span class="sxs-lookup"><span data-stu-id="27208-110">Click Clear.</span></span>
    * <span data-ttu-id="27208-111">Dies setzt die Filter zurück.</span><span class="sxs-lookup"><span data-stu-id="27208-111">This resets the filters.</span></span>  
4. <span data-ttu-id="27208-112">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="27208-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="27208-113">Filtern Sie beispielsweise nach dem Feld "Kartennummer" mit dem Wert "000149".</span><span class="sxs-lookup"><span data-stu-id="27208-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="27208-114">Ändern Sie den Status "Geleert" zum Status "Eingegangen".</span><span class="sxs-lookup"><span data-stu-id="27208-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="27208-115">Klicken Sie auf "Leere Handhabungseinheit zurücksetzen".</span><span class="sxs-lookup"><span data-stu-id="27208-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="27208-116">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="27208-116">Click OK.</span></span>
    * <span data-ttu-id="27208-117">Beachten Sie, dass der "Status der Handhabungseinheit" den Wert "Eingegangen" hat.</span><span class="sxs-lookup"><span data-stu-id="27208-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="27208-118">Ändern Sie den Status "Eingegangen" zum Status "Geleert".</span><span class="sxs-lookup"><span data-stu-id="27208-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="27208-119">Klicken Sie auf "Kanban leeren".</span><span class="sxs-lookup"><span data-stu-id="27208-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="27208-120">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="27208-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="27208-121">Beachten Sie, dass die "Handhabungseinheit" den Status "Geleert" hat.</span><span class="sxs-lookup"><span data-stu-id="27208-121">Notice that the Handling unit status is Emptied.</span></span>  

