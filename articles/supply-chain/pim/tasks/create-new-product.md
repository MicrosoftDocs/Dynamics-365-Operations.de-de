---
title: Neues Produkt erstellen
description: In diesem Thema wird beschrieben, wie Sie ein neues freigegebenes Produkt erstellen.
author: ShylaThompson
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 722414eee1e738e1438bbb40dbd9b8ca606f9245
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844800"
---
# <a name="create-a-new-product"></a><span data-ttu-id="80865-103">Neues Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="80865-103">Create a new product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="80865-104">In diesem Thema wird beschrieben, wie Sie ein neues freigegebenes Produkt erstellen.</span><span class="sxs-lookup"><span data-stu-id="80865-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="80865-105">Es wird in der Regel von einem Produktdesigner ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="80865-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="80865-106">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="80865-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="80865-107">Ein Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="80865-107">Create a product</span></span>
1. <span data-ttu-id="80865-108">Wechseln Sie im Navigationsbereich zu **Module > Produktinformationsverwaltung > Produkte > Produkte**.</span><span class="sxs-lookup"><span data-stu-id="80865-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="80865-109">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="80865-109">Select **New**.</span></span>
3. <span data-ttu-id="80865-110">Geben Sie im Feld **Produktnummer** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="80865-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="80865-111">Wenn kein Nummernkreis für die Produktnummer eingerichtet wurde, muss er manuell eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="80865-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="80865-112">Geben Sie im Feld **Produktname** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="80865-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="80865-113">Der Produktname wird standardmäßig zum Suchbegriff.</span><span class="sxs-lookup"><span data-stu-id="80865-113">The product name defaults to the search name.</span></span> <span data-ttu-id="80865-114">Diesen Wert können Sie bei Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="80865-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="80865-115">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="80865-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="80865-116">Richten Sie Dimensionsgruppen ein</span><span class="sxs-lookup"><span data-stu-id="80865-116">Set up dimension groups</span></span>
1. <span data-ttu-id="80865-117">Klicken Sie auf **Dimensionsgruppen**, um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="80865-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="80865-118">Geben Sie im Feld **Lagerdimensionsgruppe** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="80865-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="80865-119">Die Lagerdimensionsgruppe bestimmt, welche Lagerdimensionen Sie zu jeder Transaktion für das Produkt eingeben müssen und wie es im Bestand nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="80865-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="80865-120">Geben Sie im Feld **Rückverfolgungsgruppe** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="80865-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="80865-121">Die Rückverfolgungsangabengruppe bestimmt, welche Rückverfolgungsangaben Sie für jede Transaktion für das Produkt eingeben müssen und wie es im Bestand behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="80865-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="80865-122">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="80865-122">Select **OK**.</span></span>

