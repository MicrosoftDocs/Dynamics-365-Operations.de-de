--- 
title: "Einen Kanban-Bearbeitungseinzelvorgang vorbereiten, wenn keine Materialien für die Arbeitsgruppe verfügbar sind"
description: "In dieser Prozedur liegt der Schwerpunkt auf dem Vorbereiten eines Kanban-Bearbeitungseinzelvorgangs, wenn einige Materialien nicht für die Arbeitsgruppe verfügbar sind und es daher erforderlich ist, Materialien aus dem Lagerort zu entnehmen."
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
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5a47af6910a9686e74ab6d1069dd02079e60cb8a
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a>Einen Kanban-Bearbeitungseinzelvorgang vorbereiten, wenn keine Materialien für die Arbeitsgruppe verfügbar sind

[!include[task guide banner](../../includes/task-guide-banner.md)]

In dieser Prozedur liegt der Schwerpunkt auf dem Vorbereiten eines Kanban-Bearbeitungseinzelvorgangs, wenn einige Materialien nicht für die Arbeitsgruppe verfügbar sind und es daher erforderlich ist, Materialien aus dem Lagerort zu entnehmen. Das Verfahren "Bereiten Sie einen Kanban-Bearbeitungseinzelvorgang vor, wenn Materialien für die Arbeitsgruppe verfügbar sind" ist für dieses Verfahren vorausgesetzt. Diese Prozedur ist für den Maschinenbediener vorgesehen. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.

1. Wechseln Sie zu "Produktionssteuerung" > "Kanban" > "Kanban-Übersicht für Prozesseinzelvorgänge".
2. Klicken Sie im Feld "Arbeitsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Wählen Sie die Arbeitsgruppe 1250 aus.  
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie "Kanban 000356" aus.  
5. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie in der Liste die Zeile 4 ab. Heben Sie in der Liste die Auswahl von Zeile 4 auf, oder wählen Sie Zeile 4 aus, wenn Sie die Aufgabe "Bereiten Sie einen Kanban-Bearbeitungseinzelvorgang vor, wenn Material vorhanden ist" noch nicht abgeschlossen haben.  
6. Schalten Sie die Erweiterung des Abschnitts "Kommissionierliste" ein/aus.
    * Das Symbol "Kein Eintrag" im Beschaffungsstatus gibt an, dass 48 EA des Artikels P0002 für die Arbeitsgruppe fehlen.  

## <a name="transfer-materials-to-work-cell"></a>Übertragen von Materialien zur Arbeitsgruppe
1. Schalten Sie die Erweiterung des Abschnitts "Umlagerungseinzelvorgänge" ein/aus.
2. Verwenden Sie den Schnellfilter, um im Feld "Artikelnummer" nach dem Wert "P0002" zu filtern.
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
4. Klicken Sie auf "Start".
    * Übertragung läuft.  
5. Klicken Sie auf "Abgeschlossen".
    * Artikel P0002 ist nun in der Kommissionierliste für den Kanban-Einzelvorgang verfügbar. Das bedeutet, dass wir das Kanban mit allen obligatorischen Materialien vorbereiten können.  
6. Klicken Sie auf "Vorbereiten".
    * Beachten Sie, dass ein Symbol im Einzelvorgangsstatus angibt, dass der Einzelvorgang nun bereit ist.  


