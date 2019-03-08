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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9754c46010e7bbdb2edef0d6e68162f344bb1257
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "343166"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="5746f-103">Berechnung zu einem Produktkonfigurationsmodell hinzufügen</span><span class="sxs-lookup"><span data-stu-id="5746f-103">Add a calculation to a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5746f-104">Im folgenden Verfahren sehen Sie, wie Sie einen neuen Berechnung zu einem Produktkonfigurationsmodell hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="5746f-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="5746f-105">Darin wird angezeigt, wie Sie einen logischen Ausdruck unter Verwendung des "If"-Operators erstellen können, um eine Lautsprecherhöhe bis 10 für weiße Lautsprecher und 15 für alle anderen Gehäusefarben festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5746f-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="5746f-106">Das Verfahren verwendet die Komponente "High end speaker" im Vorführungsunternehmen USMF.</span><span class="sxs-lookup"><span data-stu-id="5746f-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="5746f-107">Eine Berechnung hinzufügen</span><span class="sxs-lookup"><span data-stu-id="5746f-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="5746f-108">Berechnungsausdruck erstellen</span><span class="sxs-lookup"><span data-stu-id="5746f-108">Create calculation expression</span></span>
1. <span data-ttu-id="5746f-109">Klicken Sie auf "Ausdruck bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="5746f-109">Click Edit expression.</span></span>
2. <span data-ttu-id="5746f-110">Geben Sie im Feld "ConstraintBody" "If[CabinetFinish== "White", 10, 15]" ein.</span><span class="sxs-lookup"><span data-stu-id="5746f-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="5746f-111">Klicken Sie auf "Überprüfen".</span><span class="sxs-lookup"><span data-stu-id="5746f-111">Click Validate.</span></span>
4. <span data-ttu-id="5746f-112">Klicken Sie auf "Schließen".</span><span class="sxs-lookup"><span data-stu-id="5746f-112">Click Close.</span></span>
5. <span data-ttu-id="5746f-113">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5746f-113">Click OK.</span></span>

