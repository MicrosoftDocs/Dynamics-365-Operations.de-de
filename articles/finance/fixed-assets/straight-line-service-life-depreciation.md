---
title: Abschreibungsmethode "Lineare Nutzungsdauer"
description: Dieser Artikel gibt eine Übersicht über die Abschreibungsmethode "Lineare verbleibende Nutzungsdauer".
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 3341
ms.assetid: ae5ceaeb-aeb7-45cd-b835-23cf9c5cf95a
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a6848aaa679ae42d21b40fdc5f46596aa1f2e899
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009267"
---
# <a name="straight-line-service-life-depreciation"></a>Abschreibungsmethode "Lineare Nutzungsdauer"

[!include [banner](../includes/banner.md)]

Dieser Artikel gibt eine Übersicht über die Abschreibungsmethode "Lineare verbleibende Nutzungsdauer".

Wenn Sie ein Abschreibungsprofil für Anlagen erstellen und auf der Seite Abschreibungsprofile im Feld Methode den Eintrag "Lineare Nutzungsdauer" auswählen, werden die Anlagen, denen dieses Abschreibungsprofil zugeordnet ist, auf Basis der gesamten Nutzungsdauer der jeweiligen Anlage abgeschrieben. Hierbei wird im Allgemeinen in jeder Abschreibungsperiode der gleiche Abschreibungsbetrag angewendet. 

Der Unterschied im berechneten Abschreibungsbetrag zwischen den Methoden "Verbleibende lineare Nutzungsdauer" und "Lineare Nutzungsdauer" ergibt sich, wenn für die Anlage eine Wertregulierung gebucht wird. 

Zum Einrichten der Abschreibung "linearen Abschreibung nach Nutzungsdauer" müssen Sie auch Optionen im Feld Abschreibungsjahr und im Feld Periodenhäufigkeit auf der Seite Abschreibungsprofile auswählen.

## <a name="select-a-depreciation-year"></a>Auswählen eines Abschreibungsjahrs
Sie können entweder Kalender oder Steuerlich im Feld Abschreibungsjahr auf der Seite Abschreibungsprofile auswählen. Durch Ihre Auswahl werden die Optionen definiert, die im Feld Periodenhäufigkeit zur Verfügung stehen. Die Standardoption ist Kalender.

### <a name="calendar"></a>Kalender

Bei Auswahl der Option "Kalender" wird von einem Jahr mit Beginn 1. Januar und Ende 31. Dezember ausgegangen. Dies gilt auch, wenn der Steuerkalender anders definiert wurde. 

Mit der Option "Kalender" wird die Abschreibungsbasis – in der Regel der Nettobuchwert abzüglich des Schrottwerts – am 1. Januar jedes Jahres aktualisiert. In den Beispielen weiter unten in diesem Thema ist der Zähler im ersten Ausdruck in Berechnungen in der Spalte "Berechnung" die Abschreibungsbasis. 

Bei Auswahl der Option Kalender stehen im Feld Periodenhäufigkeit die folgenden Optionen zur Verfügung. Dieses Feld dient zum Definieren der Abgrenzung der Buchungsdaten und Beträge für Abschreibungen im Laufe des Kalenderjahrs:
-   Bei Auswahl von Jährlich wird ein Betrag am 31. Dezember gebucht.
-   Bei Auswahl von Monatlich wird ein monatlicher Betrag am Ende eines jeden Kalendermonats gebucht.
-   Bei Auswahl von Vierteljährlich wird ein Quartalsbetrag am Ende eines jeden Quartals (31. März, 30. Juni, 30. September und 31. Dezember) gebucht.
-   Bei Auswahl von Halbjährlich wird am Ende jedes Kalenderhalbjahrs (30. Juni und 31. Dezember) ein Halbjahresbetrag gebucht.
-   Bei Auswahl von Täglich wird der Abschreibungsbetrag für die Abschreibungsmethode "Täglich" unter Verwendung einer Buchung für jeden Tag gebucht.

Wenn Sie z. B. Jährlich auswählen, wird die jährliche Abschreibung nur einmal am 31. Dezember eines Jahres gebucht. Bei Auswahl von Monatlich wird die monatliche Abschreibung jeden Monat als 1/12 des jährlichen Abschreibungsbetrags gebucht.

### <a name="fiscal"></a>Steuerlich

