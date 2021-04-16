---
title: Mehrwertsteuer für Online-Aufträge konfigurieren
description: Dieses Thema bietet eine Übersicht über die Auswahl von Mehrwertsteuergruppen für verschiedene Online-Auftragstypen in Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 11/16/2020
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
ms.openlocfilehash: 68b7e59a1e1ea18bdcd4e7a9117e4892407f40ff
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791846"
---
# <a name="configure-sales-tax-for-online-orders"></a>Mehrwertsteuer für Online-Aufträge konfigurieren

[!include [banner](includes/banner.md)]

Dieses Thema bietet eine Übersicht über die Auswahl von Mehrwertsteuergruppen für verschiedene Online-Auftragstypen. 

Ihr E-Commerce-Kanal möchte möglicherweise Optionen wie Lieferung oder Abholung für Online-Aufträge unterstützen. Die Anwendbarkeit der Mehrwertsteuer basiert auf der von Ihren Online-Benutzern ausgewählten Option. Wenn ein Websitekunde sich entscheidet, einen Artikel online zu kaufen, und ihn an eine Adresse geliefert bekommt, wird die Mehrwertsteuer basierend auf der Steuergruppeneinstellung der Lieferadresse des Kunden bestimmt. Wenn sich ein Kunde dafür entscheidet, einen gekauften Artikel in einem Geschäft abzuholen, wird die Mehrwertsteuer basierend auf der Steuergruppeneinstellung des Abholgeschäfts ermittelt. 

## <a name="orders-shipped-to-a-customer-address"></a>An eine Kundenadresse gelieferte Aufträge 

Im Allgemeinen werden Steuern für Online-Aufträge, die an Kundenadressen geliefert werden, vom Zielort bestimmt. Jede Mehrwertsteuergruppe hat eine Einzelhandelsziel-basierte Steuerkonfiguration, in der Ihr Unternehmen die Zieldetails definieren kann, wie Land/Region, Bundesland, Landkreis und Ort in einer hierarchischen Form. Wenn ein Online-Auftrag erteilt wird, verwendet das Commerce-Steuermodul die Lieferadresse jeder Position im Auftrag und sucht Mehrwertsteuergruppen mit übereinstimmenden zielbasierten Steuerkriterien. Bei einem Online-Auftrag mit San Francisco, Kalifornien, USA, als Positionslieferadresse findet das Steuermodul die Mehrwertsteuergruppe und den Mehrwertsteuercode für Kalifornien und berechnet dann entsprechend die Steuer für jede einzelne Position.  

## <a name="customer-based-tax-groups"></a>Kundenbasierte Steuergruppen

In der Commerce-Zentralverwaltung gibt es zwei Stellen, an denen Kundensteuergruppen konfiguriert werden:

- **Kundenprofil**
- **Lieferadresse des Kunden**

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a>Wenn für das Profil eines Kunden eine Steuergruppe konfiguriert wurde

Für den Profildatensatz eines Kunden in der Zentralverwaltung wurde möglicherweise eine Mehrwertsteuergruppe konfiguriert. Für Online-Aufträge wird die in einem Kundenprofil konfigurierte Mehrwertsteuergruppe jedoch nicht vom Steuermodul verwendet. 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a>Wenn für die Lieferadresse eines Kunden eine Steuergruppe konfiguriert wurde

Wenn für den Lieferadressdatensatz eines Kunden eine Steuergruppe konfiguriert ist und ein Online-Auftrag (oder Positionsartikel) an die Lieferadresse des Kunden geliefert wird, wird die im Adressdatensatz des Kunden konfigurierte Steuergruppe vom Steuermodul für Steuerberechnungen verwendet.

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a>Eine Steuergruppe für den Lieferadressdatensatz eines Kunden konfigurieren

Führen Sie die folgenden Schritte aus, um eine Steuergruppe für den Lieferadressdatensatz eines Kunden in der Commerce-Zentralverwaltung zu konfigurieren.

1. Wechseln Sie zu **Alle Kunden** und wählen Sie dann den gewünschten Kunden aus. 
1. Im Inforegister **Adressen** wählen Sie die gewünschte Adresse und dann **Weitere Optionen \> Erweitert** aus. 
1. Unter der Registerkarte **Allgemein** auf der Seite **Adressen verwalten** legen Sie den Mehrwertsteuerwert nach Bedarf fest.

> [!NOTE]
> Die Steuergruppe wird anhand der Lieferadresse der Auftragsposition definiert und die zielbasierten Steuern werden in der Steuergruppe selbst konfiguriert. Weitere Informationen finden Sie unter [Steuern für Online-Shops auf der Grundlage des Ziels einrichten](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

## <a name="order-pickup-in-store"></a>Auftragsabholung im Laden

Für Auftragspositionen, bei denen Abholung im Laden oder Abholung am Straßenrand angegeben ist, wird die Steuergruppe aus dem ausgewählten Abholladen angewendet. Details zum Konfigurieren der Steuergruppe für einen bestimmten Laden finden Sie unter [Andere Steueroptionen für Läden festlegen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

> [!NOTE]
> Wenn eine Bestellposition in einem Geschäft abgeholt wird, werden die Adresssteuereinstellungen des Kunden (sofern eingerichtet) vom Steuermodul ignoriert und die Steuerkonfiguration des Abholladens werden angewendet. 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Mehrwertsteuerübersicht](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[Mehrwertsteuer-Berechnungsmethoden im Feld „Ursprung“](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[Mehrwertsteuer-Zuweisung und -Außerkraftsetzungen](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[Optionen zur Berechnung von Gesamtbetrag und Intervall für Mehrwertsteuercodes](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[Berechnung der Steuerbefreiung](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]