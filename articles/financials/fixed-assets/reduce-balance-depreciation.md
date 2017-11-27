---
title: Degressive Abschreibung
description: "Dieser Artikel gibt eine Übersicht die Reduktionssaldomethode der Abschreibung."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 29bc8cd02d98479197d7e5f5664b9859c03893b3
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="reduce-balance-depreciation"></a>Degressive Abschreibung

[!include[banner](../includes/banner.md)]


Dieser Artikel gibt eine Übersicht die Reduktionssaldomethode der Abschreibung.

Wenn Sie ein Anlagenabschreibungsprofil einrichten und „Degressiv“ im Feld „Methode“ der Seite „Abschreibungsprofile“ auswählen, werden die Anlagen, denen dieses Abschreibungsprofil zugeordnet ist, in jedem Abschreibungszeitraum um den gleichen Prozentsatz abgeschrieben.

Zum Einrichten der degressiven Abschreibung müssen Sie auch in den Feldern auf dem Inforegister „Allgemein“ der Seite „Abschreibungsprofile“ eine Auswahl treffen. Wählen Sie zunächst im Feld „Abschreibungsjahr“ ein Jahr aus. Je nach Auswahl werden im Feld Periodenhäufigkeit unterschiedliche Optionen angezeigt, wie in den nachstehenden Abschnitten erläutert. 

Sie müssen einen Wert in das Feld Prozentwert für das Abschreibungsprofil auch eingeben. Wenn Sie die Option „Vollständige Abschreibung“ aktivieren, wird die verbleibende Abschreibung auf dem letzten Abschreibungszeitraum ausgeführt und es kann sich um einen großen Betrags handeln. Einigen Ländern/Regionen verwenden keinen Wechsel zu einer linearen Methode. Ein Abschreibungswechsel tritt auf, wenn der Betrag der alternativen Abschreibungsmethode größer oder gleich dem primären Abschreibungsprofilbetrag ist, und als Abschreibungsbetrag wird der Betrag nach der alternativen Methode übernommen. 

Da eine Anlage niemals vollständig auf Basis einer Prozentberechnung abgeschrieben wird, müssen Sie die Option „Vollständige Abschreibung“ aktivieren, um eine Anlage vollständig abzuschreiben.

## <a name="select-a-depreciation-year"></a>Auswählen eines Abschreibungsjahrs
Sie können entweder Kalender oder Steuerlich im Feld Abschreibungsjahr auf der Seite Abschreibungsprofile auswählen. Durch Ihre Auswahl werden die Optionen definiert, die im Feld Periodenhäufigkeit zur Verfügung stehen. Die Standardoption ist Kalender.

### <a name="calendar"></a>Kalender

Mit der Option Kalender wird die Abschreibungsbasis – in der Regel der Nettobuchwert abzüglich des Schrottwerts – am 1. Januar jedes Jahres aktualisiert. Im Beispiel für degressive Abschreibung später in diesem Thema handelt es sich bei der Abschreibungsbasis um den Zähler im ersten Ausdruck in der Spalte "Berechnung". 

Bei Auswahl der Option Kalender stehen im Feld Periodenhäufigkeit die folgenden Optionen zur Verfügung. Dieses Feld dient zum Definieren der Abgrenzung der Buchungsdaten und Beträge für Abschreibungen im Laufe des Kalenderjahrs:

-   Bei Auswahl von Jährlich erfolgt die Buchung am 31. Dezember.
-   Bei Auswahl von Monatlich wird ein monatlicher Betrag am Ende eines jeden Kalendermonats gebucht.
-   Bei Auswahl von Vierteljährlich wird ein Quartalsbetrag am Ende eines jeden Quartals (31. März, 30. Juni, 30. September und 31. Dezember) gebucht.
-   Bei Auswahl von Halbjährlich wird am Ende jedes Kalenderhalbjahrs (30. Juni und 31. Dezember) ein Halbjahresbetrag gebucht.
-   Bei Auswahl von Täglich wird der Abschreibungsbetrag für die Abschreibungsmethode "Täglich" unter Verwendung einer Buchung für jeden Tag gebucht.

Wenn Sie z. B. Jährlich auswählen, wird die jährliche Abschreibung nur einmal am 31. Dezember eines Jahres gebucht. Bei Auswahl von Monatlich wird die monatliche Abschreibung jeden Monat als 1/12 des jährlichen Abschreibungsbetrags gebucht.

### <a name="fiscal"></a>Steuerlich

Wenn Sie im Feld Abschreibungsjahr die Option Steuerlich auswählen, wird die lineare Abschreibungsmethode verwendet. Er wird anhand des Geschäftsjahres berechnet, das auf der Seite Steuerkalender für den Steuerkalender installiert ist, der auf der Seite Sachkonto ausgewählt ist. Für ein Geschäftsjahr vom 1. Juli bis zum 30. Juni beginnt die Abschreibungsberechnung am 1. Juli. Das Geschäftsjahr kann länger oder kürzer als 12 Monate sein. Die Abschreibung wird für jede Steuerperiode angepasst. Die Länge des nächsten Geschäftsjahres basiert auf den Steuerperioden, die Sie beim Erstellen eines neuen Geschäftsjahres auf der Seite Steuerkalender einrichten.


Bei Auswahl der Option Steuerlich stehen im Feld Periodenhäufigkeit die folgenden Optionen zur Verfügung:

-   Bei Auswahl von Jährlich wird der Gesamtbetrag der Abschreibung, der für das Geschäftsjahr berechnet wurde, am letzten Tag des Geschäftsjahrs als einzelner Betrag gebucht.
-   Steuerperiode bucht den Gesamtbetrag der Abschreibung, der für das Geschäftsjahr berechnet wird, das in Steuerperioden aufgeteilt ist, die für den Steuerkalender definiert sind, der auf der Seite Sachkonto ausgewählt ist, oder für den Steuerkalender, der für das Wertmodell oder Abschreibungsbuch für eine Anlage ausgewählt ist.

## <a name="example-of-reducing-balance-depreciation"></a>Beispiel für degressive Abschreibung

Angenommen, der Anlagenanschaffungspreis beträgt 11.000, der Schrottwert 1.000 und der Abschreibungsprozentsatz 30. 

Mithilfe der Reduktionssaldomethode werden am Ende des vorherigen Abschreibungszeitraums 30 % der Abschreibungsbasis (Nettobuchwert minus Schrottwert) berechnet. Die Abschreibung für die ersten drei Jahre wird in der folgenden Tabelle dargestellt.

| Periode | Berechnung des jährlichen Abschreibungsbetrags | Nettobuchwert am Ende des Jahres |
|--------|-------------------------------------------|---------------------------------------|
| Jahr 1 | (11.000 - 1.000) \* 30% = 3.000           | (11.000 - 1.000) - 3.000 = 7.000      |
| Jahr 2 | (7.000 - 1.000) \* 30% = 1.800            | (7.000 - 1.800) = 5.200                |
| Jahr 3 | (5.200 - 1.000) \* 30% = 1.260            | (5.200 - 1.260) = 3.940               |

 
-






