---
title: 'ER – Verwendung von Dokumentverwaltungsdateien in Formatausgaben (Teil 2: Datenmodell erweitern)'
description: In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb4c58dc86a159a70634c05408a8db471ebcae4c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "320948"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2-extend-data-model"></a>ER Verwenden von Dokumentverwaltungsdateien in Formatausgaben (Teil 2: Datenmodell erweitern)

[!include [task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann. Diese Schritte können in jedem Unternehmen ausgeführt werden.

Um diese Schritte ausgeführt, müssen Sie erst die Schritte im Aufgabenleitfaden "ER - Verwendung der Dokumentverwaltungsdateien in Formatausgaben (Teil 1: Vorbereiten des Datenmodells)" ausführen.

Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a>Erweitern des Datenmodells zur Darstellung von Dokumentverwaltungsdateien
1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
2. Klicken Sie auf "Berichterstellungskonfigurationen".
3. Erweitern Sie in der Strukturdarstellung "Debitorenrechnungsmodell ".
4. Wählen Sie in der Strukturdarstellung "Debitorenrechnungsmodell\Debitorenrechnungsmodell (Benutzerdefiniert)" aus.
5. Klicken Sie auf Designer.
6. Wählen Sie in der Strukturdarstellung "Debitorenrechnung(InvoiceCustomer)" aus.
    * Wir erweitern dieses Datenmodell, um es für alle Dateien zur Verfügung zu stellen, die einem Auftrag zugeordnet wurden, der einer elektronischen Rechnung zugeordnet ist.  
7. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
8. Geben Sie im Feld Name "Rechnungsanhänge" ein.
    * Anhänge fakturieren  
9. Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.
10. Klicken Sie auf Hinzufügen.
11. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
12. Geben Sie im Feld "Name" einen Wert "Dateiinhalt" ein.
    * Datei-Inhalt  
13. Wählen Sie im Feld "Artikeltyp" 'Container' aus.
14. Klicken Sie auf Hinzufügen.
15. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
16. Geben Sie im Feld "Name" "Dateiname" ein.
    * Dateiname  
17. Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.
18. Klicken Sie auf Hinzufügen.

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-enterprise-edition-data-sources"></a>Wir ordnen neue Modellelemente zu den entsprechenden Datenquellen in Dynamics 365 for Finance and Operations Enterprise Edition zu.
1. Klicken Sie auf "Modell der Datenquelle zuordnen".
2. Verwenden Sie den Schnellfilter, um im Feld "Definition" nach dem Wert 'InvoiceCustomer' zu filtern.
    * InvoiceCustomer  
    * Wir ordnen neue Modellelemente zu den entsprechenden Datenquellen zu.  
3. Klicken Sie auf Designer.
4. Wählen Sie in der Strukturdarstellung "Anhänge fakturieren" aus.
5. Erweitern Sie in der Strukturdarstellung "Anhänge fakturieren".
6. Wählen Sie in der Strukturdarstellung "Anhänge fakturieren\Dateiname" aus.
7. Klicken Sie auf "Bearbeiten".
8. Geben Sie im Feld Formel 'CustInvoiceJour.>'Relations'.SalesTable.<'Relations'.'<Documents'.'originalFileName()'' ein.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'  
9. Klicken Sie auf "Speichern".
10. Schließen Sie die Seite.
11. Wählen Sie in der Strukturdarstellung "Anhänge fakturieren\Dateiinhalt" aus.
12. Klicken Sie auf "Bearbeiten".
13. Geben Sie im Feld Formel 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'' ein.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'  
14. Klicken Sie auf "Speichern".
15. Schließen Sie die Seite.
16. Wählen Sie in der Strukturdarstellung "Anhänge fakturieren" aus.
17. Klicken Sie auf "Bearbeiten".
18. Geben Sie im Feld Formel 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'' ein.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'  
19. Klicken Sie auf "Speichern".
20. Schließen Sie die Seite.
21. Klicken Sie auf "Speichern".
22. Schließen Sie die Seite.
23. Schließen Sie die Seite.
24. Schließen Sie die Seite.
25. Klicken Sie auf "Status ändern".
26. Klicken Sie auf "Abgeschlossen".
27. Klicken Sie auf "OK".

