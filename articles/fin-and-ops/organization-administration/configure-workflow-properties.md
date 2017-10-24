---
title: Konfigurieren der Eigenschaften eines Workflows
description: "Dieses Thema erläutert, wie Sie die verschiedenen Eigenschaften eines Workflows konfigurieren können."
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
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6cad67d4108a81de545a1e633dc4e12a31af683b
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="configure-the-properties-of-a-workflow"></a>Konfigurieren der Eigenschaften eines Workflows

[!include[banner](../includes/banner.md)]


Dieses Thema erläutert, wie Sie die verschiedenen Eigenschaften eines Workflows konfigurieren können.

Öffnen Sie zum Konfigurieren der Eigenschaften eines Workflows den Workflow im Workflow-Editor. Klicken Sie auf die Canvas des Workflow-Editors und dann auf **Eigenschaften**, um die Seite **Eigenschaften** zu öffnen. Verwenden Sie dann die folgenden Prozeduren, um die verschiedenen Eigenschaften des Workflows zu konfigurieren.

## <a name="name-the-workflow"></a>Benennen des Workflows
Gehen Sie folgendermaßen vor, um einen Namen für den Workflow einzugeben.

1.  Klicken Sie im linken Bereich auf **Grundeinstellungen**.
2.  Geben Sie im Feld **Name** einen eindeutigen Namen für den Workflow ein. Wenn Sie für jedes Land bzw. jede Region, in dem/der Sie tätig sind, Workflows für Bestellanforderungen erstellen, kann der jeweilige Workflow beispielsweise **Bestellanforderungen Dänemark** oder **Bestellanforderungen Spanien** benannt werden.

## <a name="specify-the-workflow-owner"></a>Angeben des Workfloweigentümers
Der Workfloweigentümer ist die Person, die den Workflow verwaltet. Gehen Sie folgendermaßen vor, um den Workfloweigentümer anzugeben.

1.  Klicken Sie im linken Bereich auf **Grundeinstellungen**.
2.  Wählen Sie in der Liste **Eigentümer** den Namen der Person aus, die diesen Workflow verwalten soll.

## <a name="select-an-email-template"></a>Auswählen einer E-Mail-Vorlage
Gehen Sie folgendermaßen vor, um die E-Mail-Vorlage auszuwählen, die zum Generieren von Benachrichtigungsmeldungen zu diesem Workflow verwendet wird.

1.  Klicken Sie im linken Bereich auf **Grundeinstellungen**.
2.  Wählen Sie in der Liste **E-Mail-Vorlagen für Workflowbenachrichtigungen** die Vorlage aus.

## <a name="enter-instructions-for-users"></a>Eingeben von Anweisungen für Benutzer
Sie können Benutzern, die Dokumente zur Verarbeitung und Genehmigung übermitteln, Anweisungen zur Verfügung stellen. Diese Benutzer werden auch als *Ersteller* bezeichnet. Sie erstellen beispielsweise einen Workflow für eine Bestellanforderung und geben Anweisungen ein. Diese Anweisungen können von Benutzern angezeigt werden, die Bestellanforderungen auf der Seite **Bestellanforderungen** eingeben. Der Ersteller klickt auf das Symbol in der Workflowstatusleiste, um Anweisungen anzuzeigen. Gehen Sie folgendermaßen vor, um Anweisungen für Benutzer einzugeben.

1.  Klicken Sie im linken Bereich auf **Grundeinstellungen**.
2.  Geben Sie im Feld **Übermittlungsanweisungen** die Arbeitsanweisungen ein.
3.  Zum Personalisieren der Anweisungen können Sie Platzhalter einfügen. Platzhalter werden beim Anzeigen der Arbeitsanweisungen durch die entsprechenden Daten ersetzt. Führen Sie folgende Schritte aus, um einen Platzhalter einzufügen:
    1.  Wählen Sie das Feld **Übermittlungsanweisungen** aus, um festzulegen, wo der Platzhalter erscheinen soll.
    2.  Klicken Sie auf **Platzhalter einfügen**.
    3.  Wählen Sie in der angezeigten Liste den einzufügenden Platzhalter aus.
    4.  Klicken Sie auf **Einfügen**.

