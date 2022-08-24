---
title: Interne Anlagen für Wartungsarbeiten
description: Dieser Artikel beschreibt, wie Sie Microsoft Dynamics 365 Field Service verwenden können, um sowohl Debitor-Anlagen als auch interne Anlagen zu warten.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: b3e741c85fcad2abc18879280ef7332ae091c984
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289249"
---
# <a name="in-house-assets-for-servicing"></a>Interne Anlagen für Wartungsarbeiten

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Field Service wurde entwickelt, um Kundenanlagen zu unterstützen. Asset Management für Dynamics 365 Supply Chain Management wurde entwickelt, um das interne Vermögen zu erhalten. Durch die Integration dieser beiden Apps können Sie Field Service verwenden, um sowohl Kunden- als auch interne Assets zu warten. Sie können die Assets auch anhand des Funktionsstandorts oder der Hierarchie klassifizieren und die Wartung auf einer detaillierten Ebene verfolgen.

Weitere Informationen finden Sie unter [Integrieren Dynamics 365 Field Service und Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Vorlagen

Hausinterne Anlagen enthalten eine Sammlung von wichtigen Tabellenzuordnungen, die während der Dateninteraktion zusammenarbeiten, wie in der folgenden Tabelle dargestellt.

| Finanz- und Betriebs-Apps | Customer Engagement-Apps | Beschreibung |
|-----------------------------|-----------------------------------|-------------|
[Wählen Sie Anlagenverwaltung Anlagen Lebenszyklusmodelle](mapping-reference.md#119) | msdyn_assetlifecyclemodels | |
[Wählen Sie Anlagenverwaltung Anlagen Lebenszyklusstatus](mapping-reference.md#120) | msdyn_assetlifecyclestates | |
[Anlagenverwaltungs-Anlagentypen](mapping-reference.md#124) | msdyn_customerassetcategories | |
[Anlagenverwaltungs-Anlagen](mapping-reference.md#125) | msdyn_customerassets | |
[Anlagenverwaltung funktionale StandortevLebenszyklusmodelle](mapping-reference.md#134) | msdyn_functionallocationlifecyclemodels | |
[Anlagenverwaltung funktionale Standorte Lebenszyklusstatus](mapping-reference.md#135) | msdyn_functionallocationlifecyclestates | |
[Anlageverwaltung und funktionale Standorttypen](mapping-reference.md#137) | msdyn_functionallocationtypes | |
[Anlageverwaltung und funktionale Standorte](mapping-reference.md#136) | msdyn_functionallocations | |
[Anlagenverwaltungshersteller](mapping-reference.md#153) | msdyn_manufacturers | |
[Anlagenverwaltungsmodelle](mapping-reference.md#154) | msdyn_models | |
[Anlagenverwaltungsgarantie](mapping-reference.md#209) | msdyn_warranties | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
