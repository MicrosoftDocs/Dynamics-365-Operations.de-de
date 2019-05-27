---
title: Vorzeitige Abschreibung
description: Dieser Artikel enthält eine Übersicht der Bonusabschreibungsfunktionalität.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e05c0c195ddb948547ae008d050686bbcdc6ed3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567482"
---
# <a name="bonus-depreciation"></a><span data-ttu-id="9d85f-103">Vorzeitige Abschreibung</span><span class="sxs-lookup"><span data-stu-id="9d85f-103">Bonus depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d85f-104">Dieser Artikel enthält eine Übersicht der Bonusabschreibungsfunktionalität.</span><span class="sxs-lookup"><span data-stu-id="9d85f-104">This article provides an overview of the bonus depreciation functionality.</span></span>

<span data-ttu-id="9d85f-105">Die vorzeitige Abschreibung ermöglicht es Ihnen, im ersten Jahr der Inbetriebnahme und Abschreibung einer Anlage zusätzliche Abschreibungsbeträge vorzeitig geltend zu machen.</span><span class="sxs-lookup"><span data-stu-id="9d85f-105">For bonus depreciation, you can take extra or bonus depreciation amounts during the first year that the asset is put in service and depreciated.</span></span> <span data-ttu-id="9d85f-106">Vorzeitige Abschreibung muss vor jeder anderen Abschreibungsberechnung durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9d85f-106">Bonus depreciation must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="9d85f-107">Daher empfiehlt es sich, vorzeitige Abschreibung von Büchern zu verwenden, in denen der Anteil an die Hauptbuchfunktionen deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="9d85f-107">Therefore, it's best to use bonus depreciation with books where the Post to general ledger functionality is disabled.</span></span> <span data-ttu-id="9d85f-108">Mithilfe der Option **Löschungsbuchungen nicht im Hauptbuch gebucht** können Sie historische Buchungen für Bücher löschen, die nicht im Hauptbuch gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="9d85f-108">You can use the **Delete transactions not posted to general ledger** option to delete historical transactions for books that don't post to the general ledger.</span></span> <span data-ttu-id="9d85f-109">Sie können die vorzeitige Abschreibung im Anlagenlebenszyklus später aufnehmen, indem Sie Abschreibungsbuchungen löschen, die bereits gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="9d85f-109">You can then accommodate bonus depreciation later in the asset life cycle by deleting depreciation transactions that were previously posted.</span></span> 

<span data-ttu-id="9d85f-110">Sie können die vorzeitige Abschreibung mithilfe des Vorschlagsprozesses berechnen, oder Sie können Buchungen für vorzeitige Abschreibungen manuell erstellen.</span><span class="sxs-lookup"><span data-stu-id="9d85f-110">You can calculate bonus depreciation by using the proposal process, or you can create manual bonus depreciation transactions.</span></span> <span data-ttu-id="9d85f-111">Buchungen für vorzeitige Abschreibungen können nicht erstellt werden, wenn für das jeweilige Anlagenabschreibungsbuch Abschreibungsbuchungen oder Abschreibungsregulierungsbuchungen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="9d85f-111">You can't create bonus depreciation transactions if depreciation transactions or depreciation adjustment transactions exist for that asset book.</span></span>

<span data-ttu-id="9d85f-112">Wird der Vorschlagsprozess zum Berechnen der vorzeitigen Abschreibung verwendet, werden alle vorhandenen Zulagenbuchungen in die Berechnung der Basis einbezogen.</span><span class="sxs-lookup"><span data-stu-id="9d85f-112">When you use the proposal process to calculate bonus depreciation, all existing bonus transactions are included in the calculation of the basis.</span></span> <span data-ttu-id="9d85f-113">In die Berechnung sind auch alle früheren vorzeitigen Abschreibungen eingeschlossen, die manuell für die Anlage eingegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="9d85f-113">The calculation also includes any previous bonus depreciations that you manually entered for the asset.</span></span> 

<span data-ttu-id="9d85f-114">Wenn für eine Anlage mehrere vorzeitige Abschreibungen geltend gemacht werden, wird die Priorität berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="9d85f-114">If more than one bonus depreciation will be taken for an asset, the priority is considered.</span></span> <span data-ttu-id="9d85f-115">Jede Zulage reduziert den Anlagenbasiswert für die nächste Zulage.</span><span class="sxs-lookup"><span data-stu-id="9d85f-115">Each bonus reduces the asset basis for the next bonus.</span></span> <span data-ttu-id="9d85f-116">Der Schrottwert wird bei Berechnung der vorzeitigen Abschreibung nicht in der Anlagenbasis berücksichtigt, und die Abschreibungskonvention gilt nicht für die vorzeitige Abschreibung.</span><span class="sxs-lookup"><span data-stu-id="9d85f-116">Salvage value isn't considered in the asset basis for bonus depreciation calculations, and the depreciation convention doesn't apply for bonus depreciation.</span></span> 

