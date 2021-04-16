---
title: Automatische Umwandlung mit Planungsoptimierung
description: In diesem Abschnitt wird erläutert, wie Sie die automatische Fixierung mit der Planungsoptimierung verwenden.
author: ChristianRytt
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 3542e343de29c9fd9d19ed99cab4b4eebacd2899
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813002"
---
# <a name="autofirming-with-planning-optimization"></a><span data-ttu-id="26620-103">Automatische Umwandlung mit Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="26620-103">Autofirming with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="26620-104">Mit der automatischen Fixierung können Sie Planaufträge im Rahmen des Masterplanungsprozesses fixieren (d.h. freigeben).</span><span class="sxs-lookup"><span data-stu-id="26620-104">Automatic firming lets you firm (that is, release) planned orders as part of the master planning process.</span></span> <span data-ttu-id="26620-105">Wenn Planaufträge fixiert werden, werden sie in Ist-Bestellungen, Transportaufträge oder Fertigungsaufträge umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="26620-105">When planned orders are firmed, they are transformed into actual purchase orders, transfer orders, or production orders.</span></span> <span data-ttu-id="26620-106">Bei der Planungsoptimierung werden Planaufträge während eines Masterplanungslaufs fixiert, wenn das Auftragsdatum (d.h. das Startdatum) innerhalb des Zeitfensters für die Fixierung liegt.</span><span class="sxs-lookup"><span data-stu-id="26620-106">When Planning Optimization is used, planned orders are firmed during a master planning run when the order date (that is, the start date) is within the time fence for firming.</span></span>

> [!NOTE]
> <span data-ttu-id="26620-107">Die automatische Bestätigung einer geplanten Bestellung kann nur erfolgen, wenn die Position einem Lieferanten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="26620-107">Auto-firming of a planned purchase order can occur only if the item is associated with a vendor.</span></span>
> 
> <span data-ttu-id="26620-108">Fixierte abgeleitete Aufträge (Unterauftrags-Bestellungen) zeigen den Status *Wird überprüft* an, wenn die Falländerungsverfolgung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="26620-108">Firmed derived orders (subcontract purchase orders) will show a status of *In-review* when case change tracking is enabled.</span></span>

## <a name="turn-on-autofirming"></a><span data-ttu-id="26620-109">Automatische Umwandlung</span><span class="sxs-lookup"><span data-stu-id="26620-109">Turn on autofirming</span></span>

<span data-ttu-id="26620-110">Um die automatische Bestätigung einzuschalten, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="26620-110">To turn on autofirming, follow these steps.</span></span>

1. <span data-ttu-id="26620-111">Wählen Sie im Arbeitsbereich **Feature-Management** auf der Registerkarte **Neu** **Automatische Umwandlung zur Planungsoptimierung** in der Liste.</span><span class="sxs-lookup"><span data-stu-id="26620-111">In the **Feature management** workspace, on the **New** tab, select **Auto-firming for Planning Optimization** in the list.</span></span> <span data-ttu-id="26620-112">Wenn die Funktion nicht auf der Registerkarte **Neu** erscheint, schauen Sie auf die Registerkarten **Nicht aktiviert** und **Alle**.</span><span class="sxs-lookup"><span data-stu-id="26620-112">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="26620-113">Wählen Sie **Jetzt aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="26620-113">Select **Enable now**.</span></span> <span data-ttu-id="26620-114">Alternativ können Sie auch **Terminplanung** wählen und dann die Zeit auswählen, zu der die Funktion eingeschaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="26620-114">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

## <a name="set-up-the-firming-time-fence"></a><span data-ttu-id="26620-115">Den Fixierzeitanschlag einrichten</span><span class="sxs-lookup"><span data-stu-id="26620-115">Set up the firming time fence</span></span>

