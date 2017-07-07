---
title: Formeldesigner in der elektronischen Berichterstellung
description: "In diesem Artikel wird beschrieben, wie den Formel-Designer in der elektronischen Berichterstattung (ER) verwendet wird. Wenn Sie ein Format für ein bestimmtes elektronisches Dokument in ER entwerfen, können Sie Microsoft Excel ähnliche Formeln für Datenumwandlungen verwenden, um den Anforderungen für diese Dokumenterfüllung und Formattierung zu entsprechen. Unterschiedliche Arten von Funktionen werden unterstützt: Text, Datum und Uhrzeit, mathematische Logisches, Informationen, Datentypumrechnung und andere (domänenspezifische Funktionen des Geschäfts)."
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: 655a6fd99c0688b13c31c79f3322a287f902e7f1
ms.contentlocale: de-de
ms.lasthandoff: 06/20/2017


---

# <a name="formula-designer-in-electronic-reporting"></a>Formeldesigner in der elektronischen Berichterstellung

[!include[banner](../includes/banner.md)]


In diesem Artikel wird beschrieben, wie den Formel-Designer in der elektronischen Berichterstattung (ER) verwendet wird. Wenn Sie ein Format für ein bestimmtes elektronisches Dokument in ER entwerfen, können Sie Microsoft Excel ähnliche Formeln für Datenumwandlungen verwenden, um den Anforderungen für diese Dokumenterfüllung und Formattierung zu entsprechen. Unterschiedliche Arten von Funktionen werden unterstützt: Text, Datum und Uhrzeit, mathematische Logisches, Informationen, Datentypumrechnung und andere (domänenspezifische Funktionen des Geschäfts).

<a name="formula-designer-overview"></a>Formeldesignerübersicht
-------------------------

Elektronische Berichterstellung (ER) unterstützt den Formeldesigner. Daher können Sie zum Zeitpunkt des Entwurfs Ausdrücke konfigurieren, die für folgende Aufgaben zur Laufzeit verwendet werden können:

-   Transformieren von Daten der Microsoft Dynamics 365 for Finance and Operations-Datenbank, die für ein ER-Datenmodell ausgefüllt werden sollen, das als Datenquelle für ER-Formate entworfen wurde (Filterung, Gruppierung, Datentypumrechnung, usw.).
-   Formatierung von Daten, die für ein generierendes elektronisches Dokument in Übereinstimmung mit dem Layout und den Bedingungen eines bestimmtem ER-Formats ausgegeben werden müssen (in Übereinstimmung mit der angeforderten Sprache oder Kultur, Codierung, usw.)
-   Steuerung des Prozesses der Generierung elektronischer Dokumente (Aktivierung/Deaktivierung bestimmter Elemente des Formats abhängig von der Verarbeitung von Daten, Unterbrechung der Dokumenterstellung, Auslösung von Meldungen für Endbenutzer, usw.)

Die Formeldesignerseite kann von folgenden Stellen aus geöffnet werden:

-   Binden von Datenquellenartikeln zu den Datenmodellkomponenten.
-   Binden von Datenquellenartikeln zu den Datenformatkomponenten.
-   Verwaltung von berechneten Feldern als Teil der Datenquellen abschließen.
-   Definition von Sichtbedingungen für Benutzereingabeparameter.
-   Entwurf der Umwandlungen des Formats.
-   Definition der Aktivierung von Bedingungen für die Komponenten des Formats.
-   Definition von Dateinamen für die DATEIkomponenten des Formats.
-   Definition der Bedingungen für Prozesssteuerprüfungen.
-   Definition der Nachrichtentextes für Prozesssteuerprüfungen.

## <a name="designing-er-formulas"></a>Entwerfen der ER-Formeln
### <a name="data-binding"></a>Datenbindung

Der ER-Formeldesigner kann verwendet werden, um einen Ausdruck zu definieren, der Daten umwandelt, die von den Datenquellen empfangen werden, sodass die Daten beim Datenkonsument zur Laufzeit aufgefüllt werden können:

-   Von Finance and Operations-Datenquellen und -Laufzeitparametern zum ER-Datenmodell.
-   Von einem ER-Datenmodell zu einem ER-Format.
-   Von Finance and Operations-Datenquellen und -Laufzeitparametern zum ER-Format.

