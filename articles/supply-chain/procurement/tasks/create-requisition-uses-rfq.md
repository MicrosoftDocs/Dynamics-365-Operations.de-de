---
title: Eine Anforderung erstellen, die eine Angebotsanforderung verwendet
description: Dieses Thema erklärt, wie man Preis- und Kreditoreninformationen einer Bestellanforderung von einem Angebotsanforderungsprozess aus hinzufügt.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 205cba2325e76dae9572301e44e0e89cbcfd106e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204699"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a>Eine Anforderung erstellen, die eine Angebotsanforderung verwendet

[!include [banner](../../includes/banner.md)]

Dieses Thema erklärt, wie man Preis- und Kreditoreninformationen einer Bestellanforderung von einem Angebotsanforderungsprozess aus hinzufügt. Das Beispiel, das in diesem Leitfaden gezeigt wird, kann in dem USMF-Demodatenunternehmen verwendet werden, und Sie müssen als Administrator angemeldet sein, um alle Schritte abzuschließen. Die Aufgaben in diesem Leitfaden würden gewöhnlich von Prokuristen durchgeführt werden.


## <a name="create-a-requisition"></a>Eine Anforderungen erstellen
1. Wechseln Sie im Navigationsbereich zu **Module > Beschaffung > Bestellanforderungen > Von mir vorbereitete Bestellanforderungen**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Name** einen Wert ein.
4. Geben Sie im Feld **Angefordertes Datum** ein Datum ein.
5. Geben Sie ein Datum in das Feld **Abschlussstichtag** ein.
6. Wählen Sie **OK**.
7. Geben Sie im Feld **Grund** einen Wert ein, oder wählen Sie einen Wert aus.
8. Wählen Sie **Position hinzufügen** aus.
9. Wählen Sie im Feld **Beschaffungskategorie** eine Kategorie im Baum aus, und wählen Sie dann **OK** aus.
10. Geben Sie im Feld **Produktname** einen Wert ein.
11. Geben Sie im Feld **Menge** eine Zahl ein.
12. Geben Sie im Feld **Einheit** einen Wert ein, oder wählen Sie einen Wert aus.
13. Wählen Sie **Speichern**.
14. Klicken Sie zum Öffnen des Dropdown-Dialogfelds auf **Workflow**.
15. Wählen Sie **Senden**.
16. Schließen Sie die Seite.
17. Wählen Sie **Senden**.

## <a name="reassign-a-workflow-task"></a>Eine Workflowaufgabe neu zuweisen
Die folgende Aufgabe besteht darin, eine Angebotsanforderung zu erstellen, um Angebote von Lieferanten für das Produkt zu erhalten. In den USMF-Demodaten wird der Anforderungsworkflow mit einer Regel eingerichtet, damit, wenn ein Kreditor nicht ausgewählt ist oder der Einzelpreis für eine Position 0 ist, eine Aufgabe einer spezifischen Arbeitskraft zugewiesen wird, um eine Angebotsanforderung zu erstellen. Um mit diesem Leitfaden fortzufahren, müssen Sie diese Aufgabe einem anderen Benutzer (Sie selbst) erneut zuweisen. Sie können dies nur tun, wenn Sie als "Administrator" angemeldet sind.  

1. Klicken Sie zum Öffnen des Dropdown-Dialogfelds auf **Workflow**.
2. Wählen Sie **Historie anzeigen** aus.
3. Aktualisieren Sie die Seite.
4. Erweitern Sie den Abschnitt **Verfolgungsdetails**.
5. Im Baum wählen Sie dann die Position aus, die mit „Positionsworkflow aktiviert am“ beginnt.
6. Wählen Sie **Workflowdetails anzeigen** aus.
7. Erweitern Sie den Abschnitt **Arbeitsaufgaben**.
8. Wählen Sie **Neu zuordnen** aus.
9. Wählen Sie im Feld **Benutzer** die Option **Administrator** aus.
10. Wählen Sie **Neu zuordnen** aus.
11. Schließen Sie die beiden Seiten.

## <a name="create-an-rfq"></a>Eine Angebotsanforderung erstellen

1. Aktualisieren Sie die Seite.
2. Wählen Sie **Angebotsanforderung** aus.
3. Wählen Sie im Feld **Kaufende juristische Person** die Option **USMF** aus. Sie müssen dieselbe juristische Person auswählen, die auch auf der Anforderungsposition ist.  
4. Markieren Sie in der Liste die ausgewählte Zeile. Wenn Sie mehrere Positionen auf Ihrer Bestellanforderung hatten, wählen Sie alle die Positionen aus, die Sie zur Angebotsanforderung hinzufügen möchten.  
5. Wählen Sie **OK**.
6. Aktualisieren Sie die Seite.
7. Überprüfen Sie, ob die Infobox geöffnet ist, und erweitern Sie dann den Abschnitt **Zugehörige Dokumente**.
8. Wählen Sie den Link im Feld **Angebotsanforderung** aus, um die Angebotsanforderung zu öffnen, die soeben erstellt wurde.
9. Wählen Sie **Kopfzeile** aus.
10. Wählen Sie **Hinzufügen** aus.
11. Geben Sie im Feld **Kreditorenkonto** einen Wert ein, oder wählen Sie einen Wert aus.
12. Wählen Sie **Hinzufügen** aus.
13. Geben Sie im Feld **Kreditorenkonto** einen Wert ein, oder wählen Sie einen Wert aus.
14. Wählen Sie **Senden** aus.
15. Wählen Sie **OK**.
16. Wählen Sie **Antwort eingeben** aus.
17. Klicken Sie im Aktivitätsbereich auf **Antworten**.
18. Wählen Sie **Daten in Antwort kopieren** aus. Dies kopiert Daten, wie die Menge und die Datumsangaben, von der Angebotsanforderung zur Antwort.  
19. Geben Sie im Feld **Einzelpreis** eine Zahl ein. Dies ist der Preis, den Sie vom Lieferant empfangen haben. Sie sollten auch zusätzliche Information vom Kreditor eingeben.  
20. Wählen Sie **Akzeptieren** aus.
21. Wählen Sie **OK**.

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Überprüfen Sie, dass Kreditor und Preis an die Anforderung übertragen worden sind
1. Schließen Sie die Seite.
2. Wählen Sie **Positionen** aus.
3. Wählen Sie **Zugehörige Informationen** aus.
4. Wählen Sie **Bestellanforderung** aus.
5. Wählen Sie die Position aus, die zur Angebotsanforderung übertragen wurde. Überprüfen Sie, dass der Preis und der Kreditor zur Anforderung kopiert worden sind.  
6. Klicken Sie zum Öffnen des Dropdown-Dialogfelds auf **Workflow**.
7. Wählen Sie „Abgeschlossen” aus.
8. Wählen Sie die Seite aus.
9. Wählen Sie „Abgeschlossen” aus.

