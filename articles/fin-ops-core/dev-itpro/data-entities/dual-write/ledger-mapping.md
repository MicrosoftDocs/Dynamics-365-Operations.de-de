---
title: Integriertes Sachkonto
description: In diesem Thema wird die Integration von Sachkontodaten zwischen Finance and Operations und anderen Dynamics 365-Anwendungen mithilfe von Dataverse beschrieben.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 0deb4198acb59b90bf06e4050889d028df2223e3
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063646"
---
# <a name="integrated-ledger"></a>Integriertes Sachkonto

[!include [banner](../../includes/banner.md)]



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
