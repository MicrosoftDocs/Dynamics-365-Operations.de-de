---
title: "Überblick über das Workflowsystem"
description: In diesem Thema wird das Workflowsystem in Microsoft Dynamics 365 for Operations beschrieben.
author: sericks007
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 142f6f122172f717733db6f39b964c3f6f2e2f77
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="workflow-system-overview"></a>Überblick über das Workflowsystem

[!include[banner](../includes/banner.md)]


In diesem Thema wird das Workflowsystem in Microsoft Dynamics 365 for Operations beschrieben.

<a name="what-is-workflow"></a>Was ist ein Arbeitsplan?
-----------------

Der Begriff *Workflow* kann auf zwei Arten definiert werden: als System und als Geschäftsprozess.
### <a name="workflow-is-a-system"></a>Workflow als System

Workflow ist ein System, das mit Microsoft Dynamics 365 for Operations installiert wird und auf dem Anwendungsobjektserver (AOS/Application Object Server) ausgeführt wird. Das Workflowsystem verfügt über Funktionen, die zum Erstellen einzelner Workflows oder Geschäftsprozesse verwendet werden können.

### <a name="workflow-is-a-business-process"></a>Workflow als Geschäftsprozess

Ein Workflow stellt einen Geschäftsprozess dar. Ein Workflow definiert, wie ein Dokument das System durchläuft, indem angezeigt wird, wer eine Aufgabe abschließen, eine Entscheidung treffen oder ein Dokument genehmigen muss. Die folgende Abbildung zeigt z. B. einen Workflow für Spesenabrechnungen. 

![Workflow mit Elementen, die Benutzern zugewiesen sind](./media/workflow_user.gif) 

Beispiel zum besseren Verständnis dieses Workflows: Steffen reicht eine Spesenabrechnung in Höhe von 7.000 Euro ein. In diesem Szenario muss Joachim die Belege prüfen, die Steffen an ihn weiterleitet. Anschließend muss die Spesenabrechnung von Frank und Saskia genehmigt werden. Nehmen wir nun an, Steffen reicht eine Spesenabrechnung in Höhe von 11.000 Euro ein. In diesem Szenario muss Joachim die Belege prüfen, und Frank, Saskia und Anne müssen die Spesenabrechnung genehmigen.

## <a name="benefits-of-using-the-workflow-system"></a>Vorteile des Workflowsystems

Die Verwendung des Workflowsystems in der Organisation verspricht mehrere Vorteile:
-   **Konsistente Prozesse** – Sie können die Verarbeitung bestimmter Dokumente definieren, z. B. von Bestellanforderungen und Spesenabrechnungen. Das Workflowsystem gewährleistet, dass Dokumente konsistent und effizient verarbeitet und genehmigt werden.
-   **Prozesssichtbarkeit** – Sie können den Status, die Historie und die Leistungskennzahlen von Workflowinstanzen nachverfolgen. So können Sie besser feststellen, ob zur Effizienzsteigerung Änderungen am Workflow vorgenommen werden sollten.
-   **Zentralisierte Arbeitsliste** – Benutzer können eine zentralisierte Arbeitsliste öffnen, um die ihnen zugeordneten Workflowaufgaben und -genehmigungen anzuzeigen.


## <a name="workflow-content"></a>Workflowinhalt

+ [Workflowarchitektur](workflow-system-architecture.md)
+ [Workflowelemente](workflow-elements.md)
+ [Workflowaktivitäten](workflow-actions.md)
+ [Erstellen eines Workflows](create-workflow.md)
+ [Konfigurieren von Workfloweigenschaften](configure-workflow-properties.md)
+ [Konfigurieren einer manuellen Entscheidung in einem Workflow](configure-manual-task-workflow.md)
+ [Konfigurieren einer automatisierten Aufgabe in einem Workflow](configure-automated-task-workflow.md)
+ [Einen Genehmigungsschritt in einem Workflow konfirgurieren](configure-approval-process-workflow.md)
+ [Einen Genehmigungsschritt in einem Workflow genehmigen](configure-approval-step-workflow.md)
+ [Konfigurieren einer manuellen Entscheidung in einem Workflow](configure-manual-decision-workflow.md)
+ [Konfigurieren einer bedingten Entscheidung in einem Workflow](configure-conditional-decision-workflow.md)
+ [Konfigurieren einer parallelen Aktivität in einem Workflow](configure-parallel-activity-workflow.md)
+ [Konfigurieren eines Parallelzweigs in einem Workflow](configure-parallel-branch-workflow.md)
+ [Konfigurieren eines Positionsworkflows](configure-line-item-workflow.md)

