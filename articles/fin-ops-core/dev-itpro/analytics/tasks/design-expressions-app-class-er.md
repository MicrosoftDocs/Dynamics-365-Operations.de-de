---
title: EB-Ausdrücke entwerfen, um Anwendungsklassenmethoden aufzurufen
description: Dieses Thema enthält Informationen darüber, wie die vorhandene Anwendungslogik in Konfigurationen der elektronischen Berichterstellung (EB) erneut verwendet wird, indem erforderliche Methoden von Anwendungsklassen aufgerufen werden.
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
ms.openlocfilehash: a2de6464aaceadd60a82a70f428f42cd4f864eb8
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092084"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>EB-Ausdrücke entwerfen, um Anwendungsklassenmethoden aufzurufen

[!include [banner](../../includes/banner.md)]

Dieser Leitfaden enthält Informationen darüber, wie die vorhandene Anwendungslogik in Konfigurationen der elektronischen Berichterstellung (EB) erneut verwendet wird, indem erforderliche Methoden von Anwendungsklassen in EB-Ausdrücken aufgerufen werden. Werte von Argumenten zum Aufrufen von Klassen können dynamisch zur Laufzeit definiert werden: beispielsweise basierend auf Informationen im Analysedokument, um dessen Richtigkeit sicherzustellen. In diesem Handbuch erstellen Sie die erforderlichen ER-Konfigurationen für das Beispielunternehmen, Litware, Inc. Dieses Verfahren wird für Benutzer mit der zugewiesenen Rolle des Systemadministrators oder elektronischer Berichterstellungsentwicklers erstellt. 

Die Schritte können abgeschlossen werden, indem Sie einen beliebigen Dataset verwenden. Sie müssen auch folgende Datei herunterladen und lokal speichern: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.

Um diese Schritte auszuführen, müssen Sie zunächst die Schritte in der Prozedur „EB Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.

1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
    * Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als aktiv markiert ist. Sollten Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte der Prozedur „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.   
    * Sie entwerfen einen Prozess für die Analyse von eingehenden Bankauszügen für eine Anwendungsdatenaktualisierung. Sie erhalten die eingehenden Bankauszüge als TXT-Dateien, die IBAN-Codes enthalten. Als Teil des Bankauszug-Importprozesses müssen Sie die Korrektheit dieser IBAN-Codes mithilfe der Logik überprüfen, die bereits verfügbar ist.   

## <a name="import-a-new-er-model-configuration"></a>Neue EB-Modellkonfiguration importieren
1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie die Microsoft-Anbieterkachel aus.  
2. Klicken Sie auf Repositorys.
3. Klicken Sie auf "Filter anzeigen".
4. Fügen Sie ein Filterfeld Typname ein. Geben Sie im Feld „Name“ den Wert „Ressourcen“ ein, wählen Sie dann den Filteroperator „enthält“ aus, und klicken Sie dann auf „Übernehmen“.
5. Klicken Sie auf "Öffnen".
6. Wählen Sie in der Struktur die Option "Zahlungsmodell" aus.
    * Wenn die Schaltfläche „Importieren“ im Inforegister „Versionen“ nicht aktiviert ist, haben Sie die Version 1 der EB-Konfiguration „Zahlungsmodell“ bereits importiert. Sie können die übrigen Schritte in dieser Unteraufgabe überspringen.   
7. Klicken Sie auf Import.
8. Klicken Sie auf "Ja".
9. Schließen Sie die Seite.
10. Schließen Sie die Seite.

## <a name="add-a-new-er-format-configuration"></a>Neues ER-Modellformat hinzufügen
1. Klicken Sie auf "Berichterstellungskonfigurationen".
    * Fügen Sie ein neues EB-Format hinzu, um eingehende Bankauszüge im TXT-Format zu analysieren.  
2. Wählen Sie in der Struktur die Option "Zahlungsmodell" aus.
3. Klicken Sie auf „Konfiguration erstellen”, um das Dropdown-Menü zu öffnen.
4. Wählen Sie im neuen Feld geben Sie "Format auf Grundlage Datenmodell PaymentModel" ein.
5. Geben Sie im Feld „Name” die Bezeichnung „Bankauszug-Importformat (Beispiel)” ein.
    * Bankauszug-Importformat (Beispiel)  
6. Wählen Sie die Option „Ja” im Feld „Unterstützt Datenimport” aus.
7. Klicken Sie auf Konfiguration erstellen.

