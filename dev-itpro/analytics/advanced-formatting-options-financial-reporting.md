---
title: Erweiterte Formatierungsoptionen in der Finanzberichterstellung
description: "Wenn Sie einen Bericht in der Finanzberichterstellung erstellen, sind zusätzliche Formatierungsfunktionen, einschließlich Filter für Dimensionen, Einschränkungen für Spalten und Berichtseinheiten, nicht druckbare Zeilen und IF/THEN/ELSE-Anweisungen in Berechnungen, verfügbar."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Management Reporter
ms.custom: 106571
ms.assetid: 895b5127-01d6-4495-b127-343387b743aa
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 631fec1dc135565e6d38e7faf193a7a898b508cb
ms.lasthandoff: 03/29/2017


---

# <a name="advanced-formatting-options-in-financial-reporting"></a>Erweiterte Formatierungsoptionen in der Finanzberichterstellung

Wenn Sie einen Bericht in der Finanzberichterstellung erstellen, sind zusätzliche Formatierungsfunktionen, einschließlich Filter für Dimensionen, Einschränkungen für Spalten und Berichtseinheiten, nicht druckbare Zeilen und IF/THEN/ELSE-Anweisungen in Berechnungen, verfügbar. 

In der folgenden Tabelle finden Sie die erweiterten Formatierungsfunktionen, die verfügbar sind, wenn Sie Berichte entwerfen.

| Funktion                   | Beschreibung                                                                                                                                                                                                                                                                                                                     |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dimensionsfilter           | Für den Zugriff auf bestimmte Datensätze können Sie Dimensionen in der Zeilendefinition und in der Spaltendefinition verwenden. Viele Berichte verwenden nur das natürliche Segment im Zeilenformat. Allerdings können Zeilen geändert werden, damit sie Dimensionswerte enthalten. Dimensionsfilter in der Spaltendefinition werden verwendet, um auf bestimmte Dimensionswerte zuzugreifen. |
| Einschränken der Berichtseinheit | Sie können eine Berichtszeile so einrichten, dass sie nur Informationen anzeigt, die mit einer bestimmten Berichtseinheit verknüpft sind.                                                                                                                                                                                                                      |
| Nicht druckbare (NP)-Zeilen     | Nicht druckbare Zeilen sind in einer Vielzahl von Berichten hilfreich. Wenn mehrere Berechnungen erforderlich sind, um einen Wert zu erhalten, können Sie diese Berechnungen im gedruckten Bericht ausblenden. Nicht druckbare Zeilen sind auch für die Problembehandlung von Berichtsdesigns und die erweiterte Zellenplatzierung hilfreich.                                                    |
| Spalteneinschränkung         | Die Spalteneinschränkung in der Zeilendefinition ist für das Ausblenden von Werten sinnvoll, die nur für einige Zeilen des Berichts relevant sind. Wenn Prozentrechnungen über eine Zeile ausgeführt werden, verhindert die Spalteneinschränkung, dass gesamte Spalten oder andere Spalten gedruckt werden, wenn diese Zahlen nicht relevant sind.                              |
| Spaltenumbruch               | Sie können Spaltenumbrüche zu einer Zeilendefinition hinzufügen, um Berichtsinformationen nebeneinander anzuzeigen. Sie können mehrere Spaltenumbrüche zu einer einzelnen Zeilendefinition hinzufügen. Die Spaltenüberschriften werden nach dem Spaltenumbruch oben über jeder Spalte wiederholt. Kommentare für einen Bericht werden zwischen den Spaltenumbrüchen angezeigt.                              |
| IF/THEN/ELSE-Anweisung     | Sie können Berechnungen in einer Zeilendefinition oder Spaltendefinition ändern.                                                                                                                                                                                                                                                         |

## <a name="advanced-cell-placement"></a>Erweiterte Zellenplatzierung
Erweiterte Zellenplatzierung oder *Erzwingen* betrifft die Platzierung von bestimmten Werten in bestimmten Zellen. Beispielsweise wird das Erzwingen häufig verwendet, um den korrekten Saldo in einer Cashflowaufstellung zu verschieben. Sie können das Erzwingen für folgende Zwecke verwenden:

-   Verschieben Sie Werte aus Microsoft Excel in bestimmte Zellen.
-   Definieren Sie bestimmte Werte in einem Bericht vor.
-   Ändern Sie Vorzeichen, indem Sie einen Wert von einer vorherigen Zelle kopieren und diesen Wert mit -1 multiplizieren.

**Hinweis:** In vielen Fällen müssen Sie Ihre Berichtsdefinition konfigurieren, sodass Spaltenberechnungen vor Zeilenberechnungen geleistet werden. Führen Sie zum Abschließen dieser Konfiguration die folgenden Schritte durch.

