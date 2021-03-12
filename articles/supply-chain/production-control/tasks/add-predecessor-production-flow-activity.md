---
title: Eine vorherige Aktivität zu einer Produktionsflussaktivität hinzufügen
description: In einer Produktionsflussversion müssen alle Aktivitäten geordnet werden.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9b761e61bf6a810da9258870e9a994da4ced125
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981430"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="46938-103">Eine vorherige Aktivität zu einer Produktionsflussaktivität hinzufügen</span><span class="sxs-lookup"><span data-stu-id="46938-103">Add a predecessor to a production flow activity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="46938-104">In einer Produktionsflussversion müssen alle Aktivitäten geordnet werden.</span><span class="sxs-lookup"><span data-stu-id="46938-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="46938-105">Eine Aktivität kann ein oder mehrere vorherige Aktivitäten oder Folgeaktivitäten haben.</span><span class="sxs-lookup"><span data-stu-id="46938-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="46938-106">Dieses Verfahren zeigt, wie eine vorherige Aktivität zu einer Aktivität zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="46938-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="46938-107">Um diese Aufgabe durchzuführen, benötigen Sie einen Produktionsfluss das die Entwurfsversion mit mindestens zwei Aktivitäten hat, die zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="46938-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="46938-108">Weitere Informationen finden Sie im Whitepaper "Produktionsflüsse und Aktivitäten beim Lean Manufacturing".</span><span class="sxs-lookup"><span data-stu-id="46938-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="46938-109">Suchen der Produktionsfluss und -version</span><span class="sxs-lookup"><span data-stu-id="46938-109">Find the production flow and version</span></span>
1. <span data-ttu-id="46938-110">Wechseln Sie zu "Produktionssteuerung" > "Einrichten" > "Lean-Produktionsfluss" > "Produktionsflüsse".</span><span class="sxs-lookup"><span data-stu-id="46938-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="46938-111">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="46938-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="46938-112">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="46938-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="46938-113">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="46938-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="46938-114">Klicken Sie auf "Aktivitäten".</span><span class="sxs-lookup"><span data-stu-id="46938-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="46938-115">Aktivität auswählen und eine vorherige Aktivität hinzufügen</span><span class="sxs-lookup"><span data-stu-id="46938-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="46938-116">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="46938-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="46938-117">Klicken Sie auf "Vorherige Aktivität hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="46938-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="46938-118">Geben Sie im Feld 'Aktivität' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="46938-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="46938-119">Geben Sie im Feld "Zykluszeitanteil" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="46938-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="46938-120">Der Standardzykluszeitanteil einer Aktivitätsrelation ist 1.</span><span class="sxs-lookup"><span data-stu-id="46938-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="46938-121">Diese nimmt an, dass die beiden Aktivitäten mit dem gleichen Tempo oder zur gleichen Taktzeit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="46938-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="46938-122">Wenn die vorherige Aktivität an einem höheren Tempo (niedrigere Taktzeit) ausgeführt wird, sollte das Verhältnis niedriger als 1 sein. Wenn die vorherige Aktivität in einem langsameren Tempo (höhere Taktzeit) ausgeführt wird, ist der Zykluszeitanteil größer als 1.</span><span class="sxs-lookup"><span data-stu-id="46938-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="46938-123">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="46938-123">Click OK.</span></span>

