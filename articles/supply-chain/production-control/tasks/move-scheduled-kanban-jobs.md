---
title: Geplante Kanban-Einzelvorgänge verschieben
description: Der Schwerpunkt dieser Prozedur liegt auf dem Verschieben von geplanten Kanban-Bearbeitungseinzelvorgängen in eine andere Periode.
author: ChristianRytt
manager: tfehr
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2769a7d519e12613796025b658db0b08cdfc4fde
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961639"
---
# <a name="move-scheduled-kanban-jobs"></a>Geplante Kanban-Einzelvorgänge verschieben

[!include [banner](../../includes/banner.md)]

Der Schwerpunkt dieser Prozedur liegt auf dem Verschieben von geplanten Kanban-Bearbeitungseinzelvorgängen in eine andere Periode. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Dieses Verfahren ist für die Fertigungsbereichsvorgesetzten und Produktionsplaner vorgesehen, die mit Kanbans arbeiten.

## <a name="select-scheduled-kanban-jobs"></a>Wählen Sie geplante Kanban-Einzelvorgänge aus. 

1. Wechseln Sie zu **Produktionssteuerung > Kanban > Kanban-Einzelvorgangsplanung**. 

2. Klicken Sie im Feld **Arbeitsgruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen. 

3. Markieren Sie in der Liste die ausgewählte Zeile. 
   - Wählen Sie die Arbeitsgruppe 1250 aus. 
4. Klicken Sie auf **Auswählen**. 

5. Wählen Sie im Feld **Einzelvorgangsstatus anzeigen** die Option **Geplant** aus. Dieses filtert die Einzelvorgangsliste, um nur die geplanten Kanban-Einzelvorgänge anzuzeigen. 

## <a name="move-kanban-jobs-to-a-different-period"></a>Verschieben Sie Kanban-Einzelvorgänge in eine andere Periode. 

1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Wählen Sie einen Einzelvorgang aus, der den Status **Geplanter Einzelvorgang** hat, beispielsweise einen Einzelvorgang, der für den 20. Dezember 2012 geplant war, im Feld **Geplante Periode** aus. Verschieben Sie dann den Einzelvorgang in die vorherige Periode. 

2. Klicken sie auf **Vorherige Periode**. 

3. Klicken Sie auf **Ende**, um den Einzelvorgang an das Ende der Einzelvorgangsliste als den letzten Einzelvorgang in der vorherigen Periode zu verschieben. 

4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Wählen Sie einen Einzelvorgang aus, der den Status **Geplanter Einzelvorgang** hat, beispielsweise einen Einzelvorgang, der für den 18. Dezember 2012 geplant war, im Feld **Geplante Periode** aus. Verschieben Sie dann den Einzelvorgang in die nächste Periode. 

5. Klicken Sie auf **Nächste Periode**. 

6. Klicken Sie auf **Start**, um den Einzelvorgang an den Anfang der Einzelvorgangsliste als den ersten Einzelvorgang in der vorherigen Periode zu verschieben. 

## <a name="move-a-job-within-a-period"></a>Verschieben Sie einen Einzelvorgang innerhalb einer Periode. 

1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Wählen Sie einen Einzelvorgang aus, der den Status „Geplanter Einzelvorgang” hat, beispielsweise den zweiten Einzelvorgang, der für den 19. Dezember 2012 geplant war, im Feld **Geplante Periode** aus. Verschieben Sie dann den Einzelvorgang in die geplante Periode. 

2. Klicken Sie auf **Vorwärts**. Beachten Sie, dass der Einzelvorgang um eine Position in der Liste nach unten verschoben wird. 

3. Klicken Sie auf **Rückwärts**. Beachten Sie, dass der Einzelvorgang um eine Position in der Liste nach oben verschoben wird.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]