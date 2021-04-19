---
title: Konfigurieren paralleler Aktivitäten in einem Workflow
description: Führen Sie im Workflow-Editor die folgenden Schritte aus, um eine parallele Aktivität zu konfigurieren.
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1a47857cbe65c00ad678b2b0372c642abf01b41
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747830"
---
# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="d43bc-103">Konfigurieren paralleler Aktivitäten in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="d43bc-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d43bc-104">Führen Sie im Workflow-Editor die folgenden Schritte aus, um eine parallele Aktivität zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d43bc-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="d43bc-105">Eine parallele Aktivität besteht aus Workflowverzweigungen, die gleichzeitig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d43bc-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="d43bc-106">Name der Parallelaktivität</span><span class="sxs-lookup"><span data-stu-id="d43bc-106">Name a parallel activity</span></span>

<span data-ttu-id="d43bc-107">Gehen Sie folgendermaßen vor, um einen Namen für die parallele Aktivität einzugeben.</span><span class="sxs-lookup"><span data-stu-id="d43bc-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="d43bc-108">Klicken Sie mit der rechten Maustaste auf die parallele Aktivität, und klicken Sie anschließend auf **Eigenschaften**, um das Formular **Eigenschaften** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d43bc-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="d43bc-109">Klicken Sie im linken Bereich auf **Grundeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="d43bc-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="d43bc-110">Geben Sie im Feld **Name** einen eindeutigen Namen für die parallele Aktivität ein.</span><span class="sxs-lookup"><span data-stu-id="d43bc-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="d43bc-111">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="d43bc-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="d43bc-112">Konfigurieren der Verzweigungen der parallelen Aktivität</span><span class="sxs-lookup"><span data-stu-id="d43bc-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="d43bc-113">Gehen Sie folgendermaßen vor, um die Verzweigungen dieser parallelen Aktivität hinzuzufügen und zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d43bc-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="d43bc-114">Doppelklicken Sie auf die parallele Aktivität, um die Verzweigungen der parallelen Aktivität anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d43bc-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="d43bc-115">Ziehen Sie zum Hinzufügen einer Zweigstelle das Element **Zweigstelle** aus dem Bereich **Elemente** hinzu.</span><span class="sxs-lookup"><span data-stu-id="d43bc-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="d43bc-116">Die folgende Abbildung zeigt einen Einfügepunkt.</span><span class="sxs-lookup"><span data-stu-id="d43bc-116">The following figure shows an insertion point.</span></span>

    ![Einfügepunkt](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="d43bc-118">Die Reihenfolge der Verzweigungen ist nicht relevant, da alle Verzweigungen einer parallelen Aktivität gleichzeitig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d43bc-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="d43bc-119">Informationen zum Konfigurieren jeder Zweigstelle finden Sie unter [Konfigurieren paralleler Verzweigungen in einem Workflow](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="d43bc-119">To configure each branch, see [Configure parallel branches in a workflow](configure-parallel-branch-workflow.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]