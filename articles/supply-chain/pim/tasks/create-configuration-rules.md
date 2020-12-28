---
title: Variantenregeln erstellen
description: Diese Prozedur erstellt Konfigurationsregeln, die für eine dimensionsbasierte Konfiguration verwendet werden können, um bestimmte Kombinationen von Stücklistenpositionen zu erzwingen oder zu verhindern.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6bc0af4d95e9430d0b5c8b7fc9a4ade076802044
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428707"
---
# <a name="create-configuration-rules"></a><span data-ttu-id="8b83a-103">Variantenregeln erstellen</span><span class="sxs-lookup"><span data-stu-id="8b83a-103">Create configuration rules</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8b83a-104">Diese Prozedur erstellt Konfigurationsregeln, die für eine dimensionsbasierte Konfiguration verwendet werden können, um bestimmte Kombinationen von Stücklistenpositionen zu erzwingen oder zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="8b83a-104">This procedure creates configuration rules that can be used for dimension-based configuration to enforce or prevent certain combinations of BOM lines.</span></span> <span data-ttu-id="8b83a-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="8b83a-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8b83a-106">Dies ist die siebte von acht Prozeduren die beschreibt, wie Kombinationen für eine dimensionsbasierte Konfiguration erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8b83a-106">This is the seventh procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="8b83a-107">Wechseln Sie zu Produktinformationsverwaltung > Stücklisten und Formeln > Stücklisten.</span><span class="sxs-lookup"><span data-stu-id="8b83a-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="8b83a-108">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8b83a-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8b83a-109">Wählen Sie die Technologie BOM der dimensionsbasierten Konfiguration aus.</span><span class="sxs-lookup"><span data-stu-id="8b83a-109">Find and select the BOM for the dimension-based configuration.</span></span>  
3. <span data-ttu-id="8b83a-110">Klicken Sie im Aktivitätsbereich auf "Optionen".</span><span class="sxs-lookup"><span data-stu-id="8b83a-110">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="8b83a-111">Klicken Sie auf "Ansicht ändern".</span><span class="sxs-lookup"><span data-stu-id="8b83a-111">Click Change view.</span></span>
5. <span data-ttu-id="8b83a-112">Klicken Sie auf die Kopfzeilenansicht.</span><span class="sxs-lookup"><span data-stu-id="8b83a-112">Click Header view.</span></span>
    * <span data-ttu-id="8b83a-113">Öffnen Sie die Kopfzeilenansicht, um auf die Konfigurationsroute FastTab zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="8b83a-113">Open the header view to access the Configuration route FastTab.</span></span>  
6. <span data-ttu-id="8b83a-114">Erweitern oder reduzieren Sie den Abschnitt Konfigurationsplan.</span><span class="sxs-lookup"><span data-stu-id="8b83a-114">Expand or collapse the Configuration route section.</span></span>
    * <span data-ttu-id="8b83a-115">Der Konfigurationsroute-FastTab muss im Modus "Erweitert" sein.</span><span class="sxs-lookup"><span data-stu-id="8b83a-115">The Configuration route FastTab must be in the expanded mode.</span></span>  
7. <span data-ttu-id="8b83a-116">Configurationregeln anzeigen</span><span class="sxs-lookup"><span data-stu-id="8b83a-116">Click Configuration rules.</span></span>
8. <span data-ttu-id="8b83a-117">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="8b83a-117">Click New.</span></span>
9. <span data-ttu-id="8b83a-118">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="8b83a-118">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="8b83a-119">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8b83a-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8b83a-120">Die Artikel in der aktuellen Konfigurationsgruppe werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8b83a-120">The items in the current configuration group are displayed.</span></span> <span data-ttu-id="8b83a-121">Wählen Sie diejenige aus, die die Bedingung in der Regel darstellt.</span><span class="sxs-lookup"><span data-stu-id="8b83a-121">Select the one that represents the condition in the rule.</span></span>  
11. <span data-ttu-id="8b83a-122">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8b83a-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="8b83a-123">Wählen Sie im Feld "Methode" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="8b83a-123">In the Method field, select an option.</span></span>
    * <span data-ttu-id="8b83a-124">Es ist möglich, entweder eine Auswahl oder ein deselection eines Artikels aus einer anderen Konfigurationroute-Gruppe zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="8b83a-124">It is possible to enforce either a selection or a deselection of an item from another configuration group.</span></span>  
13. <span data-ttu-id="8b83a-125">Klicken Sie im Feld Abgeleitete-Gruppe auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8b83a-125">In the Derived group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="8b83a-126">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8b83a-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="8b83a-127">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8b83a-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8b83a-128">Wählen Sie die gewünschte Gruppe "Konfigurationroute" aus.</span><span class="sxs-lookup"><span data-stu-id="8b83a-128">Select the desired configuration group.</span></span>  
16. <span data-ttu-id="8b83a-129">Klicken Sie im Feld "Abgeleitete-Gruppenummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8b83a-129">In the Derived item number field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="8b83a-130">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8b83a-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8b83a-131">Die Artikelnummer, die abhängig von der gewählten Methode ausgewählt oder gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b83a-131">Select the item number that will be either selected or deselected depending on the chosen method.</span></span>  
18. <span data-ttu-id="8b83a-132">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8b83a-132">Close the page.</span></span>

