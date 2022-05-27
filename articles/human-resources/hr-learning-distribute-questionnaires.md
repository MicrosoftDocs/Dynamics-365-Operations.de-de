---
title: Fragebögen verteilen und planen
description: In diesem Artikel wird beschrieben, wie Sie die Fragebögen verteilen die Sie entworfen haben, sodass sie für die Person oder Gruppe von Personen verfügbar sind, die sie beantworten sollen.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters, HcmLearningWorkspace
audience: Application User
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a543d9b85edd493f9b5d5a0449302769c3592f7
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695899"
---
# <a name="distribute-and-schedule-questionnaires"></a>Fragebögen verteilen und planen


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Artikel wird beschrieben, wie Sie die Fragebögen verteilen die Sie entworfen haben, sodass sie für die Person oder Gruppe von Personen verfügbar sind, die sie beantworten sollen. 

Es gibt mehrere Möglichkeiten, einen Fragebogen zu verteilen:

-   Markieren Sie den Fragebogen als **Aktiv**. Der Fragebogen ist für alle Mitarbeiter verfügbar, sofern keine Fragebogengruppe eingerichtet wird, um den Zugriff auf den Fragebogen zu beschränken.
-   Zuweisen von Rechten zu einer Fragebogengruppe. Der Fragebogen ist dann für alle Mitglieder der ausgewählten Gruppe verfügbar.
-   Erstellen von geplanten Antwortsitzungen. Der Fragebogen steht dann für eine bestimmte Person zur Verfügung.
-   Zeitplan erstellen. Der Fragebogen kann dann für mehrere Personen verfügbar sein.

## <a name="marking-a-questionnaire-as-active"></a>Markieren eines Fragebogens als aktiv

Setzen Sie das Feld **Aktiv** auf **Ja** auf der Seite **Fragebögen**. Sie geben den Fragebogen für alle Mitarbeiter zur Beantwortung frei. Die Befragungsteilnehmer können den Fragebogen mehrmals ausfüllen. Diese Funktionalität ist hilfreich, wenn ständige Rückmeldung für das ganze Jahr gesammelt werden sollen. So können Sie beispielsweise einen Fragebogen erstellten, über den die Mitarbeiter ein Feedback zum Mittagessen in der Cafeteria abgeben können.

## <a name="questionnaire-groups"></a>Fragebogengruppen

Sie können Fragebogengruppen einrichten und die Befragten einbeziehen, für die ein Fragebogen verteilt werden soll. 

Sie können Fragebogengruppen von den folgenden Seiten erstellen:

-   **Fragebogengruppen** – Nur Personen innerhalb einer Fragebogengruppe können einen ausgewählten Fragebogen ausfüllen. Wenn beispielsweise die gewünschte Zielgruppe "Auftragnehmer" ist, können Sie eine Fragebogengruppe erstellen, die für diese Teilnehmer spezifisch ist.
-   **Fragebogengruppenmitglieder** – Mithilfe dieses Formulars können Sie Personen zu Fragebogengruppen hinzufügen.

Um eine Fragebogengruppe einem Fragebogen zuzuweisen, klicken Sie auf der Seite **Fragebögen** auf **Benutzerrechte**. Nachdem der Fragebogen als aktiv gespeichert ist, können die Mitglieder der Fragebogengruppe den Fragebogen ausfüllen. Diese Funktion ist hilfreich, wenn Sie einen Fragebogen mit einer Auswählensgruppe von Personen testen möchten, bevor Sie diese in einer größeren Gruppe verteilen, oder wenn Sie den Fragebogen einer Zielgruppe zukommen lassen wollen.

## <a name="planned-answer-sessions-in-a-questionnaire"></a>Geplante Beantwortungssitzung in einem Fragebogen

Geplante Antwortsitzungen sind Fragebogen, die Sie entwickelt und für die Sie die Befragten ausgewählt haben. 

> [!NOTE]
> Bevor Sie geplante Antwortsitzungen einrichten können, müssen Sie einen Fragebogen entwerfen. 

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

Verwenden Sie die **Referenztypen**-Seite, um Referenztypen für einen Fragebogen einzurichten. Jeder Referenztyp entspricht einer Tabelle in Microsoft Dynamics 365 Finance. Wenn Sie Zeitpläne für Fragebögen erstellen, können Sie einzelne Datensätze in der Tabelle oder einen Datensatzbereich angeben, denen bzw. dem der Fragebogen zugeordnet wird. 

Wenn Sie beispielsweise die Tabelle Kurse auswählen, können Sie entscheiden, für welchen Kurs der Fragebogen verwendet werden soll. Wenn Sie einen Referenztyp für die Kurstabelle einrichten, sind einige Felder und Schaltflächen auf der Seite **Kurse** verfügbar.

### <a name="questionnaire-schedules"></a>Zeitpläne für Fragebögen

