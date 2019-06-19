---
title: Implementieren benutzerdefinierter Felder für die mobile Microsoft Dynamics 365 Project Timesheet-App auf iOS und Android
description: Dieses Thema enthält allgemeine Muster zur Verwendung von Erweiterungen, um benutzerdefinierte Felder zu implementieren.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 4343c875da05641c57b7784bf52f1c814dd26d20
ms.sourcegitcommit: 19859d8566a8c7840066b2c10c6b08b67f1b83f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2019
ms.locfileid: "1617995"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Implementieren benutzerdefinierter Felder für die mobile Microsoft Dynamics 365 Project Timesheet-App auf iOS und Android

[!include [banner](../includes/banner.md)]

Dieses Thema enthält allgemeine Muster zur Verwendung von Erweiterungen, um benutzerdefinierte Felder zu implementieren. Folgende Themen werden behandelt:

- Die verschiedenen Datentypen, die das benutzerdefinierte Feldframework unterstützt
- Vorgehensweise beim Anzeigen schreibgeschützter oder bearbeitbarer Felder in Arbeitszeittabelleneinträgen und Speichern von vom Benutzer bereitgestellten Werten zurück in die Datenbank
- Vorgehensweise beim Anzeigen schreibgeschützter Felder in der Arbeitszeittabellen-Kopfzeile
- Vorgehensweise beim Integrieren anderer benutzerdefinierter Geschäftslogik, um Standardwerte in Felder einzugeben und zusätzliche Auswertung vorzunehmen

## <a name="audience"></a>Zielgruppe

Dieses Thema richtet sich an Entwickler, die ihre benutzerdefinierten Felder in die mobile Microsoft Dynamics 365 Project Timesheet-Anwendung integrieren, die für Apple iOS und Google Android verfügbar ist. Es wird davon ausgegangen, dass Leser mit der X++-Entwicklung und Projektarbeitszeittabellen-Funktion vertraut sind.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Datenvertrag – TSTimesheetCustomField X++-Klasse

Die Klasse **TSTimesheetCustomField** ist die X++-Datenvertragsklasse, die Informationen zu einem benutzerdefinierten Feld für die Arbeitszeittabellen-Funktion darstellt. Listen der benutzerdefinierten Feldobjekte werden sowohl im TSTimesheetDetails-Datenvertrag als auch im TSTimesheetEntry-Vertrag weitergegeben, um benutzerdefinierte in der mobilen App anzuzeigen.

- **TSTimesheetDetails** – Der Arbeitszeittabellen-Kopfzeilen-Vertrag
- **TSTimesheetEntry** – Der Arbeitszeittabellen-Buchungsvertrag. Gruppen dieser Objekte, die dieselben Projektinformationen und denselben **timesheetLineRecId**-Wert haben, stellen eine Position dar.

### <a name="fieldbasetype-types"></a>fieldBaseType (Typen)

Die Eigenschaft **FieldBaseType** im Objekt **TsTimesheetCustom** bestimmt den Typ des Felds, das in der App angezeigt wird. Die folgenden **Typen**-Werte, die unterstützt werden.

| Typenwert | Typ              | Notizen |
|-------------|-------------------|-------|
| 0           | Zeichenfolge und (Enumeration) | Das Feld wird als Textfeld angezeigt. |
| 1           | Ganze Zahl           | Der Wert wird als Anzahl ohne Dezimalstellen angezeigt. |
| 2           | Gleitkommazahl              | Der Wert wird als Anzahl mit Dezimalstellen angezeigt.<p>Zum Anzeigen des realen Werts als Währung in der App, verwenden Sie die Eigenschaft **fieldExtenededType**. Sie können die Eigenschaft **numberOfDecimals** verwenden, um die Anzahl von Dezimalstellen festzulegen, die angezeigt werden.</p> |
| 3           | Datum              | Datumsformate werden durch die Einstellung **Datum, Uhrzeit und Zahlenformat** des Benutzers bestimmt, die unter **Einstellung von Sprache und Land/Region** unter **Benutzeroptionen** festgelegt wird. |
| 4           | Aktiv           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Wenn die Eigenschaft **stringOptions** nicht im Objekt **TSTimesheetCustomField** angegeben ist, wird dem Benutzer ein Freitextfeld bereitgestellt.

    Die Eigenschaft **stringLength** kann verwendet werden, um die maximale Zeichenfolgenlänge festzulegen, die Benutzer eingeben können.

