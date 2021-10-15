---
title: Planzahlenverrechnungsschlüssel vorhersagen
description: Dieses Thema enthält Beispiele, die zeigen, wie Sie einen Planzahlenverrechnungsschlüssel einrichten. Er umfasst Informationen zu den verschiedenen Einstellungen der Planzahlenverrechnungsschlüssel und deren Ergebnissen. Mithilfe von Planzahlenverrechnungsschlüsseln wird definiert, wie der Planungsbedarf verringert werden soll.
author: ChristianRytt
ms.date: 04/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqReduceKeyDefaultDataWizard, ReqReduceKey
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cbed77fd1abc0e4ae26e2b9ddcc01d3f4a84889f
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570824"
---
# <a name="forecast-reduction-keys"></a>Planzahlenverrechnungsschlüssel vorhersagen

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen zu den unterschiedlichen Methoden, die verwendet werden, um die Planungsanforderungen zu reduzieren. Es enthält Beispiele der Ergebnisse der einzelnen Methoden. Es wird auch erklärt, wie Planzahlenverrechnungsschlüsselerstellt, eingerichtet und verwendet werden. Einige Methoden nutzen einen Planzahlenverrechnungsschlüssel, um die Planungsanforderungen zu reduzieren.

## <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>Methoden, die zur Reduzierung der Planungsanforderungen verwendet werden

Wenn Sie eine Planung in einem Produktprogrammplan integrieren, können Sie auswählen, wie der Planungsbedarf verringert wird, wenn der tatsächliche Bedarf enthalten ist. Beachten Sie, dass die Masterplanung Prognoseanforderungen aus der Vergangenheit ausschließt, d.h. alle Prognoseanforderungen vor dem aktuellen Datum.

Wenn Sie eine Planung in einem Produktprogrammplan einschließen und die Methode auswählen die verwendet wird, um den Planungsbedarfe zu reduzieren, gehen Sie zu **Produktprogrammplanung \> Einstellungen \> Pläne \> Produktprogrammpläne**. Im Feld **Planzahlenmodell** wählen Sie Planzahlenmodell. Im Feld **Methode, die verwendet wird, um den Planungsbedarf zu reduzieren** wählen Sie eine Methode aus. Die folgenden Optionen sind verfügbar:

- Keiner
- Prozent – Planzahlenverrechnungsschlüssel
- Transaktionen – Planzahlenverrechnungsschlüssel
- Transaktionen – dynamische Periode

Die folgenden Abschnitte enthalten mehr Informationen zu den einzelnen Optionen.

### <a name="none"></a>Keiner

Wenn Sie **Keine** auswählen, wird der Planungsbedarf während des Produktprogrammplanungslaufs nicht verringert. In diesem Fall erstellt die Produktprogrammplanung geplante Bestellungen, um den geplanten Bedarf (Planungsbedarf) zu erfüllen. Diese Bestellvorschläge halten sich an die vorgeschlagene Menge, unabhängig von anderen Bedarfstypen. Wenn beispielsweise Aufträge platziert werden, erstellt die Produktprogrammplanung zusätzliche Bestellvorschläge, um die Aufträge zu erfüllen. Die Menge des Planungsbedarf wird nicht verringert.

### <a name="percent--reduction-key"></a>Prozent – Planzahlenverrechnungsschlüssel

Wenn Sie **Prozent - Planzahlenverrechnungsschlüssel** auswählen, wird die Prognoseanforderung verringert, und zwar gemäß den vom Planzahlenverrechnungsschlüssel definierten Prozentsätzen und Perioden. In diesem Fall erstellt die Produktprogrammplanung Bestellvorschläge, bei denen die Menge in jeder Periode als geplante Menge × Planzahlenverrechnungsschlüssel berechnet wird. Wenn andere Bedarfstypen vorhanden sind, erstellt die Produktprogrammplanung Bestellvorschläge, um den Bedarf zu liefern.

#### <a name="example-percent--reduction-key"></a>Beispiel: Prozent – Planzahlenverrechnungsschlüssel

