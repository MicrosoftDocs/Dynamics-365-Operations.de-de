---
title: Artikel für einen für die erweiterte Lagerhaltung aktivierten Artikel mithilfe einer Wareneingangserfassung registrieren
description: Dieses Thema stellt ein Szenario vor, wie Artikel mithilfe der Wareneingangserfassung erfasst werden, wenn Sie die erweiterte Lagerortverwaltung verwenden.
author: ShylaThompson
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c58aa1cec6c0bfe33fa1ef90267dcd8ac1218157
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830833"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="484c3-103">Artikel für einen für die erweiterte Lagerhaltung aktivierten Artikel mithilfe einer Wareneingangserfassung registrieren</span><span class="sxs-lookup"><span data-stu-id="484c3-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="484c3-104">Dieses Thema stellt ein Szenario vor, wie Artikel mithilfe der Wareneingangserfassung erfasst werden, wenn Sie die erweiterte Lagerortverwaltung verwenden.</span><span class="sxs-lookup"><span data-stu-id="484c3-104">This topic presents a scenario that shows how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="484c3-105">Dies wird in der Regel von einem Sachbearbeiter für Zugänge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="484c3-105">This would usually be done by a receiving clerk.</span></span>

## <a name="enable-sample-data"></a><span data-ttu-id="484c3-106">Beispieldaten aktivieren</span><span class="sxs-lookup"><span data-stu-id="484c3-106">Enable sample data</span></span>

<span data-ttu-id="484c3-107">Um dieses Szenario mit den in diesem Thema angegebenen Beispieldatensätzen und -werten zu bearbeiten, müssen Sie ein System verwenden, auf dem die Standarddemodaten installiert sind, und Sie müssen die juristische Person *USMF* auswählen, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="484c3-107">To work through this scenario using the sample records and values specified in this topic, you must be using a system where the standard demo data is installed, and you must select the *USMF* legal entity before you begin.</span></span>

<span data-ttu-id="484c3-108">Sie können dieses Szenario stattdessen durcharbeiten, indem Sie Werte aus Ihren eigenen Daten nutzen, sofern die folgenden Daten verfügbar sind:</span><span class="sxs-lookup"><span data-stu-id="484c3-108">You can instead work through this scenario by substituting values from your own data provided that you have the following data available:</span></span>

- <span data-ttu-id="484c3-109">Sie müssen eine bestätigte Bestellung mit einer offenen Bestellposition haben.</span><span class="sxs-lookup"><span data-stu-id="484c3-109">You must have a confirmed purchase order with an open purchase order line.</span></span>
- <span data-ttu-id="484c3-110">Der Artikel für die Position muss gelagert sein.</span><span class="sxs-lookup"><span data-stu-id="484c3-110">The item on the line must be stocked.</span></span> <span data-ttu-id="484c3-111">Es dürfen keine Produktvarianten verwendet werden und es dürfen keine Rückverfolgungsangaben vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="484c3-111">It must not use product variants, and must not have tracking dimensions.</span></span>
- <span data-ttu-id="484c3-112">Der Artikel muss einer Lagerdimensionsgruppe zugeordnet werden, die für den Lagerortverwaltungsprozess aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="484c3-112">The item must be associated with a storage dimension group that has warehouse management process enabled.</span></span>
- <span data-ttu-id="484c3-113">Der Lagerort, der verwendet wird, muss für Lagerortverwaltungsprozesse aktiviert sein und der Lagerplatz, der für den Eingang verwendet wird, muss über Ladungsträger gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="484c3-113">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span>

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a><span data-ttu-id="484c3-114">Erstellen Sie eine Wareneingangserfassungs-Kopfzeile, die die Lagerortverwaltung verwendet</span><span class="sxs-lookup"><span data-stu-id="484c3-114">Create an item arrival journal header that uses warehouse management</span></span>

<span data-ttu-id="484c3-115">Das folgende Szenario zeigt, wie Sie eine Wareneingangserfassungs-Kopfzeile erstellen, die die Lagerortverwaltung verwendet:</span><span class="sxs-lookup"><span data-stu-id="484c3-115">The following scenario shows how to create an item arrival journal header that uses warehouse management:</span></span>