Sie können Fragebogenzeitpläne verwenden, um mehrere geplante Antwortsitzungen für eine Benutzergruppe auf Grundlage eines Referenztyps zu generieren. Dient zum Erstellen eines Zeitplans für die Seite **Fragebogenzeitpläne**. Wählen Sie den Planungstyp aus, um den Zeitplan zu Kategorisieren, und wählen Sie auch den Referenztyp aus, der verwendet werden soll, um das System für bestimmte Benutzer abzufragen. Wenn Sie zum Beispiel den Referenztyp auf die Kursetabelle festlegen, können Sie einen bestimmten Kurs im Feld **Referenz** auswählen. 

Klicken Sie auf **Einstellungsdetails**, um den Fragebogen und andere Kriterien auszuwählen. Geben Sie beispielsweise den Namen des Kursleiters als Kriterium an, nachdem der Fragebogen eine Bewertung des Kursleiters ist. Nachdem Sie abgeschlossen und die Einrichtungsdetails eingeben haben, generiert das System geplante Antwortsitzungen für die Benutzer, die in der Abfrage enthalten sind. 

Klicken Sie auf **Geplante Antwortsitzungen**, um die Antwortsitzungen für den Zeitplan anzuzeigen. Sie können dann manuell zusätzliche geplante Antwortsitzungen erstellen oder geplante Antwortsitzungen die nicht beantwortet wurden löschen. 

Klicken Sie auf **Funktionen** &gt; **Starten**, um den Fragebogen für die Benutzer in den zugehörigen geplanten Antwortsitzungen verfügbar zu machen. Klicken Sie auf **Antworten**, um die abgeschlossenen Antworten für den Fragebogen anzuzeigen. Sie können die Fragebogenzeitplaneinstellungen, geplante Antwortsitzungen und Antworten in einen neuen Fragebogenzeitplan kopieren.

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a>Benachrichtigen von Befragungsteilnehmern zu den verfügbaren Fragebögen
Wenn Sie einen Fragebogen verteilen, müssen Sie die Teilnehmer informieren, dass Fragebögen verfügbar sind. 

### <a name="notifying-respondents-about-a-planned-answer-session"></a>Benachrichtigen von Befragungsteilnehmern zu einer geplanten Beantwortungssitzung

Wenn Sie eine geplante Antwortsitzung verwenden, müssen Sie die Person z. B. telefonisch oder per E-Mail-Nachricht direkt informieren.

### <a name="notifying-respondents-about-a-scheduling"></a>Benachrichtigen von Befragungsteilnehmern zu einer Planung

Verwenden Sie die Seite **Zeitpläne für Fragebögen**, um eine E-Mail-Nachricht an alle Teilnehmer, die dem Fragebogen zugeordnet sind, zu erstellen und zu senden. Geben Sie den Text der E-Mail auf der Registerkarte **E-Mail für Mitarbeiter-Self-Service** ein. Nachdem der Plan gestartet wurde, klicken Sie **Funktionen** &gt; **E-Mail senden**, um die E-Mail den Befragungsteilnehmern zu generieren und zu senden. Die Befragungsteilnehmer können sich nun auf der Website anmelden und den Fragebogen ausfüllen. 

> [!NOTE]
> Bevor Sie die E-Mail-Funktion verwenden können, muss Ihr IT-Administrator auf der Seite **E-Mail-Parameter** die E-Mail-Einstellungen eintragen.

## <a name="ending-a-scheduled-questionnaire"></a>Beenden eines geplanten Fragebogens

Sie können einen geplanten Fragebogen beenden, nachdem alle Befragungsteilnehmer ihre zugewiesenen Antwortsitzungen abgeschlossen haben. Nachdem ein geplanter Fragebogen beendet ist, können Sie seine Einstellungen nicht in eine neue Planung kopieren. 

> [!NOTE]
>   Wenn ein oder mehrere Befragungsteilnehmer den Fragebogen nicht ausgefüllt haben, Sie aber die Planung beenden wollen, müssen Sie zuerst diese Befragungsteilnehmer aus der Liste auf der Seite **Geplante Antwortsitzung** löschen. Dann können Sie die Planung beenden.

## <a name="completing-questionnaires"></a>Ausfüllen von Fragebögen

Nachdem Sie einen Fragebogen entworfen und verteilt haben, kann der Fragebogen von ausgewählten Befragten ausgefüllt werden. Die verfügbaren Fragebögen können von zwei Orten aus aufgerufen werden:

-   Im Navigationsbereich Klicken Sie auf **Fragebögen** &gt; **Verteilen** &gt; **Fragebogen ausfüllen**.
-   Im "Mitarbeiter-Self-Service" klicken Sie auf **Auszufüllende Fragebögen**.

Fragebögen können entweder allen Personen im Netzwerk oder lediglich bestimmten Benutzern oder Benutzergruppen zur Verfügung gestellt werden.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
