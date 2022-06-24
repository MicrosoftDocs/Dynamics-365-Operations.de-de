---
title: Steuereinstellungen aus dem Steuerberechnungsdienst mit Dynamics 365 Finance synchronisieren
description: In diesem Artikel wird erläutert, wie Masterdaten zu den Steuereinstellungen vom Steuerberechnungsdienst mit Microsoft Dynamics 365 Finance synchronisiert werden.
author: wangchen
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegration, TaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: b017a19834998e1c493b0a38c1b50accd8c7e630
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853156"
---
# <a name="sync-the-tax-setup-from-the-tax-calculation-service-to-dynamics-365-finance"></a>Steuereinstellungen aus dem Steuerberechnungsdienst mit Dynamics 365 Finance synchronisieren

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erläutert, wie Masterdaten zu den Steuereinstellungen vom Steuerberechnungsdienst mit Microsoft Dynamics 365 Finance synchronisiert werden.

Nachdem Sie die erforderlichen Einstellungsschritte in [Mit der Steuerberechnung beginnen](global-get-started-with-tax-calculation-service.md) abgeschlossen haben, werden die folgenden Steuereinstellungsdaten automatisch vom Steuerberechnungsdienst mit Finance synchronisiert.

## <a name="sales-tax-code"></a>Mehrwertsteuercode

| Dienst für Steuerberechnungen           | Finance                             |
| --------------------------------- | ----------------------------------- |
| MwSt.-Code                          | Mehrwertsteuercode                      |
| Description                       | Name                                |
| Benutzereingabe                        | Ausgleichsperiode                   |
| Benutzereingabe                        | Sachkontobuchungsgruppe                |
| Benutzereingabe                        | Mehrwertsteuerwährung                  |
| Ein negativer Steuersatz ist konfiguriert | Negativen Mehrwertsteuersatz zulassen |

## <a name="tax-value"></a>Steuerwert

| Dienst für Steuerberechnungen | Finance                   |
| ----------------------- | ------------------------- |
| Von Buchungsdatum   | Startdatum                 |
| Bis Buchungsdatum     | Bis Datum                   |
| Mindestbetrag          | Untergrenze             |
| Höchstbetrag          | Höchstgrenze             |
| Steuersatz                | Wert                     |
| Nicht abzugsfähiger Tarif     | Nicht abzugsfähiger Prozentsatz |

## <a name="tax-limits"></a>Steuergrenzen

| Dienst für Steuerberechnungen | Finance           |
| ----------------------- | ----------------- |
| Von Buchungsdatum   | Startdatum         |
| Bis Buchungsdatum     | Bis Datum           |
| Mindeststeuerbetrag      | Mindest-Mehrwertsteuer |
| Höchststeuerbetrag      | Höchst-Mehrwertsteuer |

## <a name="sales-tax-group"></a>Mehrwertsteuergruppe

| Dienst für Steuerberechnungen                         | Finance                                    |
| ----------------------------------------------- | ------------------------------------------ |
| Steuergruppe                                       | Mehrwertsteuergruppe                            |
| Steuercodes unter dieser Steuergruppe                  | Mehrwertsteuercodes unter dieser Mehrwertsteuergruppe |
| Der Steuercode ist als **Ist befreit** gekennzeichnet         | Befreit                                     |
| Der Steuercode ist als **Ist befreit** gekennzeichnet         | Befreiungscode                                |
| Der Steuercode ist als **Ist Verlagerung der Steuerschuld** gekennzeichnet | Verlagerung der Steuerschuld                             |
| Der Steuercode ist als **Ist Verbrauchssteuer** gekennzeichnet        | Erwerbsteuer (USA)                                    |

## <a name="item-sales-tax-group"></a>Artikel-Mehrwertsteuergruppe

| Dienst für Steuerberechnungen             | Finance                                         |
| ----------------------------------- | ----------------------------------------------- |
| Element-Steuerkennzeichen                      | Artikel-Mehrwertsteuergruppe                            |
| Steuercodes unter dieser Artikelsteuergruppe | Mehrwertsteuercodes unter dieser Artikelmehrwertsteuergruppe |

Pflegen Sie nach Abschluss der Synchronisierung die verbleibenden Parameter für Buchungs- und Berichtszwecke weiterhin in Finance.

> [!NOTE]
> Synchronisierung den Steuereinstellungen von Fincance zu Tax Calculation Service wird nicht unterstützt. Erstellen Sie für eine vorhandene Finance-Umgebung zunächst die Steuereinstellungen im Tax Calculation Service. Synchronisieren Sie dann die Einstellungsdaten wieder mit der Finance-Umgebung.
