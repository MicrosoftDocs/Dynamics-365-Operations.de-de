--- 
title: "Eine vorherige Aktivität zu einer Produktionsflussaktivität hinzufügen"
description: "In einer Produktionsflussversion müssen alle Aktivitäten geordnet werden."
author: cvocph
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d19fb20e8cc941daeaa506e4bf1cb0c7031cf2ee
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="81a94-103">Eine vorherige Aktivität zu einer Produktionsflussaktivität hinzufügen</span><span class="sxs-lookup"><span data-stu-id="81a94-103">Add a predecessor to a production flow activity</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="81a94-104">In einer Produktionsflussversion müssen alle Aktivitäten geordnet werden.</span><span class="sxs-lookup"><span data-stu-id="81a94-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="81a94-105">Eine Aktivität kann ein oder mehrere vorherige Aktivitäten oder Folgeaktivitäten haben.</span><span class="sxs-lookup"><span data-stu-id="81a94-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="81a94-106">Dieses Verfahren zeigt, wie eine vorherige Aktivität zu einer Aktivität zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="81a94-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="81a94-107">Um diese Aufgabe durchzuführen, benötigen Sie einen Produktionsfluss das die Entwurfsversion mit mindestens zwei Aktivitäten hat, die zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="81a94-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="81a94-108">Weitere Informationen finden Sie im Whitepaper "Produktionsflüsse und Aktivitäten beim Lean Manufacturing".</span><span class="sxs-lookup"><span data-stu-id="81a94-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="81a94-109">Suchen der Produktionsfluss und -version</span><span class="sxs-lookup"><span data-stu-id="81a94-109">Find the production flow and version</span></span>
1. <span data-ttu-id="81a94-110">Wechseln Sie zu "Produktionssteuerung" > "Einrichten" > "Lean-Produktionsfluss" > "Produktionsflüsse".</span><span class="sxs-lookup"><span data-stu-id="81a94-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="81a94-111">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="81a94-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="81a94-112">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="81a94-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="81a94-113">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="81a94-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="81a94-114">Klicken Sie auf "Aktivitäten".</span><span class="sxs-lookup"><span data-stu-id="81a94-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="81a94-115">Aktivität auswählen und eine vorherige Aktivität hinzufügen</span><span class="sxs-lookup"><span data-stu-id="81a94-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="81a94-116">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="81a94-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="81a94-117">Klicken Sie auf "Vorherige Aktivität hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="81a94-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="81a94-118">Geben Sie im Feld 'Aktivität' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="81a94-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="81a94-119">Geben Sie im Feld "Zykluszeitanteil" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="81a94-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="81a94-120">Der Standardzykluszeitanteil einer Aktivitätsrelation ist 1.</span><span class="sxs-lookup"><span data-stu-id="81a94-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="81a94-121">Diese nimmt an, dass die beiden Aktivitäten mit dem gleichen Tempo oder zur gleichen Taktzeit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="81a94-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="81a94-122">Wenn die vorherige Aktivität an einem höheren Tempo (niedrigere Taktzeit) ausgeführt wird, sollte das Verhältnis niedriger als 1 sein. Wenn die vorherige Aktivität in einem langsameren Tempo (höhere Taktzeit) ausgeführt wird, ist der Zykluszeitanteil größer als 1.</span><span class="sxs-lookup"><span data-stu-id="81a94-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="81a94-123">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="81a94-123">Click OK.</span></span>


