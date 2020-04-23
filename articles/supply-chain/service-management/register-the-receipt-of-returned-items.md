---
title: Erfassen des Empfangs zurückgelieferter Artikel
description: Sie können den Beleg für zurückgegebenen Artikel über das Formular "Wareneingangsübersicht" oder das Formular "Registrierung" erfassen.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9979c6180bda406513cc3234c9fa5d9db2b32a75
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202076"
---
# <a name="register-the-receipt-of-returned-items"></a><span data-ttu-id="bce2e-103">Erfassen des Empfangs zurückgelieferter Artikel</span><span class="sxs-lookup"><span data-stu-id="bce2e-103">Register the receipt of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="bce2e-104">Es gibt zwei Methoden zum Erfassen des Eingangs zurückgelieferter Artikel.</span><span class="sxs-lookup"><span data-stu-id="bce2e-104">There are two methods for registering the receipt of returned items.</span></span> <span data-ttu-id="bce2e-105">Die erste Methode ist ein Lagerempfangsprozess, in dem das Formular **Wareneingangsübersicht** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bce2e-105">The first method is a warehouse receiving process that uses the **Arrival overview** form.</span></span> <span data-ttu-id="bce2e-106">In der zweiten Methode wird das Formular **Erfassung** verwendet.</span><span class="sxs-lookup"><span data-stu-id="bce2e-106">The second uses the **Registration** form.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a><span data-ttu-id="bce2e-107">Erfassen des Eingangs zurückgelieferter Artikel im Formular "Wareneingangsübersicht"</span><span class="sxs-lookup"><span data-stu-id="bce2e-107">Register the receipt of returned items in the Arrival overview form</span></span>

<span data-ttu-id="bce2e-108">Mithilfe des Formulars **Wareneingangsübersicht** können Sie eine Rücklieferung anhand ihrer Rücksendungsnummer bestimmen.</span><span class="sxs-lookup"><span data-stu-id="bce2e-108">You can use the **Arrival overview** form to identify a return shipment by its Return Material Authorization (RMA) number.</span></span> <span data-ttu-id="bce2e-109">Wenn ein Erfassungsname auf der Registerkarte **Einrichtung** definiert ist und Erfassungspositionen vorhanden sind, die Positionen entsprechen, die im Formular **Wareneingangsübersicht** ausgewählt sind, wird ein neuer Erfassungskopf erstellt, wenn Sie auf **Wareneingang starten** klicken.</span><span class="sxs-lookup"><span data-stu-id="bce2e-109">If a journal name is defined on the **Setup** tab, and journal lines that correspond to the lines selected on the **Arrival overview** form exist, a new journal header is created when you click **Start arrival**.</span></span>

1.  <span data-ttu-id="bce2e-110">Klicken Sie auf **Lagerverwaltung** \> **Periodisch** \> **Wareneingangsübersicht**.</span><span class="sxs-lookup"><span data-stu-id="bce2e-110">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="bce2e-111">Wählen Sie im Feld **Setupname** **Rücklieferung** und dann **Aktualisieren** klicken.</span><span class="sxs-lookup"><span data-stu-id="bce2e-111">In the **Setup name** field, select **Return order**, and then click **Update**.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="bce2e-112">Mithilfe der Felder <STRONG>Bereich</STRONG> können die Suchergebnisse eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="bce2e-112">You can use the <STRONG>Range</STRONG> fields to narrow the search results.</span></span> <span data-ttu-id="bce2e-113">Sie können die Rücksendungsnummer im Feld <STRONG>RMA-Nummer</STRONG> eingeben oder auswählen, um ein genaues Ergebnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bce2e-113">You can type or select the RMA number in the <STRONG>RMA number</STRONG> field for an exact result.</span></span> <span data-ttu-id="bce2e-114">Um einen Filter Satz zu definieren und zu speichern die eingrenzen das eingehende Wareneingänge angezeigt werden, klicken Sie auf die Registerkarte <STRONG>Einrichtung</STRONG>. Die verfügbaren Typen Filter umfassen, Lagerorte und Docks.</span><span class="sxs-lookup"><span data-stu-id="bce2e-114">To define and save a set of filters that will restrict which incoming arrivals are displayed, click the <STRONG>Setup</STRONG> tab. The available filters include types, warehouses, and docks.</span></span></P>

    

    > [!WARNING]
    > <P><span data-ttu-id="bce2e-115">Rücklieferungen können im Formular <STRONG>Wareneingangsübersicht</STRONG> nicht mit anderen Eingangstypen gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="bce2e-115">Return orders cannot be mixed with other arrival types in the <STRONG>Arrival overview</STRONG> form.</span></span> <span data-ttu-id="bce2e-116">Daher ist die Referenz stets der Auftrag; im Erfassungskopf wird jedoch keine Auftragskennung angegeben.</span><span class="sxs-lookup"><span data-stu-id="bce2e-116">Therefore, the reference will always be sales order, but no sales order ID will be specified on the journal header.</span></span></P>



