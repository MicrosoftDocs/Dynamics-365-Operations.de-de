---
title: Spaltendefinitionen in Finanzberichten
description: "Dieser Artikel enthält Informationen zu Spaltendefinitionen. Eine Spaltendefinition ist eine Berichtkomponente oder ein Baustein, die den Inhalt jeder Spalte eines Berichts angibt. Wie auch Zeilendefinitionen können grundlegende Spaltendefinitionen in mehreren Berichten verwendet werden."
author: RobinARH
manager: AnnBe
ms.date: 2016-08-09 21 - 27 - 36
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: Management Reporter, Core
ms.custom: 106601
ms.assetid: 66e72a48-edab-4e9d-815f-596a1623c258
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: af336db81f659d80248aa4ab1fbba96ed1ff48c2
ms.lasthandoff: 03/30/2017


---

# <a name="column-definitions-in-financial-reports"></a>Spaltendefinitionen in Finanzberichten

Dieser Artikel enthält Informationen zu Spaltendefinitionen. Eine Spaltendefinition ist eine Berichtkomponente oder ein Baustein, die den Inhalt jeder Spalte eines Berichts angibt. Wie auch Zeilendefinitionen können grundlegende Spaltendefinitionen in mehreren Berichten verwendet werden.

<a name="create-and-modify-a-column-definition"></a>Erstellen und Ändern einer Spaltendefinition
-------------------------------------

Eine Spaltendefinition kann zwei bis 255 Spalten enthalten.

### <a name="create-a-column-definition"></a>Erstellen einer Spaltendefinition

1.  Klicken Sie im Berichts-Designer im Navigationsbereich auf **Spaltendefinitionen** .
2.  Wählen Sie im Menü **Datei** die Option **Neu** aus, und klicken Sie dann auf **Spaltendefinitionen**.
3.  Hinzufügen von Inhalt zu der Spaltendefinition

### <a name="open-a-column-definition"></a>Öffnen einer Spaltendefinition

1.  Klicken Sie im Berichts-Designer im Navigationsbereich auf **Spaltendefinitionen** .
2.  Doppelklicken Sie auf eine Spaltendefinition, um sie zu öffnen.

### <a name="add-a-column-to-a-column-definition"></a>Hinzufügen eine Spalte zu einer Spaltendefinition

1.  Im Berichts-Designer klicken Sie auf die **Spaltendefinitionen** und öffnen dann die Spaltendefinition, um sie zu ändern.
2.  Wählen Sie die Spalte aus, in der eine neue Spalte eingefügt werden soll.
3.  Klicken Sie im Menü **Bearbeiten** auf **Spalte einfügen**. Die neue Spalte wird auf der linken Seite der Spalte, die Sie ausgewählt haben, angezeigt.

### <a name="delete-a-column-from-a-column-definition"></a>Löschen einer Spalte aus einer Spaltendefinition

1.  Im Berichts-Designer klicken Sie auf die **Spaltendefinitionen** und öffnen dann die Spaltendefinition, um sie zu ändern.
2.  Wählen Sie die zu löschende Spalte aus.
3.  Klicken Sie im Menü **Bearbeiten** auf **Spalte löschen**.

## <a name="contents-of-a-column-definition"></a>Inhalt einer Spaltendefinition
Eine Spaltendefinition umfasst die folgenden Informationen:

-   Eine Spalte der Beschreibungen für die Zeilendefinition
-   Betragsspalten, die Daten aus den Finanzdaten zeigen, ein Microsoft-Excel-Arbeitsblatt oder Berechnungen, die auf anderen Daten in der Spaltendefinition basieren
-   Formatierungsspalten
-   Attributspalten

Diese Informationen werden in den folgenden Bereichen in der Spaltendefinition angezeigt:

-   Der Kopfbereich der Spaltendefinition enthält den Überschrifttext und die Formatierung, die im Bericht angezeigt werden. Eine Überschrift kann für eine einzelne Datenspalte gelten, können mehrere Spalten umfassen kann oder auf bedingter Basis für Spalten gelten. Die Spaltendefinition kann beliebig viele Spaltenüberschriftszeilen enthalten, Sie benötigen. **Hinweis:** Spaltenkopfzeilen gelten für jede Datenspalte im Bericht. Berichtskopfzeilen gelten für den ganzen Bericht. Sie definieren Berichtskopfzeilen auf der Registerkarte **Kopf- und Fußzeilen** der Berichtsdefinition.
-   Spaltendetailzeilen sind die Zeilen unter den Kopfzeilen in der Spaltendefinition. Spaltendetailzeilen definieren die Informationen, die im Bericht enthalten ist. In der folgenden Tabelle werden die Spaltendetailzeilen angegeben und beschrieben.

    | Spaltendetailzeilenname                                                | Beschreibung                                                                                            |
    |-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
    | Spaltentyp                                                           | (Erforderlich) Geben Sie den Datentyp in der Spalte an.                                                     |
    | Buchcode/Attributkategorie                                          | Geben Sie Finanzdateninformationen für Spalten der Typen **FD** und **ATTR** an.                       |
    | Geschäftsjahresperiode-Perioden abgedeckt                                    | Geben Sie Finanzdateninformationen für Spalten des Typs **FD**.                                     |
    | Formel                                                               | Geben Sie eine Berechnungsformel für Spalten des Typs **CALC** an.                                        |
    | Spaltenbreite Zusätzliche Leerzeichen vor Spalte Formataußerkraftsetzung Drucksteuerung | Geben Sie spezielle Formatoptionen an.                                                                        |
    | Spalteneinschränkungen                                                   | Schränken Sie die Daten ein.                                                                                         |
    | Berichtseinheit                                                        | Beschränken Sie die Spalte, sodass sie nur Daten für die angegebene Berichtseinheit angezeigt werden.                      |
    | Währungsanzeige Währungsfilter                                      | Formatieren Sie die Währung.                                                                                       |
    | Dimensionsfilter                                                      | Geben Sie einen Filter an, um Daten auf bestimmte Finanzdatenberichtseinheiten zu beschränken.                           |
    | Attributfilter                                                      | Geben Sie einen Filter an, um die Finanzdaten einzuschränken.                                                       |
    | Startdatum Enddatum                                                   | Schränken Sie die Finanzdaten auf bestimmte Datumsangaben ein.                                                         |
    | Begründung                                                         | Richten Sie den Beschreibungstext, der in der Zeilendefinition angegeben ist, links, rechts oder mittig aus. |

## <a name="column-restrictions-in-a-column-definition"></a>Spalteneinschränkungszelle in einer Spaltendefinition
Sie können Spalteneinschränkungen verwenden, um festzulegen, wie eine Spaltendefinition Daten verwendet oder Informationen berechnet. Sie können eine Berichtsspalte auf eine bestimmten Einheit oder auf bestimmte Daten einschränken. **Hinweis:** Ein Code für **Spalteneinschränkung** setzt alle Konflikt verursachende Einstellungen außer Kraft, die der Zeilendefinition zugewiesen ist.

### <a name="column-restrictions-cell"></a>Spalteneinschränkungszelle

Die Zelle **Spalteneinschränkungen** kann Codes umfassen, die Informationen, wie Zeilenformatierung, Details und Beträge für diese Spalte, enthalten, beschränken oder unterdrücken.

#### <a name="add-a-column-restriction-in-a-column-definition"></a>Hinzufügen einer Spalteneinschränkung in eine Spaltendefinition

1.  Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2.  Doppelklicken Sie auf die Zelle **Spalteneinschränkungen** für die einzuschränkende Spalte.
3.  Wählen Sie im Dialogfeld **Spalteneinschränkungen** eine oder mehrere Codes aus der Liste aus, und klicken Sie anschließend auf **OK**.

### <a name="column-restriction-codes"></a>Spalteneinschränkungscodes

In der folgenden Tabelle werden die Spalteneinschränkungscodes beschrieben.

