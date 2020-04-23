---
title: Kanban-Planungsgruppen definieren
description: Lean Schedule-Gruppen werden zur Gruppierung von Einzelprodukten in der Kanban-Planung verwendet.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54151e8afd1b6e0606d17b044f545314f7012079
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212065"
---
# <a name="define-lean-schedule-groups"></a><span data-ttu-id="a4e18-103">Kanban-Planungsgruppen definieren</span><span class="sxs-lookup"><span data-stu-id="a4e18-103">Define lean schedule groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a4e18-104">Lean Schedule-Gruppen werden zur Gruppierung von Einzelprodukten in der Kanban-Planung verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4e18-104">Lean schedule groups are defined to group and distinguish products in kanban scheduling.</span></span> <span data-ttu-id="a4e18-105">Die Gruppierung kann als generische Zuordnung pro Unternehmen oder für eine Arbeitsgruppe ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a4e18-105">The grouping can be done as generic association per company or specific to a work cell.</span></span> <span data-ttu-id="a4e18-106">Jede Gruppe hat den Farbcode, der zur optische Anzeige auf der Kanbanplanung-Listenseite zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="a4e18-106">Each group has a color code assigned for visual indication in the kanban scheduling listpage.</span></span> <span data-ttu-id="a4e18-107">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="a4e18-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="define-lean-scheduling-group"></a><span data-ttu-id="a4e18-108">Definieren einer Lean Schedule-Gruppen</span><span class="sxs-lookup"><span data-stu-id="a4e18-108">Define lean scheduling group</span></span>
1. <span data-ttu-id="a4e18-109">Wechseln Sie zu "Produktinformationsverwaltung" > "Lean-Manufacturing" > "Lean-Schedule-Gruppen".</span><span class="sxs-lookup"><span data-stu-id="a4e18-109">Go to Product information management > Lean manufacturing > Lean schedule groups.</span></span>
2. <span data-ttu-id="a4e18-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="a4e18-110">Click New.</span></span>
3. <span data-ttu-id="a4e18-111">Geben Sie im Feld "Schedule-Gruppe" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a4e18-111">In the Schedule group field, type a value.</span></span>
    * <span data-ttu-id="a4e18-112">Eine Schedule-Gruppe kann als globale Gruppe oder für eine bestimmte Arbeitsgruppe definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a4e18-112">A schedule group can be defined as global group or specific to a work cell.</span></span> <span data-ttu-id="a4e18-113">In diesem Beispiel definieren wir eine globale Gruppe und die Arbeitsgruppe bleibt leer.</span><span class="sxs-lookup"><span data-stu-id="a4e18-113">In this simple example, we define a global group, and the work cell is kept empty.</span></span> <span data-ttu-id="a4e18-114">Die Einstellungen dieser Gruppe gelten für alle Arbeitsgruppen, die keine speziellen Schedule-Gruppen haben.</span><span class="sxs-lookup"><span data-stu-id="a4e18-114">The settings of this group apply to all work cells that do not have specific schedule groups.</span></span>  
4. <span data-ttu-id="a4e18-115">Wählen Sie eine Farbe aus der Farbauswahl aus.</span><span class="sxs-lookup"><span data-stu-id="a4e18-115">Select a color from the color selection.</span></span>
    * <span data-ttu-id="a4e18-116">Die Farben werden verwendet, um die Einzelvorgänge der Seite "Kanbanzeitplanlisten" auf der Kanbanprozesskarte hervorzuheben.</span><span class="sxs-lookup"><span data-stu-id="a4e18-116">The colors are used to highlight the jobs on the kanban schedule list page or the kanban process board.</span></span>  
5. <span data-ttu-id="a4e18-117">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="a4e18-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="a4e18-118">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="a4e18-118">In the list, click the link in the selected row.</span></span>

