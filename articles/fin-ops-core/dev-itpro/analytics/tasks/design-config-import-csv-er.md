---
title: EB-Konfigurationen entwerfen, um Daten aus externen CSV-Dateien zu importieren
description: Nutzen Sie diese Prozedur, um Konfigurationen zur elektronischen Berichterstellung (EB) zu erstellen, um Daten in die Finance and Operations-App aus einer externen Datei im CSV-Format zu importieren.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fbae4570448a6bb1309ffe0092ff9b07825d717
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092765"
---
# <a name="design-er-configurations-to-import-data-from-external-csv-files"></a>EB-Konfigurationen entwerfen, um Daten aus externen CSV-Dateien zu importieren

[!include [banner](../../includes/banner.md)]

Nutzen Sie diese Prozedur, um Konfigurationen zur elektronischen Berichterstellung (EB) zu erstellen, um Daten in die Anwendung aus einer externen Datei im CSV-Format zu importieren. In diesem Verfahren erstellen Sie erforderliche ER-Konfigurationen für das Beispielunternehmen, Litware, Inc. Um diesen Aufgabenleitfaden abzuschließen, müssen Sie die Schritte im Verfahren erst abschließen, ER bieten einen Konfigurationsanbieter erstellen und als aktiv markieren.

Diese Prozedur wird für Benutzer erstellt, die die Rolle des Systemadministrators oder des Entwicklers für elektronische Berichterstellung haben, die ihnen zugewiesen sind. Die Schritte können abgeschlossen werden, indem Sie den USMF-Datensatz verwenden.

