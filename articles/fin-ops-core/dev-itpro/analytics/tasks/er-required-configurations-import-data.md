---
title: ER Erforderliche Konfigurationen zum Import von Daten aus einer externen Datei estellen
description: In diesem Artikel wird beschrieben, wie Sie Konfigurationen zur elektronischen Berichterstellung (EB) entwerfen, um Daten in die Microsoft Dynamics 365 Finance-App aus einer externen Datei zu importieren.
author: kfend
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: DefaultDashboard, ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERSolutionCreateDropDialog, EROperationDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula, Tax1099Summary, VendSettlementTax1099
ms.openlocfilehash: 199873af83ec14d441aa3927dc84509486e4927a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290153"
---
# <a name="er-create-required-configurations-to-import-data-from-an-external-file"></a>ER Erforderliche Konfigurationen zum Import von Daten aus einer externen Datei estellen

[!include [banner](../../includes/banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer in der Rolle „Systemadministrator“ oder „Entwickler für elektronische Berichterstellung“ Konfigurationen für elektronische Berichterstellung (EB) entwerfen kann, um Daten in die Anwendung aus einer externen Datei zu importieren. In diesem Beispiel erstellen Sie erforderliche ER-Konfigurationen für das Beispielunternehmen, Litware, Inc., um diesen Aufgabenleitfaden abzuschließen, müssen Sie die Schritte im Aufgabenleitfaden „ER bieten einen Konfigurationsanbieter erstellen und als aktiv markieren“ erst abschließen. Die Schritte können abgeschlossen werden, indem Sie den USMF-Datensatz verwenden. Sie müssen auch die folgenden Dateien herunterladen und lokal speichern: 

| Inhaltsbeschreibung                       | Dateiname                                     |
|-------------------------------------------|-----------------------------------------------|
| ER-Datenmodell-Konfiguration – 1099 | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml)                  |
| ER-Formatkonfiguration – 1099    | [1099format.xml](https://download.microsoft.com/download/e/8/7/e87154b0-b53f-431f-8e1e-0b7f7c9805a9/1099format.xml)                  |
| Beispiel eines eingehenden Dokuments im XML-Format                          | [1099entries.xml](https://download.microsoft.com/download/4/0/3/403a4958-df24-476a-b8b0-6843a9fa7f89/1099entries.xml)        |
| Beispiel der Arbeitsmappe zur Verwaltung von Daten aus eingehenden Dokumenten                          | [1099entries.xlsx](https://download.microsoft.com/download/6/0/0/6001abab-a331-48db-a939-41851fb0f5d0/1099entries.xlsx) |

ER bietet Geschäftskunden die Möglichkeit, den Prozess des Imports externer Datendateien in Tabellen, entweder im .XML- oder .TXT-Format, zu konfigurieren. Zunächst muss eine Kurzfassungsdatenmodell- sowie ein ER-Datenmodellkonfiguration entworfen werden, um die Daten darzustellen, die Sie importieren. Danach müssen Sie die Struktur der Datei, die Sie importieren und die Methode, die Sie verwenden, um die Daten aus der Datei zum Kurzfassungsdatenmodell zu übertragen, definieren. Die ER-Formatkonfiguration, die dem entworfenen Datenmodell zugeordnet ist, muss für das Kurzfassungsatenmodell erstellt werden. Anschließend muss die Datenmodellkonfiguration mit einer Zuordnung erweitert werden, die beschreibt, wie die importierten Daten permanent als Kurzfassungsdatenmodell sind und wie sie verwendet werden, um Tabellen zu aktualisieren.  Der ER-Datenmodellkonfiguration muss eine neue Modellzuordnung angefügt werden, die die Bindung des Datenmodells an die Ziele der Anwendung beschreibt.  

Das folgende Szenario zeigt die ER-Datenimportfunktionen. Hierzu zählen Kreditorenbuchungen, die extern nachverfolgt werden und dann importiert werden, um später im Kreditorenausgleich für Steuerformulare 1099 vermeldet zu werden.   

## <a name="add-a-new-er-model-configuration"></a>Neue ER-Modellkonfiguration hinzufügen
1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.

    Überprüfen Sie den Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.“ ist verfügbar und markiert als aktiv. Sollten Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte der Prozedur „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.   

2. Klicken Sie auf "Berichterstellungskonfigurationen".

    Statt ein neuen Modells zu erstellen, um den Datenimport zu unterstützen, laden Sie die Datei 1099model.xml, die Sie zuvor heruntergeladen haben. Diese Datei enthält ein benutzerdefiniertes Datenmodell der Kreditorenbuchungen. Dieses Datenmodell ist den Datenenkomponenten zugeordnet, die in der AOT-Datenentität sind.   

3. Klicken Sie auf „Austauschen”.
4. Klicken Sie auf „Aus XML-Datei laden”.

    Klicken Sie auf „Durchsuchen” und navigieren Sie zur Datei 1099model.xml, die Sie bereits zuvor heruntergeladen haben.  

5. Klicken Sie auf "OK".
6. Wählen Sie in der Struktur „US 1099-Steuerzahlungsmodell” aus.

## <a name="review-data-model-settings"></a>Datenmodelleinstellungen überprüfen
1. Klicken Sie auf Designer.

    Dieses Modell ist dazu entworfen, die Kreditorenbuchungen seitens des Unternehmens darzustellen und sind getrennt von der Implementierung.   

2. Erweitern Sie in der Struktur „1099-MISC”.
3. Wählen Sie in der Struktur „1099-MISC\Buchungen” aus.
4. Erweitern Sie in der Struktur „1099-MISC\Buchungen”.

    Das Buchungselement dieses Modells stellt einzelne Buchungen dar. Die untergeordneten Elemente werden verwendet, um erforderliche Details wie Kreditorenkonto und Buchungsdatum für jede Buchung anzuzeigen.   

5. Schließen Sie die Seite.

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Neue ER-Formatkonfiguration hinzufügen, die Datenimport unterstützt
Die Schritte in dieser Unteraufgabe zeigen Ihnen, wie eine neue Formatkonfiguration erstellt werden kann, um den Datenimport aus externen Dateien zu verwalten.   
1. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
2. Geben Sie im Feld „Neu” folgende Bezeichnung ein: „Format basierend auf Datenmodell US 1099-Steuerzahlungsmodell”.
3. Wählen Sie die Option „Ja” im Feld „Unterstützt Datenimport” aus.
4. Drücken Sie die ESC-TASTE, um diese Seite zu schließen.

    Statt ein neues Format zu erstellen, um den Datenimport zu unterstützen, laden Sie die Datei 1099format.xml, die Sie zuvor heruntergeladen haben. Diese Datei enthält die definierte Struktur der Datei, die Sie importieren und die Zuordnung der Struktur zum benutzerdefinierten Datenmodell von Kreditorenbuchungen.   
5. Klicken Sie auf „Austauschen”.
6. Klicken Sie auf „Aus XML-Datei laden”.
    Klicken Sie auf „Durchsuchen” und navigieren Sie zur Datei 1099format.xml, die Sie bereits zuvor heruntergeladen haben.  
7. Klicken Sie auf "OK".
8. Erweitern Sie „US 1099-Steuerzahlungsmodell” in der Struktur.
9. Wählen Sie in der Struktur „US 1099-Steuerzahlungsmodell\Format für den Import von Kreditorentransaktionen” aus.

## <a name="review-format-settings"></a>Formateinstellungen überprüfen
1. Klicken Sie auf Designer.
2. Schalten Sie „Details anzeigen” ein.
3. Klicken Sie „Erweitern/reduzieren”.
4. Klicken Sie „Erweitern/reduzieren”.

    Das entworfene Format stellt die erwartete Struktur der externen Datei dar. Diese Datei muss im XML-Format sein und das Ausgleichsstammelement haben. Jede Kreditorenbuchung wird vom Buchungselement dargestellt, das mit einer Null-zu-Viele-Multiplizität definiert ist. Dies bedeutet, dass die eingehende Datei möglicherweise irgendeine Anzahl zwischen null und mehreren Buchungen enthält. Geschachtelte Elemente des Elements „Buchung“ stellen die Attribute einer einzelnen Buchung dar. Beachten Sie, dass alle Attribute, außer Land, als erforderlich markiert werden. Das bedeutet, dass es erforderlich ist, dass sie in der importierenden Datei vorhanden sind.   

## <a name="review-the-settings-of-the-format-mapping-to-the-data-model"></a>Die Einstellungen der Formatzuordnung zum Datenmodell überprüfen
1. Klicken Sie auf „Format zu Modell zuordnen”.

    Die Zuordnung „Zum Importieren von Kreditorenbuchungen“ enthält die Datenübertragungsregeln von der eingehenden XML-Datei an den ausgewählten Teil des benutzerdefinierten Datenmodells, das definiert wird, indem die 1099-MISC-Definition ausgewählt wird.  

2. Klicken Sie auf Designer.
3. Schalten Sie „Details anzeigen” ein.
4. Erweitern Sie „format: Record” in der Struktur.
5. Wählen Sie in der Struktur „format: Record” aus.

    Beachten Sie, dass das entworfene Format hier als eine Datenquellenkomponente dargestellt wird.  

6. Erweitern Sie in der Struktur `format: Record\*settlement: XML Element 1..1 (settlement): Record`.
7. Erweitern Sie in der Struktur `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list`.
8. Erweitern Sie in der Struktur `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record`.
9. Erweitern Sie in der Struktur `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\country: XML Element 0..1 (country): Record`.
10. Wählen Sie in der Struktur `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record` aus.

    Beachten Sie, dass die Präsentation von erforderlichen und optionalen Formatelementen in der vordefinierten Datenquellenkomponente „Format“ anders ist.  
11. Erweitern Sie in der Struktur „Transactions: Record list= format.settlement.'$enumerated”.

    Beachten Sie, dass die Elemente des Formats, das die Struktur der importierten Datei definiert an die Elemente des benutzerdefinierten Datenmodells gebunden sind. Basierend auf diesen Bindungen wird der Inhalt der importierten XML-Datei zur Laufzeit in das vorhandene Datenmodell gespeichert. Beachten Sie die Bindung des Länderelements. Bei jedem Buchungselement in der eingehenden Datei, die kein solches Element hat, wird der Standardländercode „USA“ im Datenmodell aufgefüllt.  

12. Klicken Sie auf die Registerkarte „Überprüfungen”.

    Diese Formatzuordnung enthält ggf. benutzerdefinierte Logik, um die Genauigkeit der importierten Daten aus einem Geschäftsstandpunkt zu überprüfen. Basierend auf der Einstellung wird für jede Buchung in der importierenden Datei ohne einen definieten Ländercode eine Warnmeldung im Infolog generiert. Diese informiert den Benutzer über die Anfrage und gibt die Sequenznummer der Buchung an.  

13. Schließen Sie die Seite.

## <a name="run-the-format-mapping-to-the-data-model"></a>Die Formatzuordnung zum Datenmodell ausführen
Führen Sie diese Formatzuordnung für Testzwecke aus. Verwenden Sie die Datei 1099entries.xml, die Sie zuvor heruntergeladen haben. Sie können diese Datei aus der Arbeitsmappe 1099entries.xlsx exportieren, die verwendet wird, um Kreditorenbuchungen zu verwalten. Die generierte Ausgabe wird aus der ausgewählten XML-Datei importiert und füllt das benutzerdefinierte Datenmodell beim tatsächlichen Import auf.  

1. Klicken Sie auf "Ausführen".

    Klicken Sie auf „Durchsuchen” und navigieren Sie zur Datei 1099entries.xml, die Sie bereits zuvor heruntergeladen haben.  

2. Klicken Sie auf "OK".

    Beachten Sie die Warnmeldung zu einem fehlenden Ländercode für eine Buchung in der importierten Datei.  
    
    Überprüfen Sie die Ausgabe im XML-Format, das die Daten darstellt, die aus der ausgewählten Datei importiert wurden und in das Datenmodell übertragen wurden.   

3. Schließen Sie die Seite.
4. Schließen Sie die Seite.

## <a name="review-the-settings-for-the-model-mapping-to-the-destinations"></a>Die Einstellungen für die Modellzuordnung zu den Zielen überprüfen
1. Wählen Sie in der Struktur „US 1099-Steuerzahlungsmodell” aus.
2. Klicken Sie auf Designer.
3. Klicken Sie auf "Modell der Datenquelle zuordnen".

    Die Zuordnung „Für den Import von manuellen 1099-Buchungen” wurde mit dem Richtungstyp „Zum Ziel” definiert. Das bedeutet, dass sie eingegeben wurde, um den Datenimport zu unterstützen und enthält die Festlegung von Regeln, die definieren, wie die importierte externe Datei und die permanent als Kurzfassungsdatenmodell bestimmten Daten verwendet werden, um Tabellen in der Anwendung zu aktualisieren.  

4. Klicken Sie auf Designer.
5. In der Struktur erweitern Sie „model: Data model 1099 Payments model”.
6. In der Struktur erweitern Sie „Modell: Datenmodell US 1099-Steuerzahlungsmodell\Buchungen: Datensatzliste”.

    Beachten Sie, dass das entworfene Modell hier als ein Datenquellenelement dargestellt wird. Zur Laufzeit enthält es die Daten, die aus der externen Datei importiert werden. Mehrere Tabellen wurden als Datenquellenelemente hinzugefügt, um sicherzustellen, dass die importierten Daten mit den Daten der aktuellen Anwendung kompatibel sind. Dazu gehört auch, ob das importierende Buchungskreditorenkonto im System verfügbar ist, ob die Kombination von importierendem Land und Statuscodes vorhanden ist, usw.  

7. Wählen Sie in der Struktur „Modell: Datenmodell US 1099-Steuerzahlungsmodell\Buchungen: Datensatzliste\\$failed: Berechnetes Feld = IF(OR(ISEMPTY(model.Transactions.'$refs”.vendor), ISEMPTY(model.Transactions.'$refs”.vendor1099), ISEMPTY(model.Transactions.'$refs”.box1099), ISEMPTY(model.Transactions.'$refs”.country), ISEMPTY(model.Transactions.'$refs”.state), ISEMPTY(model.Transactions.'$refs”.location)), true, false): Boolean” aus.
8. Klicken Sie auf "Bearbeiten".
9. Klicken Sie auf Formel bearbeiten.

    Wenn mindestens eine Überprüfung für eine einzelne importierte Buchung fehlschlägt, wird diese Buchung durch das Datenquellenattribut „$failed“ als fehlgeschlagen markiert.  

10. Schließen Sie die Seite.
11. Klicken Sie auf "Abbrechen".
12. Wählen Sie in der Struktur „tax1099trans: Table „VendSettlementTax1099” records= model.Validated” aus.
13. Klicken Sie auf „Ziel bearbeiten”.

    Dieses ER-Ziel wurde hinzugefügt, um anzugeben, wie die importierten Daren die Anwedungstabellen aktualisieren. In diesem Fall wurde die Tabelle VendSettlementTax1099 ausgewählt. Da die Datensatzaktivität INSERT ausgewählt wurde, werden die importierten Buchungen in der Tabelle VendSettlementTax1099 eingefügt. Beachten Sie, dass eine einzelne Modellzuordnung möglicherweise mehrere Ziele beinhaltet. Das bedeutet, dass die importierten Daten verwendet werden können, um Tabellen mehrerer Anwendungen auf einmal zu aktualisieren. Tabellen, Ansichten und Datenentitäten können als ER-Ziele verwendet werden.   

    Wenn die Zuordnung von einem Punkt in der Anwendung aufgerufen wird (wie beispielsweise eine Schaltfläche oder ein Menüelement), das speziell für diese Aktivität entworfen wurde, sollte das ER-Ziel als der Integrationspunkt markiert werden. In diesem Beispiel ist dies der Punkt ERTableDestination#VendSettlementTax1099.  

14. Klicken Sie auf "Abbrechen".
15. Klicken Sie auf „Alle anzeigen”.
16. Klicken Sie auf „Nur Zugeordnete anzeigen”.
17. Erweitern Sie in der Struktur „tax1099trans: Table „VendSettlementTax1099” records= model.Validated”.

    Beachten Sie, dass das Datenquellelement, das die einzigen überprüften Buchungen enthält, an das erstellte Ziel gebunden ist. Sie können die importierten Buchungen filtern, um diejenigen zu überspringen, die mit den Daten der Anwendungen nicht kompatibel sind.  

18. Wählen Sie in der Struktur „failed: Table „VendSettlementTax1099Entity” records= model.Failed” aus.
19. Klicken Sie auf die Registerkarte „Überprüfungen”.

    Diese Modellzuordnung enthält ggf. benutzerdefinierte Logik, um die Richtigkeit der importierten Daten aus den vorhandenen Anwendungsdaten zu überprüfen. Basierend auf der vorhandenen Einstellung wird für jede Buchung in der importierten Datei mit einem Kreditorenkonto, das nicht im System ist, eine Warnmeldung generiert, die den Benutzer informiert und den falschen Kreditorenkontocode angibt.  

    Beachten Sie, dass die Option „Überprüfungsaktivität buchen” für jede Überprüfung verwendet werden kann, um anzugeben, ob der Importprozess fortgefahren oder beendet werden muss sowie ob die bereits ausgeführten Einfügungen/Updates beibehalten oder zurückgesetzt werden können.  

20. Klicken Sie auf „Nur Zugeordnete anzeigen”.
21. Klicken Sie auf „Alle anzeigen”.
22. Schließen Sie die Seite.

    Führen Sie diese Modellzuordnung aus, um das entworfene Format und Modellzuordnungen zu testen. Verwenden Sie die Datei 1099entries.xml. Die Daten aus der ausgewählten Datei werden in das System importiert.  

23. Klicken Sie auf "Ausführen".

    Beachten Sie, dass das Dialogfeld keine zusätzlichen Fragen zur Formatzuordnung enthält, die verwendet werden muss, um die importierten Datei zu analysieren und die Daten dann an das Datenmodell zu übertragen. Das liegt daran, dass es aktuell nur ein Format gibt, das dieses Modell verwendet, das als entworfen zur Unterstützung von Datenimport markiert ist.  
    
    Definieren Sie die Beleg-ID, um die importierten Buchungen von anderen Buchungen zu unterscheiden, die möglicherweise bereits manuell eingegeben wurden oder importiert wurden.  

24. Geben Sie im Feld „Beleg-ID eingeben” die Zeichenfolge „IMPORT-001” ein.

    Durchsuchen Sie, um die Datei „1099entries.xml” abzurufen.  

25. Klicken Sie auf "OK".

    Die Liste mit generierten Warnungen stellt Informationen zu falschen Kreditorenkonten, einem falschen Steuerformular-Feldcode (US 1099), fehlende Ländercodes, usw. bereit. Vergleichen Sie diese Liste von Warnungen mit dem Inhalt, der in die XML-Datei der Ausführung eingeschlossen ist.  

26. Schließen Sie die Seite.
27. Schließen Sie die Seite.
28. Schließen Sie die Seite.
29. Schließen Sie die Seite.
30. Wechseln Sie zu „Kreditorenkonten” > „Periodische Aufgaben” > „Steuererklärung (US 1099)” „Kreditorenausgleich für Steuererformulare (US 1099s)”.

    Dieses Formular zeigt die kumulativen Buchungen in der Tabelle Tax1099Summary an, die auf Grundlage importierter Buchungen erstellt wurden.  

31. Legen Sie das Datum "2000-01-01" im Feld "Von Datum" fest.
32. Klicken Sie auf „Manuelle US 1099-Buchungen”.

    Dieses Formular enthält die Liste von Buchungen, die manuell hinzugefügt wurden und diejenigen, die wir soeben importiert haben.  

33. Öffnen Sie den Belegspaltenfilter .
34. Verwenden Sie den Filteroperator „begins with”, um den Filterwert „IMPORT-001” im Feld „Beleg” einzugeben.

## <a name="review-the-relationship-between-model-and-format-mappings"></a>Die Beziehung zwischen Modell- und Formatzuordnungen überprüfen
1. Schließen Sie die Seite.
2. Schließen Sie die Seite.
3. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
4. Klicken Sie auf "Berichterstellungskonfigurationen".
5. Wählen Sie in der Struktur „US 1099-Steuerzahlungsmodell” aus.

    Angenommen, Sie möchten den Import derselben Daten unterstützen, aber nicht von einem .TXT-Dateiformat.   

6. Klicken Sie auf „Konfiguration erstellen”, um das Dialogfeld zu öffnen. 
7. Geben Sie im Feld „Neu” folgende Bezeichnung ein: „Format basierend auf Datenmodell US 1099-Steuerzahlungsmodell”.
8. Geben Sie im Feld „Name” die Anweisung „Daten aus TXT-Datei importieren” ein.
9. Wählen Sie die Option „Ja” im Feld „Unterstützt Datenimport” aus.
10. Klicken Sie auf Konfiguration erstellen.
11. Klicken Sie auf Designer.
12. Klicken Sie auf „Format zu Modell zuordnen”.
13. Klicken Sie auf "Neu".
14. Geben Sie im Feld "Definition" einen Wert ein, oder wählen Sie einen Wert aus.

    Wählen Sie die Option „1099-MISC” aus.  

15. Geben Sie im Feld „Name” die Anweisung „Daten aus TXT-Datei importieren” ein.
16. Geben Sie im Feld „Beschreibung” die Anweisung „Daten aus TXT-Datei importieren” ein.
17. Klicken Sie auf "Speichern".
18. Schließen Sie die Seite.
19. Schließen Sie die Seite.
20. Klicken Sie auf Bearbeiten.

    Wenn Sie den Hotfix „KB 4012871 Unterstützung von GER-Modellzuordnungen in getrennten Konfigurationen mit der Fähigkeit, verschiedene Arten von Voraussetzungen zur Bereitstellung in verschiedenen Versionen von Dynamics 365 Finance“ ([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871)) installiert haben, führen Sie den nächsten Schritt „Kennung 'Standard für Modellzuordnung' einschalten“ für die eingegebene Formatkonfiguration aus. Überspringen Sie anderenfalls den nächsten Schritt.  

21. Wählen Sie die Option „Ja” im Feld „Standard für Modellzuordnung” aus.
22. Wählen Sie in der Struktur „US 1099-Steuerzahlungsmodell” aus.
23. Klicken Sie auf Designer.
24. Klicken Sie auf "Modell der Datenquelle zuordnen".
25. Klicken Sie auf "Ausführen".

    Wenn Sie den Hotfix „KB 4012871 Unterstützung von GER-Modellzuordnungen in getrennten Konfigurationen mit der Fähigkeit, verschiedene Arten von Voraussetzungen zur Bereitstellung in verschiedenen Versionen festzulegen“ ([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871)) installiert haben, wählen Sie die bevorzugte Modellzuordnung im Suchfeld aus. Wenn Sie den Hotfix noch nicht installiert haben, überspringen Sie diesen Schritt und gehen Sie zum nächsten Schritt, da durch die Definition der Standardformatkonfiguration die Zuordnung bereits ausgewählt wurde.  
    
    Wenn Sie den Hotfix, KB 4012871, nicht installiert haben, beachten Sie, dass das Dialogfeld eine zusätzliche Modellzuordnungsfrage enthält, die verwendet wird, um die importierte Datei zu analysieren. Die Daten werden dann aus dem Dialogfeld zum Datenmodell übertragen. Aktuell können Sie auswählen, welche Formatzuordnung verwendet werden muss, abhängig vom Dateityp, den Sie importieren möchten.  
    
    Wenn Sie planen, diese Modellzuordnung von einem Punkt in der Anwendung aus aufzurufen, der speziell für diese Aktivität entworfen wurde, müssen das ER-Ziel und die Formatzuordnung als Teil der Integration markiert sein.  

26. Klicken Sie auf "Abbrechen".
27. Schließen Sie die Seite.
28. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