4.  Führen Sie die folgenden Schritte aus, um Übersetzungen von Arbeitsanweisungen hinzuzufügen:
    1.  Klicken Sie auf **Übersetzungen**.
    2.  Klicken Sie auf der nun angezeigten Seite auf **Hinzufügen**.
    3.  Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.
    4.  Geben Sie den Text im Feld **Übersetzter Text** ein.
    5.  Zum Personalisieren des Texts können Sie Platzhalter einfügen. Anweisungen zum Eingeben eines Platzhalters finden Sie in Schritt 3.
    6.  Klicken Sie auf **Schließen**.

## <a name="specify-when-this-workflow-is-used"></a>Angeben, wann der Workflow verwendet wird
Sie können mehrere Workflows erstellen, die auf demselben Typ basieren. Sie können beispielsweise für jedes Land bzw. jede Region, in dem/der Sie tätig sind, einen Workflow für Bestellanforderungen erstellen, wie "Bestellanforderungen Dänemark" und "Bestellanforderungen Spanien". Wenn mehrere Workflows vorhanden sind, die auf demselben Typ basieren, müssen Sie angeben werden, wann jeder Workflow verwendet wird. Für obengenanntes Beispiel müssen die folgenden Bedingungen angegeben werden:

-   "Bestellanforderungen Dänemark" wird verwendet, wenn: Land/Region = DK.
-   "Bestellanforderungen Spanien" wird verwendet, wenn: Land/Region = ES.

Gehen Sie folgendermaßen vor, um anzugeben, wann der von Ihnen konfigurierte Workflow verwendet wird.

1.  Klicken Sie im linken Bereich auf **Aktivierung**.
2.  Aktivieren Sie das Kontrollkästchen **Bedingungen für Ausführung des Workflows festlegen**.
3.  Klicken Sie auf **Bedingung hinzufügen**.
4.  Geben Sie eine Bedingung ein.
5.  Geben Sie alle notwendigen zusätzlichen Bedingungen ein.
6.  Führen Sie folgende Schritte aus, um die korrekte Einstellung der eingegebenen Bedingungen zu überprüfen:
    1.  Klicken Sie auf **Test**.
    2.  Auf der Seite **Workflowbedingung testen** im Bereich **Bedingung überprüfen** wählen Sie einen Datensatz aus.
    3.  Klicken Sie auf **Test**. Der Datensatz wird ausgewertet, um zu bestimmen, ob er den angegebenen Bedingungen entspricht. Beim Erstellen eines Workflow für Bestellanforderungen z. B. für Spanien, wird im Bereich **Bedingung überprüfen** der Seite eine Liste mit Bestellanforderungen angezeigt. Wenn Sie auf **Test** klicken, wird die ausgewählte Bestellanforderung vom System ausgewertet, um festzustellen, ob Land/Region = ES ist.
    4.  Klicken Sie auf **OK** oder **Abbrechen**, um zur Seite **Eigenschaften** zurückzukehren.

## <a name="specify-when-notifications-are-sent"></a>Angeben, wann Benachrichtigungen gesendet werden
Wenn ein Dokument zur Verarbeitung übermittelt wird, wird eine Workflowinstanz erstellt. Benutzern können Benachrichtigungen gesendet werden, wenn auf diesem Workflow basierende Workflowinstanzen gestartet, abgeschlossen, beendet oder aufgrund eines Fehlers angehalten werden. Gehen Sie folgendermaßen vor, um anzugeben, wann Benachrichtigungen gesendet werden.

1.  Klicken Sie im linken Bereich auf **Benachrichtigungen**.
2.  Aktivieren Sie das Kontrollkästchen für jedes Ereignis, das Benachrichtigungen auslösen soll:
    -   **Gestartet** – Benachrichtigungen werden beim Start einer Workflowinstanz gesendet.
    -   **Beendet** – Benachrichtigungen werden gesendet, wenn eine Workflowinstanz aufgrund eines Fehlers beendet wird.
    -   **Abgeschlossen** – Benachrichtigungen werden beim Abschluss einer Workflowinstanz gesendet.
    -   **Nicht behebbar** – Benachrichtigungen werden gesendet, wenn eine Workflowinstanz aufgrund eines nicht behebbaren Fehlers beendet wird.
    -   **Beendet** – Benachrichtigungen werden beim Beenden einer Workflowinstanz gesendet.

