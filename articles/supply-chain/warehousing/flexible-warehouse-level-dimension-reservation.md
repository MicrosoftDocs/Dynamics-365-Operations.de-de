---
title: Flexible Reservierungsrichtlinie für Dimensionen auf Lagerortebene
description: In diesem Thema wird die Bestandsreservierungsrichtlinie beschrieben, mit der Unternehmen, die Produkte mit Chargenverfolgung verkaufen und für die Logistik WMS-fähige Vorgänge ausführen, bestimmte Chargen für Debitorenaufträge reservieren können, obwohl die mit den Produkten verknüpfte Reservierungshierarchie die Reservierung bestimmter Chargen nicht zulässt.
author: omulvad
manager: tfehr
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: ec80346126713cc604b00e6ca7f6e8f4c242dc6f
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530304"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="85616-103">Flexible Reservierungsrichtlinie für Dimensionen auf Lagerortebene</span><span class="sxs-lookup"><span data-stu-id="85616-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85616-104">Wenn eine Bestandsreservierungshierarchie vom Typ „Charge unterhalb\[Lagerort\]“mit Produkten verknüpft ist, können Unternehmen, die Produkte mit Chargenverfolgung verkaufen und ihre Logistik als Operationen ausführen, die für das Microsoft Dynamics 365 Warehouse Management System (WMS) aktiviert sind, bestimmte Chargen dieser Produkte nicht für Debitorenaufträge reservieren.</span><span class="sxs-lookup"><span data-stu-id="85616-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span> <span data-ttu-id="85616-105">In diesem Thema wird die Bestandsreservierungsrichtlinie beschrieben, mit der diese Unternehmen bestimmte Chargen reservieren können, auch wenn die Produkte mit einer „Charge unterhalb\[Lagerort\]“-Reservierungshierarchie verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="85616-105">This topic describes the inventory reservation policy that lets these businesses reserve specific batches, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="85616-106">Bestandreservierungshierarchie</span><span class="sxs-lookup"><span data-stu-id="85616-106">Inventory reservation hierarchy</span></span>

<span data-ttu-id="85616-107">In diesem Abschnitt wird die vorhandene Bestandsreservierungshierarchie zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="85616-107">This section summarizes the existing inventory reservation hierarchy.</span></span> <span data-ttu-id="85616-108">Der Schwerpunkt liegt auf der Art und Weise, wie Artikel mit Chargenverfolgung und Seriennummernverfolgung gehandhabt werden.</span><span class="sxs-lookup"><span data-stu-id="85616-108">It focuses on the way that batch-tracked and serial-tracked items are handled.</span></span>

<span data-ttu-id="85616-109">Die Bestandsreservierungshierarchie gibt vor, dass hinsichtlich von Lagerdimensionen, der Bedarfsauftrag die obligatorischen Dimensionen von Standort-, Lager- und Bestandsstatus trägt, während die Lagerlogik für die Zuweisung eines Lagerplatzes für die angeforderten Mengen und das Reservieren des Lagerplatzes zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="85616-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="85616-110">Mit anderen Worten, bei den Interaktionen zwischen dem Bedarfsauftrag und den Lagervorgängen wird erwartet, dass der Bedarfsauftrag angibt, von wo der Auftrag versendet werden muss (d. h., von welchem Standort und von welchem Lagerort).</span><span class="sxs-lookup"><span data-stu-id="85616-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="85616-111">Das Lager verlässt sich dann auf seine Logik, um die erforderliche Menge in den Lagerstätten zu finden.</span><span class="sxs-lookup"><span data-stu-id="85616-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="85616-112">Um jedoch das Betriebsmodell des Unternehmens widerzuspiegeln, unterliegen die Rückverfolgungsangaben (Chargen- und Seriennummern) einer größeren Flexibilität.</span><span class="sxs-lookup"><span data-stu-id="85616-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="85616-113">Eine Bestandsreservierungshierarchie kann Szenarien berücksichtigen, bei denen die folgenden Bedingungen zutreffen:</span><span class="sxs-lookup"><span data-stu-id="85616-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="85616-114">Das Unternehmen verlässt sich auf seine Lagerort-Arbeitsgänge für die Verwaltung der Kommissionierung von Mengen mit Chargen- oder Seriennummern, nachdem die Mengen in einem Lager gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="85616-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="85616-115">Dieses Modell wird häufig als *Charge unterhalb\[Lagerort\]* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="85616-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="85616-116">Es wird normalerweise verwendet, wenn die Chargen- oder Seriennummer eines Produkts für die Debitoren nicht wichtig ist, die eine Nachfrage beim verkaufenden Unternehmen stellen.</span><span class="sxs-lookup"><span data-stu-id="85616-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="85616-117">Wenn Chargen- oder Seriennummern Teil der Auftragsspezifikation eines Debitors sind und im Bedarfsauftrag aufgeführt werden, werden die Lagerortarbeitsgänge, die für die Suche nach den Mengen im Lager eingesetzt werden, durch die angegebenen Nummern eingeschränkt und können diese nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="85616-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="85616-118">Dieses Modell wird häufig als *Charge oberhalb\[Lagerort\]* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="85616-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="85616-119">In diesen Szenarien besteht die Herausforderung darin, dass jedem freigegebenen Produkt nur eine Bestandsreservierungshierarchie zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="85616-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="85616-120">Damit das WMS nachverfolgte Artikel verarbeiten kann, können, nachdem die Hierarchiezuweisung bestimmt, wann die Chargen- oder Seriennummer reserviert werden sollte (entweder wenn der Bedarfsauftrag entgegengenommen wird oder während der Lagerentnahme), diese Zeiten nicht ad-hoc geändert werden.</span><span class="sxs-lookup"><span data-stu-id="85616-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="85616-121">Flexible Reservierung für chargenverfolgte Artikel</span><span class="sxs-lookup"><span data-stu-id="85616-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="85616-122">Geschäftsszenario</span><span class="sxs-lookup"><span data-stu-id="85616-122">Business scenario</span></span>

