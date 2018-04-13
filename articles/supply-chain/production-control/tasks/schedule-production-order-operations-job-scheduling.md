--- 
title: "Einen Produktionsauftrag mit Vorgängen und Feinterminierung planen"
description: Dieses Verfahren konzentriert sich auf die Planung eines Fertigungsauftrags mit Grobterminierung und Feinterminierung.
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
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
ms.openlocfilehash: d4aac437876862e9f776264fc81f246c820bdf45
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Einen Produktionsauftrag mit Vorgängen und Feinterminierung planen

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren konzentriert sich auf die Planung eines Fertigungsauftrags mit Grobterminierung und Feinterminierung. Es werden keine Einzelvorgänge mit Grobterminierung erstellt. Es werden jedoch Einzelvorgänge mit Feinterminierung erstellt. Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF. Dieses Verfahren ist für Produktionsleiter, Produktionsplaner oder Werkstattleiter gedacht, die in einer Einzelfertigungsumgebung arbeiten.


## <a name="create-a-production-order"></a>Produktionsauftrag erstellen
1. Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".
2. Klicken Sie auf "Neuer Produktionsauftrag".
3. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie Artikelnummer D0001 aus.  
4. Klicken Sie auf "Erstellen".

## <a name="schedule-operations-for-the-production-order"></a>Planen von Vorgängen für den Produktionsauftrag
1. Markieren Sie in der Liste die ausgewählte Zeile.
    * Wählen Sie den soeben erstellten Produktionsauftrag aus. Er sollte am Anfang der Liste stehen.      
2. Klicken Sie im Aktivitätsbereich auf "Zeitplan".
3. Klicken Sie auf "Arbeitsgänge planen".
4. Wählen Sie im Feld Planungsrichtung "Vorwärts ab Planungsdatum" aus.
5. Geben Sie ein Datum in das Feld "Planungsdatum" ein.
    * Wählen Sie ein zukünftiges Datum (beispielsweise heute plus eine Woche). Mit der ausgewählten Planungsrichtung wird der Produktionsauftrag vorwärts ab diesem Datum geplant.  
6. Klicken Sie auf "OK".
7. Markieren Sie in der Liste die ausgewählte Zeile.
    * Beachten Sie, dass sich der Status in "Geplant" ändert.  
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
9. Klicken Sie auf "Alle Einzelvorgänge".
    * Beachten Sie, dass keine Aufträge mit geplanten Vorgängen erstellt werden.  
10. Schließen Sie die Seite.

## <a name="schedule-jobs-for-the-production-order"></a>Planen von Einzelvorgängen für den Produktionsauftrag
1. Klicken Sie im Aktivitätsbereich auf "Zeitplan".
2. Klicken Sie auf Einzelvorgänge planen.
3. Wählen Sie im Feld Planungsrichtung "Vorwärts ab Planungsdatum" aus.
4. Geben Sie ein Datum in das Feld "Planungsdatum" ein.
    * Wählen Sie ein zukünftiges Datum (beispielsweise heute plus eine Woche). Mit der ausgewählten Planungsrichtung wird der Produktionsauftrag vorwärts ab diesem Datum geplant.  
5. Klicken Sie auf "OK".
6. Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".
7. Klicken Sie auf "Alle Einzelvorgänge".
    * Beachten Sie, dass (basieren auf der aktiven Route) 5 neue Einzelaufträge mit Feinterminierung erstellt werden.  


