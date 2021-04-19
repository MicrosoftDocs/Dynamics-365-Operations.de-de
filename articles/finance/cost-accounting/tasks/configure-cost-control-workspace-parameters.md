---
title: Kostensteuerungs-Arbeitsbereichsparameter konfigurieren
description: Verwenden Sie das folgende Verfahren, um den Kostenkontrollearbeitsbereich zu konfigurieren, damit die Manager auf verschiedenen Stufen in einer Organisation Einblick in ihre Kostenträger, wie Kostenstellen und Produktgruppen erhalten können.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspaceConfigurationPerUser
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9c186fdd6149f4e208bb89e1c3514e2a2ac0168c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822080"
---
# <a name="configure-cost-control-workspace-parameters"></a><span data-ttu-id="01a28-103">Kostensteuerungs-Arbeitsbereichsparameter konfigurieren</span><span class="sxs-lookup"><span data-stu-id="01a28-103">Configure cost control workspace parameters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="01a28-104">Verwenden Sie das folgende Verfahren, um den Kostenkontrollearbeitsbereich zu konfigurieren, damit die Manager auf verschiedenen Stufen in einer Organisation Einblick in ihre Kostenträger, wie Kostenstellen und Produktgruppen erhalten können.</span><span class="sxs-lookup"><span data-stu-id="01a28-104">Use this procedure to configure the Cost control workspace so that managers at various levels in an organization can gain insight into their cost objects, such as cost centers and product groups.</span></span> <span data-ttu-id="01a28-105">Das Demodatenunternehmen USP2 wurde dazu verwendet, diese Aufzeichnung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="01a28-105">The USP2 demo company was used to create this recording.</span></span>

