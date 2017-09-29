--- 
title: Einen Produktionsauftrag als abgeschlossen melden
description: Diese Prozedur zeigt an, wie ein Produktionsauftrag als abgeschlossen gemeldet wird.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 17b2285e4669f1ad8fa6cea1250693a2a70c7dfa
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="report-a-production-order-as-finished"></a><span data-ttu-id="3a971-103">Einen Produktionsauftrag als abgeschlossen melden</span><span class="sxs-lookup"><span data-stu-id="3a971-103">Report a production order as finished</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3a971-104">Diese Prozedur zeigt an, wie ein Produktionsauftrag als abgeschlossen gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="3a971-104">This procedure shows how to report a production order as finished.</span></span> <span data-ttu-id="3a971-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="3a971-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3a971-106">Dies ist die sechste Prozedur von sieben, die den Produktionsauftrags-Lebenszyklus erklärt.</span><span class="sxs-lookup"><span data-stu-id="3a971-106">This is the sixth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="report-a-production-order-as-finished"></a><span data-ttu-id="3a971-107">Einen Produktionsauftrag als abgeschlossen melden</span><span class="sxs-lookup"><span data-stu-id="3a971-107">Report a production order as finished</span></span>
1. <span data-ttu-id="3a971-108">Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".</span><span class="sxs-lookup"><span data-stu-id="3a971-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="3a971-109">Wählen Sie einen Produktionsauftrag aus, der den Status "Gestartet" aufweist.</span><span class="sxs-lookup"><span data-stu-id="3a971-109">Select a production order that has the Started status.</span></span>  
2. <span data-ttu-id="3a971-110">Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="3a971-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="3a971-111">Klicken Sie auf "Fertigmeldung".</span><span class="sxs-lookup"><span data-stu-id="3a971-111">Click Report as finished.</span></span>
    * <span data-ttu-id="3a971-112">Auf dieser Seite können Sie die Menge der als fertig gestellt zu meldenden Fertigproduktionen bestätigen.</span><span class="sxs-lookup"><span data-stu-id="3a971-112">On this page, you can confirm the quantity of the finished product to be reported as finished.</span></span>  
4. <span data-ttu-id="3a971-113">Klicken Sie auf die Registerkarte "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="3a971-113">Click the General tab.</span></span>
5. <span data-ttu-id="3a971-114">Legen Sie "Gutmenge" auf "18" fest.</span><span class="sxs-lookup"><span data-stu-id="3a971-114">Set Good quantity to '18'.</span></span>
6. <span data-ttu-id="3a971-115">Legen Sie "Ausschussmenge" auf "2" fest.</span><span class="sxs-lookup"><span data-stu-id="3a971-115">Set Error quantity to '2'.</span></span>
7. <span data-ttu-id="3a971-116">Wählen Sie im Feld "Fehlerursache" " Material "aus.</span><span class="sxs-lookup"><span data-stu-id="3a971-116">In the Error cause field, select 'Material'.</span></span>
8. <span data-ttu-id="3a971-117">Aktivieren oder deaktivieren Sie das Kontrollkästchen "Enddurchlauf".</span><span class="sxs-lookup"><span data-stu-id="3a971-117">Select or clear the End job check box.</span></span>
9. <span data-ttu-id="3a971-118">Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Fehler akzeptieren".</span><span class="sxs-lookup"><span data-stu-id="3a971-118">Select or clear the Accept error check box.</span></span>
10. <span data-ttu-id="3a971-119">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3a971-119">Click OK.</span></span>

## <a name="verify-the-report-as-finished-journal"></a><span data-ttu-id="3a971-120">Die Erfassung "Fertigmeldung" überprüfen</span><span class="sxs-lookup"><span data-stu-id="3a971-120">Verify the Report as finished journal</span></span>
1. <span data-ttu-id="3a971-121">Klicken Sie im Aktivitätsbereich auf "Anzeigen".</span><span class="sxs-lookup"><span data-stu-id="3a971-121">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="3a971-122">Klicken Sie auf "Fertigmeldung".</span><span class="sxs-lookup"><span data-stu-id="3a971-122">Click Reported as finished.</span></span>
3. <span data-ttu-id="3a971-123">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="3a971-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="3a971-124">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="3a971-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3a971-125">Die Erfassung "Fertigmeldung" wurde gebucht.</span><span class="sxs-lookup"><span data-stu-id="3a971-125">The Report as finished journal is posted.</span></span> <span data-ttu-id="3a971-126">Wenn Sie Regulierungen in der Erfassung vornehmen möchten, können Sie manuell eine neue Erfassung erstellen, in der Sie Änderungen vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="3a971-126">If you want to make adjustments to the journal, you can manually create  a new journal where you can make changes.</span></span>  


