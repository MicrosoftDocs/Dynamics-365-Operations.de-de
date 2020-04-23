---
title: Verkaufspreisauswahlkriterien erstellen
description: Dieses Verfahren zeigt, wie ein Verkaufspreisauswahlkriterium für attributbasierte Verkaufspreismodelle erstellt wird.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6d1385a83da5b6448a9c753d7469979796043b60
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203772"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="c1401-103">Verkaufspreisauswahlkriterien erstellen</span><span class="sxs-lookup"><span data-stu-id="c1401-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c1401-104">Dieses Verfahren zeigt, wie ein Verkaufspreisauswahlkriterium für attributbasierte Verkaufspreismodelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c1401-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="c1401-105">Dieses Verfahren erfordert, dass mindestens ein Verkaufspreismodell vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c1401-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="c1401-106">Dieses Beispiel verwendet das Preismodell für das Lautsprecherlösungs-Verkaufspreismodell im USMF-Demodatunternehmen.</span><span class="sxs-lookup"><span data-stu-id="c1401-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="c1401-107">Normalerweise wird ein Produktmanager dieses Verfahren durchführen.</span><span class="sxs-lookup"><span data-stu-id="c1401-107">Typically, a product manager uses this procedure.</span></span>


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="c1401-108">Hinzufügen eines neuen Kriteriums für ein vorhandenes Verkaufspreismodell</span><span class="sxs-lookup"><span data-stu-id="c1401-108">Add a new criterion for an existing sales price model</span></span>
1. <span data-ttu-id="c1401-109">Klicken Sie auf "Produktvariantenmodell-Definition".</span><span class="sxs-lookup"><span data-stu-id="c1401-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="c1401-110">Klicken Sie auf "Produktkonfigurationsmodelle".</span><span class="sxs-lookup"><span data-stu-id="c1401-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="c1401-111">In der LIste wählen Sie die Zeile für das Lautsprecherlösungsproduktmodell aus, aber klicken Sie nicht auf den Link für den Modellnamen.</span><span class="sxs-lookup"><span data-stu-id="c1401-111">In the list, select the row for the Speaker solution product model, but don't click the link for the model name.</span></span>
4. <span data-ttu-id="c1401-112">Klicken Sie im Aktivitätsbereich auf "Modell".</span><span class="sxs-lookup"><span data-stu-id="c1401-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="c1401-113">Klicken Sie auf Preismodellkriterien.</span><span class="sxs-lookup"><span data-stu-id="c1401-113">Click Price model criteria.</span></span>
6. <span data-ttu-id="c1401-114">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="c1401-114">Click New.</span></span>
7. <span data-ttu-id="c1401-115">Geben Sie im Feld Typ „Debitorengruppe 10“ ein.</span><span class="sxs-lookup"><span data-stu-id="c1401-115">In the Name field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="c1401-116">Der Name des Preismodellkriteriums wird verwendet, um die zugrunde liegenden Auswahlkriterien zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="c1401-116">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
8. <span data-ttu-id="c1401-117">Geben Sie im Feld 'Preismodell' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c1401-117">In the Price model field, enter or select a value.</span></span>
9. <span data-ttu-id="c1401-118">Wählen Sie im Feld "Auftragstyp" die Option "Bestellung" aus.</span><span class="sxs-lookup"><span data-stu-id="c1401-118">In the Order type field, select Sales order.</span></span>
    * <span data-ttu-id="c1401-119">Der Auftragstyp bestimmt die Datenbankfelder, die für die Auswahlabfrage verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c1401-119">The order type determines the database fields that will be available for the selection query.</span></span>  
10. <span data-ttu-id="c1401-120">Geben Sie ein Datum in das Feld "Gültig ab" ein.</span><span class="sxs-lookup"><span data-stu-id="c1401-120">In the Valid from field, enter a date.</span></span>
11. <span data-ttu-id="c1401-121">Geben Sie im Feld "Ablaufzeitpunkt" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="c1401-121">In the Expire by field, enter a date.</span></span>
12. <span data-ttu-id="c1401-122">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="c1401-122">Click Save.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="c1401-123">Erstellen einer Abfrage für die Auswahlkriterien</span><span class="sxs-lookup"><span data-stu-id="c1401-123">Create the query for the selection criteria</span></span>
1. <span data-ttu-id="c1401-124">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="c1401-124">Click Edit.</span></span>
2. <span data-ttu-id="c1401-125">Wählen Sie im Feld "Debitoren" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="c1401-125">In the Table field, select Customers.</span></span> 
3. <span data-ttu-id="c1401-126">Wählen Sie im Feld "Feld" "Debitorengruppe" aus.</span><span class="sxs-lookup"><span data-stu-id="c1401-126">In the Field field, select Customer group.</span></span>
    * <span data-ttu-id="c1401-127">In diesem Beispiel verwenden wir eine bestimmte Debitorengruppe für die Auswahlkriterien.</span><span class="sxs-lookup"><span data-stu-id="c1401-127">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="c1401-128">Wählen Sie im Feld "Kriterien" "Debitorengruppe 10" aus.</span><span class="sxs-lookup"><span data-stu-id="c1401-128">In the Criteria field, select Customer group 10.</span></span> 
5. <span data-ttu-id="c1401-129">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c1401-129">Click OK.</span></span>

