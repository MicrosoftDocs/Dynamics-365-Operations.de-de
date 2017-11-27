---
title: "Aktualisieren der Standardkosten in einer Umgebung ohne Produktionstätigkeit"
description: "Dieser Artikel bietet eine Anleitung zum Aktualisieren von Standardkosten in einer Umgebung ohne Produktionstätigkeit."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0386ca1e5e7bf6e578ba2abf1b2c9eefe4dd2a02
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a><span data-ttu-id="953be-103">Aktualisieren der Standardkosten in einer Umgebung ohne Produktionstätigkeit</span><span class="sxs-lookup"><span data-stu-id="953be-103">Update standard costs in a non-manufacturing environment</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="953be-104">Dieser Artikel bietet eine Anleitung zum Aktualisieren von Standardkosten in einer Umgebung ohne Produktionstätigkeit.</span><span class="sxs-lookup"><span data-stu-id="953be-104">This article provides guidance for updating standard costs in a non-manufacturing environment.</span></span>

<span data-ttu-id="953be-105">Für die folgenden Richtlinien wird die Verwendung des Zwei-Versionen-Ansatzes für Standardkostenaktualisierungen vorausgesetzt.</span><span class="sxs-lookup"><span data-stu-id="953be-105">The following guidelines assume that you use a two-version approach to update standard cost.</span></span> <span data-ttu-id="953be-106">Hierbei enthält eine der Nachkalkulationsversionen die ursprünglich definierten Standardkosten für die unveränderliche Periode, während die andere Nachkalkulationsversion die stufenweisen Aktualisierungen beinhaltet.</span><span class="sxs-lookup"><span data-stu-id="953be-106">In this approach, one costing version contains the standard costs that were originally defined for the frozen period, and the second costing version contains the incremental updates.</span></span> <span data-ttu-id="953be-107">Jede Aktualisierung wird als Kostendatensatz innerhalb der zweiten Nachkalkulationsversion eingegeben und schließlich aktiviert.</span><span class="sxs-lookup"><span data-stu-id="953be-107">Each update is entered as a cost record that is enclosed in the second costing version, and eventually it's enabled.</span></span> <span data-ttu-id="953be-108">Eine alternative Lösung stellt der Einzelversionsansatz dar, bei dem die ursprünglich definierte Gruppe von Standardkosten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="953be-108">An alternative, one-version approach uses the set of standard costs that was originally defined.</span></span> <span data-ttu-id="953be-109">Für den Zwei-Versionen-Ansatz müssen Sie eine zweite Nachkalkulationsversion definieren.</span><span class="sxs-lookup"><span data-stu-id="953be-109">The two-version approach requires that you define a second costing version.</span></span> <span data-ttu-id="953be-110">Nachfolgend finden Sie die Richtlinien zur Definition dieser Nachkalkulationsversion:</span><span class="sxs-lookup"><span data-stu-id="953be-110">Here are the guidelines for defining this costing version:</span></span>

-   <span data-ttu-id="953be-111">Weisen Sie den Nachkalkulationstyp **Standardkosten** zu.</span><span class="sxs-lookup"><span data-stu-id="953be-111">Assign a costing type of **Standard costs**.</span></span>
-   <span data-ttu-id="953be-112">Weisen Sie eine aussagekräftige Kennung zu, die Aufschluss über den Zweck der Nachkalkulationsversion gibt, wie z. B. **2016-AKTUALISIERUNGEN**.</span><span class="sxs-lookup"><span data-stu-id="953be-112">Assign a meaningful identifier that indicates the contents of the costing version, such as **2016-UPDATES**.</span></span>
-   <span data-ttu-id="953be-113">Stellen Sie sicher, dass der Inhalt Kostendatensätze einschließt.</span><span class="sxs-lookup"><span data-stu-id="953be-113">Make sure that the content includes cost records.</span></span>
-   <span data-ttu-id="953be-114">Ermöglichen Sie die Eingabe von Kostendatensätzen für alle Standorte.</span><span class="sxs-lookup"><span data-stu-id="953be-114">Allow cost records to be entered for all sites.</span></span> <span data-ttu-id="953be-115">Durch Angabe eines Standorts können Kostendatensätze nur für diesen Standort eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="953be-115">If you specify a site, cost records can be entered only for that site.</span></span>
-   <span data-ttu-id="953be-116">Geben Sie als Fallback-Prinzip den Wert **Kein** an.</span><span class="sxs-lookup"><span data-stu-id="953be-116">Indicate a fallback principle of **None**.</span></span> <span data-ttu-id="953be-117">Das Fallback-Prinzip wird ausschließlich auf Kostenberechnungen für produzierte Artikel angewendet.</span><span class="sxs-lookup"><span data-stu-id="953be-117">The fallback principle applies only to cost calculations for manufactured items.</span></span>

