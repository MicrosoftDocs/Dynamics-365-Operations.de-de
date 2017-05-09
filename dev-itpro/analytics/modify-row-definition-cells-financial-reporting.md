---
title: "Ändern von Zeilendefinitionszellen"
description: "Dieser Artikel beschreibt die Informationen, die für jede Zelle in einer Zeilendefinition eines Finanzberichts benötigt werden und erläutert, wie diese Informationen eingegeben werden."
author: RobinARH
manager: AnnBe
ms.date: 2016-03-07 16 - 09 - 06
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: Management Reporter, Core
ms.custom: 58881
ms.assetid: 0af492df-a84e-450c-8045-78ef1211abaf
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: b61364c9055e5c5a63592c7f05551d0c145924b9
ms.lasthandoff: 03/29/2017


---

# <a name="modify-row-definition-cells"></a>Ändern von Zeilendefinitionszellen

Dieser Artikel beschreibt die Informationen, die für jede Zelle in einer Zeilendefinition eines Finanzberichts benötigt werden und erläutert, wie diese Informationen eingegeben werden. 

# <a name="specify-a-row-code-in-a-row-definition"></a>Angeben eines Zeilencodes in einer Zeilendefinition

In den Zeilendefinitionen bestimmen die Zahlen bzw. Beschriftungen in der Zelle **Zeilencode** jede Position in der Zeilendefinition. Sie können den Zeilencode angeben, um Daten in Berechnungen und in den Summen zu verweisen.

### <a name="row-code-requirements"></a>Zeilencodeanforderungen

Ein Zeilencode ist für alle Zeilen erforderlich. Sie können numerische, alphanumerische und nicht festgelegte (leere) Zeilencodes in einer Zeilendefinition Eingabe kombinieren. Der Zeilencode kann eine beliebige positive ganze Zahl (unter 100.000.000) oder eine beschreibende Beschriftung sein, die diese Zeile identifiziert. Eine beschreibende Beschriftung muss diesen Regeln folgen:

-   Die Beschriftung muss mit einem Buchstaben beginnen (a bis z oder A bis Z) und kann eine beliebige Kombination aus Nummern und Buchstaben von bis zu 16 Zeichen sein. **Hinweis:** Eine Beschriftung kann eine Unterstrich (\_) enthalten, aber keine anderen Sonderzeichen.
-   Die Beschriftung kann die folgenden reservierten Wörter nicht verwenden: UND, ODER, WENN, DANN SONST, PERIODEN, ZU, BASEROW, EINHEIT, NULL, CPO oder RPO.

Die folgenden Beispiele sind gültige Zeilencodes:

-   320
-   TL\_NET\_INCOME
-   TL\_NET\_94

### <a name="change-a-row-code-in-a-row-definition"></a>Ändern eines Zeilencodes in einer Zeilendefinition

1.  Klicken Sie im Berichts-Designer auf die **Zeilendefinitionen** und öffnen dann die Zeilendefinition, um sie zu ändern.
2.  Geben Sie in der entsprechenden Zeile den neuen Wert in der Spalte **Zeilencode** ein.

### <a name="reset-numeric-row-codes"></a>Zurücksetzen numerischer Zeilencodes

1.  Im Berichts-Designer klicken Sie auf die **Zeilendefinitionen** und öffnen dann die Zeilendefinition, um sie zu ändern.
2.  Klicken Sie im Menü **Bearbeiten** auf **Zeilen neu nummerieren**.
3.  Geben Sie im Dialogfeld **Zeilen neu nummerieren** neue Werte für den Anfangszeilencode und das Zeilencodeinkrement an. Sie können die numerische Zeilencodes auf die äquidistante Werte zurücksetzen. Der Berichtsdesigner nummeriert jedoch nur Zeilencodes neu, die mit Zahlen beginnen (beispielsweise 130 oder 246). Es nummeriert keine Zeilencodes neu, die mit Buchstaben beginnen (beispielsweise INCOME\_93 oder TP0693). **Hinweis:** Wenn Sie Zeilencodes neu nummerieren, aktualisiert der Berichtsdesigner **TOT** und **CAL**-Referenzen automatisch. Wenn sich beispielsweise eine **TOT**-Zeile auf einen Bereich bezieht, der mit Zeilencode 100 beginnt, und Sie Zeilen beginnend mit 90 neu nummerieren, verweist der Anfangs-**TOT** Änderungen von 100 bis 90.

## <a name="add-a-description"></a>Hinzufügen einer Beschreibung
Die Beschreibungszelle stellt die Beschreibung der Finanzdaten in der Zeile des Berichts, wie " Umsatzerlöse" oder "Nettoeinkommen" bereit. Der Text in der Zelle **Beschreibung** wird im Bericht genau, wie in der Zeilendefinition eingeben angezeigt. **Hinweis:** Die Breite der Spalte "Beschreibung" im Bericht wird in der Spaltendefinition festgelegt. Wenn der Text in der Spalte **Beschreibung** in der Zeilendefinition lang ist, überprüfen Sie die Breite der **DESC**-Spalte. Wenn Sie das Dialogfeld **Zeilen einfügen aus** verwenden, sind die Werte in der Spalte **Beschreibung** die Segmentwerte oder die Dimensionswerte aus den Finanzdaten. Sie können Zeilen einfügen, um beschreibenden Text, wie eine Abschnittsüberschrift oder eine Abschnittssumme hinzuzufügen, und um Formatierung, wie eine Position vor einer Zeilensumme, hinzuzufügen. Wenn der Bericht eine Berichtsbaumstruktur umfasst, können Sie den zusätzlichen Text einbeziehen, der für die Berichtseinheiten in der Berichtsbaumstruktur definiert ist. Sie können den zusätzlichen Text auf eine bestimmte Berichtseinheit begrenzen.

### <a name="add-the-description-for-a-line-on-a-report"></a>Hinzufügen der Beschreibung für eine Position in einem Bericht

1.  Im Berichts-Designer klicken Sie auf die **Zeilendefinitionen** und öffnen dann die Zeilendefinition, um sie zu ändern.
2.  Wählen Sie die Zelle **Beschreibung** aus, und geben Sie dann den Namen der Berichtszeile ein.
3.  Wenden Sie die Formatierung an.

### <a name="add-additional-text-from-a-reporting-tree-in-the-description"></a>Hinzufügen von zusätzlichem Text aus einer Berichtsbaumstruktur in der Beschreibung

1.  Im Berichts-Designer klicken Sie auf die **Zeilendefinitionen** und öffnen dann die Zeilendefinition, um sie zu ändern.
2.  Geben Sie den Code des zusätzlichen Textes und einen beliebigen anderen Text in der entsprechenden Zelle **Beschreibung** ein.
3.  Wenden Sie die Formatierung an.

### <a name="limit-the-additional-text-to-a-specific-reporting-unit"></a>Begrenzen des zusätzlichen Texts auf eine bestimmte Berichtseinheit.

1.  Im Berichts-Designer klicken Sie auf die **Zeilendefinitionen** und öffnen dann die Zeilendefinition, um sie zu ändern.
2.  Suchen Sie die Zeile, in der zusätzlicher Text erstellt werden soll, und doppelklicken Sie auf die Zelle in der Spalte **Verwandte Formeln/Zeilen/Einheiten**.
3.  Wählen Sie im Dialogfeld **Auswahl der Berichtseinheit** im Feld **Berichtsstruktur** eine Berichtsbaumstruktur aus.
4.  Erweitern oder reduzieren Sie die Berichtsbaumstruktur im Feld **Berichtseinheit für Einschränkung auswählen** , und wählen Sie dann eine Berichtseinheit aus.

## <a name="add-a-format-code"></a>Hinzufügen eines Formatcodes
Die Zelle **Formatcode** bietet eine Auswahl von vorformatierten Auswahlmöglichkeiten für den Inhalt dieser Zeile an. Wenn die **Formatcode**-Zelle leer ist, wird die Zeile als Finanzdatendetailzeile interpretiert. **Hinweis:** Wenn ein Bericht Formatierungszeilen enthält, die keine Betragszeilen sind aber Betragszeilen zugeordnet sind, die, (beispielsweise aufgrund der Nullsalden) unterdrückt wurden, können Sie die Spalte **Verwandte Formeln/Zeilen/Einheiten** verwenden, um zu verhindern, dass Titel- und Formatzeilen gedruckt werden.

