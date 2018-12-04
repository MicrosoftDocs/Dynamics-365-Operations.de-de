--- 
title: "Formate durch erneute Anwendung von Excel-Vorlagen ändern"
description: "Um diese Schritte abzuschließen, müssen Sie zuerst die Schritte im Aufgabenleitfaden „Eine ER-Konfiguration zum Generieren von Berichten im OPENXML-Format erstellen” abschließen."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 3d5752caba9327475bb28c7bc6b0ee7e072f44f3
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---
# <a name="modify-formats-by-reapplying-excel-templates"></a>Formate durch erneute Anwendung von Excel-Vorlagen ändern

[!include [task guide banner](../../includes/task-guide-banner.md)]

Um diese Schritte abzuschließen, müssen Sie zuerst die Schritte im Aufgabenleitfaden „Eine ER-Konfiguration zum Generieren von Berichten im OPENXML-Format erstellen” abschließen.

Dieses Verfahren zeigt, wie eine elektronische Berichtsformatkonfiguration geändert wird, indem eine Microsoft Excel-Vorlage erneut angewendet wird, die geändert wurde. In diesem Verfahren importieren Sie eine geänderte Excel-Vorlage in eine ER-Formatkonfigurationen, die für das Beispielunternehmen, Litware, Inc. erstellt wurde, und erstellen dann die elektronischen Dokumente. Diese Prozedur ist für Benutzer bestimmt, die die Rolle des Systemadministrators oder des elektronischen Berichtsentwicklers haben, die ihnen zugewiesen sind. Die Schritte können abgeschlossen werden, indem Sie den GBSI-Datensatz verwenden. Bevor Sie beginnen, laden und speichern Sie die Datei, SampleVendPaymWsReport2.xlsx, die im Hilfethema aufgeführt ist, ändern elektronisches Berichterstellungsformat, indem Sie eine Tabelle erneut öffnen (modify-electronic-reporting-format-reapply-excel-template/).

1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
    * Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als aktiv markiert ist. Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in der Prozedur „Konfigurationsanbieter erstellen und als aktiv markieren” abschließen.  

## <a name="select-the-er-format"></a>Wählen Sie ER-Format aus.
1. Klicken Sie auf "Berichterstellungskonfigurationen".
2. Erweitern oder reduzieren Sie 'Zahlungsmodell' in der Struktur.
3. Wählen Sie in der Struktur die Option "Zahlungsmodell \Beispiel-Arbeitsblattbericht" aus.
4. Klicken Sie auf Anhänge.
    * Beachten Sie, dass die SampleVendPaymWsReport.xlsx-Excel-Datei derzeit als Vorlage für die Zahlungserfassungsverarbeitung verwendet wird.   
5. Klicken Sie auf "Öffnen".
    * Klicken Sie auf Öffnen, um das Layout der Tabelle zu durchsuchen.  
    * Überprüfen der Vorlage. Beachten Sie, dass derzeit die folgenden Details für jede Zahlungsposition eingeschlossen sind: Kreditorenkontonummer, Kreditor, Bank, Bankleitzahl, Kontonummer, Soll, Haben und Währung. In vorliegenden Beispiel möchten wir dieser Liste erweitern, indem wir Details zum Zahlungsdatum hinzufügen.   
6. Schließen Sie die Seite.

## <a name="reapply-a-new-excel-template-to-er-format"></a>Wenden Sie eine neue Excelvorlage im ER-Format erneut an
1. Klicken Sie auf Designer.
    * Öffnet die Entwurfsversion des ausgewählten ER-Formats zur Bearbeitung.  
2. Klicken Sie im Aktivitätsbereich auf "Importieren".
3. Auf "Aus Excel aktualisieren" klicken.
    * Klicken Sie auf "Vorlage aktualisieren" und wählen Sie die Datei, SampleVendPaymWsReport2.xlsx aus.  
    * Klicken Sie auf Vorlage aktualisieren und suchen Sie die zuvor heruntergeladene Datei SampleVendPaymWsReport2.xlsx.  
4. Klicken Sie auf "OK".
    * Die SampleVendPaymWsReport2.xlsx-Vorlage wird angewendet. Die Struktur des ER-Formats wird mit dem Inhalt der Vorlage synchronisiert, deren Elemente in ER-Format hinzugefügt werden. Alle vorhandenen Elemente im ER-Format, die nicht in der Vorlage enthalten sind, werden von der Formatdefinition entfernt.  
5. Wählen Sie in der Struktur "Excel" aus.
    * Beachten Sie, dass das Vorlagenfeld nun eine Referenz in der neuen Vorlage beinhaltet.   
6. Klicken Sie auf Anhänge.
7. Klicken Sie auf "Öffnen".
    * Klicken Sie auf Öffnen, um das Layout der Excel-Vorlage zu bearbeiten.  
    * Überprüfen der Vorlage. Beachten Sie, dass es jetzt eine Position für das Zahlungsdatum enthält.   
8. Schließen Sie die Seite.
9. In der Struktur erweitern Sie "Excel".
10. Erweitern Sie „Excel\PaymLines” in der Struktur.
11. Wählen Sie in der Struktur Excel\Zahlungszeilen\Zahlungsdatum
    * Beachten Sie, dass das ER-Format nun einen anderen Artikel enthält. Eine Zelle, PaymDate, wurde der Tabelle hinzugefügt.  
12. Klicken Sie auf die Registerkarte Zuordnung.
13. Erweitern Sie in der -Struktur den Knoten 'Modell'.
14. Erweitern Sie 'Modell\Zahlungen' in der Struktur.
15. Wählen Sie in der Strukturdarstellung "Modell\Payments\Transaction date(TransactionDate)" aus.
16. Klicken Sie auf Binden.
    * Geben Sie an, welche Daten zur neuen Zelle zur Laufzeit hinzugefügt werden.  
17. Klicken Sie auf "Speichern".
18. Schließen Sie die Seite.

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a>Aktivieren Sie die geänderte Entwurfsversion des ER-Formats für die Verwendung bei Zahlungserfassungsverarbeitunge
1. Klicken Sie im Aktivitätsbereich auf Konfigurationen.
2. Klicken Sie auf Benutzerparameter.
3. Wählen Sie "Ja" im Feld "Testlaufeinstellungen".
4. Klicken Sie auf "OK".
5. Klicken Sie auf "Bearbeiten".
6. Wählen Sie "Ja" im Feld "Testentwurf".

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a>Nutzen Sie die geänderte Entwurfsversion des ER-Formats für die Verwendung bei Zahlungserfassungsverarbeitungen
    * Wiederholen Sie das erstellte Arbeitsblatt, einschließlich neue Details der Zahlungszeilen - Zahlungsdatum.  