1.  Im Berichts-Designer öffnen Sie die Berichtsdefinition.
2.  Wählen Sie auf der Registerkarte **Einstellungen** unter **Berechnungspriorität** die Option **Erst Spalte, dann Zeile berechnen** aus.

## <a name="designing-the-report"></a>Gestalten des Berichts
Wenn Sie einen Bericht entwerfen, sollten Sie zunächst alle Detailzeilen erstellen, um sicherzustellen, dass die Werte wie erwartet miteinbezogen werden. Fügen Sie dann **NP** (kein Druck) Format überschreibt hinzu, um das Detail zu unterdrücken, das die endgültigen Werte umfasst. **Wichtig:** Wenn Sie den **CAL**-Formatcode in der Zeilendefinition verwenden, können Sie keinen Drilldown zu den Buchungsdetails ausführen. Für das Erzwingen Formeln verwenden das folgende Format: &lt;Zielspalte&gt;=&lt;=column.row-Code auslöst, trennen&gt; sämtliche weiteren Platzierungen für eine Zeile durch ein Komma und ein Leerzeichen. Beispiel: D=C.190,E=C.100

## <a name="examples-of-advanced-formatting-options"></a>Beispiele von erweiterten Formatierungsoptionen
Das folgenden Beispiel zeigt, wie die Zeilendefinition und die Spaltendefinition formatiert wird, um einen grundlegenden Cashflowbericht (Beispiel 1) und einen statistischen Bericht (Beispiel 2) zu erzwingen.

### <a name="example-1-basic-forcing"></a>Beispiel 1: Grundlegendes Erzwingen

Die folgende Tabelle enthält ein Beispiel einer Zeilendefinition, die das grundlegende Erzwingen verwendet.

| Zeilencode | Beschreibung                      | Formatcode | Verwandte Formeln/Zeilen/Einheiten | Formataußerkraftsetzung | Normaler Saldo | Drucksteuerung | Spalteneinschränkung | Zeilenmodifizierer               | Mit Finanzdimensionen verknüpfen |
|----------|----------------------------------|-------------|-----------------------------|-----------------|----------------|---------------|--------------------|----------------------------|------------------------------|
| 100      | Barmittel am Periodenanfang (NP) |             |                             |                 |                |               |                    | Kontoen-Modifizierer = \[/BB\] | +Segment2 \[\]= 1100         |
| 130      | Barmittel am Periodenanfang      | CAL         | C=C.100,F=D.100             |                 |                |               |                    |                            |                              |
| 160      |                                  |             |                             |                 |                |               |                    |                            |                              |
| 190      |                                  |             |                             |                 |                |               |                    |                            |                              |

Die folgende Tabelle enthält ein Beispiel einer Spaltendefinition, die das grundlegende Erzwingen in einer Zeile verwendet.

|                              | A:   | Mrd    | C:        | S      | E:      | Fr    |
|------------------------------|-----|------|----------|--------|--------|------|
| Kopfzeile 1                     |     |      |          |        |        |      |
| Kopfzeile 2                     | A:   | Mrd    | C:        | S      | E:      | Fr    |
| Kopfzeile 3                     |     |      |          |        |        |      |
| Spaltentyp                  | ZEILE | BESCHR | FD       | FD     | FD     | KALK |
| Buchcode/Attributkategorie |     |      | ISTWERT   | ISTWERT | ISTWERT |      |
| Geschäftsjahr                  |     |      | BASIS     | BASIS   | BASIS   |      |
| Zeitraum                       |     |      | BASIS     | BASIS   | BASIS   |      |
| Abgedeckte Perioden              |     |      | PERIODISCH | Jahr bis dato/BB | Jahr bis dato    |      |
| Formel                      |     |      |          |        |        | E-D  |
| Spaltenbreite                 | 5   | 30   | 14       | 14     | 14     | 14   |

### <a name="example-2-statistical-reports"></a>Beispiel 2: Statistische Berichte

Die folgende Tabelle enthält ein Beispiel einer Zeilendefinition, die das grundlegende Erzwingen für einen statistischen Bericht verwendet.

