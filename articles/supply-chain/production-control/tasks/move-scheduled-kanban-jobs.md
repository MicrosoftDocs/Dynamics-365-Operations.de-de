--- 
title: "Geplante Kanban-Einzelvorgänge verschieben"
description: "Der Schwerpunkt dieser Prozedur liegt auf dem Verschieben von geplanten Kanban-Bearbeitungseinzelvorgängen in eine andere Periode."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2a12a6859a3a436706822873bc6fdd781e0ef032
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="move-scheduled-kanban-jobs"></a>Geplante Kanban-Einzelvorgänge verschieben

[!include[task guide banner](../../includes/task-guide-banner.md)]

Der Schwerpunkt dieser Prozedur liegt auf dem Verschieben von geplanten Kanban-Bearbeitungseinzelvorgängen in eine andere Periode. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Dieses Verfahren ist für die Fertigungsbereichsvorgesetzten und Produktionsplaner vorgesehen, die mit Kanbans arbeiten.


## <a name="select-scheduled-kanban-jobs"></a>Geplante Kanban-Einzelvorgänge auswählen
1. Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.
2. !MtCMR!Klicken Sie im Feld "Arbeitsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen. áçêìõý !
3. Markér den valgte række på listen.
    * Wählen Sie die Arbeitsgruppe 1250 aus.  
4. Klik på Select.
5. Vælg 'Planlagt' i feltet Display job status.
    * Dieses filtert die Einzelvorgangsliste, um nur die geplanten Kanban-Einzelvorgänge anzuzeigen.  

## <a name="move-kanban-jobs-to-a-different-period"></a>Verschieben von Kanban-Einzelvorgängen in eine andere Planungsperiode
1. Find og vælg den ønskede post på listen.
    * Wählen Sie einen Einzelvorgang aus, der den Status "Geplante Einzelvorgänge" hat, beispielsweise einen Einzelvorgang, der für den 20. Dezember 2012 geplant war, im Feld "Geplante Periode" aus. Verschieben Sie dann den Einzelvorgang in die vorherige Periode.  
2. Klik på Previous period.
3. Klik på End.
    * Dies verschiebt den Einzelvorgang an das Ende der Einzelvorgangsliste als den letzten Einzelvorgang in der vorherigen Periode.  
4. Find og vælg den ønskede post på listen.
    * Wählen Sie einen Einzelvorgang aus, der den Status "Geplante Einzelvorgänge" hat, beispielsweise einen Einzelvorgang, der für den 18. Dezember 2012 geplant war, im Feld "Geplante Periode" aus. Verschieben Sie dann den Einzelvorgang in die nächste Periode.  
5. Klik på Next period.
6. Klik på Start.
    * Dies verschiebt den Einzelvorgang an den Beginn der Einzelvorgangsliste als den ersten Einzelvorgang in der vorherigen Periode.  

## <a name="task-move-a-job-within-a-period"></a>Aufgabe: Verschieben Sie einen Einzelvorgang innerhalb einer Periode
1. Find og vælg den ønskede post på listen.
    * Wählen Sie einen Einzelvorgang aus, der den Status "Geplante Einzelvorgänge" hat, beispielsweise den zweiten Einzelvorgang, der für den 19. Dezember 2012 geplant war, im Feld "Geplante Periode" aus. Verschieben Sie dann den Einzelvorgang in die geplante Periode.  
2. Klik på Forward.
    * Beachten Sie, dass der Einzelvorgang um eine Position in der Liste nach unten verschoben wird.  
3. Klik på Backward.
    * Beachten Sie, dass der Einzelvorgang um eine Position in der Liste nach oben verschoben wird.  


