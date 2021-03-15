---
title: Degressive Abschreibung (175 Prozent)
description: Dieser Artikel gibt eine Übersicht der 175 prozentigen Reduktionssaldomethode der Abschreibung.
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 82af2a810df4ea0ab8880eb2215e22e5818e178d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995039"
---
# <a name="175-percent-reducing-balance-depreciation"></a>Degressive Abschreibung (175 Prozent)

[!include [banner](../includes/banner.md)]

Dieser Artikel gibt eine Übersicht der 175 prozentigen Reduktionssaldomethode der Abschreibung.

Wenn Sie ein Abschreibungsprofil für Anlagen einrichten und **175 % degressiv** im Feld **Methode** auf der Seite **Abschreibungsprofile** auswählen, werden Anlagen, denen das Abschreibungsprofil zugewiesen wird, in jedem Abschreibungszeitraum um denselben Prozentsatz abgeschrieben. 

Zum Einrichten der 175% degressiven Abschreibung müssen Sie auch Optionen im Feld **Abschreibungsjahr** und im Feld **Periodenhäufigkeit** auf der Seite **Abschreibungsprofile** auswählen. Die Optionen, die im Feld **Periodenhäufigkeit** zur Verfügung stehen, variieren abhängig vom Wert, der im Feld **Abschreibungsjahr** ausgewählt ist.

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

Wenn Sie **Steuerlich** im Feld **Jahresabschreibung** auswählen, wird die Abschreibungsmethode "175 % degressiv" auf Grundlage des Geschäftsjahres für den Steuerkalender berechnet, der für das Wertmodell oder das Abschreibungsbuch angegeben wird, oder für den Steuerkalender, der auf der Seite **Sachkonto** ausgewählt wird. Steuerkalender werden auf der Seite **Steuerkalender** eingerichtet. Weitere Informationen finden Sie unter [Steuerkalender, Geschäftsjahre und Perioden](../budgeting/fiscal-calendars-fiscal-years-periods.md).

Für das Geschäftsjahr vom 1. Juli bis zum 30. Juni beginnt die Abschreibungsberechnung am 1. Juli. Das Geschäftsjahr kann länger oder kürzer als 12 Monate sein. Die Abschreibung wird automatisch für jede Periode angepasst, und die Länge des nächsten Geschäftsjahres wird mit den Einstellungen für die Perioden auf der Seite **Steuerkalender** bestimmt. 

Wenn als Abschreibungsjahr **Steuerlich** ausgewählt wird, stehen im Feld **Periodenhäufigkeit** die folgenden Optionen zur Verfügung:

-   Bei Auswahl von **Jährlich** wird der Gesamtbetrag der Abschreibung, der für das Geschäftsjahr berechnet wurde, am letzten Tag des Geschäftsjahrs als einzelner Betrag gebucht.
-   **Finanzzeitraum** berechnet den Gesamtbetrag der Abschreibung für das Geschäftsjahr. Dieser Betrag wird auf Steuerperioden aufgeteilt, die auf der Seite **Steuerkalender** definiert werden.

## <a name="example-of-175-reducing-balance-depreciation"></a>Beispiel für die Abschreibungsmethode "175 % degressiv"

|                                |        |
|--------------------------------|--------|
| Anschaffungskosten               | 11.000 |
| Schrottwert                  | 1.000  |
| Abschreibungsgrundlage              | 10.000 |
| Nutzungsdauer (Jahre)             | 5      |
| Jährlicher Abschreibungsprozentsatz | 35 %    |

Bei der Abschreibungsmethode „175 % degressiv“ werden 175 Prozent durch die Anzahl der Jahre der Nutzungsdauer dividiert. Der sich ergebende Prozentsatz wird mit dem Nettobuchwert der Anlage multipliziert, um den Abschreibungsbetrag für das Jahr zu ermitteln.

| Zeitraum | Berechnung des jährlichen Abschreibungsbetrags | Buchwert                  | Nettobuchwert am Ende des Jahres |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| Jahr 1 | (11.000 – 1.000) × 35 % = 3.500                | 11.000 – 3.500 = 7.500      | 11.000 – 1.000 – 3.500 = 6.500        |
| Jahr 2 | 6.500 × 35 % = 2.275                           | 7.500 – 2.275 = 5.225       | 6.500 – 2.275 = 4.225                 |
| Jahr 3 | 4.225 × 35 % = 1.478,75                        | 5.225 – 1.478,75 = 3.746,25 | 4.225 – 1.478,75 = 2.746,25           |

> [!NOTE] 
> Hinweis: Wenn der Betrag, der mithilfe der Abschreibungsmethode "175% degressiv" berechnet wird, geringer ausfällt, als der Betrag, der mithilfe der Methode "Linear" berechnet würde, gibt es eine Umrechnung zur linearen Methode für die verbleibende Nutzungsdauer.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]