Wenn Sie im Feld "Steuer" die Option "Abschreibungsjahr" auswählen, wird Abschreibungsmethode "Lineare Nutzungsdauer" verwendet. Sie wird anhand des Geschäftsjahres berechnet, das in dem Steuerkalender festgelegt ist, der für das Wertmodell oder Abschreibungsbuch angegeben ist, oder anhand des Steuerkalenders, der auf der Seite "Sachkonto" ausgewählt wurde. Steuerkalender werden auf der Seite Steuerkalender eingerichtet.

Für ein Geschäftsjahr vom 1. Juli bis zum 30. Juni beginnt die Abschreibungsberechnung am 1. Juli. Das Geschäftsjahr kann länger oder kürzer als 12 Monate sein. Die Abschreibung wird automatisch für jede Steuerperiode angepasst. Die Länge des nächsten Geschäftsjahres basiert auf den Steuerperioden, die Sie beim Erstellen eines neuen Geschäftsjahres im Formular "Steuerkalender" einrichten. 

Bei Auswahl der Option Steuerlich stehen im Feld Periodenhäufigkeit die folgenden Optionen zur Verfügung:
-   Bei Auswahl von Jährlich wird der Gesamtbetrag der Abschreibung, der für das Geschäftsjahr berechnet wird, am letzten Tag des Geschäftsjahrs als einzelner Betrag gebucht.
-   Bei Auswahl von "Steuerperiode" wird der Gesamtbetrag der Abschreibung für das Geschäftsjahr berechnet und in Steuerperioden aufgeteilt, die im Formular "Steuerkalender" für jedes Geschäftsjahr definiert werden.

## <a name="example-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Beispiel: Lineare Abschreibung einer unveränderten Anlage
Angenommen, eine Anlage weist die folgenden Merkmale auf.

|                     |        |
|---------------------|--------|
| Anschaffungskosten    | 11.000 |
| Schrottwert       | 1.000  |
| Abschreibungsgrundlage   | 10.000 |
| Nutzungsdauer (Jahre)  | 5      |
| Jährliche Abschreibung | 2.000  |

In jedem Jahr wird der gleiche Betrag abgeschrieben. (Anschaffungskosten - Schrottwert) / Nutzungsdauer (Jahre)

| Periode | Berechnung des jährlichen Abschreibungsbetrags | Nettobuchwert am Ende des Jahres |
|--------|-------------------------------------------|---------------------------------------|
| Jahr 1 | (11.000 - 1.000) / 5 = 2.000              | 9.000                                 |
| Jahr 2 | (11.000 - 1.000) / 5 = 2.000              | 7.000                                 |
| Jahr 3 | (11.000 - 1.000) / 5 = 2.000              | 5.000                                 |
| Jahr 4 | (11.000 - 1.000) / 5 = 2.000              | 3.000                                 |
| Jahr 5 | (11.000 - 1.000) / 5 = 2.000              | 1.000                                 |

## <a name="example-straight-line-depreciation-of-a-modified-fixed-asset"></a>Beispiel: Lineare Abschreibung einer geänderten Anlage

Angenommen, dass Sie in Jahr 2 eine Anschaffungsänderung von 4.000 an der Anlage vornehmen. 

Die Nutzungsdauer der Anschaffungsänderung ist die gleiche wie die der Anlage selbst und beginnt mit dem Zeitpunkt der Anschaffung. Am Ende von Jahr 5 verbleibt ein Nettobuchwert entsprechend dem Nettobuchwert der Anschaffungsänderung. Die Abschreibung nach Perioden wird wie in der nachstehenden Tabelle gezeigt berechnet.

| Periode | Berechnung des jährlichen Abschreibungsbetrags | Nettobuchwert am Ende des Jahres |
|--------|-------------------------------------------|---------------------------------------|
| Jahr 1 | 10.000 / 5 = 2.000                        | 11.000 - 2.000 = 9.000                |
| Jahr 2 | 4.000 (Anschaffungsänderung)            | 9.000 + 4.000 =13.000                 |
| Jahr 2 | 14.000 / 5 = 2.800                        | 13.000 - 2.800 = 10.200               |
| Jahr 3 | 14.000 / 5 = 2.800                        | 10.200 - 2.800 = 7.400                |
| Jahr 4 | 14.000 / 5 = 2.800                        | 7.400 - 2.800 = 4.600                 |
| Jahr 5 | 14.000 / 5 = 2.800                        | 4.600 - 2.800 = 1.800                 |
| Jahr 6 | Rest 800\*                           | 1.800 – 800 = 1.000                   |

\*Da der Restbetrag geringer als der Abschreibungsbetrag ist, wird nur der Restbetrag abzüglich des Schrottwerts genommen.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]