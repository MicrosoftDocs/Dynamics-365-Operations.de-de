--- 
title: "Entwerfen einer Konfiguration zum Generieren von Berichten im Microsoft Word-Format für elektronische Berichterstellung (ER)"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer entweder in der Rolle „Systemadministrator” oder „Entwickler für elektronische Berichterstellung” Elektronische Berichterstellungs-(ER)-Formate zum Generieren von Berichten als Microsoft Word-Dateien konfigurieren kann."
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5adf1d6e6314ac7ea4084cfb3fcde8b83168c7ae
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="design-a-configuration-for-generating-reports-in-microsoft-word-format-for-electronic-reporting-er"></a>Entwerfen einer Konfiguration zum Generieren von Berichten im Microsoft Word-Format für elektronische Berichterstellung (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer entweder in der Rolle „Systemadministrator” oder „Entwickler für elektronische Berichterstellung” Elektronische Berichterstellungs-(ER)-Formate zum Generieren von Berichten als Microsoft Word-Dateien konfigurieren kann. Diese Schritte können im GBSI-Unternehmen ausgeführt werden.

Um diese Schritte abzuschließen, müssen Sie zuerst die Schritte im Aufgabenleitfaden „Eine ER-Konfiguration zum Generieren von Berichten im OPENXML-Format erstellen” abschließen. Im Voraus müssen Sie auch die folgenden Vorlagen für den Beispielbericht herunterladen und lokal speichern:

http://msdynamics.blob.core.windows.net/media/2016/10/SampleVendPaymDocReport.docx

http://msdynamics.blob.core.windows.net/media/2016/10/SampleVendPaymDocReportBounded.docx

Diese Prozedur ist eine Funktion, die in Microsoft Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.


## <a name="select-the-existing-er-report-configuration"></a>Wählen Sie die vorhandene ER-Berichtskonfiguration aus
1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
    * Stellen Sie sicher, dass der Konfigurationsanbieter „Litware, Inc.” als aktiv ausgewählt ist.  
2. Klicken Sie auf "Berichterstellungskonfigurationen".
    * Wir verwenden die vorhandene ER-Koniguration erneut, die ursprünglich entworfen wurde, um die Berichtsausgabe im OPENXML-Format zu generieren.  
3. Erweitern oder reduzieren Sie 'Zahlungsmodell' in der Struktur.
4. Wählen Sie in der Struktur die Option "Zahlungsmodell \Beispiel-Arbeitsblattbericht" aus.
5. Klicken Sie auf Designer.

## <a name="replace-the-excel-template-with-the-word-template"></a>Ersetzen der Excel-Vorlage durch eine Word-Vorlage
    * Aktuell wird das Excel-Dokument als Vorlage verwendet, um die Ausgabe im OPENXML-Format zu generieren. Wir importieren die Vorlage des Berichts im Word-Format.  
1. Klicken Sie auf Anhänge.
    * Ersetzen Sie die vorhandene Excel-Vorlage durch die Word-Vorlage, die Sie zuvor heruntergeladen haben, SampleVendPaymDocReport.docx. Hinweis, diese Vorlage beinhaltet nur das Layout des Dokuments, das wir als ER-Ausgabe generieren möchten.  
2. Klicken Sie auf Löschen.
3. Klicken Sie auf "Ja".
4. Klicken Sie auf "Neu".
5. Klicken Sie auf "Datei".
6. Klicken Sie auf Durchsuchen. Navigieren Sie zu SampleVendPaymDocReport.docx und wählen Sie es aus, das Sie bereits heruntergeladen haben. Klicken Sie auf "OK".
    * Wählen Sie die Vorlage aus, die Sie im vorherigen Schritt heruntergeladen haben.  
7. Geben Sie im Feld "Vorlage" einen Wert ein, oder wählen Sie einen Wert aus.

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a>Erweitern der Word-Vorlage durch Hinzufügen eines benutzerdefinierten XML-Teils
1. Klicken Sie auf "Speichern".
    * Zusätzlich zum Speichern von Konfigurationsänderungen, wird durch die Aktivität „Speichern” auch die angehängte Word-Vorlage aktualisiert. Die Struktur des entworfenen Formats wird zum zugeordneten Word-Dokument als neuer benutzerdefinierter XML-Abschnitt mit dem Namen „Bericht” übertragen. Beachten Sie, dass die angefügte Word-Vorlage nicht nur das Layout des Dokuments enthält, das wir als ER-Ausgabe generieren möchten. Es enthält auch die Struktur von Daten, die ER in diese Vorlage zur Laufzeit auffüllen wird.  
2. Klicken Sie auf Anhänge.
    * Nun müssen Sie die Elemente des benutzerdefinierten XML-Abschnitts „Bericht” an die Word-Dokumentteile binden.  
    * Wenn Sie mit Word-Dokumenten vertraut sind, die als Formulare entworfen werden können, die Inhaltssteuerelemente enthalten, die durch Elemente von benutzerdefinieten XML-Teilen begrenzt sind – geben Sie alle Schritte der nächsten Unteraufgabe wieder, um so ein Dokument zu erstellen. Genauere Informationen finden Sie unter diesem Link (in englischer Sprache): https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US. Andernfalls überspringen Sie die Schritte in der nächsten Unteraufgabe.  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a>Rufen Sie Word mit benutzerdefiniertem XML-Teil ab, um Datenbindungen vorzunehmen
    * Öffnen Sie dieses Dokument in Word und gehen Sie folgendermaßen vor:  - Öffnen Sie die Word-Entwicklerregisterkarte (passen Sie das Menüband an, wenn es noch nicht aktiviert ist).  - Wählen Sie den XML-Zuordnungsbereich aus.  - Wählen Sie den benutzerdefinierten XML-Teil „Bericht” in der Suche aus.  - Führen Sie die Zuordnung von Elementen des ausgewählten benutzerdefinierten XML-Teils und der Inhaltssteuerelemente des Word-Dokuments aus.  - Speichern Sie das aktualisierte Word-Dokument in einem lokalen Laufwerk.  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a>Hochladen der Word-Vorlage mit benutzerdefiniertem XML-Teil, der an Inhaltssteuerelemente gebunden ist
1. Klicken Sie auf Löschen.
2. Klicken Sie auf "Ja".
    * Fügen Sie eine neue Vorlage hinzu. Wenn Sie die Schritte in der vorherigen Unteraufgabe abgeschlossen haben, wählen Sie das Word-Dokument aus, das Sie vorbereitet und lokal gespeichert haben. Andernfalls wählen Sie die MS Word-Vorlage „SampleVendPaymDocReportBounded.docx” aus, die Sie vorher heruntergeladen haben.  
3. Klicken Sie auf "Neu".
4. Klicken Sie auf "Datei".
5. Klicken Sie auf Durchsuchen. Navigieren Sie zu SampleVendPaymDocReportBounded.docx und wählen Sie es aus, das Sie bereits heruntergeladen haben. Klicken Sie auf "OK".
6. Wählen Sie im Feld „Vorlage” das Dokument aus, das Sie im vorherigen Schritt heruntergeladen haben.
7. Klicken Sie auf "Speichern".
8. Schließen Sie die Seite.

## <a name="execute-the-format-to-create-word-output"></a>Das Format zum Erstellen der Word-Ausgabe ausführen
1. Klicken Sie im Aktivitätsbereich auf Konfigurationen.
2. Klicken Sie auf Benutzerparameter.
3. Wählen Sie "Ja" im Feld "Testlaufeinstellungen".
4. Klicken Sie auf "OK".
5. Klicken Sie auf "Bearbeiten".
6. Wählen Sie "Ja" im Feld "Testentwurf".
7. Klicken Sie auf "Speichern".
8. Schließen Sie die Seite.
9. Schließen Sie die Seite.
10. Wechseln Sie zu "Kreditoren" > "Zahlungen" > "Zahlungserfassung".
11. Klicken Sie auf "Positionen".
12. Markieren Sie alle Zeilen in der Liste, oder heben Sie die Markierung auf.
13. Klicken Sie "Zahlungsstatus"
14. Klicken Sie „Keine”.
15. Klicken Sie auf Zahlungen generieren.
16. Klicken Sie auf "OK".
17. Klicken Sie auf "OK".
    * Analysieren Sie das generierte Ergebnis. Beachten Sie, dass die erstellte Ausgabe im Word-Format dargestellt wird und die Details der verarbeiteten Zahlungen enthält.  


