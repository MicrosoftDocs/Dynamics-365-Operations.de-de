---
title: Kanban-Bearbeitungseinzelvorgänge durchführen
description: Diese Prozedur konzentriert sich auf das Ausführen von Kanban-Bearbeitungs-Einzelvorgängen.
author: ChristianRytt
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
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1c32b577007c400f3528a110436eb97aaabefe2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207024"
---
# <a name="execute-kanban-process-jobs"></a>Kanban-Bearbeitungseinzelvorgänge durchführen

[!include [banner](../../includes/banner.md)]

Diese Prozedur konzentriert sich auf das Ausführen von Kanban-Bearbeitungs-Einzelvorgängen. Der erste Einzelvorgang wird mit der erwarteten Menge abgeschlossen und enthält keine Fehler. Der zweite Einzelvorgang wird mit Fehlern abgeschlossen. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Diese Prozedur ist für den Maschinenbediener vorgesehen.


## <a name="select-a-kanban-job"></a>Wählen Sie einen Kanban-Einzelvorgang aus
1. Wechseln Sie zu "Produktionssteuerung" > "Kanban" > "Kanban-Übersicht für Prozesseinzelvorgänge".
2. Klicken Sie im Feld "Arbeitsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Klicken Sie auf die Zeile mit Ressourcengruppe 1250. Dies filtert die Liste "Einzelvorgänge", sodass nur die Einzelvorgänge für Arbeitsgruppe 1250 angezeigt werden.
    * Markieren Sie die Zeile, die den Status "Geplanter Einzelvorgang" aufweist.  

## <a name="complete-a-job-with-expected-quantity"></a>Schließen Sie einen Einzelvorgang mit erwarteter Menge ab
1. Erweitern oder reduzieren Sie den Abschnitt "Details".
    * Dieser Abschnitt zeigt wichtige Informationen zu Kartennummer, Artikelnummer, bestellter Menge und Aktivitätsname an.  
2. Erweitern oder reduzieren Sie den Abschnitt "Produktionsanweisungen".
    * In diesem Abschnitt werden Produktionsanweisungen für die Aktivität angezeigt. Die Anweisungen können Text, Bilder, Zeichnungen und andere Dokumente sein.  
3. Klicken Sie auf "Start".
    * Wählen Sie einen Einzelvorgang aus, die nicht abgeschlossen ist. Verwenden Sie Statussymbole im Feld "Einzelvorgangsstatus", um Einzelvorgangsstatus anzuzeigen.      
4. Klicken Sie auf "Abgeschlossen".
    * Der Einzelvorgang wird mit der erwarteten Qualität abgeschlossen.  

## <a name="complete-a-job-with-errors"></a>Schließen Sie einen Einzelvorgang mit Fehlern ab
1. Klicken Sie auf "Start".
    * Wenn ein Einzelvorgang abgeschlossen ist, wird der nächste Einzelvorgang in der Liste automatisch ausgewählt. Daher müssen Sie keinen Einzelvorgang auswählen, bevor Sie auf "Start" klicken.  
2. Klicken Sie im Aktivitätsbereich auf "Fertigung".
3. Klicken Sie auf "Abschließen (Details)".
4. Markieren Sie in der Liste die ausgewählte Zeile.
5. Geben Sie im Feld "Fehlermenge" eine Zahl ein.
6. Geben Sie im Feld "Gutmenge" eine Zahl ein.
7. Klicken Sie auf "OK".

