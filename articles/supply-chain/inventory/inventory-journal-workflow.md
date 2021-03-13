---
title: Workflows für die Genehmigung von Bestandserfassungen
description: In diesem Thema wird beschrieben, wie Sie Workflows für die Genehmigung von Bestandserfassungen für verschiedene Typen von physischen Bestandsbuchungen einrichten und verwenden, Bestandserfassungs-Workflows stellen sicher, dass nur genehmigte Bestandserfassungen in Buchungen gebucht werden können.
author: sherry-zheng
manager: tfehr
ms.date: 07/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTableWorkflowDropDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-21
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: d9f57d35adac0820d0635ab97a4cb4cefc1d504c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011671"
---
# <a name="inventory-journal-approval-workflows"></a>Workflows für die Genehmigung von Bestandserfassungen

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Workflows für die Genehmigung von Bestandserfassungen für verschiedene Typen von physischen Bestandsbuchungen einrichten und verwenden, zum Beispiel für Zugänge und Abgänge, Bestandsumlagerungen, die Erstellung von Stücklisten (BOMs) und zur Abstimmung des physischen Bestands. Bestandserfassungs-Workflows stellen sicher, dass nur genehmigte Bestandserfassungen in Buchungen gebucht werden können.

> [!NOTE]
> Workflows für die Genehmigung von Bestandserfassungen gelten nur für Buchungen, die mit dem Modul Bestandsverwaltung erfasst wurden. Sie funktionieren nicht mit Bestandserfassungen, die vom Modul Lagerortverwaltung ausgelöst werden.

## <a name="turn-on-the-inventory-journal-approval-workflows-feature"></a>Funktion für Workflows zur Genehmigung von Lagererfassungen aktivieren

Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Modul:** *Bestands- und Lagerortverwaltung*
- **Funktionsname:** *Workflow für die Genehmigung von Bestandserfassungen*

## <a name="create-your-inventory-journal-approval-workflows"></a>Workflows für die Genehmigung von Bestandserfassungen anlegen

Um diese Funktion einzurichten, müssen Sie einen Workflow für jeden Bestandserfassungstyp erstellen, den Sie steuern möchten. Da verschiedene Bestandserfassungstypen unterschiedliche Genehmigungshierarchien und Workflowschritte haben können, können Sie für jeden Bestandserfassungstyp individuelle Workflows konfigurieren.

Workflows unterstützen die Versionskontrolle und haben jeweils eine Workflow-ID und eine aktive Version. Sie können wählen, ob jede neue Workflow-Version sofort nach der Erstellung aktiviert werden oder inaktiv bleiben soll. Wenn Sie unterschiedliche Workflows für denselben Erfassungstyp benötigen, erstellen Sie mehrere Workflows für diese Erfassungstyp und weisen Sie diesen jeweils einem anderen Erfassungsnamen zu, der diesen Typ verwendet.

Legen Sie Workflows für die Genehmigung von Bestandserfassungen wie folgt an:

1. Gehen Sie zu **Bestandsverwaltung \> Einrichten\> Bestandsverwaltungs-Workflows**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Wählen Sie den Bestandserfassungstyp aus, für den Sie einen Workflow einrichten möchten:
    - **Erfassung der Markierungsinventur**
    - **Erfassung für die Änderung von Bestandseigentümern**
    - **Lagerbestands-Umlagerungserfassung**
    - **Lagerbestandsübertragungs-Erfassung**
    - **Lagerinventurerfassung**
    - **Bestandsstücklistenerfassung**
    - **Lagerregulierungserfassung**

    ![Das Dialogfeld „Workflow erstellen“](media/journal-workflow-create-workflow.png "Das Dialogfeld „Workflow erstellen“")

1. Die Workflow-Editor-App wird auf Ihrem Computer gestartet. (Möglicherweise werden Sie aufgefordert, diese Aktion zu genehmigen.) Verwenden Sie den Editor, um Ihren Workflow nach Bedarf zu gestalten. Ausführliche Informationen zur Verwendung des Workflow-Editors finden Sie unter [Workflowsystem – Übersicht](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).
1. Nach dem Speichern und Schließen der Workflow-Editor-App müssen Sie auswählen, ob diese Workflow-Version aktiviert werden oder inaktiv bleiben soll.

> [!NOTE]
> Workflows bieten eine Versionskontrolle. Dies bedeutet, dass Sie eine Liste der von Ihnen erstellten Versionen anzeigen lassen und auswählen können, welche aktiv ist. Um die Liste der verfügbaren Versionen anzuzeigen und auszuwählen, welche aktiviert werden sollen, wählen Sie einen Workflow aus der Liste auf der Seite **Bestandsverwaltungs-Workflows**. Öffnen Sie im Aktionsbereich die Registerkarte **Workflow** und wählen Sie **Versionen**. Für jede Workflow-ID kann jeweils nur eine Version aktiv sein.

## <a name="assign-approval-workflows-to-inventory-journal-names"></a>Bestandserfassungsnamen Genehmigungsworkflows zuweisen

Im nächsten Schritt weisen Sie jedem Bestandserfassungsnamen einen Bestandserfassungsworkflow zu. Sie können für jeden Bestandserfassungsstyp mehrere Bestandserfassungsnamen einrichten.

Um einem Bestandserfassungsworkflow einen Bestandserfassungsnamen zuzuweisen, gehen Sie wie folgt vor:

