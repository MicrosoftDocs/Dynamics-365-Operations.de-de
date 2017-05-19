---
title: Konfigurieren einer automatisierten Aufgabe in einem Workflow
description: "Dieses Thema erläutert, wie Sie die Eigenschaften einer automatisierten Aufgabe konfigurieren können."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 6b244dcd6d00e065c5ce7f6707078e3665c8b368
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="configure-an-automated-task-in-a-workflow"></a>Konfigurieren einer automatisierten Aufgabe in einem Workflow

[!include[banner](../includes/banner.md)]


Dieses Thema erläutert, wie Sie die Eigenschaften einer automatisierten Aufgabe konfigurieren können.

Klicken Sie zum Konfigurieren einer automatisierten Aufgabe im Workflow-Editor mit der rechten Maustaste auf die Aufgabe, und klicken Sie dann auf **Eigenschaften**, umdie Seite **Eigenschaften** zu öffnen. Verwenden Sie dann die folgenden Verfahren, um die Eigenschaften der automatisierten Aufgabe zu konfigurieren.

## <a name="name-the-task"></a>Benennen der Aufgabe
Gehen Sie folgendermaßen vor, um einen Namen für die automatisierte Aufgabe einzugeben.

1.  Klicken Sie im linken Bereich auf **Grundeinstellungen**.
2.  Geben Sie im Feld **Name** einen eindeutigen Namen für die Aufgabe ein.

## <a name="specify-when-notifications-are-sent"></a>Angeben, wann Benachrichtigungen gesendet werden
Sie können Benachrichtigungen an Personen senden, wenn eine automatisierte Aufgabe ausgeführt oder abgebrochen wurde. Gehen Sie folgendermaßen vor, um anzugeben, wann und an wen Benachrichtigungen gesendet werden.

1.  Klicken Sie im linken Bereich auf **Benachrichtigungen**.
2.  Aktivieren Sie das Kontrollkästchen neben den Ereignissen, für die Benachrichtigungen gesendet werden sollen.
    -   **Ausführung** – Benachrichtigungen werden gesendet, wenn die Aufgabe ausgeführt wurde.
    -   **Abgebrochen** – Benachrichtigungen werden gesendet, wenn die Aufgabe abgebrochen wurde.

3.  Wählen Sie eine Zeile für ein in Schritt 2 ausgewähltes Ereignis aus.
4.  Geben Sie im Textfeld auf der Registerkarte **Benachrichtigungstext** den Text der Benachrichtigung ein.
5.  Zum Personalisieren der Benachrichtigung können Sie Platzhalter einfügen. Platzhalter werden durch die entsprechenden Daten ersetzt, wenn die Benachrichtigung Benutzern angezeigt wird. Führen Sie folgende Schritte aus, um einen Platzhalter einzufügen:
    1.  Klicken Sie im Textfeld die Position des Platzhalters an.
    2.  Klicken Sie auf **Platzhalter einfügen**.
    3.  Wählen Sie in der angezeigten Liste den einzufügenden Platzhalter aus.
    4.  Klicken Sie auf **Einfügen**.

6.  Führen Sie die folgenden Schritte aus, um Übersetzungen von Benachrichtigungen hinzuzufügen:
    1.  Klicken Sie auf **Übersetzungen**.
    2.  Klicken Sie auf der nun angezeigten Seite auf **Hinzufügen**.
    3.  Wählen Sie in der angezeigten Liste die Sprache aus, in der Sie den Text eingeben.
    4.  Geben Sie den Text im Feld **Übersetzter Text** ein.
    5.  Um den Text zu personalisieren, können Platzhalter, wie in Schritt 5 beschrieben, eingefügt werden.
    6.  Klicken Sie auf **Schließen**.

7.  Auf der Registerkarte **Empfänger** geben Sie an, an wen die Benachrichtigungen gesendet werden. Wählen Sie eine der Optionen in der folgenden Tabelle aus, und führen Sie dann die zusätzlichen Schritte für diese Option aus, bevor Sie mit Schritt 8 fortfahren.
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
    <td>Teilnehmer</td>
    <td>Benutzer, die einer bestimmten Gruppe oder Rolle zugewiesen sind</td>
    <td><ol>
    <li>Nachdem Sie <strong>Teilnehmer</strong> auf der Registerkarte <strong>Rollenbasiert</strong> in der Liste <strong>Art von Teilnehmer</strong> ausgewählt haben, wählen Sie den Typ der Gruppe oder der Rolle aus, dem die Benachrichtigung gesendet werden soll.</li>
    <li>Wählen Sie in der Liste <strong>Teilnehmer</strong> die Gruppe oder Rolle aus, an die Benachrichtigungen gesendet werden sollen.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Workflowbenutzer</td>
    <td>Benutzer, die am aktuellen Workflow teilnehmen</td>
    <td><ul>
    <li>Nachdem Sie, <strong>Workflowbenutzer</strong> auf der Registerkarte <strong>Workflowbenutzer</strong>, in der Liste <strong>Workflowbenutzer</strong> ausgewählt haben, wählen Sie einen Benutzer aus, der am Workflow teilnimmt.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Benutzer</td>
    <td>Bestimmte Benutzer von Microsoft Dynamics 365 for Operations</td>
    <td><ol>
    <li>Nachdem Sie <strong>Benutzer</strong>ausegwählt haben, klicken Sie auf die Registerkarte <strong>Benutzer</strong>.</li>
    <li>Die Liste I<strong>Verfügbare Benutzer</strong> enthält die Liste aller Benutzer für Dynamics 365 for Operations. Wählen Sie die Benutzer aus, an die Benachrichtigungen gesendet werden sollen, und verschieben Sie diese Benutzer dann in die Liste <strong>Ausgewählte Benutzer</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  Wiederholen Sie die Schritte 3 bis 7 für jedes in Schritt 2 ausgewählte Ereignis.





