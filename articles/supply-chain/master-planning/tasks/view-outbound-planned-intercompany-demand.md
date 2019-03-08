---
title: Ausgehenden geplanten Intercompany-Bedarf anzeigen
description: Dieses Verfahren zeigt, wie Sie alle Bestellvorschläge anzeigen, die von einem Intercompany-Kreditor erfüllt werden.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2e0e3a4613e5598e725c475c7dff7662bf4169a7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "333713"
---
# <a name="view-outbound-planned-intercompany-demand"></a><span data-ttu-id="59693-103">Ausgehenden geplanten Intercompany-Bedarf anzeigen</span><span class="sxs-lookup"><span data-stu-id="59693-103">View outbound planned intercompany demand</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="59693-104">Dieses Verfahren zeigt, wie Sie alle Bestellvorschläge anzeigen, die von einem Intercompany-Kreditor erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="59693-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="59693-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist DEMF.</span><span class="sxs-lookup"><span data-stu-id="59693-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="59693-106">Klicken Sie auf "Produktprogrammplanung".</span><span class="sxs-lookup"><span data-stu-id="59693-106">Click Master planning.</span></span>
2. <span data-ttu-id="59693-107">Geben Sie im Feld "Plan" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="59693-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="59693-108">Wählen Sie im Feld Plan "Plan 10" aus.</span><span class="sxs-lookup"><span data-stu-id="59693-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="59693-109">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="59693-109">Click Run.</span></span>
4. <span data-ttu-id="59693-110">Geben Sie im Feld "Anzahl von Threads" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="59693-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="59693-111">Dies stellt die Anzahl von parallelen Threads für die Produktprogrammplanung dar.</span><span class="sxs-lookup"><span data-stu-id="59693-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="59693-112">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="59693-112">Click OK.</span></span>
    * <span data-ttu-id="59693-113">Dies kann einige Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="59693-113">This may take a while.</span></span>  
6. <span data-ttu-id="59693-114">Klicken Sie auf "Geplanter Intercompany-Bedarf".</span><span class="sxs-lookup"><span data-stu-id="59693-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="59693-115">Klicken Sie auf "Ausgehender geplanter Intercompany-Bedarf".</span><span class="sxs-lookup"><span data-stu-id="59693-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="59693-116">Diese Seite enthält eine Übersicht des gesamten geplanten Bedarfs, der durch einen internen Lieferkettenkreditor erfüllt wird.</span><span class="sxs-lookup"><span data-stu-id="59693-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="59693-117">Erweitern Sie den Abschnitt "Bedarfsdetails hochstreamen".</span><span class="sxs-lookup"><span data-stu-id="59693-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="59693-118">In diesem Abschnitt finden Sie Details zur Erfüllung des Bedarfs.</span><span class="sxs-lookup"><span data-stu-id="59693-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="59693-119">Möglicherweise müssen Sie auf die im Lieferungsunternehmen auszuführende Produktprogrammplanung warten, bevor Sie hier zusätzliche Informationen sehen.</span><span class="sxs-lookup"><span data-stu-id="59693-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

