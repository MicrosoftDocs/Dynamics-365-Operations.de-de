---
title: Spaltendefinitionen in Finanzberichten
description: Dieser Artikel enthält Informationen zu Spaltendefinitionen. Eine Spaltendefinition ist eine Berichtkomponente oder ein Baustein, die den Inhalt jeder Spalte eines Berichts angibt. Wie auch Zeilendefinitionen können grundlegende Spaltendefinitionen in mehreren Berichten verwendet werden.
author: ShylaThompson
manager: AnnBe
ms.date: 10/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 106601
ms.assetid: 66e72a48-edab-4e9d-815f-596a1623c258
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 54e7d517e704b7162f3e091330a246386f0203ea
ms.sourcegitcommit: d800613020d5548d100c8f240fb81bb6258a3646
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/11/2019
ms.locfileid: "2572640"
---
# <a name="column-definitions-in-financial-reports"></a>Spaltendefinitionen in Finanzberichten

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zu Spaltendefinitionen. Eine Spaltendefinition ist eine Berichtkomponente oder ein Baustein, die den Inhalt jeder Spalte eines Berichts angibt. Wie auch Zeilendefinitionen können grundlegende Spaltendefinitionen in mehreren Berichten verwendet werden.

## <a name="create-and-modify-a-column-definition"></a>Erstellen und Ändern einer Spaltendefinition

Eine Spaltendefinition kann zwei bis 255 Spalten enthalten.

### <a name="create-a-column-definition"></a>Erstellen einer Spaltendefinition

1. Klicken Sie im Berichts-Designer im Navigationsbereich auf **Spaltendefinitionen** .
2. Wählen Sie im Menü **Datei** die Option **Neu** aus, und klicken Sie dann auf **Spaltendefinitionen**.
3. Fügen Sie den Inhalt der Spaltendefinition hinzu.

### <a name="open-a-column-definition"></a>Öffnen einer Spaltendefinition

1. Klicken Sie im Berichts-Designer im Navigationsbereich auf **Spaltendefinitionen** .
2. Doppelklicken Sie auf eine Spaltendefinition, um sie zu öffnen.

### <a name="add-a-column-to-a-column-definition"></a>Hinzufügen einer Spalte zu einer Spaltendefinition

1. Im Berichts-Designer klicken Sie auf die **Spaltendefinitionen** und öffnen dann die Spaltendefinition, um sie zu ändern.
2. Wählen Sie die Spalte aus, in die die neue Spalte eingefügt werden soll.
3. Klicken Sie im Menü **Bearbeiten** auf **Spalte einfügen**. Die neue Spalte erscheint links von der ausgewählten Spalte.

### <a name="delete-a-column-from-a-column-definition"></a>Löschen einer Spalte aus einer Spaltendefinition

1. Klicken Sie im Berichts-Designer auf **Spaltendefinitionen**, und öffnen Sie dann die zu ändernde Spaltendefinition.
2. Wählen Sie die zu löschende Spalte aus.
3. Klicken Sie im Menü **Bearbeiten** auf **Spalte löschen**.

## <a name="contents-of-a-column-definition"></a>Inhalt einer Spaltendefinition
Eine Spaltendefinition enthält die folgenden Informationen:

- Eine Spalte der Zeilendefinitionsbeschreibungen
- Betragsspalten, die Daten aus den Finanzdaten oder Berechnungen anhand anderer Daten in der Spaltendefinition enthalten
- Formatierungsspalten
- Attributspalten

Diese Informationen erscheinen in den folgenden Bereichen in der Spaltendefinition:

- Der Überschriftenbereich der Spaltendefinition enthält den Überschriftentext und die Formatierung, die im Bericht erscheint. Eine Überschrift kann für eine einzelne Datenspalte gelten, auf mehrere Spalten ausgebreitet werden oder auf bedingter Basis für Spalten gelten. Die Spaltendefinition kann beliebig viele Spaltenüberschriftszeilen enthalten.

    > [!NOTE]
    > Spaltenüberschriften gelten für jede Datenspalte im Bericht. Berichtsüberschriften gelten für den ganzen Bericht. Sie definieren Berichtskopfzeilen auf der Registerkarte **Kopf- und Fußzeilen** der Berichtsdefinition.

- Spaltendetailzeilen sind die Zeilen unter den Überschriftszeilen in der Spaltendefinition. In Spaltendetailzeilen werden die Informationen definiert, die im Bericht berücksichtigt werden. In der folgenden Tabelle werden die Spaltendetailzeilen aufgeführt und beschrieben.

    | Name der Spaltendetailzeile                                                | Beschreibung                                                                                            |
    |-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
    | Spaltentyp                                                           | (Erforderlich) Legen Sie den Typ der Daten in der Spalte fest.                                                     |
    | Buchcode/Attributkategorie                                          | Geben Sie Finanzdateninformationen für Spalten der Typen **FD** und **ATTR** an.                       |
    | Geschäftsjahr Zeitraum Abgedeckte Zeiträume                                    | Geben Sie Finanzdateninformationen für Spalten des Typs **FD**.                                     |
    | Formel                                                               | Geben Sie eine Berechnungsformel für Spalten des Typs **CALC** an.                                        |
    | Spaltenbreite Zusätzliche Leerzeichen vor Spalte Formataußerkraftsetzung Drucksteuerung | Geben Sie besondere Formatierungsoptionen an.                                                                        |
    | Spalteneinschränkungen                                                   | Schränken Sie Daten ein.                                                                                         |
    | Berichtseinheit                                                        | Schränken Sie die Spalte so ein, dass sie nur Daten für die angegebene Berichtseinheit enthält.                      |
    | Währungsanzeige Währungsfilter                                      | Formatieren Sie die Währung.                                                                                       |
    | Dimensionsfilter                                                      | Geben Sie einen Filter an, mit dem Daten auf bestimmte Finanzdaten-Berichtseinheiten beschränkt werden.                           |
    | Attributfilter                                                      | Geben Sie einen Filter an, mit dem die Finanzdaten eingegrenzt werden.                                                       |
    | Startdatum Enddatum                                                   | Schränken Sie die Finanzdaten auf bestimmte Daten ein.                                                         |
    | Ausrichtung                                                         | Richten Sie die Beschreibung, die in der Zeilendefinition angegeben ist, linksbündig, mittig oder rechtsbündig aus. |

## <a name="column-restrictions-in-a-column-definition"></a>Spalteneinschränkungen in einer Spaltendefinition
Sie können Spalteneinschränkungen verwenden, um anzugeben, wie eine Spaltendefinition Daten verwendet oder Informationen berechnet. Sie können auch eine Berichtsspalte auf eine spezifische Einheit oder spezifische Datumsangaben beschränken.

> [!NOTE]
> Ein Code zur **Spalteneinschränkung** hat Vorrang vor jeglichen anders lautenden Einstellungen in der Zeilendefinition.

### <a name="column-restrictions-cell"></a>Spalteneinschränkungszelle

Die Zelle **Spalteneinschränkungen** kann Codes umfassen, die Informationen, wie Zeilenformatierung, Details und Beträge für diese Spalte, enthalten, beschränken oder unterdrücken.

#### <a name="add-a-column-restriction-in-a-column-definition"></a>Hinzufügen einer Spalteneinschränkung in eine Spaltendefinition

1. Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2. Doppelklicken Sie auf die Zelle **Spalteneinschränkungen** für die einzuschränkende Spalte.
3. Wählen Sie im Dialogfeld **Spalteneinschränkungen** eine oder mehrere Codes aus der Liste aus, und klicken Sie anschließend auf **OK**.

### <a name="column-restriction-codes"></a>Spalteneinschränkungscodes

In der folgenden Tabelle werden die Spalteneinschränkungscodes beschrieben.

