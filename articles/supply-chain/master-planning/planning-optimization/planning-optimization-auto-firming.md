---
title: Automatische Umwandlung mit Planungsoptimierung
description: In diesem Abschnitt wird erläutert, wie Sie die automatische Fixierung mit der Planungsoptimierung verwenden.
author: ChristianRytt
manager: tfehr
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: d014fcd542462e092f6e88232dff8fd5ee2253c1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963459"
---
# <a name="autofirming-with-planning-optimization"></a><span data-ttu-id="b796c-103">Automatische Umwandlung mit Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="b796c-103">Autofirming with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b796c-104">Mit der automatischen Fixierung können Sie Planaufträge im Rahmen des Masterplanungsprozesses fixieren (d.h. freigeben).</span><span class="sxs-lookup"><span data-stu-id="b796c-104">Automatic firming lets you firm (that is, release) planned orders as part of the master planning process.</span></span> <span data-ttu-id="b796c-105">Wenn Planaufträge fixiert werden, werden sie in Ist-Bestellungen, Transportaufträge oder Fertigungsaufträge umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="b796c-105">When planned orders are firmed, they are transformed into actual purchase orders, transfer orders, or production orders.</span></span> <span data-ttu-id="b796c-106">Bei der Planungsoptimierung werden Planaufträge während eines Masterplanungslaufs fixiert, wenn das Auftragsdatum (d.h. das Startdatum) innerhalb des Zeitfensters für die Fixierung liegt.</span><span class="sxs-lookup"><span data-stu-id="b796c-106">When Planning Optimization is used, planned orders are firmed during a master planning run when the order date (that is, the start date) is within the time fence for firming.</span></span>

> [!NOTE]
> <span data-ttu-id="b796c-107">Die automatische Bestätigung einer geplanten Bestellung kann nur erfolgen, wenn die Position einem Lieferanten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b796c-107">Auto-firming of a planned purchase order can occur only if the item is associated with a vendor.</span></span>

## <a name="turn-on-autofirming"></a><span data-ttu-id="b796c-108">Automatische Umwandlung</span><span class="sxs-lookup"><span data-stu-id="b796c-108">Turn on autofirming</span></span>

<span data-ttu-id="b796c-109">Um die automatische Bestätigung einzuschalten, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="b796c-109">To turn on autofirming, follow these steps.</span></span>

1. <span data-ttu-id="b796c-110">Wählen Sie im Arbeitsbereich **Feature-Management** auf der Registerkarte **Neu** **Automatische Umwandlung zur Planungsoptimierung** in der Liste.</span><span class="sxs-lookup"><span data-stu-id="b796c-110">In the **Feature management** workspace, on the **New** tab, select **Auto-firming for Planning Optimization** in the list.</span></span> <span data-ttu-id="b796c-111">Wenn die Funktion nicht auf der Registerkarte **Neu** erscheint, schauen Sie auf die Registerkarten **Nicht aktiviert** und **Alle**.</span><span class="sxs-lookup"><span data-stu-id="b796c-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="b796c-112">Wählen Sie **Jetzt aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="b796c-112">Select **Enable now**.</span></span> <span data-ttu-id="b796c-113">Alternativ können Sie auch **Terminplanung** wählen und dann die Zeit auswählen, zu der die Funktion eingeschaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b796c-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

## <a name="set-up-the-firming-time-fence"></a><span data-ttu-id="b796c-114">Den Fixierzeitanschlag einrichten</span><span class="sxs-lookup"><span data-stu-id="b796c-114">Set up the firming time fence</span></span>

<span data-ttu-id="b796c-115">Der Fixierungszeitrahmen wird aus dem Laufdatum der Masterplanung vorwärts berechnet.</span><span class="sxs-lookup"><span data-stu-id="b796c-115">The firming time fence is calculated forward from the master planning run date.</span></span> <span data-ttu-id="b796c-116">Sie wird durch die Anzahl der Tage definiert, die Sie eingeben.</span><span class="sxs-lookup"><span data-stu-id="b796c-116">It's defined by the number of days that you enter.</span></span> <span data-ttu-id="b796c-117">Sie können den Fixierungszeitanschlag wie folgt steuern:</span><span class="sxs-lookup"><span data-stu-id="b796c-117">You can control the firming time fence in the following ways:</span></span>

