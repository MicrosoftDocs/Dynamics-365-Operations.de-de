---
title: Manuelle Aufgaben in einem Workflow konfigurieren
description: Dieses Thema erläutert, wie Sie die Eigenschaften einer manuellen Aufgabe konfigurieren können.
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 492c49b1a3e8334bca401770c4c2db04e8892691
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124634"
---
# <a name="configure-manual-tasks-in-a-workflow"></a>Manuelle Aufgaben in einem Workflow konfigurieren

[!include [banner](../includes/banner.md)]

Dieses Thema erläutert, wie Sie die Eigenschaften einer manuellen Aufgabe konfigurieren können.

Klicken Sie zum Konfigurieren einer manuellen Aufgabe im Workflow-Editor mit der rechten Maustaste auf die Aufgabe, und klicken Sie dann auf **Eigenschaften**, um die Seite **Eigenschaften** zu öffnen. Verwenden Sie dann die folgenden Verfahren, um die Eigenschaften der manuellen Aufgabe zu konfigurieren.

## <a name="name-the-task"></a>Benennen der Aufgabe

Gehen Sie folgendermaßen vor, um einen Namen für die manuelle Aufgabe einzugeben.

1. Klicken Sie im linken Bereich auf **Grundeinstellungen**.
2. Geben Sie im Feld **Name** einen eindeutigen Namen für die Aufgabe ein.

## <a name="enter-a-subject-line-and-instructions"></a>Eingeben einer Betreffzeile und von Anweisungen

Sie müssen eine Betreffzeile und Anweisungen für Benutzer eingeben, die der Aufgabe zugewiesen sind. Wenn Sie z. B. eine Aufgabe für Bestellanforderungen konfigurieren, werden dem Benutzer, der dem Schritt zugewiesen ist, die Betreffzeile und Anweisungen auf der Seite **Bestellanforderungen** angezeigt. Die Betreffzeile wird in einer Statusleiste auf der Seite angezeigt. Der Benutzer kann nun auf das Symbol in der Statusleiste klicken, um die Anweisungen anzuzeigen. Gehen Sie folgendermaßen vor, um eine Betreffzeile und Anweisungen einzugeben.

1. Klicken Sie im linken Bereich auf **Grundeinstellungen**.
2. Geben Sie im Feld **Betreff für die Arbeitsaufgabe** die Betreffzeile ein.
3. Zum Personalisieren der Betreffzeile können Sie Platzhalter einfügen. Platzhalter werden durch die entsprechenden Daten ersetzt, wenn die Betreffzeile Benutzern angezeigt wird. Führen Sie folgende Schritte aus, um einen Platzhalter einzufügen:

    1. Klicken Sie im Textfeld die Position des Platzhalters an.
    2. Klicken Sie auf **Platzhalter einfügen**.
    3. Wählen Sie in der angezeigten Liste den einzufügenden Platzhalter aus.
    4. Klicken Sie auf **Einfügen**.

4. Führen Sie die folgenden Schritte aus, um Übersetzungen der Betreffzeile hinzuzufügen:

    1. Klicken Sie auf **Übersetzungen**.
    2. Klicken Sie auf der nun angezeigten Seite auf **Hinzufügen**.
    3. Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.
    4. Geben Sie den Text im Feld **Übersetzter Text** ein.
    5. Um den Text zu personalisieren, können Platzhalter, wie in Schritt 3 beschrieben, eingefügt werden.
    6. Klicken Sie auf **Schließen**.

5. Geben Sie im Feld **Arbeitsaufgabenanweisungen** die Arbeitsanweisungen ein.
6. Zum Personalisieren der Anweisungen können Sie Platzhalter einfügen. Platzhalter werden beim Anzeigen der Arbeitsanweisungen durch die entsprechenden Daten ersetzt. Führen Sie folgende Schritte aus, um einen Platzhalter einzufügen:

    1. Klicken Sie im Textfeld die Position des Platzhalters an.
    2. Klicken Sie auf **Platzhalter einfügen**.
    3. Wählen Sie in der angezeigten Liste den einzufügenden Platzhalter aus.
    4. Klicken Sie auf **Einfügen**.

