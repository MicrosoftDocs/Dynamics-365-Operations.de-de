---
title: Produktionsauftrag vorkalkulieren
description: "Sie können dieses Verfahren ausführen, indem Sie das USMF-Demodatunternehmen oder Ihren eigenen Datensatz verwenden."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 90d6dd1886deb9ec5700e1db9b5a3aaf7f83bdf8
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---
# <a name="estimate-a-production-order"></a><span data-ttu-id="8c6f4-103">Produktionsauftrag vorkalkulieren</span><span class="sxs-lookup"><span data-stu-id="8c6f4-103">Estimate a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8c6f4-104">Sie können dieses Verfahren ausführen, indem Sie das USMF-Demodatunternehmen oder Ihren eigenen Datensatz verwenden.</span><span class="sxs-lookup"><span data-stu-id="8c6f4-104">You can run this procedure by using the USMF demo data company or your own data set.</span></span> <span data-ttu-id="8c6f4-105">In beiden Fällen müssen Sie einen offenen Produktionsauftrag haben, der den Status "Erstellt" aufweist.</span><span class="sxs-lookup"><span data-stu-id="8c6f4-105">In both cases, you need to have an open production order that has the Created status.</span></span> <span data-ttu-id="8c6f4-106">Dies ist die zweite Prozedur von sieben, die den Produktionsauftrags-Lebenszyklus erklärt.</span><span class="sxs-lookup"><span data-stu-id="8c6f4-106">This is the second procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="estimate-a-production-order"></a><span data-ttu-id="8c6f4-107">Produktionsauftrag vorkalkulieren</span><span class="sxs-lookup"><span data-stu-id="8c6f4-107">Estimate a production order</span></span>
1. <span data-ttu-id="8c6f4-108">Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".</span><span class="sxs-lookup"><span data-stu-id="8c6f4-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="8c6f4-109">Wählen Sie einen Auftrag aus, der den Status "Erstellt" im Raster hat.</span><span class="sxs-lookup"><span data-stu-id="8c6f4-109">Select an order that has the Created status in the grid.</span></span>
3. <span data-ttu-id="8c6f4-110">Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="8c6f4-110">On the Action Pane, click Production order.</span></span>
4. <span data-ttu-id="8c6f4-111">Klicken Sie auf "Vorkalkulation".</span><span class="sxs-lookup"><span data-stu-id="8c6f4-111">Click Estimate.</span></span>
    * <span data-ttu-id="8c6f4-112">In diesem Schritt werden die vorkalkulierten Gesamtkosten eines einzelnen Produktionsauftrags berechnet.</span><span class="sxs-lookup"><span data-stu-id="8c6f4-112">In this step, the estimated costs of a single production order is calculated.</span></span>   
5. <span data-ttu-id="8c6f4-113">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8c6f4-113">Click OK.</span></span>

## <a name="view-the-calculation-details"></a><span data-ttu-id="8c6f4-114">Berechnungsdetails anzeigen</span><span class="sxs-lookup"><span data-stu-id="8c6f4-114">View the calculation details</span></span>
1. <span data-ttu-id="8c6f4-115">Klicken Sie im Aktivitätsbereich auf "Kosten verwalten".</span><span class="sxs-lookup"><span data-stu-id="8c6f4-115">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="8c6f4-116">Klicken Sie auf Berechnungsdetails anzeigen</span><span class="sxs-lookup"><span data-stu-id="8c6f4-116">Click View calculation details.</span></span>
    * <span data-ttu-id="8c6f4-117">Auf dieser Seite wird die Kostenaufschlüsselung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c6f4-117">This page displays the cost breakdown.</span></span> <span data-ttu-id="8c6f4-118">So können Sie beispielsweise den gesamten Einstandspreis pro Einheit für das Fertigprodukt in der ersten Zeile anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8c6f4-118">For example, you can view the total cost price per unit for the finished product in the first row.</span></span> <span data-ttu-id="8c6f4-119">Die folgenden Zeilen enthalten Kosten gemäß der Stückliste, den Produktionsarbeitsplan und die indirekten Kosten.</span><span class="sxs-lookup"><span data-stu-id="8c6f4-119">The subsequent rows contain costs according to the bill of materials, production route, and indirect costs.</span></span>  

