---
title: Sie können das Dropdown-Dialogfeld „Workflow“ für Bestandserfassungen nicht finden.
description: Sie können das Dropdown-Dialogfeld „Workflow“ auf der Erfassungsseite nicht finden oder zugehörige Workflowvorgänge sind nicht verfügbar.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b2772a75c2388f4d78a459f9dfb72ad7c1be4ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476426"
---
# <a name="you-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>Sie können das Dropdown-Dialogfeld „Workflow“ für Bestandserfassungen nicht finden.

## <a name="symptoms"></a>Symptome

Sie können das Dropdown-Dialogfeld **Workflow** auf der Erfassungsseite nicht finden oder zugehörige Workflowvorgänge sind nicht verfügbar.

Dieses Problem kann aus drei Gründen auftreten, wie in den folgenden Abschnitten beschrieben.

## <a name="resolution-1"></a>Lösung 1

Wenn das Problem für alle Benutzer gilt, kann es auftreten, weil der Genehmigungsworkflow nicht dem Erfassungsnamen zugewiesen wurde. Führen Sie folgende Schritte aus, um das Problem zu beheben.

1. Wechseln Sie zu **Bestandsverwaltung &gt; Einrichten &gt; Erfassungsnamen &gt; Bestand**.
1. Wählen Sie im Listenbereich einen Erfassungsnamen aus, um seine Einstellungen zu öffnen.
1. Legen Sie im Inforegister **Allgemein** die Option **Genehmigungsworkflow** auf *Ja* fest. Wählen Sie **Ja** aus, wenn Sie zum Bestätigen der Änderung aufgefordert werden.
1. Wählen Sie im Feld **Workflow** den Workflow aus, den Sie für den ausgewählten Erfassungsnamen verwenden möchten.

## <a name="resolution-2"></a>Lösung 2

Wenn Ihr Workflow benutzerdefinierten Code verwendet, können nach dem Upgrade des Systems Probleme auftreten. Im Erfassungsworkflow wird beispielsweise eventuell die Schaltläche **Übermitteln** ausgegraut, sodass Sie sie nicht auswählen können, um eine Übermittlung zu genehmigen.

Wenn die Schaltfläche **Übermitteln** ausgegraut ist, wurde möglicherweise Ihr Workflow angepasst. Das bedeutet, dass die Methode des Workflows, `canSubmitToWorkflow()` in `FormDataUtil`, erweitert wurde. Um dieses Problem zu beheben, ändern Sie die Art und Weise, auf die Sie die Methode von `canSubmitToWorkflow()` erweitern, indem Sie die Struktur im folgenden Beispiel verwenden.

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

## <a name="resolution-3"></a>Lösung 3

Wenn das Problem nur für einige bestimmte Benutzer gilt, verfügen diese Benutzer möglicherweise nicht über die Sicherheitsrechte, die zum Ausführen von Workflowvorgängen für Bestandserfassungen erforderlich sind. Stellen Sie sicher, dass jeder betroffene Benutzer über das Sicherheitsrecht *Workflow zur Bestandserfassung pflegen* verfügt. Standardmäßig wird dieses Recht einer Pflicht mit demselben Namen zugewiesen und diese Pflicht wird auf die Rollen *Lagerortarbeitskraft* und *Lagerortleiter* angewendet.