Die folgende Abbildung zeigt das Design eines Ausdrucks dieses Typs. In diesem Beispiel wird der Ausdruck dem Wert des **Intrastat.AmountMST** Felds der Finance and Operations-**Intrastat**-Tabelle zurückgegeben, nachdem der Wert zu zwei Dezimalstellen gerundet wurde. [![picture-expression-binding](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg) Die folgende Abbildung veranschaulicht, wie ein Ausdruck dieses Typs verwendet werden kann. In diesem Beispiel wird das Ergebnis der entworfenen Ausdrucks in die **Transaction.InvoicedAmount** Komponente des **Steuerberichterstellungsmodell** Datenmodells ausgefüllt. [![picture-expression-binding2](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg) Zur Laufzeit rundet die entworfene Formel, **ROUND (Intrastat.AmountMST, 2)**, den Wert des Feldes **AmountMST** für jeden Datensatz der **Instrastat**-Tabelle auf zwei Dezimalstellen und füllt den Rundungswert in die Komponente **Transaction.InvoicedAmount** des **Steuerberichterstattungs**-Datenmodells.

### <a name="data-formatting"></a>Datenformatierung

Der ER-Formeldesigner kann verwendet werden, um einen Ausdruck zu definieren, der Daten umwandelt, die von den Datenquellen empfangen werden, sodass die Daten als Teil zum Erstellen eines elektronischen Dokuments gesendet werden können. Wenn Sie eine Formatierung haben, die als gewöhnliche Regel angewendet werden muss, die für ein Format wieder verwendet werden soll, können Sie diese Formatierung in einer Formatkonfiguration als benannte Umwandlung einmal als Formatierungsausdruck erfassen. Später kann diese benannte Umwandlung mit vielen Formatkomponenten verknüpft werden, deren Ausgabe gemäß dem erstellten Ausdruck formatiert werden muss. Die folgende Abbildung zeigt das Design einer Umwandlung dieses Typs. In diesem Beispiel nimmt die **TrimmedString** Umwandlung die eingehenden Daten des **String** Datentyps und unterdrückt Anfangs- und Endleerschläge bei der Rückgabe des String-Werts. [![picture-transformation-design](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg) Die folgende Abbildung zeigt, wie die Umwandlung dieses Typs verwendet werden kann. In diesem Beispiel gibt es mehrere Formatkomponenten, die Texte an das zu generierende elektronische Dokument senden und sich auf die **TrimmedString** Umwandlung nach Name beziehen. [![picture-transformation-usage](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg) Wenn Formatkomponenten auf die Umwandlung verweisen **TrimmedString**-Transformation (zum Beispiel **partyName**-Komponente in der vorherigen Abbildung) sendet dieses Text als Ausgabe an das zu generierende Dokument. Der Text enthält keine vor- und nachgestellten Leerzeichen. Wenn Sie eine Formatierung haben, die einzeln angewendet werden muss, kann sie als einzelner Ausdruck der Bindung einer bestimmten Formatkomponente eingeführt werden. Die folgende Abbildung zeigt einen Ausdruck dieses Typs. In diesem Beispiel wird die Formatkomponente **partyType** an die Datenquelle über einen Ausdruck gebunden, der die eingehenden Daten aus dem Feld **Model.Company.RegistrationType** in der Datenquelle in Text in Großbuchstaben konvertiert und diesen Text als Ausgabe an ein elektronisches Dokument gesendet wird. [![picture-binding-with-formula](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Prozessflusssteuerung

Der ER-Formeldesigner wird verwendet, um Ausdrücke zu definieren, die verwendet werden, um den Arbeitsablauf zum Generieren von Dokumenten zu steuern: Sie können:

-   Definiert Bedingungen, wenn ein Dokumentenerstellungsprozess gestoppt werden muss.
-   Definiert Ausdrücke, die entweder Nachrichten für den Endnutzer über beendete Prozess erstellt oder Ausführungsprotokollnachrichten zum Fortsetzen des Prozesses der Berichterstellung auslöst.
-   Gibt den Dateinamen zum Generieren der Dokumente und die Steuerzuständen der Erstellung an.

Jede Regel der Prozessflusssteuerung ist als einzelne Prüfung entworfen. Die folgende Abbildung zeigt die Überprüfung dieses Typs. Ist hier eine Erläuterung der Konfiguration in diesem Beispiel:

-   Die Prüfung wird ausgewertet, wenn der **INSTAT** Knoten in der generierenden XML-Datei erstellt wird.
-   Wenn die Transaktionsliste leer ist, stoppt die Überprüfung den Ausführungsprozess und gibt **FALSCH** zurück.
-   Die Prüfung gibt eine Fehlermeldung zurück, der den Text der Beschriftung SYS70894 in der bevorzugten Sprache des Benutzers umfasst.

[![picture-validation](./media/picture-validation.jpg)](./media/picture-validation.jpg) Beispiel einer Prüfung Der ER-Formeldesigner wird auch verwendet, um einen Dateinamen für das Generieren elektronischer Dokumente anzugeben und einen Dateierstellungsprozess zu steuern. Die folgende Abbildung zeigt das Design einer Prozessablaufsteuerung dieses Typs. Ist hier eine Erläuterung der Konfiguration in diesem Beispiel:

-   Die Liste der Datensätze aus der Datenquelle **model.Intrastat** wird durch Chargen unterteilt, die bis 1000 Datensätze enthalten
-   Die Ausgabe erstellt eine ZIP-Datei, die eine Datei im XML-Format für jede Charge enthält, die erstellt wurde.
-   Ein Ausdruck gibt einen Dateinamen für das Generieren von elektronischen Dokumenten zurück, indem er den Dateinamen und die Dateierweiterung verkettet. Für die zweite und alle nachfolgenden Chargen enthält der Dateiname die Chargenkennung als Suffix.
-   Ein Ausdruck aktiviert (durch Rückgabe von **WAHR**) den Prozess der Dateierstellung für Chargen, die mindestens einen Datensatz beinhalten.

[![picture-file-control](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Grundlegende Syntax

Er-Ausdrücke können einzelne oder alle folgenden Elemente enthalten:

-   Konstanten
-   Operatoren
-   Referenzen
-   Pfade
-   Funktionen

#### <a name="constants"></a>Konstanten

Sie können Text und numerische Konstanten (Werte, die nicht berechnet werden) verwenden, wenn Sie Ausdrücke erstellen. So wird beispielsweise der Ausdruck **WERT ("100") + 20** als numerische Konstante 20 verwendet und die Zeichenfolgenkonstante "100" gibt den numerischen Wert **120** zurück. Der ER-Formeldesigner unterstützt einzelne Sequenzen, so dass Sie diesen Teil der Ausdruckszeichenfolge angeben können, die anders behandelt werden soll. Beispielsweise gibt der Ausdruck **“Leo Tolstoi ""Krieg und Frieden"" Band 1** folgende Textzeichenfolge zurück **Leo Tolstoi "Krieg und Frieden" Band 1**.

#### <a name="operators"></a>Operatoren

Die folgende Tabelle zeigt die arithmetischen Operatoren, die Sie verwenden können, um grundlegende mathematische Arbeitsgänge, wie Addition, Subtraktion, Division und Multiplikation auszuführen.

| Bediener | Dies bedeutet              | Beispiel |
|----------|----------------------|---------|
| +        | Hinzufügung             | 1+2     |
| -        | Subtraktions-Negation | 5-2 -1  |
| \*       | Multiplikation       | 7\*8    |
| /        | Geschäftsbereich             | 9/3     |

In der folgenden Tabelle werden die Vergleichsoperatoren gezeigt, die auch unterstützt werden und die Sie verwenden können, um zwei Werte zu vergleichen.

| Bediener | Dies bedeutet                  | Beispiel    |
|----------|--------------------------|------------|
| =        | Gleich                    | X=Y        |
| &gt;     | Größer als             | X&gt;Y     |
| &lt;     | Kleiner als                | X&lt;Y     |
| &gt;=    | Größer oder gleich | X&gt;=Y    |
| &lt;=    | Kleiner oder gleich    | X&lt;=Y    |
| &lt;&gt; | Ungleich             | X&lt;&gt;Y |

Darüber hinaus können Sie ein kaufmännisches Und-Zeichen (&) als Text-Kettungsoperator verwenden, um eine oder mehrere Textzeichenfolgen mit einem einzelnen Stück des Texts zu verknüpfen oder zu verketten.

| Bediener | Dies bedeutet     | Beispiel                                        |
|----------|-------------|------------------------------------------------|
| &        | Verketten | "Keine Datensätze" & ": "& "Keine Datensätze gefunden" |

#### <a name="operator-precedence"></a>Vorrangigkeit

Die Reihenfolge, in der die Teile eines zusammengesetzten Ausdrucks ausgewertet werden, ist wichtig. Beispielsweise variiert das Ergebnis des Ausdrucks **1 + 4 / 2**, je nachdem, ob die Addition oder Division zuerst ausgeführt wird. Sie können Klammern verwenden, um explizit zu definieren, wie ein Ausdruck ausgewertet werden soll. Beispielsweise um anzugeben, dass die Addition zuerst ausgeführt werden soll, können Sie den vorhergehenden Ausdruck abändern auf **(1 + 4) / 2**. Wenn der Reihenfolge der Arbeitsgänge, die in einem Ausdruck ausgeführt werden müssen, nicht explizit definiert ist, basiert der Auftrag auf der standardmäßigen Prioritätsreihenfolge, die den unterstützten Operatoren zugewiesen ist. Die folgende Tabelle zeigt die Operatoren und die Prioritätsreihenfolge an, die in jedem zugewiesen ist. Operatorenm, die einen höheren Vorrang haben, (beispielsweise 7), werden vor Operatoren ausgewertet, die niedrigeren Vorrang haben, (beispielsweise 1).

| Priorität | Operatoren      | Syntax                                                   |
|------------|----------------|----------------------------------------------------------|
| 7          | Gruppieren       | ( … )                                                    |
| 6          | Mitgliedszugriff  | …   …                                                    |
| 5          | Funktionsaufrufe  | … ( … )                                                  |
| 4          | Multiplikation | … \* … … / …                                             |
| 3          | Ergänzung       | … + … … - …                                              |
| 2          | Vergleich     | … &lt; … … &lt;= … … =&gt; … … &gt; … … = … … &lt;&gt; … |
| 1          | Trennung     | … , …                                                    |

Operatoren für die gleiche Position haben gleichen Vorrang. Wenn ein Ausdruck mehr als einen dieser Operatoren umfasst, wird der Ausdruck von links nach rechts ausgewertet. Beispielsweise der Ausdruck **1 + 6 / 2 \* 3 &gt; 5** gibt **WAHR** zurück. Es wird empfohlen, dass Sie Klammern verwenden, um die gewünschte Reihenfolge der Bewertung für Ausdrucke explizit anzugeben damit Ausdrücke besser lesbar für und verwaltbar sind.

#### <a name="references"></a>Referenzen

Alle Datenquellen der aktuellen ER-Komponente (entweder ein Modell oder ein Format), die während der Erstellung eines Ausdrucks verfügbar sind, können als benannte Referenzen verwendet werden. Zum Beispiel beinhaltet das aktuelle ER-Datenmodell die Datenquelle **ReportingDate**, die den Wert des **DATETIME** -Datentyps zurückgibt. Um diesen Wert ordnungsgemäß zu formatieren, können Sie auf die Datenquelle im Ausdruck wie folgt verweisen: **DATETIMEFORMAT (ReportingDate, "TT-MM-JJJ")** Alle Zeichen im Namen der verweisenden Datenquelle die keine alphabetischen Zeichen sind müssen ein vorangestelltes Anführungszeichen haben ('). Jeder Name der verweisenden Datenquelle, der mindestens ein Symbol enthält, das keinen Buchstaben des Alphabets darstellt (Satzzeichen oder andere geschriebene Symbole), muss in einfachen Anführungszeichen angezeigt werden. Nachfolgend finden Sie einige Beispiele:

-   Auf die Datenquelle **Aktuelles Datum & Zeit** muss im ER-Ausdruck wie folgt verwiesen werden: **'Heutiges Datum & Zeit’**
-   Die Methode **Name()** der **Kreditoren** datenquelle muss im ER-Ausdruck wie folgt werdendet werden: **Kunde.'Name()'**

Beachten Sie, dass die folgende Syntax verwendet wird, um Methoden der Dynamics 365 for Operations-Datenquellen mit Parametern aufzurufen:

- Auf die isLanguageRTL-Methode der Systemdatenquelle mit einem Parameter EN-US des Zeichenfolgendatentyps muss in einem ER-Ausdruck wie folgt verwiesen werden: System.’isLanguageRTL’(“EN-US”).
- Anführungszeichen sind nicht erforderlich, wenn ein Methodenname nur alphanumerische Symbole enthält. Sie sind für eine Methode einer Tabelle obligatorisch, wenn der Name Klammern enthält.

Wenn die Systemdatenquelle einer ER-Zuordnung hinzugefügt wird, die auf die Dynamics 365 for Operations-Anwendungsklasse "Global" verweist, gibt der Ausdruck den booleschen Wert "FALSCH" zurück. Der geänderte Ausdruck , System’. isLanguageRTL ("AR"), gibt booleschem Wert TRUE zurück.

Beachten Sie, dass die Übergabe an solche Methodenparameter mit den folgenden Einschränkungen definiert werden kann:

- Nur Konstanten können an Methoden übergeben werden, ihr Wert wird zur Entwurfszeit definiert.
- Nur primitive (basis) Datentypen werden für solche Parameter unterstützt (Ganzzahl, Reelle Zahl, boolesches, Zeichenfolge, usw.).

#### <a name="path"></a>Pfad

Wenn ein Ausdruck auf eine strukturierte Datenquelle verweist, können Sie die Pfadbeschreibung verwenden, um ein bestimmtes primitives Element dieser Datenquelle auszuwählen. Ein Punktzeichen (. ) wird verwendet, um einzelne Elemente einer strukturierten Datenquelle zu unterteilen. Zum Beispiel beinhaltet das aktuelle ER-Datenmodell die Datenquelle **InvoiceTransactions**, die eine Liste der Datensätze zurückgibt. Die **InvoiceTransactions**-Datensatzstruktur enthält die Felder **AmountDebit** und **AmountCredit**, die numerische Werte zurückgeben. Sie können den folgenden Ausdruck zum Berechnen des Rechnungsbetrag wie folgt konzipieren: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**

#### <a name="functions"></a>Funktionen

Im nächsten Abschnitt wird die Funktionen beschrieben, die in ER-Ausdrücken verwendet werden können. Alle Datenquellen des Ausdruckskontexts (laufendes ER-Datenmodell oder ER-Format) sowie Konstanten können als Parameter von aufrufenden Funktionen in Übereinstimmung mit der Liste der aufrufenden Funktionsargumente verwendet werden. Zum Beispiel beinhaltet das aktuelle ER-Datenmodell die Datenquelle **InvoiceTransactions**, die eine Liste der Datensätze zurückgibt. Die **InvoiceTransactions**-Datensatzstruktur enthält die Felder **AmountDebit** und **AmountCredit**, die numerische Werte zurückgeben. Ein Ausdruck, um den Rechnungsbetrag zu berechnen, kann wie folgt konzipiert werden, indem die integrierte ER-Rundungsfunktion verwendet wird: **RUNDEN (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**

## <a name="supported-functions"></a>Unterstützte Funktionen
Die folgenden Tabellen beschreiben die Datenmanipulationsfunktion, die Sie verwenden können, um ER-Datenmodelle und ER-Berichte zu entwerfen. Die Liste mit Funktionen ist nicht fest und kann von Entwicklern erweitert werden. Um die Liste von Funktionen zu finden, die Sie verwenden können, greifen Sie auf den Funktionsbereich im ER-Formeldesigner zu.

### <a name="date-and-time-functions"></a>Datums- und Zeitfunktionen

| Funktion                                   | Beschreibung                                                                                                                                                                                                                                                                                                                                                      | Beispiel                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TAG HINZUFÜGEN (Datetime, Tage)                   | Fügen Sie die angegebene Anzahl von Tagen dem angegebenen Datum-Zeit-Wert hinzu.                                                                                                                                                                                                                                                                                                | **TAGE HINZUFÜGEN (JETZT (), 7)** gibt das Datum und die Uhrzeit sieben Tage in der Zukunft zurück.                                                                                                                                                                                                                            |
| DATETODATETIME (Datum)                      | Den definierten Datumswert auf einen Zeitwert konvertieren.                                                                                                                                                                                                                                                                                                            | **DATETODATETIME (CompInfo. 'getCurrentDate() ')** gibt das Datum der aktuellen Finance and Operations-Sitzung, 12/24/2015, als **12/24/2015 12:00: 00 AM** zurück. In diesem Beispiel ist **CompInfo** eine ER-Datenquelle des **Finance and Operations/Tabellen-**-Typs, der die Tabelle "CompanyInfo" bezieht. |
| JETZT ()                                     | Gibt das aktuelle Finance and Operations-Anwendungs-Serverdatum und die Zeit als Datum-Zeit-Wert zurück.                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                       |
| HEUTE ()                                   | Gibt das aktuelle Finance and Operations-Anwendungs-Serverdatum und die Zeit als ein Datumswert zurück.                                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                                                                                                       |
| NULLDATE ()                                | Gibt einen **Null**-Datumswert zurück.                                                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                       |
| NULLDATETIME ()                            | Gibt einen **Null**-Datumswert zurück.                                                                                                                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                       |
| DATETIMEFORMAT "datetime, Format)          | Konvertieren Sie den angegebenen Datum-Zeit-Wert in eine Zeichenfolge im angegebenen Format. (Informationen zu unterstützten Formaten, finden Sie unter [Standard](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) und [Benutzerdefiniert](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).)                                                                        | **DATETIMEFORMAT (JETZT (), "TT-MM-JJJJ")** gibt das laufende Finance and Operations-Anwendungsserver-Datum, 12/24/2015, als **"24-12-2015"** gemäß dem angegebenen benutzerdefinierten Format zurück.                                                                                                          |
| DATETIMEFORMAT "datetime, Format, Kultur) | Konvertieren Sie den angegebenen Datum-Zeit-Wert in eine Zeichenfolge im angegebenen Format und [Kultur](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Informationen zu unterstützten Formaten, finden Sie unter [Standard](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) und [Benutzerdefiniert](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)). | **DATETIMEFORMAT "(NOW(), "d" de", "")** gibt das aktuelle Finance and Operations Anwendungs-Serverdatum 12/24/2015 als **"24.12.2015"** gemäß der gewählten deutschen Kultur zurück.                                                                                                             |
| SESSIONTODAY ()                            | Gibt das aktuelle Dynamics 365 for Finance and Operation-Sitzungsdatum als Datumswert zurück.                                                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                       |
| SESSIONNOW ()                              | Gibt das aktuelle Dynamics 365 for Finance and Operation-Sitzungsdatum als Zeit- und Datumswert zurück.                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                       |
| DATENFORMAT (Datum, Format)                  | Gibt die Zeichenfolgendarstellung des Datums im angegebenen Format zurück.                                                                                                                                                                                                                                                                                                    | **DATENFORMAT (SESSIONTODAY (), "TT-MM-JJJJ")** gibt das aktuelle Dynamics 365 for Finance and Operations-Sitzungsdatum, 12/24/2015 als "**24-12-2015**" entsprechend dem angegebenen benutzerdefinierten Format zurück.                                                                                                                      |
| DATENFORMAT (Datum, Format, Kultur)         | Konvertieren Sie den angegebenen Datumswert in eine Zeichenfolge im angegebenen Format und der entsprechenden [Kultur](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Informationen zu unterstützten Formaten, finden Sie unter [Standard](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) und [Benutzerdefiniert](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)).     | **DATETIMEFORMAT "(SESSIONNOW (), "d" de", "")** gibt das aktuelle Finance and Operations-Sitzungsdatum 12/24/2015 als **"24.12.2015"** gemäß der gewählten deutschen Kultur zurück.                                                                                                                       |
| DAYOFYEAR (Datum)              | Gibt eine ganzzahlige Darstellung der Anzahl von Tagen zwischen dem 1. Januar dem angegebenen Datum zurück.       | **DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))** gibt **61** zurück.
**DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))** gibt **1** zurück.                                                                                                                       |

**Datenumwandlungsfunktionen**

| Funktion                                   | Beschreibung                                                                                                                                                                                                                                                                                                                                                      | Beispiel                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DATETODATETIME (Datum)                 | Den definierten Datumswert auf einen Zeitwert konvertieren.           | **DATETODATETIME (CompInfo. 'getCurrentDate() ')** gibt das Datum der aktuellen Finance and Operations-Sitzung, 12/24/2015, als **12/24/2015 12:00: 00 AM** zurück. In diesem Beispiel ist **CompInfo** eine ER-Datenquelle des **Finance and Operations/Tabellen**-Typs, der die Tabelle **CompanyInfo** bezieht.                                                                                                                       |
| DATEVALUE (Zeichenfolge, Format)              | Gibt die Datumsdarstellung einer Zeichenfolge in einem angegebenen Format zurück.       | **DATEVALUE ("21-Dez-2016", "TT-MMM-JJJJ")** gibt das Datum 12/21/2016 gemäß benutzerdefiniertem Format und der **EN-US**-Kultur der Standardanwendung zurück.                                                                                                                       |
| DATEVALUE (Zeichenfolge, Format, Kultur)              | Gibt die Datumsdarstellung einer Zeichenfolge in einem angegebenen Format und der angegebenen Kultur zurück.       | **DATEVALUE ("21-Gen-2016", "", "TT-MMM-JJJJ", "IT")** wird das Datum 01/21/2016 gemäß benutzerdefiniertem Format und Kultur zurück. Eine Ausnahme wird für diesen Anruf der Funktion ausgelöst, **DATEVALUE ("21-Gen-2016", "TT-MMM-JJJJ", "EN-US ")** und informiert, dass eine gegebene Zeichenfolge nicht als gültiges Datum erkannt wird.                                                                                                                       |
| DATETIMEVALUE (Zeichenfolge, Format)              | Gibt die Datum-/Uhrzeitdarstellung einer Zeichenfolge in einem angegebenen Format zurück.       | **DATETIMEVALUE ("21-Dec-2016 02:55: 00 ", "TT-MMM-JJJJ SS:MM:ss")** gibt 2:55:00 AM vom 21. Dezember 2016 gemäß benutzerdefiniertem Format und der **EN-US**-Kultur der Standardanwendung zurück.                                                                                                                       |
| DATETIMEVALUE (Zeichenfolge, Format, Kultur)              | Gibt die Datum-/Uhrzeitdarstellung einer Zeichenfolge in einem angegebenen Format und der angegebenen Kultur zurück.       | **DATETIMEVALUE ("21-Gen-2016 02:55: 00 ", "TT-MMM-JJJJ SS:MM:ss", "IT")** gibt 2:55:00 AM vom 21. Dezember 2016 gemäß einem benutzerdefiniertem Format und Kultur zurück. Eine Ausnahme wird für diesen Anruf der Funktion ausgelöst, **DATETIMEVALUE ("21-Gen-2016 02:55:00", "SS:MM:ss", "EN-US ")** und informiert, dass eine gegebene Zeichenfolge nicht als gültiges Datum/Uhrzeit-Objekt erkannt wird.                                                                                                                       |
### <a name="list-functions"></a>Listenfunktionen

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>Beschreibung</th>
<th>Beispiel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TEILEN (Eingabe, Länge)</td>
<td>Teilen Sie die angegebene Eingabezeichenfolge in Teilzeichenfolgen, von denen jede die angegebene Länge hat. Geben Sie das Ergebnis als neue Liste zurück.</td>
<td><strong>TEILEN (&quot;abcd&quot;, 3)</strong> gibt eine neue Liste zurück, die aus zwei Datensätzen besteht, die ein Feld <strong>ZEICHENFOLGE</strong> haben. Das Feld im ersten Datensatz enthält den Text <strong>&quot;ABC&quot;</strong> und das Feld im zweiten Datensatz beinhaltet den Text <strong>&quot;D&quot;</strong>.</td>
</tr>
<tr class="even">
<td>TEILUNGSLISTE (Liste, Nummer)</td>
<td>Teilt die angegebene Liste in Chargen, die jeweils die angegebene Anzahl von Datensätzen enthalten. Geben Sie das Ergebnis als neue Liste von Chargen zurück, die die folgenden Elemente enthält:
<ul>
<li>Chargen als regelmäßige Listen (<strong>Wert</strong>kKomponente)</li>
<li>Die aktuelle Chargennummer (<strong>Chargennummer</strong>komponente)</li>
</ul></td>
<td>Im folgenden Beispiel werden die <strong>Positionen</strong> Datenquellen für eine Rekordliste von drei Datensätzen erstellt, die in Chargen verteilt sind, von denen jede bis zu zwei Datensätze enthält. <a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a> Dies zeigt das entsprechende Formatlayout, bei dem entsprechend den <strong>Zeilen</strong> Datenquellen erstellt wurden, um die Ausgabe im XML-Format zu generieren, das individuelle Knoten für jede Charge und die Datensätze darin anzeigt. <a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a> Das Folgende ist das Ergebnis der Ausführung des entworfenen Formats. <a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a></td>
</tr>
<tr class="odd">
<td>LISTE (Datensatz 1, Datensatz [2,...])</td>
<td>Gibt eine neue Liste zurück,, die von den angegebenen Argumenten erstellt wird.</td>
<td><strong>LISTE (model.MainData, model.OtherData)</strong> gibt einen leeren Datensatz zurück, in dem die Liste der Felder alle Felder der <strong>Hauptdaten</strong> und der <strong>Anderen Daten</strong> der Datensatzliste enthält.</td>
</tr>
<tr class="even">
<td>LISTJOIN (Liste 1, 2 Liste,...)</td>
<td>Gibt eine neue Liste zurück, die von den angegebenen Argumenten erstellt wird.</td>
<td><strong>LISTJOIN (TEILEN (&quot;ABC&quot;, 1), TEILEN (&quot;def&quot;, 1))</strong> gibt die Liste von sechs Datensätzen zurück, in der ein Feld des <strong>ZEICHENFOLGEN</strong> Datentyps einzelne Buchstaben enthält.</td>
</tr>
<tr class="odd">
<td>ISEMPTY (Liste)</td>
<td>Gibt <strong>WAHR</strong> zurück, wenn die angegebene Liste keine Elemente enthält. Andernfalls wird <strong>FALSCH</strong> zurückgegeben.</td>
<td></td>
</tr>
<tr class="even">
<td>EMPTYLIST (Liste)</td>
<td>Gibt eine leere Liste zurück, indem die angegebene Liste wie eine Quelle für die Listenstruktur verwendet wird.</td>
<td><strong>LEERER DATENSATZ (TEILEN (&quot;abc&quot;, 1))</strong> gibt eine neue leere Liste zurück, die dieselbe Struktur wie die Liste beinhaltet, die durch Funktion <strong>TEILEN </strong>zurückgegeben wird.</td>
</tr>
<tr class="odd">
<td>ZUERST (Liste)</td>
<td>Gibt den ersten Datensatz der angegebenen Liste zurück, wenn dieser Datensatz nicht leer ist. Andernfalls ergibt sich eine Ausnahme.</td>
<td></td>
</tr>
<tr class="even">
<td>FIRSTORNULL (Liste)</td>
<td>Gibt den ersten Datensatz der angegebenen Liste zurück, wenn dieser Datensatz nicht leer ist. Andernfalls wird ein <strong>NULL</strong> Datensatz zurückgegeben.</td>
<td></td>
</tr>
<tr class="odd">
<td>LISTOFFIRSTITEM (Liste)</td>
<td>Gibt eine Liste zurück, die nur das erste Element der gegebenen Liste enthält.</td>
<td></td>
</tr>
<tr class="even">
<td>ALLITEMS (Pfad)</td>
<td>Gibt eine neue vereinfachte Liste zurück, die alle Elemente darstellt, die mit dem angegebenen Pfad übereinstimmen. Der Pfad muss als gültiger Datenquellenpfad zu einem Datenquellenelement eines Beleglistendatentyps definiert werden. Der Pfad zu Zeichenfolge, Datum, Datenelemente usw. sollte einen Fehler im ER-Ausdrucks-Generator erzeugen.</td>
<td>Wenn Sie <strong>TEILEN (&quot;abcdef&quot;, 2)</strong> als Datenquelle (DS) eingeben, wird <strong>ANZAHL (ALLITEMS (DS.Value))</strong> zurückgegeben <strong>3</strong>.</td>
</tr>
<tr class="odd">
<td>ORDERBY (Liste [, Ausdruck 1, Ausdruck 2,...])</td>
<td>Gibt die angegebene Liste zurück, die entsprechend den angegebenen Argumenten sortiert wird, die als Ausdrücke definiert werden können.</td>
<td>Wenn <strong>Kreditor </strong>als ER-Datenquelle konfiguriert wurde, die sich auf die Tabelle "VendTable" bezieht, gibt<strong> ORDERBY (Kreditoren, Kreditoren. Name ())</strong> die Liste von Kreditoren zurück, die nach Name in aufsteigender Reihenfolge sortiert wird.</td>
</tr>
<tr class="even">
<td>UMKEHREN (Liste)</td>
<td>Gibt die angegebene Liste in umgekehrter Sortierreihenfolge zurück.</td>
<td>Wenn <strong>Kreditor </strong>als ER-Datenquelle konfiguriert wurde, die sich auf die Tabelle "VendTable" bezieht, gibt <strong>(UMKEHREN (Kreditoren, Kreditoren.Name ())')) )</strong> die Liste von Kreditoren zurück, die nach Namen in absteigender Reihenfolge sortiert wird.</td>
</tr>
<tr class="odd">
<td>WO (Liste, Bedingung)</td>
<td>Gibt die angegebene Liste zurück, die gemäß der angegebenen Bedingung so gefiltert ist. Im Gegensatz zu <strong>FILTER</strong>funktionen wird die angegebene Bedingung der Liste im Arbeitsspeicher angewendet.</td>
<td>Wenn <strong>Kreditor</strong> als ER-Datenquelle konfiguriert wurde, die sich auf die Tabelle "VendTable" bezieht, gibt <strong>WO (Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> die Liste von Kreditoren zurück, die zur Kreditorengruppe 40 gehören.</td>
</tr>
<tr class="even">
<td>Aufzählung (LISTE)</td>
<td>Gibt eine neue Liste zurück, die aus aufgezählten Datensätzen der angegebenen Liste besteht und die folgende Elemente verfügbar macht:
<ul>
<li>Angegebene Listendatensätze als regelmäßige Listen (<strong>Wert</strong>komponente)</li>
<li>Der Index des aktuellen Datensatzes (<strong>Nummer</strong>komponente)</li>
</ul></td>
<td>Im folgenden Beispiel wird die Datenquelle<strong>Aufzählung</strong> als Aufzählungsliste von Kreditorendatensätzen von der Datenquelle <strong>Kreditoren</strong> erstellt, die sich auf die Tabelle <strong>VendTable "</strong> bezieht. <a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>Hier ist das Format, in dem Datenbindungen erstellt werden, um Ausgaben im XML-Format zu generieren, das einzelne Kreditoren als Aufzählungsknoten darstellt. <a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a> Das Folgende ist das Ergebnis der Ausführung des entworfenen Formats. <a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a></td>
</tr>
<tr class="odd">
<td>ZÄHLEN (Liste)</td>
<td>Gibt die erste Zahl des Datensatzes der angegebenen Liste zurück, wenn dieser Datensatz nicht leer ist. Andernfalls wird <strong>0</strong> (Null) zurückgegeben.</td>
<td><strong>ANZAHL (TEILEN (&quot;abcd&quot;, 3))</strong> gibt <strong>2</strong> zurück, da die Funktion <strong>TEILEN</strong> eine Liste erstellt, die aus zwei Datensätzen besteht.</td>
</tr>
<tr class="even">
<td>LISTOFFIELDS (Pfad)</td>
<td>Gibt eine Datensatzliste zurück, die von einem Argument von einem der folgenden Typen erstellt wird:
<ul>
<li>Modellenumeration</li>
<li>Formatenumeration</li>
<li>Behälter</li>
</ul>
Die erstellte Liste besteht aus Datensätzen mit den folgenden Feldern:
<ul>
<li>Name</li>
<li>Beschriftung</li>
<li>Beschreibung</li>
</ul>
Die Beschriftungs- und Beschreibungsfelder geben zur L‎aufzeit festgelegte Werte basierend auf den Spracheinstellungen des Formats zurück.</td>
<td>Das folgende Beispiel zeigt die Enumeration in einem Datenmodell. <a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="GER LISTOFFIELDS function - model enumeration" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>Beispiel:
<ul>
<li>Modellenumeration eingefügt in einen Bericht als Datenquelle.</li>
<li>Er-Ausdruck entwickelt, um Modellenumerationen als Parameter für diese Funktion zu verwenden.</li>
<li>Datenquelle des Beleglistentyps, eingefügt in einen Bericht mit dem erstellten ER-Ausdruck.</li>
</ul>
<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="GER LISTOFFIELDS function - in format expression" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>Das folgende Beispiel zeigt die ER-Formatelemente an, die an die Datenquelle des Beleglistentyp gebunden sind, der mithilfe der LISTOFFIELDS-Funktion erstellt wurde. <a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="GER LISTOFFIELDS function - format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>Dies ist das Ergebnis der entworfenen Formatausführung. <a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="GER LISTOFFIELDS function - format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a><strong>Hinweis:</strong> Übersetzter Text für Beschriftungen und Beschreibungen wird in der ER-Formatausgabe entsprechend den Spracheinstellungen eingetragen, die für DATEI- und ORDNER-Formatelemente konfiguriert werden.</td>
</tr>
<tr class="odd">
<td>STRINGJOIN (Liste, Feldname, Trennzeichen)</td>
<td>Gibt die Zeichenfolge mit verketteten Werten eines Felds aus einer Liste zurück, die mit einem ausgewählten Trennzeichen getrennt sind.</td>
<td>Wenn Sie TEILUNG ("ABC", "1") als eine Datenquelle DS eingegeben haben, gibt der Ausdruck STRINGJOIN (DS, DS.Value, ": ") "a:b:c" zurück.</td>
</tr>
<tr class="even">
<td>SPLITLISTBYLIMIT (Liste, Grenzwert, Grenzquelle)</td>
<td>Teilt die gegebene Liste in eine neue Liste von Unterlisten und gibt das Ergebnis im Beleglisteninhalt zurück. Der Limitwertparameter gibt den Wert des Limits ein, um die Ursprungsliste aufzuteilen. Der Limitquellparameter gibt dem Schritt an, mit dem die Gesamtsumme erhöht wird. Das Limit wird auf keinen einzelnen Artikel der angegebenen Liste angewendet, wenn die Limitquelle das definierte Limit überschreitet.</td>
<td>Das folgende Beispiel zeigt das Beispielformat mithilfe der Datenquellen. <a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="GER SPLITLISTBYLIMIT - format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="GER SPLITLISTBYLIMIT - datasources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>Dies ist die Ergebnisformatausführung, die die flache Liste von Warenartikeln vorlegt.<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="GER SPLITLISTBYLIMIT - output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>das folgende Beispiel zeigt dasselbe Format an, die angepasst wurde, um die Liste der Warenartikeln in Chargen startet, wenn einer einzelnen Lagercharge Waren mit dem Gesamtgewicht enthalten muss, das das Limit der 9 überschreiten soll.<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="GER SPLITLISTBYLIMIT - format 1" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="GER SPLITLISTBYLIMIT - datasources 1" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>Das, das Ergebnis der angepassten Formatausführung ist. <a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="GER SPLITLISTBYLIMIT - output 1" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a><strong>Hinweis:</strong> Das Limit wird nicht auf den letzten Artikel der Ursprungsliste angewendet, da der Wert (11) der Quelle des Limits (Gewicht) die definiere Grenze (9) überschreitet. Verwenden Sie entweder die Funktion <strong>WO</strong> oder den Ausdruck <strong>Aktiviert</strong> des entsprechenden Formatelements, um Unterlisten für die Berichterstellung (nach Bedarf) zu ignorieren (zu überspringen).</td>
</tr>
<tr class="odd">
<td>FILTER (Liste, Bedingungen)</td>
<td>Gibt die angegebene Liste zurück, die für die jeweilige Bedingung durch Ändern der Abfrage gefiltert wird. Im Gegensatz zur Funktion <strong>WO</strong> wird die angegebene Bedingung auf der Datenbankebene in jeder ER-Datenquelle des Tabellendatensatztyps angewendet.</td>
<td>FILTER (Vendors, Vendors.VendGroup = &quot;40&quot;) gibt eine Liste von nur Kreditoren zurück, die zur Lieferantengruppe <strong>40</strong> gehören, wenn Kreditor als ER-Datenquelle konfiguriert wurde, die sich auf die Tabelle <strong>VendTable</strong> bezieht.</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Logische Funktionen

| Funktion                                                                                | Beschreibung                                                                                                                                                                                                                                                                     | Beispiel                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FALL (Ausdruck, Option 1, Ergebnis 1 \[, Option 2, Ergebnis 2\] ... \[, Standardergebnis\]) | Auswerten des angegebenen Ausdruckswert anhand der angegebenen alternativen Optionen. Gibt das Ergebnis der Option zurück, die gleich dem Wert des Ausdrucks ist. Andernfalls müssen Sie das optional eingegebene Standardergebnis zurücksetzen (der letzte Parameter, der nicht von einer Option vorangestellt wird). | **FALL (DATETIMEFORMAT (NOW (), "MM"), "10 ", "WINTER", "11 ", "WINTER", "12 ", "WINTER", "")** gibt die Zeichenfolge zurück **"WINTER"**, wenn das aktuelle Finance and Operations-Sitzungsdatum zwischen Oktober und Dezember ist. Andernfalls wird eine leere Zeichenfolge zurückgegeben. |
| WENN (Bedingung, Wert 1, Wert 2)                                                        | Gibt den angegebenen Wert 1 zurück, wenn die bestimmte Bedingung zutrifft. Andernfalls wird Wert 2 zurückgegeben. Wenn Wert 1 und Wert 2 auf Datensätzen oder Datensatzlisten basieren, besitzt das Ergebnis nur die Felder, die in beiden Listen vorhanden sind.                                                                     | **WENN (1=2, "Bedingung erfüllt", "Bedingung erfüllt wird nicht erfüllt)"** gibt die Zeichenfolge **"Bedingung wird nicht erfüllt** zurück.                                                                                                                                                      |
| NICHT (Bedingung)                                                                         | Geben Sie den umgekehrten logischen Wert der angegebenen Bedingung zurück.                                                                                                                                                                                                                   | **NICHT (WAHR=)** gibt **FALSCH** zurück.                                                                                                                                                                                                                            |
| UND (Bedingung 1\[, Bedingung 2, ...\])                                                 | Gibt **WAHR** zurück, wenn *alle * angegebenen Bedingungen erfüllt sind. Andernfalls wird **FALSCH** zurückgegeben.                                                                                                                                                                                            | **UND (1=1, "a " = "a")** gibt **WAHR** zurück. **UND (1=2, "a " = "a")** gibt **FALSCH** zurück.                                                                                                                                                                           |
| ODER (Bedingung 1\[, Bedingung 2, ...\])                                                  | Gibt **FALSCH** zurück, wenn *alle * angegebenen Bedingungen falsch sind. Gibt **WAHR** zurück, wenn *eine * angegebenen Bedingungen erfüllt ist.                                                                                                                                                                 | **ODER (1=2, "a " = "a")** gibt **WAHR** zurück.                                                                                                                                                                                                                      |

### <a name="mathematical-functions"></a>Rechenoperationen

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>Beschreibung</th>
<th>Beispiel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ABS (Nummer)</td>
<td>Gibt den absoluten Wert einer bestimmten Zahl zurück (die Zahl ohne ihr Vorzeichen).</td>
<td><strong>ABS (-1)</strong> gibt <strong>1</strong> zurück.</td>
</tr>
<tr class="even">
<td>LEISTUNG (Zahl, Leistung)</td>
<td>Gibt das Ergebnis der angehobenen spezifischen positiven Zahl der angegebenen Leistung zurück.</td>
<td><strong>LEISTUNG (10, 2)</strong> gibt <strong>100</strong> zurück.</td>
</tr>
<tr class="odd">
<td>ZAHLENWERT (Zeichenfolge, Dezimaltrennzeichen, Zifferngruppierungstrennzeichen)</td>
<td>Konvertiert die angegebene Zeichenfolge zu einer Nummer. Das angegebene Symbol wird verwendet, um die ganzzahligen Teile und die Brüche einer Dezimalzahl abzugrenzen. Das angegebene Tausendertrennzeichen wird auch verwendet.</td>
<td><strong>ZAHLENWERT (&quot;1234,56 &quot;, &quot;,&quot;, &quot; &quot;)</strong> gibt den Wert <strong>1234,56</strong> zurück.</td>
</tr>
<tr class="even">
<td>WERT (Zeichenfolge)</td>
<td>Konvertiert die angegebene Zeichenfolge zu einer Nummer. Kommas und Punktzeichen (.) gelten als Dezimaltrennzeichen und es wird ein führender Bindestrich (-) als negatives Vorzeichen verwendet. Auflösen einer Ausnahme, wenn andere nichtnumerische Zeichen in der angegebenen Zeichenfolge auftreten.</td>
<td><strong>WERT (&quot;1 234,56&quot;)</strong> löst eine Ausnahme aus.</td>
</tr>
<tr class="odd">
<td>RUNDEN (Zahl, Dezimalen)</td>
<td>Gibt die angegebene Anzahl zurück, die für die angegebene Zahl von Dezimalstellen gerundet werden soll:
<ul>
<li>Wenn der angegebene Dezimalstellewert größer als 0 (null) ist, wird die angegebene Anzahl der angegebenen Anzahl auf Dezimalstellen gerundet.</li>
<li>Wenn der angegebene Dezimalstellewert 0 (null )ist, wird die angegebene Zahl auf die nächste ganze Zahl gerundet.</li>
<li>Wenn der angegebene Dezimalstellewert kleiner als 0 (null) ist, wird die angegebene Zahl links der Dezimalstelle gerundet.</li>
</ul></td>
<td><strong>RUNDUNG (1200.767, 2)</strong> Rundet auf zwei Dezimalstellen und gibt den Wert <strong>1200.77</strong> zurück.. <strong>RUNDUNG (1200.767, -3)</strong> Rundet auf das nächste Vielfache von 1,000 und gibt den Wert <strong>1000</strong> zurück.</td>
</tr>
<tr class="even">
<td>ABRUNDEN (Zahl, Dezimalen)</td>
<td>Gibt die angegebene Anzahl zurück, die für die angegebene Zahl von Dezimalstellen abgerundet (gegen Null) werden soll. <strong>Hinweis:</strong> Diese Funktion verhält sich wie <strong>RUNDUNG</strong>, rundet die angegebene Zahl aber immer ab.</td>
<td><strong>ABRUNDUNG (1200.767, 2)</strong> Rundet auf zwei Dezimalstellen ab und gibt den Wert <strong>1200.76</strong> zurück. <strong>ABRUNDUNG (1700.767, -3)</strong> Rundet auf das nächste Vielfache von 1,000 ab und gibt den Wert <strong>1000</strong> zurück.</td>
</tr>
<tr class="odd">
<td>AUFRUNDEN (Zahl, Dezimalen)</td>
<td>Gibt die angegebene Anzahl zurück, die für die angegebene Zahl von Dezimalstellen aufgerundet (weg von Null) werden soll. <strong>Hinweis:</strong> Diese Funktion verhält sich wie <strong>RUNDUNG</strong>, rundet die angegebene Zahl aber immer auf.</td>
<td><strong>AUFRUNDUNG (1200.763, 2)</strong> Rundet auf zwei Dezimalstellen auf und gibt den Wert <strong>1200.77</strong> zurück. <strong>-AUFRUNDUNG (1200.767, -3)</strong> Rundet auf das nächste Vielfache von 1,000 auf und gibt den Wert <strong>2000</strong> zurück.</td>
</tr>
</tbody>
</table>

**Datenumwandlungsfunktionen**

| Funktion             | Beschreibung                                                                                                                                                                                                                                     | Beispiel                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| WERT (Zeichenfolge) | Konvertiert die angegebene Zeichenfolge zu einer Nummer. Kommas und Punktzeichen (.) gelten als Dezimaltrennzeichen und es wird ein führender Bindestrich (-) als ein negatives Vorzeichen verwendet. Wenn andere nichtnumerische Zeichen in der angegebenen Zeichenfolge auftreten, tritt ein Fehler auf.                                                                                  | **WERT ("1 "234,56 ")** löst eine Ausnahme aus.   |
| ZAHLENWERT (Zeichenfolge, Dezimaltrennzeichen, Zifferngruppierungstrennzeichen) | Konvertiert die angegebene Zeichenfolge zu einer Nummer. Das angegebene Symbol wird verwendet, um die ganzzahligen Teile und die Brüche einer Dezimalzahl abzugrenzen. Das angegebene Tausendertrennzeichen wird auch verwendet.                                                                                  | **ZAHLENWERT ("1234,56 ", ",", " ")** gibt den Wert **1234.56** zurück.    |
| INTVALUE (Zeichenfolge) | Gibt eine Ganzzahl-Darstellung einer Zeichenfolge zurück. Alle verfügbaren Dezimalstellenteile werden gekürzt.                                                                                  | **INTVALUE ("100,77 ")** gibt **100** zurück. |
| INTVALUE (Zahl) | Gibt ganze Darstellung der Zahl zurück. Alle verfügbaren Dezimalstellenteile werden gekürzt.                                                                                  | **INTVALUE (-100,77)** gibt **-100** zurück. |
| INT64VALUE (Zeichenfolge) | Gibt die int64-Darstellung der Zeichenfolge zurück. Alle verfügbaren Dezimalstellenteile werden gekürzt.                                                                                  | **INT64VALUE ("22565422744")** gibt **22565422744** zurück. |
| INT64VALUE (Nummer) | Gibt die int64-Darstellung der Zahl zurück. Alle verfügbaren Dezimalstellenteile werden gekürzt.                                                                                  | **INT64VALUE (22565422744.00)** gibt **22565422744** zurück. |



### <a name="record-functions"></a>Datensatzfunktionen

| Funktion             | Beschreibung                                                                                                                                                                                                                                     | Beispiel                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| NULLCONTAINER (Liste) | Gibt einen **NULL**-Datensatz zurück, der die gleiche Struktur beinhaltet, wie die angegebene Datensatzliste oder Datensatz. **Hinweis:** Diese Funktion ist veraltet. Verwenden Sie stattdessen **EMPTYRECORD**.                                                                                  | **NULLCONTAINER (TEILEN ("abc", 1))** gibt einen neuen leeren Datensatz zurück, der dieselbe Struktur wie die Liste beinhaltet, die durch Funktion **TEILEN** zurückgegeben wird. |
| LEERER DATENSATZLIST (Datensatz) | Gibt einen **NULL**-Datensatz zurück, der die gleiche Struktur beinhaltet, wie die angegebene Datensatzliste oder Datensatz. **Hinweis:** Ein **Null** datensatz ist ein Datensatz, bei dem alle Felder einen leeren Wert haben (**0** \[Null\] für Zahlen, eine leere Zeichenfolge für Zeichen usw. | **LEERER DATENSATZ (TEILEN ("abc", 1))** gibt einen neuen leeren Datensatz zurück, der dieselbe Struktur wie die Liste beinhaltet, die durch Funktion **TEILEN** zurückgegeben wird.   |

### <a name="text-functions"></a>Textfunktionen

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>Beschreibung</th>
<th>Beispiel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GROSSBUCHSTABE (Zeichenfolge)</td>
<td>Gibt die angegebene Zeichenfolge zurück, die Großbuchstaben konvertiert wird.</td>
<td><strong>GROSSBUCHSTABE (&quot;Beispiel&quot;)</strong> gibt<strong>&quot;BEISPIEL&quot;</strong> zurück.</td>
</tr>
<tr class="even">
<td>KLEINBUCHSTABEN (Zeichenfolge)</td>
<td>Gibt die angegebene Zeichenfolge zurück, die zu Kleinbuchstaben konvertiert wird.</td>
<td><strong>KLEINBUCHSTABEN (&quot;Beispiel&quot;)</strong> gibt<strong>&quot;beispiel&quot;</strong> zurück.</td>
</tr>
<tr class="odd">
<td>LINKS (Zeichenfolge, Anzahl Zeichen)</td>
<td>Gibt die angegebene Anzahl von Zeichen ab Beginn einer Textzeichenfolge zurück.</td>
<td><strong>LINKS (&quot;Beispiel&quot;, 3)</strong> gibt <strong>&quot;Sam&quot;</strong> zurück.</td>
</tr>
<tr class="even">
<td>RECHTs (Zeichenfolge, Anzahl Zeichen)</td>
<td>Gibt die angegebene Anzahl von Zeichen ab Ende einer bestimmten Textzeichenfolge zurück.</td>
<td><strong>RECHTS (&quot;Beispiel&quot;, 3)</strong> gibt <strong>&quot;ple&quot;</strong> zurück.</td>
</tr>
<tr class="odd">
<td>MITTE (Zeichenfolge, Startposition, Anzahl Zeichen)</td>
<td>Gibt die angegebene Anzahl von Zeichen ab Beginn einer Textzeichenfolge zurück.</td>
<td><strong>MITTE (&quot;Beispiel&quot;, 2, 3)</strong> gibt <strong>&quot;amp&quot;</strong> zurück.</td>
</tr>
<tr class="even">
<td>LEN (Zeichenfolge)</td>
<td>Gibt die Anzahl von Zeichen in einer Textzeichenfolge zurück.</td>
<td><strong>LEN (&quot;Beispiel&quot;)</strong> gibt <strong>6</strong> zurück.</td>
</tr>
<tr class="odd">
<td>CHAR (Nummer)</td>
<td>Gibt die Zeichenfolge von Zeichen zurück, die von der angegebene Unicode-Zahl angegeben wird.</td>
<td><strong>CHAR (255)</strong> gibt <strong>&quot;Ÿ&quot;</strong> zurück. <strong>Hinweis:</strong> Die zurückgegebene Zeichenfolge hängt von der Codierung ab, die im übergeordneten DATEIformatelement aktiviert ist. Die Liste unterstützter Codierungen kann im Thema <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Codierungs-Klasse</a> enthalten sein.</td>
</tr>
<tr class="even">
<td>VERKETTEN (Zeichenfolge 1, [, Zeichenfolge 2, ...])</td>
<td>Gibt alle angegebenen Textzeichenfolgen zurück, die in eine Zeichenfolge verknüpft werden.</td>
<td><strong>VERKETTEN (&quot;ABC&quot;, &quot;def&quot;)</strong> gibt <strong>&quot;abcdef&quot;</strong> zurück. <strong>Hinweis: </strong>Der Ausdruck <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong> gibt auch <strong>&quot;abcdef&quot;</strong> zurück.</td>
</tr>
<tr class="odd">
<td>ÜBERSETZEN (Zeichenfolge, Muster, Ersetzung)</td>
<td>Gibt die angegebene Zeichenfolge zurück, in der alle Vorkommen der Zeichen in der angegebenen Musterzeichenfolge durch die Zeichen in der entsprechenden Position der angegebenen Ersetzungszeichenfolge ersetzt werden.</td>
<td><strong>ÜBERSETZEN (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> ersetzt das Muster <strong>&quot;cd&quot;</strong> durch die Zeichenfolge <strong>&quot;GH&quot;</strong> und gibt <strong>&quot;abGHef&quot;</strong> zurück.</td>
</tr>
<tr class="even">
<td>ERSETZEN (Zeichenfolge, Muster, Ersetzung, Markierung des regulären Ausdrucks)</td>
<td>Wenn die angegebene Markierung des regulären Ausdrucks <strong>wahr</strong> ist, wird die angegebene Zeichenfolge zurückgegeben, die durch Anwendung des normalen Ausdruck angewendet wird, der als ein Musterargument für diese Funktion angegeben ist. Dieser Ausdruck wird verwendet, um Zeichen zu finden, die ersetzt werden müssen. Zeichen des angegebenen Ersetzungsarguments werden verwendet, um Zeichen zu ersetzen, die gefunden werden. Wenn die angegebene Markierung des regulären Ausdrucks <strong>falsch</strong> ist, verhält sich diese Funktion wie <strong>ÜBERSETZEN</strong>.</td>
<td>  <strong>ERSETZEN (&quot;+1 923 456 4971&quot;, &quot;[^0-9]&quot;, &quot;&quot;, true)</strong> übernimmt einen regulären Ausdruck, der alle nicht numerischen Symbole entfernt und <strong>&quot;19234564971&quot;</strong> zurückgibt. <strong>ERSETZEN (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> ersetzt das Muster <strong>&quot;cd&quot;</strong> mit der Zeichenfolge <strong>&quot;GH&quot;</strong> und gibt <strong>&quot;abGHef&quot;</strong> zurück.</td>
</tr>
<tr class="odd">
<td>TEXT (Eingabe)</td>
<td>Gibt die angegebene Eingabe zurück, die in eine Textzeichenfolge umgerechnet wird, die gemäß den Servergebietsschemaeinstellungen der aktuellen Finance and Operations-Instanz formatiert wird. Für Werte für den<strong>tatsächlich</strong> Typ, wird die Zeichenkonvertierung auf zwei Dezimalstellen beschränkt.</td>
<td>Wenn das Finance and Operations-Instanz-Server-Gebietsschema folgendermaßen definiert wird <strong>EN-US</strong>, <strong>TEXT (NOW())</strong> zeigt das laufende Finance and Operations-Sitzungsdatum, 12/17/2015 als Textzeichenfolge <strong>&quot;12/17/2015 07:59:23 AM&quot;</strong> an. <strong>TEXT (1/3)</strong> gibt <strong>&quot;0.33&quot;</strong> zurück.</td>
</tr>
<tr class="even">
<td>FORMAT (Zeichenfolge 1, Zeichenfolge 2 [, Zeichenfolge 3,...])</td>
<td>Geben Sie die angegebene Zeichenfolge zurück, die formatiert wird, indem alle Vorkommnisse von <strong>%N</strong> mit dem <em>n</em>. Argument ersetzt werden. Die Argumente sind Zeichenfolgen. Wenn eine Anfrage nicht für einen Parameter angegeben wird, wird der Parameter als <strong>&quot;%N&quot;</strong> in der Zeichenfolge zurückgegeben. Für Werte für den<strong>tatsächlich</strong> Typ, wird die Zeichenkonvertierung auf zwei Dezimalstellen beschränkt.</td>
<td>In diesem Beispiel gibt die <strong>PaymentModel</strong>Datenquelle die Liste von Kundeneinträgen über die <strong>-Kunden</strong>komponente und die Prozessdatenwerte über das Feld <strong>ProcessingDate</strong> ein. <a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>Im ER-Format, das entworfen wurde, um eine Datei für ausgewählte Debitoren zu generieren, wird <strong>PaymentModel</strong> als Datenquelle ausgewählt, um den Prozessablauf zu steuern. Eine Ausnahme wird für Endbenutzer ausgelöst, wenn ein ausgewählter Debitoren für das Datum beendet wird, an dem der Bericht verarbeitet wird. Die Formel, die für diese Art von Prozesssteuerung entworfen wurde, kann die folgenden Ressourcen verwenden:
<ul>
<li>Finance and Operations-Beschriftung SYS70894, die den folgenden Text hat:
<ul>
<li><strong>Für die EN-US-Sprache: </strong>&quot;Nichts zu drucken&quot;</li>
<li><strong>Für deutsche Sprache:</strong> &quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>Finance and Operations-Beschriftung SYS18389, die den folgenden Text hat:
<ul>
<li><strong>Für die EN-US-Sprache:</strong> &quot;Debitor %1 wird beendet für %2.&quot;</li>
<li><strong>Für deutsche Sprache: </strong>&quot;Debitor "%1 "wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
Ist hier die Formel, die so konzipiert werden kann: FORMAT (VERKETTEN (@&quot;SYS70894&quot;, &quot;. &quot;, @&quot;SYS18389&quot;) model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;D&quot;)) Wenn ein Bericht für den <strong>Einzelhandelskunden Litwares</strong> am 17. Dezember 2015 in der <strong>EN-US</strong>-Kultur und in der <strong>EN-US</strong>-Sprache verarbeitet wird, gibt diese Formel den folgenden Text zurück, der als Ausnahmebedingungsnachricht für den Endbenutzer produziert werden kann: &quot;Nichts zu drucken. Customer Litware Retail ist zum 17.12.2015 beendet.&quot; Wenn derselbe Bericht für den Einzelhandelskunden<strong> Litwares</strong> am 17. Dezember 2015, in der <strong>DE</strong>-Kultur und in der <strong>DE</strong>-Sprache verarbeitet wird, gibt diese Formel den folgenden Text zurück, der ein anderes Datumsformat verwendet: &quot;Nichts zu drucken. Schuldner-"Litware Retail" wird für 17.12.2015 gesperrt.&quot; <strong>Hinweis:</strong> Die folgende Syntax wird in ER-Formeln für Beschriftungen übernommen:
<ul>
<li><strong>Für Beschriftungen von Finance and Operations-Ressourcen:</strong> <strong>@&quot;X&quot;</strong>, wo die Beschriftungskennung in der Entwicklungsumgebung (AOT) ist</li>
<li><strong>Für Beschriftungen, die sich in der ER-Konfigurationen befinden:</strong> <strong>@&quot;GER_LABEL:X&quot;</strong>, wo die Beschriftungskennung in der ER-Konfiguration ist</li>
</ul></td>
</tr>
<tr class="odd">
<td>ZAHLENFORMAT (Zahl, Format)</td>
<td>Gibt die angegebene Anzahl von Zeichen ab Beginn einer Zahlenfolge zurück. (Informationen zum die unterstützten Formaten, finden Sie unter <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">Standard</a> und <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">Custom</a>.) Im Kontext, dass diese Funktion ausgeführt wird, bestimmt die Kultur, die den Formatnummern verwendet wird.</td>
<td>Für EN-US Kultur <strong>ZAHLENFORMAT (0.45, &quot;p&quot;)</strong> gibt <strong>&quot;45,00 %&quot;</strong> zurück. <strong>ZAHLENFORMAT (10,45, &quot;#&quot;)</strong> gibt<strong>&quot;10&quot;</strong> zurück.</td>
</tr>
<tr class="even">
<td>NUMERALSTOTEXT (Nummer, Sprache, Währung, Drucktwährungsnamenmarkierung, Dezimaltrennzeichen)</td>
<td>Gibt die Nummer zurück, die in Textzeichenfolgen in der definierten Sprache formuliert (konvertiert) wurde. Der Sprachcode ist optional: wenn dieser als Nullkette definiert ist, wird der laufende Kontextsprachcode (definiert für einen generierten Ordner oder eine Datei) stattdessen verwendet. Der Währungscode ist optional. Wenn dieser als Nullkette definiert ist, wird die Unternehmenswährung verwendet. Hinweis, der <strong>Druckwährungsnamen</strong>parameter und der <strong>Dezimaltrennzeichen</strong>-Parameter werden nur für die folgenden Sprachcodes analysiert: <strong>CS</strong><strong>ET</strong><strong>HU</strong><strong>LT</strong><strong>LV</strong><strong>PL</strong><strong>RU</strong>. Der <strong>Druckwährungsname</strong>-Parameter wird nur für Finance and Operations mit dem Länder-Kontext analysiert, der die Deklination der Währung unterstützt.</td>
<td>NUMERALSTOTEXT (1234,56, &quot;EN&quot;, &quot;&quot;, false, 2) gibt “One Thousand Two Hundred Thirty Four and 56” NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, false, 0) gibt “Sto dwadzieścia” NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, true, 2) gibt “Сто двадцать евро 21 евроцент” zurück.</td>
</tr>
<tr class="odd">
<td>PADLEFT (Zeichenfolge, Länge, Zeichen auffüllen)</td>
<td>Gibt eine Zeichenfolge mit einer angegebenen Länge zurück, bei der der Anfang der aktuellen Zeichenfolge mit angegebenen Zeichen aufgefüllt ist.</td>
<td>PADLEFT ("1234", 10, " ")  gibt die Textzeichenfolge "    1234 zurück"</td>
</tr>
<tr class="even">
<td>TRIM (Zeichenfolge)</td>
<td>Gibt den jeweiligen Text zurück, nachdem voran- und nachgestellte Leerstellen gekürzt und mehrere Leerstellen zwischen Wörtern entfernt wurden. </td>
<td><strong>TRIM ("     Beispielhafter     Text     ")</strong> gibt <strong>"Beispielhafter Text"</strong> zurück.</td>
=======
<td>GETENUMVALUEBYNAME (Enumerationsdatenquellenpfad, Enumerationswertbeschriftungstext)</td>
<td>Gibt einen Wert einer angegebenen Enumerationsdatenquelle nach angegebenen Text dieser Enumerationsbeschriftung zurück.</td>
<td>Das folgende Beispiel zeigt die in einem Datenmodell eingeführte Enumeration "ReportDirection". Beachten Sie, dass Beschriftungen für Enumerationswerte definiert werden.
Das folgende Beispiel zeigt:
<ul><li>Modellenumeration <strong>ReportDirection</strong> in einen Bericht als eine Datenquelle <strong>$Direction</strong> eingefügt</li>
<li>ER-Ausdruck <strong>$IsArrivals</strong> wurde entwickelt, um Modellenumerationen als Parameter für diese Funktion zu verwenden. Der Wert dieses Ausdrucks ist <strong>WAHR</strong></li></ul></td>
</tr>
</tbody>
</table>

**Datenumwandlungsfunktionen**

| Funktion             | Beschreibung                                                                                                                                                                                                                                     | Beispiel                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| TEXT (Eingabe) | Gibt die angegebene Eingabe zurück, die in eine Textzeichenfolge umgerechnet wird, die gemäß den Servergebietsschemaeinstellungen der aktuellen Finance and Operations-Instanz formatiert wird.
Für Werte für dentatsächlich Typ, wird die Zeichenkonvertierung auf zwei Dezimalstellen beschränkt.| Wenn das Finance and Operations-Instanz-Server-Gebietsschema folgendermaßen definiert wird **EN-US, TEXT (NOW())** wird das laufende Finance and Operations-Sitzungsdatum 12/17/2015 als Textzeichenfolge **"12/17/2015 07:59:23 AM"** zurückgegeben.
**TEXT (1/3) gibt "0.33"** zurück. |
| QRCODE (Zeichenfolge) | Gibt einen QR-Bildcode im base64-Binärformat für eine angegebene Zeichenfolge zurück. | **QRCODE (“Beispieltext”)** gibt **U2FtcGxlIHRleHQ=** zurück.   |

### <a name="data-collection-functions"></a>Datensammlungsfunktionen

| Funktion             | Beschreibung                                                                                                                                                                                                                                     | Beispiel                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| FORMATELEMENTNAME () | Gibt den Namen des aktuellen Elements des Formats zurück. Gibt leere Zeichenfolgen zurück, wenn die Markierung **Ausgabedetails sammeln** der aktiven Dateien deaktiviert ist.| Beziehen Sie sich auf **ER Benutzerdaten der Formatausgabe für Inventur und Summierungen** (Teil des Geschäftsprozesses **IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln**)Aufgabenleitfaden, um weitere Informationen über die Verwendung der Funktionen zu erhalten. |
| SUMIFS (Schlüsselzeichenfolge zum Summieren, Kriterien Range1 Zeichenfolge \[, Kriterien Value1 Zeichenfolge [,Kriterien Range2 Zeichenfolge, Kriterien Value2 Zeichenfolge, …\]) |Gibt eine Summe von einem Wert aus Knoten (mit Name, der als Schlüssel bestimmt ist) von XML zurück, der während dieser Formatausführung gesammelt wurde und die eingegebenen Bedingungen erfüllt (Paare-Bereich und Wert). Gibt Nullwerte zurück, wenn die Markierung **Ausgabedetails sammeln** der aktuellen Dateien deaktiviert ist. |            |
| SUMIF (Schlüsselzeichenfolge zum Summieren, Kriterien-Bereichszeichenfolge, Kriterien-Wertzeichenfolge) | Gibt eine Summe von einem Wert aus Knoten (mit Name, der als Schlüssel bestimmt ist) von XML zurück, der während dieser Formatausführung gesammelt wurde und die eingegebenen Bedingungen erfüllt (Bereich und Wert). Gibt Nullwerte zurück, wenn die Markierung **Ausgabedetails sammeln** der aktuellen Dateien deaktiviert ist.|           |
| COUNTIFS (Kriterien Range1 Zeichenfolge, Kriterien Value1 Zeichenfolge \[, Kriterien Range2 Zeichenfolge, Kriterien Value2 Zeichenfolge…\]]) | Gibt eine Zahl von Knoten von XML zurück, der während dieser Formatausführung gesammelt wurde und die eingegebenen Bedingungen erfüllt (Paare-Bereich und Wert). Gibt Nullwerte zurück, wenn die Markierung **Ausgabedetails sammeln** der aktuellen Dateien deaktiviert ist.|     |
| COUNTIF (Kriterien-Bereichszeichenfolge, Kriterien-Wertzeichenfolge) | Gibt eine Zahl von Knoten von XML zurück, die während dieser Formatausführung gesammelt wurde und die eingegebenen Bedingungen erfüllt (Bereich und Wert). Gibt Nullwerte zurück, wenn die Markierung **Ausgabedetails sammeln** der aktuellen Dateien deaktiviert ist.|          |
| COLLECTEDLIST ((Kriterien Range1 Zeichenfolge, Kriterien Value1 Zeichenfolge \[, Kriterien Range2-Zeichenfolge, Kriterien Value2 Zeichenfolge…\]]) | Gibt eine Liste von Werten von Knoten von XML zurück, die während dieser Formatausführung gesammelt wurden und die eingegebenen Bedingungen erfüllen (Bereich und Wert). Gibt eine leere Liste zurück, wenn die Markierung **Ausgabedetails sammeln** der aktiven Dateien deaktiviert ist.|               |   




### <a name="other-business-domainspecific-functions"></a>Andere (geschäftsdomänenspezifische) Funktionen

| Funktion                                                                         | Beschreibung                                                                                                                                                                                                                                                        | Beispiel                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONVERTCURRENCY (Betrag, Quellwährung, Zielwährung, Datum, Unternehmen)        | Konvertiert den bestimmten Geldbetrag aus der Quellwährung in die Zielwährung, indem Sie die Einstellungen des angegebenen Finance and Operations-Unternehmens am angegebenen Datum verwenden.                                                                            | **CONVERTCURRENCY (1, "EUR", "USD", HEUTE (), "DEMF")** gibt die Entsprechung von einem Euro in US Dollar am Datum der aktuellen Sitzung, auf den Einstellungen für das DEMF-Unternehmen zurück.                                                                                                                                  |
| ROUNDAMOUNT (Anzahl, Dezimalstellen, Rundungsregel)                                       | Abrunden des angegebenen Betrags gemäß der angegebenen Rundenregel und der angegebenen Anzahl von Dezimalstellen. **Hinweis:** Die Rundenregel muss als Wert der Finance and Operations **RoundOffType**-Enumeration angegeben werden.                          | Wenn der **model.RoundOff**-Parameter auf ****Abwärts**** festgelegt ist, gibt **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** den Wert **1000,78** zurück. Wenn der **model.RoundOff**-Parameter entweder auf **Normal** oder **Aufrunden** **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** festgelegt wird, wird der Wert **1000.79** zurückgegeben. |
| CURCredRef (Ziffern)                                                              | Gibt eine Gläubigerreferenz basierend auf den Ziffern der angegebenen Rechnungsnummer zurück.                                                                                                                                                                                  | **CURCredRef ("VEND-200002")** gibt **"2200002"** zurück.                                                                                                                                                                                                                                                         |
| MOD\_97 (Ziffern)                                                                 | Gibt eine Gläubigerreferenz als MOD97 Ausdruck zurück, basierend auf den Ziffern der angegebenen Rechnungsnummer.                                                                                                                                                            | **MOD\_97 ("VEND-200002")** gibt **"20000285"** zurück.                                                                                                                                                                                                                                                           |
| ISOCredRef (Ziffern)                                                              | Gibt eine ISO-Gläubigerreferenz basierend auf den Ziffern und alphabetischen Symbolen der angegebenen Rechnungsnummer zurück. **Hinweis:** Um Symbole aus dem Alphabet zu entfernen, die nicht ISO-kompatibel sind, muss der Eingabeparameter übersetzt werden, bevor er diese Fähigkeit hat. | **ISOCredRef ("VEND-200002")** gibt **"RF23VEND-200002"** zurück.                                                                                                                                                                                                                                                 |
| CN\_GBT\_AdditionalDimensionID (Zeichenfolge, Zahl)                                  | Ruft die zusätzliche Finanzdimensions-ID ab. Dimensionen werden in dieser Zeichenfolge als durch Trennzeichen getrennte IDs dargestellt. Nummern definieren die gewünschten Dimensionssequenz in dieser Zeichenfolge.                                                                            | CN\_GBT\_AdditionalDimensionID (AA ", DD CC Typ, EE, FF, GG," 3 ", gibt "CC"                                                                                                                                                                                                                                      |
| GetCurrentCompany ()                                                             | Gibt die Textdarstellung eines Codes einer juristischen Person (Unternehmen) zurück, für die ein Benutzer derzeit angemeldet ist.                                                                                                                                                                                                                    | **GETCURRENTCOMPANY ()** gibt **USMF** für einen Benutzer an, der beim Finance and Operations-Unternehmen **Contoso Entertainment System USA** angemeldet ist.                                                                                                                                                                                                                                                                                                              |
| CH\_BANK\_MOD\_10 (Stellen)                                                       | Gibt eine Kreditorenreferenz als MOD10 Ausdruck zurück, basierend auf den Ziffern der angegebenen Rechnungsnummer.                                                                                                                                                                      | CH\_BANK\_MOD\_10 ("VEND-200002") gibt 3                                                                                                                                                                                                                                                                   |
| FA\_SUM (Anlagencode, Wertmodellcode, Startdatum, Enddatum)               | Gibt den vorbereiteten Datencontainer von Anlagenbeträgen für eine Periode zurück.                                                                                                                                                                                         | FA\_SUM ("COMP-000001", "Current", Date1, Date2) gibt den Datenencontainer der Anlage "COMP-000001" mit dem Wertmodell "Current" für eine Periode von Date1 zu Date2 zurück.                                                                                                                        |
| FA\_BALANCE (Anlagencode, Wertmodellcode, Berichtsjahr, Meldedatum) | Gibt den vorbereiteten Datencontainer von Anlagensalden zurück. Berichterstellungsjahr muss als Wert der Finance and Operations-Enumeration **AssetYear** angegeben werden.                                                                                           | FA\_SUM ("COMP-000001", "Currentl", AxEnumAssetYear.ThisYear, SESSIONTODAY ()) Gibt die vorbereiteten Datenencontainer von Salden für die Anlage "COMP-000001" mit dem Wertmodell "Aktuell" auf dem aktuellen Finance and Operations-Sitzungsdatum zurück.                                                                |
| TABLENAME2ID (Zeichenfolge)                                                       | Gibt ganzzahlige Darstellung einer Tabellenkennung für einen bestimmten Tabellennamen zurück.                                                                                                                                                                      | **TABLENAME2ID ("Intrastat ")** gibt **1510** zurück.                                                                                                                                                                                                                                                                   |
| ISVALIDCHARACTERISO7064 (Zeichenfolge)                                                       | Gibt den booleschen Wert **WAHR** zurück, wenn eine bestimmte Zeichenfolge eine gültige internationale Bankkontonummer (IBAN) darstellt. Gibt andernfalls den booleschem Wert **FALSCH** zurück.                                                                                                                                                                      | **ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")** gibt **WAHR** zurück. **ISVALIDCHARACTERISO7064 ("AT61")** gibt **FALSCH** zurück.                                                                                                                                                                                                                                                                   |

### <a name="functions-list-extension"></a>Listenerweiterung der Funktionen

ER ermöglicht es Ihnen, die Liste von Funktionen zu verlängern, die in ER-Ausdrücken verwendet werden. Etwas technischer Aufwand ist hierfür erforderlich. Ausführliche Informationen finden Sie unter [Erweitern der Liste der elektronischen Berichtsfunktion](general-electronic-reporting-formulas-list-extension.md).

<a name="see-also"></a>Siehe auch
--------

[Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)

[Erweitert die Liste der elektronischen Berichtsfunktion (ER)](general-electronic-reporting-formulas-list-extension.md)




