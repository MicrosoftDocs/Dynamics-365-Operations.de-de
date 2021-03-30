---
title: Einen Produktionsauftrag starten
description: Diese Prozedur zeigt an, wie Sie Produktionsaufträge für die Produktion starten.
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationStartJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3934db907c137f25c39c5769f96f0807eb597e37
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231863"
---
# <a name="start-a-production-order"></a><span data-ttu-id="91b45-103">Einen Produktionsauftrag starten</span><span class="sxs-lookup"><span data-stu-id="91b45-103">Start a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="91b45-104">Diese Prozedur zeigt an, wie Sie Produktionsaufträge für die Produktion starten.</span><span class="sxs-lookup"><span data-stu-id="91b45-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="91b45-105">Zeit und Materialverbrauch werden in diesem Prozess gemeldet.</span><span class="sxs-lookup"><span data-stu-id="91b45-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="91b45-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="91b45-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="91b45-107">Dies ist die fünfte Prozedur von sieben, die den Produktionsauftrags-Lebenszyklus erklärt.</span><span class="sxs-lookup"><span data-stu-id="91b45-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="91b45-108">Einen Produktionsauftrag starten</span><span class="sxs-lookup"><span data-stu-id="91b45-108">Start a production order</span></span>
1. <span data-ttu-id="91b45-109">Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".</span><span class="sxs-lookup"><span data-stu-id="91b45-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="91b45-110">Wählen Sie einen Produktionsauftrag aus, der den Status "Freigegeben" aufweist.</span><span class="sxs-lookup"><span data-stu-id="91b45-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="91b45-111">Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="91b45-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="91b45-112">Klicken Sie auf "Start".</span><span class="sxs-lookup"><span data-stu-id="91b45-112">Click Start.</span></span>
    * <span data-ttu-id="91b45-113">Auf dieser Seite können Sie den Beginn des Produktionsauftrags bestätigen.</span><span class="sxs-lookup"><span data-stu-id="91b45-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="91b45-114">Klicken Sie auf die Registerkarte "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="91b45-114">Click the General tab.</span></span>
5. <span data-ttu-id="91b45-115">Im Feld "Von Arbeitsgangnr."</span><span class="sxs-lookup"><span data-stu-id="91b45-115">In the From Oper.</span></span> <span data-ttu-id="91b45-116">Nr.</span><span class="sxs-lookup"><span data-stu-id="91b45-116">No.</span></span> <span data-ttu-id="91b45-117">geben Sie "10 " ein.</span><span class="sxs-lookup"><span data-stu-id="91b45-117">field, enter '10'.</span></span>
6. <span data-ttu-id="91b45-118">Wählen Sie im Feld "Automatische Arbeitsplanrückmeldung" "Immer" aus.</span><span class="sxs-lookup"><span data-stu-id="91b45-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="91b45-119">Klicken Sie auf das Kontrollkästchen "Arbeitsplanliste jetzt buchen".</span><span class="sxs-lookup"><span data-stu-id="91b45-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="91b45-120">Wählen Sie im Feld "Soll=Istrückmeldung Material" "immer" aus.</span><span class="sxs-lookup"><span data-stu-id="91b45-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="91b45-121">Klicken Sie auf das Kontrollkästchen "Kommissionierliste jetzt buchen".</span><span class="sxs-lookup"><span data-stu-id="91b45-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="91b45-122">Klicken Sie auf das Kontrollkästchen "Kommissionierliste drucken".</span><span class="sxs-lookup"><span data-stu-id="91b45-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="91b45-123">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="91b45-123">Click OK.</span></span>
    * <span data-ttu-id="91b45-124">Dies ist die gedruckte Kommissionierliste, in der die Materialien angezeigt werden, die für den Produktionsauftrag verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="91b45-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="91b45-125">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="91b45-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="91b45-126">Kommissionierliste überprüfen</span><span class="sxs-lookup"><span data-stu-id="91b45-126">Validate the picking list</span></span>
1. <span data-ttu-id="91b45-127">Klicken Sie im Aktivitätsbereich auf "Anzeigen".</span><span class="sxs-lookup"><span data-stu-id="91b45-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="91b45-128">Klicken Sie auf "Kommissionierliste".</span><span class="sxs-lookup"><span data-stu-id="91b45-128">Click Picking list.</span></span>
3. <span data-ttu-id="91b45-129">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="91b45-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="91b45-130">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="91b45-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="91b45-131">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="91b45-131">Click Edit.</span></span>
6. <span data-ttu-id="91b45-132">Geben Sie im Feld "Verbrauch" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="91b45-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="91b45-133">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="91b45-133">Click Post.</span></span>
8. <span data-ttu-id="91b45-134">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="91b45-134">Click OK.</span></span>
    * <span data-ttu-id="91b45-135">In der Kommissionierlistenerfassung werden die Materialien, die für den Produktionsauftrag verbraucht werden, gebucht.</span><span class="sxs-lookup"><span data-stu-id="91b45-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="91b45-136">Bevor Sie die Erfassung buchen, können Sie Anpassungen vornehmen, wenn sich die vorkalkulierte Menge und die tatsächlich verbrauchte Menge von einander unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="91b45-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="91b45-137">Klicken Sie auf die Registerkarte "GridPanel".</span><span class="sxs-lookup"><span data-stu-id="91b45-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="91b45-138">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="91b45-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="91b45-139">Arbeitsplanlistenerfassung überprüfen</span><span class="sxs-lookup"><span data-stu-id="91b45-139">Verify the route card journal</span></span>
1. <span data-ttu-id="91b45-140">Klicken Sie im Aktivitätsbereich auf "Anzeigen".</span><span class="sxs-lookup"><span data-stu-id="91b45-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="91b45-141">Klicken Sie auf Arbeitsplanliste.</span><span class="sxs-lookup"><span data-stu-id="91b45-141">Click Route card.</span></span>
3. <span data-ttu-id="91b45-142">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="91b45-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="91b45-143">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="91b45-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="91b45-144">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="91b45-144">Click Edit.</span></span>
6. <span data-ttu-id="91b45-145">Geben Sie im Feld "Stunden" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="91b45-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="91b45-146">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="91b45-146">Click Post.</span></span>
8. <span data-ttu-id="91b45-147">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="91b45-147">Click OK.</span></span>
    * <span data-ttu-id="91b45-148">In der Arbeitsplanlisten-Erfassung wird die Zeit, die für die Dauer der einzelnen Arbeitsgänge aufgewendet wird, erfasst.</span><span class="sxs-lookup"><span data-stu-id="91b45-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="91b45-149">Gut- und Ausschussmengen können auch gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="91b45-149">Good and error quantity can also be reported.</span></span>  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]