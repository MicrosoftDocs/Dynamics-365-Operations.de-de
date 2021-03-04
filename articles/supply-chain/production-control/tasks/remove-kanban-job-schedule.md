---
title: Einen Kanban-Einzelvorgang aus der Planung entfernen
description: Der Schwerpunkt dieser Prozedur liegt auf dem Entfernen eines geplanten Kanban-Bearbeitungseinzelvorgang aus der Planung durch das Zurücksetzen des Einzelvorgangsstatus zu "Nicht geplant".
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0236faa9b534678ed232ac3572c8172c62e5241f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428398"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a>Einen Kanban-Einzelvorgang aus der Planung entfernen

[!include [banner](../../includes/banner.md)]

Der Schwerpunkt dieser Prozedur liegt auf dem Entfernen eines geplanten Kanban-Bearbeitungseinzelvorgang aus der Planung durch das Zurücksetzen des Einzelvorgangsstatus zu "Nicht geplant". Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Dieses Verfahren ist für Fertigungsbereichsvorgesetzte und Produktionsplaner vorgesehen.


## <a name="find-a-planned-kanban-job"></a>Geplanten Kanban-Einzelvorgang suchen
1. Wechseln Sie zu "Produktionssteuerung" > "Kanban" > "Kanban-Einzelvorgangsplanung".
2. Klicken Sie im Feld "Arbeitsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Wählen Sie die Arbeitsgruppe 1250 aus.  
4. Klicken Sie auf Auswählen.
5. Wählen Sie im Feld "Einzelvorgangsstatus anzeigen" "Geplant" aus.

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a>Entfernen des geplanten Kanban-Einzelvorgangs aus der Planung
1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie einen Einzelvorgang aus, der den Statuts "Geplant" hat, beispielsweise einen Einzelvorgang vom 19. Dezember 2012.  
2. Klicken Sie im Aktivitätsbereich auf "Plan".
3. Klicken Sie auf "Einzelvorgangsstatus zurücksetzen".
4. Klicken Sie auf "OK".
    * Dadurch wird der aktuelle Status von "Geplant" zu "Nicht geplant" geändert und aus der Prozessübersicht entfernt.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]