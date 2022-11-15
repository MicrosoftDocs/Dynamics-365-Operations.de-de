---
title: Aufgaben in der Aufgabeverwaltung einrichten
description: In diesem Artikel wird erläutert, wie Sie Aufgaben in der Aufgabenverwaltung in Microsoft Dynamics 365 Human Resources einrichten.
author: twheeloc
ms.date: 10/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-06-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6a38cc2e36c24ddbfe0d8b2886301c108599ab25
ms.sourcegitcommit: 55e440e30490b2d36d86b22aa1263d5da97633aa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745387"
---
# <a name="set-up-tasks-in-task-management"></a>Aufgaben in der Aufgabeverwaltung einrichten

[!INCLUDE [PEAP](../includes/peap-1.md)]

In Versionen von Microsoft Dynamics 365 Human Resources vor Version 10.0.30 mussten Benutzer, die eine Aufgabe bearbeiten wollten, diese Aufgabe auf jeder Checkliste, die sie enthielt, einzeln bearbeiten. Ab Human Resources Version 10.0.30 können Benutzer jedoch auswählen, wie bearbeitete Aufgaben gehandhabt werden. Wenn sich eine Aufgabe, die bearbeitet wird, auf einer Checkliste befindet, muss die **Upgrade der Aufgabenverwaltung aktivieren** Option muss auf der Registerkarte **Aufgabenmanagement** der Seite **Gemeinsame Parameter der Personalabteilung** ausgewählt werden, damit die Checkliste die bearbeitete Aufgabe verwenden kann.

[![Aktivieren Sie die Upgrade-Option für die Aufgabenverwaltung auf der Seite Gemeinsame Parameter der Personalabteilung.](./media/task-update.png)](./media/task-update.png)

Wenn Änderungen an Aufgaben auf alle zugeordneten Checklistenaufgaben angewendet werden sollen, muss bereits eine Beziehung zwischen der Aufgabe in der Aufgabenbibliothek und der Aufgabe auf der Checkliste bestehen. Es wurde eine Option hinzugefügt, um die Beziehung zwischen der Bibliotheksaufgabe und der Checklistenaufgabe herzustellen.

Sie können Aufgaben einzeln erstellen und diese dann in mehreren Checklisten wiederverwenden. Um eine Aufgabe zu erstellen, wählen Sie auf der **Onboarding-Setup**-Seite auf der **Aufgaben**-Registerkarte **Neu** aus.

## <a name="set-up-tasks"></a>Aufgaben einrichten

Um eine erstellte Aufgabe mehreren Prüflisten zuzuweisen, wählen Sie die Aufgabe aus und wählen dann **Auf Prüflisten anwenden** im Menü aus.

Alternativ können Sie Aufgaben direkt zu einer Checkliste hinzufügen. Um eine Aufgabe zu einer Checkliste hinzuzufügen, erstellen Sie auf der Seite **Onboarding-Setup** auf der **Checkliste**-Registerkarte entweder eine neue Checkliste, um die Aufgabe hinzuzufügen, oder fügen Sie die Aufgabe zu einer vorhandenen Checkliste hinzu.

Um eine Aufgabenbibliothek zu bearbeiten, wählen Sie **Bearbeiten** im Aufgabenbibliotheksmenü aus. Wenn die Aufgabe mit Prüflisten verknüpft ist, werden diese Prüflisten auf der **Aufgabe bearbeiten**-Seite angezeigt. Wenn Sie möchten, dass die Aufgaben in allen Prüflisten mit den Änderungen aktualisiert werden, wählen Sie diese Prüflisten im Bereich **Auf Prüflisten anwenden** aus.

Um Aufgaben aus der Bibliothek zu löschen, wählen Sie **Löschen**. Wenn die Aufgabe mit einer Prüfliste verknüpft ist, wird diese Aktion die Aufgabe nicht aus der Prüfliste löschen. Um eine Aufgabe aus einer Checkliste zu entfernen, ist eine separate Aktion erforderlich.

### <a name="set-up-checklists"></a>Einrichten von Checklisten

Eine Checkliste ist eine Gruppe von Aufgaben. Sie können beliebig viele Checklisten erstellen und dieselben Aufgaben mehreren Checklisten zuweisen. Wenn Sie eine Checkliste erstellen, geben Sie einen Besitzer und einen Kalender an.

Um eine neue Aufgabe auf einer Prüfliste anzulegen, wählen Sie **Ne** auf der Aufgaben-Menüleiste. Wenn Sie eine neue Aufgabe erstellen, können Sie diese Aufgabe optional hinzufügen, sodass sie von mehreren Prüflisten gemeinsam genutzt werden kann. Um die Aufgabe zur Aufgabenbibliothek hinzuzufügen, muss die **Aufgabe auf Bibliothek anwenden**-Option auf **Ja** eingestellt ist. Wenn Sie die Aufgabe zur Aufgabenbibliothek hinzufügen, können Sie die Aufgabe auch gleichzeitig zu anderen Prüflisten hinzufügen, indem Sie diese Prüflisten im Abschnitt **Auf Prüflisten anwenden** auswählen. Wenn Sie die Aufgabe nicht zur Aufgabenbibliothek hinzufügen möchten, ist die Aufgabe nur in der Prüfliste vorhanden, in der Sie sie erstellen.

Um eine Aufgabe in einer Prüfliste zu bearbeiten, wählen Sie **Bearbeiten** im Aufgabenmenü aus. Wenn die Aufgabe mit Prüflisten verknüpft ist, werden diese Prüflisten auf der **Aufgabe bearbeiten**-Seite angezeigt. Wenn Sie möchten, dass die Aufgaben in allen anderen Prüflisten mit den Änderungen aktualisiert werden, wählen Sie diese Prüflisten im Bereich **Auf Prüflisten anwenden** aus.

Um Aufgaben aus einer Prüfliste zu entfernen, wählen Sie **Entfernen**. Diese Aktion entfernt die Aufgaben aus der Prüfliste. Die Aufgaben aus der Aufgabenbibliothek werden jedoch nicht gelöscht. Um Aufgaben aus der Bibliothek zu löschen, öffnen Sie die Seite **Aufgabenbibliothek** und wählen Sie **Löschen**.
