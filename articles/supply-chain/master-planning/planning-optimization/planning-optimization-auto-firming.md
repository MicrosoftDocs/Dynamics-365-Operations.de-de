---
title: Automatische Umwandlung mit Planungsoptimierung
description: In diesem Abschnitt wird erläutert, wie Sie die automatische Fixierung mit der Planungsoptimierung verwenden.
author: ChristianRytt
manager: AnnBe
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 90319222e7357d7c54243faa8c64575377348467
ms.sourcegitcommit: 0138b6c108a10f2bcb90c91205da8092917160d8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2783152"
---
# <a name="auto-firming-with-planning-optimization"></a><span data-ttu-id="9d0ef-103">Automatische Umwandlung mit Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="9d0ef-103">Auto-firming with Planning Optimization</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9d0ef-104">Mit der automatischen Fixierung können Sie Planaufträge im Rahmen des Masterplanungsprozesses fixieren (d.h. freigeben).</span><span class="sxs-lookup"><span data-stu-id="9d0ef-104">Automatic firming lets you firm (that is, release) planned orders as part of the master planning process.</span></span> <span data-ttu-id="9d0ef-105">Wenn Planaufträge fixiert werden, werden sie in Ist-Bestellungen, Transportaufträge oder Fertigungsaufträge umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-105">When planned orders are firmed, they are transformed into actual purchase orders, transfer orders, or production orders.</span></span> <span data-ttu-id="9d0ef-106">Bei der Planungsoptimierung werden Planaufträge während eines Masterplanungslaufs fixiert, wenn das Auftragsdatum (d.h. das Startdatum) innerhalb des Zeitfensters für die Fixierung liegt.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-106">When Planning Optimization is used, planned orders are firmed during a master planning run when the order date (that is, the start date) is within the time fence for firming.</span></span>

> [!NOTE]
> <span data-ttu-id="9d0ef-107">Die automatische Bestätigung einer geplanten Bestellung kann nur erfolgen, wenn die Position einem Lieferanten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-107">Auto-firming of a planned purchase order can occur only if the item is associated with a vendor.</span></span>

## <a name="turn-on-auto-firming"></a><span data-ttu-id="9d0ef-108">Einschalten der automatischen Bestätigung</span><span class="sxs-lookup"><span data-stu-id="9d0ef-108">Turn on auto-firming</span></span>

<span data-ttu-id="9d0ef-109">Um die automatische Bestätigung einzuschalten, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-109">To turn on auto-firming, follow these steps.</span></span>

1. <span data-ttu-id="9d0ef-110">Wählen Sie im Arbeitsbereich **Feature-Management** auf der Registerkarte **Neu** **Automatische Umwandlung zur Planungsoptimierung** in der Liste.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-110">In the **Feature management** workspace, on the **New** tab, select **Auto-firming for Planning Optimization** in the list.</span></span> <span data-ttu-id="9d0ef-111">Wenn die Funktion nicht auf der Registerkarte **Neu** erscheint, schauen Sie auf die Registerkarten **Nicht aktiviert** und **Alle**.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="9d0ef-112">Wählen Sie **Jetzt aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-112">Select **Enable now**.</span></span> <span data-ttu-id="9d0ef-113">Alternativ können Sie auch **Terminplanung** wählen und dann die Zeit auswählen, zu der die Funktion eingeschaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

## <a name="set-up-the-firming-time-fence"></a><span data-ttu-id="9d0ef-114">Den Fixierzeitanschlag einrichten</span><span class="sxs-lookup"><span data-stu-id="9d0ef-114">Set up the firming time fence</span></span>

<span data-ttu-id="9d0ef-115">Der Fixierungszeitrahmen wird aus dem Laufdatum der Masterplanung vorwärts berechnet.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-115">The firming time fence is calculated forward from the master planning run date.</span></span> <span data-ttu-id="9d0ef-116">Sie wird durch die Anzahl der Tage definiert, die Sie eingeben.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-116">It's defined by the number of days that you enter.</span></span> <span data-ttu-id="9d0ef-117">Sie können den Fixierungszeitanschlag wie folgt steuern:</span><span class="sxs-lookup"><span data-stu-id="9d0ef-117">You can control the firming time fence in the following ways:</span></span>

- <span data-ttu-id="9d0ef-118">Um den voreingestellten Fixierungszeitrahmen für eine Deckungsgruppe zu definieren, gehen Sie zu **Masterplanung** \> **Einrichtung** \> **Deckung** \> **Deckungsgruppen** und wählen eine Deckungsgruppe aus.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-118">To define the default firming time fence for a coverage group, go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**, and select a coverage group.</span></span> <span data-ttu-id="9d0ef-119">Geben Sie dann auf der Registerkarte **Anderes** Inforegister im Feld **Automatischer Fixierungszeitrahmen (Tage)** die Anzahl der Tage ein.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-119">Then, on the **Other** FastTab, in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="9d0ef-120">Um den Fixierungszeitrahmen zu überschreiben, der für die Deckungsgruppe eines bestimmten Artikels definiert ist, gehen Sie zu **Produktinformationsmanagement** \> **Freigegebene Produkte**, wählen Sie dann aus dem Aktionsbereich **Plan** und wählen Sie dann **Artikelabdeckung**.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-120">To overwrite the firming time fence that is defined for the coverage group for a specific item, go to **Product information management** \> **Released products**, then from the action pane select **Plan** and then select **Item coverage**.</span></span> <span data-ttu-id="9d0ef-121">Wählen Sie dann auf der Registerkarte **Allgemein** **Überschreibungszeitraum** und geben Sie im Feld **Automatischer Fixierungszeitrahmen (Tage)** die Anzahl der Tage ein.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-121">Then, on the **General** tab, select **Override time fence** and in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="9d0ef-122">Um den Fixierungszeitrahmen zu überschreiben, der für die Deckungsgruppe und die Artikelabdeckung für einen bestimmten Produktionsplan definiert ist, gehen Sie zu **Masterplanung** \> **Setup** \> **Masterpläne** und wählen Sie einen Produktionsplan.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-122">To overwrite the firming time fence that is defined for the coverage group and item coverage for a specific master plan, go to **Master planning** \> **Setup** \> **Master plans**, and select a Master plan.</span></span> <span data-ttu-id="9d0ef-123">Stellen Sie dann am **Zeitrahmen in Tagen** Inforegister **Fixieren** auf **Ja** und geben Sie die Anzahl der Tage ein.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-123">Then, on the **Time fence in days** FastTab, set **Freeze** to **Yes**, and enter the number of days.</span></span>

