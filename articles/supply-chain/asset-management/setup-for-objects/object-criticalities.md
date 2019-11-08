---
title: Typen kritischer Werte für Anlagen
description: In diesem Thema wird erläutert, was Typen kritischer Werte für Anlagen in Asset Management sind.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f96fcc7ebb8928c6d6b17b30465ad1625d9b5be4
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571069"
---
# <a name="asset-criticality-types"></a><span data-ttu-id="0a2cd-103">Typen kritischer Werte für Anlagen</span><span class="sxs-lookup"><span data-stu-id="0a2cd-103">Asset criticality types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="0a2cd-104">In diesem Thema wird erläutert, was Typen kritischer Werte für Anlagen in Asset Management sind.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-104">The topic explains asset criticality types in Asset Management.</span></span> <span data-ttu-id="0a2cd-105">Kritische Anlagenzustände beziehen sich auf Anlagen und werden an Arbeitsaufträge übertragen.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-105">Asset criticality is related to assets and is transferred to work orders.</span></span> <span data-ttu-id="0a2cd-106">Sie können in einem Arbeitsauftrag nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-106">It can't be changed on a work order.</span></span> <span data-ttu-id="0a2cd-107">Kritische Anlagenzustände werden verwendet, um den kritischen Zustand von Arbeitsaufträgen während der Planung zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-107">Asset criticality is used to calculate work order criticality during work order scheduling.</span></span> <span data-ttu-id="0a2cd-108">Sie werden also dazu verwendet, um das Ausmaß zu berechnen, in dem ein Wartungseinzelvorgang für eine Anlage sich auf die Produktionsplan und die Produktivität in Ihrem Unternehmen auswirkt.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-108">In other words, it's used to calculate the extent to which a maintenance job on an asset affects the production schedule and productivity in your company.</span></span> <span data-ttu-id="0a2cd-109">Weitere Informationen zu den Einstellungen, die sich auf die Berechnung von Bewertungsnoten für Arbeitsauftragsplanung beziehen, finden Sie unter [Anlagenverwaltungsparameter](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0a2cd-109">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span>

<span data-ttu-id="0a2cd-110">Um kritische Anlagenzustände einzurichten, erstellen Sie zunächst die Typen der kritischen Anlagenzustände, die für die Anlageneinrichtung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-110">To set up criticality, you first create the criticality types that should be used in the asset setup.</span></span> <span data-ttu-id="0a2cd-111">Anschließend richten Sie die kritischen Anlagenzustände ein.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-111">You then set up asset criticalities.</span></span>

## <a name="set-up-criticality-types"></a><span data-ttu-id="0a2cd-112">Typen kritischer Anlagenzustände</span><span class="sxs-lookup"><span data-stu-id="0a2cd-112">Set up criticality types</span></span>

