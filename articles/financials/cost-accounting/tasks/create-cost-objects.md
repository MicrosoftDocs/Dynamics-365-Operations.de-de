---
title: Kostenobjekte erstellen
description: Dieses Verfahren zeigt, wie Kostenobjekte erstellt werden, indem die Dynamics 365 for Finance and Operations Enterprise Edition Kostenstellenfinanzdimension in die Kostenrechnung über einen Datenkonnektor importieren.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12de1d51658092fb19f652cef7c1cc78b255b5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543770"
---
# <a name="create-cost-objects"></a><span data-ttu-id="d45ea-103">Kostenobjekte erstellen</span><span class="sxs-lookup"><span data-stu-id="d45ea-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d45ea-104">Dieses Verfahren zeigt, wie Kostenobjekte erstellt werden, indem die Dynamics 365 for Finance and Operations Enterprise Edition Kostenstellenfinanzdimension in die Kostenrechnung über einen Datenkonnektor importieren.</span><span class="sxs-lookup"><span data-stu-id="d45ea-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="d45ea-105">Das USMF-Demodatenunternehmen wurde verwendet, um diese Prozedur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d45ea-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="d45ea-106">Diese Prozedur ist eine Funktion, für die Kostenrechnung-Funktion, die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="d45ea-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="d45ea-107">Neue Kostenobjekte erstellen</span><span class="sxs-lookup"><span data-stu-id="d45ea-107">Create new cost objects</span></span>
1. <span data-ttu-id="d45ea-108">Wechseln Sie zu den Kostenrechnung > Dimensionen > Kostenobjektdimensionen.</span><span class="sxs-lookup"><span data-stu-id="d45ea-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="d45ea-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d45ea-109">Click New.</span></span>
3. <span data-ttu-id="d45ea-110">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d45ea-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d45ea-111">Geben Sie im Feld "Datenkonnektor für Dimensionsmitglieder" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d45ea-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="d45ea-112">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d45ea-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="d45ea-113">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d45ea-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="d45ea-114">Den Datenkonnektor konfigurieren</span><span class="sxs-lookup"><span data-stu-id="d45ea-114">Configure the data connector</span></span>
1. <span data-ttu-id="d45ea-115">Klicken Sie auf "Dimensionselementanbieter konfigurieren".</span><span class="sxs-lookup"><span data-stu-id="d45ea-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="d45ea-116">Wählen Sie CostCenter aus, um CostCenter-Dimension in die Kostenrechnung zu importieren.</span><span class="sxs-lookup"><span data-stu-id="d45ea-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="d45ea-117">Wählen Sie im Dimensionsnamen-Feld Sie die Kostenstelle aus.</span><span class="sxs-lookup"><span data-stu-id="d45ea-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="d45ea-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d45ea-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="d45ea-119">Kostenstellen importieren</span><span class="sxs-lookup"><span data-stu-id="d45ea-119">Import cost centers</span></span>
1. <span data-ttu-id="d45ea-120">Klicken Sie auf "Dimensionsmitglieder importieren".</span><span class="sxs-lookup"><span data-stu-id="d45ea-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="d45ea-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d45ea-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="d45ea-122">Importierte Kostenstellen anzeigen</span><span class="sxs-lookup"><span data-stu-id="d45ea-122">View the imported cost centers</span></span>
1. <span data-ttu-id="d45ea-123">Klicken Sie auf "Dimensionsmitglieder anzeigen".</span><span class="sxs-lookup"><span data-stu-id="d45ea-123">Click View dimension members.</span></span>