3.  <span data-ttu-id="bce2e-117">Suchen Sie im Raster **Zugänge** die Position, die dem zurückgesendeten Artikel entspricht, und aktivieren Sie das Kontrollkästchen in der Spalte **Für Wareneingang auswählen**.</span><span class="sxs-lookup"><span data-stu-id="bce2e-117">In the **Receipts** grid, locate the line that matches the item being returned, and then select the check box in the **Select for arrival** column.</span></span>

4.  <span data-ttu-id="bce2e-118">Wenn Sie bestimmte Positionen aus dem Rücklieferungseingang ausschließen möchten, z. B. nicht in der Rücklieferung eingeschlossene Artikel aus dem ursprünglichen Auftrag, deaktivieren Sie die zugeordneten Kästchen **Für Wareneingang auswählen** in der Tabelle **Positionen** im unteren Teil des Formulars.</span><span class="sxs-lookup"><span data-stu-id="bce2e-118">To exclude certain lines from the return receipt, such as items from the original order that were not included in the return shipment, clear the associated **Select for arrival** check boxes in the **Lines** table in the lower part of the form.</span></span>

5.  <span data-ttu-id="bce2e-119">Klicken Sie auf die Schaltfläche **Wareneingang starten**, um eine Wareneingangserfassung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bce2e-119">Click the **Start arrival** button to create an arrival journal.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="bce2e-120">Sie können mehrere Rücklieferungen auswählen und alle in einen Wareneingang einschließen.</span><span class="sxs-lookup"><span data-stu-id="bce2e-120">You can select multiple return orders and include them all in a single arrival process.</span></span> <span data-ttu-id="bce2e-121">Jede Rücklieferungsposition wird in eine entsprechende Wareneingangserfassungsposition kopiert.</span><span class="sxs-lookup"><span data-stu-id="bce2e-121">Each return order line will be copied into a corresponding item arrival journal line.</span></span></P>

    

    > [!NOTE]
    > <P><span data-ttu-id="bce2e-122">Sie können eine Wareneingangserfassung auch manuell erstellen, indem Sie das Formular <STRONG>Wareneingang</STRONG> verwenden.</span><span class="sxs-lookup"><span data-stu-id="bce2e-122">You can also manually create an arrival journal by using the <STRONG>Item arrival</STRONG> form.</span></span> 



6.  <span data-ttu-id="bce2e-123">Klicken Sie auf **Lagerverwaltung** \> **Journaleinträge** \> **Wareneingang** \> **Wareneingang**.</span><span class="sxs-lookup"><span data-stu-id="bce2e-123">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>

7.  <span data-ttu-id="bce2e-124">Wählen Sie die soeben erstellte Wareneingangserfassung aus, und klicken Sie anschließend auf **Positionen**, um das Formular **Erfassungspositionen, Lagerplätze** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bce2e-124">Select the arrival journal that you just created and then click **Lines** to open the **Journal lines, locations** form.</span></span>

8.  <span data-ttu-id="bce2e-125">Passen Sie auf der Registerkarte **Allgemein** die Zahl im Feld **Menge** an, sofern dies erforderlich ist, und weisen Sie anschließend im Feld **Dispositionscode** einen Dispositionscode zu.</span><span class="sxs-lookup"><span data-stu-id="bce2e-125">On the **General** tab, adjust the number in the **Quantity** field, if it is required, and then assign a disposition code in the **Disposition code** field.</span></span>
    
    <span data-ttu-id="bce2e-126">Alternativ können Sie das Kontrollkästchen **Quarantäneverwaltung** aktivieren, um die zurückgelieferten Artikel durch einen Prüfprozess im Kontext eines Quarantäneauftrags zu senden.</span><span class="sxs-lookup"><span data-stu-id="bce2e-126">Alternatively, you can select the **Quarantine management** check box to have the returned items sent through an inspection process in the context of a quarantine order.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="bce2e-127">Wenn Sie die zurückgelieferten Artikel durch die Quarantäne senden, können Sie keinen Dispositionscode angeben.</span><span class="sxs-lookup"><span data-stu-id="bce2e-127">If you send the returned items through quarantine, you cannot specify a disposition code.</span></span></P>



