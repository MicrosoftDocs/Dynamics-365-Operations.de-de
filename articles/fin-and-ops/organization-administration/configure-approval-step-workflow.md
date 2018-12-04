---
title: Genehmigungsschritte in einem Workflow konfigurieren
description: "Dieses Thema erläutert, wie Sie die Eigenschaften eines Genehmigungsschritts konfigurieren können."
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 813866d63f38f5865666bad96f6f3590716a93ad
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---

# <a name="configure-approval-steps-in-a-workflow"></a>Genehmigungsschritte in einem Workflow konfigurieren

[!include [banner](../includes/banner.md)]

Dieses Thema erläutert, wie Sie die Eigenschaften eines Genehmigungsschritts konfigurieren können.

Klicken Sie zum Konfigurieren eines Genehmigungsschritts im Workflow-Editor mit der rechten Maustaste auf den Genehmigungsschritt, und klicken Sie dann auf **Eigenschaften**, um die Seite **Eigenschaften** zu öffnen. Verwenden Sie dann die folgenden Verfahren, um die Eigenschaften des Genehmigungsschritts zu konfigurieren.

## <a name="name-the-step"></a>Benennen des Schritts
Gehen Sie folgendermaßen vor, um einen Namen für den Genehmigungsschritt einzugeben.

1.  Klicken Sie im linken Bereich auf **Grundeinstellungen**.
2.  Geben Sie im Feld **Name** einen eindeutigen Namen für den Genehmigungsschritt ein.

## <a name="enter-a-subject-line-and-instructions"></a>Eingeben einer Betreffzeile und von Anweisungen
Sie müssen eine Betreffzeile und Anweisungen für Benutzer eingeben, die dem Genehmigungsschritt zugewiesen sind. Wenn Sie z. B. einen Genehmigungsschritt für Bestellanforderungen konfigurieren, werden dem Benutzer, der dem Schritt zugewiesen ist, die Betreffzeile und Anweisungen auf der Seite **Bestellanforderungen** angezeigt. Die Betreffzeile wird in einer Statusleiste auf der Seite angezeigt. Der Benutzer kann nun auf das Symbol in der Statusleiste klicken, um die Anweisungen anzuzeigen. Gehen Sie folgendermaßen vor, um eine Betreffzeile und Anweisungen einzugeben.

1.  Klicken Sie im linken Bereich auf **Grundeinstellungen**.
2.  Geben Sie im Feld **Betreff für die Arbeitsaufgabe** die Betreffzeile ein.
3.  Zum Personalisieren der Betreffzeile können Sie Platzhalter einfügen. Platzhalter werden durch die entsprechenden Daten ersetzt, wenn die Betreffzeile Benutzern angezeigt wird. Führen Sie folgende Schritte aus, um einen Platzhalter einzufügen:
    1.  Klicken Sie im Textfeld die Position des Platzhalters an.
    2.  Klicken Sie auf **Platzhalter einfügen**.
    3.  Wählen Sie in der angezeigten Liste den einzufügenden Platzhalter aus.
    4.  Klicken Sie auf **Einfügen**.

4.  Führen Sie die folgenden Schritte aus, um Übersetzungen der Betreffzeile hinzuzufügen:
    1.  Klicken Sie auf **Übersetzungen**.
    2.  Klicken Sie auf der nun angezeigten Seite auf **Hinzufügen**.
    3.  Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.
    4.  Geben Sie den Text im Feld **Übersetzter Text** ein.
    5.  Um den Text zu personalisieren, können Platzhalter, wie in Schritt 3 beschrieben, eingefügt werden.
    6.  Klicken Sie auf **Schließen**.

