---
title: Sachkonto-Zuordnungserfassung verarbeiten
description: Mithilfe der Seite "Zuordnungsanforderung verarbeiten" können Sie eine Zuordnungserfassung erstellen, die vor der Buchung im Hauptbuch geprüft und genehmigt oder direkt im Hauptbuch gebucht werden kann.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 087bd4f203e8762447e823b19076b79296a390d6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846366"
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

