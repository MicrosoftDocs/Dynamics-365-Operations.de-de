---
title: Berichte im Office-Format generieren, die eingebettete Bilder haben
description: In diesem Thema wird beschrieben, wie die Konfigurationen für die elektronische Berichterstellung (EB) entworfen werden, um elektronische Dokumente in Excel und Word zu generieren, die eingebettete Bilder enthalten.
author: NickSelin
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81b93c14fc4819fffd322a1b364feac3d25a0d24
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751557"
---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a>Berichte im Office-Format generieren, die eingebettete Bilder haben

[!include [banner](../../includes/banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Rolle „Systemadministratorrolle“ oder „Entwickler für elektronische Berichterstellung“ angehört, eine neue Konfiguration für elektronische Berichterstellung (ER) erstellen kann, die eine Vorlage zur Generierung elektronischer Dokumente im OPENXML-Format enthält.

In diesem Beispiel erstellen Sie eine ER-Konfigurationen für das Beispielunternehmen „Litware, Inc.“.  Um diese Schritte auszuführen, müssen Sie die Schritte zuerst im „ER Berichte im MS Office-Formaten mit eingebetteten Bildern (Teil 2: Konfiguration überprüfen)“ Aufgabenleitfaden erstellen. Diese Schritte können im „USMF“-Unternehmen ausgeführt werden.


## <a name="run-format-with-initial-model-mapping"></a>Führen Sie das Format mit Initialenmodellzuordnung aus
1. Gehen Sie zu "Bargeld- und Bankverwaltung" > Bankkonten > Bankkonten.
2. Verwenden Sie den Schnellfilter, um im Feld "Bankkonto" nach dem Wert "USMF OPER" zu filtern.
3. Klicken Sie im Aktivitätsbereich auf "Einrichten".
4. Klicken Sie auf "Prüfen".
5. Drucktest anklicken.
    * Führen Sie das Format für Testzwecke aus.  
6. Wählen Sie die Option Ja im Feld Verhandelbares Scheckformatgebiet aus.
7. Klicken Sie auf "OK".
    * Prüfen Sie das generierte Ergebnis. Das Unternehmenslogo wird ebenso im Bericht angezeigt wie die Signatur der autorisierten Person. Das Bild der Signatur stammt aus dem Feld vom Datentyp „Container“ des Schecklayoutdatensatzes, der dem ausgewählten Bankkonto zugeordnet ist.  
8. Erweitern Sie den Abschnitt Kopien.
9. Klicken Sie auf "Bearbeiten".
10. Im Wasserzeichengebiet geben Sie "Wasserzeichen als Nichtig drucken".
    * Ändern Sie die Wasserzeichenlayouteinstellung, um den Wasserzeichentext anzuzeigen, wenn Sie in einem Dokument Excel-Formelement generieren.  
11. Drucktest anklicken.
12. Klicken Sie auf "OK".
    * Prüfen Sie das generierte Ergebnis. Das Wasserzeichen wird im erstellten Bericht in Übereinstimmung mit der Auswahloption angezeigt.  
13. Schließen Sie die Seite.
14. Klicken Sie im Aktivitätsbereich auf Zahlungen verwalten.
15. Klicken Sie auf Schecks.
16. Klicken Sie auf "Filter anzeigen".
17. Wenden Sie die nachfolgenden Filter an: Geben Sie einen Filterwert von 381, 385, 389 im Checkfeld mithilfe des Filterzeichens ein.
18. Schalten Sie in der Liste 'Alle Zeilen markieren' ein/aus.
19. Scheckkopie drucken anklicken.
    * Führen Sie das Format aus, um die ausgewählten Schecks erneut zu drucken.  
    * Prüfen Sie das generierte Ergebnis. Die ausgewählten Schecks wurden erneut gedruckt. Das Firmenlogo und die Bezeichnungen werden nicht ausgedruckt, wie sie auf dem Vordruck dargestellt werden.  

## <a name="modify-the-mapping-of-the-imported-data-model"></a>Überprüfe Sie die Struktur des importierten Datenmodells.
1. Schließen Sie die Seite.
2. Schließen Sie die Seite.
3. Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.
4. Wählen Sie in der Struktur 'Modell für Cheques.
5. Klicken Sie auf Designer.
6. Klicken Sie auf "Modell der Datenquelle zuordnen".
7. Klicken Sie auf Designer.
    * Wir ändern die Bindung des Signaturartikels des Datenmodells, um das Signaturbild aus der Datei zu erhalten, die dem Schecklayoutdatensatz zugeordnet wurde, der dem ausgewählten Bankkonto zugeordnet ist.  
8. Deaktivieren Sie „Details anzeigen“.
9. Erweitern Sie in der Struktur Layout.
10. Erweitern oder reduzieren Sie Layout\Unterschrift.
11. Wählen Sie in der Strukturdarstellung Layout\Unterschrift\Bild= chequesaccount<Beziehungen. BankChequeLayout.Signature1Bmp.
12. Erweitern oder reduzieren Sie chequesaccount.
13. In der Struktur erweitern chequesaccount\<Beziehungen.
14. Erweitern Sie in der Struktur chequesaccount\<Beziehungen\BankChequeLayout.
15. Erweitern Sie in der Struktur chequesaccount\<BeziehungenBankChequeLayout\<Relations.
16. Erweitern Sie in der Struktur 'chequesaccount\<BeziehungBankChequeLayout\<Beziehung\<Dokumente'.
17. Wählen Sie in der Strukturdarstellung 'chequesaccount\<BeziehungBankChequeLayout\<Beziehung\<DokumentegetFileContentAsContainer()'.
18. Klicken Sie auf Binden.
19. Klicken Sie auf "Speichern".
20. Schließen Sie die Seite.
21. Schließen Sie die Seite.
22. Schließen Sie die Seite.
23. Schließen Sie die Seite.

## <a name="run-format-using-the-adjusted-model-mapping"></a>Die Formatzuordnung zum Datenmodell ausführen
1. Gehen Sie zu "Bargeld- und Bankverwaltung" > Bankkonten > Bankkonten.
2. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld "Bankkontofeld" mit dem Wert "USMF OPER".
3. Klicken Sie im Aktivitätsbereich auf "Einrichten".
4. Klicken Sie auf "Prüfen".
5. Drucktest anklicken.
6. Klicken Sie auf "OK".
    * Prüfen Sie das generierte Ergebnis. Das Bild aus dem Dokumentverwaltungsanhang stellt die Signatur einer autorisierten Person dar.  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a>Verwenden Sie das MS Word-Dokument als Vorlage im importierten Format
1. Schließen Sie die Seite.
2. Schließen Sie die Seite.
3. Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.
4. Wählen Sie in der Struktur erweitern 'Modell für Cheques.
5. Wählen Sie in der Strukturdarstellung "Modell für Cheques\Cheques-Druckformat.
6. Klicken Sie auf Designer.
7. Klicken Sie auf Anhänge.
8. Klicken Sie auf Löschen.
9. Klicken Sie auf "Ja".
10. Klicken Sie auf "Neu".
11. Klicken Sie auf "Datei".
    * Navigieren und wählen Sie die heruntergeladene Datei „Scheck-Vorlage Word.docx“ aus.  
12. Schließen Sie die Seite.
13. Geben Sie im Feld "Vorlage" einen Wert ein, oder wählen Sie einen Wert aus.
14. Klicken Sie auf "Speichern".
15. Schließen Sie die Seite.
16. Klicken Sie auf "Bearbeiten".
17. Wählen Sie "Ja" im Feld "Testentwurf".
18. Schließen Sie die Seite.
19. Gehen Sie zu "Bargeld- und Bankverwaltung" > Bankkonten > Bankkonten.
20. Verwenden Sie den Schnellfilter, um im Feld "Bankkonto" nach dem Wert "USMF OPER" zu filtern.
21. Klicken Sie auf "Prüfen".
22. Drucktest anklicken.
23. Klicken Sie auf "OK".
    * Prüfen Sie das generierte Ergebnis. Die Ausgabe wurde als ein Word-Dokument mit eingebetteten Bildern generiert, die das Unternehmenslogo, die Signatur einer autorisierten Person und den markierten Text des Wasserzeichens darstellen.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]