1. <span data-ttu-id="484c3-116">Stellen Sie sicher, dass Ihr System eine bestätigte Bestellung enthält, die die im vorherigen Abschnitt beschriebenen Anforderungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="484c3-116">Make sure your system contains a confirmed purchase order that fulfils the requirements outlined in the previous section.</span></span> <span data-ttu-id="484c3-117">In diesem Szenario wird eine Bestellung für das Unternehmen *USMF* verwendet, Kreditorenkonto *1001*, Lagerort *51*, mit einer Bestellposition für *10 PL* (10 Paletten) der Artikelnummer *M9200*.</span><span class="sxs-lookup"><span data-stu-id="484c3-117">This scenario uses a purchase order for company *USMF*, vendor account *1001*, warehouse *51*, with an order line for *10 PL* (10 pallets) of item number *M9200*.</span></span>
1. <span data-ttu-id="484c3-118">Notieren Sie sich die Bestellnummer, die Sie benutzen werden.</span><span class="sxs-lookup"><span data-stu-id="484c3-118">Make a note of the purchase order number that you will use.</span></span>
1. <span data-ttu-id="484c3-119">Wechseln Sie zu **Bestandsverwaltung \> Erfassunseinträge \> Wareneingang \> Wareneingang**.</span><span class="sxs-lookup"><span data-stu-id="484c3-119">Go to **Inventory management \> Journal entries \> Item arrival \> Item arrival**.</span></span>
1. <span data-ttu-id="484c3-120">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="484c3-120">Select **New** on the Action Pane.</span></span>
1. <span data-ttu-id="484c3-121">Das Dialogfeld **Lagerortverwaltungserfassung erstellen** öffnet sich.</span><span class="sxs-lookup"><span data-stu-id="484c3-121">The **Create warehouse management journal** dialog box opens.</span></span> <span data-ttu-id="484c3-122">Wählen Sie im Feld **Name** eine Erfassung aus.</span><span class="sxs-lookup"><span data-stu-id="484c3-122">Select a journal name in the **Name** field.</span></span>
    - <span data-ttu-id="484c3-123">Wenn Sie die *USMF*-Demodaten verwenden, wählen Sie *WHS* aus.</span><span class="sxs-lookup"><span data-stu-id="484c3-123">If you are using *USMF* sample data, select *WHS*.</span></span>
    - <span data-ttu-id="484c3-124">Wenn Sie Ihre eigenen Daten verwenden, muss die von Ihnen ausgewählte Erfassung bei **Entnahmeort prüfen** auf *Nein* und bei **Quarantäneverwaltung** auf *Nein* gestellt sein.</span><span class="sxs-lookup"><span data-stu-id="484c3-124">If you're using your own data, the journal you choose must have **Check picking location** set to *No* and **Quarantine management** set to *No*.</span></span>
1. <span data-ttu-id="484c3-125">Setzten Sie **Referenz** auf *Bestellung*.</span><span class="sxs-lookup"><span data-stu-id="484c3-125">Set **Reference** to *Purchase order*.</span></span>
1. <span data-ttu-id="484c3-126">Setzen Sie **Kontonummer** auf *1001*.</span><span class="sxs-lookup"><span data-stu-id="484c3-126">Set **Account number** to *1001*.</span></span>
1. <span data-ttu-id="484c3-127">Setzen Sie **Nummer** auf die Nummer der Bestellung, die Sie für diese Übung ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="484c3-127">Set **Number** to the number of the purchase order that you identified for this exercise.</span></span>

    <span data-ttu-id="484c3-128">![Wareneingangserfassung](../media/item-arrival-journal-header.png "Wareneingangserfassung")</span><span class="sxs-lookup"><span data-stu-id="484c3-128">![Item arrival journal](../media/item-arrival-journal-header.png "Item arrival journal")</span></span>

