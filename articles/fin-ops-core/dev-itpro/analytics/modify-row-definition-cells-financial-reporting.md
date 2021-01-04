---
title: Ändern von Zeilendefinitionszellen
description: Dieses Thema beschreibt die Informationen, die für jede Zelle in einer Zeilendefinition eines Finanzberichts benötigt werden und erläutert, wie diese Informationen eingegeben werden.
author: ShylaThompson
manager: AnnBe
ms.date: 02/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 58881
ms.assetid: 0af492df-a84e-450c-8045-78ef1211abaf
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 92d03f08fc5e34402f10068ed770b1f724cfd3a8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685858"
---
# <a name="modify-row-definition-cells"></a>Ändern von Zeilendefinitionszellen

[!include [banner](../includes/banner.md)]

Dieses Thema beschreibt die Informationen, die für jede Zelle in einer Zeilendefinition eines Finanzberichts benötigt werden und erläutert, wie diese Informationen eingegeben werden.

## <a name="specify-a-row-code-in-a-row-definition"></a>Angeben eines Zeilencodes in einer Zeilendefinition

In den Zeilendefinitionen bestimmen die Zahlen bzw. Beschriftungen in der Zelle **Zeilencode** jede Position in der Zeilendefinition. Sie können den Zeilencode angeben, um auf Daten in Berechnungen und Summen zu verweisen.

### <a name="row-code-requirements"></a>Zeilencodeanforderungen

Ein Zeilencode ist für alle Zeilen erforderlich. Sie können numerische, alphanumerische und nicht festgelegte (leere) Zeilencodes in einer Zeilendefinition Eingabe kombinieren. Der Zeilencode kann eine beliebige positive ganze Zahl (unter 100.000.000) oder eine beschreibende Bezeichnung der Zeile sein. Eine beschreibende Bezeichnung muss diesen Regeln folgen:

- Die Beschriftung muss mit einem Buchstaben beginnen (a bis z oder A bis Z) und kann eine beliebige Kombination aus Nummern und Buchstaben von bis zu 16 Zeichen sein.

    > [!NOTE]
    > Eine Beschriftung kann einen Unterstrich (\_) enthalten, aber keine anderen Sonderzeichen.

- Die Beschriftung kann die folgenden reservierten Wörter nicht verwenden: UND, ODER, WENN, DANN SONST, PERIODEN, ZU, BASEROW, EINHEIT, NULL, CPO oder RPO.

Die folgenden Beispiele sind gültige Zeilencodes:

- 320
- TL\_NET\_INCOME
- TL\_NET\_94

### <a name="change-a-row-code-in-a-row-definition"></a>Ändern eines Zeilencodes in einer Zeilendefinition

1. Klicken Sie im Berichts-Designer auf die **Zeilendefinitionen** und öffnen dann die Zeilendefinition, um sie zu ändern.
2. Geben Sie in der entsprechenden Zeile den neuen Wert in der Spalte **Zeilencode** ein.

### <a name="reset-numeric-row-codes"></a>Numerische Zeilencodes zurücksetzen

1. Im Berichts-Designer klicken Sie auf die **Zeilendefinitionen** und öffnen dann die Zeilendefinition, um sie zu ändern.
2. Klicken Sie im Menü **Bearbeiten** auf **Zeilen neu nummerieren**.
3. Geben Sie im Dialogfeld **Zeilen neu nummerieren** neue Werte für den Anfangszeilencode und das Zeilencodeinkrement an. Sie können die numerische Zeilencodes auf die äquidistante Werte zurücksetzen. Der Berichtsdesigner nummeriert jedoch nur Zeilencodes neu, die mit Zahlen beginnen (beispielsweise 130 oder 246). Es nummeriert keine Zeilencodes neu, die mit Buchstaben beginnen (beispielsweise INCOME\_93 oder TP0693).

> [!NOTE]
> Wenn Sie Zeilencodes neu nummerieren, aktualisiert der Berichtsdesigner **TOT** und **CAL**-Referenzen automatisch. Wenn sich beispielsweise eine **TOT**-Zeile auf einen Bereich bezieht, der mit Zeilencode 100 beginnt, und Sie Zeilen beginnend mit 90 neu nummerieren, verweist der Anfangs-**TOT** Änderungen von 100 bis 90.

## <a name="add-a-description"></a>Eine Beschreibung hinzufügen
Die Beschreibungszelle enthält die Beschreibung der Finanzdaten in der Zeile des Berichts, wie etwa "Umsatz" oder "Nettogewinn". Der Text in der Zelle **Beschreibung** wird im Bericht genau, wie in der Zeilendefinition eingeben angezeigt.

> [!NOTE]
> Die Breite der Spalte Beschreibung im Bericht wird in der Spaltendefinition festgelegt. Wenn der Text in der Spalte **Beschreibung** in der Zeilendefinition lang ist, überprüfen Sie die Breite der **DESC**-Spalte. Wenn Sie das Dialogfeld **Zeilen einfügen aus** verwenden, sind die Werte in der Spalte **Beschreibung** die Segmentwerte oder die Dimensionswerte aus den Finanzdaten. Sie können Zeilen einfügen, um beschreibenden Text wie etwa eine Abschnittsüberschrift oder eine Abschnittssumme und Formatierungen wie etwa eine Linie vor einer Summenzeile hinzuzufügen. Wenn der Bericht die Berichtsbaumstruktur umfasst, können Sie den zusätzlichen Text einbeziehen, der für die Berichtseinheiten in der Berichtsbaumstruktur definiert ist. Sie können den zusätzlichen Text auch auf eine bestimmte Berichtseinheit beschränken.

### <a name="add-the-description-for-a-line-on-a-report"></a>Hinzufügen der Beschreibung für eine Zeile in einem Bericht

1. Im Berichts-Designer klicken Sie auf die **Zeilendefinitionen** und öffnen dann die Zeilendefinition, um sie zu ändern.
2. Wählen Sie die Zelle **Beschreibung** aus, und geben Sie dann den Namen der Berichtszeile ein.
3. Übernehmen Sie die Formatierung.

### <a name="add-additional-text-from-a-reporting-tree-in-the-description"></a>Hinzufügen von zusätzlichem Text aus einer Berichtsbaumstruktur in der Beschreibung

1. Im Berichts-Designer klicken Sie auf die **Zeilendefinitionen** und öffnen dann die Zeilendefinition, um sie zu ändern.
2. Geben Sie den Code des zusätzlichen Textes und einen beliebigen anderen Text in der entsprechenden Zelle **Beschreibung** ein.
3. Übernehmen Sie die Formatierung.

### <a name="limit-the-additional-text-to-a-specific-reporting-unit"></a>Einschränken des zusätzlichen Texts auf eine bestimmte Berichtseinheit

1. Im Berichts-Designer klicken Sie auf die **Zeilendefinitionen** und öffnen dann die Zeilendefinition, um sie zu ändern.
2. Suchen Sie die Zeile, in der zusätzlicher Text erstellt werden soll, und doppelklicken Sie auf die Zelle in der Spalte **Verwandte Formeln/Zeilen/Einheiten**.
3. Wählen Sie im Dialogfeld **Auswahl der Berichtseinheit** im Feld **Berichtsstruktur** eine Berichtsbaumstruktur aus.
4. Erweitern oder reduzieren Sie die Berichtsbaumstruktur im Feld **Berichtseinheit für Einschränkung auswählen** , und wählen Sie dann eine Berichtseinheit aus.

## <a name="add-a-format-code"></a>Hinzufügen eines Formatcodes
Die Zelle **Formatcode** bietet eine Auswahl von vorformatierten Auswahlmöglichkeiten für den Inhalt dieser Zeile an. Wenn die **Formatcode**-Zelle leer ist, wird die Zeile als Finanzdatendetailzeile interpretiert.

> [!NOTE]
> Wenn ein Bericht Formatierungszeilen enthält, die keine Betragszeilen sind aber Betragszeilen zugeordnet sind, die, (beispielsweise aufgrund der Nullsalden) unterdrückt wurden, können Sie die Spalte **Verwandte Formeln/Zeilen/Einheiten** verwenden, um zu verhindern, dass Titel- und Formatzeilen gedruckt werden.