| Zeilencode | Beschreibung               | Formatcode | Verwandte Formeln/Zeilen/Einheiten     | Formataußerkraftsetzung      | Normaler Saldo | Drucksteuerung | Spalteneinschränkung | Zeilenmodifizierer | Mit Finanzdimensionen verknüpfen               |
|----------|---------------------------|-------------|---------------------------------|----------------------|----------------|---------------|--------------------|--------------|--------------------------------------------|
| 50       | Statistische Daten   | ANM         |                                 |                      |                |               |                    |              |                                            |
| 100      | Mitarbeiterzahl - US            | CAL         | 4                               | \#\#\#0.;($\#\#\#0.) |                |               |                    |              |                                            |
| 115      | Mitarbeiterzahl - International | CAL         | 11                              | \#\#\#0.;($\#\#\#0.) |                |               |                    |              |                                            |
| 130      |                           |             |                                 |                      |                |               |                    |              |                                            |
| 190      | Umsatz US                  |             |                                 |                      | C:              |               |                    |              | +Segment2 = \[41\*,\]Segment3 \[00 =\]    |
| 220      | Internationaler Umsatz       |             |                                 |                      | C:              |               |                    |              | +Segment2 = \[41\*,\]Segment3- \[01:99 =\] |
| 250      |                           |             |                                 |                      |                |               |                    |              |                                            |
| 280      |                           |             |                                 |                      |                |               |                    |              |                                            |
| 310      | Umsatz US                  | CAL         | D=C.190,E=C.100,F=(C.100/C.190) |                      |                |               |                    |              |                                            |
| 340      | Internationaler Umsatz       | CAL         | D=C.220,E=C115,F=(C.220/C.115)  |                      |                |               |                    |              |                                            |

Die folgende Tabelle enthält ein Beispiel einer Spaltendefinition, die das grundlegende Erzwingen für einen statistischen Bericht verwendet.

|                              | A:   | Mrd    | C:      | S            | E:     | Fr            |
|------------------------------|-----|------|--------|--------------|-------|--------------|
| Kopfzeile 1                     | A:   | Mrd    | C:      | S            | E:     | Fr            |
| Kopfzeile 2                     | -   | -    | Jahr bis dato    | Jährlicher Umsatz | Personal | $ pro Person |
| Kopfzeile 3                     |     |      |        |              |       |              |
| Spaltentyp                  | ZEILE | DESC | FD     | KALK         | KALK  | KALK         |
| Buchcode/Attributkategorie |     |      | ISTWERT |              |       |              |
| Geschäftsjahr                  |     |      | BASIS   |              |       |              |
| Zeitraum                       |     |      | BASIS   |              |       |              |
| Abgedeckte Perioden              |     |      | Jahr bis dato    |              |       |              |
| Formel                      |     |      |        |              |       | E-D          |
| Spaltenbreite                 | 5   | 30   | 14     | 14           | 14    | 14           |

## <a name="restricting-a-row-to-a-specific-reporting-unit"></a>Beschränken einer Zeile auf eine bestimmte Berichtseinheit
Wenn eine Berichtszeile auf eine bestimmte Berichtseinheit beschränkt ist, zeigt die Zeile die verknüpften Daten nur für die benannte Berichtseinheit und ignoriert die Daten für andere Berichtseinheiten in der Berichtsbaumstruktur. So können Sie eine Zeile erstellen, die Details für die gesamten Betriebskosten für eine bestimmte Abteilung bereitstellt. Ihr Bericht enthält möglicherweise doppelte Daten, wenn der Bericht sowohl die Berichtsbaumstruktur und eine Zeilendefinition enthält, die mehr als das natürliche Konto besitzt. Sie haben beispielsweise eine Berichtsbaumstruktur, die die sechs Abteilungen in der Organisation aufführt, und Sie haben auch eine Zeilendefinition, die eine bestimmte Kombination aus einem Konto und einer Abteilung in der Zeile aufführt. Wenn Sie den Bericht generieren, wird die bestimmte Kombination aus Konto und Abteilung für jede Ebene der Berichtsbaumstruktur gedruckt, auch wenn diese Abteilung möglicherweise nicht mit dem, was in der Struktur ist, übereinstimmt. Dieses Verhalten tritt auf, da die Zeile überschreibt, was in der Regel von der Berichtsdefinition gefiltert wird. Eine Möglichkeit, doppelte Daten zu vermeiden, besteht darin, eine Zeile auf eine bestimmte Berichtseinheit zu beschränken. **Hinweis:** Wenn eine Zeile Dimensionen umfasst und Sie beschränken diese Zeile auf eine untergeordnete Berichtseinheit, wird der Zeilenbetrag für diese untergeordnete Einheit und deren übergeordnete Einheiten mit eingeschlossen. Eine Duplizierung erfolgt nicht.

### <a name="restrict-a-row-to-a-reporting-unit"></a>Beschränken einer Zeile auf eine bestimmte Berichtseinheit