Dieses Beispiel verdeutlicht, wie ein Planzahlenverrechnungsschlüssel den Bedarf der Bedarfsplanung verringert, und zwar gemäß den vom Planzahlenverrechnungsschlüssel definierten Prozentsätzen und Perioden.

Bei diesem Beispiel integrieren Sie die folgende Bedarfsplanung in einem Produktprogrammplan.

| Monat    | Bedarfsplanung |
|----------|-----------------|
| Januar  | 1.000           |
| Februar | 1.000           |
| März    | 1.000           |
| April    | 1.000           |

Wählen Sie auf der Seite **Planzahlenverrechnungsschlüssel** die folgenden Positionen.

| Änderung | Einheit  | Prozentsatz |
|--------|-------|---------|
| 1      | Monat | 100     |
| 2      | Monat | 75      |
| 3      | Monat | 50      |
| 4      | Monat | 25      |

Sie weisen den Planzahlenverrechnungsschlüssel der Deckungsgruppe des Artikels zu. Auf der Seite **Produktprogrammpläne** im Feld **Verwendete Methode, um den Planungsbedarfe zu reduzieren** wählen Sie **Prozent - Planzahlenverrechnungsschlüssel** aus.

Wenn Sie die Umsatzplanungslauf am 1. Januar ausführen, wird die Bedarfsplanung entsprechend den Prozentwerten verbraucht, die Sie auf der Seite **Planzahlenverrechnungsschlüssel** angegeben haben. Die folgenden Bedarfsmengen werden in den Produktprogrammplan übertragen.

| Monat                | Geplante Bestellmenge. | Herstellkostenkalkulation    |
|----------------------|------------------------|----------------|
| Januar              | 0                      | = 0% × 1,000   |
| Februar             | 250                    | = 25% × 1,000  |
| März                | 500                    | = 50% × 1,000  |
| April                | 750                    | = 75% × 1,000  |
| Mai - Dezember | 1.000                  | = 100% × 1,000 |

### <a name="transactions--reduction-key"></a>Transaktionen – Planzahlenverrechnungsschlüssel

Wenn Sie das Feld **Methode zur Reduzierung des Planungsbedarfs** auf *Buchungen – Planzahlenverrechnungsschlüssel* festlegen, werden die Planungsbedarfe um die qualifizierten Bedarfsbuchungen reduziert, die in den durch den Planzahlenverrechnungsschlüssel definierten Zeiträumen anfallen.

Der qualifizierte Bedarf wird durch das Feld **Planungswert verringern um** auf der Seite **Dispositionssteuerungsgruppen** definiert. Wenn Sie das Feld **Planungswert verringern um** auf *Aufträge* festlegen, werden nur Auftragsbuchungen als qualifizierter Bedarf betrachtet. Wenn Sie es auf *Alle Buchungen* festlegen, werden alle abgehenden Nicht-Intercompany-Bestandsbuchungen als qualifizierter Bedarf betrachtet. Falls Intercompany-Aufträge ebenfalls als qualifizierter Bedarf berücksichtigt werden sollen, legen Sie die Option **Intercompany-Aufträge einschließen** auf *Ja* fest.

Die Prognoseverrechnung beginnt mit dem ersten (frühesten) Bedarfsplanungsdatensatz im Planzahlenverrechnungsschlüssel-Zeitraum. Wenn die Menge der qualifizierten Bestandsbuchungen größer ist als die Menge der Bedarfsplanungspositionen im selben Planzahlenverrechnungsschlüssel-Zeitraum, wird der Saldo der Bestandsbuchungsmenge verwendet, um die Bedarfsplanungsmenge im vorherigen Zeitraum zu reduzieren (sofern nicht verbrauchte Planungsmengen vorhanden sind).

Wenn im vorherigen Planzahlenverrechnungsschlüssel-Zeitraum keine nicht verbrauchten Planungsmengen verbleiben, wird der Saldo der Bestandsbuchungsmenge verwendet, um die Planungsmenge im nächsten Monat zu reduzieren (sofern nicht verbrauchte Planungsmengen vorhanden sind).

