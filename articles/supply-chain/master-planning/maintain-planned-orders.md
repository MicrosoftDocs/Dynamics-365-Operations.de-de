---
title: Bestellvorschläge verwalten
description: Dieser Artikel bietet Informationen dazu, wie Bestellvorschläge verwaltet werden. Es wird beschrieben, wie Sie den Status von Bestellvorschlägen aktualisieren, umwandeln und Bestellvorschläge filtern können, die den gleichen Status wie ein ausgewählter Bestellvorschlag haben.
author: roxanadiaconu
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ddf2c7b4c67bec6c29387c78d1fdb021d85d702
ms.sourcegitcommit: 620e15555d176eec3905b48d5001af1c50107ce6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2019
ms.locfileid: "1993439"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="cf32a-104">Bestellvorschläge verwalten</span><span class="sxs-lookup"><span data-stu-id="cf32a-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf32a-105">Dieser Artikel bietet Informationen dazu, wie Bestellvorschläge verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="cf32a-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="cf32a-106">Es wird beschrieben, wie Sie den Status von Bestellvorschlägen aktualisieren, umwandeln und Bestellvorschläge filtern können, die den gleichen Status wie ein ausgewählter Bestellvorschlag haben.</span><span class="sxs-lookup"><span data-stu-id="cf32a-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="cf32a-107">Sie können Bestellvorschläge aus dem Arbeitsbereich **Produktprogrammplanung**, aus der Liste **Bestellvorschlag**, oder aus den Listen **Geplante Produktionsaufträge**, **Geplante Einkaufsbestellungen** und **Geplante Umlagerung** verwalten.</span><span class="sxs-lookup"><span data-stu-id="cf32a-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="cf32a-108">Status der Bestellvorschläge</span><span class="sxs-lookup"><span data-stu-id="cf32a-108">Planned order status</span></span>
<span data-ttu-id="cf32a-109">Sie können das Feld **Status** verwenden, um Ihren Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="cf32a-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="cf32a-110">Folgende Werte werden verwendet:</span><span class="sxs-lookup"><span data-stu-id="cf32a-110">The following values are used:</span></span>

-   <span data-ttu-id="cf32a-111">Wenn vom Produktprogrammplanungslauf Bestellvorschläge generiert wurden, weisen die Bestellvorschläge den Status **Offen** auf.</span><span class="sxs-lookup"><span data-stu-id="cf32a-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="cf32a-112">Wenn ein Bestellvorschlag nicht umgewandelt werden soll, können Sie ihm den Status **Abgeschlossen** zuweisen.</span><span class="sxs-lookup"><span data-stu-id="cf32a-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="cf32a-113">Wenn Sie ein Bestellvorschlag umgewandelt werden soll, können Sie den Status in **Genehmigt** ändern.</span><span class="sxs-lookup"><span data-stu-id="cf32a-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="cf32a-114">Umgewandelte Bestellvorschläge mit Status **Genehmigt** werden von der Produktprogrammplanung respektiert, daher sind diese weder geändert noch gelöscht.</span><span class="sxs-lookup"><span data-stu-id="cf32a-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted.</span></span> 

## <a name="firming-planned-orders"></a><span data-ttu-id="cf32a-115">Umwandeln von Bestellvorschlägen</span><span class="sxs-lookup"><span data-stu-id="cf32a-115">Firming planned orders</span></span> 
<span data-ttu-id="cf32a-116">Durch die Umwandlung von Bestellvorschlägen werden tatsächliche Aufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="cf32a-116">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="cf32a-117">Diese sind auch als *freigegebene* oder *offene Aufträge* bekannt.</span><span class="sxs-lookup"><span data-stu-id="cf32a-117">These are also know as *released* or *open orders*.</span></span> <span data-ttu-id="cf32a-118">Nachdem ein Bestellvorschlag umgewandelt wurde, wird er in den Abschnitt "Aufträge" des jeweiligen Moduls verschoben.</span><span class="sxs-lookup"><span data-stu-id="cf32a-118">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="cf32a-119">Sie können auf der Seite **Bestellvorschläge** zwei Umwandlungsoptionen auswählen:</span><span class="sxs-lookup"><span data-stu-id="cf32a-119">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="cf32a-120">**Umwandlung** – Dies wandelt ein oder mehrere Bestellvorschläge um.</span><span class="sxs-lookup"><span data-stu-id="cf32a-120">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="cf32a-121">**Alle umwandeln** – Dies wandelt alle Bestellvorschläge im Filter um.</span><span class="sxs-lookup"><span data-stu-id="cf32a-121">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="cf32a-122">Wenn Sie **Alle umwandeln** verwenden, müssen Sie den Bestellvorschlag nicht auswählen, alle Bestellvorschläge innerhalb des Filters werden umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="cf32a-122">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="cf32a-123">Diese Option ist hilfreich, falls Sie eine hohe Anzahl von Bestellvorschlägen umwandeln.</span><span class="sxs-lookup"><span data-stu-id="cf32a-123">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="cf32a-124">Sie können einen Bestellvorschlag nachverfolgen, der aus der **Umwandlungshistorie** unter **Bestellvorschlagsformular > Ansicht > Umwandlungshistorie** umgewandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="cf32a-124">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="cf32a-125">Umwandlung parallelisieren</span><span class="sxs-lookup"><span data-stu-id="cf32a-125">Parallelize firming</span></span>
<span data-ttu-id="cf32a-126">Wenn Sie viele Aufträge gleichzeitig umwandeln möchten, kann das Parallelisieren des Durchlaufs die Laufzeit oder die Leistung verbessern.</span><span class="sxs-lookup"><span data-stu-id="cf32a-126">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="cf32a-127">Diese Option ist nur verfügbar, wenn mehrere Bestellvorschläge entweder mit **Umwandeln** oder **Alle umwandeln** umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="cf32a-127">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="cf32a-128">Folgende Parameter sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="cf32a-128">The following parameters are available:</span></span>

-   <span data-ttu-id="cf32a-129">**Umwandlung parallelisieren** – Bei **Ja** wird der Umwandlungsvorgang mit der Anzahl der Threads parallelisiert, die in **Anzahl der Threads** definiert werden.</span><span class="sxs-lookup"><span data-stu-id="cf32a-129">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="cf32a-130">**Anzahl der Threads** – Steuert die Anzahl der Threads, die verwendet werden, um den Umwandlungsvorgang zu parallelisieren.</span><span class="sxs-lookup"><span data-stu-id="cf32a-130">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="cf32a-131">Der Parameter wird nur angezeigt, wenn **Umwandlung parallelisieren** auf **Ja** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cf32a-131">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>


<a name="additional-resources"></a><span data-ttu-id="cf32a-132">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cf32a-132">Additional resources</span></span>
--------

[<span data-ttu-id="cf32a-133">Hauptpläne</span><span class="sxs-lookup"><span data-stu-id="cf32a-133">Master plans</span></span>](master-plans.md)