1.  Im Berichts-Designer klicken Sie auf die **Zeilendefinitionen** und wählen dann eine Zeilendefinition, um sie zu ändern.
2.  Doppelklicken Sie auf die entsprechende Zelle **Verwandte Formeln/Zeilen/Einheiten**.
3.  Wählen Sie im Dialogfeld **Auswahl der Berichtseinheit** im Feld **Berichtsbaumstruktur** die Struktur aus, die in der Berichtsdefinition zugewiesen ist.
4.  Wählen Sie eine Berichtseinheit, und klicken Sie anschließend auf **OK**. Die Einschränkung wird in der Zelle der Zeilendefinition angezeigt.
5.  Doppelklicken Sie auf die Zelle in der Spalte **Verknüpfung zu Finanzdimensionen** der beschränkten Zeile, und geben Sie dann die Verknüpfung zum Finanzdatensystem ein.

## <a name="selecting-print-control-in-a-row-definition"></a>Auswählen einer Drucksteuerelements einer Zeilendefinition
Sie können Drucksteuerungcodes für jede Spalte angeben, indem Sie die Zelle **Drucksteuerelement** verwenden.

### <a name="add-print-control-codes-to-a-report-row"></a>So fügen Sie Drucksteuerungscodes einer Berichtszeile hinzu

1.  Im Berichts-Designer öffnen Sie die zu ändernde Zeilendefinition.
2.  Doppelklicken Sie auf die Zelle **Drucksteuerung**.
3.  Wählen Sie im Dialogfeld **Drucksteuerung** einen Drucksteuerungscode aus, oder drücken Sie und halten Sie die STRG-Taste, um mehrere Codes auszuwählen. Sie können Drucksteuerungscodes auch direkt in die Zelle **Drucksteuerung** eingeben. Verwenden Sie Kommas, um mehrere Drucksteuerungscodes voneinander zu trennen.
4.  Wählen Sie alle bedingten Druckoptionen aus.
5.  Klicken Sie auf **OK**.

### <a name="regular-print-control-codes"></a>Reguläre Drucksteuerungscodes

In der folgenden Tabelle werden die regulären Drucksteuerungscodes für eine Zeilendefinition beschrieben.

| Drucksteuerungscodes | Interpretation des Drucksteuerungscodes         | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NP                 | Nicht druckbare Zeile                                 | Verhindert das Drucken von Beträgen in einem Bericht und schließt die Beträge von den Berechnungen aus. Um eine nicht druckbare Spalte in eine Berechnung einzubeziehen, verweisen Sie die Spalte in der Berechnungsformel direkt. Beispielsweise ist die nicht druckbare Zeile 240 in der folgenden Berechnung enthalten: **230+240+250**. Die nicht druckbare Zeile 240 ist aber in der folgenden Berechnung nicht enthalten: **230:250**. |
| CS                 | Währungssymbol; Währungsformat in dieser Zeile verwenden | Schließt das Währungssymbol in alle Nicht-Prozentsatzbeträge ein. Prozentuale Werte erhalten nie ein Währungssymbol.                                                                                                                                                                                                                                                                                                |
| XD                 | Zeile im Kontodetailbericht unterdrücken            | Unterdrückt die Anzeige von Konten in Kontodetailberichten und Buchungsdetailberichten. Diese Drucksteuerung ist hilfreich, wenn eine Zeile mehrere Konten umfasst, die nicht auf dem Kontodetailbericht oder dem Buchungsdetailbericht aufgeführt werden sollen.                                                                                                                                                           |
| X0                 | Zeile unterdrücken, falls nur Nullen                        | Schließt eine Zeile aus dem Bericht aus, wenn alle Zellen in dieser Zeile entweder leer sind oder Nullen enthalten. Die Drucksteuerung ist sinnvoll, wenn die Option zum Unterdrücken eines Nullsaldos nicht in der Berichtsdefinition aktiviert ist.                                                                                                                                                                                            |
| B0                 | Nullspalten leer lassen                         | Lässt Spalten in einer Zeile mit Nullbeträgen leer.                                                                                                                                                                                                                                                                                                                                                      |
| XR                 | Rollup unterdrücken                                  | Unterdrücken Sie einen Rollup. Wenn der Bericht eine Berichtsbaumstruktur verwendet, werden die Beträge in dieser Zeile nicht in folgende übergeordnete Knoten übertragen.                                                                                                                                                                                                                                                                               |
| SR                 | Runden unterdrücken                                | Verhindert, dass die Beträge in dieser Zeile gerundet werden.                                                                                                                                                                                                                                                                                                                                                          |
| XT                 | Zeile im Buchungsdetailbericht unterdrücken        | Unterdrückt die Anzeige von Transaktionen in Buchungsdetailberichten. Diese Drucksteuerung ist hilfreich, wenn eine Zeile mehrere Konten umfasst, die nicht auf dem Buchungsdetailbericht aufgeführt werden sollen.                                                                                                                                                                                                             |