1. <span data-ttu-id="0a2cd-113">Wählen Sie **Anlageverwaltung** \> **Einstellungen** \> **Anlagen** \> **Typen kritischer Werte** aus.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-113">Select **Asset management** \> **Setup** \> **Assets** \> **Criticality types**.</span></span>
2. <span data-ttu-id="0a2cd-114">Wählen Sie **Neu** aus, um einen Datensatz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-114">Select **New** to create a record.</span></span>
3. <span data-ttu-id="0a2cd-115">Geben Sie im Feld **Risiko** eine Zahl ein, die der Kritikalität angibt.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-115">In the **Criticality** field, enter a number that indicates the criticality.</span></span>
4. <span data-ttu-id="0a2cd-116">Geben Sie im Feld **Name** einen Namen für den Kritikalitätstyp ein.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-116">In the **Name** field, enter a name for the criticality type.</span></span>
5. <span data-ttu-id="0a2cd-117">Geben Sie im Feld **Faktor** einen Faktor ein.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-117">In the **Factor** field, enter a factor.</span></span> <span data-ttu-id="0a2cd-118">Dieser Faktor wird bei der Berechnung der Arbeitsauftragsplanung verwendet, um den Kritikalitätsdatensatz zu bestimmen, der verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-118">This factor is used during the calculation of work order scheduling to determine the criticality record that should be used.</span></span> <span data-ttu-id="0a2cd-119">(Es wird immer der Datensatz mit dem höchsten Faktor verwendet). Diese Einstellung ist relevant, wenn, wie in der folgenden Abbildung dargestellt, Kritikalitätspositionen erstellt werden, die den gleichen Kritikalitätswert haben.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-119">(The record that has the highest factor is always used.) This setting is relevant if, as shown in the following illustration, criticality lines are created that have the same criticality value.</span></span>

    ![Seite „Typen kritischer Werte“](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a><span data-ttu-id="0a2cd-121">Kritische Anlagenzustände einrichten</span><span class="sxs-lookup"><span data-stu-id="0a2cd-121">Set up asset criticalities</span></span>

1. <span data-ttu-id="0a2cd-122">Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Kritische Anlagenzustände**.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-122">Select **Asset management** \> **Setup** \> **Asset criticalities**.</span></span>
2. <span data-ttu-id="0a2cd-123">Wählen Sie **Neu** aus, um einen Datensatz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-123">Select **New** to create a record.</span></span>
3. <span data-ttu-id="0a2cd-124">Nehmen Sie abhängig von der erforderlichen Detailebene für die Anlagenkritikalität die zutreffende Auswahl in den Feldern **Funktionaler Standort**, **Anlagentyp**, **Hersteller**, **Modell**, **Anlage**, **Einzelvorgangstypkategorie**, **Einzelvorgangstyp**, **Einzelvorgangstypvariante** und **Einzelvorgangsanforderung** vor.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-124">Depending on the required level of detail for asset criticality, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0a2cd-125">Wenn eine Anlagenkritikalität ausgewählt ist, durchläuft Asset Management alle Anlagenkritikalitätsdatensätze, um nach einer möglichen Übereinstimmung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-125">When an asset criticality is selected, Asset Management goes through all asset criticality records to check for a possible match.</span></span> <span data-ttu-id="0a2cd-126">Die spezifischste Kombination wird immer zuerst geprüft.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-126">It always checks the most specific combination first.</span></span> <span data-ttu-id="0a2cd-127">Asset Management überprüft also zuerst das Feld **Einzelvorgangsanforderung**.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-127">In other words, Asset Management first checks **Job requirement**.</span></span> <span data-ttu-id="0a2cd-128">Wenn keine Übereinstimmung gefunden wird, wird das Feld **Einzelvorgangstypvariante** überprüft.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-128">If no match is found, it checks **Job type variant**.</span></span> <span data-ttu-id="0a2cd-129">Wenn keine Übereinstimmung gefunden wird, wird das Feld **Einzelvorgangstyp** überprüft, usw.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-129">If no match is found, it checks **Job type**, and so on.</span></span> <span data-ttu-id="0a2cd-130">Wie Sie im Layout der Seite sehen können, bedeutet dieses Verhalten, dass Asset Management zum Auffinden der spezifischsten Kombinationen jeden Datensatz von rechts nach links auf Übereinstimmung prüft.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-130">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="0a2cd-131">Wenn keine Übereinstimmung gefunden wird, wird der Standarddatensatz verwendet, der keine Auswahl hat.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-131">If no match is found, the "default" record that has no selections is used.</span></span>

4. <span data-ttu-id="0a2cd-132">Wählen Sie im Feld **Risiko** einen der Kritikalitätswerte aus, die Sie im vorherigen Verfahren erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-132">In the **Criticality** field, select one of the criticality values that you created in the previous procedure.</span></span>

### <a name="notes-about-criticality-setup"></a><span data-ttu-id="0a2cd-133">Hinweise zur Kritikalitätseinstellung</span><span class="sxs-lookup"><span data-stu-id="0a2cd-133">Notes about criticality setup</span></span>

- <span data-ttu-id="0a2cd-134">Wenn Sie eine Anlagenkritikalität in dieser Einstellung ändern, nachdem Sie diese bereits für einen Arbeitsauftrag verwendet haben, wird die Kritikalität für den Arbeitsauftrag nicht entsprechend aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-134">If you change an asset criticality in this setup after you've already used it on a work order, the criticality on the work order isn't updated accordingly.</span></span>
- <span data-ttu-id="0a2cd-135">Die Kritikalität eines Arbeitsauftrags wird jedes Mal neu berechnet, wenn eine Arbeitsauftragsposition zum Arbeitsauftrag hinzugefügt oder daraus gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-135">The criticality on a work order is recalculated every time that a work order line is added to or deleted from the work order.</span></span>
- <span data-ttu-id="0a2cd-136">Wenn ein Arbeitsauftrag mehrere Arbeitsauftragseinzelvorgänge enthält, wird die höchste Kritikalität, gemäß dem Feld **Faktor** auf der Seite **Typen kritischer Werte**, immer für den Arbeitsauftrag verwendet.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-136">If a work order contains several work order jobs, the highest criticality, according to the **Factor** field on the **Criticality types** page, is always used on the work order.</span></span>
- <span data-ttu-id="0a2cd-137">Im Allgemeinen kann sich die Anlagenkritikalität mit der Zeit ändern.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-137">Generally, asset criticality can change over a period.</span></span> <span data-ttu-id="0a2cd-138">Kritikalität kann durch den Einkauf von neuer Ausrüstung, Wiederaufbereitungen usw. beeinflusst werden.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-138">Criticality can be affected by the purchase of new equipment, refurbishments, and so on.</span></span> <span data-ttu-id="0a2cd-139">Sie sollten die kritischen Anlagenzustände regelmäßig erneut bewerten (beispielsweise einmal pro Jahr), um sicherzustellen, dass die Kritikalitätsdefinitionen mit den Einstellungen der aktuellen Produktion übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0a2cd-139">Consider reevaluating your asset criticalities at regular intervals (for example, once per year or every other year) to make sure that your criticality definitions match your current production setup.</span></span>