### <a name="add-a-format-code-to-a-report-row"></a>Hinzufügen eines Formatcodes zu einer Berichtszeile

1. Im Berichts-Designer klicken Sie auf die **Zeilendefinitionen** und wählen dann eine Zeilendefinition, um sie zu ändern.
2. Doppelklicken Sie auf die Zelle **Formatcode**.
3. Wählen Sie in der Liste einen Formatcode aus. In der folgenden Tabelle finden Sie die Formatcodes und ihre Aktionen.

    | Formatcode                   | Interpretation des Formatcodes | Aktion |
    |-------------------------------|-----------------------------------|--------|
    | (Keine)                        |                                   | Löscht die **Formatcode**-Zelle. |
    | TOT                           | Summe                             | Kennzeichnet eine Zeile, die mathematische Operatoren in der Spalte **Verwandte Formeln/Zeilen/Einheiten** verwendet. Summen enthalten einfache Operatoren, wie **+** oder **-**. |
    | CAL                           | Herstellkostenkalkulation                       | Kennzeichnet eine Zeile, die mathematische Operatoren in der Spalte **Verwandte Formeln/Zeilen/Einheiten** verwendet. Berechnungen enthalten komplexe Operatoren, wie **+**, **-**, **\**_, _*/** sowie die Anweisungen **IF/THEN/ELSE**. |
    | DES                           | Beschreibung                       | Kennzeichnet eine Überschriftposition oder eine leere Position in einem Bericht. |
    | LKS RCHTS ZEN                   | Links Rechts Zentriert                 | Richtet den Zeilenbeschreibungstext auf der Berichtsseite aus, unabhängig von seiner Position in der Spaltendefinition. |
    | ÄBZ                           | Änderungsbasiszeile                   | Gibt eine Zeile an, die die Basiszeile für Spaltenberechnungen festlegt. |
    | SPALTE                        | Spaltenumbruch                      | Hiermit wird eine neue Spalte im Bericht gestartet. |
    | SEITE                          | Seitenumbruch                        | Hiermit wird eine neue Seite im Bericht gestartet. |
    | \---                          | Einzelner Unterstrich                  | Setzt eine einzelne Linie unter alle Betragsspalten in den Bericht. |
    | ===                           | Doppelter Unterstrich                  | Setzt eine doppelte Linie unter alle Betragsspalten in den Bericht. |
    | ZEILE1                         | Dünne Linie                         | Zeichnet eine einzelne dünne Linie über die gesamte Seite. |
    | ZEILE2                         | Dicke Linie                        | Zeichnet eine einzelne dicke Linie über die gesamte Seite. |
    | ZEILE3                         | Gepunktete Linie                       | Zeichnet eine einzelne gepunktete Linie über die gesamte Seite. |
    | ZEILE4                         | Dicke Linie und dünne Linie          | Zeichnet eine Doppellinie über die gesamte Seite. Die obere Linie ist dick, die untere Linie ist dünn. |
    | ZEILE5                         | Dünne Linie und dicke Linie          | Zeichnet eine Doppellinie über die gesamte Seite. Die obere Linie ist dünn, die untere Linie ist dick. |
    | BXB BXC                       | Umrahmte Zeile                         | Zieht einen Kasten um die Berichtszeilen, die mit der **BXB**-Zeile beginnen und mit der **BXC**-Zeile beenden. |
    | ANM                           | Anmerkung                            | Gibt eine Zeile an, bei der es sich um eine Kommentarzeile handelt, die nicht im Bericht gedruckt werden soll. Beispielsweise könnten Sie in einer Anmerkungszeile die verwendeten Formatierungstechniken erläutern. |
    | SORT ASORT SORTDESC ASORTDESC | Sortieren                              | Sortiert Ausgaben oder Einnahmen, sortiert einen Istwert- oder Budgetvarianzbericht nach der größten Abweichung oder sortiert Zeilenbeschreibungen alphabetisch. |

## <a name="specify-related-formulasrowsunits"></a>Verwandte Formeln/Zeilen/Einheiten angeben
Die Zelle **Verwandte Formeln/Zeilen/Einheiten** hat mehrere Zwecke. Je nach Art der Zeile, kann eine **Verwandte Formeln/Zeilen/Einheiten**-Zelle eine der folgenden Aufgaben ausführen:

- Definieren der Zeilen, die in die Berechnung einzubezogen werden, wenn Sie einen **TOT**-Formatcode oder einen **CAL**-Formatcode verwenden.
- Es kann eine Formatierungszeile mit einer Betragszeile verknüpft werden, damit die Formatierung nur mit dem zugehörigen Betrag gedruckt wird.
- Beschränken Sie eine Zeile auf eine bestimmte Berichtseinheit.
- Definieren Sie die niedrige Basiszeile für Berechnungen, wenn Sie den Formatcode **BASEROW** verwenden.
- Es können die Zeilen definiert werden, die sortiert werden sollen, wenn Sie einen der Sortierformatcodes verwenden.

### <a name="use-a-row-total-in-a-row-definition"></a>Verwenden eines Zeilengesamtergebnisses in einer Zeilendefinition

Mit einer Zeilengesamtergebnis-Formel werden die Beträge in anderen Zeilen addiert oder subtrahiert. Eine Formel zum Erstellen eines Gesamtzeilenergebnisses kann die Operatoren + und - enthalten, um einzelne Zeilencodes und Bereiche zu kombinieren. Bereiche werden durch einen Doppelpunkt (:) angegeben. Die Formel kann bis zu 1.024 Zeichen lang sein. Dies ist ein Beispiel einer Standardsummenformel: 400+420+430+450+460LIABILITIES+EQUITY520: 546520:546-LIABILITIES

### <a name="components-of-a-row-total-formula"></a>Komponenten einer Zeilengesamtergebnis-Formel

Beim Erstellen einer Zeilengesamtergebnis-Formel müssen Sie Zeilencodes verwenden, um in der aktuellen Zeilendefinition die Zeilen anzugeben, die addiert oder subtrahiert werden sollen, und Operatoren verwenden, um anzugeben, wie die Zeilen kombiniert werden sollen. Gesamtergebniszeilen und Betragszeilen können beliebig kombiniert werden.

> [!NOTE]
> Alle Gesamtergebniszeilen in einem Bereichs werden ausgeschlossen. Sie können zum Erstellen der Gesamtsumme den Zeilenbereich angeben. Wenn die erste Zeile in einem Bereich eine Summenzeile ist, wird diese Zeile im neuen Gesamtergebnis berücksichtigt. In der folgenden Tabelle wird beschrieben, wie Operatoren in den Zeilensummenformeln verwendet werden.

| Bediener | Beispielformel | Beschreibung                                                 |
|----------|-----------------|-------------------------------------------------------------|
| +        | 100+330         | Addiert den Betrag in Zeile 100 zum Betrag in Zeile 330.        |
| :        | 100:330         | Addiert die Summen aller Zeilen zwischen Zeile 100 und 330 Zeile.    |
| -        | 100-330         | Subtrahiert den Betrag in Zeile 100 von dem Betrag in Zeile 330. |

### <a name="create-a-row-total"></a>Erstellen eines Zeilengesamtergebnisses

1. Klicken Sie im Berichts-Designer auf **Zeilendefinitionen**, und öffnen Sie dann die zu ändernde Zeilendefinition.
2. Doppelklicken Sie auf die Zelle **Formatcode** in der Zeilendefinition, und wählen Sie **TOT** aus.
3. Geben Sie in die Zelle **Verwandte Formeln/Zeilen/Einheiten** die Summenformel ein.

### <a name="relate-a-format-row-to-an-amount-row"></a>Verbinden einer Formatzeile mit einer Betragszeile

In der Spalte **Formatcode** in einer Zeilendefinition wird Formatierung mit den Formatcodes **DES**, **LFT**, **RGT**, **CEN** **---** und **===** auf Zeile, die keine Beträge enthalten, angewendet. Damit diese Formatierung nicht gedruckt wird, wenn die zugehörigen Betragszeilen unterdrückt werden (beispielsweise, da die Betragszeilen Nullwerte oder keine Periodenaktivität enthalten), müssen Sie die Formatzeilen den entsprechenden Betragszeilen zuordnen. Diese Funktion ist hilfreich, wenn Sie verhindern möchten, dass Überschriften oder Formatierung von Zwischensummen gedruckt werden, wenn es keine auszudruckenden Details während der Periode gibt.

> [!NOTE]
> Sie können das Drucken von detaillierten Betragszeilen auch verhindern, indem Sie die Option zum Anzeigen von Zeilen ohne Beträge deaktivieren. Diese Option befindet sich auf der Registerkarte **Einstellungen** der Berichtsdefinition. Standardmäßig werden Buchungsdetailkonten mit einem Nullsaldo oder ohne Zeitraumaktivität in Berichten unterdrückt. Um diese Transaktionsdetailkonten anzuzeigen, aktivieren Sie das Kontrollkästchen **Zeilen ohne Beträge anzeigen** auf der Registerkarte **Einstellungen** der Berichtsdefinition.

### <a name="relate-a-format-row-to-an-amount-row"></a>Zuordnen einer Formatzeile zu einer Betragszeile

1. Im Berichts-Designer klicken Sie auf die **Zeilendefinitionen** und wählen dann eine Zeilendefinition, um sie zu ändern.
2. Geben Sie in der Formatierungszeile in der Zelle **Verwandte Formeln/Zeilen/Einheiten** den Zeilencode der Betragszeile ein, die unterdrückt werden soll.

    > [!NOTE]
    > Um eine Betragszeile zu unterdrücken, muss der Saldo der Zeile 0 (null) sein. Eine Betragszeile mit einem Saldo wird nicht unterdrückt.

3. Klicken Sie im Menü **Datei** auf **Speichern**.

### <a name="example-of-preventing-printing-of-rows"></a>Beispiel für Unterdrücken des Druckens der Zeilen

Im folgenden Beispiel möchte ein Benutzer die Überschrift und die Unterstriche in der Zeile **Bargeld gesamt** des Berichts nicht drucken, da es in keiner der Kassenkonten Aktivitäten gab. Daher gibt der Benutzer in Zeile 220 (die, wie der Formatcode **---** angibt, eine Formatierungszeile ist) in der Zelle **Verwandte Formeln/Zeilen/Einheiten** den Wert **250** ein. Dies ist der Zeilencode der Betragszeile, die der Benutzer unterdrücken möchte.

[![RelatedRowsRowDefinition](./media/relatedrowsrowdefinition-1024x144.png)](./media/relatedrowsrowdefinition.png)

## <a name="select-the-base-row-for-a-column-calculation"></a>Auswählen der Basiszeile für eine Spaltenberechnung
In der relationalen Berichterstellung weisen Sie eine oder mehrere Basiszeilen der Zeilendefinition zu, indem Sie den Formatcode **CBR** (Basiszeile ändern) verwenden. Von einer Berechnung in der Spaltendefinition wird dann auf eine Basiszeile verwiesen. Nachfolgend einige typische Beispiele für ÄBZ-Berechnungen:

- Prozentsatz des Gesamtumsatzes im Zusammenhang mit einzelnen einnahmebezogenen Artikeln
- Prozentsatz der Gesamtausgaben im Zusammenhang mit einzelnen ausgabenbezogenen Artikeln
- Prozentsatz der Bruttogewinnmarge im Zusammenhang mit Details zu Geschäftsbereich oder Abteilung

Mindestens eine Basiszeile wird in der Zeilendefinition definiert. Die Spaltendefinition bestimmt die Beziehung, die über die Basiszeile berichtet. Der Code, der in der Spaltenformel verwendet wird, ist **BASEROW**. Die folgenden grundlegenden mathematischen Arbeitsgänge werden mit **BASEROW** verwendet: Dividieren, multiplizieren, addieren oder subtrahieren. Der Arbeitsgang, der am häufigsten verwendet wird, ist die Division durch **BASEROW**, wo das Ergebnis als Prozentsatz angezeigt wird. Spaltenberechnungen, bei denen **BASEROW** in der Formel verwendet werden, verwenden die Zeilendefinition für die zugehörigen Basiszeilencodes. **CBR** Zeilen haben folgende Merkmale:

- **CBR** Zeilen werden im ausgefüllten Bericht nicht gedruckt.
- Der **CBR**-Formatcode und der entsprechende Zeilencode werden über der Zeile oder dem Abschnitt positioniert, die bzw. der zusammenhängende Berechnungen anzeigt.

In einer Spaltendefinition kennzeichnet der **KALK**-Spaltentyp eine Spalte, die in der **Formel**-Zeile eine Formel enthält. Diese Formel arbeitet auf den Daten für diese Spalte des Berichts und verwendet das Baserow-Schlüsselwort, um Berechnungen für den Formatcode **CBR** in der Zeile zu basieren. In der Zeilendefinition definiert der **CBR**-Formatcode die Basiszeile für Spalten, die einen Prozentsatz der Basiszeile für jede Zeile im Bericht berechnen oder damit multiplizieren. Sie können über mehrere Formatcodes **CBR** in einem Zeilenformat verfügen, wie eines für den Nettoumsatz, eines für den Bruttoumsatz und eines für die Gesamtkosten. Normalerweise wird der **CBR**-Formatcode verwendet, um einen Prozentsatz für Konten zu erstellen, die in einer Summenposition verglichen werden. Eine Basiszeile wird so lange für alle Berechnungen verwendet, bis eine andere Basiszeile definiert wird. Sie müssen einen **CBR**-Anfangsformatcode und einen **CBR**-Endeformatcode definieren. Beispielsweise könnten Sie den Wert in jeder Ausgabenzeile durch den Wert in der Nettoumsatzzeile dividieren, um die Ausgaben in Prozent vom Nettoumsatz zu berechnen. In diesem Fall ist die Nettoumsatzzeile die Basiszeile. Sie können eine Spaltendefinition definieren, die aktuelle Ergebnisse und Jahresergebnisse bis dato sowie den jeweiligen Basisprozentsatz berechnet, wie in folgendem Beispiel gezeigt. Beginnen Sie mit einer detaillierten Gewinn- und Verlustrechnung.

### <a name="select-the-base-row-in-a-row-definition-for-a-column-calculation"></a>Auswählen der Basiszeile in einer Zeilendefinition für eine Spaltenberechnung

1. Klicken Sie im Berichts-Designer auf **Spaltendefinitionen**, und öffnen Sie anschließend die Spaltendefinition für eine Einkommensaufstellung.
2. Fügen Sie der Spaltendefinition eine neue Spalte hinzu, und legen Sie den Spaltentyp auf **CALC** fest.
3. Geben Sie in der **Formel**-Zelle der neuen Spalte die Formel **X/BASEROW** ein, wobei **X** der **FD**-Spaltentyp ist, von dem ein Prozentsatz angezeigt wird.
4. Doppelklicken Sie auf die Zelle **Format/Währungsaußerkraftsetzung**.
5. Wählen Sie im Dialogfeld **Formataußerkraftsetzung** in der Liste die **Formatkategorie** die Option **Prozentsatz** aus, und klicken Sie anschließend auf **OK**.
6. Klicken Sie im Menü **Datei** auf **Speichern unter**, um die Spaltendefinition unter einem neuen Namen zu speichern. Fügen Sie dem aktuellen Dateinamen **CBR** an (beispielsweise **CUR\_YTD\_CBR**). Diese Spaltendefinition ist Ihre Basiszeilen-Spaltendefinition.
7. Klicken Sie im Berichts-Designer auf **Zeilendefinitionen**, und öffnen Sie anschließend die Zeilendefinition, die durch die Basiszeilenberechnung geändert werden soll.
8. Fügen Sie eine neue Zeile über der Zeile ein, in der die Basiszeilenberechnung starten soll.
9. Doppelklicken Sie auf die Zelle **Formatcode** der Zeilendefinition, und wählen Sie dann **CBR** aus.
10. Geben Sie in Zelle **Verwandte Formeln/Zeilen/Einheiten** die Zeilencodenummer für die Basiszeile ein.

### <a name="example-of-base-row-calculation"></a>Beispiel einer Basiszeilenberechnung

Im folgenden Beispiel einer Zeilendefinition zeigt Zeile 100, dass die Basiszeile für Berechnungen Zeile 280 ist.

[![Beispiel für eine Basiszeilenberechnung](./media/cbrrowdefinition.png)](./media/cbrrowdefinition.png)

Im folgenden Beispiel für eine Spaltendefinition verwenden die Berechnungen den **CBR**-Formatcode. Mit der Berechnung in Spalte "C" wird der Wert in Spalte "B" des Berichts durch den Wert in Zeile "280" von Spalte "B" dividiert. Die Formataußerkraftsetzung in Spalte "B" druckt das Ergebnis der Berechnung als Prozentsatz. Ebenso entsprechen die Beträge in Spalte "E" dem Betrag in Spalte "D" in Prozent vom Nettoumsatz.

[![Spaltendefinitionsbeispiel](./media/cbrcolumndefinition2.png)](./media/cbrcolumndefinition2.png)

Das folgende Beispiel zeigt einen Bericht, der auf Grundlage der vorherigen Berechnungen generiert worden sein könnte.

[![Beispielsbericht auf Grundlage vorheriger Beispielberechnungen.](./media/cbrreport-1024x272.png)](./media/cbrreport.png)

## <a name="select-a-sorting-code-for-a-row-definition"></a>Auswählen eines Sortierungscodes für eine Zeilendefinition
Mit Sortiercodes werden Konten oder Werte sortiert, ein Istwert- oder Budgetvarianzbericht nach der größten Abweichung sortiert oder Zeilenbeschreibungen alphabetisch sortiert. Die folgenden Sortiercodes sind verfügbar:

- **SORTIEREN** - Sortiert den Bericht anhand der Werte in der angegebenen Spalte in aufsteigender Reihenfolge.
- **ASORT** - Sortiert den Bericht anhand der absoluten Werte der Werte in der angegebenen Spalte in aufsteigender Reihenfolge. Das Vorzeichen der einzelnen Werte wird also bei der Sortierung der Werte ignoriert. Dieser Formatcode definiert die Reihenfolge der Werte nach der Größe der Abweichung, egal ob positiv oder negativ.
- **SORTDESC** - Sortiert den Bericht anhand der Werte in der angegebenen Spalte in absteigender Reihenfolge.
- **ASORTDESC** - Sortiert den Bericht basierend auf dem absoluten Wert der Werte in der angegebenen Spalte in absteigender Reihenfolge.

### <a name="select-a-sorting-code"></a>Auswählen eines Sortiercodes

1. Im Berichts-Designer klicken Sie auf die **Zeilendefinitionen** und öffnen dann die Zeilendefinition, um sie zu ändern.
2. Doppelklicken Sie auf die Zelle **Formatcode**, und wählen Sie dann einen Sortiercode aus.
3. Geben Sie in der Zelle **Verwandte Formeln/Zeilen/Einheiten** den Bereich der Zeilencodes an, die sortiert werden sollen. Geben Sie zur Angabe eines Bereichs den ersten Zeilencode, einen Doppelpunkt (:), und dann den letzten Zeilencode ein. Geben Sie z. B. **160:490** ein, um anzugeben, dass der Bereich von Zeile 160 bis Zeile 490 reicht.
4. Geben Sie in der Zelle **Spalteneinschränkung** den Buchstaben der Berichtsspalte ein, der zum Sortieren verwendet werden soll.

    > [!NOTE]
    > Es werden nur Betragszeilen in einer Sortierungsberechnung eingeschlossen.

### <a name="examples-of-ascending-and-descending-column-values"></a>Beispiele für absteigende und absteigende Spaltenwerte

Im folgenden Beispiel werden die Werte in Spalte "D" des Berichts in aufsteigender Reihenfolge für Zeilen 160 bis 490 sortiert. Zusätzlich werden die absoluten Werte in Spalte "G" des Berichts in absteigender Reihenfolge für Zeilen 610 bis 940 sortiert.

| Zeilencode | Beschreibung                                         | Formatcode | Verwandte Formeln/Zeilen/Einheiten | Standardsaldo | Spalteneinschränkung | Verknüpfen mit Finanzdimensionen |
|----------|-----------------------------------------------------|-------------|-----------------------------|----------------|--------------------|------------------------------|
| 100      | Sortiert nach monatlicher Abweichung in aufsteigender Reihenfolge       | BESCHR         |                             |                |                    |                              |
| 130      |                                                     | SORT        | 160:490                     |                | D                  |                              |
| 160      | Verkauf                                               |             |                             | C              |                    | 4100                         |
| 190      | Retouren                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 490      | Zinsertrag                                     |             |                             | C              |                    | 7000                         |
| 520      |                                                     | BESCHR         |                             |                |                    |                              |
| 550      | Sortiert nach der absoluten Abweichung für Jahr bis dato in absteigender Reihenfolge | BESCHR         |                             |                |                    |                              |
| 580      |                                                     | AABSTSORT   | 610:940                     |                | G                  |                              |
| 610      | Vertrieb                                               |             |                             | k              |                    | 4100                         |
| 640      | Retouren                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 940      | Zinsertrag                                     |             |                             | k              |                    | 7000                         |


## <a name="specify-a-format-override-cell"></a>Angeben einer Formataußerkraftsetzungszelle an
Die Zelle **Formataußerkraftsetzung** gibt die Formatierung an, die für die Zeile verwendet wird, wenn der Bericht gedruckt wird. Diese Formatierung setzt die Formatierung außer Kraft, die in der Spaltendefinition und in der Berichtsdefinition angegeben ist. Standardmäßig handelt es sich bei der in diesen Definitionen angegebenen Formatierung um die Währung. Wird in dem Bericht die Anzahl der Anlagen (z. B. der Gebäude) in einer Zeile und deren Geldwert in einer anderen Zeile aufgelistet, können Sie die Währungsformatierung außer Kraft setzen und für die Zeile, in der die Anzahl der Gebäude angegeben wird, eine numerische Formatierung eingeben. Sie geben diese Informationen im Dialogfeld **Formataußerkraftsetzung** an. Die verfügbaren Optionen sind von der ausgewählten Formatkategorie abhängig. Der **Beispiel**-Bereich des Dialogfelds zeigt Beispielsformate an. Die verfügbaren Formatkategorien lauten wie folgt:

- Währungsformatierung
- Numerische Formatierung
- Prozentsatzformatierung
- Benutzerdefinierte Formatierung

### <a name="override-cell-formatting"></a>Außerkraftsetzen der Zellenformatierung

1. Öffnen Sie im Berichts-Designer die zu bearbeitende Zeilendefinition.
2. Doppelklicken Sie in der Zeile, deren Format außer Kraft gesetzt werden soll, auf die Zelle in der Spalte **Formataußerkraftsetzung**.
3. Wählen Sie im Dialogfeld **Formataußerkraftsetzung** die Formatierungsoptionen aus, die für diese Zeile im Bericht verwendet werden sollen.
4. Klicken Sie auf **OK**.

### <a name="currency-formatting"></a>Währungsformatierung

Währungsformatierung bezieht sich auf einen steuerlichen Betrag und schließt das Währungssymbol ein. Die folgenden Optionen sind verfügbar:

- **Währungssymbol** – Das Währungssymbol für den Bericht. Dieser Wert setzt die Einstellungen für **Regionale Optionen** für die Unternehmensdaten außer Kraft.
- **Negativen Zahlen** - Negativen Zahlen können ein Minuszeichen aufweisen (-), sie können in Klammern angezeigt werden, oder sie können ein Dreieck (∆) aufweisen.
- **Dezimalstellen** - Die Anzahl der angezeigten Stellen nach der Dezimalstelle.
- **Text für Außerkraftsetzung des Nullwerts** - Der in den Bericht einzuschließende Text, wenn der Betrag 0 (null) ist. Dieser Text wird als letzte Zeile im **Beispiel**-Bereich angezeigt.

    > [!NOTE]
    > Wenn das Drucken für Nullwerte oder keine Periodenaktivität unterdrückt wird, wird der Text unterdrückt.

### <a name="numeric-formatting"></a>Numerische Formatierung

Die numerische Formatierung gilt für jeden Betrag und umfasst kein Währungssymbol. Die folgenden Optionen sind verfügbar:

- **Negativen Zahlen** - Negativen Zahlen können ein Minuszeichen aufweisen (-), sie können in Klammern angezeigt werden, oder sie können ein Dreieck (∆) aufweisen.
- **Dezimalstellen** - Die Anzahl der angezeigten Stellen nach der Dezimalstelle.
- **Text für Außerkraftsetzung des Nullwerts** - Der in den Bericht einzuschließende Text, wenn der Betrag 0 (null) ist. Dieser Text wird als letzte Zeile im **Beispiel**-Bereich angezeigt.

    > [!NOTE]
    > Wenn das Drucken für Nullwerte oder keine Periodenaktivität unterdrückt wird, wird der Text unterdrückt.

### <a name="percentage-formatting"></a>Prozentsatzformatierung

Die Prozentsatzformatierung umfasst das Prozentzeichen (%). Die folgenden Optionen sind verfügbar:

- **Negativen Zahlen** - Negativen Zahlen können ein Minuszeichen aufweisen (-), sie können in Klammern angezeigt werden, oder sie können ein Dreieck (∆) aufweisen.
- **Dezimalstellen** - Die Anzahl der anzuzeigenden Stellen nach der Dezimalstelle.
- **Text für Außerkraftsetzung des Nullwerts** - Der in den Bericht einzuschließende Text, wenn der Betrag 0 (null) ist. Dieser Text wird als letzte Zeile im **Beispiel**-Bereich angezeigt.

    > [!NOTE]
    > Wenn das Drucken für Nullwerte oder keine Periodenaktivität unterdrückt wird, wird der Text unterdrückt.

### <a name="custom-formatting"></a>Benutzerdefinierte Formatierung

Verwenden Sie die benutzerdefinierte Formatierungskategorie, um eine benutzerdefinierte Formataußerkraftsetzung zu erstellen. Die folgenden Optionen sind verfügbar:

- **Typ** – Das benutzerdefinierte Format.
- **Text für Außerkraftsetzung des Nullwerts** - Der in den Bericht einzuschließende Text, wenn der Betrag 0 (null) ist. Dieser Text wird als letzte Zeile im **Beispiel**-Bereich angezeigt.

    > [!NOTE]
    > Wenn das Drucken für Nullwerte oder keine Periodenaktivität unterdrückt wird, wird der Text unterdrückt.

Der Typ sollte den positiven und den negativen Wert darstellen. Gewöhnlich wird ein ähnliches Format für die Unterscheidung zwischen positiven und negativen Werten eingegeben. Um beispielsweise anzugeben, dass positive und negative Werte zwei Dezimalstellen enthalten, aber negative Werte in Klammern angezeigt werden, geben Sie **0,00; (0,00)** ein. In der folgenden Tabelle sind benutzerdefinierte Formate dargestellt, mit denen das Format der Werte gesteuert werden kann. Alle Beispiele beginnen beim Wert 1234.56.

| Format                         | Positiv   | Negativ     | Null    |
|--------------------------------|------------|--------------|---------|
| 0                              | 1235       | -1235        | 0       |
| 0;0                            | 1235       | 1235         | 0       |
| 0;(0);-                        | 1235       | 1235         | -       |
| \#,\#\#\#;(\#,\#\#\#);""       | 1.235      | (1.235)      | (Leer) |
| \#,\#\#0.00;(\#,\#\#0.00);zero | 1.234,56   | (1.234,56)   | Null    |
| 0,00 %;(0,00 %)                  | 123456,00 % | (123456,00%) | 0,00%   |

## <a name="specify-a-normal-balance-cell"></a>Normale Saldozelle angeben
Die Zelle **Normaler Saldo** in einer Zellendefinition steuert das Vorzeichen der Beträge in einer Zeile. Um das Vorzeichen einer Zeile umzukehren, oder wenn der normale Saldo eines Kontos ein Habenposten ist, geben ein **C** in die Zelle **Normales Saldo** für diese Zeile ein. Report-Design kehrt das Vorzeichen für alle Habenbilanzkonten in dieser Zeile um. Wenn der Berichtsdesigner diese Konten konvertiert, entfernt er das Soll-/Habenmerkmal aus allen Beträgen und vereinfacht so das Addieren insgesamt. Um beispielsweise den Nettogewinn zu berechnen, ziehen Sie die Ausgaben vom Gewinn ab. In der Regel werden addierte und berechnete Zeilen nicht durch einen **C**-Code beeinflusst. Allerdings kehrt das **XCR**-Drucksteuerelement in der Spaltendefinition das Vorzeichen jeder Zeile mit einem **C** in der Spalte **Normaler Saldo** um. Diese Formatierung ist besonders wichtig, wenn Sie alle ungünstigen Abweichungen als negative Beträge anzeigen möchten. Wenn eine summierte oder berechnete Zahl das falsche Vorzeichen besitzt, geben Sie ein **C** in der Zelle **Normaler Saldo** für die Zeile ein, um das Vorzeichen umzukehren.

## <a name="specify-a-row-modifier-cell"></a>Angeben einer Zeilenmodifizierer-Zelle
Der Inhalt der Zelle **Zeilenmodifizierer** in einer Zeilendefinition setzt die Geschäftsjahre, Perioden und weitere Informationen, die in der Spaltendefinition für diese Zeile angegeben sind, außer Kraft. Der ausgewählte Modifizierer gilt für jedes Konto in der Zeile. Sie können jede Zeile mit einem oder mehreren der folgenden Modifizierertypen ändern:

- Kontomodifizierer
- Buchcodemodifizierer
- Konto- und Buchungsattribute

### <a name="override-a-column-definition"></a>Spaltendefinition außer Kraft setzen

1. Öffnen Sie im Berichts-Designer die zu bearbeitende Zeilendefinition.
2. Doppelklicken in der Zeile, in der Sie die Spaltendefinition außer Kraft setzen möchten, auf die Zelle **Zeilenmodifizierer**.
3. Wählen Sie im Dialogfeld **Zeilenmodifizierer** eine Option im Feld **Kontomodifizierer** aus. Eine Beschreibung der Optionen finden Sie unter "Kontomodifizierer".
4. Wählen Sie im Feld **Buchcodemodifizierer** den Buchcode aus, der für die Zeile verwendet werden soll.
5. Gehen Sie unter **Attribute** folgendermaßen vor, um einen Eintrag für jedes Attribut hinzuzufügen, das im Zeilencode eingeschlossen sein soll:

    1. Doppelklicken Sie auf die Zelle **Attribut**, und wählen Sie dann einen Attributnamen aus.

        > [!IMPORTANT]
        > Ersetzen Sie das Nummernzeichen (\#) durch einen numerischen Wert.

    2. Doppelklicken Sie auf die Zelle **Von**, und geben Sie den ersten Wert für den Bereich ein.
    3. Doppelklicken Sie auf die Zelle **Bis**, und geben Sie den letzten Wert für den Bereich ein.

6. Klicken Sie auf **OK**.

### <a name="account-modifiers"></a>Kontomodifizierer

Wenn Sie ein bestimmtes Konto auswählen, fasst der Berichtsdesigner normalerweise das Konto und die Geschäftsjahre, Perioden und weitere Informationen, die Sie in der Spaltendefinition angeben, zusammen. Sie können unterschiedliche Informationen (z. B. verschiedene Buchhaltungszeiträume) für bestimmte Zeilen verwenden. In der folgenden Tabelle werden die verfügbaren Kontomodifizierer gezeigt. Ersetzen Sie das Nummernzeichen (\#) mit einem Wert, der gleich oder weniger ist, als die Anzahl der Perioden eines Geschäftsjahrs.

| Kontomodifizierer | Was gedruckt wird                                                                           |
|------------------|-------------------------------------------------------------------------------------------|
| /BB              | Der Anfangssaldo für ein Konto.                                                     |
| /\#              | Der Saldo für die angegebene Periode.                                                     |
| /-\#             | Der Saldo für die Periode, der \# Perioden vor der aktuellen Periode liegt.                  |
| /+\#             | Der Saldo für die Periode, der \# Perioden nach der aktuellen Periode liegt.                   |
| /C               | Der Saldo für die aktuelle Periode.                                                       |
| /C-\#            | Der Saldo für die Periode, der \# Perioden vor der aktuellen Periode liegt.                  |
| /C+\#            | Der Saldo für die Periode, der \# Perioden nach der aktuellen Periode liegt.                   |
| /Y               | Der Saldo seit Jahresbeginn bis zur aktuellen Periode.                                      |
| /Y-\#            | Der Saldo seit Jahresbeginn bis zur Periode, die \# Perioden vor der aktuellen Periode liegt. |
| /Y+\#            | Der Saldo seit Jahresbeginn bis zur Periode, die \# Perioden nach der aktuellen Periode liegt.  |

### <a name="book-code-modifiers"></a>Buchcodemodifizierer

Sie können eine Zeile auf einen vorhandenen Buchcode einschränken. Die Spaltendefinition muss mindestens eine **FD**-Spalte enthalten, die einen Buchcode aufweist.

> [!NOTE]
> Die Buchcodeeinschränkung für eine Zeile setzt die Buchcodeeinschränkungen in der Spaltendefinition für diese Zeile außer Kraft.

### <a name="account-and-transaction-attributes"></a>Konto- und Buchungsattribute

Einige Kontoführungssysteme unterstützen Konto- und Buchungsattribute in den Finanzdaten. Diese Attribute funktionieren wie virtuelle Kontosegmente und können zusätzliche Informationen zu Konto oder Buchung enthalten. Diese zusätzlichen Informationen könnten Kontokennungen, Chargenkennungen, Postleitzahlen oder andere Attribute sein. Wenn Ihr Kontoführungssystem Attribute unterstützt, können Sie Kontoattribute oder Buchungsattribute als Zeilenmodifizierer in der Zeilendefinition verwenden. Informationen über das Außerkraftsetzen von Zeileninformationen finden Sie im Bereich "Spaltendefinition außer Kraft setzen" weiter oben in diesem Artikel.

## <a name="specify-a-link-to-financial-dimensions-cell"></a>Zelle „Verknüpfung mit Finanzdimensionen“ angeben
Die Zelle **Mit Finanzdimensionen verknüpfen** enthält Verknüpfungen zu den Finanzdaten, die in jeder Zeile eines Berichts einbezogen werden sollen. Diese Zelle enthält Dimensionswerte. Um das Dialogfeld **Dimensionen** zu öffnen, doppelklicken Sie auf die Zelle **Mit Finanzdimensionen verknüpfen**.

> [!NOTE]
> Berichts-Designer kann keine Konten, Dimensionen oder Felder aus dem Microsoft Dynamics ERP-System auswählen, die eines der folgenden reservierten Zeichen enthalten: &, \*, \[, \], {, oder }. Wenn Sie Informationen für eine Zeile angeben möchten, die bereits in der Zeilendefinition enthalten ist, fügen Sie die Informationen in der Zelle **Verknüpfen mit Finanzdimensionen** hinzu. Um neue Zeilen hinzuzufügen, die mit Finanzdaten verknüpfen, verwenden Sie das Dialogfeld **Zeilen einfügen aus**, um neue Zeilen in der Berichtsdefinition zu erstellen. Die Spaltenüberschrift ändert sich, je nachdem, wie die Spalte konfiguriert wird (siehe folgende Tabelle).

| Ausgewählter Linktyp       | Beschreibung in der Linkspalte |
|----------------------------------|----------------------------------------------------|
| Finanzdimensionen             | Mit Finanzdimensionen verknüpfen                       |
| Berichtsarbeitsblatt                 | Bericht der Finanzberichterstellung                         |

### <a name="specify-a-dimension-or-range"></a>Angeben einer Dimension oder eines Bereichs

1. Im Berichts-Designer öffnen Sie die zu ändernde Zeilendefinition.
2. Doppelklicken Sie auf eine Zelle in der Spalte **Verknüpfen mit Finanzdimensionen**.
3. Doppelklicken Sie im Dialogfeld **Dimensionen** auf eine Zelle unter dem Dimensionsnamen.
4. Wählen Sie im Dialogfeld für die Dimension **Einzelwert oder Bereich** aus.
5. Geben Sie im Feld **Von** die erste Dimension ein oder klicken Sie auf ![Durchsuchen](media/browse.gif "Durchsuchen"), um nach verfügbaren Dimensionen zu suchen. Um einen Bereich von Dimensionen eingeben, geben Sie die Enddimension im Feld **Bis** ein.
6. Klicken Sie auf **OK**, um das Dialogfeld für die Dimension zu schließen. Im Dialogfeld **Dimensionen** wird die aktualisierte Dimension oder der Bereich angezeigt.
7. Klicken Sie auf **OK**, um das Dialogfelds **Dimensionen** zu schließen.

## <a name="display-zero-balance-accounts-in-a-row-definition"></a>Anzeigen von Nullsaldokonten in einer Zeile
Standardmäßig druckt der Berichtsdesigner keine Zeile aus, die nicht ein entsprechendes Saldo in den Finanzdaten aufweist. Daher können Sie eine einzelne Zeilendefinition mit allen natürlichen Segmentwerten oder allen Dimensionswerten erstellen und diese Zeilendefinition beliebig für Ihre Abteilungen verwenden.

### <a name="modify-zero-balance-settings"></a>Bearbeiten von Nullsaldoeinstellungen

1. Öffnen Sie die zu ändernde Berichtsdefinition im Berichts-Designer.
2. Wählen Sie auf der Registerkarte **Einstellungen** unter **Andere Formatierung** Optionen für die Zeilendefinition aus, die in der Berichtsdefinition verwendet wird.
3. Klicken Sie im Menü **Datei** auf **Speichern**, um Ihre Änderungen zu speichern.

## <a name="use-wildcard-characters-and-ranges-in-a-row-definition"></a>Platzhalterzeichen und Bereiche in einer Zeilendefinition verwenden
Wenn Sie einen natürlichen Segmentwert im Dialogfeld **Dimensionen** eingeben, können Sie an jeder Position eines Segments ein Platzhalterzeichen (? oder \*) in jeder Position eines Segments einsetzen. Report Designer extrahiert alle Werte für die definierten Positionen, ohne die Platzhalterzeichen zu berücksichtigen. Zum Beispiel beinhaltet die Zeilendefinition nur natürliche Segmentwerte, und natürliche Segmente haben vier Zeichen. Durch Eingabe von **6???** in einer Zeilendefinition weisen des Berichts-Designers angezeigt, alle Konten einzuschließen, die einen natürlichen Segmentwert haben, die mit 6 beginnt. Wenn Sie **6\**_ eingeben, werden die gleichen Ergebnisse zurückgegeben, wobei die Ergebnisse auch Werte mit variabler Breite enthalten, z. B. _* 60** und **600000**. Der Berichtsdesigner ersetzt jedes Platzhalterzeichen (?) durch den kompletten Bereich möglicher Werte, die Buchstaben und Sonderzeichen enthalten. Zum Beispiel im Bereich von **12? 0** bis **12? 4** wird das Platzhalterzeichen **12? 0** durch den niedrigsten Wert im Zeichensatz ersetzt, und das Platzhalterzeichen in **12? 4** wird durch den höchsten Wert für im Zeichensatz ersetzt.

> [!NOTE]
> Sie sollten Platzhalterzeichen für die Start- und Endkonten von Bereichen vermeiden. Wenn Sie im Start- oder Endkonto Platzhalterzeichen verwenden, werden möglicherweise unerwartete Ergebnisse zurückgegeben.

### <a name="single-segment-or-single-dimension-ranges"></a>Bereiche mit einem einzelnen Segment oder einer einzelnen Dimension

Sie können einen Bereich von Segment- oder Dimensionswerten angeben. Der Vorteil bei der Angabe eines Bereichs ist, dass Sie die Zeilendefinition nicht jedes Mal aktualisieren müssen, wenn ein neuer Segmentwert oder ein Dimensionswert den Finanzdaten hinzugefügt wird. Beispielsweise holt der Bereich **+Account=\[6100:6900\]** die Werte aus den Konten 6100 bis 6900 in den Zeilenbetrag. Wenn ein Bereich ein Platzhalterzeichen (?) umfasst, wertet der Berichtsdesigner den Bereich nicht auf einer Zeichen-pro-Zeichenbasis aus. Stattdessen werden die unteren und oberen Grenzen des Bereichs bestimmt, und dann werden die Endwerte und alle Werte dazwischen eingeschlossen.

> [!NOTE]
> Berichts-Designer kann keine Konten, Dimensionen oder Felder aus dem Microsoft Dynamics ERP-System auswählen, die eines der folgenden reservierten Zeichen enthalten: &, \*, \[, \], {, oder }. Sie können nur dann ein kaufmännisches Und-Zeichen (&) hinzufügen, wenn Sie Zeilendefinitionen automatisch mithilfe des Dialogfelds **Zeilen aus Dimensionen einfügen** erstellen.

### <a name="multiple-segment-or-multiple-dimension-ranges"></a>Bereiche mit mehreren Segmenten oder Dimensionen

Wenn Sie einen Bereich eingeben, indem Sie Kombinationen mehrerer Dimensionswerte verwenden, wird der Bereichsvergleich ..\\financial-dimensions\\dimension-by-dimension durchgeführt. Der Bereichsvergleich kann weder auf Basis von Zeichen-nach-Zeichen noch auf Teilesegmentbasis ausgeführt werden. Beispielsweise umfasst der Bereich **+Konto=\[5000:6000\], Abteilung=\[1000:2000\], Kostenstelle=\[00\]** nur die Konten, die mit jedem Segment übereinstimmen. In diesem Szenario müssen sich die erste Dimension im Bereich von 5000 bis 6000 befinden, muss die andere Dimension im Bereich von 1000 bis 2000 befinden, und die letzte Dimension muss 00 sein. Beispielsweise **+Konto=\[5100\], Abteilung=\[1100\], Kostencenter=\[01\]** ist nicht im Bericht enthalten, da das letzte Segment außerhalb des angegebenen Bereich befindet. Wenn ein Segmentwert Leerzeichen umfasst, schließen Sie diesen Wert in eckige Klammern ein (\[ \]). Folgende Werte sind für ein vier Zeichen langes Segment gültig: **\[ 234\], \[123 \], \[1 34\]**. Dimensionswerte sollen in eckige Klammern eingeschlossen werden (\[ \]), und der Berichtsdesigner fügt diese Klammern für Sie hinzu. Wann enthält ein Bereich mit mehreren Segmenten oder Dimensionen Platzhalterzeichen (? oder \*). Stattdessen werden die unteren und oberen Grenzen des Bereichs bestimmt, und dann werden die Endwerte und alle Werte dazwischen eingeschlossen. Bei einem großen Bereich, wie dem Gesamtbereich der Konten von 40000 bis 99999, sollten Sie ein gültiges Startkonto und Endkonto angeben, wann immer möglich.

> [!NOTE] 
> Berichts-Designer kann keine Konten, Dimensionen oder Felder aus dem Microsoft Dynamics ERP-System auswählen, die eines der folgenden reservierten Zeichen enthalten: &, \*, \[, \], {, oder }. Sie können nur dann ein kaufmännisches Und-Zeichen (&) hinzufügen, wenn Sie Zeilendefinitionen automatisch mithilfe des Dialogfelds **Zeilen aus Dimensionen einfügen** erstellen.

## <a name="add-or-subtract-from-other-accounts-in-a-row-definition"></a>Addieren oder Subtrahieren von anderen Konten in einer Zeilendefinition
Um die Geldbeträge in einem Konto zu den Geldbeträgen in einem anderen Konto zu addieren oder davon zu subtrahieren, können Sie das Pluszeichen (+) und das Minuszeichen (-) in der Zelle **Mit Finanzdimensionen verknüpfen** verwenden. Die folgende Tabelle zeigt die zulässigen Formate für Additions- und Subtraktionslinks zu Finanzdaten.

| Arbeitsgang                                                                               | Verwenden Sie dieses Format                                                                                              |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Addieren Sie zwei vollständig qualifizierte Konten.                                                       | +Division=\[000\], Konto=\[1205\], Abteilung=\[00\]+Division=\[100\], Konto=\[1205\], Abteilung=\[00\] |
| Addieren Sie zwei Segmentwerte.                                                                 | +Konto=\[1205\]+Konto=\[1210\]                                                                           |
| Addieren Sie Segmentwerte, die Platzhalterzeichen enthalten.                                    | +Konto=\[120?+Konto=\[11??\]                                                                             |
| Addieren Sie einen Bereich von zwei vollständig qualifizierte Konten.                                                | +Division=\[000:100\], Konto=\[1205\], Abteilung=\[00\]                                                   |
| Addieren Sie einen Bereich von Segmentwerten.                                                          | +Konto=\[1200:1205\]                                                                                       |
| Addieren Sie einen Bereich von Segmentwerten, die Platzhalterzeichen enthalten.                         | +Konto=\[120?:130?\]                                                                                       |
| Subtrahieren Sie ein vollqualifiziertes Konto von einem anderen vollqualifizierten Konto.              | +Division=\[000\], Konto=\[1205\], Abteilung=\[00\]-Division=\[100\], Konto=\[1205\], Abteilung=\[00\] |
| Subrahieren Sie einen Segmentwert von einem anderen Segmentwert.                                  | +Konto=\[1205\]-Konto=\[1210\]                                                                           |
| Subtrahieren Sie einen Segmentwert, der ein Platzhalterzeichen enthält, von einem anderen Segmentwert. | +Konto=\[1200\]+Konto=\[11??\]                                                                           |
| Subtrahieren Sie einen Bereich zweier vollständig qualifizierter Konten.                                           | -Division=\[000:100\], Konto=\[1200:1205\], Abteilung=\[00:01\]                                           |
| Subtrahieren Sie einen Bereich von Segmentwerten.                                                     | -Konto=\[1200:1205\]                                                                                       |
| Subtrahieren Sie einen Bereich von Segmentwerten, die Platzhalterzeichen enthalten.                    | -Konto=\[120?:130?\]                                                                                       |

Zwar können Sie die Konten direkt ändern, Sie können aber auch das Dialogfeld **Dimensionen** verwenden, um die korrekte Formatierung auf Ihre Finanzdatenverknüpfungen anzuwenden. Jeder der Werte kann ein Platzhalterzeichen einschließen (? oder \*). Berichts-Designer kann jedoch keine Konten, Dimensionen oder Felder aus dem Microsoft Dynamics ERP-System auswählen, die eines der folgenden reservierten Zeichen enthalten: &, \*, \[, \], {, oder }.

> [!NOTE]
> Zum Subtrahieren von Werten müssen Sie diese in Klammern setzen. Wenn Sie beispielsweise **450? - (4509)** eingeben, wird dies als **+Konto=\[4509\]-Konto=\[450?\]** angezeigt, und Sie weisen den Berichtsdesigner an, den Betrag für das Kontosegment 4509 vom Betrag für jedes Kontosegment zu subtrahieren, das mit 450 beginnt.

### <a name="add-or-subtract-accounts-from-other-accounts"></a>Addieren oder subtrahieren von Konten aus anderen Konten

1. Im Berichts-Designer öffnen Sie die zu ändernde Zeilendefinition.
2. Doppelklicken Sie in der entsprechenden Zeile auf die Zelle in der Spalte **Mit Finanzdimensionen verknüpfen**.
3. Führen Sie in der ersten Zeile des **Dimensionen**-Dialogfelds, folgende Schritte aus:

    1. Wählen Sie im ersten Feld alle Dimensionen (Standard) aus, oder klicken Sie auf das Dialogfeld **Dimensionssätze verwalten**, in dem Sie einen Satz erstellen, ändern, kopieren oder löschen können.
    2. Doppelklicken Sie auf die Zelle **Operator +/-**, und wählen Sie den Plus- (**+**) oder Minus- (**-**) Operator aus, der für einen oder mehrere Dimensionswerte oder -sätze in der Zeile gilt.
    3. Doppelklicken Sie in der entsprechenden Dimensionswertspalte auf die Zelle, um das Dialogfeld **Dimensionen** zu öffnen, und wählen Sie aus, ob dieser Dimensionswert für einen Einzelwert oder einen Bereich, ein Dimensionswertsatz oder Summenkonten gilt. Beschreibungen der Felder im Dialogfeld **Dimensionen** finden Sie im Abschnitt "Beschreibung des Dialogfelds "Dimension".
    4. Geben Sie Segmentwerte in der Spalte **Von** und **Bis** ein.

4. Wiederholen Sie die Schritte 2 bis 3, um weitere Vorgänge hinzuzufügen.

> [!NOTE]
> Der Operator gilt für alle Dimensionen in der Zeile.

## <a name="description-of-the-dimensions-dialog-box"></a>Beschreibung des Dialogfelds "Dimensionen".
In der folgenden Tabelle werden die Felder im Dialogfeld **Dimensionen** beschrieben.

| Element                | Beschreibung |
|---------------------|-------------|
| Einzeln oder Bereich | Geben Sie im Feld **Von** den Namen eines Kontos ein oder klicken Sie auf die Schaltfläche **Durchsuchen** ![Durchsuchen](media/browse.gif "Durchsuchen"), um das Konto zu suchen. Um einen Bereich auswählen, geben Sie einen Wert in das Feld **Bis** ein, oder wählen Sie einen Wert aus. |
| Dimensionswertsatz | Geben Sie im Feld **Name** den Namen eines Dimensionswertsatzes ein. Um einen Satz, zu erstellen, zu ändern, zu kopieren oder zu löschen, klicken Sie auf **Dimensionswertsätze verwalten**. Das **Formel**-Feld wird mit der Formel aus der Zelle **Mit Finanzdimensionen verknüpfen** für diesen Dimensionswertsatz aufgefüllt, der in der Zeilendefinition festgelegt ist. |
| Summe Konten   | Geben Sie im Feld **Name** eine Dimension der Summenkonten ein oder suchen Sie danach. Das **Formel**-Feld wird mit der Formel in der Zelle **Mit Finanzdimensionen verknüpfen** für diesen Summenkonto aufgefüllt, das in der Berichtsdefinition festgelegt ist. |

## <a name="add-dimension-value-sets-in-a-row-definition"></a>Hinzufügen von Dimensionswertsätzen zu einer Zeilendefinition
Ein Dimensionswertsatz ist eine benannte Gruppe von Dimensionswerten. Ein Dimensionswertsatz kann nur Werte in einer einzelnen Dimension enthalten, aber Sie können einen Dimensionswertsatz in mehreren Zeilendefinitionen, Spaltendefinitionen, Berichtsbaumstruktur-Definitionen und Berichtsdefinitionen verwenden. Sie können Dimensionswertsätze auch in einer Berichtsdefinition kombinieren. Wenn eine Änderung an den Finanzdaten eine Änderung des Dimensionswertsatzes erforderlich macht, können Sie die Dimensionswertsatz-Definition aktualisieren. Diese Aktualisierung wird dann auf alle Bereiche angewendet, in denen der Dimensionswertsatz verwendet wird. Wenn Sie beispielsweise häufig einen Wertebereich mit einem Link zu den Finanzdaten angeben, z. B. die Werte von 5100 bis einschließlich 5600, können Sie diesen Bereich einem Kontensatz namens „Verkauf“ zuweisen. Nach dem Erstellen eines Dimensionswertsatzes können Sie diesen als Finanzdatenlink auswählen. Weiteres Beispiel: Wenn der Wertebereich von 5100 bis 5600 dem Segment „Verkauf“ und 4175 dem Segment „Rabatte“ zugewiesen ist, können Sie den Gesamtumsatz ermitteln, indem Sie „Rabatte“ von „Verkauf“ subtrahieren. Dieser Vorgang wird angegeben als **(5100:5600)-4175**.

### <a name="create-a-set-of-dimension-values"></a>Erstellen eines Satzes von Dimensionswerten

1. Öffnen Sie im Berichts-Designer die zu ändernde Zeilen-, Spalten- oder Baumstrukturdefinition.
2. Klicken Sie im Menü **Bearbeiten** auf **Dimensionswertsätze verwalten**.
3. Wählen Sie im Dialogfeld **Dimensionswertsätze verwalten** im Feld **Dimension** den Typ des Dimensionswertsatzes aus, der erstellt werden soll, und klicken Sie anschließend auf **Neu**.
4. Geben Sie in Dialogfeld **Neu** einen Namen und eine Beschreibung für den Satz ein.
5. Doppelklicken Sie in der Spalte **Von** auf eine Zelle.
6. Wählen Sie im Dialogfeld **Konto** den Kontonamen in der Liste aus, oder suchen Sie nach den Eintrag im Feld **Suchen** Feld. Klicken Sie anschließend auf **OK**.
7. Wiederholen Sie die Schritte 5 bis 6 in der Spalte **Bis**, um eine Formel für diesen Operator zu entwerfen.
8. Wenn die Formel abgeschlossen ist, klicken Sie auf **OK**.
9. Klicken Sie im Dialogfeld **Dimensionssätze verwalten** auf **Schließen**.

### <a name="update-a-set-of-dimension-values"></a>Aktualisieren eines Dimensionswertsatzes

1. Öffnen Sie im Berichts-Designer die zu ändernde Zeilen-, Spalten- oder Berichtsbaumstruktur-Definition.
2. Klicken Sie im Menü **Bearbeiten** auf **Dimensionswertsätze verwalten**.
3. Wählen Sie im Dialogfeld **Dimensionswertsätze verwalten** im Feld **Dimension** den Dimensionstyp aus.
4. Wählen Sie in der Liste den Dimensionswertsatz aus, der aktualisiert werden soll, und klicken Sie anschließend auf **Ändern**.
5. Ändern Sie im Dialogfeld **Ändern** die Formelwerte, die im Satz enthalten sein sollen.

    > [!NOTE]
    > Wenn Sie neue Konten oder Dimensionen hinzufügen, stellen Sie sicher, dass Sie die vorhandenen Dimensionswertsätze ändern, damit die Änderungen berücksichtigt werden.

6. Doppelklicken Sie auf die Zelle, und wählen Sie den entsprechenden Operator, das **Von**-Konto und das **Bis**-Konto aus.
7. Klicken Sie auf **OK**, um das Dialogfeld **Ändern** zu schließen und die Änderungen zu speichern.

### <a name="copy-a-dimension-set"></a>Kopieren eines Dimensionssatzes

1. Öffnen Sie im Berichts-Designer die zu ändernde Zeilen-, Spalten- oder Berichtsbaumstruktur-Definition.
2. Klicken Sie im Menü **Bearbeiten** auf **Dimensionswertsätze verwalten**.
3. Wählen Sie im Dialogfeld **Dimensionswertsätze verwalten** im Feld **Dimension** den Dimensionstyp aus.
4. Wählen Sie in der Liste den zu kopierenden Satz aus, und klicken Sie anschließend auf **Speichern unter**.
5. Geben Sie einen Namen neuen für den kopierten Satz ein, und klicken Sie auf **OK**.

### <a name="delete-a-dimension-set"></a>Löschen eines Dimensionssatzes

1. Öffnen Sie im Berichts-Designer die zu ändernde Zeilen-, Spalten- oder Berichtsbaumstruktur-Definition.
2. Klicken Sie im Menü **Bearbeiten** auf **Dimensionswertsätze verwalten**.
3. Wählen Sie im Dialogfeld **Dimensionswertsätze verwalten** im Feld **Dimension** den Dimensionstyp aus.
4. Wählen Sie den zu löschenden Satz aus, und klicken Sie auf **Löschen**. Klicken Sie auf **Ja**, um den Dimensionswertsatz dauerhaft zu löschen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Finanzberichterstellung](financial-reporting-intro.md)
