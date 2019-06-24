---
title: Formeldesigner in der elektronischen Berichterstellung (EB)
description: In diesem Artikel wird beschrieben, wie den Formel-Designer in der elektronischen Berichterstattung (ER) verwendet wird.
author: NickSelin
manager: AnnBe
ms.date: 05/14/2014
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85d2370353520ee588dfe2aedf9998d707f0eda6
ms.sourcegitcommit: 97ed74889a09ef385f6ecbab69e84a05ff42ee41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/20/2019
ms.locfileid: "1592659"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>Formeldesigner in der elektronischen Berichterstellung (EB)

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie den Formel-Designer in der elektronischen Berichterstattung (ER) verwendet wird. Wenn Sie ein Format für ein bestimmtes elektronisches Dokument in EB entwerfen, können Sie Formeln zum Transformieren von Daten verwenden, sodass sie den Anforderungen für die Dokumenterfüllung und Formatierung zu entsprechen. Diese Formeln ähneln Formeln in Microsoft Excel. Unterschiedliche Arten von Funktionen werden in den Formeln unterstützt: Text, Datum und Uhrzeit, Mathematisches, Logisches, Informationen, Datentypumrechnung und andere (domänenspezifische Funktionen des Unternehmens).

## <a name="formula-designer-overview"></a>Formeldesignerübersicht

EB unterstützt den Formeldesigner. Daher können Sie zum Zeitpunkt des Entwurfs Ausdrücke konfigurieren, die für folgende Aufgaben zur Laufzeit verwendet werden können:

- Transformation Sie Daten, die von einer Microsoft Dynamics 365 for Finance and Operations-Datenbank empfangen werden und in ein EB-Datenmodell eingegeben werden sollen, das so konzipiert wurde, dass es als Datenquelle für EB-Formate dient. (Diese Transformationen können beispielsweise Filterung, Gruppierung und Datentypkonvertierung umfassen.)
- Formatieren Sie Daten, die an ein generierendes elektronisches Dokument in Übereinstimmung mit dem Layout und den Bedingungen eines spezifischen EB-Formats übermittelt werden müssen. (Die Formatierung kann beispielsweise in Übereinstimmung mit der angeforderten Sprache oder Kultur oder der Codierung erfolgen).
- Steuern Sie den Prozess der Erstellung elektronischer Dokumente. (Die Ausdrücke können beispielsweise die Ausgabe bestimmter Elemente des Formats aktivieren oder deaktivieren, abhängig von der Verarbeitung von Daten. Sie können auch den Dokumenterstellungsprozess unterbrechen oder Nachrichten an Benutzer auslösen.)

Sie können die Seite **Formeldesigner** öffnen, wenn Sie irgendeine der folgenden Aktionen ausführen:

- Binden von Datenquellenartikeln zu den Datenmodellkomponenten.
- Binden von Datenquellenartikeln zu den Datenformatkomponenten.
- Verwaltung von berechneten Feldern, die Teil von Datenquellen sind, abschließen.
- Definition von Sichtbedingungen für Benutzereingabeparameter.
- Entwurf der Umwandlungen des Formats.
- Definition der Aktivierung von Bedingungen für die Komponenten des Formats.
- Definition von Dateinamen für die DATEIkomponenten des Formats.
- Definition der Bedingungen für Prozesssteuerprüfungen.
- Definition der Nachrichtentextes für Prozesssteuerprüfungen.

## <a name="designing-er-formulas"></a>Entwerfen der ER-Formeln

### <a name="data-binding"></a>Datenbindung

Der EB-Formeldesigner kann verwendet werden, um einen Ausdruck zu definieren, der Daten transformiert, die von Datenquellen empfangen werden, sodass die Daten beim Datenkonsument zur Laufzeit eingegeben werden können:

- Von Finance and Operations-Datenquellen und -Laufzeitparametern zu einem EB-Datenmodell
- Von einem ER-Datenmodell zu einem ER-Format
- Von Finance and Operations-Datenquellen und -Laufzeitparametern zu einem EB-Format

Die folgende Abbildung zeigt das Design eines Ausdrucks dieses Typs. In diesem Beispiel wird durch den Ausdruck der Wert des Felds **Intrastat.AmountMST** der Intrastat-Tabelle in Finance and Operations auf zwei Dezimalstellen gerundet und dann der gerundete Wert zurückgegeben.

