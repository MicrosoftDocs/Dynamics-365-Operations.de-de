---
title: "Fragebögen verteilen und abschließen"
description: "In diesem Thema wird erläutert, wie Sie die Fragebögen verteilen, die von Entwurf, sodass sie der Person oder die Personengruppe fest verfügbar sind, die sie ausführen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a76ec0cd86bcc810b42ae3cd8efd8a584e6c4da3
ms.openlocfilehash: 8e09c6b042d557e3b2d608fb5e278169fc3c1d88
ms.lasthandoff: 03/31/2017


---

# <a name="distribute-and-complete-a-questionnaire"></a>Fragebögen verteilen und abschließen

In diesem Thema wird erläutert, wie Sie die Fragebögen verteilen, die von Entwurf, sodass sie der Person oder die Personengruppe fest verfügbar sind, die sie ausführen. 

Es gibt mehrere Möglichkeiten, einen Fragebogen zu verteilen:

-   Markieren Sie den Fragebogen als aktiv. Der Fragebogen ist für alle Mitarbeiter verfügbar, sofern keine Fragebogengruppe eingerichtet wird, um den Zugriff auf den Fragebogen zu beschränken.
-   Zuweisen von Rechten zu einer Fragebogengruppe. Der Fragebogen ist dann für alle Mitglieder der ausgewählten Gruppe verfügbar.
-   Erstellen von geplanten Antwortsitzungen. Der Fragebogen steht dann für eine bestimmte Person zur Verfügung.
-   Zeitplan erstellen. Der Fragebogen kann dann für mehrere Personen verfügbar sein.

## <a name="marking-a-questionnaire-as-active"></a>Markieren eines Fragebogens als aktiv
Mit dem ** aktiv ** Feld auf Ja ** ** auf der Seite ** ** Fragebögen festlegen, starten Sie den Fragebogen zur Verfügung, sodass alle Mitarbeiter ausführen. Die Befragungsteilnehmer können den Fragebogen ausfüllen mehrmals. Diese Funktionalität ist hilfreich, wenn Sie ständige Rückmeldung für das ganze Jahr gesammelt werden sollen. So können Sie beispielsweise einen Fragebogen erstellten, über den die Mitarbeiter ein Feedback zum Mittagessen in der Cafeteria abgeben können.

## <a name="questionnaire-groups"></a>Fragebogengruppen
Sie können Fragebogengruppen einrichten und die Befragten einbeziehen, für die ein Fragebogen verteilt werden soll. 

Sie können Fragebogengruppen von den folgenden Seiten erstellen:

-   **Fragebogengruppen** – Nur Personen innerhalb einer Fragebogengruppe können einen ausgewählten Fragebogen ausfüllen. Wenn beispielsweise die gewünschte Zielgruppe "Auftragnehmer" ist, können Sie eine Fragebogengruppe erstellen, die für diese Teilnehmer spezifisch ist.
-   **Fragebogengruppenmitglieder** – Mithilfe dieses Formulars können Sie Personen zu Fragebogengruppen hinzufügen.

Um eine Fragebogengruppe einem Fragebogen darüber, welche Fragebögen ** ** Seite zuweisen, um Benutzerrechte ** **. Nachdem der Fragebogen gespeichert ist, z aktiv, können die Mitglieder der Fragebogengruppe den Fragebogen ausfüllen. Diese Funktion ist hilfreich, wenn Sie eines Fragebogen auf einer Auswählensgruppe von Personen testen möchten, bevor Sie diese in einer - Gruppe oder zurücksetzen, wenn Sie dem Ziel einen Fragebogen einer Zielgruppe sehr bestimmten soll.

## <a name="planned-answer-sessions-in-a-questionnaire"></a>Geplante Beantwortungssitzung in einem Fragebogen
Geplante Antwortsitzungen sind Fragebogen, die Sie entwickelt und für die Sie die Befragten ausgewählt haben. 

