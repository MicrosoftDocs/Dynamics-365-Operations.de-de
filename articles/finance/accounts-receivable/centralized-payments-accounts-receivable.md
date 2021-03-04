---
title: Zentralisierte Zahlungen für Debitorenkonten
description: Organisationen mit mehreren juristischen Personen können zum Erstellen und Verwalten von Zahlungen eine juristische Person festlegen, die alle Zahlungen abwickelt. Daher muss die gleiche Buchung nicht in mehrere juristische Personen eingegeben werden. Dieser Artikel enthält Beispiele, die zeigen, wie das Buchen für zentralisierte Zahlungen in verschiedenen Szenarien behandelt wird.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78c72bb9632d3501638d528822a3c30b05686796
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443546"
---
# <a name="centralized-payments-for-accounts-receivable"></a>Zentralisierte Zahlungen für Debitorenkonten

[!include [banner](../includes/banner.md)]

Organisationen mit mehreren juristischen Personen können zum Erstellen und Verwalten von Zahlungen eine juristische Person festlegen, die alle Zahlungen abwickelt. Daher muss die gleiche Buchung nicht in mehrere juristische Personen eingegeben werden. Dieser Artikel enthält Beispiele, die zeigen, wie das Buchen für zentralisierte Zahlungen in verschiedenen Szenarien behandelt wird.

Organisationen mit mehreren juristischen Personen können zum Erstellen und Verwalten von Zahlungen eine juristische Person festlegen, die alle Zahlungen abwickelt. Daher muss die gleiche Buchung nicht in mehrere juristische Personen eingegeben werden. Darüber hinaus spart die Organisation Zeit, da die Prozesse für Zahlungsvorschläge, Bedarfsdeckung und die offene Bearbeitung und geschlossenen Buchungen für zentralisierte Zahlungen rationalisiert werden. 

In einer Organisation mit zentralisierten Zahlungen gibt es viele juristische Personen für betriebliche Vorgänge. Dabei werden die Informationen zu ausstehenden Rechnungen von den einzelnen juristischen Personen verwaltet. Die Zahlungen für alle tätigen juristischen Personen werden von einer einzigen juristischen Person (der so genannten juristischen Person für die Zahlung) entgegengenommen. Im Zuge des Ausgleichsprozesses werden die erforderlichen Buchungen vom Typ "Fällig bis" und "Fällig von" generiert. Sie können angeben, welche juristische Person in der Organisation die Buchungen für realisierte Gewinne oder Verluste erhalten soll und wie Skontobuchungen für zentralisierte Zahlungen zu behandeln sind. Auf der zentralisierten Zahlungserfassungsposition sollte die **Kontenart** auf Debitor festgelegt werden. Die **Gegenkontenart** sollte auf Bank oder Sachkonto festgelegt werden. Das Bankkonto solle auf das aktuelle Unternehmen lauten. 

In den folgenden Beispielen wird die Behandlung von Buchungen in unterschiedlichen Szenarios erläutert. Allen Beispielen liegt die folgende Konfiguration zugrunde:

-   Fabrikam, Fabrikam Ost und Fabrikam West stellen die juristischen Personen dar. Debitorenzahlungen werden in Fabrikam eingegeben.
-   Das **Skonto buchen** Feld auf der **Verrechnung** Seite ist auf **Juristische Person der Rechnung** festgelegt.
-   Das **Gewinn bzw. Verlust bei Währungsumtausch buchen** Feld auf der **Verrechnung** Seite ist auf **Juristische Person der Zahlung** festgelegt.
-   Debitor Northwind Traders ist als Debitor in jeder juristischen Person festgelegt. Die Debitoren aus verschiedenen juristischen Personen werden als derselbe Debitor erfasst, da sie dieselbe Kennung für das globale Adressbuch gemeinsam haben.

