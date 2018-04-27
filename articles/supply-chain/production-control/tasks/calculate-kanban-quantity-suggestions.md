--- 
title: "Kanban-Mengenvorschläge berechnen"
description: "Der Schwerpunkt dieser Prozedur liegt auf dem Optimieren der Kanban-Größe und -Menge für eine bestimmte Kanban-Regel mit der Kanban-Mengenberechnung."
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
ms.openlocfilehash: a817dbc02890d863f68c5bf2a6cc11b9a5328060
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="calculate-kanban-quantity-suggestions"></a>Kanban-Mengenvorschläge berechnen

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Der Schwerpunkt dieser Prozedur liegt auf dem Optimieren der Kanban-Größe und -Menge für eine bestimmte Kanban-Regel mit der Kanban-Mengenberechnung. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Diese Vorgehensweise ist für den Wertstrommanager vorgesehen. Für dieses Verfahren wird vorausgesetzt, dass Sie die Prozedur "Kanban-Berechnungsrichtlinie zur Kanban-Regel hinzufügen" abgeschlossen haben.


## <a name="create-a-kanban-quantity-calculation"></a>Kanban-Mengenberechnung erstellen
1. Wechseln Sie zu "Produktionssteuerung" > "Periodische Aufgaben" > "Kanban-Mengenberechnung" > "Kanban-Menge berechnen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Name" "Speaker2016" ein.
4. Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Wählen Sie die Richtlinie aus, die Sie in der Prozedur "Kanban-Berechnungsrichtlinie zur Kanban-Regel hinzufügen" erstellt haben. Beispielsweise "Speaker2016".  
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Legen Sie im Feld "Stichdatum zur Auswahl von Kanban-Regeln" Datum und Uhrzeit auf "2012-12-17T08:00:00" fest.
    * Anhand dieses Datums wird ermittelt, welche festen Kanban-Regeln in die Kanban-Mengenberechnung einbezogen werden.  
7. Legen Sie im Feld "Gedeckter Bedarf - Periodenstartdatum" Datum und Uhrzeit auf "2012-11-17T09:00:00" fest.
    * Das Datum, ab dem Buchungen in Bezug auf den Bedarf in der Vergangenheit in die Kanban-Mengenberechnung einbezogen werden.  
8. Legen Sie im Feld "Gedeckter Bedarf - Periodenenddatum" Datum und Uhrzeit auf "2012-12-17T07:59:59" fest.
    * Das Datum, bis zu dem Buchungen in Bezug auf den Bedarf in der Vergangenheit in die Kanban-Mengenberechnung einbezogen werden.  
9. Legen Sie im Feld "Bedarf - Periodenstartdatum" Datum und Uhrzeit auf "2012-12-17T08:00:00" fest.
    * Das Datum, ab dem Buchungen in Bezug auf den aktuellen Bedarf in die Kanban-Mengenberechnung einbezogen werden.  
10. Legen Sie im Feld "Bedarf - Periodenenddatum" Datum und Uhrzeit auf "2013-01-16T07:59:59" fest.
    * Das Datum, bis zu dem Buchungen in Bezug auf den aktuellen Bedarf in die Kanban-Mengenberechnung einbezogen werden.  

## <a name="generate-kanban-quantity-proposal"></a>Kanban-Mengenvorschlag generieren
1. Klicken Sie auf "Speichern".
2. Klicken Sie "Generieren".
    * Dadurch wird eine Kanban-Mengenvorschlagsposition für die Kanban-Regel 000020 generiert.  

## <a name="run-kanban-quantity-calculation"></a>Kanban-Mengenberechnung ausführen
1. Klicken Sie auf "Berechnen".
    * Dies berechnet den Kanban-Mengenvorschlag.  
2. Klicken Sie auf "OK".
3. Markieren Sie in der Liste die ausgewählte Zeile.
    * Beachten Sie, dass vorgeschlagene Kanban-Menge 2 ist.  

## <a name="change-product-quantity-and-calculate-again"></a>Produktmenge ändern und erneut berechnen
1. Legen Sie "Produktmenge" auf '5' fest.
2. Klicken Sie auf "Berechnen".
3. Klicken Sie auf "OK".
    * Beachten Sie, dass bei einer Kanban-Menge von 5, der Vorschlag zu einer Kanban-Menge von 4 geändert wird.  
    * Dies wird durch dadurch verursacht, dass mit einer niedrigeren Produktmenge, mehr Kanbans erforderlich sind, um den Bedarf zu decken.  

## <a name="update-kanban-rule"></a>Kanban-Regel aktualisieren
1. Geben Sie im Feld "Gültigkeitsdatum der Regeln" ein Datum und eine Uhrzeit ein.
    * Legen Sie die "Datum, ab dem die Regel aktiv wird" auf ein Datum in der Zukunft fest. Beispielsweise heute + ein Jahr.  
2. Klicken Sie auf Aktualisieren.
3. Klicken Sie auf "OK".
4. Schließen Sie die Seite.

## <a name="validate-change-on-kanban-rule"></a>Änderung der Kanban-Regel überprüfen
1. Wechseln Sie zu "Produktinformationsverwaltung" > "Lean Manufacturing" > "Kanban-Regeln".
2. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Wählen Sie die Kanban-Regel aus, die in der vorherigen Unteraufgabe erstellt wurde. Diese sollte die erste Kanban-Regel in der nach Nummern sortierten Liste sein.  
3. Schalten Sie die Erweiterung des Abschnitts "Details" ein/aus.
    * Beachten Sie das Gültigkeitsdatum, das anzeigt, dass diese Regel bis zu diesem Datum nicht aktiviert ist.  
4. Schalten Sie die Erweiterung des Abschnitts "Mengen" ein/aus.
    * Beachten Sie, dass dies die Standardmenge ist, die Sie in der Kanban-Mengenberechnung eingegeben haben.  
    * Beachten Sie, dass dies die feste Kanban-Menge von 4 aus der Kanban-Mengenberechnung ist.  
5. Klicken Sie auf die Registerkarte "ListPanel".