Der Wert im Feld **Prozent** in den Planzahlenverrechnungsschlüssel-Positionen wird nicht verwendet, wenn das Feld **Methode zur Reduzierung des Planungsbedarfs** auf *Buchungen – Planzahlenverrechnungsschlüssel* festgelegt ist. Nur die Daten werden verwendet, um den Planzahlenverrechnungsschlüssel-Zeitraum zu definieren.

> [!NOTE]
> Alle Planungen, die am oder vor dem heutigen Datum gebucht werden, werden ignoriert und nicht zum Erstellen von Planaufträgen verwendet. Wenn Ihre Bedarfsplanung für den Monat beispielsweise am 1. Januar generiert wird und Sie eine Masterplanung mit Bedarfsplanung am 2. Januar ausführen, ignoriert die Berechnung die Bedarfsplanungsposition vom 1. Januar.

#### <a name="example-transactions--reduction-key"></a>Beispiel: Transaktionen – Planzahlenverrechnungsschlüssel

Dieses Beispiel verdeutlicht, wie tatsächliche Aufträge, die in den vom Planzahlenverrechnungsschlüssel definierten Perioden anfallen, den Bedarf der Bedarfsplanung verringern.

Für dieses Beispiel wählen Sie auf der Seite **Produktprogrammpläne** im Feld **Verwendete Methode, um den Planungsbedarfe zu reduzieren** **Transaktion - Planzahlenverrechnungsschlüssel** aus.

Am 1. Januar lagen die folgenden Aufträge vor.

| Monat    | Bestellte Stückzahl |
|----------|--------------------------|
| Januar  | 956                      |
| Februar | 1.176                    |
| März    | 451                      |
| April    | 119                      |

Wenn Sie die selbe Bedarfsplanung von 1000 Stück pro Monat verwenden, die im vorherigen Beispiel verwendet wurde, werden die folgenden Bedarfsmengen in den Produktprogrammplan übertragen.

| Monat                | Erforderliche Stückzahl |
|----------------------|---------------------------|
| Januar              | 44                        |
| Februar             | 0                         |
| März                | 549                       |
| April                | 881                       |
| Mai - Dezember | 1.000                     |

### <a name="transactions--dynamic-period"></a>Transaktionen – dynamische Periode

Wenn Sie **Transaktion - dynamische Periode** auswählen, wird der Planungsbedarf durch die tatsächlichen Auftragsbuchungen verringert, die während der dynamischen Periode stattfinden. Die dynamische Periode erstreckt sich über die aktuellen Planungsdaten und endet beim Beginn der nächsten Planung. In diesem Fall erstellt die Produktprogrammplanung geplante Bestellungen, um den geplanten Bedarf (Planungsbedarf) zu erfüllen. Wenn die tatsächlichen Auftragstransaktionen erteilt werden, werden die Planungsbedarfe reduziert. Die tatsächlichen Transaktionen verbrauchen Teil des Planungsbedarfs.

Wenn diese Option verwendet wird, tritt das folgende Verhalten auf:

- Planzahlenverrechnungsschlüssel sind nicht erforderlich oder werde nicht verwendet. 
- Wenn die Planung vollständig verringert wird, wird der Planungsbedarf für die aktuelle Planung 0 (null).
- Wenn keine zukünftige Planung vorhanden ist, wird der Planungsbedarf der letzten eingegebenen Planung verringert.
- Planungszeiträume sind in der Berechnung der Planungsverringerung enthalten.
- Positive Tage sind in der Berechnung der Planungsverringerung enthalten.
- Wenn die tatsächlichen Auftragsbuchungen größer sind als der geplante Bedarf, werden die verbleibenden Buchungen nicht in die nächste Planungsperiode vorgetragen.

#### <a name="example-1-transactions--dynamic-period"></a>Beispiel 1: Transaktion – dynamische Periode

Hier ein einfaches Beispiel, das anzeigt, wie die Methode **Transaktionen - dynamische Periode** funktioniert.