| Adressbuchkennung | Debitorenkonto | Name              | Juristische Person  |
|-----------------|------------------|-------------------|---------------|
| 4050            | 4000             | Northwind Traders | Fabrikam      |
| 4050            | 4000             | Northwind Traders | Fabrikam Ost |
| 4050            | 10.000            | Northwind Traders | Fabrikam West |

## <a name="example-1-customer-payment-of-invoice-from-another-legal-entity"></a>Beispiel 1: Debitorenzahlung der Rechnung einer anderen juristischen Person
Bei Fabrikam geht eine Zahlung in Höhe von EUR 600,00 für das Fabrikam-Debitorenkonto "4000" (Northwind Traders) ein. Die Zahlung wird mit einer offenen Rechnung für das Debitorenkonto "4000" bei Fabrikam Ost ausgeglichen.

### <a name="invoice-is-posted-in-fabrikam-east-for-customer-4000"></a>Buchung der Rechung in Fabrikam Ost für Debitor "4000"

| Konto                             | Sollbetrag | Habenbetrag |
|-------------------------------------|--------------|---------------|
| Debitoren (Fabrikam Ost) | 600,00       |               |
| Verkauf (Fabrikam Ost)               |              | 600,00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>Eingang und Buchung der Zahlung in Fabrikam für Debitor "4000"

| Konto                        | Sollbetrag | Habenbetrag |
|--------------------------------|--------------|---------------|
| Bar (Fabrikam)                | 600,00       |               |
| Debitoren (Fabrikam) |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Ausgleich der Fabrikam-Zahlung mit der Rechnung von Fabrikam Ost

**Buchung für Fabrikam**

| Konto                         | Sollbetrag | Habenbetrag |
|---------------------------------|--------------|---------------|
| Debitoren (Fabrikam)  | 600,00       |               |
| Fällig an Fabrikam Ost (Fabrikam) |              | 600,00        |

**Buchung für Fabrikam Ost**

| Konto                             | Sollbetrag | Habenbetrag |
|-------------------------------------|--------------|---------------|
| Fällig von Fabrikam (Fabrikam Ost)   | 600,00       |               |
| Debitoren (Fabrikam Ost) |              | 600,00        |

## <a name="example-2-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>Beispiel 2: Debitorenzahlung der Rechnung einer anderen juristischen Person mit Skonto
Bei Fabrikam geht eine Zahlung in Höhe von EUR 580,00 für den Fabrikam-Debitor "4000" (Northwind Traders) ein. Für Fabrikam Ost liegt eine offene Rechnung für den Kreditor "4000" vor. Für die Rechnung wird ein Skonto in Höhe von EUR 20,00 gewährt. Die Zahlung wird mit den offenen Rechnungen für Fabrikam Ost ausgeglichen. Der Skonto wird auf die juristische Person für die Rechnung (Fabrikam Ost) gebucht.

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>Buchung der Rechnung in Fabrikam Ost für Debitor "4000" von Fabrikam Ost

| Konto                             | Sollbetrag | Habenbetrag |
|-------------------------------------|--------------|---------------|
| Debitoren (Fabrikam Ost) | 580.00       |               |
| Verkauf (Fabrikam Ost)               |              | 580.00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>Eingang und Buchung der Zahlung in Fabrikam für Fabrikam-Debitor "4000"

| Konto                        | Sollbetrag | Habenbetrag |
|--------------------------------|--------------|---------------|
| Bar (Fabrikam)                | 600,00       |               |
| Debitoren (Fabrikam) |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Ausgleich der Fabrikam-Zahlung mit der Rechnung von Fabrikam Ost

**Buchung für Fabrikam**

| Konto                         | Sollbetrag | Habenbetrag |
|---------------------------------|--------------|---------------|
| Debitoren (Fabrikam)  | 580,00       |               |
| Fällig an Fabrikam Ost (Fabrikam) |              | 580,00        |

**Buchung für Fabrikam Ost**

