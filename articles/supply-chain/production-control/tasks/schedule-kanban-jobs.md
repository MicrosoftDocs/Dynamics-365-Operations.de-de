---
title: Kanban-Einzelvorgänge planen
description: Der Schwerpunkt dieser Prozedur liegt auf der Planung von Kanban-Bearbeitungseinzelvorgängen für eine spezielle Arbeitsgruppe.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c8342bf6c56adc41cc4944dc709152246ad93a3e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428898"
---
# <a name="schedule-kanban-jobs"></a>Kanban-Einzelvorgänge planen

[!include [banner](../../includes/banner.md)]

Der Schwerpunkt dieser Prozedur liegt auf der Planung von Kanban-Bearbeitungseinzelvorgängen für eine spezielle Arbeitsgruppe. Das Verfahren "Bereiten Sie einen Kanban-Bearbeitungseinzelvorgang vor, wenn Materialien für die Arbeitsgruppe verfügbar sind" ist für dieses Verfahren vorausgesetzt. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Diese Aufgabe ist für die Fertigungsbereichsvorgesetzten und Produktionsplaner vorgesehen, die mit Kanbans arbeiten.


## <a name="select-kanban-jobs-for-a-work-cell"></a>Kanban-Einzelvorgänge für eine Arbeitsgruppe auswählen
1. Wechseln Sie zu "Produktionssteuerung" > "Kanban" > "Kanban-Einzelvorgangsplanung".
2. Periodenkapazität-Infobox erweitern
    * Kanban-Infobox erweitern.  
3. Klicken Sie im Feld "Arbeitsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Markieren Sie in der Liste die ausgewählte Zeile.
    * Wählen Sie die Arbeitsgruppe 1250 aus. Dies filtert die Ansicht, sodass nur die Einzelvorgänge für Arbeitsgruppe 1250 angezeigt werden.  
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Klicken Sie auf Auswählen.

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a>Kanban-Einzelvorgang in der ersten verfügbaren Periode planen
1. Markieren Sie in der Liste die ausgewählte Zeile.
    * Wählen Sie die erste Zeile in der Liste aus, die den Status "Nicht geplant" aufweist. Das gepunktete Symbol im Feld "Einzelvorgangsstatus" gibt "Nicht geplant" an.  
2. Klicken Sie auf "Zeitplan".
    * Dies plant den Kanban-Einzelvorgang in der ersten verfügbaren Periode.  
    * Beachten Sie, dass der Kanban-Einzelvorgang an das Ende der Liste verschoben wird, da er in der Periode hinzugefügt wurde, die ab dem heutigen Tag beginnt.  
    * Wenn die ab dem heutigen Tag beginnende Periode vollständig gebucht ist, wird der Einzelvorgang in die erste verfügbare Periode verschoben.  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a>Zwei Kanban-Einzelvorgänge für einen bestimmten Tag planen
1. Wählen Sie in der Liste die Zeile "1" aus.
    * Sie sollten sehen, dass die erste Zeile den Status "Nicht geplant" im Feld "Einzelvorgangsstatus" hat.  
2. Wählen Sie in der Liste die Zeile "2" aus.
    * Sie sollten sehen, dass die zweite Zeile den Status "Nicht geplant" im Feld "Einzelvorgangsstatus" hat. Jetzt haben Sie die ersten zwei Stellen ausgewählt.  
3. Klicken Sie auf "Anfangsdatum für Zeitplan", um das Dialogfeld zu öffnen.
4. Aktivieren oder deaktivieren Sie "Reaktion auf Kapazitätsmangel überschreiben".
    * Diese Option ermöglicht es Ihnen, die standardmäßige Reaktion auf Kapazitätsmangel zu überschreiben.  
5. Wählen Sie im Feld "Reaktion auf Kapazitätsmangel" "Zur angeforderten Periode hinzufügen" aus.
    * Durch diese Option wird sichergestellt, dass der Einzelvorgang zur angeforderten Periode hinzugefügt wird, unabhängig von, ob die Arbeitsgruppe möglicherweise überlastet wird.  
6. Klicken Sie auf "Zeitplan".
    * Beachten Sie, dass beide Einzelvorgänge zur gewünschten Periode hinzugefügt werden.  
    * Im Abschnitt "Periodenkapazität" können Sie die Auslastung für jede Periode sehen. Das Feld "Verbrauch" zeigt den geplanten Verbrauch in dieser Periode an. Wenn der geplante Verbrauch höher als die verfügbare Kapazität in dieser Periode ist, wird der überladene Verbrauch ausgewählt.  