Bei diesem Beispiel integrieren Sie die folgende Bedarfsplanung in einem Produktprogrammplan.

| Datum       | Bedarfsplanung |
|------------|-----------------|
| 1. Januar  | 1.000           |
| Februar 1 | 1.000             |

Sie erstellen auch die folgenden Aufträge.

| Datum        | Auftragsmenge |
|-------------|----------------------|
| 15. Januar  | 200                  |
| Februar 15 | 400                  |

In diesem Fall werden die folgenden Aufträge erstellt.

| Bedarfsplanungsdatum | Leistung | Erläuterung                           |
|--------------------- |----------|---------------------------------------|
| 1. Januar            | 800      | Planungsanforderungen verringern (= 1,000 – 200) |
| 15. Januar           | 200      | Auftragsanforderungen             |
| Februar 1           | 600      | Planungsanforderungen verringern (= 1,000 – 400) |
| Februar 15          | 400      | Auftragsanforderungen             |

#### <a name="example-2-transactions--dynamic-period"></a>Beispiel 2: Transaktion – dynamische Periode

In den meisten Fällen werden Systeme so eingerichtet, das Transaktionen die Bedarfsplanung innerhalb bestimmter Prognoseperioden reduzieren: Wochen, Monate usw. Die Perioden werden im Planzahlenverrechnungsschlüssel definiert. Jedoch können die Zeit zwischen zwei Bedarfsplanungspositionen auch eine Periode *implizieren*.

In diesem Beispiel erstellen Sie eine Bedarfsplanung für die folgenden Datumsangaben und Mengen.

| Datum       | Bedarfsplanung |
|------------|-----------------|
| 1. Januar  | 1.000           |
| 5. Januar  | 500             |
| 12. Januar | 1.000           |

Beachten Sie, dass es in dieser Planung keine klare Periode zwischen den Planungsdatumsangaben gibt. Zwischen dem ersten und dem zweiten Datum besteht eine viertägige Spanne und zwischen dem zweiten und dem dritten Datum liegt eine siebentägige Spanne. Diese Zeitspannen sind die dynamischen Perioden.

Sie erstellen auch die folgenden Auftragspositionen.

| Datum                             | Auftragsmenge |
|----------------------------------|----------------------|
| 15. Dezember Im Jahr zuvor | 500                  |
| 3. Januar                        | 100                  |
| 10. Januar                       | 200                  |

In diesem Fall wird die Planung auf folgende Weise reduziert:

- Weil der erste Auftrag nicht innerhalb einer Periode liegt, wird die Planung nicht reduziert.
- Weil der zweite Auftrag liegt zwischen dem 1. Januar und dem 5. Januar liegt, wird die Planung für den 1. Januar um 100 reduziert.
- Weil der dritte Auftrag zwischen dem 5. Januar und dem 12. Januar liegt, wird die Planung für den 5. Januar um 200 reduziert.

Deshalb werden die folgenden Aufträge erstellt.

| Bedarfsplanungsdatum             | Leistung | Erläuterung                                                         |
|----------------------------------|----------|---------------------------------------------------------------------|
| 15. Dezember Im Jahr zuvor | 500      | Auftragsanforderungen                                            |
| 1. Januar                        | 900      | Planungsbedarfperiode vom 1. Januar bis zum 5. Januar (= 1.000 - 100 ) |
| 3. Januar                        | 100      | Auftragsanforderungen                                            |
| 5. Januar                        | 300      | Planungsbedarfperiode vom 5. Januar bis zum 10. Januar (= 500 - 200 )  |
| 12. Januar                       | 1.000    | Planungsbedarfperiode vom 12. Januar bis zum Ende                      |

## <a name="create-and-set-up-a-forecast-reduction-key"></a>Erstellen und Einrichten eines Planzahlenverrechnungsschlüssels

Ein Planungsverrechnungsschlüssel wird in den Formularen **Transaktionen - Planzahlenverrechnungsschlüssel** und **Prozentplanzahlenverrechnungsschlüssel**-Methoden zum Reduzieren des Planungsbedarfes verwendet. Gehen Sie folgendermaßen vor, um einen Planzahlenverrechnungsschlüssel zu erstellen und einzurichten.

