---
title: Produktprogrammplanung mit Bedarfsprognosen
description: In diesem Thema wird erklärt, wie Sie Bedarfsplanungen bei der Produktprogrammplanung mit der Planungsoptimierung einbeziehen können.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: cb696c365e02ab3e3b28da19b8b33f1975c142f8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983543"
---
# <a name="master-planning-with-demand-forecasts"></a>Produktprogrammplanung mit Bedarfsprognosen

[!include [banner](../../includes/banner.md)]

Sie können eine Bedarfsplanung zusammen mit der Planungsoptimierung verwenden, um den erwarteten Bedarf in Ihrer Produktprogrammplanung zu berücksichtigen. Sie können eine Bedarfsprognose manuell erstellen, importieren oder mit Hilfe der Bedarfsprognosefunktion in Microsoft Dynamics 365 Supply Chain Management generieren. Weitere Informationen zur Bedarfsplanung finden Sie unter [Übersicht zur Bedarfsprognose](../introduction-demand-forecasting.md).

> [!NOTE]
> Eine separate Prognoseplanung wird bei der Planungsoptimierung nicht unterstützt. Daher hat die Einstellung **Aktueller Prognoseplan** auf der Seite **Masterplanungsparameter** keine Wirkung, wenn Sie die Planungsoptimierung verwenden.

## <a name="set-up-a-master-plan-to-include-a-demand-forecast"></a>Einen Masterplan so festlegen, dass er eine Bedarfsplanung enthält

Um einen Masterplan so zu konfigurieren, dass er eine Bedarfsplanung enthält, gehen Sie wie folgt vor.

