---
title: Gruppieren Sie Datensätze und aggregieren Sie Berechnungen mit Hilfe von GROUPBY Datenquellen
description: In diesem Thema wird erklärt, wie Sie Datenquellen vom Typ GROUPBY im elektronischen Berichtswesen (ER) verwenden können.
author: NickSelin
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a6cdc486c5f799bdedafa38e90be989fd328c96
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075621"
---
# <a name="group-records-and-aggregate-calculations-by-using-groupby-data-sources"></a>Gruppieren Sie Datensätze und aggregieren Sie Berechnungen mit Hilfe von GROUPBY Datenquellen

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

Bei der Konfiguration von [Electronic Reporting (ER)](general-electronic-reporting.md) Modell-Zuordnungen oder -Formaten können Sie [erforderliche Datenquellen vom Typ **GroupBy** hinzufügen](#AddMmDataSource2).

Zur Designzeit wird eine **GroupBy** Datenquelle konfiguriert, um die folgenden Elemente zu identifizieren:

- Eine [Basisdatenquelle](#BaseDataSource), die Datensätze enthält, die zur Laufzeit gruppiert werden
- [Gruppierungsfelder](#GroupingFields) der Basisdatenquelle, die für die Gruppierung der Datensätze zur Laufzeit verwendet werden
- [Aggregatfunktionen](#AggregateFunctions), die die aggregierten Berechnungen angeben, die für jede ermittelte Gruppe zur Laufzeit durchgeführt werden

Zur Laufzeit gruppiert eine konfigurierte **GroupBy** Datenquelle Datensätze, die die gleichen Werte in den Gruppierungsfeldern haben, und gibt dann eine Liste von Datensätzen zurück. Jeder Datensatz steht für eine einzelne Gruppe. Für jede Gruppe zeigt die Datenquelle die Feldwerte an, nach denen die ursprünglichen Datensätze gruppiert wurden, die Werte der berechneten Aggregatfunktionen und die Liste der Datensätze der Basisdatenquelle, die zu der Gruppe gehören.

## <a name="aggregate-functions"></a><a name="AggregateFunctions"></a>Funktionen gruppieren

Zur Laufzeit wird jede Aggregatberechnung für jede Gruppe von Datensätzen durchgeführt. Diese Berechnung erfolgt anhand des Wertes eines einzelnen Feldes oder eines Ausdrucks in den Datensätzen einer Datenquelle, die für die Gruppierung in der bearbeitbaren Datenquelle vom Typ **GroupBy** ausgewählt wurde. Die folgenden Aggregatfunktionen werden derzeit unterstützt:

- **AVG** - Diese Funktion gibt den Durchschnitt der Werte in einer Gruppe zurück. Sie kann nur mit numerischen Feldern verwendet werden.
- **COUNT** - Diese Funktion gibt die Anzahl der Artikel zurück, die in einer Gruppe gefunden wurden.
- **Min** - Diese Funktion gibt den Mindestwert unter den Werten einer Gruppe zurück.
- **Max** - Diese Funktion gibt den Maximalwert unter den Werten in einer Gruppe zurück.
- **SUM** - Diese Funktion gibt die Summe aller Werte in einer Gruppe zurück. Sie kann nur mit numerischen Feldern verwendet werden.

## <a name="execution-location"></a><a name="ExecutionLocation"></a>Ausführungsstandort

Wenn Sie eine **GroupBy** Datenquelle bearbeiten und die Basisdatenquelle angeben, die die Datensätze enthält, die gruppiert werden müssen, erkennt das System automatisch den effizientesten [Ort](#ExecutionLocation) für die Ausführung dieser **GroupBy** Datenquelle. Wenn die Basisdatenquelle [abfragbar](er-functions-list-filter.md#usage-notes) ist (d.h. wenn sie auf Datenbankebene ausgeführt werden kann), wird die Anwendungsdatenbank auch als Ausführungsort der editierbaren **GroupBy**-Datenquelle angegeben. Andernfalls wird der Speicher des Anwendungsservers als Ausführungsort angegeben.

Sie können den automatisch erkannten Ausführungsort manuell ändern, indem Sie den Ort auswählen, der für die konfigurierte Datenquelle gilt. Wenn der ausgewählte Ausführungsort nicht zutreffend ist, wird zur Entwurfszeit ein [Validierungsfehler](er-components-inspections.md#i5) ausgegeben.

> [!TIP]
> Wir empfehlen Ihnen, den Datenbankstandort zu verwenden, um Datenquellen zu gruppieren, die eine große Anzahl von Datensätzen offenlegen.

## <a name="memory-consumption"></a><a name="MemoryConsumption"></a>Speicherverbrauch

Wenn eine **GroupBy**-Datenquelle im Speicher ausgeführt wird, wird standardmäßig der Speicher des Anwendungsservers verwendet, um Datensätze der Basisdatenquelle, die zu jeder entdeckten Gruppe gehören, als Datensätze einer einzelnen Gruppe zu speichern. Um den Speicherverbrauch zu reduzieren, können Sie die Speicherung von Datensätzen für **GroupBy**-Datenquellen unterdrücken, wenn diese so konfiguriert wurden, dass nur aggregierte Funktionen berechnet werden und die Datensätze ihrer Gruppe zur Laufzeit nicht verwendet werden. Um den Speicherverbrauch auf diese Weise zu reduzieren, aktivieren Sie im Arbeitsbereich **Funktionsverwaltung** die Funktion **Speicherverbrauch in ER reduzieren, wenn die Gruppierung von Datensätzen nur zum Berechnen von Aggregationen verwendet wird**.

## <a name="alternatives"></a><a name="Alternatives"></a>Alternativen

Ähnliche Aggregationen können mit [verschiedenen](er-data-collection-data-sources.md#if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions) Arten von Datenquellen oder mit den integrierten Funktionen von ER berechnet werden.

Um mehr über diese Funktion zu erfahren, führen Sie das folgende Beispiel aus.

## <a name="example-use-a-groupby-data-source-for-aggregate-calculations-and-record-grouping"></a><a name="Example"></a>Beispiel: Verwendung einer GROUPBY-Datenquelle für Aggregatberechnungen und Gruppierung von Datensätzen

Dieses Beispiel zeigt, wie ein Benutzer in der Rolle Systemadministrator oder Funktionsberater für elektronisches Reporting eine ER-Model-Zuordnung konfigurieren kann, die eine **GROUPBY**-Datenquelle enthält, die zur Berechnung von Aggregatfunktionen und Gruppendatensätzen verwendet wird. Diese Modellzuordnung wird verwendet, um den Steuerbericht zu drucken, wenn die Intrastat-Meldung erstellt wird. Mit diesem Bericht können Sie die gemeldeten Intrastat-Transaktionen überprüfen.

Die Vorgänge in diesem Beispiel können in der Firma **DEMF** in Microsoft Dynamics 365 Finance abgeschlossen werden. 

### <a name="prepare-sample-data"></a>Vorbereiten von Beispieldaten

Vergewissern Sie sich, dass Sie Intrastat-Transaktionen für die Berichterstattung auf der Seite **Intrastat** haben. Sie müssen über Transaktionen für verschiedene Transportcodes verfügen, da Sie in diesem Beispiel Transaktionen nach dem Feld **Transport** gruppieren werden.

![Vorbereiten von Intrastat-Transaktionen auf der Seite Intrastat.](./media/er-groupby-data-sources-prepare-transactions.png)

### <a name="configure-the-er-framework"></a>Konfigurieren des EB-Frameworks

Befolgen Sie die Schritte in [ER-Framework konfigurieren](er-quick-start2-customize-report.md#ConfigureFramework), um den minimalen Satz von ER-Parametern einzurichten. Sie müssen diese Einrichtung abschließen, bevor Sie mit dem ER-Framework eine ER-Model-Zuordnung entwerfen können.

### <a name="import-the-standard-er-format-configuration"></a>Die standardmäßige ER-Formatkonfiguration importieren

Befolgen Sie die Schritte in [ER-Standard-Formatkonfiguration importieren](er-quick-start2-customize-report.md#ImportERSolution1), um die ER-Standardkonfigurationen Ihrer aktuellen Instanz von Dynamics 365 Finance hinzuzufügen. Importieren Sie Version 1 der **Intrastat-Modell** Konfiguration aus dem Repository.

### <a name="create-a-custom-data-model-configuration"></a>Erstellen Sie eine angepasste Datenmodellkonfiguration

Führen Sie die Schritte unter [Hinzufügen einer angepassten Datenmodellkonfiguration](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) aus, um manuell eine neue **Intrastat-Modell (Litware)** ER-Datenmodellkonfiguration hinzuzufügen, die Sie aus der importierten **Intrastat-Modell**-Konfiguration ableiten.

### <a name="configure-a-custom-data-model-component"></a>Konfigurieren Sie eine angepasste Datenmodellkomponente

Führen Sie diese Schritte aus, um die erforderlichen Änderungen am abgeleiteten **Intrastat-Modell (Litware)** Datenmodell vorzunehmen, sodass es verwendet werden kann, um Transportcodes mit den erforderlichen Details freizulegen.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Intrastat-Modell (Litware)**.
3. Wählen Sie **Designer** aus.
4. Wählen Sie auf der Seite **Datenmodell-Designer** im Modellbaum **Intrastat**.
5. Wählen Sie **Neu**, um einen neuen verschachtelten Knoten für den ausgewählten **Intrastat**-Knoten hinzuzufügen. Führen Sie im Dropdown-Dialogfeld zum Hinzufügen eines Datenmodellknotens die folgenden Schritte aus:

    1. Geben Sie in das Feld **Name** **Transport** ein.
    2. Wählen Sie im Feld **Artikeltyp** **Datensatzliste** aus.
    3. Wählen Sie zum Hinzufügen des neuen Knotens **Hinzufügen** aus.

6. Wählen Sie **Neu**, um einen neuen verschachtelten Knoten für den Knoten **Transport** hinzuzufügen, den Sie gerade hinzugefügt haben. Führen Sie im Dropdown-Dialogfeld zum Hinzufügen eines Datenmodellknotens die folgenden Schritte aus:

    1. Geben Sie in das Feld **Name** den **Code** ein.
    2. Wählen Sie im Feld **Artikeltyp** **Zeichenfolge** aus.
    3. Wählen Sie zum Hinzufügen des neuen Knotens **Hinzufügen** aus.

7. Wählen Sie **Neu**, um einen weiteren neuen verschachtelten Knoten für den Knoten **Transport** hinzuzufügen. Führen Sie im Dropdown-Dialogfeld zum Hinzufügen eines Datenmodellknotens die folgenden Schritte aus:

    1. Geben Sie in das Feld **Name** **TotalInvoicedAmount** ein.
    2. Wählen Sie im Feld **Artikeltyp** **Gleitkommazahl** aus.
    3. Wählen Sie zum Hinzufügen des neuen Knotens **Hinzufügen** aus.

8. Wählen Sie **Neu**, um einen weiteren neuen verschachtelten Knoten für den Knoten **Transport** hinzuzufügen. Führen Sie im Dropdown-Dialogfeld zum Hinzufügen eines Datenmodellknotens die folgenden Schritte aus:

    1. Geben Sie in das Feld **Name** **NumberOfTransactions** ein.
    2. Wählen Sie im Feld **Artikeltyp** die Option **Integer** aus.
    3. Wählen Sie zum Hinzufügen des neuen Knotens **Hinzufügen** aus.

9. Wählen Sie **Neu**, um einen weiteren neuen verschachtelten Knoten für den Knoten **Transport** hinzuzufügen. Führen Sie im Dropdown-Dialogfeld zum Hinzufügen eines Datenmodellknotens die folgenden Schritte aus:

    1. Geben Sie in das Feld **Name** **Transaktion** ein.
    2. Wählen Sie im Feld **Artikeltyp** **Datensatzliste** aus.
    3. Wählen Sie zum Hinzufügen des neuen Knotens **Hinzufügen** aus.

10. Für den Knoten **Transaktion**, den Sie gerade hinzugefügt haben, wählen Sie auf der Registerkarte **Knoten** Inforegister **Artikelreferenz wechseln**.
11. Wählen Sie im Dialogfeld **Elementreferenz wechseln** in der Datenmodellstruktur **CommodityRecord**. Wählen Sie dann **OK** aus.

![Konfiguriertes Datenmodell im EB-Datenmodelldesigner.](./media/er-groupby-data-sources-configure-data-model.png)

### <a name="complete-the-design-of-a-custom-data-model"></a>Vervollständigen Sie den Entwurf eines angepassten Datenmodells

Folgen Sie den Schritten unter [Entwurf des Datenmodells vervollständigen](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration), um den Entwurf des abgeleiteten **Intrastat Modells (Litware)** Datenmodells zu vervollständigen.

### <a name="create-a-new-model-mapping-configuration"></a>Erstellen einer neuen Modellzuordnungskonfiguration

Folgen Sie den Schritten in [Erstellen Sie eine neue Modellzuordnungskonfiguration](er-quick-start1-new-solution.md#CreateModelMapping), um manuell eine neue **Intrastat-Musterzuordnung** ER-Modellzuordnungskonfiguration für die abgeleitete **Intrastat-Modell (Litware)**-Konfiguration zu erstellen.

### <a name="add-a-new-model-mapping-component"></a>Hinzufügen einer neuen Komponente für die Zuordnung von Modellen

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** im Konfigurationsbaum die Konfiguration **Intrastat-Modell**.
3. Wählen Sie die Konfiguration **Intrastat Musterzuordnung**.
4. Wählen Sie **Designer** aus, um die Liste der Zuordnungen zu öffnen.
5. Wählen Sie **Löschen**, um die vorhandene Zuordnung zu entfernen.
6. Wählen Sie **Neu**, um eine neue Zuordnungskomponente hinzuzufügen.
7. Im Feld **Definition** wählen Sie **Intrastat**.
8. Geben Sie in das Feld **Name** **Intrastat-Zuordnung** ein.
9. Wählen Sie **Designer**, um die neue Zuordnung zu konfigurieren.

### <a name="design-the-added-model-mapping-component"></a>Entwerfen Sie die hinzugefügte Komponente zur Modellzuordnung

#### <a name="add-a-data-source-to-access-an-application-table"></a><a name="AddMmDataSource1"></a>Hinzufügen einer Datenquelle für den Zugriff auf eine Anwendungstabelle

Konfigurieren Sie eine Datenquelle für den Zugriff auf die Anwendungstabellen, die die Details der Intrastat-Transaktionen enthalten.

1. Wählen Sie auf der Seite **Modellzuordnungsdesigner** im Bereich **Datenquellentypen** die Option **Dynamics 365 for Operations\\Tabellendatensätze** aus.
2. Wählen Sie im Bereich **Datenquellen** die Option **Wurzel hinzufügen**, um eine neue Datenquelle hinzuzufügen, die für den Zugriff auf die Tabelle **Intrastat** verwendet werden soll. Jeder Datensatz in der Tabelle **Intrastat** steht für eine einzelne Intrastat-Transaktion.
3. Geben Sie im Dialogfeld **Eigenschaften der Datenquelle** im Feld **Name** den Eintrag **Transaktion** ein.
4. Geben Sie in das Feld **Tabelle** **Intrastat** ein.
5. Wählen Sie **OK** aus, um die neue Datenquelle hinzuzufügen.

#### <a name="add-a-data-source-to-group-intrastat-transactions"></a><a name="AddMmDataSource2"></a>Hinzufügen einer Datenquelle, um Intrastat Transaktionen zu gruppieren

Konfigurieren Sie eine **GroupBy** Datenquelle, um Intrastat Transaktionen zu gruppieren und Aggregatfunktionen zu berechnen.

1. Wählen Sie auf der Seite **Designer für die Datenzuordnung** im Bereich **Datenquellentypen** den Knoten **Funktionen\\Gruppieren nach**.
2. Wählen Sie im Bereich **Datenquellen** die Option **Wurzel hinzufügen**, um eine neue Datenquelle hinzuzufügen, die für die Gruppierung von Intrastat-Transaktionen und die Berechnung von Aggregatfunktionen verwendet wird.
3. Geben Sie im Dialogfeld **Eigenschaften der Datenquelle** im Feld **Name** **TransportRecord** ein.
4. Wählen Sie **Gruppe bearbeiten nach**, um die Gruppierungsbedingungen zu konfigurieren.
5. Wählen Sie auf der Seite **Parameter gruppieren nach** in der Liste der Datenquellen im rechten Bereich die Datenquelle **Transaktion** und erweitern Sie sie.
6. Markieren Sie **Feld zu \> Was zu gruppieren** hinzufügen, um anzugeben, dass die Datenquelle **Transaktion** als <a name="BaseDataSource">Basisdatenquelle</a> für die konfigurierte Datenquelle **GroupBy** ausgewählt wird. Die Datensätze der Datenquelle **Transaktion** werden gruppiert, und die Feldwerte dieser Datenquelle werden für Berechnungen in Aggregatfunktionen verwendet.
7. Markieren Sie das Feld **Transaktion\Transport** und wählen Sie dann **Feld zu \> Gruppiertes Feld hinzufügen**, um anzugeben, dass das Feld **Transport** der Basisdatenquelle als <a name="GroupingFields">Gruppierungskriterium</a> für die konfigurierte Datenquelle **GroupBy** ausgewählt ist. Mit anderen Worten, die Datensätze der Datenquelle **Transaktion** werden auf der Grundlage des Wertes des Feldes **Transport** gruppiert. Jeder Datensatz der konfigurierten **GroupBy** Datenquelle repräsentiert einen einzelnen Transportcode, der in Datensätzen der Basisdatenquelle gefunden wurde.
8. Wählen Sie das Feld **Transaktion\AmountMST** und folgen Sie dann diesen Schritten:

    1. Wählen Sie **Feld zu \> Aggregatfelder hinzufügen**, um anzugeben, dass eine <a name="AggregateFunctions">Aggregatfunktion</a> für dieses Feld berechnet werden soll.
    2. Wählen Sie im Bereich **Aggregationen** in dem Datensatz, der für das ausgewählte Feld **Transaction\AmountMST** hinzugefügt wurde, im Feld **Methode** die Funktion **Sum**.
    3. Geben Sie in das optionale Feld **Name** **TotalInvoicedAmount** ein.

    Diese Einstellungen legen fest, dass für jede Transportgruppe der Gesamtbetrag des Feldes **Transaction\AmountMST** berechnet wird.

9. Wählen Sie das Feld **Transaction\RecId** und folgen Sie dann diesen Schritten:

    1. Markieren Sie **Feld zu \> Aggregatfelder hinzufügen**, um anzugeben, dass für dieses Feld eine Aggregatfunktion berechnet werden soll.
    2. Wählen Sie im Bereich **Aggregationen** in dem Datensatz, der für das ausgewählte Feld **Transaktion\RecId** hinzugefügt wurde, im Feld **Methode** die Funktion **Zahl**.
    3. Geben Sie in das optionale Feld **Name** **NumberOfTransactions** ein.

    Diese Einstellungen legen fest, dass für jede Transportgruppe die Anzahl der Transaktionen in der Gruppe berechnet wird.

10. Wählen Sie **Speichern** aus.
11. Überprüfen Sie die <a name="ExecutionLocation">Ausführungsparameter</a> der bearbeitbaren Datenquelle. Beachten Sie, dass **Autodetect** im Feld **Ausführungsort** automatisch ausgewählt wurde und das Feld **Ausführung bei** den Wert **SQL** enthält. Diese Einstellungen legen fest, dass die ausgewählte Basisdatenquelle **Transaktion** aktuell abfragbar ist und Sie die editierbare Datenquelle **GroupBy** auf Datenbankebene ausführen können.
12. Öffnen Sie das Suchfeld für das Feld **Ausführungsort**, um die Liste der verfügbaren Werte zu überprüfen. Beachten Sie, dass Sie **Abfrage** oder **Im Speicher** auswählen können, um zu erzwingen, dass diese **GroupBy**-Datenquelle auf Datenbankebene oder im Speicher des Anwendungsservers ausgeführt wird.
13. Wählen Sie **Speichern** und schließen Sie die Seite **Bearbeiten der Parameter 'Gruppieren nach'**.
14. Wählen Sie **OK**, um die Einstellungen der Datenquelle **GroupBy** abzuschließen.

#### <a name="bind-the-groupby-data-source-to-data-model-fields"></a><a name="AddMmBindings"></a>Binden Sie die GroupBy-Datenquelle an Datenmodellfelder

Binden Sie die konfigurierte Datenquelle an die Felder des Datenmodells, um festzulegen, wie das Datenmodell zur Laufzeit mit Anwendungsdaten gefüllt werden soll.

1. Erweitern Sie auf der Seite **Designer für die Zuordnung von Modellen** im Bereich **Datenmodell** den Knoten **Transport**.
2. Erweitern Sie im Bereich **Datenquellen** die Datenquelle **TransportRecord**.
3. Fügen Sie einen Datenfluss hinzu, um die Liste der gefundenen Transportgruppen anzuzeigen:

    1. Wählen Sie im Bereich **Datenmodell** den Artikel **Transport**.
    2. Wählen Sie im Bereich **Datenquellen** die Datenquelle **TransportRecord**.
    3. Wählen Sie **Bindung** aus.

4. Fügen Sie eine Bindung hinzu, um den Transportcode jeder gefundenen Transportgruppe anzuzeigen:

    1. Wählen Sie den Artikel **Transport.Code** des Datenmodells.
    2. Wählen Sie das gruppierte Feld **TransportRecord.grouped.TransportMode**.
    3. Wählen Sie **Bindung** aus.

5. Fügen Sie eine Bindung hinzu, um die Werte der berechneten Aggregatfunktionen für jede entdeckte Transportgruppe anzuzeigen:

    1. Wählen Sie den Artikel **Transport.NumberOfTransactions** des Datenmodells.
    2. Wählen Sie das aggregierte Feld **TransportRecord.aggregated.NumberOfTransactions**.
    3. Wählen Sie **Bindung** aus.
    4. Markieren Sie den Datenmodelleintrag **Transport.TotalInvoicedAmount**.
    5. Markieren Sie das aggregierte Feld **TransportRecord.aggregated.TotalInvoicedAmount**.
    6. Wählen Sie **Bindung** aus.

6. Hinzufügen einer Bindung, um die Datensätze der Transaktionen, die zu jeder entdeckten Transportgruppe gehören, anzuzeigen:

    1. Markieren Sie den Artikel **Transport.Transaction** Datenmodell.
    2. Markieren Sie das Feld **TransportRecord.lines**.
    3. Wählen Sie **Bindung** aus.

    Sie können weiterhin Bindungen für die verschachtelten Artikel des Datenmodells **Transport.Transaction** und das Datenquellenfeld **TransportRecord.lines** konfigurieren, um zur Laufzeit Details zu den Intrastat-Transaktionen anzuzeigen, die zu jeder ermittelten Transportgruppe gehören.

![Konfigurierte Modellzuordnung im EB-Modellzuordnungsdesigner.](./media/er-groupby-data-sources-configure-model-mapping.png)

### <a name="debug-the-added-model-mapping-component"></a>Debuggen der hinzugefügten Komponente für die Modellzuordnung

Verwenden Sie den [ER-Datenquellendebugger](er-debug-data-sources.md), um die konfigurierte Modellzuordnung zu testen.

1. Wählen Sie auf der Seite **Designer für die Zuordnung von Modellen** die Option **Debugging starten**.
2. Wählen Sie auf der Seite **Datenquellen** im linken Fensterbereich die Datenquelle **TransportRecord** und wählen Sie dann **Alle Datensätze lesen**.
3. Erweitern Sie die Datenquelle **TransportRecord**, und folgen Sie dann diesen Schritten:

    1. Wählen Sie die Datenquelle **TransportRecord.grouped.TransportMode**.
    2. Wählen Sie **Wert abrufen**.
    3. Wählen Sie die Datenquelle **TransportRecord.grouped.NumberOfTransactions**.
    4. Wählen Sie **Wert abrufen**.
    5. Wählen Sie die Datenquelle **TransportRecord.grouped.TotalInvoicedAmount**.
    6. Wählen Sie **Wert abrufen**.

4. Wählen Sie im rechten Bereich **Alle erweitern**.

Die Datenquelle **TransportRecord** stellt zwei Datensätze und zwei Transportcodes zur Verfügung. Für jeden Transportcode werden die Anzahl der Transaktionen und der Gesamtrechnungsbetrag berechnet.

> [!NOTE]
> Der Ansatz des „faulen Lesens“ wird verwendet, wenn eine **GroupBy** Datenquelle aufgerufen wird, um Datenbankaufrufe zu optimieren. Daher werden einige der Feldwerte in einer **GroupBy**-Datenquelle im ER-Datenquellendebugger nur berechnet, wenn sie an Datenmodellfelder gebunden sind.

![Ergebnisse der Datenquellendebugging auf der Seite Debug datasources.](./media/er-groupby-data-sources-debug-datasource.png)

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="is-there-any-way-to-calculate-grand-totals-when-the-group-totals-are-calculated"></a>Gibt es eine Möglichkeit, Gesamtsummen zu berechnen, wenn die Gruppensummen berechnet werden?

Ja. Um Gesamtsummen zu berechnen, konfigurieren Sie eine weitere **GroupBy** Datenquelle, wobei die **GroupBy** Datenquelle, die Sie zuvor konfiguriert haben, als Basisdatenquelle verwendet wird. Die folgende Abbildung zeigt die Datenquelle **Summen** vom Typ **GroupBy**, die zur Berechnung der Aggregatfunktion **SUM** verwendet wird, basierend auf der Aggregation **SUM** der Datenquelle **TransportRecord** vom Typ **GroupBy**.

![Summen-Datenquelle im Designer für die Zuordnung von ER-Modellen.](./media/er-groupby-data-sources-configure-model-mapping2.png)

Die folgende Abbildung zeigt die Ergebnisse der **Summen** Datenquelle debuggen.

![Ergebnisse der Fehlersuche in der Datenquelle Summen auf der Seite Fehlersuche in Datenquellen.](./media/er-groupby-data-sources-debug-datasource2.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)
- [Debuggen Sie Datenquellen eines ausgeführten EB-Formats, um den Datenfluss und die Transformation zu analysieren](er-debug-data-sources.md)
- [Verwendung von DATA COLLECTION Datenquellen in elektronischen Berichtsformaten](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
