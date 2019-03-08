---
title: Melden Sie einen nicht kennzeichengesteuerte Lagerplatz als beendet (Anwendung, Mai 2016)
description: Dieser Aufgabenleitfaden zeigt ein Beispiel der Berichterstellung als beendet zu einem Lagerplatz an, der nicht kennzeichengesteuert ist.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4da6868a2184a76c435efe824f4670504e1134e7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "344546"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a><span data-ttu-id="4a223-103">Melden Sie einen nicht kennzeichengesteuerte Lagerplatz als beendet (Anwendung, Mai 2016)</span><span class="sxs-lookup"><span data-stu-id="4a223-103">Report as finished to a non-license plate controlled location  (Application, May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4a223-104">Dieser Aufgabenleitfaden zeigt ein Beispiel der Berichterstellung als beendet zu einem Lagerplatz an, der nicht kennzeichengesteuert ist.</span><span class="sxs-lookup"><span data-stu-id="4a223-104">This task guide shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="4a223-105">Eine anwendbare Arbeitsrichtlinie ist die Voraussetzung für diese Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="4a223-105">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="4a223-106">Ein vorheriger Aufgabenleitfaden zeigte die Einstellungen der Arbeitsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="4a223-106">A previous task guide showed the setup of the work policy.</span></span> <span data-ttu-id="4a223-107">Dieser Aufgabenleitfaden erfordert eine Dynamics AX-Anwendung der Version 7.0.1 oder später.</span><span class="sxs-lookup"><span data-stu-id="4a223-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>




## <a name="set-up-an-output-location"></a><span data-ttu-id="4a223-108">Richten Sie einen Ausgabelagerplatz ein</span><span class="sxs-lookup"><span data-stu-id="4a223-108">Set up an output location</span></span>
1. <span data-ttu-id="4a223-109">Wechseln Sie zu Organisationsverwaltung > Ressourcen > Ressourcengruppen.</span><span class="sxs-lookup"><span data-stu-id="4a223-109">Go to Organization administration > Resources > Resource groups.</span></span>
2. <span data-ttu-id="4a223-110">Wählen Sie in der Liste Ressourcengruppe "5102" aus.</span><span class="sxs-lookup"><span data-stu-id="4a223-110">In the list, select resource group '5102'.</span></span>
3. <span data-ttu-id="4a223-111">Klicken Sie auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="4a223-111">Click Edit.</span></span>
4. <span data-ttu-id="4a223-112">Geben Sie im Feld "Ausgangslagerort" den Wert "51" ein.</span><span class="sxs-lookup"><span data-stu-id="4a223-112">In the Output warehouse field, enter '51'.</span></span>
5. <span data-ttu-id="4a223-113">Geben Sie im Feld "Ausgangslagerplatz" den Wert "001" ein.</span><span class="sxs-lookup"><span data-stu-id="4a223-113">In the Output location field, enter '001'.</span></span>
    * <span data-ttu-id="4a223-114">Lagerplatz 001 ist kein kennzeichengesteuerter Lagerplatz.</span><span class="sxs-lookup"><span data-stu-id="4a223-114">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="4a223-115">Sie können einen Ausgabelagerplatz ohne Kennzeichen nur einrichten, wenn eine anwendbare Arbeitsrichtlinie für den Lagerplatz vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4a223-115">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span>  

## <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="4a223-116">Erstellen Sie einen Produktionsauftrag und melden Sie ihn als abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="4a223-116">Create a production order and report it as finished</span></span>
1. <span data-ttu-id="4a223-117">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4a223-117">Close the page.</span></span>
2. <span data-ttu-id="4a223-118">Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".</span><span class="sxs-lookup"><span data-stu-id="4a223-118">Go to Production control > Production orders > All production orders.</span></span>
3. <span data-ttu-id="4a223-119">Klicken Sie auf "Neuer Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="4a223-119">Click New production order.</span></span>
4. <span data-ttu-id="4a223-120">Geben Sie im Feld "Artikelnummer" den Wert "L0101" ein.</span><span class="sxs-lookup"><span data-stu-id="4a223-120">In the Item number field, enter 'L0101'.</span></span>
5. <span data-ttu-id="4a223-121">Klicken Sie auf Erstellen.</span><span class="sxs-lookup"><span data-stu-id="4a223-121">Click Create.</span></span>
6. <span data-ttu-id="4a223-122">Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="4a223-122">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="4a223-123">Klicken Sie auf "Vorkalkulation".</span><span class="sxs-lookup"><span data-stu-id="4a223-123">Click Estimate.</span></span>
8. <span data-ttu-id="4a223-124">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4a223-124">Click OK.</span></span>
9. <span data-ttu-id="4a223-125">Klicken Sie auf "Start".</span><span class="sxs-lookup"><span data-stu-id="4a223-125">Click Start.</span></span>
10. <span data-ttu-id="4a223-126">Klicken Sie auf die Registerkarte Allgemeines.</span><span class="sxs-lookup"><span data-stu-id="4a223-126">Click the General tab.</span></span>
11. <span data-ttu-id="4a223-127">Wählen Sie im Feld "Stücklistenverbrauch" die Option "Nie" aus.</span><span class="sxs-lookup"><span data-stu-id="4a223-127">In the Automatic BOM consumption field, select 'Never'.</span></span>
12. <span data-ttu-id="4a223-128">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4a223-128">Click OK.</span></span>
13. <span data-ttu-id="4a223-129">Klicken Sie auf Fertigmeldung.</span><span class="sxs-lookup"><span data-stu-id="4a223-129">Click Report as finished.</span></span>
14. <span data-ttu-id="4a223-130">Klicken Sie auf die Registerkarte Allgemeines.</span><span class="sxs-lookup"><span data-stu-id="4a223-130">Click the General tab.</span></span>
15. <span data-ttu-id="4a223-131">Wählen Sie "Ja" im Feld "Fehler akzeptieren" aus.</span><span class="sxs-lookup"><span data-stu-id="4a223-131">Select Yes in the Accept error field.</span></span>
16. <span data-ttu-id="4a223-132">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4a223-132">Click OK.</span></span>
17. <span data-ttu-id="4a223-133">Klicken Sie im Aktivitätsbereich auf "Lagerort".</span><span class="sxs-lookup"><span data-stu-id="4a223-133">On the Action Pane, click Warehouse.</span></span>
18. <span data-ttu-id="4a223-134">Klicken Sie auf "Arbeitsdetails".</span><span class="sxs-lookup"><span data-stu-id="4a223-134">Click Work details.</span></span>
    * <span data-ttu-id="4a223-135">Wenn der Produktionsauftrag als fertig gemeldet wurde, wurde keine Arbeit für die Einlagerung generiert.</span><span class="sxs-lookup"><span data-stu-id="4a223-135">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="4a223-136">Dies tritt auf, weil eine Arbeitsrichtlinie definiert ist, die verhindert, dass Arbeit generiert wird, wenn Produkt L0101 als fertig nach Lagerplatz 001 gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="4a223-136">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span>  

