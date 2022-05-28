---
title: Automatischer Ausgleich und Priorisierung
description: In diesem Artikel wird beschrieben, wie Buchungen ausgeglichen werden, wenn Sie "Automatischer Ausgleich" auf der Seite "Debitorenparameter" auswählen. Es wird ausserdem erläutert, wie der automatische Ausgleich in Kombination mit der Zahlungspriorität verwendet werden kann.
author: ShivamPandey-msft
ms.date: 01/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: kfend
ms.custom: 14531
ms.assetid: e7837cf6-ec69-44b4-8d47-eba38d5c7b1f
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 47ccdb49b4d5c43b4f9cb9a967bd30376474e4c1
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712257"
---
# <a name="automatic-settlement-and-prioritization"></a>Automatischer Ausgleich und Priorisierung

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Buchungen ausgeglichen werden, wenn Sie "Automatischer Ausgleich" auf der Seite "Debitorenparameter" auswählen. Es wird ausserdem erläutert, wie der automatische Ausgleich in Kombination mit der Zahlungspriorität verwendet werden kann.

Sie haben zwei Optionen, wenn Sie Zahlungen mit Rechnungen und anderen Buchungen ausgleichen. Sie können die auszugleichenden Transaktionen manuell auswählen, oder das System kann die Transaktionen automatisch auswählen, indem die automatische Ausgleichsfunktion verwendet wird. Sie können auch anpassen, wie automatische Ausgleiche verarbeitet werden, indem Sie die Option **Ausgleich priorisieren** verwenden. All diese Optionen sind Teil der Ausgleichsparameter, die auf der Seite **Debitorenparameter** definiert werden. Die Art, in der Buchungen automatisch ausgeglichen werden, kann sich je nach der Methode unterscheiden, die Sie für den automatischen Ausgleich verwenden. Folgende Methoden stehen zur Verfügung:

-   Benutzerdefinierte Ausgleichspriorität
-   Standardmäßiger automatischer Ausgleich

In den folgenden Abschnitten wird beschrieben, wie Buchungen für jede Methode ausgeglichen werden.

## <a name="example-transactions"></a>Beispielbuchungen
Die Beispiele von Ausgleichungen weiter unten in diesem Artikel basieren auf den folgenden Buchungen. Alle Buchungen sind für Debitor 2050.

| Buchung   | Datum        | Betrag | Skontobedingungen. | Skontodatum | Kommentare                                                                                                                                                                                      |
|---------------|-------------|--------|---------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rechnung 1     | 15. August   | 100,00 | 2%14, Netto 30        | 29. August          |                                                                                                                                                                                               |
| Rechnung 2     | 1. September | 250,00 | 2%14, Netto 30        | 15. September       |                                                                                                                                                                                               |
| Rechnung 3     | Oktober 15  | 500,00 | 2% 14/Netto 30        | 29. Oktober         |                                                                                                                                                                                               |
| Zinsrechnung | 15. Oktober  | 7:00   |                     |                    | Die Zinsrechnung ist für Rechnung 1 und 2. Der Betrag wird als 2 Prozent-Zinsen auf Beträge berechnet, die 30 Tage oder länger überfällig sind. Beispiel: 0,02 × (100,00 + 250,00) = 7,00. |

## <a name="user-defined-settlement-priority"></a>Benutzerdefinierte Ausgleichspriorität
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
| Rechnung 3     | 15. Oktober 2015 |         | 500.00                         | 350.00           | 150.00  | EUR      |
| Zinsrechnung | 15. Oktober 2015 |         | 7.00                           | 0,00             | 7.00    | EUR      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
