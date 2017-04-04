---
title: "Workflowsystemüberblick"
description: "In diesem Artikel wird beschrieben des Workflowsystems in Microsoft Dynamics 365 für Arbeitsgänge."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 08c36f02f88fef7508730b6c01a1c99a0f77fb0c
ms.lasthandoff: 03/31/2017


---

# <a name="workflow-system-overview"></a>Workflowsystemüberblick

In diesem Artikel wird beschrieben des Workflowsystems in Microsoft Dynamics 365 für Arbeitsgänge.

<a name="what-is-workflow"></a>Was ist ein Arbeitsplan?
-----------------

Der Begriff *Workflow* kann auf zwei Arten definiert werden: als System und als Geschäftsprozess.
### <a name="workflow-is-a-system"></a>Workflow als System

Der Workflow ist ein System, das mit 365 Dynamics für Arbeitsgänge eingerichtet wird und das auf dem Anwendungsobjektserver (AOS) ausgeführt wird. Das Workflowsystem verfügt über Funktionen, die zum Erstellen einzelner Workflows oder Geschäftsprozesse verwendet werden können.

### <a name="workflow-is-a-business-process"></a>Workflow als Geschäftsprozess

Ein Workflow stellt einen Geschäftsprozess dar. Ein Workflow definiert, wie ein Dokument das System durchläuft, indem angezeigt wird, wer eine Aufgabe abschließen, eine Entscheidung treffen oder ein Dokument genehmigen muss. Die folgende Abbildung zeigt z. B. einen Workflow für Spesenabrechnungen. ![Workflow mit Elementen, die Benutzern zugewiesen sind](./media/workflow_user.gif) Um diesen Workflow besser zu verstehen, gehen wir davon aus, dass Sam einen Ausgabenbericht für 7.000 EUR sendet. In diesem Szenario muss Joachim die Belege prüfen, die Steffen an ihn weiterleitet. Anschließend muss die Spesenabrechnung von Frank und Saskia genehmigt werden. Nehmen wir nun an, Steffen reicht eine Spesenabrechnung in Höhe von 11.000 Euro ein. In diesem Szenario muss Joachim die Belege prüfen, und Frank, Saskia und Anne müssen die Spesenabrechnung genehmigen.
Vorteile des Workflowsystems
-------------------------------------

Die Verwendung des Workflowsystems in der Organisation verspricht mehrere Vorteile:
-   **Konsistente Prozesse** – Sie können die Verarbeitung bestimmter Dokumente definieren, z. B. von Bestellanforderungen und Spesenabrechnungen. Das Workflowsystem gewährleistet, dass Dokumente konsistent und effizient verarbeitet und genehmigt werden.
-   **Prozesssichtbarkeit** – Sie können den Status, die Historie und die Leistungskennzahlen von Workflowinstanzen nachverfolgen. So können Sie besser feststellen, ob zur Effizienzsteigerung Änderungen am Workflow vorgenommen werden sollten.
-   **Zentralisierte Arbeitsliste** – Benutzer können eine zentralisierte Arbeitsliste öffnen, um die ihnen zugeordneten Workflowaufgaben und -genehmigungen anzuzeigen.




