---
title: Zentralisierte Zahlungen für Kreditorenkonten
description: Organisationen mit mehreren juristischen Personen können zum Erstellen und Verwalten von Zahlungen eine juristische Person festlegen, die alle Zahlungen abwickelt. Daher müssen die gleichen Zahlungen nicht in mehrere juristische Personen eingegeben werden. Dieser Artikel enthält Beispiele, die zeigen, wie das Buchen für zentralisierte Zahlungen in verschiedenen Szenarien behandelt wird.
author: abruer
manager: AnnBe
ms.date: 02/12/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14341
ms.assetid: 7bd02e32-2416-4ac6-8a60-85525267fdb7
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a4632056d6873cfeb748251c77becc410f5cf54
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837419"
---
# <a name="centralized-payments-for-accounts-payable"></a>Zentralisierte Zahlungen für Kreditorenkonten

[!include [banner](../includes/banner.md)]

Organisationen mit mehreren juristischen Personen können zum Erstellen und Verwalten von Zahlungen eine juristische Person festlegen, die alle Zahlungen abwickelt. Daher müssen die gleichen Zahlungen nicht in mehrere juristische Personen eingegeben werden. Dieser Artikel enthält Beispiele, die zeigen, wie das Buchen für zentralisierte Zahlungen in verschiedenen Szenarien behandelt wird.

Organisationen mit mehreren juristischen Personen können zum Erstellen und Verwalten von Zahlungen eine juristische Person festlegen, die alle Zahlungen abwickelt. Daher müssen die gleichen Zahlungen nicht in mehrere juristische Personen eingegeben werden. Darüber hinaus spart die Organisation Zeit, da der Zahlungsvorgang rationalisiert wird.

In einer Organisation mit zentralisierten Zahlungen gibt es viele juristische Personen für betriebliche Vorgänge. Dabei werden die Informationen zu Kreditorenrechnungen von den einzelnen juristischen Personen verwaltet. Die Zahlungen für alle tätigen juristischen Personen werden von einer einzigen juristischen Person (der so genannten juristischen Person für die Zahlung) generiert. Im Zuge des Ausgleichsprozesses werden die erforderlichen Buchungen vom Typ "Fällig bis" und "Fällig von" generiert. Sie können angeben, welche juristische Person in der Organisation die Buchungen für realisierte Gewinne oder Verluste erhält und wie Skontobuchungen für unternehmensübergreifende Zahlungen zu behandeln sind. Auf der zentralisierten Zahlungserfassungsposition sollte **Kontenart** auf Kreditor festgelegt werden. Die **Gegenkontenart** sollte auf Bank oder Sachkonto festgelegt werden. Das Bankkonto solle auf das aktuelle Unternehmen lauten. 

In den folgenden Beispielen wird die Behandlung von Buchungen in unterschiedlichen Szenarios erläutert. Allen Beispielen liegt die folgende Konfiguration zugrunde:

-   Fabrikam, Fabrikam Ost und Fabrikam West stellen die juristischen Personen dar. Zahlungen werden von Fabrikam geleistet.
-   Das **Skonto buchen** Feld auf der **Verrechnung** Seite ist auf **Juristische Person der Rechnung** festgelegt.
-   Das **Gewinn bzw. Verlust bei Währungsumtausch buchen** Feld auf der **Verrechnung** Seite ist auf **Juristische Person der Zahlung** festgelegt.
-   Der Kreditor Fourth Coffee ist als Kreditor in jeder juristischen Person festgelegt. Die Kreditoren aus verschiedenen juristischen Personen werden als derselbe Kreditor erfasst, da sie dieselbe Kennung für das globale Adressbuch gemeinsam haben.

| Verzeichniskennung | Kreditorenkonto | Name          | Juristische Person  |
|--------------|----------------|---------------|---------------|
| 1050         | 3004           | Fourth Coffee | Fabrikam      |
| 1050         | 100            | Fourth Coffee | Fabrikam Ost |
| 1050         | 3004           | Fourth Coffee | Fabrikam West |