<span data-ttu-id="26620-116">Der Fixierungszeitrahmen wird aus dem Laufdatum der Masterplanung vorwärts berechnet.</span><span class="sxs-lookup"><span data-stu-id="26620-116">The firming time fence is calculated forward from the master planning run date.</span></span> <span data-ttu-id="26620-117">Sie wird durch die Anzahl der Tage definiert, die Sie eingeben.</span><span class="sxs-lookup"><span data-stu-id="26620-117">It's defined by the number of days that you enter.</span></span> <span data-ttu-id="26620-118">Sie können den Fixierungszeitanschlag wie folgt steuern:</span><span class="sxs-lookup"><span data-stu-id="26620-118">You can control the firming time fence in the following ways:</span></span>

- <span data-ttu-id="26620-119">Um den voreingestellten Fixierungszeitrahmen für eine Deckungsgruppe zu definieren, gehen Sie zu **Masterplanung** \> **Einrichtung** \> **Deckung** \> **Deckungsgruppen** und wählen eine Deckungsgruppe aus.</span><span class="sxs-lookup"><span data-stu-id="26620-119">To define the default firming time fence for a coverage group, go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**, and select a coverage group.</span></span> <span data-ttu-id="26620-120">Geben Sie dann auf der Registerkarte **Anderes** Inforegister im Feld **Automatischer Fixierungszeitrahmen (Tage)** die Anzahl der Tage ein.</span><span class="sxs-lookup"><span data-stu-id="26620-120">Then, on the **Other** FastTab, in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="26620-121">Um den Fixierungszeitrahmen zu überschreiben, der für die Deckungsgruppe eines bestimmten Artikels definiert ist, gehen Sie zu **Produktinformationsmanagement** \> **Freigegebene Produkte**, wählen Sie dann aus dem Aktionsbereich **Plan** und wählen Sie dann **Artikelabdeckung**.</span><span class="sxs-lookup"><span data-stu-id="26620-121">To overwrite the firming time fence that is defined for the coverage group for a specific item, go to **Product information management** \> **Released products**, then from the Action Pane select **Plan** and then select **Item coverage**.</span></span> <span data-ttu-id="26620-122">Wählen Sie dann auf der Registerkarte **Allgemein** **Überschreibungszeitraum** und geben Sie im Feld **Automatischer Fixierungszeitrahmen (Tage)** die Anzahl der Tage ein.</span><span class="sxs-lookup"><span data-stu-id="26620-122">Then, on the **General** tab, select **Override time fence** and in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="26620-123">Um den Fixierungszeitrahmen zu überschreiben, der für die Deckungsgruppe und die Artikelabdeckung für einen bestimmten Produktionsplan definiert ist, gehen Sie zu **Masterplanung** \> **Setup** \> **Masterpläne** und wählen Sie einen Produktionsplan.</span><span class="sxs-lookup"><span data-stu-id="26620-123">To overwrite the firming time fence that is defined for the coverage group and item coverage for a specific master plan, go to **Master planning** \> **Setup** \> **Master plans**, and select a Master plan.</span></span> <span data-ttu-id="26620-124">Legen Sie dann auf dem Inforegister **Zeitfenster in Tagen** **Bestätigen** auf **Ja** fest und geben Sie die Anzahl der Tage ein.</span><span class="sxs-lookup"><span data-stu-id="26620-124">Then, on the **Time fence in days** FastTab, set **Firming** to **Yes**, and enter the number of days.</span></span>

<span data-ttu-id="26620-125">Wenn die Automatische Umwandlung für eine Produktprogrammplanung, die die Planungsoptimierung verwendet, eingeschaltet ist, wird der Automatische Umwandlung-Prozess gemäß dem Automatische-Umwandlung-Setup durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="26620-125">If autofirming is turned on for a master planning run that uses Planning Optimization, the autofirming process is done according to the autofirming setup.</span></span> <span data-ttu-id="26620-126">Wenn Automatische Umwandlung nicht eingeschaltet ist oder wenn die Planung von der Seite **Netzanforderungen** aus gestartet wird, wird der Automatische Umwandlung-Vorgang übersprungen.</span><span class="sxs-lookup"><span data-stu-id="26620-126">If autofirming isn't turned on, or if planning is started from the **Net requirements** page, the autofirming process is skipped.</span></span>

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a><span data-ttu-id="26620-127">Planungsoptimierung im Vergleich zur integrierten Supply Chain Management Planungs-Engine</span><span class="sxs-lookup"><span data-stu-id="26620-127">Planning Optimization vs. the built-in Supply Chain Management planning engine</span></span>

