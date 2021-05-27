---
title: Das Lagerplatzprofil verbietet negative Bestände, negative verfügbare Bestände sind jedoch zulässig
description: Die Option „Negativen Bestand zulassen“ ist für das Lagerplatzprofil auf „Nein“ festgelegt, das System lässt jedoch weiterhin negative Bestände zu.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026539"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a><span data-ttu-id="91c58-103">Das Lagerplatzprofil verbietet negative Bestände, negative verfügbare Bestände sind jedoch zulässig</span><span class="sxs-lookup"><span data-stu-id="91c58-103">Location profile disallows negative inventory, but negative on-hand inventory is permitted</span></span>

<span data-ttu-id="91c58-104">KB-Nummer: 4613622</span><span class="sxs-lookup"><span data-stu-id="91c58-104">KB number: 4613622</span></span>

## <a name="symptoms"></a><span data-ttu-id="91c58-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="91c58-105">Symptoms</span></span>

<span data-ttu-id="91c58-106">Die Option **Negativen Bestand zulassen** ist für das Lagerplatzprofil auf *Nein* festgelegt, das System lässt jedoch weiterhin negative Bestände zu.</span><span class="sxs-lookup"><span data-stu-id="91c58-106">The **Allow negative inventory** option for the location profile is set to *No*, but the system still allows negative on-hand inventory.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="91c58-107">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="91c58-107">Example scenario</span></span>

<span data-ttu-id="91c58-108">Bei staatlich regulierten Transaktionen muss das System in der Lage sein, negative Bestände zu erfassen, um Verluste zu buchen.</span><span class="sxs-lookup"><span data-stu-id="91c58-108">For government-regulated transactions, the system must be able to record negative inventory to book losses.</span></span> <span data-ttu-id="91c58-109">Sie möchten, dass ein Artikel einen negativen Bestand aufweist, jedoch nur an bestimmten Lagerplätzen, z. B. in Tanks.</span><span class="sxs-lookup"><span data-stu-id="91c58-109">You want an item to be able to show negative inventory, but only in designated locations, such as tanks.</span></span> <span data-ttu-id="91c58-110">Wenn die Artikelmodellgruppe jedoch einen negativen Bestand zulässt, spielt es keine Rolle, ob der Lagerlatz so eingestellt ist, dass ein negativer Bestand zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="91c58-110">However, if the item model group allows negative inventory, you find that it doesn't matter whether the location is set to allow negative inventory.</span></span> <span data-ttu-id="91c58-111">Wenn der Artikel so eingerichtet ist, dass kein negativer Bestand zulässig ist, spielt es keine Rolle, wie das Lagerplatzprofil eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="91c58-111">If the item is set up so that negative inventory isn't allowed, it doesn't matter how the location profile is set up.</span></span>

## <a name="resolution"></a><span data-ttu-id="91c58-112">Lösung</span><span class="sxs-lookup"><span data-stu-id="91c58-112">Resolution</span></span>

<span data-ttu-id="91c58-113">Die Einstellung **Negativen Bestand zulassen** aus dem Lagerplatzprofil gilt nur für Lagerortprozesse, z. B. Kommissionierung.</span><span class="sxs-lookup"><span data-stu-id="91c58-113">The **Allow negative inventory** setting from the location profile applies only to warehouse processes, such as picking.</span></span> <span data-ttu-id="91c58-114">Artikelmodellgruppen, die so eingestellt sind, dass sie einen negativen Bestand zulassen, wirken sich jedoch auf alle Prozesse aus den Modulen „Bestandsverwaltung“ und „Lagerortverwaltung“ aus, und das Lagerplatzprofil überschreibt die Einstellung nicht.</span><span class="sxs-lookup"><span data-stu-id="91c58-114">However, item model groups that are set to allow negative inventory affect all processes from the Inventory management and Warehouse management modules, and the location profile won't override the setting.</span></span>

<span data-ttu-id="91c58-115">Sie können steuern, ob ein Lagerort einen negativen Bestand führen darf.</span><span class="sxs-lookup"><span data-stu-id="91c58-115">You can control whether a warehouse is allowed to carry negative inventory.</span></span> <span data-ttu-id="91c58-116">Stellen Sie Ihre Artikelmodellgruppen so ein, dass negative Bestände nicht zulässig sind, und legen Sie nur den entsprechenden Lagerort fest, um negative Bestände zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="91c58-116">Set your item model groups to disallow negative physical inventory, and set only the relevant warehouse to allow negative inventory.</span></span>