| Spalteneinschränkungscode | Beschreibung |
|-------------------------|-------------|
| UU                      | Unterdrücken Sie den Unterstrich für eine Spalte, wo entweder ein Unterstrichbefehl (**---**) oder ein doppelter Unterstrichbefehl (**===**) in die Zeilendefinition eingegeben wird. Beispielsweise sollten Sie keine Beträge unterstreichen, die von einer Prozentberechnung produziert werden. |
| SU                      | Unterdrücken Sie Summen und zeigen Sie in dieser Spalte nur Details an (z. B. in statistischen Spalten). |
| DU                      | Unterdrücken Sie Details, sodass nur **TOT** und **CAL**-Zeilen (von der Zeilendefinition) in der Spalte angezeigt werden. |
| DR                      | Beschränken Sie die Beträge in einer **FD**-Spalte auf die Sollbeträge. |
| CR                      | Beschränken Sie die Beträge in einer **FD**-Spalte auf die Habenbeträge. |
| ADJ                     | Schränken Sie die Beträge in der Spalte auf Zeitraumberichtigungsbeträge (falls verfügbar) ein. |
| XAD                     | Schränken Sie die Beträge in der Spalte so ein, dass Zeitraumberichtigungsbeträge (falls verfügbar) ausgeschlossen werden. |
| PT                      | Schränken Sie die Beträge in der Spalte so ein, sodass nur gebuchte Posten enthalten sind, wenn diese verfügbar sind. |
| UPT                     | Beschränken Sie die Beträge in der Spalte, sodass nur nicht gebuchte Transaktionen enthalten sind, wenn diese Transaktionen verfügbar sind.<p><strong>Hinweis:</strong> Nicht alle Daten unterstützen nicht gebuchte Transaktionen. Weitere Informationen finden Sie im <a href='https://go.microsoft.com/fwlink/?LinkID=162565'>Datenintegrationshandbuch</a> für Ihr Microsoft Dynamics ERP-System.</p> |

### <a name="restrict-a-column-to-a-reporting-unit"></a>Einschränken einer Spalte auf eine Berichtseinheit

1. Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2. Doppelklicken Sie auf die Zelle **Berichtseinheit** für die einzuschränkende Spalte.
3. Wählen Sie im Dialogfeld **Auswahl der Berichtseinheit** in der Liste **Berichtsstruktur** eine Berichtserstellungsbaumstruktur aus.
4. Erweitern oder reduzieren Sie die Liste der Einheiten, wählen Sie eine Berichtseinheit aus, und klicken Sie anschließend auf **OK**.

## <a name="format-column-headers"></a>Formatieren Sie Spaltenüberschriften
Sie können die Überschriften, die am oberen Rand der Spalten in einem Bericht angezeigt werden, hinzufügen, ändern und löschen. Sie können bedingte umfassende Spaltenüberschriften basierend auf dem Feld **Periode** aus den Spaltendefinitionen und dem Feld **Basiszeitraum** aus den Berichtsdefinitionen konfigurieren. Mit dem Feature "Basiszeitraum" können Sie beim Erstellen von Berichten mit rollenden Prognosen Zeit sparen.

### <a name="create-and-manage-column-headers"></a>Spaltenkopfzeilen erstellen und verwalten

Sie können das Dialogfeld **Spaltenüberschrift** verwenden, um Überschriften hinzuzufügen, zu ändern und zu löschen, die am oberen Rand der Spalten in einem Bericht angezeigt werden. In der folgenden Tabelle werden die Felder im Dialogfeld **Spaltenüberschriften** beschrieben.

| Feld                 | Beschreibung |
|-----------------------|-------------|
| Spaltenüberschriftstext    | Dieser Text wird in der Spaltenüberschrift angezeigt. Sie können Text direkt in dieses Feld eingeben, oder auf **AutoText einfügen** klicken, um eine Option auszuwählen, die die Spaltenüberschrift jedes Mal aktualisiert, wenn der Bericht generiert wird. Um mehrere Autotextcodes einzubeziehen, klicken Sie erneut auf **AutoText einfügen**, und klicken Sie anschließend auf einen anderen Code in der Liste. |
| Formatoptionen        | Wenden Sie Formatierungen für Spaltenüberschriften an, beispielsweise Rahmen oder Unterstreichung. |
| Zuweisen von Zuweisen bis | Definieren Sie die Spalte oder die Spalten, für die der Überschriftstext gilt. |
| Ausrichtung         | Geben Sie an, wie der Spaltenüberschrifttext für die Spalte oder den Bereich der Spalten ausgerichtet sein soll, die in den Feldern **Verbreiten von** und **Verbreiten zu** angegeben sind. |

### <a name="create-a-column-header"></a>Erstellen einer Spaltenüberschrift

1. Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2. Doppelklicken Sie auf eine Überschriftszelle.
3. Geben Sie im Dialogfeld **Spaltenüberschrift** den Text der Spaltenüberschrift ein. Klicken Sie alternativ auf **AutoText einfügen**, und wählen Sie eine Option aus.
4. Wählen Sie im Feld **Formatoptionen** ein Format für die Überschrift aus.
5. Geben Sie im Feld **Verbreiten von** den Buchstaben der Spalte ein, die über der die Spaltenüberschrift anfangen soll. Geben Sie im Feld **Verbreiten zu** den Buchstaben der Spalte ein, die über der die Spaltenüberschrift enden soll.
6. Wählen Sie unter **Begründung** aus, ob der Text der Spaltenüberschrift links, rechts oder zentriert ausgerichtet sein soll.
7. Klicken Sie auf **OK**.

### <a name="add-a-column-header-row"></a>Hinzufügen einer Spaltenüberschrift

1. Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2. Wählen Sie eine Zelle in der Überschriftszeile aus.
3. Klicken Sie im Menü **Bearbeiten** auf **Zeile einfügen**. Die neue Zeile wird über der in Schritt 2 ausgewählten Zeile eingefügt.

> [!NOTE]
> Wenn Sie mehr als vier Zeilen für Kopfzeilen auf einem Bericht haben, überschneiden sich die Kopfzeilen, wenn der Bericht in ein Excel-Arbeitsblatt exportiert wird. Vergrößern Sie den oberen Rand in der Berichtsdefinition, damit alle Kopfzeilen im Bericht angezeigt werden.

### <a name="delete-a-column-header-row"></a>Löschen einer Spaltenüberschrift

1. Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2. Wählen Sie eine zu löschende Zelle in der Überschriftszeile aus.
3. Klicken Sie im Menü **Bearbeiten** auf **Zeile löschen**.

### <a name="create-an-automatically-generated-header"></a>Erstellen einer automatisch generierten Überschrift

Der Bericht-Designer kann Spaltenüberschriften auf Grundlage von Autotextcodes automatisch generieren. AutoText-Codes sind Variablen, die bei jedem Generieren eines Berichts aktualisiert werden. Diese Codes können in jeder Spaltenüberschrift enthalten sein und geben Berichtsinformationen (z. B. Datum oder Zeitraumnummer) an, die variieren können. Daher können Sie eine Spaltendefinition für mehrere Berichtsdefinitionen, Zeiträume und Berichtsbaumstrukturen verwenden. Da Autotextcodes auf den Kalenderdaten aus den Detailzeilen der Spaltendefinition beruhen, werden sie nur für **CALC** und **FD**-Spalten unterstützt. Die Darstellung des AutoText-Codes in der Spaltenüberschriftszelle beeinflusst auch die Darstellung der Informationen im Bericht. Im Dialogfeld **Spaltenüberschrift** werden die Autotextcodes in Groß- und Kleinbuchstaben angezeigt. Daher wird der Text im Bericht in gemischter Groß- und Kleinschreibung angezeigt. Beispielsweise wird in einem standardmäßigen Kalenderjahr von **\@CalMonthLong** der Monat **7** zu **Juli** aufgelöst. Wenn Sie möchten, dass der Monat in Großbuchstaben angezeigt wird (z. B. **JULI**), geben Sie den AutoText-Code im Feld **Spaltenüberschriftstext** in Großbuchstaben ein. Geben Sie beispielsweise **\@CALMONTHLONG** ein. Sie können Codes mit Text kombinieren. Geben Sie beispielsweise den folgenden Überschrifttext ein: **Period \@FiscalPeriod-\@FiscalYear von \@StartDate zu \@EndDate**. Die Berichtsüberschrift, die generiert wird, ähnelt dem folgenden Text: **Periode 1-02 von 01/01/02 bis 01/31/02**.

> [!NOTE]
> Das Format von Teilen des Texts, wie z. B. ein langes Datum, hängt von den regionalen Einstellungen des Servers ab. Um diese Einstellungen zu ändern, klicken Sie auf die Schaltfläche **Start**, klicken Sie auf **Systemsteuerung**, und klicken Sie anschließend auf **Region und Sprache**. In der folgenden Tabelle werden die verfügbaren AutoText-Optionen für Spaltenüberschriften aufgelistet.


