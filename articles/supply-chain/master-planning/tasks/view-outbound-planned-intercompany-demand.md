---
title: Ausgehenden geplanten Intercompany-Bedarf anzeigen
description: Dieses Verfahren zeigt, wie Sie alle Bestellvorschläge anzeigen, die von einem Intercompany-Kreditor erfüllt werden.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 259ce229c18466b7d29fd231dc3f0be8a6906c6b
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978103"
---
# <a name="view-outbound-planned-intercompany-demand"></a><span data-ttu-id="45cce-103">Ausgehenden geplanten Intercompany-Bedarf anzeigen</span><span class="sxs-lookup"><span data-stu-id="45cce-103">View outbound planned intercompany demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="45cce-104">Dieses Verfahren zeigt, wie Sie alle Bestellvorschläge anzeigen, die von einem Intercompany-Kreditor erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="45cce-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="45cce-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist DEMF.</span><span class="sxs-lookup"><span data-stu-id="45cce-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="45cce-106">Klicken Sie auf "Produktprogrammplanung".</span><span class="sxs-lookup"><span data-stu-id="45cce-106">Click Master planning.</span></span>
2. <span data-ttu-id="45cce-107">Geben Sie im Feld "Plan" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="45cce-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="45cce-108">Wählen Sie im Feld Plan "Plan 10" aus.</span><span class="sxs-lookup"><span data-stu-id="45cce-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="45cce-109">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="45cce-109">Click Run.</span></span>
4. <span data-ttu-id="45cce-110">Geben Sie im Feld "Anzahl von Threads" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="45cce-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="45cce-111">Dies stellt die Anzahl von parallelen Threads für die Produktprogrammplanung dar.</span><span class="sxs-lookup"><span data-stu-id="45cce-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="45cce-112">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="45cce-112">Click OK.</span></span>
    * <span data-ttu-id="45cce-113">Dies kann einige Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="45cce-113">This may take a while.</span></span>  
6. <span data-ttu-id="45cce-114">Klicken Sie auf "Geplanter Intercompany-Bedarf".</span><span class="sxs-lookup"><span data-stu-id="45cce-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="45cce-115">Klicken Sie auf "Ausgehender geplanter Intercompany-Bedarf".</span><span class="sxs-lookup"><span data-stu-id="45cce-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="45cce-116">Diese Seite enthält eine Übersicht des gesamten geplanten Bedarfs, der durch einen internen Lieferkettenkreditor erfüllt wird.</span><span class="sxs-lookup"><span data-stu-id="45cce-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="45cce-117">Erweitern Sie den Abschnitt "Bedarfsdetails hochstreamen".</span><span class="sxs-lookup"><span data-stu-id="45cce-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="45cce-118">In diesem Abschnitt finden Sie Details zur Erfüllung des Bedarfs.</span><span class="sxs-lookup"><span data-stu-id="45cce-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="45cce-119">Möglicherweise müssen Sie auf die im Lieferungsunternehmen auszuführende Produktprogrammplanung warten, bevor Sie hier zusätzliche Informationen sehen.</span><span class="sxs-lookup"><span data-stu-id="45cce-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