**Hinweis:** Bevor Sie geplante Antwortsitzungen einrichten können, müssen Sie einen Fragebogen entwerfen. 

Auf der Seite **Geplante Antwortsitzung** können Sie eine geplante Antwortsitzung für einen einzelnen Mitarbeiter erstellen. In der Liste auf der Seite werden alle geplanten Fragebögen angezeigt. 

Geplante Antwortsitzungen werden auch auf der Seite **Zeitpläne für Fragebögen** verwendet, in dem Sie Fragebögen für mehrere Personen planen können:

-   Mitarbeiter
-   Kursteilnehmer
-   Organisationseinheiten

Jede Person kann den Fragebogen nur einmal beantworten.

## <a name="scheduling-a-questionnaire"></a>Planung eines Fragebogens
Sie können einen Fragebogen optional für mehrere Befragungsteilnehmer planen.

### <a name="planning-types"></a>Planungstypen

Planungstypen werden benötigt, wenn Sie geplante Antwortsitzungen für mehrere Befragungsteilnehmer planen möchten. Planungstypen werden verwendet, um Fragebogenzeitpläne zu klassifizieren. Beispielsweise können Sie Fragebögen für folgende Zwecke planen:

-   Beurteilung
-   Umfrage
-   Testen

Sie können Planungstypen für einen Fragebogenzeitplan auf der Seite **Zeitpläne für Fragebögen** angeben.

### <a name="reference-types-for-questionnaire"></a>Referenztypen für Fragebögen

Sie können Referenztypen verwenden, um Kriterien für die Auswahl von Befragungsteilnehmern einzugeben, wenn Sie einen Fragebogen terminieren. 

Verwenden Sie die **Referenztypen**-Seite, um Referenztypen für einen Fragebogen einzurichten. Jeder Referenztyp für eine Tabelle in Microsoft Dynamics 365 für Arbeitsgänge. Wenn Sie Zeitpläne für Fragebögen erstellen, können Sie einzelne Datensätze in der Tabelle oder einen Datensatzbereich angeben, denen bzw. dem der Fragebogen zugeordnet wird. 

Wenn Sie beispielsweise die Tabelle Kurse auswählen, können Sie entscheiden, für welchen Kurs der Fragebogen verwendet werden soll. Wenn Sie einen Referenztyp für die Kurstabelle einrichten, sind einige Felder und Schaltflächen auf der Seite **Kurse** verfügbar.

### <a name="questionnaire-schedules"></a>Zeitpläne für Fragebögen

Sie können Fragebogenzeitpläne verwenden, um mehrere geplante Antwortsitzungen für eine Benutzergruppe, auf Grundlage eines Referenztyps zu generieren. Dient zum Erstellen eines Zeitplans für die Fragebogenzeitpläne ** ** Seite. Wählen Sie den Planungstyp aus, um den Zeitplan zum Kategorisieren, und wählen Sie auch den Referenztyp auswählen, der verwendet werden soll, um das System für bestimmte Benutzer abgefragt werden. Wenn Sie z legen den Referenztyp auf die Kurse Tabelle, Sie einen bestimmten Kurs im Feld Referenz ** ** Feld auswählen können. 

Klicken Sie auf **Einstellungsdetails**, um den Fragebogen und andere Kriterien auszuwählen. Geben Sie beispielsweise den Namen des Kursleiters als Kriterium angezeigt, nachdem der Fragebogen eine Bewertung des Kursleiters ist. Nachdem Sie abschließend, den Einrichtungsdetails eingeben, generiert das System geplanten Antwortsitzungen für die Benutzer, die in der Abfrage enthalten sind. 

Klicken Sie auf **Geplante Antwortsitzungen**, um die Antwortsitzungen für den Zeitplan anzuzeigen. Sie können dann manuell zusätzliche geplante Antwortsitzungen erstellen oder geplante Antwortsitzungen die nicht beantwortet wurden löschen. 

