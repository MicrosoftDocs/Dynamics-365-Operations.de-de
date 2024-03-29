---
title: Übergangsmaterialien mit Kanban-Einzelvorgängen
description: Der Schwerpunkt dieser Prozedur liegt auf dem Ausführen eines Entnahme-Kanban-Einzelvorgangs, um Material zu übertragen.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 11771bbedc9fe4bdfaaa074c449cd329ce1a1d8f
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567990"
---
# <a name="transfer-materials-with-kanban-jobs"></a>Übergangsmaterialien mit Kanban-Einzelvorgängen

[!include [banner](../../includes/banner.md)]

Der Schwerpunkt dieser Prozedur liegt auf dem Ausführen eines Entnahme-Kanban-Einzelvorgangs, um Material zu übertragen. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Diese Prozedur ist für Lagerarbeitskräfte vorgesehen.


## <a name="display-transfer-jobs"></a>Umlagerungseinzelvorgänge anzeigen
1. Wechseln Sie zu "Produktionssteuerung" > "Kanban" >"Kanban-Übersicht für Umlagerungseinzelvorgänge".
2. Erweitern oder reduzieren Sie den Abschnitt ''Filter".
    * Im Abschnitt "Filter" können Sie angeben, welche Einzelvorgänge Sie anzeigen möchten, indem Sie nach Produktionsfluss, Name der Aktivität, Von-Lagerort und Ort sowie An-Lagerort und Ort filtern.  
3. Geben Sie im Feld "Von Lagerort" "11" ein.
4. Geben Sie im Feld "An Lagerplatz" "12" ein.

## <a name="start-a-transfer-job"></a>Umlagerungseinzelvorgang starten
1. Deaktivieren Sie ggf. die ausgewählte Zeile in der Liste.
2. Wählen Sie in der Liste die Zeile "4" aus.
    * Wählen Sie den ersten Einzelvorgang mit dem Status "Nicht geplant" aus. Stellen Sie sicher, dass dies der einzige ausgewählte Einzelvorgang ist.  
3. Klicken Sie auf "Start".
    * Beachten Sie, dass ein Symbol anzeigt, dass der Einzelvorgang gestartet wurde.  

## <a name="select-a-second-transfer-job-and-change-quantity"></a>Wählen Sie einen zweiten Umlagerungseinzelvorgang aus und ändern Sie die Menge
1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Sie können mehrere Einzelvorgänge ausgewählt haben, wählen Sie hier jedoch Zeile 5 aus.  
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Stellen Sie sicher, dass der Einzelvorgang im vorherigen Schritt der einzige ausgewählte Einzelvorgang ist. Heben Sie die Auswahl anderer Einzelvorgänge auf.  
3. Notieren Sie sich den Wert im Feld "Einzelvorgangsmenge" für Ihre Unterlagen
4. Legen Sie "Einzelvorgangsmenge" auf "30" fest.
    * Beachten Sie die Warnung! Sie sind nicht zulässig, 30 zu übertragen. Entsprechend den Einstellungen der Kanban-Regel, können Sie nur die ursprüngliche Menge übertragen.  
5. Den zuvor im Feld "Einzelvorgangsmenge" notierten Wert verwenden
    * Legen Sie die Einzelvorgangsmenge auf den vorherigen Wert fest.  

## <a name="start-the-second-transfer-job"></a>Starten Sie den zweiten Umlagerungseinzelvorgang
1. Klicken Sie auf "Start".
    * Dadurch beginnt die Übertragung des Einzelvorgangs in Zeile 5.  

## <a name="complete-both-transfer-jobs"></a>Schließen Sie beide Umlagerungseinzelvorgänge ab
1. Wählen Sie in der Liste die Zeile "4" aus.
    * Es sind jetzt zwei Umlagerungseinzelvorgänge in Zeile 4 und Zeile 5 ausgewählt.  
2. Klicken Sie auf "Abgeschlossen".
    * Dadurch wird die Übertragung beider Einzelvorgänge abgeschlossen.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]