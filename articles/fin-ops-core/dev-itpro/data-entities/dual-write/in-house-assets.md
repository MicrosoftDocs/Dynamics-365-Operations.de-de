---
title: Inhouse-Assets für die Wartung
description: In diesem Thema wird beschrieben, wie Sie mit Microsoft Dtnamics 365 Field Service sowohl Kunden- als auch interne Assets warten können.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 0e87a3d645c19fab3bb0560ba5114d193e2d0be7
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997169"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="f102e-103">Inhouse-Assets für die Wartung</span><span class="sxs-lookup"><span data-stu-id="f102e-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="f102e-104">Microsoft Dynamics 365 Field Service wurde entwickelt, um Kundenvermögen zu bedienen.</span><span class="sxs-lookup"><span data-stu-id="f102e-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="f102e-105">Asset Management für Dynamics 365 Supply Chain Management wurde entwickelt, um das interne Vermögen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f102e-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="f102e-106">Durch die Integration dieser beiden Apps können Sie Field Service verwenden, um sowohl Kunden- als auch interne Assets zu warten.</span><span class="sxs-lookup"><span data-stu-id="f102e-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="f102e-107">Sie können die Assets auch anhand des Funktionsstandorts oder der Hierarchie klassifizieren und die Wartung auf einer detaillierten Ebene verfolgen.</span><span class="sxs-lookup"><span data-stu-id="f102e-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="f102e-108">Weitere Informationen finden Sie unter [Integrieren Dynamics 365 Field Service und Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span><span class="sxs-lookup"><span data-stu-id="f102e-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="f102e-109">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="f102e-109">Templates</span></span>

<span data-ttu-id="f102e-110">In-House-Anlagen enthalten eine Sammlung von wichtigen Finanzentitätszuordnungen, die während der Dateninteraktion zusammenarbeiten, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f102e-110">In-house-assets include a collection of core entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="f102e-111">Finance and Operations Apps</span><span class="sxs-lookup"><span data-stu-id="f102e-111">Finance and Operations apps</span></span> | <span data-ttu-id="f102e-112">Modellgesteuerte Anwendungen in Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="f102e-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="f102e-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f102e-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="f102e-114">Wählen Sie Anlagenverwaltung Anlagen Lebenszyklusmodelle</span><span class="sxs-lookup"><span data-stu-id="f102e-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="f102e-115">Msdyn\_AssetLifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="f102e-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="f102e-116">Wählen Sie Anlagenverwaltung Anlagen Lebenszyklusstatus</span><span class="sxs-lookup"><span data-stu-id="f102e-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="f102e-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="f102e-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="f102e-118">Anlagenverwaltungs-Anlagen</span><span class="sxs-lookup"><span data-stu-id="f102e-118">Asset management assets</span></span> | <span data-ttu-id="f102e-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="f102e-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="f102e-120">Anlagenverwaltungs-Anlagentypen</span><span class="sxs-lookup"><span data-stu-id="f102e-120">Asset management asset types</span></span> | <span data-ttu-id="f102e-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="f102e-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="f102e-122">Anlagenverwaltung funktionale StandortevLebenszyklusmodelle</span><span class="sxs-lookup"><span data-stu-id="f102e-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="f102e-123">Msdyn \_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="f102e-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="f102e-124">Anlagenverwaltung funktionale Standorte Lebenszyklusstatus</span><span class="sxs-lookup"><span data-stu-id="f102e-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="f102e-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="f102e-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="f102e-126">Anlageverwaltung und funktionale Standorte</span><span class="sxs-lookup"><span data-stu-id="f102e-126">Asset management functional locations</span></span> | <span data-ttu-id="f102e-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="f102e-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="f102e-128">Anlageverwaltung und funktionale Standorttypen</span><span class="sxs-lookup"><span data-stu-id="f102e-128">Asset management functional location types</span></span> | <span data-ttu-id="f102e-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="f102e-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="f102e-130">Anlagenverwaltungshersteller</span><span class="sxs-lookup"><span data-stu-id="f102e-130">Asset management manufacturers</span></span> | <span data-ttu-id="f102e-131">Msdyn \_Hersteller</span><span class="sxs-lookup"><span data-stu-id="f102e-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="f102e-132">Anlagenverwaltungsmodelle</span><span class="sxs-lookup"><span data-stu-id="f102e-132">Asset management models</span></span> | <span data-ttu-id="f102e-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="f102e-133">msdyn\_models</span></span> | |
| <span data-ttu-id="f102e-134">Anlagenverwaltungsgarantie</span><span class="sxs-lookup"><span data-stu-id="f102e-134">Asset management warranty</span></span> | <span data-ttu-id="f102e-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="f102e-135">msdyn\_warranties</span></span> | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]
