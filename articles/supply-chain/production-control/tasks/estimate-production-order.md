---
title: Produktionsauftrag vorkalkulieren
description: Sie können dieses Verfahren ausführen, indem Sie das USMF-Demodatunternehmen oder Ihren eigenen Datensatz verwenden.
author: johanhoffmann
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8544f468b7870b265b0c206471ad88e219258a03
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828657"
---
# <a name="estimate-a-production-order"></a><span data-ttu-id="10573-103">Produktionsauftrag vorkalkulieren</span><span class="sxs-lookup"><span data-stu-id="10573-103">Estimate a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="10573-104">Sie können dieses Verfahren ausführen, indem Sie das USMF-Demodatunternehmen oder Ihren eigenen Datensatz verwenden.</span><span class="sxs-lookup"><span data-stu-id="10573-104">You can run this procedure by using the USMF demo data company or your own data set.</span></span> <span data-ttu-id="10573-105">In beiden Fällen müssen Sie einen offenen Produktionsauftrag haben, der den Status "Erstellt" aufweist.</span><span class="sxs-lookup"><span data-stu-id="10573-105">In both cases, you need to have an open production order that has the Created status.</span></span> <span data-ttu-id="10573-106">Dies ist die zweite Prozedur von sieben, die den Produktionsauftrags-Lebenszyklus erklärt.</span><span class="sxs-lookup"><span data-stu-id="10573-106">This is the second procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="estimate-a-production-order"></a><span data-ttu-id="10573-107">Produktionsauftrag vorkalkulieren</span><span class="sxs-lookup"><span data-stu-id="10573-107">Estimate a production order</span></span>
1. <span data-ttu-id="10573-108">Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".</span><span class="sxs-lookup"><span data-stu-id="10573-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="10573-109">Wählen Sie einen Auftrag aus, der den Status "Erstellt" im Raster hat.</span><span class="sxs-lookup"><span data-stu-id="10573-109">Select an order that has the Created status in the grid.</span></span>
3. <span data-ttu-id="10573-110">Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="10573-110">On the Action Pane, click Production order.</span></span>
4. <span data-ttu-id="10573-111">Klicken Sie auf "Vorkalkulation".</span><span class="sxs-lookup"><span data-stu-id="10573-111">Click Estimate.</span></span>
    * <span data-ttu-id="10573-112">In diesem Schritt werden die vorkalkulierten Gesamtkosten eines einzelnen Produktionsauftrags berechnet.</span><span class="sxs-lookup"><span data-stu-id="10573-112">In this step, the estimated costs of a single production order is calculated.</span></span>   
5. <span data-ttu-id="10573-113">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="10573-113">Click OK.</span></span>

## <a name="view-the-calculation-details"></a><span data-ttu-id="10573-114">Berechnungsdetails anzeigen</span><span class="sxs-lookup"><span data-stu-id="10573-114">View the calculation details</span></span>
1. <span data-ttu-id="10573-115">Klicken Sie im Aktivitätsbereich auf "Kosten verwalten".</span><span class="sxs-lookup"><span data-stu-id="10573-115">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="10573-116">Klicken Sie auf Berechnungsdetails anzeigen</span><span class="sxs-lookup"><span data-stu-id="10573-116">Click View calculation details.</span></span>
    * <span data-ttu-id="10573-117">Auf dieser Seite wird die Kostenaufschlüsselung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="10573-117">This page displays the cost breakdown.</span></span> <span data-ttu-id="10573-118">So können Sie beispielsweise den gesamten Einstandspreis pro Einheit für das Fertigprodukt in der ersten Zeile anzeigen.</span><span class="sxs-lookup"><span data-stu-id="10573-118">For example, you can view the total cost price per unit for the finished product in the first row.</span></span> <span data-ttu-id="10573-119">Die folgenden Zeilen enthalten Kosten gemäß der Stückliste, den Produktionsarbeitsplan und die indirekten Kosten.</span><span class="sxs-lookup"><span data-stu-id="10573-119">The subsequent rows contain costs according to the bill of materials, production route, and indirect costs.</span></span>  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]