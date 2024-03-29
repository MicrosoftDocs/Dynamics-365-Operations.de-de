---
title: Einrichten von Zinssätzen für einen Zinscode
description: Zinscodes enthalten Einstellungen, die festlegen, wann Zinsen erhoben werden und wie Zinsen für fällige Rechnungen berechnet werden.
author: ShivamPandey-msft
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: kfend
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c1d85e50a8e6f57ed0678fa6169d94152320861
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726071"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a>Einrichten von Zinssätzen für einen Zinscode

[!include [banner](../includes/banner.md)]

Zinscodes enthalten Einstellungen, die festlegen, wann Zinsen erhoben werden und wie Zinsen für fällige Rechnungen berechnet werden.

Sie können einen einzelnen Zinscode einrichten und diesen auf mehrere Debitorenbuchungsprofile, Abrechnungscodes  oder auf bestimmte Rechnungspositionen anwenden. Wenn die Details des Zinscodes geändert werden, werden diese Änderungen für alle Funktionen, in denen dieser Code verwendet wird, automatisch bei neuen Buchungen übernommen. Für jeden Zinscode können Sie zwei Typen von Sätzen einrichten:
-   Sätze für Zinserträge − diese stellen Umsatzerlöse dar, die durch die Berechnung von Zinsen auf Rechnungen oder Zinsrechnungen erzielt werden.
-   Sätze für die Zinszahlungen − diese stellen Kosten dar, die für Zinsen auf Gutschriften bezahlt werden.

Beide Satztypen können im gleichen Zinscode gleichzeitig vorhanden ein. Zinssätze können auf drei Berechnungstypen basieren:
-   Zinsen nach Prozentsatz.
-   Zinsen nach Betrag.
-   Zinsen nach Bereich, was zu einem einzelnen Prozentsatz oder Betrag führt.

Bei der Berechnung der Zinsen mit einem Zinscode, wird für jeden Zinssatz, der für den Zeitraum gilt, in dem die Zahlung das Buchungsfälligkeitsdatum überschritten hat, eine separate Zinsrechnung erstellt. Verwenden Sie die **Einnahmen**-Registerkarte auf der **Zinscode**-Seite, um Zinssätze für Zinsen einzurichten, die Sie über Zinsen erzielen. Um Zinssätze für Zinsen einzurichten, die Sie zahlen, verwenden Sie stattdessen die Registerkarte **Zahlungen**.

## <a name="interest-rates-based-on-a-percentage"></a>Zinssätzen auf der Basis von Prozentsätzen
Sie können Zinssätze einrichten, die einen angegebenen Prozentsatz berechnen.

- Der Zinsbetrag gilt für alle Währungen.
- Es können optional Zinsbetraggrenzen eingegeben werden.
- Der **Prozentsatz** wird im Feld **Grundlage für Zinsberechnung** auf der Seite **Zinscodes einrichten** ausgewählt.

Um beispielsweise einen Zinscode einzurichten, der Zinsen in Höhe von 5 Prozent für alle 2 Monate festlegt die die Rechnungszahlung das Fälligkeitsdatum überschreitet, geben Sie 2 im Feld **Zinsen berechnen alle** ein wählen Sie **Monat** aus.

