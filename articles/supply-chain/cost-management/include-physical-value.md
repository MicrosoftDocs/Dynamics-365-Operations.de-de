---
title: Physischen Wert einbeziehen
description: Verwenden Sie das Kontrollkästchen "Physischen Wert einbeziehen"auf dem Inforegister "Lagermodell" im Formular "Artikelmodellgruppen", um anzugeben, ob physisch aktualisierte Buchungen in der Berechnung des laufenden Durchschnittseinstandspreises für einen Artikel berücksichtigt werden sollen.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e96d5e2a658a027d66663868329cf4eedcb1d46f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "357311"
---
# <a name="include-physical-value"></a><span data-ttu-id="f0ebc-103">Physischen Wert einbeziehen</span><span class="sxs-lookup"><span data-stu-id="f0ebc-103">Include physical value</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0ebc-104">Verwenden Sie das Kontrollkästchen "Physischen Wert einbeziehen"auf dem Inforegister "Lagermodell" im Formular "Artikelmodellgruppen", um anzugeben, ob physisch aktualisierte Buchungen in der Berechnung des laufenden Durchschnittseinstandspreises für einen Artikel berücksichtigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f0ebc-104">You use the Include physical value check box on the Inventory model FastTab of the Item model groups page to specify whether physically updated transactions are considered when the running average cost price is calculated for an item.</span></span>

<span data-ttu-id="f0ebc-105">Das Kontrollkästchen **Physischen Wert einbeziehen** weist die folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="f0ebc-105">The **Include physical value** check box has the following values.</span></span>

| <span data-ttu-id="f0ebc-106">Wert</span><span class="sxs-lookup"><span data-stu-id="f0ebc-106">Value</span></span>    | <span data-ttu-id="f0ebc-107">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="f0ebc-107">Result</span></span>                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ebc-108">Ausgewählt</span><span class="sxs-lookup"><span data-stu-id="f0ebc-108">Selected</span></span> | <span data-ttu-id="f0ebc-109">Sowohl physisch als auch wertmäßig aktualisierte Buchungen werden verwendet, um den laufenden Durchschnittseinstandspreis zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="f0ebc-109">Both physically updated transactions and financially updated transactions are used to calculate the running average cost price.</span></span> |
| <span data-ttu-id="f0ebc-110">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="f0ebc-110">Cleared</span></span>  | <span data-ttu-id="f0ebc-111">Es werden nur wertmäßig aktualisierte Buchungen verwendet, um den laufenden Durchschnittseinstandspreis zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="f0ebc-111">Only financially updated transactions are used to calculate the running average cost price.</span></span>                                     |

<span data-ttu-id="f0ebc-112">Die Verwendung des Kontrollkästchens hat je nach genutztem Lagermodell etwas andere Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="f0ebc-112">The check box has slightly different effects, depending on the inventory model that you use.</span></span>

-   <span data-ttu-id="f0ebc-113">Wird das Kontrollkästchen **Physischen Wert einbeziehen** bei Verwendung eines Lagermodells vom Typ "FIFO" (First in, first out), "LIFO" (Last in, first out) oder "LIFO-Datum" aktiviert, hat der Lagerabschluss auch Änderungen an physisch aktualisierten Buchungen zur Folge.</span><span class="sxs-lookup"><span data-stu-id="f0ebc-113">If you select the **Include physical value** check box when you use the FIFO (First in, first out), LIFO (Last in, first out), or LIFO date inventory model, inventory close also makes adjustments to physically updated transactions.</span></span>
-   <span data-ttu-id="f0ebc-114">Wird das Kontrollkästchen **Physischen Wert einbeziehen** bei Verwendung dieser Lagermodelle nicht aktiviert, werden beim Lagerabschluss lediglich Ausgleichsvorgänge für wertmäßig aktualisierte Buchungen vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="f0ebc-114">If you don't select the **Include physical value** check box when you use these inventory models, inventory close makes settlements only to financially updated transactions.</span></span>
-   <span data-ttu-id="f0ebc-115">Bei Verwendung des Lagermodells mit gewichtetem Durchschnitt oder Datum für gewichteten Durchschnitt werden beim Lagerabschluss lediglich wertmäßig aktualisierte Buchungen ausgeglichen. Der Status des Kontrollkästchens **Physischen Wert einbeziehen** spielt in diesem Fall keine Rolle.</span><span class="sxs-lookup"><span data-stu-id="f0ebc-115">When you use the weighted average or weighted average date inventory model, inventory close settles only financially updated transactions, regardless of whether you select the **Include physical value** check box.</span></span>

<span data-ttu-id="f0ebc-116">**Beispiel 1** Bei aktiviertem Kontrollkästchen**Physischen Wert einbeziehen** gehen die folgenden Bestellungen ein:</span><span class="sxs-lookup"><span data-stu-id="f0ebc-116">**Example 1** You've selected the **Include physical value** check box and receive the following purchase orders:</span></span>

-   <span data-ttu-id="f0ebc-117">Eine Bestellung mit einer Menge von 2 zu einem Einstandspreis von EUR 10,00, die auf Grundlage des Lieferscheins aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f0ebc-117">A purchase order for a quantity of 2 and a cost price of USD 10.00 that has been packing slip–updated</span></span>
-   <span data-ttu-id="f0ebc-118">Eine Bestellung mit einer Menge von 3 zu einem Einstandspreis von EUR 12,00, die auf Grundlage einer Rechnung aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f0ebc-118">A purchase order for a quantity of 3 and a cost price of USD 12.00 that has been invoice-updated</span></span>

<span data-ttu-id="f0ebc-119">In diesem Fall beträgt der laufende Durchschnittseinstandspreis EUR 11,20, da für die Einstandspreisberechnung sowohl physisch als auch wertmäßig aktualisierte Buchungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f0ebc-119">In this case, the running average cost price will be USD 11.20, because both physically updated transactions and financially updated transactions are used to calculate the cost price.</span></span> <span data-ttu-id="f0ebc-120">**Beispiel 2** Das Kontrollkästchen **Physischen Wert einbeziehen** ist nicht aktiviert, und der Einstandspreis in den Artikeleinstellungen beträgt EUR 10,00.</span><span class="sxs-lookup"><span data-stu-id="f0ebc-120">**Example 2** You haven't selected the **Include physical value** check box, and the cost price on the item setup is USD 10.00.</span></span> <span data-ttu-id="f0ebc-121">Sie erhalten eine Bestellung mit einer Menge von 20 zu einem Einstandspreis von EUR 12,00, die auf Grundlage des Lieferscheins aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f0ebc-121">You receive a purchase order for a quantity of 20 and a cost price of USD 12.00 that has been packing slip–updated.</span></span> <span data-ttu-id="f0ebc-122">Bei der Buchung eines Auftrags wird der Einstandspreis mit EUR 10,00 gebucht, da im laufenden Durchschnittseinstandspreis keine physisch gebuchten Posten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="f0ebc-122">When a sales order is posted, the posted cost amount is USD 10.00, because the running average cost price won't include physically posted transactions.</span></span> <span data-ttu-id="f0ebc-123">**Hinweis:** Wenn Sie zum Vergleich das Kontrollkästchen **Physischen Wert einbeziehen** bei der Auftragsbuchung für diesen Artikel aktivieren, beträgt der gebuchte Einstandspreis EUR 12.00.</span><span class="sxs-lookup"><span data-stu-id="f0ebc-123">**Note:** For comparison, if you select the **Include physical value** check box for this item, when a sales order is posted, the posted cost amount will be USD 12.00.</span></span>



