---
title: Unterstützte primitive Datentypen für elektronische Berichtsformeln
description: Dieses Thema enthält Informationen zu den primitiven Datentypen, die in Formeln für die elektronische Berichterstellung (EB) unterstützt werden.
author: NickSelin
ms.date: 06/02/2021
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72c372a4d9b6af337731ff0bbd750b3b58f27bb79cb3813a0b5e4f79707d9f5c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730606"
---
# <a name="supported-primitive-data-types-for-electronic-reporting-formulas"></a>Unterstützte primitive Datentypen für elektronische Berichtsformeln

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen zu den primitiven Datentypen, die in Ausdrücke für die [elektronische Berichterstellung (EB)](general-electronic-reporting.md) unterstützt werden. Hier ist eine Liste der Typen der primitiven Daten:

- [boolean](#boolean)
- [Datum](#date)
- [datetime](#datetime)
- [enumeration](#enumeration)
- [guid](#guid)
- [integer](#integer)
- [int64](#int64)
- [real](#real)
- [string](#string)

## <a name="boolean"></a><a name="boolean"></a>Aktiv

Der primitive Datentyp *boolean* enthält einen Wert, der entweder als *wahr* oder *falsch* bewertet wird. Sie können die reservierten Literalschlüsselwörter **Wahr** und **Falsch** überall verwenden, wo ein *boolescher* Ausdruck erwartet wird. Der Standardwert ist *Falsch*.

Die interne Darstellung eines *boolean* ist eine *Integer*. Der *Ganzzahl*-Wert 0 (Null) wird als *falsch* bewertet, und alle anderen *Ganzzahl*-Werte werden als *wahr* bewertet. Wenn Sie einen konfigurierten Ausdruck [bestätigen](general-electronic-reporting-formula-designer.md#TestFormula), der einen *boolean* im [EB-Formeldesigner](er-advanced-formula-editor.md) zurückgibt, präsentiert das Testergebnisfenster *0* (null), wenn ein Ausdruck *falsch* zurückgibt. Andernfalls wird im Testergebnisbereich *1* angezeigt.

Ein *boolean* hat keine impliziten Konvertierungen. Sie können jedoch die Funktion [TEXT](er-functions-text-text.md) zum expliziten Konvertieren von *boolean* zu einer *Zeichenfolge*:

- Der *falsche* Wert wird in die Textzeichenfolge **Falsch** umgewandelt.
- Der *wahre* Wert wird in die Textzeichenfolge **Wahr** umgewandelt.

> [!NOTE]
> Diese Konvertierung hängt nicht vom [Kontext](er-design-multilingual-reports.md) der bereitgestellten Sprache und Kultur ab.

Vergleichs [operatoren](er-formula-language.md#Operators) sind der einzige Operatortyp, der mit demDatentyp *boolean* verwendet werden kann. Die folgenden Operatoren können verwendet werden, um zwei *boolesche* Werte zu vergleichen: \<\> und =.

## <a name="date"></a><a name="date"></a>Datum

Der primitive Datentyp *Datum* enthält Tag, Monat und Jahr. Daten können mit folgenden Funktionen initiiert werden:

- [DATEVALUE](er-functions-datetime-datevalue.md)
- [NULLDATE](er-functions-datetime-nulldate.md)
- [SESSIONTODAY](er-functions-datetime-sessiontoday.md)
- [TODAY](er-functions-datetime-today.md)

Der Datentyp *Datum* kann Daten zwischen dem 1. Januar 1900 und dem 31. Dezember 2154 enthalten. Der Standardwert ist **Null**, und die interne Darstellung ist das Datum 1. Januar 1900.

Ein *Datum* hat keine impliziten Konvertierungen. Sie können jedoch die folgenden expliziten Konvertierungsfunktionen verwenden:

- [DATEFORMAT](er-functions-datetime-dateformat.md)
- [DATETODATETIME](er-functions-datetime-datetodatetime.md)
- [TEXT](er-functions-text-text.md)

Mit der [ADDDAYS](er-functions-datetime-adddays.md)-Funktion können Sie Tage von Datumsangaben hinzufügen und davon subtrahieren. Auf diese Weise können Sie das Datum um eine bestimmte Anzahl von Tagen in die Zukunft und in die Vergangenheit verschieben. Mit der [DAYS](er-functions-datetime-days.md)-Funktion können Sie Daten voneinander subtrahieren und die Differenz in Tagen berechnen. Weitere Informationen zur Transformation von *Datums* werten, siehe [Liste der EB-Funktionen in der Katgorie „Datum und Uhrzeit“](er-functions-category-datetime.md).

Vergleichs [operatoren](er-formula-language.md#Operators) sind der einzige Operatortyp, der mit dem Datentyp *Datum* verwendet werden kann. Die folgenden Operatoren können verwendet werden, um zwei *Datums* werte zu vergleichen: \<\>, \<, \<=, =, \>, und \>=.

## <a name="datetime"></a><a name="datetime"></a>Datetime

Der primitive Datentyp *datetime* kombiniert den Typ *Datum* und einen Wert, der die seit Mitternacht vergangene Zeit darstellt. Die Zeit wird in Stunden, Minuten, Sekunden und Sekundenbruchteilen angegeben. Ein *datetime*-Wert enthält auch Informationen über die Zeitzone.

Der Datentyp *datetime* kann Daten zwischen dem 1. Januar 1900 (1900-01-01T00:00:00.0000000+00:00 im Round-Trip-[Format](/dotnet/standard/base-types/standard-date-and-time-format-strings)) und 31. Dezember, 2154 (2154/12/31T11:59:59.9999999+00:00 im Round-Trip-Format) enthalten. Die kleinste Zeiteinheit in einer *datetime* ist eine Zehnmillionstelsekunde.

> [!NOTE]
> Wenn der **hh**-[Bezeichner](/dotnet/standard/base-types/standard-date-and-time-format-strings) für Stunden verwendet wird, können Zeitwerte über 12:59:59:9999999 nicht als gültige Zeiten interpretiert werden.
>
> Wenn der **HH**-Bezeichner für Stunden verwendet wird, können Zeitwerte über 23:59:59:9999999 nicht als gültige Zeiten interpretiert werden.

Der Standardwert ist **Null**, und die interne Darstellung ist das Datum 1. Januar 1900 (1900-01-01T00:00:00.0000000+00:00 im Roundtrip-Format).

Datetimes können mit folgenden Funktionen initiiert werden:

- [DATETIMEVALUE](er-functions-datetime-datetimevalue.md)
- [NULNULLDATETIMELDATE](er-functions-datetime-nulldatetime.md)
- [SESSIONNOW](er-functions-datetime-sessionnow.md)
- [NOW](er-functions-datetime-now.md)

Ein *datetime* hat keine impliziten Konvertierungen. Sie können jedoch die folgenden expliziten Konvertierungsfunktionen verwenden:

- [DATETIMEFORMAT](er-functions-datetime-datetimeformat.md)
- [TEXT](er-functions-text-text.md)

Weitere Informationen zur Transformation von *datetime*-Werten, siehe [Liste der EB-Funktionen in der Katgorie „Datum und Uhrzeit“](er-functions-category-datetime.md).

Vergleichs [operatoren](er-formula-language.md#Operators) sind der einzige Operatortyp, der mit dem Datentyp *datetime* verwendet werden kann. Die folgenden Operatoren können verwendet werden, um zwei *datetime*-Werte zu vergleichen: \<\>, \<, \<=, =, \>, und \>=.

## <a name="enumeration"></a><a name="enumeration"></a>Aufzählung

Der primitive Datentyp *Enumeration* ist eine Liste von Literalen. Sie können Aufzählungen verwenden, die in der Anwendung [Quellcode](../dev-ref/xpp-data-primitive.md#enum) definiert sind. Sie können auch Ihre eigenen Aufzählungen in die Komponenten EB-[Datenmodell](general-electronic-reporting.md#data-model-and-model-mapping-components) und EB-[Format](general-electronic-reporting.md#FormatComponentOutbound) einführen.

Eine Anwendung *Enumeration* kann in Ausdrücken jedes EB-Modell-Mappings und EB-Formats verwendet werden.

Die folgende Abbildung zeigt, wie Sie die Modellenumeration **CustVendCorrectiveReasonCode** zum bearbeitbaren EB-Datenmodell hinzufügen.

[![Eine Modellenumeration im EB-Datenmodelldesigner konfigurieren.](./media/er-formula-supported-data-types-primitive-enum1.gif)](./media/er-formula-supported-data-types-primitive-enum1.gif)

Eine Modell *enumeration* kann in Ausdrücken aller EB-Modellzuordnungen und EB-Formate verwendet werden, die unter einem Datenmodell erstellt wurden, in dem die *Enumeration* wurde vorgestellt.

Die folgende Abbildung zeigt, wie Sie die Formatenumeration **Liste der Natura-Verlagerungsunterkategorien** in das bearbeitbare ER-Format.

[![Eine Formatenumeration im EB-Formatdesigner konfigurieren.](./media/er-formula-supported-data-types-primitive-enum2.gif)](./media/er-formula-supported-data-types-primitive-enum2.gif)

Eine Format *enumeration* kann nur in Ausdrücken des EB-Formats verwendet werden, in denen die *Enumeration* wurde vorgestellt.

Sie müssen den entsprechenden Typ von EB-Datenquellen verwenden, um eine bestimmte Enumeration als Konstante oder als Wert, den der Benutzer, der eine EB-Lösung ausführt, im Dialogfeld zur Laufzeit definiert hat, in eine konfigurierte EB-Komponente zu bringen.

- Auf Anwendungsenumeration kann zugegriffen werden, indem Sie die Datenquellen **Dynamics 365 for Operations \ Aufzählung** und **Allgemein \ Benutzereingabeparameter** Datenquellen verwenden. Die folgende Abbildung zeigt, wie Sie dem bearbeitbaren EB-Format die Datenquellen **BlinddarmNeinJa** und **uipNeinJa** hinzufügen, die sich auf die Anwendungsenumeration **NoYes** beziehen.

    [![Hinzufügen von Anwendungsenumerationsdatenquellen im EB-Formatdesigner.](./media/er-formula-supported-data-types-primitive-enum3a.gif)](./media/er-formula-supported-data-types-primitive-enum3a.gif)

- Auf Datenmodellenumeration kann zugegriffen werden, indem Sie die Datenquellen **Datenmodell \ Enumeration** und **Datenmodell \ Enumerationsbenutzereingabeparameter** verwenden. Die folgende Abbildung zeigt, wie Sie dem bearbeitbaren EB-Format die Datenquelle **CustVendCorrectiveReasonCode** hinzufügen, die sich auf die Anwendungsenumeration **CustVendCorrectiveReasonCode** bezieht.

    [![Hinzufügen von Modellenumerationsdatenquellen im EB-Formatdesigner.](./media/er-formula-supported-data-types-primitive-enum3b.gif)](./media/er-formula-supported-data-types-primitive-enum3b.gif)

- Auf Formatenumeration kann zugegriffen werden, indem Sie die Datenquellen **Format \ Enumeration** und **Format \ Enumerationsbenutzereingabeparameter** verwenden. Die folgende Abbildung zeigt, wie Sie dem bearbeitbaren EB-Format die Datenquelle **NaturaReverseCharge** hinzufügen, die sich auf die Formatenumeration **Natura-Verlagerungsunterkategorien** bezieht.

    [![Hinzufügen von Formatenumerationsdatenquellen im EB-Formatdesigner.](./media/er-formula-supported-data-types-primitive-enum3c.gif)](./media/er-formula-supported-data-types-primitive-enum3c.gif)

Eine *Enumeration* hat keine impliziten Konvertierungen. Sie können jedoch die Konvertierungsfunktion [TEXT](er-functions-text-text.md) zum Konvertieren einer *Enumeration* zu einer Textzeichenfolge. Diese Konvertierung ist nicht sprachabhängig. Informationen dazu, wie Sie einen *Enumerations* wert einem entsprechenden sprachspezifischen Label zuordnen können, finden Sie in den Verwendungsbeispielen für die Funktionen [LISTOFFFIELDS](er-functions-list-listoffields.md) und [GETENUMVALUEBYNAME](er-functions-text-getenumvaluebyname.md).

Vergleichs [operatoren](er-formula-language.md#Operators) sind der einzige Operatortyp, der mit dem Datentyp *Enumeration* verwendet werden kann. Die folgenden Operatoren können verwendet werden, um zwei *Enumerations* werte zu vergleichen: \<\> und =.

## <a name="guid"></a><a name="guid"></a>Guid

Der primitive Datentyp *guid* enthält einen Global Unique Identifier (GUID)-Wert. Eine GUID ist ein Wert, der auf allen Computern und Netzwerken verwendet werden kann, wo immer eine eindeutige Kennung erforderlich ist. Es ist unwahrscheinlich, dass die Nummer verdoppelt wird. Eine gültige GUID erfüllt alle folgenden Spezifikationen:

- Es müssen 32 hexadezimale Ziffern vorhanden sein.
- Darüber hinaus müssen vier Bindestriche an den folgenden Stellen eingebettet sein: 8-4-4-4-12.
- Zusätzlich können optionale Klammern \{\} am Anfang und Ende der Zeichenfolge hinzugefügt werden. Zum Beispiel sind beide **\{2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212\}** und **2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212** gültige GUID-Zeichenfolgen.
- Daher müssen insgesamt 36 oder 38 Zeichen vorhanden sein, je nachdem, ob geschweifte Klammern hinzugefügt werden.
- Die als Hexadezimalziffern verwendeten Buchstaben können Großbuchstaben (A–F), Kleinbuchstaben (a–f) oder gemischt sein.

Sie können die folgenden expliziten Konvertierungsfunktionen verwenden:

- [GUIDVALUE](er-functions-text-guidvalue.md)
- [TEXT](er-functions-text-text.md)

Vergleichs [operatoren](er-formula-language.md#Operators) sind der einzige Operatortyp, der mit dem Datentyp *guid* verwendet werden kann. Die folgenden Operatoren können verwendet werden, um zwei *guid*-Werte zu vergleichen: \<\> und =.

## <a name="integer"></a><a name="integer"></a>Ganzzahl

Der primitive Datentyp *Ganzzahl* stellt eine Zahl dar, die keine Dezimalstellen hat. Ganzzahlen werden als Kontrollvariablen in sich wiederholenden Anweisungen oder als Indizes in Datensatzlisten verwendet.

Ein *Ganzzahl* ist die ganze Zahl, wie sie direkt in einen EB-[Ausdruck](general-electronic-reporting-formula-designer.md#formula-designer-overview) (Formel) eingegeben wird, wie zum Beispiel **12345**. Ein *Ganzzahl* ist 32 Bit breit. Der Standardwert ist **0**, und die interne Darstellung ist eine lange Zahl. Eine *Ganzzahl* wird automatisch in eine *echte* umgewandelt.

Zusätzlich können die folgenden expliziten Konvertierungsfunktionen verwendet werden:

- [INTVALUE](er-functions-conversion-intvalue.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)

Der Bereich einer *Ganzzahl* ist \[-2,147,483,647: 2,147,483,647\]. Alle ganzen Zahlen dieses Bereichs können als Literale verwendet werden.

Alle Vergleiche und mathematischen [Operatoren](er-formula-language.md#Operators) kann mit dem Datentyp *Ganzzahl* verwendet werden.

## <a name="int64"></a><a name="int64"></a>Int64

Der primitive Datentyp *int64* stellt eine Zahl dar, die keine Dezimalstellen hat. *Int64*-Werte werden als Kontrollvariablen in sich wiederholenden Anweisungen oder als Datensatzbezeichner verwendet.

Ein *int64* ist 64 Bit breit. Der Standardwert ist **0**, und die interne Darstellung ist eine lange Zahl. Ein *int64* wird automatisch in eine *echte* umgewandelt.

Zusätzlich können die folgenden expliziten Konvertierungsfunktionen verwendet werden:

- [INT64VALUE](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)

Der Bereich einer *int64* ist \[-9,223,372,036,854,775,807: 9,223,372,036,854,775,807\].

Alle Vergleiche und mathematischen [Operatoren](er-formula-language.md#Operators) kann mit dem Datentyp *int64* verwendet werden.

## <a name="real"></a><a name="real"></a>Gleitkommazahl

Der primitive Datentyp *echt* kann neben ganzen Zahlen auch Dezimalwerte enthalten. Sie können Dezimalliterale überall verwenden, wo ein *echter* erwartet wird. Ein Dezimalliteral ist die Dezimalzahl, wie sie direkt im Code eingegeben wird, wie z. B. **2.19**.

> [!NOTE]
> In EB-Ausdrücken wird immer ein Punkt (.) als Dezimaltrennzeichen verwendet.

Reelle Zahlen können in allen Ausdrücken verwendet werden, und sie können sowohl mit Vergleichs- als auch mit arithmetischen Operatoren verwendet werden. Eine *echte* hat eine Genauigkeit von 16 signifikanten Stellen. Der Standardwert für eine *echte* ist **0.0**, und die interne Darstellung ist eine binär codierte digitale (BCD) Zahl. Die BCD-Codierung ermöglicht exakte Darstellungen von Werten, die Vielfache von 0,1 sind. Die Reichweite von einer *echten* Variable ist -(10)<sup>127</sup> bis (10)<sup>127</sup>. Alle reellen Zahlen in diesem Bereich können als Literale in EB-Ausdrücken verwendet werden.

Eine *echte* hat keine impliziten Konvertierungen. Sie können jedoch die folgenden Funktionen verwenden, um eine *echte* zu anderen Datentypen und anderen Datentypen zu einer *echten* signifikant umzuwandeln:

- [INTVALUE](er-functions-conversion-intvalue.md)
- [INT64VALUE](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)
- [VALUE](er-functions-conversion-value.md)

Alle Vergleiche und mathematischen [Operatoren](er-formula-language.md#Operators) kann mit dem Datentyp *echt* verwendet werden.

## <a name="string"></a><a name="string"></a>Zeichenfolge

Der primitive Datentyp *Zeichenfolge* stellt eine Folge von Zeichen dar, die als Texte, Kontonummern, Adressen und Telefonnummern verwendet werden.

*Zeichenfolgen* literale sind Zeichen, die in Anführungszeichen ("") eingeschlossen sind. *Zeichenfolge* literale können überall verwendet werden, wo *Zeichenfolge* werte in EB-Ausdrücken erwartet werden. Sie können Zeichenfolgen in logischen Ausdrücken verwenden, z. B. in Vergleichen. Sie können auch *Zeichenfolge* werte verketten, indem Sie den **\&** Operator oder die Funktion [CONCATENATE](er-functions-text-concatenate.md) verwenden.

> [!NOTE]
> Wenn Sie zwei *Zeichenfolge* werte verketten, und Sie wollen, dass die resultierende *Zeichenfolge* mehr als eine Zeile umfassent, verwenden Sie das Zeilenumbruchtrennzeichen zwischen den Werten. Für die TEXT-Ausgabe kann dieses Trennzeichen ein Zeichen sein, das mit dem Ausdruck [CHAR](er-functions-text-char.md)(10) oder CHAR(13) generiert wird. Für HTML kann es das Tag **\<br\>** sein.

Der Standardwert für eine *Zeichenfolge* ist eine leere Textzeichenfolge ohne Zeichen, und die interne Darstellung ist eine Liste von Zeichen.

Es gibt keine automatischen Konvertierungen für Strings. Sie können jedoch die folgenden expliziten Konvertierungsfunktionen verwenden:

- [CHAR](er-functions-text-char.md)
- [FORMAT](er-functions-text-format.md)
- [LEFT](er-functions-text-left.md)
- [LEN](er-functions-text-len.md)
- [MID](er-functions-text-mid.md)
- [PADLEFT](er-functions-text-padleft.md)
- [REPLACE](er-functions-text-replace.md)
- [RIGHT](er-functions-text-right.md)
- [TEXT](er-functions-text-text.md)
- [TRANSLATE](er-functions-text-translate.md)
- [TRIM](er-functions-text-trim.md)
- [UPPER](er-functions-text-upper.md)

Weitere Informationen zur Transformation von *Zeichenfolge* werten, siehe [Liste der EB-Funktionen der Listenkategorie](er-functions-category-text.md).

Eine *Zeichenfolge* kann eine unbestimmte Anzahl von Zeichen enthalten.

Alle Vergleiche und mathematischen [Operatoren](er-formula-language.md#Operators) kann mit dem Datentyp *Zeichenfolge* verwendet werden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)
- [Formelsprache in der elektronischen Berichterstellung](er-formula-language.md)
- [Unterstützte zusammengesetzte Datentypen](er-formula-supported-data-types-composite.md)
