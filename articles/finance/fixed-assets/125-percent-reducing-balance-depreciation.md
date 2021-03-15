---
title: Degressiven Abschreibung von 125 Prozent
description: Dieser Artikel gibt eine Übersicht die 125 Prozent Reduktionssaldomethode der Abschreibung.
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9511917d72a1bb45daf2ce7e4b56d94c17825daf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969227"
---
# <a name="125-percent-reducing-balance-depreciation"></a>Degressiven Abschreibung von 125 Prozent

[!include [banner](../includes/banner.md)]

Dieser Artikel gibt eine Übersicht die 125 Prozent Reduktionssaldomethode der Abschreibung.

Wenn Sie ein Abschreibungsprofil für Anlagen einrichten und **125 % degressiv** im Feld **Methode** auf der Seite **Abschreibungsprofile** auswählen, werden Anlagen, denen das Abschreibungsprofil zugewiesen wird, in jedem Abschreibungszeitraum um denselben Prozentsatz abgeschrieben. Dieser Prozentsatz wird auf Grundlage der Nutzungsdauer der Anlage berechnet. Wenn eine Anlage beispielsweise eine Nutzungsdauer von fünf Jahren hat, beträgt der Prozentsatz 25 Prozent (125 % ÷ 5).

Zum Einrichten der 125% degressiven Abschreibung müssen Sie auch Optionen im Feld **Abschreibungsjahr** und im Feld **Periodenhäufigkeit** auf der Seite **Abschreibungsprofile** auswählen. Die Optionen, die im Feld **Periodenhäufigkeit** zur Verfügung stehen, variieren abhängig vom Wert, der im Feld **Abschreibungsjahr** ausgewählt ist.

## <a name="select-a-depreciation-year"></a>Auswählen eines Abschreibungsjahrs
Sie können entweder **Kalender** oder **Steuerlich** im Feld **Abschreibungsjahr** auf der Seite **Abschreibungsprofile** auswählen. Der Standardwert ist **Kalender**. 

Durch Ihre Auswahl werden die Optionen bestimmt, die im Feld **Periodenhäufigkeit** zur Verfügung stehen. In diesem Feld wird die Abgrenzung der Buchungsdaten und Beträge für Abschreibungen über das Kalenderjahr definiert.

### <a name="calendar"></a>Kalender

Falls gewünscht, können Sie im Feld **Abschreibungsjahr** den Standardwert **Kalender** beibehalten. 

Die **Kalender** Option aktualisiert die Abschreibungsbasis am 1. Januar jedes Jahres. Normalerweise ist die Abschreibungsbasis der Nettobuchwert abzüglich des Restwerts. In den Beispielen weiter unten in diesem Thema ist der Zähler im ersten Ausdruck in Berechnungen in der Spalte "Berechnung" die Abschreibungsbasis. 

Wenn als Abschreibungsjahr **Kalender** ausgewählt wird, stehen im Feld **Periodenhäufigkeit** die folgenden Optionen zur Verfügung:

-   Bei Auswahl von **Jährlich** wird ein Betrag am 31. Dezember gebucht.
-   Bei Auswahl von **Monatlich** wird ein monatlicher Betrag am Ende eines jeden Kalendermonats gebucht.
-   Bei Auswahl von **Vierteljährlich** wird ein Quartalsbetrag am Ende eines jeden Quartals (31. März, 30. Juni, 30. September und 31. Dezember) gebucht.
-   Bei Auswahl von **Halbjährlich** wird am Ende jedes Kalenderhalbjahrs (30. Juni und 31. Dezember) ein Halbjahresbetrag gebucht.
-   Bei Auswahl von **Täglich** wird der Abschreibungsbetrag für die Abschreibungsmethode "Täglich" unter Verwendung einer Buchung für jeden Tag gebucht.

### <a name="fiscal"></a>Steuerlich

Wenn Sie **Steuerlich** im Feld **Jahresabschreibung** auswählen, wird die Abschreibungsmethode "125 % degressiv" auf Grundlage des Geschäftsjahres für den Steuerkalender berechnet, der für das Wertmodell oder das Abschreibungsbuch angegeben wird, oder für den Steuerkalender, der auf der Seite **Sachkonto** ausgewählt wird. Steuerkalender werden auf der Seite **Steuerkalender** eingerichtet. 

Für das Geschäftsjahr vom 1. Juli bis zum 30. Juni beginnt die Abschreibungsberechnung am 1. Juli. Das Geschäftsjahr kann länger oder kürzer als 12 Monate sein. Die Abschreibung wird automatisch für jede Periode angepasst, und die Länge des nächsten Geschäftsjahres wird mit den Einstellungen für die Perioden auf der Seite **Steuerkalender** bestimmt. 

Wenn als Abschreibungsjahr **Steuerlich** ausgewählt wird, stehen im Feld **Periodenhäufigkeit** die folgenden Optionen zur Verfügung:

-   Bei Auswahl von **Jährlich** wird der Gesamtbetrag der Abschreibung, der für das Geschäftsjahr berechnet wird, am letzten Tag des Geschäftsjahrs als einzelner Betrag gebucht.
-   **Finanzzeitraum** bucht den Gesamtbetrag der Abschreibung, die für das Geschäftsjahr berechnet wird. Dieser Betrag wird auf Steuerperioden aufgeteilt, die auf der Seite **Steuerkalender** definiert werden.

## <a name="example-of-125-reducing-balance-depreciation"></a>Beispiel für die Abschreibungsmethode "125 % degressiv"

|                                |        |
|--------------------------------|--------|
| Anschaffungskosten               | 11.000 |
| Schrottwert                  | 1.000  |
| Abschreibungsgrundlage              | 10.000 |
| Nutzungsdauer (Jahre)             | 5      |
| Jährlicher Abschreibungsprozentsatz | 25 %    |

Bei der Abschreibungsmethode „125 % degressiv“ werden 125 Prozent durch die Anzahl der Jahre der Nutzungsdauer dividiert. Der sich ergebende Prozentsatz wird mit dem Nettobuchwert der Anlage multipliziert, um den Abschreibungsbetrag für das Jahr zu ermitteln.

| Zeitraum | Berechnung des jährlichen Abschreibungsbetrags | Buchwert                    | Nettobuchwert am Ende des Jahres |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| Jahr 1 | (11.000 – 1.000) × 25 % = 2.500                | (11.000 – 2.500) = 8.500      | (11.000 – 1.000 – 2.500) = 7.500      |
| Jahr 2 | 7.500 × 25 % = 1.875                           | (8.500 – 1.875) = 6.625       | (7.500 – 1.875) = 5.625               |
| Jahr 3 | 5.625 × 25 % = 1.406,25                        | (6.625 – 1.406,25) = 5.218,75 | (5.625 – 1.406,25) = 4.218,75         |

> [!NOTE] 
> Hinweis: Wenn der Betrag, der mithilfe der Abschreibungsmethode "125% degressiv" berechnet wird, geringer ausfällt, als der Betrag, der mithilfe der Methode "Linear" berechnet würde, gibt es eine Umrechnung zur linearen Methode für die verbleibende Nutzungsdauer.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]