### <a name="conditional-print-control-codes"></a>Bedingte Drucksteuerungscodes

In der folgenden Tabelle werden die bedingten Drucksteuerungscodes für eine Zeilendefinition beschrieben.

| Drucksteuerungscodes | Beschreibung                                  |
|--------------------|----------------------------------------------|
| (keine)             | Löschen Sie die bedingte Druckauswahl.       |
| DR                 | Druckt nur die Sollsalden für diese Zeile  |
| CR                 | Druckt nur die Habensalden für diese Zeile |

## <a name="column-restriction-cell-in-a-row-definition"></a>Spalteneinschränkungszelle in einer Zeilendefinition
Die Zelle **Spalteneinschränkung** in einer Zellendefinition hat mehrere Zwecke. Je nach Art der Zeile können Sie die Zelle **Spalteneinschränkung** verwenden, um eine der folgenden Funktionen anzugeben:

-   Die Zelle kann das Drucken von Zeilenbeträgen auf eine bestimmte Spalte beschränken. Diese Funktion ist hilfreich, wenn Sie eine tabellarische Bilanz erstellen.
-   Die Zelle kann die Spalte der Beträge angeben, die sortiert werden sollen.

## <a name="using-a-calculation-formula-in-a-row-definition"></a>Verwenden einer Berechnungsformel in einer Zeilendefinition
Eine Berechnungsformel in einer Zeilendefinition kann enthalten ** ** **+,-,\*** ** **, und/** ** Operatoren, und auch ** IF/THEN/ELSE ** Auszüge. Darüber hinaus kann eine Berechnung einzelne Zellen und absolute Beträge (Istzahlen, die in der Formel enthalten sind) beinhalten. Die Formel kann 1.024 Zeichen enthalten. Berechnungen können nicht auf die Zeilen angewendet werden, die Zellen vom Typ **Verknüpfung zu Finanzdimensionen** (FD) enthalten. Allerdings können Sie Berechnungen für fortlaufenden Zeilen einbeziehen, das Drucken dieser Zeilen unterdrücken und dann die Berechnungszeilen summieren.

### <a name="operators-in-a-calculation-formula"></a>Operatoren in einer Berechnungsformel

Eine Berechnungsformel verwendet komplexere Operatoren als eine Zeilengesamtformel. Sie können jedoch \*** ** und **/** Operatoren zusammen mit den zusätzlichen Operatoren verwenden, um (/) von Beträgen zu multiplizieren (\*) und Dividieren. Um einen Bereich oder eine Summe in einer Berechnungsformel zu verwenden, müssen Sie das At-Zeichen (@) vor dem Zeilencode verwenden, es sei denn, Sie nutzen eine Spalte in der Zeilendefinition. Wenn Sie beispielsweise den Betrag in Zeile 100 zum Betrag in Zeile 330 addieren möchten, können Sie die Zeilengesamtergebnis-Formel ** 100+330 ** oder die Berechnungsformel verwenden **@100@330. **Hinweis:** Sie müssen ein At-Zeichen(@) vor jedem Zeilencode verwenden, den Sie in einer Berechnungsformel verwenden. Andernfalls wird die Zahl als absoluter Betrag gelesen. Beispielsweise wird die Formel **@100+330 ** EUR 330 zum Betrag in Zeile 100. Wenn Sie eine Spalte in einer Berechnungsformel referenzieren, ist ein At-Zeichen (@) nicht erforderlich.

### <a name="create-a-calculation-formula"></a>Erstellen einer Berechnungsformel

1.  Im Berichts-Designer klicken Sie auf die **Zeilendefinitionen** und öffnen dann die Zeilendefinition, um sie zu ändern.
2.  Doppelklicken Sie auf die Zelle **Formatcode**, und wählen Sie dann **CAL** aus.
3.  Geben Sie in die Zelle **Verwandte Formeln/Zeilen/Einheiten** die Berechnungsformel ein.

### <a name="example-of-a-calculation-formula-for-specific-rows"></a>Beispiel für eine Berechnungsformel für bestimmte Zeilen

In diesem Beispiel bedeutet die Berechnungsformel **@100+@330** dass der Betrag in Zeile 100 zum Betrag in Zeile 330 addiert wird. Zeilengesamtergebnis-Formel ** Die 340+370 ** fügt den Betrag in Zeile 340 zum Betrag in Zeile 370. (Der Betrag in Zeile 370 wird der Betrag aus der Berechnungsformel.)