9.  <span data-ttu-id="bce2e-128">Klicken Sie auf die Schaltfläche '**Prüfen**'.</span><span class="sxs-lookup"><span data-stu-id="bce2e-128">Click the **Validate** button.</span></span>

10. <span data-ttu-id="bce2e-129">Klicken Sie auf **Buchen**, wenn im Prüfungsprozess keine Fehler aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="bce2e-129">If there are no errors in the validation process, click **Post**.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a><span data-ttu-id="bce2e-130">Erfassen des Eingangs zurückgelieferter Artikel im Formular "Registrierung"</span><span class="sxs-lookup"><span data-stu-id="bce2e-130">Register the receipt of returned items in the Registration form</span></span>

<span data-ttu-id="bce2e-131">Alternativ zur **Verwendung des Formulars** können Sie das Formular **Erfassung** verwenden, um den Eingang zurückgelieferter Artikel zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="bce2e-131">As an alternative to using the **Arrival overview** form, you can use the **Registration** form to register the arrival of returned items.</span></span>

1.  <span data-ttu-id="bce2e-132">Klicken auf **Vertrieb und Marketing** \> **Gemeinsam** \> **Rücklieferungen** \> **Alle Rücklieferungen**.</span><span class="sxs-lookup"><span data-stu-id="bce2e-132">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span> <span data-ttu-id="bce2e-133">Erstellen Sie eine neue Rücklieferung, oder öffnen Sie die Rücklieferung in der Liste.</span><span class="sxs-lookup"><span data-stu-id="bce2e-133">Create a new return order or open the return order from the list.</span></span> <span data-ttu-id="bce2e-134">Wählen Sie auf der Inforegister **Positionen** die Rücklieferungsposition aus.</span><span class="sxs-lookup"><span data-stu-id="bce2e-134">On the **Lines** FastTab, select the return order line.</span></span> <span data-ttu-id="bce2e-135">Klicken Sie auf **Position aktualisieren** und dann auf **Registrierung**.</span><span class="sxs-lookup"><span data-stu-id="bce2e-135">Click **Update line**, and then click **Registration**.</span></span>

2.  <span data-ttu-id="bce2e-136">Weisen Sie im Feld **Dispositionscode** einen Dispositionscode zu, und klicken Sie anschließend auf **O**K.</span><span class="sxs-lookup"><span data-stu-id="bce2e-136">Assign a disposition code in the **Disposition code** field, and then click **OK**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="bce2e-137">Es ist nicht möglich, den zu prüfenden Artikel mithilfe des Formulars <STRONG>Erfassung</STRONG> als Quarantäneauftrag zu senden.</span><span class="sxs-lookup"><span data-stu-id="bce2e-137">It is not possible to send the item for inspection as a quarantine order using the <STRONG>Registration</STRONG> form.</span></span></P>



3.  <span data-ttu-id="bce2e-138">Wählen Sie im Raster **Transaktionen** die zu erfassende Buchung aus.</span><span class="sxs-lookup"><span data-stu-id="bce2e-138">In the **Transactions** grid, select the transaction to be registered.</span></span>

4.  <span data-ttu-id="bce2e-139">Im Raster **Jetzt erfassen** klicken Sie **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="bce2e-139">In the **Register now** grid, click **Add**.</span></span> <span data-ttu-id="bce2e-140">Wiederholen Sie die beiden vorherigen Schritte, bis alle zurückgelieferten Artikel im Raster **Jetzt erfassen** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bce2e-140">Repeat the previous two steps until all of the returned items appear in the **Register now** grid.</span></span>

5.  <span data-ttu-id="bce2e-141">Klicken Sie auf **Alle buchen**.</span><span class="sxs-lookup"><span data-stu-id="bce2e-141">Click **Post all**.</span></span>

## <a name="see-also"></a><span data-ttu-id="bce2e-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bce2e-142">See also</span></span>

<span data-ttu-id="bce2e-143">[Formular "Wareneingangsübersicht"](https://technet.microsoft.com/library/hh227654\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="bce2e-143">[Arrival overview (form)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))</span></span>

  


