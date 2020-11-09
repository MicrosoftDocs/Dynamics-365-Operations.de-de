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
# <a name="in-house-assets-for-servicing"></a>Inhouse-Assets für die Wartung

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Field Service wurde entwickelt, um Kundenvermögen zu bedienen. Asset Management für Dynamics 365 Supply Chain Management wurde entwickelt, um das interne Vermögen zu erhalten. Durch die Integration dieser beiden Apps können Sie Field Service verwenden, um sowohl Kunden- als auch interne Assets zu warten. Sie können die Assets auch anhand des Funktionsstandorts oder der Hierarchie klassifizieren und die Wartung auf einer detaillierten Ebene verfolgen.

Weitere Informationen finden Sie unter [Integrieren Dynamics 365 Field Service und Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Vorlagen

In-House-Anlagen enthalten eine Sammlung von wichtigen Finanzentitätszuordnungen, die während der Dateninteraktion zusammenarbeiten, wie in der folgenden Tabelle dargestellt.

| Finance and Operations Apps | Modellgesteuerte Anwendungen in Dynamics 365 | Beschreibung |
|-----------------------------|-----------------------------------|-------------|
| Wählen Sie Anlagenverwaltung Anlagen Lebenszyklusmodelle | Msdyn\_AssetLifecyclemodels | |
| Wählen Sie Anlagenverwaltung Anlagen Lebenszyklusstatus | msdyn\_assetlifecyclestates | |
| Anlagenverwaltungs-Anlagen | msdyn\_customerassets | |
| Anlagenverwaltungs-Anlagentypen | msdyn\_customerassetcategories | |
| Anlagenverwaltung funktionale StandortevLebenszyklusmodelle | Msdyn \_functionallocationlifecyclemodels | |
| Anlagenverwaltung funktionale Standorte Lebenszyklusstatus | msdyn\_functionallocationlifecyclestates | |
| Anlageverwaltung und funktionale Standorte | msdyn\_functionallocations | |
| Anlageverwaltung und funktionale Standorttypen | msdyn\_functionallocationtypes | |
| Anlagenverwaltungshersteller | Msdyn \_Hersteller | |
| Anlagenverwaltungsmodelle | msdyn\_models | |
| Anlagenverwaltungsgarantie | msdyn\_warranties | |

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
