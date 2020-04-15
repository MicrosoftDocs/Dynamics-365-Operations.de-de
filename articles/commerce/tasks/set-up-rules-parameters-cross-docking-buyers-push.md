---
title: " Auffüllungsregeln für Crossdocking und Käuferübertragung einrichten"
description: Diese Prozedur zeigt die Schritte, um Auffüllungsregeln zu erstellen.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bccd92946783628dce37c3fd018e4dd927efd49
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141130"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a><span data-ttu-id="9bf04-103"> Auffüllungsregeln für Crossdocking und Käuferübertragung einrichten</span><span class="sxs-lookup"><span data-stu-id="9bf04-103">Set up rules and parameters for cross docking and buyer's push</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9bf04-104">Diese Prozedur zeigt die Schritte, um Auffüllungsregeln zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9bf04-104">This procedure demonstrates the steps to create Replenishment rules.</span></span> <span data-ttu-id="9bf04-105">Auffüllungsregeln können verwendet werden, um zu steuern, wie Produkte an Shops verteilt werden, wenn Crossdocking und Käuferübertragung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9bf04-105">Replenishment rules can be used to control how products are distributed to stores when using Cross-docking and Buyer´s push.</span></span> <span data-ttu-id="9bf04-106">Auffüllungsregeln können für Shops oder Shopgruppen eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="9bf04-106">Replenishment rules can be set up for stores or store groups.</span></span> <span data-ttu-id="9bf04-107">Das Gewicht, das für jede Position in einer Regel definiert wurde, steuert, wie die Mengen von Produkten zwischen den Shops verteilt werden, wenn die Auffüllungsregeln als die Verteilungsmethode im Crossdocking oder in der Käuferübertragung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9bf04-107">The weight defined for each line in a rule will control how the quantities of products will get distributed between the stores when using Replenishment rules as the distribution method in Cross-docking or Buyer´s push.</span></span> <span data-ttu-id="9bf04-108">Für diese Prozedur wird das Demo-Unternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="9bf04-108">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="9bf04-109">Gehen Sie zu "Auffüllungsregeln".</span><span class="sxs-lookup"><span data-stu-id="9bf04-109">Go to Replenishment rules.</span></span>
2. <span data-ttu-id="9bf04-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="9bf04-110">Click New.</span></span>
3. <span data-ttu-id="9bf04-111">Geben Sie im Feld "Auffüllungsregel" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9bf04-111">In the Replenishment rule field, type a value.</span></span>
4. <span data-ttu-id="9bf04-112">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9bf04-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9bf04-113">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="9bf04-113">Click Save.</span></span>
6. <span data-ttu-id="9bf04-114">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9bf04-114">Click Add.</span></span>
7. <span data-ttu-id="9bf04-115">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="9bf04-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9bf04-116">Sie können "Auffüllungshierarchie" oder "Kanal" für den Typ auswählen.</span><span class="sxs-lookup"><span data-stu-id="9bf04-116">You can choose Replenishment hierarchy or Channel for the type.</span></span> <span data-ttu-id="9bf04-117">Der Wert überprüft, ob die Auswahl in "Name" eine Hierarchie von Kanälen oder ein bestimmter Kanal ist.</span><span class="sxs-lookup"><span data-stu-id="9bf04-117">The value controls whether the selection in Name will be a hierarchy of channels or a specific channel.</span></span>  <span data-ttu-id="9bf04-118">Im vorliegenden Beispiel lassen Sie es festgelegt als "Auffüllungshierarchie".</span><span class="sxs-lookup"><span data-stu-id="9bf04-118">For this example, leave it set as Replenishment hierarchy.</span></span>  
8. <span data-ttu-id="9bf04-119">Wählen Sie im Feld "Name" einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9bf04-119">In the Name field, select a value.</span></span>
    * <span data-ttu-id="9bf04-120">Der standardmäßige Gewichtswert wird aus dem Gewicht ausgefüllt, das für den Lagerort definiert ist.</span><span class="sxs-lookup"><span data-stu-id="9bf04-120">The default weight value is populated from the weight defined on the warehouse.</span></span>  <span data-ttu-id="9bf04-121">Dieses Gewicht kann für die Auffüllungsregel verwendet werden, oder Sie können ein neues Gewicht im Feld "Gewicht" eingeben.</span><span class="sxs-lookup"><span data-stu-id="9bf04-121">This weight can be used for the Replenishment rule or you can enter a new weight in the Weight field.</span></span>  
9. <span data-ttu-id="9bf04-122">Geben Sie im Feld "Gewicht" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="9bf04-122">In the Weight field, enter a number.</span></span>
10. <span data-ttu-id="9bf04-123">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9bf04-123">Click Add.</span></span>
11. <span data-ttu-id="9bf04-124">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="9bf04-124">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="9bf04-125">Wählen Sie im Feld "Typ" die Option "Kanal" aus.</span><span class="sxs-lookup"><span data-stu-id="9bf04-125">In the Type field, select 'Channel'.</span></span>
13. <span data-ttu-id="9bf04-126">Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9bf04-126">In the Name field, enter or select a value.</span></span>
14. <span data-ttu-id="9bf04-127">Geben Sie im Feld "Gewicht" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="9bf04-127">In the Weight field, enter a number.</span></span>
15. <span data-ttu-id="9bf04-128">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="9bf04-128">Click Save.</span></span>