7. Führen Sie die folgenden Schritte aus, um Übersetzungen von Arbeitsanweisungen hinzuzufügen:

    1. Klicken Sie auf **Übersetzungen**.
    2. Klicken Sie auf der nun angezeigten Seite auf **Hinzufügen**.
    3. Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.
    4. Geben Sie den Text im Feld **Übersetzter Text** ein.
    5. Um den Text zu personalisieren, können Platzhalter, wie in Schritt 6 beschrieben, eingefügt werden.
    6. Klicken Sie auf **Schließen**.

## <a name="assign-the-task"></a>Zuweisen der Aufgabe

Gehen Sie folgendermaßen vor, um anzugeben, wem die manuelle Aufgabe zugewiesen werden soll.

1. Klicken Sie im linken Bereich auf **Zuweisung**.
2. Wählen Sie auf der Registerkarte **Zuweisungstyp** eine der Optionen der folgenden Tabelle aus, und führen Sie dann die zusätzlichen Schritte für die Option aus, bevor Sie mit Schritt 3 fortfahren.

    <table>
    <thead>
    <tr>
    <th>Mit der folgenden Option...</th>
    <th>Benutzer, denen die Aufgabe zugewiesen ist</th>
    <th>Zusätzliche Schritte</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Teilnehmer</td>
    <td>Benutzer, die einer bestimmten Gruppe oder Rolle zugewiesen sind</td>
    <td>
    <ol>
    <li>Nachdem Sie <strong>Teilnehmer</strong> auf der Registerkarte <strong>Rollenbasiert</strong> in der Liste <strong>Art von Teilnehmer</strong> ausgewählt haben, wählen Sie den Typ der Gruppe oder der Rolle aus, dem die Aufgabe zugewiesen werden soll.</li>
    <li>Wählen Sie in der Liste <strong>Teilnehmer</strong> die Gruppe oder Rolle aus, der die Aufgabe zugewiesen werden soll.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Hierarchie</td>
    <td>Benutzer in einer bestimmten Organisationshierarchie</td>
    <td>
    <ol>
    <li>Nachdem Sie <strong>Hierarchie</strong> auf der Registerkarte <strong>Hierarchieauswahl</strong> in der Liste <strong>Hierarchietyp</strong> ausgewählt haben, wählen Sie den Typ der Hierarchie aus, dem die Aufgabe zugewiesen werden soll.</li>
    <li>Vom System muss eine Reihe von Benutzernamen aus der Hierarchie abgerufen werden. Diese Namen stellen Benutzer dar, denen die Aufgabe zugewiesen wird. Gehen Sie folgendermaßen vor, um den Anfangs- und Endpunkt des Bereichs von Benutzernamen anzugeben, die vom System abgerufen werden: <ol>
    <li>Wählen Sie zum Angeben eines Startpunkts eine Person in der Liste <strong>Beginn</strong> aus.</li>
    <li>Klicken Sie zum Angeben des Endpunkts auf <strong>Bedingung hinzufügen</strong>. Geben Sie dann eine Bedingung ein, die bestimmt, an welcher Position in der Hierarchie das Abrufen von Namen beendet werden soll.</li>
    </ol>
    </li>
    <li>Geben Sie auf der Registerkarte <strong>Hierarchieoptionen</strong> an, welchen Benutzern im Bereich die Aufgabe zugewiesen werden soll: <ul>
    <li><strong>Allen abgerufenen Benutzern zuordnen</strong> – Die Aufgabe wird allen Benutzern im Bereich zugeordnet.</li>
    <li><strong>Nur letztem abgerufenen Benutzer zuordnen</strong> – Die Aufgabe wird nur dem letzten Benutzer im Bereich zugewiesen.</li>
    <li><strong>Benutzer ausschließen, die die folgenden Bedingung erfüllen</strong> – Die Aufgabe wird keinem Benutzer im Bereich zugewiesen, der eine bestimmte Bedingung erfüllt. Klicken Sie auf <strong>Bedingung hinzufügen</strong>, um die Bedingung anzugeben.</li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Workflowbenutzer</td>
    <td>Benutzer im aktuellen Workflow</td>
    <td>
    <ul>
    <li>Nachdem Sie, <strong>Workflowbenutzer</strong> auf der Registerkarte <strong>Workflowbenutzer</strong>, in der Liste <strong>Workflowbenutzer</strong> ausgewählt haben, wählen Sie einen Benutzer aus, der am Workflow teilnimmt.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Benutzer</td>
    <td>Bestimmte Benutzer</td>
    <td>
    <ol>
    <li>Nachdem Sie <strong>Benutzer</strong>ausegwählt haben, klicken Sie auf die Registerkarte <strong>Benutzer</strong>.</li>
    <li>Die Liste <strong>Verfügbare Benutzer</strong> enthält alle Benutzer. Wählen Sie die Benutzer aus, um die Aufgabe zuzuweisen, und verschieben Sie diese Benutzer dann in die Liste <strong>Ausgewählte Benutzer</strong>.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Warteschlange</td>
    <td>Eine Warteschlange für Arbeitsaufgaben</td>
    <td>
    <ol>
    <li>Nachdem Sie <strong>Warteschlange</strong> ausgewählt haben, klicken Sie auf die Registerkarte <strong>Warteschlangenbasiert</strong>.</li>
    <li>Gehen Sie folgendermaßen vor, um die Aufgabe einer bestimmten Warteschlange zuzuweisen: <ol>
    <li>In der Liste <strong>Warteschlangentyp</strong> wählen Sie <strong>Warteschlangen für Arbeitsaufgaben</strong> aus.</li>
    <li>Wählen Sie in der Liste <strong>Warteschlangenname</strong> die Warteschlange aus.</li>
    </ol>
    </li>
    <li>Wenn mit einer bestimmten Bedingung festgelegt werden soll, welcher Warteschlange die Aufgabe zugewiesen wird, führen Sie die folgenden Schritte aus: <ol>
    <li>In der Liste <strong>Warteschlangentyp</strong> wählen Sie <strong>Bedingte Warteschlangen für Arbeitsaufgaben</strong> aus.</li>
    <li>Wählen Sie in der Liste <strong>Warteschlangenname</strong> <strong>Bedingte Warteschlange</strong>aus.</li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] Diese Option wird nur für einige Workflows verwendet, wie z.B. Anfrageverwaltung.</blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. Geben Sie auf der Registerkarte **Zeitlimit** im Feld **Dauer** an, wie viel Zeit dem Benutzer zum Ausführen der Aufgabe zur Verfügung steht. Folgende Optionen stehen zur Auswahl:

    - **Stunden** – Geben Sie die Anzahl der Stunden ein, die der Benutzer zum Ausführen der Aufgabe hat. Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.
    - **Tage** – Geben Sie die Anzahl von Tagen ein, die der Benutzer zum Ausführen der Aufgabe hat. Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.
    - **Wochen** – Geben Sie die Anzahl von Wochen ein, die der Benutzer zum Ausführen der Aufgabe hat.
    - **Monate** – Wählen Sie den Tag und die Woche aus, bis zu dem der Benutzer die Aufgabe ausführen muss. Sie können z. B. angeben, dass der Benutzer bis Freitag der dritten Woche des Monats die Aufgabe ausführen soll.
    - **Jahre** – Wählen Sie den Tag, die Woche und den Monat aus, bis zu dem der Benutzer die Aufgabe ausführen muss. Sie können z. B. angeben, dass der Benutzer bis Freitag der dritten Woche im Dezember die Aufgabe ausführen soll.

    Wenn der Benutzer die Aufgabe nicht innerhalb der vorgesehenen Zeit ausführt, ist die Aufgabe überfällig. Eine überfällige Aufgabe kann basierend auf den im Bereich **Eskalation** der Seite ausgewählten Optionen eskaliert werden.

