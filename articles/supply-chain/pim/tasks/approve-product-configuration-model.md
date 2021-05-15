---
title: Ein Produktkonfigurationsmodell genehmigen
description: Die Ausführung dieser Prozedur erfordert mindestens ein vorhandenes Produktkonfigurationsmodell.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c945756997b0580ac7ffb19261f9184e53a1c10
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920506"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="db5a7-103">Ein Produktkonfigurationsmodell genehmigen</span><span class="sxs-lookup"><span data-stu-id="db5a7-103">Approve a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="db5a7-104">Die Ausführung dieser Prozedur erfordert mindestens ein vorhandenes Produktkonfigurationsmodell.</span><span class="sxs-lookup"><span data-stu-id="db5a7-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="db5a7-105">Diese Prozedur verwendet das Spitzenlautsprechermodell im Vorführungsunternehmen USMF.</span><span class="sxs-lookup"><span data-stu-id="db5a7-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="db5a7-106">Beachten Sie, dass dieses Modell bereits genehmigt wurde. Das Verfahren führt Sie jedoch durch den gesamten Prozess.</span><span class="sxs-lookup"><span data-stu-id="db5a7-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="db5a7-107">Wechseln Sie zu **Produktinformationsmanagement \> Produkte \> Produktkonfigurationsmodelle**.</span><span class="sxs-lookup"><span data-stu-id="db5a7-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="db5a7-108">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="db5a7-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="db5a7-109">Wählen Sie den Spitzenlautsprecher für diese Aufgabe aus.</span><span class="sxs-lookup"><span data-stu-id="db5a7-109">Select the High end speaker model for this procedure.</span></span>  
1. <span data-ttu-id="db5a7-110">Wählen Sie **Versionen**.</span><span class="sxs-lookup"><span data-stu-id="db5a7-110">Select **Versions**.</span></span>
1. <span data-ttu-id="db5a7-111">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="db5a7-111">Select **New**.</span></span>
1. <span data-ttu-id="db5a7-112">Geben Sie im Feld **Produktnummer** einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="db5a7-112">In the **Product number** field, enter or select a value.</span></span>
    * <span data-ttu-id="db5a7-113">Die Referenz auf einem Produkt stellt eine Version eines Produktkonfigurationsmodells dar.</span><span class="sxs-lookup"><span data-stu-id="db5a7-113">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="db5a7-114">Nur Produktmaster mit der einschränkungsbasierter Konfigurationstechnologie werden in dieser Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="db5a7-114">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
1. <span data-ttu-id="db5a7-115">Geben Sie im Feld **Von Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="db5a7-115">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="db5a7-116">Wählen Sie aus, wann die Produktmodellversion verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="db5a7-116">Select when the product model version will be available.</span></span>  
1. <span data-ttu-id="db5a7-117">Geben Sie im Feld **Bis Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="db5a7-117">In the **To date** field, enter a date.</span></span>
    * <span data-ttu-id="db5a7-118">Wählen Sie ein Enddatum zu dem diese Produktmodellversion abläuft, oder wählen Sie "Nie" aus.</span><span class="sxs-lookup"><span data-stu-id="db5a7-118">Select an end date when this product model version will expire, or select Never.</span></span>  
1. <span data-ttu-id="db5a7-119">Wählen Sie **Genehmigen**, um den Dropdown-Dialog zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="db5a7-119">Select **Approve** to open the drop dialog.</span></span>
1. <span data-ttu-id="db5a7-120">Geben Sie im Feld **Genehmigt von** einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="db5a7-120">In the **Approved by** field, enter or select a value.</span></span>
    * <span data-ttu-id="db5a7-121">Wählen Sie die Person aus, die für die Genehmigung der Produktmodelle für die Verwendung in diesem Arbeitsgang zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="db5a7-121">Select the person who is responsible for approving product models for use in operations.</span></span>  
1. <span data-ttu-id="db5a7-122">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="db5a7-122">Select **OK**.</span></span>
1. <span data-ttu-id="db5a7-123">Wählen Sie im Feld **Preismethode** eine Option.</span><span class="sxs-lookup"><span data-stu-id="db5a7-123">In the **Pricing method** field, select an option.</span></span>
    * <span data-ttu-id="db5a7-124">Aktivieren Sie die Produktmodellversion.</span><span class="sxs-lookup"><span data-stu-id="db5a7-124">Activate the product model version.</span></span> <span data-ttu-id="db5a7-125">Sie können nur ein Produkt gleichzeitig haben, das für ein Produktmodell aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="db5a7-125">It is only possible to have one product active for one product model at a time.</span></span>  
1. <span data-ttu-id="db5a7-126">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="db5a7-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]