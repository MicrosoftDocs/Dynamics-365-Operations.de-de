---
title: Mehrwertsteuer für Online-Aufträge konfigurieren
description: Dieses Thema bietet eine Übersicht über die Auswahl von Mehrwertsteuergruppen für verschiedene Online-Auftragstypen in Dynamics 365 Commerce.
author: gvrmohanreddy
manager: AnnBe
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8df939c1a566fb63bc53e455cc6c2aa85956ac79
ms.sourcegitcommit: 583801af75c50915ea5ffc60e831fb617d045533
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "5853810"
---
# <a name="configure-sales-tax-for-online-orders"></a>Mehrwertsteuer für Online-Aufträge konfigurieren

[!include [banner](includes/banner.md)]

Dieses Thema bietet einen Überblick über die Auswahl von Mehrwertsteuergruppen für verschiedene Online-Auftragstypen unter Verwendung von steuerlichen Einstellungen auf Ziel oder Debitorenkontobasis. 

Ihr E-Commerce-Kanal soll möglicherweise Optionen wie Lieferung oder Abholung für Online-Aufträge unterstützen. Die Anwendbarkeit der Mehrwertsteuer basiert auf der von Ihren Onlinedebitoren ausgewählten Option. 

## <a name="destination-based-taxes-for-online-orders"></a>Zielbasierte Steuern für Online-Bestellungen

Im Allgemeinen werden Steuern für Online-Aufträge, die an Kundenadressen geliefert werden, vom Zielort bestimmt. Jede Mehrwertsteuergruppe hat eine Einzelhandelsziel-basierte Steuerkonfiguration, in der Ihr Unternehmen die Zieldetails definieren kann, wie Land oder Region, Bundesland, Landkreis und Ort in einer hierarchischen Form.

### <a name="orders-delivered-to-customer-address"></a>An eine Debitorenadresse gelieferte Aufträge

Wenn ein Online-Auftrag erteilt wird, verwendet das Commerce-Steuermodul die Lieferadresse jeder Position im Auftrag und sucht Mehrwertsteuergruppen mit übereinstimmenden zielbasierten Steuerkriterien. Bei einem Online-Auftrag mit San Francisco, Kalifornien, USA, als Positionslieferadresse findet das Steuermodul die Mehrwertsteuergruppe und den Mehrwertsteuercode für Kalifornien und berechnet dann entsprechend die Steuer für jede einzelne Position.

### <a name="order-pick-up-in-store"></a>Auftragsabholung im Laden

