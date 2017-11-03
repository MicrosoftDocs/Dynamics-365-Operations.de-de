---
title: Einen Genehmigungsschritt in einem Workflow genehmigen
description: Verwenden Sie das folgende Verfahren, um die Eigenschaften des Genehmigungsprozesses zu konfigurieren.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: eedadfcbfac9d792a5ab80c1dcd8f3abfaddca08
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="configure-an-approval-process-in-a-workflow"></a>Einen Genehmigungsschritt in einem Workflow genehmigen

[!include[banner](../includes/banner.md)]


Verwenden Sie das folgende Verfahren, um die Eigenschaften des Genehmigungsprozesses zu konfigurieren.

Klicken Sie zum Konfigurieren eines Genehmigungsprozesses im Workflow-Editor mit der rechten Maustaste auf das Genehmigungselement, und klicken Sie dann auf **Eigenschaften**, um das Formular  **Eigenschaftens** zu öffnen.
Benennen des Genehmigungsprozesses
-------------------------

Gehen Sie folgendermaßen vor, um einen Namen für den Genehmigungsprozess einzugeben.
1.  Klicken Sie im linken Bereich auf **Grundeinstellungen**.
2.  Geben Sie im Feld **Name** einen eindeutigen Namen für den Genehmigungsprozess ein.

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a>Angeben, wann das Dokument automatisch bearbeitet wird
Sie können festlegen, dass eine automatische Aktivität für das Dokument ausgeführt wird, wenn bestimmte Bedingungen erfüllt sind. So können z. B. Spesenabrechnungen mit einem Gesamtbetrag unter 100 Euro automatisch genehmigt werden. Gehen Sie folgendermaßen vor, um anzugeben, wann das Dokument automatisch bearbeitet wird.
1.  Klicken Sie im linken Bereich auf **Automatische Aktivitäten**.
2.  Aktivieren Sie dieses Kontrollkästchen **Automatische Aktivitäten aktivieren**.
3.  Klicken Sie auf **Bedingung hinzufügen**.
4.  Geben Sie eine Bedingung ein.
5.  Geben Sie ggf. zusätzliche Bedingungen ein.
6.  Führen Sie folgende Schritte aus, um die korrekte Konfiguration der eingegebenen Bedingungen zu überprüfen:
    1.  Klicken Sie auf **Test**, um das Formular **Workflow-Bedingungen testen** zu öffnen.
    2.  Wählen Sie im Bereich **Bedingung überprüfen** des Formulars einen Datensatz aus.
    3.  Klicken Sie auf **Test**. Der Datensatz wird ausgewertet, um zu bestimmen, ob er den festgelegten Bedingungen entspricht.
    4.  Klicken Sie auf **OK** oder **Abbrechen**, um zum Formular **Eigenschaften** zurückzukehren.

7.  Wählen Sie in der Liste **Aktivität für Auto-Vervollständigen** die Aktivität aus, die für das Dokument ausgeführt werden soll.

## <a name="specify-when-notifications-are-sent"></a>Angeben, wann Benachrichtigungen gesendet werden
Sie können Benachrichtigungen an Personen senden, wenn ein Dokument genehmigt, abgelehnt, delegiert oder eskaliert wurde oder eine Änderung für das Dokument angefordert wurde. Gehen Sie folgendermaßen vor, um anzugeben, wann und an wen Benachrichtigungen gesendet werden.
1.  Klicken Sie im linken Bereich auf **Benachrichtigungen**.
2.  Aktivieren Sie das Kontrollkästchen neben den Ereignissen, für die Benachrichtigungen gesendet werden sollen.
    -   **Delegieren** – Wenn ein Dokument einem anderen Benutzer zur Genehmigung zugewiesen wurde.
    -   **Eskalieren** – Wenn der zugewiesene Benutzer das Dokument nicht innerhalb der vorgesehenen Zeit bearbeitet hat.
    -   **Genehmigen** – Wenn ein Dokument genehmigt wurde.
    -   **Ablehnen** – Wenn ein Dokument abgelehnt wurde.
    -   **Änderung anfordern** – Wenn der zugewiesene Benutzer eine Änderung eines übermittelten Dokuments angefordert hat.

