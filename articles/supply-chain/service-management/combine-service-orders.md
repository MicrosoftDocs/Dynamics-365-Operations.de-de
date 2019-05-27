---
title: Serviceaufträge kombinieren
description: Sie können Serviceaufträge kombinieren.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b94d81c431a068e891a0e05e996594f7e0be19f9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571956"
---
# <a name="combine-service-orders"></a><span data-ttu-id="2b547-103">Serviceaufträge kombinieren</span><span class="sxs-lookup"><span data-stu-id="2b547-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2b547-104">Beim automatischen Erstellen von Serviceauftragspositionen im Formular **Serviceverträge** können Sie eine der folgenden Optionen wählen, um die Art der Gruppierung anzugeben:</span><span class="sxs-lookup"><span data-stu-id="2b547-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="2b547-105">**Nach Servicevertrag**</span><span class="sxs-lookup"><span data-stu-id="2b547-105">**By service agreement**</span></span>

  - <span data-ttu-id="2b547-106">**Nach Serviceaufgabe**</span><span class="sxs-lookup"><span data-stu-id="2b547-106">**By service task**</span></span>

  - <span data-ttu-id="2b547-107">**Nach Mitarbeiter**</span><span class="sxs-lookup"><span data-stu-id="2b547-107">**By employee**</span></span>

  - <span data-ttu-id="2b547-108">**Nach Serviceobjekt**</span><span class="sxs-lookup"><span data-stu-id="2b547-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="2b547-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2b547-109">Example</span></span>

<span data-ttu-id="2b547-110">Sie erstellen eine Servicevereinbarung mit dem Startdatum 31.03.2007.</span><span class="sxs-lookup"><span data-stu-id="2b547-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="2b547-111">Wählen Sie im Feld **Serviceaufträge kombinieren** **Nach Serviceobjekte** aus.</span><span class="sxs-lookup"><span data-stu-id="2b547-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="2b547-112">Anschließend erstellen Sie die folgenden Servicevertragspositionen:</span><span class="sxs-lookup"><span data-stu-id="2b547-112">You then create the following service agreement lines:</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b547-113">Vereinbarungspositionsnummer</span><span class="sxs-lookup"><span data-stu-id="2b547-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="2b547-114">Buchungsart</span><span class="sxs-lookup"><span data-stu-id="2b547-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="2b547-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b547-115">Description</span></span></p></th>
<th><p><span data-ttu-id="2b547-116">Intervall</span><span class="sxs-lookup"><span data-stu-id="2b547-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="2b547-117">Serviceobjekt</span><span class="sxs-lookup"><span data-stu-id="2b547-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="2b547-118">Eintrittstermin</span><span class="sxs-lookup"><span data-stu-id="2b547-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b547-119">1</span><span class="sxs-lookup"><span data-stu-id="2b547-119">1</span></span></p></td>
<td><p><span data-ttu-id="2b547-120"><strong>Stunde</strong></span><span class="sxs-lookup"><span data-stu-id="2b547-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="2b547-121">SVP1</span><span class="sxs-lookup"><span data-stu-id="2b547-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="2b547-122">Wöchentlich</span><span class="sxs-lookup"><span data-stu-id="2b547-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="2b547-123">X-1</span><span class="sxs-lookup"><span data-stu-id="2b547-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="2b547-124">01.04.2007</span><span class="sxs-lookup"><span data-stu-id="2b547-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b547-125">2</span><span class="sxs-lookup"><span data-stu-id="2b547-125">2</span></span></p></td>
<td><p><span data-ttu-id="2b547-126"><strong>Stunde</strong></span><span class="sxs-lookup"><span data-stu-id="2b547-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="2b547-127">SVP2</span><span class="sxs-lookup"><span data-stu-id="2b547-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="2b547-128">Zweiwöchentlich</span><span class="sxs-lookup"><span data-stu-id="2b547-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="2b547-129">X-2</span><span class="sxs-lookup"><span data-stu-id="2b547-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="2b547-130">01.04.2007</span><span class="sxs-lookup"><span data-stu-id="2b547-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b547-131">3</span><span class="sxs-lookup"><span data-stu-id="2b547-131">3</span></span></p></td>
<td><p><span data-ttu-id="2b547-132"><strong>Stunde</strong></span><span class="sxs-lookup"><span data-stu-id="2b547-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="2b547-133">SVP3</span><span class="sxs-lookup"><span data-stu-id="2b547-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="2b547-134">Wöchentlich</span><span class="sxs-lookup"><span data-stu-id="2b547-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="2b547-135">X-2</span><span class="sxs-lookup"><span data-stu-id="2b547-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="2b547-136">01.04.2007</span><span class="sxs-lookup"><span data-stu-id="2b547-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2b547-137">Sie geben keine Zeitfenster für die Servicevertragspositionen an.</span><span class="sxs-lookup"><span data-stu-id="2b547-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="2b547-138">Daher werden die Serviceauftragspositionen nicht vom berechneten Tag, auf den sie fallen, verschoben.</span><span class="sxs-lookup"><span data-stu-id="2b547-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="2b547-139">Nun erstellen Sie mit dem Formular **Erstellen von Serviceaufträgen** Serviceauftragspositionen vom 01.04.2007 bis zum 30.04.2007.</span><span class="sxs-lookup"><span data-stu-id="2b547-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="2b547-140">Insgesamt werden 10 Serviceaufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="2b547-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="2b547-141">Da Sie **Nach Serviceobjekt** als Einstellung für die Zusammenfassung ausgewählt haben, verfügen alle erstellten Serviceaufträge nur über Serviceauftragspositionen mit einem bestimmten Serviceobjekt.</span><span class="sxs-lookup"><span data-stu-id="2b547-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="2b547-142">Aus der Servicevereinbarung generierte Serviceauftragspositionen mit gleichem Servicedatum und Objekt werden im gleichen Serviceauftrag zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="2b547-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2b547-143">In diesem Beispiel hat der im Formular <STRONG>Serviceverwaltungsparameter</STRONG> angegebene Kalender keine geschlossenen Tage.</span><span class="sxs-lookup"><span data-stu-id="2b547-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="2b547-144">Die weitere Gruppierung von Serviceauftragspositionen in Serviceaufträge erfolgt gemäß den einzelnen Zeitfenstern, die in den Servicevertragspositionen jeweils angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="2b547-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="2b547-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b547-145">See also</span></span>

[<span data-ttu-id="2b547-146">Automatische Erstellung von Serviceaufträgen</span><span class="sxs-lookup"><span data-stu-id="2b547-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  