1. Gehen Sie zu **Produktprogrammplanung \> Einstellungen \> Abdeckung \> Planzahlenverrechnungsschlüssel**.
2. Wählen Sie **Neu**, um einen Reduzierungsschlüssel zu erstellen.
3. Im Feld **Planzahlenverrechnungsschlüssel** geben Sie eine eindeutige Kennung für den Planzahlenverrechnungsschlüssel ein. Geben Sie im Feld  **Namen** einen Namen ein. 
4. Hier können Sie die Perioden sowie die Planzahlenverrechnungsschlüsselprozentsatz in jeder Periode eingeben:

    - Das Feld **Gültigkeitsdatum** gibt das Datum der Erstellung der Periode an. Wenn die Option **Gültigkeitsdatum verwenden** auf **Ja** gesetzt ist, beginnt die Periode am Gültigkeitsdatum. Wenn Sie auf **Nein** festgelegt ist, beginnt der Periodenanfang an dem Tag, an dem die Produktprogrammplanung ausgeführt wird.
    - Hier können Sie die Perioden definieren, in denen die geplante Planzahlenverrechnung ausgeführt werden soll.
    - Während einer bestimmten Periode geben Sie den Prozentsatz ein, um den der Planungsbedarf reduziert werden soll. Bei einem positiven Wert wird der Bedarf verringert, bei einem negativen Wert wird er erhöht.

## <a name="use-a-reduction-key"></a>Verwenden eines Planzahlenverrechnungsschlüssels

Ein Planzahlenverrechnungsschlüssel muss der Deckungsgruppe des Artikels zugewiesen werden. Gehen Sie folgendermaßen vor, um einen Planzahlenverrechnungsschlüssels eines Artikels der Dispositionssteuerungsgruppe zuzuweisen.

1. Gehen Sie zu **Produktprogrammplanung \> Einstellungen \> Planungshorizont \> Dispositionssteuerungsgruppen**
2. Wählen Sie im Feld **Planzahlenverrechnungsschlüssel** auf der Registerkarte **Andere** den Planzahlenverrechnungsschlüssel aus, der der Deckungsgruppe zugewiesen werden soll. Der Planzahlenverrechnungsschlüssel gilt dann für die Artikel, die zur Deckungsgruppe gehören.
3. Wenn der Planzahlenverrechnungsschlüsse eine Reduktion während der Produktprogrammplanung verwendet werden soll, müssen Sie diese Einstellungen in der Absatzplanung oder in den Einstellungen der Produktprogrammplanung definieren. Gehen Sie zu den folgenden Standorten:

    - Produktprogrammpläne \>Einstellungen \>Pläne \> Absatzplanungen
    - Produktprogrammplanung \> Einstellungen \> Pläne \> Produktprogrammpläne

4. Auf der Seite **Absatzpläne** oder **Produktprogrammpläne** auf dem Inforegister **Allgemeine** im Feld **Methode, um die Planungsbedarfe zu reduzieren**, wählen Sie entweder **Prozent - Planzahlenverrechnungsschlüssel** oder **Transaktionen - Planzahlenverrechnungsschlüssel** aus.

## <a name="reduce-a-forecast-by-transactions"></a>Reduzieren einer Planung durch Transaktionen

Wenn Sie **Transaktionen - Planzahlenverrechnungsschlüssel** oder **Transaktioen - dynamische Periode** als Methode für das Reduzieren von Planungsbedarfen aktivieren, können Sie angeben, welche Transaktionen die Planung verringert. Wählen Sie auf der Seite **Dispositionssteuerungsgruppe** im Inforegister **Sonstiges** für das Feld **Planungswert verringern um** die Option **Alle Transaktionen** aus, wenn alle Transaktionen die Planung reduzieren sollen, oder die Option **Aufträge**, wenn nur Aufträge die Planung reduzieren sollen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Hauptpläne – Übersicht](master-plans.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