5.  Geben Sie im Feld **Arbeitsaufgabenanweisungen** die Arbeitsanweisungen ein.
6.  Zum Personalisieren der Anweisungen können Sie Platzhalter einfügen. Platzhalter werden beim Anzeigen der Arbeitsanweisungen durch die entsprechenden Daten ersetzt. Führen Sie folgende Schritte aus, um einen Platzhalter einzufügen:
    1.  Klicken Sie im Textfeld die Position des Platzhalters an.
    2.  Klicken Sie auf **Platzhalter einfügen**.
    3.  Wählen Sie in der angezeigten Liste den einzufügenden Platzhalter aus.
    4.  Klicken Sie auf **Einfügen**.

7.  Führen Sie die folgenden Schritte aus, um Übersetzungen von Arbeitsanweisungen hinzuzufügen:
    1.  Klicken Sie auf **Übersetzungen**.
    2.  Klicken Sie auf der nun angezeigten Seite auf **Hinzufügen**.
    3.  Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.
    4.  Geben Sie den Text im Feld **Übersetzter Text** ein.
    5.  Um den Text zu personalisieren, können Platzhalter, wie in Schritt 6 beschrieben, eingefügt werden.
    6.  Klicken Sie auf **Schließen**.

## <a name="assign-the-approval-step"></a>Zuweisen des Genehmigungsschritts
Gehen Sie folgendermaßen vor, um anzugeben, wem der Genehmigungsschritt zugewiesen werden soll.

1.  Klicken Sie im linken Bereich auf **Zuweisung**.
2.  Wählen Sie auf der Registerkarte **Zuweisungstyp** eine der Optionen der folgenden Tabelle aus, und führen Sie dann die zusätzlichen Schritte für die Option aus, bevor Sie mit Schritt 3 fortfahren.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Mit der folgenden Option...</th>
    <th>Benutzer, denen der Genehmigungsschritt zugewiesen ist</th>
    <th>Zusätzliche Schritte</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Teilnehmer</td>
    <td>Benutzer, die einer bestimmten Gruppe oder Rolle zugewiesen sind</td>
    <td><ol>
    <li>Nachdem Sie <strong>Teilnehmer</strong> auf der Registerkarte <strong>Rollenbasiert</strong> in der Liste <strong>Art von Teilnehmer</strong> ausgewählt haben, wählen Sie den Typ der Gruppe oder der Rolle aus, dem der Schritt zugewiesen werden soll.</li>
    <li>Wählen Sie in der Liste <strong>Teilnehmer</strong> den Typ der Gruppe oder der Rolle aus, dem der Schritt zugewiesen werden soll.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Hierarchie</td>
    <td>Benutzer in einer bestimmten Organisationshierarchie</td>
    <td><ol>
    <li>Nachdem Sie <strong>Hierarchie</strong> auf der Registerkarte <strong>Hierarchieauswahl</strong> in der Liste <strong>Hierarchietyp</strong> ausgewählt haben, wählen Sie den Typ der Hierarchie aus, dem der Schritt zugewiesen werden soll.</li>
    <li>Vom System muss eine Reihe von Benutzernamen aus der Hierarchie abgerufen werden. Diese Namen stellen Benutzer dar, denen der Schritt zugewiesen werden kann. Gehen Sie folgendermaßen vor, um den Anfangs- und Endpunkt des Bereichs von Benutzernamen anzugeben, die vom System abgerufen werden: <ol>
    <li>Wählen Sie zum Angeben eines Startpunkts eine Person in der Liste <strong>Beginn</strong> aus.</li>
    <li>Klicken Sie zum Angeben des Endpunkts auf <strong>Bedingung hinzufügen</strong>. Geben Sie dann eine Bedingung ein, die bestimmt, an welcher Position in der Hierarchie das Abrufen von Namen beendet werden soll.</li>
    </ol></li>
    <li>Geben Sie auf der Registerkarte <strong>Hierarchieoptionen</strong> an, welchen Benutzern im Bereich der Schritt zugewiesen werden soll: <ul>
    <li><strong>Allen abgerufenen Benutzern zuordnen</strong> – Der Schritt wird allen Benutzern im Bereich zugeordnet.</li>
    <li><strong>Nur letztem abgerufenen Benutzer zuordnen</strong> – Der Schritt wird nur dem letzten Benutzer im Bereich zugewiesen.</li>
    <li><strong>Benutzer ausschließen, die die folgenden Bedingung erfüllen</strong> – Der Schritt wird keinem Benutzer im Bereich zugewiesen, der eine bestimmte Bedingung erfüllt. Klicken Sie auf <strong>Bedingung hinzufügen</strong>, um die Bedingung anzugeben.</li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Workflowbenutzer</td>
    <td>Benutzer im aktuellen Workflow</td>
    <td><ul>
    <li>Nachdem Sie, <strong>Workflowbenutzer</strong> auf der Registerkarte <strong>Workflowbenutzer</strong>, in der Liste <strong>Workflowbenutzer</strong> ausgewählt haben, wählen Sie einen Benutzer aus, der am Workflow teilnimmt.</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>Benutzer</td>
    <td>Bestimmte Benutzer von Microsoft Dynamics 365 Finance and Operations</td>
    <td><ol>
    <li>Nachdem Sie <strong>Benutzer</strong>ausegwählt haben, klicken Sie auf die Registerkarte <strong>Benutzer</strong>.</li>
    <li>Die Liste <strong>Verfügbare Benutzer</strong> enthält die Liste aller Benutzer von Finance and Operations. Wählen Sie die Benutzer aus, um den Schritt zuzuweisen, und verschieben Sie diese Benutzer dann in die Liste <strong>Ausgewählte Benutzer</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

