---
title: Übersicht über die Quellenbesteuerung in Indien (TDS)
description: Dieser Artikel enthält detaillierte Informationen zur indischen Quellenbesteuerung (TDS). Die TDS-Dokumentation behandelt die Funktionalität dieser Funktion.
author: kailiang
ms.date: 03/19/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "15721"
- intro-internal
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7ddcf11013921b5d5e242c9026d332d319ed8169
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896282"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a>Übersicht über die Quellenbesteuerung in Indien (TDS)

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält detaillierte Informationen zur indischen Quellenbesteuerung (TDS).

Die TDS-Dokumentation behandelt die Funktionalität dieser Funktion. Außerdem wird erläutert, wie Sie die Grundeinstellungen für TDS festlegen, TDS für Buchungen berechnen, den TDS-Ausgleichsprozess durchführen, TDS-Zertifikatsnummern aufzeichnen und TDS-Anfragen, TDS-Erklärungen und TDS-Zertifikate generieren. Die Dokumentation enthält die folgenden Themen:

- [Grundeinstellungen für TDS](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [Formeldesigner und Schwellenwertfunktionalität für die TDS-Berechnung](apac-ind-TDS-Formula-designer.md)
- [TDS-Berechnung für Rechnungen, Zahlungen, Solawechsel und Intercompany-Buchungen](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [Der periodische TDS-Ausgleichsprozess und der Ausgleich von TDS-Beträgen gegenüber Behördenkreditoren](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [TDS-Zertifikatsnummern und -daten aufzeichnen und aktualisieren](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a>Einführung in TDS

Gemäß dem Einkommensteuergesetz von 1961 wird die Einkommensteuer vom Empfänger der Dienstleistung zum Zeitpunkt der Vorauszahlung oder der Verbuchung der Gutschrift an der Quelle abgezogen, je nachdem, was zuerst eintritt. Wer die Zahlung leistet, muss den Steuerbetrag abziehen und nur den Nettosaldo an den Dienstleister zahlen. TDS wird auf staatlich festgelegte Dienstleistungen angewendet, und die Steuer wird unter Verwendung der vom Staat für einen bestimmten Zeitraum festgelegten Sätze abgezogen. Der Abzugssatz basiert auf dem Status der Entität, die die Zahlung erhält oder die Dienstleistung erbringt. Mögliche Status sind unter anderem **Einzelperson**, **Ungeteilte Hindufamilie** (**HUF**), **Unternehmen**, **Firma**, **Personenverband** (**AOP**), **Personenzusammenschluss** (**BOI**) und **Gemeinde**.

In den folgenden Abschnitten werden die Dienste aufgeführt, auf die TDS, wie vom indischen Staat festgelegt, angewendet wird.

**Einwohner**

- Einkommen aus Gehältern (gemäß § 192)
- Zinserträge aus Wertpapieren (gemäß § 193)
- Dividendenerträge (gemäß § 194)
- Zinserträge (gemäß § 194A)
- Einkünfte aus Lotterien oder Gewinnspielen (gemäß § 194B)
- Gewinne von Pferderennen usw. (gemäß § 194BB)
- Auftragnehmer und Unterauftragnehmer (gemäß § 194C)
- Versicherungsprovisionen (gemäß § 194D)
- Einkünfte aus Einlagen in den nationalen Sparplan (gemäß § 194EE)
- Erträge aus Investmentfonds oder UTI (gemäß § 194F)
- Provisionen, Honorare, Preise usw. aus einem Verkauf oder einer Lotterie (gemäß § 194G)
- Zahlung von Provisionen oder Maklergebühren (gemäß § 194H)
- Miete (gemäß § 194I)
- Fachliche Dienstleistungen (gemäß § 194J)
- Einkommen aus Anteilen (gemäß § 194K)
- Zahlung einer Entschädigung beim Erwerb bestimmter Immobilien (gemäß § 194LA)

**Nicht ansässige Personen**

- Zahlungen an nicht ansässige Sportler oder Sportverbände (gemäß § 194E)
- Andere Beträge (unter § 195)
- Einkommen in Bezug auf Anteilen von nicht ansässigen Personen (gemäß § 196A)

    - Erträge aus Anleihen oder Aktien eines indischen Unternehmens in einer Fremdwährung (gemäß § 196C)
    - Erträge ausländischer institutioneller Anleger aus Wertpapieren (gemäß § 196D)
    - Gehälter und alle anderen positiven Einkommen unter einer Einkommensüberschrift (§ 192)
    - Zinsen auf Wertpapiere (§ 193)
    - Andere Zinsen als Zinsen auf Wertpapiere (§ 194A)
    - Zahlungen an Auftragnehmer und Unterauftragnehmer (§ 194C)
    - Gewinne aus Lotterien oder Kreuzworträtseln (§ 194B)
    - Gewinne aus Pferderennen (§ 194BB)
    - Versicherungsprovisionen für alle Zahlungen für den Erwerb eines Versicherungsabschlusses (§ 194D)
    - Alle anderen Zinsen als Zinsen auf Wertpapiere, die an nicht ansässige Personen, die kein Unternehmen sind, oder ausländische Unternehmen zu zahlen sind (§ 195)
    - Zahlung an einen nicht ansässigen Sportler, einschließlich Sportler, Sportverbände oder -einrichtungen. Im Falle eines nicht ansässigen Sportlers sind Zahlungen in Bezug auf Werbung sowie Artikel zu Spielen/Sportarten in Indien in Zeitungen, Zeitschriften usw. enthalten (§ 194E).
    - Zahlung für Einlagen im Rahmen des NSS \[nationaler Sparplan\] (§ 194EE)
    - Zahlungen aufgrund des Rückkaufs von Anteilen durch Investmentfonds oder UTI (§ 194F)
    - Zahlungen für Provisionen oder Maklergebühren (§ 194H)
    - Mietzahlungen (§ 194I)
    - Zahlung von Gebühren für fachliche oder technische Dienstleistungen (§ 194J)
    - Provision an Fachhändler, Händler, Käufer und Verkäufer von Lottoscheinen einschließlich Vergütungen oder Preise für solche Scheine (§ 194G)
    - Erträge aus in Fremdwährung gekauften Anteilen oder langfristige Kapitalgewinn aus der Übertragung solcher in Fremdwährung erworbenen Anteile (§ 196B)
    - Zahlung von Erträgen an nicht ansässige Personen in Bezug auf Zinsen oder Dividenden auf Anleihen und Aktien (§ 196C)

Die TDS wird für Käufe, Verkäufe, Rücksendungen, Gutschriften, Anschaffungen von Anlagen, Vorauszahlungen, Anzahlungen, Solawechsel, Einkommen und Intercompany-Buchungen berechnet.

> [!NOTE]
> Im indischen Steuerszenario wird TDS derzeit für Verkaufstransaktionen nicht berechnet. Das System enthält jedoch eine Bestimmung zur Berechnung der TDS, die bei Verkaufstransaktionen, insbesondere bei Intercompany-Buchungen, erstattungsfähig ist.

Bei der Berechnung der TDS werden immer der Schwellenwert und der Ausnahmeschwellenwert berücksichtigt, die für die TDS-Komponente festgelegt sind.

Der periodische TDS-Ausgleichsprozess muss ausgeführt werden, und die TDS-Zahlungen müssen gegenüber TDS-Behördenkreditoren ausgeglichen werden.

Die Zertifikatsnummern und -daten für TDS-Zertifikate, die von Kreditoren oder Debitoren empfangen werden, können aufgezeichnet und aktualisiert werden. Darüber hinaus können in Finance die Formulare 26Q und 27Q für die vierteljährlichen Erklärungen sowie das Zertifikat Formular 16A erstellt werden.

## <a name="setting-up-and-working-with-tds"></a>TDS einrichten und damit arbeiten

Hier finden Sie eine Übersicht, wie Sie TDS einrichten und damit arbeiten:

1. **TDS-Setup:**

    - Parametereinstellungen:

        - Aktivieren Sie unter Hauptbuchparameter Parameter, die mit TDS zusammenhängen.
        - Richten Sie unter Hauptbuchparameter die Nummernkreise für Quellensteuerzahlungen ein.
        - Richten Sie Parameter für Kreditoren und Debitoren ein.

    - Grundeinstellungen:

        - Richten Sie TDS-Registrierungsnummern für Unternehmen, Debitoren und Kreditoren ein.
        - Richten Sie TDS-Komponentengruppen ein.
        - Richten Sie TDS-Komponenten ein, verknüpfen Sie TDS-Komponentengruppen damit und definieren Sie den Schwellenwert sowie den Ausnahmeschwellenwert dafür.
        - Richten Sie TDS-Behörden ein.
        - Richten Sie TDS-Ausgleichsperioden ein.
        - Richten Sie TDS-Steuercodes ein und fügen Sie ihnen TDS-Komponenten hinzu.
        - Richten Sie TDS-Steuergruppen ein und fügen Sie ihnen TDS-Steuercodes hinzu.
        - Legen Sie im Formeldesigner eine Formel zur Berechnung der TDS für eine TDS-Gruppe fest.
        - Erfassen Sie die Nummern der TDS-Konzessionszertifikate.

    - Sachkonten und Unternehmen einrichten:

        - Richten sie Sachkonten für Debitoren und Kreditoren ein.
        - Legen Sie eine Steuerabzugs- und Inkassokontonummer (TAN) und eine Kategorie des Abzugstyps für das Unternehmen fest.

    - Andere Einstellungen:

        - Legen Sie einen Zahlungsplan fest, der die TDS-Zuteilung enthält.
        - Legen Sie einen Zahlungsgebührentyp für Zahlungen an die TDS-Behörden fest.
        - Legen Sie Angaben zu TDS-Gruppen, Permanente Kontonummern (PANs) und TANs für Kreditoren und Debitoren fest.

2. **Berechnung der TDS in Transaktionen:**

    - Rechnungen und Zahlungen
    - Solawechsel
    - Anzahlungen
    - Vorauszahlungen

3. **TDS-Ausgleich:**

    - Periodischer TDS-Ausgleichsprozess
    - Ausgleich von TDS-Zahlungen an TDS-Behördenkreditoren und Generierung von TDS-Challan

4. **TDS-Anfragen, -abrechnungen und -zertifikate:**

    - Zeichen Sie TDS-Zertifikatsnummern und -daten auf und aktualisieren Sie sie.
    - Generieren Sie eine TDS-Anfrage und eine gebuchte TDS-Anfrage.
    - Generieren Sie die Formulare 27A, 26Q und 27Q für die vierteljährliche TDS- und E-TDS-Erklärung.
    - Generieren Sie ein TDS-Zertifikat des Formulars 16A.