- Wenn die Eigenschaft **stringOptions** im Objekt **TSTimesheetCustomField** bereitgestellt wird, sind diese Listenelemente die einzigen Werte, die Benutzer auswählen können, indem sie Optionsfelder (Optionsfelder) verwenden.

    In diesem Fall kann das Zeichenfolgenfeld als ein Enumerationswert für den Zweck des Benutzereintrags dienen. Um den Wert in der Datenbank als Enumeration zu speichern, weisen Sie den Zeichenfolgenwert manuell dem Enumerationswert zurück zu, bevor Sie ihn in der Datenbank mithilfe einer Befehlskette speichern (im Abschnitt „Verwenden einer Befehlskette in der TSTimesheetEntryService-Klasse, um einen Arbeitszeittabelleneintrag aus der App wieder in der Datenbank zu speichern“ später in diesem Thema finden Sie ein Beispiel).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Sie können diese Eigenschaft verwenden, um tatsächliche Werte als Währung zu formatieren. Dieser Ansatz ist nur anwendbar, wenn der **fieldBaseType**-Wert **Tatsächlich** ist.

- **TSCustomFieldExtendedType:None** – Keine Formatierung wird angewendet.
- **TSCustomFieldExtendedType::Currency** – Formatieren Sie den Wert als Währung.

    Wenn die Währungsformatierung aktiv ist, kann das Feld **stringValue** verwendet werden, um den Währungscode weiterzugeben, der in der App angezeigt werden soll. Der Wert ist ein schreibgeschützter Wert.

    Das Feld **realValue** enthält den Geldbetrag, der in der Datenbank gespeichert werden soll.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Sie können diese Eigenschaft verwenden, um anzugeben, wo das benutzerdefinierte Feld in der App angezeigt werden soll.

- **TSCustomFieldSection::Header** – Das Feld wird im Abschnitt **Weitere Details anzeigen** in der App angezeigt. Diese Felder sind immer schreibgeschützt.
- **TSCustomFieldSection::Line** – Das Feld wird nach den gesamten vorkonfigurierten Positionsfeldern in Zeittabelleneinträgen angezeigt. Diese Felder können entweder bearbeitbar oder schreibgeschützt sein.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Diese Eigenschaft identifiziert das Feld, wenn Werte, die die App bereitstellt, wieder in der Datenbank gespeichert werden.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Diese Eigenschaft identifiziert das Feld, wenn Werte, die die App bereitstellt, wieder in der Datenbank gespeichert werden.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Legen Sie diese Eigenschaft auf **Ja** fest, um anzugeben, dass das Feld im Arbeitszeittabellen-Eintragsabschnitt von Benutzern bearbeitbar sein soll. Legen Sie die Eigenschaft auf **Nein** fest, damit das Feld schreibgeschützt wird.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Legen Sie diese Eigenschaft auf **Ja** fest, um anzugeben, dass das Feld im Arbeitszeittabellen-Eintragsabschnitt obligatorisch sein soll.

### <a name="label-str"></a>Bezeichnung (str)

Diese Eigenschaft gibt die Bezeichnung an, die neben dem Feld in der App angezeigt wird.

### <a name="stringoptions-list-of-strings"></a>stringOptions (Liste der Zeichenfolgen)

Diese Eigenschaft ist nur anwendbar, wenn **fieldBaseType** auf **Zeichenfolge** festgelegt ist. Wenn **stringOptions** festgelegt ist, werden die Zeichenfolgenwerte, die zur Auswahl mittels Optionsfelder (Optionsfelder) verfügbar sind, durch die Zeichenfolgen in der Liste angegeben. Wenn keine Zeichenfolgen bereitgestellt werden, ist der Freitexteintrag im Zeichenfolgenfeld zulässig (im Abschnitt „Verwenden von Befehlskette in der TSTimesheetEntryService-Klasse, um einen Arbeitszeittabellen-Eintrag aus der App wieder in der Datenbank zu speichern“ später in diesem Thema finden Sie ein Beispiel).

