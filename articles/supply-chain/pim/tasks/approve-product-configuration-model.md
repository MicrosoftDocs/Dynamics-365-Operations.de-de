---
title: Ein Produktkonfigurationsmodell genehmigen
description: Die Ausführung dieser Prozedur erfordert mindestens ein vorhandenes Produktkonfigurationsmodell.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eef6568e012c311c0e5438245c011b876fc4d522
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844969"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="52798-103">Ein Produktkonfigurationsmodell genehmigen</span><span class="sxs-lookup"><span data-stu-id="52798-103">Approve a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="52798-104">Die Ausführung dieser Prozedur erfordert mindestens ein vorhandenes Produktkonfigurationsmodell.</span><span class="sxs-lookup"><span data-stu-id="52798-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="52798-105">Diese Prozedur verwendet das Spitzenlautsprechermodell im Vorführungsunternehmen USMF.</span><span class="sxs-lookup"><span data-stu-id="52798-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="52798-106">Beachten Sie, dass dieses Modell bereits genehmigt wurde. Das Verfahren führt Sie jedoch durch den gesamten Prozess.</span><span class="sxs-lookup"><span data-stu-id="52798-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="52798-107">Klicken Sie auf "Produktvariantenmodell-Definition".</span><span class="sxs-lookup"><span data-stu-id="52798-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="52798-108">Klicken Sie auf "Produktkonfigurationsmodelle".</span><span class="sxs-lookup"><span data-stu-id="52798-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="52798-109">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="52798-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="52798-110">Wählen Sie den Spitzenlautsprecher für diese Aufgabe aus.</span><span class="sxs-lookup"><span data-stu-id="52798-110">Select the High end speaker model for this procedure.</span></span>  
4. <span data-ttu-id="52798-111">Klicken Sie auf "Versionen".</span><span class="sxs-lookup"><span data-stu-id="52798-111">Click Versions.</span></span>
5. <span data-ttu-id="52798-112">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="52798-112">Click New.</span></span>
6. <span data-ttu-id="52798-113">Geben Sie im Feld "Produktnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="52798-113">In the Product number field, enter or select a value.</span></span>
    * <span data-ttu-id="52798-114">Die Referenz auf einem Produkt stellt eine Version eines Produktkonfigurationsmodells dar.</span><span class="sxs-lookup"><span data-stu-id="52798-114">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="52798-115">Nur Produktmaster mit der einschränkungsbasierter Konfigurationstechnologie werden in dieser Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="52798-115">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
7. <span data-ttu-id="52798-116">Geben Sie in das Feld "Von Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="52798-116">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="52798-117">Wählen Sie aus, wann die Produktmodellversion verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="52798-117">Select when the product model version will be available.</span></span>  
8. <span data-ttu-id="52798-118">Geben Sie in das Feld "Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="52798-118">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="52798-119">Wählen Sie ein Enddatum zu dem diese Produktmodellversion abläuft, oder wählen Sie "Nie" aus.</span><span class="sxs-lookup"><span data-stu-id="52798-119">Select an end date when this product model version will expire, or select Never.</span></span>  
9. <span data-ttu-id="52798-120">Klicken Sie auf "Genehmigen", um den Dropdown-Dialog zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="52798-120">Click Approve to open the drop dialog.</span></span>
10. <span data-ttu-id="52798-121">Geben Sie im Feld 'Genehmig von' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="52798-121">In the Approved by field, enter or select a value.</span></span>
    * <span data-ttu-id="52798-122">Wählen Sie die Person aus, die für die Genehmigung der Produktmodelle für die Verwendung in diesem Arbeitsgang zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="52798-122">Select the person who is responsible for approving product models for use in operations.</span></span>  
11. <span data-ttu-id="52798-123">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="52798-123">Click OK.</span></span>
12. <span data-ttu-id="52798-124">Wählen Sie im Feld "Preis" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="52798-124">In the Pricing method field, select an option.</span></span>
    * <span data-ttu-id="52798-125">Aktivieren Sie die Produktmodellversion.</span><span class="sxs-lookup"><span data-stu-id="52798-125">Activate the product model version.</span></span> <span data-ttu-id="52798-126">Sie können nur ein Produkt gleichzeitig haben, das für ein Produktmodell aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="52798-126">It is only possible to have one product active for one product model at a time.</span></span>  
13. <span data-ttu-id="52798-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="52798-127">Close the page.</span></span>

