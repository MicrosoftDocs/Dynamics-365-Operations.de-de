--- 
title: Eine Produktionsflussversion deaktivieren
description: Wenn eine aktive Produktionsflussversion nicht mehr erforderlich ist, kann diese deaktiviert werden.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 4a7eee6617e12d59a3d06207f5f6b58c93e28240
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="deactivate-a-production-flow-version"></a>Eine Produktionsflussversion deaktivieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Wenn eine aktive Produktionsflussversion nicht mehr erforderlich ist, kann diese deaktiviert werden. Sie sollten diese Option nur verwenden, wenn alle Kanban-Regeln und Aktivitäten beendet sind und nicht erneut aktiviert werden. Beachten Sie, dass das Ablaufdatum aller Kanban-Regeln für diese Produktionsflussversion mit dem aktuellen Datum und der aktuellen aktualisiert werden. 

Um eine aktive Produktionsflussversion zu ändern, sollten Sie ein Ablaufdatum für die aktive Version festgelegt und eine neue Version erstellen. Dadurch wird es Ihnen ermöglicht, die Produktionsarbeitsgänge beim Vorbereiten der neuen Version sowie der verwandten Kanban-Regeln fortzusetzen. 

Um eine aktive Produktionsflussversion ablaufen zu lassen, müssen Sie ein Ablaufdatum festlegen. Die Deaktivierung ist somit mehr eine Ausnahme als eine Regel. 

Für diese Prozedur benötigen Sie einen Produktionsfluss mit einer Version, die deaktiviert werden kann. Führen Sie dies nicht in einer Produktionsumgebung aus, es sei denn, Sie sind 100% sicher, dass die Version nicht mehr benötigt wird.


## <a name="deactivate-a-production-flow-version"></a>Eine Produktionsflussversion deaktivieren
1. Wechseln Sie zu "Produktionssteuerung" > "Einrichten" > "Lean-Produktionsfluss" > "Produktionsflüsse".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Klicken Sie auf "Deaktivieren".
    * Fahren Sie fort nicht, wenn Sie nicht 100% sicher sind, dass die Produktionsflussversion nicht mehr aktuell ist. Beim Klicken auf "Ok" laufen alle aktiven Kaban-Regeln aus und alle Produktions- und Wiederbeschaffungsaktivitäten dieser Produktionsflussversion werden sofort gestoppt.  
6. Klicken Sie auf "OK".