## <a name="specify-what-happens-when-the-task-is-overdue"></a>Festlegen der Vorgehensweise für überfällige Aufgaben

Wenn ein Benutzer die manuelle Aufgabe nicht innerhalb der vorgesehenen Zeit ausführt, ist die Aufgabe überfällig. Eine überfällige Aufgabe kann eskaliert oder automatisch einem anderen Benutzer zugewiesen werden. Führen Sie die folgenden Schritte aus, um die Aufgabe zu eskalieren, wenn sie überfällig ist.

1. Klicken Sie im linken Bereich auf **Eskalation**.
2. Aktivieren Sie das Kontrollkästchen **Eskalationspfad verwenden**, um einen Eskalationspfad zu erstellen. Die Aufgabe wird automatisch den im Eskalationspfad aufgeführten Benutzern zugewiesen. Die folgende Tabelle stellt z. B. einen Eskalationspfad dar.

    | Sequenz | Eskalationspfad      |
    |----------|----------------------|
    | 1        | Zuweisen zu: Doris     |
    | 2        | Zuweisen zu: Elke      |
    | 3        | Abschließende Aktivität: Ablehnen |

    In diesem Beispiel wird die überfällige Aufgabe Doris zugewiesen. Führt Doris die Aufgabe nicht innerhalb der vorgesehenen Zeit aus, wird die Aufgabe Elke zugewiesen. Führt Elke die Aufgabe nicht innerhalb der vorgesehenen Zeit aus, wird das zur Verarbeitung übermittelte Dokument abgelehnt.

