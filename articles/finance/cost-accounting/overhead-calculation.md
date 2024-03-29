---
title: Gemeinkostenberechnung
description: In diesem Artikel werden die typischen Prozesse für die Berechnung und Zuweisung von Gemeinkosten beschrieben.
author: AndersGirke
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: twheeloc
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: twheeloc
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 9322fb5237afdbf73147bb549eb3f70929c46ce2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881990"
---
# <a name="overhead-calculation"></a>Gemeinkostenberechnung

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die typischen Prozesse für die Berechnung und Zuweisung von Gemeinkosten beschrieben.

## <a name="term-definition"></a>Begriffsdefinition

Gemeinkosten sind die Kosten, die entstehen, wenn ein Unternehmen Geschäfte tätigt, die aber keinem bestimmten Geschäftsvorgang, Produkt oder Dienstleistung direkt zugeordnet werden können. Gemeinkosten leisten wichtigen Support für die Generierung von gewinnbringenden Aktivitäten. Hier sind einige Beispiele für Gemeinkosten:

-   Miete
-   Elektrizität
-   Verwaltungsgehälter

## <a name="overhead-calculation-overview"></a>Gemeinkostenberechnung, Übersicht
Gemeinkostenberechnung wird in der Kostenrechnungsmethoden in der korrekten Reihenfolge ausgeführt. Sie können obenliegende Berechnung Innerhalb desselben Finanzzeitraums mehrfach ausführen, wenn Kostenrechnungsmethoden der Buchführung geändert wurden, oder bestimmte Fehler erkannt wurden. Jede Ausführung der Gemeinkostenberechnung wird gespeichert und erhält eine eindeutige Versionen-Kennung, mit der Sie die Berechnungen in verschiedenen Versionen vergleichen können. Kosteneinträge, die die Gemeinkostenrechnung generiert, erhalten ein Buchungsdatum. Der Abschlussstichtag entspricht dem Enddatum der Periode, die in der Berechnung verwendet wird. Die eindeutige Version-Kennung besteht aus den folgenden Elementen:

-   Versionstyp
-   Datum und Uhrzeit
-   Kostenrechnungssachkonto
-   Geschäftsjahr
-   Finanzzeitraum

Die Gemeinkostenberechnung wird unabhängig von der Version ausgeführt. Daher können Sie die Budgetversion vor der tatsächlichen Version berechnen. Gemeinkostenberechnung besteht aus vier Schritten, wie in der folgenden Abbildung dargestellt. In jedem Schritt wird ein Erfassungskopf erstellt, der Journaleinträge hat. Dieser Erfassungskopf führt die Eingabedaten für jeden Berechnungsschritt aus. Richtlinien und Regeln werden für jede Erfassungsposition übernommen, und Kosteneinträge werden generiert. Deshalb ist die Nachweisbarkeit immer gegeben. 

