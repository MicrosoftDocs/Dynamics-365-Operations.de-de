---
title: Abschreibung des Nutzungsrechts am Leasingobjekt erfassen (Vorschau)
description: In diesem Artikel wird erläutert, wie Sie den Journaleintrag für die Amortisierung erstellen, die für Mietverträge erforderlich ist, die in der Bilanz eines Unternehmens erfasst werden.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseAssetSchedule
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 93e521cf409af4c01d625f27bdd7a7564e471bd9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903275"
---
# <a name="record-right-of-use-asset-depreciation-preview"></a>Abschreibung des Nutzungsrechts am Leasingobjekt erfassen (Vorschau)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Bei Mietverträgen, die in der Bilanz eines Unternehmens erfasst werden, wird das Nutzungsrecht am Leasingobjekt monatlich abgeschrieben. In diesem Artikel wird erläutert, wie Sie den Journaleintrag für die Amortisierung erstellen. Die Amortisierung belastet das Ausgabensachkonto und schreibt das kumulierte Abschreibungssachkonto gut, basierend auf der Einrichtung Ihres Buchungsprofils und der Mietvertragsart. Diese Einträge können für jeden Mietvertrag oder für mehrere Mietverträge mithilfe der Batch-Erfassungsfunktion erstellt werden.

## <a name="asset-depreciation-schedule"></a>Anlagenabschreibungszeitplan

