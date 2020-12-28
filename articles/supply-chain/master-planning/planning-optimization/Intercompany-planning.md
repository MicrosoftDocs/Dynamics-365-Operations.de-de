---
title: Intercompany-Planung
description: Dieses Thema beschreibt die Intercompany-Planung und erklärt, wie Sie die Intercompany-Planung mit der Planungsoptimierung in Microsoft Dynamics 365 Supply Chain Management konfigurieren.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 25c80ce27498131c6eb92174ab14a592bfa9915a
ms.sourcegitcommit: fe21a3a98dcf6fe4eb9351941493f2c0443d8696
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672186"
---
# <a name="intercompany-planning"></a><span data-ttu-id="0b3ed-103">Intercompany-Planung</span><span class="sxs-lookup"><span data-stu-id="0b3ed-103">Intercompany planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b3ed-104">Für einige Organisationen hängen logistische Operationen von anderen juristischen Entitäten (Firmen) in der Organisation ab.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-104">For some organizations, logistics operations depend on other legal entities (companies) in the organization.</span></span> <span data-ttu-id="0b3ed-105">Diese Vorgänge werden über Intercompany-Verkäufe und -Einkäufe abgewickelt, da jede juristische Entität einen eigenen Kontenplan hat.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-105">These operations are handled by using intercompany sales and purchases, because each legal entity has a separate chart of accounts.</span></span>

<span data-ttu-id="0b3ed-106">Dieses Thema beschreibt die Intercompany-Planung und erklärt, wie Sie die Intercompany-Planung mit der Planungsoptimierung in Microsoft Dynamics 365 Supply Chain Management konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-106">This topic describes intercompany planning and explains how to configure intercompany planning with Planning Optimization in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="0b3ed-107">In diesem Thema werden die folgenden wichtigen Intercompany-Begriffe verwendet:</span><span class="sxs-lookup"><span data-stu-id="0b3ed-107">This topic uses the following important intercompany terms:</span></span>

- <span data-ttu-id="0b3ed-108">**Aufwärts** - Eine relative Referenz in einer Firma oder Lieferkette.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-108">**Upstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="0b3ed-109">Er zeigt die Bewegung in Richtung des Rohstofflieferanten an.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-109">It indicates movement in the direction of the raw material supplier.</span></span>
- <span data-ttu-id="0b3ed-110">**Abwärts** - Ein relativer Verweis in einer Firma oder Lieferkette.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-110">**Downstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="0b3ed-111">Er zeigt die Bewegung in Richtung des Kunden an.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-111">It indicates movement in the direction of the customer.</span></span>
- <span data-ttu-id="0b3ed-112">**Geplanter Intercompany-Bedarf** - Geplanter Bedarf für ein Produkt in einem Unternehmen, basierend auf dem geplanten Bedarf für das Produkt von einem nachgelagerten Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-112">**Planned intercompany demand** – Planned demand for a product in a company, based on planned demand for the product from a downstream company.</span></span>

<span data-ttu-id="0b3ed-113">In der Produktprogrammplanung kann ein Plan in einem Unternehmen einen geplanten Intercompany-Bedarf enthalten, der sich auf geplante Aufträge aus einem Plan in einem anderen Unternehmen bezieht.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-113">In master planning, a plan in one company can include planned intercompany demand that is related to planned orders from a plan in another company.</span></span> <span data-ttu-id="0b3ed-114">Diese Funktionalität ist nützlich, da sie einen vollständigen Überblick über die geplanten Aufträge in allen Unternehmen bietet.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-114">This capability is useful, because it provides full visibility into planned orders across companies.</span></span> <span data-ttu-id="0b3ed-115">Sie stellt auch sicher, dass alle erforderlichen geplanten Lieferaufträge erstellt werden, ohne dass jedoch Planaufträge für den Intercompany-Bedarf umgewandelt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-115">It also ensures that all required planned supply orders are created, but without requiring that planned orders be firmed for the intercompany demand.</span></span>

