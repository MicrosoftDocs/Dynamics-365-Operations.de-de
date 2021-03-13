---
title: Neues Produkt erstellen
description: In diesem Thema wird beschrieben, wie Sie ein neues freigegebenes Produkt erstellen.
author: ShylaThompson
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d313d76d40476bec5c8bc9c8ea5fc93b217e7e87
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007565"
---
# <a name="create-a-new-product"></a><span data-ttu-id="12d8b-103">Neues Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="12d8b-103">Create a new product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="12d8b-104">In diesem Thema wird beschrieben, wie Sie ein neues freigegebenes Produkt erstellen.</span><span class="sxs-lookup"><span data-stu-id="12d8b-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="12d8b-105">Es wird in der Regel von einem Produktdesigner ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12d8b-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="12d8b-106">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="12d8b-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="12d8b-107">Ein Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="12d8b-107">Create a product</span></span>
1. <span data-ttu-id="12d8b-108">Wechseln Sie im Navigationsbereich zu **Module > Produktinformationsverwaltung > Produkte > Produkte**.</span><span class="sxs-lookup"><span data-stu-id="12d8b-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="12d8b-109">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="12d8b-109">Select **New**.</span></span>
3. <span data-ttu-id="12d8b-110">Geben Sie im Feld **Produktnummer** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="12d8b-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="12d8b-111">Wenn kein Nummernkreis für die Produktnummer eingerichtet wurde, muss er manuell eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="12d8b-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="12d8b-112">Geben Sie im Feld **Produktname** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="12d8b-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="12d8b-113">Der Produktname wird standardmäßig zum Suchbegriff.</span><span class="sxs-lookup"><span data-stu-id="12d8b-113">The product name defaults to the search name.</span></span> <span data-ttu-id="12d8b-114">Diesen Wert können Sie bei Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="12d8b-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="12d8b-115">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="12d8b-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="12d8b-116">Richten Sie Dimensionsgruppen ein</span><span class="sxs-lookup"><span data-stu-id="12d8b-116">Set up dimension groups</span></span>
1. <span data-ttu-id="12d8b-117">Klicken Sie auf **Dimensionsgruppen**, um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="12d8b-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="12d8b-118">Geben Sie im Feld **Lagerdimensionsgruppe** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="12d8b-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="12d8b-119">Die Lagerdimensionsgruppe bestimmt, welche Lagerdimensionen Sie zu jeder Transaktion für das Produkt eingeben müssen und wie es im Bestand nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="12d8b-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="12d8b-120">Geben Sie im Feld **Rückverfolgungsgruppe** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="12d8b-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="12d8b-121">Die Rückverfolgungsangabengruppe bestimmt, welche Rückverfolgungsangaben Sie für jede Transaktion für das Produkt eingeben müssen und wie es im Bestand behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="12d8b-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="12d8b-122">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="12d8b-122">Select **OK**.</span></span>

