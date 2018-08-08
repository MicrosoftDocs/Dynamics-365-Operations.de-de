---
title: Verbrauchsabschreibung
description: "Dieser Artikel enthält eine Übersicht der Verbrauchsabschreibungsmethode."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: c0f64fee275f63a3e6b31a196df872e41c84dde6
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---

# <a name="consumption-depreciation"></a><span data-ttu-id="df662-103">Verbrauchsabschreibung</span><span class="sxs-lookup"><span data-stu-id="df662-103">Consumption depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df662-104">Dieser Artikel enthält eine Übersicht der Verbrauchsabschreibungsmethode.</span><span class="sxs-lookup"><span data-stu-id="df662-104">This article gives an overview of the Consumption method of depreciation.</span></span>

<span data-ttu-id="df662-105">Wenn Sie beim Einrichten eines Anlagenabschreibungsprofils **Verbrauch** im Feld **Methode** auf der Seite **Abschreibungsprofile** auswählen, basiert die Abschreibung von Anlagen, die diesem Abschreibungsprofil zugeordnet sind, auf der Nutzung der jeweiligen Anlage.</span><span class="sxs-lookup"><span data-stu-id="df662-105">If you set up a depreciation profile for fixed assets and select **Consumption** in the **Method** field on the **Depreciation profiles** page, fixed assets are assigned to the depreciation profile based on their usage.</span></span> <span data-ttu-id="df662-106">Sie müssen Prozentsätze und Intervalle nicht auf der Seite **Abschreibungsprofile** einrichten.</span><span class="sxs-lookup"><span data-stu-id="df662-106">You don't have to set up percentages and intervals on the **Depreciation profiles** page.</span></span> <span data-ttu-id="df662-107">Nach der Erstellung des Profils für die Methode "Verbrauch" kann die Methode auf vielfältige Weise eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="df662-107">After you create a depreciation profile that uses the Consumption method, you can set up the method in various ways.</span></span>

