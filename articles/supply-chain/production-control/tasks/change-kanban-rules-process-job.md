---
title: Kanban-Regeln für einen Prozesseinzelvorgang ändern
description: Ziel dieser Prozedur ist es, die verwendete Kanban-Regel für einen angegebenen Kanban zu ändern.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13798e3521efacda896ca88a39faf36ac979d42c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574496"
---
# <a name="change-kanban-rules-for-a-process-job"></a>Kanban-Regeln für einen Prozesseinzelvorgang ändern

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]