> [!NOTE] 
> Der neue Algorithmus zur Berechnung der Zinsrechnung wird mithilfe der Funktionsverwaltung hinzugefügt. Aktivieren Sie zur Verwendung dieses Algorithmus die Funktion **(GBL) Berechnung der Zinsen pro Tag als jährlichen Prozentsatz geteilt durch 365 zulassen**. Informationen zur Aktivierung der Funktionen finden Sie unter [Funktionsverwaltungsüberblick](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
> 
> Die Formel zur Berechnung des Zinsrechnungsbetrags lautet: 
>  
> Zinsrechnungsbetrag = geschuldeter Betrag * jährliche Zinsen % / 365 * Anzahl der verspäteten Tage
>  
> Diese Funktion ist ab Version 10.0.18 und höher verfügbar.    
 
## <a name="interest-rates-based-on-amounts"></a>Zinssätzen auf der Basis von Beträgen
Sie können Zinssätze einrichten, die einen angegebenen Betrag pro Währung berechnen.
- Für jede Währung wird im Zinscode ein Zinsbetrag angegeben.
- Es können optional Zinsbetraggrenzen eingegeben werden.
- Der **Betrag** wird im Feld **Grundlage für Zinsberechnung** auf der Seite **Einrichten von Zinscodes** ausgewählt.

Um beispielsweise einen Zinscode einzurichten, der Zinsen in Höhe von 25,00 für alle 20 Tage festlegt die die Rechnungszahlung das Fälligkeitsdatum überschreitet, geben Sie 20 im Feld **Zinsen berechnen alle** ein wählen Sie **Tag** aus.

## <a name="interest-rates-based-on-ranges"></a>Zinssätzen auf der Basis von Bereichen
Sie können Zinssätze einrichten, die je nach überfälligem Betrag, der Anzahl der Überfälligkeitstage oder der Anzahl der Überfälligkeitsmonate variieren.
-   Sie können die Registerkarte **Einnahmen nach Währung** verwenden, um bestimmte Zinseneinstellungen für jede Währung festlegen. Hier definieren Sie auch den Bereich.
-   Verwenden Sie die **Bereiche** Schaltfläche, um Positionen hinzuzufügen, die die Bereiche darstellen, die Sie einrichten möchten. Der **Von**-Wert stellt den Beginn des Zeitraums dar und die **Zinswert** repräsentiert entweder einen Prozentsatz oder einen Betrag, abhängig von der Auswahl im **Grundlage für Zinsberechnung**-Feld auf der **Einrichten von Zinscodes**-Seite.

## <a name="example-1-interest-by-range--amount"></a>Beispiel 1: Zinsen nach Bereich = Betrag
Sie richten einen Zinscode ein, der Zinsen einmal für alle drei Monate, um die die Rechnungszahlung das Fälligkeitsdatum übersteigt, festlegt. Sie möchten die Berechnung auf einem Prozentsatzzinsenwert basieren, gemäß bestimmten Betragsschritten. Der Zinsenwert beträgt 1 Prozent für Rechnungsbeträge bis 1.000,00, 2 Prozent für Beträge von 1.001,00 bis 5.000,00 und 3 Prozent für die Beträge, die größer 5.000,00 sind. Sie richten die Zinscodefeldwerte wie folgt ein.

| **Feldname**                  | **Feldwert** |
|---------------------------------|-----------------|
| **Zinscode**               | 3M%ByAmt        |
| **Zinsen berechnen alle**    | 3/Monat         |
| **Zinsen nach Bereich**           | Betrag          |
| **Grundlage für Zinsberechnung** | Prozentsatz      |

Sie richten die Bereichsinformationen wie folgt ein.

| **Von Wert** | **Zinswert** |
|----------------|--------------------|
| 0              | 1                  |
| 1,001          | 2                  |
| 5,001          | 3                  |


## <a name="example-2-interest-by-range--days"></a>Beispiel 2: Zinsen nach Bereich = Tage

Sie richten einen Zinscode ein, der Zinsen einmal für alle 15 Tage, um die die Rechnungszahlung das Fälligkeitsdatum übersteigt, festlegt. Sie möchten die Berechnung auf einem Zinsbetragswert basieren, gemäß bestimmten Tagesschritten. Der Zinsenwert ist 10,00 pro 15 Tage für die ersten 60 Tage, 15,00 pro 15 Tage für die Tage 61 bis 90 und 20,00 pro 15 Tagen nach Tag 91. Sie richten die Zinscodefeldwerte wie folgt ein.

| **Feldname**                  | **Feldwert** |
|---------------------------------|-----------------|
| **Zinscode**               | 15DAmtXDay      |
| **Zinsen berechnen alle**    | 15/Tag          |
| **Zinsen nach Bereich**           | Tage            |
| **Grundlage für Zinsberechnung** | Betrag          |

Sie richten die Bereichsinformationen wie folgt ein.

| **Von Wert** | **Zinswert** |
|----------------|--------------------|
| 0              | 10                 |
| 61             | 15                 |
| 91             | 20                 |


## <a name="example-3-interest-by-range--months"></a>Beispiel 3: Zinsen nach Bereich = Monate

Sie richten einen Zinscode ein, der Zinsen einmal für jeden Monat, um die die Rechnungszahlung das Fälligkeitsdatum übersteigt, festlegt. Sie möchten die Berechnung auf einem Prozentsatzzinsenwert basieren, gemäß bestimmten Monatsschritten. Der Zinsenwert beträgt 1,5 Prozent pro Monat für die ersten drei Monate Überfälligkeit, 2,0 Prozent pro Monat für die zweiten drei Monate und 2,5 Prozent pro Monat für jeden Monat nach den ersten sechs Monaten. Sie richten die Zinscodefeldwerte wie folgt ein.

| **Feldname**                  | **Feldwert** |
|---------------------------------|-----------------|
| **Zinscode**               | 1M%ByMth        |
| **Zinsen berechnen alle**    | 1/Monat         |
| **Zinsen nach Bereich**           | Monate          |
| **Grundlage für Zinsberechnung** | Prozentsatz      |

Sie richten die Bereichsinformationen wie folgt ein.

| **Von Wert** | **Zinswert** |
|----------------|--------------------|
| 0              | 1.5                |
| 4              | 2                  |
| 7              | 2,5                |

## <a name="new-versions"></a>Neue Versionen
Zinscodes sind ein Gültigkeitsdatum. Wenn Sie den Zinssatz ändern möchten, können Sie eine **neue Version** mit einem zukünftigen Gültigkeitsdatum erstellten.

Um die verschiedenen Versionen anzeigen, können Sie die Menüauswahl **Anfangsdatum.** verwenden, um das Abschnittsdatum auszuwählen. Sie können auch **Alle Datensätze anzeigen** auswählen, um alle Zinscodes auf der Seite anzuzeigen.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
