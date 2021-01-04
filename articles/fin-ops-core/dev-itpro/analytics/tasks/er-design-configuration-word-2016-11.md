---
title: EB-Konfigurationen entwerfen, um Berichte im Word-Format zu generieren
description: In den folgenden Schritten wird erläutert, wie ein Benutzer entweder in der Rolle „Systemadministrator” oder „Entwickler für elektronische Berichterstellung” Formate für die elektronische Berichterstellung zum Generieren von Berichten als Microsoft Word-Dateien konfigurieren kann.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9d4959b511022e1aa98544d23da6afcda1f6adf2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681924"
---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a>EB-Konfigurationen entwerfen, um Berichte im Word-Format zu generieren

[!include [banner](../../includes/banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer entweder in der Rolle „Systemadministrator” oder „Entwickler für elektronische Berichterstellung” Formate für die elektronische Berichterstellung (EB) zum Generieren von Berichten als Microsoft Word-Dateien konfigurieren kann. Diese Schritte können im GBSI-Unternehmen ausgeführt werden.

Um diese Schritte abzuschließen, müssen Sie die Schritte im Aufgabenleitfaden „Eine ER-Konfiguration zum Generieren von Berichten im OPENXML-Format erstellen“ abschließen. Im Voraus müssen Sie auch die folgenden Vorlagen für den Beispielbericht herunterladen und lokal speichern:

- [Vorlage des Zahlungsberichts](https://go.microsoft.com/fwlink/?linkid=862266)
- [Begrenzte Vorlage eines Zahlungsberichtes](https://go.microsoft.com/fwlink/?linkid=862266)


Diese Prozedur ist eine Funktion, für die in Microsoft Dynamics 365 for Operations Version 1611 hinzugefügt wurde.


## <a name="select-the-existing-er-report-configuration"></a>Wählen Sie die vorhandene ER-Berichtskonfiguration aus
1. Gehen Sie im **Navigationsbereich zu Module > Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung**. Stellen Sie sicher, dass der Konfigurationsanbieter „Litware, Inc.“ ist als aktiv ausgewählt ist.  
2. Klicken Sie auf **Berichterstellungskonfigurationen**. Wir verwenden die vorhandene ER-Koniguration erneut, die ursprünglich entworfen wurde, um die Berichtsausgabe im OPENXML-Format zu generieren.  
3. Erweitern oder reduzieren Sie 'Zahlungsmodell' in der Struktur.
4. Wählen Sie in der Struktur die Option "Zahlungsmodell \Beispiel-Arbeitsblattbericht" aus.
5. Klicken Sie auf Designer.

## <a name="replace-the-excel-template-with-the-word-template"></a>Ersetzen der Excel-Vorlage durch eine Word-Vorlage

Aktuell wird das Excel-Dokument als Vorlage verwendet, um die Ausgabe im OPENXML-Format zu generieren. Wir importieren die Vorlage des Berichts im Word-Format.

1. Klicken Sie auf **Anhänge**. Ersetzen Sie die vorhandene Excel-Vorlage durch die Word-Vorlage, die Sie zuvor heruntergeladen haben, SampleVendPaymDocReport.docx. Hinweis, diese Vorlage beinhaltet nur das Layout des Dokuments, das wir als ER-Ausgabe generieren möchten.  
2. Klicken Sie auf **Löschen**.
3. Klicken Sie auf **Ja**.
4. Klicken Sie auf **Neu**.
5. Klicken Sie auf **Datei**.
6. Klicken Sie auf **Durchsuchen**. Navigieren Sie zu SampleVendPaymDocReport.docx und wählen Sie es aus, das Sie bereits heruntergeladen haben. Klicken Sie auf **OK**. Wählen Sie die Vorlage aus, die Sie im vorherigen Schritt heruntergeladen haben.  
7. Geben Sie im Feld **Vorlage** einen Wert ein, oder wählen Sie einen Wert aus.

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a>Erweitern der Word-Vorlage durch Hinzufügen eines benutzerdefinierten XML-Teils
1. Klicken Sie auf **Speichern**. Zusätzlich zum Speichern von Konfigurationsänderungen, wird durch die Aktivität „Speichern” auch die angehängte Word-Vorlage aktualisiert. Die Struktur des entworfenen Formats wird dem zugeordneten Word-Dokument als neuer benutzerdefinierter XML-Abschnitt mit dem Namen „Bericht“ übertragen. Beachten Sie, dass die angefügte Word-Vorlage nicht nur das Layout des Dokuments enthält, das wir als ER-Ausgabe generieren möchten. Es enthält auch die Struktur von Daten, die ER in diese Vorlage zur Laufzeit auffüllen wird.  
2. Klicken Sie auf **Anhänge**.
    + Nun müssen Sie die Elemente des benutzerdefinierten XML-Abschnitts „Bericht“ an die Word Dokumentteile binden.  
    + Wenn Sie mit Word-Dokumenten vertraut sind, die als Formulare entworfen werden können, die Inhaltssteuerelemente enthalten, die durch Elemente von benutzerdefinieten XML-Teilen begrenzt sind – geben Sie alle Schritte der nächsten Unteraufgabe wieder, um so ein Dokument zu erstellen. Weitere Informationen finden Sie unter [Erstellen von Formularen, die in Word ausgefüllt oder gedruckt werden können](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US). Andernfalls überspringen Sie die Schritte in der nächsten Unteraufgabe.  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a>Rufen Sie Word mit benutzerdefiniertem XML-Teil ab, um Datenbindungen vorzunehmen

Öffnen Sie das Dokument in Word und gehen Sie folgendermaßen vor:  
1. Öffnen Sie die Word-Entwicklerregisterkarte (Menüband anpassen, sofern dieses noch nicht aktiviert ist).
2. Wählen Sie den XML-Zuordnungsbereich aus.
3. Wählen Sie den benutzerdefinierten XML-Teil „Bericht“ in der Suche.
4. Führen Sie die Zuordnung von Elementen des ausgewählten benutzerdefinierten XML-Teils und der Inhaltssteuerelemente des Word-Dokuments aus.  5. Speichern Sie das aktualisierte Word-Dokument in einem lokalen Laufwerk.  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a>Hochladen der Word-Vorlage mit benutzerdefiniertem XML-Teil, der an Inhaltssteuerelemente gebunden ist
1. Klicken Sie auf **Löschen**.
2. Klicken Sie auf **Ja**. Fügen Sie eine neue Vorlage hinzu. Wenn Sie die Schritte in der vorherigen Unteraufgabe abgeschlossen haben, wählen Sie das Word-Dokument aus, das Sie vorbereitet und lokal gespeichert haben. Andernfalls wählen Sie die MS Word-Vorlage „SampleVendPaymDocReportBounded.docx” aus, die Sie vorher heruntergeladen haben.  
3. Klicken Sie auf **Neu**.
4. Klicken Sie auf **Datei**.
5. Klicken Sie auf **Durchsuchen**. Navigieren Sie zu SampleVendPaymDocReportBounded.docx und wählen Sie es aus, das Sie bereits heruntergeladen haben. Klicken Sie auf **OK**.
6. Wählen Sie im Feld **Vorlage** das Dokument aus, das Sie im vorherigen Schritt heruntergeladen haben.
7. Klicken Sie auf **Speichern**.
8. Schließen Sie die Seite.

## <a name="execute-the-format-to-create-word-output"></a>Das Format zum Erstellen der Word-Ausgabe ausführen
1. Klicken Sie im **Aktivitätsbereich** auf **Konfigurationen**.
2. Klicken Sie auf **Benutzerparameter**.
3. Wählen Sie „Ja“ im Feld **Testlaufeinstellungen** aus.
4. Klicken Sie auf **OK**.
5. Klicken Sie auf **Bearbeiten**.
6. Wählen Sie „Ja“ im Feld **Testentwurf** aus.
7. Klicken Sie auf **Speichern**.
8. Schließen Sie die Seite.
9. Schließen Sie die Seite.
10. Wechseln Sie im **Navigationsbereich** zu **Module > Kreditoren > Zahlungen > Zahlungserfassung**.
11. Klicken Sie auf **Positionen**.
12. Markieren Sie alle Zeilen in der Liste, oder heben Sie die Markierung auf.
13. Klicken Sie auf **Zahlungsstatus**
14. Klicken Sie auf **Keine**.
15. Klicken Sie auf **Zahlungen generieren**.
16. Klicken Sie auf **OK**.
17. Klicken Sie auf **OK**. Analysieren Sie das generierte Ergebnis. Beachten Sie, dass die erstellte Ausgabe im Word-Format dargestellt wird und die Details der verarbeiteten Zahlungen enthält.  