| Zeilencode | Beschreibung                 | Formatcode | Verwandte Formeln/Zeilen/Einheiten | Drucksteuerung | Zeilenmodifizierer | Mit Finanzdimensionen verknüpfen |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Barmittel am Periodenanfang |             |                            | NP            | BB//           | +Konto= 1100:1110\]\[       |
| 370      | Barmittel am Jahresanfang   | CAL         | @100+@330                  | NP            |              |                              |
| 400      | Barmittel am Periodenanfang | TOT         | 340+370                    |               |              |                              |

Wenn die Zeile in einer Zeilendefinition den Formatcode **CAL** hat und Sie geben eine mathematische Berechnung in die Zelle **Verwandte Formeln/Zeilen/Einheiten** ein, müssen Sie auch den Buchstaben der zugeordneten Spalte und Zeile im Bericht eingeben. Geben Sie z ** A.120 ein ** mit Spalte "A", Zeile 120 anzugeben. Sie können auch ein @-Zeichen verwenden "@) um alle Spalten anzugeben. Geben Sie z **@120ein ** um alle Spalten in Zeile 120 anzugeben. Mathematische Berechnungen, die nicht über einen Spaltenbuchstaben oder hat, ein @-Zeichens wird akzeptiert, werden als reelle Zahl angesehen. ** Hinweis: ** Wenn Sie einen Bezeichnungszeilencode verwenden, um auf eine Zeile zu verweisen, müssen Sie eine Periode (.) als Trennzeichen zwischen den Spaltenbuchstaben der Beschriftung und verwenden (beispielsweise, A.GROSS **\_MARGIN/A.SALES\_). Wenn Sie ein @-Zeichens verwenden, ist kein Trennzeichen erforderlich (z **@GROSS,\_MARGIN/@SALES**).

### <a name="example-of-a-calculation-formula-for-a-specific-column"></a>Beispiel für eine Berechnungsformel für eine bestimmte Spalte

In diesem Beispiel bedeutet die Berechnungsformel **E=C.340**, dass die Berechnung in der Zelle in der Spalte C, Zeile 340, ausschließlich auf Spalte E ausgeführt wird. **Hinweis:** Wenn Sie eine Spalte in einer Berechnungsformel referenzieren, ist kein At-Zeichen (@) erforderlich.

| Zeilencode | Beschreibung                 | Formatcode | Verwandte Formeln/Zeilen/Einheiten | Drucksteuerung | Zeilenmodifizierer | Mit Finanzdimensionen verknüpfen |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Barmittel am Periodenanfang |             |                            | NP            | BB//           | +Konto= 1100:1110\]\[       |
| 370      | Barmittel am Jahresanfang   | CAL         | E=C.340                    | NP            |              |                              |
| 400      | Barmittel am Periodenanfang | TOT         | 340+370                    |               |              |                              |

### <a name="modifying-a-number-in-selected-columns"></a>Ändern einer Zahl in ausgewählten Spalten

Wenn Sie eine Zahl oder eine Berechnung in einer Spalte einer bestimmten Zeile ändern, jedoch keine Auswirkungen auf andere Spalten im Bericht haben möchten, können Sie **CAL** (Berechnung) in der Spalte **Formatcode** der Zeilendefinition angeben.

-   Um eine Berechnung für alle (**FD**)-Spalten des Berichts vorzunehmen, geben Sie keine Spaltenzuweisung ein.
-   Wenn Sie eine Formel auf bestimmte Spalten einschränken möchten, geben Sie den Spaltenbuchstaben, einem Gleichheitszeichen ein (**=) und dann die Formel.
-   Sie können mehrere Spalten angeben. Wenn Sie ein At-Zeichen (@) mit bestimmter Spaltenplatzierung verwenden, wird das At-Zeichen (@) der Zeile zugeordnet.
-   Sie können mehrere Spaltenformeln in einer Zeile eingeben. Trennen Sie die Formeln durch Kommas.

### <a name="calculation-examples"></a>Berechnungsbeispiele

| Herstellkostenkalkulation            | Aktivität, die erstellt wird                                                                                                   |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| @130\*.75              | Für jede Spalte wird der Wert in Zeile 130 mit 0,75 multipliziert. Das Ergebnis wird in die aktuelle Zeile jeder Spalte übertragen. |
| B=@130\*.75            | Die gleiche Berechnung wird nun nur für Spalte B ausgeführt.                                                                      |
| A, B, C= (@100/@130\*.75) | A= () A.100/A.130\*.75 B= () B.100/B.130\*.75 C= (C.100/C.130\*.75)                                                           |

### <a name="ifthenelse-statements-in-a-row-definition"></a>IF/THEN/ELSE-Anweisungen in einer Zeilendefinition

