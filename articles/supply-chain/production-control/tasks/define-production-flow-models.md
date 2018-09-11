--- 
title: Produktionsflussmodelle definieren
description: "Produktionsflussmodelle beschreiben, wie die Kapazität von Lean Manufacturing-Arbeitsgruppen berechnet und gepflegt wird."
author: cvocph
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlowModel
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7850a121ca06f25f6c532e49e18c0b6811bd7455
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="define-production-flow-models"></a>Produktionsflussmodelle definieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Produktionsflussmodelle beschreiben, wie die Kapazität von Lean Manufacturing-Arbeitsgruppen berechnet und gepflegt wird. Daher ist die Definition eines Produktionsflussmodells eine Voraussetzung für die Definition der Arbeitsgruppen. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="define-a-production-flow-model"></a>Definieren Sie ein Produktionsflussmodell. 
1. Wechseln Sie zu Produktionssteuerung > Einrichten > Lean-Produktionsfluss > Produktionsflussmodelle.
2. Klicken Sie auf "Neu".
3. Wählen Sie im Feld "Produktionsflussmodell" eine Kennung für das Produktionsflussmodell.
4. Wählen Sie im Feld "Modell" eine Option aus.
    * Es gibt zwei Modelltypen: Durchsatz und Stunden. Für "Durchsatz" wird die Kapazität von Arbeitsgruppen verwendet und berechnet, die dieses Produktionsflussmodell verwenden. Für "Stunden" wird die Kapazität von Arbeitsgruppen in Stunden verwendet und berechnet, die dieses Produktionsflussmodell verwenden. Beachten Sie, dass diese Eigenschaft nicht für ein vorhandenes Produktionsflussmodell geändert werden kann. Nachdem eine Arbeitsgruppe Kapazitätsreservierungen hat, kann der Produktionsflussmodelltyp nicht geändert werden.  
5. Geben Sie die Anzahl von Tagen in das Feld "EPE-Zyklus" ein.
    * Das Intervall beschreibt die Periode, in jeder Teil, der von einem Produktionsfluss oder von einer Arbeitsgruppe produziert wird, mindestens einmal produziert wird. Je kürzer der EPE-Zyklus, desto flexibler ist der Produktionsprozess. Wenn der EPE-Zyklus gleich 0 ist, kann der gesamte Bedarf am selben Tag produziert werden. Der EPE-Zyklus wird verwendet, um Leanproduktions-Einzelvorgänge zu planen. Wenn Sie einen Einzelvorgang in einer Arbeitsgruppe mit EPE-Zyklus = 5 planen, sucht der Planungsvorgang nach einer Kapazität der Arbeitsgruppe mit dem Fälligkeitsdatum - EPE-Zyklus (5 Tage nach dem aktuellen Datum), um sicherzustellen dass das Produkt in diesem Zyklus produziert werden kann. Die Lagerlieferzeit eines Produkts ist normalerweise größer oder gleich dem EPE-Zyklus des zugehörigen Produktionsprozesses.  
6. Wählen Sie im Feld "Planungsperiodentyp" eine Option aus.
    * Nachdem eine Arbeitsgruppe Kapazitätsreservierungen hat, kann der Planungsperiodentyp nicht geändert werden. Sie können nur Produktionsflussmodelle mit demselben Periodentyp für diese Arbeitsgruppe auswählen.  
7. Geben Sie im Feld "Planungszeitraum" eine Zahl ein.
    * Der Planungszeitraum beschreibt die Anzahl von Tagen, innerhalb derer Kapazitätsreservierungen für die zugehörigen Arbeitsgruppen vorgenommen werden können. Geben Sie im Feld Planungszeitraum die Anzahl der Tage ein.   Kanban-Bearbeitungseinzelvorgänge, die außerhalb dieser Periode liegen, werden nicht mit der automatischen Planung geplant. Der Planungszeitraum ist normalerweise das Zweifache der durchschnittlichen Lagerlieferzeit der in einem Produktionsfluss oder in einer Arbeitsgruppe produzierten Produkte. Der EPE-Zyklus sollte nicht mehr als Hälfte des Planungszeitraums betragen.     
8. Wählen Sie im Feld "Reaktion auf Kapazitätsmangel" eine Option aus.
    * Die Optionen umfassen: "Termin verschieben" - Verschieben des vollständigen Bedarfs des Planungsereignisses auf den nächsten verfügbaren Produktionstag mit verfügbarem Durchsatz. Abbrechen - Beenden der automatischen Planung für das Planungsereignis und belassen der zugehörigen Einzelvorgänge als ungeplant.   Zum angeforderten Tag hinzufügen - Planen der angeforderten Einzelvorgänge für die gewünschte Periode. Dieses überlädt die Zelle für diesen Tag und erfordert vom Planer eine Überprüfung und eine manuelle Interaktion.   Verteilen verfügbarer Perioden - Verteilt die verschiedenen Einzelvorgänge des Planungsereignisses von verfügbaren Produktionstagen ab dem ersten verfügbaren Tag. Die Mindestverteilungsmenge ist die Menge des Kanban-Einzelvorgangs. Die Verteilung weist die minimale Planungsmenge (Kanban-Menge) zu jedem Tag mit genügendem verfügbaren Durchsatz zu.  


