---
title: Neues Produkt erstellen
description: Diese Aufgabe zeigt, wie ein neues freigegebenes Produkt erstellt wird.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a603d89749242a4c6039ab83da286ec6ab727d8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "328538"
---
# <a name="create-a-new-product"></a><span data-ttu-id="68ba6-103">Neues Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="68ba6-103">Create a new product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="68ba6-104">Diese Aufgabe zeigt, wie ein neues freigegebenes Produkt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="68ba6-104">This task shows how to create a new shared product.</span></span> <span data-ttu-id="68ba6-105">Es wird in der Regel von einem Produktdesigner ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="68ba6-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="68ba6-106">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="68ba6-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="68ba6-107">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Produkte".</span><span class="sxs-lookup"><span data-stu-id="68ba6-107">Go to Product information management > Products > Products.</span></span>

## <a name="create-a-product"></a><span data-ttu-id="68ba6-108">Ein Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="68ba6-108">Create a product</span></span>
1. <span data-ttu-id="68ba6-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="68ba6-109">Click New.</span></span>
2. <span data-ttu-id="68ba6-110">Geben Sie im Feld "Produktnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="68ba6-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="68ba6-111">Wenn kein Nummernkreis für die Produktnummer eingerichtet wurde, muss er manuell eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="68ba6-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
3. <span data-ttu-id="68ba6-112">Geben Sie im Feld "Produktname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="68ba6-112">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="68ba6-113">Der Produktname wird standardmäßig zum Suchbegriff.</span><span class="sxs-lookup"><span data-stu-id="68ba6-113">The product name defaults to the search name.</span></span> <span data-ttu-id="68ba6-114">Diesen Wert können Sie bei Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="68ba6-114">You can change this if needed.</span></span>  
4. <span data-ttu-id="68ba6-115">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="68ba6-115">Click OK.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="68ba6-116">Richten Sie Dimensionsgruppen ein</span><span class="sxs-lookup"><span data-stu-id="68ba6-116">Set up dimension groups</span></span>
1. <span data-ttu-id="68ba6-117">Klicken Sie auf "Dimensionsgruppen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="68ba6-117">Click Dimension groups to open the drop dialog.</span></span>
2. <span data-ttu-id="68ba6-118">Geben Sie im Feld "Lagerdimensionsgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="68ba6-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="68ba6-119">Die Lagerdimensionsgruppe bestimmt, welche Lagerdimensionen Sie zu jeder Transaktion für das Produkt eingeben müssen und wie es im Bestand nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="68ba6-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="68ba6-120">Geben Sie im Feld "Rückverfolgungsangabengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="68ba6-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="68ba6-121">Die Rückverfolgungsangabengruppe bestimmt, welche Rückverfolgungsangaben Sie für jede Transaktion für das Produkt eingeben müssen und wie es im Bestand behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="68ba6-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="68ba6-122">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="68ba6-122">Click OK.</span></span>

