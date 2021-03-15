---
title: Neue Entnahme-Kanban-Regel erstellen
description: Diese Prozedur zeigt die Einstellungen, die benötigt werden, um eine Kanban-Entnahmeregel für das Übertragen von Material in einer schlanken Umgebung zu erstellen.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1694472e20c28a0b0f94c1ced8544b7258c22b40
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007090"
---
# <a name="create-a-withdrawal-kanban-rule"></a>Neue Entnahme-Kanban-Regel erstellen

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt die Einstellungen, die benötigt werden, um eine Kanban-Entnahmeregel für das Übertragen von Material in einer schlanken Umgebung zu erstellen. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Diese Prozedur ist für den Fertigungsplaner oder den Wertstrommanager vorgesehen, da dieser die Auffüllung eines neuen oder geänderten Materials vorbereitet.


## <a name="create-new-kanban-rule"></a>Neue Kanban-Regel erstellen
1. Wechseln Sie zu Kanban-Regeln.
2. Klicken Sie auf "Neu".
3. Wählen Sie im Feld "Typ" die Option "Entnahme" aus.
    * Der "Entnahmetyp" wird verwendet, sodass Kanban-Regeln Material oder Waren übertragen können.  
4. Geben Sie im Feld "Erste Planaktivität" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie "ReplenishSpeakerComponents" aus.   Diese Aktivität wird so eingerichtet, dass Komponenten aus Lagerort 11, Lagerplatz 11, nach Lagerort 12 und Lagerplatz 12 verschoben werden.  
5. Geben Sie im Feld "Produkt" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie M0007 aus.  
6. Geben Sie im Feld "Lieferzeit" eine Zahl ein.
    * Beispiel: 60.  
7. Geben Sie im Feld "Maßeinheit" einen Wert ein, oder wählen Sie einen Wert aus.
    * Beispielsweise "Minuten".  

## <a name="set-quantities-for-kanban"></a>Legen Sie Mengen für Kanban fest
1. Legen Sie "Standardmenge" auf "5" fest.
    * Dies ist die Menge, die für jeden Kanban übertragen wird.  
2. Geben Sie im Feld "Feste Kanban-Menge" die Zahl "2"ein.
    * Dies ist der Betrag von Kanbans, die aktiv sein sollen. In diesem Fall 2 Kanbans, die jeweils 5 übertragen.  
3. Geben Sie im Feld "Min. Warnungsgrenzwert" "1 "ein.
    * Dies wird verwendet, um die Mindestmenge vollständiger Kanbans zu verfolgen, die am Ziel sein sollen. Beispielsweise wird dieses in der Kanban-Mengenübersicht verwendet.  
4. Geben Sie im Feld "Max. Warnungsgrenzwert" "2 "ein.
    * Wird verwendet, um die maximale Menge vollständiger Kanbans zu verfolgen, die am Ziel sein sollen. Beispielsweise wird dieses in der Kanban-Mengenübersicht verwendet.  

## <a name="create-kanbans"></a>Kanbans erstellen
1. Klicken Sie auf "Speichern".
    * Die Kanban-Regel muss gespeichert werden, bevor Kanbans erstellt werden können.  
2. Klicken Sie auf Hinzufügen.
    * Beachten Sie, dass keine aktiven Kanbans vorhanden sind, da die vorgeschlagene "Anzahl der neuen Kanbans" 2 beträgt. Dies entspricht der "Feste Kanban-Menge".  
3. Klicken Sie auf "Erstellen".
    * Dadurch werden zwei Kanbans erstellt.  
    * Beachten Sie, dass 2 Kanbans für jeweils 5 für diese Kanban-Entnahmeregel erstellt wurden.  Dies ist der letzte Schritt in diesem Verfahren.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]