3.  Wählen Sie eine Zeile für ein in Schritt 2 ausgewähltes Ereignis aus.
4.  Klicken Sie auf die Registerkarte **Benachrichtigungstext**.
5.  Geben Sie im Textfeld den Text für die Benachrichtigung ein.
6.  Zum Anpassen des Texts können Sie Platzhalter einfügen, die bei der Anzeige für Benutzer durch die entsprechenden Daten ersetzt werden. Führen Sie folgende Schritte aus, um einen Platzhalter einzufügen:
    1.  Klicken Sie im Textfeld auf die Position, an der der Platzhalter erscheinen soll.
    2.  Klicken Sie auf **Platzhalter einfügen**.
    3.  Wählen Sie in der angezeigten Liste den einzufügenden Platzhalter aus.
    4.  Klicken Sie auf **Einfügen**.

7.  Klicken Sie auf **Übersetzungen**, um Übersetzungen der Benachrichtigung hinzuzufügen. Führen Sie im angezeigten Formular die folgenden Schritte aus:
    1.  Klicken Sie auf **Hinzufügen**.
    2.  Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.
    3.  Geben Sie den Text im Feld **Übersetzter Text** ein.
    4.  Fügen Sie zum Personalisieren des Texts Platzhalter ein.
    5.  Klicken Sie auf **Schließen**.

8.  Klicken Sie auf die Registerkarte **Empfänger**.
9.  Geben Sie an, an wen die Benachrichtigungen gesendet werden. Wählen Sie eine der Optionen in der folgenden Tabelle aus, und führen Sie dann die zusätzlichen Schritte für die Option aus, bevor Sie mit Schritt 10 fortfahren.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Mit der folgenden Option...</th>
    <th>Empfänger der Benachrichtigung</th>
    <th>Zusätzliche Schritte</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><strong>Teilnehmer</strong></td>
    <td>Benutzer, die einer bestimmten Gruppe oder Rolle zugewiesen sind</td>
    <td><ol>
    <li>Nachdem Sie <strong>Teilnehmer</strong> ausgewählt haben, klicken Sie auf die Registerkarte <strong>Rollenbasiert</strong>.</li>
    <li>Wählen Sie in der Liste <strong>Teilnehmertyp</strong> den Typ der Gruppe oder Rolle aus, an die Benachrichtigungen gesendet werden sollen.</li>
    <li>Wählen Sie in der Liste <strong>Teilnehmer</strong> die Gruppe oder Rolle aus, an die Benachrichtigungen gesendet werden sollen.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><strong>Workflowbenutzer</strong></td>
    <td>Benutzer, die am aktuellen Workflow teilnehmen</td>
    <td><ol>
    <li>Nachdem Sie <strong>Workflow-Benutzer</strong>ausegwählt haben, klicken Sie auf die Registerkarte <strong>Workflow-Benutzer</strong>.</li>
    <li>Wählen Sie in der Liste <strong>Workflow-Benutzer</strong> einen Benutzer aus, der am Workflow teilnimmt.</li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><strong>Benutzer</strong></td>
    <td>Bestimmte Benutzer von Microsoft Dynamics 365 Finance and Operations</td>
    <td><ol>
    <li>Nachdem Sie <strong>Benutzer</strong>ausegwählt haben, klicken Sie auf die Registerkarte <strong>Benutzer</strong>.</li>
    <li>Die <strong>Verfügbaren Benutzer</strong>:-Liste umfasst alle Benutzer von Microsoft Dynamics 365 for Finance and Operations. Wählen Sie die Benutzer aus, an die Benachrichtigungen gesendet werden sollen, und verschieben Sie diese Benutzer dann in die Liste <strong>Ausgewählte Benutzer</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

10. Wiederholen Sie die Schritte 3 bis 9 für jedes in Schritt 2 ausgewählte Ereignis.

## <a name="specify-a-final-approver"></a>Festlegen einer letzten genehmigenden Person
Eine letzte genehmigende Person sollte für Szenarios festgelegt werden, in denen die genehmigende Person die Person ist, die das Dokument zur Genehmigung übermittelt hat. Gehen Sie zum Festlegen einer letzten genehmigenden Person folgendermaßen vor.
1.  Klicken Sie im linken Bereich auf **Erweiterte Einstellungen**.
2.  Aktivieren Sie das Kontrollkästchen **Letzter Genehmiger verwenden**.
3.  Wählen Sie in der Liste den Benutzer aus, der als letzte genehmigende Person fungieren soll.