## <a name="associate-product"></a><span data-ttu-id="a4e18-119">Produkt zuordnen</span><span class="sxs-lookup"><span data-stu-id="a4e18-119">Associate product</span></span>
1. <span data-ttu-id="a4e18-120">Zuordnen eines bestimmtes Produkts</span><span class="sxs-lookup"><span data-stu-id="a4e18-120">Associate a specific product</span></span>
    * <span data-ttu-id="a4e18-121">Es gibt zwei Möglichkeiten, um Produkte den Lean Schedule-Gruppe zuzuordnen. Entweder als bestimmtes Produkt (Artikelrelationstyp = Artikel) oder als Teil eines Artikelverteilungsschlüssels (Artikelrelationstyp = Gruppe).</span><span class="sxs-lookup"><span data-stu-id="a4e18-121">There are two ways to associate products to lean schedule groups, either as a specific product (Item relation type = Item) or as part of an item allocation key (item relation type = group).</span></span>    
2. <span data-ttu-id="a4e18-122">Wählen Sie im Feld "Artikelrelation" "Artikel" aus.</span><span class="sxs-lookup"><span data-stu-id="a4e18-122">In the Item relation type field, select Item</span></span>
3. <span data-ttu-id="a4e18-123">Geben Sie im Feld "Artikelnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a4e18-123">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="a4e18-124">Geben Sie im Feld "Durchsatzverhältnis" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="a4e18-124">In the Throughput ratio field, enter a number.</span></span>
    * <span data-ttu-id="a4e18-125">Das standardmäßige Durchsatzverhältnis ist 1, was bedeutet, dass die zugehörigen Produkte exakt die Kapazität verbraucht werden, die in den Verarbeitungsaktivitäten der Produktionsflüsse angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a4e18-125">The default Throughput ratio is 1, which means that the related products consume exactly the capacity specified in the process activites of the production flows.</span></span> <span data-ttu-id="a4e18-126">Ein Durchsatzverhältnis > 1 definiert einen höheren Ressourcenverbrauch, Durchsatzverhältnis > 1 definiert den geringeren Ressourcenverbrauch.</span><span class="sxs-lookup"><span data-stu-id="a4e18-126">Throughput ratio > 1 defines a higher resource consumption, Throughput ratio < 1 defines a lower resource consumption.</span></span> <span data-ttu-id="a4e18-127">Das Verhältnis wird in der Kostenberechnung und bei der Berechnung des Kanban-Einzelvorgangsverbrauchs verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4e18-127">The ratio is used in the cost calculation and in the calculation of the kanban job consumption.</span></span>  

## <a name="associate-item-allocation-key"></a><span data-ttu-id="a4e18-128">Zuordnen eines Artikelverteilungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="a4e18-128">Associate item allocation key</span></span>
1. <span data-ttu-id="a4e18-129">Zuordnen eines Artikelverteilungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="a4e18-129">Associate an item allocation key</span></span>
    * <span data-ttu-id="a4e18-130">Fügen Sie einem Artikelverteilungsschlüssel eine Zuordnung hinzu, indem Sie die Artikelrelationstyp "Gruppe" verwenden.</span><span class="sxs-lookup"><span data-stu-id="a4e18-130">Add an association to an item allocation key by using the Item relation type Group.</span></span>   <span data-ttu-id="a4e18-131">Beachten Sie das Sie für diesen Prozess einen Planungsartikelzuordnungsschlüssel in Ihren Daten benötigen.</span><span class="sxs-lookup"><span data-stu-id="a4e18-131">Note that for this process, you need a forecast item alllocation key defined in your data.</span></span>  
2. <span data-ttu-id="a4e18-132">Wählen Sie im Feld "Artikelrelation" "Gruppe" aus.</span><span class="sxs-lookup"><span data-stu-id="a4e18-132">In the Item relation type field, select Group</span></span>
3. <span data-ttu-id="a4e18-133">Klicken Sie im Feld "Artikelzuteilungsschlüssel" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a4e18-133">In the Item allocation key field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a4e18-134">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="a4e18-134">In the list, click the link in the selected row.</span></span>

