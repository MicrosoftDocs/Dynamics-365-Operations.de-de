---
title: Ausgewählte Formelnummer ist nicht für einen Batch-Auftrag genehmigt
description: Wenn Sie versuchen, einen geplanten Auftrag zu fixieren, erhalten Sie eine Fehlermeldung, die besagt, dass die ausgewählte Formelnummer nicht für einen Batch-Auftrag genehmigt ist.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294079"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a><span data-ttu-id="12b3a-103">Ausgewählte Formelnummer ist nicht für einen Batch-Auftrag genehmigt</span><span class="sxs-lookup"><span data-stu-id="12b3a-103">Selected formula number isn't approved for a batch order</span></span>

<span data-ttu-id="12b3a-104">Fehlercode: PRO2614</span><span class="sxs-lookup"><span data-stu-id="12b3a-104">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="12b3a-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="12b3a-105">Symptoms</span></span>

<span data-ttu-id="12b3a-106">Wenn Sie versuchen, einen geplanten Auftrag zu fixieren, erhalten Sie die folgende Fehlermeldung:</span><span class="sxs-lookup"><span data-stu-id="12b3a-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="12b3a-107">Die ausgewählte Formelnummer ist nicht für einen Chargenauftrag genehmigt.</span><span class="sxs-lookup"><span data-stu-id="12b3a-107">The selected formula number is not approved for a batch order.</span></span>

## <a name="cause"></a><span data-ttu-id="12b3a-108">Ursache</span><span class="sxs-lookup"><span data-stu-id="12b3a-108">Cause</span></span>

<span data-ttu-id="12b3a-109">Das System validiert den Vorgang der Fixierung, um sicherzustellen, dass eine genehmigte Formel für das aktive Element verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="12b3a-109">The system validates the firming operation to make sure that an approved formula is available for the active item.</span></span> <span data-ttu-id="12b3a-110">Wahrscheinlich müssen Sie die Formel genehmigen.</span><span class="sxs-lookup"><span data-stu-id="12b3a-110">You must probably approve the formula.</span></span>

## <a name="resolution"></a><span data-ttu-id="12b3a-111">Lösung</span><span class="sxs-lookup"><span data-stu-id="12b3a-111">Resolution</span></span>

<span data-ttu-id="12b3a-112">Führen Sie die folgenden Schritte aus, um eine Formel zu genehmigen.</span><span class="sxs-lookup"><span data-stu-id="12b3a-112">To approve a formula, follow these steps.</span></span>

1. <span data-ttu-id="12b3a-113">Gehen Sie zu **Produktinformationsmanagement \> Stücklisten und Formeln \> Formeln**.</span><span class="sxs-lookup"><span data-stu-id="12b3a-113">Go to **Product information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="12b3a-114">Wählen Sie die entsprechende Formel aus.</span><span class="sxs-lookup"><span data-stu-id="12b3a-114">Select the relevant formula.</span></span>
1. <span data-ttu-id="12b3a-115">Wählen Sie im Aktionsbereich auf der Registerkarte **Formel** in der Gruppe **Bearbeiten** die Option **Formel genehmigen**.</span><span class="sxs-lookup"><span data-stu-id="12b3a-115">On the Action Pane, on the **Formula** tab, in the **Maintain** group, select **Approve formula**.</span></span>
1. <span data-ttu-id="12b3a-116">Wählen Sie im Dialogfeld **Stückliste oder Formel genehmigen** einen Genehmigenden aus und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="12b3a-116">In the **Approve BOM or formula** dialog box, select an approver, and then select **OK**.</span></span>
