---
title: Konfigurieren paralleler Aktivitäten in einem Workflow
description: Führen Sie im Workflow-Editor die folgenden Schritte aus, um eine parallele Aktivität zu konfigurieren.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14b4410a0bd177159817cd5116a5a0d959992ad5
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812408"
---
# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="f4eea-103">Konfigurieren paralleler Aktivitäten in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="f4eea-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4eea-104">Führen Sie im Workflow-Editor die folgenden Schritte aus, um eine parallele Aktivität zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f4eea-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="f4eea-105">Eine parallele Aktivität besteht aus Workflowverzweigungen, die gleichzeitig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f4eea-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="f4eea-106">Name der Parallelaktivität</span><span class="sxs-lookup"><span data-stu-id="f4eea-106">Name a parallel activity</span></span>

<span data-ttu-id="f4eea-107">Gehen Sie folgendermaßen vor, um einen Namen für die parallele Aktivität einzugeben.</span><span class="sxs-lookup"><span data-stu-id="f4eea-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="f4eea-108">Klicken Sie mit der rechten Maustaste auf die parallele Aktivität, und klicken Sie anschließend auf **Eigenschaften**, um das Formular **Eigenschaften** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f4eea-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="f4eea-109">Klicken Sie im linken Bereich auf **Grundeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="f4eea-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="f4eea-110">Geben Sie im Feld **Name** einen eindeutigen Namen für die parallele Aktivität ein.</span><span class="sxs-lookup"><span data-stu-id="f4eea-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="f4eea-111">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="f4eea-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="f4eea-112">Konfigurieren der Verzweigungen der parallelen Aktivität</span><span class="sxs-lookup"><span data-stu-id="f4eea-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="f4eea-113">Gehen Sie folgendermaßen vor, um die Verzweigungen dieser parallelen Aktivität hinzuzufügen und zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f4eea-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="f4eea-114">Doppelklicken Sie auf die parallele Aktivität, um die Verzweigungen der parallelen Aktivität anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f4eea-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="f4eea-115">Ziehen Sie zum Hinzufügen einer Zweigstelle das Element **Zweigstelle** aus dem Bereich **Elemente** hinzu.</span><span class="sxs-lookup"><span data-stu-id="f4eea-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="f4eea-116">Die folgende Abbildung zeigt einen Einfügepunkt.</span><span class="sxs-lookup"><span data-stu-id="f4eea-116">The following figure shows an insertion point.</span></span>

    ![Einfügepunkt](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="f4eea-118">Die Reihenfolge der Verzweigungen ist nicht relevant, da alle Verzweigungen einer parallelen Aktivität gleichzeitig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f4eea-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="f4eea-119">Informationen zum Konfigurieren jeder Zweigstelle finden Sie unter [Konfigurieren paralleler Verzweigungen in einem Workflow](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="f4eea-119">To configure each branch, see [Configure parallel branches in a workflow](configure-parallel-branch-workflow.md).</span></span>