| AutoText-Option und -Code                | Beschreibung |
|-----------------------------------------|-------------|
| Monatsname (@CalMonthLong)              | Drucken Sie den Namen des aktuellen Monats in der Spaltenüberschrift aus. Wenn Sie die Beträge im Bericht auf Tausend, Millionen oder Milliarden runden oder die Spaltenbreite im Bericht auf weniger als neun Zeichen festlegen, wird der Monatsname mit den ersten drei Zeichen abgekürzt. |
| Abgekürzter Monatsname (@CalMonthShort) | Drucken Sie den abgekürzten Monatsnamen für den ausgewählten Buchhaltungszeitraum aus. |
| Zeitraumnummer (@FiscalPeriod)           | Drucken Sie die numerische Form des Buchhaltungszeitraums für diese Spalte aus. Wenn die Spalte mehrere Zeiträume umfasst, wird der letzte Zeitraum im Bereich ausgegeben. |
| Zeitraumbeschreibung (@FiscalPeriodName)  | Drucken Sie die Beschreibung des Buchhaltungszeitraums für die Finanzdaten aus. |
| Geschäftsjahr (@FiscalYear)               | Drucken Sie das Geschäftsjahr für die Spalte in numerischer Form aus. |
| Kalenderjahr (@CalYear)                | Drucken Sie das Kalenderjahr für die Spalte in numerischer Form aus. |
| Startdatum (@StartDate)                 | Drucken Sie das Startdatum für die Spalte aus. |
| Enddatum (@EndDate)                     | Drucken Sie das Enddatum für die Spalte aus. |
| Einheitsname aus Struktur (@UnitName)         | Druckt den Einheitsnamen in der Spaltenüberschrift, wenn Sie eine Spalte auf eine bestimmte Einheit der Berichtsbaumstruktur einschränken. |
| Einheitenbeschreibung (@UnitDesc)            | Druckt die Einheitsbeschreibung in der Spaltenüberschrift, wenn Sie eine Spalte auf eine bestimmte Einheit der Berichtsbaumstruktur einschränken. |
| Buchcode (@BookCode)                   | Druckt den in der Spalte angegebenen Buchcode. |
| Leerzeile (@Blank)                     | Fügen Sie eine leere Zeile in die Spaltenüberschrift ein. |

### <a name="create-a-conditional-spanning-header"></a>Erstellen einer Kopfzeile für bedingte Aufteilung

Kopfzeilen für bedingte Aufteilung können basierend auf Daten für spezifische Zeiträume mehrere Spalten umfassen. Wenn Sie beispielsweise über einen Budgetbericht für das Geschäftsjahr verfügen und die tatsächlichen Budgets vergangener Monate mit den voraussichtlichen Budgets für künftige Monate anzeigen möchten, können Sie eine Kopfzeile für bedingte Aufteilung verwenden, um die Kopfzeile des Berichts automatisch zu aktualisieren. Beachten Sie beim Erstellen einer Kopfzeile für bedingte Aufteilung Folgendes:

- Jedes Beendigungsbedingung (**Verbreiten zu**-Feld), die vor einer Startbedingung (**Verbreiten von**-Feld) entsprochen wird, wird ignoriert. Wenn beispielsweise in Spalte B die Zuweisungsbedingung als „BASE+1 bis BASE“ definiert ist und sich BASE in Spalte C und BASE+1 in Spalte D befinden, wird die Stopp-Bedingung in Spalte C ignoriert, und der Druck der Kopfzeile beginnt bei Spalte D.
- Wenn Sie Spaltenüberschriften angeben, die sich überschneiden, überschneiden sich diese auch auf dem ausgedruckten Bericht. Der Bericht wird generiert, jedoch die folgende Warnung wird im Feld **Berichtswarteschlangenstatus** angezeigt: "Spaltenüberschriften mit BASE überschneiden sich mit anderen Spaltenüberschriften und können eine Überlappung des Texts zur Folge haben." Beispielsweise ist die Kopfzeilendefinition für Spalte B "B bis BASE+1, und die Kopfzeilendefinition für Spalte D "BASE +1 zu F. in diesem Fall, werden die Kopfzeilen übereinander gedruckt und sind nicht lesbar. Sobald BASIS in einer Definition **Verbreiten aus/Verbreiten bis** verwendet wird, stellen Sie sicher, den Bericht anzuzeigen, der generiert wird, um festzustellen, ob die Überschriften sich überschneiden.
- Wenn Sie in der Verbreitungsdefinition in einer nicht gedruckten Spalte(**NP**) BASIS angeben, wird diese ignoriert, unabhängig davon, was in der Spaltendefinition definiert ist. Im Wesentlichen entspricht dieses Szenario einer Situation, in der keine Spaltenüberschriftdefinition erstellt wird.
- Für bedingte Drucksspalten (**P&lt;B**, **P&gt;=B**) verhalten sich bedingte Überschriften wie die einzelnen regulären Spaltenüberschriftdefinition. Ist die Bedingung beispielsweise „false“, wird der Druck der Kopfzeile bei einer beliebigen darauffolgenden Spalte gestartet, die die Zuweisungsbedingung erfüllt.

#### <a name="create-a-conditional-spanning-header"></a>Erstellen einer Kopfzeile für bedingte Aufteilung

1. Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2. Doppelklicken Sie auf eine Überschriftszelle.
3. Geben Sie im Dialogfeld **Spaltenüberschrift** den Text der Spaltenüberschrift ein. Klicken Sie alternativ auf **AutoText einfügen**, und wählen Sie eine Option aus.
4. Wählen Sie im Feld **Formatoptionen** ein Formatierungstil für die Überschrift aus.
5. Geben Sie einen Zeitraum an, der relativ zu dem beim Generieren des Berichts angegebenen Basiszeitraum ist. Geben Sie in den Feldern **Verbreiten von** und **Verbreiten bis** einen der folgenden Werte ein: **BASIS**, **BASIS-X** oder **BASIS+X**, wobei X die Anzahl von Perioden des Basiszeitraums ist. Wenn Sie beispielsweise **BASIS** im Feld **Verbreiten von** eingeben, beginnt der bedingte verbreitete Spaltenüberschrifttext in der Spaltenüberschrift, in der der Wert des **Basiszeitraums** der Berichtsdefinition dem **Perioden**-Wert der Spaltendefinition entspricht. Er endet in der Spalte, die im **Verbreiten bis**-Feld angegeben ist. Wenn die Verbreitung z. B. BASIS bis M ist, und der Wert des **Basiszeitraums** der Berichtsdefinition **4** ist, beginnt die Überschrift in der Spalte, in der die Periode auf **4** festgelgt ist, und stoppt bei Spalte M. Überschriften beginnen und enden nur bei Druckspalten.
6. Wählen Sie unter **Begründung** aus, ob der Text der Spaltenüberschrift links, rechts oder zentriert ausgerichtet sein soll.
7. Klicken Sie auf **OK**.

#### <a name="example-of-a-conditional-spanning-header"></a>Beispiel einer Kopfzeile für bedingte Aufteilung

Phyllis erstellt einen Bericht für eine dynamische Sechs-Monats-Prognose. Das Wort "Istwert" soll über die Spalten mit Istdaten gedruckt werden, und das Wort "Budget" soll über die Spalten mit Prognosen für das Budget gedruckt werden. Jeden Monat, den der Bericht ausgeführt wird, gibt es eine Istwert-Spalte mehr und eine Budget-Spalte weniger. Phyllis könnte die Spaltendefinition jedes Mal, wenn der Bericht erstellt wird, manuell ändern und die Kopfzeilen anpassen. Sie möchte jedoch Zeit und Arbeit sparen und erstellt Kopfzeilen für bedingte Aufteilung, von denen automatisch bei jeder Ausführung des Berichts Kopfzeilen über den entsprechenden Spalten erstellt werden. Phyllis öffnet den Berichts-Designer, klickt im Navigationsbereich auf **Spaltendefinition** und öffnet die Spaltendefinition für den Bericht. Sie gibt die folgenden Informationen ein. Der Basiszeitraum in der Berichtsdefinition ist 4.


