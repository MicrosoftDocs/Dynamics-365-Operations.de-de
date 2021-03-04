---
title: Kanban-Einzelvorgangsstatus zurücksetzen
description: Ziel dieser Prozedur ist das Zurücksetzen eines falschen Kanban-Einzelvorgangsstatus.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cca5ea3a4c33c7f36acd18a8af7034466b3b580
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428665"
---
# <a name="revert-kanban-job-status"></a>Kanban-Einzelvorgangsstatus zurücksetzen

[!include [banner](../../includes/banner.md)]

Ziel dieser Prozedur ist das Zurücksetzen eines falschen Kanban-Einzelvorgangsstatus. Dies ist hilfreich, falls der Maschinenbediener den falschen Einzelvorgang aktualisiert, oder versehentlich den falschen Status festgelegt hat. In diesem Verfahren wird ein Kanban-Einzelvorgang versehentlich als vorbereitet erfasst und der Status wird zurückgesetzt. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Diese Prozedur ist für Filialleiter oder Maschinenbediener vorgesehen, die in einem Lean Manufacturing-Unternehmen arbeiten.


## <a name="open-process-board-for-the-work-cell"></a>Öffnen Sie die Prozessübersicht für Arbeitsgruppen.
1. Gehen Sie zu "Kanban Tafel für Prozesseinzelvorgänge".
2. Geben Sie im Feld 'Arbeitsgruppe' einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie die Arbeitsgruppe 1260 aus.  

## <a name="prepare-kanban-job"></a>Kanban-Einzelvorgang vorbereiten
1. Klicken Sie auf "Vorbereiten".
    * Wenn Sie nicht auf "Vorbereiten" klicken können, da es ausgeblendet ist, sollten Sie überprüfen, dass der ausgewählte Kanban-Einzelvorgang den Status "Geplant" hat, der durch das leere Kanbansymbol angegeben wird. Wenn "Vorbereiten" fehlschlägt, überprüfen Sie, ob alle Materialien in der Kommissionierliste verfügbar sind.  
2. Wählen Sie in der Liste den gewünschten Einzelvorgang aus.
    * Wählen Sie den ersten Einzelvorgang aus, den Sie soeben vorbereitet haben.  
    * Beachten Sie, dass der Einzelvorgangsstatus vorbereitet ist, der mit einem Dreieck innerhalb des Kanbansymbols angegeben ist.  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a>Hiermit wird der Status des vorbereiteten Kanban-Einzelvorgangs wiederhergestellt.
1. Markieren Sie in der Liste die ausgewählte Zeile.
    * Wählen Sie den ersten Einzelvorgang aus, den Sie bereits vorbereitet wurde.  
2. Klicken Sie im Aktivitätsbereich auf "Fertigung".
3. Klicken Sie auf "Status wiederherstellen".
    * Sie können eine alternative Kanban-Regel verwenden, wenn die folgenden Bedingungen erfüllt sind: - Die Wiederbeschaffungsstrategie ist die gleiche für beide Regeln.  - Die Version des Produktionsflusses ist die gleiche für beide Regeln.  - Das Produkt, das beschafft wird, ist das gleiche für beide Regeln.  - Alle Downstream-Aktivitäten, die für die letzte Aktivität der Kanban-Regeln konfiguriert werden, müssen die gleichen für beide Regeln sein.  - Die gleichen angegebene Lagerungsdimensionen müssen für beide Regeln konfiguriert werden.  - Der Status der Handhabungseinheit muss "Nicht zugewiesen" sein.  - Die Konfiguration für Ereignis-Kanbans muss die gleiche sein.  
    * Stellen Sie sicher, dass der neue Status "Geplant" lautet.  
4. Klicken Sie auf "OK".
5. Heben Sie in der Liste die Markierung der ausgewählten Zeile auf.
    * Wählen Sie den gleichen Einzelvorgang aus.  
    * Beachten Sie, dass der Einzelvorgangsstatus für den Kanban-Einzelvorgang auf "Geplant" zurückgesetzt wurde und von einem leeren Kanbansymbol angegeben wird.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]