<span data-ttu-id="953be-118">Gehen Sie zum Korrigieren, Regulieren oder Aktualisieren der Standardkosten für neue Artikel folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="953be-118">To correct, adjust, or update standard costs for new items, follow these steps.</span></span>

1.  <span data-ttu-id="953be-119">Verwenden Sie die Seite **Nachkalkulationsversion** **Einstellungen**, um die Eingabe von Kostendaten in die zweite Nachkalkulationsversion zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="953be-119">Use the **Costing version** **setup** page to enable cost data to be entered into the second costing version.</span></span> <span data-ttu-id="953be-120">Sperren Sie optional die Aktivierung ausstehender Kosten, sodass eine Aktivierung erst möglich ist, nachdem die ausstehenden Kosten vollständig und exakt definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="953be-120">Optionally, prevent the activation of pending costs, so that activation will be allowed after pending costs have been completely and accurately defined.</span></span> <span data-ttu-id="953be-121">Sie können auch optional ein Datum im Feld **Von Datum** eingeben.</span><span class="sxs-lookup"><span data-stu-id="953be-121">You can also optionally enter a date in the **From date** field.</span></span> <span data-ttu-id="953be-122">Allgemeine Richtlinie: Geben Sie das Datum an, an dem die stufenweisen Aktualisierungen voraussichtlich aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="953be-122">As a general guideline, use the date when you intend to enable the incremental updates.</span></span> <span data-ttu-id="953be-123">Alternative: Lassen Sie das Feld **Von Datum** für die Nachkalkulationsversion leer, und geben Sie anschließend im Feld **Von Datum** für jeden Kostendatensatz ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="953be-123">Alternatively, leave the **From date** field blank for the costing version, and then enter a date in the **From date** field for each cost record.</span></span>
2.  <span data-ttu-id="953be-124">Geben Sie mithilfe der Seite **Artikelpreis** Aktualisierungen als Artikelkostendatensätze in der zweiten Nachkalkulationsversion ein.</span><span class="sxs-lookup"><span data-stu-id="953be-124">Use the **Item price** page to enter updates as item cost records that are enclosed in the second costing version.</span></span>
3.  <span data-ttu-id="953be-125">Prüfen Sie mithilfe des Berichts **Artikelpreis** die Artikelkostendatensätze in der zweiten Nachkalkulationsversion auf Vollständigkeit und Richtigkeit.</span><span class="sxs-lookup"><span data-stu-id="953be-125">Use the **Item prices** report to verify the completeness and accuracy of the item cost records that are enclosed in the second costing version.</span></span>
4.  <span data-ttu-id="953be-126">Ändern Sie mithilfe der Seite **Verwaltung der Nachkalkulationsversion** die Sperrmarkierung, um in der zweiten Nachkalkulationsversion die Aktivierung von Datensätzen für ausstehende Kosten zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="953be-126">Use the **Costing version maintenance** page to change the blocking flag to allow activation of the pending cost records that are enclosed in the second costing version.</span></span>
5.  <span data-ttu-id="953be-127">Verwenden Sie die Seite **Preise aktivieren** (die Sie über die Seite **Verwaltung der Nachkalkulationsversion** öffnen), um alle ausstehenden Artikelkostendatensätze in der zweiten Nachkalkulationsversion zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="953be-127">Use the **Activate prices** page (which you open from the **Costing version maintenance** page) to activate all pending item cost records that are enclosed in the second costing version.</span></span> <span data-ttu-id="953be-128">Die Datensätze mit ausstehenden Kosten können auch für einzelne Artikel aktiviert werden, indem Sie auf der Seite **Artikelkosten** auf die Schaltfläche **Ausstehende Preise aktivieren** klicken.</span><span class="sxs-lookup"><span data-stu-id="953be-128">You can also activate the pending cost records for individual items by clicking the **Activate pending price** button on the **Item price** page.</span></span>
6.  <span data-ttu-id="953be-129">Mithilfe der Seite **Einstellungen für Nachkalkulationsversion** können Sie die Sperrmarkierungen in der zweiten Nachkalkulationsversion ändern, um eine weitere Datenverwaltung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="953be-129">To prevent additional data maintenance, use the **Costing version setup** page to change the blocking flags that are enclosed in the second costing version.</span></span> <span data-ttu-id="953be-130">Durch die Sperrrichtlinien werden die Eingabe neuer ausstehender Kosten sowie die Aktivierung ausstehender Kosten verhindert.</span><span class="sxs-lookup"><span data-stu-id="953be-130">The blocking policies will prevent the entry of new pending costs and the activation of pending costs.</span></span>