3. Klicken Sie auf **Eskalation hinzufügen**, um dem Eskalationspfad einen Benutzer hinzuzufügen. Wählen Sie auf der Registerkarte **Zuweisungstyp** eine der Optionen der folgenden Tabelle aus, und führen Sie dann die zusätzlichen Schritte für die Option aus, bevor Sie mit Schritt 4 fortfahren.

    <table>
    <thead>
    <tr>
    <th>Mit der folgenden Option...</th>
    <th>Benutzer, denen die Aufgabe eskaliert wird</th>
    <th>Zusätzliche Schritte</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Hierarchie</td>
    <td>Benutzer in einer bestimmten Organisationshierarchie</td>
    <td>
    <ol>
    <li>Nachdem Sie <strong>Hierarchie</strong> auf der Registerkarte <strong>Hierarchieauswahl</strong> in der Liste <strong>Hierarchietyp</strong> ausgewählt haben, wählen Sie den Typ der Hierarchie aus, dem die Aufgabe eskaliert werden soll.</li>
    <li>Vom System muss eine Reihe von Benutzernamen aus der Hierarchie abgerufen werden. Diese Namen stellen Benutzer dar, denen die Aufgabe eskaliert wird. Gehen Sie folgendermaßen vor, um den Anfangs- und Endpunkt des Bereichs von Benutzernamen anzugeben, die vom System abgerufen werden: <ol>
    <li>Wählen Sie zum Angeben eines Startpunkts eine Person in der Liste <strong>Beginn</strong> aus.</li>
    <li>Klicken Sie zum Angeben des Endpunkts auf <strong>Bedingung hinzufügen</strong>. Geben Sie dann eine Bedingung ein, die bestimmt, an welcher Position in der Hierarchie das Abrufen von Namen beendet werden soll.</li>
    </ol>
    </li>
    <li>Geben Sie auf der Registerkarte <strong>Hierarchieoptionen</strong> an, welchen Benutzern im Bereich die Aufgabe eskaliert werden soll: <ul>
    <li><strong>Allen abgerufenen Benutzern zuordnen</strong> – Die Aufgabe wird allen Benutzern im Bereich eskaliert.</li>
    <li><strong>Nur letztem abgerufenen Benutzer zuordnen</strong> – Die Aufgabe wird nur dem letzten Benutzer im Bereich eskaliert.</li>
    <li><strong>Benutzer ausschließen, die die folgenden Bedingung erfüllen</strong> – Diese Aufgabe wird keinem Benutzer im Bereich eskaliert, der eine bestimmte Bedingung erfüllt. Klicken Sie auf <strong>Bedingung hinzufügen</strong>, um die Bedingung anzugeben.</li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Workflowbenutzer</td>
    <td>Benutzer im aktuellen Workflow</td>
    <td>
    <ul>
    <li>Nachdem Sie, <strong>Workflowbenutzer</strong> auf der Registerkarte <strong>Workflowbenutzer</strong>, in der Liste <strong>Workflowbenutzer</strong> ausgewählt haben, wählen Sie einen Benutzer aus, der am Workflow teilnimmt.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Benutzer</td>
    <td>Bestimmte Benutzer</td>
    <td>
    <ol>
    <li>Nachdem Sie <strong>Benutzer</strong>ausegwählt haben, klicken Sie auf die Registerkarte <strong>Benutzer</strong>.</li>
    <li>Die Liste <strong>Verfügbare Benutzer</strong> enthält alle Benutzer. Wählen Sie die Benutzer aus, um die Aufgabe zu eskalieren, und verschieben Sie diese Benutzer dann in die Liste <strong>Ausgewählte Benutzer</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. Geben Sie auf der Registerkarte **Zeitlimit** im Feld **Dauer** an, wie viel Zeit dem Benutzer zum Ausführen der Aufgabe zur Verfügung steht. Folgende Optionen stehen zur Auswahl:

    - **Stunden** – Geben Sie die Anzahl der Stunden ein, die der Benutzer zum Ausführen der Aufgabe hat. Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.
    - **Tage** – Geben Sie die Anzahl von Tagen ein, die der Benutzer zum Ausführen der Aufgabe hat. Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.
    - **Wochen** – Geben Sie die Anzahl von Wochen ein, die der Benutzer zum Ausführen der Aufgabe hat.
    - **Monate** – Wählen Sie den Tag und die Woche aus, bis zu dem der Benutzer die Aufgabe ausführen muss. Sie können z. B. angeben, dass der Benutzer bis Freitag der dritten Woche des Monats die Aufgabe ausführen soll.
    - **Jahre** – Wählen Sie den Tag, die Woche und den Monat aus, bis zu dem der Benutzer die Aufgabe ausführen muss. Sie können z. B. angeben, dass der Benutzer bis Freitag der dritten Woche im Dezember die Aufgabe ausführen soll.

