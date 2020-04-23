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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 1e423199d0639db5e403e280880036b590149095
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172945"
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