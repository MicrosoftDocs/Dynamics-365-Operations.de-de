---
title: Doppelte Währungsunterstützung für Steuern
description: In diesem Thema wird erklärt, wie die Doppelwährungs-Buchhaltungsfunktion im Steuerbereich erweitert werden kann und welche Auswirkungen dies auf die Steuerberechnung und -buchung hat.
author: EricWang
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 449ebe55b8be7ee7ea22b4be7c44162d83fc3c2affbd4d20f4cad235ddb0f772
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742203"
---
# <a name="dual-currency-support-for-sales-tax"></a>Unterstützung der Umsatzsteuer in zwei Währungen
[!include [banner](../includes/banner.md)]

In diesem Thema wird erklärt, wie die doppelte Währungsabrechnung für die Umsatzsteuer erweitert werden kann und welche Auswirkungen dies auf die Umsatzsteuerberechnung, -buchung und -abrechnung hat.

Die Doppelwährungsfunktion für Dynamics 365 Finance wurde in Version 8.1 (Oktober 2018) eingeführt. Sie ändert die Art und Weise, wie Buchungen in der Berichtswährung berechnet werden.

In früheren Versionen wurden die Transaktionen in der folgenden Reihenfolge in die Berichtswährung umgerechnet: 

- Die Transaktionssumme wurde in der Transaktionswährung berechnet > Der Transaktionsbetrag wurde in die Buchhaltungswährung umgerechnet > Der Betrag in der Buchhaltungswährung wurde in die Berichtswährung umgerechnet

Nachdem die Doppelwährungsfunktion aktiviert wurde, wurden die Transaktionen in der folgenden Reihenfolge in die Berichtswährung umgerechnet:

- Betrag der Transaktionswährung > Betrag der Berichtswährung

Weitere Informationen über Doppelwährung finden Sie unter [Duale Währung](dual-currency.md).

Als Folge der Unterstützung von Doppelwährungen sind zwei neue Funktionen in der Funktionsverwaltung verfügbar: 

- Umsatzsteuerumrechnung (neu in Version 10.0.13)
- Geben Sie die Finanzdimensionen in die realisierten Währungsbereinigungs-Gewinn- und Verlustrechnungen für die Umsatzsteuerabrechnung ein (neu in Version 10.0.17)

Die Doppelwährungsunterstützung für die Umsatzsteuer stellt sicher, dass die Steuern genau in der Steuerwährung berechnet werden und dass der Umsatzsteuerabrechnungssaldo sowohl in der Buchhaltungs- als auch in der Berichtswährung genau berechnet wird.

## <a name="sales-tax-conversion"></a>Mehrwertsteuerkonvertierung

Der Parameter **Umsatzsteuerumrechnung** bietet zwei Optionen zur Umrechnung des Steuerbetrags von der Transaktionswährung in die Steuerwährung. 

- Buchführungswährung: Der Pfad lautet „Betrag in Transaktionswährung > Betrag in Buchhaltungswährung > Betrag in Steuerwährung“. Für die Währungsumrechnung wird der Wechselkurs-Typ der Buchhaltungswährung (konfiguriert in der Einrichtung des Ledgers) verwendet.
- Berichtswährung: Der Pfad lautet „Betrag in Transaktionswährung > Betrag in Berichtswährung > Betrag in Steuerwährung“. Der (im Ledger-Setup konfigurierte) Berichtswährungswechselkurstyp wird für die Währungsumrechnung verwendet.

### <a name="example"></a>Beispiel

Ein einfaches Beispiel zur Veranschaulichung dieser Funktionalität ist:

Währungseinrichtung für Sachkonto und Steuer

| Buchungswährung | Buchhaltungswährung | Berichtswährung | Steuerwährung |
| -------------------- | ------------------- | ------------------ | ------------ |
| EUR                  | EUR                 | GBP                | GBP          |

Kurs

| Ausgangswährung | Zielwährung | Faktor | Kurs |
| ------------- | ----------- | ------ | ------------- |
| EUR           | EUR         | 1      | 1.11          |
| EUR           | GBP         | 1      | 0.83          |
| EUR           | GBP         | 1      | 0.75          |

Berechnung des Steuerbetrags in verschiedenen Parameteroptionen

Steuerbetrag = 100 EUR

| Parameter für die Umsatzsteuerumwandlung | Transaktionswährung (EUR) | Rechnungswährung (USD) | Berichtswährung (GBP) | Steuerwährung (GBP) |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| Buchhaltungswährung             | 100                        | 111                       | 83                       | **83.25**          |
| Berichtswährung              | 100                        | 111                       | 83                       | **83**             |

Dieser Parameter kann auf der Grundlage des Compliance-Bedarfs der Steuerbehörde konfiguriert werden.


### <a name="upgrade-consideration"></a>Upgrade-Überlegung.

Diese Funktion gilt nur für neue Transaktionen. Für Steuertransaktionen, die bereits in der Tabelle TAXTRANS gespeichert, aber noch nicht abgerechnet wurden, berechnet das System den Steuerbetrag in Steuerwährung nicht neu, da der Wechselkurs zum Zeitpunkt der Steuerbuchung bereits fehlt.

Um das vorhergehende Szenario zu verhindern, empfehlen wir, diesen Parameterwert in einer neuen (sauberen) Steuerabrechnungsperiode zu ändern, die keine nicht abgerechneten Steuertransaktionen enthält. Um diesen Wert in der Mitte einer Steuerabrechnungsperiode zu ändern, führen Sie bitte das Programm „Umsatzsteuer abrechnen und buchen“ für die aktuelle Steuerabrechnungsperiode aus, bevor Sie diesen Parameterwert ändern.