## <a name="example-1-vendor-payment-of-invoice-from-another-legal-entity"></a>Beispiel 1: Kreditorenzahlung der Rechnung einer anderen juristischen Person
Für Fabrikam Ost liegt eine offene Rechnung für das Kreditorenkonto "100" (Fourth Coffee) vor. Bei Fabrikam wird eine Zahlung an das Fabrikam-Kreditorenkonto "3004" (Fourth Coffee) eingegeben und gebucht. Die Zahlung wird mit der offenen Rechnung ausgeglichen.

### <a name="invoice-is-posted-in-fabrikam-east-for-vendor-100"></a>Buchung der Rechung in Fabrikam Ost für Kreditor "100"

| Konto                          | Sollbetrag | Habenbetrag |
|----------------------------------|--------------|---------------|
| Ausgabe (Fabrikam Ost)          | 600,00       |               |
| Kreditoren (Fabrikam Ost) |              | 600,00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>Generierung und Buchung der Zahlung in Fabrikam für Kreditor "3004"

| Konto                     | Sollbetrag | Habenbetrag |
|-----------------------------|--------------|---------------|
| Kreditoren (Fabrikam) | 600,00       |               |
| Bar (Fabrikam)             |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Ausgleich der Fabrikam-Zahlung mit der Rechnung von Fabrikam Ost

**Buchung für Fabrikam**

| Konto                           | Sollbetrag | Habenbetrag |
|-----------------------------------|--------------|---------------|
| Fällig von Fabrikam Ost (Fabrikam) | 600,00       |               |
| Kreditoren (Fabrikam)       |              | 600,00        |

**Buchung für Fabrikam Ost**

| Konto                          | Sollbetrag | Habenbetrag |
|----------------------------------|--------------|---------------|
| Kreditoren (Fabrikam Ost) | 600,00       |               |
| Fällig an Fabrikam (Fabrikam Ost)  |              | 600,00        |

## <a name="example-2-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>Beispiel 2: Kreditorenzahlung der Rechnung einer anderen juristischen Person mit Skonto
Für Fabrikam Ost liegt eine offene Rechnung für den Kreditor "100" (Fourth Coffee) vor. Für die Rechnung wird ein Skonto in Höhe von EUR 20,00 gewährt. Bei Fabrikam wird eine Zahlung in Höhe von EUR 580,00 für den Fabrikam-Kreditor "3004" (Fourth Coffee) eingegeben und gebucht. Die Zahlung wird mit den offenen Rechnungen für Fabrikam Ost ausgeglichen. Der Skonto wird auf die juristische Person für die Rechnung (Fabrikam Ost) gebucht.

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Buchung der Rechnung in Fabrikam Ost für Kreditor "100" von Fabrikam Ost

| Konto                          | Sollbetrag | Habenbetrag |
|----------------------------------|--------------|---------------|
| Ausgabe (Fabrikam Ost)          | 600,00       |               |
| Kreditoren (Fabrikam Ost) |              | 600,00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Generierung und Buchung der Zahlung in Fabrikam für Fabrikam-Kreditor "3004"

| Konto                     | Sollbetrag | Habenbetrag |
|-----------------------------|--------------|---------------|
| Kreditoren (Fabrikam) | 580,00       |               |
| Bar (Fabrikam)             |              | 580,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Ausgleich der Fabrikam-Zahlung mit der Rechnung von Fabrikam Ost

**Buchung für Fabrikam**

| Konto                           | Sollbetrag | Habenbetrag |
|-----------------------------------|--------------|---------------|
| Fällig von Fabrikam Ost (Fabrikam) | 580,00       |               |
| Kreditoren (Fabrikam)       |              | 580,00        |

**Buchung für Fabrikam Ost**

| Konto                          | Sollbetrag | Habenbetrag |
|----------------------------------|--------------|---------------|
| Kreditoren (Fabrikam Ost) | 580,00       |               |
| Fällig an Fabrikam (Fabrikam Ost)  |              | 580,00        |
| Kreditoren (Fabrikam Ost) | 20,00        |               |
| Skonto (Fabrikam Ost)    |              | 20,00         |