### <a name="stringlength-int"></a>stringLength (int)

Diese Eigenschaft gibt die maximale Länge für ein Zeichenfolgenfeld an. Sie ist nur anwendbar, wenn **fieldBaseType** auf **Zeichenfolge** festgelegt ist.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Diese Eigenschaft gibt die Anzahl von Dezimalstellen an, die für ein tatsächliches Feld angezeigt werden. Sie ist nur anwendbar, wenn **fieldBaseType** auf **Tatsächlich** festgelegt ist.

### <a name="ordersequence-int"></a>orderSequence (int)

Diese Eigenschaft steuert die Reihenfolge, in der benutzerdefinierte Felder in der App angezeigt werden, wenn mehr als ein benutzerdefiniertes Feld angegeben ist. Felder, die niedrigere Zahlen besitzen, werden zuerst angezeigt.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Für Felder des Typs **Boolesch** gibt diese Eigenschaft den booleschen Wert des Felds zwischen dem Server und der App weiter.

### <a name="guidvalue-guid"></a>guidValue (guid)

Für Felder des Typs **GUID** gibt diese Eigenschaft den Wert des global eindeutigen Bezeichners (GUID) des Felds zwischen dem Server und der App weiter.

### <a name="int64value-int64"></a>int64Value (int64)

Für Felder des Typs **Int64** gibt diese Eigenschaft den int64-Wert des Felds zwischen dem Server und der App weiter.

### <a name="intvalue-int"></a>intValue (int)

Für Felder des Typs **Int** gibt diese Eigenschaft den int-Wert des Felds zwischen dem Server und der App weiter.

### <a name="realvalue-real"></a>realValue (real)

Für Felder des Typs **Tatsächlich** gibt diese Eigenschaft den tatsächlichen Wert des Felds zwischen dem Server und der App weiter.

### <a name="stringvalue-str"></a>stringValue (str)

Für Felder des Typs **Zeichenfolge** gibt diese Eigenschaft den Zeichenfolgenwert des Felds zwischen dem Server und der App weiter. Sie wird auch für Felder des Typs **Tatsächlich** verwendet, die als Währung formatiert werden. Für diese Felder wird die Eigenschaft verwendet, um den Währungscode an die App weiterzugeben.

### <a name="datevalue-date"></a>dateValue (date)

Für Felder des Typs **Datum** gibt diese Eigenschaft den Datumswert des Felds zwischen dem Server und der App weiter.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Anzeigen und Speichern eines benutzerdefinierten Felds im Abschnitt Arbeitszeittabellen-Eintrag

Unten befindet sich ein Bildschirmfoto von der mobilen App. Es zeigt eine Arbeitszeittabellen-Eintragserstellung Er zeigt die vorkonfigurierten Felder und ein benutzerdefiniertes Feld im Abschnitt „Zeiteintrag“, der „Testzeichenfolge“ bezeichnet wird, bei dem ein Enumerationswert „Zweite Option“ bereits festgelegt ist.

![Benutzerdefiniertes Testzeichenfolgen-Feld in der App](media/timesheet-entry.jpg)



Unten ist ein Bildschirmfoto der mobilen App des Benutzers, der eine der Enumerationsoptionen auswählt, die für das benutzerdefinierte Feld „Testzeichenfolge“ verfügbar sind.  Die zwei Optionen sind „Erste Option“ und „Zweite Option“, die als Optionsfelder angezeigt werden. Die zweite Option ist derzeit ausgewählt.