**IF/THEN/ELSE**-Anweisungen können zu einer gültigen Berechnung hinzugefügt werden und mit dem Format **CAL** verwendet werden. Sie geben **IF/THEN/ELSE**-Berechnungsformeln in die Zelle in der Spalte **Verwandte Formeln/Zeilen/Einheiten** ein. ** IF/THEN/ELSE ** Berechnungsformeln verwenden das folgende Format: IF &lt;ELSE Formel der Formel für echten&gt; / &lt;falschen&gt; Auszugs &lt;THEN&gt; der ** ELSE &lt;Formel&gt;** Teil der Anweisung ist optional.

#### <a name="if-statements"></a>IF-Anweisungen

Die Anweisung, die der **IF**-Anweisung folgt, kann jede Anweisung sein, die als „true“ oder „false“ ausgewertet werden kann. Die Anweisung, die der **IF**-Anweisung folgt, kann eine einfache Auswertung oder eine komplexe Anweisung mit mehreren Ausdrücken enthalten. Nachfolgend finden Sie einige Beispiele:

-   ** IF A.2000&gt;** (einfache Auswertung)
-   ** IF A.2000&gt;UND, 000 A.20010&lt;** (komplexe Anweisung)
-   ** ODER IF A.20010000&gt;"(A.340/B.1200\*2) &lt;1200)** (Komplexer Anweisung, die mehreren Ausdrücken)

Der Begriff **Perioden** in einer **IF**-Anweisung gibt die Anzahl der Perioden für den Bericht an. Der Begriff wird in der Regel verwendet, um einen Durchschnitt für den Zeitraum Jahr bis dato zu berechnen. Wenn Sie beispielsweise einen Bericht für den Zeitraum 7 Jahr bis dato ausführen, bedeutet **B.150/Zeiträume**, dass der Wert in Zeile 150 der Spalte B durch 7 geteilt wird.

#### <a name="then-and-else-formulas"></a>THEN- und ELSE-Formeln

Die Formeln **THEN** und **ELSE** können eine beliebige gültige Berechnung sein, von sehr einfachen Wertzuweisungen bis hin zu komplexen Formeln. Beispielsweise können Sie den Auszug A.2000&gt;** IF, THEN A=B.200 ** Durchschnitt ", wenn der Wert in der Zelle in Spalte A aus Zeile " 200 "größer als 0 (null) ist, der den Wert aus der Zelle in Spalte B aus Zeile " 200 "in der Zelle in Spalte "A" der aktuellen Zeile.") Die vorangehende **IF/THEN**-Anweisung trägt einen Wert in eine Spalte der aktuellen Zeile ein. Sie können jedoch ein At-Zeichen (@) entweder in true/false-Anweisungen oder die Formel eingeben, um alle Spalten darzustellen. Nachfolgend einige andere Beispiele, die in den folgenden Abschnitten beschrieben werden:

-   ** IF A.200 &gt;0 THEN B.200 **: Wenn der Wert in Zelle "A.200" positiv ist, wird der Wert aus Zelle "B.200 " in jeder Spalte der aktuellen Zeile platziert.
-   ** IF A.200 &gt;0 THEN @200**: Wenn der Wert in Zelle "A.200" positiv ist, wird der Wert aus jeder Spalte in Zeile "200" in die entsprechende Spalte der aktuellen Zeile platziert.
-   ** IF @200&gt;0 THEN @200**: Wenn der Wert in Zeile "200 " der aktuellen Spalte positiv ist, wird der Wert aus Zeile "200 " in derselben Spalte der aktuellen Zeile platziert.

### <a name="restricting-a-calculation-to-a-reporting-unit-in-a-row-definition"></a>Beschränken einer Berechnung auf eine Berichtseinheit in einer Zeilendefinition