- <span data-ttu-id="b796c-118">Um den voreingestellten Fixierungszeitrahmen für eine Deckungsgruppe zu definieren, gehen Sie zu **Masterplanung** \> **Einrichtung** \> **Deckung** \> **Deckungsgruppen** und wählen eine Deckungsgruppe aus.</span><span class="sxs-lookup"><span data-stu-id="b796c-118">To define the default firming time fence for a coverage group, go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**, and select a coverage group.</span></span> <span data-ttu-id="b796c-119">Geben Sie dann auf der Registerkarte **Anderes** Inforegister im Feld **Automatischer Fixierungszeitrahmen (Tage)** die Anzahl der Tage ein.</span><span class="sxs-lookup"><span data-stu-id="b796c-119">Then, on the **Other** FastTab, in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="b796c-120">Um den Fixierungszeitrahmen zu überschreiben, der für die Deckungsgruppe eines bestimmten Artikels definiert ist, gehen Sie zu **Produktinformationsmanagement** \> **Freigegebene Produkte**, wählen Sie dann aus dem Aktionsbereich **Plan** und wählen Sie dann **Artikelabdeckung**.</span><span class="sxs-lookup"><span data-stu-id="b796c-120">To overwrite the firming time fence that is defined for the coverage group for a specific item, go to **Product information management** \> **Released products**, then from the Action Pane select **Plan** and then select **Item coverage**.</span></span> <span data-ttu-id="b796c-121">Wählen Sie dann auf der Registerkarte **Allgemein** **Überschreibungszeitraum** und geben Sie im Feld **Automatischer Fixierungszeitrahmen (Tage)** die Anzahl der Tage ein.</span><span class="sxs-lookup"><span data-stu-id="b796c-121">Then, on the **General** tab, select **Override time fence** and in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="b796c-122">Um den Fixierungszeitrahmen zu überschreiben, der für die Deckungsgruppe und die Artikelabdeckung für einen bestimmten Produktionsplan definiert ist, gehen Sie zu **Masterplanung** \> **Setup** \> **Masterpläne** und wählen Sie einen Produktionsplan.</span><span class="sxs-lookup"><span data-stu-id="b796c-122">To overwrite the firming time fence that is defined for the coverage group and item coverage for a specific master plan, go to **Master planning** \> **Setup** \> **Master plans**, and select a Master plan.</span></span> <span data-ttu-id="b796c-123">Legen Sie dann auf dem Inforegister **Zeitfenster in Tagen** **Bestätigen** auf **Ja** fest und geben Sie die Anzahl der Tage ein.</span><span class="sxs-lookup"><span data-stu-id="b796c-123">Then, on the **Time fence in days** FastTab, set **Firming** to **Yes**, and enter the number of days.</span></span>

<span data-ttu-id="b796c-124">Wenn die Automatische Umwandlung für eine Produktprogrammplanung, die die Planungsoptimierung verwendet, eingeschaltet ist, wird der Automatische Umwandlung-Prozess gemäß dem Automatische-Umwandlung-Setup durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="b796c-124">If autofirming is turned on for a master planning run that uses Planning Optimization, the autofirming process is done according to the autofirming setup.</span></span> <span data-ttu-id="b796c-125">Wenn Automatische Umwandlung nicht eingeschaltet ist oder wenn die Planung von der Seite **Netzanforderungen** aus gestartet wird, wird der Automatische Umwandlung-Vorgang übersprungen.</span><span class="sxs-lookup"><span data-stu-id="b796c-125">If autofirming isn't turned on, or if planning is started from the **Net requirements** page, the autofirming process is skipped.</span></span>

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a><span data-ttu-id="b796c-126">Planungsoptimierung im Vergleich zur integrierten Supply Chain Management Planungs-Engine</span><span class="sxs-lookup"><span data-stu-id="b796c-126">Planning Optimization vs. the built-in Supply Chain Management planning engine</span></span>