|                     |  A   | B             | C             | D             | E             | F             | G             | H             | I             | J             | K             | L             | M             |
|---------------------|------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|
| Überschrift 1            |      | Istwert        | Budget        |               |               |               |               |               |               |               |               |               |               |
| Überschrift 2            |      | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong |
| Überschrift 3            |      |               |               |               |               |               |               |               |               |               |               |               |               |
| Spaltentyp         | BESCHR | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            |
| Buchcode/Attribut |      | ISTWERT        | BUDGET2012    | ISTWERT        | BUDGET2012    | ISTWERT        | BUDGET2012    | ISTWERT        | BUDGET2012    | ISTWERT        | BUDGET2012    | ISTWERT        | BUDGET2012    |
| Geschäftsjahr         |      | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          |
| Zeitraum              |      | 1             | 1             | 2             | 2             | 3             | 3             | 4             | 4             | 5             | 5             | 6             | 6             |
| Abgedeckte Zeiträume     |      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      |
| Spaltenbreite        | 30   | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            |
| Drucksteuerung       |      | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        |

Phyllis doppelklickt auf eine Spaltenüberschriftzelle, um das Dialogfeld **Spaltenüberschrift** zu öffnen, in dem sie die folgenden Informationen eingibt.

| Feld              | Wert                 |
|--------------------|-----------------------|
| Spaltenüberschriftstext | Istwert                |
| AutoText einfügen    | Keine Auswahl getroffen. |
| Formatoptionen     | Kasten                   |
| Ausrichtung      | Keine Auswahl getroffen. |
| Zuweisen von        | B                     |
| Zuweisen bis          | BASE                  |
| Budget-Kopfzeile      | BASE+1 bis letzte Spalte  |

Nachdem sie die Informationen eingeben hat, klickt Phyllis auf **OK**. Dann doppelklickt sie auf die Spaltenüberschriftzelle in Spalte C, um das Dialogfeld **Spaltenüberschrift** zu öffnen, in dem sie die folgenden Informationen eingibt.

| Feld              | Wert                 |
|--------------------|-----------------------|
| Spaltenüberschriftstext | Budget                |
| AutoText einfügen    | Keine Auswahl getroffen. |
| Formatoptionen     | Kasten                   |
| Ausrichtung      | Keine Auswahl getroffen. |
| Zuweisen von        | C                     |
| Zuweisen bis          | BASE+2                |

Jetzt wird jedes Mal, wenn dieser Bericht generiert wird, das Wort "Istwert" über die Spalten mit Istdaten gedruckt, und das Wort "Budget" über die Spalten mit Prognosen für das Budget gedruckt. Darüber hinaus wird die Anzahl der Spalten jeden Monat reguliert.

## <a name="apply-column-justification"></a>Anwenden der Spaltenausrichtung
Die Zelle **Begründung** wird verwendet, um die Begründungsformatierung in einem Bericht auf eine Berichtspalte anzuwenden. Diese Option betrifft nur die Spaltenbeschreibungen, nicht die Werte selbst.

1. Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2. Doppelklicken Sie auf die Zelle **Begründung**.
3. Wählen Sie in der Liste einen der folgenden Werte aus:

    - **Keine** - Keine Begründung wird verwendet.
    - **Links** - Richten Sie die Spaltenbeschreibungen links aus.
    - **Mitte** - Zentrieren Sie die Spaltenbeschreibungen.
    - **Rechts** - Richten Sie die Spaltenbeschreibungen rechts aus.

## <a name="add-special-formatting-options"></a>Hinzufügen besonderer Formatierungsoptionen
In der Spaltendefinition wird von den Detailzeilen der Formatierungsspalte eine spezielle Formatierung auf ausgewählte Spalten angewendet. Obwohl einige der Optionen für **Drucksteuerelemente** und **Spalteneinschränkungen** für **FD**-Spalten spezifisch sind, gelten die meisten Optionen für alle Spaltentypen. Die in der Spaltendefinition angegebene Formatierung setzt die Formatierung außer Kraft, die in der Berichtsdefinition angegeben ist. Die in der Zeilendefinition angegebene Formatierung setzt jedoch die Formatierung außer Kraft, die in der Spaltendefinition angegeben ist. Die folgenden Zeilen werden als Formatierungszeilen betrachtet:

- Spaltenbreite
- Zusätzliche Leerzeichen vor Spalte
- Format/Währungsaußerkraftsetzung
- Drucksteuerung

### <a name="changing-the-column-width"></a>Ändern der Spaltenbreite

Die Zelle **Spaltenbreite** gibt die Anzahl der Zeichen an, die für die Breite dieser Spalte im gedruckten Bericht verwendet werden. Spaltenbreite ist für Spalten wichtig, die Beträge (Spalten des Typs **CALC** **WKS** oder **FD** ), Beschreibungen (Spalten des Typs **DESC** ) oder Füllung (Spalten des **AUSFÜLLEN**-Typs) enthalten. Standardmäßig wird die Option **Automatisch anpassen** ausgewählt, damit die Breite jeder Spalte automatisch an den Inhalt angepasst wird.

#### <a name="specify-the-width-of-a-column-on-a-report"></a>Angeben der Breite einer Spalte in einem Bericht

1. Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2. Geben Sie in Zelle **Spaltenbreite** die Anzahl der Stellen für die Spaltenbreite ein. Die maximale Breite einer beliebigen Spalte ist 255 Zeichen (diese Anzahl umfasst Cent, Kommas und Klammern). Wenn Sie alternativ den Bericht-Designer so aktivieren möchten, dass die richtige Breite für die Spalte basierend auf dem Zelleninhalt auswählt wird, klicken Sie doppelt auf die Zelle **Spaltenbreite** und dann auf **Automatisch anpassen**.

### <a name="add-space-between-columns"></a>Leerzeichen zwischen Spalten hinzufügen

Die Zelle **Zusätzliche Leerzeichen vor Spalte** gibt die Breite des Trennzeichens zwischen einer Spalte und benachbarten Spalten in der Spaltendefinition an. Die **Zusätzliche Leerzeichen vor Spalte**-Einstellung bezieht sich alle Spaltendetailzeilen für die Spalte, nicht aber die Spaltenüberschriftzeilen. Verwenden Sie diese Option, um Gruppen von Spalten zu trennen oder um einige Leerzeichen vor der Beschreibung hinzuzufügen, sodass die Beschreibungsspalte gegenüber den linksbündig ausgerichteten Titeln im Bericht eingerückt wird. Die Standardanzahl von Leerzeichen zwischen jeder Spalte beträgt zwei. Sie können diese Einstellung auf der Registerkarte **Einstellungen** in der Berichtsdefinition ändern.

#### <a name="specify-the-space-between-columns"></a>Angeben der Leerzeichen zwischen Spalten

1. Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2. Geben Sie in Zelle **Zusätzliche Leerzeichen vor Spalte** die Anzahl der Stellen an, die zwischen Spalten eingefügt werden soll.

### <a name="specify-a-format-currency-override"></a>Angeben einer Währungsaußerkraftsetzung

Die Zelle **Format/Währungsaußerkraftsetzung** gibt die Formatierung der Dezimalstelle, der Währung und der Prozentsatzbeträge in der Spalte an. Diese Formatierung setzt alle Formatierungen außer Kraft, die in der Berichtsdefinition oder im System angegeben sind.

#### <a name="assign-a-format-currency-override-to-a-report-column"></a>Zuweisen einer Berichtsspalte zu einer Währungsaußerkraftsetzung

1. Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2. Doppelklicken Sie in einer Betragsspalte auf eine Zelle **Format/Währungsaußerkraftsetzung**.
3. Wählen Sie im Dialogfeld **Formataußerkraftsetzung** Formatierungsoptionen aus.

### <a name="add-a-print-control-code"></a>Drucksteuerungscode hinzufügen

Die Zelle **Drucksteuerung** kann Codes enthalten, die die Anzeige oder die Druckmerkmale einer Spalte anpassen. Es gibt zwei Typen Drucksteuerungscodes: reguläre Drucksteuerungscodes und bedingte Drucksteuerungscodes.

#### <a name="regular-print-control-codes"></a>Reguläre Drucksteuerungscodes