## <a name="set-a-time-limit"></a>Festlegen einer Zeitgrenze
Gehen Sie folgendermaßen vor, wenn der Genehmigungsprozess in einer bestimmten Zeit abgeschlossen werden muss.
| **Hinweis**                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die in diesen Schritten ausgewählten Optionen setzen die Optionen außer Kraft, die Sie in den Bereichen **Zuweisung** und **Eskalation** jedes Genehmigungsschritts ausgewählt haben. |

1.  Klicken Sie im linken Bereich auf **Erweiterte Einstellungen**.
2.  Wählen Sie das Kontrollkästchen **Zeitgrenze für das Workflow****element** festlegen.
3.  Legen Sie im Feld **Dauer** fest, wann der Genehmigungsprozess abgeschlossen sein muss. Folgende Optionen stehen zur Auswahl:
    -   **Stunden** – Geben Sie die Anzahl der Stunden ein, in denen der Genehmigungsprozess abgeschlossen sein muss. Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.
    -   **Tage** – Geben Sie die Anzahl von Tagen ein, in denen der Genehmigungsprozess abgeschlossen sein muss. Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.
    -   **Wochen** – Geben Sie die Anzahl von Wochen ein, in denen der Genehmigungsprozess abgeschlossen sein muss.
    -   **Monate** – Wählen Sie den Tag, die Woche und den Monat aus, bis zu dem der Genehmigungsprozess abgeschlossen sein muss. Sie können z. B. angeben, dass der Genehmigungsprozess bis Freitag der dritten Woche des Monats abgeschlossen sein soll.
    -   **Jahre** – Wählen Sie den Tag, die Woche und den Monat aus, bis zu dem der Genehmigungsprozess abgeschlossen sein muss. Sie können z. B. angeben, dass der Genehmigungsprozess bis Freitag der dritten Woche im Dezember abgeschlossen sein soll.

4.  Wenn die Zeitgrenze überschritten wird, wird das Dokument automatisch bearbeitet. Wählen Sie in der Liste **Aktivität** die Aktivität aus, die vom System ausgeführt werden soll.

## <a name="specify-which-actions-are-available-to-the-user"></a>Angeben der verfügbaren Aktivitäten für den Benutzer
Wenn ein Dokument einem Benutzer zur Genehmigung zugewiesen wird, muss der Benutzer das Dokument durch entsprechende Aktivitäten bearbeiten. Gehen Sie folgendermaßen vor, um anzugeben, welche Aktivitäten der Benutzer für das übermittelte Dokument ausführen kann.
1.  Klicken Sie im linken Bereich auf **Erweiterte Einstellungen**.
2.  Aktivieren Sie das Kontrollkästchen **Genehmigen**, wenn der Benutzer das Dokument genehmigen kann.
3.  Aktivieren Sie das Kontrollkästchen **Ablehnen**, wenn der Benutzer das Dokument ablehnen kann.
4.  Aktivieren Sie das Kontrollkästchen **Änderung anfordern**, wenn der Benutzer Änderungen des Dokuments anfordern kann.
5.  Aktivieren Sie das Kontrollkästchen **Delegieren**, wenn der Benutzer das Dokument einem anderen Benutzer zur Genehmigung zuweisen kann.

**Hinweis**: Das Kontrollkästchen **Aktionen von der Arbeitsliste in Enterprise Portal aktivieren** ist nicht mehr vorhanden.

## <a name="configure-the-approval-steps"></a> Konfigurieren der Genehmigungsschritte
Ein Genehmigungsprozess besteht aus Genehmigungsschritten. Führen Sie die folgende Prozedur aus, um dem Genehmigungsprozess Schritte hinzuzufügen und die Schritte zu konfigurieren.
1.  Doppelklicken Sie im Workflow-Editor auf den Genehmigungsprozess. Im Workflow-Editor werden die Schritte des Genehmigungsprozesses angezeigt.
2.  Ziehen Sie zum Hinzufügen eines Genehmigungsschritts den Schritt aus dem Bereich **Workflow-Elemente** auf die Canvas.
3.  Informationen zum Konfigurieren eines Genehmigungsschritts finden, finden Sie unter[Konfigurieren eines Genehmigungsschritts](configure-approval-step-workflow.md).