<span data-ttu-id="85616-123">In diesem Szenario verwendet ein Unternehmen eine Bestandsstrategie, bei der Fertigwaren anhand von Chargennummern verfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="85616-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="85616-124">Diese Firma verwendet auch die WMS-Arbeitsauslastung.</span><span class="sxs-lookup"><span data-stu-id="85616-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="85616-125">Da diese Auslastung eine gut gerüstete Logik für die Planung und Durchführung von Kommissionierungs- und Versandvorgängen für Artikel hat, für die Chargen aktiviert sind, werden die meisten Fertigprodukte mit der Bestandsreservierungshistorie „Charge unterhalb\[Lagerort\]“ verknüpft.</span><span class="sxs-lookup"><span data-stu-id="85616-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="85616-126">Der Vorteil dieser Art des operativen Einrichtung besteht darin, dass Entscheidungen (die im Grunde genommen Reservierungsentscheidungen sind) darüber, welche Chargen kommissioniert werden sollen und wo sie im Lager abgelegt werden sollen, verschoben werden, bis mit der Kommissionierung begonnen wird.</span><span class="sxs-lookup"><span data-stu-id="85616-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="85616-127">Sie werden nicht schon gemacht, wenn der Kunde bestellt.</span><span class="sxs-lookup"><span data-stu-id="85616-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="85616-128">Obwohl die Reservierungshistorie „Charge unterhalb\[Lagerort\]“ den Geschäftszielen des Unternehmens dient, fordern viele der etablierten Unternehmenskunden bei der Nachbestellung die gleiche Charge an, wie beim vorherigen Kauf.</span><span class="sxs-lookup"><span data-stu-id="85616-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="85616-129">Aus diesem Grund ist das Unternehmen bestrebt, die Regeln für die Chargenreservierung flexibel zu gestalten, sodass, je nachdem, ob der Kunde den gleichen Artikel wünscht, die folgenden Verhaltensweisen auftreten:</span><span class="sxs-lookup"><span data-stu-id="85616-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="85616-130">Eine Chargennummer kann aufgezeichnet und reserviert werden, wenn der Auftrag vom Verkäufer entgegengenommen wird. Sie kann während des Lagerortbetriebs nicht geändert werden und/oder aufgrund anderer Bedarfe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85616-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="85616-131">Dieses Verhalten hilft zu gewährleisten, dass die bestellte Chargennummer an den Kunden gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="85616-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="85616-132">Wenn die Chargennummer für den Kunden nicht wichtig ist, kann der Lagerbetrieb während der Kommissionierungsarbeiten eine Chargennummer bestimmen, nachdem die Kundenauftragsregistrierung und -reservierung durchgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="85616-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="85616-133">Reservierung einer bestimmten Charge im Auftrag zulassen</span><span class="sxs-lookup"><span data-stu-id="85616-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="85616-134">Um der gewünschten Flexibilität bei der Chargenreservierung für Artikel, die mit einer „Charge unterhalb\[Lagerort\]“-Bestandsreservierungshistorie verknüpft sind, gerecht zu werden, müssen Bestandsverwalter das Kontrollkästchen für **Reservierung für Bedarfsauftrag zulassen** für die **Chargennummer**-Ebene auf der Seite **Bestandsreservierungshierarchien** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="85616-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Bestandreservierungshierarchie flexibler machen](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="85616-136">Wenn die **Chargennummer**-Ebene in der Hierarchie ausgewählt wird, werden alle Dimensionen über dieser Ebene und bis zur **Lagerort**-Ebene wird automatisch ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="85616-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="85616-137">(Standardmäßig sind alle Dimensionen über der **Lagerort**-Ebene ausgewählt.) Dieses Verhalten spiegelt eine Logik wider, bei der alle Dimensionen im Bereich zwischen Chargennummer und Lagerort automatisch reserviert werden, nachdem Sie eine bestimmte Chargennummer aus der Auftragsposition reserviert haben.</span><span class="sxs-lookup"><span data-stu-id="85616-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="85616-138">Das Kontrollkästchen **Reservierung für Bedarfsauftrag zulassen** gilt nur für die Reservierungshierarchieebenen, die unterhalb der Lagerortdimension liegen.</span><span class="sxs-lookup"><span data-stu-id="85616-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="85616-139">**Chargennummer** ist die einzige Ebene in der Hierarchie, die für die flexible Reservierungsrichtlinie offen ist.</span><span class="sxs-lookup"><span data-stu-id="85616-139">**Batch number** is the only level in the hierarchy that is open for the flexible reservation policy.</span></span> <span data-ttu-id="85616-140">Mit anderen Worten, Sie können das Kontrollkästchen **Reservierung für Bedarfsauftrag zulassen** nicht für die Ebenen **Lagerort**, **Ladungsträger** oder **Seriennummer** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="85616-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location**, **License plate**, or **Serial number** level.</span></span>
>
> <span data-ttu-id="85616-141">Wenn Ihre Reservierungshierarchie die Seriennummerdimension enthält (die immer unterhalb der **Chargennummer**-Ebene liegen muss), und wenn Sie die chargenspezifische Reservierung für die Chargennummer aktiviert haben, wird das System weiterhin die Seriennummernreservierung und die Kommissionierungsvorgänge basierend auf den Regeln durchführen, die für die Reservierungsrichtlinie „Serie unterhalb\[Lagerort\]“ gelten.</span><span class="sxs-lookup"><span data-stu-id="85616-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="85616-142">Sie können jederzeit eine chargenspezifische Reservierung für eine vorhandene „Charge unterhalb\[Lagerort\]“-Reservierungsrichtlinie in Ihrer Bereitstellung zulassen.</span><span class="sxs-lookup"><span data-stu-id="85616-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="85616-143">Diese Änderung wirkt sich nicht auf Reservierungen und offene Lagerarbeiten aus, die vor der Änderung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="85616-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="85616-144">Das Kontrollkästchen \***Reservierung für Bedarfsauftrag zulassen** kann aber nicht deaktiviert werden, wenn Lagerbuchungen vom Abgangstyp **Bestellt reserviert**, **Physisch reserviert** oder **Bestellt** für mindestens einen Artikel vorhanden sind, der mit der Reservierungshistorie verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="85616-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="85616-145">Wenn die vorhandene Reservierungshierarchie eines Artikels keine Chargenspezifikation für den Auftrag zulässt, können Sie ihn einer Reservierungshierarchie zuordnen, die eine Chargenspezifikation zulässt, vorausgesetzt, die Struktur der Hierarchieebene ist in beiden Hierarchien gleich.</span><span class="sxs-lookup"><span data-stu-id="85616-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="85616-146">Verwenden Sie die **Reservierungshierarchie für Artikel ändern**-Funktion, um die Neuzuweisung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="85616-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="85616-147">Diese Änderung ist möglicherweise relevant, wenn Sie die flexible Chargenreservierung für eine Teilmenge von Artikeln mit Chargenverfolgung verhindern möchten, aber für den Rest des Produktportfolios zulassen möchten.</span><span class="sxs-lookup"><span data-stu-id="85616-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="85616-148">Unabhängig davon, ob Sie das Kontrollkästchen **Reservierung für Bedarfsauftrag zulassen** aktiviert haben, wird dennoch die standardmäßige Lagerort-Operationslogik angewendet, die für eine „Charge unterhalb\[Lagerort\]“-Reservierungshierarchie gilt, wenn Sie keine bestimmte Chargennummer für den Artikel in einer Auftragsposition reservieren möchten.</span><span class="sxs-lookup"><span data-stu-id="85616-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="85616-149">Reservieren einer bestimmten Chargennummer für eine Kundenbestellung</span><span class="sxs-lookup"><span data-stu-id="85616-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="85616-150">Nachdem die „Charge unterhalb\[Lagerort\]“-Bestandsreservierungshierarchie eines Artikels mit Chargenverfolgung so eingerichtet ist, dass bestimmte Chargennummern für Aufträge reserviert werden können, können Verarbeiter von Aufträgen, je nach Kundenwunsch, die Kundenaufträge für den gleichen Artikel auf eine der folgenden Arten aufnehmen:</span><span class="sxs-lookup"><span data-stu-id="85616-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="85616-151">**Auftragsdetails ohne Angabe einer Chargennummer eingeben** – Dieser Ansatz sollte verwendet werden, wenn die Chargenspezifikation des Produkts für den Kunden nicht wichtig ist.</span><span class="sxs-lookup"><span data-stu-id="85616-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="85616-152">Alle bestehenden Prozesse, die mit der Abwicklung eines Auftrags dieser Art verbunden sind, bleiben im System unverändert.</span><span class="sxs-lookup"><span data-stu-id="85616-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="85616-153">Es sind keine zusätzlichen Überlegungen seitens der Benutzer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="85616-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="85616-154">**Bestelldetails eingeben und eine bestimmte Chargennummer reservieren** – Dieser Ansatz sollte verwendet werden, wenn der Kunde eine bestimmte Charge anfordert.</span><span class="sxs-lookup"><span data-stu-id="85616-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="85616-155">In der Regel fordern Kunden eine bestimmte Charge an, wenn sie ein zuvor erworbenes Produkt erneut bestellen.</span><span class="sxs-lookup"><span data-stu-id="85616-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="85616-156">Diese Art der chargenspezifischen Reservierung wird als *auftragsgebundene Reservierung* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="85616-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="85616-157">Die folgenden Regeln gelten, wenn Mengen verarbeitet werden und eine Chargennummer für eine bestimmte Bestellung vorgegeben ist:</span><span class="sxs-lookup"><span data-stu-id="85616-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="85616-158">Um die Reservierung einer bestimmten Chargennummer für einen Artikel zuzulassen, für den die Reservierungsrichtlinie „Charge unterhalb\[Lagerort\]“ gilt, muss das System alle Dimensionen bis zum Lagerort reservieren.</span><span class="sxs-lookup"><span data-stu-id="85616-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="85616-159">Dieser Bereich umfasst normalerweise die Ladungsträgerdimension.</span><span class="sxs-lookup"><span data-stu-id="85616-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="85616-160">Lagerplatzrichtlinien werden nicht verwendet, wenn Kommissionierungsarbeiten für eine Verkaufsposition angelegt werden, die die auftragsgebundene Chargenreservierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="85616-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="85616-161">Während der Verarbeitung von Lagerarbeit für auftragsgebundene Chargen dürfen weder der Benutzer noch das System die Chargennummer ändern.</span><span class="sxs-lookup"><span data-stu-id="85616-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="85616-162">(Diese Verarbeitung umfasst auch die Ausnahmebehandlung.)</span><span class="sxs-lookup"><span data-stu-id="85616-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="85616-163">Das folgende Beispiel zeigt den vollständigen Ablauf.</span><span class="sxs-lookup"><span data-stu-id="85616-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="85616-164">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="85616-164">Example scenario</span></span>

<span data-ttu-id="85616-165">Für dieses Beispielmüssen Demodaten eingerichtet werden, und Sie müssen das **USMF**-Demodatunternehmen verwenden.</span><span class="sxs-lookup"><span data-stu-id="85616-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><span data-ttu-id="85616-166">Einrichten einer Bestandsreservierungshierarchie, um eine chargenspezifische Reservierung zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="85616-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="85616-167">Gehen Sie zu **Lagerortverwaltung** \> **Einrichten** \> **Bestand \> Reservierungshierarchie**.</span><span class="sxs-lookup"><span data-stu-id="85616-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="85616-168">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="85616-168">Select **New**.</span></span>
3. <span data-ttu-id="85616-169">Geben Sie im Feld **Name** einen Namen ein (beispielsweise **BatchFlex**).</span><span class="sxs-lookup"><span data-stu-id="85616-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="85616-170">Geben Sie im Feld **Beschreibung** eine Beschreibung ein (beispielsweise **Charge unterhalb flexibel**).</span><span class="sxs-lookup"><span data-stu-id="85616-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="85616-171">Wählen Sie im Feld **Ausgewählt** **Seriennummer** und **Besitzer** aus und wählen Sie dann die linke Pfeiltaste, um sie zum Feld **Verfügbar** zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="85616-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="85616-172">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="85616-172">Select **OK**.</span></span>
7. <span data-ttu-id="85616-173">In der Zeile mit der **Chargennummer**-Dimensionsebene aktivieren Sie das Kontrollkästchen **Reservierung für Bedarfsauftrag zulassen**.</span><span class="sxs-lookup"><span data-stu-id="85616-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="85616-174">Die Ebenen **Ladungsträger** und **Lagerort** werden automatisch ausgewählt und Sie können die Kontrollkästchen für diese nicht deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="85616-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="85616-175">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="85616-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="85616-176">Neues freigegebenes Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="85616-176">Create a new released product</span></span>

1. <span data-ttu-id="85616-177">Stellen Sie die drei Stammdatenparameter des Produkts mit diesen Werten ein:</span><span class="sxs-lookup"><span data-stu-id="85616-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="85616-178">Wählen Sie im Feld **Lagerdimensionsgruppe** **Ware** aus.</span><span class="sxs-lookup"><span data-stu-id="85616-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="85616-179">Wählen Sie im Feld **Rückverfolgungsgruppe** **Batch-Phy** aus.</span><span class="sxs-lookup"><span data-stu-id="85616-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="85616-180">Wählen Sie im Feld **Reservierungshierarchie** **BatchFlex** aus.</span><span class="sxs-lookup"><span data-stu-id="85616-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="85616-181">Erstellen Sie zwei Chargennummern, beispielsweise **B11** und **B22**.</span><span class="sxs-lookup"><span data-stu-id="85616-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="85616-182">Fügen Sie unter Verwendung der folgenden Werte Artikelmengen zum verfügbaren Bestand hinzu.</span><span class="sxs-lookup"><span data-stu-id="85616-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="85616-183">Lagerort</span><span class="sxs-lookup"><span data-stu-id="85616-183">Warehouse</span></span> | <span data-ttu-id="85616-184">Chargennummer</span><span class="sxs-lookup"><span data-stu-id="85616-184">Batch number</span></span> | <span data-ttu-id="85616-185">Elektronische Adresse</span><span class="sxs-lookup"><span data-stu-id="85616-185">Location</span></span> | <span data-ttu-id="85616-186">Ladungsträger</span><span class="sxs-lookup"><span data-stu-id="85616-186">License plate</span></span> | <span data-ttu-id="85616-187">Leistung</span><span class="sxs-lookup"><span data-stu-id="85616-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="85616-188">24</span><span class="sxs-lookup"><span data-stu-id="85616-188">24</span></span>        | <span data-ttu-id="85616-189">B11</span><span class="sxs-lookup"><span data-stu-id="85616-189">B11</span></span>          | <span data-ttu-id="85616-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="85616-190">BULK-001</span></span> | <span data-ttu-id="85616-191">Nichts</span><span class="sxs-lookup"><span data-stu-id="85616-191">None</span></span>          | <span data-ttu-id="85616-192">10</span><span class="sxs-lookup"><span data-stu-id="85616-192">10</span></span>       |
    | <span data-ttu-id="85616-193">24</span><span class="sxs-lookup"><span data-stu-id="85616-193">24</span></span>        | <span data-ttu-id="85616-194">B11</span><span class="sxs-lookup"><span data-stu-id="85616-194">B11</span></span>          | <span data-ttu-id="85616-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="85616-195">FL-001</span></span>   | <span data-ttu-id="85616-196">LP11</span><span class="sxs-lookup"><span data-stu-id="85616-196">LP11</span></span>          | <span data-ttu-id="85616-197">10</span><span class="sxs-lookup"><span data-stu-id="85616-197">10</span></span>       |
    | <span data-ttu-id="85616-198">24</span><span class="sxs-lookup"><span data-stu-id="85616-198">24</span></span>        | <span data-ttu-id="85616-199">B22</span><span class="sxs-lookup"><span data-stu-id="85616-199">B22</span></span>          | <span data-ttu-id="85616-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="85616-200">FL-002</span></span>   | <span data-ttu-id="85616-201">LP22</span><span class="sxs-lookup"><span data-stu-id="85616-201">LP22</span></span>          | <span data-ttu-id="85616-202">10</span><span class="sxs-lookup"><span data-stu-id="85616-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><span data-ttu-id="85616-203">Auftragsdetails eingeben</span><span class="sxs-lookup"><span data-stu-id="85616-203">Enter sales order details</span></span>