5. Wiederholen Sie die Schritte 3 bis 4 für alle Benutzer, die dem Eskalationspfad hinzugefügt werden sollen. Sie können die Reihenfolge der Benutzer ändern.
6. Wenn die Benutzer im Eskalationspfad die Aufgabe nicht innerhalb der vorgesehenen Zeit ausführen, wird die Aufgabe automatisch bearbeitet. Um die vom System auszuführende Aktivität anzugeben, wählen Sie die Zeile **Aktivität** aus, klicken Sie dann auf die Registerkarte **Aktivität bei Beendigung** und wählen eine Aktivität aus.

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a>Angeben, wann die Aufgabe automatisch bearbeitet wird

Sie können festlegen, dass unter bestimmten Bedingungen die manuelle Aufgabe automatisch bearbeitet wird. Angenommen, eine Aufgabe erfordert, dass ein Mitglied der für Spesenabrechnungen zuständigen Abteilung die zusammen mit einer Spesenabrechnung eingereichten Belege prüft. Entsprechend den Unternehmensrichtlinien muss diese Aufgabe ausgeführt werden, wenn der Gesamtbetrag der Spesenabrechnung 100 Euro überschreitet. In diesem Szenario können Sie das System zur automatischen Markierung der Aufgabe als **Abschließen** konfigurieren, wenn Gesamtbetrag < 100. Gehen Sie folgendermaßen vor, um anzugeben, wann die manuelle Aufgabe automatisch bearbeitet wird.

1. Klicken Sie im linken Bereich auf **Automatische Aktivitäten**.
2. Aktivieren Sie dieses Kontrollkästchen **Automatische Aktivitäten aktivieren**.
3. Klicken Sie auf **Bedingung hinzufügen**.
4. Geben Sie eine Bedingung ein.
5. Geben Sie alle notwendigen zusätzlichen Bedingungen ein.
6. Führen Sie folgende Schritte aus, um die korrekte Konfiguration der eingegebenen Bedingungen zu überprüfen:

    1. Klicken Sie auf **Test**.
    2. Auf der Seite **Workflowbedingung testen** im Bereich **Bedingung überprüfen** wählen Sie einen Datensatz aus.
    3. Klicken Sie auf **Test**. Der Datensatz wird ausgewertet, um zu bestimmen, ob er den festgelegten Bedingungen entspricht.
    4. Klicken Sie auf **OK** oder **Abbrechen**, um zur Seite **Eigenschaften** zurückzukehren.

7. Wählen Sie in der Liste **Aktivität für AutoVervollständigen** die Aktivität aus, die für die Aufgabe ausgeführt werden soll.

## <a name="specify-when-notifications-are-sent"></a>Angeben, wann Benachrichtigungen gesendet werden

Sie können Benachrichtigungen an Personen senden, wenn eine manuelle Aufgabe delegiert, eskaliert, abgeschlossen oder abgelehnt wurde oder eine Änderung für die Aufgabe angefordert wurde. Gehen Sie folgendermaßen vor, um anzugeben, wann und an wen Benachrichtigungen gesendet werden.