<span data-ttu-id="0b3ed-116">Wenn Sie die Produktprogrammplanung von einem Masterplan aus durchführen, der geplanten nachgelagerten Bedarf enthält, werden geplante Einkaufsbestellungen von den entsprechenden Intercompany-Lieferanten als Bedarf in den Plan aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-116">If you run master planning from a master plan that includes planned downstream demand, planned purchase orders from the related intercompany vendors will be included in the plan as demand.</span></span>

## <a name="required-setup"></a><span data-ttu-id="0b3ed-117">Erforderliches Einrichten</span><span class="sxs-lookup"><span data-stu-id="0b3ed-117">Required setup</span></span>

<span data-ttu-id="0b3ed-118">Um die Intercompany-Planung zu verwenden, müssen Sie Ihr System wie folgt vorbereiten:</span><span class="sxs-lookup"><span data-stu-id="0b3ed-118">To use intercompany planning, you must prepare your system in the following way:</span></span>

1. <span data-ttu-id="0b3ed-119">Die relevanten Produkte müssen in allen relevanten Firmen freigegeben sein.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-119">The relevant products must be released in all the relevant companies.</span></span> <span data-ttu-id="0b3ed-120">Weitere Informationen finden Sie unter [Konfigurieren und verwenden Sie Intercompany-Handel in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) auf Microsoft Learn.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-120">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="0b3ed-121">Der nachgelagerte Bedarf muss durch Einkäufe bei einem Lieferanten gedeckt werden, der eine Intercompany-Beziehung zum vorgelagerten Unternehmen und entsprechende Standard-Bestandsdimensionen (Standort und Lagerort) beim Kunden hat.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-121">Downstream demand must be covered by purchases from a vendor that has an intercompany relation to the upstream company and relevant default inventory dimensions (site and warehouse) on the customer.</span></span> <span data-ttu-id="0b3ed-122">Weitere Informationen finden Sie unter [Konfigurieren und verwenden Sie Intercompany-Handel in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) auf Microsoft Learn.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-122">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="0b3ed-123">Der Masterplan im vorgelagerten Unternehmen muss den geplanten nachgelagerten Bedarf enthalten, und das entsprechende Unternehmen und der Masterplan müssen in den nachgelagerten Plänen angegeben sein.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-123">The master plan in the upstream company must include planned downstream demand, and the relevant company and master plan must be specified in the downstream plans.</span></span>

## <a name="include-planned-downstream-demand"></a><span data-ttu-id="0b3ed-124">Geplanten Downstream-Bedarf einschließen</span><span class="sxs-lookup"><span data-stu-id="0b3ed-124">Include planned downstream demand</span></span>

<span data-ttu-id="0b3ed-125">Gehen Sie wie folgt vor, um Ihren Masterplan so zu konfigurieren, dass er den geplanten nachgelagerten Bedarf enthält.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-125">Follow these steps to configure your master plan so that it includes planned downstream demand.</span></span>

1. <span data-ttu-id="0b3ed-126">Wechseln Sie zu **Produktprogrammplanung \> Einrichtung \> Pläne \> Produktprogrammpläne**.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-126">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="0b3ed-127">Wählen oder erstellen Sie einen Masterplan.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-127">Select or create a master plan.</span></span>
1. <span data-ttu-id="0b3ed-128">Legen Sie auf dem Inforegister **Intercompany-Planung** die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="0b3ed-128">On the **Intercompany planning** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="0b3ed-129">**Geplanten nachgelagerten Bedarf einbeziehen** - Legen Sie diese Option auf *Ja* fest, um die Intercompany-Planung für den Masterplan zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-129">**Include planned downstream demand** – Set this option to *Yes* to enable intercompany planning for the master plan.</span></span>
    - <span data-ttu-id="0b3ed-130">**Nachgelagerte Pläne** - Wenn Sie die Option **Geplanten nachgelagerten Bedarf einbeziehen** auf *Ja* festlegen, verwenden Sie die Symbolleiste und das Raster, um die gewünschten Produktprogrammplanungen von anderen Unternehmen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-130">**Downstream plans** – If you set the **Include planned downstream demand** option to *Yes*, use the toolbar and grid to add the desired master plans from other companies.</span></span>