| Drucksteuerungscode | Bedeutung                                     | Beschreibung |
|--------------------|-------------------------------------------------|-------------|
| ND                 | Nicht druckbar                                     | Schließen Sie die Beträge in dieser Spalte vom Drucken im Bericht und von Berechnungen aus. Wenn eine nicht druckbare Spalte in einer Berechnung enthalten sein soll, verweisen Sie direkt in der Berechnungsformel auf die Spalte. Beispielsweise ist die nicht druckbare Spalte C in der folgenden Berechnung enthalten: **B+C+D**. Allerdings ist die nicht druckbare Spalte C nicht in der folgenden Berechnung enthalten: **B:D**. |
| XCR                | Vorzeichen in Spalte ändern, wenn der typische Saldo der Zeile ein Habenwert ist | Erstellen Sie ein Budget oder einen Vergleichsbericht, in der bzw. dem eine ungünstige Abweichung (z. B. ein Umsatzdefizit oder eine Kostenüberschreitung) immer negativ ist. Wenden Sie diesen Code auf einer **CALC**-Spalte an, um das Vorzeichen des Spaltenbetrags umzukehren, wenn der typische Saldo einer gegebenen Zeile ein Habenposten ist (wie von einem **C** in der Spalte **Normaler Saldo** der Zeilendefinition gekennzeichnet).<p><strong>Hinweis:</strong> Achten Sie bei <strong>TOT</strong>-Zeilen und </strong>CAL</strong>-Zeilen, die üblicherweise ein Habensaldo enthalten, darauf, ein <strong>C</strong> in der Spalte <strong>Normaler Saldo</strong> in der Zeilendefinition einzugeben.</p> |
| X0                 | Spalte unterdrücken, wenn nur Nullen oder keine Daten enthalten sind          | Schließen Sie eine **FD**-Spalte aus dem Bericht aus, wenn alle Zellen in dieser Spalte entweder leer sind oder Nullen enthalten. |
| RU                 | Runden unterdrücken                               | Verhindern Sie, dass die Beträge in dieser Spalte gerundet werden. |
| XR                 | Rollup unterdrücken                                 | Unterdrücken Sie ein Rollup. Wenn für den Bericht eine Berichtsbaumstruktur verwendet wird, wird für die Beträge in dieser Spalte kein Rollup in nachfolgende übergeordnete Knoten ausgeführt. |
| WDH                 | Spalte auf jeder Seite wiederholen                      | Wiederholen Sie eine angegebene Spalte auf jeder Seite eines Berichts. So können beispielsweise den Drucksteuerungscode **RP** verwenden, um eine Spalte vom Typ **ZEILE** einzubeziehen, der auf jeder Seite Zeilencodes bezieht. |
| TU                 |  Text umbrechen                                      |  Wenn der Text in einer Spalte zu lang ist, führen Sie mit dieser Option ein Textumbruch durch, damit der gesamte Text innerhalb der Spalte angezeigt wird. |

#### <a name="conditional-print-control-codes"></a>Bedingte Drucksteuerungscodes

| Bedingter Drucksteuerungscode | Beschreibung                                                                             |
|--------------------------------|-----------------------------------------------------------------------------------------|
| (keine)                         | Löschen Sie die bedingte Druckauswahl.                                                  |
| P&lt;B                         | Zeigen Sie eine angegebene Spalte nur an, wenn die Periode geringer als der Basiszeitraum ist.             |
| P&gt;B                         | Zeigen Sie eine angegebene Spalte nur an, wenn die Periode länger als der Basiszeitraum ist.             |
| P=B                            | Zeigen Sie eine angegebene Spalte nur an, wenn die Periode gleich dem Basiszeitraum ist.              |
| P&lt;=B                        | Zeigen Sie eine angegebene Spalte nur an, wenn die Periode geringer als oder gleich dem Basiszeitraum ist. |
| P&gt;=B                        | Zeigen Sie eine angegebene Spalte nur an, wenn die Periode länger oder gleich dem Basiszeitraum ist. |

#### <a name="add-print-control-codes-to-a-report-column"></a>Hinzufügen einer Berichtsspalte zu Drucksteuerungscodes

1. Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2. Doppelklicken Sie auf die Zelle **Drucksteuerung**.
3. Wählen Sie im Dialogfeld **Drucksteuerung** einen Code aus der Liste **Drucksteuerungsoptionen auswählen** aus. Um mehr als einen Code auszuwählen, halten Sie die STRG-Taste gedrückt, während Sie die Codes auswählen.
4. Wählen Sie im Feld **Bedingte Druckoptionen** eine Option aus. Standardmäßig ist **(keine)** ausgewählt. Sie können nur jeweils einen bedingten Druckcode auswählen.
5. Klicken Sie auf **OK**.

> [!TIP]
> Sie können die Druckcodes direkt in die Zelle **Drucksteuerung** eingeben. Trennen Sie mehrere Drucksteuerungscodes durch Kommas voneinander.

## <a name="column-types"></a>Spaltentypen
Der Typ der Informationen, die jede Spalte in einem Bericht umfasst, wird vom Wert in der Zeile **Spaltentyp** in der Spaltendefinition angegeben. Jede Spaltendefinition muss mindestens eine Beschreibungsspalte (**BESCHR**) und eine Betragsspalte (**FD**, **AB** oder **KALK**) enthalten.

> [!NOTE]
> Die Spaltentyp-Codes gelten nicht für alle Kontoführungssysteme. Wenn Sie einen für Ihr Kontoführungssystem ungültigen Typ auswählen, wird die Spalte im Bericht leer angezeigt.

### <a name="specify-a-column-type"></a>Angeben eines Spaltentyps

1. Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2. Doppelklicken Sie in der entsprechenden Spalte auf eine Zelle in der Zeile **Spaltentyp**.
3. Wählen Sie in der Liste einen Spaltentyp aus. In der folgenden Tabelle werden die verschiedenen Spaltentypen beschrieben.

    <table>
    <thead>
    <tr>
    <th>Spaltentypcode</th>
    <th>Beschreibung</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>FD</td>
    <td>Zeigen Sie Finanzdaten an, wenn Sie eine <strong>Link zu Finanzdimensionen</strong>-Spalte in der Zeilendefinition verwenden. Wenn Sie den Spaltentyp <strong>FD</strong> auswählen, werden die Standardeinstellungen automatisch in den folgenden Zeilen festgelegt: <ul>
    <li><strong>Buchcode/Attributkategorie:</strong> ISTWERT</li>
    <li><strong>Buchcode/Attributkategorie:</strong> ISTWERT</li>
    <li><strong>Geschäftsjahr:</strong> BASE</li>
    <li><strong>Zeitraum:</strong> BASE</li>
    <li><strong>Abgedeckte Zeiträume:</strong> PERIODIC</li>
    <li><strong>Spaltenbreite:</strong> 14</li>
    </ul>
Diese Standardeinstellungen können geändert werden.</td>
    </tr>
    <tr>
    <td>KALK</td>
    <td>Hier wird das Ergebnis einer einfachen oder komplexen Berechnung angezeigt, die in der Zelle <strong>Formel</strong> angegeben ist. Weitere Informationen finden Sie unter <a href="advanced-formatting-options-financial-reporting.md">Erweiterte Formatierungsoptionen in Finanzberichten</a>.</td>
    </tr>
    <tr>
    <td>DESC</td>
    <td>Zeigen Sie die Zeilenbeschreibung der Zeilendefinition an. Die Beschreibungsspalte ist zwar häufig die erste Spalte im Bericht, kann sich jedoch an einer beliebigen Position befinden.</td>
    </tr>
    <tr>
    <td>ZEILE</td>
    <td>Hier werden einzelne Zeilencodes für Finanzzeilen aus der Spalte <strong>Zeilencode</strong> in der Zeilendefinition angezeigt. Weitere Informationen finden Sie unter <a href="row-definitions-financial-reporting.md">Zeilendefinitionen in Finanzberichten</a>.</td>
    </tr>
    <tr>
    <td>ACCT (Kontocodes)</td>
    <td>Hier werden die Finanzdatensegmentwerte oder Dimensionswerte angezeigt, die für jede Zeile gelten. Für Konto- und Buchungsdetailberichte wird das vollqualifizierte Konto gedruckt (z. B. <strong>110140-070-0101</strong>). Falls in der Spalte <strong>Verknüpfen mit Finanzdimensionen</strong> Bereiche in einer zugeordneten Zeilendefinition festgelegt wurden, wird der Bereich von eckigen Klammern umgeben und als einzelner Wert behandelt (z. B. <strong>[110140:110700]-070-[0101:0200]</strong>). Für Finanzberichte und Übersichtsberichte, die mehrere Konten umfassen, wird der Finanzdatenlink aus der Zeilendefinition gedruckt (z. B. <strong>1100:1200</strong>).</td>
    </tr>
    <tr>
    <td>FÜLL</td>
    <td>Füllen Sie die Zelle mit einem Zeichen, das Sie in einfachen Anführungszeichen angeben. Wenn Sie kein Zeichen eingeben, ist die Spalte leer. Um beispielsweise eine Spalte mit Auslassungspunkten (...) auszufüllen, geben Sie <strong>AUSFÜLLEN</strong> <strong>'.'</strong> ein.</td>
    </tr>
    <tr>
    <td>SEITE</td>
    <td>Fügen Sie einen vertikalen Seitenumbruch in den Bericht ein. Die Spalten rechts neben der <strong>SEITE</strong>-Spalte werden auf einer anderen Seite angezeigt.</td>
    </tr>
    <tr>
    <td>ATTR</td>
    <td>Wenn Ihr Kontoführungssystem die Verwendung von Attributen unterstützt, zeigen Sie ein Konto- oder Buchungsattribut in der Spalte an. Mit einem Attribut, das für ein einzelnes vollständiges Konto gelten muss, werden die zugrunde liegenden Konto- oder Buchungsinformationen aus den Finanzdaten extrahiert. Die Attribute auf Kontoebene zeigen Daten aus dem Konto an, und die Attribute auf Buchungsebene zeigen Daten an, die zum Zeitpunkt der Buchung aufgetreten sind. Wenn Sie <strong>ATTR</strong> als Spaltentyp auswählen, geben Sie in der <strong>Buchcode/Attributkategorie</strong>-Detailzeile der Spaltendefinition die Attributkategorie an.</td>
    </tr>
    </tbody>
    </table>