3.  Wählen Sie eine Zeile für ein in Schritt 2 ausgewähltes Ereignis aus.
4.  Geben Sie auf der Registerkarte **Benachrichtigungstext** den Text der Benachrichtigung ein.
5.  Zum Personalisieren des Texts können Sie Platzhalter einfügen. Platzhalter werden bei der Anzeige für Benutzer durch die entsprechenden Daten ersetzt. Führen Sie folgende Schritte aus, um einen Platzhalter einzufügen:
    1.  Klicken Sie in das Feld, um die Position des Platzhalters anzugeben.
    2.  Klicken Sie auf **Platzhalter einfügen**.
    3.  Wählen Sie in der angezeigten Liste den einzufügenden Platzhalter aus.
    4.  Klicken Sie auf **Einfügen**.

6.  Führen Sie die folgenden Schritte aus, um Übersetzungen von Text hinzuzufügen:
    1.  Klicken Sie auf **Übersetzungen**.
    2.  Klicken Sie auf der nun angezeigten Seite auf **Hinzufügen**.
    3.  Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.
    4.  Geben Sie den Text im Feld **Übersetzter Text** ein.
    5.  Zum Personalisieren des Texts können Sie Platzhalter einfügen. Anweisungen zum Eingeben eines Platzhalters finden Sie in Schritt 5.
    6.  Klicken Sie auf **Schließen**.

7.  Verwenden Sie auf der Registerkarte **Empfänger** die folgenden Optionen, um anzugeben, wer die Benachrichtigungen erhalten soll.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Mit der folgenden Option...</th>
    <th>Benachrichtigungen werden an diese Benutzer gesendet</th>
    <th>Gehen Sie folgendermaßen vor, um Benachrichtigungen zu senden.</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Teilnehmer</td>
    <td>Benutzer, die einer bestimmten Gruppe oder Rolle zugewiesen sind</td>
    <td><ol>
    <li>Klicken Sie auf der Registerkarte <strong>Empfänger</strong> auf <strong>Teilnehmer</strong>.</li>
    <li>Wählen Sie in der Liste <strong>Art von Teilnehmer</strong> auf der Registerkarte <strong>Rollenbasiert</strong> die Art der Gruppe oder Rolle, an die die Benachrichtigungen gesendet werden sollen.</li>
    <li>Wählen Sie in der Liste <strong>Teilnehmer</strong> die Gruppe oder Rolle aus, an die Benachrichtigungen gesendet werden sollen.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Workflowbenutzer</td>
    <td>Benutzer, die an diesem Workflow teilnehmen</td>
    <td><ol>
    <li>Klicken Sie auf der Registerkarte <strong>Empfänger</strong> auf <strong>Workflowbenutzer</strong>.</li>
    <li>Wählen Sie auf der Registerkarte <strong>Workflowbenutzer</strong> in der Liste <strong>Workflowbenutzer</strong>, einen Teilnehmer dieses Workflow aus.</li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Benutzer</td>
    <td>Bestimmte Benutzer von Finance and Operations</td>
    <td><ol>
    <li>Klicken Sie auf der Registerkarte <strong>Empfänger</strong> auf <strong>Benutzer</strong>.</li>
    <li>In der Registerkarte <strong>Benutzer</strong> enthält die Liste <strong>Verfügbare Benutzer</strong> alle Finance and Operations-Benutzer. Wählen Sie die Benutzer aus, an die Benachrichtigungen gesendet werden sollen, und verschieben Sie diese Benutzer in die Liste <strong>Ausgewählte Benutzer</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  Wiederholen Sie die Schritte 3 bis 7 für jedes in Schritt 2 ausgewählte Ereignis.

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a>Geben Sie Kommentare zu den Änderungen am Workflow ein
Gehen Sie folgendermaßen vor, um Kommentare zu den Änderungen am Workflow einzugeben.

1.  Klicken Sie im linken Bereich auf **Hinweise**.
2.  Geben Sie im Feld **Kommentare zum Workflow eingeben** Ihre Kommentare ein.
3.  Prüfen Sie die Kommentare. Nach dem Hinzufügen von Kommentaren können diese nicht mehr geändert werden.
4.  Klicken Sie auf **Hinzufügen**, um Ihre Kommentare dem Bereich **Kommentarhistorie** hinzuzufügen.