1. Gehen Sie zu **Bestandsverwaltung \> Einrichten \> Erfassungsnamen \> Bestand**.
1. Wählen Sie einen Erfassungsnamen aus der Listenspalte aus, um die Einstellungsseite zu öffnen.
1. Auf dem Inforegister **Allgemein** stellen Sie die Option **Genehmigungsworkflow** auf **Ja**. Klicken Sie auf **Ja**, wenn Sie zum Bestätigen Ihrer Auswahl aufgefordert werden.

    ![Einem Erfassungsnamen einen Workflow zuweisen](media/journal-workflow-journal-name.png "Einem Erfassungsnamen einen Workflow zuweisen")

1. Öffnen Sie die **Workflow**-Drop-down-Liste und wählen Sie den gewünschten Workflow aus. Die Liste zeigt alle aktiven Workflows, die Sie mit der Workflow-Editor-App erstellt haben.

## <a name="create-an-inventory-journal-and-send-it-for-approval"></a>Eine Bestandserfassung anlegen und zur Genehmigung senden

Nachdem Sie einen Bestandserfassungsnamen mit dem entsprechenden Workflow für die Genehmigung von Bestandserfassungen verknüpft haben, können Sie neue Bestandserfassungen erstellen, die diesen Namen verwenden, und diese Erfassungen dann mithilfe dieses Workflows zur Genehmigung senden. Sie können die Bestandserfassung erst dann veröffentlichen, wenn der im Workflow festgelegte Genehmiger sie genehmigt hat.

1. Erweitern Sie im Navigationsbereich **Bestandsverwaltung \> Erfassungseinträge \> Artikel** und wählen Sie dann einen Bestandserfassungstyp aus.
1. Wählen Sie **Neu**, um eine neue Erfassung des ausgewählten Typs zu erstellen.
1. Das Dialogfeld **Bestandserfassung erstellen** öffnet sich. Füllen Sie das Formular wie gewünscht aus und wählen Sie **OK**, um die Erfassung zu speichern.
1. Füllen Sie die Erfassung wie erforderlich aus.
1. Wenn Sie eine Bestandserfassung mit einem damit verbundenen Genehmigungsworkflow erstellen oder öffnen, wird die Schaltfläche **Workflow** im Aktionsbereich aktiviert. Wenn Sie bereit sind, die Erfassung zur Genehmigung einzureichen, wählen Sie die Schaltfläche **Workflow**, um ein Drop-down-Dialogfeld zu öffnen, und wählen Sie dann **Übermitteln**. Die Genehmigungsanforderung wird dann an den entsprechenden Genehmiger weitergeleitet, der mithilfe der für den Workflow konfigurierten Methode benachrichtigt wird.

    ![Eine Erfassung zur Genehmigung übermitteln](media/journal-workflow-inventory-journal.png "Eine Erfassung zur Genehmigung übermitteln")

Um eine Genehmigungsanforderung zurückzurufen, öffnen Sie die entsprechende Erfassung und wählen Sie die Schaltfläche **Workflow** und dann **Zurückrufen**. Dadurch wird der Workflow zurückgesetzt.

Wenn Ihre Erfassung genehmigt wurde, können Sie sie veröffentlichen. Um die Erfassung zu veröffentlichen, wählen Sie **Veröffentlichen** aus dem Aktionsbereich. Wenn die Schaltfläche **Veröffentlichen** nicht aktiv ist, wurde die Erfassung noch nicht genehmigt.

## <a name="respond-to-an-inventory-journal-approval-request"></a>Eine Genehmigungsanforderung für eine Bestandserfassung beantworten

Als Genehmiger sollten Sie jedes Mal eine Nachricht erhalten, wenn Ihre Genehmigung erforderlich ist (wie im entsprechenden Workflow konfiguriert). Sie können eine Erfassungsgenehmigungsanforderung wie folgt genehmigen oder ablehnen:

1. Erweitern Sie im Navigationsbereich **Bestandsverwaltung \> Erfassungseinträge \> Artikel** und wählen Sie dann einen Bestandserfassungstyp aus.
1. Öffnen Sie die entsprechende Erfassung und überprüfen Sie sie.
1. Wählen Sie die Schaltfläche **Workflow** im Aktionsbereich, um ein Drop-down-Dialogfeld zu öffnen. Wählen Sie eine der folgenden Optionen:
    - **Genehmigen**, um die Anforderung zu genehmigen.
    - **Ablehnen**, um die Anforderung abzulehnen.
    - **Mehr \> Änderung anfordern**, um eine Nachricht an die anfordernde Person zu senden und sie zu bitten, etwas Bestimmtes zu ändern und die Anforderung dann erneut zu übermitteln.
    - **Mehr \> Delegieren**, um die Genehmigung an einen anderen Benutzer zu delegieren.
    - **Mehr \> Zurückrufen**, um die Genehmigungsanforderung zurückzurufen (setzt den Workflow zurück).
    - **Mehr \> Workflowhistorie**, um den bisherigen Verlauf dieses Genehmigungsworkflows anzuzeigen.

## <a name="review-the-approval-history"></a>Die Genehmigungshistorie überprüfen

Wie bei anderen Workflowtypen können Sie die Seite **Workflowhistorie** nutzen, um die Genehmigungsworkflowhistorie für eine Erfassung anzuzeigen.

So überprüfen Sie die Workflowhistorie für eine Erfassung:

1. Erweitern Sie im Navigationsbereich **Bestandsverwaltung \> Erfassungseinträge \> Artikel** und wählen Sie dann einen Bestandserfassungstyp aus.
1. Öffnen Sie die relevante Erfassung.
1. Wählen Sie die Schaltfläche **Workflow** im Aktionsbereich, um ein Drop-down-Dialogfeld zu öffnen. Wählen Sie **Workflowhistorie**. Weitere Informationen finden Sie unter [Workflowhistorie anzeigen](../../fin-ops-core/fin-ops/organization-administration/tasks/view-workflow-history.md).