### <a name="add-a-format-code-to-a-report-row"></a>Hinzufügen eines Formatcodes zu einer Berichtszeile

1.  Im Berichts-Designer klicken Sie auf die **Zeilendefinitionen** und wählen dann eine Zeilendefinition, um sie zu ändern.
2.  Doppelklicken Sie auf die Zelle **Formatcode**.
3.  Wählen Sie in der Liste einen Formatcode aus. Die folgende Tabelle beschreibt die Formatcodes und deren Aktionen.
    | Formatcode                   | Interpretation des Formatcodes | Aktion|
    |---|---|---|
    | (Keine)                        |                                    | Löscht die **Formatcode**-Zelle.                                                                                                                                                                               |
    | TOT                           | Summe                              | Kennzeichnet eine Zeile, die mathematische Operatoren in der Spalte **Verwandte Formeln/Zeilen/Einheiten** verwendet. Summen enthalten einfache Operatoren, wie **+** oder **-**.                                                      |
    | CAL                           | Herstellkostenkalkulation                        | Kennzeichnet eine Zeile, die mathematische Operatoren in der Spalte **Verwandte Formeln/Zeilen/Einheiten** verwendet. Berechnungen enthalten komplexe Operatoren, wie  **+**, **-**, **\***, **/** und **IF/THEN/ELSE** Anweisungen. |
    | DES                           | Beschreibung                        | Kennzeichnet eine Überschriftposition oder eine leere Position in einem Bericht.                                                                                                                                                        |
    | LFT RGT CEN                   | Links, rechts, zentriert                  | Richtet den Zeilenbeschreibungstext auf der Berichtsseite aus, unabhängig von der Platzierung des Texts in der Spaltendefinition.                                                                                               |
    | CBR                           | Basis-Zeile ändern                    | Kennzeichnet eine Zeile, die die Basiszeile für Spaltenberechnungen festlegt.                                                                                                                                               |
    | SPALTE                        | Spaltenumbruch                       | Hiermit wird eine neue Spalte im Bericht gestartet.                                                                                                                                                                             |
    | SEITE                          | Seitenumbruch                         | Hiermit wird eine neue Seite im Bericht gestartet.                                                                                                                                                                               |
    | ---                           | Einzelner Unterstrich                   | Setzt eine einzelne Linie unter alle Betragsspalten in den Bericht.                                                                                                                                                     |
    | ===                           | Doppelter Unterstrich                   | Setzt eine doppelte Linie unter alle Betragsspalten in den Bericht.                                                                                                                                                     |
    | LINE1                         | Dünne Linie                          | Zeichnet eine einzelne dünne Linie über die Seite.                                                                                                                                                                      |
    | LINE2                         | Dicke Linie                         | Zeichnet eine einzelne dicke Linie über die Seite.                                                                                                                                                                     |
    | LINE3                         | Punktierte Linie                        | Zeichnet eine punktierte Linie über die Seite.                                                                                                                                                                    |
    | LINE4                         | Dicke und dünne Linie           | Zeichnet eine doppelte Linie über die Seite. Die ober Linie ist dick und die untere ist dünn.                                                                                                                       |
    | LINE5                         | Dünne und dicke Linie           | Zeichnet eine doppelte Linie über die Seite. Die ober Linie ist dünn und die untere ist dick.                                                                                                                       |
    | BXB BXC                       | Umrandete Zeile                          | Zieht einen Kasten um die Berichtszeilen, die mit der **BXB**-Zeile beginnen und mit der **BXC**-Zeile beenden.                                                                                                               |
    | ANM                           | Bemerkung                             | Kennzeichnet eine Zeile, die eine Kommentarzeile ist und nicht im Bericht gedruckt werden soll. Beispielsweise erklärt möglicherweise eine Hinweiszeile Ihr Formatierungsverfahren.                                                            |
    | SORT ASORT SORTDESC ASORTDESC | Sortieren                               | Sortiert Ausgaben oder Umsatzerlöse, sortiert einen tatsächlichen oder Abweichungsbericht nach der größten Abweichung oder sortiert Zeilenbeschreibungen alphabetisch.                                                                   |

## <a name="specify-related-formulasrowsunits"></a>Angeben verwandter Formeln/Zeilen/Einheiten
Die Zelle **Verwandte Formeln/Zeilen/Einheiten** hat mehrere Zwecke. Je nach Art der Zeile, kann eine **Verwandte Formeln/Zeilen/Einheiten**-Zelle eine der folgenden Aufgaben ausführen:

-   Definieren der Zeilen, die in die Berechnung einzubezogen werden, wenn Sie einen **TOT**-Formatcode oder einen **CAL**-Formatcode verwenden.
-   Verknüpfen Sie eine Formatierungszeile mit einer Betragszeile, damit die Formatierung nur gedruckt wird, wenn der zugehörige Betrag gedruckt wird.
-   Schränken Sie einer Zeile auf eine bestimmte Berichtseinheit ein.
-   Definieren Sie die niedrige Basiszeile für Berechnungen, wenn Sie den Formatcode **BASEROW** verwenden.
-   Definieren Sie die zu sortierenden Zeilen, wenn Sie eine der Sortierenformatcodes verwenden.

### <a name="use-a-row-total-in-a-row-definition"></a>Verwenden einer Zeilensumme in einer Zeilendefinition

Verwenden Sie eine Zeilengesamtformel, um Beträge in anderen Zeilen zu addieren oder zu subtrahieren. Eine Formel zum Erstellen einer Zeilensumme kann + und - Operatoren enthalten, um einzelner Zeilencodes und Bereiche zusammenzufassen. Bereiche werden durch ein Trennzeichen angegeben (:). Die Formel kann 1.024 Zeichen enthalten. Dies ist ein Beispiel einer Standardsummenformel: 400+420+430+450+460LIABILITIES+EQUITY520: 546520:546-LIABILITIES

### <a name="components-of-a-row-total-formula"></a>Komponenten einer Zeilengesamtformel

Wenn Sie eine Zeilensummenformel erstellen, müssen Sie Zeilencodes verwenden, um anzugeben, welche Zeilen in der aktuelle Zeilendefinition addiert oder subtrahiert werden sollen, und Sie müssen Operatoren verwenden, um festzulegen, wie die Zeilen kombiniert werden. Summenzeilen und Betragszeilen können in allen möglichen Kombinationen verwendet werden. **Hinweis:** Alle Summenzeilen in einem Bereich werden nicht berücksichtigt. Um einen Gesamtbetrag zu erstellen, können Sie den Bereich von Zeilen angeben. Wenn die erste Zeile eines Bereichs eine Summenzeile ist, wird diese Zeile in der neuen Summe einbezogen. In der folgenden Tabelle wird beschrieben, wie Operatoren in den Zeilensummenformeln verwendet werden.

| Bediener | Beispielformel | Beschreibung                                                 |
|----------|-----------------|-------------------------------------------------------------|
| +        | 100+330         | Addiert den Betrag in Zeile 100 zum Betrag in Zeile 330.        |
| :        | 100:330         | Addiert die Summen aller Zeilen zwischen Zeile 100 und 330 Zeile.    |
| -        | 100-330         | Subtrahiert den Betrag in Zeile 100 von dem Betrag in Zeile 330. |

### <a name="create-a-row-total"></a>Erstellen einer Zeilensumme

1.  Im Berichts-Designer klicken Sie auf die **Zeilendefinitionen** und öffnen dann die Zeilendefinition, um sie zu ändern.
2.  Doppelklicken Sie auf die Zelle **Formatcode** in der Zeilendefinition, und wählen Sie **TOT** aus.
3.  Geben Sie in die Zelle **Verwandte Formeln/Zeilen/Einheiten** die Summenformel ein.

### <a name="relate-a-format-row-to-an-amount-row"></a>Zuordnen einer Formatzeile zu einer Betragszeile

In der Spalte **Formatcode** in einer Zeilendefinition wird Formatierung mit den Formatcodes **DES**, **LFT**, **RGT**, **CEN** **---** und **===** auf Zeile, die keine Beträge enthalten, angewendet. Damit diese Formatierung nicht gedruckt wird, wenn die zugehörigen Betragszeilen unterdrückt werden (beispielsweise, da die Betragszeilen Nullwerte oder keine Periodenaktivität enthalten), müssen Sie die Formatzeilen den entsprechenden Betragszeilen zuordnen. Diese Funktion ist hilfreich, wenn Sie verhindern möchten, dass Überschriften oder Formatierung von Zwischensummen gedruckt werden, wenn es keine auszudruckenden Details während der Periode gibt. **Hinweis:** Sie können auch verhindern, dass die detaillierten Betragszeilen gedruckt werden, indem Sie die Option zum Anzeigen der Zeilen ohne Beträge deaktivieren. Diese Option befindet sich auf der Registerkarte **Einstellungen** der Berichtsdefinition. Standardmäßig werden Buchungsdetailkonten, mit Nullsaldo oder ohne Periodenaktivität, in Berichten unterdrückt. Um diese Transaktionsdetailkonten anzuzeigen, aktivieren Sie das Kontrollkästchen **Zeilen ohne Beträge anzeigen** auf der Registerkarte **Einstellungen** der Berichtsdefinition.

### <a name="relate-a-format-row-to-an-amount-row"></a>Zuordnen einer Formatzeile zu einer Betragszeile

1.  Im Berichts-Designer klicken Sie auf die **Zeilendefinitionen** und wählen dann eine Zeilendefinition, um sie zu ändern.
2.  Geben Sie in der Formatierungszeile in der Zelle **Verwandte Formeln/Zeilen/Einheiten** den Zeilencode der Betragszeile ein, die unterdrückt werden soll. **Hinweis:** Um eine Betragszeile zu unterdrücken, muss der Saldo der Zeile 0 (null) sein. Eine Betragszeile, die einen Saldo aufweist, wird nicht unterdrückt.
3.  Klicken Sie im Menü **Datei** auf **Speichern**.

### <a name="example-of-preventing-printing-of-rows"></a>Beispiel, wie das Drucken von Zeilen verhindert wird

Im folgenden Beispiel möchte Phyllis die Überschrift und die Unterstriche in der Zeile **Bargeld gesamt** ihres Berichts nicht drucken, da es in keiner der Kassenkonten Aktivitäten gab. Daher gibt Sie in Zeile 220 (die, wie der **---**Formatcode angibt, eine Formatierungszeile ist) in der Zelle **Verwandte Formeln/Zeilen/Einheiten** den Wert **250** ein. Dies ist der Zeilencode der Betragszeile, die sie unterdrücken möchte. [![RelatedRowsRowDefinition](./media/relatedrowsrowdefinition-1024x144.png)](./media/relatedrowsrowdefinition.png)

## <a name="select-the-base-row-for-a-column-calculation"></a>Auswählen der Basiszeile für eine Spaltenberechnung
In der relationalen Berichterstellung weisen Sie eine oder mehrere Basiszeilen der Zeilendefinition zu, indem Sie den Formatcode **CBR** (Basiszeile ändern) verwenden. Eine Basiszeile wird dann durch eine Berechnung in der Spaltendefinition verwiesen. Hier ein typisches Beispiele für CBR_Berechnungen:

-   Prozentsatz des gesamten Umsatzerlöses, wie es den einzelnen Umsatzerlöselementen zugeordnet ist
-   Prozentsatz der Gesamtausgaben, wie sie den einzelnen Ausgabenelementen zugeordnet sind
-   Prozentsatz des Bruttogewinns, wie er den Division- oder Abteilungsdetails zugeordnet ist.

Eine oder mehrere Basiszeilen werden in der Zeilendefinition definiert, und die Spaltendefinition bestimmt dann die Beziehung, auf der die Basiszeile gemeldet wird. Der Code, der in der Spaltenformel verwendet wird, ist **BASEROW**. Die folgenden grundlegenden mathematischen Arbeitsgänge werden mit **BASEROW** verwendet: Dividieren, multiplizieren, addieren oder subtrahieren. Der Arbeitsgang, der am häufigsten verwendet wird, ist die Division durch **BASEROW**, wo das Ergebnis als Prozentsatz angezeigt wird. Spaltenberechnungen, bei denen **BASEROW** in der Formel verwendet werden, verwenden die Zeilendefinition für die zugehörigen Basiszeilencodes. **CBR** Zeilen haben folgende Merkmale:

-   **CBR** Zeilen werden im ausgefüllten Bericht nicht gedruckt.
-   Der **CBR**-Formatcode und der entsprechende Zeilencode werden über der Zeile oder dem Abschnitt positioniert, die bzw. der zusammenhängende Berechnungen anzeigt.

In einer Spaltendefinition gibt **CALC** den Spaltentyp eine Spalte an, die eine Formel in der Zeile **Formel** angibt. Diese Formel arbeitet auf den Daten für diese Spalte des Berichts und verwendet das Baserow-Schlüsselwort, um Berechnungen für den Formatcode **CBR** in der Zeile zu basieren. In der Zeilendefinition definiert der **CBR**-Formatcode die Basiszeile für Spalten, die einen Prozentsatz der Basiszeile für jede Zeile im Bericht berechnen oder damit multiplizieren. Sie können über mehrere Formatcodes **CBR** in einem Zeilenformat verfügen, wie eines für den Nettoumsatz, eines für den Bruttoumsatz und eines für die Gesamtkosten. Normalerweise wird der **CBR**-Formatcode verwendet, um einen Prozentsatz für Konten zu erstellen, die in einer Summenposition verglichen werden. Eine Basiszeile wird für alle Berechnungen verwendet, bis eine andere Basiszeile definiert ist. Sie müssen einen **CBR**-Anfangsformatcode und einen **CBR **-Endeformatcode definieren. Um beispielsweise Ausgaben als Prozentsatz des Nettoumsatzes zu bestimmen, können Sie den Wert in jeder Ausgabenenzeile durch den Wert in der Nettoumsatzzeile dividieren. In diesem Fall ist die Nettoumsatzzeile die Basiszeile. Sie können eine Spaltendefinition definieren, die die aktuellen Ergebnisse und die seit Jahresbeginn zusammen mit einem Basisprozentsatz jedes Ergebnisses meldet, wie im folgenden Beispiel dargestellt. Beginnen Sie mit einer detaillierten Einkommensaufstellung.

### <a name="select-the-base-row-in-a-row-definition-for-a-column-calculation"></a>Auswählen der Basisdefinition in einer Zeilendefinition für eine Spaltenberechnung

1.  Klicken Sie im Berichts-Designer auf **Spaltendefinitionen**, und öffnen Sie anschließend die Spaltendefinition für eine Einkommensaufstellung.
2.  Fügen Sie der Spaltendefinition eine neue Spalte hinzu, und legen Sie den Spaltentyp auf **CALC** fest.
3.  Geben Sie in der **Formel**-Zelle der neuen Spalte die Formel **X/BASEROW** ein, wobei **X** der **FD**-Spaltentyp ist, von dem ein Prozentsatz angezeigt wird.
4.  Doppelklicken Sie auf die Zelle **Format/Währungsaußerkraftsetzung**.
5.  Wählen Sie im Dialogfeld **Formataußerkraftsetzung** in der Liste die **Formatkategorie** die Option **Prozentsatz** aus, und klicken Sie anschließend auf **OK**.
6.  Klicken Sie im Menü **Datei** auf **Speichern unter**, um die Spaltendefinition unter einem neuen Namen zu speichern. Fügen Sie dem aktuellen Dateinamen **CBR** an (**CUR\_YTD\_CBR**). Diese Spaltendefinition ist Ihre Basiszeilen-Spaltendefinition.
7.  Klicken Sie im Berichts-Designer auf **Zeilendefinitionen**, und öffnen Sie anschließend die Zeilendefinition, die durch die Basiszeilenberechnung geändert werden soll.
8.  Fügen Sie eine neue Zeile oberhalb der Zeile ein, in der die Basiszeilenberechnung beginnen soll.
9.  Doppelklicken Sie auf die Zelle **Formatcode** der Zeilendefinition, und wählen Sie dann **CBR** aus.
10. Geben Sie in Zelle **Verwandte Formeln/Zeilen/Einheiten** die Zeilencodenummer für die Basiszeile ein.

### <a name="example-of-base-row-calculation"></a>Beispiel für eine Basiszeilenberechnung

Im folgenden Beispiel einer Zeilendefinition zeigt Zeile 100, dass die Basiszeile für Berechnungen Zeile 280 ist. [![Beispiel für eine Basiszeilenberechnung](./media/cbrrowdefinition.png)](./media/cbrrowdefinition.png) Im folgenden Beispiel für eine Spaltendefinition verwenden die Berechnungen den **CBR**-Formatcode. Die Berechnung in Spalte C dividiert den Wert in Spalte B des Berichts durch den Wert in Zeile 280 der Spalte B. Die Formataußerkraftsetzung in Spalte B druckt das Berechnungsergebnis als Prozentsatz. Ebenso weißt jeder Betrag in der Spalte E den Betrag in der Spalte D als Prozentsatz des Nettoumsatzes auf. [![Spaltendefinitionsbeispiel](./media/cbrcolumndefinition2.png)](./media/cbrcolumndefinition2.png) Das folgende Beispiel zeigt einen Bericht, der möglicherweise auf Basis der vorherigen Berechnungen generiert wird. [![Beispielsbericht auf Grundlage vorheriger Beispielberechnungen.](./media/cbrreport-1024x272.png)](./media/cbrreport.png)

## <a name="select-a-sorting-code-for-a-row-definition"></a>Auswählen eines Sortiercodes für eine Zeilendefinition aus
Sortiercodes sortieren Konten oder Werte, sortieren einen Ist- oder Abweichungsbericht nach der größten Abweichung oder sortieren Zeilenbeschreibungen alphabetisch. Die folgenden Statuscodes sind verfügbar:

-   **SORTIEREN** - Sortiert den Bericht anhand der Werte in der angegebenen Spalte in aufsteigender Reihenfolge.
-   **ASORT** - Sortiert den Bericht anhand der absoluten Werte der Werte in der angegebenen Spalte in aufsteigender Reihenfolge. Das bedeutet, dass das Vorzeichen jedes Werts ignoriert wird, wenn die Werte sortiert werden. Dieser Formatcode ordnet die Werte nach Größe der Abweichung, unabhängig davon, ob die Abweichung positiv oder negativ ist.
-   **SORTDESC** - Sortiert den Bericht anhand der Werte in der angegebenen Spalte in absteigender Reihenfolge.
-   **ASORTDESC** - Sortiert den Bericht basierend auf dem absoluten Wert der Werte in der angegebenen Spalte in absteigender Reihenfolge.

### <a name="select-a-sorting-code"></a>Auswählen eines Sortiercodes

1.  Im Berichts-Designer klicken Sie auf die **Zeilendefinitionen** und öffnen dann die Zeilendefinition, um sie zu ändern.
2.  Doppelklicken Sie auf die Zelle **Formatcode**, und wählen Sie dann einen Sortiercode aus.
3.  Geben Sie in der Zelle **Verwandte Formeln/Zeilen/Einheiten** den Bereich der Zeilencodes an, die sortiert werden sollen. Um einen Bereich anzugeben, geben Sie den ersten Zeilencode, ein Trennzeichen (:) und dann den Code der letzten Zeile ein. Geben Sie z. B. **160:490** ein, um anzugeben, dass der Bereich von Zeile 160 bis Zeile 490 reicht.
4.  Geben Sie in der Zelle **Spalteneinschränkung** den Buchstaben der Berichtsspalte ein, der zum Sortieren verwendet werden soll. **Hinweis:** Es werden nur Betragszeilen in einer Sortierungsberechnung eingeschlossen.

### <a name="examples-of-ascending-and-descending-column-values"></a>Beispiele für absteigende und absteigende Spaltenwerte

Im folgenden Beispiel werden die Werte in Spalte "D" des Berichts in aufsteigender Reihenfolge für Zeilen 160 bis 490 sortiert. Zusätzlich werden die absoluten Werte in Spalte "G" des Berichts in absteigender Reihenfolge für Zeilen 610 bis 940 sortiert.

| Zeilencode | Beschreibung                                         | Formatcode | Verwandte Formeln/Zeilen/Einheiten | Normaler Saldo | Spalteneinschränkung | Mit Finanzdimensionen verknüpfen |
|----------|-----------------------------------------------------|-------------|-----------------------------|----------------|--------------------|------------------------------|
| 100      | Sortiert nach Monatsabweichung in aufsteigender Reihenfolge       | DES         |                             |                |                    |                              |
| 130      |                                                     | SORT        | 160:490                     |                | S                  |                              |
| 160      | Verk.                                               |             |                             | C:              |                    | 4100                         |
| 190      | Retouren                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 490      | Zinserträge                                     |             |                             | C:              |                    | 7000                         |
| 520      |                                                     | DES         |                             |                |                    |                              |
| 550      | Sortiert nach absoluter Abweichung seit Jahresbeginn in absteigender Reihenfolge | DES         |                             |                |                    |                              |
| 580      |                                                     | ASORTDESC   | 610:940                     |                | G:                  |                              |
| 610      | Verk.                                               |             |                             | C:              |                    | 4100                         |
| 640      | Retouren                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 940      | Zinserträge                                     |             |                             | C:              |                    | 7000                         |

Hier ist ein Beispiel des erzeugten Berichts.

**Abweichungsanalyse (Sortiert nach Abweichung)**

**Peking- und Atlanta-Regionen**

**Für die sieben Monate, die zum 31. Juli 2013 enden**

**Juli**

**Seit Jahresbeginn**

**Istwert**

**Budget**

**Abweichung**

**Istwert**

**Budget**

**Abweichung**

**Sortiert nach Monatsabweichung in aufsteigender Reihenfolge**

COGS (Wareneinsatz)

873.872

236.144

(637.728)

4.864.274

1.590.315

(3.273.959)

Gehälter und Löhne

97.624

65.573

(32.051)

653.884

441.664

(212.220)

Verkaufsrabatte

36.383

24.152

(12.231)

241.562

162.670

(78.892)

Retouren

10.917

7.246

(3.671)

62.809

48.803

(14.006)

Mietausgaben

12.052

9.019

(3.033)

80.444

60.748

(19.696)

Bürounkosten

5.023

3.291

(1.732)

33.420

22.098

(11.322)

Reisekosten

7.656

7.641

(15)

51.062

51.469

407

Verk.

1.240.119

410.389

829.730

7.139.288

2.764.549

4.374.739

**Sortiert nach absoluter Abweichung seit Jahresbeginn in absteigender Reihenfolge**

Verk.

1.240.119

410.389

829.730

7.139.288

2.764.549

4.374.739

Reisekosten

7.656

7.641

(15)

51.062

51.469

407

Bürounkosten

5.023

3.291

(1.732)

33.420

22.098

(11.322)

Retouren

10.917

7.246

(3.671)

62.809

48.803

(14.006)

Mietausgaben

12.052

9.019

(3.033)

80.444

60.748

(19.696)

Verkaufsrabatte

36.383

24.152

(12.231)

241.562

162.670

(78.892)

Gehälter und Löhne

97.624

65.573

(32.051)

653.884

441.664

(212.220)

COGS (Wareneinsatz)

873.872

236.144

(637.728)

4.864.274

1.590.315

(3.273.959)

## <a name="specify-a-format-override-cell"></a>Angeben einer Formataußerkraftsetzungszelle an
Die Zelle **Formataußerkraftsetzung** gibt die Formatierung an, die für die Zeile verwendet wird, wenn der Bericht gedruckt wird. Diese Formatierung setzt die Formatierung außer Kraft, die in der Spaltendefinition und in der Berichtsdefinition angegeben ist. Standardmäßig ist die im Formular angegebene Formatierung dieser Definitionen "Währung". Wenn eine Zeile des Berichts die Anzahl der Anlagen aufführt, wie die Anzahl von Gebäuden, und eine andere Zeile den Geldwert dieser Anlagen aufführt, können Sie die Währungsformatierung außerkraftsetzen und numerische Formatierung für die Zeile eingeben, in der die Anzahl der Gebäuden angegeben wird. Sie geben diese Informationen im Dialogfeld **Formataußerkraftsetzung** an. Die verfügbaren Optionen hängen von der Formatkategorie ab, die Sie auswählen. Der **Beispiel**-Bereich des Dialogfelds zeigt Beispielsformate an. Die folgenden Formatkategorien stehen zur Verfügung:

-   Währungsformatierung
-   Numerische Formatierung
-   Prozentsatzformatierung
-   Benutzerdefinierte Formatierung

### <a name="override-cell-formatting"></a>Zellenformatierung außer Kraft setzen

1.  Im Berichts-Designer öffnen Sie die zu ändernde Zeilendefinition.
2.  Doppelklicken Sie in der Zeile, deren Format außer Kraft gesetzt werden soll, auf die Zelle in der Spalte **Formataußerkraftsetzung**.
3.  Wählen Sie im Dialogfeld **Formataußerkraftsetzung** die Formatierungsoptionen aus, die für diese Zeile im Bericht verwendet werden sollen.
4.  Klicken Sie auf **OK**.

### <a name="currency-formatting"></a>Währungsformatierung

Währungsformatierung bezieht sich auf einen steuerlichen Betrag und schließt das Währungssymbol ein. Die folgenden Optionen sind verfügbar:

-   **Währungssymbol** - Das Währungssymbol für den Bericht. Dieser Wert setzt die Einstellungen für **Regionale Optionen** für die Unternehmensdaten außer Kraft.
-   **Negativen Zahlen** - Negativen Zahlen können ein Minuszeichen aufweisen (-), sie können in Klammern angezeigt werden, oder sie können ein Dreieck (∆) aufweisen.
-   **Dezimalstellen** - Die Anzahl der angezeigten Stellen nach der Dezimalstelle.
-   **Text für Außerkraftsetzung des Nullwerts** - Der in den Bericht einzuschließende Text, wenn der Betrag 0 (null) ist. Dieser Text wird als letzte Zeile im **Beispiel**-Bereich angezeigt. **Hinweis:** Wenn das Drucken für Nullwerte oder keine Periodenaktivität unterdrückt wird, wird der Text unterdrückt.

### <a name="numeric-formatting"></a>Numerische Formatierung

Numerische Formatierung bezieht sich auf jeden Betrag und schließt kein Währungssymbol ein. Die folgenden Optionen sind verfügbar:

-   **Negativen Zahlen** - Negativen Zahlen können ein Minuszeichen aufweisen (-), sie können in Klammern angezeigt werden, oder sie können ein Dreieck (∆) aufweisen.
-   **Dezimalstellen** - Die Anzahl der angezeigten Stellen nach der Dezimalstelle.
-   **Text für Außerkraftsetzung des Nullwerts** - Der in den Bericht einzuschließende Text, wenn der Betrag 0 (null) ist. Dieser Text wird als letzte Zeile im **Beispiel**-Bereich angezeigt. **Hinweis:** Wenn das Drucken für Nullwerte oder keine Periodenaktivität unterdrückt wird, wird der Text unterdrückt.

### <a name="percentage-formatting"></a>Prozentsatzformatierung

Prozentsatzformatierung umfasst das Prozentzeichen (%). Die folgenden Optionen sind verfügbar:

-   **Negativen Zahlen** - Negativen Zahlen können ein Minuszeichen aufweisen (-), sie können in Klammern angezeigt werden, oder sie können ein Dreieck (∆) aufweisen.
-   **Dezimalstellen** - Die Anzahl der anzuzeigenden Stellen nach der Dezimalstelle.
-   **Text für Außerkraftsetzung des Nullwerts** - Der in den Bericht einzuschließende Text, wenn der Betrag 0 (null) ist. Dieser Text wird als letzte Zeile im **Beispiel**-Bereich angezeigt. **Hinweis:** Wenn das Drucken für Nullwerte oder keine Periodenaktivität unterdrückt wird, wird der Text unterdrückt.

### <a name="custom-formatting"></a>Benutzerdefinierte Formatierung

Verwenden Sie die benutzerdefinierte Formatierungskategorie, um eine benutzerdefinierte Formataußerkraftsetzung zu erstellen. Die folgenden Optionen sind verfügbar:

-   **Typ** - Das benutzerdefinierten Format.
-   **Text für Außerkraftsetzung des Nullwerts** - Der in den Bericht einzuschließende Text, wenn der Betrag 0 (null) ist. Dieser Text wird als letzte Zeile im **Beispiel**-Bereich angezeigt. **Hinweis:** Wenn das Drucken für Nullwerte oder keine Periodenaktivität unterdrückt wird, wird der Text unterdrückt.

Der Typ sollte den positiven Wert und dann den negativen Wert darstellen. In der Regel geben Sie eine ähnliches Format ein, das positive und negative Werte unterscheidet. Um beispielsweise anzugeben, dass positive und negative Werte zwei Dezimalstellen enthalten, aber negative Werte in Klammern angezeigt werden, geben Sie **0,00; (0,00)** ein. In der folgenden Tabelle werden benutzerdefinierten Formate angezeigt, die Sie verwenden können, um das Format der Werte zu steuern. Alle diese Beispiele beginnen mit dem Wert 1234,56.

| Format                         | Positiv   | Negativ     | Null    |
|--------------------------------|------------|--------------|---------|
| 0                              | 1235       | -1235        | 0       |
| 0;0                            | 1235       | 1235         | 0       |
| 0;(0);-                        | 1235       | 1235         | -       |
| \#,\#\#\#;(\#,\#\#\#);“”       | 1.235      | (1.235)      | (Leer) |
| \#,\#\#0.00;(\#,\#\#0.00);zero | 1.234.56   | (1.234,56)   | Null    |
| 0,00 %;(0,00 %)                  | 123456,00 % | (123456,00 %) | 0,00 %   |

## <a name="specify-a-normal-balance-cell"></a>Angeben einer normalen Saldozelle
Die Zelle **Normaler Saldo** in einer Zellendefinition steuert das Vorzeichen der Beträge in einer Zeile. Um das Vorzeichen einer Zeile umzukehren, oder wenn der normale Saldo eines Kontos ein Habenposten ist, geben ein **C** in die Zelle **Normales Saldo** für diese Zeile ein. Report-Design kehrt das Vorzeichen für alle Habenbilanzkonten in dieser Zeile um. Wenn der Berichtsdesigner diese Konten konvertiert, entfernt er das Soll-/Habenmerkmal aus allen Beträgen und vereinfacht so das Addieren insgesamt. Um beispielsweise Nettoeinkommen zu berechnen, subtrahieren Sie die Ausgaben von den Einnahmen. In der Regel werden addierte und berechnete Zeilen nicht durch einen **C**-Code beeinflusst. Allerdings kehrt das **XCR**-Drucksteuerelement in der Spaltendefinition das Vorzeichen jeder Zeile mit einem **C** in der Spalte **Normaler Saldo** um. Diese Formatierung ist besonders wichtig, wenn Sie alle ungünstigen Abweichungen als negative Beträge anzeigen möchten. Wenn eine summierte oder berechnete Zahl das falsche Vorzeichen besitzt, geben Sie ein **C** in der Zelle **Normaler Saldo** für die Zeile ein, um das Vorzeichen umzukehren.

## <a name="specify-a-row-modifier-cell"></a>Angeben einer Zeilenmodifiziererzelle
Der Inhalt der Zelle **Zeilenmodifizierer** in einer Zeilendefinition setzt die Geschäftsjahre, Perioden und weitere Informationen, die in der Spaltendefinition für diese Zeile angegeben sind, außer Kraft. Der ausgewählte Modifizierer gilt für jedes Konto in der Zeile. Sie können jede Zeile ändern, indem Sie mindestens eine der folgenden Modifizierertypen verwenden:

-   Kontomodifizierer
-   Buchcodemodifizierer
-   Konto- und Transaktionsattribute

### <a name="override-a-column-definition"></a>Außerkraftsetzung einer Spaltendefinition

1.  Im Berichts-Designer öffnen Sie die zu ändernde Zeilendefinition.
2.  Doppelklicken in der Zeile, in der Sie die Spaltendefinition außer Kraft setzen möchten, auf die Zelle **Zeilenmodifizierer**.
3.  Wählen Sie im Dialogfeld **Zeilenmodifizierer** eine Option im Feld **Kontomodifizierer** aus. Eine Beschreibung der Optionen finden Sie im Abschnitt "Kontomodifizierer".
4.  Wählen Sie im Feld **Buchcodemodifizierer** den Buchcode aus, der für die Zeile verwendet werden soll.
5.  Gehen Sie unter **Attribute** folgendermaßen vor, um einen Eintrag für jedes Attribut hinzuzufügen, das im Zeilencode eingeschlossen sein soll:
    1.  Doppelklicken Sie auf die Zelle **Attribut**, und wählen Sie einen Attributnamen aus. **Achtung: **Ersetzen Sie das Nummernzeichen (\#) mit einem numerischen Wert.
    2.  Doppelklicken Sie auf die Zelle **Von**, und geben Sie den ersten Wert für den Bereich ein.
    3.  Doppelklicken Sie auf die Zelle **Bis**, und geben Sie den letzten Wert für den Bereich ein.

6.  Klicken Sie auf **OK**.

### <a name="account-modifiers"></a>Kontomodifizierer

Wenn Sie ein bestimmtes Konto auswählen, fasst der Berichtsdesigner normalerweise das Konto und die Geschäftsjahre, Perioden und weitere Informationen, die Sie in der Spaltendefinition angeben, zusammen. Sie können verschiedene Informationen, wie verschiedene Finanzzeiträume, für bestimmte Zeilen verwenden. In der folgenden Tabelle werden die verfügbaren Kontomodifizierer gezeigt. Ersetzen Sie das Nummernzeichen (\#) mit einem Wert, der gleich oder weniger ist, als die Anzahl der Perioden eines Geschäftsjahrs.

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

Sie können eine Zeile auf einen vorhandenen Buchcode einschränken. Die Spaltendefinition muss mindestens eine **FD**-Spalte enthalten, die einen Buchcode aufweist. **Hinweis:** Die Buchcodeeinschränkung für eine Zeile setzt die Buchcodeeinschränkungen in der Spaltendefinition für diese Zeile außer Kraft.

### <a name="account-and-transaction-attributes"></a>Konto- und Transaktionsattribute

Einige Buchführungssysteme unterstützen Kontoenattribute und Transaktionsattribute in den Finanzdaten. Diese Attribute arbeiten wie virtuelle Kontosegmente und können zusätzliche Informationen zum Konto oder zur Transaktion beinhalten. Diese zusätzlichen Informationen können Kontenkennungen, Charge-Kennungen, Postleitzahlen oder andere Attribute sein. Wenn Ihre Buchhaltungssystem Attribute unterstützt, können Sie Kontoattribute oder Transaktionsattribute als Zeilenmodifizierer in der Zeilendefinition verwenden. Informationen darüber, wie Zeileninformationen außer Kraft gesetzt werden finden Sie im Abschnitt "Außerkraftsetzung einer Spaltendefinition" weiter oben im Artikel.

## <a name="specify-a-link-to-financial-dimensions-cell"></a>Angeben eines Links zur Finanzdimensionszelle
Die Zelle **Mit Finanzdimensionen verknüpfen** enthält Verknüpfungen zu den Finanzdaten, die in jeder Zeile eines Berichts einbezogen werden sollen. Diese Zelle enthält Dimensionswerte, Sie können jedoch anstelle von oder zusätzlich zu Segmentwerten oder Dimensionswerten Zellen in einem Microsoft Excel-Arbeitsblatt angeben. Um das Dialogfeld **Dimensionen** zu öffnen, doppelklicken Sie auf die Zelle **Mit Finanzdimensionen verknüpfen**. **Hinweis:** Berichts-Designer kann Konten, Dimensionen oder Felder aus dem Microsoft Dynamics ERP-System nicht auswählen, die eines der folgenden reservierten Zeichen enthalten: &, \*, \[, \], {, oder }. Um Informationen für eine Zeile anzugeben, die bereits in der Zeilendefinition ist, fügen Sie die Informationen in der Zelle **Mit Finanzdimensionen verknüpfen** hinzu. Um neue Zeilen hinzuzufügen, die mit Finanzdaten verknüpfen, verwenden Sie das Dialogfeld **Zeilen einfügen aus**, um neue Zeilen in der Berichtsdefinition zu erstellen. Der Spaltentitel ändern sich, je nachdem, wie die Spalte konfiguriert wird; wie in der folgenden Tabelle dargestellt.

| Ausgewählter Verbindungstyp       | Die Beschreibung der Linkspalte ändert sich hierzu |
|----------------------------------|----------------------------------------------------|
| Finanzdimensionen             | Mit Finanzdimensionen verknüpfen                       |
| Externes Arbeitsblatt               | Mit Arbeitsblatt verknüpfen                                  |
| Finanzdimensionen + Arbeitsblatt | Mit Finanzdimensionen + Arbeitsblatt verknüpfen           |
| Management Reporter-Bericht       | Management Reporter-Bericht                         |

### <a name="specify-a-dimension-or-range"></a>Angeben einer Dimension oder eines Bereichs

1.  Im Berichts-Designer öffnen Sie die zu ändernde Zeilendefinition.
2.  Doppelklicken Sie auf eine Zelle in der Spalte **Mit Finanzdimensionen verknüpfen**.
3.  Doppelklicken Sie im Dialogfeld **Dimensionen** auf eine Zelle unter dem Dimensionsnamen.
4.  Wählen Sie im Dialogfeld für die Dimension **Einzelwert oder Bereich** aus.
5.  Geben Sie im Feld **Von** die erste Dimension ein, oder klicken Sie auf ![Durchsuchen](https://i-technet.sec.s-msft.com/dynimg/IC679490.gif "Durchsuchen"), um nach verfügbaren Dimensionen zu suchen. Um einen Bereich von Dimensionen eingeben, geben Sie die Enddimension im Feld **Bis** ein.
6.  Klicken Sie auf **OK**, um das Dialogfeld für die Dimension zu schließen. Im Dialogfeld **Dimensionen** wird die aktualisierte Dimension oder der Bereich angezeigt.
7.  Klicken Sie auf **OK**, um das Dialogfelds **Dimensionen** zu schließen.

## <a name="display-zero-balance-accounts-in-a-row-definition"></a>Anzeigen von Nullsaldokonten in einer Zeile
Standardmäßig druckt der Berichtsdesigner keine Zeile aus, die nicht ein entsprechendes Saldo in den Finanzdaten aufweist. Daher können Sie eine Zeilendefinition erstellen, die alle natürlichen Segmentwerte oder alle Dimensionswerte umfasst, und diese Zeilendefinition dann für alle Ihre Abteilungen verwenden.

### <a name="modify-zero-balance-settings"></a>Ändern der Nullsaldoeinstellungen

1.  Öffnen Sie die zu ändernde Zeilendefinition im Berichts-Designer.
2.  Wählen Sie auf der Registerkarte **Einstellungen** unter **Andere Formatierung** Optionen für die Zeilendefinition aus, die in der Berichtsdefinition verwendet wird.
3.  Klicken Sie im Menü **Datei** auf **Speichern**, um Ihre Änderungen zu speichern.

## <a name="use-wildcard-characters-and-ranges-in-a-row-definition"></a>Verwenden von Platzhalterzeichen und Bereichen in einer Zeilendefinition
Wenn Sie einen natürlichen Segmentwert im Dialogfeld **Dimensionen** eingeben, können Sie an jeder Position eines Segments ein Platzhalterzeichen (? oder \*) in jeder Position eines Segments einsetzen. Report Designer extrahiert alle Werte für die definierten Positionen, ohne die Platzhalterzeichen zu berücksichtigen. Zum Beispiel beinhaltet die Zeilendefinition nur natürliche Segmentwerte, und natürliche Segmente haben vier Zeichen. Durch Eingabe von **6???** in einer Zeilendefinition weisen des Berichts-Designers angezeigt, alle Konten einzuschließen, die einen natürlichen Segmentwert haben, die mit 6 beginnt. Wenn Sie **6\*** eingeben, sind die gleichen Ergebnisse zurückgegeben, doch die Ergebnisse auch Variable-Breitenwerte enthalten, z.B. **60** und **600000**. Der Berichtsdesigner ersetzt jedes Platzhalterzeichen (?) durch den kompletten Bereich möglicher Werte, die Buchstaben und Sonderzeichen enthalten. Zum Beispiel im Bereich von **12? 0** bis **12? 4** wird das Platzhalterzeichen **12? 0** durch den niedrigsten Wert im Zeichensatz ersetzt, und das Platzhalterzeichen in **12? 4** wird durch den höchsten Wert für im Zeichensatz ersetzt. **Hinweis:** Sie sollten Platzhalterzeichen für die Start- und Endkonten von Bereichen vermeiden. Wenn Sie Platzhalterzeichen entweder im Startkonto oder im Endkonto verwenden, erhalten Sie möglicherweise unerwartete Ergebnisse.

### <a name="single-segment-or-single-dimension-ranges"></a>Einzelsegment oder Bereiche mit einer Dimension

Sie können einen Bereich von Segmentwerten oder von Dimensionswerten angeben. Der Vorteil bei der Angabe eines Bereichs ist, dass Sie die Zeilendefinition nicht jedes Mal aktualisieren müssen, wenn ein neuer Segmentwert oder ein Dimensionswert den Finanzdaten hinzugefügt wird. Beispielsweise holt der Bereich **+Account=\[6100:6900\]** die Werte aus den Konten 6100 bis 6900 in den Zeilenbetrag. Wenn ein Bereich ein Platzhalterzeichen (?) umfasst, wertet der Berichtsdesigner den Bereich nicht auf einer Zeichen-pro-Zeichenbasis aus. Stattdessen werden die unteren und oberen Grenzen des Bereichs bestimmt, und dann werden die Endwerte und alle Werte dazwischen eingeschlossen. **Hinweis:** Berichts-Designer kann Konten, Dimensionen oder Felder aus dem Microsoft Dynamics ERP-System nicht auswählen, die eines der folgenden reservierten Zeichen enthalten: &, \*, \[, \], {, oder }. Sie können nur dann ein kaufmännisches Und-Zeichen (&) hinzufügen, wenn Sie Zeilendefinitionen automatisch mithilfe des Dialogfelds **Zeilen aus Dimensionen einfügen** erstellen.

### <a name="multiple-segment-or-multiple-dimension-ranges"></a>Bereiche mit mehreren Segmenten oder mehreren Dimensionen

Wenn Sie einen Bereich eingeben, indem Sie Kombinationen mehrerer Dimensionswerte verwenden, wird der Bereichsvergleich ..\financial-dimensions\dimension-by-dimension durchgeführt. Der Bereichsvergleich kann weder auf Basis von Zeichen-nach-Zeichen noch auf Teilesegmentbasis ausgeführt werden. Beispielsweise umfasst der Bereich **+Konto=\[5000:6000\], Abteilung=\[1000:2000\], Kostenstelle=\[00\]** nur die Konten, die mit jedem Segment übereinstimmen. In diesem Szenario müssen sich die erste Dimension im Bereich von 5000 bis 6000 befinden, muss die andere Dimension im Bereich von 1000 bis 2000 befinden, und die letzte Dimension muss 00 sein. Beispielsweise **+Konto=\[5100\], Abteilung=\[1100\], Kostencenter=\[01\]** ist nicht im Bericht enthalten, da das letzte Segment außerhalb des angegebenen Bereich befindet. Wenn ein Segmentwert Leerzeichen umfasst, schließen Sie diesen Wert in eckige Klammern ein (\[ \]). Folgende Werte sind für ein vier Zeichen langes Segment gültig: **\[ 234\], \[123 \], \[1 34\]**. Dimensionswerte sollen in eckige Klammern eingeschlossen werden (\[ \]), und der Berichtsdesigner fügt diese Klammern für Sie hinzu. Wann enthält ein Bereich mit mehreren Segmenten oder Dimensionen Platzhalterzeichen (? oder \*). Stattdessen werden die unteren und oberen Grenzen des Bereichs bestimmt, und dann werden die Endwerte und alle Werte dazwischen eingeschlossen. Bei einem großen Bereich, wie dem Gesamtbereich der Konten von 40000 bis 99999, sollten Sie ein gültiges Startkonto und Endkonto angeben, wann immer möglich. **Hinweis:** Berichts-Designer kann Konten, Dimensionen oder Felder aus dem Microsoft Dynamics ERP-System nicht auswählen, die eines der folgenden reservierten Zeichen enthalten: &, \*, \[, \], {, oder }. Sie können nur dann ein kaufmännisches Und-Zeichen (&) hinzufügen, wenn Sie Zeilendefinitionen automatisch mithilfe des Dialogfelds **Zeilen aus Dimensionen einfügen** erstellen.

## <a name="add-or-subtract-from-other-accounts-in-a-row-definition"></a>Addieren zu oder subtrahieren von anderen Konten in einer Zeile
Um die Geldbeträge in einem Konto zu den Geldbeträgen in einem anderen Konto zu addieren oder davon zu subtrahieren, können Sie das Pluszeichen (+) und das Minuszeichen (-) in der Zelle **Mit Finanzdimensionen verknüpfen** verwenden. In der folgenden Tabelle werden akzeptable Formate für das Addieren und subtrahieren von Links zu Finanzdaten aufgezeigt.

| Vorgang                                                                               | Verwenden Sie dieses Format                                                                                              |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Addieren Sie zwei vollständig qualifizierte Konten.                                                       | +Division= \[000\], Konto= \[1205\], Abteilung= \[00\] +Division= \[100\], Konto= \[1205\], Abteilung=\[00\] |
| Addieren Sie zwei Segmentwerte.                                                                 | +Konto= \[1205\] +Konto=\[1210\]                                                                           |
| Addieren Sie Segmentwerte, die Platzhalterzeichen enthalten.                                    | +Konto=\[120?+Konto=\[11??\]                                                                             |
| Addieren Sie einen Bereich von zwei vollständig qualifizierte Konten.                                                | +Division= \[000:100\]], Konto= \[[1205\]], Abteilung= \[00\]                                                   |
| Addieren Sie einen Bereich von Segmentwerten.                                                          | +Konto=\[1200:1205\]                                                                                       |
| Addieren Sie einen Bereich von Segmentwerten, die Platzhalterzeichen enthalten.                         | +Konto=\[120?:130?\]                                                                                       |
| Subtrahieren Sie ein vollqualifiziertes Konto von einem anderen vollqualifizierten Konto.              | +Division= \[000\], Konto= \[1205\], Abteilung= \[00\]-Division= \[100\], Konto= \[1205\], Abteilung=\[00\] |
| Subrahieren Sie einen Segmentwert von einem anderen Segmentwert.                                  | +Konto= \[1205\]-Konto=\[1210\]                                                                           |
| Subtrahieren Sie einen Segmentwert, der ein Platzhalterzeichen enthält, von einem anderen Segmentwert. | +Konto=\[1200\]?+Konto=\[11??\]                                                                           |
| Subtrahieren Sie einen Bereich zweier vollständig qualifizierter Konten.                                           | -Division=\[000:100\], Konto=\[1200:1205\], Abteilung=\[00:01\]                                           |
| Subtrahieren Sie einen Bereich von Segmentwerten.                                                     | -Konto=\[1200:1205\]                                                                                       |
| Subtrahieren Sie einen Bereich von Segmentwerten, die Platzhalterzeichen enthalten.                    | -Konto=\[120?:130?\]                                                                                       |

Zwar können Sie die Konten direkt ändern, Sie können aber auch das Dialogfeld **Dimensionen** verwenden, um die korrekte Formatierung auf Ihre Finanzdatenverknüpfungen anzuwenden. Jeder der Werte kann ein Platzhalterzeichen einschließen (? oder \*). Allerdings kann der Berichts-Designer Konten, Dimensionen oder Felder aus dem Microsoft Dynamics ERP-System nicht auswählen, die eines der folgenden reservierten Zeichen enthalten: &, \*, \[, \], {, oder }. **Hinweis:** Um Werte zu subtrahieren, müssen diese Werte in Klammern stehen. Wenn Sie beispielsweise **450? - (4509)** eingeben, wird dies als **+Konto=\[4509\]-Konto=\[450?\]** angezeigt, und Sie weisen den Berichtsdesigner an, den Betrag für das Kontosegment 4509 vom Betrag für jedes Kontosegment zu subtrahieren, das mit 450 beginnt.

### <a name="add-or-subtract-accounts-from-other-accounts"></a>Addieren oder subtrahieren von Konten aus anderen Konten

1.  Im Berichts-Designer öffnen Sie die zu ändernde Zeilendefinition.
2.  Doppelklicken Sie in der entsprechenden Zeile auf die Zelle in der Spalte **Mit Finanzdimensionen verknüpfen**.
3.  Führen Sie in der ersten Zeile des **Dimensionen**-Dialogfelds, folgende Schritte aus:
    1.  Wählen Sie im ersten Feld alle Dimensionen (Standard) aus, oder klicken Sie auf das Dialogfeld **Dimensionssätze verwalten**, in dem Sie einen Satz erstellen, ändern, kopieren oder löschen können.
    2.  Doppelklicken Sie auf die Zelle **Operator +/- **, und wählen Sie den Plus- (**+**) oder Minus- (**-**) Operator aus, der für einen oder mehrere Dimensionswerte oder -sätze in der Zeile gilt.
    3.  Doppelklicken Sie in der entsprechenden Dimensionswertspalte auf die Zelle, um das Dialogfeld **Dimensionen** zu öffnen, und wählen Sie aus, ob dieser Dimensionswert für einen Einzelwert oder einen Bereich, ein Dimensionswertsatz oder Summenkonten gilt. Beschreibungen der Felder im Dialogfeld **Dimensionen** finden Sie im Abschnitt "Beschreibung des Dialogfelds "Dimension".
    4.  Geben Sie Segmentwerte in der Spalte **Von** und **Bis** ein.

4.  Wiederholen Sie die Schritte 2 bis 3, um weitere Vorgänge hinzuzufügen.

**Hinweis:** Der Operator gilt für alle Dimensionen in der Zeile.

## <a name="description-of-the-dimensions-dialog-box"></a>Beschreibung des Dialogfelds "Dimensionen".
In der folgenden Tabelle werden die Felder im Dialogfeld **Dimensionen** beschrieben.

| Artikel                | Beschreibung                                                                                                                                                                                                                                                                                             |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Einzelwert oder Bereich | Geben Sie im Feld **Von** den Namen eines Kontos ein, oder klicken Sie auf die Schaltfläche **Durchsuchen** ![Durchsuchen](https://i-technet.sec.s-msft.com/dynimg/IC679490.gif "Durchsuchen"), um das Konto zu suchen. Um einen Bereich auswählen, geben Sie einen Wert in das Feld **Bis** ein, oder wählen Sie einen Wert aus.                                             |
| Dimensionswertsatz | Geben Sie im Feld **Name** den Namen eines Dimensionswertsatzes ein. Um einen Satz, zu erstellen, zu ändern, zu kopieren oder zu löschen, klicken Sie auf **Dimensionswertsätze verwalten**. Das **Formel**-Feld wird mit der Formel aus der Zelle **Mit Finanzdimensionen verknüpfen** für diesen Dimensionswertsatz aufgefüllt, der in der Zeilendefinition festgelegt ist. |
| Summenbildung für Konten   | Geben Sie im Feld **Name** eine Dimension der Summenkonten ein oder suchen Sie danach. Das **Formel**-Feld wird mit der Formel in der Zelle **Mit Finanzdimensionen verknüpfen** für diesen Summenkonto aufgefüllt, das in der Berichtsdefinition festgelegt ist.                                                                       |

## <a name="add-dimension-value-sets-in-a-row-definition"></a>Hinzufügen von Dimensionswertsätzen zu einer Zeilendefinition
Ein Dimensionswertsatz ist eine benannte Gruppe von Dimensionswerten. Ein Dimensionswertsatz kann nur Werte in einer einzelnen Dimension enthalten, aber Sie können einen Dimensionswertsatz in mehreren Zeilendefinitionen, Spaltendefinitionen, Berichtsbaumstruktur-Definitionen und Berichtsdefinitionen verwenden. Sie können Dimensionswertsätze auch in einer Berichtsdefinition kombinieren. Wenn eine Änderung an Ihren Finanzdaten die Änderung eines Dimensionswertsatzes erfordert, können Sie Definition des Dimensionswertsatzes aktualisieren und die Aktualisierung gilt für alle Bereiche, die den Dimensionswertsatz verwenden. Wenn Sie beispielsweise häufig einen Wertebereich angeben, der mit Ihren Finanzdaten verknüpft wird, wie die Werte von 5100 bis 5600, können Sie diesen Bereich einem Kontensatz namens "Vertrieb" zuweisen. Nach dem Erstellen eines Dimensionswertsatzes, können Sie diesen als Finanzdatenlink auswählen. Ein anderes Beispiel wenn dem Umsatz der Wertebereich von 5100 bis 5600 und 4175 zugewiesen wird, wird den Rabatten, kann bestimmt gesamten Verkauf zugeordnet, indem Rabatte aus Verkaufs- subtrahiert. Dieser Vorgang wird angegeben als **(5100:5600)-4175 **.

### <a name="create-a-set-of-dimension-values"></a>Erstellen eines Satzes von Dimensionswerten

1.  Öffnen Sie im Berichts-Designer die zu ändernde Zeilen-, Spalten- oder Baumstrukturdefinition.
2.  Klicken Sie im Menü **Bearbeiten** auf **Dimensionswertsätze verwalten**.
3.  Wählen Sie im Dialogfeld **Dimensionswertsätze verwalten** im Feld **Dimension** den Typ des Dimensionswertsatzes aus, der erstellt werden soll, und klicken Sie anschließend auf **Neu**.
4.  Geben Sie in Dialogfeld **Neu** einen Namen und eine Beschreibung für den Satz ein.
5.  Doppelklicken Sie in der Spalte **Von** auf eine Zelle.
6.  Wählen Sie im Dialogfeld **Konto** den Kontonamen in der Liste aus, oder suchen Sie nach den Eintrag im Feld **Suchen** Feld. Klicken Sie anschließend auf **OK**.
7.  Wiederholen Sie die Schritte 5 bis 6 in der Spalte **Bis**, um eine Formel für diesen Operator zu entwerfen.
8.  Wenn die Formel abgeschlossen ist, klicken Sie auf **OK**.
9.  Klicken Sie im Dialogfeld **Dimensionssätze verwalten** auf **Schließen**.

### <a name="update-a-set-of-dimension-values"></a>Aktualisieren eines Satzes von Dimensionswerten

1.  Öffnen Sie im Berichts-Designer die zu ändernde Zeilen-, Spalten- oder Baumstrukturdefinition.
2.  Klicken Sie im Menü **Bearbeiten** auf **Dimensionswertsätze verwalten**.
3.  Wählen Sie im Dialogfeld **Dimensionswertsätze verwalten** im Feld **Dimension** den Dimensionstyp aus.
4.  Wählen Sie in der Liste den Dimensionswertsatz aus, der aktualisiert werden soll, und klicken Sie anschließend auf **Ändern**.
5.  Ändern Sie im Dialogfeld **Ändern** die Formelwerte, die im Satz enthalten sein sollen. **Hinweis:** Wenn Sie neue Konten oder Dimensionen hinzufügen, stellen Sie sicher, dass Sie die vorhandenen Dimensionswertsätze ändern, damit die Änderungen berücksichtigt werden.
6.  Doppelklicken Sie auf die Zelle, und wählen Sie den entsprechenden Operator, das **Von**-Konto und das **Bis**-Konto aus.
7.  Klicken Sie auf **OK**, um das Dialogfeld **Ändern** zu schließen und die Änderungen zu speichern.

### <a name="copy-a-dimension-set"></a>Kopieren eines Dimensionssatzes

1.  Öffnen Sie im Berichts-Designer die zu ändernde Zeilen-, Spalten- oder Baumstrukturdefinition.
2.  Klicken Sie im Menü **Bearbeiten** auf **Dimensionswertsätze verwalten**.
3.  Wählen Sie im Dialogfeld **Dimensionswertsätze verwalten** im Feld **Dimension** den Dimensionstyp aus.
4.  Wählen Sie in der Liste den zu kopierenden Satz aus, und klicken Sie anschließend auf **Speichern unter**.
5.  Geben Sie einen Namen neuen für den kopierten Satz ein, und klicken Sie auf **OK**.

### <a name="delete-a-dimension-set"></a>Löschen eines Dimensionssatzes

1.  Öffnen Sie im Berichts-Designer die zu ändernde Zeilen-, Spalten- oder Baumstrukturdefinition.
2.  Klicken Sie im Menü **Bearbeiten** auf **Dimensionswertsätze verwalten**.
3.  Wählen Sie im Dialogfeld **Dimensionswertsätze verwalten** im Feld **Dimension** den Dimensionstyp aus.
4.  Wählen Sie die den löschenden Satz aus, und klicken Sie auf **Löschen**. Klicken Sie auf **Ja**, um den Dimensionswertsatz dauerhaft zu löschen.


<a name="see-also"></a>Siehe auch
--------

[Finanzberichterstellung für Microsoft Dynamics 365 for Operations](financial-reporting-intro.md)


