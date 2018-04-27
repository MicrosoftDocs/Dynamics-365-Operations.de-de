--- 
title: "Format zum Verwenden von Dokumentverwaltungsdateien in Formatausgaben verändern und ausführen"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b38f69fc169367aa56468b2c8f06b65fd1291c79
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="modify-and-run-format-to-use-document-management-files-in-format-outputs"></a>Format zum Verwenden von Dokumentverwaltungsdateien in Formatausgaben verändern und ausführen

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann. Diese Schritte können im DEMF-Unternehmen ausgeführt werden.

Um diese Schritte ausgeführt, müssen Sie erst die Schritte im Aufgabenleitfaden "ER - Verwendung der Dokumentverwaltungsdateien in Formatausgaben (Teil 4: Format ausführen)" ausführen.

Diese Prozedur ist eine Funktion, die in Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a>Bearbeiten Sie das Format, um Anlagen mit Nachrichten im Binärformat zu füllen.
1. Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.
2. Erweitern Sie in der Strukturdarstellung "Debitorenrechnungsmodell ".
3. Erweitern Sie in der Strukturdarstellung "Debitorenrechnungsmodell\Debitorenrechnungsmodell (Benutzerdefiniert)" aus.
4. Wählen Sie in der Strukturdarstellung 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.
5. Klicken Sie auf Designer.
    * Die Rechnungsnachricht in der generierten Ausgabe wird als XML-Datei per Unicode-Codierung ausgefüllt.Rechnung  
6. Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.
7. Wählen Sie in der Struktur 'Common\File' aus.
8. Geben Sie im Feld Name "Xml-Nachricht" ein.
    * Xml-Nachricht  
9. Geben Sie im Feld Kodierung "UTF-8" ein.
    * UTF-8  
10. Klicken Sie auf "OK".
    * Konfigurieren Sie das Generieren der Ausgabe als Zip-Datei.  
11. Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.
12. Wählen Sie in der Struktur 'Common\Folder' aus.
13. Geben Sie im Feld "Name" "Zip-Ausgabe" ein.
    * ZIP-Ausgabe  
14. Klicken Sie auf "OK".
15. Wählen Sie in der Struktur 'Zip-Ausgabe' aus.
    * Fügen Sie Anhänge zur generierenden Zip-Datei als Dateien mit ursprünglichen Namen und Erweiterungen hinzu.  
16. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
17. Wählen Sie in der Struktur 'Common\File' aus.
18. Geben Sie im Feld "Name" "Angehängte Datei" ein.
    * Angehängte Datei  
19. Klicken Sie auf "OK".
20. Wählen Sie in der Struktur 'Zip-Ausgabe\Angehängte Datei'.
21. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
22. Wählen Sie in der Struktur 'Text\Base64' aus.
23. Klicken Sie auf "OK".

## <a name="map-new-format-elements-to-data-model"></a>Zuweisen von neuen Formatkomponenten zum Datenmodell
1. Klicken Sie auf die Registerkarte Zuordnung.
2. Erweitern Sie in der -Struktur den Knoten 'Modell'.
3. Erweitern Sie in der Strukturdarstellung "Modell\Rechnungsanhänge".
4. Wählen Sie in der Struktur 'Zip-Ausgabe\Angehängte Datei\Base64'.
5. Wählen Sie in der Strukturdarstellung "Modell\Rechnungsanhänge\Dateiinhalt" aus.
6. Klicken Sie auf Binden.
7. Wählen Sie in der Struktur 'Zip-Ausgabe\Angehängte Datei'.
8. Klicken Sie auf "Dateiname bearbeiten".
9. Erweitern Sie in der -Struktur den Knoten 'Modell'.
10. Erweitern Sie in der Strukturdarstellung "Modell\Rechnungsanhänge".
11. Wählen Sie in der Strukturdarstellung "Modell\Rechnungsanhänge\Dateiname" aus.
12. Klicken Sie auf Datenquelle hinzufügen.
13. Klicken Sie auf Speichern.
14. Schließen Sie die Seite.
15. Wählen Sie in der Strukturdarstellung "Modell\Rechnungsanhänge " aus.
16. Klicken Sie auf Binden.
17. Klicken Sie auf "Speichern".
18. Schließen Sie die Seite.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Ausführen des Berichts für die ausgewählte Rechnung
1. Klicken Sie auf "Ausführen".
2. Erweitern Sie den Abschnitt "Records to include ()".
3. Klicken Sie auf "Filter".
4. Wählen Sie die Zeile des Feldes "Debitorenrechnungserfassung" und "Auftrag".
5. Geben Sie im Feld "Auftrag" die Auftragsnummer 000148 ein.
    * 000148  
6. Klicken Sie auf "OK".
7. Klicken Sie auf "OK".
    * Prüfen Sie das generierte Ergebnis. Beachten Sie, das neben der Rechnungsnachricht im XML-Format eine einzelne Datei für jede Anlage erstellt wurde. Die Anhangdateien werden mit der gezippten Ausgabe im Binärformat ausgefüllt.  


