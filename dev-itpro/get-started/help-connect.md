---
title: Verbinden des Hilfesystems
description: "Dieses Thema beschreibt die Komponenten des Hilfesystems für Microsoft Dynamics 365 und enthält einen Überblick, wie sie verbunden und benutzerdefinierte Hilfen erstellt werden können."
author: margoc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 5ac5e30cff2239f601778001368fa7aaba478f5c
ms.lasthandoff: 03/31/2017


---

# <a name="connect-the-help-system"></a>Verbinden des Hilfesystems

In diesem Thema werden die Komponenten des Hilfesystems für Microsoft Dynamics 365 für Arbeitsgänge. Es bietet einen Überblick darüber, wie diese Komponenten und eine Zusammenfassung zu aus, wie Sie benutzerdefinierte Hilfe erstellt. 

<a name="help-architecture"></a>Hilfearchitektur
-----------------

Die folgende Abbildung zeigt Teile des Dynamics 365 für Arbeitsgangs-Hilfesystem angezeigt. Das im Produkt enthaltenen Hilfesystem übernehmen Artikel vom Dynamics 365 für Arbeitsgangsstandort https://docs.microsoft.com auf sowie die Aufgabenleitfäden, die, die im Geschäftsprozessmodellierer in den Lebenszyklus-Dienstleistungen (LCS) gespeichert werden. 
** Hinweis: ** Die Funktionen, die im Diagramm mit einem Sternchen (\*) aufgeführt werden geplant, aber noch nicht verfügbar. [![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Verbindung des Hilfesystems
Verwenden der Seite ** Systemparameter ** schließen die Systemadministratoren Stück des Hilfesystems für einer Implementierung angezeigt. [Systemparameterformular ![mit Hilfeeinstellungen] ". /media/system-parameters_ops-1024x437.png)]". /media/system-parameters_ops.png) Auf Bundesebene ** Systemparameter ** Seite, gehen folgendermaßen vor:

1.  ** Wichtig: ** Das erste Mal öffnen Sie die Hilfe ** ** Registerkarte, Sie müssen mit Lebenszyklus-Dienstleistungen herstellen. Vergewissern Sie sich, auf den Link mitten in im Formular auf, warten Sie auf die Verknüpfung, schließen Sie das Dialogfeld, und klicken Sie anschließend auf OK ** ** die der ** Systemparameter ** Seite des Bruttobetrags. [! [Verbinden mit Kreditbriefen] angezeigt. (/media/connect-to-lcs-crop-1024x365.png "Verbinden mit Kreditbriefen" angezeigt)]". /media/connect-to-lcs-crop.png)
2.  Wählen Sie das Projekt Lifecycle Services, um eine Verbindung herzustellen.
3.  Wählen Sie die BPM-Bibliotheken (innerhalb des ausgewählten Projekts) aus, von denen Sie die Aufgabenaufzeichnungen abrufen wollen.
4.  Wählen Sie die Anzeigereihenfolge der BMP-Bibliotheken aus. So können Sie bestimmen, in welcher Reihenfolge Aufgabenaufzeichnungen aus den Bibliotheken im Bereich **Hilfe** angezeigt werden.

Nachdem Sie diese Schritte abgeschlossen haben, können Sie den Bereich **Hilfe** öffnen und auf die Registerkarte **Aufgabenleitfäden** klicken. Sie finden nun die Aufgabenhandbücher, die für die Seite gelten, an denen Sie derzeit in Dynamics 365 for Operations sind. Wenn keine Aufgabenhandbücher gefunden werden, können Sie Schlüsselwörter eingeben, um die Suche genauer zu definieren.

### <a name="showing-translated-task-guides"></a>Zeigt übersetzte Aufgabenleitfäden

Aufgabenleitfäden Übersetzte wurden zuerst in die APQC vereinheitlichte Bibliothek im Mai 2016 und die momentan Schritte-Bibliothek versendet. Um lokalisierte Aufgabenleitfäden in Microsoft Dynamics 365 for Operations anzuzeigen, stellen Sie sicher, dass die mit der Mai-Bibliothek verbunden sind. Die Sprache, die ein Aufgabenleitfaden in verwendet, wird für jeden Benutzer durch die Spracheinstellungen unter ** Optionen ** ** Einstellungen &gt; gesteuert **. **Hinweis:** Auch wenn viele Aufgabenleitfäden übersetzt wurden, zeigt der Dynamics 365 for Operations-Client im Moment nicht die übersetzten Namen der Aufgabenleitfäden an. Zudem wird nur für die Aufgabenleitfäden, die im Februar 2016 freigegeben wurden, werden bei der Umwandlung in der Mai-Bibliothek verfügbar. Wir werden eine aktualisierte Bibliothek mit zusätzlichen Übersetzung veröffentlichen.

-   Wenn ein Aufgabenleitfaden übersetzt wurde, wird beim Öffnen der gesamte Text des Leitfadens in der ausgewählten Sprache angezeigt.
-   Wenn ein Aufgabenleitfaden noch nicht übersetzt wurde, wird beim Öffnen nur ein Teil des Texts (der Text der Steuerelemente) in der ausgewählten Sprache angezeigt.

## <a name="creating-custom-help"></a>Erstellen einer benutzerdefinierten Hilfe
Sie können eine benutzerdefinierte Hilfe für Ihre Implementierung von Dynamics 365 for Operations erstellen, indem Sie Aufgabenaufzeichnungen erstellen, die die Implementierung widerspiegeln, und diese in einer LCS Business Process Library speichern. Wenn Partner eine Bibliothek auf eine Unternehmensbibliothek hochstufen und in eine Lösung aufnehmen, wir diese für die Kunden verfügbar. Sie können eine Kopie der globalen APQC Unified Bibliothek für Dynamics AX erstellen und dann Ihre Kopie öffnen, Aufgabenaufzeichnungen aus dieser öffnen, sie ändern und dann Aufzeichnungen mit den Änderungen speichern. Weitere Informationen finden Sie [wie eine Aufgabenaufzeichnung erstellt, das als Dokumentation oder Schulung zu verwenden.] ". /user-interface/task-recorder.md).

<a name="see-also"></a>Siehe auch
--------

[Help overview](help-overview.md)

[]( Aufgabenaufzeichnungsüberblick .. /user-interface/task-recorder.md)

[Wie Sie Aufgabenaufzeichnungen zu Dokumentations- und Schulungszwecken erstellen](../user-interface/task-recorder-training-docs.md)

[Neue Trainings-Bibliotheken für Dynamics 365 für Arbeitsgänge innerhalb der Lebenszyklus- mithilfe der Aufgabenaufzeichnung (externer Link) Erstellen]https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax) "


