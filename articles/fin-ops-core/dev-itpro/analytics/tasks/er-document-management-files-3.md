---
title: Formate zur Verwendung von Dokumentverwaltungsdateien in EB-Ausgabe erstellen
description: In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien in ER-Berichten nutzen kann.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05c0c4a38f34774e7018504c5e3fab834a2ec1b1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182530"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3-create-format"></a>ER Verwenden von Dokumentverwaltungsdateien in Formatausgaben (Teil 3: Format erstellen)

[!include [task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann. Diese Schritte können in jedem Unternehmen ausgeführt werden.

Um diese Schritte ausgeführt, müssen Sie erst die Schritte im Aufgabenleitfaden "ER - Verwendung der Dokumentverwaltungsdateien in Formatausgaben (Teil 2: Erweitern des Datenmodells)" ausführen.

Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.


## <a name="create-a-format-to-process-invoices"></a>Erstellen eines Formats zur Rechnungsverarbeitung
1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
2. Klicken Sie auf "Berichterstellungskonfigurationen".
3. Erweitern Sie in der Strukturdarstellung "Debitorenrechnungsmodell ".
4. Wählen Sie in der Strukturdarstellung "Debitorenrechnungsmodell\Debitorenrechnungsmodell (Benutzerdefiniert)" aus.
    * Sie erstellen ein Format, um elektronische Nachrichten mit Informationen zu allen Dateien zu generieren, die einem Auftrag zugeordnet wurden, der einer elektronischen Rechnung zugeordnet ist.  
5. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
6. Geben Sie im Feld "Neu" "Format basierend auf Debitorenrechnungsmodell (benutzerdefiniert)" ein.
7. Geben Sie im Feld Name "Beispielnachricht für elektronische Rechnung" ein.
    * Beispielnachricht für elektronische Rechnung  
8. Geben Sie im Feld "Datenmodelldefinition" einen Wert ein, oder wählen Sie einen Wert aus.
    * InvoiceCustomer  
9. Klicken Sie auf Konfiguration erstellen.

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a>Entwerfen Sie ein Format, um Anlagen in einem MIME-Format zu generieren.
1. Klicken Sie auf Designer.
2. Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.
3. Wählen Sie in der Struktur den Knoten 'XML\Element'.
4. Geben Sie im Feld "Name" "Rechnung" ein.
    * Rechnung  
5. Klicken Sie auf "OK".
6. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
7. Wählen Sie in der Struktur 'XML\Attribute' aus.
8. Geben Sie im Feld "Name" "SalesOrder" ein.
    * SalesOrder  
9. Klicken Sie auf "OK".
10. Klicken Sie auf "Attribut hinzufügen".
11. Geben Sie im Feld "Name" "InvoiceNumber" ein.
    * InvoiceNumber  
12. Klicken Sie auf "OK".
13. Klicken Sie auf "Attribut hinzufügen".
14. Geben Sie im Feld "Name" "InvoiceAmount" ein.
    * InvoiceAmount  
15. Klicken Sie auf "OK".
16. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
17. Wählen Sie in der Struktur den Knoten 'XML\Element'.
18. Geben Sie im Feld "Name" "EnclosedDocs" ein.
    * EnclosedDocs  
19. Klicken Sie auf "OK".
20. Wählen Sie in der Strukturdarstellung "Rechnung\EnclosedDocs" aus.
21. Klicken Sie auf "Element hinzufügen".
22. Geben Sie im Feld "Name" 'Dokument' ein.
    * Dokument  
23. Klicken Sie auf "OK".
24. Wählen Sie in der Strukturdarstellung "Rechnung\EnclosedDocs\Dokument" aus.
25. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
26. Wählen Sie in der Struktur 'XML\Attribute' aus.
27. Geben Sie im Feld "Name" "FileName" ein.
    * Dateiname  
28. Klicken Sie auf "OK".
29. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
30. Wählen Sie in der Struktur den Knoten 'XML\Element'.
31. Geben Sie im Feld "Name" den Wert "FileContent" ein.
    * FileContent  
32. Klicken Sie auf "OK".
33. Wählen Sie in der Strukturdarstellung "Rechnung\EnclosedDocs\Dokument\FileContent" aus.
34. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
35. Wählen Sie in der Struktur 'Text\Base64' aus.
36. Klicken Sie auf "OK".

## <a name="map-format-elements-to-data-model-as-data-source"></a>Zuordnen von Formatelementen zum Datenmodell als Datenquelle
1. Wählen Sie in der Strukturdarstellung "Rechnung\SalesOrder" aus.
2. Klicken Sie auf die Registerkarte Zuordnung.
3. Erweitern Sie in der -Struktur den Knoten 'Modell'.
4. Wählen Sie in der Strukturdarstellung "Modell\Auftragsnummer(SalesId)") aus.
5. Klicken Sie auf Binden.
6. Wählen Sie in der Strukturdarstellung "Rechnung\InvoiceNumber" aus.
7. Erweitern Sie in der Strukturdarstellung "Modell\Basisrechnung(InvoiceBase)".
8. Wählen Sie in der Struktur 'Modell\Basisrechnung(InvoiceBase)\Rechnungsnummer(Id)' aus.
9. Klicken Sie auf Binden.
10. Wählen Sie in der Strukturdarstellung "Rechnung\InvoiceAmount" aus.
11. Wählen Sie in der Struktur 'Modell\Basisrechnung(InvoiceBase)\Rechnungsbetrag(Amount)' aus.
12. Klicken Sie auf Binden.
13. Erweitern Sie in der Strukturdarstellung "Modell\Rechnungsanhänge".
14. Wählen Sie in der Strukturdarstellung "Modell\Rechnungsanhänge\Dateiinhalt" aus.
15. Wählen Sie in der Strukturdarstellung "Rechnung\EnclosedDocs\Dokument\FileContent\Base64" aus.
16. Klicken Sie auf Binden.
17. Wählen Sie in der Strukturdarstellung "Modell\Rechnungsanhänge\Dateiname" aus.
18. Wählen Sie in der Strukturdarstellung "Rechnung\EnclosedDocs\Dokument\FileName" aus.
19. Klicken Sie auf Binden.
20. Wählen Sie in der Strukturdarstellung "Modell\Rechnungsanhänge " aus.
21. Wählen Sie in der Strukturdarstellung "Rechnung\EnclosedDocs\Dokument" aus.
22. Klicken Sie auf Binden.
23. Klicken Sie auf "Speichern".
24. Schließen Sie die Seite.