| Konto                             | Sollbetrag | Habenbetrag |
|-------------------------------------|--------------|---------------|
| Fällig von Fabrikam (Fabrikam Ost)   | 580,00       |               |
| Debitoren (Fabrikam Ost) |              | 580,00        |
| Skonto (Fabrikam Ost)       | 20,00        |               |
| Debitoren (Fabrikam Ost) |              | 20,00         |

## <a name="example-3-customer-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-gain"></a>Beispiel 3: Debitorenzahlung der Rechnung eines anderen Unternehmens mit realisiertem Wechselkursgewinn
Bei Fabrikam geht eine Zahlung in Höhe von 600,00 Euro für den Fabrikam-Debitor "4000" (Northwind Traders) ein. Die Zahlung wird mit einer offenen Rechnung für den Debitor "4000" bei Fabrikam Ost ausgeglichen. Im Zuge des Ausgleichsprozesses wird eine Wechselkursgewinnbuchung generiert.

-   Wechselkurs von EUR in US-Dollar (USD) zum Rechnungsdatum: 1,2062
-   Wechselkurs für EUR in USD zum Zahlungsdatum: 1,2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>Buchung der Rechung in Fabrikam Ost für Debitor "4000" von Fabrikam Ost

| Konto                             | Sollbetrag            | Habenbetrag           |
|-------------------------------------|-------------------------|-------------------------|
| Debitoren (Fabrikam Ost) | EUR 600,00/USD 723,72 |                         |
| Verkauf (Fabrikam Ost)               |                         | EUR 600,00/USD 723,72 |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>Eingang und Buchung der Zahlung in Fabrikam für Fabrikam-Debitor "4000"

| Konto                        | Sollbetrag            | Habenbetrag           |
|--------------------------------|-------------------------|-------------------------|
| Bar (Fabrikam)                | EUR 600,00/USD 736,62 |                         |
| Debitoren (Fabrikam) |                         | EUR 600,00/USD 736,62 |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Ausgleich der Fabrikam-Zahlung mit der Rechnung von Fabrikam Ost

**Buchung für Fabrikam**

| Konto                         | Sollbetrag            | Habenbetrag           |
|---------------------------------|-------------------------|-------------------------|
| Debitoren (Fabrikam)  | EUR 600,00/USD 736,62 |                         |
| Fällig an Fabrikam Ost (Fabrikam) |                         | EUR 600,00/USD 736,62 |
| Fällig an Fabrikam Ost (Fabrikam) | EUR 0,00/USD 12,90    |                         |
| Realisierter Gewinn (Fabrikam)        |                         | EUR 0,00/USD 12,90    |

**Buchung für Fabrikam Ost**

| Konto                             | Sollbetrag            | Habenbetrag           |
|-------------------------------------|-------------------------|-------------------------|
| Fällig von Fabrikam (Fabrikam Ost)   | EUR 600,00/USD 736,62 |                         |
| Debitoren (Fabrikam Ost) |                         | EUR 600,00/USD 736,62 |
| Debitoren (Fabrikam Ost) | EUR 0,00/USD 12,90    |                         |
| Fällig von Fabrikam (Fabrikam Ost)   |                         | EUR 0,00/USD 12,90    |

## <a name="example-4-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-gain"></a>Beispiel 4: Debitorenzahlung der Rechnung einer anderen juristischen Person mit Skonto und realisiertem Wechselkursverlust
Von Fabrikam wird eine Zahlung für den Fabrikam-Debitor "4000" (Northwind Traders) für eine offene Rechnung bei Fabrikam Ost gebucht. Auf die Rechnung wird Skonto gewährt, und eine Mehrwertsteuerbuchung wird generiert. Die Zahlung wird mit der offenen Rechnung für Fabrikam Ost ausgeglichen. Im Zuge des Ausgleichsprozesses wird eine Wechselkursgewinnbuchung generiert. Der Skonto wird auf die juristische Person für die Rechnung (Fabrikam Ost), der Wechselkursgewinn auf die juristische Person für die Zahlung (Fabrikam) gebucht.

