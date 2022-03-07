---
title: Aufträge bestätigen
description: Diese Verfahren zeigt, wie Aufträge bestätigt werden.
author: omulvad
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup, SalesUnconfirmedOrdersPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ac5217ecd74e3a8d4dd6a82112788a7aaba4698857cd5854eed1f8c91aa97e73
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779157"
---
# <a name="confirm-sales-orders"></a>Aufträge bestätigen

[!include [banner](../../includes/banner.md)]

Diese Verfahren zeigt, wie Aufträge bestätigt werden. Es wird angezeigt, wie ein einzelner Auftrag bestätigt wird und wie man mehrere Aufträge gleichzeitig bestätigt. Diese Aufgaben werden normalerweise von einem Auftragsbearbeiter ausgeführt. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden. Bevor Sie beginnen, stellen Sie sicher, dass es mehrere offene Aufträge für denselben Debitor vorhanden ist. Wenn Sie USMF verwenden, können Sie Debitor US-027 verwenden.


## <a name="confirm-a-single-sales-order"></a>Einzelnen Auftrag bestätigen
1. Wechseln Sie zu **Navigationsbereich > Module > Vertrieb und Marketing > Aufträge > Alle Aufträge**.
2. Suchen Sie in der Liste den Auftrag und wählen Sie diese aus, den Sie bestätigen wollen.
3. Klicken Sie auf den Link auf der Auftragsnummer, um den ausgewählten Auftrag zu öffnen.
4. Klicken Sie im **Aktivitätsbereich** auf **Verkaufen**.
5. Klicken Sie auf **Auftrag bestätigen**.
6. Erweitern Sie den Abschnitt **Parameter**. Stellen Sie sicher, dass die Option **Buchung** auf „Ja“ festgelegt ist.  
7. Legen Sie die Option **Bestätigung drucken** auf „Ja“ fest. Das Feld **Scheckkreditlimit** gibt die Methode an, die verwendet wird, um den verbleibenden Kredit von einem Debitor zu berechnen. Standardmäßig wird der Code aus der Seite Debitorenparameter kopiert. Wenn die Kreditlimitprüfung übersprungen werden soll, wenn Sie einen bestimmten Auftrag bestätigen, setzen Sie **Kreditlimit prüfen** auf „Nein“. Sie sollten jedoch daran denken, dass auch dann, wenn dieses Feld auf „Nein“ festgelegt ist, die Kreditlimitprüfung weiterhin ausgeführt wird, wenn die Option **Kreditlimit erforderlich** bei den Debitorenmasterdaten ausgewählt ist. 
8. Klicken Sie auf **OK**.
9. Klicken Sie auf **Ja**.
10. Schließen Sie die Seite.
11. Klicken Sie im **Aktivitätsbereich** auf **Optionen**.
12. Klicken Sie auf **Ansicht ändern**.
13. Klicken Sie auf **Kopfzeilenansicht**. Wenn ein Auftrag bestätigt wird, wird der **Dokumentstatus** auf „Bestätigung“ festgelegt. 
14. Klicken Sie im **Aktivitätsbereich** auf **Verkaufen**.
15. Klicken Sie auf **Auftragsbestätigung**.
16. Schließen Sie die Seite.

## <a name="confirm-multiple-sales-orders-at-once"></a>Bestätigen Sie mehrere Aufträge gleichzeitig
1. Wechseln Sie zu **Vertrieb und Marketing > Aufträge > Auftragsbestätigung > Auftrag bestätigen**.
2. Klicken Sie auf **Auswählen**.
3. Suchen Sie in der Liste auf der Registerkarte **Bereich** nach dem Datensatz, der auf das Feld **Debitorenkonto** verweist, und wählen Sie ihn aus.
4. Klicken Sie im Feld **Kriterien** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Suchen und wählen Sie das Debitorenkonto aus, für das mehrere Aufträge hat, die per Massenerstellung soll bestätigen. Wenn Sie USMF verwenden, können Sie Konto US-027 wählen.  
6. Klicken Sie auf **OK**.
    - Die Registerkarte **Überblick** zeigt eine Liste der Aufträge an, die mit den Abfragekriterien übereinstimmen. Dabei werden in der Bestätigung eingeschlossen.  
    - Die Feld **Sammelaktualisierung für** im Abschnitt **Parameter** gibt die Parameter an, mit denen mehrere Aufträge in einem Bestätigungsdokument zusammengefasst werden sollen. Standardmäßig wird die Option von der Einstellung **Standardwerte für Sammelaktualisierung** auf der Seite **Debitorenparameter** kopiert.  
7. Wählen Sie im Feld **Sammelaktualisierung für** die Option „Auftrag“ aus. Die mindestens erforderlichen Parameter zum Erstellen von Zusammenfassungsupdates sind **Rechnungsbetrag** und **Währung**. Das bedeutet, dass Sammelaktualisierungen, die verschiedene Rechnungskontos und verschiedene Währungen aufweisen, nicht zulässig sind. Zusätzliche Parameter können auf der Seite **Sammelaktualisierungsparameter** eingerichtet werden, über die von der Seite **Debitorenparameter** zugegriffen werden kann. 
8. Klicken Sie im Feld **Auftrag** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
9. Wählen Sie in der Liste den als Sammelauftrag zu verwendenden Auftragsnummer aus.
10. Klicken Sie auf **Anordnen**.
11. Klicken Sie auf **OK**.
12. Klicken Sie auf **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]