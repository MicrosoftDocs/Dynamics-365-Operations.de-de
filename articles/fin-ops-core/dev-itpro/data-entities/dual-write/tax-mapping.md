---
title: Integrierte Steuer
description: In diesem Artikel wird die Integration von Steuerdaten zwischen Finance + Operations und Dataverse beschrieben.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8864a9567d57739aa72fa1859f5cfce6df33e8f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864542"
---
# <a name="integrated-tax"></a>Integrierte Steuer

[!include [banner](../../includes/banner.md)]



Steuereinstellungsdaten definieren die Einstellung sowohl für indirekte Steuern (MwSt., GST, Mehrwertsteuer) und Quellensteuer. Es werden die Steuerberechnungsregel, der Steuersatz, die Steuerbuchhaltung, der Steuerausgleich und weitere Konzepte beschrieben.

## <a name="templates"></a>Vorlagen

Steuerdaten enthalten eine Sammlung von Tabellenzuordnungen, die während der Dateninteraktion zusammenarbeiten, wie in der folgenden Tabelle dargestellt.

| Finanz- und Betriebs-Apps | Customer Engagement-Apps | Description |
|-----------------------------|-----------------------------------|-------------|
[Artikel-Mehrwertsteuergruppe](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Mehrwertsteuer-Behörden](mapping-reference.md#193) | msdyn_taxauthorities | |
[Entität „Mehrwertsteuer-Befreiungscode“ in CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[Mehrwertsteuergruppen](mapping-reference.md#195) | msdyn_taxgroups | |
[Mehrwertsteuer-Sachkontobuchungsgruppen V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Quellensteuercodes](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Quellensteuergruppen](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