![Optionsfelder (Optionsfelder) für benutzerdefinierte Feld „Testzeichenfolge“](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Erweitern der TSTimesheetLine-Tabelle, sodass sie ein benutzerdefiniertes Feld hat

In typischen Szenarien ist es wahrscheinlich, dass die Daten für ein benutzerdefiniertes Feld im Abschnitt Arbeitszeittabelleneintrag in der Tabelle TSTimesheetLine gespeichert werden. Allerdings können andere Tabellen verwendet werden, wenn die Daten auf Basis eines TSTimesheetTrans-Datensatzes abgerufen werden können, oder wenn sie keinen spezifischen Datensatzkontext haben (beispielsweise wenn das Feld in den Projektparametern als schreibgeschützt festgelegt wird).

Beachten Sie, dass benutzerdefinierte Felder keine unterstützenden Datenbank-Datensätze haben müssen. Sie können auf Grundlage der X++-Logik dynamisch generiert werden. Dieser Ansatz kann bei schreibgeschützten Szenarien nützlich sein (im Abschnitt „Befehlskettenbefehl in der TSTimesheetDetails class-Klasse, buildCustomFieldListForHeader-Methode verwenden, um Arbeitszeittabellendetails auszufüllen“ finden Sie ein Beispiel dynamisch generierter benutzerdefinierter Feldwerte.)

Unten ist ein Bildschirmfoto von Visual Studio, das die Entwicklungsumgebung zeigt. Er zeigt eine Erweiterung der TSTimesheetLine-Tabelle mit dem Feld TestLineString an, das als benutzerdefiniertes Feld hinzugefügt ist.

![Positionszeichenfolge](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Verwenden der Befehlskette in der Methode buildCustomFieldList der Klasse TSTimesheetSettings zum Anzeigen eines Felds im Arbeitszeittabelleneintrags-Abschnitt

Dieser Code steuert die Anzeigeeinstellungen für das Feld in der App. Er steuert beispielsweise den Feldtyp, die Bezeichnung, ob das Feld ein Pflichtfeld ist und in welchem Abschnitt das Feld angezeigt wird.

Im folgenden Beispiel wird ein Zeichenfolgenfeld in Zeiteinträgen angezeigt. Dieses Feld enthält zwei Optionen, **Erste Option** und **Zweite Option**, die über Optionsfelder (Optionsfelder) verfügbar sind. Das Feld in der App ist dem Feld **TestLineString** zugeordnet, das der Tabelle TSTimesheetLine-Tabelle hinzugefügt wird.

Beachten Sie die Verwendung der **TSTimesheetCustomField::newFromMetatdata()**-Methode, um die Initialisierung der Eigenschaften benutzerdefinierter Felder zu vereinfachen: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** und **numberOfDecimals**. Sie können diese Parameter auch manuell festlegen, wenn Sie dies bevorzugen.

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Verwenden der Befehlskette in der Methode buildCustomFieldListForEntry der Klasse TSTimesheetEntry zum Eingeben von Werten in einem Arbeitszeittabelleneintrag

Die Methode **buildCustomFieldListForEntry** wird verwendet, um Werte in den gespeicherten Arbeitszeittabellen-Positionen in der mobilen App einzugeben. Sie übernimmt einen TSTimesheetTrans-Datensatz als Parameter. Felder aus diesem Datensatz können verwendet werden, um den benutzerdefinierten Feldwert in der App auszufüllen.

```
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Verwenden von Befehlskette in der Klasse TSTimesheetEntryService zum erneuten Speichern eines Arbeitszeittabellen-Eintrags aus der App in der Datenbank

Um ein benutzerdefiniertes Feld in typischer Verwendung wieder in die Datenbank zu speichern, müssen Sie mehrere Methoden erweitern:

- Die Methode **timesheetLineNeedsUpdating** wird verwendet, um zu bestimmen, ob der Positionsdatensatz vom Benutzer in der App geändert wurde und in der Datenbank gespeichert werden muss. Wenn Leistung keine Rolle spielt, kann diese Methode vereinfacht werden, damit sie immer **true** zurückgibt.
- Die Methoden **populateTimesheetLineFromEntryDuringCreate** und **populateTimesheetLineFromEntryDuringUpdate** können auch erweitert werden, sodass sie Werte im Datenbank-Datensatz TSTimesheetLine aus dem bereitgestellten TSTimesheetEntry-Datenvertrags-Datensatz eingeben. Beachten Sie im folgenden Beispiel, wie die Zuordnung zwischen dem Datenbankfeld und dem Eingabefeld manuell über den X++-Code erfolgt.
- Die Methode **populateTimesheetWeekFromEntry** kann auch erweitert werden, wenn das benutzerdefinierte Feld, das dem Objekt **TSTimesheetEntry** zugeordnet ist, erneut in die Datenbanktabelle TSTimesheetLineweek schreiben muss.

> [!NOTE]
> Das folgende Beispiel speichert die Werte **firstOption** oder **secondOption**, die der Benutzer auswählt, in der Datenbank als unformatierter Zeichenfolgenwert. Wenn das Datenbankfeld ein Feld vom Typ **Enumeration** ist, können diese Werte manuell einem Enumerationswwert zugeordnet werden und dann in einem Enumerationsfeld in der Datenbanktabelle gespeichert werden.

```
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Anzeigen eines benutzerdefinierten Felds im Abschnitt Arbeitszeittabellen-Kopfzeile

Unten befindet sich ein Bildschirmfoto von der mobilen App. Es zeigt einen Benutzer, der die Arbeitszeittabelle anzeigt. Die Schaltfläche „Weitere Informationen“ in der rechten oberen Ecke ist ausgewählt worden, um die Option „Weitere Details anzeigen“ anzuzeigen.  

![Weitere Details anzeigen – Befehl](media/show-more.png)



Unten befindet sich ein Bildschirmfoto von der mobilen App. Es zeigt den Abschnitt „Mehr“ in der Arbeitszeittabelle. Ein benutzerdefiniertes Feld mit der Bezeichnung „Benutzungsrate der Arbeitszeittabelle (berechnetes benutzerdefiniertes Feld)“ ist dem Arbeitszeittabellen-Kopfzeilenabschnitt hinzugefügt worden. Ein schreibgeschützter Wert „0,667“ ist im benutzerdefinierten Feld festgelegt.

![Weiterer Abschnitt](media/more-section.jpg)



### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Erweitern der TSTimesheetTable-Tabelle, sodass sie ein benutzerdefiniertes Feld hat

In typischen Szenarien ist es wahrscheinlich, dass die Daten für ein benutzerdefiniertes Feld im Kopfzeilenabschnitt aus der TSTimesheetHeader-Tabelle entnommen werden. Allerdings können andere Tabellen verwendet werden, wenn die Daten auf Basis eines TSTimesheetTable-Datensatzes abgerufen werden können, oder wenn sie keinen spezifischen Datensatzkontext haben (beispielsweise wenn das Feld in den Projektparametern als schreibgeschützt festgelegt wird).

Beachten Sie, dass benutzerdefinierte Felder keine unterstützenden Datenbank-Datensätze haben müssen. Sie können auf Grundlage der X++-Logik dynamisch generiert werden. Das Beispiel, das folgt, zeigt diesen Ansatz.

Felder im Kopfzeilenabschnitt sind immer in der App immer schreibgeschützt.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Verwenden der Befehlskette in der Methode buildCustomFieldList der Klasse TSTimesheetSettings zum Anzeigen eines Felds im Kopfzeilenabschnitt

Dieser Code steuert die Anzeigeeinstellungen für das Feld in der App. Er steuert beispielsweise den Feldtyp, die Bezeichnung, ob das Feld ein Pflichtfeld ist und in welchem Abschnitt das Feld angezeigt wird.

Das folgende Beispiel zeigt einen berechneten Wert im Kopfzeilenabschnitt in der App an.

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Verwenden der Befehlskette in der Methode buildCustomFieldListForHeader der Klasse TSTimesheetDetails zum Eingeben von Werten in Arbeitszeittabellen-Details

Die Methode **buildCustomFieldListForHeader** wird verwendet, um die Arbeitszeittabellen-Kopfzeilendetails in der mobilen App einzugeben. Sie übernimmt einen TSTimesheetTable-Datensatz als Parameter. Felder aus diesem Datensatz können verwendet werden, um den benutzerdefinierten Feldwert in der App auszufüllen. Im folgenden Beispiel werden keine Werte aus der Datenbank gelesen. Stattdessen wird eine X++-Logik verwendet, um einen berechneten Wert zu generieren, der dann in der App angezeigt wird.


```
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Andere Konfigurierberkeits-/Erweiterbarkeits-Verkaufschancen

### <a name="adding-additional-validation-for-the-app"></a>Zusätzliche Überprüfung für die App hinzufügen

Vorhandene Logik für die Arbeitszeittabellen-Funktion auf der Datenbankebene funktioniert noch wie erwartet. Um den Abschluss der Speicher- oder Sendevorgänge zu unterbrechen und eine spezifische Fehlermeldung anzuzeigen, können Sie dem Code **throw error("message to user")** über eine Befehlskettenerweiterung hinzufügen. Nachfolgend finden Sie drei Beispiele von nützlichen erweiterbaren Methoden:

- Wenn **validateWrite** in der TSTimesheetLine-Tabelle **false** während eines Speichervorgangs für eine Arbeitszeittabellen-Position zurückgibt, wird eine Fehlermeldung in der mobilen App angezeigt.
- Wenn **validateSubmit** in der TSTimesheetTable-Tabelle **false** während der Arbeitszeittabellen-Übermittlung in der App zurückgibt, wird dem Benutzer eine Fehlermeldung angezeigt.
- Logik die Felder ausfüllt (zum Beispiel **Positionseigenschaft**) während die **insert**-Methode in der Tabelle TSTimesheetLine immer noch ausgeführt wird.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Ausblenden und Markieren vorkonfigurierter Felder als schreibgeschützt über eine Konfiguration

Von den Projektparametern aus können Sie vorkonfigurierte Felder in der mobilen App mit einem Schreibschutz versehen oder ausblenden. Legen Sie die Optionen im Abschnitt **Mobile Arbeitszeittabellen** unter der Registerkarte **Arbeitszeittabelle** der Seite **Projektverwaltungs- und Buchhaltungsparameter** fest.

![Projektparameter](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Die Aktivitäten ändern, die zur Auswahl über Erweiterungen verfügbar sind

Die Aktivitäten, die zur Auswahl für ein Projekt verfügbar sind, werden über die Methoden **getActivitiesForProject()** und **getActivityQuery()** in der Klasse **TsTimesheetProjectService** eingegeben. Sie können eine Befehlskette verwenden, um dieses Verhalten zu ändern, damit es Ihrem Geschäftsszenario entspricht. Das gilt für die Aktivitäten, die für ein bestimmtes Projekt zur Auswahl stehen.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Eingeben einer Standardprojektkategorie in Arbeitszeittabellen-Einträge

Eingabe einer standardmäßigen Projektkategorie in Arbeitszeittabellen-Einträgen erfolgt auf drei Ebenen. Sie können Befehlsketten verwenden, um das Verhalten auf irgendeine oder alle dieser Ebenen auszudehnen, um das gewünschte Verhalten zu erreichen. Die folgende Hierarchie wird verwendet:

1. Die App versucht, die Standardkategorie aus der Projektressource zu platzieren. Diese Standardkategorie wird in den Methoden **getCurrentUserResource** und **getDelegatedResourcesForCurrentUser** in der Klasse **TSTimesheetSettingsService** festgelegt.
2. Wenn die Standardkategorie nicht auf der Projektressourcenebene bereitgestellt wird, versucht die App, sie aus der Projektaktivität zu beziehen. Diese Standardkategorie wird in der Methode **getActivitiesForProject** in der Klasse **TSTimesheetProjectService** festgelegt.
3. Wenn die Standardkategorie nicht auf der Projektaktivitätsebene bereitgestellt wird, wird die Standardkategorie aus den Projektparametern bezogen. Diese Standardkategorie wird in der Methode **getProjectDetailsbyRule** in der Klasse **TSTimesheetProjectService** festgelegt.