3.  Geben Sie auf der Registerkarte **Zeitlimit** im Feld **Dauer** an, wie viel Zeit dem Benutzer zum Bearbeiten oder Beantworten von Dokumenten zur Verfügung steht, die den Genehmigungsschritt erreichen. Folgende Optionen stehen zur Auswahl:
    -   **Stunden** – Geben Sie die Anzahl der Stunden ein, die der Benutzer zum Beantworten hat. Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.
    -   **Tage** – Geben Sie die Anzahl der Tage ein, die der Benutzer zum Beantworten hat. Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.
    -   **Wochen** – Geben Sie die Anzahl der Wochen ein, die der Benutzer zum Beantworten hat.
    -   **Monate** – Wählen Sie den Tag und die Woche aus, bis zu dem der Benutzer antworten muss. Sie können z. B. angeben, dass der Benutzer bis Freitag der dritten Woche des Monats antworten soll.
    -   **Jahre** – Wählen Sie den Tag, die Woche und den Monat aus, bis zu dem der Benutzer antworten muss. Sie können z. B. angeben, dass der Benutzer bis Freitag der dritten Woche im Dezember antworten soll.

    Wenn der Benutzer das Dokument nicht innerhalb der vorgesehenen Zeit bearbeitet, ist das Dokument überfällig. Ein überfälliges Dokument wird basierend auf den ausgewählten Optionen im Bereich **Eskalation** der Seite eskaliert.