1. Klicken Sie im linken Bereich auf **Benachrichtigungen**.
2. Aktivieren Sie das Kontrollkästchen neben den Ereignissen, für die Benachrichtigungen gesendet werden sollen:

    - **Delegieren** – Die Aufgabe wurde einem anderen Benutzer zugewiesen.
    - **Eskalieren** – Der zugewiesene Benutzer hat die Aufgabe nicht innerhalb der vorgesehenen Zeit ausgeführt.
    - **Abschließen** – Der zugewiesene Benutzer hat die Aufgabe ausgeführt.
    - **Ablehnen** – Der zugewiesene Benutzer hat das übermittelte Dokument abgelehnt.
    - **Änderung anfordern** – Der zugewiesene Benutzer eine Änderung des übermittelten Dokuments angefordert hat.

3. Wählen Sie eine Zeile für ein in Schritt 2 ausgewähltes Ereignis aus.
4. Geben Sie im Textfeld auf der Registerkarte **Benachrichtigungstext** den Text der Benachrichtigung ein.
5. Zum Personalisieren der Benachrichtigung können Sie Platzhalter einfügen. Platzhalter werden durch die entsprechenden Informationen ersetzt, wenn die Benachrichtigung Benutzern angezeigt wird. Führen Sie folgende Schritte aus, um einen Platzhalter einzufügen:

    1. Klicken Sie im Textfeld die Position des Platzhalters an.
    2. Klicken Sie auf **Platzhalter einfügen**.
    3. Wählen Sie in der angezeigten Liste den einzufügenden Platzhalter aus.
    4. Klicken Sie auf **Einfügen**.

6. Führen Sie die folgenden Schritte aus, um Übersetzungen von Benachrichtigungen hinzuzufügen:

    1. Klicken Sie auf **Übersetzungen**.
    2. Klicken Sie auf der nun angezeigten Seite auf **Hinzufügen**.
    3. Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.
    4. Geben Sie den Text im Feld **Übersetzter Text** ein.
    5. Um den Text zu personalisieren, können Platzhalter, wie in Schritt 5 beschrieben, eingefügt werden.
    6. Klicken Sie auf **Schließen**.

7. Auf der Registerkarte **Empfänger** geben Sie an, an wen die Benachrichtigungen gesendet werden. Wählen Sie eine der Optionen in der folgenden Tabelle aus, und führen Sie dann die zusätzlichen Schritte für diese Option aus, bevor Sie mit Schritt 8 fortfahren.

    <table>
    <thead>
    <tr>
    <th>Mit der folgenden Option...</th>
    <th>Empfänger der Benachrichtigung</th>
    <th>Zusätzliche Schritte</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Teilnehmer</td>
    <td>Benutzer, die einer bestimmten Gruppe oder Rolle zugewiesen sind</td>
    <td>
    <ol>
    <li>Nachdem Sie <strong>Teilnehmer</strong> auf der Registerkarte <strong>Rollenbasiert</strong> in der Liste <strong>Art von Teilnehmer</strong> ausgewählt haben, wählen Sie den Typ der Gruppe oder der Rolle aus, dem die Benachrichtigung gesendet werden soll.</li>
    <li>Wählen Sie in der Liste <strong>Teilnehmer</strong> die Gruppe oder Rolle aus, an die Benachrichtigungen gesendet werden sollen.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Workflowbenutzer</td>
    <td>Benutzer im aktuellen Workflow</td>
    <td>
    <ul>
    <li>Nachdem Sie, <strong>Workflowbenutzer</strong> auf der Registerkarte <strong>Workflowbenutzer</strong>, in der Liste <strong>Workflowbenutzer</strong> ausgewählt haben, wählen Sie einen Benutzer aus, der am Workflow teilnimmt.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Benutzer</td>
    <td>Bestimmte Benutzer</td>
    <td>
    <ol>
    <li>Nachdem Sie <strong>Benutzer</strong>ausegwählt haben, klicken Sie auf die Registerkarte <strong>Benutzer</strong>.</li>
    <li>Die Liste <strong>Verfügbare Benutzer</strong> enthält alle Benutzer. Wählen Sie die Benutzer aus, an die Benachrichtigungen gesendet werden sollen, und verschieben Sie diese Benutzer dann in die Liste <strong>Ausgewählte Benutzer</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. Wiederholen Sie die Schritte 3 bis 7 für jedes in Schritt 2 ausgewählte Ereignis.

