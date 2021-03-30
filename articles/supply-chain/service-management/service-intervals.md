---
title: Serviceintervalle
description: Durch das Servicevereinbarungsintervall wird die Häufigkeit angegeben, mit der bei der automatischen Erstellung von Serviceaufträgen Serviceauftragspositionen für Servicevereinbarungspositionen erstellt werden.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da43f914af75a7f85dc43d3ab1d16abcd82561c1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242984"
---
# <a name="service-intervals"></a><span data-ttu-id="9e4cb-103">Serviceintervalle</span><span class="sxs-lookup"><span data-stu-id="9e4cb-103">Service intervals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e4cb-104">Durch das Servicevereinbarungsintervall wird die Häufigkeit angegeben, mit der bei der automatischen Erstellung von Serviceaufträgen Serviceauftragspositionen für Servicevereinbarungspositionen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-104">The service agreement interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders automatically.</span></span>

<span data-ttu-id="9e4cb-105">Bei der automatischen Erstellung von Serviceaufträgen werden Serviceauftragspositionen ab dem Startdatum der Vereinbarungsposition gemäß dem Intervall erstellt, das für die Servicevereinbarungsposition festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-105">When you create service orders automatically, service order lines are created according to the interval that you have specified for the service agreement line from the start date of the agreement line.</span></span>

<span data-ttu-id="9e4cb-106">Ist im Formular **Intervall** das Feld  einer Servicevereinbarungsposition auf der Seite **Servicevereinbarung** leer, handelt es sich bei der Position um ein einmaliges Ereignis, und die Position wird nicht zur wiederholten Erstellung von Serviceaufträgen verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-106">If the **Interval** field of a service agreement line in the **Service agreements** page is blank, the line is a one-time event, and it is not used to create service orders repeatedly.</span></span>

## <a name="example"></a><span data-ttu-id="9e4cb-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9e4cb-107">Example</span></span>

<span data-ttu-id="9e4cb-108">Dieses Beispiel veranschaulicht, wie sich ein Serviceintervall auf die Servicevertrags- und Serviceauftragspositionen in einem Serviceauftrag auswirkt.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-108">This example illustrates how a service interval will affect service agreement lines and service order lines on a service order.</span></span>

### <a name="create-a-service-agreement"></a><span data-ttu-id="9e4cb-109">Erstellen Sie eine Servicevereinbarung.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-109">Create a service agreement</span></span>

<span data-ttu-id="9e4cb-110">Erstellen Sie zunächst eine Servicevereinbarung und setzen die Option **Serviceaufträge kombinieren** auf **Nach Servicevertrag** fest.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-110">First, you create a service agreement and set the **Combine service orders** option to **By service agreement**.</span></span>

1. <span data-ttu-id="9e4cb-111">**Servicevereinbarungen** anklicken</span><span class="sxs-lookup"><span data-stu-id="9e4cb-111">Click **Service agreements**</span></span>
2. <span data-ttu-id="9e4cb-112">Klicken Sie im **Aktivitätsbereich** auf der Registerkarte **Servicevereinbarung** in der Gruppe **Neu** auf **Servicevereinbarung**, um einen neuen Servicevertrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-112">On the **Action Pane**, on the **Service agreement** tab, in the **New** group, click **Service agreement** to create a new service agreement.</span></span>
3. <span data-ttu-id="9e4cb-113">Geben Sie auf dem Inforegister **Projekt-ID** eine Beschreibung ein, wählen Sie im Feld **Anfangsdatum** ein Projekt aus, und geben Sie ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-113">Enter a description, select a project in the **Project ID** field, and enter a date in the **Start date** field.</span></span>
4. <span data-ttu-id="9e4cb-114">Wählen Sie im Feld **Serviceaufträge kombinieren** **Nach Servicevertrag** aus.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-114">In the **Combine service orders** field, select **By service agreement**.</span></span>

