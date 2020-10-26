---
title: Serviceauftragsphasen
description: Wenn Sie die Phasen für einen Serviceauftrag definieren und diese den Arbeitskräften zuweisen, können Sie den Ablauf eines Serviceauftrags durch die Aufgaben steuern, die verschiedene Personen in der Serviceorganisation ausführen.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52bcb72e8222b378198fcd044428fa1a4a0e8944
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978434"
---
# <a name="service-order-stages"></a><span data-ttu-id="dd49f-103">Serviceauftragsphasen</span><span class="sxs-lookup"><span data-stu-id="dd49f-103">Service order stages</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="dd49f-104">Sie können Phasen für einen Serviceauftrag einrichten, um die Aufgaben zu definieren, die abgeschlossen werden müssen, die Reihenfolge, in der sie ausgeführt werden, und die Arbeitskräfte, die für ihre Ausführung zuständig sind.</span><span class="sxs-lookup"><span data-stu-id="dd49f-104">You can set up stages for a service order to define the tasks that must be completed, the order in which they are completed, and the workers who are responsible for completing them.</span></span> <span data-ttu-id="dd49f-105">Wenn Sie die Phasen für einen Serviceauftrag definieren und diese den Arbeitskräften zuweisen, können Sie den Ablauf eines Serviceauftrags durch die Aufgaben steuern, die verschiedene Personen in der Serviceorganisation ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd49f-105">By defining the stages for a service order and assigning them to workers, you can control the flow of a service order through the tasks that various people perform in the service organization.</span></span> <span data-ttu-id="dd49f-106">Die Sequenz der Phasen muss eine Anfangsphase enthalten.</span><span class="sxs-lookup"><span data-stu-id="dd49f-106">The sequence of stages must include an initial stage.</span></span>

<span data-ttu-id="dd49f-107">Sie können auch die Aktivitäten festlegen, die in jeder Stufe zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="dd49f-107">You can also define the actions that are permitted at each stage.</span></span> <span data-ttu-id="dd49f-108">Beispiel: Wird das Kontrollkästchen **Buchen** mit Ausnahme der letzten Phase für alle Phasen deaktiviert, können Serviceaufträge erst gebucht werden, nachdem sie die Phasen vollständig durchlaufen haben.</span><span class="sxs-lookup"><span data-stu-id="dd49f-108">For example, if you clear the **Post** check box for all stages except the final stage, you prevent any service orders from being posted before the service orders are processed through the complete sequence of stages.</span></span>

## <a name="branching-in-service-order-stages"></a><span data-ttu-id="dd49f-109">Verzweigung in Phasen des Serviceauftrags</span><span class="sxs-lookup"><span data-stu-id="dd49f-109">Branching in service order stages</span></span>

<span data-ttu-id="dd49f-110">Wenn Sie eine Servicephase einrichten, können Sie mehrere Optionen oder Verzweigungen erstellen, aus denen für die nächste Servicephase ausgewäht werden kann.</span><span class="sxs-lookup"><span data-stu-id="dd49f-110">When you set up a service stage, you can create multiple options, or branches, to select from for the next service stage.</span></span> <span data-ttu-id="dd49f-111">Alle Verzweigungen, die Sie erstellen, können ausgewählt werden, wenn die Anfangsphase abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="dd49f-111">All the branches that you create are available to select from when the initial stage is completed.</span></span> <span data-ttu-id="dd49f-112">Beispielsweise richten Sie **Planung** als Anfangsphase ein.</span><span class="sxs-lookup"><span data-stu-id="dd49f-112">For example, you set up **Planning** as an initial stage.</span></span> <span data-ttu-id="dd49f-113">Sie erstellen zwei Phasen, die **In Bearbeitung** und **Abbrechen** benannt sind, und wählen dann **Planung** als das übergeordnete Element für sie aus.</span><span class="sxs-lookup"><span data-stu-id="dd49f-113">You create two stages named **In process** and **Cancel**, and then select **Planning** as the parent for them.</span></span> <span data-ttu-id="dd49f-114">Sie weisen die Phase **Planung** dem Auftrag zu.</span><span class="sxs-lookup"><span data-stu-id="dd49f-114">You assign the **Planning** stage to sales order.</span></span> <span data-ttu-id="dd49f-115">Wenn die Planungsphase für den Auftrag abgeschlossen ist, können Sie die Phase **In Bearbeitung** auswählen, wenn der Auftrag für die Bearbeitung bereit ist, oder Sie können die Phase **Abbrechen** auswählen, wenn der Auftrag storniert wird.</span><span class="sxs-lookup"><span data-stu-id="dd49f-115">When the planning stage for the sales order is completed, you can select the **In process** stage if the sales order is ready to work on, or you can select the **Cancel** stage if the sales order is canceled.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd49f-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd49f-116">See also</span></span>

[<span data-ttu-id="dd49f-117">Serviceauftragsphasen einrichten</span><span class="sxs-lookup"><span data-stu-id="dd49f-117">Set up service order stages</span></span>](set-up-service-order-stages.md)

[<span data-ttu-id="dd49f-118">Ändern der Phase eines Serviceauftrags</span><span class="sxs-lookup"><span data-stu-id="dd49f-118">Change the service order stage</span></span>](change-service-order-stage.md)

  