## <a name="example-3-vendor-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-loss"></a>Beispiel 3: Kreditorenzahlung der Rechnung einer anderen juristischen Person mit realisiertem Wechselkursverlust
Für Fabrikam Ost liegt eine offene Rechnung für den Kreditor "100" (Fourth Coffee) vor. Bei Fabrikam wird eine Zahlung für den Fabrikam-Kreditor "3004" (Fourth Coffee) eingegeben und gebucht. Die Zahlung wird mit der offenen Rechnung für Fabrikam Ost ausgeglichen. Im Zuge des Ausgleichsprozesses wird eine Wechselkursverlustbuchung generiert.

-   Wechselkurs von Euro (EUR) in US-Dollar (USD) zum Rechnungsdatum: 1,2062
-   Wechselkurs für EUR in USD zum Zahlungsdatum: 1,2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Buchung der Rechung in Fabrikam Ost für Kreditor "100" von Fabrikam Ost

| Konto                          | Sollbetrag            | Habenbetrag           |
|----------------------------------|-------------------------|-------------------------|
| Ausgabe (Fabrikam Ost)          | 600,00 EUR/723,72 USD |                         |
| Kreditoren (Fabrikam Ost) |                         | 600,00 EUR/723,72 USD |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Generierung und Buchung der Zahlung in Fabrikam für Fabrikam-Kreditor "3004"

| Konto                     | Sollbetrag            | Habenbetrag           |
|-----------------------------|-------------------------|-------------------------|
| Kreditoren (Fabrikam) | 600,00 EUR/736,62 USD |                         |
| Bar (Fabrikam)             |                         | 600,00 EUR/736,62 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Ausgleich der Fabrikam-Zahlung mit der Rechnung von Fabrikam Ost

**Buchung für Fabrikam**

| Konto                           | Sollbetrag            | Habenbetrag           |
|-----------------------------------|-------------------------|-------------------------|
| Fällig von Fabrikam Ost (Fabrikam) | 600,00 EUR/736,62 USD |                         |
| Kreditoren (Fabrikam)       |                         | 600,00 EUR/736,62 USD |
| Realisierter Verlust (Fabrikam)          | 0,00 EUR/12,90 USD    |                         |
| Fällig von Fabrikam Ost (Fabrikam) |                         | 0,00 EUR/12,90 USD    |

**Buchung für Fabrikam Ost**

| Konto                          | Sollbetrag            | Habenbetrag           |
|----------------------------------|-------------------------|-------------------------|
| Kreditoren (Fabrikam Ost) | 600,00 EUR/736,62 USD |                         |
| Fällig an Fabrikam (Fabrikam Ost)  |                         | 600,00 EUR/736,62 USD |
| Fällig an Fabrikam (Fabrikam Ost)  | 0,00 EUR/12,90 USD    |                         |
| Kreditoren (Fabrikam Ost) |                         | EUR 0,00/USD 12,90    |

## <a name="example-4-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-loss"></a>Beispiel 4: Kreditorenzahlung der Rechnung einer anderen juristischen Person mit Skonto und realisiertem Wechselkursverlust
Für Fabrikam Ost liegt eine offene Rechnung für den Kreditor "100" (Fourth Coffee) vor. Auf die Rechnung wird Skonto gewährt, und eine Mehrwertsteuerbuchung wird generiert. Bei Fabrikam wird eine Zahlung für den Fabrikam-Kreditor "3004" (Fourth Coffee) gebucht. Die Zahlung wird mit der offenen Rechnung für Fabrikam Ost ausgeglichen. Im Zuge des Ausgleichsprozesses wird eine Wechselkursverlustbuchung generiert. Der Skonto wird auf die juristische Person für die Rechnung (Fabrikam Ost), der Wechselkursverlust auf die juristische Person für die Zahlung (Fabrikam) gebucht.

