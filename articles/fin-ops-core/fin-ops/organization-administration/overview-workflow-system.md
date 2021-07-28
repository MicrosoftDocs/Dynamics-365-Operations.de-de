---
title: Workflowsystem – Übersicht
description: In diesem Thema wird das Workflowsystem beschrieben.
author: ChrisGarty
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom:
- "56381"
- intro-internal
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc73f1bde3407c144dc1cd48283385c19713430e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349083"
---
# <a name="workflow-system-overview"></a>Workflowsystem – Übersicht

[!include [banner](../includes/banner.md)]

In diesem Thema wird das Workflowsystem beschrieben.

## <a name="what-is-workflow"></a>Was ist ein Arbeitsplan?

Der Begriff *Workflow* kann auf zwei Arten definiert werden: als System und als Geschäftsprozess.

### <a name="workflow-is-a-system"></a>Workflow als System

Der Workflow ist ein System, das auf dem Anwendungsobjektserver (AOS) ausgeführt wird. Das Workflowsystem verfügt über Funktionen, die zum Erstellen einzelner Workflows oder Geschäftsprozesse verwendet werden können.

### <a name="workflow-is-a-business-process"></a>Workflow als Geschäftsprozess

Ein Workflow stellt einen Geschäftsprozess dar. Ein Workflow definiert, wie ein Dokument das System durchläuft, indem angezeigt wird, wer eine Aufgabe abschließen, eine Entscheidung treffen oder ein Dokument genehmigen muss. Die folgende Abbildung zeigt z. B. einen Workflow für Spesenabrechnungen.

![Workflow mit Elementen, die Benutzern zugewiesen sind.](./media/workflow_user.gif)

Beispiel zum besseren Verständnis dieses Workflows: Steffen reicht eine Spesenabrechnung in Höhe von 7.000 Euro ein. In diesem Szenario muss Joachim die Belege prüfen, die Steffen an ihn weiterleitet. Anschließend muss die Spesenabrechnung von Frank und Saskia genehmigt werden. Nehmen wir nun an, Steffen reicht eine Spesenabrechnung in Höhe von 11.000 Euro ein. In diesem Szenario muss Joachim die Belege prüfen, und Frank, Saskia und Anne müssen die Spesenabrechnung genehmigen.

## <a name="benefits-of-using-the-workflow-system"></a>Vorteile des Workflowsystems

Die Verwendung des Workflowsystems in der Organisation verspricht mehrere Vorteile:

- **Konsistente Prozesse** – Sie können die Verarbeitung bestimmter Dokumente definieren, z. B. von Bestellanforderungen und Spesenabrechnungen. Das Workflowsystem gewährleistet, dass Dokumente konsistent und effizient verarbeitet und genehmigt werden.
- **Prozesssichtbarkeit** – Sie können den Status, die Historie und die Leistungskennzahlen von Workflowinstanzen nachverfolgen. So können Sie besser feststellen, ob zur Effizienzsteigerung Änderungen am Workflow vorgenommen werden sollten.
- **Zentralisierte Arbeitsliste** – Benutzer können eine zentralisierte Arbeitsliste öffnen, um die ihnen zugeordneten Workflowaufgaben und -genehmigungen anzuzeigen.


## <a name="workflow-content"></a>Workflowinhalt

+ [Workflow-Systemarchitektur](workflow-system-architecture.md)
+ [Workflow-Elemente](workflow-elements.md)
+ [Aktivitäten in Workflow-Genehmigungsprozessen](workflow-actions.md)
+ [Erstellen von Workflows – Übersicht](create-workflow.md)
+ [Konfigurieren von Workflow-Eigenschaften](configure-workflow-properties.md)
+ [Manuelle Aufgaben in einem Workflow konfigurieren](configure-manual-task-workflow.md)
+ [Konfigurieren von automatisierten Aufgaben in einem Workflow](configure-automated-task-workflow.md)
+ [Genehmigungsprozesse in einem Workflow konfigurieren](configure-approval-process-workflow.md)
+ [Genehmigungsschritte in einem Workflow konfigurieren](configure-approval-step-workflow.md)
+ [Manuellen Entscheidungen in einem Workflow konfigurieren](configure-manual-decision-workflow.md)
+ [Konfigurieren von bedingten Entscheidungen in einem Workflow](configure-conditional-decision-workflow.md)
+ [Konfigurieren paralleler Aktivitäten in einem Workflow](configure-parallel-activity-workflow.md)
+ [Konfigurieren paralleler Verzweigungen in einem Workflow](configure-parallel-branch-workflow.md)
+ [Konfigurieren von Positionsworkflows](configure-line-item-workflow.md)
+ [Workflow-FAQs](workflow-FAQ.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]