Diese Funktion fügt Buchhaltungseinträge hinzu, die Gewinne und Verluste aus Geldwechseln verdeutlichen. Die Buchungen werden in der realisierten Gewinn- und Verlustrechnung der Währungsanpassung vorgenommen, wenn die Neubewertung während der Umsatzsteuerabrechnung erfolgt. Weitere Informationen finden Sie im Abschnitt [Automatische Bilanzierung der Steuerabrechnung in Berichtswährung](#tax-settlement-auto-balance-in-reporting-currency) später in diesem Thema.

> [!NOTE]
> Während der Abrechnung werden Informationen für Finanzdimensionen aus Umsatzsteuerkonten, die Bilanzkonten sind, entnommen und in Gewinn- und Verlustrechnungen zur Währungsanpassung, die Gewinn- und Verlustrechnungen sind, erfasst. Da sich die Wertbeschränkungen der Finanzdimensionen zwischen Bilanzkonten und Gewinn- und Verlustrechnungskonten unterscheiden, kann während des Abrechnungs- und Nachsteuerprozesses ein Fehler auftreten. Um zu vermeiden, dass Kontostrukturen geändert werden müssen, können Sie die Funktion Finanzielle Dimensionen mit den realisierten Währungsanpassungs-Gewinn-/Verlustkonten für die Umsatzsteuerabrechnung füllen aktivieren. Diese Funktion erzwingt die Ableitung von Finanzdimensionen zu Währungsanpassungs-Gewinn-/Verlustrechnungen. 

## <a name="track-reporting-currency-tax-amount"></a>Steuerbetrag in Berichtswährung verfolgen

Drei neue Felder wurden zu den steuerbezogenen Tabellen hinzugefügt, um Beträge in der Berichtswährung zu verfolgen. Diese Felder befinden sich innerhalb der Tabellen TAXUNCOMMITTED und TAXTRANS:

- TaxAmountRep: Steuerbetrag in der Berichtswährung
- TaxBaseAmountRep: Basisbetrag in Berichtswährung
- TaxInCostPriceRep: nicht abzugsfähiger Betrag in Berichtswährung

Für Steuern, die nur in der Tabelle TAXUNCOMMITTED gespeichert, aber noch nicht gebucht wurden, berechnet das System den Steuerbetrag in der Berichtswährung zum Zeitpunkt der Buchung neu und speichert ihn in der Tabelle TAXTRANS.

Diese Version enthält keine Änderungen an Berichten und Formularen, die den Steuerbetrag in der Berichtswährung anzeigen. Änderungen an Berichten und Formularen werden in der zukünftigen Version geliefert.



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a>Automatische Steuerabrechnung in der Berichtswährung

Wenn die Steuerabrechnung aus bestimmten Gründen nicht in der Berichtswährung ausgeglichen wird, z.B. wenn der Umsatzsteuerumrechnungspfad „Buchhaltungswährung“ ist oder die Wechselkursänderung in einer einzelnen Steuerabrechnungsperiode erfolgt, erzeugt das System automatisch Buchhaltungsbuchungen, um die Steuerbetragsabweichung zu korrigieren und mit dem Konto für realisierten Kursgewinn/-verlust, das im Ledger-Setup konfiguriert ist, zu verrechnen.

Anhand des vorhergehenden Beispiels zur Veranschaulichung dieser Funktion wird angenommen, dass die Daten in der Tabelle TAXTRANS zum Zeitpunkt der Buchung wie folgt aussehen.

| Parameter für die Umsatzsteuerumwandlung | Transaktionswährung (EUR) | Rechnungswährung (USD) | Berichtswährung (GBP) | Steuerwährung (GBP) |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| Buchhaltungswährung             | 100                        | 111                       | 83                       | **83.25**          |
| Berichtswährung              | 100                        | 111                       | 83                       | **83**             |

Wenn Sie das Umsatzsteuerabrechnungsprogramm am Monatsende ausführen, wird die Buchhaltung wie folgt gebucht.
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a>Szenario: Umsatzsteuerumrechnung = „Buchhaltungswährung“.

| Hauptkonto           | Transaktionswährung (GBP) | Rechnungswährung (USD) | Berichtswährung (GBP) |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| Zu zahlende/erhaltende Steuer | -83,25                     | -111                      | -83,25                   |
| Steuerabrechnung         | 83.25                      | 111                       | 83.25                    |
| Realisierter Gewinn/Verlust     | 0                          | 0                         | -0,25                    |
| Zu zahlende/erhaltende Steuer | 0                          | 0                         | 0.25                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a>Szenario: Umsatzsteuerumrechnung = „Berichtswährung“.


| Hauptkonto           | Transaktionswährung (GBP) | Rechnungswährung (USD) | Berichtswährung (GBP) |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| Zu zahlende/erhaltende Steuer | -83                        | -110,67                   | -83                      |
| Steuerabrechnung         | 83                         | 110.67                    | 83                       |
| Realisierter Gewinn/Verlust     | 0                          | 0.33                      | 0                        |
| Zu zahlende/erhaltende Steuer | 0                          | -0,33                     | 0                        |



Weitere Informationen finden Sie in folgenden Themen:

- [Doppelte Währung](dual-currency.md)
- [Mehrwertsteuerübersicht](indirect-taxes-overview.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
