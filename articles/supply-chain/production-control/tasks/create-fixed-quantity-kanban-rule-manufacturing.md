---
title: Kanban-Regel für feste Mengen für die Fertigung erstellen
description: Ziel dieser Prozedur ist es, eine notwendige Einstellung für eine feste Fertigungs-Kanban-Regel zum Starten von Umwandlungsaktivitäten in einer Arbeitsgruppe einer kleinen Umgebung zu erstellen.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e0f58d1e265fb001474eb572b9bc325cf08790c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "338681"
---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a>Kanban-Regel für feste Mengen für die Fertigung erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ziel dieser Prozedur ist es, eine notwendige Einstellung für eine feste Fertigungs-Kanban-Regel zum Starten von Umwandlungsaktivitäten in einer Arbeitsgruppe einer kleinen Umgebung zu erstellen. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Diese Vorgehensweise ist für den Verfahrenstechniker oder den Wertstrom-Manager vorgesehen, da dieser die Produktion eines neuen oder geänderten Produkts vorbereitet.


## <a name="create-new-kanban-rule"></a>Neue Kanban-Regel erstellen
1. Wechseln Sie zu Kanban-Regeln.
2. Klicken Sie auf "Neu".
    * Beachten Sie, dass der Standardtyp "Manufacturing und Auffüllungsstrategie sind festgelegt" ist. Sie müssen diese Parameter nicht ändern.  
3. Geben Sie im Feld "Erste Planaktivität" einen Wert ein oder wählen Sie einen Wert aus.
    * Dies ist die Aktivität, die für die Kanbans ausgeführt wird, die auf dieser Kanban-Regel erstellt werden.  Wählen Sie "SpeakerTestAndPackaging" aus.  
4. Erweitern Sie den Abschnitt "Details".
5. Geben Sie im Feld "Produkt" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie L0050 aus.  
6. Geben Sie im Feld "Maßeinheit" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie Minuten aus.  
7. Geben Sie im Feld "Lieferzeit" eine Zahl ein.
    * Geben Sie "5" ein.  

## <a name="set-quantities"></a>Mengen festlegen
1. Erweitern Sie den Abschnitt "Mengen".
2. Legen Sie "Standardmenge" auf "10" fest.
    * Dies ist die Menge, die für jeden Kanban übertragen wird.  
3. Aktivieren Sie das Kontrollkästchen "Abweichung der Produktmenge".
    * Hiermit können ausgewählte Kanbans mit einer Abweichung von der Standardmenge abgeschlossen werden.  Um Kanbans einen Abschluss mit einer Menge von 8 bis 12 zu ermöglichen, legen Sie beide Abweichungen auf 2 fest.  
4. Legen Sie "Abweichung unter" auf '2' fest.
    * Dies ermöglicht einen Abschluss nach unten bis 10 - 2 = 8  
5. Legen Sie "Abweichung über" auf '2' fest.
    * Dies ermöglicht einen Abschluss nach oben bis 10 + 2 = 12  
6. Geben Sie im Feld "Feste Kanban-Menge" eine Zahl ein.
    * Dies ist der Betrag von Kanbans, die aktiv sein sollen. In diesem Fall 5 Kanbans, die je 10 verarbeiten.  
7. Geben Sie im Feld "Min. Warnungsgrenzwert" "2 "ein.
    * Dies wird verwendet, um die Mindestmenge vollständiger Kanbans zu verfolgen, die am Ziel sein sollen. Beispielsweise wird dieses in der Kanban-Mengenübersicht verwendet.  
8. Geben Sie im Feld "Max. Warnungsgrenzwert" "4 "ein.
    * Wird verwendet, um die maximale Menge vollständiger Kanbans zu verfolgen, die am Ziel sein sollen. Beispielsweise wird dieses in der Kanban-Mengenübersicht verwendet.  
9. Geben Sie im Feld "Automatische Planungsmenge" "1"ein.
    * Wenn hier bis 1 festgelegt wird, bedeutet es, dass jeder Kanban automatisch geplant wird.   Wenn wir 3 eingegeben haben, werden die Kanbans nicht terminiert, bis 3 leere Kanbans für die Planung bereit sind. Dies ist zum Gruppieren der Arbeit und der Vermeidung zu vieler Einstellungen hilfreich.  

## <a name="create-kanbans"></a>Kanbans erstellen
1. Erweitern Sie den Abschnitt "Kanbans".
2. Klicken Sie auf "Speichern".
    * Die Kanban-Regel muss gespeichert werden, bevor Kanbans erstellt werden können.  
3. Klicken Sie auf Hinzufügen.
    * Beachten Sie, dass keine aktiven Kanbans vorhanden, deshalb ist die vorgeschlagenen "Anzahl der neuen Kanbans. 5. Dies entspricht der "festen Kanban-Menge".  
4. Klicken Sie auf "Erstellen".
    * Dieses erstellt 5 Kanbans.  
    * Beachten Sie, dass 5 Kanbans mit jeweils 10 für diese Kanban-Produktionsregel erstellt wurden. Dies ist der letzte Schritt in diesem Verfahren.  