1. <span data-ttu-id="85616-204">Wechseln Sie zu **Vertrieb und Marketing** \> **Aufträge** \> **Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="85616-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="85616-205">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="85616-205">Select **New**.</span></span>
3. <span data-ttu-id="85616-206">Geben Sie im Auftragskopf im Feld **Debitorenkonto** **US-003** ein.</span><span class="sxs-lookup"><span data-stu-id="85616-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="85616-207">Fügen Sie eine Position für den neuen Artikel hinzu und geben Sie als Menge **10** ein.</span><span class="sxs-lookup"><span data-stu-id="85616-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="85616-208">Stellen Sie sicher, dass das Feld **Lagerort** auf **24** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="85616-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="85616-209">Wählen Sie im Inforegister **Auftragspositionen** **Bestand**und dann in der Gruppe **Verwalten** **Chargenreservierung** aus.</span><span class="sxs-lookup"><span data-stu-id="85616-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="85616-210">Die Seite **Chargenreservierung** zeigt eine Liste der Chargen, die für die Reservierung für die Bestellposition verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="85616-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="85616-211">In diesem Beispiel wird eine Menge von **20** für die Chargennummer **B11** und eine Menge von **10** für die Chargennummer **B22** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="85616-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="85616-212">Beachten Sie, dass auf die Seite **Chargenreservierung** nicht von einer Position aus zugegriffen werden kann, wenn der Artikel in dieser Position mit einer „Charge unterhalb\[Lagerort\]“-Reservierungshierarchie verknüpft ist, es sei denn, diese ist so eingerichtet, dass chargenspezifische Reservierungen möglich sind.</span><span class="sxs-lookup"><span data-stu-id="85616-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="85616-213">Um eine bestimmte Charge für einen Auftrag zu reservieren, müssen Sie die Seite **Chargenreservierung** verwenden.</span><span class="sxs-lookup"><span data-stu-id="85616-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="85616-214">Wenn Sie die Chargennummer direkt in die Auftragsposition eingeben, verhält sich das System so, als hätten Sie einen bestimmten Chargenwert für einen Artikel eingegeben, für den die „Charge unterhalb\[Lagerort\]“-Reservierungsrichtlinie gilt.</span><span class="sxs-lookup"><span data-stu-id="85616-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="85616-215">Wenn Sie die Position speichern, erhalten Sie eine Warnmeldung.</span><span class="sxs-lookup"><span data-stu-id="85616-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="85616-216">Wenn Sie bestätigen, dass die Chargennummer direkt in der Bestellposition angegeben werden soll, wird die Position nicht von der normalen Lagerortverwaltungslogik verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="85616-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="85616-217">Wenn Sie die Menge über die Seite **Reservierung** reservieren, wird keine bestimmte Charge reserviert und die Ausführung der Lagerortoperationen für die Position folgt den Regeln, die im Rahmen der Reservierungsrichtlinie „Charge unterhalb\[Lagerort\]“ gelten.</span><span class="sxs-lookup"><span data-stu-id="85616-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="85616-218">Im Allgemeinen funktioniert und interagiert diese Seite genauso wie sie bei Artikeln funktioniert und interagiert, die mit einer Reservierungshierarchie vom Typ „Charge oberhalb\[Lagerort\]“ verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="85616-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="85616-219">Es gelten jedoch folgende Ausnahmen:</span><span class="sxs-lookup"><span data-stu-id="85616-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="85616-220">Das Inforegister **Chargennummern für Quellposition zugesagt** zeigt die Chargennummern an, die für die Bestellposition reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="85616-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="85616-221">Die Chargenwerte im Raster werden während des gesamten Erfüllungszyklus der Auftragsposition angezeigt, einschließlich der Phasen der Lagerortverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="85616-221">The batch values in the grid will be shown throughout the fulfillment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="85616-222">Im Gegensatz dazu werden auf dem Inforegister **Übersicht** regelmäßige Auftragspositionsreservierungen (also Reservierungen für die Dimensionen oberhalb der **Lagerort**-Ebene) im Raster bis zu dem Punkt angezeigt, wenn Lagerarbeiten generiert werden.</span><span class="sxs-lookup"><span data-stu-id="85616-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="85616-223">Die Arbeitsentität übernimmt dann die Positionsreservierung und die Positionsreservierung erscheint nicht mehr auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="85616-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="85616-224">Das Inforegister **Chargennummern für Quellposition zugesagt** sorgt mit dafür, dass der Auftragsverarbeiter die Chargennummern, die für den Kundenauftrag zugesagt wurden, während des gesamten Lebenszyklus bis hin zur Rechnungsstellung anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="85616-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="85616-225">Zusätzlich zur Reservierung einer bestimmten Charge kann ein Benutzer den spezifischen Lagerort und Ladungsträger manuell auswählen und auf die automatische Auswahl durch das System verzichten.</span><span class="sxs-lookup"><span data-stu-id="85616-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="85616-226">Diese Funktion hängt mit dem Design des auftragsgebunden Chargenreservierungsmechanismus zusammen.</span><span class="sxs-lookup"><span data-stu-id="85616-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="85616-227">Wie bereits erwähnt: Wenn eine Chargenummer für einen Artikel reserviert ist, für den die Reservierungsrichtlinie „Charge unterhalb\[Lagerort\]“ gilt, muss das System alle Dimensionen bis zum Lagerort reservieren.</span><span class="sxs-lookup"><span data-stu-id="85616-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="85616-228">Aus diesem Grund gelten für die Lagerarbeit die gleichen Lagerdimensionen, die von den Benutzern reserviert wurden, die diese Aufträge bearbeitet haben. Sie zeigt möglicherweise nicht immer die Artikellagerplatzierung, die für Kommissionierungsarbeiten zweckmäßig oder möglich ist.</span><span class="sxs-lookup"><span data-stu-id="85616-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="85616-229">Wenn Auftragsbearbeiter die Einschränkungen des Lagerorts kennen, möchten sie möglicherweise die spezifischen Lagerorte und Ladungsträger manuell auswählen, wenn sie eine Charge reservieren.</span><span class="sxs-lookup"><span data-stu-id="85616-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="85616-230">In diesem Fall muss der Benutzer die **Dimensionen anzeigen**-Funktionalität auf dem Seitenkopf nutzen und den Lagerort und den Ladungsträger zum Raster im Inforegister **Übersicht** hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="85616-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="85616-231">Auf der Seite **Chargenreservierung** wählen Sie die Position für Charge **B11** sowie **Position reservieren** aus.</span><span class="sxs-lookup"><span data-stu-id="85616-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="85616-232">Es gibt keine festgelegte Logik zum Zuweisen von Lagerorten und Ladungsträgern während der automatischen Reservierung.</span><span class="sxs-lookup"><span data-stu-id="85616-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="85616-233">Sie können die Menge manuell in das Feld **Reservierung** eingeben.</span><span class="sxs-lookup"><span data-stu-id="85616-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="85616-234">Beachten Sie, dass auf dem Inforegister **Chargennummern für Quellposition zugesagt** die Charge **B11** als **Zugesagt** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="85616-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Festlegen einer bestimmten Chargennummer für eine Auftragsposition auf der Seite „Chargenreservierung“](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="85616-236">Die Reservierung der Menge auf einer Auftragsposition kann über mehrere Chargen hinweg erfolgen.</span><span class="sxs-lookup"><span data-stu-id="85616-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="85616-237">Ebenso kann die Reservierung der gleichen Charge für mehrere Lagerorte und Ladungsträger erfolgen (sofern Ladungsträger für die Lagerorte aktiviert sind).</span><span class="sxs-lookup"><span data-stu-id="85616-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="85616-238">Die Reservierung einer bestimmten Charge in der Menge auf einer Auftragsposition kann auch teilweise erfolgen.</span><span class="sxs-lookup"><span data-stu-id="85616-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="85616-239">Beispielsweise kann eine Gesamtmenge von 100 Einheiten reserviert werden, sodass eine bestimmte Charge 20 Einheiten enthalten muss. Für die restlichen 80 Einheiten werden verfügbare Chargen auf Standort- und Lagerortebene reserviert.</span><span class="sxs-lookup"><span data-stu-id="85616-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="85616-240">In diesem Fall übernimmt das WMS die Kommissionierung mittels zweier separater Arbeitspositionen.</span><span class="sxs-lookup"><span data-stu-id="85616-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="85616-241">Wechseln Sie zu **Produktinformationsverwaltung** \> **Produkte** \> **Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="85616-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="85616-242">Wählen Sie Ihren Artikel und dann **Lagerbestand verwalten** \> **Ansicht** \> **Transaktionen** aus.</span><span class="sxs-lookup"><span data-stu-id="85616-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Auftragsgebundene Reservierung als Lagerbuchungstyp](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="85616-244">Überprüfen Sie die Lagerbuchungen, die mit der Reservierung der Auftragsposition verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="85616-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="85616-245">Eine Transaktion, bei der das Feld **Referenz** auf **Auftrag** gesetzt ist und das Feld **Abgang** auf **Physisch reserviert**, stellt die Auftragspositionsreservierung für Bestandsdimensionen oberhalb der Ebene **Lagerort** dar.</span><span class="sxs-lookup"><span data-stu-id="85616-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="85616-246">Entsprechend der Bestandsreservierungshierarchie des Artikels sind diese Dimensionen Standort, Lagerort und Bestandsstatus.</span><span class="sxs-lookup"><span data-stu-id="85616-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="85616-247">Eine Transaktion, bei der das Feld **Referenz** auf **Auftragsgebundene Reservierung** und das Feld **Abgang** auf **Physisch reserviert** gesetzt ist, stellt die Auftragspositionsreservierung für die spezifische Charge und alle Bestandsdimensionen darüber dar.</span><span class="sxs-lookup"><span data-stu-id="85616-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="85616-248">Entsprechend der Bestandsreservierungshierarchie des Artikels sind diese Dimensionen Chargenummer und Lagerort.</span><span class="sxs-lookup"><span data-stu-id="85616-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="85616-249">In diesem Beispiel ist der Lagerort **Bulk-001**.</span><span class="sxs-lookup"><span data-stu-id="85616-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="85616-250">Wählen Sie im Auftragskopf **Lagerort** \> **Aktionen** \> **Für Lagerort freigeben** aus.</span><span class="sxs-lookup"><span data-stu-id="85616-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="85616-251">Die Bestellposition ist jetzt gewellt und eine Ladung sowie Arbeit werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="85616-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="85616-252">Überprüfen und Verarbeiten von Lagerarbeit mit auftragsgebundenen Chargennummern</span><span class="sxs-lookup"><span data-stu-id="85616-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="85616-253">Wählen Sie auf dem Inforegister **Auftragspositionen** **Lagerort** \> **Arbeitsdetails** aus.</span><span class="sxs-lookup"><span data-stu-id="85616-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="85616-254">Die Arbeit, die den Kommissionierungsvorgang für Chargenmengen erledigt, die für die Kundenauftragsposition zugesagt sind, weist folgende Merkmale auf:</span><span class="sxs-lookup"><span data-stu-id="85616-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="85616-255">Das System verwendet Arbeitsvorlagen, jedoch keine Lagerplatzrichtlinien, um Arbeit zu generieren.</span><span class="sxs-lookup"><span data-stu-id="85616-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="85616-256">Alle Standardeinstellungen, die für Arbeitsvorlagen definiert sind, z. B. eine maximale Anzahl von Entnahmepositionen oder eine bestimmte Maßeinheit, werden angewendet, um festzulegen, wann neue Arbeit angelegt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="85616-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="85616-257">Die Regeln, die mit Lagerplatzrichtlinien zum Identifizieren von Entnahmepositionen verknüpft sind, werden nicht berücksichtigt, da die auftragsgebundene Reservierung bereits alle Bestandsdimensionen angibt.</span><span class="sxs-lookup"><span data-stu-id="85616-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="85616-258">Diese Bestandsdimensionen enthalten Dimensionen auf Lagerortebene.</span><span class="sxs-lookup"><span data-stu-id="85616-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="85616-259">Daher erbt die Arbeit diese Dimensionen, ohne dass Lagerplatzrichtlinien berücksichtigt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="85616-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="85616-260">Die Chargennummer wird nicht an der Entnahmeposition angezeigt (im Gegensatz zur Arbeitsposition, die für einen Artikel mit verknüpfter „Charge oberhalb\[Lagerort\]“-Reservierungshierarchie erstellt wird.) Stattdessen werden die von-Chargennummer und alle anderen Lagerdimensionen in der Lagerbuchung der Arbeitsposition angezeigt, auf die von den verknüpften Lagerbuchungen verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="85616-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Lagerort-Lagerbuchungen für Arbeit, die aus einer auftragsgebundenen Reservierung stammt](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="85616-262">Nachdem die Arbeit erstellt wurde, wird die Lagerbuchung, bei der das Feld **Referenz** auf **Auftragsgebundene Reservierung** gesetzt ist, entfernt.</span><span class="sxs-lookup"><span data-stu-id="85616-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="85616-263">Die Lagerbuchung, bei das Feld **Referenz** auf **Arbeit** gesetzt ist, enthält nun die physische Reservierung für alle Lagerdimensionen der Menge.</span><span class="sxs-lookup"><span data-stu-id="85616-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="85616-264">Arbeitsgänge am Arbeitsort können auf die übliche Art und Weise abgewickelt werden.</span><span class="sxs-lookup"><span data-stu-id="85616-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="85616-265">Die Anweisungen auf dem Mobilgerät weisen die Arbeitskraft jedoch an, eine bestimmte Chargennummer auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="85616-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="85616-266">In Lagerortumgebungen, bei denen Lagerorte durch Ladungsträger gesteuert werden, kann eine Arbeitskraft, nachdem sie den Lagerort erreicht hat, der die gleiche Charge auf mehreren Ladungsträgern lagert, von einem beliebigen Ladungsträger entnehmen, der nicht bereits reserviert ist (beispielsweise von einer anderen auftragsgebundenen Reservierung oder einer Arbeit, die von einer Reservierung diesen Typs stammt).</span><span class="sxs-lookup"><span data-stu-id="85616-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="85616-267">Wenn es sich als unpraktisch herausstellt, von dem Lagerort zu entnehmen, der in der Arbeitsposition angegeben ist, kann der Lagerortoperator eine der folgenden Aktionen verwenden, um die Kommissionierung der bestimmten Charge zu einem passenderen Lagerort umleiten.</span><span class="sxs-lookup"><span data-stu-id="85616-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="85616-268">Der Standardaktion **Lagerplatzüberschreibung** auf einem mobilen Gerät (vorausgesetzt, die Lagerort-Arbeitskräfte-Einstellung **Außerkraftsetzen des Entnahmeorts zulassen** ist aktiviert)</span><span class="sxs-lookup"><span data-stu-id="85616-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="85616-269">Die Aktion **Lagerplatz ändern** auf der Seite **Arbeitslistendetails**.</span><span class="sxs-lookup"><span data-stu-id="85616-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="85616-270">Beenden Sie auf dem mobilen Gerät die Kommissionierung und Platzierung der Arbeit.</span><span class="sxs-lookup"><span data-stu-id="85616-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="85616-271">Die Menge von **10** für Chargennummer **B11** wird nun für die Auftragsposition und im Lagerort **Baydoor** platziert.</span><span class="sxs-lookup"><span data-stu-id="85616-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="85616-272">Zu diesem Zeitpunkt kann es auf den LKW verladen und an die Adresse des Kunden versendet werden.</span><span class="sxs-lookup"><span data-stu-id="85616-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="85616-273">Ausnahmenbehandlung von Lagerortarbeit mit auftragsgebundenen Chargennummern</span><span class="sxs-lookup"><span data-stu-id="85616-273">Exception handling of warehouse work that has order-committed batch numbers</span></span>

<span data-ttu-id="85616-274">Die Lagerarbeit für die Kommissionierung von auftragsgebundenen Chargennummern unterliegt denselben standardmäßigen Lagerortausnahmebehandlungen und -Aktionen wie die reguläre Arbeit.</span><span class="sxs-lookup"><span data-stu-id="85616-274">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="85616-275">Im Allgemeinen kann die offene Arbeit oder Arbeitsposition storniert werden. Sie kann unterbrochen werden, weil ein Lagerort voll ist, sie kann kurz entnommen werden und sie kann aufgrund einer Bewegung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="85616-275">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="85616-276">Ebenso kann die kommissionierte Arbeit, die bereits erledigt wurde, reduziert oder rückgängig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="85616-276">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="85616-277">Für alle diese Ausnahmebehandlungsaktionen gilt die folgende Grundregel: Die für den Kunden reservierte Chargennummer kann niemals durch eine andere Chargennummer ersetzt werden, ihre Lagerdimensionen (Lagerort und Ladungsträger) können jedoch durch eine manuelle Aktualisierung seitens des Benutzers geändert werden oder durch eine automatische Aktualisierung seitens des Systems.</span><span class="sxs-lookup"><span data-stu-id="85616-277">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="85616-278">Die automatische Aktualisierung basiert auf der gleichen zufälligen Zuweisung von Lagerdimensionen, die galten, als eine bestimmte Charge automatisch reserviert wurde, aber keine Lagerdimensionen angegeben waren.</span><span class="sxs-lookup"><span data-stu-id="85616-278">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="85616-279">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="85616-279">Example scenario</span></span>

<span data-ttu-id="85616-280">Ein Beispiel für dieses Szenario ist eine Situation, in der zuvor abgeschlossene Arbeiten teilweise rückgängig gemacht wird, indem die Funktion **Entnommene Menge reduzieren** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="85616-280">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="85616-281">Bei diesem Beispiel wird das vorherige Bespiel dieses Themas fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="85616-281">This example continues the previous example in this topic.</span></span>

1. <span data-ttu-id="85616-282">Gehen Sie zu **Lagerortverwaltung** \> **Ladungen** \> **Aktive**.</span><span class="sxs-lookup"><span data-stu-id="85616-282">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="85616-283">Wählen Sie die Ladung aus, die im Zusammenhang mit dem Versand Ihres Auftrags erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="85616-283">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="85616-284">Wählen Sie auf dem Inforegister für **Auftragspositionen laden** die Option **Entnommene Menge reduzieren** aus.</span><span class="sxs-lookup"><span data-stu-id="85616-284">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="85616-285">Wählen Sie auf der Seite **Entnommene Menge reduzieren** im Feld **An Lagerplatz verschieben** **FL-001** aus.</span><span class="sxs-lookup"><span data-stu-id="85616-285">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="85616-286">Wählen Sie im Feld **Auf Ladungsträger verschieben** **LP33** aus.</span><span class="sxs-lookup"><span data-stu-id="85616-286">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="85616-287">Geben Sie im Raster des Felds **Bestandsmenge, deren Entnahme rückgängig gemacht werden soll** **10** ein.</span><span class="sxs-lookup"><span data-stu-id="85616-287">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="85616-288">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="85616-288">Select **OK**.</span></span>

<span data-ttu-id="85616-289">Hier sind die Ergebnisse der Entnahme-Aktion:</span><span class="sxs-lookup"><span data-stu-id="85616-289">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="85616-290">Der Status der zuvor abgeschlossenen Arbeit wird auf **Storniert** gesetzt.</span><span class="sxs-lookup"><span data-stu-id="85616-290">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="85616-291">Neue Arbeit vom Typ **Lagerumlagerung** wird für die nicht entnommene Menge von **10** für die Chargennummer **B11** erstellt.</span><span class="sxs-lookup"><span data-stu-id="85616-291">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="85616-292">Diese Arbeit repräsentiert die Verschiebung vom Lagerort **Baydoor** zum Ladungsträger **LP33** im Lagerort **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="85616-292">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="85616-293">Der Status wird auf **Abgeschlossen** gesetzt.</span><span class="sxs-lookup"><span data-stu-id="85616-293">The status is set to **Closed**.</span></span>
- <span data-ttu-id="85616-294">Das System reserviert die ursprünglich bestellte Chargennummer erneut und weist die IDs des Lagerorts und des Ladungsträgers zu.</span><span class="sxs-lookup"><span data-stu-id="85616-294">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="85616-295">(Dieser Vorgang entspricht dem Ausführen der Funktion **Position reservieren** für die Bestellposition einer bestimmten Chargennummer).</span><span class="sxs-lookup"><span data-stu-id="85616-295">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="85616-296">Als Ergebnis wird Charge **B11** nun als „Zugesagt“ auf dem Inforegister für **Chargennummern für Quellposition zugesagt** der Seite **Chargenreservierung** angezeigt und das Feld **Reservierung** enthält eine Menge von **10** für die Chargennummer **B11**.</span><span class="sxs-lookup"><span data-stu-id="85616-296">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="85616-297">Zusätzlich wird das Feld **Lagerort** auf **FL-001** gesetzt und das Feld **Ladungsträger** auf **LP11**.</span><span class="sxs-lookup"><span data-stu-id="85616-297">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="85616-298">(Sie können diese Felder zum Raster hinzufügen, wenn sie nicht sichtbar sind.)</span><span class="sxs-lookup"><span data-stu-id="85616-298">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="85616-299">Die folgenden Tabellen bieten eine Übersicht darüber, wie das System die auftragsgebundene Chargenreservierung für bestimmte Lagerortaktionen handhabt.</span><span class="sxs-lookup"><span data-stu-id="85616-299">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="85616-300">Um den Inhalt in den Tabellen zu interpretieren, nehmen Sie an, dass jede Lagerortaktion im Kontext einer vorhandenen Lagerarbeit ausgeführt wird, die aus einer auftragsgebundenen Chargenreservierung stammt, oder dass sich die Ausführung jeder Lageraktion auf eine Arbeit dieses Typs auswirkt.</span><span class="sxs-lookup"><span data-stu-id="85616-300">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="85616-301">In diesen Tabellen gibt die Spalte „Chargenmenge verfügbar“ an, ob eine Chargenmenge zusätzlich zu der Menge verfügbar ist, die entweder bereits für die aktuellen auftragsgebundenen Reservierungen reserviert ist oder die bereits von der Lagerarbeit reserviert wurde, die aus Reservierungen dieser Art stammt.</span><span class="sxs-lookup"><span data-stu-id="85616-301">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="85616-302">Überschreiben des Entnahmeplatzes bei offener Arbeit</span><span class="sxs-lookup"><span data-stu-id="85616-302">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="85616-303">Wichtige Einrichtungsparameter</span><span class="sxs-lookup"><span data-stu-id="85616-303">Key setup parameter</span></span></th>
<th><span data-ttu-id="85616-304">Chargenmenge ist verfügbar</span><span class="sxs-lookup"><span data-stu-id="85616-304">Batch quantity is available</span></span></th>
<th><span data-ttu-id="85616-305">Wichtige Schritte für den Benutzer</span><span class="sxs-lookup"><span data-stu-id="85616-305">Key user steps</span></span></th>
<th><span data-ttu-id="85616-306">Lagerarbeit</span><span class="sxs-lookup"><span data-stu-id="85616-306">Warehouse work</span></span></th>
<th><span data-ttu-id="85616-307">Auftragsgebundene Chargenreservierung</span><span class="sxs-lookup"><span data-stu-id="85616-307">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="85616-308">Die Option <strong>Außerkraftsetzen des Entnahmeorts zulassen</strong> ist für die Arbeitskraft aktiviert.</span><span class="sxs-lookup"><span data-stu-id="85616-308">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="85616-309">Ja</span><span class="sxs-lookup"><span data-stu-id="85616-309">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="85616-310">Wählen Sie das Menüelement <strong>Lagerplatz überschreiben</strong> in der Warehouse-App aus, wenn Sie mit der Entnahmearbeit beginnen.</span><span class="sxs-lookup"><span data-stu-id="85616-310">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="85616-311">Wählen Sie die Option für <strong>Vorschlagen</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="85616-311">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="85616-312">Bestätigen Sie den neuen Lagerort, der basierend auf der Verfügbarkeit der Chargenmenge vorgeschlagen wird.</span><span class="sxs-lookup"><span data-stu-id="85616-312">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="85616-313">Bei der aktuellen Arbeit werden folgende Aktionen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="85616-313">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="85616-314">Der Ort der Entnahmeposition wird auf den neuen Lagerort aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="85616-314">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="85616-315">(Wenn der Lagerort durch einen Ladungsträger gesteuert wird, wird ein zufällig ausgewählter Ladungsträger zur Lagerbuchung für Arbeit zugewiesen und die Arbeitskraft kann von jedem Ladungsträger mit verfügbarer Menge entnehmen.)</span><span class="sxs-lookup"><span data-stu-id="85616-315">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="85616-316">Ist die Menge am neuen Lagerort auf mehreren Ladungsträgern verfügbar, wird die ursprüngliche Entnahmeposition in mehrere Positionen aufgeteilt, um den einzelnen Ladungsträgern zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="85616-316">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="85616-317">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="85616-317">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85616-318">Nr.</span><span class="sxs-lookup"><span data-stu-id="85616-318">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="85616-319">Wählen Sie das Menüelement <strong>Lagerplatz überschreiben</strong> in der Warehouse-App aus, wenn Sie mit der Entnahmearbeit beginnen.</span><span class="sxs-lookup"><span data-stu-id="85616-319">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="85616-320">Geben Sie einen Lagerort manuell ein.</span><span class="sxs-lookup"><span data-stu-id="85616-320">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="85616-321">Die Aktion <strong>Standort überschreiben</strong> ist nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="85616-321">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="85616-322">Sie schlägt fehl und löst einen Fehler aus.</span><span class="sxs-lookup"><span data-stu-id="85616-322">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="85616-323">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="85616-323">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="85616-324">Schaltfläche „Voll“ – Teilt eine Arbeitsposition aufgrund eines Überlaufs am Benutzerstandort</span><span class="sxs-lookup"><span data-stu-id="85616-324">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="85616-325">Wichtige Einrichtungsparameter</span><span class="sxs-lookup"><span data-stu-id="85616-325">Key setup parameter</span></span></th>
<th><span data-ttu-id="85616-326">Chargenmenge ist verfügbar</span><span class="sxs-lookup"><span data-stu-id="85616-326">Batch quantity is available</span></span></th>
<th><span data-ttu-id="85616-327">Wichtige Schritte für den Benutzer</span><span class="sxs-lookup"><span data-stu-id="85616-327">Key user steps</span></span></th>
<th><span data-ttu-id="85616-328">Lagerarbeit</span><span class="sxs-lookup"><span data-stu-id="85616-328">Warehouse work</span></span></th>
<th><span data-ttu-id="85616-329">Auftragsgebundene Chargenreservierung</span><span class="sxs-lookup"><span data-stu-id="85616-329">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85616-330">Die Option <strong>Aufteilung der Arbeit zulassen</strong> ist bei mobilen Geräten im Menüelement aktiviert.</span><span class="sxs-lookup"><span data-stu-id="85616-330">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="85616-331">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="85616-331">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="85616-332">Wählen Sie das Menüelement <strong>Voll</strong> in der Warehouse-App aus, wenn Sie die Entnahmearbeit verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="85616-332">Select the <strong>Full</strong> menu item on the warehouse app when you process picking work.</span></span></li>
<li><span data-ttu-id="85616-333">Geben Sie im Feld <strong>Entnahmemenge</strong> eine Teilmenge der erforderlichen Entnahme ein, um die volle Kapazität anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="85616-333">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="85616-334">Bei der aktuellen Arbeit wird die Menge auf die verbleibende Menge aktualisiert, die kommissioniert werden muss.</span><span class="sxs-lookup"><span data-stu-id="85616-334">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="85616-335">Für die kommissionierte Menge wird eine neue Arbeit angelegt und abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="85616-335">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="85616-336">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="85616-336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="85616-337">Reduzieren der entnommenen Menge für abgeschlossene Arbeit (von einer Ladung)</span><span class="sxs-lookup"><span data-stu-id="85616-337">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="85616-338">Wichtige Einrichtungsparameter</span><span class="sxs-lookup"><span data-stu-id="85616-338">Key setup parameter</span></span></th>
<th><span data-ttu-id="85616-339">Chargenmenge ist verfügbar</span><span class="sxs-lookup"><span data-stu-id="85616-339">Batch quantity is available</span></span></th>
<th><span data-ttu-id="85616-340">Wichtige Schritte für den Benutzer</span><span class="sxs-lookup"><span data-stu-id="85616-340">Key user steps</span></span></th>
<th><span data-ttu-id="85616-341">Lagerarbeit</span><span class="sxs-lookup"><span data-stu-id="85616-341">Warehouse work</span></span></th>
<th><span data-ttu-id="85616-342">Auftragsgebundene Chargenreservierung</span><span class="sxs-lookup"><span data-stu-id="85616-342">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="85616-343">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="85616-343">Not applicable</span></span></td>
<td><span data-ttu-id="85616-344">Ja</span><span class="sxs-lookup"><span data-stu-id="85616-344">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="85616-345">Öffnen Sie die Seite <strong>Entnommene Menge reduzieren</strong> über die Ladungsposition.</span><span class="sxs-lookup"><span data-stu-id="85616-345">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="85616-346">Geben Sie die gesamte Menge an, deren Entnahme rückgängig gemach werden soll.</span><span class="sxs-lookup"><span data-stu-id="85616-346">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="85616-347">Wählen Sie einen „Verschieben nach“-Ladungsträger aus.</span><span class="sxs-lookup"><span data-stu-id="85616-347">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="85616-348">Arbeit, die mit der Ladungsposition verbunden sind, wird abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="85616-348">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="85616-349">Für die Lagerumlagerung wird eine neue Arbeit angelegt und abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="85616-349">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="85616-350">Die Menge wird für dieselbe Charge erneut reserviert.</span><span class="sxs-lookup"><span data-stu-id="85616-350">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="85616-351">Das System weist nach dem Zufallsprinzip einen Lagerort und einen Ladungsträger zu (sofern der Lagerort durch einen Ladungsträger gesteuert wird), an bzw. bei dem die Menge verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="85616-351">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85616-352">Nein</span><span class="sxs-lookup"><span data-stu-id="85616-352">No</span></span></td>
<td><span data-ttu-id="85616-353">Siehe vorherige Zeile.</span><span class="sxs-lookup"><span data-stu-id="85616-353">See the previous row.</span></span></td>
<td><span data-ttu-id="85616-354">Siehe vorherige Zeile.</span><span class="sxs-lookup"><span data-stu-id="85616-354">See the previous row.</span></span></td>
<td><span data-ttu-id="85616-355">Die Menge wird für die gleiche Charge und für den gleichen Lagerort und den gleichen Ladungsträger erneut reserviert (wenn der Lagerort durch einen Ladungsträger gesteuert wird), die während des Zurücknehmens der Entnahme eingegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="85616-355">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="85616-356">Verschieben eines Artikels innerhalb eines Lagerorts</span><span class="sxs-lookup"><span data-stu-id="85616-356">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="85616-357">Diese Lagerortaktion gilt nur für die Verlagerung vom Typ **Arbeitserstellungsprozess**, nicht für die Verlagerung nach Vorlage.</span><span class="sxs-lookup"><span data-stu-id="85616-357">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="85616-358">Wichtige Einrichtungsparameter</span><span class="sxs-lookup"><span data-stu-id="85616-358">Key setup parameter</span></span></th>
<th><span data-ttu-id="85616-359">Chargenmenge ist verfügbar</span><span class="sxs-lookup"><span data-stu-id="85616-359">Batch quantity is available</span></span></th>
<th><span data-ttu-id="85616-360">Wichtige Schritte für den Benutzer</span><span class="sxs-lookup"><span data-stu-id="85616-360">Key user steps</span></span></th>
<th><span data-ttu-id="85616-361">Lagerarbeit</span><span class="sxs-lookup"><span data-stu-id="85616-361">Warehouse work</span></span></th>
<th><span data-ttu-id="85616-362">Auftragsgebundene Chargenreservierung</span><span class="sxs-lookup"><span data-stu-id="85616-362">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="85616-363">Die Option <strong>Bewegung von Bestand mit zugeordneter Arbeit zulassen</strong> ist für die Arbeitskraft aktiviert.</span><span class="sxs-lookup"><span data-stu-id="85616-363">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="85616-364">Ja</span><span class="sxs-lookup"><span data-stu-id="85616-364">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="85616-365">Starten Sie eine Verlagerung in der Warehouse-App.</span><span class="sxs-lookup"><span data-stu-id="85616-365">Start a movement on the warehouse app.</span></span></li>
<li><span data-ttu-id="85616-366">Geben Sie „Von“- und „Nach“-Lagerorte ein.</span><span class="sxs-lookup"><span data-stu-id="85616-366">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="85616-367">Bei allen vorhandenen Arbeiten, die von der Verlagerung betroffen ist, wird der Entnahmeort auf den neuen „Nach“-Lagerort aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="85616-367">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="85616-368">Für die Lagerumlagerung wird eine neue Arbeit angelegt und abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="85616-368">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="85616-369">Alle vorhandenen Reservierungen, die von der Mengenverlagerung vom angegebenen Lagerort betroffen sind, werden für dieselbe Charge erneut reserviert.</span><span class="sxs-lookup"><span data-stu-id="85616-369">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="85616-370">Das System weist nach dem Zufallsprinzip einen Lagerort und einen Ladungsträger zu (sofern der Lagerort durch einen Ladungsträger gesteuert wird), an bzw. bei dem die Menge verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="85616-370">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85616-371">Nein</span><span class="sxs-lookup"><span data-stu-id="85616-371">No</span></span></td>
<td><span data-ttu-id="85616-372">Siehe vorherige Zeile.</span><span class="sxs-lookup"><span data-stu-id="85616-372">See the previous row.</span></span></td>
<td><span data-ttu-id="85616-373">Siehe vorherige Zeile.</span><span class="sxs-lookup"><span data-stu-id="85616-373">See the previous row.</span></span></td>
<td><span data-ttu-id="85616-374">Alle vorhandenen Reservierungen, die von der Mengenverlagerung vom angegebenen Lagerort betroffen sind, werden für dieselbe Charge und den neuen Zielstandort und den Ladungsträger erneut reserviert (sofern der Lagerort durch einen Ladungsträger gesteuert wird).</span><span class="sxs-lookup"><span data-stu-id="85616-374">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="85616-375">Stornieren der entnommenen Menge für abgeschlossene Arbeit (von einer Ladung oder Welle)</span><span class="sxs-lookup"><span data-stu-id="85616-375">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="85616-376">Wichtige Einrichtungsparameter</span><span class="sxs-lookup"><span data-stu-id="85616-376">Key setup parameter</span></span></th>
<th><span data-ttu-id="85616-377">Chargenmenge ist verfügbar</span><span class="sxs-lookup"><span data-stu-id="85616-377">Batch quantity is available</span></span></th>
<th><span data-ttu-id="85616-378">Wichtige Schritte für den Benutzer</span><span class="sxs-lookup"><span data-stu-id="85616-378">Key user steps</span></span></th>
<th><span data-ttu-id="85616-379">Lagerarbeit</span><span class="sxs-lookup"><span data-stu-id="85616-379">Warehouse work</span></span></th>
<th><span data-ttu-id="85616-380">Auftragsgebundene Chargenreservierung</span><span class="sxs-lookup"><span data-stu-id="85616-380">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="85616-381">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="85616-381">Not applicable</span></span></td>
<td><span data-ttu-id="85616-382">Ja</span><span class="sxs-lookup"><span data-stu-id="85616-382">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="85616-383">Öffnen Sie die Seite <strong>Arbeit stornieren</strong>.</span><span class="sxs-lookup"><span data-stu-id="85616-383">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="85616-384">Wählen Sie auf der Anforderungsseite die Option <strong>Artikel am aktuellen Lagerplatz belassen</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="85616-384">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="85616-385">Arbeit, die mit der Ladung verbunden ist, wird abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="85616-385">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="85616-386">Die Menge wird für dieselbe Charge erneut reserviert.</span><span class="sxs-lookup"><span data-stu-id="85616-386">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="85616-387">Das System weist nach dem Zufallsprinzip einen Lagerort und einen Ladungsträger zu (sofern der Lagerort durch einen Ladungsträger gesteuert wird), an bzw. bei dem die Menge verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="85616-387">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85616-388">Nein</span><span class="sxs-lookup"><span data-stu-id="85616-388">No</span></span></td>
<td><span data-ttu-id="85616-389">Siehe vorherige Zeile.</span><span class="sxs-lookup"><span data-stu-id="85616-389">See the previous row.</span></span></td>
<td><span data-ttu-id="85616-390">Siehe vorherige Zeile.</span><span class="sxs-lookup"><span data-stu-id="85616-390">See the previous row.</span></span></td>
<td><span data-ttu-id="85616-391">Die Menge wird für dieselbe Charge und für den Lagerort und den Ladungsträger erneut reserviert, an dem bzw. bei dem die Menge bei der Stornierung belassen wurde.</span><span class="sxs-lookup"><span data-stu-id="85616-391">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85616-392">Ja</span><span class="sxs-lookup"><span data-stu-id="85616-392">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="85616-393">Öffnen Sie die Seite <strong>Arbeit stornieren</strong>.</span><span class="sxs-lookup"><span data-stu-id="85616-393">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="85616-394">Wählen Sie auf der Anforderungsseite die Option <strong>Artikel diesem Lagerplatz zuweisen</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="85616-394">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="85616-395">Die aktuelle Arbeit wird storniert.</span><span class="sxs-lookup"><span data-stu-id="85616-395">The current work is canceled.</span></span></li>
<li><span data-ttu-id="85616-396">Für die Lagerumlagerung wird eine neue Arbeit angelegt und abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="85616-396">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="85616-397">Die Menge wird für dieselbe Charge erneut reserviert.</span><span class="sxs-lookup"><span data-stu-id="85616-397">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="85616-398">Das System weist nach dem Zufallsprinzip einen Lagerort und einen Ladungsträger zu (sofern der Lagerort durch einen Ladungsträger gesteuert wird), an bzw. bei dem die Menge verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="85616-398">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85616-399">Nein</span><span class="sxs-lookup"><span data-stu-id="85616-399">No</span></span></td>
<td><span data-ttu-id="85616-400">Siehe vorherige Zeile.</span><span class="sxs-lookup"><span data-stu-id="85616-400">See the previous row.</span></span></td>
<td><span data-ttu-id="85616-401">Siehe vorherige Zeile.</span><span class="sxs-lookup"><span data-stu-id="85616-401">See the previous row.</span></span></td>
<td><span data-ttu-id="85616-402">Die Menge wird für dieselbe Charge und für den Lagerort und den Ladungsträger reserviert, zu dem die Menge bei der Stornierung zugewiesen war.</span><span class="sxs-lookup"><span data-stu-id="85616-402">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85616-403">Ja/Nein</span><span class="sxs-lookup"><span data-stu-id="85616-403">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="85616-404">Öffnen Sie die Seite <strong>Arbeit stornieren</strong>.</span><span class="sxs-lookup"><span data-stu-id="85616-404">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="85616-405">Wählen Sie auf der Anforderungsseite die Option <strong>Artikel an diesen Lagerplatz umlagern</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="85616-405">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="85616-406">Eine Stornierung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="85616-406">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="85616-407">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="85616-407">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85616-408">Ja/Nein</span><span class="sxs-lookup"><span data-stu-id="85616-408">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="85616-409">Öffnen Sie die Seite <strong>Arbeit stornieren</strong>.</span><span class="sxs-lookup"><span data-stu-id="85616-409">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="85616-410">Wählen Sie auf der Anforderungsseite die Option <strong>Artikel auf der Grundlage von Lagerplatzrichtlinien umlagern</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="85616-410">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="85616-411">Eine Stornierung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="85616-411">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="85616-412">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="85616-412">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="85616-413">Kurzentnahme einer Menge – Registrieren Sie die Menge als Menge, die physisch nicht am Lagerort/auf dem Ladungsträger vorhanden war, als Sie die Entnahmearbeiten durchführten</span><span class="sxs-lookup"><span data-stu-id="85616-413">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="85616-414">Wichtige Einrichtungsparameter</span><span class="sxs-lookup"><span data-stu-id="85616-414">Key setup parameter</span></span></th>
<th><span data-ttu-id="85616-415">Chargenmenge ist verfügbar</span><span class="sxs-lookup"><span data-stu-id="85616-415">Batch quantity is available</span></span></th>
<th><span data-ttu-id="85616-416">Wichtige Schritte für den Benutzer</span><span class="sxs-lookup"><span data-stu-id="85616-416">Key user steps</span></span></th>
<th><span data-ttu-id="85616-417">Lagerarbeit</span><span class="sxs-lookup"><span data-stu-id="85616-417">Warehouse work</span></span></th>
<th><span data-ttu-id="85616-418">Auftragsgebundene Chargenreservierung</span><span class="sxs-lookup"><span data-stu-id="85616-418">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="85616-419">Eine Arbeitsausnahme vom Typ <strong>Kurzentnahme</strong> wird eingerichtet, wenn <strong>Artikelneuzuteilung</strong> = <strong>Keine</strong>, <strong>Bestandsregulierung</strong> = <strong>Ja</strong> und <strong>Reservierungen entfernen</strong> = <strong>Nein</strong> ist.</span><span class="sxs-lookup"><span data-stu-id="85616-419">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="85616-420">Ja</span><span class="sxs-lookup"><span data-stu-id="85616-420">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="85616-421">Wählen Sie das Menüelement <strong>Entnahme unzureichender Menge</strong> in der Warehouse-App aus, wenn Sie die Entnahmearbeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="85616-421">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="85616-422">Geben Sie im Feld <strong>Entnahmemenge</strong> den Wert <strong>0</strong> (Null) ein.</span><span class="sxs-lookup"><span data-stu-id="85616-422">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="85616-423">Geben Sie im Feld <strong>Grund</strong> <strong>Keine Neuzuteilung</strong> ein.</span><span class="sxs-lookup"><span data-stu-id="85616-423">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="85616-424">Die aktuelle Arbeit wird geschlossen und die Entnahmemenge ist 0 (Null).</span><span class="sxs-lookup"><span data-stu-id="85616-424">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="85616-425">Eine Lagerbuchung vom Typ <strong>Inventur</strong> und der Abgangstyp <strong>Verkauft</strong> werden erstellt, um die Anpassung darzustellen.</span><span class="sxs-lookup"><span data-stu-id="85616-425">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="85616-426">Die Menge wird für dieselbe Charge erneut reserviert.</span><span class="sxs-lookup"><span data-stu-id="85616-426">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="85616-427">Das System weist nach dem Zufallsprinzip einen Lagerort und einen Ladungsträger zu (sofern der Lagerort durch einen Ladungsträger gesteuert wird), an bzw. bei dem die Menge verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="85616-427">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85616-428">Nein</span><span class="sxs-lookup"><span data-stu-id="85616-428">No</span></span></td>
<td><span data-ttu-id="85616-429">Siehe vorherige Zeile.</span><span class="sxs-lookup"><span data-stu-id="85616-429">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="85616-430">Die Kurzentnahme-Aktion schlägt fehl und es wird ein Fehler ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="85616-430">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="85616-431">Die aktuelle Arbeit bleibt offen.</span><span class="sxs-lookup"><span data-stu-id="85616-431">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="85616-432">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="85616-432">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="85616-433">Eine Arbeitsausnahme vom Typ <strong>Kurzentnahme</strong> wird eingerichtet, wenn <strong>Artikelneuzuteilung</strong> = <strong>Keine</strong>, <strong>Bestandsregulierung</strong> = <strong>Ja</strong> und <strong>Reservierungen entfernen</strong> = <strong>Ja</strong> ist.</span><span class="sxs-lookup"><span data-stu-id="85616-433">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="85616-434">Ja</span><span class="sxs-lookup"><span data-stu-id="85616-434">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="85616-435">Wählen Sie das Menüelement <strong>Entnahme unzureichender Menge</strong> in der Warehouse-App aus, wenn Sie die Entnahmearbeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="85616-435">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="85616-436">Geben Sie im Feld <strong>Entnahmemenge</strong> den Wert <strong>0</strong> (Null) ein.</span><span class="sxs-lookup"><span data-stu-id="85616-436">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="85616-437">Geben Sie im Feld <strong>Grund</strong> <strong>Keine Neuzuteilung</strong> ein.</span><span class="sxs-lookup"><span data-stu-id="85616-437">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="85616-438">Die aktuelle Arbeit wird geschlossen und die Entnahmemenge ist 0 (Null).</span><span class="sxs-lookup"><span data-stu-id="85616-438">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="85616-439">Eine Lagerbuchung vom Typ <strong>Inventur</strong> und der Abgangstyp <strong>Verkauft</strong> werden erstellt, um die Anpassung darzustellen.</span><span class="sxs-lookup"><span data-stu-id="85616-439">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="85616-440">Alle vorhandenen Reservierungen, die von der Mengenanpassung im Lagerort der Kurzentnahme betroffen sind, werden für dieselbe Charge erneut reserviert.</span><span class="sxs-lookup"><span data-stu-id="85616-440">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="85616-441">Das System weist nach dem Zufallsprinzip einen Lagerort und einen Ladungsträger zu (sofern der Lagerort durch einen Ladungsträger gesteuert wird), an bzw. bei dem die Menge verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="85616-441">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85616-442">Nein</span><span class="sxs-lookup"><span data-stu-id="85616-442">No</span></span></td>
<td><span data-ttu-id="85616-443">Siehe vorherige Zeile.</span><span class="sxs-lookup"><span data-stu-id="85616-443">See the previous row.</span></span></td>
<td><span data-ttu-id="85616-444">Siehe vorherige Zeile.</span><span class="sxs-lookup"><span data-stu-id="85616-444">See the previous row.</span></span></td>
<td><span data-ttu-id="85616-445">Alle vorhandenen Reservierungen, die von der Mengenanpassung im Lagerort der Kurzentnahme betroffen sind, werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="85616-445">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85616-446">Eine Arbeitsausnahme vom Typ <strong>Kurzentnahme</strong> wird eingerichtet, wenn <strong>Artikelneuzuteilung</strong> = <strong>Manuell</strong>, <strong>Bestandsregulierung</strong> = <strong>Ja</strong> und <strong>Reservierungen entfernen</strong> = <strong>Nein/Ja</strong> ist.</span><span class="sxs-lookup"><span data-stu-id="85616-446">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="85616-447">Zusätzlich wird die Option <strong>Manuelle Artikelneuzuordnung zulassen</strong> für die Arbeitskraft aktiviert.</span><span class="sxs-lookup"><span data-stu-id="85616-447">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="85616-448">Ja</span><span class="sxs-lookup"><span data-stu-id="85616-448">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="85616-449">Wählen Sie das Menüelement <strong>Entnahme unzureichender Menge</strong> in der Warehouse-App aus, wenn Sie die Entnahmearbeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="85616-449">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="85616-450">Geben Sie im Feld für <strong>Menge der Kurzentnahme</strong> den Wert <strong>0</strong> (Null) ein.</span><span class="sxs-lookup"><span data-stu-id="85616-450">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="85616-451">Wählen Sie im Feld <strong>Grund</strong> <strong>Kurze Entnahme mit manueller Neuzuteilung</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="85616-451">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="85616-452">Wählen Sie den Lagerort/Ladungsträger in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="85616-452">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="85616-453">Bei der aktuellen Arbeit werden folgende Aktionen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="85616-453">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="85616-454">Die Entnahmeposition wird geschlossen und die Entnahmemenge ist 0 (Null).</span><span class="sxs-lookup"><span data-stu-id="85616-454">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="85616-455">Die Einlagerungsposition wird storniert.</span><span class="sxs-lookup"><span data-stu-id="85616-455">The put line is canceled.</span></span></li>
<li><span data-ttu-id="85616-456">Eine neue Entnahmeposition wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="85616-456">A new pick line is created.</span></span> <span data-ttu-id="85616-457">Es wird der Lagerort/Ladungsträger verwendet, den der Benutzer ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="85616-457">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="85616-458">Eine neue Einlagerungsposition wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="85616-458">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="85616-459">Eine Lagerbuchung vom Typ <strong>Inventur</strong> und der Abgangstyp <strong>Verkauft</strong> werden erstellt, um die Anpassung darzustellen.</span><span class="sxs-lookup"><span data-stu-id="85616-459">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="85616-460">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="85616-460">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85616-461">Eine Arbeitsausnahme vom Typ <strong>Kurzentnahme</strong> wird eingerichtet, wenn <strong>Artikelneuzuteilung</strong> = <strong>Manuell</strong>, <strong>Bestandsregulierung</strong> = <strong>Ja</strong> und <strong>Reservierungen entfernen</strong> = <strong>Nein</strong> ist.</span><span class="sxs-lookup"><span data-stu-id="85616-461">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="85616-462">Zusätzlich wird die Option <strong>Manuelle Artikelneuzuordnung zulassen</strong> für die Arbeitskraft aktiviert.</span><span class="sxs-lookup"><span data-stu-id="85616-462">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="85616-463">Nr.</span><span class="sxs-lookup"><span data-stu-id="85616-463">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="85616-464">Wählen Sie das Menüelement <strong>Entnahme unzureichender Menge</strong> in der Warehouse-App aus, wenn Sie die Entnahmearbeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="85616-464">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="85616-465">Geben Sie im Feld für <strong>Menge der Kurzentnahme</strong> den Wert <strong>0</strong> (Null) ein.</span><span class="sxs-lookup"><span data-stu-id="85616-465">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="85616-466">Wählen Sie im Feld <strong>Grund</strong> <strong>Kurze Entnahme mit manueller Neuzuteilung</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="85616-466">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="85616-467">Die Kurzentnahme-Aktion schlägt fehl und es wird ein Fehler ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="85616-467">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="85616-468">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="85616-468">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85616-469">Eine Arbeitsausnahme vom Typ <strong>Kurzentnahme</strong> wird eingerichtet, wenn <strong>Artikelneuzuteilung</strong> = <strong>Manuell</strong>, <strong>Bestandsregulierung</strong> = <strong>Ja</strong> und <strong>Reservierungen entfernen</strong> = <strong>Ja</strong> ist.</span><span class="sxs-lookup"><span data-stu-id="85616-469">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="85616-470">Zusätzlich wird die Option <strong>Manuelle Artikelneuzuordnung zulassen</strong> für die Arbeitskraft aktiviert.</span><span class="sxs-lookup"><span data-stu-id="85616-470">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="85616-471">Nr.</span><span class="sxs-lookup"><span data-stu-id="85616-471">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="85616-472">Wählen Sie das Menüelement <strong>Entnahme unzureichender Menge</strong> in der Warehouse-App aus, wenn Sie die Entnahmearbeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="85616-472">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="85616-473">Geben Sie im Feld für <strong>Menge der Kurzentnahme</strong> den Wert <strong>0</strong> (Null) ein.</span><span class="sxs-lookup"><span data-stu-id="85616-473">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="85616-474">Wählen Sie im Feld <strong>Grund</strong> <strong>Kurze Entnahme mit manueller Neuzuteilung</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="85616-474">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="85616-475">Wählen Sie den Lagerort/Ladungsträger in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="85616-475">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="85616-476">Bei der aktuellen Arbeit werden folgende Aktionen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="85616-476">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="85616-477">Die Entnahmeposition wird geschlossen und die Entnahmemenge ist 0 (Null).</span><span class="sxs-lookup"><span data-stu-id="85616-477">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="85616-478">Die Einlagerungsposition wird storniert.</span><span class="sxs-lookup"><span data-stu-id="85616-478">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="85616-479">Eine Lagerbuchung vom Typ <strong>Inventur</strong> und der Abgangstyp <strong>Verkauft</strong> werden erstellt, um die Anpassung darzustellen.</span><span class="sxs-lookup"><span data-stu-id="85616-479">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="85616-480">Alle vorhandenen Reservierungen, die von der Mengenanpassung im Lagerort der Kurzentnahme/am Ladungsträger der Kurzentnahme betroffen sind, werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="85616-480">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85616-481">Eine Arbeitsausnahme vom Typ <strong>Kurzentnahme</strong> wird eingerichtet, wenn <strong>Artikelneuzuteilung</strong> = <strong>Automatisch</strong>, <strong>Bestandsregulierung</strong> = <strong>Ja/Nein</strong> und <strong>Reservierungen entfernen</strong> = <strong>Ja/Nein</strong> ist.</span><span class="sxs-lookup"><span data-stu-id="85616-481">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="85616-482">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="85616-482">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="85616-483">Wählen Sie das Menüelement <strong>Entnahme unzureichender Menge</strong> in der Warehouse-App aus, wenn Sie die Entnahmearbeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="85616-483">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="85616-484">Geben Sie im Feld für <strong>Menge der Kurzentnahme</strong> den Wert <strong>0</strong> (Null) ein.</span><span class="sxs-lookup"><span data-stu-id="85616-484">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="85616-485">Wählen Sie im Feld <strong>Grund</strong> <strong>Kurze Entnahme mit automatischer Neuzuteilung</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="85616-485">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="85616-486">Eine Kurzentnahme mit automatischer Neuzuteilung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="85616-486">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="85616-487">Eine Kurzentnahme mit automatischer Neuzuteilung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="85616-487">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="85616-488">Bestandsstatus ändern</span><span class="sxs-lookup"><span data-stu-id="85616-488">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="85616-489">Diese Lagerortaktion kann von mehreren Einstiegspunkten aus durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="85616-489">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="85616-490">Das hier gezeigte Beispiel verwendet die Aktion **Bestandsstatusänderung** auf der Seite **Verfügbarer Lagerbestand nach Lagerplatz**.</span><span class="sxs-lookup"><span data-stu-id="85616-490">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="85616-491">Wichtige Einrichtungsparameter</span><span class="sxs-lookup"><span data-stu-id="85616-491">Key setup parameter</span></span></th>
<th><span data-ttu-id="85616-492">Chargenmenge ist verfügbar</span><span class="sxs-lookup"><span data-stu-id="85616-492">Batch quantity is available</span></span></th>
<th><span data-ttu-id="85616-493">Wichtige Schritte für den Benutzer</span><span class="sxs-lookup"><span data-stu-id="85616-493">Key user steps</span></span></th>
<th><span data-ttu-id="85616-494">Lagerarbeit</span><span class="sxs-lookup"><span data-stu-id="85616-494">Warehouse work</span></span></th>
<th><span data-ttu-id="85616-495">Auftragsgebundene Chargenreservierung</span><span class="sxs-lookup"><span data-stu-id="85616-495">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="85616-496">Auf der Registerkarte <strong>Lagerort</strong> im Datensatz <strong>Lagerort</strong> ist das Feld <strong>Reservierungen und Markierungen entfernen</strong> auf <strong>Reservierungen</strong> oder <strong>Markierungen und Reservierungen</strong> gesetzt.</span><span class="sxs-lookup"><span data-stu-id="85616-496">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="85616-497">Ja</span><span class="sxs-lookup"><span data-stu-id="85616-497">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="85616-498">Wählen Sie einen bestimmten Lagerort aus.</span><span class="sxs-lookup"><span data-stu-id="85616-498">Select a specific location.</span></span></li>
<li><span data-ttu-id="85616-499">Wählen Sie eine Position mit einem bestimmten Artikel, Lagerort und Ladungsträger (sofern der Lagerort durch einen Ladungsträger gesteuert wird).</span><span class="sxs-lookup"><span data-stu-id="85616-499">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="85616-500">Wählen Sie <strong>Bestandsstatusänderung</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="85616-500">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="85616-501">Setzen Sie das Feld <strong>Bestandsstatus</strong> auf <strong>Sperrung</strong>.</span><span class="sxs-lookup"><span data-stu-id="85616-501">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="85616-502">Bestandsstatusänderungen sind für Mengen, die für Arbeit reserviert sind, nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="85616-502">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="85616-503">Die Menge wird für dieselbe Charge erneut reserviert.</span><span class="sxs-lookup"><span data-stu-id="85616-503">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="85616-504">Das System weist nach dem Zufallsprinzip einen Lagerort und einen Ladungsträger zu (sofern der Lagerort durch einen Ladungsträger gesteuert wird), an bzw. bei dem die Menge verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="85616-504">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="85616-505">Zwei Lagerbuchungen vom Typ <strong>Bestandsstatusänderung</strong> werden erstellt, um die Änderung in der Bestandsstatusdimension darzustellen.</span><span class="sxs-lookup"><span data-stu-id="85616-505">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="85616-506">Eine Lagerbuchung vom Typ <strong>Sperrung von Lagerbestand</strong> sowie der Abgangstyp <strong>Physisch reserviert</strong> werden erstellt, um die Reservierung der gesperrten Menge darzustellen.</span><span class="sxs-lookup"><span data-stu-id="85616-506">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="85616-507">Nein</span><span class="sxs-lookup"><span data-stu-id="85616-507">No</span></span></td>
<td><span data-ttu-id="85616-508">Siehe vorherige Zeile.</span><span class="sxs-lookup"><span data-stu-id="85616-508">See the previous row.</span></span></td>
<td><span data-ttu-id="85616-509">Bestandsstatusänderungen sind für Mengen, die für Arbeit reserviert sind, nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="85616-509">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="85616-510">Die Reservierung wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="85616-510">The reservation is removed.</span></span></li>
<li><span data-ttu-id="85616-511">Zwei Lagerbuchungen vom Typ <strong>Bestandsstatusänderung</strong> werden erstellt, um die Änderung in der Bestandsstatusdimension darzustellen.</span><span class="sxs-lookup"><span data-stu-id="85616-511">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="85616-512">Eine Lagerbuchung vom Typ <strong>Sperrung von Lagerbestand</strong> sowie der Abgangstyp <strong>Physisch reserviert</strong> werden erstellt, um die Reservierung der gesperrten Menge darzustellen.</span><span class="sxs-lookup"><span data-stu-id="85616-512">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="85616-513">Auf der Registerkarte <strong>Lagerort</strong> im Datensatz <strong>Lagerort</strong> ist das Feld <strong>Reservierungen und Markierungen entfernen</strong> auf <strong>Nein</strong> gesetzt.</span><span class="sxs-lookup"><span data-stu-id="85616-513">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="85616-514">Ja</span><span class="sxs-lookup"><span data-stu-id="85616-514">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="85616-515">Wählen Sie einen bestimmten Lagerort aus.</span><span class="sxs-lookup"><span data-stu-id="85616-515">Select a specific location.</span></span></li>
<li><span data-ttu-id="85616-516">Wählen Sie eine Position mit einem bestimmten Artikel, Lagerort und Ladungsträger (sofern der Lagerort durch einen Ladungsträger gesteuert wird).</span><span class="sxs-lookup"><span data-stu-id="85616-516">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="85616-517">Wählen Sie <strong>Bestandsstatusänderung</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="85616-517">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="85616-518">Setzen Sie das Feld <strong>Bestandsstatus</strong> auf <strong>Sperrung</strong>.</span><span class="sxs-lookup"><span data-stu-id="85616-518">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="85616-519">Bestandsstatusänderungen sind für Mengen, die für Arbeit reserviert sind, nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="85616-519">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="85616-520">Die Menge wird für dieselbe Charge erneut reserviert.</span><span class="sxs-lookup"><span data-stu-id="85616-520">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="85616-521">Das System weist nach dem Zufallsprinzip einen Lagerort und einen Ladungsträger zu (sofern der Lagerort durch einen Ladungsträger gesteuert wird), an bzw. bei dem die Menge verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="85616-521">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85616-522">Nein</span><span class="sxs-lookup"><span data-stu-id="85616-522">No</span></span></td>
<td><span data-ttu-id="85616-523">Siehe vorherige Zeile.</span><span class="sxs-lookup"><span data-stu-id="85616-523">See the previous row.</span></span></td>
<td><span data-ttu-id="85616-524">Bestandsstatusänderungen sind für Mengen, die für Arbeit reserviert sind, nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="85616-524">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="85616-525">Bestandsstatusänderungen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="85616-525">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="85616-526">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="85616-526">Limitations</span></span>

- <span data-ttu-id="85616-527">Die flexible Reservierungsfunktion für Dimensionen auf Lagerortebene unterstützt die folgenden Funktionen nicht:</span><span class="sxs-lookup"><span data-stu-id="85616-527">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="85616-528">Artikelgewichtsverwaltung</span><span class="sxs-lookup"><span data-stu-id="85616-528">Catch weight management</span></span>
    - <span data-ttu-id="85616-529">Physischer negativer Bestand</span><span class="sxs-lookup"><span data-stu-id="85616-529">Physical negative inventory</span></span>
    - <span data-ttu-id="85616-530">Reservierung kontra gegen bestellte Lieferung</span><span class="sxs-lookup"><span data-stu-id="85616-530">Reservation against ordered supply</span></span>
    - <span data-ttu-id="85616-531">Transportaufträge und Rohmaterialentnahme</span><span class="sxs-lookup"><span data-stu-id="85616-531">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="85616-532">Die Containerkonsolidierungsregel für das Verpacken nach Richtlinieneinheit hat Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="85616-532">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="85616-533">Für auftragsgebundene Reservierungen empfehlen wir, keine Container-Build-Vorlagen zu verwenden, bei denen das Feld **Nach Richtlinieneinheit verpacken** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="85616-533">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="85616-534">Beim aktuellen Design werden keine Lagerplatzrichtlinien verwendet, wenn Lagerarbeit erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="85616-534">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="85616-535">Daher wird nur die niedrigste Einheit in der Nummernkreisgruppe (der Lagereinheit) während des Containerisierungswellenschritts angewendet.</span><span class="sxs-lookup"><span data-stu-id="85616-535">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
