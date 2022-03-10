---
title: Integrierte Steuer
description: In diesem Thema wird die Integration von Steuerdaten zwischen Finance and Operations und Dataverse beschrieben.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 532e6603b74ad0293d65684d2d6858ef31fbc496
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063186"
---
# <a name="integrated-tax"></a>Integrierte Steuer

[!include [banner](../../includes/banner.md)]



Steuereinstellungsdaten definieren die Einstellung sowohl für indirekte Steuern (MwSt., GST, Mehrwertsteuer) und Quellensteuer. Es werden die Steuerberechnungsregel, der Steuersatz, die Steuerbuchhaltung, der Steuerausgleich und weitere Konzepte beschrieben.

## <a name="templates"></a>Vorlagen

Steuerdaten enthalten eine Sammlung von Tabellenzuordnungen, die während der Dateninteraktion zusammenarbeiten, wie in der folgenden Tabelle dargestellt.

| Finance and Operations-Apps | Customer Engagement-Apps | Description |
|-----------------------------|-----------------------------------|-------------|
[Artikel-Mehrwertsteuergruppe](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Mehrwertsteuer-Behörden](mapping-reference.md#193) | msdyn_taxauthorities | |
[Entität „Mehrwertsteuer-Befreiungscode“ in CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[Mehrwertsteuergruppen](mapping-reference.md#195) | msdyn_taxgroups | |
[Mehrwertsteuer-Sachkontobuchungsgruppen V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Quellensteuercodes](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Quellensteuergruppen](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
