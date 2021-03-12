---
title: Bestellvorschläge genehmigen
description: In diesem Thema wird die Genehmigung von Planaufträgen beschrieben, die in der Planungsoptimierung unterstützt werden.
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c29ede7ad8916a97b4a04b68f41961f79810e0c8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983568"
---
# <a name="approve-planned-orders"></a><span data-ttu-id="d4455-103">Bestellvorschläge genehmigen</span><span class="sxs-lookup"><span data-stu-id="d4455-103">Approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d4455-104">Dieses Thema enthält Informationen zum Aktualisieren des Status von Planaufträgen in der Planungsoptimierung.</span><span class="sxs-lookup"><span data-stu-id="d4455-104">This topic provides information about how to update the status of planned orders in Planning Optimization.</span></span>

<span data-ttu-id="d4455-105">Beachten Sie, dass die Genehmigung von Planaufträgen ein optionaler Schritt ist, um aus einem Planauftrag einen festen Auftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d4455-105">Note that approval of planned orders is an optional step, on the way to create a firmed order from a planned order.</span></span> <span data-ttu-id="d4455-106">Es wird empfohlen, geänderte Planaufträge zu genehmigen, da sonst die Änderungen beim nächsten Planungslauf ignoriert und überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d4455-106">It is recommended to approve modified planned orders, otherwise the edits will be ignored and overwritten by the next planning run.</span></span>

![Flow des Bestellvorschlags](media/approved-planned-orders-1.png)

<span data-ttu-id="d4455-108">Das **Status**-Feld hilft Ihnen dabei, Ihren Fortschritt anhand der folgenden Werte zu steuern:</span><span class="sxs-lookup"><span data-stu-id="d4455-108">The **Status** field helps you tack your progress using the following values:</span></span>

- <span data-ttu-id="d4455-109">**Offen:** Wenn vom Produktprogrammplanungslauf Bestellvorschläge generiert wurden, weisen die Bestellvorschläge den Status *Offen* auf.</span><span class="sxs-lookup"><span data-stu-id="d4455-109">**Unprocessed:** When master planning generates planned orders, the planned orders have a status of *Unprocessed*.</span></span> <span data-ttu-id="d4455-110">Planaufträge mit diesem Status werden beim nächsten Planungslauf gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d4455-110">Planned orders with this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="d4455-111">**Abgeschlossen:** Wenn Sie einen Planauftrag nicht festlegen möchten, können Sie den Status in *Abgeschlossen* ändern , um anzuzeigen, dass Sie die Bewertung dieses geplanten Auftrags abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="d4455-111">**Completed:** If you decide not to firm a planned order, you can change the status to *Completed* to indicate that you completed evaluating this planned order.</span></span> <span data-ttu-id="d4455-112">Beachten Sie, dass ein Status von *Offen* und *Abgeschlossen* vom System gleich behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="d4455-112">Note that a status of *Unprocessed* and *Completed* are treated the same by the system.</span></span>
- <span data-ttu-id="d4455-113">**Genehmigt:** Wenn Sie Änderungen beibehalten möchten oder eine geplante Bestellung festlegen möchten, ändern Sie den Status in *Genehmigt*.</span><span class="sxs-lookup"><span data-stu-id="d4455-113">**Approved:** If you want to keep edits or are planning to firm a planned order, change the status to *Approved*.</span></span> <span data-ttu-id="d4455-114">Planaufträge mit dem Status *Genehmigt* gelten als festgelegt und erwarten eine Lieferung von der Produktprogrammplanung, so dass sie bei einer späteren Ausführung der Produktprogrammplanung nicht geändert oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="d4455-114">Planned orders with *Approved* status are considered as fixed and expected supply by master planning, so they are not modified or deleted during later master planning runs.</span></span> <span data-ttu-id="d4455-115">Um dies zu erreichen, kopiert die Planungslogik während der Produktplanung die *genehmigten* Planaufträge aus der alten Planversion in die neue Planversion.</span><span class="sxs-lookup"><span data-stu-id="d4455-115">To achieve this, the planning logic copies the *Approved* planned orders from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="d4455-116">Beachten Sie, dass *Genehmigte* Planaufträge nur als Lieferung innerhalb der jeweiligen Produktprogrammplanung gelten.</span><span class="sxs-lookup"><span data-stu-id="d4455-116">Note that *Approved* planned orders are only considered supply within the specific master plan.</span></span>

<span data-ttu-id="d4455-117">Sie können Bestellvorschläge aus dem Arbeitsbereich **Produktprogrammplanung**, aus der Liste **Bestellvorschlag**, oder aus den Listen **Geplante Produktionsaufträge**, **Geplante Einkaufsbestellungen** und **Geplante Umlagerung** verwalten.</span><span class="sxs-lookup"><span data-stu-id="d4455-117">You can manage planned orders from the  **Master planning**  workspace, the  **Planned order**  list, or the  **Planned production orders**,  **Planned purchase orders**, and  **Planned transfer**  lists.</span></span>
