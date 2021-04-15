---
title: Bestandskennzeichnung mit Planungsoptimierung
description: Dieses Thema enthält Informationen über die Optionen, die für die Markierung von Beständen in umgewandelten Aufträgen zur Verfügung stehen, wenn Sie die Planungsoptimierung verwenden.
author: ChristianRytt
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 3b139673ddf17e13d6687db485208e1aeb3908dc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809493"
---
# <a name="inventory-marking-with-planning-optimization"></a><span data-ttu-id="791af-103">Bestandskennzeichnung mit Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="791af-103">Inventory marking with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="791af-104">Dieses Thema enthält Informationen über die Optionen, die für die Markierung von Beständen in umgewandelten Aufträgen zur Verfügung stehen, wenn Sie die Planungsoptimierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="791af-104">This topic provides information about the options that are available for marking inventory in firmed orders when you use Planning Optimization.</span></span>

<span data-ttu-id="791af-105">*Markierung* wird verwendet, um Angebot und Nachfrage zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="791af-105">*Marking* is used to link supply and demand.</span></span> <span data-ttu-id="791af-106">Sie ähnelt dem *Bedarfsverursacher*, der angibt, wie die Produktprogrammplanung die Nachfrage zu decken gedenkt.</span><span class="sxs-lookup"><span data-stu-id="791af-106">It resembles *pegging*, which indicates how master planning expects to cover demand.</span></span> <span data-ttu-id="791af-107">Aus Sicht der Planung besteht der Hauptunterschied darin, dass die Markierung dauerhafter ist als der Bedarfsverursacher.</span><span class="sxs-lookup"><span data-stu-id="791af-107">From a planning point of view, the main difference is that marking is more permanent than pegging.</span></span>

<span data-ttu-id="791af-108">Die Markierung wurde eingeführt, um spezielle Kalkulationsszenarien für First In, First Out (FIFO) und Last In, First Out (LIFO) zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="791af-108">Marking was introduced to support special costing scenarios for first in, first out (FIFO) and last in, first out (LIFO).</span></span> <span data-ttu-id="791af-109">Sie wird jetzt aber auch für einige Nicht-Kalkulationsszenarien verwendet.</span><span class="sxs-lookup"><span data-stu-id="791af-109">However, it's now also used for some non-costing scenarios.</span></span> <span data-ttu-id="791af-110">Die Markierung zwischen Angebot und Nachfrage ist optional und fast permanent.</span><span class="sxs-lookup"><span data-stu-id="791af-110">Marking between supply and demand is optional and almost permanent.</span></span> <span data-ttu-id="791af-111">Die Markierung kann manuell von einem Benutzer entfernt werden, oder sie kann durch die Ausführung einer Verkaufsauftragszeilenauflösung entfernt werden, bei der die Option **Markierung entfernen** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="791af-111">Marking can be removed manually by a user, or it can be removed by running a sales order line explosion where the **Remove marking** option is selected.</span></span>

<span data-ttu-id="791af-112">Die Bedarfsverursacher werden von der Produktprogrammplanung während der Deckung gesteuert, um die Nachfrage mit dem benötigten Angebot zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="791af-112">Pegging is controlled by master planning during coverage to link demand with the required supply.</span></span> <span data-ttu-id="791af-113">Die Bedarfsverursacher können für jeden Planungslauf aktualisiert werden, um das Angebot zu optimieren, das zur Deckung der Nachfrage erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="791af-113">Pegging can be updated for each planning run to optimize the supply that is required to cover demand.</span></span> <span data-ttu-id="791af-114">Wenn die Produktprogrammplanung Bedarfsverursacher-Informationen aktualisiert, berücksichtigt sie alle vorhandenen Markierungen.</span><span class="sxs-lookup"><span data-stu-id="791af-114">When master planning updates pegging information, it respects any existing marking.</span></span>

<span data-ttu-id="791af-115">Der Bedarfsverursacher beginnt mit der Einbeziehung relevanter Markierungen, Bestandsreservierungen und Bestellreservierungen in der folgenden Sequenz:</span><span class="sxs-lookup"><span data-stu-id="791af-115">Pegging starts by including relevant marking, on-hand reservations, and on-order reservations, in the following sequence:</span></span>

1. <span data-ttu-id="791af-116">Markierung zwischen Bedarf und Angebot</span><span class="sxs-lookup"><span data-stu-id="791af-116">Marking between demand and supply</span></span>
1. <span data-ttu-id="791af-117">Bestandsreservierungen</span><span class="sxs-lookup"><span data-stu-id="791af-117">On-hand reservations</span></span>
1. <span data-ttu-id="791af-118">Reservierungen auf Bestellung</span><span class="sxs-lookup"><span data-stu-id="791af-118">On-order reservations</span></span>

<span data-ttu-id="791af-119">Wenn Sie einen Planauftrag umwandeln, bietet die Dialogbox **Umwandlung** ein Feld **Bestandsmarkierung aktualisieren**, mit dem Sie Markierungsoptionen für die Aufträge festlegen können, die während der Umwandlung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="791af-119">When you firm a planned order, the **Firming** dialog box provides an **Update marking** field that you use to set marking options for the orders that are created during firming.</span></span> <span data-ttu-id="791af-120">Wählen Sie einen der folgenden Werte aus:</span><span class="sxs-lookup"><span data-stu-id="791af-120">Select one of the following values:</span></span>

- <span data-ttu-id="791af-121">**Nein** - Es wird keine Bestandsmarkierung angewendet.</span><span class="sxs-lookup"><span data-stu-id="791af-121">**No** – No inventory marking is applied.</span></span>
- <span data-ttu-id="791af-122">**Standard** - Die Bestandsmarkierung wird entsprechend dem Bedarfsverursacher aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="791af-122">**Standard** – Inventory marking is updated according to the pegging.</span></span> <span data-ttu-id="791af-123">Ein Bedarfsauftrag (Nachfrage) wird gegen einen Erfüllungsauftrag (Lieferung) markiert.</span><span class="sxs-lookup"><span data-stu-id="791af-123">A requirement order (demand) is marked against a fulfillment order (supply).</span></span> <span data-ttu-id="791af-124">Wenn eine bestimmte Menge auf dem Erfüllungsauftrag verbleibt, wird sie nicht markiert und die Referenzinformationen bleiben leer.</span><span class="sxs-lookup"><span data-stu-id="791af-124">If some quantity remains on the fulfillment order, it isn't marked, and the reference information is left blank.</span></span> <span data-ttu-id="791af-125">Wenn z. B. ein Verkaufsauftrag über 100 ea gegen eine Einkaufsbestellung über 150 ea verrechnet wird, werden die Referenzinformationen nur dem Verkaufsauftrag zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="791af-125">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned only to the sales order.</span></span>
- <span data-ttu-id="791af-126">**Erweitert** - Sowohl der Bedarfsauftrag (Nachfrage) als auch der Erfüllungsauftrag (Lieferung) werden markiert, unabhängig von der Menge, die auf dem Erfüllungsauftrag verbleibt.</span><span class="sxs-lookup"><span data-stu-id="791af-126">**Extended** – Both the requirement order (demand) and the fulfillment order (supply) are marked, regardless of any quantity that remains on the fulfillment order.</span></span> <span data-ttu-id="791af-127">Wenn z. B. ein Verkaufsauftrag über 100 ea mit einer Einkaufsbestellung über 150 ea verrechnet wird, werden die Referenzinformationen sowohl dem Verkaufsauftrag als auch der Einkaufsbestellung zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="791af-127">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned to both the sales order and the purchase order.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]