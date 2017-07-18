---
title: Workflowelemente
description: Dieser Artikel beschreibt die verschiedenen Elemente, die einen Workflow darstellen.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a3a12080efcb138365c26981abd51222c51663ff
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017

---

# <a name="workflow-elements"></a>Workflowelemente

[!include[banner](../includes/banner.md)]


Dieser Artikel beschreibt die verschiedenen Elemente, die einen Workflow darstellen.

Ein Workflow besteht aus Elementen. In den folgenden Abschnitten wird jeder Elementtyp beschrieben.

## <a name="tasks"></a>Aufgaben
Bei einer *Aufgabe* handelt es sich um eine auszuführende Arbeitseinheit. Es können zwei Arten von Aufgaben zu einem Workflow hinzugefügt werden: manuelle Aufgaben und automatisierte Aufgaben.

### <a name="manual-task"></a>Manuelle Aufgabe

Bei einer *manuellen Aufgabe* handelt es sich um eine Arbeitseinheit, die von einem Benutzer auszuführen ist. Beispielsweise beinhaltet ein Workflow für Spesenabrechnungen manuelle Aufgaben, die von den zugewiesenen Benutzern folgende Aktionen erfordern:

-   Prüfen der zusammen mit einer Spesenabrechnung eingereichten Belege.
-   Anrufen des Vorgesetzten eines Mitarbeiters.

### <a name="automated-task"></a>Automatisierte Aufgabe

Bei einer *automatisierten Aufgabe* handelt es sich um eine Arbeitseinheit, die vom System auszuführen ist. Es sind keine manuellen Benutzeraktivitäten erforderlich. Beispielsweise beinhaltet ein Workflow für Aufträge automatisierte Aufgaben, die vom System folgende Aktionen erfordern:

-   Ausführen einer Kreditprüfung.
-   Erstellen eines Debitorendatensatzes für den Debitor, sofern noch nicht vorhanden.

## <a name="approval-processes"></a>Genehmigungsprozesse
Bei einem *Genehmigungsprozess* handelt es sich um einen Prozess, der aus getrennten Schritten besteht. Bei jedem Genehmigungsschritt kann der Benutzer die folgenden Aktivitäten ausführen:

-   Dient zum Genehmigen des Dokuments.
-   Dient zum Ablehnen des Dokuments.
-   eine Änderung am Dokument anzufordern,
-   Dokument einem anderen Benutzer zur Genehmigung zuweisen.

## <a name="lineitem-workflow-elements"></a>Lineitem-Workflow-Elemente
Ein Workflow kann zum Verarbeiten von Dokumenten oder der Positionen in einem Dokument erstellt werden. Angenommen, Sie haben einen Genehmigungsworkflow für Arbeitszeitnachweise erstellt. (Wir bezeichnen diesen Workflow als *Dokumentworkflow*.) Sie können ein *Positionsworkflow*-Element zu diesem Dokumentworkflow hinzufügen. Bei der Ausführung des Positionselements wird jede Position im Dokument zur Verarbeitung übermittelt. Dabei können alle Positionen durch denselben Positionsworkflow oder jede Position durch einen anderen Positionsworkflow verarbeitet werden. Angenommen, ein Mitarbeiter hat einen Arbeitszeitnachweis übermittelt, der der folgenden Abbildung ähnelt. ![Workflow mit Positionen](./media/workflow_lineitemworkflow.gif) In diesem Szenario sollten Sie die folgenden Positionsworkflows erstellen:

-   **Positionsworkflow 1** – Dieser Workflow wird zum Verarbeiten von Positionen mit Projektkennung 1111 verwendet.
-   **Positionsworkflow 2** – Dieser Workflow wird zum Verarbeiten von Positionen mit Projektkennung 2222 verwendet.
-   **Positionsworkflow 3** – Dieser Workflow wird zum Verarbeiten von Positionen mit Projektkennung 3333 verwendet.

## <a name="flowcontrol-elements"></a>Flowcontrol-Elemente
Mithilfe der folgenden Elemente können Sie Workflows mit alternativen Verzweigungen oder gleichzeitig ausgeführten Verzweigungen entwerfen.

### <a name="manual-decision"></a>Manuelle Entscheidung

Eine *manuelle Entscheidung* ist ein Punkt, an dem sich ein Workflow verzweigt. Ein Benutzer muss eine Entscheidung treffen, und diese Entscheidung bestimmt, welche Verzweigung zum Verarbeiten des übermittelten Dokuments verwendet wird.

### <a name="conditional-decision"></a>Bedingte Entscheidung

Eine *bedingte Entscheidung* ist ein Punkt, an dem sich ein Workflow verzweigt. Das System entscheidet jedoch, welcher Zweig zum Verarbeiten des übermittelten Dokuments verwendet wird. Um diese Entscheidung zu treffen, wertet das System das Dokument aus, um zu bestimmen, ob es den angegebenen Bedingungen entspricht.

### <a name="parallel-activity"></a>Parallele Aktivität

Eine *parallele Aktivität* ist ein Workflowelement, das zwei oder mehr Workflowverzweigungen enthält, die gleichzeitig ausgeführt werden.

### <a name="subworkflow"></a>Untergeordneter Workflow

Ein *untergeordneter Workflow* ist ein Workflow, der im Kontext eines anderen Workflows ausgeführt wird.




