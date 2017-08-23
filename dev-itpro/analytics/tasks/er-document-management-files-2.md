--- 
title: "Erweitern des Datenmodells zur Verwendung von Dokumentverwaltungsdateien in Formatausgaben für elektronische Berichterstellung (ER)"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 92177f4653325f6a43c704097d8d5d54d0e15ba9
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a>Erweitern des Datenmodells zur Verwendung von Dokumentverwaltungsdateien in Formatausgaben für elektronische Berichterstellung (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann. Diese Schritte können in jedem Unternehmen ausgeführt werden.

Um diese Schritte ausgeführt, müssen Sie erst die Schritte im Aufgabenleitfaden "ER - Verwendung der Dokumentverwaltungsdateien in Formatausgaben (Teil 1: Vorbereiten des Datenmodells)" ausführen.

Diese Prozedur ist eine Funktion, die in Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.


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

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-enterprise-edition-data-sources"></a>Ordnet Modellelementen die neuen Daten in Dynamics 365 for Finance and Operations , Enterprise edition zu
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

