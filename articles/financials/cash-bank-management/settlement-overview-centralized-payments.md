---
title: "Ausgleichsüberblick für zentralisierte Zahlungen"
description: "In diesem Thema wird der Ausgleich von zentralisierten Zahlungen für Microsoft Dynamics 365 for Finance and Operations beschrieben."
author: abruer
manager: AnnBe
ms.date: 08/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 222414
ms.assetid: 610f6858-0f37-4d0f-8c68-bab5a971ef4a
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: fc5a65c299adbf86fb2f38dff1a9aaa36f7367fa
ms.openlocfilehash: 1fecc9027d0df7b268a3241ea0f1797849db2d90
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---

# <a name="settlement-overview-for-centralized-payments"></a>Ausgleichsüberblick für zentralisierte Zahlungen

[!include [banner](../includes/banner.md)]

Organisationen mit mehreren juristischen Personen können zum Erstellen und Verwalten von Zahlungen eine juristische Person festlegen, die alle Zahlungen abwickelt. Dadurch wird vermieden, dass die gleiche Buchung für mehrere juristische Personen eingegeben werden muss. Dies hat eine Zeitersparnis zur Folge, da so der Zahlungsvorschlagsprozess, der Ausgleichsprozess, die Bearbeitung offener Posten sowie die Bearbeitung abgeschlossener Buchungen bei zentralisierten Zahlungen optimiert werden. 

Wird eine Debitoren- oder Kreditorenzahlung für eine juristische Person eingegeben und mit einer Rechnung ausgeglichen, die für eine andere juristische Person eingegeben wurde, werden die entsprechenden Buchungen vom Typ "Ausgleich", "Fällig bis" und "Fällig von" für jede juristische Person automatisch generiert. Für jede Rechnungs- und Zahlungskombination der Buchung wird ein Ausgleichsdatensatz erstellt. Jedem Ausgleichsdatensatz wird eine neue Belegnummer zugewiesen, die auf der Nummernkreisserie basiert, die auf der Seite **Debitoren-Parameter** für Kunden und auf der Seite **Kreditorenkontenparameter** für Kreditoren definiert wird. 

Zusätzlich generierten Datensätzen für Skonti, Neubewertungen der Fremdwährung, Centdifferenzen, Überzahlungen oder Unterzahlungen wird entweder das Datum der Zahlungs- oder das Datum der Rechnungsbuchung zugewiesen – je nachdem, welches Datum weniger weit zurückliegt. Erfolgt der Ausgleich, nachdem die Zahlung gebucht wurde, werden für die Ausgleichsdatensätze das Buchungsdatum des Ausgleichs verwendet, das im Formular **Offene Transaktionen abschließen** angegeben wurde.

## <a name="posting-types-transaction-types-and-default-descriptions"></a>Buchungsarten, Buchungstext und Standardbeschreibungen

Intercompany-Belegbuchungen nutzen den Intercompany-Buchungstyp, Intercompany-Debitoren-Ausgleichsbuchungen und Intercompany-Kreditoren-Ausgleichsbuchungstypen. Verwenden Sie zum Einrichten von Informationen zur Buchungsart die Seite **Standardbeschreibungen**. 

Die folgenden Buchungsarten stehen sowohl für Ausgleiche in einzelnen Unternehmen als auch für unternehmensübergreifende Ausgleiche zur Verfügung:

-   Ausgleich
-   Skonto
-   Neubewertungen der Fremdwährung (sowohl realisierte als auch nicht realisierte Neubewertungen)
-   Centdifferenz
-   Überzahlung/Unterzahlung

Sie können auch Standardbeschreibungen für Intercompany-Ausgleichsbelege definieren.

## <a name="currency-exchange-gains-or-losses"></a>Wechselkursgewinne oder -verluste

Der für Debitoren- oder Kreditorenbuchungen verwendete Wechselkurs ist in der Buchung gespeichert. Realisierte Wechselkursgewinne oder -verluste werden – abhängig von der Option, die für die juristische Person für die Rechnung oder die juristische Person für die Zahlung im Feld **Gewinn bzw. Verlust bei Währungsumtausch buchen** auf der Seite **Intercompany Buchhaltung** für die juristische Person der Zahlung ausgewählt wurde, gebucht. In den folgenden Beispielen werden die hier aufgeführten Währungen verwendet:
-   Buchhaltungswährung für die Zahlung: EUR
-   Buchhaltungswährung für die Rechnung: USD
-   Währung der Zahlungsbuchung: DKK
-   Währung der Rechnungsbuchung: CAD

