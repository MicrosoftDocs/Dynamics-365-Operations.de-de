---
title: Berechnung zu einem Produktkonfigurationsmodell hinzufügen
description: Im folgenden Verfahren sehen Sie, wie Sie einen neuen Berechnung zu einem Produktkonfigurationsmodell hinzufügen können.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55f8fcfdafb2d5fb5a4d4800221fabf4b2111f86
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150262"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="e4236-103">Berechnung zu einem Produktkonfigurationsmodell hinzufügen</span><span class="sxs-lookup"><span data-stu-id="e4236-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e4236-104">Im folgenden Verfahren sehen Sie, wie Sie einen neuen Berechnung zu einem Produktkonfigurationsmodell hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="e4236-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="e4236-105">Darin wird angezeigt, wie Sie einen logischen Ausdruck unter Verwendung des "If"-Operators erstellen können, um eine Lautsprecherhöhe bis 10 für weiße Lautsprecher und 15 für alle anderen Gehäusefarben festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e4236-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="e4236-106">Das Verfahren verwendet die Komponente "High end speaker" im Vorführungsunternehmen USMF.</span><span class="sxs-lookup"><span data-stu-id="e4236-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="e4236-107">Eine Berechnung hinzufügen</span><span class="sxs-lookup"><span data-stu-id="e4236-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="e4236-108">Berechnungsausdruck erstellen</span><span class="sxs-lookup"><span data-stu-id="e4236-108">Create calculation expression</span></span>
1. <span data-ttu-id="e4236-109">Klicken Sie auf "Ausdruck bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="e4236-109">Click Edit expression.</span></span>
2. <span data-ttu-id="e4236-110">Geben Sie im Feld "ConstraintBody" "If[CabinetFinish== "White", 10, 15]" ein.</span><span class="sxs-lookup"><span data-stu-id="e4236-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="e4236-111">Klicken Sie auf "Überprüfen".</span><span class="sxs-lookup"><span data-stu-id="e4236-111">Click Validate.</span></span>
4. <span data-ttu-id="e4236-112">Klicken Sie auf "Schließen".</span><span class="sxs-lookup"><span data-stu-id="e4236-112">Click Close.</span></span>
5. <span data-ttu-id="e4236-113">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="e4236-113">Click OK.</span></span>