Sie müssen auch die folgenden Dateien herunterladen und lokal speichern: [Dynamics 365 Finance Beispiele für die elektronische Berichterstellung](https://go.microsoft.com/fwlink/?linkid=862266): 1099model.xml, 1099formatcsv.xml, 1099entriescsv.csv.

1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
    * Sie können einen Prozesses konfigurieren, um externe Dateien im XML-, TXT- oder CSV-Format in Tabellen in der Anwendung zu importieren. Zunächst müssen Sie ein abstraktes Datenmodell erstellen, um die importierten Daten darzustellen, von einem Geschäftsstandpunkt aus wird dafür eine Datenmodellkonfiguration für die elektronische Berichterstellung erstellt. Als nächstes definieren Sie eine Struktur der importierten Datei, die dem entworfenen Datenmodell zugeordnet ist, als Methode, um Daten aus der Datei in das abstrakte Datenmodell zu übertragen – dazu wird eine Formatkonfiguration für die elektronische Berichterstellung erstellt. Anschließend muss die Datenmodellkonfiguration für die elektronische Berichterstellung mit einer neuen Modellzuordnung erweitert werden, die beschreibt, wie die Daten aus der importierten Datei und die persistierten Daten aus dem abstrakten Datenmodell verwendet werden, um die Anwendungstabellen oder Datenentitäten zu aktualisieren.
    * Die nachfolgenden Schritte veranschaulichen, wie extern nachverfolgte Kreditorentransaktionen aus der externen CSV-Datei importiert werden, um dann später im Ausgleich des Kreditors für 1099-Formulare (für Steuererklärung US 1099) verwendet zu werden.
    * Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als aktiv markiert ist. Sollten Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte der Prozedur „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.
2. Klicken Sie auf "Berichterstellungskonfigurationen".
3. Wenden Sie den Filter „US 1099-Steuerzahlungsmodell” an. Wenn Sie schon die Prozedur „EB – Erforderliche Konfigurationen erstellen, um Daten aus einer externen Datei für die elektronische Berichterstellung importieren“ abgeschlossen haben und die Konfiguration „US 1099-Steuerzahlungsmodell“ in der Konfigurationsstruktur verfügbar ist, überspringen Sie alle Schritte in der nächsten Unteraufgabe.

## <a name="add-a-new-er-model-configuration"></a>Neue ER-Modellkonfiguration hinzufügen

1. Statt ein neues Modell zu erstellen, um den Datenimport zu unterstützen, laden Sie die Datei „1099model.xml”, die Sie zuvor heruntergeladen haben. Diese Datei enthält ein benutzerdefiniertes Datenmodell der Kreditorenbuchungen. Dieses Datenmodell ist bereits den erforderlichen Datenkomponenten zugeordnet.
2. Klicken Sie auf „Austauschen”.
3. Klicken Sie auf „Aus XML-Datei laden”.
4. Klicken Sie auf „Durchsuchen” und navigieren Sie zur Datei 1099model.xml, die Sie bereits zuvor heruntergeladen haben.
5. Klicken Sie auf "OK".

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Neue ER-Formatkonfiguration hinzufügen, die Datenimport unterstützt

1. Wählen Sie in der Struktur „US 1099-Steuerzahlungsmodell” aus.
2. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
3. Geben Sie im Feld „Neu” folgende Bezeichnung ein: „Format basierend auf Datenmodell US 1099-Steuerzahlungsmodell”.
4. Wählen Sie die Option „Ja” im Feld „Unterstützt Datenimport” aus.
5. Drücken Sie die ESC-TASTE, um diese Seite zu schließen.
    * Statt ein neues EB-Format zu erstellen, um den Datenimport zu unterstützen, laden Sie die Datei „1099formatcsv.xml”, die Sie zuvor heruntergeladen haben. Diese Datei enthält das erforderliche EB-Format, das die Struktur der eingehenden CSV-Datei definiert und die Zuordnung dieser Struktur zum Datenmodell von den Kreditorenbuchungen.
6. Klicken Sie auf „Austauschen”.
7. Klicken Sie auf „Aus XML-Datei laden”.
    * Klicken Sie auf „Durchsuchen” und navigieren Sie zur Datei „1099formatcsv.xml”, die Sie bereits zuvor heruntergeladen haben.
8. Klicken Sie auf "OK".
9. Erweitern Sie „US 1099-Steuerzahlungsmodell” in der Struktur.
10. Wählen Sie in der Struktur „US 1099-Steuerzahlungsmodelll\Für den Import von Kreditorenbuchungen (CSV)” aus.

## <a name="review-format-settings"></a>Formateinstellungen überprüfen

1. Klicken Sie auf Designer.
2. Klicken Sie „Erweitern/reduzieren”.
3. Schalten Sie „Details anzeigen” ein.
    * Das entworfene Format stellt die erwartete Struktur der externen Datei im CSV-Format dar.
4. Wählen Sie in der Struktur „Eingehend: Datei\Stamm: Nummernkreis” aus.
    * Für das Stammelement vom Typ NUMMERNKREIS, wurde die Option „Neue Position – Windows (CR LF)“ im Feld „Sonderzeichen“ ausgewählt. Basierend auf dieser Einstellung muss jede Position in der Analysedatei als ein separater Datensatz behandelt werden.
5. Wählen Sie in der Struktur `Incoming: File\Root: Sequence\Line: Sequence 1..*` aus.
    * Für das Stamm\Position-Element des Typs NUMMERNKREIS wurde die Option „Eins viele“ im Feld „Multiplizität“ ausgewählt. Basierend auf dieser Einstellung wird mindestens eine Position in der Analysedatei dargestellt.
6. Wählen Sie in der Struktur `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case` aus.
    * Beachten Sie, dass das Element Stamml\Positionl\Typen des Typs ANFRAGE als verschachteltes Element dem Nummernkreis Stamml\Position hinzugefügt wurde. Da dieses ANFRAGE-Element 3 geschachtelte Nummernkreiselemente enthält, wird bei dieser Einstellung davon ausgegangen, dass erwartungsgemäß 3 verschiedene Positionstypen in der Analysedatei angetroffen werden.
7. Wählen Sie in der Struktur `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Header: Sequence 1..1` aus.
    * Das Element Stamm\Position\Typen\Kopf des Typs NUMMERNKREIS enthält das geschachtelte Element ZEICHENFOLGE, dessen Wert als feste Zeichenfolgenwert definiert wurde. Dieser Nummernkreis analysiert die Kopfposition der Analysedatei.
8. Wählen Sie in der Struktur `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)` aus.
    * Das Element Stamm\Position\Typen\Datensatz des Typs NUMMERNKREIS wurde konfiguriert, um die Buchungspositionen zu analysieren. Beachten Sie, dass die Zeichenoption für „Benutzerdefiniertes Trennzeichen“ als Komma konfiguriert wurde. Dies bedeutet, dass das Komma als ein Trennzeichen für Felder für diesen Positionstyp in der Analysedatei verwendet wird.
    * Beachten Sie, dass mehrere geschachtelte Elemente verschiedener Datentypen für das Element Stamm\Zeile\Typen\Datensatz hinzugefügt wurden, um die Positionen der Transaktion als getrennte Felder zu analysieren. Beachten Sie, dass die Option „Angebotsanwendung“ als „Keine“ konfiguriert worden ist. Dies bedeutet, dass in der Analysedatei alle Felder dieses Typs so betrachtet werden, als ob sie keine eingeschlossenen Zeichen hätten.
9. Wählen Sie in der Struktur `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\TransactionDate: DateTime` aus.
    * Beispielsweise wurde das Element Stamm\Position\Typen\Datensatz\Transaktionsdatumselement des Typs DATUM/UHRZEIT so konfiguriert, dass es den Datums- und Uhrzeitwert der Transaktion aus der Analysedatei im Format „T/M/JJJJ“ abruft.
10. Wählen Sie in der Struktur `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\CountryCode: String 0..1` aus.
    * Beachten Sie, dass das Element Stamm\Position\Typen\Datensatz\Ländercode des Typs ZEICHENFOLGE so konfiguriert wurde, dass es die Option „Null eins“ im Feld „Multiplizität“ hat. Bei dieser Einstellung wird der Wert des Felds CountryCode in der Analyseposition als optional betrachtet.
11. Wählen Sie in der Struktur `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\Remark: Sequence 1..1 (,)` aus.
    * Beachten Sie, dass das Element Stamm\Position\Typen\Datensatz\Hinweis des Typs NUMMERNKREIS so konfiguriert ist, dass es die Option „Alle“ im Feld „Angebotsanwendung“ sowie ein doppeltes Anführungszeichen im Feld „Anführungszeichen“ hat. Dies bedeutet, dass alle Felder dieses Positionstyps in der Analysedatei (beschrieben durch die geschachtelten Elemente: Text des Typs ZEICHENFOLGE) als in doppelte Anführungszeichen eingeschlossen betrachtet werden.
12. Wählen Sie in der Struktur `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Unparsed: Sequence 1..1` aus.
    * Das Element „Stamm\Position\Typen\Nicht analysiert” des Typs NUMMERNKREIS wurde so konfiguriert, dass es die Buchungspositionen für die Struktur analysiert, die nicht mit der oben beschriebenen Struktur im übergeordneten Element ANFRAGE übereinstimmt.

## <a name="review-the-setting-of-the-format-mapping-to-the-data-model"></a>Die Einstellung der Formatzuordnung zum Datenmodell überprüfen

1. Klicken Sie auf „Format zu Modell zuordnen”.
    * Die Modellzuordnung „Zuordnungsmodell aus CSV-Format“ beschreibt den Datenfluss der Datenübertragung von der eingehenden CSV-Datei bis hin zum Datenmodell.
2. Klicken Sie auf Designer.
3. Erweitern Sie in der Struktur Format.
    * Beachten Sie, dass das entworfene Format hier als eine Datenquellenkomponente dargestellt wird.
4. Erweitern Sie in der Struktur „Format\Eingehend: Datei(Eingehend)”.
5. Erweitern Sie in der Struktur „Format\Eingehend: Datei(Eingehend)\Stamm: Nummernkreis(Stamm)”.
6. Erweitern Sie in der Struktur `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)`.
7. Erweitern Sie in der Struktur `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)`.
8. Erweitern Sie in der Struktur `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)`.
9. Erweitern Sie in der Struktur `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data`.
10. Erweitern Sie in der Struktur `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data\CountryCode: String 0..1 (CountryCode)`.
11. Wählen Sie in der Struktur `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data\TransactionDate: DateTime(TransactionDate)` aus.
    * Beachten Sie, dass die erforderlichen und optionalen Formatelemente wie TransactionDate und CountryCode in der vordefinierten Datenquellenkomponente „Format“ anders aussehen.
12. Erweitern Sie in der Struktur „Transaktionen = '$both'”.
    * Beachten Sie, dass die Elemente des Formats, das die Struktur der importierten Datei definiert an die Elemente des Datenmodells gebunden sind. Basierend auf diesen Bindungen wird der Inhalt der importierten CSV-Datei zur Laufzeit in das vorhandene Datenmodell gespeichert. Beachten Sie die Bindung des Elements CountryRegion. Bei jedem Buchungselement in der eingehenden Datei, für das kein Ländercodewert angegeben worden ist, wird der Standardländercode „USA“ im Datenmodell aufgefüllt.
13. Schalten Sie nun „Details anzeigen“ ein.
14. Klicken Sie auf die Registerkarte „Überprüfungen”.
15. Klicken Sie auf "Suchen".
16. Geben sie im Feld „Suchen” das Wort „Kred.” ein.
17. Klicken Sie auf „Weitersuchen”.
    * Diese Formatzuordnung enthält ggf. benutzerdefinierte Logik, um die Genauigkeit der importierten Daten aus einem Geschäftsstandpunkt zu überprüfen. Basierend auf der Einstellung wird für jede Position in der importierten Datei, deren Struktur weder mit der Struktur der Kopfzeilenposition noch der Buchungsposition übereinstimmt, eine Warnmeldung im Infolog generiert, die den Benutzer über diesen Fall informiert, wobei die Sequenznummer der Buchung in der Datei angegeben wird.
18. Schließen Sie die Seite.

## <a name="run-the-format-mapping"></a>Die Formatzuordnung ausführen

Zu Textwecken führen Sie die Formatzuordnung mithilfe der Datei 1099entriescsv.csv aus, die Sie zuvor heruntergeladen haben. Die generierte Ausgabe stellt Daten dar, die aus der ausgewählten CSV-Datei importiert werden und im benutzerdefinierte Datenmodell beim tatsächlichen Import aufgefüllt werden.

1. Klicken Sie auf "Ausführen".
    * Klicken Sie auf „Durchsuchen” und navigieren Sie zur Datei 1099entriescsv.csv, die Sie bereits zuvor heruntergeladen haben.
2. Klicken Sie auf "OK".
    * Beachten Sie die Warnmeldungen zu Positionen, die nicht akzeptiert werden. Position 4 enthält den Einnahmewert, der im nicht annehmbaren Format dargestellt wird, wohingegen Position 7 nicht den Buchungshinweistext in doppelten Anführungszeichen enthält.
    * Überprüfen Sie die Ausgabe im XML-Format, das die Daten darstellt, die aus der ausgewählten Datei importiert wurden und in das Datenmodell übertragen wurden. Beachten Sie, dass alle 7 Positionen der importierten CSV-Datei verarbeitet wurden. Die Position 1 der Titel der enthaltenen Felder wurden übersprungen, 4 Transaktionen wurden richtig analysiert und 2 Transaktionen wurden als ungültig erkannt.
3. Schließen Sie die Seite.
4. Schließen Sie die Seite.
