---
title: Erweiterte Formatierungsoptionen in der Finanzberichterstellung
description: In diesem Thema werden erweiterte Formatierungsfunktionen beschrieben, einschließlich Filter, Einschränkungen, nicht druckbare Zeilen und bedingte Anweisungen in Berechnungen.
author: panolte
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 106571
ms.assetid: 895b5127-01d6-4495-b127-343387b743aa
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f0417ac1007fc94431aeb11d2464ee699e3f3441
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093161"
---
# <a name="advanced-formatting-options-in-financial-reporting"></a>Erweiterte Formatierungsoptionen in der Finanzberichterstellung

[!include [banner](../includes/banner.md)]

Wenn Sie einen Bericht in der Finanzberichterstellung erstellen, sind zusätzliche Formatierungsfunktionen, einschließlich Filter für Dimensionen, Einschränkungen für Spalten und Berichtseinheiten, nicht druckbare Zeilen und IF/THEN/ELSE-Anweisungen in Berechnungen, verfügbar.

In der folgenden Tabelle finden Sie die erweiterten Formatierungsfunktionen, die verfügbar sind, wenn Sie Berichte entwerfen.

| Funktion                   | Beschreibung |
|----------------------------|-------------|
| Dimensionsfilter           | Für den Zugriff auf bestimmte Datensätze können Sie Dimensionen in der Zeilendefinition und in der Spaltendefinition verwenden. Viele Berichte verwenden nur das natürliche Segment im Zeilenformat. Allerdings können Zeilen geändert werden, damit sie Dimensionswerte enthalten. Dimensionsfilter in der Spaltendefinition werden verwendet, um auf bestimmte Dimensionswerte zuzugreifen. |
| Einschränken der Berichtseinheit | Sie können eine Berichtszeile so einrichten, dass sie nur Informationen anzeigt, die mit einer bestimmten Berichtseinheit verknüpft sind. |
| Nicht druckbare (NP)-Zeilen     | Nicht druckbare Zeilen sind in einer Vielzahl von Berichten hilfreich. Wenn mehrere Berechnungen erforderlich sind, um einen Wert zu erhalten, können Sie diese Berechnungen im gedruckten Bericht ausblenden. Nicht druckbare Zeilen sind auch für die Problembehandlung von Berichtsdesigns und die erweiterte Zellenplatzierung hilfreich. |
| Spalteneinschränkung         | Die Spalteneinschränkung in der Zeilendefinition ist für das Ausblenden von Werten sinnvoll, die nur für einige Zeilen des Berichts relevant sind. Wenn Prozentrechnungen über eine Zeile ausgeführt werden, verhindert die Spalteneinschränkung, dass gesamte Spalten oder andere Spalten gedruckt werden, wenn diese Zahlen nicht relevant sind. |
| Spaltenumbruch               | Sie können Spaltenumbrüche zu einer Zeilendefinition hinzufügen, um Berichtsinformationen nebeneinander anzuzeigen. Sie können mehrere Spaltenumbrüche zu einer einzelnen Zeilendefinition hinzufügen. Die Spaltenüberschriften werden nach dem Spaltenumbruch oben über jeder Spalte wiederholt. Kommentare für einen Bericht werden zwischen den Spaltenumbrüchen angezeigt. |
| IF/THEN/ELSE-Anweisung     | Sie können Berechnungen in einer Zeilendefinition oder Spaltendefinition ändern. |
| Verwenden Sie einfache Anführungszeichen (") und ein kaufmännisches Und-Zeichen (&) für Dimensionswerte | Sie könen Dimensionswerte einschließlich das kaufännische Und-Zeichens für Berichtsentwürfe verwenden. |

## <a name="advanced-cell-placement"></a>Erweiterte Zellenplatzierung

Erweiterte Zellenplatzierung oder *Erzwingen* betrifft die Platzierung von bestimmten Werten in bestimmten Zellen. Beispielsweise wird das Erzwingen häufig verwendet, um den korrekten Saldo in einer Cashflowaufstellung zu verschieben. Sie können das Erzwingen für folgende Zwecke verwenden:

- Verschieben Sie Werte aus Microsoft Excel in bestimmte Zellen.
- Definieren Sie bestimmte Werte in einem Bericht vor.
- Ändern Sie Vorzeichen, indem Sie einen Wert von einer vorherigen Zelle kopieren und diesen Wert mit -1 multiplizieren.

> [!NOTE]
> In vielen Fällen müssen Sie Ihre Berichtsdefinition konfigurieren, sodass Spaltenberechnungen vor Zeilenberechnungen geleistet werden. Führen Sie zum Abschließen dieser Konfiguration die folgenden Schritte durch.
>
> 1. Im Berichts-Designer öffnen Sie die Berichtsdefinition.
> 2. Wählen Sie auf der Registerkarte **Einstellungen** unter **Berechnungspriorität** die Option **Erst Spalte, dann Zeile berechnen** aus.

## <a name="designing-the-report"></a>Gestalten des Berichts

Wenn Sie einen Bericht entwerfen, sollten Sie zunächst alle Detailzeilen erstellen, um sicherzustellen, dass die Werte wie erwartet miteinbezogen werden. Fügen Sie dann **NP** (kein Druck) Format überschreibt hinzu, um das Detail zu unterdrücken, das die endgültigen Werte umfasst.

> [!IMPORTANT]
> Wenn Sie den **CAL**-Formatcode in der Zeilendefinition verwenden, können Sie keinen Drilldown zu den Buchungsdetails durchführen.

Für das Erzwingen von Formeln verwenden Sie das folgende Format: &lt;Zielspalte&gt;=&lt;Ursprungsspalte&gt;.&lt;Zeilencode&gt;. Trennen Sie alle zusätzlichen Platzierungen für eine Zeile durch ein Komma und eine Leerstelle. Beispiel: D=C.190,E=C.100

## <a name="examples-of-advanced-formatting-options"></a>Beispiele von erweiterten Formatierungsoptionen

Das folgenden Beispiel zeigt, wie die Zeilendefinition und die Spaltendefinition formatiert wird, um einen grundlegenden Cashflowbericht (Beispiel 1) und einen statistischen Bericht (Beispiel 2) zu erzwingen.

### <a name="example-1-basic-forcing"></a>Beispiel 1: Grundlegendes Erzwingen

Die folgende Tabelle enthält ein Beispiel einer Zeilendefinition, die das grundlegende Erzwingen verwendet.

| Zeilencode |           Beschreibung            | Formatcode | Verwandte Formeln/Zeilen/Einheiten |        Zeilenmodifizierer        | Verknüpfen mit Finanzdimensionen |
|----------|----------------------------------|-------------|-----------------------------|----------------------------|------------------------------|
| 100      | Barmittel am Periodenanfang (NP) |             |                             | Kontomodifizierer = \[/BB\] | +Segment2 = \[1100\]         |
| 130      | Mittel am Anfang der Periode      | CAL         | C=C.100,F=D.100             |                            |                              |
| 160      |                                  |             |                             |                            |                              |
| 190      |                                  |             |                             |                            |                              |

> [!NOTE]
> Leere Spalten wurden von der vorherigen Tabelle zu Präsentationszwecken entfernt: Format-Außerkraftsetzung, normaler Saldo, Drucksteuerung, Spalten-Einschränkung werden nicht angezeigt.

Die folgende Tabelle enthält ein Beispiel einer Spaltendefinition, die das grundlegende Erzwingen in einer Zeile verwendet.

|           Formate             | K   | Mrd    | C        | S      | E      | Fr    |
|------------------------------|-----|------|----------|--------|--------|------|
| Überschrift 1                     |     |      |          |        |        |      |
| Überschrift 2                     | K   | Mrd    | C        | S      | E      | Fr    |
| Überschrift 3                     |     |      |          |        |        |      |
| Spaltentyp                  | ROW | DESC | FD       | FD     | FD     | KALK |
| Buchcode/Attributkategorie |     |      | ISTWERT   | ISTWERT | ISTWERT |      |
| Geschäftsjahr                  |     |      | BASIS     | BASIS   | BASIS   |      |
| Zeitraum                       |     |      | BASIS     | BASIS   | BASIS   |      |
| Abgedeckte Zeiträume              |     |      | PERIODIC | YTD/BB | Jahr bis dato    |      |
| Formel                      |     |      |          |        |        | E-D  |
| Spaltenbreite                 | 5   | 30   | 14       | 14     | 14     | 14   |

### <a name="example-2-statistical-reports"></a>Beispiel 2: Statistische Berichte

Die folgende Tabelle enthält ein Beispiel einer Zeilendefinition, die das grundlegende Erzwingen für einen statistischen Bericht verwendet.

| Zeilencode | Beschreibung               | Formatcode | Verwandte Formeln/Zeilen/Einheiten     | Formataußerkraftsetzung      | Standardsaldo | Verknüpfen mit Finanzdimensionen               |
|----------|---------------------------|-------------|---------------------------------|----------------------|----------------|--------------------------------------------|
| 50       | Statistische Daten   | ANM         |                                 |                      |                |                                            |
| 100      | Mitarbeiterzahl - US            | CAL         | 4                               | \#\#\#0.;($\#\#\#0.) |                |                                            |
| 115      | Mitarbeiterzahl - International | CAL         | 11                              | \#\#\#0.;($\#\#\#0.) |                |                                            |
| 130      |                           |             |                                 |                      |                |                                            |
| 190      | Umsatz US                  |             |                                 |                      | C:              | +Segment2 = \[41\*\], Segment3 = \[00\]    |
| 220      | Internationaler Umsatz       |             |                                 |                      | C:              | +Segment2 = \[41\*\], Segment3 = \[01:99\] |
| 250      |                           |             |                                 |                      |                |                                            |
| 280      |                           |             |                                 |                      |                |                                            |
| 310      | Umsatz US                  | CAL         | D=C.190,E=C.100,F=(C.100/C.190) |                      |                |                                            |
| 340      | Internationale Umsätze       | CAL         | D=C.220,E=C115,F=(C.220/C.115)  |                      |                |                                            |

> [!NOTE]
> Leere Spalten wurden von der vorherigen Tabelle für Präsentationszwecke entfernt: Die Saplten Drucksteuerung, Spalteneinschränkung und Zeilenbearbeiter werden nicht angezeigt.

Die folgende Tabelle enthält ein Beispiel einer Spaltendefinition, die das grundlegende Erzwingen für einen statistischen Bericht verwendet.

|    Formate                    | K   | Mrd    | C      | S            | E     | Fr            |
|------------------------------|-----|------|--------|--------------|-------|--------------|
| Überschrift 1                     | K   | Mrd    | C      | S            | E     | Fr            |
| Überschrift 2                     | -   | -    | Jahr bis dato    | Jährlicher Umsatz | Personal | $ pro Person |
| Kopfzeile 3                     |     |      |        |              |       |              |
| Spaltentyp                  | ZEILE | DESC | FD     | KALK         | KALK  | KALK         |
| Buchcode/Attributkategorie |     |      | ISTWERT |              |       |              |
| Geschäftsjahr                  |     |      | BASE   |              |       |              |
| Zeitraum                       |     |      | BASE   |              |       |              |
| Abgedeckte Perioden              |     |      | Jahr bis dato    |              |       |              |
| Formel                      |     |      |        |              |       | E-D          |
| Spaltenbreite                 | 5   | 30   | 14     | 14           | 14    | 14           |

## <a name="restricting-a-row-to-a-specific-reporting-unit"></a>Beschränken einer Zeile auf eine bestimmte Berichtseinheit

Wenn eine Berichtszeile auf eine bestimmte Berichtseinheit beschränkt ist, zeigt die Zeile die verknüpften Daten nur für die benannte Berichtseinheit und ignoriert die Daten für andere Berichtseinheiten in der Berichtsbaumstruktur. So können Sie eine Zeile erstellen, die Details für die gesamten Betriebskosten für eine bestimmte Abteilung bereitstellt. Ihr Bericht enthält möglicherweise doppelte Daten, wenn der Bericht sowohl die Berichtsbaumstruktur und eine Zeilendefinition enthält, die mehr als das natürliche Konto besitzt. Sie haben beispielsweise eine Berichtsbaumstruktur, die die sechs Abteilungen in der Organisation aufführt, und Sie haben auch eine Zeilendefinition, die eine bestimmte Kombination aus einem Konto und einer Abteilung in der Zeile aufführt. Wenn Sie den Bericht generieren, wird die bestimmte Kombination aus Konto und Abteilung für jede Ebene der Berichtsbaumstruktur gedruckt, auch wenn diese Abteilung möglicherweise nicht mit dem, was in der Struktur ist, übereinstimmt. Dieses Verhalten tritt auf, da die Zeile überschreibt, was in der Regel von der Berichtsdefinition gefiltert wird. Eine Möglichkeit, doppelte Daten zu vermeiden, besteht darin, eine Zeile auf eine bestimmte Berichtseinheit zu beschränken.

> [!NOTE]
> Wenn eine Zeile Dimensionen umfasst und Sie beschränken diese Zeile auf eine untergeordnete Berichtseinheit, wird der Zeilenbetrag für diese untergeordnete Einheit und deren übergeordnete Einheiten mit eingeschlossen. Eine Duplizierung erfolgt nicht.

### <a name="restrict-a-row-to-a-reporting-unit"></a>Beschränken einer Zeile auf eine bestimmte Berichtseinheit

1. Im Berichts-Designer klicken Sie auf die **Zeilendefinitionen** und wählen dann eine Zeilendefinition, um sie zu ändern.
2. Doppelklicken Sie auf die entsprechende Zelle **Verwandte Formeln/Zeilen/Einheiten**.
3. Wählen Sie im Dialogfeld **Auswahl der Berichtseinheit** im Feld **Berichtsbaumstruktur** die Struktur aus, die in der Berichtsdefinition zugewiesen ist.
4. Wählen Sie eine Berichtseinheit, und klicken Sie anschließend auf **OK**. Die Einschränkung wird in der Zelle der Zeilendefinition angezeigt.
5. Doppelklicken Sie auf die Zelle in der Spalte **Verknüpfung zu Finanzdimensionen** der beschränkten Zeile, und geben Sie dann die Verknüpfung zum Finanzdatensystem ein.

## <a name="selecting-print-control-in-a-row-definition"></a>Auswählen einer Drucksteuerelements einer Zeilendefinition

Sie können Drucksteuerungcodes für jede Spalte angeben, indem Sie die Zelle **Drucksteuerelement** verwenden.

### <a name="add-print-control-codes-to-a-report-row"></a>So fügen Sie Drucksteuerungscodes einer Berichtszeile hinzu

1. Öffnen Sie im Berichts-Designer die zu bearbeitende Zeilendefinition.
2. Doppelklicken Sie auf die Zelle **Drucksteuerung**.
3. Wählen Sie im Dialogfeld **Drucksteuerung** einen Drucksteuerungscode aus, oder drücken Sie und halten Sie die STRG-Taste, um mehrere Codes auszuwählen. Sie können Drucksteuerungscodes auch direkt in die Zelle **Drucksteuerung** eingeben. Verwenden Sie Kommas, um mehrere Drucksteuerungscodes voneinander zu trennen.
4. Wählen Sie alle bedingten Druckoptionen aus.
5. Klicken Sie auf **OK**.

### <a name="regular-print-control-codes"></a>Reguläre Drucksteuerungscodes

In der folgenden Tabelle werden die regulären Drucksteuerungscodes für eine Zeilendefinition beschrieben.

| Drucksteuerungscodes | Interpretation des Drucksteuerungscodes         | Beschreibung |
|--------------------|--------------------------------------------------|-------------|
| NP                 | Nicht druckbare Zeile                                 | Verhindert das Drucken von Beträgen in einem Bericht und schließt die Beträge von den Berechnungen aus. Um eine nicht druckbare Spalte in eine Berechnung einzubeziehen, verweisen Sie die Spalte in der Berechnungsformel direkt. Beispielsweise ist die nicht druckbare Zeile 240 in der folgenden Berechnung enthalten: **230+240+250**. Die nicht druckbare Zeile 240 ist aber in der folgenden Berechnung nicht enthalten: **230:250**. |
| CS                 | Währungssymbol; Währungsformat in dieser Zeile verwenden | Schließt das Währungssymbol in alle Nicht-Prozentsatzbeträge ein. Prozentuale Werte erhalten nie ein Währungssymbol. |
| XD                 | Zeile im Kontodetailbericht unterdrücken            | Unterdrückt die Anzeige von Konten in Kontodetailberichten und Buchungsdetailberichten. Diese Drucksteuerung ist hilfreich, wenn eine Zeile mehrere Konten umfasst, die nicht auf dem Kontodetailbericht oder dem Buchungsdetailbericht aufgeführt werden sollen. |
| X0                 | Zeile unterdrücken, falls nur Nullen                        | Schließt eine Zeile aus dem Bericht aus, wenn alle Zellen in dieser Zeile entweder leer sind oder Nullen enthalten. Die Drucksteuerung ist sinnvoll, wenn die Option zum Unterdrücken eines Nullsaldos nicht in der Berichtsdefinition aktiviert ist. |
| B0                 | Nullspalten leer lassen                         | Lässt Spalten in einer Zeile mit Nullbeträgen leer. |
| XR                 | Rollup unterdrücken                                  | Unterdrücken Sie einen Rollup. Wenn der Bericht eine Berichtsbaumstruktur verwendet, werden die Beträge in dieser Zeile nicht in folgende übergeordnete Knoten übertragen. |
| SR                 | Runden unterdrücken                                | Verhindert, dass die Beträge in dieser Zeile gerundet werden. |
| XT                 | Zeile im Buchungsdetailbericht unterdrücken        | Unterdrückt die Anzeige von Transaktionen in Buchungsdetailberichten. Diese Drucksteuerung ist hilfreich, wenn eine Zeile mehrere Konten umfasst, die nicht auf dem Buchungsdetailbericht aufgeführt werden sollen. |

### <a name="conditional-print-control-codes"></a>Bedingte Drucksteuerungscodes

In der folgenden Tabelle werden die bedingten Drucksteuerungscodes für eine Zeilendefinition beschrieben.

| Drucksteuerungscodes | Beschreibung                                  |
|--------------------|----------------------------------------------|
| (keine)             | Löschen Sie die bedingte Druckauswahl.       |
| DR                 | Druckt nur die Sollsalden für diese Zeile  |
| CR                 | Druckt nur die Habensalden für diese Zeile |

## <a name="column-restriction-cell-in-a-row-definition"></a>Spalteneinschränkungszelle in einer Zeilendefinition

Die Zelle **Spalteneinschränkung** in einer Zellendefinition hat mehrere Zwecke. Je nach Art der Zeile können Sie die Zelle **Spalteneinschränkung** verwenden, um eine der folgenden Funktionen anzugeben:

- Die Zelle kann das Drucken von Zeilenbeträgen auf eine bestimmte Spalte beschränken. Diese Funktion ist hilfreich, wenn Sie eine tabellarische Bilanz erstellen.
- Die Zelle kann die Spalte der Beträge angeben, die sortiert werden sollen.

## <a name="using-a-calculation-formula-in-a-row-definition"></a>Verwenden einer Berechnungsformel in einer Zeilendefinition

Eine Berechnungsformel in einer Zeilendefinition kann die Operatoren **+**, **-**, **\**_ und _*/** sowie die Anweisungen **IF/THEN/ELSE** enthalten. Darüber hinaus kann eine Berechnung einzelne Zellen und absolute Beträge (Istzahlen, die in der Formel enthalten sind) beinhalten. Die Formel kann 1.024 Zeichen enthalten. Berechnungen können nicht auf die Zeilen angewendet werden, die Zellen vom Typ **Verknüpfung zu Finanzdimensionen** (FD) enthalten. Allerdings können Sie Berechnungen für fortlaufenden Zeilen einbeziehen, das Drucken dieser Zeilen unterdrücken und dann die Berechnungszeilen summieren.

### <a name="operators-in-a-calculation-formula"></a>Operatoren in einer Berechnungsformel

Eine Berechnungsformel verwendet komplexere Operatoren als eine Zeilengesamtformel. Sie können jedoch die Operatoren **\**_ und _*/** zusammen mit den zusätzlichen Operatoren zum Multiplizieren (\*) und Dividieren (/) von Beträgen verwenden. Um einen Bereich oder eine Summe in einer Berechnungsformel zu verwenden, müssen Sie das At-Zeichen (@) vor dem Zeilencode verwenden, es sei denn, Sie nutzen eine Spalte in der Zeilendefinition. Um beispielsweise den Betrag in Zeile 100 dem Betrag in Zeile 330 hinzuzufügen, können Sie die Zeilengesamtformel **100+330** oder die Berechnungsformel **@100+@330** verwenden.

> [!NOTE]
> Sie müssen ein At-Zeichen(@) vor jedem Zeilencode verwenden, den Sie in einer Berechnungsformel verwenden. Andernfalls wird die Zahl als absoluter Betrag gelesen. Beispielsweise fügt die Formel **@100+330** dem Betrag in Zeile 100 330 EUR hinzu. Wenn Sie eine Spalte in einer Berechnungsformel referenzieren, ist ein At-Zeichen (@) nicht erforderlich.

### <a name="create-a-calculation-formula"></a>Erstellen einer Berechnungsformel

1. Im Berichts-Designer klicken Sie auf die **Zeilendefinitionen** und öffnen dann die Zeilendefinition, um sie zu ändern.
2. Doppelklicken Sie auf die Zelle **Formatcode**, und wählen Sie dann **CAL** aus.
3. Geben Sie in die Zelle **Verwandte Formeln/Zeilen/Einheiten** die Berechnungsformel ein.

### <a name="example-of-a-calculation-formula-for-specific-rows"></a>Beispiel für eine Berechnungsformel für bestimmte Zeilen

In diesem Beispiel bedeutet die Berechnungsformel **@100+@330**, dass der Betrag in Zeile 100 zum Betrag in Zeile 330 addiert wird. Zeilengesamtergebnis-Formel **340+370** fügt den Betrag in Zeile 340 zum Betrag in Zeile 370. (Der Betrag in Zeile 370 wird der Betrag aus der Berechnungsformel.)

| Zeilencode | Beschreibung                 | Formatcode | Verwandte Formeln/Zeilen/Einheiten | Drucksteuerung | Zeilenmodifizierer | Mit Finanzdimensionen verknüpfen |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Mittel am Anfang der Periode |             |                            | ND            | BB           | +Konto=\[1100:1110\]       |
| 370      | Mittel zu Jahresbeginn   | CAL         | @100+@330                  | ND            |              |                              |
| 400      | Mittel am Anfang der Periode | TOT         | 340+370                    |               |              |                              |

Wenn die Zeile in einer Zeilendefinition den Formatcode **CAL** hat und Sie geben eine mathematische Berechnung in die Zelle **Verwandte Formeln/Zeilen/Einheiten** ein, müssen Sie auch den Buchstaben der zugeordneten Spalte und Zeile im Bericht eingeben. Geben Sie **A.120** ein, um Spalte "A", Zeile 120 anzugeben. Sie können auch ein @-Zeichen verwenden, um alle Spalten anzugeben. Geben Sie z. B. **@120** ein, um alle Spalten in Zeile 120 anzugeben. Mathematische Berechnungen, die nicht über einen Spaltenbuchstaben oder ein @-Zeichens erfolgen werden als reelle Zahl angesehen.

> [!NOTE]
> Wenn Sie einen Bezeichungszeilencode nutzen, um eine Zeile zu referenzieren, müssen Sie einen Punkt (.) als Trennzeichen zwischen dem Spaltenbuchstaben und der Bezeichnung verwenden (beispielsweise **A.GROSS\_MARGIN/A.SALES**). Wenn Sie ein At-Zeichen (@) verwenden, ist ein Trennzeichen nicht erforderlich (z.B. **\@GROSS\_MARGIN/@SALES**).

### <a name="example-of-a-calculation-formula-for-a-specific-column"></a>Beispiel für eine Berechnungsformel für eine bestimmte Spalte

In diesem Beispiel bedeutet die Berechnungsformel **E=C.340**, dass die Berechnung in der Zelle in Spalte C, Zeile 340, ausschließlich auf Spalte E ausgeführt wird.

> [!NOTE]
> Wenn Sie eine Spalte in einer Berechnungsformel referenzieren, ist ein At-Zeichen (@) nicht erforderlich.

| Zeilencode | Beschreibung                 | Formatcode | Verwandte Formeln/Zeilen/Einheiten | Drucksteuerung | Zeilenmodifizierer | Mit Finanzdimensionen verknüpfen |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Barmittel am Periodenanfang |             |                            | NP            | BB//           | +Konto=\[1100:1110\]       |
| 370      | Barmittel am Jahresanfang   | CAL         | E=C.340                    | NP            |              |                              |
| 400      | Barmittel am Periodenanfang | TOT         | 340+370                    |               |              |                              |

### <a name="modifying-a-number-in-selected-columns"></a>Ändern einer Zahl in ausgewählten Spalten

Wenn Sie eine Zahl oder eine Berechnung in einer Spalte einer bestimmten Zeile ändern, jedoch keine Auswirkungen auf andere Spalten im Bericht haben möchten, können Sie **CAL** (Berechnung) in der Spalte **Formatcode** der Zeilendefinition angeben.

- Um eine Berechnung für alle (**FD**)-Spalten des Berichts vorzunehmen, geben Sie keine Spaltenzuweisung ein.
- Um eine Formel auf bestimmte Spalten einzuschränken, geben Sie den Spaltenbuchstaben, ein Gleichheitszeichen (**=**) und dann die Formel ein.
- Sie können mehrere Spalten angeben. Wenn Sie ein At-Zeichen (@) mit bestimmter Spaltenplatzierung verwenden, wird das At-Zeichen (@) der Zeile zugeordnet.
- Sie können mehrere Spaltenformeln in einer Zeile eingeben. Trennen Sie die Formeln durch Kommas.

### <a name="calculation-examples"></a>Berechnungsbeispiele

| Herstellkostenkalkulation            | Aktivität, die erstellt wird                                                                                                   |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| @130\*.75              | Für jede Spalte wird der Wert in Zeile 130 mit 0,75 multipliziert. Das Ergebnis wird in die aktuelle Zeile jeder Spalte übertragen. |
| B=@130\*.75            | Die gleiche Berechnung wird nun nur für Spalte B ausgeführt.                                                                      |
| A,B,C=(@100/@130)\*.75 | A=(A.100/A.130)\*.75 B=(B.100/B.130)\*.75 C=(C.100/C.130)\*.75                                                           |

### <a name="ifthenelse-statements-in-a-row-definition"></a>IF/THEN/ELSE-Anweisungen in einer Zeilendefinition

**IF/THEN/ELSE**-Anweisungen können zu einer gültigen Berechnung hinzugefügt werden und mit dem Format **CAL** verwendet werden. Sie geben **IF/THEN/ELSE**-Berechnungsformeln in die Zelle in der Spalte **Verwandte Formeln/Zeilen/Einheiten** ein. **IF/THEN/ELSE** Berechnungsformeln nutzen das folgende Format: IF &lt;true/false statement&gt; THEN &lt;formula&gt; ELSE &lt;formula&gt; Der **ELSE &lt;Formel&gt;** tiel des Berichts ist optional.

#### <a name="if-statements"></a>IF-Anweisungen

Die Anweisung, die der **IF**-Anweisung folgt, kann jede Anweisung sein, die als „true“ oder „false“ ausgewertet werden kann. Die Anweisung, die der **IF**-Anweisung folgt, kann eine einfache Auswertung oder eine komplexe Anweisung mit mehreren Ausdrücken enthalten. Nachfolgend finden Sie einige Beispiele:

- **IF A.200&gt;0** (Einfache Auswertung)
- **IF A.200&gt;0 AND A.200&lt;10,000** (Komplexe Anweisung)
- **IF A.200&gt;10000 OR ((A.340/B.1200)\*2 &lt;1200)** (Komplexe Anweisung mit mehreren Ausdrücken)

Der Begriff **Perioden** in einer **IF**-Anweisung gibt die Anzahl der Perioden für den Bericht an. Der Begriff wird in der Regel verwendet, um einen Durchschnitt für den Zeitraum Jahr bis dato zu berechnen. Wenn Sie beispielsweise einen Bericht für den Zeitraum 7 Jahr bis dato ausführen, bedeutet **B.150/Zeiträume**, dass der Wert in Zeile 150 der Spalte B durch 7 geteilt wird.

#### <a name="then-and-else-formulas"></a>THEN- und ELSE-Formeln

Die Formeln **THEN** und **ELSE** können eine beliebige gültige Berechnung sein, von sehr einfachen Wertzuweisungen bis hin zu komplexen Formeln. Beispielsweise bedeutet die Anweisung **IF A.200&gt;0 THEN A=B.200** "wenn der Wert in der Zelle in Spalte A der Zeile 200 größer ist als 0 (Null), übertrage den Wert der Zelle in Spalte B der Zeile 200 in die Zelle in Spalte A der aktuellen Zeile“. Die vorangehende **IF/THEN**-Anweisung trägt einen Wert in eine Spalte der aktuellen Zeile ein. Sie können jedoch ein At-Zeichen (@) entweder in true/false-Anweisungen oder die Formel eingeben, um alle Spalten darzustellen. Nachfolgend einige andere Beispiele, die in den folgenden Abschnitten beschrieben werden:

- **IF A.200 &gt;0 THEN B.200**: Wenn der Wert in der Zelle A.200 positiv ist, wird der Wert aus der Zelle B.200 in jede Spalte der aktuellen Zeile platziert.
- **IF A.200 &gt;0 THEN @200**: Wenn der Wert in der Zelle A.200 positiv ist, wird der Wert aus jeder Spalte in Zeile 200 in die entsprechende Spalte in der aktuellen Zeile platziert.
- **IF @200 &gt;0 THEN @200**: Wenn der Wert in Zeile 200 der aktuellen Spalte positiv ist, wird der Wert von Zeile 200 in die gleiche Spalte in der aktuellen Zeile platziert.

### <a name="restricting-a-calculation-to-a-reporting-unit-in-a-row-definition"></a>Beschränken einer Berechnung auf eine Berichtseinheit in einer Zeilendefinition

Um eine Berechnung auf eine einzelne Berichtseinheit in einer Berichtsbaumstruktur zu beschränken, sodass für den resultierenden Betrag kein Rollup zu einer Einheit auf höherer Ebene durchgeführt wird, verwenden Sie in der Zeilendefinition den Code **\@Unit** in der Zelle **Verwandte Formeln/Zeilen/Einheiten**. Der Code **\@Unit** wird in Spalte B der Berichtsbaumstruktur **Einheitenname** aufgeführt. Wenn Sie den Code **\@Unit** verwenden, wird für die Werte kein Rollup durchgeführt, sondern die Berechnung wird auf allen Ebenen der Berichtsbaumstruktur ausgewertet.

> [!NOTE]
> Zur Verwendung dieser Funktion, muss eine Berichtsbaumstruktur zu einer Zeilendefinition zugeordnet sein.

Die Berechnungszeile kann auf eine Berechnungszeile oder Finanzdatenzeile verweisen. Die Berechnung wird in der Zelle **Verwandte Formeln/Zeilen/Einheiten** der Zeilendefinition und der Finanzdatentypeinschränkung erfasst. Die Berechnung muss eine bedingte Berechnung verwenden, die mit einer **IF @Unit**-Konstruktion beginnt. Beispiel: IF @Unit(SALES) THEN @100 ELSE 0. Diese Berechnung enthält die Beträge aus Zeile 100 in jeder Spalte des Berichts, aber nur für die Verkaufseinheit. Wenn mehrere Einheiten SALES benannt sind, wird der Betrag in jeder dieser Einheiten angezeigt. Darüber hinaus kann Zeile 100 eine Finanzdatenzeile sein und kann als NP (kein Druck) definiert werden. In diesem Fall wird das Anzeigen des Betrags in allen Einheiten der Struktur verhindert. Sie können den Betrag auf eine einzelne Spalte des Berichts beschränken, beispielsweise Spalte H, indem Sie eine Spalteneinschränkung nutzen, um den Wert nur in dieser Spalte des Berichts zu drucken. Sie können auch **OR**-Kombinationen in eine **IF**-Anweisung einschließen. Beispiel: IF @Unit(SALES) OR @Unit(SALESWEST) THEN 5 ELSE @100 Sie können eine Einheit in einer Berechnungstypeinschränkung auf verschiedenen Wegen angeben:

- Geben Sie einen Einheitsnamen ein, um Einheiten mit einzubeziehen, die übereinstimmen. Beispiel: **IF @UNIT(SALES)** ermöglicht die Berechnung für jede Einheit namens SALES, auch wenn es mehrere SALES-Einheiten (Verkaufseinheiten) in der Berichtsbaumstruktur gibt.
- Geben Sie den Unternehmens- und Einheitsnamen ein, um die Berechnung auf bestimmte Einheiten in einem bestimmten Unternehmen zu beschränken. Beispiel: Geben Sie **IF @Unit(ACME:SALES**) ein, um die Berechnung auf Verkaufseinheiten im Unternehmen ACME zu beschränken.
- Geben Sie den vollständigen Hierarchiecode aus der Berichtsbaumstruktur ein, um die Berechnung auf eine bestimmte Einheit zu beschränken. Geben Sie beispielsweise **IF @Unit(SUMMARY^ACME^WEST COAST^SALES)** ein.

> [!NOTE]
> Um den vollständigen Hierarchiecode anzuzeigen, klicken Sie mit der rechten Maustaste in die Berichtsbaumstrukturdefinition, und wählen Sie dann **Berichtseinheitsidentifizierer (H-Code) kopieren** aus.

#### <a name="restrict-a-calculation-to-a-reporting-unit"></a>Einschränken einer Berechnung auf eine Berichtseinheit

1. Klicken Sie im Berichts-Designer auf **Zeilendefinitionen**, und öffnen Sie dann die zu ändernde Zeilendefinition.
2. Doppelklicken Sie auf die Zelle **Formatcode**, und wählen Sie dann **CAL** aus.
3. Klicken Sie auf die Zelle **Verwandte Formeln/Zeilen/Einheiten**, und geben Sie dann eine bedingte Berechnung ein, die mit einer **IF @Unit**-Konstruktion beginnt.

### <a name="ifthenelse-statements-in-a-column-definition"></a>IF/THEN/ELSE-Anweisungen in einer Spaltendefinition

Eine **IF/THEN/ELSE**-Anweisung ermöglicht, dass eine Berechnung von den Ergebnissen aus einer anderen Spalte abhängt. Sie können auf andere Spalten verweisen; ein Verweis auf eine Berichtszelle in der **IF**-Anweisung ist jedoch nicht möglich. Jede Berechnung muss auf die gesamte Spalte angewendet werden. Die Anweisung **IF B&gt;100 THEN B ELSE C\*1.25** bedeutet beispielsweise „Wenn der Betrag in Spalte B größer ist als 100, platziere den Wert aus der Spalte B in die Spalte **CALC**. Wenn der Betrag in der Spalte B nicht mehr als 100 ist, multipliziere den Wert in der Spalte C mit 1,25, und platziere das Ergebnis in die Spalte **KALK**." Nach der **IF**-Anweisung muss immer eine logische Anweisung folgen, die als „true“ oder „false“ ausgewertet werden kann. Die Formeln, die Sie für die Anweisungen **THEN** und **ELSE** verwenden, können Referenzen auf eine beliebige Zahl an Spalten enthalten. Die Formeln können so komplex sein, wie Sie es möchten.

> [!NOTE]
> Sie können die Ergebnisse einer Berechnung in keine andere Spalte einfügen. Die Ergebnisse müssen in der Spalte sein, die die Formel enthält.

#### <a name="use-single-quotes-and-an-ampersand-for-dimension-values-in-a-row-column-or-tree"></a>Verwenden Sie einfache Anführungszeichen (") und ein kaufmännisches Und-Zeichen (&) in einer Zeile, Spalte oder Struktur

Sie können Berichte mithilfe von Dimensionswerten entwerfen, die ein kaufmännisches Und-Zeichen (&) enthalten.

Innerhalb eines beliebigen Feld **Link zur Finanzdimension** können Sie einen Wert wie beispielsweise **GuV** eingeben. Das Einschließen von einfachen Anführungszeichen ('') auf beiden Seiten des Dimensionswert gibt an, dass Sie den Literalwert verwenden, wie beispielsweise das Einschließen des kaufmännischen Und-Zeichens (&).