-   Wechselkurs von EUR in USD zum Rechnungsdatum: 1,2062
-   Wechselkurs für EUR in USD zum Zahlungsdatum: 1,2277

### <a name="invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-vendor-100"></a>Buchung der Rechnung und Generierung einer Steuerbuchung in Fabrikam Ost für Kreditor "100"

| Konto                          | Sollbetrag            | Habenbetrag           |
|----------------------------------|-------------------------|-------------------------|
| Ausgabe (Fabrikam Ost)          | 564,07 EUR/680,38 USD |                         |
| Mehrwertsteuer (Fabrikam Ost)        | 35,93 EUR/43,34 USD   |                         |
| Kreditoren (Fabrikam Ost) |                         | 600,00 EUR/723,72 USD |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>Generierung und Buchung der Zahlung in Fabrikam für Kreditor "3004"

| Konto                     | Sollbetrag            | Habenbetrag           |
|-----------------------------|-------------------------|-------------------------|
| Kreditoren (Fabrikam) | 588,72 EUR/722,77 USD |                         |
| Bar (Fabrikam Ost)        |                         | 588,72 EUR/722,77 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Ausgleich der Fabrikam-Zahlung mit der Rechnung von Fabrikam Ost

**Buchung für Fabrikam**

| Konto                           | Sollbetrag            | Habenbetrag           |
|-----------------------------------|-------------------------|-------------------------|
| Fällig von Fabrikam Ost (Fabrikam) | 588,72 EUR/722,77 USD |                         |
| Kreditoren (Fabrikam)       |                         | 588,72 EUR/722,77 USD |
| Realisierter Verlust (Fabrikam)          | 0,00 EUR/12,66 USD    |                         |
| Fällig von Fabrikam Ost (Fabrikam) |                         | 0,00 EUR/12,66 USD    |

**Buchung für Fabrikam Ost**

| Konto                          | Sollbetrag            | Habenbetrag           |
|----------------------------------|-------------------------|-------------------------|
| Kreditoren (Fabrikam Ost) | 588,72 EUR/722,77 USD |                         |
| Fällig an Fabrikam (Fabrikam Ost)  |                         | 588,72 EUR/722,77 USD |
| Fällig an Fabrikam (Fabrikam Ost)   | 0,00 EUR/12,66 USD    |                         |
| Kreditoren (Fabrikam Ost) |                         | 0,00 EUR/12,66 USD    |
| Kreditoren (Fabrikam Ost) | 11,28 EUR/13,61 USD   |                         |
| Skonto (Fabrikam Ost)    |                         | 11,28 EUR/13,61 USD   |

## <a name="example-5-vendor-credit-note-with-primary-payment"></a>Beispiel 5: Kreditorengutschrift mit primärer Zahlung
Bei Fabrikam wird eine Zahlung in Höhe von 75,00 für den Kreditor "3004" (Fourth Coffee) generiert. Die Zahlung wird mit einer offenen Rechnung für den Kreditor "3004" von Fabrikam West und einer offenen Gutschrift für den Kreditor "100" von Fabrikam Ost ausgeglichen. Die Zahlung wird im Formular zum Bearbeiten offener Posten als Seite **Transaktion begleich** dargestellt.

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>Buchung der Rechnung an Fabrikam West für Kreditor "3004"

| Konto                          | Sollbetrag | Habenbetrag |
|----------------------------------|--------------|---------------|
| Ausgabe (Fabrikam West)          | 100,00       |               |
| Kreditoren (Fabrikam West) |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>Buchung der Gutschrift an Fabrikam West für Kreditor "100"

| Konto                          | Sollbetrag | Habenbetrag |
|----------------------------------|--------------|---------------|
| Kreditoren (Fabrikam Ost) | 25,00        |               |
| Bestellretouren (Fabrikam Ost) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>Buchung der Zahlung an Fabrikam für Kreditor "3004"

