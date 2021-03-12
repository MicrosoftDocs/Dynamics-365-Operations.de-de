---
title: Kostenobjekte erstellen
description: Dieses Verfahren zeigt, wie Kostenobjekte erstellt werden, indem die Kostenstellenfinanzdimension in die Kostenrechnung über einen Datenkonnektor importiert wird.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3d2ef7d6549bdeb3ba2afd2a594f36b47c912db
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990766"
---
# <a name="create-cost-objects"></a><span data-ttu-id="d7d9d-103">Kostenobjekte erstellen</span><span class="sxs-lookup"><span data-stu-id="d7d9d-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d7d9d-104">Dieses Verfahren zeigt, wie Kostenobjekte erstellt werden, indem die Kostenstellenfinanzdimension in die Kostenrechnung über einen Datenkonnektor importiert wird.</span><span class="sxs-lookup"><span data-stu-id="d7d9d-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="d7d9d-105">Das USMF-Demodatenunternehmen wurde verwendet, um diese Prozedur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d7d9d-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="d7d9d-106">Neue Kostenobjekte erstellen</span><span class="sxs-lookup"><span data-stu-id="d7d9d-106">Create new cost objects</span></span>
1. <span data-ttu-id="d7d9d-107">Wechseln Sie zu den Kostenrechnung > Dimensionen > Kostenobjektdimensionen.</span><span class="sxs-lookup"><span data-stu-id="d7d9d-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="d7d9d-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d7d9d-108">Click New.</span></span>
3. <span data-ttu-id="d7d9d-109">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d7d9d-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d7d9d-110">Geben Sie im Feld "Datenkonnektor für Dimensionsmitglieder" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d7d9d-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="d7d9d-111">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d7d9d-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="d7d9d-112">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d7d9d-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="d7d9d-113">Den Datenkonnektor konfigurieren</span><span class="sxs-lookup"><span data-stu-id="d7d9d-113">Configure the data connector</span></span>
1. <span data-ttu-id="d7d9d-114">Klicken Sie auf "Dimensionselementanbieter konfigurieren".</span><span class="sxs-lookup"><span data-stu-id="d7d9d-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="d7d9d-115">Wählen Sie CostCenter aus, um CostCenter-Dimension in die Kostenrechnung zu importieren.</span><span class="sxs-lookup"><span data-stu-id="d7d9d-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="d7d9d-116">Wählen Sie im Dimensionsnamen-Feld Sie die Kostenstelle aus.</span><span class="sxs-lookup"><span data-stu-id="d7d9d-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="d7d9d-117">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d7d9d-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="d7d9d-118">Kostenstellen importieren</span><span class="sxs-lookup"><span data-stu-id="d7d9d-118">Import cost centers</span></span>
1. <span data-ttu-id="d7d9d-119">Klicken Sie auf "Dimensionsmitglieder importieren".</span><span class="sxs-lookup"><span data-stu-id="d7d9d-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="d7d9d-120">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d7d9d-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="d7d9d-121">Importierte Kostenstellen anzeigen</span><span class="sxs-lookup"><span data-stu-id="d7d9d-121">View the imported cost centers</span></span>
1. <span data-ttu-id="d7d9d-122">Klicken Sie auf "Dimensionsmitglieder anzeigen".</span><span class="sxs-lookup"><span data-stu-id="d7d9d-122">Click View dimension members.</span></span>