<span data-ttu-id="26620-128">Sowohl die Planungsoptimierung als auch die in Microsoft Dynamics 365 Supply Chain Management eingebaute Planungs-Engine können zur automatischen Bestätigung von Planaufträgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26620-128">Both Planning Optimization and the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management can be used to autofirm planned orders.</span></span> <span data-ttu-id="26620-129">Jedoch gibt es mehrere wichtige Unterschiede.</span><span class="sxs-lookup"><span data-stu-id="26620-129">However, there are some important differences.</span></span> <span data-ttu-id="26620-130">Während die Planungsoptimierung beispielsweise anhand des Auftragsdatums (d.h. des Startdatums) ermittelt, welche Planaufträge zu fixieren sind, verwendet die integrierte Supply Chain Management Planungs-Engine das Bedarfsdatum (d.h. das Enddatum).</span><span class="sxs-lookup"><span data-stu-id="26620-130">For example, whereas Planning Optimization uses the order date (that is, the start date) to determine which planned orders to firm, the built-in Supply Chain Management planning engine uses the requirement date (that is, the end date).</span></span> <span data-ttu-id="26620-131">Hier ist eine Zusammenfassung der Unterschiede.</span><span class="sxs-lookup"><span data-stu-id="26620-131">Here is a summary of the differences.</span></span>

<span data-ttu-id="26620-132">**Planungsoptimierung**</span><span class="sxs-lookup"><span data-stu-id="26620-132">**Planning Optimization**</span></span>

- <span data-ttu-id="26620-133">Die automatische Bestätigung basiert auf dem Auftragsdatum (Startdatum).</span><span class="sxs-lookup"><span data-stu-id="26620-133">Autofirming is based on the order date (start date).</span></span>
- <span data-ttu-id="26620-134">Da das Auftragsdatum (Startdatum) die Fixierung auslöst, müssen Sie die Durchlaufzeit nicht als Teil des Fixierungszeitfensters betrachten.</span><span class="sxs-lookup"><span data-stu-id="26620-134">Because the order date (start date) triggers the firming, you don't have to consider the lead time as part of the firming time fence.</span></span>
- <span data-ttu-id="26620-135">Wenn Sie alle Aufträge fixieren wollen, die in der aktuellen Woche beginnen müssen, muss der Fixierungszeitrahmen eine Woche betragen.</span><span class="sxs-lookup"><span data-stu-id="26620-135">If you want to firm all orders that must start during the current week, the firming time fence must be one week.</span></span>

<span data-ttu-id="26620-136">**Integrierte Supply Chain Management Planungs-Engine**</span><span class="sxs-lookup"><span data-stu-id="26620-136">**Built-in Supply Chain Management planning engine**</span></span>

- <span data-ttu-id="26620-137">Die automatische Bestätigung basiert auf dem Bedarfsdatum (Enddatum).</span><span class="sxs-lookup"><span data-stu-id="26620-137">Autofirming is based on the requirement date (end date).</span></span>
- <span data-ttu-id="26620-138">Um eine rechtzeitige Auftragsfeststellung zu gewährleisten, muss der Fixierungszeitrahmen länger als die Vorlaufzeit sein.</span><span class="sxs-lookup"><span data-stu-id="26620-138">To help guarantee that orders are firmed in due time, the firming time fence must be longer than the lead time.</span></span>
- <span data-ttu-id="26620-139">Wenn Sie alle Aufträge fixieren wollen, die in der aktuellen Woche beginnen müssen, muss der Fixierungszeitrahmen die Durchlaufzeit plus eine Woche sein.</span><span class="sxs-lookup"><span data-stu-id="26620-139">If you want to firm all orders that must start during the current week, the firming time fence must be the lead time plus one week.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
