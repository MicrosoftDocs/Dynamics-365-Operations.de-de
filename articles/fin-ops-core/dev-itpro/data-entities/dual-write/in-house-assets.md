---
title: Interne Anlagen für Wartungsarbeiten
description: Dieses Thema beschreibt, wie Sie Microsoft Dynamics 365 Field Service verwenden können, um sowohl Debitor-Anlagen als auch interne Anlagen zu warten.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ebda6b5679ec601513fb6d046725b396e69fe0f3
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941413"
---
# <a name="in-house-assets-for-servicing"></a>Interne Anlagen für Wartungsarbeiten

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Field Service wurde entwickelt, um Kundenanlagen zu unterstützen. Asset Management für Dynamics 365 Supply Chain Management wurde entwickelt, um das interne Vermögen zu erhalten. Durch die Integration dieser beiden Apps können Sie Field Service verwenden, um sowohl Kunden- als auch interne Assets zu warten. Sie können die Assets auch anhand des Funktionsstandorts oder der Hierarchie klassifizieren und die Wartung auf einer detaillierten Ebene verfolgen.

Weitere Informationen finden Sie unter [Integrieren Dynamics 365 Field Service und Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Vorlagen

Hausinterne Anlagen enthalten eine Sammlung von wichtigen Tabellenzuordnungen, die während der Dateninteraktion zusammenarbeiten, wie in der folgenden Tabelle dargestellt.

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]