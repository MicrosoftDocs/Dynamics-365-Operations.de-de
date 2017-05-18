---
title: "Vor kurzem hinzugefügte Aufgabenaufzeichnungsfunktionen"
description: "Wenn Sie Aufgabenaufzeichnung verwenden, um Aufgabenleitfäden zu erstellen, können Sie die Dateien mithilfe der Funktionen, die in diesem Thema beschrieben werden, noch effizienter beschreiben."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core
ms.custom: 266464
ms.assetid: b4640e67-4b92-4855-8041-1bfc71aadc47
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 3be54879494948f75b192fcc22239b9064173220
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="recently-added-editing-features-in-task-recorder"></a>Vor kurzem hinzugefügte Aufgabenaufzeichnungsfunktionen

[!include[banner](../includes/banner.md)]


Wenn Sie Aufgabenaufzeichnung verwenden, um Aufgabenleitfäden zu erstellen, können Sie die Dateien mithilfe der Funktionen, die in diesem Thema beschrieben werden, noch effizienter beschreiben.

Diese Funktionen sind im Menü **Einstellungen &gt; Aufgabenaufzeichnung &gt; Aufzeichnung bearbeiten** verfügbar.

-   Einfügen von Schritte, ohne die gesamte Datei neu aufzuzeichen.
-   Verschieben von Schritten in eine Unteraufgabe, ohne die gesamte Datei neu aufzuzeichnen.
-   Aufzeichnungsname und -beschreibung-Felder minimieren.

## <a name="insert-steps-without-rerecording-the-entire-file"></a>Einfügen von Schritte, ohne die gesamte Datei neu aufzuzeichen.
Sie können einen beliebigen Stelle in einem Schritt Aufgabenleitfaden nun hinzufügen, ohne nach wiederzugeben oder die gesamte überspielen Datei an.

1.  Wählen Sie den Schritt aus, wenn nicht ausgegebene den neuen Schritt eingefügt werden. Stellen Sie sicher, dass der Schritt hervorgehoben wird.

Damit Aufgabenaufzeichnung einfügt einen Schritt, müssen Sie die korrekte offene Seite haben. Die korrekte Seite ist die Seite, auf der der neue Schritt auftritt. Aufgabenaufzeichnung hat den Mechanismus, der bestimmt, wofür die aktive, Seite ist, und die Funktion deaktivieren wird, wenn der richtige Seite nicht offen ist. 

[![tg1](./media/tg1.png)](./media/tg1.png) 


Wenn Sie auf der korrekten Seite sind, wird **Schritt einfügen** verfügbar.

[![tg2](./media/tg2-231x300.png)](./media/tg2.png)

2. Klicken Sie auf **Schritt einfügen**.

Wenn Sie auf **Schritt einfügen** klicken, schaltet die Aufgabenaufzeichnung in den Aufzeichnungsmodus. Jede Aktivität in der Benutzeroberfläche wird nun erfasst und nachträgliche als Schritte hinzugefügt.

3. Klicken Sie auf **Stop**

Sie können den Prozess überprüfen, nach Schritten hinzufügen oder nach Bedarf nach außerdem verschieben (siehe unten außerdem für).

4. Wenn Sie die Aufgabenleitfaden Bearbeitung fertig ist, klicken Sie auf **Bearbeitung fertig**, und wählen Sie dann eine der Optionen, die Aufgabenleitfaden zu speichern oder zu veröffentlichen aus.

## <a name="move-steps-under-a-subtask-without-rerecording-the-entire-file"></a>Verschieben von Schritten in eine Unteraufgabe, ohne die gesamte Datei neu aufzuzeichnen.
Sie können Schritte in eine Unteraufgabe veschieben, ohne die gesamte Datei abzuspielen neu aufzuzeichnen. Sie können den Unteraufgabenschritt oder den End-Unteraufgabenschritt auch verschieben, wenn Sie einen vorhandenen Block Schritte zusammenfassen möchten.

1.  Markieren Sie den Schritt oder Unteraufgabenschritt, der verschoben werden soll. Stellen Sie sicher, dass der Schritt hervorgehoben wird.
2.  Klicken Sie auf die Auslassungspunkte, klicken Sie **Schritt nach verschieben**.

[![tg3](./media/tg3.png)](./media/tg3.png)

3. Wählen den Schritt oder Unteraufgabenschritt aus, dem der Schritt Unteraufgabenschritt nachfolgend oder verschieben möchten. Die Aufgabenaufzeichnung verschiebt den Schritt.

4. Um den End-Unteraufgabenschritt zu verschieben, markieren Sie diesen, klicken Sie auf die Auslassungspunkte, nach **Schritt nach verschieben** und wählen Sie dann den gewünschten aus Schritt nach den End-Unteraufgabenschritt sein.

Wenn Sie der erste Schritt im Aufgabenleitfaden für eine Unteraufgabe werden soll, erstellen Sie einen Unteraufgabenschritt als zweite der Schritt, und verschieben Sie dann der erste Schritt in ihn. Sie können beliebig viele außerdem Schritte oder nach Bedarf hinzufügen oder verschieben.

5. Wenn Sie die Aufgabenleitfaden Bearbeitung fertig ist, klicken Sie auf **Bearbeitung fertig**, und wählen Sie dann eine der Optionen, die Aufgabenleitfaden zu speichern oder zu veröffentlichen aus.

## <a name="collapse-recording-name-and-description"></a>Aufzeichnungsname und Beschreibung minimieren.
Sie können **Aufzeichnungsname**und **Aufzeichnungsbeschreibung** Felder erweitern bzw. reduzieren. Wenn diese Felder reduziert werden, sind weitere Schritte im Aufgabenaufzeichnungsbearbeitungsbereich angezeigt. 

[![tg4](./media/tg4-300x252.png)](./media/tg4.png)  

<a name="see-also"></a>Siehe auch
--------

[Dokumentation oder Schulungen mithilfe von"Aufgabenaufzeichnungen" erstellen](/dynamics365/operations/dev-itpro/user-interface/task-recorder)

[Aufgabenaufzeichnungskurzübersicht](/dynamics365/operations/dev-itpro/user-interface/task-recorder-quick-reference)




