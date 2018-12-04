--- 
title: Eine Anforderung erstellen, die eine Angebotsanforderung verwendet
description: "Dieser Leitfaden zeigt, wie man Preis- und Kreditoreninformationen einer Bestellanforderung von einem Angebotsanforderungsprozess aus hinzufügt."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d97ccd15031b2f7398486eee4a716ecef5e9dafd
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-requisition-that-uses-an-rfq"></a>Eine Anforderung erstellen, die eine Angebotsanforderung verwendet

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieser Leitfaden zeigt, wie man Preis- und Kreditoreninformationen einer Bestellanforderung von einem Angebotsanforderungsprozess aus hinzufügt. Das Beispiel, das in diesem Leitfaden gezeigt wird, kann in dem USMF-Demodatenunternehmen verwendet werden, und Sie müssen als Administrator angemeldet sein, um alle Schritte abzuschließen. Die Aufgaben in diesem Leitfaden würden gewöhnlich von Prokuristen durchgeführt werden.


## <a name="create-a-requisition"></a>Eine Anforderungen erstellen
1. Wechseln Sie zu "Beschaffung" >"Bestellanforderungen" > "Von mir vorbereitete Bestellanforderungen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Name" einen Wert ein.
4. Geben Sie im Feld "Angefordertes Datum" ein Datum ein.
5. Geben Sie ein Datum in das Feld "Datum" ein.
6. Klicken Sie auf "OK".
7. Geben Sie im Feld 'Grund' einen Wert ein, oder wählen Sie einen Wert aus.
8. Klicken Sie auf "Position hinzufügen".
9. Wählen Sie im Feld "Beschaffungskategorie" eine Kategorie im Baum aus, und klicken Sie dann auf O.K.
10. Geben Sie im Feld "Produktname" einen Wert ein.
11. Geben Sie im Feld "Menge" eine Zahl ein.
12. Geben Sie im Feld 'Einheit' einen Wert ein, oder wählen Sie einen Wert aus.
13. Klicken Sie auf "Speichern".
14. Klicken Sie zum Öffnen des Dropdown-Dialogfeldformulars auf ''.
15. Klicken Sie auf Absenden.
16. Schließen Sie die Seite.
17. Klicken Sie auf Absenden.

## <a name="reassign-a-workflow-task"></a>Eine Workflowaufgabe neu zuweisen
    * Die folgende Aufgabe besteht darin, eine Angebotsanforderung zu erstellen, um Angebote von Lieferanten für das Produkt zu erhalten. In den USMF-Demodaten wird der Anforderungsworkflow mit einer Regel eingerichtet, damit, wenn ein Kreditor nicht ausgewählt ist oder der Einzelpreis für eine Position 0 ist, eine Aufgabe einer spezifischen Arbeitskraft zugewiesen wird, um eine Angebotsanforderung zu erstellen. Um mit diesem Leitfaden fortzufahren, müssen Sie diese Aufgabe einem anderen Benutzer (Sie selbst) erneut zuweisen. Sie können dies nur tun, wenn Sie als "Administrator" angemeldet sind.  
1. Klicken Sie zum Öffnen des Dropdown-Dialogfeldformulars auf ''.
2. Klicken Sie auf "Verlauf anzeigen".
3. Aktualisieren Sie die Seite.
4. Erweitern Sie den Abschnitt "Verfolgungsdetails".
5. Im Baum wählen Sie 'die Position aus, die mit "Positionsworkflow aktiviert am"' beginnt.
6. Klicken Sie auf "Workflowdetails anzeigen".
7. Erweitern Sie den Abschnitt "Arbeitsaufgaben".
8. Klicken Sie auf "Neu zuweisen".
9. Wählen Sie im Feld "Benutzer" die Option "Administrator" aus.
10. Klicken Sie auf "Neu zuweisen".
11. Schließen Sie die Seite.
12. Schließen Sie die Seite.

## <a name="create-an-rfq"></a>Eine Angebotsanforderung erstellen
1. Aktualisieren Sie die Seite.
2. Klicken Sie auf "Angebotsanforderung".
3. Wählen Sie im Feld "Kaufende juristische Person" die Option "USMF" aus.
    * Sie müssen dieselbe juristische Person auswählen, die auf der Anforderungsposition ist.  
4. Markieren Sie in der Liste die ausgewählte Zeile.
    * Wenn Sie mehrere Positionen auf Ihrer Bestellanforderung hatten, wählen Sie alle die Positionen aus, die Sie zur Angebotsanforderung hinzufügen möchten.  
5. Klicken Sie auf "OK".
6. Aktualisieren Sie die Seite.
7. Öffnen Sie die Infobox und erweitern Sie dann den Abschnitt "Zugehörige Dokumente".
    * Sie haben möglicherweise bereits die Infobox offen. Suchen Sie nach dem Symbol, auf der sich ein Pfeil befindet. Es befindet sich rechts von den Umschaltflächen "Positionen/Header". Wenn der Pfeil nach rechts zeigt, ist die Infobox bereits offen. Wenn der Pfeil nach links zeigt, klicken Sie auf ihn, um die Infobox zu öffnen.  
8. Klicken Sie auf den Link im Feld "Angebotsanforderung", um die Angebotsanforderung zu öffnen, die soeben erstellt wurde.
9. Klicken Sie auf "Kopfzeile".
10. Klicken Sie auf Hinzufügen.
11. Geben Sie im Feld "Kreditorenkonto" einen Wert ein, oder wählen Sie einen Wert aus.
12. Klicken Sie auf Hinzufügen.
13. Geben Sie im Feld "Kreditorenkonto" einen Wert ein, oder wählen Sie einen Wert aus.
14. Klicken Sie auf Senden.
15. Klicken Sie auf "OK".
16. Klicken Sie auf "Antwort eingeben".
17. Klicken Sie im Aktivitätsbereich auf "Antworten".
18. Klicken Sie auf "Daten in Antwort kopieren".
    * Dies kopiert Daten, wie die Menge und die Datumsangaben, von der Angebotsanforderung zur Antwort.  
19. Geben Sie im Feld "Preis je Einheit" eine Zahl ein.
    * Dies ist der Preis, den Sie vom Kreditor empfangen haben. Sie sollten auch zusätzliche Information vom Kreditor eingeben.  
20. Klicken Sie auf "Annehmen".
21. Klicken Sie auf "OK".

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Überprüfen Sie, dass Kreditor und Preis an die Anforderung übertragen worden sind
1. Schließen Sie die Seite.
2. Klicken Sie auf "Positionen".
3. Klicken Sie auf "Zugehörige Informationen".
4. Klicken Sie auf "Bestellanforderung".
5. Wählen Sie die Position aus, die zur Angebotsanforderung übertragen wurde.
    * Überprüfen Sie, dass der Preis und der Kreditor zur Anforderung kopiert worden sind.  
6. Klicken Sie zum Öffnen des Dropdown-Dialogfeldformulars auf ''.
7. Klicken Sie auf "Abgeschlossen".
8. Schließen Sie die Seite.
9. Klicken Sie auf "Abgeschlossen".