## <a name="set-up-and-use-consumption-depreciation"></a><span data-ttu-id="df662-108">Einrichten und Nutzen der Verbrauchsabschreibung</span><span class="sxs-lookup"><span data-stu-id="df662-108">Set up and use consumption depreciation</span></span>
1.  <span data-ttu-id="df662-109">Erstellen Sie auf der Seite **Abschreibungsprofile** das Abschreibungsprofil.</span><span class="sxs-lookup"><span data-stu-id="df662-109">On the **Depreciation profiles** page, create the depreciation profile.</span></span> <span data-ttu-id="df662-110">Für Verbrauchsberechnungen muss das Abschreibungsprofil eine Kennung und einen Namen besitzen, und **Verbrauch** muss im Feld **Methode** ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="df662-110">For consumption calculations, the depreciation profile must have an ID and a name, and **Consumption** must be selected in the **Method** field.</span></span>
2.  <span data-ttu-id="df662-111">Auf der **Verbrauchsfaktoren**-Seite richten Sie Verbrauchsfaktoren ein.</span><span class="sxs-lookup"><span data-stu-id="df662-111">On the **Consumption factors** page, set up consumption factors.</span></span> <span data-ttu-id="df662-112">Jeder Verbrauchsfaktor muss eine Kennung und einen Namen und einen Verbrauchsfaktor besitzen, der entweder als Menge oder Prozentsatz angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="df662-112">Each consumption factor must have an ID and a name, and a consumption factor that is specified as either a quantity or a percentage.</span></span>
3.  <span data-ttu-id="df662-113">Auf der **Verbrauchseinheiten**-Seite richten Sie Verbrauchseinheiten ein.</span><span class="sxs-lookup"><span data-stu-id="df662-113">On the **Consumption units** page, set up consumption units.</span></span> <span data-ttu-id="df662-114">Jede Verbrauchseinheit muss eine Kennung und einen Namen besitzen.</span><span class="sxs-lookup"><span data-stu-id="df662-114">Each consumption unit must have an ID and a name.</span></span> <span data-ttu-id="df662-115">Abschreibungseinheiten werden verwendet, um Verbrauchsabschreibung auf der Seite **Verbrauchsabschreibung** zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="df662-115">Depreciation units are used to calculate consumption depreciation on the **Consumption depreciation** page.</span></span> <span data-ttu-id="df662-116">Beispiele für Einheiten sind Kilometer (km), Kilogramm (kg) oder Stunde.</span><span class="sxs-lookup"><span data-stu-id="df662-116">Examples of units are kilometer (km), kilogram (kg), and hour.</span></span>
4.  <span data-ttu-id="df662-117">Auf der **Anlagevermögen**-Seite richtet Sie einzelne Anlagen ein.</span><span class="sxs-lookup"><span data-stu-id="df662-117">On the **Fixed assets** page, set up individual fixed assets.</span></span> <span data-ttu-id="df662-118">Wählen Sie für jede Anlage Wertmodelle oder Abschreibungsbücher aus, die über Abschreibungsprofile verfügen.</span><span class="sxs-lookup"><span data-stu-id="df662-118">For each fixed asset, select value models and depreciation books that have depreciation profiles.</span></span> <span data-ttu-id="df662-119">Sie müssen Wertmodelle oder Abschreibungsbücher für die Verbrauchsabschreibung einrichten, wenn Sie Anlagen haben, die Abschreibungsprofile verwenden, die auf der Methode "Verbrauch" basieren.</span><span class="sxs-lookup"><span data-stu-id="df662-119">You must set up value models or depreciation books for consumption depreciation if any of your fixed assets use depreciation profiles that are based on the Consumption method.</span></span> <span data-ttu-id="df662-120">Diese Einrichtung wird entweder auf der Registerkarte **Abschreibung** der Seite **Wertmodelle** oder auf dem Inforegister **Allgemeines** der Seite **Abschreibungsprofil** ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="df662-120">This setup is done either on the **Depreciation** tab of the **Value models** page or on the **General** FastTab of the **Depreciation profile** page.</span></span> <span data-ttu-id="df662-121">Das gleiche Wertmodell kann für mehrere Anlagen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="df662-121">You can use the same value model for multiple fixed assets.</span></span> <span data-ttu-id="df662-122">Abschreibungsprofile sind Teil des Wertmodells oder des Abschreibungsbuchs, das für jede Anlage ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="df662-122">Depreciation profiles are part of the value model or depreciation book that you select for each fixed asset.</span></span> <span data-ttu-id="df662-123">Auf der Seite **Anlagen** können Abschreibungsprofile nicht direkt hinzufügen oder geändert werden.</span><span class="sxs-lookup"><span data-stu-id="df662-123">You can't add or modify depreciation profiles directly on the **Fixed assets** page.</span></span> <span data-ttu-id="df662-124">Sie können Abschreibungsprofile nur auf der Seite **Abschreibungsbücher** ändern.</span><span class="sxs-lookup"><span data-stu-id="df662-124">You can modify depreciation profiles only on the **Depreciation books** page.</span></span>
5.  <span data-ttu-id="df662-125">Geben Sie auf der Seite **Wertmodelle** oder **Abschreibungsbücher** in der Feldgruppe **Verbrauchsabschreibung** in den folgenden Feldern Daten ein:</span><span class="sxs-lookup"><span data-stu-id="df662-125">On the **Value models** page or the **Depreciation books** page, in the **Consumption depreciation** field group, enter information in the following fields:</span></span>
    -   <span data-ttu-id="df662-126">Verbrauchsfaktor</span><span class="sxs-lookup"><span data-stu-id="df662-126">Consumption factor</span></span>
    -   <span data-ttu-id="df662-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="df662-127">Unit</span></span>
    -   <span data-ttu-id="df662-128">Abschreibung pro Einheit</span><span class="sxs-lookup"><span data-stu-id="df662-128">Unit depreciation</span></span>
    -   <span data-ttu-id="df662-129">Vorkalkulierter Verbrauch</span><span class="sxs-lookup"><span data-stu-id="df662-129">Estimated consumption</span></span>

    <span data-ttu-id="df662-130">Das Feld**Gebuchter Verbrauch** enthält die Verbrauchsabschreibung (in Einheiten), die bereits für die Kombination aus Anlage und Wertmodell oder für das Abschreibungsbuch gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="df662-130">The **Posted consumption** field shows the consumption depreciation, in units, that has already been posted either for the combination of the fixed asset and value model, or for the depreciation book.</span></span> <span data-ttu-id="df662-131">Sie können diesen Feldwert nicht manuell aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="df662-131">You can't manually update the value in this field.</span></span>