### <a name="currency-calculations"></a>Währungsberechnung

Wird eine Rechnung, die für eine juristischen Person eingegeben wurde, mit einer Zahlung ausgeglichen, die für eine andere juristischen Person eingegeben wurde, wird die Buchungswährung der Zahlung (DKK) in drei Schritten umgerechnet:
1.  Umrechnung in die Buchhaltungswährung der Zahlung (EUR) unter Verwendung der Wechselkurse der juristischen Person für die Zahlung.
2.  Umrechnung in die Buchhaltungswährung der Rechnung (USD).
3.  Umrechnung in die Buchungswährung der Rechnung (CAD) unter Verwendung der Wechselkurse der juristischen Person für die Rechnung.

Für die Umrechnung werden die Wechselkurse zum Zahlungsdatum verwendet. Entspricht der sich ergebende Zahlungsbetrag in der Buchungswährung der Rechnung (CAD) dem Rechnungsbetrag (CAD), gilt die Rechnung als vollständig bezahlt. 

Wird das Formular **Offene Transaktion begleichen** von einer Zahlungserfassung aus geöffnet, in der kein Zahlungsbetrag eingegeben wurde, wird der auszugleichende Betrag auf Basis der Rechnungen berechnet, die im Formular **Offen Transaktion begleichen** ausgewählt sind. Der auszugleichende Betrag wird in drei Schritten umgerechnet:
1.  Umrechnung in die Buchhaltungswährung der Rechnung (USD) unter Verwendung der Wechselkurse der juristischen Person für die Rechnung zum Zahlungsdatum.
2.  Umrechnung in die Buchhaltungswährung der Zahlung (EUR) unter Verwendung der Wechselkurse der juristischen Person für die Rechnung zum Zahlungsdatum.
3.  Umrechnung in die Buchungswährung der Zahlung (DKK).

Der sich ergebende Zahlungsbetrag wird durch Schließen des Formulars **Offene Transaktion begleichen** in die Position der Zahlungserfassung übertragen.

### <a name="posting-for-gain-or-loss-because-of-different-accounting-currencies"></a>Buchungen für Gewinne/Verluste aufgrund unterschiedlicher Buchhaltungswährungen

Liegt ein Wechselkursgewinn oder - verlust vor, wird der Gewinn/Verlust auf die juristische Person gebucht, die für das Feld **Gewinn bzw. Verlust bei Währungsumtausch buchen** auf der Seite **Intercompany Buchhaltung** für die juristische Person der Zahlung angegeben wird. Der Gewinn-/Verlustbetrag wird in die Buchhaltungswährung der juristischen Person umgerechnet, für die er gebucht wird. Verwendet wird hierzu der für diese juristische Person definierte Wechselkurs.

## <a name="cash-discounts"></a>Skonti

Skonti, die im Zuge des unternehmensübergreifenden Ausgleichs generiert wurden, werden – abhängig davon, welche Option für die juristische Person für die Zahlung im Formular **Skonto buchen** auf der Seite **Intercompany Buchhaltung** für die juristische Person der Zahlung ausgewählt wurde, gebucht. Unter der juristischen Person für die Rechnung wird eine entsprechende Ausgleichsbuchung generiert.

## <a name="overpayments-and-underpayments"></a>Überzahlungen und Unterzahlungen

Toleranzen für Über-/Unterzahlung oder für Centdifferenzen werden auf Basis der juristischen Person für die Zahlung (bei Überzahlungen) sowie auf Basis der juristischen Person für die Rechnung (bei Unterzahlungen) ermittelt. Das Buchungskonto, das verwendet wird, hängt von der Einstellung im Feld **Skontoverwaltung** auf der Seite **Debitorenparameter** für Debitoren und dem Feld **Skontoverwaltung** für **Kreditorenparameter** für Kreditoren ab.