## <a name="peg-across-companies-by-using-multilevel-pegging"></a><span data-ttu-id="0b3ed-131">Firmenübergreifende Bedarfsverursacher mit Hilfe des mehrstufigen Bedarfsverursachers</span><span class="sxs-lookup"><span data-stu-id="0b3ed-131">Peg across companies by using multilevel pegging</span></span>

<span data-ttu-id="0b3ed-132">Bei mehrstufigen Bedarfsverursachern können Sie den Bedarfsverursacher firmenübergreifend anzeigen, um die ursprüngliche Bedarfsquelle zu sehen, die durch ein Angebot abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-132">In multilevel pegging, you can view pegging across companies to see the initial source of demand that is being covered by a supply.</span></span>

<span data-ttu-id="0b3ed-133">Führen Sie die folgenden Schritte aus, um Informationen zum mehrstufigen Bedarfsverursacher anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-133">To view multilevel pegging information, follow these steps.</span></span>

1. <span data-ttu-id="0b3ed-134">Gehen Sie zu **Produktprogrammplanung \> Gesamtplanung \> Geplante Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-134">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="0b3ed-135">Wählen oder öffnen Sie einen Planauftrag.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-135">Select or open a planned order.</span></span>
1. <span data-ttu-id="0b3ed-136">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Ansicht** in der Gruppe **Bedarf** die Option **Mehrstufiger Bedarfsverursacher**.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-136">On the Action Pane, on the **View** tab, in the **Requirements** group, select **Multilevel pegging**.</span></span>

### <a name="intercompany-example-that-involves-two-companies"></a><span data-ttu-id="0b3ed-137">Intercompany-Beispiel, an dem zwei Firmen beteiligt sind</span><span class="sxs-lookup"><span data-stu-id="0b3ed-137">Intercompany example that involves two companies</span></span>

<span data-ttu-id="0b3ed-138">In diesem Beispiel wird in der Firma USMF ein geplanter Fertigungsauftrag erstellt, um einen Auftrag in der Firma DEMF zu decken.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-138">For this example, a planned production order is created in the USMF company to cover a sales order in the DEMF company.</span></span> <span data-ttu-id="0b3ed-139">In USMF ist der direkte Bedarf ein geplanter Intercompany-Bedarf.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-139">In USMF, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="0b3ed-140">Um diesen Bedarf in USMF erscheinen zu lassen, wird die Produktprogrammplanung zuerst in DEMF und dann in USMF ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-140">To make this demand appear in USMF, master planning is run first in DEMF and then in USMF.</span></span>

<span data-ttu-id="0b3ed-141">Die folgende Abbildung zeigt, wie dieses Beispiel auf der Seite **Multilevel Bedarfsverursacher** für den geplanten Produktionsauftrag erscheinen könnte.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-141">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Intercompany-Beispiel, an dem zwei Firmen beteiligt sind](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a><span data-ttu-id="0b3ed-143">Intercompany-Beispiel, an dem drei Firmen beteiligt sind</span><span class="sxs-lookup"><span data-stu-id="0b3ed-143">Intercompany example that involves three companies</span></span>

<span data-ttu-id="0b3ed-144">Für dieses Beispiel wird eine geplante Einkaufsbestellung in der USMF-Firma erstellt, um einen Auftrag in der FRRT-Firma zu decken.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-144">For this example, a planned purchase order is created in the USMF company to cover a sales order in the FRRT company.</span></span> <span data-ttu-id="0b3ed-145">In den Firmen DEMF und USMF ist der direkte Bedarf ein geplanter Intercompany-Bedarf.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-145">In the DEMF and USMF companies, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="0b3ed-146">Um diesen Bedarf in USMF erscheinen zu lassen, wird die Produktprogrammplanung zuerst in FRRT, dann in DEMF und schließlich in USMF ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-146">To make this demand appear in USMF, master planning is run first in FRRT, then in DEMF, and finally in USMF.</span></span>

<span data-ttu-id="0b3ed-147">Die folgende Abbildung zeigt, wie dieses Beispiel auf der Seite **Multilevel Bedarfsverursacher** für den geplanten Produktionsauftrag erscheinen könnte.</span><span class="sxs-lookup"><span data-stu-id="0b3ed-147">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Intercompany-Beispiel, an dem drei Firmen beteiligt sind](media/IntercompanyPlanning2.png)