<span data-ttu-id="b796c-127">Sowohl die Planungsoptimierung als auch die in Microsoft Dynamics 365 Supply Chain Management eingebaute Planungs-Engine können zur automatischen Bestätigung von Planaufträgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b796c-127">Both Planning Optimization and the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management can be used to autofirm planned orders.</span></span> <span data-ttu-id="b796c-128">Jedoch gibt es mehrere wichtige Unterschiede.</span><span class="sxs-lookup"><span data-stu-id="b796c-128">However, there are some important differences.</span></span> <span data-ttu-id="b796c-129">Während die Planungsoptimierung beispielsweise anhand des Auftragsdatums (d.h. des Startdatums) ermittelt, welche Planaufträge zu fixieren sind, verwendet die integrierte Supply Chain Management Planungs-Engine das Bedarfsdatum (d.h. das Enddatum).</span><span class="sxs-lookup"><span data-stu-id="b796c-129">For example, whereas Planning Optimization uses the order date (that is, the start date) to determine which planned orders to firm, the built-in Supply Chain Management planning engine uses the requirement date (that is, the end date).</span></span> <span data-ttu-id="b796c-130">Hier ist eine Zusammenfassung der Unterschiede.</span><span class="sxs-lookup"><span data-stu-id="b796c-130">Here is a summary of the differences.</span></span>

<span data-ttu-id="b796c-131">**Planungsoptimierung**</span><span class="sxs-lookup"><span data-stu-id="b796c-131">**Planning Optimization**</span></span>

- <span data-ttu-id="b796c-132">Die automatische Bestätigung basiert auf dem Auftragsdatum (Startdatum).</span><span class="sxs-lookup"><span data-stu-id="b796c-132">Autofirming is based on the order date (start date).</span></span>
- <span data-ttu-id="b796c-133">Da das Auftragsdatum (Startdatum) die Fixierung auslöst, müssen Sie die Durchlaufzeit nicht als Teil des Fixierungszeitfensters betrachten.</span><span class="sxs-lookup"><span data-stu-id="b796c-133">Because the order date (start date) triggers the firming, you don't have to consider the lead time as part of the firming time fence.</span></span>
- <span data-ttu-id="b796c-134">Wenn Sie alle Aufträge fixieren wollen, die in der aktuellen Woche beginnen müssen, muss der Fixierungszeitrahmen eine Woche betragen.</span><span class="sxs-lookup"><span data-stu-id="b796c-134">If you want to firm all orders that must start during the current week, the firming time fence must be one week.</span></span>

<span data-ttu-id="b796c-135">**Integrierte Supply Chain Management Planungs-Engine**</span><span class="sxs-lookup"><span data-stu-id="b796c-135">**Built-in Supply Chain Management planning engine**</span></span>

- <span data-ttu-id="b796c-136">Die automatische Bestätigung basiert auf dem Bedarfsdatum (Enddatum).</span><span class="sxs-lookup"><span data-stu-id="b796c-136">Autofirming is based on the requirement date (end date).</span></span>
- <span data-ttu-id="b796c-137">Um eine rechtzeitige Auftragsfeststellung zu gewährleisten, muss der Fixierungszeitrahmen länger als die Vorlaufzeit sein.</span><span class="sxs-lookup"><span data-stu-id="b796c-137">To help guarantee that orders are firmed in due time, the firming time fence must be longer than the lead time.</span></span>
- <span data-ttu-id="b796c-138">Wenn Sie alle Aufträge fixieren wollen, die in der aktuellen Woche beginnen müssen, muss der Fixierungszeitrahmen die Durchlaufzeit plus eine Woche sein.</span><span class="sxs-lookup"><span data-stu-id="b796c-138">If you want to firm all orders that must start during the current week, the firming time fence must be the lead time plus one week.</span></span>
