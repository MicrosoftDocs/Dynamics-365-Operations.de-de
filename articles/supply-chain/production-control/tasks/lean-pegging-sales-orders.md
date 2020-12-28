---
title: Schlanker Bedarfsverursacher aus Aufträgen
description: Ziel dieser Prozedur ist die Prüfung der Bedarfsverursacherstruktur von einer Verkaufsposition, in der der Artikel mit Kanbans produziert wird.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e429fef6101f611d7a2c1b5323d6fe1e39d1cdd3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428670"
---
# <a name="lean-pegging-from-sales-orders"></a><span data-ttu-id="a351b-103">Schlanker Bedarfsverursacher aus Aufträgen</span><span class="sxs-lookup"><span data-stu-id="a351b-103">Lean pegging from sales orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a351b-104">Ziel dieser Prozedur ist die Prüfung der Bedarfsverursacherstruktur von einer Verkaufsposition, in der der Artikel mit Kanbans produziert wird.</span><span class="sxs-lookup"><span data-stu-id="a351b-104">This procedure focuses on validating the pegging tree from a sales line where the item is produced with kanbans.</span></span> <span data-ttu-id="a351b-105">Nach Überrpüfung der Bedarfsverursacherstruktur geprüft, werden alle Kanban-Einzelvorgänge geplant.</span><span class="sxs-lookup"><span data-stu-id="a351b-105">After validating the pegging tree, all the kanban jobs are planned.</span></span> <span data-ttu-id="a351b-106">Dies ist für Auftragsszenarien hilfreich, in denen die Auftragsannahme sicherstellen muss, dass Produktion unverzüglich beginnen kann.</span><span class="sxs-lookup"><span data-stu-id="a351b-106">This is useful for order scenarios where the order taker needs to ensure that production can start right away.</span></span> <span data-ttu-id="a351b-107">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="a351b-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a351b-108">Diese Vorgehensweise ist für die erweiterte Auftragsannahme kleiner Unternehmen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="a351b-108">This procedure is intended for the advanced order taker working in a lean company.</span></span>


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a><span data-ttu-id="a351b-109">Erstellen Sie einen Auftrag für einen Kanban gesteuerten Artikel</span><span class="sxs-lookup"><span data-stu-id="a351b-109">Create a sales order for a kanban controlled item</span></span>
1. <span data-ttu-id="a351b-110">Wechseln Sie zu "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="a351b-110">Go to All sales orders.</span></span>
2. <span data-ttu-id="a351b-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="a351b-111">Click New.</span></span>
3. <span data-ttu-id="a351b-112">Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a351b-112">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="a351b-113">US-001 verwenden.</span><span class="sxs-lookup"><span data-stu-id="a351b-113">Use US-001.</span></span>  
4. <span data-ttu-id="a351b-114">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="a351b-114">Click OK.</span></span>
5. <span data-ttu-id="a351b-115">Geben Sie im Feld "Artikelnummer" die Zeichenfolge "L0001" ein.</span><span class="sxs-lookup"><span data-stu-id="a351b-115">In the Item number field, type 'L0001'.</span></span>
6. <span data-ttu-id="a351b-116">Legen Sie die Menge auf "30" fest.</span><span class="sxs-lookup"><span data-stu-id="a351b-116">Set Quantity to '30'.</span></span>
    * <span data-ttu-id="a351b-117">Es ist wichtig, dass die Menge höher als 24 ist, um die Ereignis-Kanban-Regel auszulösen.</span><span class="sxs-lookup"><span data-stu-id="a351b-117">It is important that the quantity is higher than 24 in order to trigger the event kanban rule.</span></span>  

