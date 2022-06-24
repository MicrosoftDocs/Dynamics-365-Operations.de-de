---
title: Degressiven Abschreibung von 200 Prozent
description: Dieser Artikel gibt eine Übersicht der 200 prozentigen Reduktionssaldomethode der Abschreibung.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7abcf26f3e658e8a6f451f26240890d183547982
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870161"
---
# <a name="200-percent-reducing-balance-depreciation"></a>Degressiven Abschreibung von 200 Prozent

[!include [banner](../includes/banner.md)]

Dieser Artikel gibt eine Übersicht der 200 prozentigen Reduktionssaldomethode der Abschreibung.

Wenn Sie ein Abschreibungsprofil für Anlagen einrichten und **200% degressiv** im Feld **Methode** auf der Seite **Abschreibungsprofile** auswählen, werden Anlagen, denen das Abschreibungsprofil zugewiesen wird, in jedem Abschreibungszeitraum um denselben Prozentsatz abgeschrieben. Der Prozentsatz wird auf Grundlage der Nutzungsdauer der Anlage berechnet. Wenn eine Anlage beispielsweise eine Nutzungsdauer von fünf Jahren hat, beträgt der Prozentsatz 40 Prozent (200% ÷ 5). 

Diese Methode wird auch als "degressive Doppelratenabschreibung" bezeichnet.

Zum Einrichten der 200% degressiven Abschreibung müssen Sie auch Optionen im Feld **Abschreibungsjahr** und im Feld **Periodenhäufigkeit** auf der Seite **Abschreibungsprofile** auswählen. Die Optionen, die im Feld **Periodenhäufigkeit** zur Verfügung stehen, variieren abhängig vom Wert, den Sie im Feld **Abschreibungsjahr** auswählen.

## <a name="select-a-depreciation-year"></a>Auswählen eines Abschreibungsjahrs
Sie können entweder **Kalender** oder **Steuerlich** im Feld **Abschreibungsjahr** auf der Seite **Abschreibungsprofile** auswählen. Der Standardwert ist **Kalender**. 

Durch Ihre Auswahl werden die Optionen bestimmt, die im Feld **Periodenhäufigkeit** zur Verfügung stehen. In diesem Feld wird die Abgrenzung der Buchungsdaten und Beträge für Abschreibungen über das Kalenderjahr definiert.

### <a name="calendar"></a>Kalender

Falls gewünscht, können Sie im Feld **Abschreibungsjahr** den Standardwert **Kalender** beibehalten. 

Die **Kalender** Option aktualisiert die Abschreibungsbasis am 1. Januar jedes Jahres. Normalerweise ist die Abschreibung der Nettobuchwert abzüglich des Restwerts. In den Beispielen weiter unten in diesem Artikel ist der Zähler im ersten Ausdruck in Berechnungen in der Spalte „Berechnung“ die Abschreibungsbasis. 

Wenn als Abschreibungsjahr **Kalender** ausgewählt wird, stehen im Feld **Periodenhäufigkeit** die folgenden Optionen zur Verfügung:

-   Bei Auswahl von **Jährlich** wird ein Betrag am 31. Dezember gebucht.
-   Bei Auswahl von **Monatlich** wird ein monatlicher Betrag am Ende eines jeden Kalendermonats gebucht.
-   Bei Auswahl von **Vierteljährlich** wird ein Quartalsbetrag am Ende eines jeden Quartals (31. März, 30. Juni, 30. September und 31. Dezember) gebucht.
-   Bei Auswahl von **Halbjährlich** wird am Ende jedes Kalenderhalbjahrs (30. Juni und 31. Dezember) ein Halbjahresbetrag gebucht.
-   Bei Auswahl von **Täglich** wird der Abschreibungsbetrag für die Abschreibungsmethode "Täglich" unter Verwendung einer Buchung für jeden Tag gebucht.

### <a name="fiscal"></a>Steuerlich

Wenn Sie **Steuerlich** im Jahrfeld **Abschreibung** auswählen, wird die Abschreibungsmethode "200 % degressiv" auf Grundlage des Geschäftsjahres für den Steuerkalender berechnet, der für das Wertmodell oder das Abschreibungsbuch angegeben wird, oder für den Steuerkalender, der auf der Seite **Sachkonto** ausgewählt wird. Steuerkalender werden auf der Seite **Steuerkalender** eingerichtet. 

Für das Geschäftsjahr vom 1. Juli bis zum 30. Juni beginnt die Abschreibungsberechnung am 1. Juli. Das Geschäftsjahr kann länger oder kürzer als 12 Monate sein. Die Abschreibung wird für jede Periode angepasst. Die Länge des nächsten Geschäftsjahrs wird anhand der Finanzzeiträume bestimmt, die auf der Seite **Steuerkalender** eingerichtet werden. 

Wenn **Steuerlich** als Abschreibungsjahr ausgewählt wird, stehen im Feld **Periodenhäufigkeit** die folgenden Optionen zur Verfügung:

-   Bei Auswahl von **Jährlich** wird der Gesamtbetrag der Abschreibung, der für das Geschäftsjahr berechnet wird, am letzten Tag des Geschäftsjahrs als einzelner Betrag gebucht.
-   **Finanzzeitraum** bucht den Gesamtbetrag der Abschreibung, die für das Geschäftsjahr berechnet wird. Dieser Betrag wird auf Steuerperioden aufgeteilt, die auf der Seite **Steuerkalender** definiert werden.

## <a name="example-of-200-reducing-balance-depreciation"></a>Beispiel für die Abschreibungsmethode "200 % degressiv"

| &nbsp;                         | &nbsp; |
|--------------------------------|--------|
| Anschaffungskosten               | 11.000 |
| Schrottwert                  | 1, 000 |
| Abschreibungsgrundlage              | 10.000 |
| Nutzungsdauer (Jahre)             | 5      |
| Jährlicher Abschreibungsprozentsatz | 40 %    |

Bei der Abschreibungsmethode „200 % degressiv“ werden 200 Prozent durch die Anzahl der Jahre der Nutzungsdauer dividiert. Der sich ergebende Prozentsatz wird mit dem Nettobuchwert der Anlage multipliziert, um den Abschreibungsbetrag für das Jahr zu ermitteln.

| Zeitraum | Berechnung des jährlichen Abschreibungsbetrags | Buchwert             | Nettobuchwert am Ende des Jahres |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| Jahr 1 | (11.000 – 1.000) × 40 % = 4.000                | 11.000 – 4.000 = 7.000 | 11.000 – 1.000 – 4.000 = 6.000        |
| Jahr 2 | 6.000 × 40 % = 2.400                           | 7.000 – 2.400 = 4.600  | 6.000 – 2.400 = 3.600                 |
| Jahr 3 | 3.600 × 40 % = 1.440                           | 4.600 – 1.440 = 3.160  | 3.600 – 1.440 = 2.160                 |

> [!NOTE] 
> Hinweis: Wenn der Betrag, der mithilfe der Abschreibungsmethode "200% degressiv" berechnet wird, geringer ausfällt, als der Betrag, der mithilfe der Methode "Linear" berechnet würde, gibt es eine Umrechnung zur linearen Methode für die verbleibende Nutzungsdauer.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
