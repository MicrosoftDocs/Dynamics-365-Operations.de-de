---
title: Serviceaufträge kombinieren
description: Sie können Serviceaufträge kombinieren.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7bd3ac8cf3c025b082b33247fcd020aebc010bc8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247717"
---
# <a name="combine-service-orders"></a><span data-ttu-id="93531-103">Serviceaufträge kombinieren</span><span class="sxs-lookup"><span data-stu-id="93531-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="93531-104">Beim automatischen Erstellen von Serviceauftragspositionen im Formular **Serviceverträge** können Sie eine der folgenden Optionen wählen, um die Art der Gruppierung anzugeben:</span><span class="sxs-lookup"><span data-stu-id="93531-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="93531-105">**Nach Servicevertrag**</span><span class="sxs-lookup"><span data-stu-id="93531-105">**By service agreement**</span></span>

  - <span data-ttu-id="93531-106">**Nach Serviceaufgabe**</span><span class="sxs-lookup"><span data-stu-id="93531-106">**By service task**</span></span>

  - <span data-ttu-id="93531-107">**Nach Mitarbeiter**</span><span class="sxs-lookup"><span data-stu-id="93531-107">**By employee**</span></span>

  - <span data-ttu-id="93531-108">**Nach Serviceobjekt**</span><span class="sxs-lookup"><span data-stu-id="93531-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="93531-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="93531-109">Example</span></span>

<span data-ttu-id="93531-110">Sie erstellen eine Servicevereinbarung mit dem Startdatum 31.03.2007.</span><span class="sxs-lookup"><span data-stu-id="93531-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="93531-111">Wählen Sie im Feld **Serviceaufträge kombinieren** **Nach Serviceobjekte** aus.</span><span class="sxs-lookup"><span data-stu-id="93531-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="93531-112">Anschließend erstellen Sie die folgenden Servicevertragspositionen:</span><span class="sxs-lookup"><span data-stu-id="93531-112">You then create the following service agreement lines:</span></span>

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
<th><p><span data-ttu-id="93531-113">Vereinbarungspositionsnummer</span><span class="sxs-lookup"><span data-stu-id="93531-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="93531-114">Buchungsart</span><span class="sxs-lookup"><span data-stu-id="93531-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="93531-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93531-115">Description</span></span></p></th>
<th><p><span data-ttu-id="93531-116">Intervall</span><span class="sxs-lookup"><span data-stu-id="93531-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="93531-117">Serviceobjekt</span><span class="sxs-lookup"><span data-stu-id="93531-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="93531-118">Eintrittstermin</span><span class="sxs-lookup"><span data-stu-id="93531-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93531-119">1</span><span class="sxs-lookup"><span data-stu-id="93531-119">1</span></span></p></td>
<td><p><span data-ttu-id="93531-120"><strong>Stunde</strong></span><span class="sxs-lookup"><span data-stu-id="93531-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="93531-121">SVP1</span><span class="sxs-lookup"><span data-stu-id="93531-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="93531-122">Wöchentlich</span><span class="sxs-lookup"><span data-stu-id="93531-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="93531-123">X-1</span><span class="sxs-lookup"><span data-stu-id="93531-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="93531-124">01.04.2007</span><span class="sxs-lookup"><span data-stu-id="93531-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93531-125">2</span><span class="sxs-lookup"><span data-stu-id="93531-125">2</span></span></p></td>
<td><p><span data-ttu-id="93531-126"><strong>Stunde</strong></span><span class="sxs-lookup"><span data-stu-id="93531-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="93531-127">SVP2</span><span class="sxs-lookup"><span data-stu-id="93531-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="93531-128">Zweiwöchentlich</span><span class="sxs-lookup"><span data-stu-id="93531-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="93531-129">X-2</span><span class="sxs-lookup"><span data-stu-id="93531-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="93531-130">01.04.2007</span><span class="sxs-lookup"><span data-stu-id="93531-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93531-131">3</span><span class="sxs-lookup"><span data-stu-id="93531-131">3</span></span></p></td>
<td><p><span data-ttu-id="93531-132"><strong>Stunde</strong></span><span class="sxs-lookup"><span data-stu-id="93531-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="93531-133">SVP3</span><span class="sxs-lookup"><span data-stu-id="93531-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="93531-134">Wöchentlich</span><span class="sxs-lookup"><span data-stu-id="93531-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="93531-135">X-2</span><span class="sxs-lookup"><span data-stu-id="93531-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="93531-136">01.04.2007</span><span class="sxs-lookup"><span data-stu-id="93531-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93531-137">Sie geben keine Zeitfenster für die Servicevertragspositionen an.</span><span class="sxs-lookup"><span data-stu-id="93531-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="93531-138">Daher werden die Serviceauftragspositionen nicht vom berechneten Tag, auf den sie fallen, verschoben.</span><span class="sxs-lookup"><span data-stu-id="93531-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="93531-139">Nun erstellen Sie mit dem Formular **Erstellen von Serviceaufträgen** Serviceauftragspositionen vom 01.04.2007 bis zum 30.04.2007.</span><span class="sxs-lookup"><span data-stu-id="93531-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="93531-140">Insgesamt werden 10 Serviceaufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="93531-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="93531-141">Da Sie **Nach Serviceobjekt** als Einstellung für die Zusammenfassung ausgewählt haben, verfügen alle erstellten Serviceaufträge nur über Serviceauftragspositionen mit einem bestimmten Serviceobjekt.</span><span class="sxs-lookup"><span data-stu-id="93531-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="93531-142">Aus der Servicevereinbarung generierte Serviceauftragspositionen mit gleichem Servicedatum und Objekt werden im gleichen Serviceauftrag zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="93531-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="93531-143">In diesem Beispiel hat der im Formular <STRONG>Serviceverwaltungsparameter</STRONG> angegebene Kalender keine geschlossenen Tage.</span><span class="sxs-lookup"><span data-stu-id="93531-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="93531-144">Die weitere Gruppierung von Serviceauftragspositionen in Serviceaufträge erfolgt gemäß den einzelnen Zeitfenstern, die in den Servicevertragspositionen jeweils angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="93531-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="93531-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93531-145">See also</span></span>

[<span data-ttu-id="93531-146">Automatische Erstellung von Serviceaufträgen</span><span class="sxs-lookup"><span data-stu-id="93531-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]