## <a name="examples"></a><span data-ttu-id="df662-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df662-132">Examples</span></span>
### <a name="example-1"></a><span data-ttu-id="df662-133">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="df662-133">Example 1</span></span>

<span data-ttu-id="df662-134">Für den 31. Januar wird der folgende Verbrauchsfaktor eingerichtet:</span><span class="sxs-lookup"><span data-stu-id="df662-134">The following consumption factor is set up for January 31:</span></span>

-   <span data-ttu-id="df662-135">Die Menge beträgt 1.000.</span><span class="sxs-lookup"><span data-stu-id="df662-135">The quantity is 1,000.</span></span>
-   <span data-ttu-id="df662-136">Die für die Anlage angegebene Abschreibung pro Einheit beträgt 1,5.</span><span class="sxs-lookup"><span data-stu-id="df662-136">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>

<span data-ttu-id="df662-137">Der Abschreibungsvorschlag am 31. Januar lautet wie folgt: Menge × Abschreibung pro Einheit 1.000 × 1,5 = 1,500. Wenn der Faktor, der für die Anlage angegeben wird, ein Prozentsatz ist, wir die Menge im Feld **Vorkalkulierter Verbrauch** für das Wertmodell der Anlage mit dem Prozentsatz multipliziert, der für das ausgewählte Enddatum eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="df662-137">The depreciation proposal on January 31 is as follows: Quantity × Unit depreciation 1,000 × 1.5 = 1,500 If the factor that is specified for the fixed asset is a percentage factor, the quantity that is estimated in the **Estimated consumption** field for the value model of the fixed asset is multiplied by the percentage that is set up for the selected end date.</span></span> <span data-ttu-id="df662-138">Die resultierende Menge wird als Abschreibungsmenge für die Periode vorgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="df662-138">The resulting quantity is then suggested as the depreciation quantity for the period.</span></span>

### <a name="example-2"></a><span data-ttu-id="df662-139">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="df662-139">Example 2</span></span>

<span data-ttu-id="df662-140">Für den 31. Januar wird der folgende Faktor für die Verbrauchsabschreibung eingerichtet:</span><span class="sxs-lookup"><span data-stu-id="df662-140">The following factor for consumption depreciation is set up for January 31:</span></span>

-   <span data-ttu-id="df662-141">Der Prozentsatz beträgt 10 Prozent.</span><span class="sxs-lookup"><span data-stu-id="df662-141">The percentage is 10 percent.</span></span>
-   <span data-ttu-id="df662-142">Die für die Anlage angegebene Abschreibung pro Einheit beträgt 1,5.</span><span class="sxs-lookup"><span data-stu-id="df662-142">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>
-   <span data-ttu-id="df662-143">Die vorkalkulierte Menge der Anlage ist 2.000.</span><span class="sxs-lookup"><span data-stu-id="df662-143">The estimated quantity of the fixed asset is 2,000.</span></span>

<span data-ttu-id="df662-144">Der Abschreibungsvorschlag am 31. Januar lautet wie folgt: Abschreibung pro Einheit × Prozentsatz × Abschreibung pro Einheit 2.000 × 0,10 × 1,5 = 300</span><span class="sxs-lookup"><span data-stu-id="df662-144">The depreciation proposal on January 31 is as follows: Estimated quantity × Percentage × Unit depreciation 2,000 × .10 × 1.5 = 300</span></span>