<span data-ttu-id="9e4cb-115">Die folgende Servicevereinbarung wurde erstellt:</span><span class="sxs-lookup"><span data-stu-id="9e4cb-115">You have now created the following service agreement:</span></span>

| <span data-ttu-id="9e4cb-116">Project</span><span class="sxs-lookup"><span data-stu-id="9e4cb-116">Project</span></span>      | <span data-ttu-id="9e4cb-117">Startdatum</span><span class="sxs-lookup"><span data-stu-id="9e4cb-117">Start date</span></span>                                                                         |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9e4cb-118">Ihr Projekt</span><span class="sxs-lookup"><span data-stu-id="9e4cb-118">Your project</span></span> | <span data-ttu-id="9e4cb-119">Das für das Projekt angegebene Datum.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-119">The date you specified for the project.</span></span> <span data-ttu-id="9e4cb-120">In diesem Beispiel wird das aktuelle Datum verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-120">In this example, the current date is used.</span></span> |

### <a name="create-a-service-agreement-line"></a><span data-ttu-id="9e4cb-121">Erstellen einer Servicevertragsposition</span><span class="sxs-lookup"><span data-stu-id="9e4cb-121">Create a service agreement line</span></span>

<span data-ttu-id="9e4cb-122">Erstellen Sie im nächsten Schritt eine Servicevertragsposition mit der Buchungsart  **Stunde**.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-122">Next, you create a service agreement line that has the transaction type **Hour**.</span></span>

<span data-ttu-id="9e4cb-123">Um diesen Teil des Beispiels abzuschließen, muss im Formular **Serviceintervall** ein Serviceintervall mit einer Dauer von 10 Tagen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-123">To complete this part of the example, you must create a service interval of 10 days in the **Service intervals** page.</span></span> 

1. <span data-ttu-id="9e4cb-124">Wählen Sie den soeben erstellten Servicevertrag aus.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-124">Select the service agreement that you just created.</span></span> 
2. <span data-ttu-id="9e4cb-125">Klicken Sie auf dem Inforegister **Zeilen** auf die Schaltfläche **Hinzufügen**, um im unteren Bereich des Formulars **Servicevereinbarung** eine neue Position zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-125">On the **Lines** FastTab, click the **Add** button to create a new line in the lower pane of the **Service agreements** page.</span></span>
3. <span data-ttu-id="9e4cb-126">Wählen Sie im Feld **Transaktionstyp** **Stunde** aus.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-126">In the **Transaction type** field, select **Hour**.</span></span>
4. <span data-ttu-id="9e4cb-127">Wählen Sie im Feld **Arbeitskraft** die Arbeitskraft aus, die den Service erbringt.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-127">In the **Worker** field, select the worker who will deliver the service.</span></span>
5. <span data-ttu-id="9e4cb-128">Wählen Sie im Feld **Serviceinterfall** das Serviceintervall von 10 Tagen aus.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-128">In the **Service interval** field, select the 10 days interval.</span></span>

<span data-ttu-id="9e4cb-129">Sie haben nun eine Servicevertragsposition mit den folgenden Informationen erstellt:</span><span class="sxs-lookup"><span data-stu-id="9e4cb-129">You have now created a service agreement line with the following information:</span></span>

| <span data-ttu-id="9e4cb-130">Buchungsart</span><span class="sxs-lookup"><span data-stu-id="9e4cb-130">Transaction type</span></span> | <span data-ttu-id="9e4cb-131">Eintrittstermin</span><span class="sxs-lookup"><span data-stu-id="9e4cb-131">Start date</span></span>                               | <span data-ttu-id="9e4cb-132">Serviceintervall</span><span class="sxs-lookup"><span data-stu-id="9e4cb-132">Service interval</span></span> |
|------------------|------------------------------------------|------------------|
| <span data-ttu-id="9e4cb-133">Stunde</span><span class="sxs-lookup"><span data-stu-id="9e4cb-133">Hour</span></span>             | <span data-ttu-id="9e4cb-134">Das aktuelle Datum.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-134">The current date.</span></span>                        | <span data-ttu-id="9e4cb-135">Alle 10 Tage</span><span class="sxs-lookup"><span data-stu-id="9e4cb-135">Every 10 days</span></span>    |
| <span data-ttu-id="9e4cb-136">Arbeitskraft</span><span class="sxs-lookup"><span data-stu-id="9e4cb-136">Worker</span></span>           | <span data-ttu-id="9e4cb-137">Die Arbeitskraft, die den Service durchführt.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-137">The worker who will perform the service.</span></span> |                  |