<span data-ttu-id="9d0ef-124">Wenn die automatische Bestätigung für einen Masterplanungslauf mit Planungsoptimierung eingeschaltet ist, wird der automatische Bestätigungsprozess entsprechend dem Setup der automatischen Bestätigung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-124">If auto-firming is turned on for a master planning run that uses Planning Optimization, the auto-firming process is done according to the auto-firming setup.</span></span> <span data-ttu-id="9d0ef-125">Wenn die automatische Bestätigung nicht eingeschaltet ist oder wenn die Planung von der Seite **Nettobedarf** aus gestartet wird, wird der automatische Bestätigungsprozess übersprungen.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-125">If auto-firming isn't turned on, or if planning is started from the **Net requirements** page, the auto-firming process is skipped.</span></span>

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a><span data-ttu-id="9d0ef-126">Planungsoptimierung im Vergleich zur integrierten Supply Chain Management Planungs-Engine</span><span class="sxs-lookup"><span data-stu-id="9d0ef-126">Planning Optimization vs. the built-in Supply Chain Management planning engine</span></span>

<span data-ttu-id="9d0ef-127">Sowohl die Planungsoptimierung als auch die in Microsoft Dynamics 365 Supply Chain Management integrierte Planungs-Engine können zur automatischen Fixierung von Planaufträgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-127">Both Planning Optimization and the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management can be used to auto-firm planned orders.</span></span> <span data-ttu-id="9d0ef-128">Jedoch gibt es mehrere wichtige Unterschiede.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-128">However, there are some important differences.</span></span> <span data-ttu-id="9d0ef-129">Während die Planungsoptimierung beispielsweise anhand des Auftragsdatums (d.h. des Startdatums) ermittelt, welche Planaufträge zu fixieren sind, verwendet die integrierte Supply Chain Management Planungs-Engine das Bedarfsdatum (d.h. das Enddatum).</span><span class="sxs-lookup"><span data-stu-id="9d0ef-129">For example, whereas Planning Optimization uses the order date (that is, the start date) to determine which planned orders to firm, the built-in Supply Chain Management planning engine uses the requirement date (that is, the end date).</span></span> <span data-ttu-id="9d0ef-130">Hier ist eine Zusammenfassung der Unterschiede.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-130">Here is a summary of the differences.</span></span>

<span data-ttu-id="9d0ef-131">**Planungsoptimierung**</span><span class="sxs-lookup"><span data-stu-id="9d0ef-131">**Planning Optimization**</span></span>

- <span data-ttu-id="9d0ef-132">Die automatische Bestätigung basiert auf dem Bestelldatum (Startdatum).</span><span class="sxs-lookup"><span data-stu-id="9d0ef-132">Auto-firming is based on the order date (start date).</span></span>
- <span data-ttu-id="9d0ef-133">Da das Auftragsdatum (Startdatum) die Fixierung auslöst, müssen Sie die Durchlaufzeit nicht als Teil des Fixierungszeitfensters betrachten.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-133">Because the order date (start date) triggers the firming, you don't have to consider the lead time as part of the firming time fence.</span></span>
- <span data-ttu-id="9d0ef-134">Wenn Sie alle Aufträge fixieren wollen, die in der aktuellen Woche beginnen müssen, muss der Fixierungszeitrahmen eine Woche betragen.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-134">If you want to firm all orders that must start during the current week, the firming time fence must be one week.</span></span>

<span data-ttu-id="9d0ef-135">**Integrierte Supply Chain Management Planungs-Engine**</span><span class="sxs-lookup"><span data-stu-id="9d0ef-135">**Built-in Supply Chain Management planning engine**</span></span>

- <span data-ttu-id="9d0ef-136">Die automatische Bestätigung basiert auf dem Bedarfstermin (Enddatum).</span><span class="sxs-lookup"><span data-stu-id="9d0ef-136">Auto-firming is based on the requirement date (end date).</span></span>
- <span data-ttu-id="9d0ef-137">Um eine rechtzeitige Auftragsfeststellung zu gewährleisten, muss der Fixierungszeitrahmen länger als die Vorlaufzeit sein.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-137">To help guarantee that orders are firmed in due time, the firming time fence must be longer than the lead time.</span></span>
- <span data-ttu-id="9d0ef-138">Wenn Sie alle Aufträge fixieren wollen, die in der aktuellen Woche beginnen müssen, muss der Fixierungszeitrahmen die Durchlaufzeit plus eine Woche sein.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-138">If you want to firm all orders that must start during the current week, the firming time fence must be the lead time plus one week.</span></span>
