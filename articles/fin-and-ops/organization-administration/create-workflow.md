---
title: Erstellen eines Workflows
description: "Dieses Thema erläutert, wie Sie einen Workflow erstellen."
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ee3f60575d0eaaf56ce08adb1936728a76488dac
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="create-a-workflow"></a>Erstellen eines Workflows

[!INCLUDE [banner](../includes/banner.md)]

Dieses Thema erläutert, wie Sie einen Workflow erstellen.

<a name="open-the-workflow-editor"></a>Öffnen des Workflow-Editors
------------------------

Das Microsoft Dynamics 365 for Finance and Operations-Modul, in dem Sie arbeiten, bestimmt die Workflowtypen, die Sie erstellen können. Gehen Sie folgendermaßen vor, um den Workflowtyp zum Erstellen und Öffnen des Workflow-Editors auszuwählen.

1.  Öffnen Sie das Modul, für das Sie einen neuen Workflow erstellen möchten. Sie können beispielsweise einen Workflow für Bestellanforderungen erstellen. Klicken Sie dazu auf **Beschaffung**.
2.  Klicken Sie auf **Einrichten** &gt; **\[Modulname\] Workflows**.
3.  Klicken Sie auf der Listenseite im Aktivitätsbereich auf der Registerkarte auf **Neu**.
4.  Wählen Sie auf der Seite **Workflow erstellen** den Typ des Workflows aus, den Sie erstellen möchten und klicken Sie dann **Workflow erstellen**. Der Workflow-Editor wird angezeigt. Verwenden Sie jetzt die folgenden Verfahren zum Entwerfen des Workflows.

## <a name="drag-workflow-elements-onto-the-canvas"></a>Ziehen von Workflowelementen auf die Canvas
Der Bereich **Workflow-Elemente** des Workflow-Editors enthält die Elemente, die Sie dem Workflow hinzufügen können. Um dem Workflow Elemente hinzuzufügen, ziehen Sie die Elemente aus dem Bereich auf die Canvas.

## <a name="connect-the-elements"></a>Verbinden der Elemente
Wenn Sie ein Workflowelement mit einem anderen verbinden möchten, halten Sie den Zeiger über ein Element, bis Verbindungspunkte angezeigt werden. Klicken Sie auf einen Verbindungspunkt, und ziehen Sie ihn zum anderen Element. Stellen Sie sicher, dass Sie alle Elemente verbinden.

## <a name="configure-the-properties-of-the-workflow"></a>Konfigurieren der Eigenschaften des Workflows
Gehen Sie folgendermaßen vor, um die Eigenschaften des Workflows zu konfigurieren.

1.  Klicken Sie auf die Canvas, um sicherzustellen, dass kein Workflowelement ausgewählt ist.
2.  Klicken Sie auf **Eigenschaften****, um die Seite** Eigenschaften für den Workflow zu öffnen.
3.  Folgen Sie der Prozedur unter [Eigenschaften für einen Workflow konfigurieren](configure-workflow-properties.md).

## <a name="configure-the-elements-of-the-workflow"></a>Konfigurieren der Elemente des Workflows
Konfigurieren Sie jedes auf die Canvas gezogene Element. Informationen zum Konfigurieren jedes Workflowelements finden Sie unter folgenden Themen:

-   [Konfigurieren einer manuellen Aufgabe](configure-manual-task-workflow.md)
-   [Konfigurieren einer automatisierten Aufgabe](configure-automated-task-workflow.md)
-   [Konfigurieren eines Genehmigungsprozesses](configure-approval-process-workflow.md)
-   [Konfigurieren eines Genehmigungsschritts](configure-approval-step-workflow.md)
-   [Konfigurieren einer manuellen Entscheidung](configure-manual-decision-workflow.md)
-   [Konfigurieren einer bedingten Entscheidung](configure-conditional-decision-workflow.md)
-   [Konfigurieren einer parallelen Aktivität](configure-parallel-activity-workflow.md)
-   [Konfigurieren eines Parallelzweigs](configure-parallel-branch-workflow.md)
-   [Konfigurieren eines Positionsworkflows](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>Beheben von Fehlern oder Warnungen
Im Bereich **Fehler und Warnungen** im unteren Bereich des Workflow-Editors werden für den Workflow generierte Meldungen angezeigt. Doppelklicken Sie auf die Fehler- oder Warnmeldung, um das Element zu suchen, in dem ein Fehler oder eine Warnung auftritt. Bevor der Workflow aktiviert werden kann, müssen alle Fehler und Warnungen behoben sein.

## <a name="save-and-activate-the-workflow"></a>Speichern und Aktivieren des Workflows
Führen Sie zum Speichern und Aktivieren des Workflows die folgenden Schritte aus.

1.  Klicken Sie auf **Speichern und schließen**, um den Workflow-Editor zu schließen und die Seite **Workflow speichern** zu öffnen.
2.  Geben Sie Kommentare zu den Änderungen am Workflow ein und klicken Sie auf **OK**.
3.  Wenn alle Fehler und Warnungen behoben wurden, wird die Seite **Workflow aktivieren** angezeigt. Folgende Optionen stehen zur Auswahl:
    -   Klicken Sie zum Aktivieren dieser Version des Workflows auf **Neue Version aktivieren**. Wenn ein Workflow aktiv ist, können Benutzer Dokumente zwecks Verarbeitung übermitteln.
    -   Wenn diese Version nicht aktiviert werden soll, klicken Sie **Neue Version nicht aktivieren** an. Der Workflow kann auch später aktiviert werden.






