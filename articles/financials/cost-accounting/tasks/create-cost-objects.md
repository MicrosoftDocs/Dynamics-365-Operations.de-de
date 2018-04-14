--- 
title: Kostenobjekte erstellen
description: "Diese Prozedur zeigt an, wie Kostenobjekte erstellt werden, indem die Kostenstellen-Finanzdimension von Dynamics 365 for Finance and Operations nach Kostenrechnung über einen Datenkonnektor importiert wird."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e469fc30d649aac0c544b6de9e17fd173f3ce497
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="create-cost-objects"></a><span data-ttu-id="a3ee5-103">Kostenobjekte erstellen</span><span class="sxs-lookup"><span data-stu-id="a3ee5-103">Create cost objects</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a3ee5-104">Diese Prozedur zeigt an, wie Kostenobjekte erstellt werden, indem die Kostenstellen-Finanzdimension von Dynamics 365 for Finance and Operations nach Kostenrechnung über einen Datenkonnektor importiert wird.</span><span class="sxs-lookup"><span data-stu-id="a3ee5-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="a3ee5-105">Das USMF-Demodatenunternehmen wurde verwendet, um diese Prozedur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a3ee5-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="a3ee5-106">Diese Prozedur ist für eine Kostenbuchhaltungs-Funktion, die in Microsoft Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="a3ee5-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="a3ee5-107">Neue Kostenobjekte erstellen</span><span class="sxs-lookup"><span data-stu-id="a3ee5-107">Create new cost objects</span></span>
1. <span data-ttu-id="a3ee5-108">Wechseln Sie zu den Kostenrechnung > Dimensionen > Kostenobjektdimensionen.</span><span class="sxs-lookup"><span data-stu-id="a3ee5-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="a3ee5-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="a3ee5-109">Click New.</span></span>
3. <span data-ttu-id="a3ee5-110">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a3ee5-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a3ee5-111">Geben Sie im Feld "Datenkonnektor für Dimensionsmitglieder" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a3ee5-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="a3ee5-112">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a3ee5-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="a3ee5-113">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="a3ee5-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="a3ee5-114">Den Datenkonnektor konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a3ee5-114">Configure the data connector</span></span>
1. <span data-ttu-id="a3ee5-115">Klicken Sie auf "Dimensionselementanbieter konfigurieren".</span><span class="sxs-lookup"><span data-stu-id="a3ee5-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="a3ee5-116">Wählen Sie CostCenter aus, um CostCenter-Dimension in die Kostenrechnung zu importieren.</span><span class="sxs-lookup"><span data-stu-id="a3ee5-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="a3ee5-117">Wählen Sie im Dimensionsnamen-Feld Sie die Kostenstelle aus.</span><span class="sxs-lookup"><span data-stu-id="a3ee5-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="a3ee5-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="a3ee5-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="a3ee5-119">Kostenstellen importieren</span><span class="sxs-lookup"><span data-stu-id="a3ee5-119">Import cost centers</span></span>
1. <span data-ttu-id="a3ee5-120">Klicken Sie auf "Dimensionsmitglieder importieren".</span><span class="sxs-lookup"><span data-stu-id="a3ee5-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="a3ee5-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="a3ee5-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="a3ee5-122">Importierte Kostenstellen anzeigen</span><span class="sxs-lookup"><span data-stu-id="a3ee5-122">View the imported cost centers</span></span>
1. <span data-ttu-id="a3ee5-123">Klicken Sie auf "Dimensionsmitglieder anzeigen".</span><span class="sxs-lookup"><span data-stu-id="a3ee5-123">Click View dimension members.</span></span>