<span data-ttu-id="9e4cb-138">Für die Position wurde kein Zeitfenster angegeben.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-138">There is no time window specified for the line.</span></span> 

### <a name="create-planned-service-orders"></a><span data-ttu-id="9e4cb-139">Erstellen von geplanten Serviceaufträgen</span><span class="sxs-lookup"><span data-stu-id="9e4cb-139">Create planned service orders</span></span>

<span data-ttu-id="9e4cb-140">Sie können nun geplante Serviceaufträge und Serviceauftragspositionen für den kommenden Monat erstellen.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-140">You can now create planned service orders and service order lines for the coming month.</span></span>

1. <span data-ttu-id="9e4cb-141">Klicken Sie auf der Seite **Servicevereinbarung** auf der Registerkarte **Aktivität** in der Gruppe **Bereitstellung** auf **Geplant Servicevereinbarungen**.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-141">In the **Service agreements** page, on the **Action Pane**, on the **Deliver** tab, click **Planned service orders**.</span></span>
2. <span data-ttu-id="9e4cb-142">Geben Sie im Formular **Serviceaufträge erstellen** das aktuelle Datum im Feld **Datum ab** und im Feld **Datum bis** ein Datum an, das einen Monat hinter dem aktuellen Datum liegt.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-142">In the **Create service orders** page, enter the current date in the **From date** field and a date that is one month from the current date in the **To date** field.</span></span>
3. <span data-ttu-id="9e4cb-143">Setzen Sie den Schieberegler **Stunde** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-143">Set the **Hour** slider to **Yes**.</span></span> 
4. <span data-ttu-id="9e4cb-144">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-144">Click **OK**.</span></span>

<span data-ttu-id="9e4cb-145">Da für den Serviceauftrag keine Gruppierung vorhanden ist (definiert unter Option **Nach Servicevereinbarung** im Feld **Serviceaufträge kombinieren**), wird pro Serviceauftrag jeweils eine Serviceauftragsposition erstellt.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-145">Because there is no grouping on the service order (defined by the **By service agreement** option in the **Combine service orders** field), one service order line is created per service order.</span></span>

### <a name="service-orders-created"></a><span data-ttu-id="9e4cb-146">Erstellte Serviceaufträge</span><span class="sxs-lookup"><span data-stu-id="9e4cb-146">Service orders created</span></span>

<span data-ttu-id="9e4cb-147">Drei Serviceauftragspositionen wurden in dem Zeitrahmen erstellt, den Sie im Dialogfeld **Serviceauftrag erstellen** angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-147">Three service order lines have been created within the time frame that you specified in the **Create service orders** dialog box.</span></span> <span data-ttu-id="9e4cb-148">Sie können die Serviceauftragspositionen im Formular **Servicevereinbarungen**  (**Aktivitätsbereich** \> **Lieferung**\>**Ansicht** Schaltfläche ) anzeigen.</span><span class="sxs-lookup"><span data-stu-id="9e4cb-148">You can view the service order lines in the **Service agreements** page (**Action Pane** \> **Deliver** tab \>**View** button).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e4cb-149">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9e4cb-149">Related topics</span></span>

[<span data-ttu-id="9e4cb-150">Einrichten von Serviceintervallen</span><span class="sxs-lookup"><span data-stu-id="9e4cb-150">Set up service intervals</span></span>](set-up-service-intervals.md)  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]