<span data-ttu-id="9d85f-117">In den Vereinigten Staaten werden gegenwärtig bestimmte Anlagen als Anlagen gemäß Abschnitt 179 eingestuft.</span><span class="sxs-lookup"><span data-stu-id="9d85f-117">Currently, in the United States, some property qualifies as Section 179 property.</span></span> <span data-ttu-id="9d85f-118">Beim Abzug gemäß Abschnitt 179 haben Sie die Möglichkeit, die Kosten für bestimmte Anlagen ganz oder teilweise und bis zu einer bestimmten Grenze zurückzuerhalten.</span><span class="sxs-lookup"><span data-stu-id="9d85f-118">By using the Section 179 deduction, you can recover all or part of the cost of some property, up to a limit.</span></span> <span data-ttu-id="9d85f-119">Sie erhalten die Kosten zurück, wenn Sie diese im Jahr der Inbetriebsetzung der Anlage zum Abzug bringen.</span><span class="sxs-lookup"><span data-stu-id="9d85f-119">You can recover the cost by deducting it in the year when you put the property in service.</span></span>

## <a name="example"></a><span data-ttu-id="9d85f-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9d85f-120">Example</span></span>
<span data-ttu-id="9d85f-121">Folgende vorzeitige Abschreibungen sind einem Abschreibungsbuch zugeordnet:</span><span class="sxs-lookup"><span data-stu-id="9d85f-121">The following bonus depreciations are associated with an asset book:</span></span>

-   <span data-ttu-id="9d85f-122">**Abschnitt 179:** 1,000.00, Priorität 1</span><span class="sxs-lookup"><span data-stu-id="9d85f-122">**Section 179:** 1,000.00, Priority 1</span></span>
-   <span data-ttu-id="9d85f-123">**Liberty Zone:** 30 Prozent, Priorität 2</span><span class="sxs-lookup"><span data-stu-id="9d85f-123">**Liberty Zone:** 30 percent, Priority 2</span></span>

<span data-ttu-id="9d85f-124">Die Anlagenanschaffungskosten belaufen sich auf 5.000,00.</span><span class="sxs-lookup"><span data-stu-id="9d85f-124">The asset acquisition cost is 5,000.00.</span></span> <span data-ttu-id="9d85f-125">Bei der Berechnung der vorzeitigen Abschreibung beträgt der erste Abschreibungsbetrag 1.000,00 für die Abschreibung gemäß Abschnitt 179.</span><span class="sxs-lookup"><span data-stu-id="9d85f-125">When bonus depreciation is calculated, the first bonus depreciation amount is 1,000.00 for the Section 179 depreciation.</span></span> 

<span data-ttu-id="9d85f-126">Der nächste Betrag für die vorzeitige Abschreibung für die Liberty Zone-Abschreibung wird wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="9d85f-126">The next bonus depreciation amount, for the Liberty Zone depreciation, is calculated as follows:</span></span> 

<span data-ttu-id="9d85f-127">Anschaffungskosten – 1.000 (Abschreibung gemäß Abschnitt 179) x 30 % = 1.200</span><span class="sxs-lookup"><span data-stu-id="9d85f-127">Acquisition cost – 1,000 (Section 179 depreciation) × 30 percent = 1,200</span></span> 

<span data-ttu-id="9d85f-128">Wenn der Betrag für die vorzeitige Abschreibung höher als die verbleibenden Anschaffungskosten ist, entspricht der Abschreibungsbetrag entweder dem Berechnungsergebnis der vorzeitigen Abschreibung oder den verbleibenden Anschaffungskosten, je nachdem, welcher Betrag geringer ist.</span><span class="sxs-lookup"><span data-stu-id="9d85f-128">If the bonus depreciation amount is more than the remaining acquisition cost, the bonus depreciation amount is either the result of the bonus depreciation calculation or the remaining acquisition cost, whichever amount is less.</span></span> 

<span data-ttu-id="9d85f-129">Wenn die verbleibenden Anschaffungskosten 0 (Null) oder negativ sind, werden keine Buchungen für die vorzeitige Abschreibung generiert.</span><span class="sxs-lookup"><span data-stu-id="9d85f-129">If the remaining acquisition cost is 0 (zero) or less, bonus depreciation transactions isn't generated.</span></span> 

<span data-ttu-id="9d85f-130">Wenn die vorzeitige Abschreibung unter Verwendung des Vorschlagsprozesses berechnet wird, wird eine Abschreibungsbuchung für alle anwendbaren Datensätze der vorzeitigen Abschreibung erstellt, die dem jeweiligen Anlagenabschreibungsbuch zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9d85f-130">When bonus depreciation is calculated by using the proposal process, a bonus depreciation transaction is created for all applicable bonus depreciation records that are associated with the asset book.</span></span> 

<span data-ttu-id="9d85f-131">Sie können eine unbegrenzte Anzahl von Datensätzen für die vorzeitige Abschreibung erstellen.</span><span class="sxs-lookup"><span data-stu-id="9d85f-131">You can create an unlimited number of bonus depreciation records.</span></span> <span data-ttu-id="9d85f-132">Nach deren Zuordnung zu einem Anlagengruppen-Abschreibungsbuch werden sie auf das Anlagenabschreibungsbuch angewendet.</span><span class="sxs-lookup"><span data-stu-id="9d85f-132">After you assign those records to the asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="9d85f-133">Die vorzeitige Abschreibung wird als Prozentsatz oder als fester Wert eingegeben.</span><span class="sxs-lookup"><span data-stu-id="9d85f-133">Bonus depreciation is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="9d85f-134">Beim Buchen von Abschreibungsvorschlägen werden Buchungen für die vorzeitige Abschreibung im Abschreibungsbuch getrennt von Abschreibungsbuchungen erfasst.</span><span class="sxs-lookup"><span data-stu-id="9d85f-134">When you post depreciation proposals, bonus depreciation transactions are posted to the book as separate transactions from the depreciation transactions.</span></span>