## <a name="open-a-pegging-tree"></a><span data-ttu-id="a351b-118">Öffnen Sie den Bedarfsverursacherstruktur - Überblick</span><span class="sxs-lookup"><span data-stu-id="a351b-118">Open a pegging tree</span></span> 
1. <span data-ttu-id="a351b-119">Klicken Sie auf "Produkt und Beschaffung".</span><span class="sxs-lookup"><span data-stu-id="a351b-119">Click Product and supply.</span></span>
2. <span data-ttu-id="a351b-120">Klicken Sie auf "Bedarfsverursacherstruktur anzeigen".</span><span class="sxs-lookup"><span data-stu-id="a351b-120">Click View pegging tree.</span></span>
    * <span data-ttu-id="a351b-121">Beachten Sie, dass die Bedarfsverursacherstruktur alle Projektebenen des Bedarfsverursachers anzeigt, die für die Auftragsposition erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a351b-121">Notice that the pegging tree shows all levels of the pegging needed for the sales order line.</span></span> <span data-ttu-id="a351b-122">In diesem Fall gibt es zwei Ebenen von Kanbans und allen erforderlichen Komponenten.</span><span class="sxs-lookup"><span data-stu-id="a351b-122">In this case, there are two levels of kanbans and all the required components.</span></span>  

## <a name="plan-the-pegging-tree"></a><span data-ttu-id="a351b-123">Bedarfsverursacherstruktur planen</span><span class="sxs-lookup"><span data-stu-id="a351b-123">Plan the pegging tree</span></span>
1. <span data-ttu-id="a351b-124">Wählen Sie in der Struktur "Verkaufsposition 000832 \ Kanban 000558 "aus.</span><span class="sxs-lookup"><span data-stu-id="a351b-124">In the tree, select 'Sales line 000832\Kanban 000558'.</span></span>
2. <span data-ttu-id="a351b-125">Erweitern Sie den Abschnitt "Kanban-Einzelvorgang".</span><span class="sxs-lookup"><span data-stu-id="a351b-125">Expand the Kanban jobs section.</span></span>
    * <span data-ttu-id="a351b-126">Beachten Sie, dass der Einzelvorgangsstatus für den Kanban-Einzelvorgang nicht geplant wird.</span><span class="sxs-lookup"><span data-stu-id="a351b-126">Notice that the job status for the kanban job is Not planned.</span></span>  
3. <span data-ttu-id="a351b-127">Klicken Sie "Gesamte bedarfsverursachende Struktur planen".</span><span class="sxs-lookup"><span data-stu-id="a351b-127">Click Plan entire pegging tree.</span></span>
    * <span data-ttu-id="a351b-128">Dieses plant alle Kanban-Einzelvorgänge in der Bedarfsverursacherstruktur und ändert den Einzelvorgangsstatus "Nicht geplant" nach "Geplant".</span><span class="sxs-lookup"><span data-stu-id="a351b-128">This will plan all kanban jobs in the pegging tree, changing the Job status from Not planned to Planned.</span></span>  
4. <span data-ttu-id="a351b-129">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a351b-129">Refresh the page.</span></span>
    * <span data-ttu-id="a351b-130">Beachten Sie, dass sich der Kanban-Einzelvorgangsstatus von "Nicht geplant" nach "Geplant" geändert hat.</span><span class="sxs-lookup"><span data-stu-id="a351b-130">Notice that the kanban Job status changed from Not planned to Planned.</span></span>  
5. <span data-ttu-id="a351b-131">Wählen Sie in der Struktur "Verkaufsposition Kanban 000832 \ 000558 \ Problem für L0001 \ Kanban 000559 ".</span><span class="sxs-lookup"><span data-stu-id="a351b-131">In the tree, select 'Sales line 000832\Kanban 000558\Issue for L0001\Kanban 000559'.</span></span>
    * <span data-ttu-id="a351b-132">Der Einzelvorgang für den zweiten Kanban wird auch geplant, da die gesamte Bedarfsverursacherstruktur geplant wird.</span><span class="sxs-lookup"><span data-stu-id="a351b-132">The job for the second kanban is also planned, because the entire pegging tree is planned.</span></span> <span data-ttu-id="a351b-133">Beachten Sie, dass sich der Kanban-Einzelvorgangsstatus von "Nicht geplant" nach "Geplant" geändert hat.</span><span class="sxs-lookup"><span data-stu-id="a351b-133">Notice that the kanban job status is changed from Not planned to Planned.</span></span>  