[![Gemeinkostenberechnung.](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a>Berechnen Sie die Elektrizitäts-Gemeinkosten und weisen Sie diese zu
In der Finanzbuchhaltung werden einige Kosten wie Elektrizität als Pauschalbetrag erfasst. Daher wird ein detaillierter Verwaltungseinblick für Kostenrechnung nicht bereitgestellt. In der Kostenrechnung müssen die Kosten die Organisationseinheit durchlaufen, um auf allen Organisationsstufen und Ebenen korrekt dargestellt zu werden. Dieser Fluss muss entweder auf einem genauen Datensatz des Verbrauchs oder einer reellen Bewertung basieren. Im Hauptbuch können Stromkosten wie unten in der Tabelle dargelegt gebucht werden.

<table>
<thead>
<tr>
<th>Abschlussstichtag</th>
<th colspan="2">Kostenstelle</th>
<th colspan="2">Hauptkonto</th>
<th>Betrag in Buchhaltungswährung</th>
</tr>
</thead>
<tbody>
<tr>
<td>3. Januar 2017</td>
<td>CC099</td>
<td>Standardmäßige Kostenstelle</td>
<td>10001</td>
<td>Elektrizität</td>
<td>10.000,00</td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a>Schritt 1: Verarbeiten Sie die Kostenverhaltensberechnung

Standardmäßig wenn Einträge mit Kosten von den Daten importiert werden, erhalten Sie die Verhaltensklassifizierung **Nicht klassifiziert** in der Kostenrechnung. Wenn Sie Kostenverhaltensrichtlinienregeln anwenden, können sie die Kosteneinträge entweder als **Fixkosten** oder **Variable Kosten** neu klassifizieren.

#### <a name="define-the-cost-behavior-rule"></a>Definieren Sie die Kostenverhaltensregel

Manchmal ist ein Teil der Kosten eine feste Gebühr, und die verbleibenden Kosten basieren auf dem Verbrauch. Elektrizitätsrechnungen entsprechen oftmals dieser Definition. Nachdem Sie eine bestimmte festen Gebühr bezahlt haben, bezahlen Sie für den Verbrauch pro Kilowattstunde (KWH). Wenn beispielsweise die Fixkostengebühr 1.000,00 ist, wird die Kostenverhaltensregel wie folge definiert:

-   Fester Betrag 1,000.00
    -   0 &lt;= 1,000.00 = Fest
    -   1000,01 &lt; N = Variabel

##### <a name="journal"></a>Erfassung

<table>
<thead>
<tr>
<th>Erfassung</th>
<th>Journaltyp</th>
<th colspan="3">Steuerkalenderperiode</th>
<th>Version</th>
</tr>
</thead>
<tbody>
<tr>
<td>00001</td>
<td>Erfassung der Kostenverhaltensberechnung</td>
<td>Steuerlich</td>
<td>2017</td>
<td>Periode 1</td>
<td>Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)

<table>
<thead>
<tr>
<th>Abschlussstichtag</th>
<th colspan="2">Kostenobjekt</th>
<th colspan="2">Kostenelement</th>
<th>Kostenverhalten</th>
<th>Betrag</th>
</tr>
</thead>
<tbody>
<tr>
<td>3. Januar 2017</td>
<td>CC099</td>
<td>Standardmäßige Kostenstelle</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Nicht klassifiziert</td>
<td>10.000,00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kosteneinträge

<table>
<thead>
<tr>
<th colspan="2">Kostenobjekt</th>
<th colspan="2">Kostenelement</th>
<th>Kostenverhalten</th>
<th>Betrag</th>
<th>Abschlussstichtag</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>Standardmäßige Kostenstelle</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Nicht klassifiziert</td>
<td>10.000,00</td>
<td>3. Januar 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Standardmäßige Kostenstelle</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Nicht klassifiziert</td>
<td>-10,000.00</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Standardmäßige Kostenstelle</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>1.000,00</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Standardmäßige Kostenstelle</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>9.000,00</td>
<td>31. Januar 2017</td>
</tr>
</tbody>
</table>

Weitere Informationen finden Sie unter [Eine Kostenverhaltensrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).
### <a name="step-2-process-the-cost-distribution-calculation"></a>Schritt 2: Verarbeiten Sie die Kostenaufteilungsberechnung

Kostenaufteilung wird verwendet, um Kosten von einen Kostenträger in einen oder mehrere andere Kostenträger neu zu verteilen, indem Sie die gewünschte Verrechnungsgrundlage anwenden. Kostenaufteilung und Kostenzuweisung unterscheiden sich in dieser Kostenaufteilung immer auf der Ebene des Selbstkostenelements der Kosten.

#### <a name="define-the-cost-distribution-rule"></a>Definieren Sie die Kostenaufteilungsregel

In der Finanzbuchhaltung werden Kosten wie Elektrizität oft als Pauschalbetrag erfasst. In der Kostenrechnung ist dieser Ansatz nicht genau genug. Die variablen Kosten müssen den einzelnen Kostenträgern auf einer reellen Basis verteilt werden. Die logischste Zuweisungsgrundlage ist der Stromverbrauch (KWH). Ein statistisches Dimensionsmitglied, das als Elektrizität bezeichnet wird, wird erstellt und der Elektrizitätsverbrauch wird erfasst. Standardmäßig werden alle statistischen Dimensionswerte als Zuteilungsbasis verfügbar.

<table>
<thead>
<tr>
<th colspan="2">Kostenobjekt</th>
<th>KWH</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personalverwaltung</td>
<td>1.000</td>
</tr>
<tr>
<td>CC002</td>
<td>Finanzen</td>
<td>6.000</td>
</tr>
<tr>
<td>CC003</td>
<td>Montage</td>
<td>0</td>
</tr>
</tbody>
</table>

Die folgende Tabelle zeigt das Ergebnis, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.

<table>
<thead>
<tr>
<th colspan="2">Kostenobjekt</th>
<th>Größe</th>
<th>Zuweisungsfaktor</th>
<th>Betrag</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personalverwaltung</td>
<td>1.000</td>
<td>(1,000 ÷ 7,000) × 9,000.00</td>
<td>1,285.71</td>
</tr>
<tr>
<td>CC002</td>
<td>Finanzen</td>
<td>6.000</td>
<td>(6,000 ÷ 7,000) × 9,000.00</td>
<td>7,714.29</td>
</tr>
<tr>
<td>CC003</td>
<td>Montage</td>
<td>0</td>
<td>(0 ÷ 7,000) × 9,000.00</td>
<td>0,00</td>
</tr>
</tbody>
</table>

Die fixen Kosten sollten den jeweiligen Kostenträgern gleichmäßig aufgeteilt werden, die Elektrizität verbraucht haben. Sie können dieses Ergebnis erreichen, indem Sie das statistische Dimensionsmitglied in einer Formelverrechnungsgrundlage verwenden: (Elektrizität &gt; 0,00) Die folgende Tabelle zeigt das Ergebnis an, wenn Stromverbrauch als Verrechnungsgrundlage für variable Kosten angewendet wird.

<table>
<thead>
<tr>
<th colspan="2">Kostenobjekt</th>
<th>Berechnungsgrundlage</th>
<th>Größe</th>
<th>Zuweisungsfaktor</th>
<th>Betrag</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personalverwaltung</td>
<td>(1,000 &gt; 0.00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1,000.00</td>
<td>500,00</td>
</tr>
<tr>
<td>CC002</td>
<td>Finanzen</td>
<td>(6,000 &gt; 0.00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1,000.00</td>
<td>500,00</td>
</tr>
<tr>
<td>CC003</td>
<td>Montage</td>
<td>(0 &gt; 0.00)</td>
<td>0</td>
<td>(0 ÷ 2) × 1,000.00</td>
<td>0,00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>Erfassung

<table>
<thead>
<tr>
<th>Erfassung</th>
<th>Journaltyp</th>
<th colspan="3">Steuerkalenderperiode</th>
<th>Version</th>
</tr>
</thead>
<tbody>
<tr>
<td>00002</td>
<td>Berechnung der Kostenverteilung</td>
<td>Steuerlich</td>
<td>2017</td>
<td>Periode 1</td>
<td>Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)

<table>
<thead>
<tr>
<th>Abschlussstichtag</th>
<th colspan="2">Kostenobjekt</th>
<th colspan="2">Kostenelement</th>
<th>Kostenverhalten</th>
<th>Betrag</th>
</tr>
</thead>
<tbody>
<tr>
<td>31. Januar 2017</td>
<td>CC099</td>
<td>Standardmäßige Kostenstelle</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>1.000,00</td>
</tr>
<tr>
<td>31. Januar 2017</td>
<td>CC099</td>
<td>Standardmäßige Kostenstelle</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>9.000,00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kosteneinträge

<table>
<thead>
<tr>
<th colspan="2">Kostenobjekt</th>
<th colspan="2">Kostenelement</th>
<th>Kostenverhalten</th>
<th>Betrag</th>
<th>Abschlussstichtag</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>Standardmäßige Kostenstelle</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>-1.000,00</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Personalverwaltung</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>500,00</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finanzen</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>500,00</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Standardmäßige Kostenstelle</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>-9,000.00</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Personalverwaltung</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>1,285.71</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finanzen</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>7,714.29</td>
<td>31. Januar 2017</td>
</tr>
</tbody>
</table>

Weitere Informationen finden Sie unter [Eine Kostenverteilungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen](tasks/create-assign-cost-distribution-policy-cost-control-unit.md). 

### <a name="step-3-process-the-overhead-rate-calculation"></a>Schritt 3: Verarbeiten Sie die Gemeinkostensatzberechnung

Der Gemeinkostensatz wird verwendet, um eine oder mehrere bestimmte Kostenträger zu belasten. Der Zuschlag erfolgt auf Grundlage eines vorbestimmten Kostensatzes und der Größe der zugewiesenen Verrechnungsgrundlage. 

#### <a name="define-the-overhead-rate"></a>Definieren Sie den Gemeinkostensatz

Kostenträger CC001 Personalverwaltung trägt zu einer Gruppe bei internen Projekten bei. Ein statistisches Dimensionsmitglied, das HR-Projekte heißt, wird erstellt, um die verbrauchte Größe zu messen.

<table>
<thead>
<tr>
<th colspan="2">Kostenobjekt</th>
<th>Stunden</th>
</tr>
</thead>
<tbody>
<tr>
<td>Proj 1</td>
<td>Projekt 1</td>
<td>3</td>
</tr>
<tr>
<td>Proj 2</td>
<td>Projekt 2</td>
<td>1</td>
</tr>
</tbody>
</table>

Ein vorbestimmter Normalkostensatz für den Kostenprojektbeitrag wurde definiert.

<table>
<thead>
<tr>
<th colspan="2">Kostenobjekt</th>
<th>Kostenelement</th>
<th>Kostenverhalten</th>
<th>Einheiten</th>
<th>Satz</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personalverwaltung</td>
<td>10001</td>
<td>Variable Kosten</td>
<td>1</td>
<td>10</td>
</tr>
</tbody>
</table>

Die folgende Tabelle zeigt das Ergebnis an, wenn die Personalverwaltungsprojekte als Verrechnungsgrundlage angewendet werden.

<table>
<thead>
<tr>
<th colspan="2">Kostenobjekt</th>
<th>Größe</th>
<th>Kostenelement</th>
<th>Zuweisungsfaktor</th>
<th>Betrag</th>
</tr>
</thead>
<tbody>
<tr>
<td>Proj 1</td>
<td>Projekt 1</td>
<td>3</td>
<td>10001</td>
<td>(3 ÷ 1) × 10.00</td>
<td>30,00</td>
</tr>
<tr>
<td>Proj 2</td>
<td>Projekt 2</td>
<td>1</td>
<td>10001</td>
<td>(1 ÷ 1) × 10.00</td>
<td>10,00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>Erfassung

<table>
<thead>
<tr>
<th>Erfassung</th>
<th>Journaltyp</th>
<th colspan="3">Steuerkalenderperiode</th>
<th>Version</th>
</tr>
</thead>
<tbody>
<tr>
<td>00003</td>
<td>Erfassung der Gemeinkostensatzberechnung</td>
<td>Steuerlich</td>
<td>2017</td>
<td>Periode 1</td>
<td>Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a>Journaleinträge (Journaleinträge für Gemeinkostensatzberechnung)

<table>
<thead>
<tr>
<th>Abschlussstichtag</th>
<th colspan="2">Kostenobjekt</th>
<th>Größe</th>
</tr>
</thead>
<tbody>
<tr>
<td>31. Januar 2017</td>
<td>Proj 1</td>
<td>Internes Projekt 1</td>
<td>3,00</td>
</tr>
<tr>
<td>31. Januar 2017</td>
<td>Proj 2</td>
<td>Internes Projekt 2</td>
<td>1,00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kosteneinträge

<table>
<thead>
<tr>
<th colspan="2">Kostenobjekt</th>
<th colspan="2">Kostenelement</th>
<th>Kostenverhalten</th>
<th>Betrag</th>
<th>Abschlussstichtag</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC0001</td>
<td>Personalverwaltung</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>-30.00</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>Proj 1</td>
<td>Internes Projekt 1</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>30,00</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Personalverwaltung</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>-10,00</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>Proj 2</td>
<td>Internes Projekt 2</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>10.00</td>
<td>31. Januar 2017</td>
</tr>
</tbody>
</table>

Weitere Informationen finden Sie unter [Gemeinkostenberechnung ausführen](cost-rollup.md#perform-overhead-calculation)

### <a name="step-4-process-the-cost-allocation-calculation"></a>Schritt 4: Verarbeiten Sie die Kostenaufteilungsberechnung

Die Zuteilung wird verwendet, um den Saldo eines Kostenträgers zu anderen Kostenträgern zuweisen, indem eine Verrechnungsgrundlage angewendet wird. Finance unterstützt die gegenseitige Zuordnungsmethode. In der gegenseitigen Zuordnungsmethode werden die gegenseitigen Dienstleistungen, die Unterkostenobjekte austauschen, vollständig berücksichtigt werden. Das System bestimmt automatisch die korrekte Reihenfolge, in der die Zuordnungen ausgeführt werden. Der Saldo eines Kostenträgers wird durch eine einzelne Verrechnungsgrundlage zugewiesen. Zuweisungen für Kostenträgerdimensionen und ihre jeweiligen Mitglieder werden unterstützt. Der Zuweisungsauftrag wird durch die Kostenkontrollsteuereinheit gesteuert. 

[![Reziproke Methode.](./media/reciprocal-method.png)](./media/reciprocal-method.png)

#### <a name="define-the-cost-allocation"></a>Kostenzuteilung definieren

Das hier ein einfaches Beispiel, das erklärt, wie Sie den Kostenfluss nachverfolgen können. Kostenträger CC001 Personalverwaltung trägt zu mehreren Kostenträgern bei. Ein statistisches Dimensionsmitglied, das HR-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.

<table>
<thead>
<tr>
<th colspan="2">Kostenobjekt</th>
<th>HR-Dienste</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>Finanzen</td>
<td>35</td>
</tr>
<tr>
<td>CC003</td>
<td>Montage</td>
<td>55</td>
</tr>
<tr>
<td>CC004</td>
<td>Verpackung</td>
<td>10</td>
</tr>
</tbody>
</table>

Kostenträger CC002 Finanzen trägt zu mehreren Kostenträgern bei. Ein statistisches Dimensionsmitglied, das Finance-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.

<table>
<thead>
<tr>
<th colspan="2">Kostenobjekt</th>
<th>Finanzdienste</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>Montage</td>
<td>65</td>
</tr>
<tr>
<td>CC004</td>
<td>Verpackung</td>
<td>35</td>
</tr>
</tbody>
</table>

Kostenträger CC003 Montage trägt zu mehreren Kostenträgern bei. Ein statistisches Dimensionsmitglied, das Montage-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.

<table>
<thead>
<tr>
<th colspan="2">Kostenobjekt</th>
<th>Montage-Services (Stunden)</th>
</tr>
</thead>
<tbody>
<tr>
<td>Produktion 1</td>
<td>Produkt 1</td>
<td>60</td>
</tr>
<tr>
<td>Produktion 2</td>
<td>Produkt 2</td>
<td>20</td>
</tr>
</tbody>
</table>

Kostenträger CC004 Montage trägt zu mehreren Kostenträgern bei. Ein statistisches Dimensionsmitglied, das Verpackungs-Services heißt, wird erstellt, um die verbrauchte Größe zu messen.

<table>
<thead>
<tr>
<th colspan="2">Kostenobjekt</th>
<th>Packdienste (Stunden)</th>
</tr>
</thead>
<tbody>
<tr>
<td>Produktion 1</td>
<td>Produkt 1</td>
<td>80</td>
</tr>
<tr>
<td>Produktion 2</td>
<td>Produkt 2</td>
<td>15</td>
</tr>
</tbody>
</table>

> [!NOTE]
> Statistische Kennzahlen wie Produktionsstunden, die ein Produkt verbraucht, können von den Quelldaten abgeleitet werden. Weitere Informationen finden Sie unter [Anbietervorlagen für statistische Maßnahmen](statistical-measure-provider-template.md#statistical-measure-provider-template). Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn HR-Dienste als Zuteilungsbasis für die Gesamtkosten übernommen werden (Fixkosten und variable Kosten).

<table>
<thead>
<tr>
<th colspan="2">Kostenobjekt</th>
<th>Größe</th>
<th>Zuweisungsfaktor</th>
<th>Betrag</th>
<th>Kostenverhalten</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>Finanzen</td>
<td>35</td>
<td>(35 ÷ 100) × 500.00</td>
<td>175.00</td>
<td>Fixkosten</td>
</tr>
<tr>
<td>CC003</td>
<td>Montage</td>
<td>55</td>
<td>(55 ÷ 100) × 500.00</td>
<td>275.00</td>
<td>Fixkosten</td>
</tr>
<tr>
<td>CC004</td>
<td>Verpackung</td>
<td>10</td>
<td>(10 ÷ 100) × 500.00</td>
<td>50,00</td>
<td>Fixkosten</td>
</tr>
<tr>
<td>CC002</td>
<td>Finanzen</td>
<td>35</td>
<td>(35 ÷ 100) × 1,245.71</td>
<td>436.00</td>
<td>Variable Kosten</td>
</tr>
<tr>
<td>CC003</td>
<td>Montage</td>
<td>55</td>
<td>(55 ÷ 100) × 1,245.71</td>
<td>685.14</td>
<td>Variable Kosten</td>
</tr>
<tr>
<td>CC004</td>
<td>Verpackung</td>
<td>10</td>
<td>(10 ÷ 100) × 1,245.71</td>
<td>124.57</td>
<td>Variable Kosten</td>
</tr>
</tbody>
</table>

Die folgende Tabelle zeigt das Ergebnis angezeigt, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).

<table>
<thead>
<tr>
<th colspan="2">Kostenobjekt</th>
<th>Größe</th>
<th>Zuweisungsfaktor</th>
<th>Betrag</th>
<th>Kostenverhalten</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>Montage</td>
<td>65</td>
<td>(65 ÷ 100) × (500.00 + 175.00)</td>
<td>438.75</td>
<td>Fixkosten</td>
</tr>
<tr>
<td>CC004</td>
<td>Verpackung</td>
<td>35</td>
<td>(35 ÷ 100) × (500.00 + 175.00)</td>
<td>236.25</td>
<td>Fixkosten</td>
</tr>
<tr>
<td>CC003</td>
<td>Montage</td>
<td>65</td>
<td>(65 ÷ 100) × (7,714.29 + 436.00)</td>
<td>5,297.69</td>
<td>Variable Kosten</td>
</tr>
<tr>
<td>CC004</td>
<td>Verpackung</td>
<td>35</td>
<td>(35 ÷ 100) × (7,714.29 + 436.00)</td>
<td>2,852.60</td>
<td>Variable Kosten</td>
</tr>
</tbody>
</table>

Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).

<table>
<thead>
<tr>
<th colspan="2">Kostenobjekt</th>
<th>Größe</th>
<th>Zuweisungsfaktor</th>
<th>Betrag</th>
<th>Kostenverhalten</th>
</tr>
</thead>
<tbody>
<tr>
<td>Produktion 1</td>
<td>Produkt 1</td>
<td>60</td>
<td>(60 ÷ 80) × (275.00 + 438.75)</td>
<td>535.31</td>
<td>Fixkosten</td>
</tr>
<tr>
<td>Produktion 2</td>
<td>Produkt 2</td>
<td>20</td>
<td>(20 ÷ 80) × (275.00 + 438.75)</td>
<td>178.44</td>
<td>Fixkosten</td>
</tr>
<tr>
<td>Produktion 1</td>
<td>Produkt 1</td>
<td>60</td>
<td>(60 ÷ 80) × (5,297.69 + 685.14)</td>
<td>4,487.12</td>
<td>Variable Kosten</td>
</tr>
<tr>
<td>Produktion 2</td>
<td>Produkt 2</td>
<td>20</td>
<td>(20 ÷ 80) × (5,297.69 + 685.14)</td>
<td>1,495.71</td>
<td>Variable Kosten</td>
</tr>
</tbody>
</table>

Die folgende Tabelle zeigt das Ergebnis an, wenn die Verrechnungsgrundlage für Finanzdienstleistungen als Gesamtkosten übernommen werden (Fixkosten und variable Kosten).

<table>
<thead>
<tr>
<th colspan="2">Kostenobjekt</th>
<th>Größe</th>
<th>Zuweisungsfaktor</th>
<th>Betrag</th>
<th>Kostenverhalten</th>
</tr>
</thead>
<tbody>
<tr>
<td>Produktion 1</td>
<td>Produkt 1</td>
<td>80</td>
<td>(80 ÷ 95) × (50.00 + 236.25)</td>
<td>241.05</td>
<td>Fixkosten</td>
</tr>
<tr>
<td>Produktion 2</td>
<td>Produkt 2</td>
<td>15</td>
<td>(15 ÷ 95) × (50.00 + 236.25)</td>
<td>45.20</td>
<td>Fixkosten</td>
</tr>
<tr>
<td>Produktion 1</td>
<td>Produkt 1</td>
<td>80</td>
<td>(80 ÷ 95) × (2,852.60 + 124.57)</td>
<td>2,507.09</td>
<td>Variable Kosten</td>
</tr>
<tr>
<td>Produktion 2</td>
<td>Produkt 2</td>
<td>15</td>
<td>(15 ÷ 95) × (2,852.60 + 124.57)</td>
<td>470.08</td>
<td>Variable Kosten</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Erfassungseinträge (Kostenobjektbasierte Erfassungseinträge)

<table>
<thead>
<tr>
<th>Erfassung</th>
<th>Journaltyp</th>
<th colspan="3">Steuerkalenderperiode</th>
<th>Version</th>
</tr>
</thead>
<tbody>
<tr>
<td>00004</td>
<td>Kostenzuteilungserfassung</td>
<td>Steuerlich</td>
<td>2017</td>
<td>Periode 1</td>
<td>Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a>Erfassungspositionen

<table>
<thead>
<tr>
<th>Abschlussstichtag</th>
<th colspan="2">Kostenobjekt</th>
<th colspan="2">Kostenelement</th>
<th>Kostenverhalten</th>
<th>Betrag</th>
</tr>
</thead>
<tbody>
<tr>
<td>31. Januar 2017</td>
<td>CC001</td>
<td>Personalverwaltung</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>500,00</td>
</tr>
<tr>
<td>31. Januar 2017</td>
<td>CC001</td>
<td>Personalverwaltung</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>1,245.71</td>
</tr>
<tr>
<td>31. Januar 2017</td>
<td>CC002</td>
<td>Finanzen</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>675.00</td>
</tr>
<tr>
<td>31. Januar 2017</td>
<td>CC002</td>
<td>Finanzen</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>8,150.29</td>
</tr>
<tr>
<td>31. Januar 2017</td>
<td>CC003</td>
<td>Montage</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>713.75</td>
</tr>
<tr>
<td>31. Januar 2017</td>
<td>CC003</td>
<td>Montage</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>5,982.83</td>
</tr>
<tr>
<td>31. Januar 2017</td>
<td>CC003</td>
<td>Verpackung</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>286.25</td>
</tr>
<tr>
<td>31. Januar 2017</td>
<td>CC003</td>
<td>Verpackung</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>2,977.17</td>
</tr>
<tr>
<td>31. Januar 2017</td>
<td>Produktion 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>776.36</td>
</tr>
<tr>
<td>31. Januar 2017</td>
<td>Produktion 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>6,994.21</td>
</tr>
<tr>
<td>31. Januar 2017</td>
<td>Produktion 2</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>223.64</td>
</tr>
<tr>
<td>31. Januar 2017</td>
<td>Produktion 2</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>1,965.79</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kosteneinträge

<table>
<thead>
<tr>
<th colspan="2">Kostenobjekt</th>
<th colspan="2">Kostenelement</th>
<th>Kostenverhalten</th>
<th>Betrag</th>
<th>Abschlussstichtag</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personalverwaltung</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>-500,00</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finanzen</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>175.00</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Montage</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>275.00</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Verpackung</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>50,00</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Personalverwaltung</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>-1,245.71</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finanzen</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>436.00</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Montage</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>685.14</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Verpackung</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>124.57</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finanzen</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>-675.00</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Montage</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>438.75</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Verpackung</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>236.25</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finanzen</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>-8,150.29</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Montage</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>5,297.69</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Verpackung</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>2,852.60</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Montage</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>-713.75</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>Produktion 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>535.31</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>Produktion 2</td>
<td>Produkt 2</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>178.44</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Montage</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>-5,982.83</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>Produktion 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>4,487.12</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>Produktion 2</td>
<td>Produkt 2</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>1,495.71</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Montage</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>-286.25</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>Produktion 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>241.05</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>Produktion 2</td>
<td>Produkt 2</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Fixkosten</td>
<td>45.20</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Montage</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>-2,977.17</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>Produktion 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>2,507.09</td>
<td>31. Januar 2017</td>
</tr>
<tr>
<td>Produktion 2</td>
<td>Produkt 2</td>
<td>10001</td>
<td>Elektrizität</td>
<td>Variable Kosten</td>
<td>470.08</td>
<td>31. Januar 2017</td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a>Schlussfolgerung
In der Finanzrechnung werden Kosten von 10.000,00 für Elektrizität einer blinden Kostenstellen-Kennung zugeordnet. Daher wissen Buchhaltern dass diese Kosten zugewiesen werden müssen. In der Kostenrechnung fließen die Kosten über Organisationseinheiten und Ebenen, basierend auf den Richtlinien und Regeln, die angewendet werden. Jeder Kostenträger gehören zu einer Verrechnungsgrundlage,die die beste Bewertung für die Kostenverteilung bereitstellt.

Kostenelement | Kostenobjekt<br>CC099 | Kostenobjekt<br>CC001 | Kostenobjekt<br>CC002 | Kostenobjekt<br>CC003 | Kostenobjekt<br>CC004 | Kostenobjekt<br>Proj 1 | Kostenobjekt<br>Proj 2 | Kostenobjekt<br>Produktion 1 | Kostenobjekt<br>Produktion 2 | Gesamt
---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:
100'1 Elektrizität | 0,00 | 0,00 | 0,00 | 0,00 |  | 30.00 | 10.00 | 7,770.57 | 2,189.43 | 10,000.00 |
Nicht klassifiziert | 0,00 |  |  |  |  |  |  |  |  |  |
Fixkosten | 0,00 | 0,00 | 0,00 | 0,00 | 0,00 |  |  | 776.36 | 223.64 | 1,000.00 |
Variable Kosten | 000 | 0,00 | 0,00 | 0,00 | 0,00 | 30.00 | 10.00 | 6,994.21 | 1,965.79 | 9,000.00 |

> [!NOTE]
> Dieser Artikel veranschaulicht, wie ein Selbstkostenelement, hier 10001 Elektrizität die Kostenträger durchläuft. Daher werden diese Gemeinkosten der niedrigsten Ebene in der Organisation zugeordnet. Das bedeutet, die Kostenträger auf unterster Ebene müssen die Kosten tragen. Wenn Sie einen visuellen Fluss der Kosten zwischen dem Kostenträger und dem Kostenobjekt anfordern, können Sie die Richtlinie Kostenzusammenfassung verwenden, um den Kostenfluss zu visualisieren. Weitere Informationen finden Sie unter [Kostenrollup-Richtlinie und Zuschlagsberechnung](cost-rollup.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