### <a name="financial-dimensions-column"></a>Spalte „Finanzdimensionen“

Die folgenden **Spaltendefinition**-Zeilendefinitionen gelten für Spalten, mit Spaltentyp **FD** (Beträge von den Finanzdimensionen).

#### <a name="book-codeattribute-category-cell"></a>Zelle Buchcode/Attributkategorie

Die Zelle **Buchcode/Attributkategorie** bestimmt den Buchcode für die Daten in der Spalte **FD**. Eine Spaltendefinition kann mehrere Ist-, Budget- und Statistikspalten enthalten. Eine Spaltendefinition kann auch unterschiedliche Zeiträume (z. B. aktuell oder Jahr bis dato) sowie unterschiedliche Beträge anzeigen. Die Liste der Buchcodes spiegelt das tatsächlichen, Budget- und statistischen (nicht wertmäßigen) Optionen wieder, die in den Finanzdaten eingerichtet worden sind.

#### <a name="fiscal-year-cell"></a>Zelle Geschäftsjahr

Die Zelle **Geschäftsjahr** identifiziert das Geschäftsjahr, das in der Spalte enthalten sein soll. Das Jahr kann relativ zum Basisjahr sein, das beim Generieren des Berichts angegeben wird. Die folgenden Optionen sind verfügbar.

| Option  | Beschreibung                                                                                                                  |
|---------|------------------------------------------------------------------------------------------------------------------------------|
| BASIS    | Verwenden Sie das Basisjahr, das zum Zeitpunkt des Berichts angegeben wird.                                                                          |
| BASE+\# | Verwenden Sie das \# Jahr nach dem Basisjahr. Wenn Sie also beispielsweise das dritte Jahr nach dem Basisjahr verwenden, geben Sie **BASIS+3** ein. |
| BASE-\# | Verwenden Sie das \# Jahr, vor dem Basisjahr. Wenn Sie also beispielsweise das Vorjahr verwenden, geben Sie **BASIS-1** ein.                 |
| \#      | Geben Sie das tatsächliche Geschäftsjahr ein.                                                                                                |

#### <a name="period-cell"></a>Periodenzelle

Die Zelle **Periode** identifiziert die Geschäftsperioden, die in der Spalte enthalten sein sollen. Der Zeitraum kann relativ zum Basiszeitraum sein, der beim Generieren des Berichts angegeben wird. Die folgenden Optionen sind verfügbar.

| Mit der folgenden Option...          | Beschreibung |
|-----------------|-------------|
| BASIS            | Verwenden Sie den Basiszeitraum. |
| BASE+\#         | Verwenden Sie die \# Periode, nach der Basisperiode. Wenn Sie also beispielsweise die dritte Periode nach der Basisperiode verwenden, geben Sie **BASIS+3** ein. |
| BASE-\#         | Verwenden Sie die \# Periode, vor der Basisperiode. Wenn Sie also beispielsweise die vorherige Periode verwenden, geben Sie **BASIS-1** ein. |
| BASE-\#:BASE    | Verwenden Sie mehrere Perioden, aus mehreren Perioden vor der Basisperiode durch die Basisperiode. Um beispielsweise die drei vorangegangenen Perioden und die Basisperiode zu verwenden, geben Sie **BASIS-3: BASIS** ein. |
| BASE:BASE+\#    | Verwenden Sie mehrere Perioden, aus mehreren Basisperioden durch mehrere Perioden nach der Basisperiode. Um beispielsweise die Basisperiode und die folgenden zwei Perioden zu verwenden, geben Sie **BASIS: BASIS+2** ein. |
| BASE-\#:BASE+\# | Verwenden Sie mehrere Perioden, aus mehreren Perioden vor der Basisperiode bis zu mehreren Perioden nach der Basisperiode. Um beispielsweise die drei vorangegangenen Perioden, die Basisperioden und die folgenden zwei Perioden zu verwenden, geben Sie **BASIS-3: BASIS+2** ein. |
| 1:BASE          | Verwenden Sie mehrere Perioden, aus der ersten Periode durch die Basisperiode. |
| \#              | Verwenden Sie immer eine bestimmte Periodenanzahl. Es wird nicht empfohlen, diese Option zu verwenden, da sie die Flexibilität der Spaltendefinition verringert. |
| \#:\#           | Verwenden Sie immer einen bestimmten Periodenbereich. Es wird nicht empfohlen, diese Option zu verwenden, da sie die Flexibilität der Spaltendefinition verringert. |

Sie können bei jeder Zeitraumangabe Geschäftsjahresabgrenzungen überschreiten und mehrere Jahre in einem Zeitraumbereich kombinieren. Definieren Sie zum Beispiel die Perioden als **BASE-5** (um die letzten sechs Zeiträume anzuzeigen) und führen Sie einen Bericht aus, der einen Basiszeitraum von 2 Perioden hat. In diesem Fall enthält der Bericht die Daten für die ersten beiden Zeiträume des angegebenen Geschäftsjahrs und die letzten vier Zeiträume des vorherigen Geschäftsjahrs.

### <a name="specify-the-periods-for-an-fd-column"></a>Angeben der Zeiträume für eine FD-Spalte

1. Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2. Doppelklicken Sie in einer **FD**-Spalte auf die Zelle in der Zeile **Periode**, und wählen Sie dann in der Liste eine Option aus.
3. Schließen Sie die Formel in der Formelleiste über dem Navigationsbereich oder in der Zelle **Periode** ab. Ersetzen Sie ein beliebiges Nummernzeichen (\#) durch den entsprechenden Wert.

#### <a name="periods-covered-cell"></a>Zelle "Abgedeckte Perioden"

Die Zelle **Abgedeckte Perioden** identifiziert den Betrag, der in der Spalte angezeigt werden soll. Dieser Betrag ist relativ zum Wert in den Zellen **Geschäftsjahr** und **Periode** für die Spalte. Die folgenden Optionen sind verfügbar.

| Option      | Beschreibung                                                                 |
|-------------|-----------------------------------------------------------------------------|
| PERIODIC    | Zeigen Sie die Summe der Aktivitäten für den aktuellen Zeitraum oder Zeitraumbereich an. |
| PERIODIC/BB | Zeigen Sie den Anfangssaldo für den aktuellen Zeitraum oder Zeitraumbereich an.   |
| Jahr bis dato         | Zeigen Sie die Summe der Aktivitäten des Jahres bis dato an.                               |
| YTD/BB      | Zeigen Sie den Anfangssaldo für das Jahr an.                                 |

### <a name="specify-the-periods-that-are-covered-for-an-fd-column"></a>Angeben der abgedeckten Zeiträume für eine FD-Spalte

1. Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2. Doppelklicken Sie in einer **FD**-Spalte auf die Zelle in der Zeile **Abgedeckte Perioden**, und wählen Sie in der Liste eine Option aus.

### <a name="attribute-filter-in-a-column-definition"></a>Attributfilter in einer Spaltendefinition

Attribute sind Finanzdatenwerte, die ein Konto oder eine Buchung näher definieren. Die Kontoattribute umfassen **Anlage**, **Verbindlichkeiten**, **Umsatzerlös** und **Ausgaben**. Die Transaktionsattribute sind **Buchungsbeschreibung** und **Anwendungsdatum der Buchung**. Die Attributunterstützung unterscheidet sich möglicherweise zwischen den verschiedenen Microsoft Dynamics ERP-Systemen. Die **Attributfilter**-Zelle beschränkt die Daten in den **FD**-Spalten auf bestimmte Werte oder Bereiche für Attributkategorien. Obwohl diese Funktion zusammen mit einer **ATTR**-Spalte verwendet werden kann, ist die **ATTR**-Spalte nicht erforderlich. In einer **FD**-Spalte gibt es eine Grenze für den Konten oder Transaktionen, die der Bericht aus dem Attributfilter umfasst.

> [!NOTE]
> Informationen zu den von Ihrem ERP-System unterstützten Attributen finden Sie im Integrationshandbuch für Ihr System.

#### <a name="apply-an-attribute-filter-for-an-fd-column-on-a-report"></a>Anwenden eines Attributfilters für eine FD-Spalte in einem Bericht

1. Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2. Doppelklicken Sie auf die Zelle **Attributfilter** für eine **FD**-Spalte.
3. Doppelklicken Sie im Dialogfeld **Attributfilter** in die Spalte **Attribut**, und wählen Sie dann den Filtertyp aus.
4. Wenn Sie die Ergebnisse weiter einzuschränken möchten, geben Sie in den Spalten und **Von** und **Bis** einen Bereich ein. Das Feld **Von** muss einen positiven Wert enthalten.
5. Klicken Sie auf **OK**.

#### <a name="example-of-an-attribute-filter"></a>Beispiel eines Attributfilters

Im folgenden Beispiel wird ein Teil einer Spaltenbeschreibung angezeigt, die ein Kontoattribut in der Zeile hat **Buchcode/Attributkategorie** aufweist. Der Attributfilter für diese Spalte gibt den Wertebereich an, der im Bericht berücksichtigt werden soll.

|                              | K    | B                   |
|------------------------------|------|---------------------|
| Spaltentyp                  | BESCHR | FD                  |
| Buchcode/Attributkategorie |      | ISTWERT              |
| Geschäftsjahr                  |      | BASE                |
| Zeitraum                       |      | 1:BASE              |
| Abgedeckte Zeiträume              |      | PERIODISCH            |
| ...                          |      |                     |
| Spaltenbreite                 | 30   |                     |
| ...                          |      |                     |
| Attributfilter             |      | Referenz=\[01:10\] |

### <a name="dimension-filter-in-a-column-definition"></a>Dimensionsfilter in einer Spaltendefinition

Ein Dimensionsfilter wird verwendet, um die Spalte **FD** auf bestimmte Dimensionswerte einzuschränken. Der Filter kann eine einzelne Dimension, einen Bereich von Dimensionen oder eine Gruppe von Dimensionen enthalten. Der Filter kann auch Dimensionswertsätze enthalten. Da Dimensionswerte variieren können, muss ein ..\\financial-dimensions\\dimension-based System nicht einer genauen Länge entsprechen. Der Filter wird unabhängig davon angewendet, ob der Bericht die Berichtsbaumstruktur umfasst. Sie können in jeder Position ein Platzhalterzeichen (\* oder ?) verwenden. Wenn Sie mehrere Konten angeben, setzen Sie ein Komma zwischen die Konten. Beispiel: +Konto=\[1200\]+Konto=\[1100\], Abteilung=\[01?\] Um alle Abteilungen für ein bestimmtes Konto zu erhalten, können Sie die Abteilungsdimension aus dem Dimensionsfilter ausschließen. Beispielsweise werden die folgenden Dimensionsfilter auf dieselbe Weise behandelt:

- +Konto=\[1100\],Abteilung
- +Konto=\[1100\]

Sie können eine beliebige Kombination von alphanumerischen Zeichen für genaue Treffer verwenden, und Sie können Teildimensionen definieren. Beispielsweise umfasst **Standort = \[10\*\]** alle Standortdimensionswerte, die mit 10 beginnen.

#### <a name="apply-a-dimension-filter-for-a-column-on-a-report"></a>Anwenden eines Dimensionsfilters für eine Spalte in einem Bericht

1. Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2. Doppelklicken Sie auf die Zelle **Dimensionsfilter** für eine **FD**-Spalte.
3. Geben Sie im Dialogfeld **Dimensionen** die Filter ein, die angewendet werden sollen.
4. Klicken Sie auf **OK**.

### <a name="format-a-multiple-currency-report-in-a-column-definition"></a>Formatieren eines Berichts für mehrere Währungen in einer Spaltendefinition

In einem Bericht mit mehreren Währungen können Beträge in der Buchhaltungswährung des Sachkontos, den Berichten des Sachkontos, der ursprünglichen Buchungswährung oder der umgerechneten Berichtswährung angezeigt werden. Die Kontowährung eines Unternehmens wird in der Sachkontoeinrichtung definiert. Verwechseln Sie diese Einstellung nicht mit den Optionen für die regionale Einstellung des Betriebssystems, in denen Sie die Währungssymbole auswählen können, die standardmäßig in Berichten verwendet werden. Die folgenden währungsbezogenen Zellen sind in der Spaltendefinition verfügbar:

- **Währungs-Anzeige** – Geben Sie die Art der Währung an (Konto-, Berichts-, Transaktions- oder umgerechnete Berichtswährung), in der die Buchungen angezeigt werden. Die Umrechnung in eine Berichtswährungsfunktion wird gelegentlich als Währungsumrechnung bezeichnet. Hierbei handelt es sich um die Möglichkeit, Berichte für Hauptbuchbeträge in einer Währung zu erstellen, bei der es sich möglicherweise nicht um die funktionale oder Berichtswährung des Unternehmens und auch nicht um die Währung handelt, in der die Transaktion eingegeben wurde.
- **Währungsfilter** - Geben Sie einen Währungsfilter an. Nur Transaktionen, die in der ausgewählten Währung eingegeben werden, werden im Bericht angezeigt.

> 
Gehen Sie folgendermaßen vor, um die Buchungswährung eines Unternehmens festzulegen.

1. Klicken Sie im Berichts-Designer im Menü **Unternehmen** auf **Unternehmen**.
2. Wählen Sie im Dialogfeld **Unternehmen** ein Unternehmen aus, und klicken Sie anschließend auf **Anzeigen**.
3. Im Dialogfeld **Unternehmen anzeigen** unter **Regionale Optionen** können Sie die Währung anzeigen, die für das ausgewählte Unternehmen definiert ist.

#### <a name="specify-the-currency-on-a-multiple-currency-report"></a>Angeben der Währung in einem Bericht mit mehreren Währungen

1. Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2. Doppelklicken Sie auf die Zelle **Wähungsanzeige** in der entsprechenden **FD**-Spalte, und wählen Sie dann die Option für das Anzeigen von Währungsinformationen aus: **Sachkontowährung**, **Sachkontobericht**, Transaktionswährung oder wählen Sie die Umrechnung in eine andere Berichtswährung aus.
3. Doppelklicken Sie auf die Zelle **Währungsfilter** in der entsprechenden **FD**-Spalte, und wählen Sie dann den entsprechenden Währungscode in der Liste aus. Es werden nur Transaktionen im Bericht angezeigt, die in dieser Währung eingegeben werden.


### <a name="example-for-currency-display-and-currency-filter-cells"></a>Beispiel für Währungsanzeige und Währungsfilterzellen

Phyllis hat die folgende Auswahl für die Währung in der Spaltendefinition getroffen:

- **Währungsfilter:** Yen
- **Währungsanzeige:** Buchungswährung des Sachkontos (US-Dollar)

Basierend auf dem von Phyllis ausgewählten Währungsfilter enthält der Bericht nur Transaktionen, die in japanischen Yen (JPY) eingegeben wurden. Basierend auf ihrer ausgewählten Währungsanzeige zeigt der Bericht diese Transaktionen in der Buchungswährung US-Dollar (USD) an.

#### <a name="currency-filter-and-currency-display-combinations"></a>Kombinationen aus Währungsfilter und Währungsanzeige

In der folgenden Tabelle werden die Berichtsergebnisse aufgelistet, die aufgrund der von Phyllis getroffenen Auswahl für verschiedene Kombinationen der Optionen in den Zellen **Währungsanzeige** und **Währungsfilter** auftreten können. Die funktionale Währung ist USD.


| Zelle Währungsanzeige                        | Zelle Währungsfilter | Berichtsergebnis |
|----------------------------------------------|----------------------|---------------|
| Buchungswährung                 | **YEN**              | **Y6.000** - Das Ergebnis zeigt nur Buchungen an, die in JPY eingegeben wurden. |
| Buchhaltungswährung des Sachkontos | **YEN**              |**$60** - Das Ergebnis zeigt nur die Transaktionen, die in JPY eingegeben wurden zeigt diese Transaktionen in USD an.<p><strong>Hinweis:</strong> Der Wechselkurs ist ungefähr 100 JPY pro USD.</p> |
| Buchhaltungswährung des Sachkontos | Leer                | **$2.310** - Das Ergebnis zeigt alle Daten in der Buchungswährung an, die im Sachkonto angegeben sind.<p><strong>Hinweis:</strong> Dieser Betrag ist die Summe aller Transaktionen in der Buchhaltungswährung.</p> |
| Buchungswährung                 | Leer                | **$2.250** - Das Ergebnis zeigt alle Beträge in der Währung an, in der die Transaktion ausgeführt wurde. Das bedeutet, dass die Summe errechnet sich aus den Beträgen verschiedener Währungen. |

### <a name="calculation-column-in-a-column-definition"></a>Berechnungsspalte in einer Spaltendefinition

Ein **CALC** Spaltentyp in einer Spaltendefinition unterstützt komplexe Berechnungen in der **Formel** Zelle und kann **+**, **-**, **\***, und **/** Operatoren, und auch **IF/THEN/ELSE** Aussagen enthalten. Eine Berechnungsspalte kann auf jede beliebige andere Spalte auch auf nachfolgende Spalten verweisen. Dazu kann eine Berechnungsspalte das Geschäftsjahr und die Periode enthalten, um Überschriften für die Spalte zu unterstützen. Die Berechnungsformel kann bis zu 1024 Zeichen lang sein. Verwenden Sie eine spezielle Formatüberschreibung, um das Ergebnis der Berechnung in Prozent auszudrücken.

> [!NOTE]
> In den Ergebnissen von Berechnungsformeln werden keine Werte in nicht druckbaren Spaltenbereichen berücksichtigt. Beispielsweise **A:D** druckt **0** (null), wobei **A+B+C** für nicht druckbare Werte den Wert berechnet.

#### <a name="operators-in-calculation-columns"></a>Operatoren in Berechnungsspalten

Zum Addieren, Subtrahieren, Multiplizieren oder Teilen von Spalten geben Sie die Buchstaben der Spalte in der Reihenfolge der Berechnung ein und verwenden dann den entsprechenden Operator, um die Spaltenbuchstaben voneinander zu trennen. In der folgenden Tabelle werden die Operatoren beschrieben, die Sie in einer Berechnungsspalte verwenden können.

| Bediener | Beispielberechnung | Beschreibung |
|----------|---------------------|-------------|
| +        | A+C                 | Addieren Sie den Betrag in Spalte A zum Betrag in der Spalte C. |
| :        | A:C A:C-D           | Addieren Sie einen Bereich aufeinanderfolgender Spalten. Beispielsweise addiert die **A:C**-Formel die Summen der Spalten A bis C, und die Formel **A:C-D** addiert die Summen der Spalten A bis C und subtrahiert anschließend den Betrag in der Spalte D. |
| -        | A-C                 | Subtrahieren Sie den Betrag in Spalte C vom Betrag in Spalte A.<p><strong>Hinweis:</strong> Sie können auch das Minuszeichen (-) verwenden, um die Vorzeichen in einer Spalte umzukehren. Verwenden Sie beispielsweise <strong>- A+B</strong>, um den umgekehrten Betrag in Spalte A zum Betrag in der Spalte B zu addieren.</p> |
| \*       | A\*C                | Multiplizieren Sie den Betrag in Spalte A mit dem Betrag in der Spalte C. |
| /        | A/C                 | Dividieren Sie den Betrag in Spalte A durch den Betrag in der Spalte C. |

#### <a name="use-a-calculation-formula-in-a-column-definition"></a>Verwenden einer Berechnungsformel in einer Spaltendefinition

1. Öffnen Sie die zu ändernde Spaltendefinition im Berichts-Designer.
2. Geben Sie in der entsprechenden **CALC**-Spalte eine Formel in der Zelle **Formel** ein.

#### <a name="complex-calculations"></a>Komplexe Berechnungen

Eine komplexe Berechnung kann eine beliebige Kombination von Zellbezügen, Operatoren, Werten und Ebenen geschachtelter Klammern enthalten. Um beispielsweise den Durchschnitt der Spalten A und B zu berechnen, verwenden Sie die Berechnungsformel **((A+B)/2)**.

#### <a name="specify-report-cells-in-a-column-calculation"></a>Angeben von Berichtszellen in einer Spaltenberechnung

Sie können auf eine bestimmte Berichtszelle verweisen, indem Sie einen Spaltenbuchstaben und einen Zeilencode eingeben. Beispielsweise bezieht sich **B.100** auf Zeilencode 100 in der Spalte B. Sie können eine vollständige Spalte durch einen bestimmten Berichtszellenbetrag dividieren, der in der gleichen Spalte ist. Die Berechnung **B/B.100** bedeutet beispielsweise, dass der Betrag in der Spalte B durch den Wert in Zeilencode 100 in der Spalte B dividiert werden soll. Wenn die Berechnung auf eine Spalte verweist, die von einer anderen Spalte abhängt, wird die abhängige Spalte zuerst aufgelöst. Wenn Sie in einer Spalte auf eine andere Spalte verweisen, die wiederum zurück auf die erste Spalte verweist, führt dies zu einem Zirkelverweisfehler.

> [!NOTE]
> Diese Berechnung ist möglicherweise falsch, wenn Sie die Berechnungspriorität für den Bericht ändern. Sie können die Berechnungspriorität auf der Registerkarte **Einstellungen** der Berichtsdefinition festlegen.

#### <a name="multiply-or-divide-a-column-by-a-base-row"></a>Multiplizieren oder Teilen einer Spalte mit/durch eine(r) Basiszeile

Sie können eine Spalte erstellen, in der alle Werte in einer angegebenen Spalte als Prozentsatz einer Basiszahl angezeigt werden. Damit verfügen Sie über eine Methode, um Beziehungen zwischen Zeilen darzustellen, z. B. einen Prozentsatz einer Zeile mit Umsätzen oder mit Gesamtausgaben. Um jede Zeile in einer bestimmten Spalte mit einer Basiszeile zu multiplizieren oder zu dividieren, geben Sie die zu verwendeten Spalte in die Berechnung ein und geben Sie anschließend **\*BASEROW** oder **/BASEROW** ein. Geben Sie **C\*BASEROW** or **C/BASEROW**.

> [!NOTE]
> Wenn Sie in einer Spaltendefinition eine Basiszeilenberechnung verwenden, muss jede Zeilendefinition, die mit dieser Spaltendefinition verwendet wird, mindestens eine Basiszeile für Berechnungen enthalten.

#### <a name="divide-the-amount-in-a-column-by-the-number-of-periods"></a>Teilen des Betrags in der Spalte durch die Anzahl der Zeiträume

Sie können den Betrag in einer Spalte durch eine angegebene Anzahl von Zeiträumen dividieren. Beispielsweise dividiert die Formel **B/Perioden** den Wert in der Spalte B durch die Anzahl der Perioden in der Spalte B. Wenn die Berechnung mehrere Spalten umfasst, geben Sie die Anzahl der Perioden an, die bei der Berechnung verwendet werden sollen. Beispielsweise addiert die Formel **(B+C)/Perioden** die Beträge in der Spalte B und in der Spalte C und dividiert dann das Ergebnisses durch den Periodenwert.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Zeilendefinitionen in der Finanzberichterstellung](row-definitions-financial-reporting.md)

[Erweiterte Formatierungsoptionen in der Finanzberichterstellung](advanced-formatting-options-financial-reporting.md)
