---
title: "Fertigmeldung für Produktionsaufträge"
description: "Einen Produktionsauftrag als abgeschlossen melden. In dieser Phase wird ein Produkt aus dem Produktionsauftrag für Bestand gemeldet und verschoben."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 80a882e51332d87835bdfb41a1bb1fcda2471f02
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="report-production-orders-as-finished"></a><span data-ttu-id="3a216-104">Fertigmeldung für Produktionsaufträge</span><span class="sxs-lookup"><span data-stu-id="3a216-104">Report production orders as finished</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3a216-105">Einen Produktionsauftrag als abgeschlossen melden.</span><span class="sxs-lookup"><span data-stu-id="3a216-105">Report as finished is a production stage.</span></span> <span data-ttu-id="3a216-106">In dieser Phase wird ein Produkt aus dem Produktionsauftrag für Bestand gemeldet und verschoben.</span><span class="sxs-lookup"><span data-stu-id="3a216-106">At this stage, a finished product is reported and moved from the production order to the inventory.</span></span>

<span data-ttu-id="3a216-107">Wenn eine Menge der fertiggestellten Güter auf einem Produktionsauftrag als fertig gemeldet wurde, wird sie im Bestand als verfügbar aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3a216-107">When a quantity of the finished goods is reported as finished on a production order it is updated as on-hand in the inventory.</span></span> <span data-ttu-id="3a216-108">Teilmengen der ursprünglichen geplanten Bestellmenge können als fertig gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="3a216-108">Partial quantities of the originally planned order quantity can be reported as finished.</span></span> <span data-ttu-id="3a216-109">Es ist auch möglich, Ausschussmengen mit einem zugeordneten Fehlergrund zu melden, wenn Mengen als fertig gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="3a216-109">It is also possible to report error quantities with an associated error reason when reporting quantities as finished.</span></span> <span data-ttu-id="3a216-110">Wenn der Produktionsauftrag die Phase „Als fertig gemeldet“ erreicht, bedeutet das, dass keine weitere Menge am Produktionsauftrag fertig gemeldet werden wird.</span><span class="sxs-lookup"><span data-stu-id="3a216-110">When the production order reach the stage Reported as finished it indicates that no more quantity is going to be reported at the production  order.</span></span>
<span data-ttu-id="3a216-111">Die folgenden Merkmale werden auch dem Vorgang **Fertigmeldung** zugeordnet:</span><span class="sxs-lookup"><span data-stu-id="3a216-111">The following characteristics are also associated with the **Report as finished** process:</span></span>
-   <span data-ttu-id="3a216-112">Es ist möglich, den Verbrauch des Rohmaterials und der Zeit einzurichten, die proportional zur gemeldeten Menge sind (Zurückströmen)</span><span class="sxs-lookup"><span data-stu-id="3a216-112">It is possible to set up consumption of raw material and time that are proportional to the reported quantity (back-flushing)</span></span>
-   <span data-ttu-id="3a216-113">Einlagerungsarbeit kann für Artikel generiert werden, die für Lagerortprozesse aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="3a216-113">Put-away work can be generated for items that are enabled for warehouse processes.</span></span>
-   <span data-ttu-id="3a216-114">Geplanter oder Standardkostenwert der Fertigerzeugnisse kann so eingerichtet werden, dass er in die Sachkonten angegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="3a216-114">The planned or standard cost value of the finished goods can be set up to be reported to ledger accounts.</span></span>
-   <span data-ttu-id="3a216-115">Ein Qualitätsprüfungsauftrag kann für die gemeldete Menge auf Grundlage der Einstellungen einer Qualitätszuordnung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3a216-115">A quality order can be created for the reported quantity based on the setup of a quality association.</span></span>

<span data-ttu-id="3a216-116">Die Menge wird für den Ausgangslagerplatz gemeldet.</span><span class="sxs-lookup"><span data-stu-id="3a216-116">The quantity is reported to the output location.</span></span> <span data-ttu-id="3a216-117">Lagerarbeit wird dann generiert, um die Menge vom Ausgangslagerplatz zum endgültigen Bestimmungsort zu verschieben, die durch die Lagerplatzdirektive für die Einlagerungsarbeit definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="3a216-117">Warehouse work is then generated to move the quantity from the output location to its final destination defined by the location directive for the put-away work.</span></span>

-   <span data-ttu-id="3a216-118">Ein Qualitätsprüfungsauftrag kann erstellt werden, wenn ein Produktionsauftrag als fertig gemeldet wird, wenn eine Qualitätszuordnung eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="3a216-118">A quality order can be created when a production order is reported as finished if a quality association has been set up.</span></span>

## <a name="set-a-production-order-to-reporting-as-finished"></a><span data-ttu-id="3a216-119">Produktionsauftrag als Fertigmeldung einrichten</span><span class="sxs-lookup"><span data-stu-id="3a216-119">Set a production order to Reporting as finished</span></span>
<span data-ttu-id="3a216-120">Sie können einen Produktionsauftrag auf **Fertigmeldung** setzen, über die standardmäßige Aktualisierungsfunktion des Produktionsauftrags, oder durch die Übersichtserfassungen für Arbeitspläne und Einzelvorgänge, oder über die Erfassung **Fertigmeldung**.</span><span class="sxs-lookup"><span data-stu-id="3a216-120">You can set a production order to **Report as finished** through the standard production order update function, or through the route and job card journals, or through the journal **Report as finished**.</span></span> <span data-ttu-id="3a216-121">Sie können die Phase auch auf **Fertigmeldung** über die Einzelvorgangslistenterminal- und Einzelvorgangslistengerätenseiten aktualisieren, wenn Sie zum letzten Einzelvorgang des Produktionsauftrags melden.</span><span class="sxs-lookup"><span data-stu-id="3a216-121">You can also update the stage to **Report as finished** through the job card terminal and job card device pages, when you report on the last job of the production order.</span></span> <span data-ttu-id="3a216-122">Abschließend können Sie die Option **Fertigmeldung** als Prozess für die Handheld-Lösung am Lagerort aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3a216-122">Finally, you can enable the **Report as finished** option as a process for the handheld warehouse device solution.</span></span>  




