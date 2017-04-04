---
title: "Datenzuteilung für die Budgetplanung"
description: "In diesem Artikel wird beschrieben die verschiedene Zuordnungsmethoden, die in Microsoft Dynamics 365 für Arbeitsgänge sind verfügbar und wie sie verwendet werden können."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: f717e9de361b5511ac4af360cddb1ea16ad4a1e2
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-data-allocation"></a>Datenzuteilung für die Budgetplanung

In diesem Artikel wird beschrieben die verschiedene Zuordnungsmethoden, die in Microsoft Dynamics 365 für Arbeitsgänge sind verfügbar und wie sie verwendet werden können.  

Sie können die Daten in einem Budgetplan auf vielfältige Weise verteilen, um die geplanten Beträge genau zu darzustellen.

## <a name="allocation-methods"></a>Zuweisungsmethoden
Drei Zuordnungsmethoden (Auf Perioden verteilen, Zu Dimensionen zuordnen und Sachkonto-Zuordnungsregeln verwenden) können Budgetplanpositionen erstellen, die auf den Positionen im gleichen Budgetplan basieren. Drei andere Methoden (Zusammenführen, Verteilen und Aus Budgetplan kopieren), können Budgetplanpositionen in anderen Budgetplänen erstellen. Für alle sechs Zuordnungsmethoden geben Sie das Zielszenario an. Das Zielszenario kann entweder dem Quellszenario gleichen oder sich davon sich unterscheiden. Darüber hinaus können Sie angeben, ob dem Haushaltsplan neue Positionen angehängt oder die aktuellen Positionen im Budgetplan ersetzt werden.

![AllocateAcrossPeriods ([]. /media/allocateacrossperiods-300x259.png)]". /media/allocateacrossperiods.png"
** Ablehnen periodenübergreifend zu ** – eine Perioden-Zuweisungskategorie wird verwendet, um die Budgetplanpositionen vom Quellbudgetplanszenario periodenübergreifend im Zielszenario zuzuweisen. Der Quellbetrag wird mehreren Positionen im Zielszenario basierend auf dem Prozentsatz und dem Datum zugewiesen, die in der Periodenzuteilungskategorie definiert werden.         

[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Zu Dimensionen zuordnen** - die Budgetplanpositionen werden vom Quellbudgetplanungsszenario an einen oder mehrere Positionen im Zielszenario auf Grundlage der Prozentsätze und der Finanzdimensionen zugeordnet, die in einer ausgewählten Bedingung für Budgetzuteilung definiert werden.           

![AggregateChart](./media/aggregatechart-300x230.png)
**Zusammenführen** - Die Budgetplanpositionen werden aus dem Quellbudgetplanszenario in zugeordneten (untergeordneten) Budgetplänen auf das Zielszenario in den übergeordneten Budgetplan verteilt. Diese Methode erlaubt Budgetbeträge, die auf einer niedrigeren Ebene in der Organisation vorbereitet werden, auf einer höheren Ebene zu konsolidierenden.          

[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Verteilen** - Die Budgetplanpositionen werden vom Quellbudgetplanungsszenario im übergeordneten Budgetplan dem Zielszenario in den zugehörigen (untergeordneten)Budgetplänen auf Grundlage die Finanzdimensionen der Organisationseinheiten der zugeordneten Pläne verteilt. Diese Methode erlaubt Budgetbeträge, die auf einer höheren Ebene in der Organisation vorbereitet werden, für eine örtlichere Überprüfung auszubreiten.           

[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Sachkonto-Zuordnungsregeln verwenden** - Die Budgetplanpositionen werden vom Quellbudgetplanungsszenario auf Grundlage der ausgewählten Sachkonto-Zuordnungsregel auf das Zielbudgetplanszenario verteilt. 

[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Kopie des Haushaltsplans** - Wie bei der Verteilungszuordnungsmethode, Budgetplanpositionen werden im Ziel, auf Grundlage der Positionen in einem dazugehörigen Budgetplan erstellt. Für diese Methode muss der Quellbudgetplan nicht der übergeordnete Plan sein, kann jedoch auf jeder höheren Ebene in der Budgetplanhierarchie stehen. Diese Zuordnungsmethode ist hilfreich, wenn konsolidierte Beträge ursprünglich auf einer viel höheren Ebene geplant werden, und muss einer untergeordneten Ebene der Organisation für detaillierten Prüfung und Regulierung übertragen werden, bevor sie höhere Genehmigung erhalten können.          

## <a name="using-allocation-methods-in-a-budget-plan"></a>Verwenden der Zuordnungsmethoden in einem Budgetplan
Um Zuweisungen auf der Budgetplanseite auszuführen, wählen Sie die zuzuweisenden Positionen aus, und klicken Sie anschließend auf **Budget zuteilen**.

![AllocateBudgetButton ([]. /media/allocatebudgetbutton-300x84.png)]". /media/allocatebudgetbutton.png) 

Als Wählen Sie anschließend eine Zuordnungsmethode aus. Die übrigen Felder werden dann auf Grundlage der Methode festgelegt, die Sie ausgewählt haben. Diese Felder enthalten die Quelle und das Ziel der Budgetplandaten und eine Option, mit der Sie die Quelle durch einen angegebenen Faktor multiplizieren können, wenn die Zielbeträge erstellt werden, um die Massenregulierung zu vereinfachen. Sie können auch die Option **An Plan anheften** festlegen. Wählen Sie **Nein** aus, um die vorhandenen Budgetplanpositionen zu ersetzen, oder **Ja**, um die vorhandenen Budgetplanpositionen zu verwalten und neue Positionen für die zugeteilten Beträge hinzuzufügen.

## <a name="automating-allocations-during-a-workflow"></a>Automatisieren von Zuweisungen während eines Workflows
Eine leistungsfähige Funktion ermöglicht es Zuweisungen als Teil eines Budgetplanungsworkflows automatisch ausführen zu lassen. Während ein Budgetplan den Workflow durchläuft, können automatisierte Aufgaben eine Zuteilung in einem angegebenen Budgetplanungsstadium aufrufen. 

Um die automatisierte Zuweisung einrichten, müssen Sie auf der Seite **Budgetplanungskonfiguration** zunächst einen Zuteilungszeitplan erstellen. Der Zuteilungszeitplan definiert die Zuteilungsmethode, die verwendet wird, wenn die automatisierte Zuteilung ausgeführt wird, und die Werte der verschiedenen Zuteilungsoptionen (Informationen dazu finden Sie im vorherigen Abschnitt zu Beschreibungen). 

Anschließend erstellen Sie eine Phasenzuteilung auf der Seite **Budgetplanungskonfiguration**. Die Phasenzuteilung weist einen Zuteilungsplan dem Budgetplanungsworkflow und der -phase zu. 

Schließlich fügen Sie in dem gewünschten Workflowstadium eine automatisierte Aufgabe für Budgetplanungsphasenzuteilung hinzu. Im folgenden Beispiel wurden zwei Budgetplanungsphasenzuteilungen (in rot umrissen) in den Workflow eingefügt.

![BudgetPlanningStageAllocations ([]. /media/budgetplanningstageallocations-300x300.png)]". /media/budgetplanningstageallocations.png)


