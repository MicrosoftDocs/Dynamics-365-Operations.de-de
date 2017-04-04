---
title: Abschreibungsmethode &quot;Verbleibende lineare Nutzungsdauer&quot;
description: "Dieser Artikel gibt eine Übersicht über die Abschreibungsmethode &quot;Verbleibende lineare Nutzungsdauer&quot;."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b41901d573e977a89fcd1a7c1ebf7185e162c654
ms.openlocfilehash: 9b690b80f148e7ccecba19850bd78c81216d8658
ms.lasthandoff: 03/31/2017


---

# <a name="straight-line-life-remaining-depreciation"></a>Abschreibungsmethode "Verbleibende lineare Nutzungsdauer"

Dieser Artikel gibt eine Übersicht über die Abschreibungsmethode "Verbleibende lineare Nutzungsdauer".

Wenn Sie ein Anlageabschreibungsprofil erstellen und im Feld **Methode** auf der Seite **Abschreibungsprofile** die Option **Verbleibende lineare Nutzungsdauer** auswählen, basiert die Abschreibung der Anlagen, die dem Abschreibungsprofil zugewiesen werden, auf der verbleibenden Nutzungsdauer der Anlage. Der Abschreibungsbetrag ist im Allgemeinen der gleiche in jedem Abschreibungszeitraum. Zum Einrichten der Abschreibung "Verbleibende lineare Nutzungsdauer" müssen Sie auch Optionen im Feld **Abschreibungsjahr** und im Feld **Periodenhäufigkeit** auf der Seite **Abschreibungsprofile** auswählen. Die Optionen, die im Feld **Periodenhäufigkeit** zur Verfügung stehen, variieren abhängig vom Wert, der im Feld **Abschreibungsjahr** ausgewählt ist.

## <a name="select-a-depreciation-year"></a>Auswählen eines Abschreibungsjahrs
Sie können entweder **Kalender** oder **Steuerlich** im Feld **Abschreibungsjahr** auf der Seite **Abschreibungsprofile** auswählen. Der Standardwert ist **Kalender**. Durch Ihre Auswahl werden die Optionen bestimmt, die im Feld **Periodenhäufigkeit** zur Verfügung stehen. In diesem Feld wird die Abgrenzung der Buchungsdaten und Beträge für Abschreibungen über das Kalenderjahr definiert.

### <a name="calendar"></a>Kalender

** Kalender ** Wenn Sie im Feld *** Abschreibungsjahr *** Feld auswählen, wird von einem Jahr mit dem 1. Januar bis zum 31. Dezember akzeptiert, auch wenn der Steuerkalender anders definiert haben. Die **Kalender** Option aktualisiert die Abschreibungsbasis am 1. Januar jedes Jahres. Normalerweise ist die Abschreibungsbasis der Nettobuchwert abzüglich des Restwerts. Im Beispiel weiter unten in diesem Thema ist der Zähler im ersten Ausdruck in Berechnungen in der Spalte "Berechnung" die Abschreibungsbasis. Wenn als Abschreibungsjahr **Kalender** ausgewählt wird, stehen im Feld **Periodenhäufigkeit** die folgenden Optionen zur Verfügung:

-   Bei Auswahl von **Jährlich** wird ein Betrag am 31. Dezember gebucht.
-   Bei Auswahl von **Monatlich** wird ein monatlicher Betrag am Ende eines jeden Kalendermonats gebucht.
-   Bei Auswahl von **Vierteljährlich** wird ein Quartalsbetrag am Ende eines jeden Quartals (31. März, 30. Juni, 30. September und 31. Dezember) gebucht.
-   Bei Auswahl von **Halbjährlich** wird am Ende jedes Kalenderhalbjahrs (30. Juni und 31. Dezember) ein Halbjahresbetrag gebucht.
-   Bei Auswahl von **Täglich** wird der Abschreibungsbetrag für die Abschreibungsmethode "Täglich" unter Verwendung einer Buchung für jeden Tag gebucht.

Wenn Sie z. B. **Jährlich** auswählen, wird die jährliche Abschreibung nur einmal am 31. Dezember eines Jahres gebucht. Bei Auswahl von **Monatlich** wird die monatliche Abschreibung jeden Monat als 1/12 des jährlichen Abschreibungsbetrags gebucht.

### <a name="fiscal"></a>Steuerlich

Wenn Sie die Option **Steuerlich** im Feld **Abschreibungsjahr** auswählen, wird die Abschreibungsmethode "Verbleibende lineare Nutzungsdauer" verwendet. Die Abschreibung wird anhand der verbleibenden Geschäftsjahre berechnet. Beispiel für das Geschäftsjahr am 1. Juli 2015 bis zum 30. Juni 2016 die bis zum.am 1. Juli Das Geschäftsjahr kann länger oder kürzer als 12 Monate sein. Die Abschreibung wird für jede Steuerperiode angepasst. Die Länge des nächsten Geschäftsjahrs wird anhand der Finanzzeiträume bestimmt, die auf der Seite **Steuerkalender** eingerichtet werden. Wenn als Abschreibungsjahr **Steuerlich** ausgewählt wird, stehen im Feld **Periodenhäufigkeit** die folgenden Optionen zur Verfügung:

-   Bei Auswahl von **Jährlich** wird der Gesamtbetrag der Abschreibung, der für das Geschäftsjahr berechnet wird, am letzten Tag des Geschäftsjahrs als einzelner Betrag gebucht.
-   **Finanzzeitraum **berechnet den Gesamtbetrag der Abschreibung für das Geschäftsjahr. Dieser Betrag wird dann in Finanzzeiträume aufgeteilt, die auf der Seite **Steuerkalender** für den Steuerkalender definiert werden, der für das Wertmodell oder Abschreibungsbuch angegeben wird.

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Beispiel für eine lineare Abschreibung einer unveränderten Anlage
Eine Anlage weist die folgenden Merkmale auf.

|                     |        |
|---------------------|--------|
| Anschaffungskosten    | 11.000 |
| Schrottwert       | 1.000  |
| Abschreibungsgrundlage   | 10.000 |
| Nutzungsdauer (Jahre)  | 5      |
| Jährliche Abschreibung | 2.000  |

Der Abschreibungsbetrag ist derselbe jedes Jahr: (Anschaffungskosten – Restwert) ÷ Nutzungsdauer (Jahre)

| Zeitraum | Berechnung des jährlichen Abschreibungsbetrags | Nettobuchwert am Ende des Jahres |
|--------|-----------------------------------------------|---------------------------------------|
| Jahr 1 | (11.000 – 1.000) ÷ 5 = 2.000                  | 9.000                                 |
| Jahr 2 | (9.000 – 1.000) ÷ 4 = 2.000                   | 7.000                                 |
| Jahr 3 | (7.000 – 1.000) ÷ 3 = 2.000                   | 5.000                                 |
| Jahr 4 | (5.000 – 1.000) ÷ 2 = 2.000                   | 3.000                                 |
| Jahr 5 | (3.000 – 1.000) ÷ 1 = 2.000                   | 1.000                                 |




