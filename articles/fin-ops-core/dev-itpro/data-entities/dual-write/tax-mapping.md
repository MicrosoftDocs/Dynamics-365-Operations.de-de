---
title: Integrierte Steuer
description: In diesem Thema wird die Integration von Steuerdaten zwischen Finance and Operations and Dataverse beschrieben.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: rhaertle
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: c7e76294944196670ed4b02ebf785c1bed7b5106f73d4b66a15a19c9a4235cbf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738551"
---
# <a name="integrated-tax"></a>Integrierte Steuer

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Steuereinstellungsdaten definieren die Einstellung sowohl für indirekte Steuern (MwSt., GST, Mehrwertsteuer) und Quellensteuer. Es werden die Steuerberechnungsregel, der Steuersatz, die Steuerbuchhaltung, der Steuerausgleich und weitere Konzepte beschrieben.

## <a name="templates"></a>Vorlagen

Steuerdaten enthalten eine Sammlung von Tabellenzuordnungen, die während der Dateninteraktion zusammenarbeiten, wie in der folgenden Tabelle dargestellt.

| Finance and Operations Apps | Customer Engagement-Apps | Beschreibung |
|-----------------------------|-----------------------------------|-------------|
[Artikel-Mehrwertsteuergruppe](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Mehrwertsteuer-Behörden](mapping-reference.md#193) | msdyn_taxauthorities | |
[Entität „Mehrwertsteuer-Befreiungscode“ in CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[Mehrwertsteuergruppen](mapping-reference.md#195) | msdyn_taxgroups | |
[Mehrwertsteuer-Sachkontobuchungsgruppen V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Quellensteuercodes](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Quellensteuergruppen](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
