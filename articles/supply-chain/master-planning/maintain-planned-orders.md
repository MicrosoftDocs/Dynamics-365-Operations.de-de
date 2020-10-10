---
title: Bestellvorschläge verwalten
description: Dieser Artikel bietet Informationen dazu, wie Bestellvorschläge verwaltet werden. Es wird beschrieben, wie Sie den Status von Bestellvorschlägen aktualisieren, umwandeln und Bestellvorschläge filtern können, die den gleichen Status wie ein ausgewählter Bestellvorschlag haben.
author: roxanadiaconu
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b0becf73ddde6add4076bd5b47a49eb3a0976206
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2020
ms.locfileid: "3886895"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="42ac0-104">Bestellvorschläge verwalten</span><span class="sxs-lookup"><span data-stu-id="42ac0-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42ac0-105">Dieser Artikel bietet Informationen dazu, wie Bestellvorschläge verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="42ac0-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="42ac0-106">Es wird beschrieben, wie Sie den Status von Bestellvorschlägen aktualisieren, umwandeln und Bestellvorschläge filtern können, die den gleichen Status wie ein ausgewählter Bestellvorschlag haben.</span><span class="sxs-lookup"><span data-stu-id="42ac0-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="42ac0-107">Sie können Bestellvorschläge aus dem Arbeitsbereich **Produktprogrammplanung**, aus der Liste **Bestellvorschlag**, oder aus den Listen **Geplante Produktionsaufträge**, **Geplante Einkaufsbestellungen** und **Geplante Umlagerung** verwalten.</span><span class="sxs-lookup"><span data-stu-id="42ac0-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="42ac0-108">Status der Bestellvorschläge</span><span class="sxs-lookup"><span data-stu-id="42ac0-108">Planned order status</span></span>
<span data-ttu-id="42ac0-109">Sie können das Feld **Status** verwenden, um Ihren Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="42ac0-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="42ac0-110">Folgende Werte werden verwendet:</span><span class="sxs-lookup"><span data-stu-id="42ac0-110">The following values are used:</span></span>

-   <span data-ttu-id="42ac0-111">Wenn vom Produktprogrammplanungslauf Bestellvorschläge generiert wurden, weisen die Bestellvorschläge den Status **Offen** auf.</span><span class="sxs-lookup"><span data-stu-id="42ac0-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="42ac0-112">Wenn ein Bestellvorschlag nicht umgewandelt werden soll, können Sie ihm den Status **Abgeschlossen** zuweisen.</span><span class="sxs-lookup"><span data-stu-id="42ac0-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="42ac0-113">Wenn Sie ein Bestellvorschlag umgewandelt werden soll, können Sie den Status in **Genehmigt** ändern.</span><span class="sxs-lookup"><span data-stu-id="42ac0-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="42ac0-114">Planaufträge mit dem Status **Genehmigt** werden von der Masterplanung berücksichtigt, so dass sie bei einem späteren Masterplanungslauf nicht geändert oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="42ac0-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted during a later master planning run.</span></span> <span data-ttu-id="42ac0-115">Um dies zu erreichen, kopiert die Planungslogik während der Produktplanung die **genehmigten** Planaufträge aus der alten Planversion in die neue Planversion.</span><span class="sxs-lookup"><span data-stu-id="42ac0-115">To achieve this, the planning logic copies the **Approved** planned orders from the old plan version to the new plan version during master planning.</span></span>

## <a name="firming-planned-orders"></a><span data-ttu-id="42ac0-116">Umwandeln von Bestellvorschlägen</span><span class="sxs-lookup"><span data-stu-id="42ac0-116">Firming planned orders</span></span> 
<span data-ttu-id="42ac0-117">Durch die Umwandlung von Bestellvorschlägen werden tatsächliche Aufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="42ac0-117">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="42ac0-118">Diese sind auch als *freigegebene* oder *offene Aufträge* bekannt.</span><span class="sxs-lookup"><span data-stu-id="42ac0-118">These are also known as *released* or *open orders*.</span></span> <span data-ttu-id="42ac0-119">Nachdem ein Bestellvorschlag umgewandelt wurde, wird er in den Abschnitt "Aufträge" des jeweiligen Moduls verschoben.</span><span class="sxs-lookup"><span data-stu-id="42ac0-119">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="42ac0-120">Sie können auf der Seite **Bestellvorschläge** zwei Umwandlungsoptionen auswählen:</span><span class="sxs-lookup"><span data-stu-id="42ac0-120">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="42ac0-121">**Umwandlung** – Dies wandelt ein oder mehrere Bestellvorschläge um.</span><span class="sxs-lookup"><span data-stu-id="42ac0-121">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="42ac0-122">**Alle umwandeln** – Dies wandelt alle Bestellvorschläge im Filter um.</span><span class="sxs-lookup"><span data-stu-id="42ac0-122">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="42ac0-123">Wenn Sie **Alle umwandeln** verwenden, müssen Sie den Bestellvorschlag nicht auswählen, alle Bestellvorschläge innerhalb des Filters werden umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="42ac0-123">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="42ac0-124">Diese Option ist hilfreich, falls Sie eine hohe Anzahl von Bestellvorschlägen umwandeln.</span><span class="sxs-lookup"><span data-stu-id="42ac0-124">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="42ac0-125">Sie können einen Bestellvorschlag nachverfolgen, der aus der **Umwandlungshistorie** unter **Bestellvorschlagsformular > Ansicht > Umwandlungshistorie** umgewandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="42ac0-125">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="42ac0-126">Umwandlung parallelisieren</span><span class="sxs-lookup"><span data-stu-id="42ac0-126">Parallelize firming</span></span>
<span data-ttu-id="42ac0-127">Wenn Sie viele Aufträge gleichzeitig umwandeln möchten, kann das Parallelisieren des Durchlaufs die Laufzeit oder die Leistung verbessern.</span><span class="sxs-lookup"><span data-stu-id="42ac0-127">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="42ac0-128">Diese Option ist nur verfügbar, wenn mehrere Bestellvorschläge entweder mit **Umwandeln** oder **Alle umwandeln** umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="42ac0-128">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="42ac0-129">Folgende Parameter sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="42ac0-129">The following parameters are available:</span></span>

-   <span data-ttu-id="42ac0-130">**Umwandlung parallelisieren** – Bei **Ja** wird der Umwandlungsvorgang mit der Anzahl der Threads parallelisiert, die in **Anzahl der Threads** definiert werden.</span><span class="sxs-lookup"><span data-stu-id="42ac0-130">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="42ac0-131">**Anzahl der Threads** – Steuert die Anzahl der Threads, die verwendet werden, um den Umwandlungsvorgang zu parallelisieren.</span><span class="sxs-lookup"><span data-stu-id="42ac0-131">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="42ac0-132">Der Parameter wird nur angezeigt, wenn **Umwandlung parallelisieren** auf **Ja** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="42ac0-132">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>

> [!NOTE]
> <span data-ttu-id="42ac0-133">Die Option für **Umwandlung parallelisieren** wird nur angezeigt, wenn Sie mehr als einen Planauftrag zum Fixieren ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="42ac0-133">The option for **Parallelize firming** is only shown when you have more than one planned order selected for firming.</span></span>

<a name="additional-resources"></a><span data-ttu-id="42ac0-134">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="42ac0-134">Additional resources</span></span>
--------

[<span data-ttu-id="42ac0-135">Übersicht zu Produktprogrammplänen</span><span class="sxs-lookup"><span data-stu-id="42ac0-135">Master plans overview</span></span>](master-plans.md)