## <a name="set-a-time-limit"></a>Festlegen einer Zeitgrenze

Gehen Sie folgendermaßen vor, wenn die manuelle Aufgabe in einer bestimmten Zeit abgeschlossen werden muss.

> [!NOTE]
> Die hier ausgewählten Optionen setzen die Optionen außer Kraft, die Sie in den Bereichen **Zuweisung**und **Eskalation** der Seite auswählen.

1. Klicken Sie im linken Bereich auf **Erweiterte Einstellungen**.
2. Aktivieren Sie das Kontrollkästchen **Zeitgrenze für das Workflowelement festlegen**.
3. Legen Sie im Feld **Dauer** fest, wann die Aufgabe abgeschlossen sein muss. Folgende Optionen stehen zur Auswahl:

    - **Stunden** – Geben Sie die Anzahl der Stunden ein, in denen die Aufgabe ausgeführt sein muss. Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.
    - **Tage** – Geben Sie die Anzahl von Tagen ein, in denen die Aufgabe ausgeführt sein muss. Wählen Sie dann den Kalender aus, den Ihre Organisation verwendet, und geben Sie Informationen zur Arbeitswoche der Organisation ein.
    - **Wochen** – Geben Sie die Anzahl von Wochen ein, in denen die Aufgabe ausgeführt sein muss.
    - **Monate** – Wählen Sie den Tag und die Woche aus, bis zu dem die Aufgabe ausgeführt sein muss. Sie können z. B. angeben, dass die Aufgabe bis Freitag der dritten Woche des Monats abgeschlossen sein soll.
    - **Jahre** – Wählen Sie den Tag, die Woche und den Monat aus, bis zu dem die Aufgabe ausgeführt sein muss. Sie können z. B. angeben, dass die Aufgabe bis Freitag der dritten Woche im Dezember ausgeführt sein soll.

4. Wenn die Zeitgrenze überschritten wird, wird die Aufgabe bearbeitet. Wählen Sie in der Liste **Aktivität** die Aktivität aus, die vom System ausgeführt werden soll.

## <a name="specify-which-actions-are-available-to-the-user"></a>Angeben der verfügbaren Aktivitäten für den Benutzer

Wenn die manuelle Aufgabe einem Benutzer zugewiesen wird, muss der Benutzer die Aufgabe bearbeiten. Gehen Sie folgendermaßen vor, um anzugeben, welche Aktivitäten der Benutzer für die Aufgabe ausführen kann.

> [!NOTE]
> Die verfügbaren Aktivitäten unterscheiden sich abhängig davon, wie die Aufgabe entworfen wurde.

1. Klicken Sie im linken Bereich auf **Erweiterte Einstellungen**.
2. Aktivieren Sie das Kontrollkästchen **Abgeschlossen**, wenn der Benutzer in der Lage sein soll, die Aufgabe als **Abgeschlossen** zu markieren.
3. Aktivieren Sie das Kontrollkästchen **Ablehnen**, wenn der Benutzer in der Lage sein soll, das übermittelte Dokument abzulehnen.
4. Aktivieren Sie das Kontrollkästchen **Änderung anfordern**, wenn der Benutzer in der Lage sein soll, Änderungen des übermittelten Dokuments anzufordern.
5. Aktivieren Sie das Kontrollkästchen **Delegieren**, wenn der Benutzer in der Lage sein soll, die Aufgabe einem anderen Benutzer zuzuweisen.
6. Aktivieren Sie das Kontrollkästchen **Neu zuordnen**, wenn der Benutzer in der Lage sein soll, die Aufgabe einem anderen Benutzer in der Warteschlange für Arbeitsaufgaben neu zuzuweisen.
7. Aktivieren Sie das Kontrollkästchen **Freigeben**, wenn der Benutzer in der Lage sein soll, die Aufgabe der Warteschlange für Arbeitsaufgaben neu zuzuweisen. Ein anderer Benutzer kann die Aufgabe anschließend ausführen.