Um eine Berechnung auf eine einzelne Berichtseinheit in einer Berichtsbaumstruktur einzuschränken, damit für den Ergebnisbetrag kein Rollup zu einer höheren Einheit ausgeführt wird, können Sie den @Unit** ** Code in der Zeilen ** zugehörigen Formeln//Einheiten ** Zelle in der Zeilendefinition verwenden. ** Der @Unit** Code wird in Spalte B der Berichtsbaumstruktur aufgeführt, Einheits-Name ** **. Wenn der @Unit** ** Code verwenden, werden die Werte kein Rollup durchgeführt, aber die Berechnung wird auf jeder Ebene der Berichtsbaumstruktur bewertet. **Hinweis:** Zur Verwendung dieser Funktion, muss eine Berichtsbaumstruktur zu einer Zeilendefinition zugeordnet sein. Die Berechnungszeile kann auf eine Berechnungszeile oder Finanzdatenzeile verweisen. Die Berechnung wird in der Zelle **Verwandte Formeln/Zeilen/Einheiten** der Zeilendefinition und der Finanzdatentypeinschränkung erfasst. Die Berechnung muss eine bedingte Berechnung verwenden, die mit @Unit** IF ** Konstruktionen beginnt. Das folgende Beispiel: IF @Unit(" VERTRIEB THEN @100 ELSE 0 diese Berechnung den Betrag aus Zeile " 100 "in jede Spalte des Berichts, aber nur für die Einheit enthält. Wenn mehrere Einheiten SALES benannt sind, wird der Betrag in jeder dieser Einheiten angezeigt. Darüber hinaus kann Zeile 100 eine Finanzdatenzeile sein und kann als NP (kein Druck) definiert werden. In diesem Fall wird das Anzeigen des Betrags in allen Einheiten der Struktur verhindert. Sie können den Betrag auf eine einzelne Spalte des Berichts beschränken, beispielsweise Spalte H, indem Sie eine Spalteneinschränkung nutzen, um den Wert nur in dieser Spalte des Berichts zu drucken. Sie können auch **OR**-Kombinationen in eine **IF**-Anweisung einschließen. Das folgende Beispiel: IF @Unit(" VERTRIEB ODER ( @Unit) SALESWEST THEN 5 ELSE @100 Sie eine Einheit in einer Berechnungseinschränkung haben auf eine der folgenden Arten angeben können:

-   Geben Sie einen Einheitsnamen ein, um Einheiten mit einzubeziehen, die übereinstimmen. Beispielsweise ** IF @Unit(" VERTRIEB ** aktiviert die Berechnung für jede Einheit, die Person namens SALES, wenn mehrere Verkaufseinheiten in der Berichtsbaumstruktur angegeben ist.
-   Geben Sie den Unternehmens- und Einheitsnamen ein, um die Berechnung auf bestimmte Einheiten in einem bestimmten Unternehmen zu beschränken. Geben Sie z ein IF-Knoten ** @Unit(ACME: VERTRIEB **) die Berechnung zu Verkaufseinheiten im Unternehmen ACME einzuschränken.
-   Geben Sie den vollständigen Hierarchiecode aus der Berichtsbaumstruktur ein, um die Berechnung auf eine bestimmte Einheit zu beschränken. Geben Sie z ** IF @Unit(SUMMARY^ACME^WEST COAST^SALES **) ein. **Hinweis:** Klicken Sie zum Suchen des vollständigen Hierarchiecodes mit der rechten Maustaste in die Definition der Berichtsbaumstruktur, und wählen Sie dann **Berichtseinheitsidentifizierer (H-Code) kopieren** aus.

#### <a name="restrict-a-calculation-to-a-reporting-unit"></a>Beschränken einer Berechnung auf eine Berichtseinheit

1.  Im Berichts-Designer klicken Sie auf die **Zeilendefinitionen** und öffnen dann die Zeilendefinition, um sie zu ändern.
2.  Doppelklicken Sie auf die Zelle **Formatcode**, und wählen Sie dann **CAL** aus.
3.  Klicken Sie auf die zugehörige **//Formeln Zeilen Einheiten ** Zelle, und geben Sie anschließend eine bedingte Berechnung ein, die mit @Unit** IF ** Konstruktionen beginnt.

### <a name="ifthenelse-statements-in-a-column-definition"></a>IF/THEN/ELSE-Anweisungen in einer Spaltendefinition

Eine **IF/THEN/ELSE**-Anweisung ermöglicht, dass eine Berechnung von den Ergebnissen aus einer anderen Spalte abhängt. Sie können auf andere Spalten verweisen; ein Verweis auf eine Berichtszelle in der **IF**-Anweisung ist jedoch nicht möglich. Jede Berechnung muss auf die gesamte Spalte angewendet werden. Beispiel der Auszug ** IF B100&gt;THEN B ELSE C\*1.25 **, Durchschnitt ", wenn der Betrag in Spalte B mehr als 100 ist, setzen Sie den Wert aus Spalte B in CALC ** ** Spalte. Wenn der Betrag in der Spalte B nicht mehr als 100 ist, multipliziere den Wert in der Spalte C mit 1,25, und platziere das Ergebnis in die Spalte **KALK**." Nach der **IF**-Anweisung muss immer eine logische Anweisung folgen, die als „true“ oder „false“ ausgewertet werden kann. Die Formeln, die Sie für die Anweisungen **THEN** und **ELSE** verwenden, können Referenzen auf eine beliebige Zahl an Spalten enthalten. Die Formeln können so komplex sein, wie Sie es möchten. **Hinweis:** Sie können die Ergebnisse einer Berechnung in keine andere Spalte einfügen. Die Ergebnisse müssen in der Spalte sein, die die Formel enthält.


