---
title: Integriertes Sachkonto
description: In diesem Thema wird die Integration von Sachkontodaten zwischen Finance and Operations und anderen Dynamics 365-Anwendungen mithilfe von Dataverse beschrieben.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: rhaertle
ms.openlocfilehash: 9e6e65b2b8ec8241bc2082b30ae641692c31afdd
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542660"
---
# <a name="integrated-ledger"></a>Integriertes Sachkonto

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In einer Geschäftsanwendung definieren Sachkontodaten den Kern der Geschäftsabläufe eines Unternehmens. Sachkontodaten beschreiben beispielsweise das Geschäftsjahr, in dem das Unternehmen tätig ist, die Währungen, in denen es handelt, und die Konten, die es verwendet. In diesem Thema wird die Integration dieser Finanzkennzahlen beschrieben.

## <a name="templates"></a>Vorlagen

Sachkontodaten enthalten eine Sammlung von wichtigen Tabellenzuordnungen, die während der Dateninteraktion zusammenarbeiten, wie in der folgenden Tabelle dargestellt.

Finance and Operations-Apps | Customer Engagement-Apps     | Beschreibung
---------------------------------|----------------------------------|------------
[CDS-Wechselkurse](mapping-reference.md#123) | msdyn_currencyexchangerates |
[Kontenplan](mapping-reference.md#121) | msdyn_chartofaccountses |
[Währungen](mapping-reference.md#218) | transactioncurrencies |
[Währungspaar für Wechselkurs](mapping-reference.md#122) | msdyn_currencyexchangeratepairs |
[Wechselkurstyp](mapping-reference.md#129) | msdyn_exchangeratetypes |
[Finanzdimensionsformat](mapping-reference.md#130) | msdyn_financialdimensionformats |
[Finanzdimensionen](mapping-reference.md#128) | msdyn_dimensionattributes |
[Entität „Steuerkalenderintegration“](mapping-reference.md#132) | msdyn_fiscalcalendars |
[Steuerkalenderperiode](mapping-reference.md#131) | msdyn_fiscalcalendarperiods |
[Entität „Steuerkalender-Jahresintegration“](mapping-reference.md#133) | msdyn_fiscalcalendaryears |
[Unternehmen](mapping-reference.md#148) | msdyn_ledgers |
[Hauptkonto](mapping-reference.md#152) | msdyn_mainaccounts |
[Hauptkontokategorien](mapping-reference.md#151) | msdyn_mainaccountcategories |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
