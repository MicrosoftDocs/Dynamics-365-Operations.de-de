---
title: 'ER Verwenden von Dokumentverwaltungsdateien in Formatausgaben (Teil 4: Format ausführen)'
description: In diesem Thema wird beschrieben, wie Sie ein elektronisches Berichtsformat für die Verwendung von Dokumentenverwaltungsdateien in der EB-Ausgabe konfigurieren. (Teil 4)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ede71118f64eec27b150a4c575aead97d3174509
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559724"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a>ER Verwenden von Dokumentverwaltungsdateien in Formatausgaben (Teil 4: Format ausführen)

[!include [banner](../../includes/banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann. Diese Schritte können im DEMF-Unternehmen ausgeführt werden.

Um diese Schritte auszuführen, müssen Sie erst die Schritte im Aufgabenleitfaden „ER Verwendung der Dokumentverwaltungsdateien in Formatausgaben (Teil 3: Format erstellen)“ ausführen.

Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a>Erforderliche Anhänge für den Auftrag einer einzelnen Rechnung hinzufügen
1. Wechseln Sie zu "Debitoren" > "Rechnungen" > "Offene Debitorenrechnungen".
2. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld "Rechnung" mit dem Wert "CIV-000148".
    * CIV-000148  
3. Klicken Sie darauf, um dem ausgewählten Link von der Rechnung zu folgen.
    * CIV-000148  
4. Klicken Sie, um dem Link im Feld "Auftrag" zu folgen.
    * 000148  
5. Wählen Sie im Feld "Positionen oder Kopfzeile" "Kopfzeile" aus.
    * Wählen Sie den Kopf aus, um anzugeben, dass dies das Ziel für das Hinzufügen von Anlagen ist.  
6. Klicken Sie auf Anhänge.
    * Fügen Sie einige Dateien als Anhänge für diesen Auftrag hinzu. Verwenden Sie die Dateien der Dokumenttypen, die von der Dokumentverwaltung unterstützt werden (mit DOCX-, DPF- XML-, JPG-Dateierweiterungen, usw.). Wählen Sie Dateien aus, die angehängt und mit der entsprechenden Rechnung in der elektronischen ER-Nachricht weiterverarbeitet werden sollen.  
7. Klicken Sie auf "Neu".
8. Klicken Sie auf "Datei".
9. Klicken Sie auf "Neu".
10. Klicken Sie auf "Datei".
11. Schließen Sie die Seite.
12. Schließen Sie die Seite.
13. Schließen Sie die Seite.
14. Schließen Sie die Seite.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Ausführen des Berichts für die ausgewählte Rechnung
1. Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.
2. Erweitern Sie in der Strukturdarstellung "Debitorenrechnungsmodell ".
3. Erweitern Sie in der Strukturdarstellung "Debitorenrechnungsmodell\Debitorenrechnungsmodell (Benutzerdefiniert)" aus.
4. Wählen Sie in der Strukturdarstellung 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.
5. Klicken Sie auf "Ausführen".
6. Erweitern Sie den Abschnitt "Records to include ()".
7. Klicken Sie auf "Filter".
8. Wählen Sie die Zeile des Feldes "Debitorenrechnungserfassung" und "Auftrag".
9. Geben Sie im Feld "Kriterien" den Wert "000148" ein.
    * Geben Sie im Feld Auftrag die Auftragsnummer 000148 ein.  
10. Klicken Sie auf "OK".
11. Klicken Sie auf "OK".
    * Prüfen Sie das generierte Ergebnis. Beachten Sie, das für jede Anlage ein einzelner XML-Knoten erstellt wurde. Der Inhalt des Anhangs wird dann mit der XML-Ausgabe im MIME-Textformat (Base64) ausgefüllt.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]