---
title: Verkaufspreisauswahlkriterien erstellen
description: Dieses Verfahren zeigt, wie ein Verkaufspreisauswahlkriterium für attributbasierte Verkaufspreismodelle erstellt wird.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72940f719baca5e8042c2f2caa8abbacb7d8264e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844488"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="acd55-103">Verkaufspreisauswahlkriterien erstellen</span><span class="sxs-lookup"><span data-stu-id="acd55-103">Create sales price selection criteria</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="acd55-104">Dieses Verfahren zeigt, wie ein Verkaufspreisauswahlkriterium für attributbasierte Verkaufspreismodelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="acd55-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="acd55-105">Dieses Verfahren erfordert, dass mindestens ein Verkaufspreismodell vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="acd55-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="acd55-106">Dieses Beispiel verwendet das Preismodell für das Lautsprecherlösungs-Verkaufspreismodell im USMF-Demodatunternehmen.</span><span class="sxs-lookup"><span data-stu-id="acd55-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="acd55-107">Normalerweise wird ein Produktmanager dieses Verfahren durchführen.</span><span class="sxs-lookup"><span data-stu-id="acd55-107">Typically, a product manager uses this procedure.</span></span>


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="acd55-108">Hinzufügen eines neuen Kriteriums für ein vorhandenes Verkaufspreismodell</span><span class="sxs-lookup"><span data-stu-id="acd55-108">Add a new criterion for an existing sales price model</span></span>
1. <span data-ttu-id="acd55-109">Klicken Sie auf "Produktvariantenmodell-Definition".</span><span class="sxs-lookup"><span data-stu-id="acd55-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="acd55-110">Klicken Sie auf "Produktkonfigurationsmodelle".</span><span class="sxs-lookup"><span data-stu-id="acd55-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="acd55-111">In Sie wählen der Liste die Zeile für das Lautsprecherlösungsproduktmodell aus, aber klicken Sie nicht auf den Link für den Modellnamen.</span><span class="sxs-lookup"><span data-stu-id="acd55-111">In the list, select the row for the Speaker solution product model, but don’t click the link for the model name.</span></span>
4. <span data-ttu-id="acd55-112">Klicken Sie im Aktivitätsbereich auf "Modell".</span><span class="sxs-lookup"><span data-stu-id="acd55-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="acd55-113">Klicken Sie auf Preismodellkriterien.</span><span class="sxs-lookup"><span data-stu-id="acd55-113">Click Price model criteria.</span></span>
6. <span data-ttu-id="acd55-114">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="acd55-114">Click New.</span></span>
7. <span data-ttu-id="acd55-115">Geben Sie im Feld "Name" "Debitorengruppe 10" ein.</span><span class="sxs-lookup"><span data-stu-id="acd55-115">In the Name field, type ‘Customer group 10’.</span></span>
    * <span data-ttu-id="acd55-116">Der Name des Preismodellkriteriums wird verwendet, um die zugrunde liegenden Auswahlkriterien zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="acd55-116">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
8. <span data-ttu-id="acd55-117">Geben Sie im Feld 'Preismodell' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="acd55-117">In the Price model field, enter or select a value.</span></span>
9. <span data-ttu-id="acd55-118">Wählen Sie im Feld "Auftragstyp" die Option "Bestellung" aus.</span><span class="sxs-lookup"><span data-stu-id="acd55-118">In the Order type field, select Sales order.</span></span>
    * <span data-ttu-id="acd55-119">Der Auftragstyp bestimmt die Datenbankfelder, die für die Auswahlabfrage verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="acd55-119">The order type determines the database fields that will be available for the selection query.</span></span>  
10. <span data-ttu-id="acd55-120">Geben Sie ein Datum in das Feld "Gültig ab" ein.</span><span class="sxs-lookup"><span data-stu-id="acd55-120">In the Valid from field, enter a date.</span></span>
11. <span data-ttu-id="acd55-121">Geben Sie im Feld "Ablaufzeitpunkt" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="acd55-121">In the Expire by field, enter a date.</span></span>
12. <span data-ttu-id="acd55-122">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="acd55-122">Click Save.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="acd55-123">Erstellen einer Abfrage für die Auswahlkriterien</span><span class="sxs-lookup"><span data-stu-id="acd55-123">Create the query for the selection criteria</span></span>
1. <span data-ttu-id="acd55-124">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="acd55-124">Click Edit.</span></span>
2. <span data-ttu-id="acd55-125">Wählen Sie im Feld "Debitoren" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="acd55-125">In the Table field, select Customers.</span></span> 
3. <span data-ttu-id="acd55-126">Wählen Sie im Feld "Feld" "Debitorengruppe" aus.</span><span class="sxs-lookup"><span data-stu-id="acd55-126">In the Field field, select Customer group.</span></span>
    * <span data-ttu-id="acd55-127">In diesem Beispiel verwenden wir eine bestimmte Debitorengruppe für die Auswahlkriterien.</span><span class="sxs-lookup"><span data-stu-id="acd55-127">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="acd55-128">Wählen Sie im Feld "Kriterien" "Debitorengruppe 10" aus.</span><span class="sxs-lookup"><span data-stu-id="acd55-128">In the Criteria field, select Customer group 10.</span></span> 
5. <span data-ttu-id="acd55-129">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="acd55-129">Click OK.</span></span>

