---
title: Kanban-Regel für ein Stücklistenpositionsereignis erstellen
description: Diese Aufgabe konzentriert sich auf die Einstellungen, die zum Erstellen einer Ereignis-Kanban-Regel erforderlich sind, um die Beschaffung für Produktions-Stücklistenpositionen in einer gemischten schlanken und klassischen Produktionsumgebung sicherzustellen.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdTable, ProdBOM, ProdParmCostEstimation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27d415e146f33224bcbbfb73498040d584e07f10
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829209"
---
# <a name="create-a-bom-line-event-kanban-rule"></a>Kanban-Regel für ein Stücklistenpositionsereignis erstellen

[!include [banner](../../includes/banner.md)]

Diese Aufgabe konzentriert sich auf die Einstellungen, die zum Erstellen einer Ereignis-Kanban-Regel erforderlich sind, um die Beschaffung für Produktions-Stücklistenpositionen in einer gemischten schlanken und klassischen Produktionsumgebung sicherzustellen. Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF. Diese Aufgabe ist für den Fertigungsplaner oder den Wertstrommanager vorgesehen, da dieser die Produktion eines neuen oder geänderten Produkts vorbereitet.


## <a name="create-a-new-kanban-rule"></a>Neue Kanban-Regel erstellen
1. Wechseln Sie zu "Produktionssteuerung" > "Periodische Aufgaben" > "Kanban-Mengenberechnung" > "Kanban-Regeln".
2. Klicken Sie auf "Neu".
3. Wählen Sie im Feld "Typ" die Option "Entnahme" aus.
    * Der "Entnahmetyp" wird verwendet, um Umlagerungs-Kanbans zu erstellen.  
4. Wählen Sie im Feld "Auffüllungsstrategie" "Ereignis" aus.
    * Die "Ereignisstrategie" wird ausgewählt, um die Übertragung von Kanbans auf Grundlage eines Ereignisses zu erstellen. Später im Aufgabenleitfaden lösen wir sie aus, indem wir einen Produktionsauftrag vorkalkulieren.  
5. Geben Sie im Feld "Erste Planaktivität" einen Wert ein oder wählen Sie einen Wert aus.
    * Geben Sie "ReplenishSpeakerComponents" ein oder wählen Sie es aus. Diese Umlagerungsaktivität hat Zugangs- (Ausgangs-)Lagerort und Lagerplatz 12. Das bedeutet, dass Material zu Lagerplatz 12 in Lagerort 12 verschoben wird.  
6. Erweitern Sie den Abschnitt "Details".
7. Geben Sie im Feld "Produkt" den Wert "M0001" ein, oder wählen Sie ihn aus.
8. Erweitern Sie den Abschnitt "Ereignis".
9. Wählen Sie im Feld "Stücklisten-Positionsereignis" die Option "Automatisch" aus.
    * Wenn das Feld "Stücklistenpositionsereignis" auf "Automatisch" festgelegt ist, wird Kanban erstellt, um die Materialanforderungen für Produktionsauftrags-Stücklistenpositionen zu erfüllen.  
10. Schließen Sie die Seite.

## <a name="create-and-modify-a-new-production-order"></a>Erstellen und ändern Sie einen neuen Produktionsauftrag
1. Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".
2. Klicken Sie auf "Neuer Produktionsauftrag".
3. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
    * Geben Sie "L0001" ein oder wählen Sie es aus. Wir verwenden Artikel L0001, da Artikel M0001 in der Stückliste für Artikel L0001 enthalten ist.  
4. Klicken Sie auf "Erstellen".
5. Klicken Sie in der Liste auf den Link in der Zeile für "L0001".
6. Klicken Sie auf "Stückliste".
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Klicken Sie auf "Bearbeiten".
9. Wählen Sie im Feld "Positionstyp" die Option "Lieferung mit Bedarfsverursachung" aus.
    * "Lieferung mit Bedarfsverursachung" ist ausgewählt, um die Beschaffungserstellung eines Kanban auszulösen.  
10. Wählen Sie "Nein" im Feld "Ressourcenverbrauch" aus.
    * Das Deaktivieren des Kontrollkästchens "Ressourcenverbrauch" ermöglicht es uns, den Lagerort zu ändern.  
11. Erweitern Sie den Abschnitt "Lagerungsdimensionen".
12. Geben Sie im Feld Lagerort "12" ein.
    * Lagerort wird auf 12 festgelegt, da dies der Ausgangslagerort für die Entnahmeaktivität ist.  
13. Geben Sie im Feld "Lagerplatz" den Wert "12" ein.
    * Lagerplatz wird auf 12 festgelegt, da dies der Ausgangslagerplatz der Entnahmeaktivität ist.  
14. Schließen Sie die Seite.
15. Schließen Sie die Seite.

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a>Nehmen Sie eine Vorkalkulation des Produktionsauftrags vor und zeigen Sie den erstellten Kanban an
1. Klicken Sie auf "Vorkalkulation".
    * Die Vorkalkulation des Produktionsauftrags löst die Erstellung des zugeordneten Kanbans aus, um Artikel M0001 zu liefern.  
2. Klicken Sie auf "OK".
3. Schließen Sie die Seite.
4. Schließen Sie die Seite.
5. Wechseln Sie zu "Produktinformationsverwaltung" > "Lean Manufacturing" > "Kanban-Regeln".
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Wählen Sie die Ereignis-Kanban-Regel aus, die für "M0001 erstellt wurde.  
7. Erweitern Sie den Abschnitt "Kanbans".
8. Markieren Sie in der Liste die ausgewählte Zeile.
    * Beachten Sie das Kanban, das erstellt wird, um M0001 für den vorkalkulierten Produktionsauftrag zu liefern.  
    * Dies ist der letzte Schritt!  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]