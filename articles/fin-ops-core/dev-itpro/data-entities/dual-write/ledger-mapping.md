---
title: Integriertes Sachkonto
description: Dieser Artikel beschreibt die Integration von Sachkontodaten zwischen Finanzen und Betrieb und anderen Dynamics 365-Anwendungen unter Verwendung der Dataverse.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e5598295a25e31b33cd8b4d7ce3250a982ab4e87
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112239"
---
# <a name="integrated-ledger"></a>Integriertes Sachkonto

[!include [banner](../../includes/banner.md)]



In einer Geschäftsanwendung definieren Sachkontodaten den Kern der Geschäftsabläufe eines Unternehmens. Sachkontodaten beschreiben beispielsweise das Geschäftsjahr, in dem das Unternehmen tätig ist, die Währungen, in denen es handelt, und die Konten, die es verwendet. In diesem Artikel wird die Integration dieser Finanzkennzahlen beschrieben.

## <a name="templates"></a>Vorlagen

Sachkontodaten enthalten eine Sammlung von wichtigen Tabellenzuordnungen, die während der Dateninteraktion zusammenarbeiten, wie in der folgenden Tabelle dargestellt.

Finanz- und Betriebs-Apps | Customer Engagement-Apps     | Beschreibung
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

