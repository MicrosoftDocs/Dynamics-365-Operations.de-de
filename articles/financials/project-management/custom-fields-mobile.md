<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="custom-fields-mobile.md" target-language="de-DE">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>custom-fields-mobile.2a9e5e.4343c875da05641c57b7784bf52f1c814dd26d20.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4343c875da05641c57b7784bf52f1c814dd26d20</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>19859d8566a8c7840066b2c10c6b08b67f1b83f4</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/04/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\financials\project-management\custom-fields-mobile.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Implementieren benutzerdefinierter Felder für die mobile Microsoft Dynamics 365 Project Timesheet-App auf iOS und Android</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides common patterns for using extensions to implement custom fields.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dieses Thema enthält allgemeine Muster zur Verwendung von Erweiterungen, um benutzerdefinierte Felder zu implementieren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Implementieren benutzerdefinierter Felder für die mobile Microsoft Dynamics 365 Project Timesheet-App auf iOS und Android</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides common patterns for using extensions to implement custom fields.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Dieses Thema enthält allgemeine Muster zur Verwendung von Erweiterungen, um benutzerdefinierte Felder zu implementieren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The following topics are covered:</source><target logoport:matchpercent="82" state="translated" state-qualifier="x-fuzzy-match-unedited">Folgende Themen werden behandelt:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The various data types that the custom field framework supports</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die verschiedenen Datentypen, die das benutzerdefinierte Feldframework unterstützt</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Vorgehensweise beim Anzeigen schreibgeschützter oder bearbeitbarer Felder in Arbeitszeittabelleneinträgen und Speichern von vom Benutzer bereitgestellten Werten zurück in die Datenbank</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>How to show read-only fields on the timesheet header</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Vorgehensweise beim Anzeigen schreibgeschützter Felder in der Arbeitszeittabellen-Kopfzeile</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>How to integrate other custom business logic to enter default values in fields and do additional validation</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Vorgehensweise beim Integrieren anderer benutzerdefinierter Geschäftslogik, um Standardwerte in Felder einzugeben und zusätzliche Auswertung vorzunehmen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Audience</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Zielgruppe</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dieses Thema richtet sich an Entwickler, die ihre benutzerdefinierten Felder in die mobile Microsoft Dynamics 365 Project Timesheet-Anwendung integrieren, die für Apple iOS und Google Android verfügbar ist.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The assumption is that readers are familiar with X++ development and project timesheet functionality.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Es wird davon ausgegangen, dass Leser mit der X++-Entwicklung und Projektarbeitszeittabellen-Funktion vertraut sind.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Data contract – TSTimesheetCustomField X++ class</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Datenvertrag – TSTimesheetCustomField X++-Klasse</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The <bpt id="p1">**</bpt>TSTimesheetCustomField<ept id="p1">**</ept> class is the X++ data contract class that represents information about a custom field for timesheet functionality.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die Klasse <bpt id="p1">**</bpt>TSTimesheetCustomField<ept id="p1">**</ept> ist die X++-Datenvertragsklasse, die Informationen zu einem benutzerdefinierten Feld für die Arbeitszeittabellen-Funktion darstellt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Listen der benutzerdefinierten Feldobjekte werden sowohl im TSTimesheetDetails-Datenvertrag als auch im TSTimesheetEntry-Vertrag weitergegeben, um benutzerdefinierte in der mobilen App anzuzeigen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">**</bpt>TSTimesheetDetails<ept id="p1">**</ept> - The timesheet header contract.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>TSTimesheetDetails<ept id="p1">**</ept> – Der Arbeitszeittabellen-Kopfzeilen-Vertrag</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">**</bpt>TSTimesheetEntry<ept id="p1">**</ept> - The timesheet transaction contract.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>TSTimesheetEntry<ept id="p1">**</ept> – Der Arbeitszeittabellen-Buchungsvertrag.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Groups of these objects that have the same project information and <bpt id="p1">**</bpt>timesheetLineRecId<ept id="p1">**</ept> value constitute a line.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Gruppen dieser Objekte, die dieselben Projektinformationen und denselben <bpt id="p1">**</bpt>timesheetLineRecId<ept id="p1">**</ept>-Wert haben, stellen eine Position dar.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>fieldBaseType (Types)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">fieldBaseType (Typen)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The <bpt id="p1">**</bpt>FieldBaseType<ept id="p1">**</ept> property on the <bpt id="p2">**</bpt>TsTimesheetCustom<ept id="p2">**</ept> object determines the type of the field that appears in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die Eigenschaft <bpt id="p1">**</bpt>FieldBaseType<ept id="p1">**</ept> im Objekt <bpt id="p2">**</bpt>TsTimesheetCustom<ept id="p2">**</ept> bestimmt den Typ des Felds, das in der App angezeigt wird.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The following <bpt id="p1">**</bpt>Types<ept id="p1">**</ept> values that are supported.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die folgenden <bpt id="p1">**</bpt>Typen<ept id="p1">**</ept>-Werte, die unterstützt werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Types value</source><target logoport:matchpercent="81" state="translated" state-qualifier="fuzzy-match">Typenwert</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Type</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Typ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Notes</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Notizen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>0</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>String (and Enum)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Zeichenfolge und (Enumeration)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The field appears as a text field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Das Feld wird als Textfeld angezeigt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>1</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Integer</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Ganze Zahl</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The value is shown as a number without decimal places.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Der Wert wird als Anzahl ohne Dezimalstellen angezeigt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>2</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Real</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Gleitkommazahl</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The value is shown as a number that has decimal places.</source><target logoport:matchpercent="84" state="translated" state-qualifier="fuzzy-match">Der Wert wird als Anzahl mit Dezimalstellen angezeigt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>To show the real value as a currency in the app, use the <bpt id="p1">**</bpt>fieldExtenededType<ept id="p1">**</ept> property.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Zum Anzeigen des realen Werts als Währung in der App, verwenden Sie die Eigenschaft <bpt id="p1">**</bpt>fieldExtenededType<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>You can use the <bpt id="p1">**</bpt>numberOfDecimals<ept id="p1">**</ept> property to set the number of decimal places that are shown.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sie können die Eigenschaft <bpt id="p1">**</bpt>numberOfDecimals<ept id="p1">**</ept> verwenden, um die Anzahl von Dezimalstellen festzulegen, die angezeigt werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>3</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Date</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Datum</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Date formats are determined by the user's <bpt id="p1">**</bpt>Date, times, and number format<ept id="p1">**</ept> setting that is specified under <bpt id="p2">**</bpt>Language and country/region preference<ept id="p2">**</ept> in <bpt id="p3">**</bpt>User options<ept id="p3">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Datumsformate werden durch die Einstellung <bpt id="p1">**</bpt>Datum, Uhrzeit und Zahlenformat<ept id="p1">**</ept> des Benutzers bestimmt, die unter <bpt id="p2">**</bpt>Einstellung von Sprache und Land/Region<ept id="p2">**</ept> unter <bpt id="p3">**</bpt>Benutzeroptionen<ept id="p3">**</ept> festgelegt wird.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>4</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Boolean</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Aktiv</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>15</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">15</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>GUID</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">GUID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>16</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">16</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Int64</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Int64</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>If the <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> property isn't provided on the <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> object, a free-text field is provided to the user.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wenn die Eigenschaft <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> nicht im Objekt <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> angegeben ist, wird dem Benutzer ein Freitextfeld bereitgestellt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>The <bpt id="p1">**</bpt>stringLength<ept id="p1">**</ept> property can be used to set the maximum string length that users can enter.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die Eigenschaft <bpt id="p1">**</bpt>stringLength<ept id="p1">**</ept> kann verwendet werden, um die maximale Zeichenfolgenlänge festzulegen, die Benutzer eingeben können.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>If the <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> property is provided on the <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> object, those list elements are the only values that users can select by using option buttons (radio buttons).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wenn die Eigenschaft <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> im Objekt <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> bereitgestellt wird, sind diese Listenelemente die einzigen Werte, die Benutzer auswählen können, indem sie Optionsfelder (Optionsfelder) verwenden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>In this case, the string field can act as an enum value for the purpose of user entry.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">In diesem Fall kann das Zeichenfolgenfeld als ein Enumerationswert für den Zweck des Benutzereintrags dienen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Um den Wert in der Datenbank als Enumeration zu speichern, weisen Sie den Zeichenfolgenwert manuell dem Enumerationswert zurück zu, bevor Sie ihn in der Datenbank mithilfe einer Befehlskette speichern (im Abschnitt „Verwenden einer Befehlskette in der TSTimesheetEntryService-Klasse, um einen Arbeitszeittabelleneintrag aus der App wieder in der Datenbank zu speichern“ später in diesem Thema finden Sie ein Beispiel).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>fieldExtendedType (TSCustomFieldExtendedType)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">fieldExtendedType (TSCustomFieldExtendedType)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>You can use this property to format real values as currency.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sie können diese Eigenschaft verwenden, um tatsächliche Werte als Währung zu formatieren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>This approach is applicable only when the <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> value is <bpt id="p2">**</bpt>Real<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dieser Ansatz ist nur anwendbar, wenn der <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept>-Wert <bpt id="p2">**</bpt>Tatsächlich<ept id="p2">**</ept> ist.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>TSCustomFieldExtendedType:None<ept id="p1">**</ept> – No formatting is applied.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>TSCustomFieldExtendedType:None<ept id="p1">**</ept> – Keine Formatierung wird angewendet.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>TSCustomFieldExtendedType::Currency<ept id="p1">**</ept> – Format the value as currency.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>TSCustomFieldExtendedType::Currency<ept id="p1">**</ept> – Formatieren Sie den Wert als Währung.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>When currency formatting is active, the <bpt id="p1">**</bpt>stringValue<ept id="p1">**</ept> field can be used pass the currency code that should be shown in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wenn die Währungsformatierung aktiv ist, kann das Feld <bpt id="p1">**</bpt>stringValue<ept id="p1">**</ept> verwendet werden, um den Währungscode weiterzugeben, der in der App angezeigt werden soll.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>The value is a read-only value.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Der Wert ist ein schreibgeschützter Wert.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The <bpt id="p1">**</bpt>realValue<ept id="p1">**</ept> field contains the money amount that should be saved to the database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Das Feld <bpt id="p1">**</bpt>realValue<ept id="p1">**</ept> enthält den Geldbetrag, der in der Datenbank gespeichert werden soll.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>fieldSection (TSCustomFieldSection)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">fieldSection (TSCustomFieldSection)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>You can use this property specify where the custom field should appear in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sie können diese Eigenschaft verwenden, um anzugeben, wo das benutzerdefinierte Feld in der App angezeigt werden soll.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>TSCustomFieldSection::Header<ept id="p1">**</ept> – The field will appear in the <bpt id="p2">**</bpt>View more details<ept id="p2">**</ept> section in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>TSCustomFieldSection::Header<ept id="p1">**</ept> – Das Feld wird im Abschnitt <bpt id="p2">**</bpt>Weitere Details anzeigen<ept id="p2">**</ept> in der App angezeigt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>These fields are always read-only.</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">Diese Felder sind immer schreibgeschützt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>TSCustomFieldSection::Line<ept id="p1">**</ept> – The field will appear after all the out-of-box line fields on timesheet entries.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>TSCustomFieldSection::Line<ept id="p1">**</ept> – Das Feld wird nach den gesamten vorkonfigurierten Positionsfeldern in Zeittabelleneinträgen angezeigt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>These fields can be either editable or read-only.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Diese Felder können entweder bearbeitbar oder schreibgeschützt sein.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>fieldName (FieldNameShort)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">fieldName (FieldNameShort)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>This property identifies the field when values that the app provides are saved back to the database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Diese Eigenschaft identifiziert das Feld, wenn Werte, die die App bereitstellt, wieder in der Datenbank gespeichert werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>tableName (TableNameShort)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">tableName (TableNameShort)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>This property identifies the field when values that the app provides are saved back to the database.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Diese Eigenschaft identifiziert das Feld, wenn Werte, die die App bereitstellt, wieder in der Datenbank gespeichert werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>isEditable (NoYes)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">isEditable (NoYes)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Set this property to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to specify that the field in the timesheet entry section should be editable by users.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Legen Sie diese Eigenschaft auf <bpt id="p1">**</bpt>Ja<ept id="p1">**</ept> fest, um anzugeben, dass das Feld im Arbeitszeittabellen-Eintragsabschnitt von Benutzern bearbeitbar sein soll.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Set the property to <bpt id="p1">**</bpt>No<ept id="p1">**</ept> to make the field read-only.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Legen Sie die Eigenschaft auf <bpt id="p1">**</bpt>Nein<ept id="p1">**</ept> fest, damit das Feld schreibgeschützt wird.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>isMandatory (NoYes)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">isMandatory (NoYes)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Set this property to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to specify that the field in the timesheet entry section should be mandatory.</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Legen Sie diese Eigenschaft auf <bpt id="p1">**</bpt>Ja<ept id="p1">**</ept> fest, um anzugeben, dass das Feld im Arbeitszeittabellen-Eintragsabschnitt obligatorisch sein soll.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>label (str)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Bezeichnung (str)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This property specifies the label that is shown next the field in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Diese Eigenschaft gibt die Bezeichnung an, die neben dem Feld in der App angezeigt wird.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>stringOptions (List of Strings)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">stringOptions (Liste der Zeichenfolgen)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>This property is applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Diese Eigenschaft ist nur anwendbar, wenn <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> auf <bpt id="p2">**</bpt>Zeichenfolge<ept id="p2">**</ept> festgelegt ist.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>If <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wenn <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> festgelegt ist, werden die Zeichenfolgenwerte, die zur Auswahl mittels Optionsfelder (Optionsfelder) verfügbar sind, durch die Zeichenfolgen in der Liste angegeben.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wenn keine Zeichenfolgen bereitgestellt werden, ist der Freitexteintrag im Zeichenfolgenfeld zulässig (im Abschnitt „Verwenden von Befehlskette in der TSTimesheetEntryService-Klasse, um einen Arbeitszeittabellen-Eintrag aus der App wieder in der Datenbank zu speichern“ später in diesem Thema finden Sie ein Beispiel).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>stringLength (int)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">stringLength (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>This property specifies the maximum length for a string field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Diese Eigenschaft gibt die maximale Länge für ein Zeichenfolgenfeld an.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>It's applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">Sie ist nur anwendbar, wenn <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> auf <bpt id="p2">**</bpt>Zeichenfolge<ept id="p2">**</ept> festgelegt ist.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>numberOfDecimals (int)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">numberOfDecimals (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This property specifies the number of decimal places that are shown for a real field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Diese Eigenschaft gibt die Anzahl von Dezimalstellen an, die für ein tatsächliches Feld angezeigt werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>It's applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>Real<ept id="p2">**</ept>.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Sie ist nur anwendbar, wenn <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> auf <bpt id="p2">**</bpt>Tatsächlich<ept id="p2">**</ept> festgelegt ist.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>orderSequence (int)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">orderSequence (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Diese Eigenschaft steuert die Reihenfolge, in der benutzerdefinierte Felder in der App angezeigt werden, wenn mehr als ein benutzerdefiniertes Feld angegeben ist.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Fields that have lower numbers are shown first.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Felder, die niedrigere Zahlen besitzen, werden zuerst angezeigt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>booleanValue (boolean)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">booleanValue (boolean)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>For fields of the <bpt id="p1">**</bpt>Boolean<ept id="p1">**</ept> type, this property passes the Boolean value of the field between the server and the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Für Felder des Typs <bpt id="p1">**</bpt>Boolesch<ept id="p1">**</ept> gibt diese Eigenschaft den booleschen Wert des Felds zwischen dem Server und der App weiter.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>guidValue (guid)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">guidValue (guid)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>For fields of the <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</source><target logoport:matchpercent="81" state="translated" state-qualifier="fuzzy-match">Für Felder des Typs <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> gibt diese Eigenschaft den Wert des global eindeutigen Bezeichners (GUID) des Felds zwischen dem Server und der App weiter.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>int64Value (int64)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">int64Value (int64)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>For fields of the <bpt id="p1">**</bpt>Int64<ept id="p1">**</ept> type, this property passes the int64 value of the field between the server and the app.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Für Felder des Typs <bpt id="p1">**</bpt>Int64<ept id="p1">**</ept> gibt diese Eigenschaft den int64-Wert des Felds zwischen dem Server und der App weiter.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>intValue (int)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">intValue (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>For fields of the <bpt id="p1">**</bpt>Int<ept id="p1">**</ept> type, this property passes the int value of the field between the server and the app.</source><target logoport:matchpercent="92" state="translated" state-qualifier="fuzzy-match">Für Felder des Typs <bpt id="p1">**</bpt>Int<ept id="p1">**</ept> gibt diese Eigenschaft den int-Wert des Felds zwischen dem Server und der App weiter.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>realValue (real)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">realValue (real)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>For fields of the <bpt id="p1">**</bpt>Real<ept id="p1">**</ept> type, this property passes the real value of the field between the server and the app .</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Für Felder des Typs <bpt id="p1">**</bpt>Tatsächlich<ept id="p1">**</ept> gibt diese Eigenschaft den tatsächlichen Wert des Felds zwischen dem Server und der App weiter.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>stringValue (str)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">stringValue (str)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>For fields of the <bpt id="p1">**</bpt>String<ept id="p1">**</ept> type, this property passes the string value of the field between the server and the app.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Für Felder des Typs <bpt id="p1">**</bpt>Zeichenfolge<ept id="p1">**</ept> gibt diese Eigenschaft den Zeichenfolgenwert des Felds zwischen dem Server und der App weiter.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>It's also used for fields of the <bpt id="p1">**</bpt>Real<ept id="p1">**</ept> type that are formatted as currency.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sie wird auch für Felder des Typs <bpt id="p1">**</bpt>Tatsächlich<ept id="p1">**</ept> verwendet, die als Währung formatiert werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>For those fields, the property is used to pass the currency code to the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Für diese Felder wird die Eigenschaft verwendet, um den Währungscode an die App weiterzugeben.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>dateValue (date)</source><target logoport:matchpercent="67" state="translated" state-qualifier="fuzzy-match">dateValue (date)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>For fields of the <bpt id="p1">**</bpt>Date<ept id="p1">**</ept> type, this property passes the date value of the field between the server and the app.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Für Felder des Typs <bpt id="p1">**</bpt>Datum<ept id="p1">**</ept> gibt diese Eigenschaft den Datumswert des Felds zwischen dem Server und der App weiter.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Show and save a custom field in the timesheet entry section</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Anzeigen und Speichern eines benutzerdefinierten Felds im Abschnitt Arbeitszeittabellen-Eintrag</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Below is a screenshot from the mobile app of a timesheet entry creation.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Unten befindet sich ein Bildschirmfoto von der mobilen App. Es zeigt eine Arbeitszeittabellen-Eintragserstellung</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Er zeigt die vorkonfigurierten Felder und ein benutzerdefiniertes Feld im Abschnitt „Zeiteintrag“, der „Testzeichenfolge“ bezeichnet wird, bei dem ein Enumerationswert „Zweite Option“ bereits festgelegt ist.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Test string custom field in the app</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Benutzerdefiniertes Testzeichenfolgen-Feld in der App</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Unten ist ein Bildschirmfoto der mobilen App des Benutzers, der eine der Enumerationsoptionen auswählt, die für das benutzerdefinierte Feld „Testzeichenfolge“ verfügbar sind.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>The two options are "First option" and "Second option" shown as radio buttons.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die zwei Optionen sind „Erste Option“ und „Zweite Option“, die als Optionsfelder angezeigt werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>The second option is currently selected.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die zweite Option ist derzeit ausgewählt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Option buttons (radio buttons) for the Test string custom field</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Optionsfelder (Optionsfelder) für benutzerdefinierte Feld „Testzeichenfolge“</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Extend the TSTimesheetLine table so that it has a custom field</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Erweitern der TSTimesheetLine-Tabelle, sodass sie ein benutzerdefiniertes Feld hat</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">In typischen Szenarien ist es wahrscheinlich, dass die Daten für ein benutzerdefiniertes Feld im Abschnitt Arbeitszeittabelleneintrag in der Tabelle TSTimesheetLine gespeichert werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Allerdings können andere Tabellen verwendet werden, wenn die Daten auf Basis eines TSTimesheetTrans-Datensatzes abgerufen werden können, oder wenn sie keinen spezifischen Datensatzkontext haben (beispielsweise wenn das Feld in den Projektparametern als schreibgeschützt festgelegt wird).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Note that custom fields don't have to have any backing database records.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Beachten Sie, dass benutzerdefinierte Felder keine unterstützenden Datenbank-Datensätze haben müssen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>They can be dynamically generated based on X++ logic.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sie können auf Grundlage der X++-Logik dynamisch generiert werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dieser Ansatz kann bei schreibgeschützten Szenarien nützlich sein (im Abschnitt „Befehlskettenbefehl in der TSTimesheetDetails class-Klasse, buildCustomFieldListForHeader-Methode verwenden, um Arbeitszeittabellendetails auszufüllen“ finden Sie ein Beispiel dynamisch generierter benutzerdefinierter Feldwerte.)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Below is a screenshot from Visual Studio of the Application Object Tree.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Unten ist ein Bildschirmfoto von Visual Studio, das die Entwicklungsumgebung zeigt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Er zeigt eine Erweiterung der TSTimesheetLine-Tabelle mit dem Feld TestLineString an, das als benutzerdefiniertes Feld hinzugefügt ist.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Line string</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Positionszeichenfolge</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Verwenden der Befehlskette in der Methode buildCustomFieldList der Klasse TSTimesheetSettings zum Anzeigen eines Felds im Arbeitszeittabelleneintrags-Abschnitt</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>This code controls the display settings for the field in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dieser Code steuert die Anzeigeeinstellungen für das Feld in der App.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Er steuert beispielsweise den Feldtyp, die Bezeichnung, ob das Feld ein Pflichtfeld ist und in welchem Abschnitt das Feld angezeigt wird.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>The following example shows a string field on time entries.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Im folgenden Beispiel wird ein Zeichenfolgenfeld in Zeiteinträgen angezeigt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>This field has two options, <bpt id="p1">**</bpt>First option<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Second option<ept id="p2">**</ept>, that are available via option buttons (radio buttons).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dieses Feld enthält zwei Optionen, <bpt id="p1">**</bpt>Erste Option<ept id="p1">**</ept> und <bpt id="p2">**</bpt>Zweite Option<ept id="p2">**</ept>, die über Optionsfelder (Optionsfelder) verfügbar sind.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>The field in the app is associated with the <bpt id="p1">**</bpt>TestLineString<ept id="p1">**</ept> field that is added to the TSTimesheetLine table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Das Feld in der App ist dem Feld <bpt id="p1">**</bpt>TestLineString<ept id="p1">**</ept> zugeordnet, das der Tabelle TSTimesheetLine-Tabelle hinzugefügt wird.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Note the use of the <bpt id="p1">**</bpt>TSTimesheetCustomField::newFromMetatdata()<ept id="p1">**</ept> method to simplify the initialization of the custom field properties: <bpt id="p2">**</bpt>fieldBaseType<ept id="p2">**</ept>, <bpt id="p3">**</bpt>tableName<ept id="p3">**</ept>, <bpt id="p4">**</bpt>fieldname<ept id="p4">**</ept>, <bpt id="p5">**</bpt>label<ept id="p5">**</ept>, <bpt id="p6">**</bpt>isEditable<ept id="p6">**</ept>, <bpt id="p7">**</bpt>isMandatory<ept id="p7">**</ept>, <bpt id="p8">**</bpt>stringLength<ept id="p8">**</ept>, and <bpt id="p9">**</bpt>numberOfDecimals<ept id="p9">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Beachten Sie die Verwendung der <bpt id="p1">**</bpt>TSTimesheetCustomField::newFromMetatdata()<ept id="p1">**</ept>-Methode, um die Initialisierung der Eigenschaften benutzerdefinierter Felder zu vereinfachen: <bpt id="p2">**</bpt>fieldBaseType<ept id="p2">**</ept>, <bpt id="p3">**</bpt>tableName<ept id="p3">**</ept>, <bpt id="p4">**</bpt>fieldname<ept id="p4">**</ept>, <bpt id="p5">**</bpt>label<ept id="p5">**</ept>, <bpt id="p6">**</bpt>isEditable<ept id="p6">**</ept>, <bpt id="p7">**</bpt>isMandatory<ept id="p7">**</ept>, <bpt id="p8">**</bpt>stringLength<ept id="p8">**</ept> und <bpt id="p9">**</bpt>numberOfDecimals<ept id="p9">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>You can also set these parameters manually, as you prefer.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sie können diese Parameter auch manuell festlegen, wenn Sie dies bevorzugen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Verwenden der Befehlskette in der Methode buildCustomFieldListForEntry der Klasse TSTimesheetEntry zum Eingeben von Werten in einem Arbeitszeittabelleneintrag</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The <bpt id="p1">**</bpt>buildCustomFieldListForEntry<ept id="p1">**</ept> method is used to enter values on the saved timesheet lines in the mobile app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die Methode <bpt id="p1">**</bpt>buildCustomFieldListForEntry<ept id="p1">**</ept> wird verwendet, um Werte in den gespeicherten Arbeitszeittabellen-Positionen in der mobilen App einzugeben.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>It takes a TSTimesheetTrans record as a parameter.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sie übernimmt einen TSTimesheetTrans-Datensatz als Parameter.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Fields from that record can be used to fill in the custom field value in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Felder aus diesem Datensatz können verwendet werden, um den benutzerdefinierten Feldwert in der App auszufüllen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Verwenden von Befehlskette in der Klasse TSTimesheetEntryService zum erneuten Speichern eines Arbeitszeittabellen-Eintrags aus der App in der Datenbank</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>To save a custom field back to the database in typical usage, you must extend multiple methods:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Um ein benutzerdefiniertes Feld in typischer Verwendung wieder in die Datenbank zu speichern, müssen Sie mehrere Methoden erweitern:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>The <bpt id="p1">**</bpt>timesheetLineNeedsUpdating<ept id="p1">**</ept> method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die Methode <bpt id="p1">**</bpt>timesheetLineNeedsUpdating<ept id="p1">**</ept> wird verwendet, um zu bestimmen, ob der Positionsdatensatz vom Benutzer in der App geändert wurde und in der Datenbank gespeichert werden muss.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>If performance isn't a concern, this method can be simplified so that it always returns <bpt id="p1">**</bpt>true<ept id="p1">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wenn Leistung keine Rolle spielt, kann diese Methode vereinfacht werden, damit sie immer <bpt id="p1">**</bpt>true<ept id="p1">**</ept> zurückgibt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>The <bpt id="p1">**</bpt>populateTimesheetLineFromEntryDuringCreate<ept id="p1">**</ept> and <bpt id="p2">**</bpt>populateTimesheetLineFromEntryDuringUpdate<ept id="p2">**</ept> methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die Methoden <bpt id="p1">**</bpt>populateTimesheetLineFromEntryDuringCreate<ept id="p1">**</ept> und <bpt id="p2">**</bpt>populateTimesheetLineFromEntryDuringUpdate<ept id="p2">**</ept> können auch erweitert werden, sodass sie Werte im Datenbank-Datensatz TSTimesheetLine aus dem bereitgestellten TSTimesheetEntry-Datenvertrags-Datensatz eingeben.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Beachten Sie im folgenden Beispiel, wie die Zuordnung zwischen dem Datenbankfeld und dem Eingabefeld manuell über den X++-Code erfolgt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>The <bpt id="p1">**</bpt>populateTimesheetWeekFromEntry<ept id="p1">**</ept> method can also be extended if the custom field that is mapped to the <bpt id="p2">**</bpt>TSTimesheetEntry<ept id="p2">**</ept> object must write back to the TSTimesheetLineweek database table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die Methode <bpt id="p1">**</bpt>populateTimesheetWeekFromEntry<ept id="p1">**</ept> kann auch erweitert werden, wenn das benutzerdefinierte Feld, das dem Objekt <bpt id="p2">**</bpt>TSTimesheetEntry<ept id="p2">**</ept> zugeordnet ist, erneut in die Datenbanktabelle TSTimesheetLineweek schreiben muss.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>The following example saves the <bpt id="p1">**</bpt>firstOption<ept id="p1">**</ept> or <bpt id="p2">**</bpt>secondOption<ept id="p2">**</ept> value that the user selects to the database as a raw string value.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Das folgende Beispiel speichert die Werte <bpt id="p1">**</bpt>firstOption<ept id="p1">**</ept> oder <bpt id="p2">**</bpt>secondOption<ept id="p2">**</ept>, die der Benutzer auswählt, in der Datenbank als unformatierter Zeichenfolgenwert.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>If the database field is a field of the <bpt id="p1">**</bpt>Enum<ept id="p1">**</ept> type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wenn das Datenbankfeld ein Feld vom Typ <bpt id="p1">**</bpt>Enumeration<ept id="p1">**</ept> ist, können diese Werte manuell einem Enumerationswwert zugeordnet werden und dann in einem Enumerationsfeld in der Datenbanktabelle gespeichert werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Show a custom field in the timesheet header section</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Anzeigen eines benutzerdefinierten Felds im Abschnitt Arbeitszeittabellen-Kopfzeile</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Below is a screenshot from the mobile app of a user viewing a timesheet.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Unten befindet sich ein Bildschirmfoto von der mobilen App. Es zeigt einen Benutzer, der die Arbeitszeittabelle anzeigt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The "More information" button has been selected in the upper-right corner to show the "View more details" option.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die Schaltfläche „Weitere Informationen“ in der rechten oberen Ecke ist ausgewählt worden, um die Option „Weitere Details anzeigen“ anzuzeigen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>View more details command</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Weitere Details anzeigen – Befehl</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Below is a screenshot from the mobile app showing the “More” section of a timesheet.</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Unten befindet sich ein Bildschirmfoto von der mobilen App. Es zeigt den Abschnitt „Mehr“ in der Arbeitszeittabelle.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ein benutzerdefiniertes Feld mit der Bezeichnung „Benutzungsrate der Arbeitszeittabelle (berechnetes benutzerdefiniertes Feld)“ ist dem Arbeitszeittabellen-Kopfzeilenabschnitt hinzugefügt worden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>A read-only value of "0.667" is set on the custom field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ein schreibgeschützter Wert „0,667“ ist im benutzerdefinierten Feld festgelegt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>More section</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">Weiterer Abschnitt</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Extend the TSTimesheetTable table so that it has a custom field</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match">Erweitern der TSTimesheetTable-Tabelle, sodass sie ein benutzerdefiniertes Feld hat</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">In typischen Szenarien ist es wahrscheinlich, dass die Daten für ein benutzerdefiniertes Feld im Kopfzeilenabschnitt aus der TSTimesheetHeader-Tabelle entnommen werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</source><target logoport:matchpercent="97" state="translated" state-qualifier="fuzzy-match">Allerdings können andere Tabellen verwendet werden, wenn die Daten auf Basis eines TSTimesheetTable-Datensatzes abgerufen werden können, oder wenn sie keinen spezifischen Datensatzkontext haben (beispielsweise wenn das Feld in den Projektparametern als schreibgeschützt festgelegt wird).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Note that custom fields don't have to have any backing database records.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Beachten Sie, dass benutzerdefinierte Felder keine unterstützenden Datenbank-Datensätze haben müssen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>They can be dynamically generated based on X++ logic.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Sie können auf Grundlage der X++-Logik dynamisch generiert werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>The example that follows shows this approach.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Das Beispiel, das folgt, zeigt diesen Ansatz.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Fields in the header section are always read-only in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Felder im Kopfzeilenabschnitt sind immer in der App immer schreibgeschützt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Verwenden der Befehlskette in der Methode buildCustomFieldList der Klasse TSTimesheetSettings zum Anzeigen eines Felds im Kopfzeilenabschnitt</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>This code controls the display settings for the field in the app.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Dieser Code steuert die Anzeigeeinstellungen für das Feld in der App.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Er steuert beispielsweise den Feldtyp, die Bezeichnung, ob das Feld ein Pflichtfeld ist und in welchem Abschnitt das Feld angezeigt wird.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>The following example shows a computed value in the header section in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Das folgende Beispiel zeigt einen berechneten Wert im Kopfzeilenabschnitt in der App an.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Verwenden der Befehlskette in der Methode buildCustomFieldListForHeader der Klasse TSTimesheetDetails zum Eingeben von Werten in Arbeitszeittabellen-Details</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>The <bpt id="p1">**</bpt>buildCustomFieldListForHeader<ept id="p1">**</ept> method is used to fill in the timesheet header details in the mobile app.</source><target logoport:matchpercent="71" state="translated" state-qualifier="fuzzy-match">Die Methode <bpt id="p1">**</bpt>buildCustomFieldListForHeader<ept id="p1">**</ept> wird verwendet, um die Arbeitszeittabellen-Kopfzeilendetails in der mobilen App einzugeben.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>It takes a TSTimesheetTable record as a parameter.</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Sie übernimmt einen TSTimesheetTable-Datensatz als Parameter.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Fields from that record can be used to fill in the custom field value in the app.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Felder aus diesem Datensatz können verwendet werden, um den benutzerdefinierten Feldwert in der App auszufüllen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>The following example doesn't read any values from the database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Im folgenden Beispiel werden keine Werte aus der Datenbank gelesen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Instead, it uses X++ logic to generate a computed value that is then shown in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Stattdessen wird eine X++-Logik verwendet, um einen berechneten Wert zu generieren, der dann in der App angezeigt wird.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Other configurability/extensibility opportunities</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Andere Konfigurierberkeits-/Erweiterbarkeits-Verkaufschancen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Adding additional validation for the app</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Zusätzliche Überprüfung für die App hinzufügen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Existing logic for timesheet functionality at the database level will still work as expected.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Vorhandene Logik für die Arbeitszeittabellen-Funktion auf der Datenbankebene funktioniert noch wie erwartet.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>To interrupt the completion of save or submit operations and show a specific error message, you can add <bpt id="p1">**</bpt>throw error("message to user")<ept id="p1">**</ept> to the code via a chain of command extension.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Um den Abschluss der Speicher- oder Sendevorgänge zu unterbrechen und eine spezifische Fehlermeldung anzuzeigen, können Sie dem Code <bpt id="p1">**</bpt>throw error("message to user")<ept id="p1">**</ept> über eine Befehlskettenerweiterung hinzufügen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Here are three examples of useful extensible methods:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Nachfolgend finden Sie drei Beispiele von nützlichen erweiterbaren Methoden:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>If <bpt id="p1">**</bpt>validateWrite<ept id="p1">**</ept> on the TSTimesheetLine table returns <bpt id="p2">**</bpt>false<ept id="p2">**</ept> during a save operation for a timesheet line, an error message is shown in the mobile app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wenn <bpt id="p1">**</bpt>validateWrite<ept id="p1">**</ept> in der TSTimesheetLine-Tabelle <bpt id="p2">**</bpt>false<ept id="p2">**</ept> während eines Speichervorgangs für eine Arbeitszeittabellen-Position zurückgibt, wird eine Fehlermeldung in der mobilen App angezeigt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>If <bpt id="p1">**</bpt>validateSubmit<ept id="p1">**</ept> on the TSTimesheetTable table returns <bpt id="p2">**</bpt>false<ept id="p2">**</ept> during timesheet submission in the app, an error message is shown to the user.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Wenn <bpt id="p1">**</bpt>validateSubmit<ept id="p1">**</ept> in der TSTimesheetTable-Tabelle <bpt id="p2">**</bpt>false<ept id="p2">**</ept> während der Arbeitszeittabellen-Übermittlung in der App zurückgibt, wird dem Benutzer eine Fehlermeldung angezeigt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Logic that fills in fields (for example, <bpt id="p1">**</bpt>Line Property<ept id="p1">**</ept>) during the <bpt id="p2">**</bpt>insert<ept id="p2">**</ept> method on the TSTimesheetLine table will still run.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Logik die Felder ausfüllt (zum Beispiel <bpt id="p1">**</bpt>Positionseigenschaft<ept id="p1">**</ept>) während die <bpt id="p2">**</bpt>insert<ept id="p2">**</ept>-Methode in der Tabelle TSTimesheetLine immer noch ausgeführt wird.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Hiding and marking out-of-box fields as read-only via configuration</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ausblenden und Markieren vorkonfigurierter Felder als schreibgeschützt über eine Konfiguration</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Von den Projektparametern aus können Sie vorkonfigurierte Felder in der mobilen App mit einem Schreibschutz versehen oder ausblenden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Set the options in the <bpt id="p1">**</bpt>Mobile timesheets<ept id="p1">**</ept> section on the <bpt id="p2">**</bpt>Timesheet<ept id="p2">**</ept> tab of the <bpt id="p3">**</bpt>Project management and accounting parameters<ept id="p3">**</ept> page.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Legen Sie die Optionen im Abschnitt <bpt id="p1">**</bpt>Mobile Arbeitszeittabellen<ept id="p1">**</ept> unter der Registerkarte <bpt id="p2">**</bpt>Arbeitszeittabelle<ept id="p2">**</ept> der Seite <bpt id="p3">**</bpt>Projektverwaltungs- und Buchhaltungsparameter<ept id="p3">**</ept> fest.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Project parameters</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Projektparameter</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Changing the activities that are available for selection via extensions</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die Aktivitäten ändern, die zur Auswahl über Erweiterungen verfügbar sind</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>The activities that are available for selection for a project are filled in via the <bpt id="p1">**</bpt>getActivitiesForProject()<ept id="p1">**</ept> and <bpt id="p2">**</bpt>getActivityQuery()<ept id="p2">**</ept> methods in the <bpt id="p3">**</bpt>TsTimesheetProjectService<ept id="p3">**</ept> class.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die Aktivitäten, die zur Auswahl für ein Projekt verfügbar sind, werden über die Methoden <bpt id="p1">**</bpt>getActivitiesForProject()<ept id="p1">**</ept> und <bpt id="p2">**</bpt>getActivityQuery()<ept id="p2">**</ept> in der Klasse <bpt id="p3">**</bpt>TsTimesheetProjectService<ept id="p3">**</ept> eingegeben.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sie können eine Befehlskette verwenden, um dieses Verhalten zu ändern, damit es Ihrem Geschäftsszenario entspricht. Das gilt für die Aktivitäten, die für ein bestimmtes Projekt zur Auswahl stehen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Entering a default project category on timesheet entries</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Eingeben einer Standardprojektkategorie in Arbeitszeittabellen-Einträge</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Entry of a default project category on timesheet entries occurs at three levels.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Eingabe einer standardmäßigen Projektkategorie in Arbeitszeittabellen-Einträgen erfolgt auf drei Ebenen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sie können Befehlsketten verwenden, um das Verhalten auf irgendeine oder alle dieser Ebenen auszudehnen, um das gewünschte Verhalten zu erreichen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>The following hierarchy is used:</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Die folgende Hierarchie wird verwendet:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>The app tries to put the default category from the project resource.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die App versucht, die Standardkategorie aus der Projektressource zu platzieren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>This default category is set in the <bpt id="p1">**</bpt>getCurrentUserResource<ept id="p1">**</ept> and <bpt id="p2">**</bpt>getDelegatedResourcesForCurrentUser<ept id="p2">**</ept> methods in the <bpt id="p3">**</bpt>TSTimesheetSettingsService<ept id="p3">**</ept> class.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Diese Standardkategorie wird in den Methoden <bpt id="p1">**</bpt>getCurrentUserResource<ept id="p1">**</ept> und <bpt id="p2">**</bpt>getDelegatedResourcesForCurrentUser<ept id="p2">**</ept> in der Klasse <bpt id="p3">**</bpt>TSTimesheetSettingsService<ept id="p3">**</ept> festgelegt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wenn die Standardkategorie nicht auf der Projektressourcenebene bereitgestellt wird, versucht die App, sie aus der Projektaktivität zu beziehen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>This default category is set in the <bpt id="p1">**</bpt>getActivitiesForProject<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> class.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Diese Standardkategorie wird in der Methode <bpt id="p1">**</bpt>getActivitiesForProject<ept id="p1">**</ept> in der Klasse <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> festgelegt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Wenn die Standardkategorie nicht auf der Projektaktivitätsebene bereitgestellt wird, wird die Standardkategorie aus den Projektparametern bezogen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>This default category is set in the <bpt id="p1">**</bpt>getProjectDetailsbyRule<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> class.</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">Diese Standardkategorie wird in der Methode <bpt id="p1">**</bpt>getProjectDetailsbyRule<ept id="p1">**</ept> in der Klasse <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> festgelegt.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>