## <a name="design-the-er-format-configuration---format"></a>Die Formatkonfiguration für die elektronische Berichterstellung (EB) entwerfen – Format
1. Klicken Sie auf Designer.
    * Das entworfene Format stellt die erwartete Struktur der externen Datei im TXT-Format dar.  
2. Klicken Sie auf „Stamm hinzufügen”, um das Dialogmenü zu öffnen.
3. Wählen Sie in der Struktur 'Text\Sequence'..
4. Geben Sie im Feld Name "Root" ein.
    * Stamm  
5. Wählen Sie im Feld "Sonderzeichen" "Neue Zeile - Windows (CR LF)".
    * Die Option „Neue Postion – Windows (CR LF)“ wurde im Feld „Sonderzeichen“ ausgewählt. Basierend auf dieser Einstellung wird jede Position in der Analysedatei als ein separater Datensatz behandelt.  
6. Klicken Sie auf "OK".
7. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
8. Wählen Sie in der Struktur 'Text\Sequence'..
9. Geben Sie im Feld „Name” die Bezeichnung „Zeilen” ein.
    * Zeilen  
10. Wählen Sie im Vielfältigkeitsgebiet wählen Sie "viele" aus.
    * Die Option „viele“ wurde im Feld „Multiplizität“ ausgewählt. Basierend auf dieser Einstellung wird erwartet, dass mindestens eine Position in der Analysedatei dargestellt wird.  
11. Klicken Sie auf "OK".
12. Wählen Sie in der Struktur „Stamm\Zeilen” aus.
13. Klicken Sie auf „Nummernkreis hinzufügen”.
14. Geben Sie im Feld „Name” die Bezeichnung „Felder” ein.
    * Felder  
15. Wählen Sie im Vielfältigkeitsgebiet wählen Sie "Genau eines" aus.
16. Klicken Sie auf "OK".
17. Wählen Sie in der Struktur „Stamm\Zeilen\Felder”.
18. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
19. Wählen Sie in der Struktur 'Text\String' aus.
20. Geben Sie im Feld "Name" "IBAN" ein.
    * IBAN  
21. Klicken Sie auf "OK".
    * Es wurde so konfiguriert, dass jede Position in der Analysedatei den einzigen IBAN-Code enthält.  
22. Klicken Sie auf "Speichern".

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a>Die EB-Formatkonfiguration entwerfen – Zuordnung zu Datenmodell
1. Klicken Sie auf „Format zu Modell zuordnen”.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld „Definition” die Bezeichnung „BankToCustomerDebitCreditNotificationInitiation” ein.
    * BankToCustomerDebitCreditNotificationInitiation  
4. ResolveChanges die Definition.
5. Geben Sie im Feld „Name” die Bezeichnung „Zuordnung zu Datenmodell” ein.
    * Zu Datenmodell zuordnen  
6. Klicken Sie auf "Speichern".
7. Klicken Sie auf Designer.
8. Wählen Sie in der Struktur "Dynamics 365 for Operations\Klasse" aus.
9. Klicken Sie auf "Stamm hinzufügen".
    * Fügen Sie eine neue Datenquelle hinzu, um die vorhandene Anwendungslogik für die IBAN-Codeprüfung aufzurufen.  
10. Geben Sie im Feld „Name” die Bezeichnung „Codes überprüfen” ein.
    * Code prüfen  
11. Geben Sie im Feld „Klasse” den Wert „ISO7064” ein.
    * ISO7064  
12. Klicken Sie auf "OK".
13. Erweitern Sie in der Struktur Format.
14. Erweitern Sie in der Struktur „Format\Stamm: Nummernkreis(Stamm)”.
15. Wählen Sie in der Struktur „Format\Stamm: Nummernkreis(Stamm)\Zeilen: Nummernkreis 1..* (Zeilen)” aus.
16. Klicken Sie auf Binden.
17. Erweitern Sie in der Struktur „Format\Stamm: Nummernkreis(Stamm)\Zeilen: Nummernkreis 1..* (Zeilen)”.
18. Erweitern Sie in der Struktur „Format\Stamm: Nummernkreis(Stamm)\Zeilen: Nummernkreis 1..* (Zeilen)Felder: Nummernkreis 1..1 (Felder)”.
19. Wählen Sie in der Struktur „Format\Stamm: Nummernkreis(Stamm)\Zeilen: Nummernkreis 1..* (Zeilen)Felder: Nummernkreis 1..1 (Felder)\IBAN: Zeichenfolge(IBAN)” aus.
20. Erweitern Sie in der Struktur „Zahlungen = format.Root.Rows”.
21. In der Struktur erweitern Sie „Zahlungen = format.Root.Rows\Kreditorenkonto (CreditorAccount)”.
22. In der Struktur erweitern Sie „Zahlungen = format.Root.Rows\Kreditorenkonto (CreditorAccount)\Identifizierung”.
23. In der Struktur wählen Sie „Zahlungen = format.Root.Rows\Kreditorenkonto (CreditorAccount)\Identifizierung\IBAN” aus.
24. Klicken Sie auf Binden.
25. Klicken Sie auf die Registerkarte „Überprüfungen”.
26. Klicken Sie auf "Neu".
    * Fügen Sie eine neue Überprüfungsregel hinzu, die in der Analysedatei für jede Position einen Fehler anzeigt, die ungültigen IBAN-Code enthält.  
