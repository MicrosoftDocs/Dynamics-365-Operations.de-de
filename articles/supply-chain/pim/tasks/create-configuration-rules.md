---
title: Variantenregeln erstellen
description: Diese Prozedur erstellt Konfigurationsregeln, die für eine dimensionsbasierte Konfiguration verwendet werden können, um bestimmte Kombinationen von Stücklistenpositionen zu erzwingen oder zu verhindern.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a315ddecd2e10f508b86ac8ea18a36df71616963
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "314738"
---
# <a name="create-configuration-rules"></a><span data-ttu-id="dfbdd-103">Variantenregeln erstellen</span><span class="sxs-lookup"><span data-stu-id="dfbdd-103">Create configuration rules</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dfbdd-104">Diese Prozedur erstellt Konfigurationsregeln, die für eine dimensionsbasierte Konfiguration verwendet werden können, um bestimmte Kombinationen von Stücklistenpositionen zu erzwingen oder zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-104">This procedure creates configuration rules that can be used for dimension-based configuration to enforce or prevent certain combinations of BOM lines.</span></span> <span data-ttu-id="dfbdd-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="dfbdd-106">Dies ist die siebte von acht Prozeduren die beschreibt, wie Kombinationen für eine dimensionsbasierte Konfiguration erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-106">This is the seventh procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="dfbdd-107">Wechseln Sie zu Produktinformationsverwaltung > Stücklisten und Formeln > Stücklisten.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="dfbdd-108">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="dfbdd-109">Wählen Sie die Technologie BOM der dimensionsbasierten Konfiguration aus.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-109">Find and select the BOM for the dimension-based configuration.</span></span>  
3. <span data-ttu-id="dfbdd-110">Klicken Sie im Aktivitätsbereich auf "Optionen".</span><span class="sxs-lookup"><span data-stu-id="dfbdd-110">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="dfbdd-111">Klicken Sie auf "Ansicht ändern".</span><span class="sxs-lookup"><span data-stu-id="dfbdd-111">Click Change view.</span></span>
5. <span data-ttu-id="dfbdd-112">Klicken Sie auf die Kopfzeilenansicht.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-112">Click Header view.</span></span>
    * <span data-ttu-id="dfbdd-113">Öffnen Sie die Kopfzeilenansicht, um auf die Konfigurationsroute FastTab zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-113">Open the header view to access the Configuration route FastTab.</span></span>  
6. <span data-ttu-id="dfbdd-114">Erweitern oder reduzieren Sie den Abschnitt Konfigurationsplan.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-114">Expand or collapse the Configuration route section.</span></span>
    * <span data-ttu-id="dfbdd-115">Der Konfigurationsroute-FastTab muss im Modus "Erweitert" sein.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-115">The Configuration route FastTab must be in the expanded mode.</span></span>  
7. <span data-ttu-id="dfbdd-116">Configurationregeln anzeigen</span><span class="sxs-lookup"><span data-stu-id="dfbdd-116">Click Configuration rules.</span></span>
8. <span data-ttu-id="dfbdd-117">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="dfbdd-117">Click New.</span></span>
9. <span data-ttu-id="dfbdd-118">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-118">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="dfbdd-119">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="dfbdd-120">Die Artikel in der aktuellen Konfigurationsgruppe werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-120">The items in the current configuration group are displayed.</span></span> <span data-ttu-id="dfbdd-121">Wählen Sie diejenige aus, die die Bedingung in der Regel darstellt.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-121">Select the one that represents the condition in the rule.</span></span>  
11. <span data-ttu-id="dfbdd-122">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="dfbdd-123">Wählen Sie im Feld "Methode" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-123">In the Method field, select an option.</span></span>
    * <span data-ttu-id="dfbdd-124">Es ist möglich, entweder eine Auswahl oder ein deselection eines Artikels aus einer anderen Konfigurationroute-Gruppe zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-124">It is possible to enforce either a selection or a deselection of an item from another configuration group.</span></span>  
13. <span data-ttu-id="dfbdd-125">Klicken Sie im Feld Abgeleitete-Gruppe auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-125">In the Derived group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="dfbdd-126">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="dfbdd-127">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="dfbdd-128">Wählen Sie die gewünschte Gruppe "Konfigurationroute" aus.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-128">Select the desired configuration group.</span></span>  
16. <span data-ttu-id="dfbdd-129">Klicken Sie im Feld "Abgeleitete-Gruppenummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-129">In the Derived item number field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="dfbdd-130">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="dfbdd-131">Die Artikelnummer, die abhängig von der gewählten Methode ausgewählt oder gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-131">Select the item number that will be either selected or deselected depending on the chosen method.</span></span>  
18. <span data-ttu-id="dfbdd-132">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dfbdd-132">Close the page.</span></span>