1. <span data-ttu-id="01a28-106">Wechseln Sie zur Kostenbuchhaltung > Einstellungs > Kostenkontrollearbeitsbereichskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="01a28-106">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
2. <span data-ttu-id="01a28-107">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="01a28-107">Click New.</span></span>
3. <span data-ttu-id="01a28-108">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="01a28-108">In the Name field, type a value.</span></span>
4. <span data-ttu-id="01a28-109">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="01a28-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="01a28-110">Wählen Sie "Ja" im Feld "Veröffentlichte Felder" aus.</span><span class="sxs-lookup"><span data-stu-id="01a28-110">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="01a28-111">Wenn Sie diese Option auf Ja setzen, können Benutzer, denen eine der Rollen zugewiesen wurde, den Bericht im Kostenkontrollerarbeitsbereich sehen: Kostenrechnungsmanager, Buchhalter, Kostenbuchhalter oder Kostenträgercontroller.</span><span class="sxs-lookup"><span data-stu-id="01a28-111">If you set this option to Yes, users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, or cost object controller.</span></span> <span data-ttu-id="01a28-112">Wenn Sie diese Option auf Nein setzen, können nur Benutzer, denen eine der Rollen zugewiesen wurde, den Bericht im Kostenkontrollerarbeitsbereich sehen: Kostenrechnungsmanager, Buchhalter, Kostenbuchhalter oder Kostenträgercontroller.</span><span class="sxs-lookup"><span data-stu-id="01a28-112">If you set this option to No, only users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, or cost accountant clerk.</span></span>  
6. <span data-ttu-id="01a28-113">Erweitern Sie den Datenenfilterungsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="01a28-113">Expand the Data filtering section.</span></span>
7. <span data-ttu-id="01a28-114">Geben Sie im Feld "Kostenkontrolleinheit" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="01a28-114">In the Cost control unit field, enter or select a value.</span></span>
8. <span data-ttu-id="01a28-115">Geben Sie im Feld "Ursprüngliche Budgetversion" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="01a28-115">In the Budget original version field, enter or select a value.</span></span>
9. <span data-ttu-id="01a28-116">Geben Sie im Feld "Kostenelementdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="01a28-116">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
10. <span data-ttu-id="01a28-117">Geben Sie im Feld "Kostenobjektdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="01a28-117">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
11. <span data-ttu-id="01a28-118">Erweitern Sie den Kalkulationsdatensatzabschnitt zuweisen.</span><span class="sxs-lookup"><span data-stu-id="01a28-118">Expand the Assign calculation records section.</span></span>
12. <span data-ttu-id="01a28-119">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="01a28-119">Click New.</span></span>
13. <span data-ttu-id="01a28-120">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="01a28-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="01a28-121">Geben Sie im Feld "Steuerperiode" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="01a28-121">In the Fiscal calendar period field, enter or select a value.</span></span>
15. <span data-ttu-id="01a28-122">Geben Sie im Feld „Aktuelle Version” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="01a28-122">In the Actual version field, enter or select a value.</span></span>
16. <span data-ttu-id="01a28-123">Erweitern Sie Steuerperioden pro Spaltenabschnitt.</span><span class="sxs-lookup"><span data-stu-id="01a28-123">Expand the Fiscal periods per column section.</span></span>
17. <span data-ttu-id="01a28-124">Wählen Sie "Ja" im Feld Aktuelle Periode aus.</span><span class="sxs-lookup"><span data-stu-id="01a28-124">Select Yes in the Current period field.</span></span>
18. <span data-ttu-id="01a28-125">Erweitern Sie die Spalten, um die Kostenabschnitte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="01a28-125">Expand the Columns to display for costs section.</span></span>
19. <span data-ttu-id="01a28-126">Wählen Sie "Ja" im Feld "Fixkosten" aus.</span><span class="sxs-lookup"><span data-stu-id="01a28-126">Select Yes in the Fixed cost field.</span></span>
20. <span data-ttu-id="01a28-127">Wählen Sie "Ja" im Feld "Varialble Fixkosten" aus.</span><span class="sxs-lookup"><span data-stu-id="01a28-127">Select Yes in the Variable cost field.</span></span>
21. <span data-ttu-id="01a28-128">Wählen Sie "Ja" im Feld "Totale Fixkosten" aus.</span><span class="sxs-lookup"><span data-stu-id="01a28-128">Select Yes in the Total cost field.</span></span>
22. <span data-ttu-id="01a28-129">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="01a28-129">Click Save.</span></span>
23. <span data-ttu-id="01a28-130">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="01a28-130">Close the page.</span></span>
24. <span data-ttu-id="01a28-131">Wechseln Sie zu Buchhaltung > Arbeitsbereich  Kostenkontrolle.</span><span class="sxs-lookup"><span data-stu-id="01a28-131">Go to Cost accounting > Workspaces > Cost control.</span></span>
25. <span data-ttu-id="01a28-132">Wählen Sie eine Anweisung aus, um die festen, variable, und nicht klassifizierten Gesamtkosten für den ausgewählten Buchhaltungszeitraum anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="01a28-132">Select a statement to see fixed, variable, total, and unclassified costs for the selected fiscal periods.</span></span>
26. <span data-ttu-id="01a28-133">Geben Sie im Feld "Steuerperiode" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="01a28-133">In the Fiscal calendar period field, enter or select a value.</span></span>
27. <span data-ttu-id="01a28-134">Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="01a28-134">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="01a28-135">Nachdem Sie eine Kostenträgerdimensionshierarchie ausgewählt haben, erweitern Sie die Kostenfaktordimensionshierarchie, um die gewünschten Kostenwerte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="01a28-135">After you've selected a Cost object dimension hierarchy, expand the Cost element dimension hierarchy to see the desired cost values.</span></span> <span data-ttu-id="01a28-136">So können Sie die Hierarchie zu den Produktionsgeschäftskosten erweitern, um den Wert zu finden.</span><span class="sxs-lookup"><span data-stu-id="01a28-136">For example, you can expand the hierarchy to Manufacturing overhead to see the value.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]