27. Klicken Sie auf "Bedingung bearbeiten".
28. Erweitern Sie in der Struktur „check_codes”.
29. Wählen Sie in der Struktur „check_codes\verifyMOD1271_36” aus.
30. Klicken Sie auf Datenquelle hinzufügen.
31. Im Feld „Formel” geben Sie „check_codes.verifyMOD1271_36(” ein.
    * check_codes.verifyMOD1271_36(  
32. Erweitern Sie in der Struktur Format.
33. Erweitern Sie in der Struktur „Format\Stamm: Nummernkreis(Stamm)”.
34. Erweitern Sie in der Struktur „Format\Stamm: Nummernkreis(Stamm)\Zeilen: Nummernkreis 1..* (Zeilen)”.
35. Erweitern Sie in der Struktur „Format\Stamm: Nummernkreis(Stamm)\Zeilen: Nummernkreis 1..* (Zeilen)Felder: Nummernkreis 1..1 (Felder)”.
36. Wählen Sie in der Struktur „Format\Stamm: Nummernkreis(Stamm)\Zeilen: Nummernkreis 1..* (Zeilen)Felder: Nummernkreis 1..1 (Felder)\IBAN: Zeichenfolge(IBAN)” aus.
37. Klicken Sie auf Datenquelle hinzufügen.
38. Im Feld „Formel” geben Sie „check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)” ein.
    * check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)  
39. Klicken Sie auf "Speichern".
40. Schließen Sie die Seite.
    * Die Überprüfungsbedingung wurde so konfiguriert, dass sie FALSE für jeden ungültigen IBAN-Code zurückgibt, indem die vorhandene Methode „verifyMOD1271_36“ von der Anwendungsklasse „ISO7064“ aufgerufen wird. Beachten Sie, dass der Wert des IBAN-Codes dynamisch zur Laufzeit als Argument der aufrufenden Methode basierend auf dem Inhalt der analysierenden TXT-Datei definiert wird.   
41. Klicken Sie auf „Nachricht bearbeiten”.
42. Geben Sie im Feld „Formel” die Zeichenfolge „CONCATENATE("ungültiger IBAN-Code wurde gefunden: ", format.Root.Rows.Fields.IBAN)” ein.
    * CONCATENATE("Ungültiger IBAN-Code wurde gefunden: ", format.Root.Rows.Fields.IBAN)  
43. Klicken Sie auf "Speichern".
44. Schließen Sie die Seite.
45. Klicken Sie auf "Speichern".
46. Schließen Sie die Seite.

## <a name="run-the-format-mapping"></a>Die Formatzuordnung ausführen
Zu Textwecken führen Sie die Formatzuordnung mithilfe der Datei SampleIncomingMessage.txt aus, die Sie zuvor heruntergeladen haben. Die generierte Ausgabe umfasst Daten, die aus der ausgewählten TXT-Datei importiert werden und im benutzerdefinierte Datenmodell während des tatsächlichen Imports aufgefüllt werden.   
1. Klicken Sie auf "Ausführen".
    * Klicken Sie auf „Durchsuchen”, und navigieren Sie zur Datei SampleIncomingMessage.txt, die Sie bereits zuvor heruntergeladen haben.  
2. Klicken Sie auf "OK".
    * Überprüfen Sie die Ausgabe im XML-Format, das die Daten darstellt, die aus der ausgewählten Datei importiert wurden und in das Datenmodell übertragen wurden. Beachten Sie, dass nur 3 Positionen der importierten TXT-Datei verarbeitet wurden. Der IBAN-Code in Position 4, der ungültig ist, wurde übersprungen, und eine Fehlermeldung wird im Infolog bereitgestellt.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]