1. Auf der **Mietvertragsübersicht**-Seite wählen Sie einen Mietvertrag. Dann wählen Sie **Bücher \> Abschreibungsplan für Anlagen**, um die **Abschreibungsplan für Anlagen**-Seite zu öffnen.

    Der Journaleintrag für den Abschreibungsaufwand für das Nutzungsrecht am Leasingobjekt basiert auf dem Betrag in der **Abschreibungen**-Spalte. Ein Beispiel für die Richtlinien zur Einhaltung von Rechnungslegungsstandards finden Sie im Abschnitt [Berechnung des Amortisierungsaufwands für das Nutzungsrecht am Leasingobjekt für Finanzierungsleasing](#calculation-of-rou-asset-amortization-expense-for-finance-leases) später in diesem Artikel.
    
2. Wählen Sie den Abschreibungszeitraum aus und wählen Sie dann **Erfassung erstellen**. Sie erhalten eine Nachricht, die besagt, dass die Erfassung erstellt wurde, in dem die Abschreibung erfasst wird.
3. Wählen Sie **Erfassungen \> Anlagenleasingerfassungen**, um die **Anlagenleasingerfassung**-Seite zu öffnen, auf der Sie den erstellten Abschreibungskostenjournaleintrag anzeigen können.

   Das System sperrt bestimmte Finanzfelder für die Bearbeitung, um Abweichungen zwischen den Transaktionen und den Zeitplänen zu verhindern. Einige Felder, die gesperrt sind, sind: **Konto**, **Beträge**, **Finanzielle Dimensionen**, **Währung** und **Transaktionstyp**. Außerdem können Sie in den Journaleinträgen des Anlagenleasings keine Zeilen für Journaleinträge hinzufügen oder löschen, da dies zu Abweichungen zwischen den Zeitplänen und den Transaktionen führen kann.

4. Wählen Sie den Journaleintrag aus und wählen Sie dann **Buchen**, um den Abschreibungseintrag im Hauptbuch zu erfassen.

## <a name="calculation-of-rou-asset-amortization-expense-for-operating-leases"></a>Berechnung des Amortisierungsaufwands für das Nutzungsrecht am Leasingobjekt für Ausrüstungs-Leasingverträge

Der Abschreibungsaufwand eines Ausrüstungs-Leasingvertrags wird als Differenz zwischen dem monatlichen linearen Leasingaufwand und dem monatlichen Zinsaufwand für die Leasingverbindlichkeit gemäß dem Themas 842 zur Kodifizierung von Rechnungslegungsstandards (ASC 842) berechnet, das der Standard der Allgemein anerkannten Rechnungslegungsgrundsätze in den USA (US GAAP) ist. Der lineare Mietaufwand wird als die Summe aller Mietzahlungen geteilt durch die Mietdauer in Monaten berechnet. (Die Summe der Mietzahlungen umfasst Vorauszahlungen, anfängliche direkte Kosten, Demontagekosten und Mietanreize.) Die folgende Tabelle zeigt ein Beispiel für den Amortisierungsaufwand für einen Ausrüstungs-Leasingvertrag.

### <a name="example-of-rou-asset-amortization-expense-for-operating-leases"></a>Beispiel eines Amortisierungsaufwands für das Nutzungsrecht am Leasingobjekt für Ausrüstungs-Leasingverträge

| Feld                                          | Wert       |
|------------------------------------------------|-------------|
| Zahlungsbetrag                                 | 1.000       |
| Zahlungshäufigkeit                              | Monatlich     |
| Mietdauer (Monate)                            | 24          |
| Gesamte Mietzahlungen                           | 24,000      |
| Zinssatz für Neukredit                     | 5 %          |
| Annuitätstyp                                   | Fällige Annuität |
| Aufzinsungsintervall                           | Monatlich     |
| Barwert zukünftiger Mindestmietzahlungen | 22,888.87   |

Wie zuvor erwähnt wird der lineare Mietaufwand als die Summe aller Mietzahlungen geteilt durch die Mietdauer in Monaten berechnet. Das System berechnet automatisch den monatlichen Zinsaufwand für den Tilgungsplan. Der Zinsaufwand wird nach der Effektivzinsmethode berechnet. Das System verwendet die linearen Mietkosten, um den Zinsaufwand für jeden Monat abzuziehen. Der Wert wird verwendet, um das Nutzungsrecht am Leasingobjekt zu reduzieren.

| Monat | Lineare Mietverträge | Zinsausgaben                        | Berechnung des Amortisierungsaufwands für das Nutzungsrecht am Leasingobjekt |
|-------|--------------------------|-----------------------------------------|-----------------------------------------------|
| 1     | (24.000 ÷ 24) = 1.000,00 | (22.888,87 – 1.000) × (5 % ÷ 12) = 91,20 | 1.000 – 91,20 = 908,80                        |
| 2     | (24.000 ÷ 24) = 1.000,00 | (21.980,08 – 1.000) × (5 % ÷ 12) = 87,42 | 1.000 – 87,42 = 912,58                        |
| 3     | (24.000 ÷ 24) = 1.000,00 | (21.067,49 – 1.000) × (5 % ÷ 12) = 83,62 | 1.000 – 83,62 = 916,39                        |

> [!NOTE]
> Gemäß ASC 842 wird die Abschreibung des Nutzungsrechts am Leasingobjekt für einen Ausrüstungs-Leasingvertrag in der Gewinn- und Verlustrechnung als Leasingaufwand ausgewiesen. Aus Gründen der Sichtbarkeit beschreibt das Anlagenleasing den Eintrag als Abschreibung des Nutzungsrechts am Leasingobjekt. Die Belastungsbuchung sollte jedoch einem Aufwandskonto für Ausrüstungs-Leasingverträge zugeordnet werden, und die Gutschriftbuchung sollte direkt dem Nutzungsrecht am Leasingobjekt für das Ausrüstungs-Leasingvertrag zugeordnet werden. In den Mietvertragsparametern können Sie jedoch festlegen, dass Gutschriften auf einem kumulierten Abschreibungskonto für das Nutzungsrecht am Leasingobjekt für Ausrüstung vorgenommen werden sollen.

Ist das Leasingverhältnis als Operating-Leasingverhältnis klassifiziert, wird die monatliche Abschreibung nach Wertminderung nach der linearen Abschreibung berechnet.

## <a name="calculation-of-rou-asset-amortization-expense-for-finance-leases"></a>Berechnung des Amortisierungsaufwands für das Nutzungsrecht am Leasingobjekt für Finanzierungs-Leasing

Für Mietverträge mit einer Finanzklassifizierung berechnet das System die Abschreibung des Nutzungsrechts am Leasingobjekt linear. Daher ist der Abschreibungsaufwand für jeden Monat gleich.

Gemäß dem International Financial Reporting Standard 16 (IFRS 16) und ASC 842 wird der Vermögenswert entweder über die Laufzeit des Mietvertrags oder über die Nutzungsdauer des Leasingobjekts abgeschrieben, je nachdem, welcher Wert geringer ist. Zusätzlich gilt, wenn der **Eigentumsübergang**-Parameter für der Mietvertrag aktiviert ist, wird der Mietvertrag automatisch über die Nutzungsdauer des Leasingobjekts abgeschrieben.

### <a name="example-of-rou-asset-amortization-expense-for-finance-leases"></a>Beispiel eines Amortisierungsaufwands für das Nutzungsrecht am Leasingobjekt für Finanzierungs-Leasing

| Feld                                | Wert                                   |
|--------------------------------------|-----------------------------------------|
| Abschreibung des Nutzungsrechts am Leasingobjekt beginnen | 22,889.87                               |
| Mietdauer (Monate)                  | 24                                      |
| Nutzungsdauer für Anlagen (Monate)           | 36                                      |
| Monat                                | Amortisierungsaufwand für das Nutzungsrecht am Leasingobjekt |
| 1                                    | 22.889,87 ÷ 24 = 953,74                 |
| 2                                    | 22.889,87 ÷ 24 = 953,74                 |
| 3                                    | 22.889,87 ÷ 24 = 953,74                 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
