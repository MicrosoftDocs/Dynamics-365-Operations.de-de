--- 
title: "Kanban-Regeln für einen Prozesseinzelvorgang ändern"
description: "Ziel dieser Prozedur ist es, die verwendete Kanban-Regel für einen angegebenen Kanban zu ändern."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: e8355a94322e6489fe64f22a049a34b7ecfe65b9
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="change-kanban-rules-for-a-process-job"></a>Kanban-Regeln für einen Prozesseinzelvorgang ändern

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ziel dieser Prozedur ist es, die verwendete Kanban-Regel für einen angegebenen Kanban zu ändern. Dies ist hilfreich für Ebenenauslastungen von Recourcen oder im Falle der Aufschlüsselung. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Diese Vorgehensweise ist für den Planer vorgesehen, der bei einem Lean Manufacturing-Unternehmen arbeitet, das für Wertstrom zuständig ist.


## <a name="copy-kanban-rule"></a>Kanban-Regel kopieren
1. Wechseln Sie zu Kanban-Regeln.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie die Ereignis-Kanban-Regel 000022 für L0001 aus.  
3. Klicken Sie auf das Formular "Kanban-Regel duplizieren"
4. Klicken Sie auf "OK".

## <a name="change-kanban-rule"></a>Kanban-Regel ändern
1. Schließen Sie die Seite.
2. Wechseln Sie zu "Kanban-Feinterminierung".
3. Markieren Sie in der Liste die ausgewählte Zeile.
    * Wählen Sie die Position mit Kanban 000177 aus.  
4. Klicken Sie auf "Alternative Kanban-Regel verwenden".
5. Klicken Sie auf Weiter.
6. Geben Sie im Feld 'Kanban-Regel' einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie die Kanban-Regel aus, die Sie eben erstellt haben. Dies ist die Kanban-Regel mit der höchsten Nummer.  
7. Klicken Sie auf Fertig stellen.
    * Jetzt verwendet der Kanban-Einzelvorgang eine andere Kanban-Regel. Dies kann hilfreich sein, um Arbeitsgruppen auf eine Ebene zu laden.  