| Konto                     | Sollbetrag | Habenbetrag |
|-----------------------------|--------------|---------------|
| Kreditoren (Fabrikam) | 75,00        |               |
| Bar (Fabrikam)             |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Ausgleich der Fabrikam-Zahlung mit Rechnung für Fabrikam West und Gutschrift für Fabrikam Ost

**Buchung für Fabrikam**

| Konto                           | Sollbetrag | Habenbetrag |
|-----------------------------------|--------------|---------------|
| Kreditoren (Fabrikam)       | 25,00        |               |
| Fällig an Fabrikam Ost (Fabrikam)   |              | 25,00         |
| Fällig von Fabrikam West (Fabrikam) | 100,00       |               |
| Kreditoren (Fabrikam)       |              | 100,00        |

**Buchung für Fabrikam Ost**

| Konto                           | Sollbetrag | Habenbetrag |
|-----------------------------------|--------------|---------------|
| Fällig von Fabrikam (Fabrikam Ost) | 25,00        |               |
| Kreditoren (Fabrikam Ost)  |              | 25,00         |

**Buchung für Fabrikam West**

| Konto                          | Sollbetrag | Habenbetrag |
|----------------------------------|--------------|---------------|
| Kreditoren (Fabrikam West) | 100,00       |               |
| Fällig an Fabrikam (Fabrikam West)  |              | 100,00        |

## <a name="example-6-vendor-credit-note-without-primary-payment"></a>Beispiel 6: Kreditorengutschrift ohne primäre Zahlung
Bei Fabrikam wird eine Zahlung in Höhe von 75,00 für den Kreditor "3004" (Fourth Coffee) generiert. Die Zahlung wird mit einer offenen Rechnung für den Kreditor "3004" von Fabrikam West und einer offenen Gutschrift für den Kreditor "100" von Fabrikam Ost ausgeglichen. Die Zahlung ist im Formular zum Bearbeiten offener Posten als Seite **Transaktion begleich** nicht ausgewählt.

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>Buchung der Rechnung an Fabrikam West für Kreditor "3004"

| Konto                          | Sollbetrag | Habenbetrag |
|----------------------------------|--------------|---------------|
| Ausgabe (Fabrikam West)          | 100,00       |               |
| Kreditoren (Fabrikam West) |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>Buchung der Gutschrift an Fabrikam West für Kreditor "100"

| Konto                          | Sollbetrag | Habenbetrag |
|----------------------------------|--------------|---------------|
| Kreditoren (Fabrikam Ost) | 25,00        |               |
| Bestellretouren (Fabrikam Ost) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>Buchung der Zahlung an Fabrikam für Kreditor "3004"

| Konto                     | Sollbetrag | Habenbetrag |
|-----------------------------|--------------|---------------|
| Kreditoren (Fabrikam) | 75,00        |               |
| Bar (Fabrikam)             |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Ausgleich der Fabrikam-Zahlung mit Rechnung für Fabrikam West und Gutschrift für Fabrikam Ost

**Buchung für Fabrikam**

| Konto                           | Sollbetrag | Habenbetrag |
|-----------------------------------|--------------|---------------|
| Fällig von Fabrikam West (Fabrikam) | 75,00        |               |
| Kreditoren (Fabrikam)       |              | 75,00         |

**Buchung für Fabrikam Ost**

| Konto                                | Sollbetrag | Habenbetrag |
|----------------------------------------|--------------|---------------|
| Fällig von Fabrikam West (Fabrikam Ost) | 25,00        |               |
| Kreditoren (Fabrikam Ost)       |              | 25,00         |

**Buchung für Fabrikam West**

| Konto                              | Sollbetrag | Habenbetrag |
|--------------------------------------|--------------|---------------|
| Kreditoren (Fabrikam West)     | 75,00        |               |
| Fällig an Fabrikam (Fabrikam West)      |              | 75,00         |
| Kreditoren (Fabrikam West)     | 25,00        |               |
| Fällig an Fabrikam Ost (Fabrikam West) |              | 25,00         |