1. Wechseln Sie zu **Produktprogrammplanung \> Einrichtung \> Pläne \> Produktprogrammpläne**.
1. Wählen Sie einen bestehenden Plan aus, oder erstellen Sie einen neuen Plan.
1. Legen Sie im Inforegister **Allgemein** die folgenden Felder fest:

    - **Prognosemodell** - Wählen Sie das zu verwendende Prognosemodell. Dieses Modell wird berücksichtigt, wenn ein Versorgungsvorschlag für den aktuellen Masterplan erstellt wird.
    - **Bedarfsprognose einbeziehen** - Legen Sie diese Option auf *Ja* fest, um die Bedarfsplanung in den aktuellen Masterplan einzubeziehen. Wenn Sie sie auf *Nein* festlegen, werden die Transaktionen der Bedarfsplanung nicht in den Masterplan aufgenommen.
    - **Methode zur Reduzierung des Prognosebedarfs** - Wählen Sie die Methode, die zur Reduzierung des Prognosebedarfs verwendet werden soll. Weitere Informationen finden Sie im Abschnitt [Schlüssel zur Prognosereduzierung](#reduction-keys) weiter unten in diesem Thema.

1. Auf dem Inforegister **Zeitrahmen in Tagen** können Sie die folgenden Felder festlegen, um den Zeitraum festzulegen, in dem die Bedarfsplanung berücksichtigt wird:

    - **Prognoseplan** - Legen Sie diese Option auf *Ja* fest, um den Prognoseplan-Zeitzaun, der von den einzelnen Deckungsgruppen ausgeht, außer Kraft zu setzen. Legen Sie sie auf *Nein* fest, um die Werte aus den einzelnen Coverage-Gruppen für den aktuellen Masterplan zu verwenden.
    - **Prognosezeitraum** - Wenn Sie die Option **Prognoseplan** auf *Ja* festlegen, geben Sie die Anzahl der Tage (ab dem heutigen Datum) an, für die die Bedarfsplanung gelten soll.

    > [!IMPORTANT]
    > Die Einstellung **Prognoseplan** wird bei der Planungsoptimierung noch nicht unterstützt.

## <a name="set-up-a-coverage-group-to-include-a-demand-forecast"></a>Festlegen einer Abdeckungsgruppe zur Einbeziehung einer Bedarfsplanung

Um eine Deckungsgruppe so zu konfigurieren, dass sie eine Bedarfsplanung enthält, gehen Sie wie folgt vor.

1. Gehen Sie zu **Produktprogrammplanung \> Einrichten \> Pläne \> Abdeckungsgruppen**.
1. Wählen Sie eine vorhandene Deckungsgruppe aus, oder erstellen Sie eine neue Gruppe.
1. Legen Sie auf dem Inforegister **Sonstiges** die folgenden Felder fest:

    - **Zeitraum für die Absatzplanung** - Geben Sie die Anzahl der Tage (ab dem heutigen Datum) ein, für die die Bedarfsplanung gelten soll. Dieser Wert kann mit der Option **Vorhersageplan** auf dem Masterplan überschrieben werden, wie im vorherigen Abschnitt beschrieben.
    - **Reduktionsschlüssel** - Wählen Sie den Reduktionsschlüssel, der angewendet werden soll. Weitere Informationen finden Sie in den Abschnitten [Erstellen und Festlegen eines Prognosereduktionsschlüssels](#create-reduction-key) und [Verwenden eines Reduktionsschlüssels](#use-reduction-key) weiter unten in diesem Thema.
    - **Prognose reduzieren um** - Für Produktprogrammplanungen, bei denen das Feld **Methode zur Reduzierung des Prognosebedarfs** auf *Transaktionen - Reduzierungsschlüssel* oder *Transaktionen - dynamischer Zeitraum* festgelegt ist, geben Sie an, welche Transaktionen die Prognose reduzieren sollen. Wählen Sie einen der folgenden Werte aus:

        - **Alle Transaktionen** - Alle Transaktionen sollen die Prognose reduzieren.
        - **Aufträge** - Nur Verkaufsaufträge sollen die Prognose reduzieren.

        > [!NOTE]
        > Wenn Sie *Alle Transaktionen* wählen, werden Transaktionen, die sowohl Bedarf als auch Angebot in derselben Bestandsdimension haben, als neutral betrachtet und bei der Prognosereduzierung ignoriert. Wenn die Planungsdimension z. B. nur auf Standort und nicht auf Lagerort festgelegt ist, wird ein Transportauftrag zwischen Standort 1, Lagerort 11, und Standort 1, Lagerort 13, ignoriert und reduziert die verbleibende Bedarfsplanung nicht.

    - **Intercompany-Bestellungen einschließen** - Legen Sie diese Option auf *Ja* fest, wenn Intercompany-Bestellungen bei der Reduzierung der Prognose berücksichtigt werden sollen. Andernfalls legen Sie sie auf *Nein* fest.
    - **Kundenprognose in die Bedarfsplanung einbeziehen** - Geben Sie an, ob eine Kundenprognose in die Gesamtprognose einbezogen werden soll. Diese Option bestimmt, wie die tatsächliche Nachfrage die prognostizierte Nachfrage reduziert. Sie können sie verwenden, um sicherzustellen, dass die Produktprogrammplanung die Lieferung von Elementen abdeckt, die von bestimmten Kunden gekauft werden.

        - Legen Sie diese Option auf *Ja* fest, um eine Kundenprognose in die Gesamtprognose aufzunehmen. In diesem Fall reduziert die tatsächliche Kundennachfrage sowohl die Kundenprognose als auch die Gesamtprognose. Die Produktprogrammplanung erzeugt Planaufträge, die nur die Gesamtprognosemenge abdecken.
        - Legen Sie diese Option auf *Nein* fest, wenn Sie eine Kundenprognose nicht in die Gesamtprognose einbeziehen wollen. In diesem Fall reduziert der tatsächliche Kundenbedarf nur die Kundenprognose. Die Produktprogrammplanung erzeugt Planaufträge, um sowohl die Gesamtprognosemenge als auch die Prognose für jede Kundenmenge abzudecken.

## <a name="forecast-reduction-keys"></a><a name="reduction-keys"></a>Planzahlenverrechnungsschlüssel vorhersagen

In diesem Abschnitt finden Sie Informationen zu den verschiedenen Methoden, die zur Reduzierung des Prognosebedarfs verwendet werden. Es enthält Beispiele der Ergebnisse der einzelnen Methoden. Es wird auch erklärt, wie Planzahlenverrechnungsschlüsselerstellt, eingerichtet und verwendet werden. Einige Methoden nutzen einen Planzahlenverrechnungsschlüssel, um die Planungsanforderungen zu reduzieren.

### <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>Methoden, die zur Reduzierung der Planungsanforderungen verwendet werden

Wenn Sie eine Planung in einem Produktprogrammplan integrieren, können Sie auswählen, wie der Planungsbedarf verringert wird, wenn der tatsächliche Bedarf enthalten ist. Beachten Sie, dass die Masterplanung Prognoseanforderungen aus der Vergangenheit ausschließt, d.h. alle Prognoseanforderungen vor dem aktuellen Datum.

Wenn Sie eine Planung in einem Produktprogrammplan einschließen und die Methode auswählen die verwendet wird, um den Planungsbedarfe zu reduzieren, gehen Sie zu **Produktprogrammplanung \> Einstellungen \> Pläne \> Produktprogrammpläne**. Im Feld **Planzahlenmodell** wählen Sie Planzahlenmodell. Im Feld **Methode, die verwendet wird, um den Planungsbedarf zu reduzieren** wählen Sie eine Methode aus. Die folgenden Optionen stehen zur Verfügung:

- Keines
- Prozent – Planzahlenverrechnungsschlüssel
- Vorgänge - Reduzierungsschlüssel (noch nicht mit Planungsoptimierung unterstützt)
- Transaktionen – dynamische Periode

Die folgenden Abschnitte enthalten mehr Informationen zu den einzelnen Optionen.

#### <a name="none"></a>Keiner

Wenn Sie **Keine** auswählen, wird der Planungsbedarf während des Produktprogrammplanungslaufs nicht verringert. In diesem Fall erstellt die Produktprogrammplanung geplante Bestellungen, um den geplanten Bedarf (Planungsbedarf) zu erfüllen. Diese Bestellvorschläge halten sich an die vorgeschlagene Menge, unabhängig von anderen Bedarfstypen. Wenn beispielsweise Aufträge platziert werden, erstellt die Produktprogrammplanung zusätzliche Bestellvorschläge, um die Aufträge zu erfüllen. Die Menge des Planungsbedarf wird nicht verringert.

#### <a name="percent--reduction-key"></a>Prozent – Planzahlenverrechnungsschlüssel

Wenn Sie **Prozent - Planzahlenverrechnungsschlüssel** auswählen, wird die Prognoseanforderung verringert, und zwar gemäß den vom Planzahlenverrechnungsschlüssel definierten Prozentsätzen und Perioden. In diesem Fall erstellt die Produktprogrammplanung Bestellvorschläge, bei denen die Menge in jeder Periode als geplante Menge × Planzahlenverrechnungsschlüssel berechnet wird. Wenn andere Bedarfstypen vorhanden sind, erstellt die Produktprogrammplanung Bestellvorschläge, um den Bedarf zu liefern.

##### <a name="example-percent--reduction-key"></a>Beispiel: Prozent – Planzahlenverrechnungsschlüssel

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

#### <a name="transactions--reduction-key"></a>Transaktionen – Planzahlenverrechnungsschlüssel

Wenn Sie **Transaktionen - Planzahlenverrechnungsschlüssel** wählen wird der Planungsbedarf um die Transaktion reduziert, die während der im Planzahlenverrechnungsschlüssel definierten Zeitperioden stattfinden.

##### <a name="example-transactions--reduction-key"></a>Beispiel: Transaktionen – Planzahlenverrechnungsschlüssel

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

#### <a name="transactions--dynamic-period"></a>Transaktionen – dynamische Periode

Wenn Sie **Transaktion - dynamische Periode** auswählen, wird der Planungsbedarf durch die tatsächlichen Auftragsbuchungen verringert, die während der dynamischen Periode stattfinden. Die dynamische Periode erstreckt sich über die aktuellen Planungsdaten und endet beim Beginn der nächsten Planung. In diesem Fall erstellt die Produktprogrammplanung geplante Bestellungen, um den geplanten Bedarf (Planungsbedarf) zu erfüllen. Wenn die tatsächlichen Auftragstransaktionen erteilt werden, werden die Planungsbedarfe reduziert. Die tatsächlichen Transaktionen verbrauchen Teil des Planungsbedarfs.

Wenn diese Option verwendet wird, tritt das folgende Verhalten auf:

- Planzahlenverrechnungsschlüssel sind nicht erforderlich oder werde nicht verwendet. 
- Wenn die Planung vollständig verringert wird, wird der Planungsbedarf für die aktuelle Planung 0 (null).
- Wenn keine zukünftige Planung vorhanden ist, wird der Planungsbedarf der letzten eingegebenen Planung verringert.
- Planungszeiträume sind in der Berechnung der Planungsverringerung enthalten.
- Positive Tage sind in der Berechnung der Planungsverringerung enthalten.
- Wenn die tatsächlichen Auftragsbuchungen größer sind als der geplante Bedarf, werden die verbleibenden Buchungen nicht in die nächste Planungsperiode vorgetragen.

##### <a name="example-1-transactions--dynamic-period"></a>Beispiel 1: Transaktion – dynamische Periode

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

##### <a name="example-2-transactions--dynamic-period"></a>Beispiel 2: Transaktion – dynamische Periode

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

### <a name="create-and-set-up-a-forecast-reduction-key"></a><a name="create-reduction-key"></a>Erstellen und Einrichten eines Planzahlenverrechnungsschlüssels

Ein Planungsverrechnungsschlüssel wird in den Formularen **Transaktionen - Planzahlenverrechnungsschlüssel** und **Prozentplanzahlenverrechnungsschlüssel**-Methoden zum Reduzieren des Planungsbedarfes verwendet. Gehen Sie folgendermaßen vor, um einen Planzahlenverrechnungsschlüssel zu erstellen und einzurichten.

1. Gehen Sie zu **Produktprogrammplanung \> Einstellungen \> Abdeckung \> Planzahlenverrechnungsschlüssel**.
2. Klicken Sie auf **Neu** oder drücken Sie **STRG+N**, um einen neuen Planzahlenverrechnungsschlüssel zu erstellen.
3. Im Feld **Planzahlenverrechnungsschlüssel** geben Sie eine eindeutige Kennung für den Planzahlenverrechnungsschlüssel ein. Geben Sie im Feld  **Namen** einen Namen ein. 
4. Hier können Sie die Perioden sowie die Planzahlenverrechnungsschlüsselprozentsatz in jeder Periode eingeben:

    - Das Feld **Gültigkeitsdatum** gibt das Datum der Erstellung der Periode an. Wenn die Option **Gültigkeitsdatum verwenden** auf **Ja** gesetzt ist, beginnt die Periode am Gültigkeitsdatum. Wenn Sie auf **Nein** festgelegt ist, beginnt der Periodenanfang an dem Tag, an dem die Produktprogrammplanung ausgeführt wird.
    - Hier können Sie die Perioden definieren, in denen die geplante Planzahlenverrechnung ausgeführt werden soll.
    - Während einer bestimmten Periode geben Sie den Prozentsatz ein, um den der Planungsbedarf reduziert werden soll. Bei einem positiven Wert wird der Bedarf verringert, bei einem negativen Wert wird er erhöht.

### <a name="use-a-reduction-key"></a><a name="use-reduction-key"></a>Verwenden eines Planzahlenverrechnungsschlüssels

Ein Planzahlenverrechnungsschlüssel muss der Deckungsgruppe des Artikels zugewiesen werden. Gehen Sie folgendermaßen vor, um einen Planzahlenverrechnungsschlüssels eines Artikels der Dispositionssteuerungsgruppe zuzuweisen.

1. Gehen Sie zu **Produktprogrammplanung \> Einstellungen \> Planungshorizont \> Dispositionssteuerungsgruppen**
2. Wählen Sie im Feld **Planzahlenverrechnungsschlüssel** auf der Registerkarte **Andere** den Planzahlenverrechnungsschlüssel aus, der der Deckungsgruppe zugewiesen werden soll. Der Planzahlenverrechnungsschlüssel gilt dann für die Artikel, die zur Deckungsgruppe gehören.
3. Wenn der Planzahlenverrechnungsschlüsse eine Reduktion während der Produktprogrammplanung verwendet werden soll, müssen Sie diese Einstellungen in der Absatzplanung oder in den Einstellungen der Produktprogrammplanung definieren. Gehen Sie zu den folgenden Standorten:

    - Produktprogrammpläne \>Einstellungen \>Pläne \> Absatzplanungen
    - Produktprogrammplanung \> Einstellungen \> Pläne \> Produktprogrammpläne

4. Auf der Seite **Absatzpläne** oder **Produktprogrammpläne** auf dem Inforegister **Allgemeine** im Feld **Methode, um die Planungsbedarfe zu reduzieren**, wählen Sie entweder **Prozent - Planzahlenverrechnungsschlüssel** oder **Transaktionen - Planzahlenverrechnungsschlüssel** aus.

### <a name="reduce-a-forecast-by-transactions"></a>Reduzieren einer Planung durch Transaktionen

Wenn Sie **Transaktionen - Planzahlenverrechnungsschlüssel** oder **Transaktioen - dynamische Periode** als Methode für das Reduzieren von Planungsbedarfen aktivieren, können Sie angeben, welche Transaktionen die Planung verringert. Wählen Sie auf der Seite **Dispositionssteuerungsgruppe** im Inforegister **Sonstiges** für das Feld **Planungswert verringern um** die Option **Alle Transaktionen** aus, wenn alle Transaktionen die Planung reduzieren sollen, oder die Option **Aufträge**, wenn nur Aufträge die Planung reduzieren sollen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]