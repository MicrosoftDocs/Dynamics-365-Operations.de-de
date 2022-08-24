---
title: Integrierte Steuer
description: Dieser Artikel beschreibt die Integration von Steuerdaten zwischen Finance und Operations und Dataverse.
author: josaw
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8f148b710e2294edf1e402b9b8b22cb24e60a1f2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288793"
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

