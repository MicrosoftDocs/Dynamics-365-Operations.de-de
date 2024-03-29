---
title: Einen Fragebogen mithilfe des Zeitplans verteilen
description: Die Fragebogenplanung ermöglicht es Ihnen, Fragebögen für mehrere Befragungsteilnehmer zu planen und zu verteilen.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c82f688a3d9366e629eedefd876dd5669bd7ed04
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691637"
---
# <a name="distribute-questionnaires-using-scheduling"></a>Einen Fragebogen mithilfe des Zeitplans verteilen


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Die Fragebogenplanung ermöglicht es Ihnen, Fragebögen für mehrere Befragungsteilnehmer zu planen und zu verteilen. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.

## <a name="create-a-questionnaire-schedule"></a>Erstellen eines Fragebogenzeitplans

1. Gehen Sie zu **Fragebogen** > **Verteilen** > **Fragebogenzeitpläne**.

2. Klicken Sie auf **Neu**.

3. Geben Sie im Feld **Zeitplan** einen Wert ein.

4. Geben Sie im Feld **Beschreibung** einen Wert ein.
    * Legen Sie den Zeitplan auf **Anonym** fest, wenn die Antworten ohne die Namen erfasst werden sollen, die den Antworten zugeordnet sind.  
    * Das Zulassen von anonymen Ergebnissen muss zuerst über die Personalverwaltungsparameter eingerichtet werden.  

5. Wählen Sie im Feld **Typ** den Zeitplantyp aus.  In diesem Beispiel nutzen wir den Typ **Zufriedenheit**.

6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.

7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.

8. Geben Sie ein Datum in das Feld **Datum** ein.

9. Erweitern oder reduzieren Sie den Abschnitt **E-Mail für Mitarbeiter-Self-Service**.

10. Geben Sie in das Feld **Subjekt** einen Wert ein.

    * Beispiel: Fragebogen verfügbar  

11. Geben Sie im Feld **Text** den Textkörper der E-Mail ein. Beachten Sie, das die Variable nur zum Ersetzen von Werten im System verwendet werden kann.

    * Beispiel: Sehr geehrte %P%, bitte melden Sie sich im Mitarbeiter-Self-Service an, um den Fragebogen zur Mitarbeitergesundheit auszufüllen.  Contoso  

12. Klicken Sie auf **Speichern**.

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a>Verwenden Sie die Einrichtungsdetails, um die zu beantwortenden Fragebögen sowie alle Abfragen für Auswahl der Antwortenden auszuwählen.

1. Auf **Einstellungsdetails** klicken.

2. Wählen Sie in der Liste eine Abfrage zur Suche im System für die Antwortenden für den Fragebogen aus.

    * Beispiel: Arbeitskräfte  

3. Klicken Sie auf **Anzeigen oder Ändern**, um bestimmte Personen auszuwählen oder die Abfrage anzupassen, um Personen zu finden, die den Kriterien entsprechen.

    * Beachten Sie, dass alle Befragten auch Benutzer im System sein müssen.  

4. Markieren Sie in der Liste die Zeile für „Person“.

5. Geben Sie im Feld **Kriterien** einen Wert ein, oder wählen Sie einen Wert aus.

    * Wählen Sie "Julia Funderburk" aus.  

6. Wählen Sie in der Liste "Julia Funderburk".

7. Klicken Sie auf **OK**.

8. Klicken Sie auf die Registerkarte **Fragebogen**.

9. In der Struktur erweitern Sie den Knoten für den Fragebogentyp **Zufriedenheitsumfrage**.

10. In der Struktur markieren Sie "Mitarbeiterstatusbewertung".

11. Klicken Sie auf **OK**.

12. Klicken Sie auf **Geplante Antwortsitzung**.

    * Beachten Sie, dass **geplante Antwortsitzungen** für jeden ausgewählten/abgefragten Benutzer erstellt wurden.  

13. Schließen Sie die Seite.

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a>Starten Sie den Fragebogenzeitplan, um den Fragebogen bereitzustellen, damit ihn die Befragten abschließen können.

1. Klicken Sie auf **Funktionen**.

2. Klicken Sie auf **Start**.

3. Klicken Sie auf **OK**.

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a>Senden Sie die E-Mail, um Befragungsteilnehmer über den verfügbaren Fragebogen zu informieren.

1. Klicken Sie auf **Funktionen**.

2. Klicken Sie auf **E-Mail senden**.

3. Klicken Sie auf **Abbrechen**.

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a>Verwenden Sie geplante Antwortsitzungen, um zu überwachen, wer den Fragebogen ausfüllen muss.

1. Klicken Sie auf **Geplante Antwortsitzung**.

    * Löschen Sie alle verbleibenden geplante Antwortsitzung, wenn Sie bereit sind, die geplante Sitzung zu beenden.  

2. Klicken Sie auf **Löschen**.

3. Klicken Sie auf **Ja**.

4. Schließen Sie die Seite.

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a>Beenden Sie den Zeitplan, wenn alle Befragten den Fragebogen abgeschlossen haben und/oder alle restlichen geplanten Antwortsitzungen gelöscht wurden.

1. Klicken Sie auf **Funktionen**.
2. Klicken Sie auf **Beenden**.
3. Klicken Sie auf **OK**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
