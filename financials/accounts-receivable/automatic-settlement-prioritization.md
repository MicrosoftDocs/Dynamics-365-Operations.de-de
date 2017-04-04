---
title: Automatischer Ausgleich und Priorisierung
description: "In diesem Artikel wird beschrieben, wie Buchungen ausgeglichen werden, wenn Sie &quot;Automatischer Ausgleich&quot; auf der Seite &quot;Debitorenparameter&quot; auswählen. Es wird ausserdem erläutert, wie der automatische Ausgleich in Kombination mit der Zahlungspriorität verwendet werden kann."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14531
ms.assetid: e7837cf6-ec69-44b4-8d47-eba38d5c7b1f
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: a751973b49febd6925267d00fb1d2c72114f86b0
ms.lasthandoff: 03/31/2017


---

# <a name="automatic-settlement-and-prioritization"></a>Automatischer Ausgleich und Priorisierung

In diesem Artikel wird beschrieben, wie Buchungen ausgeglichen werden, wenn Sie "Automatischer Ausgleich" auf der Seite "Debitorenparameter" auswählen. Es wird ausserdem erläutert, wie der automatische Ausgleich in Kombination mit der Zahlungspriorität verwendet werden kann.

Sie haben zwei Optionen, wenn Sie Zahlungen mit Rechnungen und anderen Buchungen ausgleichen. Sie können die Buchungen manuell aktiviert werden, um Beträge auszugleichen, oder Microsoft Dynamics 365 für Arbeitsgänge kann die Buchungen automatisch auswählen, indem die automatischen Ausgleich verwendet. Sie können auch anpassen, wie automatische Ausgleiche verarbeitet werden, indem Sie die Option **Ausgleich priorisieren** verwenden. Alle diese Optionen sind Teil der Ausgleichsparameter, die auf der Seite ** Debitorenparameter ** definiert werden. Die Art, in der Buchungen automatisch ausgeglichen werden, kann sich je nach der Methode unterscheiden, die Sie für den automatischen Ausgleich verwenden. Folgende Methoden stehen zur Verfügung:

-   Benutzerdefinierte Ausgleichspriorität
-   Standardmäßiger automatischer Ausgleich

In den folgenden Abschnitten wird beschrieben, wie Buchungen für jede Methode ausgeglichen werden.

## <a name="example-transactions"></a>Beispielbuchungen
Die Beispiele von Ausgleichungen weiter unten in diesem Artikel basieren auf den folgenden Buchungen. Alle Buchungen sind für Debitor 2050.

| Buchung   | Datum        | Betrag | Skontobedingungen. | Skontodatum | Kommentare                                                                                                                                                                                      |
|---------------|-------------|--------|---------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rechnung 1     | 15. August   | 100,00 | 2%14, Netto 30        | 29. August          |                                                                                                                                                                                               |
| Rechnung 2     | 1. September | 250,00 | 2%14, Netto 30        | 15. September       |                                                                                                                                                                                               |
| Rechnung 3     | 15. Oktober  | 500,00 | 2% 14/Netto 30        | 29. Oktober         |                                                                                                                                                                                               |
| Zinsrechnung | 15. Oktober  | 7:00   |                     |                    | Die Zinsrechnung wird für Rechnung 1 und 2. Rechnung. Der Betrag wird als 2 -Prozent-Zinsen auf Beträge, die 30 Tage überfällig sind oder mehr berechnet. Beispiel: 0,02 × (100,00 + 250,00) = 7,00. |

## <a name="userdefined-settlement-priority"></a>Benutzerbestimmte Ausgleichspriorität
Wenn Sie **Priorität für automatischen Ausgleich verwenden** auf **Ja** auf der Seite **Debitorenparameter** festlegen, wird die Ausgleichspriorität, die Sie auf der Seite **Ausgleichspriorität** definieren, verwendet, wenn Buchungen für automatischen Ausgleich ausgewählt werden. Im vorliegenden Beispiel wird die nächste Ausgleichspriorität definiert:

1.  Transaktionstyp
    -   Zahlungsgebühren
    -   Mahnschreiben
    -   Zinsrechnungen
    -   Rechnungen

2.  Buchungsdatum, Aufsteigend
3.  Beleg

Wenn Sie eine Zahlung für 700,00 am 25. Oktober buchen, werden die Buchungen in der folgenden Reihenfolge für den Ausgleich ausgewählt.

| Beleg       | Datum       | Rechnung | Betrag in Buchungswährung | Auszugleichender Betrag | Gesamtbetrag | Währung |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Zinsrechnung | 15. Oktober 2015 |         | 7:00                           | 7:00             | 0,00    | USD      |
| Rechnung 1     | 15. August 2015  | 10001   | 100,00                         | 100,00           | 0,00    | USD      |
| Rechnung 2     | 1. September 2015   | 10002   | 250,00                         | 250,00           | 0,00    | USD      |
| Rechnung 3     | 15. Oktober 2015 |         | 500,00                         | 343,00           | 157,00  | USD      |

## <a name="default-automatic-settlement"></a>Standardmäßiger automatischer Ausgleich
Wenn keine benutzerdefinierte Ausgleichspriorität vorhanden ist, werden Buchungen automatisch für den Ausgleich basierend auf dem Fälligkeitsdatum ausgewählt. Die Buchungen, die ausgeglichen werden, müssen die gleiche Währung wie die Buchung haben, mit der sie ausgeglichen werden. Wenn Sie eine Zahlung für 700,00 am 25. Oktober buchen, werden die folgenden Buchungen für den Ausgleich ausgewählt.

| Beleg       | Datum       | Rechnung | Betrag in Buchungswährung | Auszugleichender Betrag | Gesamtbetrag | Währung |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Rechnung 1     | 15. August 2015  | 10001   | 100,00                         | 100,00           | 0,00    | USD      |
| Rechnung 2     | 1. September 2015   | 10002   | 250,00                         | 250,00           | 0,00    | USD      |
| Rechnung 3     | 15. Oktober 2015 |         | 500,00                         | 350,00           | 150,00  | USD      |
| Zinsrechnung | 15. Oktober 2015 |         | 7:00                           | 0,00             | 0,00    | USD      |




