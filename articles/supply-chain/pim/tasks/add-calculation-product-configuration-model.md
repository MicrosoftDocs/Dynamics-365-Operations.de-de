---
title: Berechnung zu einem Produktkonfigurationsmodell hinzufügen
description: Im folgenden Verfahren sehen Sie, wie Sie einen neuen Berechnung zu einem Produktkonfigurationsmodell hinzufügen können.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49d09a3544631960e3f6b292dbdd8927dd499f07
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987053"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="38460-103">Berechnung zu einem Produktkonfigurationsmodell hinzufügen</span><span class="sxs-lookup"><span data-stu-id="38460-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="38460-104">Im folgenden Verfahren sehen Sie, wie Sie einen neuen Berechnung zu einem Produktkonfigurationsmodell hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="38460-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="38460-105">Darin wird angezeigt, wie Sie einen logischen Ausdruck unter Verwendung des "If"-Operators erstellen können, um eine Lautsprecherhöhe bis 10 für weiße Lautsprecher und 15 für alle anderen Gehäusefarben festzulegen.</span><span class="sxs-lookup"><span data-stu-id="38460-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="38460-106">Das Verfahren verwendet die Komponente "High end speaker" im Vorführungsunternehmen USMF.</span><span class="sxs-lookup"><span data-stu-id="38460-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="38460-107">Eine Berechnung hinzufügen</span><span class="sxs-lookup"><span data-stu-id="38460-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="38460-108">Berechnungsausdruck erstellen</span><span class="sxs-lookup"><span data-stu-id="38460-108">Create calculation expression</span></span>
1. <span data-ttu-id="38460-109">Klicken Sie auf "Ausdruck bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="38460-109">Click Edit expression.</span></span>
2. <span data-ttu-id="38460-110">Geben Sie im Feld "ConstraintBody" "If[CabinetFinish== "White", 10, 15]" ein.</span><span class="sxs-lookup"><span data-stu-id="38460-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="38460-111">Klicken Sie auf "Überprüfen".</span><span class="sxs-lookup"><span data-stu-id="38460-111">Click Validate.</span></span>
4. <span data-ttu-id="38460-112">Klicken Sie auf "Schließen".</span><span class="sxs-lookup"><span data-stu-id="38460-112">Click Close.</span></span>
5. <span data-ttu-id="38460-113">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="38460-113">Click OK.</span></span>