4.  Wenn Sie den Genehmigungsschritt mehreren Benutzern oder einer Gruppe von Benutzern zugewiesen haben, klicken Sie auf die Registerkarte **Vollendungsrichtlinie**, und wählen Sie eine der folgenden Optionen aus:
    -   **Einzelne genehmigende Person** – Die Aktivität für das Dokument wird von der ersten antwortenden Person bestimmt. Nehmen wir an, Steffen hat eine Spesenabrechnung in Höhe von 15.000 Euro eingereicht. Die Spesenabrechnung ist derzeit Saskia, Jens und Bastian zugewiesen. Falls Saskia die erste Person ist, die das Dokument beantwortet, wird ihre Aktivität für das Dokument übernommen. Falls Saskia das Dokument ablehnt, wird es abgelehnt und an Steffen zurückgesendet. Wenn Saskia das Dokument genehmigt, wird es zur Genehmigung an Anne gesendet. 

    ![Workflow mit Genehmigungsprozesses](./media/workflow_multipleusersinstep.gif)

    -   **Mehrheit der genehmigenden Personen** – Die Aktivität für das Dokument wird bei Antwort der Mehrheit der genehmigenden Personen bestimmt. Nehmen wir an, Steffen hat eine Spesenabrechnung in Höhe von 15.000 Euro eingereicht. Die Spesenabrechnung ist derzeit Saskia, Jens und Bastian zugewiesen. Falls Saskia und Jens die ersten beiden genehmigenden Personen sind, die antworten, wird ihre Aktivität für das Dokument übernommen.
        -   Wird das Dokument von Saskia genehmigt, von Jens jedoch abgelehnt, wird es abgelehnt und an Steffen zurückgesendet.
        -   Wird das Dokument sowohl von Saskia als auch von Jens genehmigt, wird es zur Genehmigung an Anne gesendet.
    -   **Prozentsatz der Genehmiger** – Die Aktivität für das Dokument wird bei Antwort eines bestimmten Prozentsatzes der genehmigenden Personen bestimmt. Nehmen wir an, Steffen hat eine Spesenabrechnung in Höhe von 15.000 Euro eingereicht. Die Spesenabrechnung ist derzeit Saskia, Jens und Bastian zugewiesen, und Sie haben **50** als Prozentsatz eingegeben. Falls Saskia und Jens die ersten beiden genehmigenden Personen sind, die antworten, wird ihre Aktivität für das Dokument übernommen, da sie die Anforderung von 50 Prozent der genehmigenden Personen erfüllen.
        -   Wird das Dokument von Saskia genehmigt, von Jens jedoch abgelehnt, wird es abgelehnt und an Steffen zurückgesendet.
        -   Wird das Dokument sowohl von Saskia als auch von Jens genehmigt, wird es zur Genehmigung an Anne gesendet.
    -   **Alle genehmigenden Personen** – Alle genehmigenden Personen müssen das Dokument genehmigen. Andernfalls kann der Workflow nicht fortgesetzt werden. Nehmen wir an, Steffen hat eine Spesenabrechnung in Höhe von 15.000 Euro eingereicht. Die Spesenabrechnung ist derzeit Saskia, Jens und Bastian zugewiesen. Wird das Dokument von Saskia und Jens genehmigt, von Bastian jedoch abgelehnt, wird es abgelehnt und an Steffen zurückgesendet. Wird das Dokument von Saskia, Jens und Bastian genehmigt, wird es zur Genehmigung an Anne gesendet.

## <a name="specify-when-the-approval-step-is-required"></a>Angeben, wann der Genehmigungsschritt erforderlich ist
Sie können angeben, wann der Genehmigungsschritt erforderlich ist. Der Genehmigungsschritt kann immer oder nur dann erforderlich sein, wenn bestimmte Bedingungen erfüllt sind.

### <a name="the-approval-step-is-always-required"></a>Der Genehmigungsschritt ist immer erforderlich

Gehen Sie folgendermaßen vor, wenn der Genehmigungsschritt immer erforderlich ist.

1.  Klicken Sie im linken Bereich auf **Bedingung**.
2.  Wählen Sie die Option **Diesen Schritt immer ausführen** aus.

### <a name="the-approval-step-is-required-in-specific-conditions"></a>Der Genehmigungsschritt ist unter bestimmten Bedingungen erforderlich

Der Genehmigungsschritt, den Sie konfigurieren, ist möglicherweise nur erforderlich, wenn bestimmte Bedingungen erfüllt sind. Beispiel: Sie konfigurieren einen Genehmigungsschritt für einen Workflow für Bestellanforderungen und möchten, dass der Genehmigungsschritt nur dann ausgeführt wird, wenn die Bestellanforderung einen Betrag von 10.000 Euro überschreitet. Gehen Sie folgendermaßen vor, um anzugeben, wann der Genehmigungsschritt erforderlich ist.

