--- 
title: "Regeln und Parameter für Crossdocking und Käuferübertragung einrichten"
description: "Diese Prozedur zeigt die Schritte, um Auffüllungsregeln zu erstellen."
author: josaw1
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 08f047ab38aea4958da97d80d7d274644b735cd7
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a><span data-ttu-id="31e75-103">Regeln und Parameter für Crossdocking und Käuferübertragung einrichten</span><span class="sxs-lookup"><span data-stu-id="31e75-103">Set up rules and parameters for cross-docking and buyer's push</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="31e75-104">Diese Prozedur zeigt die Schritte, um Auffüllungsregeln zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="31e75-104">This procedure demonstrates the steps to create Replenishment rules.</span></span> <span data-ttu-id="31e75-105">Auffüllungsregeln können verwendet werden, um zu steuern, wie Produkte an Shops verteilt werden, wenn Crossdocking und Käuferübertragung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31e75-105">Replenishment rules can be used to control how products are distributed to stores when using Cross-docking and Buyer´s push.</span></span> <span data-ttu-id="31e75-106">Auffüllungsregeln können für Shops oder Shopgruppen eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="31e75-106">Replenishment rules can be set up for stores or store groups.</span></span> <span data-ttu-id="31e75-107">Das Gewicht, das für jede Position in einer Regel definiert wurde, steuert, wie die Mengen von Produkten zwischen den Shops verteilt werden, wenn die Auffüllungsregeln als die Verteilungsmethode im Crossdocking oder in der Käuferübertragung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31e75-107">The weight defined for each line in a rule will control how the quantities of products will get distributed between the stores when using Replenishment rules as the distribution method in Cross-docking or Buyer´s push.</span></span> <span data-ttu-id="31e75-108">Für diese Prozedur wird das Demo-Unternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="31e75-108">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="31e75-109">Gehen Sie zu "Auffüllungsregeln".</span><span class="sxs-lookup"><span data-stu-id="31e75-109">Go to Replenishment rules.</span></span>
2. <span data-ttu-id="31e75-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="31e75-110">Click New.</span></span>
3. <span data-ttu-id="31e75-111">Geben Sie im Feld "Auffüllungsregel" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="31e75-111">In the Replenishment rule field, type a value.</span></span>
4. <span data-ttu-id="31e75-112">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="31e75-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="31e75-113">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="31e75-113">Click Save.</span></span>
6. <span data-ttu-id="31e75-114">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="31e75-114">Click Add.</span></span>
7. <span data-ttu-id="31e75-115">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="31e75-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="31e75-116">Sie können "Auffüllungshierarchie" oder "Kanal" für den Typ auswählen.</span><span class="sxs-lookup"><span data-stu-id="31e75-116">You can choose Replenishment hierarchy or Channel for the type.</span></span> <span data-ttu-id="31e75-117">Der Wert überprüft, ob die Auswahl in "Name" eine Hierarchie von Kanälen oder ein bestimmter Kanal ist.</span><span class="sxs-lookup"><span data-stu-id="31e75-117">The value controls whether the selection in Name will be a hierarchy of channels or a specific channel.</span></span>  <span data-ttu-id="31e75-118">Im vorliegenden Beispiel lassen Sie es festgelegt als "Auffüllungshierarchie".</span><span class="sxs-lookup"><span data-stu-id="31e75-118">For this example, leave it set as Replenishment hierarchy.</span></span>  
8. <span data-ttu-id="31e75-119">Wählen Sie im Feld "Name" einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="31e75-119">In the Name field, select a value.</span></span>
    * <span data-ttu-id="31e75-120">Der standardmäßige Gewichtswert wird aus dem Gewicht ausgefüllt, das für den Lagerort definiert ist.</span><span class="sxs-lookup"><span data-stu-id="31e75-120">The default weight value is populated from the weight defined on the warehouse.</span></span>  <span data-ttu-id="31e75-121">Dieses Gewicht kann für die Auffüllungsregel verwendet werden, oder Sie können ein neues Gewicht im Feld "Gewicht" eingeben.</span><span class="sxs-lookup"><span data-stu-id="31e75-121">This weight can be used for the Replenishment rule or you can enter a new weight in the Weight field.</span></span>  
9. <span data-ttu-id="31e75-122">Geben Sie im Feld "Gewicht" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="31e75-122">In the Weight field, enter a number.</span></span>
10. <span data-ttu-id="31e75-123">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="31e75-123">Click Add.</span></span>
11. <span data-ttu-id="31e75-124">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="31e75-124">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="31e75-125">Wählen Sie im Feld "Typ" die Option "Kanal" aus.</span><span class="sxs-lookup"><span data-stu-id="31e75-125">In the Type field, select 'Channel'.</span></span>
13. <span data-ttu-id="31e75-126">Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="31e75-126">In the Name field, enter or select a value.</span></span>
14. <span data-ttu-id="31e75-127">Geben Sie im Feld "Gewicht" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="31e75-127">In the Weight field, enter a number.</span></span>
15. <span data-ttu-id="31e75-128">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="31e75-128">Click Save.</span></span>


