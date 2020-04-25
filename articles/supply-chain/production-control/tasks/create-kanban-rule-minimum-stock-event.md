---
title: Eine Kanban-Regel mithilfe eines Mindestbestandsereignisses erstellen
description: Diese Prozedur konzentriert sich auf die Einstellungen, die benötigt werden, um eine Kanban-Regel unter Verwendung eines Mindestbestandsereignisses zu erstellen, um zu garantieren, dass ein spezifisches Produkt immer an einem spezifischen Lagerplatz verfügbar ist.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b295000e132b8551045520df1af55a37673f131d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212249"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a>Eine Kanban-Regel mithilfe eines Mindestbestandsereignisses erstellen

[!include [banner](../../includes/banner.md)]

Diese Prozedur konzentriert sich auf die Einstellungen, die benötigt werden, um eine Kanban-Regel unter Verwendung eines Mindestbestandsereignisses zu erstellen, um zu garantieren, dass ein spezifisches Produkt immer an einem spezifischen Lagerplatz verfügbar ist. Eine Kanban-Regel wird erstellt, um Material zum Lagerplatz zu übertragen, wenn das Bestandsniveau unterhalb von 200 Stücke fällt. Durch das Ausführen der Verarbeitung des bedarfsverursachenden Ereignisses werden die erforderlichen Kanbans erstellt. Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF. Diese Aufgabe ist für den Fertigungsplaner oder den Wertstrom-Manager vorgesehen, da diese die Produktion eines neuen oder geänderten Produkts in einer schlanken Umgebung vorbereiten.


## <a name="create-a-new-kanban-rule"></a>Neue Kanban-Regel erstellen
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

## <a name="set-the-minimum-quantity-for-the-item"></a>Die Mindestmenge für den Artikel festlegen
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

## <a name="run-the-batch-event-creation-job"></a>Stapelereignis-Erstellungseinzelvorgang ausführen
1. Wechseln Sie zu "Produktionssteuerung" > "Periodisches Aufgaben" > "Kanban-Einzelvorgangs-Stapelverarbeitung" > "Verarbeitung des bedarfsverursachenden Ereignisses".
2. Klicken Sie auf "OK".
3. Wechseln Sie zu "Produktinformationsverwaltung" > "Lean Manufacturing" > "Kanban-Regeln".
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Wählen Sie die Kanban-Regel aus, die Sie zuvor erstellt haben.  
5. Erweitern Sie den Abschnitt "Kanbans".
    * Beachten Sie, dass ein Kanban erstellt wurde, um das erforderliche Material an Lagerort 12 zu übertragen.  