** Auf Funktionen ** &gt; ** Start ** den Fragebogen Katalogs für die Benutzer in die zugehörigen geplanten Antwortsitzungen. Klicken Sie auf **Antworten**, um die abgeschlossenen Antworten für den Fragebogen anzuzeigen. Sie können die Fragebogenzeitplaneinstellungen, geplante Antwortsitzungen und Antworten in einen neuen Fragebogenzeitplan kopieren.

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a>Benachrichtigen von Befragungsteilnehmern zu den verfügbaren Fragebögen
Wenn Sie einen Fragebogen verteilen, müssen Sie die Teilnehmer informieren, dass Fragebögen verfügbar sind. 

** Hinweis: ** Die Befragungsteilnehmer müssen Benutzer in Microsoft Dynamics 365 sein, sodass Arbeitsgänge einen Fragebogen ausfüllen.

### <a name="notifying-respondents-about-a-planned-answer-session"></a>Benachrichtigen von Befragungsteilnehmern zu einer geplanten Beantwortungssitzung

Wenn Sie eine geplante Antwortsitzung verwenden, müssen Sie die Person z. B. telefonisch oder per E-Mail-Nachricht direkt informieren.

### <a name="notifying-respondents-about-a-scheduling"></a>Benachrichtigen von Befragungsteilnehmern zu einer Planung

Verwenden Sie die Seite **Zeitpläne für Fragebögen**, um eine E-Mail-Nachricht an alle Teilnehmer, die dem Fragebogen zugeordnet sind, zu erstellen und zu senden. Geben Sie den Text der E-Mail auf der Registerkarte **E-Mail für Mitarbeiter-Self-Service** ein. Nachdem der Plan gestartet wurde, klicken Sie auf Funktionen ** ** &gt; ** E-Mail senden ** die E-Mail den Befragungsteilnehmern generieren und senden. Die Befragungsteilnehmer können zur Website dann in signieren und den Fragebogen ausfüllen. 

**Hinweis:** Bevor Sie die E-Mail-Funktionalität verwenden können, muss der IT-Administrator die E-Mail-Einstellungen auf der Seite **E-Mail-Parameter** eingeben.

## <a name="ending-a-scheduled-questionnaire"></a>Beenden eines geplanten Fragebogens
Sie können einen geplanten Fragebogen beenden, nachdem alle Befragungsteilnehmer ihre zugewiesenen Antwortsitzungen abgeschlossen haben. Nachdem ein geplanter Fragebogen beendet ist, können Sie seine Einstellungen nicht in eine neue Planung kopieren. 

**Hinweis:** Wenn der Fragebogen von einem oder mehreren Befragungsteilnehmern noch nicht ausgefüllt wurde, Sie die Planung aber trotzdem beenden möchten, löschen Sie zuerst die betreffenden Teilnehmer aus der Liste auf der Seite **Geplante Antwortsitzung**. Dann können Sie die Planung beenden.

## <a name="completing-questionnaires"></a>Ausfüllen von Fragebögen
Nachdem Sie einen Fragebogen entworfen und verteilt haben, kann der Fragebogen von ausgewählten Befragten ausgefüllt werden. Die verfügbaren Fragebögen können von zwei Orten aus aufgerufen werden:

-   Im Navigationsbereich auf Fragebögen ** ** &gt; ** Verteilt sich ** &gt; ** füllen Sie einen Fragebogen aus **.
-   Im "Mitarbeiter-Self-Service" klicken Sie auf **Auszufüllende Fragebögen**.

Fragebögen können entweder allen Personen im Netzwerk oder lediglich bestimmten Benutzern oder Benutzergruppen zur Verfügung gestellt werden.

<a name="see-also"></a>Siehe auch
--------

[Entwurf von Fragebögen](design-questionnaires.md)

[Verwenden von Fragebögen](questionnaires.md)

[Anzeigen und Bewertung der Ergebnisse von Fragebögen evaluate-questionnaire-results.md] ()


