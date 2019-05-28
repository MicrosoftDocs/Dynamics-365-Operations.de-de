---
title: Aufträge bestätigen
description: Diese Verfahren zeigt, wie Aufträge bestätigt werden.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db475cf967bebec2d442aaa864800d920cf0ab81
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563993"
---
# <a name="confirm-sales-orders"></a>Aufträge bestätigen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Verfahren zeigt, wie Aufträge bestätigt werden. Sie werden angezeigt, wie einen einzelnen Auftrag bestätigt und wie man bestätigt mehrerer Aufträge gleichzeitig. Diese Aufgaben werden normalerweise von einem Auftragsbearbeiter ausgeführt. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden. Bevor Sie beginnen, stellen Sie sicher, dass es mehrere offene Aufträge für denselben Debitor vorhanden ist. Wenn Sie USMF verwenden, können Sie Debitor US-027 verwenden.


## <a name="confirm-a-single-sales-order"></a>Einzelnen Auftrag bestätigen
1. Wechseln Sie zu "Vertrieb und Marketing" > "Aufträge" > "Alle Aufträge".
2. Suchen Sie in der Liste den Auftrag und wählen Sie diese aus, den Sie bestätigen wollen.
3. Klicken Sie auf den Link auf der Auftragsnummer, um den ausgewählten Auftrag zu öffnen.
4. Klicken Sie im Aktivitätsbereich auf "Verkaufen".
5. Klicken Sie auf "Auftrag bestätigen".
6. Erweitern oder reduzieren Sie den Abschnitt "Parameter".
    * Stellen Sie sicher, dass das Feld Buchen Ja aktiv ist.  
7. Legen Sie die Option "Bestätigung drucken" auf "Ja" fest.
    * Das Scheckkreditlimitfeld gibt die Methode, die verwendet wird, um den verbleibenden Kredit eines Debitors zu berechnen. Standardmäßig wird der Code wird aus der Seite Debitorenparameter kopiert. Wenn Sie die Kreditlimitprüfung übersprungen werden sollen, wenn Sie einen bestimmten Auftrag bestätigen, festsetzten das Kreditlimit auf Kein. Sie sollten jedoch daran denken, dass auch mit, wenn dieses Feld auf Kein festgelegt ist, die Kreditlimitprüfung weiterhin ausgeführt wird, wenn die erforderliche Kreditlimitoption auf den Debitorenmasterdaten aktiviert ist.  
8. Klicken Sie auf "OK".
9. Klicken Sie auf "Ja".
10. Schließen Sie die Seite.
11. Klicken Sie im Aktivitätsbereich auf "Optionen".
12. Klicken Sie auf "Ansicht ändern".
13. Klicken Sie auf die Kopfzeilenansicht.
    * Wenn ein Auftrag bestätigt wird, wird der Dokumentstatus zur Bestätigung festgelegt.  
14. Klicken Sie im Aktivitätsbereich auf "Verkaufen".
15. Klicken Sie auf Auftragsbestätigung anzeigen.
16. Schließen Sie die Seite.

## <a name="confirm-multiple-sales-orders-at-once"></a>Bestätigen Sie mehrere Aufträge gleichzeitig
1. Wechseln Sie zu Vertrieb und Marketing > Aufträge > Buchungsbeschreibung > Bestätigen Sie Auftrag.
2. Klicken Sie auf Auswählen.
3. In der Liste auf der Registerkarte "Bereich", finden und wählen Sie den Datensatz aus, der das Feld "Debitorenkonto" verweist.
4. Klicken Sie im Feld "Kriterien" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Suchen und wählen Sie das Debitorenkonto aus, für das mehrere Aufträge hat, die per Massenerstellung soll bestätigen.
    * Wenn Sie USMF verwenden, können Sie Konto US-027 auswählen.  
6. Klicken Sie auf "OK".
    * Die Registerkarte Überblick zeigt eine Liste der Aufträge an, die die Abfragekriterien übereinstimmen. Dabei werden in der Bestätigung eingeschlossen.  
    * Die Feld Sammelaktualisierung für gibt den Parameter an, um den mehrere Aufträge in einem Bestätigungsdokument zusammengefasst werden sollen. Standardmäßig wird der Option in den Standardwerten für Sammelaktualisierungseinstellung auf der Debitorenparameterseite kopiert.  
7. Wählen Sie im Feld "Sammelaktualisierung für" die Option "Auftrag" aus.
    * Die mindestens erforderlichen Parameter zum Erstellen von Zusammenfassungsupdates sind Rechnungsbetrag und Währung. Das bedeutet, dass Sammelaktualisierungen, die verschiedene Rechnungskontos und verschiedene Währungen aufweisen, nicht zulässig sind. Zusätzliche Parameter können in der Sammelaktualisierungsparameterseite eingerichtet werden, die von der Debitorenparameterseite zugegriffen werden kann.  
8. Klicken Sie im Feld Auftrag auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
9. Wählen Sie in der Liste den als Sammelauftrag zu verwendenden Auftragsnummer aus.
10. Klicken Sie auf Anordnen.
11. Klicken Sie auf "OK".
12. Klicken Sie auf "OK".