-   Wechselkurs von EUR in USD zum Rechnungsdatum: 1,2062
-   Wechselkurs für EUR in USD zum Zahlungsdatum: 1,2277

### <a name="free-text-invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-customer-4000"></a>Buchung einer Freitextrechnung und Generierung einer Steuerbuchung in Fabrikam Ost für Debitor "4000"

| Konto                             | Sollbetrag            | Habenbetrag           |
|-------------------------------------|-------------------------|-------------------------|
| Debitoren (Fabrikam Ost) | EUR 638,22/USD 769,82 |                         |
| Verkauf (Fabrikam Ost)               |                         | EUR 600,00/USD 723,72 |
| Mehrwertsteuer (Fabrikam Ost)           |                         | EUR 38,22/USD 46,10   |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>Eingang und Buchung der Zahlung in Fabrikam für Debitor "4000"

| Konto                        | Sollbetrag            | Habenbetrag           |
|--------------------------------|-------------------------|-------------------------|
| Bar (Fabrikam)                | EUR 626,22/USD 768,81 |                         |
| Debitoren (Fabrikam) |                         | EUR 626,22/USD 768,81 |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Ausgleich der Fabrikam-Zahlung mit der Rechnung von Fabrikam Ost

**Buchung für Fabrikam**

| Konto                         | Sollbetrag            | Habenbetrag           |
|---------------------------------|-------------------------|-------------------------|
| Debitoren (Fabrikam)  | EUR 626,22/USD 768,81 |                         |
| Fällig an Fabrikam Ost (Fabrikam) |                         | EUR 626,22/USD 768,81 |
| Fällig an Fabrikam Ost (Fabrikam) | EUR 0,00/USD 13,46    |                         |
| Realisierter Gewinn (Fabrikam)        |                         | EUR 0,00/USD 13,46    |

**Buchung für Fabrikam Ost**

| Konto                             | Sollbetrag            | Habenbetrag           |
|-------------------------------------|-------------------------|-------------------------|
| Fällig von Fabrikam (Fabrikam Ost)   | EUR 626,22/USD 768,81 |                         |
| Debitoren (Fabrikam Ost) |                         | EUR 626,22/USD 768,81 |
| Debitoren (Fabrikam Ost)  | EUR 0,00/USD 13,46    |                         |
| Fällig von Fabrikam (Fabrikam Ost)   |                         | EUR 0,00/USD 13,46    |
| Skonto (Fabrikam Ost)       | EUR 12,00/USD 14,47   |                         |
| Debitoren (Fabrikam Ost) |                         | EUR 12,00/USD 14,47   |

## <a name="example-5-customer-credit-note-with-primary-payment"></a>Beispiel 5: Debitorengutschrift mit primärer Zahlung
Bei Fabrikam geht eine Zahlung in Höhe von EUR 75,00 vom Debitor "4000" (Northwind Traders) ein. Die Zahlung wird mit einer offenen Rechnung für den Debitor "10.000" von Fabrikam West und einer offenen Gutschrift für den Debitor "4000" von Fabrikam Ost ausgeglichen. Die Zahlung wird im Formular zum Bearbeiten offener Posten als Seite **Transaktion begleich** dargestellt.

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>Buchung der Rechnung in Fabrikam West für Debitor "10.000"

| Konto                             | Sollbetrag | Habenbetrag |
|-------------------------------------|--------------|---------------|
| Debitoren (Fabrikam West) | 100,00       |               |
| Verkauf (Fabrikam West)               |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>Buchung der Gutschrift an Fabrikam West für Debitor "4000"

| Konto                             | Sollbetrag | Habenbetrag |
|-------------------------------------|--------------|---------------|
| Verkaufsrücklieferungen (Fabrikam Ost)       | 25,00        |               |
| Debitoren (Fabrikam Ost) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>Buchung der Zahlung an Fabrikam für Debitor "4000"