1. <span data-ttu-id="484c3-129">Wählen Sie **OK**, um die Erfassungkopfzeile zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="484c3-129">Select the **OK** to create the journal header.</span></span>
1. <span data-ttu-id="484c3-130">Im Abschnitt **Erfassungspositionen** wählen Sie **Position hinzufügen** aus und geben Sie folgende Daten ein:</span><span class="sxs-lookup"><span data-stu-id="484c3-130">In the **Journal lines** section, select **Add line** and enter the following data:</span></span>
    - <span data-ttu-id="484c3-131">**Artikelnummer** – *M9200*.</span><span class="sxs-lookup"><span data-stu-id="484c3-131">**Item number** – Set to *M9200*.</span></span> <span data-ttu-id="484c3-132">**Standort**, **Lagerort** und **Menge** werden basierend auf den Bestandstransaktionsdaten für die 10 Paletten (1.000 Stück) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="484c3-132">The **Site**, **Warehouse**, and **Quantity** will get set based on the inventory transaction data for the 10 pallets (1000 ea.).</span></span>
    - <span data-ttu-id="484c3-133">**Standort** – Stellen Sie *001* ein.</span><span class="sxs-lookup"><span data-stu-id="484c3-133">**Location** – Set to  *001*.</span></span> <span data-ttu-id="484c3-134">Dieser spezielle Standort verfolgt Ladungsträger nicht nach.</span><span class="sxs-lookup"><span data-stu-id="484c3-134">This specific location does not track license plates.</span></span>

    <span data-ttu-id="484c3-135">![Wareneingangserfassungsposition](../media/item-arrival-journal-line.png "Wareneingangserfassungsposition")</span><span class="sxs-lookup"><span data-stu-id="484c3-135">![Item arrival journal line](../media/item-arrival-journal-line.png "Item arrival journal line")</span></span>

    > [!NOTE]
    > <span data-ttu-id="484c3-136">Das Feld **Datum** bestimmt das Datum, an dem die verfügbare Menge dieses Artikels im Bestand erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="484c3-136">The **Date** field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    >
    > <span data-ttu-id="484c3-137">Die **Loskennung** wird vom System ausgefüllt, wenn sie über die bereitgestellten Informationen eindeutig identifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="484c3-137">The **Lot ID** will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="484c3-138">Andernfalls müssen Sie sie manuell eingeben.</span><span class="sxs-lookup"><span data-stu-id="484c3-138">Otherwise you will have to enter this manually.</span></span> <span data-ttu-id="484c3-139">Dies ist ein Pflichtfeld, das diese Erfassung mit einer bestimmten Quelldokumentposition verknüpft.</span><span class="sxs-lookup"><span data-stu-id="484c3-139">This is a required field, which links this registration to a specific source document line.</span></span>  

1. <span data-ttu-id="484c3-140">Wählen Sie im Aktivitätsbereich **Überprüfen** aus.</span><span class="sxs-lookup"><span data-stu-id="484c3-140">Select **Validate** on the Action Pane.</span></span> <span data-ttu-id="484c3-141">Dies überprüft, ob die Erfassung für die Buchung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="484c3-141">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="484c3-142">Wenn die Prüfung fehlschlägt, müssen Sie die Fehler korrigieren, bevor Sie die Erfassung buchen können.</span><span class="sxs-lookup"><span data-stu-id="484c3-142">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
1. <span data-ttu-id="484c3-143">Das Dialogfeld **Erfassung überprüfen** öffnet sich.</span><span class="sxs-lookup"><span data-stu-id="484c3-143">The **Check journal** dialog box opens.</span></span> <span data-ttu-id="484c3-144">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="484c3-144">Select **OK**.</span></span>
1. <span data-ttu-id="484c3-145">Überprüfen Sie die Meldungsleiste.</span><span class="sxs-lookup"><span data-stu-id="484c3-145">Review the message bar.</span></span> <span data-ttu-id="484c3-146">Es sollte eine Meldung geben, die darauf hinweist, dass der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="484c3-146">There should be a message denoting that the operation was completed.</span></span>  
1. <span data-ttu-id="484c3-147">Wählen Sie im Aktivitätsbereich **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="484c3-147">Select **Post** on the Action Pane.</span></span>
1. <span data-ttu-id="484c3-148">Das Dialogfeld **Erfassung buchen** öffnet sich.</span><span class="sxs-lookup"><span data-stu-id="484c3-148">The **Post journal** dialog box opens.</span></span> <span data-ttu-id="484c3-149">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="484c3-149">Select **OK**.</span></span>
1. <span data-ttu-id="484c3-150">Überprüfen Sie die Meldungsleiste.</span><span class="sxs-lookup"><span data-stu-id="484c3-150">Review the message bar.</span></span> <span data-ttu-id="484c3-151">Es sollte eine Meldung geben, die darauf hinweist, dass der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="484c3-151">There should be messages denoting that the operation completed.</span></span>
1. <span data-ttu-id="484c3-152">Wählen Sie im Aktivitätsbereich **Funktionen > Produktzugang**, um die Bestellposition zu aktualisieren und einen Produktzugang zu buchen.</span><span class="sxs-lookup"><span data-stu-id="484c3-152">Select **Functions > Product receipt** on the Action Pane to update the purchase order line and post a product receipt.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