[![Datenbindung](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

Die folgende Abbildung zeigt, wie ein Ausdruck dieses Typs verwendet werden kann. In diesem Beispiel wird das Ergebnis des entworfenen Ausdrucks in die Komponente **Transaction.InvoicedAmount** des Datenmodells **Steuererklärungsmodell** eingegeben.

[![Datenbindung, die verwendet wird](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Zur Laufzeit rundet die entworfene Formel **ROUND (Intrastat.AmountMST, 2)** den Wert des Felds **AmountMST** für jeden Datensatz in der Intrastat-Tabelle auf zwei Dezimalstellen. Sie gibt dann den gerundeten Wert in der Komponente **Transaction.InvoicedAmount** des Datenmodells **Steuererklärung** ein.

### <a name="data-formatting"></a>Datenformatierung

Der ER-Formeldesigner kann verwendet werden, um einen Ausdruck zu definieren, der Daten umwandelt, die von den Datenquellen empfangen werden, sodass die Daten als Teil zum Erstellen eines elektronischen Dokuments gesendet werden können. Möglicherweise haben Sie Formatierung, die als eine typische Regel angewendet werden muss, die für ein Format erneut verwendet werden muss. In diesem Fall können Sie diese Formatierung einmal in der Formatkonfiguration einführen, als benannte Transformation, die einen Formatierungsausdruck hat. Diese benannte Transformation kann dann mit vielen Formatkomponenten verknüpft werden, wobei die Ausgabe gemäß dem Formatierungsausdruck formatiert werden muss, den Sie erstellt haben.

Die folgende Abbildung zeigt das Design einer Umwandlung dieses Typs. In diesem Beispiel kürzt die **TrimmedString**-Tansformation eingehende Daten des Datentyps **Zeichenfolge**, indem führende und nachfolgende Leerzeichen entfernt werden. Sie gibt dann einen gekürzten Zeichenfolgenwert zurück.

[![Umwandlung](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

Die folgende Abbildung zeigt, wie die Umwandlung dieses Typs verwendet werden kann. In diesem Beispiel senden mehrere Formatkomponenten Text als Ausgabe an das generierende elektronische Dokument zur Laufzeit. Alle diese Formatkomponenten verweisen auf die Transformation **TrimmedString** nach Name.

[![Transformation, die verwendet wird](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Wenn Formatkomponenten, wie beispielsweise die Komponente **partyName** in der vorausgehenden Abbildung, auf die Transformation **TrimmedString** verweisen, übermittelt die Transformation Text als Ausgabe an das generierende elektronische Dokument. Dieser Text umfasst keine vor- und nachgestellten Leerzeichen.

Wenn Sie eine Formatierung haben, die einzeln angewendet werden muss, kann sie als einzelner Ausdruck der Bindung einer bestimmten Formatkomponente eingeführt werden. Die folgende Abbildung zeigt einen Ausdruck dieses Typs. In diesem Beispiel wird die Formatkomponente **partyType** an die Datenquelle über einen Ausdruck gebunden, der die eingehenden Daten aus dem Feld **Model.Company.RegistrationType** in der Datenquelle in Text in Großbuchstaben konvertiert. Der Ausdruck sendet dann diesen Text als Ausgabe an das elektronische Dokument.

[![Anwenden der Formatierung auf eine einzelne Komponente](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Prozessflusssteuerung

Der EB-Formeldesigner kann verwendet werden, um Ausdrücke zu definieren, die den Prozessfluss zum Generieren elektronischer Dokumenten steuern. Die folgenden Aufgaben können ausgeführt werden:

- Definiert Bedingungen, wenn ein Dokumentenerstellungsprozess gestoppt werden muss.
- Geben Sie Ausdrücke an, die entweder Nachrichten für den Benutzer über beendete Prozess erstellen oder Ausführungsprotokollnachrichten zum fortlaufenden Prozess der Berichterstellung auslösen.
- Geben Sie die Dateinamen zum Generieren elektronischer Dokumente an, und steuern Sie die Bedingungen ihrer Erstellung.

Jede Regel der Prozessflusssteuerung ist als einzelne Prüfung entworfen. Die folgende Abbildung zeigt die Überprüfung dieses Typs. Ist hier eine Erläuterung der Konfiguration in diesem Beispiel:

- Die Überprüfung wird ausgewertet, wenn der **INSTAT** Knoten während der Generierung der XML-Datei erstellt wird.
- Wenn die Transaktionsliste leer ist, stoppt die Überprüfung den Ausführungsprozess und gibt **FALSCH** zurück.
- Die Überprüfung gibt eine Fehlermeldung zurück, der den Text der Beschriftung SYS70894 von Finance and Operations in der bevorzugten Sprache des Benutzers umfasst.

[![Validierung](./media/picture-validation.jpg)](./media/picture-validation.jpg)

Der EB-Formeldesigner wird auch verwendet, um einen Dateinamen für ein generierendes elektronisches Dokument zu generieren und den Dateierstellungsprozess zu steuern. Die folgende Abbildung zeigt das Design einer Prozessablaufsteuerung dieses Typs. Ist hier eine Erläuterung der Konfiguration in diesem Beispiel:

- Die Liste der Datensätze aus der Datenquelle **model.Intrastat** wird in Chargen aufgeteilt. Jede Charge enthält bis zu 1.000 Datensätze.
- Die Ausgabe erstellt eine ZIP-Datei, die eine Datei im XML-Format für jede Charge enthält, die erstellt wurde.
- Ein Ausdruck gibt einen Dateinamen für das Generieren von elektronischen Dokumenten zurück, indem er den Dateinamen und die Dateinamenerweiterung verkettet. Für die zweite und alle nachfolgenden Chargen enthält der Dateiname die Chargenkennung als Suffix.
- Ein Ausdruck aktiviert (durch Rückgabe von **WAHR**) den Dateierstellungsprozess für Chargen, die mindestens einen Datensatz beinhalten.

[![Dateisteuerelement](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Grundlegende Syntax

Er-Ausdrücke können einzelne oder alle folgenden Elemente enthalten:

- Konstanten
- Operatoren
- Verweise
- Pfade
- Funktionen

#### <a name="constants"></a>Konstanten

Wenn Sie Ausdrücke entwerfen, können Sie Text und numerische Konstanten (das heißt Werte, die nicht berechnet werden) verwenden. So verwendet beispielsweise der Ausdruck **WERT ("100") + 20** die numerische Konstante **20** und die Zeichenfolgenkonstante **"100"**, und gibt den numerischen Wert **120** zurück. Der EB-Formeldesigner unterstützt Escapesequenzen. Daher können Sie eine Ausdruckszeichenfolge angeben, die anders behandelt werden soll. Beispielsweise gibt der Ausdruck **“Leo Tolstoi ""Krieg und Frieden"" Band 1** folgende Textzeichenfolge zurück **Leo Tolstoi "Krieg und Frieden" Band 1**.

#### <a name="operators"></a>Operatoren

Die folgende Tabelle zeigt die arithmetischen Operatoren, die Sie verwenden können, um grundlegende mathematische Arbeitsgänge auszuführen, wie Addition, Subtraktion, Multiplikation und Division.

| Operator | Dies bedeutet               | Beispiel |
|----------|-----------------------|---------|
| +        | Hinzufügung              | 1+2     |
| -        | Subtraktion, Negation | 5-2, -1 |
| \*       | Multiplikation        | 7\*8    |
| /        | Geschäftsbereich              | 9/3     |

In der folgenden Tabelle werden die Vergleichsoperatoren angezeigt, die unterstützt werden. Sie können diese Operatoren verwenden, um zwei Werte zu vergleichen.

| Operator | Dies bedeutet                  | Beispiel    |
|----------|--------------------------|------------|
| =        | Gleich                    | X=Y        |
| &gt;     | Größer als             | X&gt;Y     |
| &lt;     | Kleiner als                | X&lt;Y     |
| &gt;=    | Größer oder gleich | X&gt;=Y    |
| &lt;=    | Kleiner oder gleich    | X&lt;=Y    |
| &lt;&gt; | Ungleich             | X&lt;&gt;Y |

Darüber hinaus können Sie auch ein kaufmännisches Und-Zeichen (&) als Textverkettungsoperator verwenden. Auf diese Weise können Sie eine oder mehrere Textzeichenfolgen zu einem einzigen Stück Text verbinden oder verketten.

| Bediener | Dies bedeutet     | Beispiel                                             |
|----------|-------------|-----------------------------------------------------|
| &        | Verketten | „Nichts zu drucken” & „:&nbsp;” & „keine Datensätze gefunden” |

##### <a name="operator-precedence"></a>Vorrangigkeit

Die Reihenfolge, in der die Teile eines zusammengesetzten Ausdrucks ausgewertet werden, ist wichtig. Beispielsweise variiert das Ergebnis des Ausdrucks **1 + 4 / 2**, je nachdem, ob der Additionsvorgang oder der Divisionsvorgang zuerst erfolgt. Sie können Klammern verwenden, um explizit zu definieren, wie ein Ausdruck ausgewertet werden soll. Beispielsweise um anzugeben, dass die Addition zuerst ausgeführt werden soll, können Sie den vorhergehenden Ausdruck abändern auf **(1 + 4) / 2**. Wenn Sie die Reihenfolge der Vorgänge, die in einem Ausdruck ausgeführt werden müssen, nicht explizit angeben, basiert die Reihenfolge auf der standardmäßigen Prioritätsreihenfolge, die den unterstützten Operatoren zugewiesen ist. Die folgende Tabelle zeigt die Prioritätsreihenfolge an, die jedem Operator zugewiesen ist. Operatoren, die eine höhere Rangfolge haben, (beispielsweise 7), werden vor Operatoren ausgewertet, die eine niedrigere Rangfolge haben, (beispielsweise 1).

| Priorität | Operatoren      | Syntax                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | Gruppieren       | ( … )                                                                   |
| 6          | Mitgliedszugriff  | … . …                                                                   |
| 5          | Funktionsaufrufe  | … ( … )                                                                 |
| 4          | Multiplikation | … \* …<br>… / …                                                         |
| 3          | Ergänzung       | … + …<br>… - …                                                          |
| 2          | Vergleich     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Trennung     | … , …                                                                   |

Wenn ein Ausdruck mehrere aufeinander folgende Operatoren enthält, die dieselbe Rangfolge haben, werden diese Arbeitsgänge von links nach rechts ausgewertet. Beispielsweise der Ausdruck **1 + 6 / 2 \* 3 &gt; 5** gibt **WAHR** zurück. Es wird empfohlen, dass Sie Klammern verwenden, um die gewünschte Reihenfolge der Arbeitsgänge für Ausdrucke explizit anzugeben, damit Ausdrücke besser lesbar und verwaltbar sind.

#### <a name="references"></a>Verweise

Alle Datenquellen der aktuellen EB-Komponente, die während des Entwurfs eines Ausdrucks verfügbar sind, können als benannte Referenzen verwendet werden. (Die aktuellen EB-Komponente kann entweder ein Modells oder ein Format sein.) Zum Beispiel enthält das aktuelle EB-Datenmodell die Datenquelle **ReportingDate**, und diese Datenquelle gibt einen Wert des Datentyps **DATETIME** zurück. Um diesen Wert im generierenden Dokument korrekt zu formatieren, können Sie auf die Datenquelle im Ausdruck als **DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")** verweisen.

Allen Zeichen im Namen einer verweisenden Datenquelle, die keinen Buchstaben des Alphabets darstellen, muss ein einfaches Anführungszeichen (') vorausgehen. Wenn der Name einer verweisenden Datenquelle, der mindestens ein Symbol enthält, das keinen Buchstaben des Alphabets darstellt, muss der Name in einfache Anführungszeichen gesetzt werden. (Diese nichtalphabetischen Symbole können Satzzeichen oder andere geschriebene Symbole sein.) Hier sind einige Beispiele:

- Auf die Datenquelle **Aktuelles Datum & Zeit** muss in einem EB-Ausdruck als **'Heutiges Datum & Zeit’** verwiesen werden.
- Auf die Methode **name()** der Datenquelle **Kunden** muss in einem EB-Ausdruck als **Customers.'name()'** verwiesen werden.

Wenn die Methoden von Finance and Operations-Datenquellen Parameter besitzen, wird der folgende Syntax verwendet, um diese Methoden aufzurufen:

- Wenn die Methode **isLanguageRTL** der Datenquelle **System** einen Parameter **EN-US** des Datentyps **Zeichenfolge** hat, muss auf diese Methode in einem EB-Ausdruck als **System.'isLanguageRTL'("EN-US")** verwiesen werden.
- Anführungszeichen sind nicht erforderlich, wenn ein Methodenname nur alphanumerische Symbole enthält. Sie sind jedoch für eine Methode einer Tabelle erforderlich, wenn der Name Klammern enthält.

Wenn die Datenquelle **System** einer EB-Zuordnung hinzugefügt wird, die auf die Finance and Operations-Anwendungsklasse **Global** verweist, gibt der Ausdruck den booleschen Wert **FALSCH** zurück. Der geänderte Ausdruck **System.' isLanguageRTL'("AR")** gibt den booleschen Wert **WAHR** zurück.

Sie können die Art und Weise eingrenzen, in der Werte an die Parameter dieses Methodentyps übergeben werden:

- Nur Konstanten können an andere Methoden dieses Typs übergeben werden. Die Werte der Konstanten werden zur Entwurfszeit definiert.
- Nur primitive (grundlegende) Datentypen werden für Parameter dieses Typs unterstützt. (Die primitiven Datentypen sind ganze Zahlen, tatsächlich, boolesch, Zeichenfolgen, usw.)

#### <a name="paths"></a>Pfade

Wenn ein Ausdruck auf eine strukturierte Datenquelle verweist, können Sie die Pfadbeschreibung verwenden, um ein bestimmtes primitives Element dieser Datenquelle auszuwählen. Ein Punktzeichen (. ) wird verwendet, um einzelne Elemente einer strukturierten Datenquelle zu unterteilen. Zum Beispiel enthält das aktuelle EB-Datenmodell die Datenquelle **InvoiceTransactions**, und diese Datenquelle gibt eine Liste von Datensätzen zurück. Die **InvoiceTransactions**-Datensatzstruktur enthält die Felder **AmountDebit** und **AmountCredit**, und diese beiden Felder geben numerische Werte zurück. Sie können daher den folgenden Ausdruck zum Berechnen des Rechnungsbetrag wie folgt konzipieren: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**.

#### <a name="functions"></a>Funktionen

Im nächsten Abschnitt wird die Funktionen beschrieben, die in ER-Ausdrücken verwendet werden können. Alle Datenquellen des Ausdruckskontexts (das aktuelle EB-Datenmodell oder EB-Format) können als Parameter von aufrufenden Funktionen in Übereinstimmung mit der Liste von Argumenten zum Aufrufen von Funktionen verwendet werden. Konstanten können auch als Parameter aufrufender Funktionen verwendet werden. Zum Beispiel enthält das aktuelle EB-Datenmodell die Datenquelle **InvoiceTransactions**, und diese Datenquelle gibt eine Liste von Datensätzen zurück. Die **InvoiceTransactions**-Datensatzstruktur enthält die Felder **AmountDebit** und **AmountCredit**, und diese beiden Felder geben numerische Werte zurück. Um daher den Rechnungsbetrag zu berechnen, können Sie den folgenden Ausdruck entwerfen, der die integrierte EB-Rundungsfunktion verwendet: **ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**.

## <a name="supported-functions"></a>Unterstützte Funktionen

Die folgenden Tabellen beschreiben die Datenmanipulationsfunktion, die Sie verwenden können, um ER-Datenmodelle und ER-Berichte zu entwerfen. Die Liste von Funktionen ist nicht unveränderlich festgelegt. Entwickler können sie erweitern. Um die Liste von Funktionen anzuzeigen, die Sie verwenden können, öffnen Sie den Funktionsbereich im EB-Formeldesigner zu.

### <a name="date-and-time-functions"></a>Datums- und Zeitfunktionen

| Funktion | Beschreibung | Beispiel |
|----------|-------------|---------|
| TAG HINZUFÜGEN (Datetime, Tage) | Fügt die angegebene Anzahl von Tagen dem angegebenen Datum/Uhrzeit-Wert hinzu. | **TAGE HINZUFÜGEN (JETZT (), 7)** gibt das Datum und die Uhrzeit sieben Tage in der Zukunft zurück. |
| DATETODATETIME (Datum) | Konvertiert den angegebenen Datumswert in einen Datums-/Uhrzeitwert. | **DATETODATETIME (CompInfo. 'getCurrentDate() ')** gibt das Datum der aktuellen Finance and Operations-Sitzung, 24. Dezember 2015, als **12/24/2015 12:00: 00 AM** zurück. In diesem Beispiel ist **CompInfo** eine EB-Datenquelle des Typs **Finance and Operations/Tabelle** und bezieht sich auf die Tabelle „CompanyInfo”. |
| JETZT () | Gibt das aktuelle Finance and Operations-Anwendungsserverdatum und -uhrzeit als ein Datums-/Uhrzeitwert zurück. | |
| HEUTE () | Gibt das aktuelle Finance and Operations-Anwendungs-Serverdatum und die Zeit als ein Datumswert zurück. | |
| NULLDATE () | Gibt einen **Null**-Datumswert zurück. | |
| NULLDATETIME () | Gibt einen **Null**-Datums-/Uhrzeitwert zurück. | |
| DATETIMEFORMAT "datetime, Format) | Konvertiert den angegebenen Datums-/Uhrzeitwert in eine Zeichenfolge im angegebenen Format. (Informationen zu unterstützten Formaten, finden Sie unter [Standard](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) und [Benutzerdefiniert](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "dd-MM-yyyy")** gibt das laufende Finance and Operations-Anwendungsserverdatum, 24. Dezember 2015, als **"24-12-2015"** basierend auf dem angegebenen benutzerdefinierten Format zurück. |
| DATETIMEFORMAT "datetime, Format, Kultur) | Konvertiert den angegebenen Datums-/Uhrzeitwert in eine Zeichenfolge im angegebenen Format und [Kultur](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Informationen zu unterstützten Formaten, finden Sie unter [Standard](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) und [Benutzerdefiniert](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "d", "de")** gibt das aktuelle Finance and Operations Anwendungsserverdatum, 24. Dezember 2015, als **"24.12.2015"** basierend auf der ausgewählten deutschen Kultur zurück. |
| SESSIONTODAY () | Gibt das aktuelle Finance and Operations-Sitzungsdatum als Datumswert zurück. | |
| SESSIONNOW () | Gibt das aktuelle Finance and Operations-Sitzungsdatum und -uhrzeit als ein Datums-/Uhrzeitwert zurück. | |
| DATENFORMAT (Datum, Format) | Gibt eine Zeichenfolgendarstellung des angegebenen Datums im angegebenen Format zurück. | **DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy")** gibt das aktuelle Finance and Operations-Sitzungsdatum, 24. Dezember 2015, als **"24-12-2015"** basierend auf dem angegebenen benutzerdefinierten Format zurück. |
| DATENFORMAT (Datum, Format, Kultur) | Konvertieren Sie den angegebenen Datumswert in eine Zeichenfolge im angegebenen Format und der entsprechenden [Kultur](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Informationen zu unterstützten Formaten, finden Sie unter [Standard](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) und [Benutzerdefiniert](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** gibt das aktuelle Finance and Operations-Sitzungsdatum, 24. Dezember 2015, als **"24.12.2015"** basierend auf der ausgewählten deutschen Kultur zurück. |
| DAYOFYEAR (Datum) | Gibt eine ganzzahlige Darstellung der Anzahl von Tagen zwischen dem 1. Januar dem angegebenen Datum zurück. | **DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))** gibt **61** zurück. **DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))** gibt **1** zurück. |
| DAYS (date 1, date 2) | Gibt die Anzahl der Tage zwischen dem ersten angegebenen Datum und dem zweiten angegebenen Datum zurück. Gibt einen positiven Wert zurück, wenn das erste Datum nach dem zweiten Datum liegt, gibt **0** (null) zurück, wenn das erste Datum gleich dem zweiten Datum ist oder gibt einen negativen Wert zurück, wenn das erste Datum vor dem zweiten Datum liegt. | **DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS(NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))** gibt **-1** zurück. |

### <a name="data-conversion-functions"></a>Datenumwandlungsfunktionen

| Funktion | Beschreibung | Beispiel |
|----------|-------------|---------|
| DATETODATETIME (Datum) | Konvertiert den angegebenen Datumswert in einen Datums-/Uhrzeitwert. | **DATETODATETIME (CompInfo. 'getCurrentDate() ')** gibt das Datum der aktuellen Finance and Operations-Sitzung, 24. Dezember 2015, als **12/24/2015 12:00: 00 AM** zurück. In diesem Beispiel ist **CompInfo** eine EB-Datenquelle des Typs **Finance and Operations/Tabelle** und bezieht sich auf die Tabelle „CompanyInfo”. |
| DATEVALUE (Zeichenfolge, Format) | Gibt eine Datumsdarstellung der angegebenen Zeichenfolge im angegebenen Format zurück. | **DATEVALUE ("21-Dez-2016", "dd-MMM-yyyy")** gibt das Datum 21. Dezember 2016 basierend auf dem benutzerdefinierten Format und der **EN-US**-Kultur der Standardanwendung zurück. |
| DATEVALUE (Zeichenfolge, Format, Kultur) | Gibt eine Datumsdarstellung der angegebenen Zeichenfolge im angegebenen Format und Kultur zurück. | **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")** gibt das Datum 21. Januar 2016 basierend auf dem angegebenen benutzerdefinierten Format und Kultur zurück. Allerdings löst **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")** eine Ausnahme aus, um den Benutzer zu informieren, dass die angegebene Zeichenfolge nicht als gültiges Datum anerkannt wird. |
| DATETIMEVALUE (Zeichenfolge, Format) | Gibt eine Datums-/Uhrzeitdarstellung der angegebenen Zeichenfolge im angegebenen Format zurück. | **DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")** gibt 02:55:00 Uhr am 21. Dezember 2016 zurück, basierend auf dem angegebenen benutzerdefinierten Format und der **EN-US**-Kultur der Standardanwendung. |
| DATETIMEVALUE (Zeichenfolge, Format, Kultur) | Gibt eine Datums-/Uhrzeitdarstellung der angegebenen Zeichenfolge im angegebenen Format und Kultur zurück. | **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")** gibt 02:55:00 Uhr am 21. Dezember 2016 zurück, basierend auf dem angegebenen benutzerdefinierten Format und Kultur. Allerdings löst **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")** eine Ausnahme aus, um den Benutzer zu informieren, dass die angegebene Zeichenfolge nicht als gültiges Datum/Uhrzeit anerkannt wird. |

### <a name="list-functions"></a>Listenfunktionen

<table>
<thead>
<tr>
<th>Funktion</th>
<th>Beschreibung</th>
<th>Beispiel</th>
</tr>
</thead>
<tbody>
<tr>
<td>TEILEN (Eingabe, Länge)</td>
<td>Teilen Sie die angegebene Eingabezeichenfolge in Teilzeichenfolgen, von denen jede die angegebene Länge hat. Geben Sie das Ergebnis als neue Liste zurück.</td>
<td><strong>TEILEN (&quot;abcd&quot;, 3)</strong> gibt eine neue Liste zurück, die aus zwei Datensätzen besteht, die ein Feld <strong>ZEICHENFOLGE</strong> haben. Das Feld im ersten Datensatz enthält den Text <strong>&quot;ABC&quot;</strong> und das Feld im zweiten Datensatz beinhaltet den Text <strong>&quot;D&quot;</strong>.</td>
</tr>
<tr>
<td>TEILEN (Eingabe, Trennzeichen)</td>
<td>Teilen Sie die angegebene Eingabezeichenfolge in Teilzeichenfolgen, von denen jede die angegebene Länge hat.</td>
<td><strong>TEILEN (&quot;XAb aBy&quot;, &quot;aB&quot;)</strong> gibt eine neue Liste zurück, die aus ei Datensätzen besteht, die ein Feld <strong>ZEICHEN</strong> hat. Das Feld im ersten Datensatz enthält den Text <strong>&quot;X&quot;</strong>, das Feld im zweiten Datensatz den Text &quot;&nbsp;&quot;, und das Feld im dritten Datensatz enthält den Text <strong>&quot;y&quot;</strong>. Wenn Trennzeichen leer ist, wird eine neue Liste zurückgegeben, die aus einem Datensatz, besteht der ein Feld <strong>ZEICHENFOLGE</strong> hat, das den Eingabetext enthält. Falls die Eingabe leer ist, wird eine neue leere Liste zurückgegeben.
Wenn Eingabe oder Trennzeichen nicht definiert ist (Null), wird eine Bewerbungsausnahme ausgelöst.</td>
</tr>
<tr>
<td>TEILUNGSLISTE (Liste, Nummer)</td>
<td>Teilt die angegebene Liste in Chargen, die jeweils die angegebene Anzahl von Datensätzen enthalten. Geben Sie das Ergebnis als neue Liste von Chargen zurück, die die folgenden Elemente enthält:
<ul>
<li>Chargen als regelmäßige Listen (<strong>Wert</strong>-Komponente)</li>
<li>Die aktuelle Chargennummer (<strong>Chargennummer</strong>-Komponente)</li>
</ul>
</td>
<td>In der folgenden Abbildung wird eine Datenquelle <strong>Positionen</strong> als eine Datensatzliste von drei Datensätze erstellt. Diese Liste wird in Chargen aufgeteilt, die jeweils bis zu zwei Datensätze enthalten.
<p><a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>Die folgende Abbildung zeigt das entworfene Formatlayout. In diesem Formatlayout werden die Bindungen an die Datenquelle <strong>Positionen</strong> erstellt, mit Ausgabe im XML-Format zu generieren. Dies Ausgabe präsentiert einzelne Knoten für jede Charge und die darin befindlichen Datensätze.</p>
<p><a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a></p>
<p>Die folgende Abbildung zeigt das Ergebnis, wenn das entworfene Format ausgeführt wird.</p>
<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>
</td>
</tr>
<tr>
<td>LIST (record 1 [, record 2, …])</td>
<td>Gibt eine neue Liste zurück,, die von den angegebenen Argumenten erstellt wird.</td>
<td><strong>LISTE (model.MainData, model.OtherData)</strong> gibt einen leeren Datensatz zurück, in dem die Liste der Felder alle Felder der <strong>Hauptdaten</strong> und der <strong>Anderen Daten</strong> der Datensatzliste enthält.</td>
</tr>
<tr>
<td>LISTJOIN (list 1, list 2, …)</td>
<td>Gibt eine neue Liste zurück, die von den angegebenen Argumenten erstellt wird.</td>
<td><strong>LISTJOIN (SPLIT (&quot;abc&quot;, 1), SPLIT (&quot;def&quot;, 1))</strong> gibt eine Liste von sechs Datensätzen zurück, in der ein Feld des Datentyps <strong>ZEICHENFOLGE</strong> einzelne Buchstaben enthält.</td>
</tr>
<tr>
<td>ISEMPTY (Liste)</td>
<td>Gibt <strong>WAHR</strong> zurück, wenn die angegebene Liste keine Elemente enthält. Andernfalls wird <strong>FALSCH</strong> zurückgegeben.</td>
<td></td>
</tr>
<tr>
<td>EMPTYLIST (Liste)</td>
<td>Gibt eine leere Liste zurück, indem die angegebene Liste wie eine Quelle für die Listenstruktur verwendet wird.</td>
<td><strong>EMPTYLIST (SPLIT (&quot;abc&quot;, 1))</strong> gibt eine neue leere Liste zurück, die dieselbe Struktur wie die Liste hat, die durch Funktion <strong>TEILEN</strong> zurückgegeben wird.</td>
</tr>
<tr>
<td>ZUERST (Liste)</td>
<td>Gibt den ersten Datensatz der angegebenen Liste zurück, wenn dieser Datensatz nicht leer ist. Andernfalls ergibt sich eine Ausnahme.</td>
<td></td>
</tr>
<tr>
<td>FIRSTORNULL (Liste)</td>
<td>Gibt den ersten Datensatz der angegebenen Liste zurück, wenn dieser Datensatz nicht leer ist. Andernfalls wird ein <strong>NULL</strong> Datensatz zurückgegeben.</td>
<td></td>
</tr>
<tr>
<td>LISTOFFIRSTITEM (Liste)</td>
<td>Gibt eine Liste zurück, die nur das erste Element der gegebenen Liste enthält.</td>
<td></td>
</tr>
<tr>
<td>ALLITEMS (Pfad)</td>
<td>Diese Funktion wurde als Auswahl im Arbeitsspeicher ausgeführt. Es wird eine neue, vereinfachte Liste zurückgegeben, die alle Elemente darstellt, die dem angegebenen Pfad entsprechen. Der Pfad muss als gültiger Datenquellenpfad eines Datenquellenelements eines Datensatzlisten-Datentyps definiert werden. Datenelemente, wie beispielsweise die Pfadzeichenfolge und Datum, sollten ein Fehler im EB-Ausdrucksgenerator zur Entwurfszeit erzeugen.</td>
<td>Wenn Sie <strong>TEILEN (&quot;abcdef&quot;, 2)</strong> als Datenquelle (DS) eingeben, wird <strong>ANZAHL (ALLITEMS (DS.Value))</strong> zurückgegeben <strong>3</strong>.</td>
</tr>
<tr>
<td>ALLITEMSQUERY (Pfad)</td>
<td>Diese Funktion wird als verknüpfte SQL-Abfrage ausgeführt. Es wird eine neue, vereinfachte Liste zurückgegeben, die alle Elemente darstellt, die dem angegebenen Pfad entsprechen. Der angegebene Pfad muss als gültiger Datenquellenpfad eines Datenquellenelements eines Datensatzliste-Datentyps definiert sein und mindestens eine Relation enthalten. Datenelemente, wie beispielsweise die Pfadzeichenfolge und Datum, sollten ein Fehler im EB-Ausdrucksgenerator zur Entwurfszeit erzeugen.</td>
<td>Definieren Sie die folgenden Datenquellen in Ihrer Modellzuordnung:
<ul>
<li><strong>CustInv</strong> (<strong>Tabellendatensätze</strong>-Typ), der auf die CustInvoiceTable-Tabelle verweist</li> 
<li><strong>FilteredInv</strong> (<strong>Berechnetes Feld</strong>-Typ), der den Ausdruck <strong>FILTER (CustInv, CustInv.InvoiceAccount = &quot;US-001&quot;)</strong> enthält</li>
<li><strong>JourLines</strong> (<strong>Berechnetes Feld</strong>-Typ), der den gewünschten Ausdruck <strong>ALLITEMSQUERY (FilteredInv.'&lt;Relations'.CustInvoiceJour.'&lt;Relations'.CustInvoiceTrans)</strong> enthält</li>
</ul>
<p>Wenn Sie Ihre Modellzuordnung ausführen, um die Datenquelle <strong>JourLines</strong> aufzurufen, wird die folgende SQL-Anweisung ausgeführt:</p>
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN CUSTINVOICETRANS T3 WHERE...
</td>
</tr>
<tr>
<td>ORDERBY (Liste [, Ausdruck 1, Ausdruck 2,...])</td>
<td>Geben Sie die angegebenen Liste zurück, nachdem sie gemäß der angegebenen Argumente sortiert wurde. Diese Argumente können als Ausdrücke definiert werden.</td>
<td>Wenn <strong>Lieferant</strong> als EB-Datenquelle konfiguriert wurde, die sich auf die Tabelle „VendTable” bezieht, gibt <strong>ORDERBY (Vendors, Vendors.'name()')</strong> eine Liste von Lieferanten zurück, die nach Name in aufsteigender Reihenfolge sortiert ist.</td>
</tr>
<tr>
<td>UMKEHREN (Liste)</td>
<td>Gibt die angegebene Liste in umgekehrter Sortierreihenfolge zurück.</td>
<td>Wenn <strong>Lieferant</strong> als EB-Datenquelle konfiguriert wurde, die sich auf die Tabelle „VendTable” bezieht, gibt <strong>REVERSE (ORDERBY (Vendors, Vendors.'name()')) )</strong> eine Liste von Kreditoren zurück, die nach Namen in absteigender Reihenfolge sortiert ist.</td>
</tr>
<tr>
<td>WO (Liste, Bedingung)</td>
<td>Gibt die angegebene Liste zurück, nachdem sie gemäß der angegebenen Bedingung gefiltert wurde. Die angegebene Bedingung wird auf die Liste im Arbeitsspeicher angewendet. Hierin unterscheidet sich die Funktion <strong>WO</strong> von der Funktion <strong>FILTER</strong>.</td>
<td>Wenn <strong>Lieferant</strong> als EB-Datenquelle konfiguriert wurde, die sich auf die Tabelle „VendTable” bezieht, gibt <strong>WHERE(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> eine Liste von ausschließlich den Lieferanten zurück, die zur Lieferantengruppe 40 gehören.</td>
</tr>
<tr>
<td>Aufzählung (LISTE)</td>
<td>Gibt eine neue Liste zurück, die aus aufgezählten Datensätzen der angegebenen Liste besteht und die folgende Elemente verfügbar macht:
<ul>
<li>Angegebene Listendatensätze als regelmäßige Listen (<strong>Wert</strong>-Komponente)</li>
<li>Der Index des aktuellen Datensatzes (<strong>Nummer</strong>-Komponente)</li>
</ul>
</td>
<td>In der folgenden Abbildung wird eine Datenquelle <strong>Aufgezählt</strong> als Aufzählungsliste von Lieferantendatensätzen von der Datenquelle <strong>Lieferanten</strong> erstellt, die sich auf die Tabelle „VendTable” bezieht.
<p><a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a></p>
<p>Die folgende Abbildung zeigt das Format. In diesem Format werden Datenbindungen erstellt, um eine Ausgabe im XML-Format zu generieren. In dieser Ausgabe werden einzelne Lieferanten als aufgezählte Knoten präsentiert.</p>
<p><a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a></p>
<p>Die folgende Abbildung zeigt das Ergebnis, wenn das entworfene Format ausgeführt wird.</p>
<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>
</td>
</tr>
<tr>
<td>ZÄHLEN (Liste)</td>
<td>Gibt die erste Zahl des Datensatzes der angegebenen Liste zurück, wenn dieser Datensatz nicht leer ist. Andernfalls wird <strong>0</strong> (Null) zurückgegeben.</td>
<td><strong>ANZAHL (TEILEN (&quot;abcd&quot;, 3))</strong> gibt <strong>2</strong> zurück, da die Funktion <strong>TEILEN</strong> eine Liste erstellt, die aus zwei Datensätzen besteht.</td>
</tr>
<tr>
<td>LISTOFFIELDS (Pfad)</td>
<td>Gibt eine Datensatzliste zurück, die von einem Argument von einem der folgenden Typen erstellt wird:
<ul>
<li>Modellenumeration</li>
<li>Formatenumeration</li>
<li>Behälter</li>
</ul>
<p>Die Liste, die erstellt wird, besteht aus Datensätzen, die die folgenden Felder haben:</p>
<ul>
<li>Name</li>
<li>Beschriftung</li>
<li>Beschreibung</li>
</ul>
Zur Laufzeit geben die Felder <strong>Beschriftung</strong> und <strong>Beschreibung</strong> Werte basierend auf den Spracheinstellungen des Formats zurück.
</td>
<td>In der folgenden Abbildung wird eine Aufzählung in einem Datenmodell vorgestellt.
<p><a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a></p>
<p>Die folgende Abbildung zeigt diese Details an:</p>
<ul>
<li>Die Modellaufzählung ist eingefügt in einen Bericht als Datenquelle.</li>
<li>Ein EB-Ausdruck verwendet die Modellaufzählung als Parameter der Funktion <strong>LISTOFFIELDS</strong>.</li>
<li>Eine Datenquelle des Datensatzlistentyp wird in einen Bericht eingefügt mithilfe des EB-Ausdrucks, der erstellt wird.</li>
</ul>
<p><a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a></p>
<p>Das folgende Beispiel zeigt die EB-Formatelemente, die an die Datenquelle des Datensatzlistentyps gebunden sind, der mithilfe der Funktion <strong>LISTOFFIELDS</strong> erstellt wurde.</p>
<p><a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a></p>
<p>Die folgende Abbildung zeigt das Ergebnis, wenn das entworfene Format ausgeführt wird.</p>
<p><a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a></p>
<blockquote>[!NOTE] Basierend auf den Spracheinstellungen des Formats von übergeordneten DATEI- und ORDNER-Elementen, wird übersetzter Text für Beschriftungen und Beschreibungen in der Ausgabe des EB-Formats eingegeben.</blockquote>
</td>
</tr>
<tr>
<td>LISTOFFIELDS (path, language)</td>
<td>Gibt eine Datensatzliste zurück, die aus einem Argument erstellt wurde, wie beispielsweise eine Modellaufzählung, eine Formataufzählung oder ein Container. Die Liste, die erstellt wird, besteht aus Datensätzen, die die folgenden Felder haben:
<ul>
<li>Name</li>
<li>Beschriftung</li>
<li>Beschreibung</li>
<li>IstÜbersetzt</li>
</ul>
Zur Laufzeit geben die Felder <strong>Beschriftung</strong> und <strong>Beschreibung</strong> Werte basierend auf den Spracheinstellungen des Formats und der angegebenen Sprache zurück. Das Feld <strong>Wurde übersetzt</strong> gibt an, dass das Feld <strong>Beschriftung</strong> in die angegebene Sprache übersetzt wurde.
</td>
<td>Beispielsweise verwenden Sie den Datenquellentyp <strong>Berechnetes Feld</strong>, um die Datenquellen <strong>enumType_de</strong> und <strong>enumType_deCH</strong> für die Datenmodellaufzählung <strong>enumType</strong> zu konfigurieren:
<ul>
<li>enumType_de = <strong>LISTOFFIELDS</strong> (enumType, &quot;de&quot;)</li>
<li>enumType_deCH = <strong>LISTOFFIELDS</strong> (enumType, &quot;de-CH&quot;)</li>
</ul>
<p>In diesem Fall können Sie den folgenden Ausdruck verwenden, um die Beschriftung des Aufzählungswerts in Schweizer Deutsch abzurufen, wenn diese Übersetzung verfügbar ist. Wenn die schweizerdeutsche Übersetzung nicht verfügbar ist, ist das Etikett auf Deutsch.</p>
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
</td>
</tr>
<tr>
<td>STRINGJOIN (Liste, Feldname, Trennzeichen)</td>
<td>Gibt eine Zeichenfolge zurück, die aus verketteten Werten des angegebenen Felds aus der angegebenen Liste besteht. Die Werte sind durch das angegebene Trennzeichen getrennt.</td>
<td>Wenn Sie <strong>SPLIT(&quot;abc&quot; , 1)</strong> als Datenquelle (DS) eingeben, gibt <strong>STRINGJOIN (DS, DS.Value, &quot;-&quot;)</strong> <strong>&quot;a-b-c&quot;</strong> zurück.</td>
</tr>
<tr>
<td>SPLITLISTBYLIMIT (Liste, Grenzwert, Grenzquelle)</td>
<td>Teilt die angegebene Liste in eine neue Liste von Unterlisten und gibt das Ergebnis im Datensatz-Listeninhalt zurück. Der Parameter <strong>Grenzwert</strong> definiert den Wert der Begrenzung für die Teilung der ursprünglichen Liste. Der Parameter <strong>Grenzquelle</strong> gibt den Schritt an, in dem die Gesamtsumme erhöht wird. Die Begrenzung wird auf keinen einzelnen Artikel der ursprünglichen Liste angewendet, wenn die Begrenzungsquelle die definierte Begrenzung überschreitet.</td>
<td>Die folgende Abbildung zeigt ein Format. 
<p><a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a></p>
<p>Die folgende Abbildung zeigt die Datenquellen an, die für das Format verwendet werden.</p>
<p><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a></p>
<p>Die folgende Abbildung zeigt das Ergebnis an, wenn Format ausgeführt wird. In diesem Fall ist die Ausgabeliste eine flache Liste von Warenartikeln.</p>
<p><a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a></p>
<p>In den folgenden Abbildungen ist dasselbe Format so angepasst worden, dass es die Liste der Warenpositionen in Chargen präsentiert, wenn eine einzelne Charge Waren enthalten muss und das Gesamtgewicht nicht die Begrenzung von 9 überschreiten sollte.</p>
<p><a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a></p>
<p><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a></p>
<p>Die folgende Abbildung zeigt das Ergebnis, wenn das angepasste Format ausgeführt wird.</p>
<p><a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a></p>
<blockquote>[!NOTE] Die Begrenzung wird nicht auf den letzten Artikel der ursprünglichen Liste angewendet, weil der Wert (11) der Begrenzungsquelle (Gewicht) die definierte Begrenzung (9) überschreitet. Verwenden Sie entweder die Funktion <strong>WO</strong> oder den Ausdruck <strong>Aktiviert</strong> des entsprechenden Formatelements, um Unterlisten während der Berichtgenerierung, nach Bedarf, zu ignorieren (zu überspringen).</blockquote>
</td>
</tr>
<tr>
<td>FILTER (Liste, Bedingungen)</td>
<td>Gibt die angegebene Liste zurück, nachdem die Abfrage geändert wurde, um nach der angegebenen Bedingung zu filtern. Diese Funktion unterscheidet sich von der Funktion <strong>WO</strong>, da die angegebene Bedingung auf jede beliebige EB-Datenquelle des Typs <strong>Tabellendatensätze</strong> auf Datenbankebene angewendet wird. Die Liste und die Bedingung können definiert werden, indem Tabellen und Relationen verwendet werden.</td>
<td>Wenn <strong>Lieferant</strong> als EB-Datenquelle konfiguriert wurde, die sich auf die Tabelle „VendTable” bezieht, gibt <strong>FILTER (Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> eine Liste von ausschließlich den Lieferanten zurück, die zur Lieferantengruppe 40 gehören. Wenn <strong>Kreditor</strong> als ER-Datenquelle konfiguriert ist, die auf die Tabelle VendTable verweist, und wenn <strong>parmVendorBankGroup</strong> als ER-Datenquelle konfiguriert ist, die einen Wert des Datentyps <strong><Zeichenfolge</strong> zurückgibt, liefert <strong>FILTER (Vendor.&lt;Relations'.VendBankAccount, Vendor.&lt;Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)</strong> eine Liste nur der Kreditorenkonten, die zu einer bestimmten Bankengruppe gehören.</td>
</tr>
<tr>
<td>INDEX (Liste, Index)</td>
<td>Diese Funktion gibt einen Datensatz zurück, der von einem bestimmten numerischen Index in der Liste ausgewählt wird. Eine Ausnahme wird ausgelöst, wenn der Index außerhalb des Bereichs der Datensätze in der Liste liegt.</td>
<td>Wenn Sie die Datenquelle <strong>DS</strong> für den Typ <strong>Berechnetes Feld</strong> eingeben und dieser den Ausdruck <strong>SPLIT („A|B|C“, „|“), 2</strong> enthält, gibt der Ausdruck <strong>DS.Value</strong> den Textwert „B“ zurück. Der Ausdruck <strong>INDEX (SPLIT („A|B|C“, „|“), 2).Value</strong> gibt außerdem den Textwert „B“ zurück.</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Logische Funktionen

| Funktion | Beschreibung | Beispiel |
|----------|-------------|---------|
| CASE (expression, option 1, result 1 \[, option 2, result 2\] … \[, default result\]) | Auswerten des angegebenen Ausdruckswert anhand der angegebenen alternativen Optionen. Gibt das Ergebnis der Option zurück, die gleich dem Wert des Ausdrucks ist. Andernfalls wird das optionale Standardergebnis zurückgegeben, wenn ein Standardergebnis angegeben ist. (Das Standardergebnis ist der letzte Parameter, dem keine Option vorangestellt ist). | **FALL (DATETIMEFORMAT (NOW (), "MM"), "10 ", "WINTER", "11 ", "WINTER", "12 ", "WINTER", "")** gibt die Zeichenfolge zurück **"WINTER"**, wenn das aktuelle Finance and Operations-Sitzungsdatum zwischen Oktober und Dezember ist. Andernfalls wird eine leere Zeichenfolge zurückgegeben. |
| WENN (Bedingung, Wert 1, Wert 2) | Gibt den ersten angegebenen Wert zurück, wenn die angegebene Bedingung zutrifft. Gibt anderenfalls den zweiten angegebenen Wert zurück. Wenn Wert 1 und Wert 2 Datensätze oder Datensatzlisten sind, hat das Ergebnis nur die Felder, die in beiden Listen vorhanden sind. | **WENN (1=2, "Bedingung erfüllt", "Bedingung erfüllt wird nicht erfüllt)"** gibt die Zeichenfolge **"Bedingung wird nicht erfüllt** zurück. |
| NICHT (Bedingung) | Geben Sie den umgekehrten logischen Wert der angegebenen Bedingung zurück. | **NICHT (WAHR=)** gibt **FALSCH** zurück. |
| AND (condition 1\[, condition 2, …\]) | Gibt **WAHR** zurück, wenn *alle* angegebenen Bedingungen erfüllt sind. Andernfalls wird **FALSCH** zurückgegeben. | **UND (1=1, "a " = "a")** gibt **WAHR** zurück. **UND (1=2, "a " = "a")** gibt **FALSCH** zurück. |
| OR (condition 1\[, condition 2, …\]) | Gibt **FALSCH** zurück, wenn *alle* angegebenen Bedingungen falsch sind. Gibt **WAHR** zurück, wenn *eine* angegebenen Bedingungen erfüllt ist. | **ODER (1=2, "a " = "a")** gibt **WAHR** zurück. |
| VALUEIN (Eingabe, Liste, Listenelementausdruck) | Bestimmen, ob die Eingabemit einem angegebenen Wert eines Artikels in der angegebenen Liste übereinstimmt. Rückhol-__ent_dict_UI wenn die **WAHR** Eingabe das Ergebnis aus den angegebenen Ausdruck für mindestens einen Datensatz ausführen übereinstimmt. Andernfalls wird **FALSCH** zurückgegeben. Der Parameter **Eingabe** stellt den Pfad eines Datenquellenelements dar. Der Wert dieses Elements, der abgeglichen wird. Der Parameter **Liste** stellt den Pfad eines Datenquellenelements des Rekordlistentyps als Liste von Datensätzen dar, die einen Ausdruck enthält. Der Wert dieses Elements wird mit der angegebenen Eingabe verglichen. Das **Listenelementausdruck**-Argument stellt einen Ausdruck dar, der entweder zu einem Feld zeigt oder ein einzelnes Feld der Liste enthält, die zum Abgleich verwendet werden soll. | Beispiele hierzu finden Sie in [Beispiele: VALUEIN (Eingabe, Liste, Listenelementausdruck)](#examples-valuein-input-list-list-item-expression) Abschnitten wie folgt. |

#### <a name="examples-valuein-input-list-list-item-expression"></a>Beispiele: VALUEIN (Eingabe, Liste, Listenelementausdruck)
Im Allgemeinen wird die Funktion **VALUEIN** zu einem Satz **ODER** Bedingungen umgerechnet:

(Eingabe = list.item1.value) ODER (Eingabe = list.item2.value) ODER...

##### <a name="example-1"></a>Beispiel 1
Sie definieren die folgende Datenquelle in der Zuordnung eines Projekt-Planzahlenmodells: Typ **Liste** (**Berechnetes Feld** ). Diese Datenquelle enthält den Suchbegriff **TEILUNG ("a,b,c", ", ")**.

Wenn eine Datenquelle aufgerufen wird, die als Ausdruck **VALUEIN ("B", "Liste, List.Value)** konfiguriert ist, gibt er **WAHR** zurück. In diesem Fall wird die Funktion **VALUEIN** zu einem Satz der folgenden Bedingungen umgerechnet:

**(("B" =" a") oder ("B" = "B") oder ("B" = "C"")**, wobei **("B" = "B")** ist gleich **WAHR**

Wenn eine Datenquelle aufgerufen wird, die als Ausdruck **VALUEIN ("B", "Liste, LINKS (List.Value, 0)))** konfiguriert ist, gibt er **FALSCH** zurück. In diesem Fall wird die Funktion **VALUEIN** zu einem Satz der folgenden Bedingungen umgerechnet:

**("B" = "")**, das nicht gleich **WAHR** ist

Beachten Sie, ob der obere Grenzwert für die Anzahl der Zeichen im Text beispielsweise eine Bedingung mit 32.768 Zeichen ist. Daher sollten Sie keine Datenquellen erstellen, die möglicherweise zur Laufzeit diesen Grenzwert überschreiten. Wenn das Unterzeichnungslimit überschritten wird, wird die Anwendung nicht mehr ausgeführt und eine Ausnahme ausgelöst. Beispielsweise kann diese Situation erfolgen, wenn die Datenquelle als **WO (List1, VALUEIN (List1.ID, List2, List2.ID)** konfiguriert wird, und die **List1** und **List2** Listen enthalten eine große Anzahl von Datensätzen.

In einigen Fällen wird die Funktion **VALUEIN** zu einem Datenbankauszug übersetzt, indem **EXISTIERT VERKNÜPFUNG** verwendet wird. Dieses Verhalten ist der Fall, wenn die Funktion **FILTER** verwendet wird und die folgenden Bedingungen erfüllt sind:

- Die Option **BITTEN SIE UM ABFRAGE** wird für die Datenquelle der Funktion **VALUEIN** deaktiviert, die die Liste von Datenträgen bezieht. (Es werden keine zusätzliche Bedingungen auf diese Datenquelle zur Bearbeitungszeit angewendet).
- Es werden keine eingebetteten Ausdrücke für die Datenquelle der Funktion **VALUEIN** konfiguriert, die sich auf die Liste von Datenträgen bezieht.
- Ein Listenelement der Funktion **VALUEIN** bezieht sich auf ein Feld (kein Ausdruck oder eine Methode) der angegebenen Datenquelle.

Ändern Sie diese Option anstelle der Funktion **WO** wie weiter oben in diesem Beispiel beschrieben.

##### <a name="example-2"></a>Beispiel 2

Die folgenden Datenquellen definieren Sie in Ihrer Modellzuordnung:

- **In** (**Tabellendatensätze**-Typ), der auf die Intrastat -Tabelle verweist
- **Port** (**Tabellendatensätze**-Typ), der auf die Intrastat -Port-Tabelle verweist

Wenn eine Datenquelle angerufen wird, die als **FILTERN (IN, VALUEIN(In.Port, Port, Port.PortId)** als Ausdruck konfiguriert, wird die nächste SQL-Anweisung generiert, um Datensätze gefilterten der Intrastat-Tabelle zurückzugeben:

```
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

Für **dataAreaId** Felder wird die abschließende SQL-Anweisung vom Anwendungs Operator **EIN** generiert.

##### <a name="example-3"></a>Beispiel 3

Die folgenden Datenquellen definieren Sie in Ihrer Modellzuordnung:

- **LE** (**Berechneter Feld** Typ), der den gewünschten Ausdruck **TEILUNG ("DEMF,GBSI, USMF", ", ")** enthält
- **Ein** (**Tabellendatensatz** Typ), der sich auf die Intrastat-Tabelle bezieht und für welches die Option **Unternehmensübergreifend** aktiviert ist

Wenn eine Datenquelle angerufen wird, die als **FILTER (in, VALUEIN (In.dataAreaId, Le, Le.Value)** als Ausdruck konfiguriert wird, enthält die abschließende SQL-Anweisung die folgende Bedingung:

```
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

### <a name="mathematical-functions"></a>Rechenoperationen

| Funktion | Beschreibung | Beispiel |
|----------|-------------|---------|
| ABS (Nummer) | Gibt den absoluten Wert der angegebenen Zahl zurück. (In anderen Worten gibt sie die Zahl ohne das Vorzeichens zurück). | **ABS (-1)** gibt **1** zurück. |
| LEISTUNG (Zahl, Leistung) | Gibt das Ergebnis der angehobenen spezifischen positiven Zahl der angegebenen Leistung zurück. | **LEISTUNG (10, 2)** gibt **100** zurück. |
| ZAHLENWERT (Zeichenfolge, Dezimaltrennzeichen, Zifferngruppierungstrennzeichen) | Konvertiert die angegebene Zeichenfolge zu einer Nummer. Das angegebene Dezimaltrennzeichen wird zwischen der ganzen Zahl und den Bruchteilen einer Dezimalzahl verwendet. Das angegebene Zifferngruppierungstrennzeichen wird als Tausendertrennzeichen verwendet. | **ZAHLENWERT ("1234,56 ", ",", " ")** gibt den Wert **1234.56** zurück. |
| WERT (Zeichenfolge) | Konvertiert die angegebene Zeichenfolge zu einer Nummer. Kommas und Punktzeichen (.) gelten als Dezimaltrennzeichen und es wird ein führender Bindestrich (-) als ein negatives Vorzeichen verwendet. Löst eine Ausnahme aus, wenn die angegebene Zeichenfolge andere nichtnumerische Zeichen enthält. | **WERT ("1 "234,56 ")** löst eine Ausnahme aus. |
| RUNDEN (Zahl, Dezimalen) | Gibt die angegebene Zahl zurück, nachdem sie auf die angegebene Zahl von Dezimalstellen gerundet wurde:<ul><li>Wenn der Wert des **Dezimalstellen**-Parameters größer als 0 (null) ist, wird die angegebene Zahl auf genau so viele Dezimalstellen gerundet.</li><li>Wenn der Wert des **Dezimalstellen**-Parameters **0** (null) ist, wird die angegebene Zahl auf die nächste ganze Zahl gerundet.</li><li>Wenn der Wert des **Dezimalstellen**-Parameters kleiner als 0 (null) ist, wir die angegebene Zahl links der Dezimalstelle gerundet.</li></ul> | **RUNDUNG (1200.767, 2)** Rundet auf zwei Dezimalstellen und gibt den Wert **1200.77** zurück.. **RUNDUNG (1200.767, -3)** Rundet auf das nächste Vielfache von 1,000 und gibt den Wert **1000** zurück. |
| ABRUNDEN (Zahl, Dezimalen) | Gibt die angegebene Zahl zurück, nachdem sie auf die angegebene Zahl von Dezimalstellen abgerundet wurde.<blockquote>[!NOTE] Diese Funktion verhält sich wie **RUNDUNG**, rundet die angegebene Zahl aber immer ab (in Richtung null).</blockquote> | **ABRUNDUNG (1200.767, 2)** Rundet auf zwei Dezimalstellen ab und gibt den Wert **1200.76** zurück. **ABRUNDUNG (1700.767, -3)** Rundet auf das nächste Vielfache von 1,000 ab und gibt den Wert **1000** zurück. |
| AUFRUNDEN (Zahl, Dezimalen) | Gibt die angegebene Zahl zurück, nachdem sie auf die angegebene Zahl von Dezimalstellen aufgerundet wurde.<blockquote>[!NOTE] Diese Funktion verhält sich wie **RUNDUNG**, rundet die angegebene Zahl aber immer auf (weg von null).</blockquote> | **AUFRUNDUNG (1200.763, 2)** Rundet auf zwei Dezimalstellen auf und gibt den Wert **1200.77** zurück. **-AUFRUNDUNG (1200.767, -3)** Rundet auf das nächste Vielfache von 1,000 auf und gibt den Wert **2000** zurück. |

### <a name="data-conversion-functions"></a>Datenumwandlungsfunktionen

| Funktion | Beschreibung | Beispiel |
|----------|-------------|---------|
| WERT (Zeichenfolge) | Konvertiert die angegebene Zeichenfolge zu einer Nummer. Kommas und Punktzeichen (.) gelten als Dezimaltrennzeichen und es wird ein führender Bindestrich (-) als ein negatives Vorzeichen verwendet. Löst eine Ausnahme aus, wenn die angegebene Zeichenfolge andere nichtnumerische Zeichen enthält. | **WERT ("1 "234,56 ")** löst eine Ausnahme aus. |
| ZAHLENWERT (Zeichenfolge, Dezimaltrennzeichen, Zifferngruppierungstrennzeichen) | Konvertiert die angegebene Zeichenfolge zu einer Nummer. Das angegebene Dezimaltrennzeichen wird zwischen der ganzen Zahl und den Bruchteilen einer Dezimalzahl verwendet. Das angegebene Zifferngruppierungstrennzeichen wird als Tausendertrennzeichen verwendet. | **NUMBERVALUE("1 234,56", ",", " ")** gibt **1234.56** zurück. |
| INTVALUE (Zeichenfolge) | Gibt eine Darstellung der angegebenen Zeichenfolge in ganzen Zahlen zurück. Sämtliche Dezimalstellen werden abgeschnitten. | **INTVALUE ("100.77")** gibt **100** zurück. |
| INTVALUE (Zahl) | Gibt eine Darstellung der angegebenen Zahl als ganze Zahl zurück. Sämtliche Dezimalstellen werden abgeschnitten. | **INTVALUE (-100,77)** gibt **-100** zurück. |
| INT64VALUE (Zeichenfolge) | Gibt eine int64-Darstellung der angegebenen Zeichenfolge zurück. Sämtliche Dezimalstellen werden abgeschnitten. | **INT64VALUE ("22565422744")** gibt **22565422744** zurück. |
| INT64VALUE (Nummer) | Gibt eine int64-Darstellung der angegebenen Zahl zurück. Sämtliche Dezimalstellen werden abgeschnitten. | **INT64VALUE (22565422744.00)** gibt **22565422744** zurück. |

### <a name="record-functions"></a>Datensatzfunktionen

| Funktion | Beschreibung | Beispiel |
|----------|-------------|---------|
| NULLCONTAINER (Liste) | Gibt einen **NULL**-Datensatz zurück, der die gleiche Struktur beinhaltet, wie die angegebene Datensatzliste oder Datensatz.<blockquote>[!NOTE] Diese Funktion ist veraltet. Verwenden Sie stattdessen **EMPTYRECORD**.</blockquote> | **NULLCONTAINER (TEILEN ("abc", 1))** gibt einen neuen leeren Datensatz zurück, der dieselbe Struktur wie die Liste beinhaltet, die durch Funktion **TEILEN** zurückgegeben wird. |
| LEERER DATENSATZLIST (Datensatz) | Gibt einen **NULL**-Datensatz zurück, der die gleiche Struktur beinhaltet, wie die angegebene Datensatzliste oder Datensatz.<blockquote>[!NOTE] Ein Datensatz **NULL** ist ein Datensatz, in dem alle Felder einen leeren Wert haben. Ein leerer Wert ist **0** (null) für Zahlen, eine leere Zeichenfolge für Zeichenfolgen usw.</blockquote> | **LEERER DATENSATZ (TEILEN ("abc", 1))** gibt einen neuen leeren Datensatz zurück, der dieselbe Struktur wie die Liste beinhaltet, die durch Funktion **TEILEN** zurückgegeben wird. |

### <a name="text-functions"></a>Textfunktionen

<table>
<thead>
<tr>
<th>Funktion</th>
<th>Beschreibung</th>
<th>Beispiel</th>
</tr>
</thead>
<tbody>
<tr>
<td>GROSSBUCHSTABE (Zeichenfolge)</td>
<td>Gibt die angegebene Zeichenfolge zurück, nachdem sie in Großbuchstaben konvertiert wurde.</td>
<td><strong>GROSSBUCHSTABE (&quot;Beispiel&quot;)</strong> gibt <strong>&quot;BEISPIEL&quot;</strong> zurück.</td>
</tr>
<tr>
<td>KLEINBUCHSTABEN (Zeichenfolge)</td>
<td>Gibt die angegebene Zeichenfolge zurück, nachdem sie in Kleinbuchstaben konvertiert wurde.</td>
<td><strong>KLEINBUCHSTABEN (&quot;Beispiel&quot;)</strong> gibt <strong>&quot;Beispiel&quot;</strong> zurück.</td>
</tr>
<tr>
<td>LINKS (Zeichenfolge, Anzahl Zeichen)</td>
<td>Gibt die angegebene Anzahl von Zeichen ab Beginn einer Textzeichenfolge zurück.</td>
<td><strong>LINKS (&quot;Beispiel&quot;, 3)</strong> gibt <strong>&quot;Sam&quot;</strong> zurück.</td>
</tr>
<tr>
<td>RECHTs (Zeichenfolge, Anzahl Zeichen)</td>
<td>Gibt die angegebene Anzahl von Zeichen ab Ende einer bestimmten Textzeichenfolge zurück.</td>
<td><strong>RECHTS (&quot;Beispiel&quot;, 3)</strong> gibt <strong>&quot;ple&quot;</strong> zurück.</td>
</tr>
<tr>
<td>MITTE (Zeichenfolge, Startposition, Anzahl Zeichen)</td>
<td>Gibt die angegebene Anzahl von Zeichen ab Beginn einer Textzeichenfolge zurück.</td>
<td><strong>MITTE (&quot;Beispiel&quot;, 2, 3)</strong> gibt <strong>&quot;amp&quot;</strong> zurück.</td>
</tr>
<tr>
<td>LEN (Zeichenfolge)</td>
<td>Gibt die Anzahl von Zeichen in einer Textzeichenfolge zurück.</td>
<td><strong>LEN (&quot;Beispiel&quot;)</strong> gibt <strong>6</strong> zurück.</td>
</tr>
<tr>
<td>CHAR (Nummer)</td>
<td>Gibt die Zeichenfolge von Zeichen zurück, die von der angegebene Unicode-Zahl angegeben wird.</td>
<td><strong>CHAR (255)</strong> gibt <strong>&quot;Ÿ&quot;</strong> zurück.
<blockquote>[!NOTE] Die Zeichenfolge, die diese Funktion zurück gibt, hängt von der Codierung ab, die im übergeordneten DATEI-Formatelement ausgewählt ist. Die Liste unterstützter Codierungen finden Sie unter <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Codierungsklasse</a>.</blockquote>
</td>
</tr>
<tr>
<td>VERKETTEN (Zeichenfolge 1, [, Zeichenfolge 2, ...])</td>
<td>Gibt alle angegebenen Textzeichenfolgen zurück, nachdem sie zu einer Zeichenfolge verknüpft wurden.</td>
<td><strong>VERKETTEN (&quot;ABC&quot;, &quot;def&quot;)</strong> gibt <strong>&quot;abcdef&quot;</strong> zurück.
<blockquote>[!NOTE] Der Ausdruck <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong> gibt auch <strong>&quot;abcdef&quot;</strong> zurück.</blockquote>
</td>
</tr>
<tr>
<td>ÜBERSETZEN (Zeichenfolge, Muster, Ersetzung)</td>
<td>Gibt die angegebene Zeichenfolge zurück, nachdem alle Vorkommen der Zeichen in der angegebenen Musterzeichenfolge durch die Zeichen in der entsprechenden Position in der angegebenen Austauschzeichenfolge ersetzt wurden.</td>
<td><strong>ÜBERSETZEN (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> ersetzt das Muster <strong>&quot;cd&quot;</strong> durch die Zeichenfolge <strong>&quot;GH&quot;</strong> und gibt <strong>&quot;abGHef&quot;</strong> zurück.</td>
</tr>
<tr>
<td>ERSETZEN (Zeichenfolge, Muster, Ersetzung, Markierung des regulären Ausdrucks)</td>
<td>Wenn die angegebene Markierung des <strong>regulären Ausdrucks</strong> <strong>wahr</strong> ist, wird die angegebene Zeichenfolge zurückgegeben, nachdem sie durch Anwendung des normalen <strong>Ausdruck</strong> geändert wurde, der als ein Musterargument für diese Funktion angegeben ist. Dieser Ausdruck wird verwendet, um Zeichen zu finden, die ersetzt werden müssen. Zeichen des angegebenen <strong>Ersetzungs</strong>arguments werden verwendet, um Zeichen zu ersetzen, die gefunden werden. Wenn die angegebene <strong>Markierung des regulären Ausdrucks</strong> <strong>falsch</strong> ist, verhält sich diese Funktion wie <strong>ÜBERSETZEN</strong>.</td>
<td><strong>ERSETZEN (&quot;+1 923 456 4971&quot;, &quot;[^0-9]&quot;, &quot;&quot;, true)</strong> übernimmt einen regulären Ausdruck, der alle nicht numerischen Symbole entfernt und <strong>&quot;19234564971&quot;</strong> zurückgibt. <strong>ERSETZEN (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> ersetzt das Muster <strong>&quot;cd&quot;</strong> mit der Zeichenfolge <strong>&quot;GH&quot;</strong> und gibt <strong>&quot;abGHef&quot;</strong> zurück.</td>
</tr>
<tr>
<td>TEXT (Eingabe)</td>
<td>Gibt die angegebene Eingabe zurück, nachdem sie in eine Textzeichenfolge konvertiert wurde, die gemäß den Servergebietsschemaeinstellungen der aktuellen Finance and Operations-Instanz formatiert ist. Für Werte für den <strong>tatsächlich</strong> Typ, wird die Zeichenkonvertierung auf zwei Dezimalstellen beschränkt.</td>
<td>Wenn das Servergebietsschema der Finance and Operations Instanz als <strong>EN-US</strong>, <strong>TEXT (NOW ())</strong> definiert wird, wird das aktuelle Finance and Operations-Sitzungsdatum, 17. Dezember 2015, als Textzeichenfolge <strong>&quot;12/17/2015 07:59:23 AM&quot;</strong> zurückgegeben. <strong>TEXT (1/3)</strong> gibt <strong>&quot;0.33&quot;</strong> zurück.</td>
</tr>
<tr>
<td>FORMAT (string 1, string 2[, string 3, …])</td>
<td>Geben Sie die angegebene Zeichenfolge zurück, nachdem sie formatiert wurde, indem sämtliche Vorkommnisse von <strong>%N</strong> durch das <em>n</em>. Argument ersetzt werden. Die Argumente sind Zeichenfolgen. Wenn eine Anfrage nicht für einen Parameter angegeben wird, wird der Parameter als <strong>&quot;%N&quot;</strong> in der Zeichenfolge zurückgegeben. Für Werte für den <strong>tatsächlich</strong> Typ, wird die Zeichenkonvertierung auf zwei Dezimalstellen beschränkt.</td>
<td>In der folgenden Abbildung gibt die Datenquelle <strong>PaymentModel</strong> die Liste von Kundendatensätzen über die Komponente <strong>-Kunde</strong> und den Verarbeitungsdatumswert über das Feld <strong>ProcessingDate</strong> zurück.
<p><a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a></p>
<p>Im ER-Format, das entworfen wurde, um eine Datei für ausgewählte Debitoren zu generieren, wird <strong>PaymentModel</strong> als Datenquelle ausgewählt, um den Prozessablauf zu steuern. Eine Ausnahme wird ausgelöst, um den Benutzer zu informieren, wann ein Kunde für das Datum angehalten wird, an dem der Bericht verarbeitet wird. Die Formel, die für diese Art von Prozesssteuerung entworfen wurde, kann die folgenden Ressourcen verwenden:</p>
<ul>
<li>Finance and Operations-Beschriftung SYS70894, die den folgenden Text hat:
<ul>
<li><strong>Für die EN-US-Sprache:</strong> &quot;Nichts zu drucken&quot;</li>
<li><strong>Für deutsche Sprache:</strong> &quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>Finance and Operations-Beschriftung SYS18389, die den folgenden Text hat:
<ul>
<li><strong>Für die EN-US-Sprache:</strong> &quot;Debitor %1 wird beendet für %2.&quot;</li>
<li><strong>Für deutsche Sprache:</strong> &quot;Debitor '%1' wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
<p>Hier die Formel, die gestaltet werden kann:</p>
<p>FORMAT (CONCATENATE (@&quot;SYS70894&quot;, &quot;. &quot;, @&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;d&quot;))</p>
<p>Wenn ein Bericht für den Kunden <strong>Litware Retail</strong> am 17. Dezember 2015 in der <strong>EN-US</strong>-Kultur und in der <strong>EN-US</strong>-Sprache verarbeitet wird, gibt diese Formel den folgenden Text zurück, der dann als Ausnahmenachricht für den Benutzer präsentiert werden kann:</p>
<p>&quot;Nichts zu drucken. Debitor Litware Retail wird auf 12/17/2015&quot; beendet.</p>
<p>Wenn derselbe Bericht für den Kunden <strong>Litware Retail</strong> am 17. Dezember 2015 in der <strong>DE</strong>-Kultur und in der <strong>DE</strong>-Sprache verarbeitet wird, gibt diese Formel den folgenden Text zurück, der ein anderes Datumsformat verwendet:</p>
<p>&quot;Nichts-zu drucken. Schuldner-"Litware Einzelhandel" wird für 17.12.2015 gesperrt.&quot;</p>
<blockquote>[!NOTE] Die folgende Syntax wird in EB-Formeln für Beschriftungen angewendet:
<ul>
<li><strong>Für Beschriftungen aus Finance and Operations-Ressourcen</strong> <strong>@&quot;X&quot;</strong>, wobei <strong>X</strong> die Beschriftungs-ID im Application Object Tree (AOT) ist</li>
<li><strong>Für Beschriftungen, die sich in ER-Konfigurationen befinden:</strong> <strong>@&quot;GER_LABEL:X&quot;</strong>, wobei <strong>X</strong> die Beschriftungs-ID in der ER-Konfiguration ist</li>
</ul>
</blockquote>
</td>
</tr>
<tr>
<td>ZAHLENFORMAT (Zahl, Format)</td>
<td>Gibt eine Zeichenfolgendarstellung der angegebenen Zahl im angegebenen Format zurück. (Informationen zum die unterstützten Formaten, finden Sie unter <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">Standard</a> und <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">Custom</a>.) Im Kontext, dass diese Funktion ausgeführt wird, bestimmt die Kultur, die den Formatnummern verwendet wird.</td>
<td>Für EN-US Kultur <strong>ZAHLENFORMAT (0.45, &quot;p&quot;)</strong> gibt <strong>&quot;45,00 %&quot;</strong> zurück. <strong>ZAHLENFORMAT (10,45, &quot;#&quot;)</strong> gibt <strong>&quot;10&quot;</strong> zurück.</td>
</tr>
<tr>
<td>NUMERALSTOTEXT (Nummer, Sprache, Währung, Drucktwährungsnamenmarkierung, Dezimaltrennzeichen)</td>
<td>Gibt die angegebene Zahl zurück, nachdem sie (konvertiert in Textzeichenfolgen) in der angegebenen Sprache formuliert wurde. Der Sprachcode ist optional. Wenn es als leere Zeichenfolge definiert ist, wird stattdessen der Sprachcode für den ausgeführten Kontext verwendet. (Der Sprachcode für den ausgeführten Kontext wird für einen generierenden Ordner oder Datei definiert.) Der Währungscode ist auch optional. Wenn dieser als leere Zeichenfolge definiert ist, wird die Unternehmenswährung verwendet.
<blockquote>[!NOTE] Die Parameter für <strong>Druckwährungsnamen-Kennzeichen</strong> und <strong>Dezimalstellen</strong> werden nur für die folgenden Sprachcodes analysiert: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong> und <strong>RU</strong>. Darüber hinaus wird der <strong>Druckwährungsnamen-Kennzeichen</strong>-Parameter nur für Finance and Operations-Unternehmen analysiert, bei denen der Landes- oder Regionenkontext die Deklination von Währungsnamen unterstützt.</blockquote>
</td>
<td><strong>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, false, 2)</strong> gibt <strong>&quot;Eintausendzweihundertvierunddreißig und 56&quot;</strong> zurück. <strong>NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, false, 0)</strong> gibt <strong>&quot;Sto dwadzieścia&quot;</strong> zurück. <strong>NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, true, 2)</strong> gibt <strong>&quot;Сто двадцать евро 21 евроцент&quot;</strong> zurück.</td>
</tr>
<tr>
<td>PADLEFT (Zeichenfolge, Länge, Zeichen auffüllen)</td>
<td>Gibt eine Zeichenfolge mit der angegebenen Länge zurück, bei der der Anfang der angegebenen Zeichenfolge mit den angegebenen Zeichen aufgefüllt ist.</td>
<td><strong>PADLEFT (&quot;1234&quot;, 10, &quot;&nbsp;&quot;)</strong> gibt die Textzeichenfolge <strong>&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234&quot;</strong> zurück.</td>
</tr>
<tr>
<td>TRIM (Zeichenfolge)</td>
<td>Gibt die angegebene Textzeichenfolge zurück, nachdem führende und nachfolgende Leerzeichen abgeschnitten wurden und nachdem mehrfache Leerzeichen zwischen Wörtern entfernt wurden.</td>
<td><strong>TRIM (&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Sample&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;text&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&quot;)</strong> gibt <strong>&quot;Beispieltext&quot;</strong> zurück.</td>
</tr>
<tr>
<td>GETENUMVALUEBYNAME (Enumerationsdatenquellenpfad, Enumerationswertbeschriftungstext)</td>
<td>Gibt einen Wert der angegebenen Aufzählungsdatenquelle basierend auf dem angegebenen Text und der Aufzählungsbeschriftung zurück.</td>
<td>In der folgenden Abbildung wird die Aufzählung <strong>ReportDirection</strong> in einem Datenmodell eingeführt. Beachten Sie, dass Beschriftungen für Enumerationswerte definiert werden.
<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>Die folgende Abbildung zeigt diese Details an:</p>
<ul>
<li>Die Modellaufzählung <strong>ReportDirection</strong> wird in einen Bericht als Datenquelle eingefügt, <strong>$Direction</strong>.</li>
<li>Ein EB-Ausdruck <strong>$IsArrivals</strong> ist dazu konzipiert, die Modellaufzählung als Parameter dieser Funktion zu verwenden. Der Wert dieses Ausdrucks ist <strong>WAHR</strong></li>
</ul>
<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>
</td>
</tr>
<tr>
<td>GUIDVALUE (Eingabe)</td>
<td>Konvertieren Sie die angegebene Eingabe des Datentyps <strong>Zeichenfolge</strong> in ein Datenelement des Datentyps <strong>GUID</strong>.<blockquote>[!NOTE] Um eine Umwandlung in der entgegengesetzten Richtung zu bewerkstelligen (das heißt, die angegebene Eingabe des Datentyps <strong>GUID</strong> zu einem Datenelement des Datentyps <strong>Zeichenfolge</strong> konvertieren), können Sie dies mithilfe der <strong>TEXT()</strong>-Funktion tun.</blockquote></td>
<td>Die folgenden Datenquellen definieren Sie in Ihrer Modellzuordnung:
<ul>
<li><strong>myID</strong> (<strong>Berechnetes Feld</strong>-Typ), das den gewünschten Ausdruck <strong>GUIDVALUE (&quot;AF5CCDAC-F728-4609-8C8B-, A4B30B0C0AA0&quot;)</strong> enthält</li>
<li><strong>Users</strong> (<strong>Tabellendatensätze</strong>-Typ), der auf die UserInfo -Tabelle verweist</li>
</ul>
Wenn diese Datenquellen definiert sind, können Sie einen Ausdruck wie <strong>FILTER (Users, Users.objectId = myID)</strong> verwenden, um die Tabelle UserInfo nach dem Feld <strong>objectId</strong> des Datentyps <strong>GUID</strong> zu filtern.
</td>
</tr>
<tr>
<td>JSONVALUE (id, path)</td>
<td>Analysieren Sie Daten im JavaScript Object Notation (JSON)-Format, auf die über den angegebenen Pfad zugegriffen wird, um einen Skalarwert zu extrahieren, der auf der angegebenen ID basiert.</td>
<td>Die Datenquelle <strong>$JsonField</strong> enthält folgende Daten im JSON-Format: <strong>{&quot;BuildNumber&quot;:&quot;7.3.1234.1&quot;, &quot;KeyThumbprint&quot;:&quot;7366E&quot;}</strong>. Für diese Datenquelle gibt </strong>JSONVALUE ( &quot;BuildNumber&quot;, $JsonField)</strong> den Wert <strong>7.3.1234.1</strong> des Datentyps <strong>String</strong> zurück.</td>
</tr>
</tbody>
</table>

### <a name="data-conversion-functions"></a>Datenumwandlungsfunktionen

| Funktion | Beschreibung | Beispiel |
|----------|-------------|---------|
| TEXT (Eingabe) | Gibt die angegebene Eingabe zurück, nachdem sie in eine Textzeichenfolge konvertiert wurde, die gemäß den Servergebietsschemaeinstellungen der aktuellen Finance and Operations-Instanz formatiert ist. Für Werte für den **tatsächlich** Typ, wird die Zeichenkonvertierung auf zwei Dezimalstellen beschränkt. | Wenn das Servergebietsschema der Finance and Operations Instanz als **EN-US**, **TEXT (NOW ())** definiert wird, wird das aktuelle Finance and Operations-Sitzungsdatum, 17. Dezember 2015, als Textzeichenfolge **12/17/2015 07:59:23 AM** zurückgegeben. **TEXT (1/3)** gibt **"0.33"** zurück. |
| QRCODE (Zeichenfolge) | Gibt ein Quick Response Code (QR-Code) Bild im base64-Binärformat für die angegebene Zeichenfolge zurück. | **QRCODE ("Beispieltext")** gibt **U2FtcGxlIHRleHQ=** zurück. |

### <a name="data-collection-functions"></a>Datensammlungsfunktionen

| Funktion | Beschreibung | Beispiel |
|----------|-------------|---------|
| FORMATELEMENTNAME () | Gibt den Namen des Elements des aktuellen Formats zurück. Gibt eine leere Zeichenfolge zurück, wenn das Kennzeichen **Ausgabedetails sammeln** der aktuellen Dateien deaktiviert ist. | Um mehr darüber zu erfahren, wie diese Funktion verwendet wird, finden Sie Informationen im Aufgabenleitfaden **EB – Verwendung von Daten der Formatausgabe für Inventur und Summierungen**, der Teil des Geschäftsprozesses **IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln** ist. |
| SUMIFS (Schlüsselzeichenfolge zum Summieren, Kriterien Range1 Zeichenfolge \[, Kriterien Value1 Zeichenfolge [,Kriterien Range2 Zeichenfolge, Kriterien Value2 Zeichenfolge, …\]) | Gibt die Summe von Werten von XML-Knoten (bei denen der Name als Schlüssel definiert ist) zurück, die während der Ausführung des Formats gesammelt wurden und die angegebenen Bedingungen erfüllen (Koppelungen von Bereichen und Werten). Gibt einen Wert **0** (null) zurück, wenn das Kennzeichen **Ausgabedetails sammeln** der aktuellen Dateien deaktiviert ist. | |
| SUMIF (Schlüsselzeichenfolge zum Summieren, Kriterien-Bereichszeichenfolge, Kriterien-Wertzeichenfolge) | Gibt die Summe von Werten von XML-Knoten (bei denen der Name als Schlüssel definiert ist) zurück, die während der Ausführung des Formats gesammelt wurden und die angegebenen Bedingungen erfüllen (Koppelungen von Bereichen und Werten). Gibt einen Wert **0** (null) zurück, wenn das Kennzeichen **Ausgabedetails sammeln** der aktuellen Dateien deaktiviert ist. | |
| COUNTIFS (Kriterien Range1 Zeichenfolge, Kriterien Value1 Zeichenfolge \[, Kriterien Range2 Zeichenfolge, Kriterien Value2 Zeichenfolge…\]) | Gibt die Zahl von XML-Knoten zurück, die während der Ausführung des Formats gesammelt wurden, und die die angegebenen Bedingungen erfüllen (Koppelungen von Bereichen und Werten). Gibt einen Wert **0** (null) zurück, wenn das Kennzeichen **Ausgabedetails sammeln** der aktuellen Dateien deaktiviert ist. | |
| COUNTIF (Kriterien-Bereichszeichenfolge, Kriterien-Wertzeichenfolge) | Gibt die Zahl von XML-Knoten zurück, die während der Ausführung des Formats gesammelt wurden, und die die angegebenen Bedingungen erfüllen (Bereiche und Werte). Gibt einen Wert **0** (null) zurück, wenn das Kennzeichen **Ausgabedetails sammeln** der aktuellen Dateien deaktiviert ist. | |
| COLLECTEDLIST (Kriterien Range1 Zeichenfolge, Kriterien Value1 Zeichenfolge \[, Kriterien Range2-Zeichenfolge, Kriterien Value2 Zeichenfolge…\]) | Gibt die Zahl von XML-Knoten zurück, die während der Ausführung des Formats gesammelt wurden, und die die angegebenen Bedingungen erfüllen (Bereiche und Werte). Gibt eine leere Liste zurück, wenn die Markierung **Ausgabedetails sammeln** der aktuellen Dateien deaktiviert ist. | |

### <a name="other-business-domainspecific-functions"></a>Andere (geschäftsdomänenspezifische) Funktionen

| Funktion | Beschreibung | Beispiel |
|----------|-------------|---------|
| CONVERTCURRENCY (Betrag, Quellwährung, Zielwährung, Datum, Unternehmen) | Konvertiert den angegebenen Geldbetrag aus der angegebenen Quellwährung in die angegebene Zielwährung, indem die Einstellungen des angegebenen Finance and Operations-Unternehmens am angegebenen Datum verwendet werden. | **CONVERTCURRENCY (1, "EUR", "USD", HEUTE (), "DEMF")** gibt die Entsprechung von einem Euro in US Dollar am Datum der aktuellen Sitzung, auf den Einstellungen für das DEMF-Unternehmen zurück. |
| ROUNDAMOUNT (Anzahl, Dezimalstellen, Rundungsregel) | Rundet den angegebenen Betrag auf die angegebene Zahl von Dezimalstellen gemäß der angegebenen Rundungsregel.<blockquote>[!NOTE] Die Rundenregel muss als Wert der **RoundOffType**-Aufzählung von Finance and Operations angegeben werden.</blockquote> | Wenn der Parameter **model.RoundOff** auf **Abwärts** festgelegt ist, gibt **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** den Wert **1000.78** zurück. Wenn der **model.RoundOff**-Parameter entweder auf **Normal** oder **Aufrunden** **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** festgelegt wird, wird der Wert **1000.79** zurückgegeben. |
| CURCredRef (Ziffern) | Gibt eine Gläubigerreferenz basierend auf den Ziffern der angegebenen Rechnungsnummer zurück. | **CURCredRef ("VEND-200002")** gibt **"2200002"** zurück. |
| MOD\_97 (Ziffern) | Gibt eine Gläubigerreferenz als MOD97 Ausdruck zurück, basierend auf den Ziffern der angegebenen Rechnungsnummer. | **MOD\_97 ("VEND-200002")** gibt **"20000285"** zurück. |
| ISOCredRef (Ziffern) | Gibt eine Gläubigerreferenz der Internationale Organisation für Normung (ISO) basierend auf den Ziffern und alphabetischen Symbolen der angegebenen Rechnungsnummer zurück.<blockquote>[!NOTE] Um Symbole aus Alphabeten zu entfernen, die nicht ISO-kompatibel sind, muss der Eingabeparameter übersetzt werden, bevor er an diese Funktion übergeben wird.</blockquote> | **ISOCredRef ("VEND-200002")** gibt **"RF23VEND-200002"** zurück. |
| CN\_GBT\_AdditionalDimensionID (Zeichenfolge, Zahl) | Ruft die angegebene zusätzliche Finanzdimensions-ID ab. Im Parameter **Zeichenfolge** werden Dimensionen als IDs dargestellt, die durch Kommas getrennt sind. Der Parameter **Zahl** definiert den Sequenzcode der gewünschten Dimension in der Zeichenfolge. | **CN\_GBT\_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH",3)** gibt **"CC"** zurück. |
| GetCurrentCompany () | Gibt die Textdarstellung des Codes für die juristische Person (Unternehmen) zurück, bei dem ein Benutzer derzeit angemeldet ist. | **GETCURRENTCOMPANY ()** gibt **USMF** für einen Benutzer zurück, der beim Unternehmen **Contoso Entertainment System USA** in Finance and Operations angemeldet ist. |
| CH\_BANK\_MOD\_10 (Stellen) | Gibt eine Gläubigerreferenz als MOD10-Ausdruck zurück, basierend auf den Ziffern der angegebenen Rechnungsnummer. | **CH\_BANK\_MOD\_10 ("VEND-200002")** gibt **3** zurück. |
| FA\_SUM (Anlagencode, Wertmodellcode, Startdatum, Enddatum) | Gibt den vorbereiteten Datencontainer des Anlagenbetrags für die angegebene Periode zurück. | **FA\_SUM ("COMP-000001", "Current", Date1, Date2)** gibt den vorbereiteten Datenconteiner der Anlage **"COMP-000001"** zurück, der das Wertmodell **"Current"** für eine Periode von **Date1** bis **Date2** hat. |
| FA\_BALANCE (Anlagencode, Wertmodellcode, Berichtsjahr, Meldedatum) | Gibt den vorbereiteten Datencontainer des Anlagensaldos zurück. Das Berichterstellungsjahr muss als Wert der Aufzählung **AssetYear** in Finance and Operations angegeben werden. | **FA\_SUM ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())** gibt den vorbereiteten Datencontainer von Salden für Anlage **"COMP-000001"** zurück, der das Wertmodell **"Current"** zum aktuellen Finance and Operations-Sitzungsdatum hat. |
| TABLENAME2ID (Zeichenfolge) | Gibt eine ganzzahlige Darstellung einer Tabellenkennung für den angegebenen Tabellennamen zurück. | **TABLENAME2ID ("Intrastat")** gibt **1510** zurück. |
| ISVALIDCHARACTERISO7064 (Zeichenfolge) | Gibt den booleschen Wert **WAHR** zurück, wenn die angegebene Zeichenfolge eine gültige internationale Bankkontonummer (IBAN) darstellt. Gibt anderenfalls den booleschen Wert **FALSCH** zurück. | **ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")** gibt **WAHR** zurück. **ISVALIDCHARACTERISO7064 ("AT61")** gibt **FALSCH** zurück. |
| NUMSEQVALUE (Nummernkreiscode, "Bereich, Umfangs-ID) | Gibt den neuen, generierten Wert eines Nummernkreises basierend auf dem Nummernkreiscode der angegebenen Anzahl, der Bereich und die Bereichs-ID zurück. Der Bereich muss als Wert der Option **ERExpressionNumberSequenceScopeType** (**Gemeinsam genutzt**, **Juristische Person** oder **Unternehmen**) angegeben werden. Für den Bereich **Gemeinsam genutzt** geben Sie eine Nullkette als die Bereichs-ID an. Für **Unternehmen** und **Juristische Person** Bereiche geben Sie den Unternehmenscode als die Bereichs-ID an. Für **Unternehmen** und **Juristische Person** Bereiche wenn Sie eine Nullkette als die Bereichs-ID angeben, wird der aktuelle Unternehmenscode verwendet. | Die folgenden Datenquellen definieren Sie in Ihrer Modellzuordnung:<ul><li>**enumScope** (**Dynamics 365 for Operations-Enumeration**-Typ), der sich auf die **ERExpressionNumberSequenceScopeType**-Enumeration bezieht.</li><li>Typ **NumSeq** (**Berechnetes Feld** Typ), das den gewünschten Ausdruck **NUMSEQVALUE ("Gen \_1 ", enumScope.Company, "")** enthält</li></ul>Wenn die Datenquelle **NumSeq** aufgerufen wird, wird er dem generierten neuen Wert des **Gen \_1** Nummernkreis zurückgegeben, der für das Unternehmen konfiguriert wurde, der den Kontext liefe, unter dem das ER-Format ausgeführt wird. |
| NUMSEQVALUE (Nummernkreiscode) | Gibt den neuen generierten Wert eines Nummernkreises zurück, basierend auf dem angegebenen Nummernkreis, dem Bereich **Unternehmen** und (als die Bereichs-ID) den Code des Unternehmens, das den Kontext enthält, unter dem das ER-Format ausgeführt wird. | Sie definieren die folgende Datenquelle in der Zuordnung: **Num Seq** (**Berechneter Feld** Typ). Diese Datenquelle enthält den Suchbegriff **NUMSEQVALUE ("Gene\_1")**. Wenn die Datenquelle **NumSeq** aufgerufen wird, wird er dem generierten neuen Wert des **Gen \_1** Nummernkreis zurückgegeben, der für das Unternehmen konfiguriert wurde, der den Kontext liefe, unter dem das ER-Format ausgeführt wird. |
| NUMSEQVALUE (Nummernkreiscode RecordID) | Gibt den neuen, generierten Wert eines Nummernkreises basierend auf dem Nummernkreiscode der angegebenen RecordID zurück. | Die folgenden Datenquellen definieren Sie in Ihrer Modellzuordnung:<ul><li>**LedgerParms** (**Tabellen**-Typ), der auf die LedgerParameters-Tabelle verweist</li><li>**NumSeq** (**Berechneter Feld** Typ), das den gewünschten Ausdruck **NUMSEQVALUE (LedgerParameters.'numRefJournalNum()'.NumberSequenceId)** enthält</li></ul>Wenn die Datenquelle **NumSeq** aufgerufen wird, wird er dem generierten neuen Wert des Gen 1 Nummernkreis zurückgegeben, der für die Hauptbuch-Parameter für das Unternehmen konfiguriert wurde, der den Kontext liefert, unter dem das ER-Format ausgeführt wird. Dieser Nummernkreis kennzeichnet eindeutige Erfassungen und fungiert als eine Chargennummer, die die Buchungen zusammen verknüpft. |

### <a name="functions-list-extension"></a>Listenerweiterung der Funktionen

ER ermöglicht es Ihnen, die Liste von Funktionen zu verlängern, die in ER-Ausdrücken verwendet werden. Etwas technischer Aufwand ist erforderlich. Ausführliche Informationen finden Sie unter [Erweitern der Liste der elektronischen Berichtsfunktion](general-electronic-reporting-formulas-list-extension.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)
- [Erweitert die Liste der elektronischen Berichtsfunktion (ER)](general-electronic-reporting-formulas-list-extension.md)
