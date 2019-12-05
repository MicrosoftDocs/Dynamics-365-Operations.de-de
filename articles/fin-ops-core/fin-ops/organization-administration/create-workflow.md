---
title: Erstellen von Workflows – Übersicht
description: Dieses Thema erläutert, wie Sie einen Workflow erstellen.
author: sericks007
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
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
ms.openlocfilehash: a643be553f3fcdfbe53f2024982a596e498830a8
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811289"
---
# <a name="create-workflows-overview"></a>Erstellen von Workflows – Übersicht

[!include [banner](../includes/banner.md)]

Dieses Thema erläutert, wie Sie einen Workflow erstellen.

## <a name="open-the-workflow-editor"></a>Öffnen des Workflow-Editors

Das Modul, in dem Sie arbeiten, bestimmt die Workflowtypen, die Sie erstellen können. Gehen Sie folgendermaßen vor, um den Workflowtyp zum Erstellen und Öffnen des Workflow-Editors auszuwählen.

1. Öffnen Sie das Modul, für das Sie einen neuen Workflow erstellen möchten. Sie können beispielsweise einen Workflow für Bestellanforderungen erstellen. Klicken Sie dazu auf **Beschaffung**.
2. Klicken Sie auf **Einrichten** &gt; **\[Modulname\] Workflows**.
3. Klicken Sie auf der Listenseite im Aktivitätsbereich auf der Registerkarte auf **Neu**.
4. Wählen Sie auf der Seite **Workflow erstellen** den Typ des Workflows aus, den Sie erstellen möchten und klicken Sie dann **Workflow erstellen**. Der Workflow-Editor wird angezeigt. Verwenden Sie jetzt die folgenden Verfahren zum Entwerfen des Workflows.

## <a name="drag-workflow-elements-onto-the-canvas"></a>Ziehen von Workflowelementen auf die Canvas

Der Bereich **Workflow-Elemente** des Workflow-Editors enthält die Elemente, die Sie dem Workflow hinzufügen können. Um dem Workflow Elemente hinzuzufügen, ziehen Sie die Elemente aus dem Bereich auf die Canvas.

## <a name="connect-the-elements"></a>Verbinden der Elemente

Wenn Sie ein Workflowelement mit einem anderen verbinden möchten, halten Sie den Zeiger über ein Element, bis Verbindungspunkte angezeigt werden. Klicken Sie auf einen Verbindungspunkt, und ziehen Sie ihn zum anderen Element. Stellen Sie sicher, dass Sie alle Elemente verbinden.

## <a name="configure-the-properties-of-the-workflow"></a>Konfigurieren der Eigenschaften des Workflows

Gehen Sie folgendermaßen vor, um die Eigenschaften des Workflows zu konfigurieren.

1. Klicken Sie auf die Canvas, um sicherzustellen, dass kein Workflowelement ausgewählt ist.
2. Klicken Sie auf **Eigenschaften** **, um die Seite** Eigenschaften für den Workflow zu öffnen.
3. Folgen Sie den Schritten des Verfahrens unter [Konfigurieren von Workfloweigenschaften](configure-workflow-properties.md).

## <a name="configure-the-elements-of-the-workflow"></a>Konfigurieren der Elemente des Workflows

Konfigurieren Sie jedes auf die Canvas gezogene Element. Informationen zum Konfigurieren jedes Workflowelements finden Sie unter folgenden Themen:

- [Manuelle Aufgaben in einem Workflow konfigurieren](configure-manual-task-workflow.md)
- [Konfigurieren von automatisierten Aufgaben in einem Workflow](configure-automated-task-workflow.md)
- [Genehmigungsprozesse in einem Workflow konfigurieren](configure-approval-process-workflow.md)
- [Genehmigungsschritte in einem Workflow konfigurieren](configure-approval-step-workflow.md)
- [Manuellen Entscheidungen in einem Workflow konfigurieren](configure-manual-decision-workflow.md)
- [Konfigurieren von bedingten Entscheidungen in einem Workflow](configure-conditional-decision-workflow.md)
- [Konfigurieren paralleler Verzweigungen in einem Workflow](configure-parallel-activity-workflow.md)
- [Konfigurieren eines Parallelzweigs](configure-parallel-branch-workflow.md)
- [Konfigurieren von Positionsworkflows](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>Beheben von Fehlern oder Warnungen

Im Bereich **Fehler und Warnungen** im unteren Bereich des Workflow-Editors werden für den Workflow generierte Meldungen angezeigt. Doppelklicken Sie auf die Fehler- oder Warnmeldung, um das Element zu suchen, in dem ein Fehler oder eine Warnung auftritt. Bevor der Workflow aktiviert werden kann, müssen alle Fehler und Warnungen behoben sein.

## <a name="save-and-activate-the-workflow"></a>Speichern und Aktivieren des Workflows

Führen Sie zum Speichern und Aktivieren des Workflows die folgenden Schritte aus.

1. Klicken Sie auf **Speichern und schließen**, um den Workflow-Editor zu schließen und die Seite **Workflow speichern** zu öffnen.
2. Geben Sie Kommentare zu den Änderungen am Workflow ein und klicken Sie auf **OK**.
3. Wenn alle Fehler und Warnungen behoben wurden, wird die Seite **Workflow aktivieren** angezeigt. Folgende Optionen stehen zur Auswahl:

    - Klicken Sie zum Aktivieren dieser Version des Workflows auf **Neue Version aktivieren**. Wenn ein Workflow aktiv ist, können Benutzer Dokumente zwecks Verarbeitung übermitteln.
    - Wenn diese Version nicht aktiviert werden soll, klicken Sie **Neue Version nicht aktivieren** an. Der Workflow kann auch später aktiviert werden.
