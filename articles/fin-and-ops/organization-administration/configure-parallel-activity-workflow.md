---
title: "Konfigurieren einer parallelen Aktivität in einem Workflow"
description: "Führen Sie im Workflow-Editor die folgenden Schritte aus, um eine parallele Aktivität zu konfigurieren."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a913655b584aa23c2614903e6ede4f5826fec1fb
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="configure-a-parallel-activity-in-a-workflow"></a><span data-ttu-id="f31eb-103">Konfigurieren einer parallelen Aktivität in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="f31eb-103">Configure a parallel activity in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f31eb-104">Führen Sie im Workflow-Editor die folgenden Schritte aus, um eine parallele Aktivität zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f31eb-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="f31eb-105">Eine parallele Aktivität besteht aus Workflowverzweigungen, die gleichzeitig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f31eb-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="f31eb-106">Name der Parallelaktivität</span><span class="sxs-lookup"><span data-stu-id="f31eb-106">Name a parallel activity</span></span>
<span data-ttu-id="f31eb-107">Gehen Sie folgendermaßen vor, um einen Namen für die parallele Aktivität einzugeben.</span><span class="sxs-lookup"><span data-stu-id="f31eb-107">Follow these steps to enter a name for a parallel activity.</span></span>
1.  <span data-ttu-id="f31eb-108">Klicken Sie mit der rechten Maustaste auf die parallele Aktivität, und klicken Sie anschließend auf **Eigenschaften**, um das Formular **Eigenschaften** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f31eb-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2.  <span data-ttu-id="f31eb-109">Klicken Sie im linken Bereich auf **Grundeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="f31eb-109">In the left pane, click **Basic Settings**.</span></span>
3.  <span data-ttu-id="f31eb-110">Geben Sie im Feld **Name** einen eindeutigen Namen für die parallele Aktivität ein.</span><span class="sxs-lookup"><span data-stu-id="f31eb-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4.  <span data-ttu-id="f31eb-111">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="f31eb-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="f31eb-112">Konfigurieren der Verzweigungen der parallelen Aktivität</span><span class="sxs-lookup"><span data-stu-id="f31eb-112">Configure the branches of a parallel activity</span></span>
<span data-ttu-id="f31eb-113">Gehen Sie folgendermaßen vor, um die Verzweigungen dieser parallelen Aktivität hinzuzufügen und zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f31eb-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>
1.  <span data-ttu-id="f31eb-114">Doppelklicken Sie auf die parallele Aktivität, um die Verzweigungen der parallelen Aktivität anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f31eb-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2.  <span data-ttu-id="f31eb-115">Ziehen Sie zum Hinzufügen einer Zweigstelle das Element **Zweigstelle** aus dem Bereich **Elemente** hinzu.</span><span class="sxs-lookup"><span data-stu-id="f31eb-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="f31eb-116">Die folgende Abbildung zeigt einen Einfügepunkt.![Einfügepunkt](./media/workflow_insertionpoint.gif)</span><span class="sxs-lookup"><span data-stu-id="f31eb-116">The following figure shows an insertion point.![Insertion point](./media/workflow_insertionpoint.gif)</span></span>
    | <span data-ttu-id="f31eb-117">**Hinweis**</span><span class="sxs-lookup"><span data-stu-id="f31eb-117">**Note**</span></span>                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="f31eb-118">Die Reihenfolge der Verzweigungen ist nicht relevant, da alle Verzweigungen einer parallelen Aktivität gleichzeitig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f31eb-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span> |

3.  <span data-ttu-id="f31eb-119">Informationen zum Konfigurieren jeder Zweigstelle finden Sie unter [Konfigurieren einer parallelen Zweigstelle](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="f31eb-119">To configure each branch, see [Configure a parallel branch](configure-parallel-branch-workflow.md).</span></span>






