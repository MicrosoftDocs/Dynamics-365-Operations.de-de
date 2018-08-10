--- 
title: Sachkonto-Zuordnungserfassung verarbeiten
description: "Mithilfe der Seite \"Zuordnungsanforderung verarbeiten\" können Sie eine Zuordnungserfassung erstellen, die vor der Buchung im Hauptbuch geprüft und genehmigt oder direkt im Hauptbuch gebucht werden kann."
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7d299657758b1e1322aef07bfe8c71f7bf00b0ca
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="process-ledger-allocation-journal"></a>Sachkonto-Zuordnungserfassung verarbeiten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Mithilfe der Seite "Zuordnungsanforderung verarbeiten" können Sie eine Zuordnungserfassung erstellen, die vor der Buchung im Hauptbuch geprüft und genehmigt oder direkt im Hauptbuch gebucht werden kann. Vor der Erstellung einer Zuordnungserfassung muss mindesten eine Sachkontozuordnungsregel erstellt werden. Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.

1. Wechseln Sie zu "Hauptbuch" > "Zuteilungen" > "Zuteilungsanforderung verarbeiten".
2. Klicken Sie im Feld "Regel" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Geben Sie im Feld "Per Datum" ein Datum ein.
    * Das Anfangsdatum ist außerordentlich wichtig, wenn das Sachkonto die Datenquelle für die Regel ist. Dieses Datum steuert, welche Sachkonto für die Zuweisung genutzt wird.     Wählen Sie im Feld "Keine Quelle" "Beenden". Dies beendet den Zuordnungsprozess und eine Fehlermeldung mit dem Hinweis wird angezeigt, dass ein Ausgangsbetrag mit dem Wert "Null" ausgewählt ist.  
6. Wählen Sie im Feld "Vorschlagsoptionen" "nur Vorschlag" aus.
    * Wählen Sie "Nur Vorschlag" aus, um das Ergebnis in den Zuordnungserfassungen vor dem Buchen der Zuordnung in das Hauptbuch zu prüfen und optional zu genehmigen.  
7. Geben Sie im Feld "Datum für Sachkontobuchung" ein Datum ein.
8. Klicken Sie auf "OK".
9. Wechseln Sie zu "Hauptbuch" > "Zuteilungen" > "Zuteilungserfassungen".
10. Klicken Sie auf "Positionen".
11. Klicken Sie auf "Buchen".
12. Klicken Sie auf "Buchen".