| Spalteneinschränkungscode | Beschreibung                                                                                                                                                                                                                                                                                                                             |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SU                      | Unterdrücken den Unterstrich für eine Spalte, in dem entweder ein Befehl zur Unterstreichung (**---) oder zur doppelten Unterstreichung (**===**===wird in die Zeilendefinition eingegeben. Beispielsweise sollten Sie keine Beträge unterstreichen, die von einer Prozentberechnung produziert werden.                                                                        |
| ST                      | Unterdrücken Sie Summen, sodass nur Details in der Spalte angezeigt werden, (beispielsweise eine statistische Spalte).                                                                                                                                                                                                                                      |
| SD                      | Unterdrücken Sie Details, sodass nur **TOT** und **CAL**-Zeilen (von der Zeilendefinition) in der Spalte angezeigt werden.                                                                                                                                                                                                                              |
| DR                      | Beschränken Sie die Beträge in einer **FD**-Spalte auf die Sollbeträge.                                                                                                                                                                                                                                                                              |
| CR                      | Beschränken Sie die Beträge in einer **FD**-Spalte auf die Habenbeträge.                                                                                                                                                                                                                                                                             |
| ADJ                     | Beschränken Sie die Beträge in der Spalte auf Periodenausgleichsbeträge, wenn diese Beträge verfügbar sind.                                                                                                                                                                                                                                        |
| XAD                     | Beschränken Sie die Beträge in der Spalte, sodass Periodenausgleichsbeträge ausgeschlossen werden.                                                                                                                                                                                                                                                     |
| GU                      | Beschränken Sie die Beträge in der Spalte, sodass nur gebuchte Transaktionen enthalten sind, wenn diese Transaktionen verfügbar sind.                                                                                                                                                                                                                 |
| UPT                     | Beschränken Sie die Beträge in der Spalte, sodass nur nicht gebuchte Transaktionen enthalten sind, wenn diese Transaktionen verfügbar sind. **Hinweis:** Nicht alle Daten unterstützen nicht gebuchte Transaktionen. Weitere Informationen finden Sie im [Datenintegrationshandbuch](http://go.microsoft.com/fwlink/?LinkID=162565) für Ihr Microsoft Dynamics ERP-System. |

### <a name="restrict-a-column-to-a-reporting-unit"></a>Beschränken einer Spalte auf eine bestimmte Berichtseinheit

1.  Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2.  Doppelklicken Sie auf die Zelle **Berichtseinheit** für die einzuschränkende Spalte.
3.  Wählen Sie im Dialogfeld **Auswahl der Berichtseinheit** in der Liste **Berichtsstruktur** eine Berichtserstellungsbaumstruktur aus.
4.  Erweitern oder reduzieren Sie die Liste der Einheiten, wählen Sie eine Berichtseinheit aus, und klicken Sie anschließend auf **OK**.

## <a name="format-column-headers"></a>Formatieren der Spaltenüberschrift
Sie können die Überschriften hinzufügen, ändern und löschen, die am oberen Rand der Spalten in einem Bericht angezeigt werden. Sie können bedingte umfassende Spaltenüberschriften basierend auf dem Feld **Periode** aus den Spaltendefinitionen und dem Feld **Basiszeitraum** aus den Berichtsdefinitionen konfigurieren. Die Basiszeitraumfunktion spart Zeit, wenn Sie Rollenplanungsberichte erstellen.

### <a name="create-and-manage-column-headers"></a>Erstellen und Verwalten von Spaltenüberschriften

Sie können das Dialogfeld **Spaltenüberschrift** verwenden, um Überschriften hinzuzufügen, zu ändern und zu löschen, die am oberen Rand der Spalten in einem Bericht angezeigt werden. In der folgenden Tabelle werden die Felder im Dialogfeld **Spaltenüberschriften** beschrieben.

| Feld                 | Beschreibung                                                                                                                                                                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spaltenüberschriftentext    | Dieser Text wird in der Spaltenüberschrift angezeigt. Sie können Text direkt in dieses Feld eingeben, oder auf **AutoText einfügen** klicken, um eine Option auszuwählen, die die Spaltenüberschrift jedes Mal aktualisiert, wenn der Bericht generiert wird. Um mehrere Autotextcodes einzubeziehen, klicken Sie erneut auf **AutoText einfügen**, und klicken Sie anschließend auf einen anderen Code in der Liste. |
| Formatoptionen        | Wenden Sie Formatierung auf eine Spaltenüberschrift an, beispielsweise als Kasten oder Unterstrich.                                                                                                                                                                                                                                                           |
| Verbreiten aus "Verbreiten zu" | Definieren Sie die Spalte oder die Spalten, für die der Überschrifttext gilt.                                                                                                                                                                                                                                                            |
| Begründung         | Geben Sie an, wie der Spaltenüberschrifttext für die Spalte oder den Bereich der Spalten ausgerichtet sein soll, die in den Feldern **Verbreiten von** und **Verbreiten zu** angegeben sind.                                                                                                                                                               |

### <a name="create-a-column-header"></a>Erstellen einer Spaltenüberschrift

1.  Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2.  Doppelklicken Sie auf eine Kopfzelle.
3.  Geben Sie im Dialogfeld **Spaltenüberschrift** den Text der Spaltenüberschrift ein. Klicken Sie alternativ auf **AutoText einfügen**, und wählen Sie eine Option aus.
4.  Wählen Sie im Feld **Formatoptionen** ein Format für die Überschrift aus.
5.  Geben Sie im Feld **Verbreiten von** den Buchstaben der Spalte ein, die über der die Spaltenüberschrift anfangen soll. Geben Sie im Feld **Verbreiten zu** den Buchstaben der Spalte ein, die über der die Spaltenüberschrift enden soll.
6.  Wählen Sie unter **Begründung** aus, ob der Text der Spaltenüberschrift links, rechts oder zentriert ausgerichtet sein soll.
7.  Klicken Sie auf **OK**.

### <a name="add-a-column-header-row"></a>Hinzufügen einer Spaltenüberschriftzeile

1.  Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2.  Wählen Sie eine Zelle in der Kopfzeile aus.
3.  Klicken Sie im Menü **Bearbeiten** auf **Zeile einfügen**. Die neue Zeile wird über der Zeile eingefügt, die Sie in Schritt 2 ausgewählt haben. **Hinweis: **Wenn Sie mehr als vier Zeilen für Kopfzeilen auf einem Bericht haben, überschneiden sich die Kopfzeilen, wenn der Bericht in ein Excel-Arbeitsblatt exportiert wird. Um alle Überschriften im Bericht anzuzeigen, vergrößern Sie den oberen Rand in der Berichtsdefinition.

### <a name="delete-a-column-header-row"></a>Löschen einer Spaltenüberschriftzeile

1.  Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2.  Wählen Sie in der Überschriftzeile die Zelle aus, die gelöscht werden soll.
3.  Klicken Sie im Menü **Bearbeiten** auf **Zeile löschen**.

### <a name="create-an-automatically-generated-header"></a>Erstellen einer automatisch generierten Überschrift

Der Bericht-Designer kann Spaltenüberschriften auf Grundlage von Autotextcodes automatisch generieren. Autotextcodes sind Variablen, die jedes Mal aktualisiert werden, wenn ein Bericht generiert wird. Jeder Spaltenüberschrift kann diese Codes umfassen, um Berichtsinformationen anzugeben, die variieren können, wie Datumswerte oder Periodenzahlen. Daher können Sie eine Spaltendefinition für mehrere Berichtsdefinitionen, Zeiträume und Berichtsbaumstrukturen verwenden. Da Autotextcodes auf den Kalenderdaten aus den Detailzeilen der Spaltendefinition beruhen, werden sie nur für **CALC** und **FD** und **WKS**-Spalten unterstützt. Die Methode, auf die ein Autotextcode in der Spaltenüberschriftzelle angezeigt wird, beeinflusst, wie diese Informationen im Bericht angezeigt werden. Im Dialogfeld **Spaltenüberschrift** werden die Autotextcodes in Groß- und Kleinbuchstaben angezeigt. Daher wird der Text im Bericht in Groß- und Kleinbuchstaben angezeigt. Beispielsweise wird in einem Standardkalenderjahr, **@CalMonthLongBeschlussmonat ** 7 ** zu ** Juli **. Wenn der Name des Monats aktiviert ist (z ** JULI **), geben Sie den AutoText-Code den in Großbuchstaben im ** Spaltenüberschriftstext ** Feld ein. Geben Sie z ** **@CALMONTHLONGein. Sie können Codes und Text kombinieren. Geben Sie z den folgenden Überschriftstext ein: ** Periode @FiscalPeriod-@FiscalYear mit @StartDate zu @EndDate**. Die Berichtsüberschrift, die generiert wird, ähnelt dem folgenden Text: **Periode 1-02 von 01/01/02 bis 01/31/02**. ** Hinweis: ** Das Format von Einige der im Text, wie den langen Datum, hängt von den regionalen Einstellungen auf dem für Arbeitsgangsserver Dynamics 365 ab. Um diese Einstellungen zu ändern, klicken Sie auf die Schaltfläche **Start**, klicken Sie auf **Systemsteuerung**, und klicken Sie anschließend auf **Region und Sprache**. In der folgenden Tabelle werden die verfügbaren Autotext-Optionen für Spaltenüberschriften aufgeführt.

| Autotext-Option und -Code                | Beschreibung                                                                                                                                                                                                                                                                                      |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Monatsname (@CalMonthLong)              | Druckt den Namen des aktuellen Monats in der Spaltenüberschrift. Wenn Sie sich entscheiden, die Beträge im Bericht auf Tausend, Millionen oder Milliarden zu runden, oder wenn Sie die Spaltenbreite im Bericht auf weniger als neun Zeichen festlegen, wird der Name des Monats auf die ersten drei Zeichen gekürzt. |
| Abgekürzter Monatsname (@CalMonthShort) | Druckt den abgekürzte Monatsnamen für den ausgewählten Finanzzeitraum.                                                                                                                                                                                                                          |
| Zeitraumnummer (@FiscalPeriod           | Druckt das numerische Formular des Finanzzeitraums, der für diese Spalte gekennzeichnet ist, aus. Wenn die Spalte mehrere Perioden umfasst, wird die letzte Periode im Bereich gedruckt.                                                                                                                                   |
| Zeitraumbeschreibung (@FiscalPeriodName  | Druckt die Finanzzeitraumbeschreibung, die in den Finanzdaten identifiziert wird, aus.                                                                                                                                                                                                                    |
| Geschäftsjahr (@FiscalYear)               | Druckt das Geschäftsjahr für die Spalte in der numerischen Formular aus.                                                                                                                                                                                                                                            |
| Kalenderjahr (@CalYear)                | Druckt das Kalenderjahr für die Spalte in der numerischen Formular aus.                                                                                                                                                                                                                                          |
| Startdatum (@StartDate)                 | Druckt das Startdatum für die Spalte aus.                                                                                                                                                                                                                                                             |
| Enddatum (@EndDate)                     | Druckt das Enddatum für die Spalte aus.                                                                                                                                                                                                                                                               |
| Einheitsname aus Struktur (@UnitName         | Wenn Sie eine Spalte auf eine bestimmten Einheit der Berichtsbaumstruktur einschränken, drucken Sie den Einheitsnamen in der Spaltenüberschrift aus.                                                                                                                                                                                     |
| Einheitenbeschreibung (@UnitDesc            | Wenn Sie eine Spalte auf eine bestimmten Einheit der Berichtsbaumstruktur einschränken, drucken Sie die Einheitsbeschreibung in der Spaltenüberschrift aus.                                                                                                                                                                              |
| Buchcode (@BookCode)                   | Druckt den Buchcode, der in der Spalte angegeben wird, aus.                                                                                                                                                                                                                                             |
| Leerzeile (@Blank)                     | Fügt eine Leerzeile in der Spaltenüberschrift ein.                                                                                                                                                                                                                                                       |

### <a name="create-a-conditional-spanning-header"></a>Erstellen einer bedingten verbreiteten Überschrift

Bedingte verbreitete Überschriften können mehrere Spalten umfassen, die auf bestimmten Periodendaten basieren. Wenn Sie beispielsweise einen Budgetbericht für das Geschäftsjahr haben und die Ist-Budgets der letzten Monate zusammen mit den Projektbudgets künftiger Monate anzeigen möchten, können Sie eine bedingte verbreitete Überschrift verwenden, um die Berichtsüberschrift automatisch zu aktualisieren. Berücksichtigen Sie die folgenden Situationen, wenn Sie eine bedingte verbreitete Überschrift erstellen:

-   Jedes Beendigungsbedingung (**Verbreiten zu**-Feld), die vor einer Startbedingung (**Verbreiten von**-Feld) entsprochen wird, wird ignoriert. So ist für Spalte B beispielsweise die Verbreitungsbedingung als BASIS+1 zu BASIS definiert, ist BASIS in der Spalte C und BASE+1 in die Spalte D. In diesem Fall wird die Beendigungsbedingung in der Spalte C ignoriert und die Überschrift wird ab Spalte D gedruckt.
-   Wenn Sie Spaltenüberschriften angeben, die überlappen, überschneiden sie sich, wenn sie im Bericht gedruckt werden. Der Bericht wird generiert, jedoch die folgende Warnung wird im ** Berichtswarteschlangenstatus ** Feld: "Spaltenüberschriften mit BASE überschneiden sich mit anderen Spaltenüberschriften und können eine Überlappung des Texts zur Folge haben." Beispielsweise ist die Kopfzeilendefinition für Spalte B "B bis BASE+1, und die Kopfzeilendefinition für Spalte D "zu F. in diesem Fall, werden die Kopfzeilen auf miteinander gedruckt und sind nicht lesbar. Sobald BASIS in einer Definition **Verbreiten aus/Verbreiten bis** verwendet wird, stellen Sie sicher, den Bericht anzuzeigen, der generiert wird, um festzustellen, ob die Überschriften sich überschneiden.
-   Wenn Sie in der Verbreitungsdefinition in einer nicht gedruckten Spalte(**NP**) BASIS angeben, wird diese ignoriert, unabhängig davon, was in der Spaltendefinition definiert ist. Im Wesentlichen entspricht dieses Szenario einer Situation, in der keine Spaltenüberschriftdefinition erstellt wird.
-   In Spalten mit bedingtem Druck (PB ****&lt;, P=B ** **&gt;, ) verhalten sich Kopfzeilen für bedingte Aufteilung wie normale wie die einzelnen Spaltenüberschriftdefinition. Wenn beispielsweise die Bedingung falsch ist, beginnt jede nachfolgende Spalte, die mit der Verbreitungsbedingung übereinstimmt, das Drucken der Überschriften.

#### <a name="create-a-conditional-spanning-header"></a>Erstellen einer bedingten verbreiteten Überschrift

1.  Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2.  Doppelklicken Sie auf eine Kopfzelle.
3.  Geben Sie im Dialogfeld **Spaltenüberschrift** den Text der Spaltenüberschrift ein. Klicken Sie alternativ auf **AutoText einfügen**, und wählen Sie eine Option aus.
4.   Wählen Sie im Feld **Formatoptionen** ein Formatierungstil für die Überschrift aus.
5.  Geben Sie einen Zeitraum im Verhältnis zum Basiszeitraum an, der angegeben wird, wenn der Bericht generiert wird. Geben Sie in den Feldern **Verbreiten von** und **Verbreiten bis** einen der folgenden Werte ein: **BASIS**, **BASIS-X** oder **BASIS+X**, wobei X die Anzahl von Perioden des Basiszeitraums ist. Wenn Sie beispielsweise **BASIS** im Feld **Verbreiten von** eingeben, beginnt der bedingte verbreitete Spaltenüberschrifttext in der Spaltenüberschrift, in der der Wert des **Basiszeitraums** der Berichtsdefinition dem **Perioden**-Wert der Spaltendefinition entspricht. Er endet in der Spalte, die im **Verbreiten bis**-Feld angegeben ist. Wenn die Verbreitung z. B. BASIS bis M ist, und der Wert des **Basiszeitraums** der Berichtsdefinition **4** ist, beginnt die Überschrift in der Spalte, in der die Periode auf **4** festgelgt ist, und stoppt bei Spalte M. Überschriften beginnen und enden nur bei Druckspalten.
6.  Wählen Sie unter **Begründung** aus, ob der Text der Spaltenüberschrift links, rechts oder zentriert ausgerichtet sein soll.
7.  Klicken Sie auf **OK**.

#### <a name="example-of-a-conditional-spanning-header"></a>Beispiel einer bedingten verbreiteten Überschrift

Phyllis erstellt einen Bericht für eine dynamische Sechsmonatsprognose. Sie möchte das Wort "Istwert" über allen Spalten, die Ist-Daten enthalten, und das Wort "Budget" über den Spalten drucken, die Budgetplanungen enthalten. Für jeden Monat, in dem der Bericht ausgeführt wird, gibt es eine weitere Ist-Spalte und eine Budgetspalte weniger. Obwohl Phyllis die Spaltendefinition jedes Mal manuell ändern kann, wenn der Bericht generiert wird, um die Überschriften anzupassen, entscheidet sie sich, um Zeit und Mühe zu sparen, bedingte verbreitete Überschriften zu erstellen, die automatisch Überschriften über den entsprechenden Spalten erstellen, wenn der Bericht ausgeführt wird. Phyllis öffnet den Berichts-Designer, klickt im Navigationsbereich auf **Spaltendefinition** und öffnet die Spaltendefinition für den Bericht. Dann gibt sie die folgenden Informationen ein: Der Basiszeitraum in der Berichtsdefinition ist 4.

|                     | A:    | Mrd             | C:             | S             | E:             | Fr             | G:             | H:             | I             | J             | K             | L             | Mo             |
|---------------------|------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|
| Kopfzeile 1            |      | Tatsächlich        | Budget        |               |               |               |               |               |               |               |               |               |               |
| Kopfzeile 2            |      | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong |
| Kopfzeile 3            |      |               |               |               |               |               |               |               |               |               |               |               |               |
| Spaltentyp         | DESC | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            |
| Buchcode/Attribute |      | ISTWERT        | BUDGET2012    | ISTWERT        | BUDGET2012    | ISTWERT        | BUDGET2012    | ISTWERT        | BUDGET2012    | ISTWERT        | BUDGET2012    | ISTWERT        | BUDGET2012    |
| Geschäftsjahr         |      | BASIS          | BASIS          | BASIS          | BASIS          | BASIS          | BASIS          | BASIS          | BASIS          | BASIS          | BASIS          | BASIS          | BASIS          |
| Zeitraum              |      | 1             | 1             | 2             | 2             | 3             | 3             | 4             | 4             | 5             | 5             | 6             | 6             |
| Abgedeckte Perioden     |      | PERIODISCH      | PERIODISCH      | PERIODISCH      | PERIODISCH      | PERIODISCH      | PERIODISCH      | PERIODISCH      | PERIODISCH      | PERIODISCH      | PERIODISCH      | PERIODISCH      | PERIODISCH      |
| Spaltenbreite        | 30   | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            |
| Drucksteuerung       |      | P=B &lt;       | PB &gt;        | P=B &lt;       | PB &gt;        | P=B &lt;       | PB &gt;        | P=B &lt;       | PB &gt;        | P=B &lt;       | PB &gt;        | P=B &lt;       | PB &gt;        |

Phyllis doppelklickt auf eine Spaltenüberschriftzelle, um das Dialogfeld **Spaltenüberschrift** zu öffnen, in dem sie die folgenden Informationen eingibt.

| Feld              | Wert                 |
|--------------------|-----------------------|
| Spaltenüberschriftentext | Istwert                |
| AutoText einfügen    | Keine Auswahl vorgenommen. |
| Formatoptionen     | Feld                   |
| Begründung      | Keine Auswahl vorgenommen. |
| Verbreiten von        | Mrd                     |
| Verbreiten bis          | BASIS                  |
| Budgetkopfzeile      | BASE+1 zur Endspalte  |

Nachdem sie die Informationen eingeben hat, klickt Phyllis auf **OK**. Dann doppelklickt sie auf die Spaltenüberschriftzelle in Spalte C, um das Dialogfeld **Spaltenüberschrift** zu öffnen, in dem sie die folgenden Informationen eingibt.

| Feld              | Wert                 |
|--------------------|-----------------------|
| Spaltenüberschriftentext | Budget                |
| AutoText einfügen    | Keine Auswahl vorgenommen. |
| Formatoptionen     | Feld                   |
| Begründung      | Keine Auswahl vorgenommen. |
| Verbreiten von        | C:                     |
| Verbreiten bis          | BASE+2                |

Jedes Mal, wenn der Bericht generiert wird, wird das Wort "Istwert" über allen Spalten, die Ist-Daten enthalten, und das Wort "Budget" über den Spalten gedruckten, die Budgetplanungen enthalten. Darüber hinaus wird die Anzahl der Spalten jeden Monat reguliert.

## <a name="apply-column-justification"></a>Anwenden von Spaltenbegründung
Die Zelle **Begründung** wird verwendet, um die Begründungsformatierung in einem Bericht auf eine Berichtspalte anzuwenden. Diese Option wirkt sich nur auf die Spaltenbeschreibungen, nicht auf die Istwerte, aus.

1.  Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2.  Doppelklicken Sie auf die Zelle **Begründung**.
3.  Wählen Sie einen der folgenden Werte aus der Liste aus:
    -   **Keine** - Keine Begründung wird verwendet.
    -   **Links** - Richten Sie die Spaltenbeschreibungen links aus.
    -   **Mitte** - Zentrieren Sie die Spaltenbeschreibungen.
    -   **Rechts** - Richten Sie die Spaltenbeschreibungen rechts aus.

## <a name="add-special-formatting-options"></a>Hinzufügen von speziellen Formatierungsoptionen
In der Spaltendefinition wenden die Formatierungsspalte und Detailzeilen spezielle Formatierung auf ausgewählte Spalten an. Obwohl einige der Optionen für **Drucksteuerelemente** und **Spalteneinschränkungen** für **FD**-Spalten spezifisch sind, gelten die meisten Optionen für alle Spaltentypen. Die Formatierung, die in der Spaltendefinition angegeben wird, setzt die Formatierung außer Kraft, die in der Berichtsdefinition angegeben ist. Allerdings setzt die Formatierung, die in der Zeilendefinition angegeben wird, die Formatierung außer Kraft, die in der Spaltendefinition angegeben ist. Die folgenden Zeilen gelten als Formatierungszeilen:

-   Spaltenbreite
-   Zusätzliche Leerstellen vor Spalte
-   Format/Währungsaußerkraftsetzung
-   Drucksteuerung

### <a name="changing-the-column-width"></a>Ändern der Spaltenbreite

Die Zelle **Spaltenbreite** gibt die Anzahl der Zeichen an, die für die Breite dieser Spalte im gedruckten Bericht verwendet werden. Spaltenbreite ist für Spalten wichtig, die Beträge (Spalten des Typs **CALC** **WKS** oder **FD** ), Beschreibungen (Spalten des Typs **DESC** ) oder Füllung (Spalten des **AUSFÜLLEN**-Typs) enthalten. Standardmäßig wird die Option **Automatisch anpassen** ausgewählt, damit die Breite jeder Spalte automatisch an den Inhalt angepasst wird.

#### <a name="specify-the-width-of-a-column-on-a-report"></a>Angeben der Breite einer Spalte in einem Bericht

1.  Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2.  Geben Sie in Zelle **Spaltenbreite** die Anzahl der Stellen für die Spaltenbreite ein. Die maximale Breite einer beliebigen Spalte ist 255 Zeichen (diese Anzahl umfasst Cent, Kommas und Klammern). Wenn Sie alternativ den Bericht-Designer so aktivieren möchten, dass die richtige Breite für die Spalte basierend auf dem Zelleninhalt auswählt wird, klicken Sie doppelt auf die Zelle **Spaltenbreite** und dann auf **Automatisch anpassen**.

### <a name="add-space-between-columns"></a>Hinzufügen von Leerstellen zwischen Spalten

Die Zelle **Zusätzliche Leerzeichen vor Spalte** gibt die Breite des Trennzeichens zwischen einer Spalte und benachbarten Spalten in der Spaltendefinition an. Die **Zusätzliche Leerzeichen vor Spalte**-Einstellung bezieht sich alle Spaltendetailzeilen für die Spalte, nicht aber die Spaltenüberschriftzeilen. Verwenden Sie diese Option, um Spaltengruppen abzugrenzen oder einige Leerzeichen vor der Beschreibung hinzuzufügen, damit die Beschreibungsspalte von den linksbündigen Titeln im Bericht eingezogen wird. Die Standardanzahl von Stellen zwischen jeder Spalte ist zwei. Sie können diese Einstellung auf der Registerkarte **Einstellungen** in der Berichtsdefinition ändern.

#### <a name="specify-the-space-between-columns"></a>Angeben des Abstands zwischen Spalten

1.  Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2.  Geben Sie in Zelle **Zusätzliche Leerzeichen vor Spalte** die Anzahl der Stellen an, die zwischen Spalten eingefügt werden soll.

### <a name="specify-a-currency"></a>Angeben einer Währung

Die Zelle **Format/Währungsaußerkraftsetzung** gibt die Formatierung der Dezimalstelle, der Währung und der Prozentsatzbeträge in der Spalte an. Diese Formatierung setzt alle Formatierungen außer Kraft, die in der Spaltendefinition oder den Systemstandardeinstellungen angegeben sind.

#### <a name="assign-a-format-currency-override-to-a-report-column"></a>Zuweisen einer Währungsaußerkraftsetzung zu einer Berichtsspalte

1.  Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2.  Doppelklicken Sie auf eine **Format/Währungsaußerkraftsetzung**-Zelle in einer Betragsspalte.
3.  Wählen Sie im Dialogfeld **Formataußerkraftsetzung** Formatierungsoptionen aus.

### <a name="add-a-print-control-code"></a>Hinzufügen einer Drucksteuerung

Die Zelle **Drucksteuerung** kann Codes enthalten, die die Anzeige oder die Druckmerkmale einer Spalte anpassen. Es gibt zwei Typen von Drucksteuerungscodes: reguläre Drucksteuerungscodes und bedingte Drucksteuerungscodes.

#### <a name="regular-print-control-codes"></a>Reguläre Drucksteuerungscodes

| Drucksteuerungscodes | Übersetzung                                     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NP                 | Nicht druckbar                                     | Schließen Sie die Beträge in dieser Spalte aus dem Bericht, der gedruckt wird, und von Berechnungen aus. Um eine nicht druckbare Spalte in eine Berechnung einzubeziehen, verweisen Sie die Spalte in der Berechnungsformel direkt. Beispielsweise ist die nicht druckbare Spalte C in der folgenden Berechnung enthalten: **B+C+D**. Allerdings ist die nicht druckbare Spalte C nicht in der folgenden Berechnung enthalten: **B:D**.                                                                                                                                          |
| XCR                | Ändern der Vorzeichen, wenn der typische Saldo der Zeile Haben ist | Erstellen Sie einen Budget- oder vergleichbaren Bericht, in dem jede ungünstige Abweichung (wie ein Umsatzerlösdefizit oder eine Ausgabenüberschreitung) immer negativ ist. Wenden Sie diesen Code auf einer **CALC**-Spalte an, um das Vorzeichen des Spaltenbetrags umzukehren, wenn der typische Saldo einer gegebenen Zeile ein Habenposten ist (wie von einem **C** in der Spalte **Normaler Saldo** der Zeilendefinition gekennzeichnet). **Hinweis:** Achten Sie bei **TOT**-Zeilen und **CAL**-Zeilen, die üblicherweise ein Habensaldo enthalten, darauf, ein **C** in der Spalte **Normaler Saldo** in der Zeilendefinition einzugeben. |
| X0                 | Unterdrücken einer Spalte, wenn alle null oder Leerzeichen sind          | Schließen Sie eine **FD**-Spalte aus dem Bericht aus, wenn alle Zellen in dieser Spalte entweder leer sind oder Nullen enthalten.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| SR                 | Runden unterdrücken                               | Verhindert, dass die Beträge in dieser Spalte gerundet werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| XR                 | Rollup unterdrücken                                 | Unterdrücken Sie einen Rollup. Wenn der Bericht eine Berichtsbaumstruktur verwendet, werden die Beträge in dieser Spalte nicht in folgende übergeordnete Knoten übertragen.                                                                                                                                                                                                                                                                                                                                                                                                   |
| RP                 | Wiederholen der Spalte auf jeder Seite                      | Wiederholen Sie eine angegebene Spalte auf jeder Seite eines Berichts. So können beispielsweise den Drucksteuerungscode **RP** verwenden, um eine Spalte vom Typ **ZEILE** einzubeziehen, der auf jeder Seite Zeilencodes bezieht.                                                                                                                                                                                                                                                                                                                                           |
| WT                 |  Textumbruch                                      |  Wenn der Text in einer Spalte zu lang ist, brechen Sie den Text um, um den gesamten Text in der Spalte behalten.                                                                                                                                                                                                                                                                                                                                                                                                                            |

#### <a name="conditional-print-control-codes"></a>Bedingte Drucksteuerungscodes

| Bedingter Drucksteuerungscode | Beschreibung                                                                             |
|--------------------------------|-----------------------------------------------------------------------------------------|
| (keine)                         | Löschen Sie die bedingte Druckauswahl.                                                  |
| PB &lt;                         | Zeigen Sie eine angegebene Spalte nur an, wenn die Periode geringer als der Basiszeitraum ist.             |
| PB &gt;                         | Zeigen Sie eine angegebene Spalte nur an, wenn die Periode länger als der Basiszeitraum ist.             |
| P=B                            | Zeigen Sie eine angegebene Spalte nur an, wenn die Periode gleich dem Basiszeitraum ist.              |
| P=B &lt;                        | Zeigen Sie eine angegebene Spalte nur an, wenn die Periode geringer als oder gleich dem Basiszeitraum ist. |
| P=B &gt;                        | Zeigen Sie eine angegebene Spalte nur an, wenn die Periode länger oder gleich dem Basiszeitraum ist. |

#### <a name="add-print-control-codes-to-a-report-column"></a>So fügen Sie Drucksteuerungscodes einer Spaltenzeile hinzu

1.  Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2.  Doppelklicken Sie auf die Zelle **Drucksteuerung**.
3.  Wählen Sie im Dialogfeld **Drucksteuerung** einen Code aus der Liste **Drucksteuerungsoptionen auswählen** aus. Um mehr als einen Code auszuwählen, halten Sie die STRG-Taste gedrückt, während Sie die Codes auswählen.
4.  Wählen Sie im Feld **Bedingte Druckoptionen** eine Option aus. Standardmäßig ist **(keine)** aktiviert. Sie können nur jeweils einen bedingten Druckcode auswählen.
5.  Klicken Sie auf **OK**.

**Tipp:** Sie können die Druckcodes direkt in die Zelle **Drucksteuerung** eingeben. Trennen Sie mehrere Drucksteuerungscodes mit einem Komma voneinander.

### 

## <a name="column-types"></a>Spaltentypen
Der Typ der Informationen, die jede Spalte in einem Bericht umfasst, wird vom Wert in der Zeile **Spaltentyp** in der Spaltendefinition angegeben. Jede Spaltendefinition muss mindestens eine Beschreibungspalte (**DESC**) und eine Betragsspalte (**FD**, **WKS** oder **CALC**) enthalten. **Hinweis:** Die Spaltencodes gelten nicht für alle Buchhaltungssysteme. Wenn Sie einen Typ auswählen, der für Ihr Buchhaltungssystem nicht gültig ist, ist diese Spalte im Bericht leer.

### <a name="specify-a-column-type"></a>Angeben eines Spaltentyps

1.  Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2.  Doppelklicken Sie in der entsprechenden Spalte auf eine Zelle in der Zeile **Spaltentyp**.
3.  Wählen Sie in der Liste einen Spaltentyp aus. In der folgenden Tabelle werden die verschiedenen Spaltentypen beschrieben.
    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Spaltentypcode</th>
    <th>Beschreibung</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>FD</td>
    <td>Hier können Sie Finanzdaten oder Daten aus einem Excel-Arbeitsblatt anzeigen, wenn Sie eine <strong>Mit Finanzdimensionen verknüpfen</strong>-Spalte oder eine <strong>Mit Arbeitsblatt verknüpfen</strong>-Spalte in der Zeilendefinition verwenden. Wenn Sie den Spaltentyp <strong>FD</strong> auswählen, werden Standardeinstellungen automatisch für die folgenden Zeilen angegeben:
    <ul>
    <li><strong>Buchcode/Attributkategorie:</strong> ISTWERT</li>
    <li><strong>Buchcode/Attributkategorie:</strong> ISTWERT</li>
    <li><strong>Geschäftsjahr</strong> BASIS</li>
    <li><strong>Periode:</strong> BASIS</li>
    <li><strong>Abgedeckte Perioden:</strong> PERIODISCH</li>
    <li><strong>Spaltenbreite:</strong> 14</li>
    </ul>
    Diese Standardeinstellungen können geändert werden.</td>
    </tr>
    <tr class="even">
    <td>KALK</td>
    <td>Hier wird das Ergebnis einer einfachen oder komplexen Berechnung angezeigt, die in der Zelle <strong>Formel</strong> angegeben ist. Weitere Informationen finden Sie unter <a href="advanced-formatting-options-financial-reporting.md">Erweiterte Formatierungsoptionen in Finanzberichten</a>.</td>
    </tr>
    <tr class="odd">
    <td>DESC</td>
    <td>Zeigen Sie die Zeilenbeschreibung der Zeilendefinition an. Obwohl die Beschreibungsspalte häufig die erste Spalte im Bericht ist, kann sie an jeder beliebigen Position sein.</td>
    </tr>
    <tr class="even">
    <td>ZEILE</td>
    <td>Hier werden einzelne Zeilencodes für Finanzzeilen aus der Spalte <strong>Zeilencode</strong> in der Zeilendefinition angezeigt. Weitere Informationen finden Sie unter <a href="row-definitions-financial-reporting.md">Zeilendefinitionen in Finanzberichten</a>.</td>
    </tr>
    <tr class="odd">
    <td>ACCT (Kontocodes)</td>
    <td>Hier werden die Finanzdatensegmentwerte oder Dimensionswerte angezeigt, die für jede Zeile gelten. Für Konto- und Transaktionsdetailberichte wird das vollqualifizierte Konto ausgedruckt (z. B. <strong>110140-070-0101</strong>). Wenn Bereiche in der Spalte <strong>Mit Finanzdimensionen verknüpfen</strong> in einer zugeordneten Zeilendefinition angegeben wurden, wird der Bereich in den eckigen Klammern einbezogen und als Einzelwert behandelt (z. B. <strong>[110140:110700] - 070- [0101:0200]</strong>). Für Finanzberichte und allgemeine Berichte, die eine Kombination mehrerer Konten sind, wird die Finanzdatenverknüpfung von der Zeilendefinition ausgedruckt (beispielsweise <strong>1100:1200</strong>).</td>
    </tr>
    <tr class="even">
    <td>FILL</td>
    <td>Füllen Sie die Zelle mit einem Zeichen aus, das Sie in einfache Anführungszeichen einschließen. Wenn Sie kein Zeichen eingeben, ist die Spalte leer. Um beispielsweise eine Spalte mit Auslassungspunkten (...) auszufüllen, geben Sie <strong>AUSFÜLLEN</strong> <strong>'.'</strong> ein.</td>
    </tr>
    <tr class="odd">
    <td>SEITE</td>
    <td>Fügen Sie einen vertikalen Seitenumbruch in den Bericht ein. Die Spalten rechts neben der Spalte <strong>SEITE</strong> werden auf einer anderen Seite angezeigt.</td>
    </tr>
    <tr class="even">
    <td>WKS</td>
    <td>Zeigen Sie die Daten an, die aus einem Excel-Arbeitsblatt abgerufen wurden. Wenn Sie den Spaltentyp <strong>WKS</strong> auswählen, werden Standardeinstellungen automatisch für die folgenden Zeilen angegeben:
    <ul>
    <li><strong>Geschäftsjahr:</strong> PERIODISCH</li>
    <li><strong>Periode:</strong> BASIS</li>
    </ul>
    Diese Standardeinstellungen können geändert werden.</td>
    </tr>
    <tr class="odd">
    <td>ATTR</td>
    <td>Wenn Ihr Buchhaltungssystem Attribute unterstützt, zeigen Sie ein Konto oder ein Transaktionsattribut in der Spalte an. Ein Attribut, das für einen einzelnen detaillierten Bericht gelten muss, extrahiert zugrunde liegende Konto- oder Transaktionsinformationen aus den Finanzdaten. Attribute auf Kontoebene zeigen Daten aus dem Konto an, und die Attribute auf Buchungsebene zeigen Daten an, die zum Zeitpunkt ausgeblendet werden, an dem die Buchung gebucht wurde. Wenn Sie als <strong>ATTR</strong> Spaltentyp auswählen, geben Sie in der Detailzeile der Attributkategorie der Spaltendefinition angegeben.</td>
    </tr>
    </tbody>
    </table>

### <a name="financial-dimensions-column"></a>Finanzdimensionensspalte

Die folgenden **Spaltendefinition**-Zeilendefinitionen gelten für Spalten, mit Spaltentyp **FD** (Beträge von den Finanzdimensionen).

#### <a name="book-codeattribute-category-cell"></a>Zelle "Buchcode/Attributkategorie"

Die Zelle **Buchcode/Attributkategorie** bestimmt den Buchcode für die Daten in der Spalte **FD**. Eine Spaltendefinition kann mehrere Ist-, Budget- und statistische Spalten enthalten. Eine Spaltendefinition kann unterschiedliche Perioden, wie aktuelles oder laufendes Jahr und unterschiedliche Beträge anzeigen. Die Liste der Buchcodes spiegelt das tatsächlichen, Budget- und statistischen (nicht wertmäßigen) Optionen wieder, die in den Finanzdaten eingerichtet worden sind.

#### <a name="fiscal-year-cell"></a>Geschäftsjahrzelle

Die Zelle **Geschäftsjahr** identifiziert das Geschäftsjahr, das in der Spalte enthalten sein soll. Das Jahr kann relativ zum Basisjahr sein, das angegeben wird, wenn der Bericht generiert wird. Die folgenden Optionen sind verfügbar.

| Mit der folgenden Option...  | Beschreibung                                                                                                                  |
|---------|------------------------------------------------------------------------------------------------------------------------------|
| BASIS    | Verwenden Sie das Basisjahr, das zum Zeitpunkt des Berichts angegeben wird.                                                                          |
| BASE+\# | Das Jahr, das \# Jahre nach das Basisjahr ist. Wenn Sie also beispielsweise das dritte Jahr nach dem Basisjahr verwenden, geben Sie **BASIS+3** ein. |
| \#Sie ignoriert | Das Jahr, das \# Jahre vor das Basisjahr ist. Wenn Sie also beispielsweise das Vorjahr verwenden, geben Sie **BASIS-1** ein.                 |
| \#      | Geben Sie das tatsächliche Geschäftsjahr ein.                                                                                                |

#### <a name="period-cell"></a>Periodenzelle

Die Zelle **Periode** identifiziert die Geschäftsperioden, die in der Spalte enthalten sein sollen. Der Zeitraum kann relativ zum Basiszeitraum sein, der angegeben wird, wenn der Bericht generiert wird. Die folgenden Optionen sind verfügbar.

| Mit der folgenden Option...          | Beschreibung                                                                                                                                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BASIS            | Verwenden Sie den Basiszeitraum.                                                                                                                                                                                                                 |
| BASE+\#         | Verwendet den Zeitraum, die \# Zeiträume nach dem Basiszeitraum liegt. Wenn Sie also beispielsweise die dritte Periode nach der Basisperiode verwenden, geben Sie **BASIS+3** ein.                                                                                               |
| \#Sie ignoriert         | Verwendet den Zeitraum, die \# Zeiträume vor dem Basiszeitraum liegt. Wenn Sie also beispielsweise die vorherige Periode verwenden, geben Sie **BASIS-1** ein.                                                                                                                 |
| Sie ignoriert \#: BASIS    | Verwenden Sie mehrere Perioden, aus mehreren Perioden vor der Basisperiode durch die Basisperiode. Um beispielsweise die drei vorangegangenen Perioden und die Basisperiode zu verwenden, geben Sie **BASIS-3: BASIS** ein.                                                |
| : BASEBASE+\#    | Verwenden Sie mehrere Perioden, aus mehreren Basisperioden durch mehrere Perioden nach der Basisperiode. Um beispielsweise die Basisperiode und die folgenden zwei Perioden zu verwenden, geben Sie **BASIS: BASIS+2** ein.                                                  |
| \#: BASEBASE+\# | Verwenden Sie mehrere Perioden, aus mehreren Perioden vor der Basisperiode bis zu mehreren Perioden nach der Basisperiode. Um beispielsweise die drei vorangegangenen Perioden, die Basisperioden und die folgenden zwei Perioden zu verwenden, geben Sie **BASIS-3: BASIS+2** ein. |
| 1:BASE          | Verwenden Sie mehrere Perioden, aus der ersten Periode durch die Basisperiode.                                                                                                                                                                 |
| \#              | Verwenden Sie immer eine bestimmte Periodenanzahl. Es wird nicht empfohlen, diese Option zu verwenden, da sie die Flexibilität der Spaltendefinition verringert.                                                                                       |
| \#                                      : \#           | Verwenden Sie immer einen bestimmten Periodenbereich. Es wird nicht empfohlen, diese Option zu verwenden, da sie die Flexibilität der Spaltendefinition verringert.                                                                                    |

Sie können in jedem der Zeitraumangaben über Geschäftsjahresgrenzen hinausgehen, und Sie können in einem Bereich von Perioden Jahre kombinieren. Geben Sie z den Perioden wie BASE-5 ** ** (also die letzten sechs Zeiträume enthält) und einen Bericht ausführen angezeigt, der einen Basiszeitraum. von 2 hat. In diesem Fall enthält der Bericht die Daten für die ersten beiden Zeiträume des angegebenen Geschäftsjahrs und die letzten vier Zeiträume des vorherigen Geschäftsjahrs angezeigt.

### <a name="specify-the-periods-for-an-fd-column"></a>Angeben der Perioden für eine FD-Spalte

1.  Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2.  Doppelklicken Sie in einer **FD**-Spalte auf die Zelle in der Zeile **Periode**, und wählen Sie dann in der Liste eine Option aus.
3.  Schließen Sie die Formel in der Formelleiste über dem Navigationsbereich oder in der Zelle **Periode** ab. Ersetzen Sie ein beliebiges Nummernzeichen (\#) durch den entsprechenden Wert.

#### <a name="periods-covered-cell"></a>Zelle "Abgedeckte Perioden"

Die Zelle **Abgedeckte Perioden** identifiziert den Betrag, der in der Spalte angezeigt werden soll. Dieser Betrag ist relativ zum Wert in den Zellen **Geschäftsjahr** und **Periode** für die Spalte. Die folgenden Optionen sind verfügbar.

| Mit der folgenden Option...      | Beschreibung                                                                 |
|-------------|-----------------------------------------------------------------------------|
| PERIODISCH    | Hier wird die Summe der Aktivität für die aktuelle Periode oder den Bereich der Perioden angezeigt. |
| PERIODISCH/BB | Hier wird der Anfangssaldo der Aktivität für die aktuelle Periode oder den Bereich der Perioden angezeigt.   |
| YTD         | Zeigen Sie die Summe der Aktivität seit Jahresbeginn an.                               |
| YTD/BB      | Hier wird der Anfangssaldo für das Jahr angezeigt.                                 |

### <a name="specify-the-periods-that-are-covered-for-an-fd-column"></a>Angeben der Perioden, die in einer FD-Spalte abgedeckt werden.

1.  Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2.  Doppelklicken Sie in einer **FD**-Spalte auf die Zelle in der Zeile **Abgedeckte Perioden**, und wählen Sie in der Liste eine Option aus.

### <a name="attribute-filter-in-a-column-definition"></a>Attributfilter in einer Spaltendefinition

Attribute sind Finanzdatenwerte, die ein Konto oder eine Transaktion weiter definieren. Die Kontoattribute umfassen **Anlage**, **Verbindlichkeiten**, **Umsatzerlös** und **Ausgaben**. Die Transaktionsattribute sind **Buchungsbeschreibung** und **Anwendungsdatum der Buchung**. Die Attributunterstützung unterschiedet sich möglicherweise zwischen Microsoft Dynamics ERP-Systemen. Die **Attributfilter**-Zelle beschränkt die Daten in den **FD**-Spalten auf bestimmte Werte oder Bereiche für Attributkategorien. Obwohl diese Funktion zusammen mit einer **ATTR**-Spalte verwendet werden kann, ist die **ATTR**-Spalte nicht erforderlich. In einer **FD**-Spalte gibt es eine Grenze für den Konten oder Transaktionen, die der Bericht aus dem Attributfilter umfasst. **Hinweis:** Im Integrationshandbuch für Ihr System sehen Sie, welche Attribute Ihr ERP-System unterstützt.

#### <a name="apply-an-attribute-filter-for-an-fd-column-on-a-report"></a>Anwenden eines Attributfilters für eine FD-Spalte in einem Bericht

1.  Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2.  Doppelklicken Sie auf die Zelle **Attributfilter** für eine **FD**-Spalte.
3.  Doppelklicken Sie im Dialogfeld **Attributfilter** auf eine Zelle in der Spalte **Attribute**, und wählen Sie anschließend den Filtertyp aus.
4.  Wenn Sie die Ergebnisse weiter einzuschränken möchten, geben Sie in den Spalten und **Von** und **Bis** einen Bereich ein. Das Feld **Von** muss einen positiven Wert enthalten.
5.  Klicken Sie auf **OK**.

#### <a name="example-of-an-attribute-filter"></a>Beispiel eines Attributfilters

Im folgenden Beispiel wird ein Teil einer Spaltenbeschreibung angezeigt, die ein Kontoattribut in der Zeile hat **Buchcode/Attributkategorie** aufweist. Der Attributfilter für diese Spalte gibt den Wertebereich an, der in den Bericht eingeschlossen werden soll.

|                              | A:    | Mrd                    |
|------------------------------|------|----------------------|
| Spaltentyp                  | BESCHR | FD                   |
| Buchcode/Attributkategorie |      | ISTWERT               |
| Geschäftsjahr                  |      | BASIS                 |
| Zeitraum                       |      | 1:BASIS               |
| Abgedeckte Perioden              |      | PERIODISCH             |
| ...                          |      |                      |
| Spaltenbreite                 | 30   |                      |
| ...                          |      |                      |
| Attributfilter             |      |  01:10 Reference=\]\[ |

### <a name="dimension-filter-in-a-column-definition"></a>Dimensionsfilter in einer Spaltendefinition

Ein Dimensionsfilter wird verwendet, um die Spalte **FD** auf bestimmte Dimensionswerte einzuschränken. Der Filter kann eine einzelne Dimension, einen Bereich von Dimensionen oder eine Gruppe von Dimensionen enthalten. Der Filter kann auch Dimensionswertsätze enthalten. Da Dimensionswerte variieren können, A. \ muss Finanzdimensionen \ dimensionsbasiertes System keine genaue Länge einer zu entsprechen. Der Filter wird unabhängig davon angewendet, ob der Bericht die Berichtsbaumstruktur umfasst. Sie können ein Platzhalterzeichen (?) in \* oder jeder beliebigen Position verwendet werden. Wenn Sie mehrere Konten angeben, ein Komma setzen Sie zwischen Konten, in wie im folgenden Beispiel ein: +Konto=\[1200\], +Konto=\[1100\], Abteilung=\[01?\] Um alle Abteilungen für ein bestimmtes Konto zu erhalten, können Sie die Abteilungsdimension aus dem Dimensionsfilter ausschließen. Beispielsweise werden die folgenden Dimensionsfilter auf dieselbe Weise behandelt:

-   +Konto=\[1100, Abteilung\]
-   +Konto=\[\]1100

Sie können eine beliebige Kombination von alphanumerischen Zeichen für genaue Treffer verwenden, und Sie können Teildimensionen definieren. Beispielsweise ** Lagerplatz \[= 10\*\]** schließt alle Standortdimensionswerte, die mit 10 beginnen.

#### <a name="apply-a-dimension-filter-for-a-column-on-a-report"></a>Anwenden von einen Dimensionsfilter für eine Spalte in einem Bericht

1.  Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2.  Doppelklicken Sie auf die Zelle **Dimensionsfilter** für eine **FD**-Spalte.
3.  Geben Sie im Dialogfeld **Dimensionen** die Filter ein, die angewendet werden sollen.
4.  Klicken Sie auf **OK**.

### <a name="format-a-multiple-currency-report-in-a-column-definition"></a>Formatieren eines Berichts mit mehreren Währungen in einer Spaltendefinition

Ein Bericht mit mehreren Währungen kann Beträge in der natürlichen (lokalen) Währung, der funktionalen (Standard)Währung oder der Berichtswährung anzeigen. Die funktionale Währung eines Unternehmens wird im Microsoft Dynamics ERP-System definiert. Verwechseln Sie diese ERP-Einstellung nicht mit den regionalen Optionseinstellungen des Betriebssystems, in dem Sie die Standardwährungssymbole konfigurieren können, die in Berichten verwendet werden. Die folgenden mit der Währung in Zusammenhang stehenden Zellen sind in der Spaltendefinition verfügbar:

-   ** Währungs-Anzeige ** – Geben Sie die Art der Währung an (natürliche oder funktionale Währung oder Berichtswährung), in dem die Buchungen angezeigt werden. Diese Funktionen auch als Währungsumrechnung bezeichnet. Währungsübersetzung ist die Möglichkeit, einen Bericht zu Hauptbuchbeträgen in einer Fremdwährung zu erstellen, die möglicherweise nicht die funktionelle Währung des Unternehmens ist oder die Währung, in der die Transaktion eingegeben wurde.
-   **Währungsfilter** - Geben Sie einen Währungsfilter an. Nur Transaktionen, die in der ausgewählten Währung eingegeben werden, werden im Bericht angezeigt.

**Hinweis:** Um Berichte zu erstellen, die mehrere Währungen verwenden, müssen Sie das Kontrollkästchen **Alle Berichtswährungen einschließen** auf der Registerkarte **Bericht** der Berichtsdefinition auswählen. Führen Sie die folgenden Schritte aus, um die funktionalen Währung eines Unternehmens zu bestimmen.

1.  Klicken Sie im Berichts-Designer im Menü **Unternehmen** auf **Unternehmen**.
2.  Wählen Sie im Dialogfeld **Unternehmen** ein Unternehmen aus, und klicken Sie anschließend auf **Anzeigen**.
3.  Im Dialogfeld **Unternehmen anzeigen** unter **Regionale Optionen** können Sie die Währung anzeigen, die für das ausgewählte Unternehmen definiert ist.

#### <a name="specify-the-currency-on-a-multiple-currency-report"></a>Angeben der Währung für einen Bericht mit mehreren Währungen

1.  Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2.  Doppelklicken Sie auf die Zelle ** Wähungsanzeige** in der entsprechenden **FD**-Spalte, und wählen Sie dann die Option für das Anzeigen von Währungsinformationen aus: **Natürlich/ursprüngliche Währung**, **Funktionale Währung aus Unternehmensinformationen** oder die Berichtswährung.
3.  Doppelklicken Sie auf die Zelle **Währungsfilter** in der entsprechenden **FD**-Spalte, und wählen Sie dann den entsprechenden Währungscode in der Liste aus. Es werden nur Transaktionen im Bericht angezeigt, die in dieser Währung eingegeben werden.

**Hinweis:** Die Optionen, die hier beschriebenen werden, unterschieden sich je nach ERP-System. Weitere Informationen finden Sie Systemdokumentation ERP Ihr [Microsoft] (https://www.microsoft.com/en-us/download/details.aspx?id=5916).

### <a name="example-for-currency-display-and-currency-filter-cells"></a>Beispiel für Währungsanzeige und Währungsfiltertellen

Phyllis hat die folgende Währungsauswahl in ihrer Spaltendefinition vorgenommen:

-   **Währungsfilter:** Yen
-   **Währungsanzeige:**-Funktional (US-Dollar)

Aufgrund des Währungsfilters, den Phyllis ausgewählt hat, umfasst der Bericht nur Transaktionen, die in japanischen Yen (JPY) eingegeben wurden. Aufgrund der Währungsanzeige, die sie auswählt hat, werden im Bericht die Transaktionen in der funktionalen Währung US-Dollar (USD) angezeigt.

#### <a name="currency-filter-and-currency-display-combinations"></a>Währungsfilter und Währungsanzeige-Kombinationen

In der folgenden Tabelle werden die Berichtsergebnisse aufgelistet, die aufgrund der von Phyllis getroffenen Auswahl für verschiedene Kombinationen der Optionen in den Zellen **Währungsanzeige** und **Währungsfilter** auftreten können. Die funktionalen Währung in USD

| Währungsanzeigezelle                        | Währungsfilterzelle | Ergebnisbericht                                                                                                                                                                                    |
|----------------------------------------------|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Natürlich/ursprüngliche Währung                 | **YEN**              | **Y6.000** - Das Ergebnis zeigt nur Buchungen an, die in JPY eingegeben wurden.                                                                                                                        |
| Funktionale Währung aus Unternehmensinformationen | **YEN**              | **$60** - Das Ergebnis zeigt nur die Transaktionen, die in JPY eingegeben wurden zeigt diese Transaktionen in USD an. **Hinweis:** Der Wechselkurs ist ungefähr 100 JPY pro USD.                    |
| Funktionale Währung aus Unternehmensinformationen | Leer                | **\*\*– $2.310 ** das Ergebnis werden alle Daten in der funktionalen Währung angezeigt, das in den Unternehmensinformationen angegeben wird. **Hinweis:** Dieser Betrag ist die Summe aller Transaktionen in der funktionalen Währung. |
| Natürliche/ursprüngliche Währung                 | Leer                | **$2.250** - Das Ergebnis zeigt alle Beträge in der Währung an, in der die Transaktion ausgeführt wurde.                                                                                                 |

### <a name="calculation-column-in-a-column-definition"></a>Berechnungsspalte in einer Spaltendefinition

Ein von CALC Spaltentyp ** ** in einer Spaltendefinition unterstützt komplexe Berechnungen in der Formel ** ** Zelle und kann beigefügt ** ** **+,-,\*** ** **, und/** ** Operatoren, und auch ** IF/THEN/ELSE ** Auszüge. Eine Berechnungsspalte kann jede beliebige andere Spalte, auch auch folgende Spalten verweisen. Darüber hinaus kann eine Spalte das Geschäftsjahr und die Periode umfassen, um Überschriften für die Spalte zu unterstützen. Die Berechnungsformel kann bis zu 1.024 Zeichen lang sein. Um das Berechnungsergebnis als Prozentsatz auszudrücken, verwenden Sie eine spezielle Formataußerkraftsetzung. **Hinweis:** Die Ergebnisse der Berechnungsformeln enthalten keine Werte der nicht druckbaren Spaltenbereiche. Beispielsweise **A:D** druckt **0** (null), wobei **A+B+C** für nicht druckbare Werte den Wert berechnet.

#### <a name="operators-in-calculation-columns"></a>Operatoren in den Berechnungsspalten

Um Spalten zu addieren, subtrahieren, multiplizieren oder zu dividieren geben Sie die Buchstaben in der Reihenfolge der Berechnung ein und verwenden den entsprechenden Operator, um jeden Spaltenbuchstaben abzugrenzen. In der folgenden Tabelle werden die Operatoren beschrieben, die Sie in einer Berechnungsspalte verwenden können.

| Bediener | Beispielberechnung | Beschreibung                                                                                                                                                                                                                                    |
|----------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| +        | A+C                 | Addieren Sie den Betrag in Spalte A zum Betrag in der Spalte C.                                                                                                                                                                                          |
| :        | A:C A:C-D           | Addieren Sie einen Bereich fortlaufender Spalten. Beispielsweise addiert die **A:C**-Formel die Summen der Spalten A bis C, und die Formel **A:C-D** addiert die Summen der Spalten A bis C und subtrahiert anschließend den Betrag in der Spalte D.                          |
| -        | A-C                 | Subtrahieren Sie den Betrag in Spalte A vom Betrag in der Spalte C. **Hinweis:** Sie können auch das Minuszeichen (-) verwenden, um die Vorzeichen in einer Spalte umzukehren. Verwenden Sie beispielsweise **- A+B**, um den umgekehrten Betrag in Spalte A zum Betrag in der Spalte B zu addieren. |
| \*       | \*C                | Multiplizieren Sie den Betrag in Spalte A mit dem Betrag in der Spalte C.                                                                                                                                                                                     |
| /        | A/C                 | Dividieren Sie den Betrag in Spalte A durch den Betrag in der Spalte C.                                                                                                                                                                                       |

#### <a name="use-a-calculation-formula-in-a-column-definition"></a>Verwenden einer Berechnungsformel in einer Spaltendefinition

1.  Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2.  Geben Sie in der entsprechenden **CALC**-Spalte eine Formel in der Zelle **Formel** ein.

#### <a name="complex-calculations"></a>Komplexe Berechnungen

Eine komplexen Berechnung kann eine beliebige Kombination aus Zellenreferenzen, Operatoren, Werten und Ebenen geschachtelter Klammern enthalten. Um beispielsweise den Durchschnitt der Spalten A und B zu berechnen, verwenden Sie die Berechnungsformel **((A+B)/2)**.

#### <a name="specify-report-cells-in-a-column-calculation"></a>Angeben von Berichtszellen in einer Spaltenberechnung

Sie können eine bestimmte Berichtszelle verweisen, indem Sie einen Spaltenbuchstaben und einen Zeilencode eingeben. Beispielsweise bezieht sich **B.100** auf Zeilencode 100 in der Spalte B. Sie können eine vollständige Spalte durch einen bestimmten Berichtszellenbetrag dividieren, der in der gleichen Spalte ist. Die Berechnung **B/B.100** bedeutet beispielsweise, dass der Betrag in der Spalte B durch den Wert in Zeilencode 100 in der Spalte B dividiert werden soll. Wenn die Berechnung auf eine Spalte verweist, die von einer anderen Spalte abhängt, wird die abhängige Spalte zuerst aufgelöst. Wenn Sie eine Spalte auf eine andere Spalte verweist, die wieder auf die erste Spalte verweist, verursacht dies einen Zirkelverweisfehler. **Hinweis:** Die Berechnung ist möglicherweise nicht korrekt, wenn Sie die Berechnungspriorität für den Bericht ändern. Sie können die Berechnungspriorität auf der Registerkarte **Einstellungen** der Berichtsdefinition festlegen.

#### <a name="multiply-or-divide-a-column-by-a-base-row"></a>Multiplizieren oder dividieren einer Spalte mit einer Basiszeile

Sie können eine Spalte erstellen, die alle Werte in einer angegebenen Spalte als Prozentsatz einer Basiszahl anzeigt. Daher können Sie Beziehungen zwischen Zeilen, wie den Prozentsatz einer Vertriebszeile oder den Prozentsatz einer Gesamtkostenzeile, anzeigen. Multiplizieren jeder Zeile in einer bestimmten Spalte mit einer Basiszeile oder zum Dividieren der Spalte, die Sie zur Verwendung innerhalb der Berechnung ein, und geben Sie anschließend \*** BASEROW ** ein oder ** ** /BASEROW. Geben Sie z ** C \*BASEROW ** ein oder C/BASEROW ** **. ** Hinweis:** Wenn Sie eine Basiszeilenberechnung in einer Spaltendefinition verwenden, sollten Sie sicherstellen, dass jede Zeilendefinition, die mit dieser Spaltendefinition verwendet wird, mindestens eine Basiszeile für Berechnungen enthält.

#### <a name="divide-the-amount-in-a-column-by-the-number-of-periods"></a>Dividieren des Betrag in einer Spalte durch die Anzahl der Perioden

Sie können den Betrag in einer Spalte durch eine angegebene Anzahl von Perioden dividieren. Beispielsweise dividiert die Formel **B/Perioden** den Wert in der Spalte B durch die Anzahl der Perioden in der Spalte B. Wenn die Berechnung mehrere Spalten umfasst, geben Sie die Anzahl der Perioden an, die bei der Berechnung verwendet werden sollen. Beispielsweise addiert die Formel **(B+C)/Perioden** die Beträge in der Spalte B und in der Spalte C und dividiert dann das Ergebnisses durch den Periodenwert.

<a name="see-also"></a>Siehe auch
--------

[Zeilendefinitionen in der Finanzberichterstellung](row-definitions-financial-reporting.md)

[Erweiterte Formatierungsoptionen in der Finanzberichterstellung](advanced-formatting-options-financial-reporting.md)


