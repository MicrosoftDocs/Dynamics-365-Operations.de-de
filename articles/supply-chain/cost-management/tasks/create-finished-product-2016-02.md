---
title: Ein fertiges Produkt erstellen (nur Februar 2016)
description: Diese Aufgabe konzentriert sich auf das Erstellen eines fertigen Produkts.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44f9693e04160ffe9307de5e454d8269ca883679
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "339026"
---
# <a name="create-a-finished-product-february-2016-only"></a><span data-ttu-id="4aa4e-103">Ein fertiges Produkt erstellen (nur Februar 2016)</span><span class="sxs-lookup"><span data-stu-id="4aa4e-103">Create a finished product (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4aa4e-104">Diese Aufgabe konzentriert sich auf das Erstellen eines fertigen Produkts.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-104">This task focuses on creating a finished product.</span></span> <span data-ttu-id="4aa4e-105">Es ist die erste Aufgabe in der Stücklistenberechnungsserie.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-105">It is the first task in the BOM calculation series.</span></span> <span data-ttu-id="4aa4e-106">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="4aa4e-107">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="4aa4e-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="4aa4e-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="4aa4e-108">Click New.</span></span>
3. <span data-ttu-id="4aa4e-109">Geben Sie im Feld "Produktnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="4aa4e-110">Geben Sie für die Demonstration BOM_1 ein.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-110">For the demonstration, type BOM_1.</span></span>  
4. <span data-ttu-id="4aa4e-111">Geben Sie im Feld "Artikelmodellgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="4aa4e-112">Wählen Sie STD aus.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-112">Select STD.</span></span> <span data-ttu-id="4aa4e-113">STD steht für Standardkosten und ist das am häufigsten verwendete Modell, wenn mit Kostenberechnungen gearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="4aa4e-114">Geben Sie im Feld "Artikelgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="4aa4e-115">Wählen Sie z. B. „Audio” aus.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-115">For example, select Audio.</span></span> <span data-ttu-id="4aa4e-116">Dies hat keine Auswirkungen auf Kostenberechnungen.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="4aa4e-117">Geben Sie im Feld "Lagerdimensionsgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="4aa4e-118">Wählen Sie „SiteWH” aus.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-118">Select SiteWH.</span></span> <span data-ttu-id="4aa4e-119">Nur „Standort” und „Lagerort” werden für die Demonstration verwendet.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-119">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="4aa4e-120">Geben Sie im Feld "Rückverfolgungsangabengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="4aa4e-121">Rückverfolgungsangaben werden nicht für dieses Beispiel verwendet, wählen Sie „Keine” aus.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="4aa4e-122">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4aa4e-122">Click OK.</span></span>
9. <span data-ttu-id="4aa4e-123">Klicken Sie im Aktivitätsbereich auf "Lagerbestand verwalten".</span><span class="sxs-lookup"><span data-stu-id="4aa4e-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="4aa4e-124">Klicken Sie auf "Standardmäßige Auftragseinstellungen".</span><span class="sxs-lookup"><span data-stu-id="4aa4e-124">Click Default order settings.</span></span>
11. <span data-ttu-id="4aa4e-125">Wählen Sie im Feld „Standardauftragstyp” die Option „Produktion” aus.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="4aa4e-126">Da dies ein fertiges Produkt ist, das produziert wird, wählen Sie „Produktion” aus.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-126">Because this is a finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="4aa4e-127">Geben Sie im Feld „Einkaufsstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="4aa4e-128">Für die Demonstration wählen Sie „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-128">For the demonstration, select Site 1.</span></span>  
13. <span data-ttu-id="4aa4e-129">Geben Sie im Feld „Lagerstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="4aa4e-130">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="4aa4e-131">Geben Sie im Feld „Verkaufsstandort” einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="4aa4e-132">Wählen Sie für dieses Beispiel „Standort 1” aus.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="4aa4e-133">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-133">Close the page.</span></span>