-   Ist die Einstellung für die Skontoverwaltung auf "Spezifisch" festgelegt, oder ist die Einstellung auf "Nicht spezifisch" festgelegt, und der entsprechende Skontobetrag wird auf eine andere juristische Person aus der Überzahlung gebucht, wird das automatisch ausgewählte Konto für Debitorenskonto, Lieferantenskonto oder Centdifferenz in Buchhaltungswährung verwendet. Sie können diese Konten auf der Seite **Konten für automatische Buchungen** definieren.
-   Ist die Einstellung für die Skontoverwaltung auf "Nicht spezifisch" festgelegt, und die Buchung des Skontobetrags erfolgt auf die gleiche juristische Person wie die Buchung der Überzahlung (die juristischen Personen für Zahlung und Rechnung sind also identisch), wird das Skontokonto angepasst. Beispiel: Wird eine Rechnung in Höhe von 100,00 EUR mit einem Skonto von 3,00 EUR mit einer Zahlung von 98,00 EUR ausgeglichen, erfolgt eine Regulierung des Skontokontos um 1,00 EUR. Der Nettoskonto beträgt 2,00 EUR.
-   Ist die Einstellung für die Skontoverwaltung auf "Nicht spezifisch" festgelegt, wird der Skonto auf die gleiche juristische Person gebucht wie die Überzahlung, und die Über- oder Unterzahlung wird mit mehreren Rechnungen mit Skonto ausgeglichen, erfolgt eine Regulierung des Skontokontos für die letzte Rechnung.

Wenn die Skontoverwaltung "Nicht spezifisch" ist, gelten die Zahlungsausgleichsregeln nur in den folgenden Situationen:
-   Eine Überzahlung liegt vor.
-   Die Überzahlung wird mit mindestens einer Rechnung mit Skonto ausgeglichen.
-   Der Skonto wird auf die gleiche juristische Person gebucht wie die Überzahlung.

In allen anderen Situationen erfolgt die Buchung von Über- oder Unterzahlungen auf das automatisch ausgewählte Konto für Debitorenskonto, Kreditorenskonto oder Centdifferenz in der Buchhaltungswährung.

## <a name="sales-tax"></a>Mehrwertsteuer
Mehrwertsteuerbuchungen verbleiben bei der juristische Person, auf die diese ursprünglich gebucht wurden. 

Ist für eine Vorauszahlung eine Mehrwertsteuerbuchung erfolgt, wird die Mehrwertsteuer der Vorauszahlung bei der juristischen Person für die Vorauszahlung durch den unternehmensübergreifenden Ausgleich storniert. Die Steuern der juristischen Person für die Rechnung verbleiben bei dieser juristischen Person.

## <a name="financial-dimensions"></a>Finanzdimensionen
Bei Debitorenzahlungen werden für die Buchungen vom Typ "Fällig bis" und "Fällig von" unter der juristischen Person für die Zahlung die Finanzdimensionen verwendet, die für das Debitorensammelkonto aus der auszugleichenden Zahlung angegeben sind. Unter der juristischen Person für die Rechnung werden für die Buchungen vom Typ "Fällig bis" und "Fällig von" die Finanzdimensionen verwendet, die für das Debitorensammelkonto aus der auszugleichenden Rechnung angegeben sind. 

Bei Kreditorenzahlungen werden für die Buchungen vom Typ "Fällig bis" und "Fällig von" unter der juristischen Person für die Zahlung die Finanzdimensionen verwendet, die für das Kreditorensammelkonto aus der auszugleichenden Zahlung angegeben sind. Unter der juristischen Person für die Rechnung werden für die Buchungen vom Typ "Fällig bis" und "Fällig von" die Finanzdimensionen verwendet, die für das Kreditorensammelkonto aus der auszugleichenden Rechnung angegeben sind.

## <a name="withholding-tax"></a>Quellensteuer
Anhand des Kreditorenkontos, das der Rechnung zugeordnet ist, wird bestimmt, ob Quellensteuer berechnet werden soll. Wenn Quellensteuer anfällt, wird sie für die juristische Person berechnet, die der Rechnung zugeordnet ist. Wenn die juristischen Personen unterschiedliche Währungen verwenden, wird der Wechselkurs der juristischen verwendet, die der Rechnung zugeordnet ist.