1.  Klicken Sie im linken Bereich auf **Bedingung**.
2.  Wählen Sie die Option **Diesen Schritt nur ausführen, wenn folgende Bedingungen erfüllt sind** aus.
3.  Geben Sie eine Bedingung ein.
4.  Geben Sie alle notwendigen zusätzlichen Bedingungen ein.
5.  Führen Sie folgende Schritte aus, um die korrekte Konfiguration der eingegebenen Bedingungen zu überprüfen:
    1.  Klicken Sie auf **Test**.
    2.  Auf der Seite **Workflowbedingung testen** im Bereich **Bedingung überprüfen** wählen Sie einen Datensatz aus.
    3.  Klicken Sie auf **Test**. Der Datensatz wird ausgewertet, um zu bestimmen, ob er den festgelegten Bedingungen entspricht.
    4.  Klicken Sie auf **OK** oder **Abbrechen**, um zur Seite **Eigenschaften** zurückzukehren.

## <a name="specify-what-happens-when-the-document-is-overdue"></a>Festlegen der Vorgehensweise für überfällige Dokumente
Wenn ein Benutzer ein Dokument nicht innerhalb der vorgesehenen Zeit bearbeitet, ist das Dokument überfällig. Ein überfälliges Dokument kann eskaliert oder automatisch einem anderen Benutzer zur Genehmigung zugewiesen werden. Führen Sie die folgenden Schritte aus, um das Dokument zu eskalieren, wenn es überfällig ist.

1.  Klicken Sie im linken Bereich auf **Eskalation**.
2.  Aktivieren Sie das Kontrollkästchen **Eskalationspfad verwenden**, um einen Eskalationspfad zu erstellen. Das Dokument wird automatisch den im Eskalationspfad aufgeführten Benutzern zugewiesen. Die folgende Tabelle stellt z. B. einen Eskalationspfad dar.

    | Sequenz | Eskalationspfad      |
    |----------|----------------------|
    | 1        | Zuweisen zu: Doris     |
    | 2        | Zuweisen zu: Elke      |
    | 3        | Abschließende Aktivität: Ablehnen |

    In diesem Beispiel wird das überfällige Dokument Doris zugewiesen. Antwortet Doris nicht innerhalb der vorgesehenen Zeit, wird das Dokument Elke zugewiesen. Antwortet Elke nicht innerhalb der vorgesehenen Zeit, wird das Dokument abgelehnt.