Für Auftragspositionen, bei denen Abholung im Laden oder Abholung am Straßenrand angegeben ist, wird die Steuergruppe aus dem ausgewählten Abholladen angewendet. Details zum Einrichten der Mehrwertsteuer für einen bestimmten Laden finden Sie unter [Andere Steueroptionen für Läden festlegen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

## <a name="customer-account-based-taxes-for-online-orders"></a>Debitorenkontobasierte Steuern für Online-Bestellungen

Möglicherweise gibt es ein Geschäftsszenario, in dem Sie eine Mehrwertsteuergruppe für ein bestimmtes Debitorenkonto in der Commerce-Zentralverwaltung konfigurieren möchten. In der Zentralverwaltung gibt es zwei Stellen, an denen Sie die Mehrwertsteuer für ein Debitorenkonto konfigurieren können. Um auf diese zuzugreifen, müssen Sie zunächst eine Seite „Debitorendetails“ aufrufen, indem Sie auf **Retail und Commerce \> Debitoren \> Alle Debitoren** gehen und dann einen Debitor auswählen.

Die zwei Stellen, an denen Sie die Mehrwertsteuer für ein Debitorenkonto konfigurieren können, sind:

- **Mehrwertsteuergruppe** auf dem Inforegister **Rechnung und Lieferung** der Seite „Debitorendetails“. 
- **Mehrwertsteuer** auf dem Inforegister **Allgemein** der Seite **Adressen verwalten**. Um von der Seite „Debitorendetails“ dorthin zu gelangen, wählen Sie eine bestimmte Adresse im Inforegister **Adressen** und dann **Erweitert** aus.

> [!TIP]
> Wenn Sie bei Online-Kundenbestellungen nur die zielbasierten Steuern anwenden und debitorenkontobasierte Steuern vermeiden möchten, stellen Sie sicher, dass das Feld **Mehrwertsteuergruppe** im Inforegister **Rechnung und Lieferung** der Seite „Debitorendetails“ leer ist. Um sicherzustellen, dass für Neukunden, die sich über den Online-Kanal anmelden, nicht die Einstellungen der Mehrwertsteuergruppe aus den Standardeinstellungen für Debitoren oder Debitorengruppen übernommen werden, stellen Sie sicher, dass das **Mehrwertsteuergruppe** für die Standard-Debitoreneinstellungen und Debitorengruppeneinstellungen des Onlinekanals ebenfalls leer ist (**Retail und Commerce \> Debitoren \> Debitorengruppen**).

## <a name="determine-destination-based-tax-or-customer-account-based-tax-applicability"></a>Die anwendbare zielbasierte oder debitorenkontobasierte Steuer bestimmen 

In der folgenden Tabelle wird erläutert, ob für Online-Bestellungen zielbasierte oder debitorenkontobasierte Steuern angewendet werden. 

| Debitorentyp | Versandadresse                   | Debitor > Rechnung und Lieferung> Mehrwertsteuergruppe? | Adresse auf Debitorenkonto in der Zentralverwaltung? | Debitorenadresse > Erweitert > Allgemein > Mehrwertsteuergruppe?                                              | Angewendete Mehrwertsteuergruppe      |
|---------------|------------------------------------|-----------------------------------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------|------------------------------|
| Gast         | Manhattan, New York                      | Nein (leer)                                                | Nein (leer)                              | Nein (leer)                                                                                                   | New York (zielbasierte Steuern) |
| Angemeldet     | Austin, Texas                          | Nein (leer)                                             | Ja                               | Keines<br/><br/>Neue Adresse über Onlinekanal hinzugefügt.                                                            | Texas (zielbasierte Steuern) |
| Angemeldet     | San Francisco, Kalifornien (Abholung im Geschäft) | Ja (New York)                                            | Nicht zutreffend                              | Nicht zutreffend                                                                                                    | Kalifornien (zielbasierte Steuern) |
| Angemeldet     | Houston, Texas                         | Ja (New York)                                            | Ja                               | Ja (New York)<br/><br/>Neue Adresse über Onlinekanal und Mehrwertsteuergruppe hinzugefügt, die vom Debitorenkonto übernommen wurde. | New York (debitorenkontobasierte Steuern)  |
| Angemeldet     | Austin, Texas                          | Ja (New York)                                            | Ja                               | Ja (New York)<br/><br/>Neue Adresse über Onlinekanal und Mehrwertsteuergruppe hinzugefügt, die vom Debitorenkonto übernommen wurde. | New York (debitorenkontobasierte Steuern)  |
| Angemeldet     | Sarasota, Florida                       | Ja (New York)                                            | Ja                               | Ja (Washington)<br/><br/>Manuell auf Washington gesetzt.                                                                          | Washington (debitorenkontobasierte Steuern)  |
| Angemeldet     | Sarasota, Florida                       | Nein (leer)                                                | Ja                               | Ja (Washington)<br/><br/>Manuell auf Washington gesetzt.                                                                          | Washington (debitorenkontobasierte Steuern)  |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einrichten von Steuern für Onlineshops auf Zielbasis](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)

[Übersicht über die Mehrwertsteuer](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[Mehrwertsteuer-Berechnungsmethoden im Feld „Ursprung“](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[Mehrwertsteuer-Zuweisung und -Außerkraftsetzungen](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[Optionen zur Berechnung von Gesamtbetrag und Intervall für Mehrwertsteuercodes](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[Berechnung der Steuerbefreiung](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
