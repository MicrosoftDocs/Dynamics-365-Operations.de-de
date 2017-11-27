---
title: "Bestellvorschläge verwalten"
description: "Dieser Artikel bietet Informationen dazu, wie Bestellvorschläge verwaltet werden. Es wird beschrieben, wie Sie den Status von Bestellvorschlägen aktualisieren, umwandeln und Bestellvorschläge filtern können, die den gleichen Status wie ein ausgewählter Bestellvorschlag haben."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8931908fbf643a8154da70d2ad065ea47d2aa4e6
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="maintain-planned-orders"></a><span data-ttu-id="7e287-104">Bestellvorschläge verwalten</span><span class="sxs-lookup"><span data-stu-id="7e287-104">Maintain planned orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7e287-105">Dieser Artikel bietet Informationen dazu, wie Bestellvorschläge verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="7e287-105">This article provides information about how to manage planned orders.</span></span> <span data-ttu-id="7e287-106">Es wird beschrieben, wie Sie den Status von Bestellvorschlägen aktualisieren, umwandeln und Bestellvorschläge filtern können, die den gleichen Status wie ein ausgewählter Bestellvorschlag haben.</span><span class="sxs-lookup"><span data-stu-id="7e287-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="7e287-107">Sie können Bestellvorschläge aus dem Arbeitsbereich **Produktprogrammplanung**, aus der Liste **Bestellvorschlag**, oder aus den Listen **Geplante Produktionsaufträge**, **Geplante Einkaufsbestellungen** und **Geplante Umlagerung** verwalten.</span><span class="sxs-lookup"><span data-stu-id="7e287-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> <span data-ttu-id="7e287-108">Sie können das Feld **Status** verwenden, um Ihren Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="7e287-108">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="7e287-109">Folgende Werte werden verwendet:</span><span class="sxs-lookup"><span data-stu-id="7e287-109">The following values are used:</span></span>

-   <span data-ttu-id="7e287-110">Wenn vom Produktprogrammplanungslauf Bestellvorschläge generiert wurden, weisen die Bestellvorschläge den Status **Offen** auf.</span><span class="sxs-lookup"><span data-stu-id="7e287-110">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="7e287-111">Wenn ein Bestellvorschlag nicht umgewandelt werden soll, können Sie ihm den Status **Abgeschlossen** zuweisen.</span><span class="sxs-lookup"><span data-stu-id="7e287-111">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="7e287-112">Wenn ein Bestellvorschlag nicht umgewandelt werden soll, können Sie diesem den Status **Genehmigt** zuweisen.</span><span class="sxs-lookup"><span data-stu-id="7e287-112">When you decide to firm a planned order, you can give it a status of **Approved**.</span></span> <span data-ttu-id="7e287-113">Mit diesem Status geben Sie an, dass Sie die Umwandlung des Bestellvorschlags genehmigen, was jedoch nicht bedeutet, dass er bereits umgewandelt ist.</span><span class="sxs-lookup"><span data-stu-id="7e287-113">This status indicates that you approve firming of the planned order, but it isn't firmed yet.</span></span>

<span data-ttu-id="7e287-114">**Hinweis:** Ein genehmigter Bestellvorschlag wird mit dem aktuellen Status in die nächste Produktprogrammplanungs-Berechnung übertragen.</span><span class="sxs-lookup"><span data-stu-id="7e287-114">**Note:** An approved planned order is transferred, in its current state, to the next master planning calculation.</span></span> <span data-ttu-id="7e287-115">Bestellvorschläge können umgewandelt werden, indem Sie auf **Vorschlagsumwandlung** klicken.</span><span class="sxs-lookup"><span data-stu-id="7e287-115">You can firm planned orders by clicking **Firm**.</span></span> <span data-ttu-id="7e287-116">Die folgenden Bestellvorschläge können umgewandelt werden:</span><span class="sxs-lookup"><span data-stu-id="7e287-116">You can firm the following planned orders:</span></span>

-   <span data-ttu-id="7e287-117">Der Bestellvorschlag, der ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="7e287-117">The planned order that is selected.</span></span>
-   <span data-ttu-id="7e287-118">Mehrere Bestellvorschläge.</span><span class="sxs-lookup"><span data-stu-id="7e287-118">Multiple planned orders.</span></span>
-   <span data-ttu-id="7e287-119">Bestellvorschläge, die mithilfe einer Stücklistenauflösung auf der Seite **Stücklistenauflösung** generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="7e287-119">Planned orders that are generated by an explosion from the **Explosion** page.</span></span> <span data-ttu-id="7e287-120">Klicken Sie auf **Bestellvorschläge**, wählen Sie den Bestellvorschlag aus, und klicken Sie dann auf **Vorschlagsumwandlung**.</span><span class="sxs-lookup"><span data-stu-id="7e287-120">Click **Planned orders**, select the planned order, and then click **Firm**.</span></span>

<span data-ttu-id="7e287-121">Nachdem ein Bestellvorschlag umgewandelt wurde, wird er in den Abschnitt "Aufträge" des jeweiligen Moduls verschoben.</span><span class="sxs-lookup"><span data-stu-id="7e287-121">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span> <span data-ttu-id="7e287-122">**Hinweis:** Sie können mit der rechten Maustaste auf einen Bestellvorschlag mit einem bestimmten Status klicken und so andere Bestellvorschläge herausfiltern, die den gleichen Status aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7e287-122">**Note:** You can right-click a planned order that has a particular status and filter for other planned orders that have the same status.</span></span> <span data-ttu-id="7e287-123">Diese Funktion ist beispielsweise nützlich zum Filtern nach allen Bestellvorschlägen mit dem Status **Genehmigt**, um sie dann umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="7e287-123">This functionality is useful if, for example, you want to filter for all planned orders that have a status of **Approved**, so that you can then firm them.</span></span>

<a name="see-also"></a><span data-ttu-id="7e287-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e287-124">See also</span></span>
--------

[<span data-ttu-id="7e287-125">Produktprogrammpläne</span><span class="sxs-lookup"><span data-stu-id="7e287-125">Master plans</span></span>](master-plans.md)