3.  Klicken Sie auf **Eskalation hinzufügen**, um dem Eskalationspfad einen Benutzer hinzuzufügen. Wählen Sie auf der Registerkarte **Zuweisungstyp** eine der Optionen der folgenden Tabelle aus, und führen Sie dann die zusätzlichen Schritte für die Option aus, bevor Sie mit Schritt 4 fortfahren.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Mit der folgenden Option...</th>
    <th>Benutzer, denen das Dokument eskaliert wird</th>
    <th>Zusätzliche Schritte</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Hierarchie</td>
    <td>Benutzer in einer bestimmten Organisationshierarchie</td>
    <td><ol>
    <li>Nachdem Sie <strong>Hierarchie</strong> auf der Registerkarte <strong>Hierarchieauswahl</strong> in der Liste <strong>Hierarchietyp</strong> ausgewählt haben, wählen Sie den Typ der Hierarchie aus, an den das Dokument eskaliert werden soll.</li>
    <li>Vom System muss eine Reihe von Benutzernamen aus der Hierarchie abgerufen werden. Diese Namen stellen Benutzer dar, an die das Dokument unter Umständen eskaliert werden kann. Gehen Sie folgendermaßen vor, um den Anfangs- und Endpunkt des Bereichs von Benutzernamen anzugeben, die vom System abgerufen werden: <ol>
    <li>Wählen Sie zum Angeben eines Startpunkts eine Person in der Liste <strong>Beginn</strong> aus.</li>
    <li>Klicken Sie zum Angeben des Endpunkts auf <strong>Bedingung hinzufügen</strong>. Geben Sie dann eine Bedingung ein, die bestimmt, an welcher Position in der Hierarchie das Abrufen von Namen beendet werden soll.</li>
    </ol></li>
    <li>Geben Sie auf der Registerkarte <strong>Hierarchieoptionen</strong> an, an welche Benutzer im Bereich das Dokument eskaliert werden soll: <ul>
    <li><strong>Allen abgerufenen Benutzern zuordnen</strong> – Das Dokument wird an alle Benutzer im Bereich eskaliert.</li>
    <li><strong>Nur letztem abgerufenen Benutzer zuordnen</strong> – Das Dokument wird nur an den letzten Benutzer im Bereich eskaliert.</li>
    <li><strong>Benutzer ausschließen, die die folgenden Bedingung erfüllen</strong> – Das Dokument wird an keinen Benutzer im Bereich eskaliert, der eine bestimmte Bedingung erfüllt. Klicken Sie auf <strong>Bedingung hinzufügen</strong>, um die Bedingung anzugeben.</li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Workflowbenutzer</td>
    <td>Benutzer im aktuellen Workflow</td>
    <td><ul>
    <li>Nachdem Sie, <strong>Workflowbenutzer</strong> auf der Registerkarte <strong>Workflowbenutzer</strong>, in der Liste <strong>Workflowbenutzer</strong> ausgewählt haben, wählen Sie einen Benutzer aus, der am Workflow teilnimmt.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Benutzer</td>
    <td>Bestimmte Benutzer von Finance and Operations</td>
    <td><ol>
    <li>Nachdem Sie <strong>Benutzer</strong>ausegwählt haben, klicken Sie auf die Registerkarte <strong>Benutzer</strong>.</li>
    <li>Die Liste <strong>Verfügbare Benutzer</strong> enthält die Liste aller Benutzer von Finance and Operations. Wählen Sie die Benutzer aus, an die das Dokument eskaliert werden soll, und verschieben Sie diese Benutzer in die Liste <strong>Ausgewählte Benutzer</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

4.  Geben Sie auf der Registerkarte **Zeitlimit** im Feld **Dauer** an, wie viel Zeit dem Benutzer zum Bearbeiten oder Beantworten von Dokumenten zur Verfügung steht. Folgende Optionen stehen zur Auswahl:
    -   **Stunden** – Geben Sie die Anzahl der Stunden ein, die der Benutzer zum Beantworten hat. Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.
    -   **Tage** – Geben Sie die Anzahl der Tage ein, die der Benutzer zum Beantworten hat. Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.
    -   **Wochen** – Geben Sie die Anzahl der Wochen ein, die der Benutzer zum Beantworten hat.
    -   **Monate** – Wählen Sie den Tag und die Woche aus, bis zu dem der Benutzer antworten muss. Sie können z. B. angeben, dass der Benutzer bis Freitag der dritten Woche des Monats antworten soll.
    -   **Jahre** – Wählen Sie den Tag, die Woche und den Monat aus, bis zu dem der Benutzer antworten muss. Sie können z. B. angeben, dass der Benutzer bis Freitag der dritten Woche im Dezember antworten soll.

5.  Wiederholen Sie die Schritte 3 bis 4 für alle Benutzer, die dem Eskalationspfad hinzugefügt werden sollen. Sie können die Reihenfolge der Benutzer ändern.
6.  Wenn die Benutzer im Eskalationspfad nicht innerhalb der vorgesehenen Zeit antworten, wird das Dokument automatisch bearbeitet. Um die vom System auszuführende Aktivität anzugeben, wählen Sie die Zeile **Aktivität** aus, klicken Sie dann auf die Registerkarte **Aktivität bei Beendigung** und wählen eine Aktivität aus.