| Konto                        | Sollbetrag | Habenbetrag |
|--------------------------------|--------------|---------------|
| Bar (Fabrikam)                | 75,00        |               |
| Debitoren (Fabrikam) |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Ausgleich der Fabrikam-Zahlung mit Rechnung für Fabrikam West und Gutschrift für Fabrikam Ost

**Buchung für Fabrikam**

| Konto                           | Sollbetrag | Habenbetrag |
|-----------------------------------|--------------|---------------|
| Fällig von Fabrikam Ost (Fabrikam) | 25,00        |               |
| Debitoren (Fabrikam)    |              | 25,00         |
| Debitoren (Fabrikam)    | 100,00       |               |
| Fällig an Fabrikam West (Fabrikam)   |              | 100,00        |

**Buchung für Fabrikam Ost**

| Konto                             | Sollbetrag | Habenbetrag |
|-------------------------------------|--------------|---------------|
| Debitoren (Fabrikam Ost) | 25,00        |               |
| Fällig an Fabrikam (Fabrikam Ost)     |              | 25,00         |

**Buchung für Fabrikam West**

| Konto                             | Sollbetrag | Habenbetrag |
|-------------------------------------|--------------|---------------|
| Fällig von Fabrikam (Fabrikam West)   | 100,00       |               |
| Debitoren (Fabrikam West) |              | 100,00        |

## <a name="example-6-customer-credit-note-without-primary-payment"></a>Beispiel 6: Debitorengutschrift ohne primäre Zahlung
Bei Fabrikam geht eine Zahlung in Höhe von EUR 75,00 vom Debitor "4000" (Northwind Traders) ein. Die Zahlung wird mit einer offenen Rechnung für den Debitor "10.000" von Fabrikam West und einer offenen Gutschrift für den Debitor "4000" von Fabrikam Ost ausgeglichen. Die Zahlung ist im Formular zum Bearbeiten offener Posten als Seite **Transaktion begleich** nicht ausgewählt.

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>Buchung der Rechnung in Fabrikam West für Debitor "10.000"

| Konto                             | Sollbetrag | Habenbetrag |
|-------------------------------------|--------------|---------------|
| Debitoren (Fabrikam West) | 100,00       |               |
| Verkauf (Fabrikam West)               |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>Buchung der Gutschrift an Fabrikam West für Debitor "4000"

| Konto                             | Sollbetrag | Habenbetrag |
|-------------------------------------|--------------|---------------|
| Verkaufsrücklieferungen (Fabrikam Ost)       | 25,00        |               |
| Debitoren (Fabrikam Ost) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>Buchung der Zahlung an Fabrikam für Debitor "4000"

| Konto                        | Sollbetrag | Habenbetrag |
|--------------------------------|--------------|---------------|
| Bar (Fabrikam)                | 75,00        |               |
| Debitoren (Fabrikam) |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Ausgleich der Fabrikam-Zahlung mit Rechnung für Fabrikam West und Gutschrift für Fabrikam Ost

**Buchung für Fabrikam**

| Konto                         | Sollbetrag | Habenbetrag |
|---------------------------------|--------------|---------------|
| Debitoren (Fabrikam)  | 75,00        |               |
| Fällig an Fabrikam West (Fabrikam) |              | 75,00         |

**Buchung für Fabrikam Ost**

| Konto                              | Sollbetrag | Habenbetrag |
|--------------------------------------|--------------|---------------|
| Debitoren (Fabrikam Ost)  | 25,00        |               |
| Fällig an Fabrikam West (Fabrikam Ost) |              | 25,00         |

**Buchung für Fabrikam West**

| Konto                                | Sollbetrag | Habenbetrag |
|----------------------------------------|--------------|---------------|
| Fällig von Fabrikam (Fabrikam West)      | 75,00        |               |
| Debitoren (Fabrikam West)    |              | 75,00         |
| Fällig von Fabrikam Ost (Fabrikam West) | 25,00        |               |
| Debitoren (Fabrikam West)    |              | 25,00         |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]