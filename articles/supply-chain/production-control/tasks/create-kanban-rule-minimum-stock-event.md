--- 
title: Eine Kanban-Regel mithilfe eines Mindestbestandsereignisses erstellen
description: "Diese Prozedur konzentriert sich auf die Einstellungen, die benötigt werden, um eine Kanban-Regel unter Verwendung eines Mindestbestandsereignisses zu erstellen, um zu garantieren, dass ein spezifisches Produkt immer an einem spezifischen Lagerplatz verfügbar ist."
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
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
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: c655f9e2cb3967a44c357f16d18884ec0bc55357
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# Eine Kanban-Regel mithilfe eines Mindestbestandsereignisses erstellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur konzentriert sich auf die Einstellungen, die benötigt werden, um eine Kanban-Regel unter Verwendung eines Mindestbestandsereignisses zu erstellen, um zu garantieren, dass ein spezifisches Produkt immer an einem spezifischen Lagerplatz verfügbar ist. Eine Kanban-Regel wird erstellt, um Material zum Lagerplatz zu übertragen, wenn das Bestandsniveau unterhalb von 200 Stücke fällt. Durch das Ausführen der Verarbeitung des bedarfsverursachenden Ereignisses werden die erforderlichen Kanbans erstellt. Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF. Diese Aufgabe ist für den Fertigungsplaner oder den Wertstrom-Manager vorgesehen, da diese die Produktion eines neuen oder geänderten Produkts in einer schlanken Umgebung vorbereiten.


## Neue Kanban-Regel erstellen
1. Wechseln Sie zu "Produktinformationsverwaltung" > "Lean Manufacturing" > "Kanban-Regeln".
2. Klicken Sie auf "Neu".
3. Wählen Sie im Feld "Typ" die Option "Entnahme" aus.
    * Dieser Typ wird verwendet, um Kanban-Umlagerungen zu erstellen.  
4. Wählen Sie im Feld "Auffüllungsstrategie" "Ereignis" aus.
    * Die "Ereignisstrategie" wird verwendet, um die Kanban-Umlagerungen auf Grundlage eines Ereignisses zu erstellen. Später in dieser Prozedur lösen Sie Kanban-Umlagerungen mithilfe der Bestandswiederbeschaffung aus.  
5. Geben Sie im Feld "Erste Planaktivität" einen Wert ein oder wählen Sie einen Wert aus.
    * Geben Sie "ReplenishSpeakerComponents" ein oder wählen Sie es aus. Diese Umlagerungsaktivität hat Zugangs- (Ausgangs-)Lagerort und Lagerplatz 12. Das bedeutet, dass Materialien zu Lagerplatz 12 in Lagerort 12 verschoben werden.  
6. Erweitern Sie den Abschnitt "Details".
7. Geben Sie im Feld "Produkt" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie M0007 aus.  
8. Erweitern Sie den Abschnitt "Ereignis".
9. Wählen Sie im Feld "Bestandswiederbeschaffungsereignis" die Option "Charge" aus.
    * Dies erstellt Kanbans, um Materialbedarf am verknüpften Lagerplatz während der "Verarbeitung von bedarfsverursachenden Ereignissen" zu erfüllen.  

## Die Mindestmenge für den Artikel festlegen
1. Klicken Sie, um dem Link im Feld "Produkt" zu folgen.
2. Klicken Sie, um dem Link im Feld "Artikelnummer" zu folgen.
3. Erweitern Sie die Infobox "Produktbild".
4. Klicken Sie im Aktivitätsbereich auf "Plan".
5. Klicken Sie auf "Artikeldeckung".
6. Klicken Sie auf "Neu".
7. Markieren Sie in der Liste die ausgewählte Zeile.
8. Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.
    * Legen Sie den "Lagerort" auf 12 fest.  
9. Legen Sie das Minimum auf "200" fest.

## Stapelereignis-Erstellungseinzelvorgang ausführen
1. Wechseln Sie zu "Produktionssteuerung" > "Periodisches Aufgaben" > "Kanban-Einzelvorgangs-Stapelverarbeitung" > "Verarbeitung des bedarfsverursachenden Ereignisses".
2. Klicken Sie auf "OK".
3. Wechseln Sie zu "Produktinformationsverwaltung" > "Lean Manufacturing" > "Kanban-Regeln".
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Wählen Sie die Kanban-Regel aus, die Sie zuvor erstellt haben.  
5. Erweitern Sie den Abschnitt "Kanbans".
    * Beachten Sie, dass ein Kanban erstellt wurde, um das erforderliche Material an Lagerort 12 zu übertragen.  


