---
title: Gesprächsplanung und -rückmeldung
description: Dieses Thema enthält Informationen zu Gesprächsplanungs- und -rückmeldungsaktivitäten in Attract.
author: ''
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: hasrivas
ms.openlocfilehash: 7bc5a66bb221cb0ab2c69fcb1013ed48a7c664a6
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2019
ms.locfileid: "374905"
---
# <a name="interview-scheduling-and-feedback"></a>Gesprächsplanung und -rückmeldung

[!include[banner](../includes/banner.md)]

## <a name="scheduler-activity"></a>Planungsaktivität

Die Planungsaktivität ist optional und enthält zwei Komponenten: Kandidatenverfügbarkeitsanforderung und Zeitplan. Mit der Kandidatenverfügbarkeitskomponente können Sie E-Mail verwenden, um die Verfügbarkeit des Kandidaten anzufordern. Die Zeitplankomponente bietet die Möglichkeit, Gespräche mit dem Kandidaten und dem Einstellungsteam zu planen.

### <a name="candidate-availability-request"></a>Kandidatenverfügbarkeitsanforderung

Um den Kandidaten eine E-Mail zu senden, um ihre Verfügbarkeit anzufordern, wählen SIe das Feld **Kandidatenverfügbarkeit anfordern** aus. Wenn das Feld nicht ausgewählt wird, wird dieser Schritt nicht im Einstellungsprozess für die Stelle angezeigt.

Um die Verfügbarkeitsanforderung zu senden, klicken Sie auf **Anforderung senden**, wählen Sie die verfügbaren Daten und eine E-Mail-Vorlage aus, und senden Sie dann die E-Mail an den Kandidaten.

[![Attract-Personalbeschafferansicht zum Senden einer Kandidatenverfügbarkeitsanforderung](./media/scheduler-candidate-request.png)](./media/scheduler-candidate-request.png)

Wenn der Kandidat eine E-Mail erhält, um auf die Anforderung zu antworten, können sie sich beim Kandidatenportal anmelden, die Datumsangaben gemäß ihrer Verfügbarkeit auswählen, und auf **Übermitteln** klicken.

### <a name="schedule"></a>Planung
Es gibt die mehrere Konfigurationen, die für den Gesprächsplaner verfügbar sind, um die Gesprächsschleife schnell zu erstellen und an die Gesprächsleiter und den Kandidaten zu senden.

1. Klicken Sie auf **Zeitplan erstellen**, und listen Sie im Feld **Gesprächsleiter hinzufügen** alle Gesprächsleiter auf, die Teil der Gesprächsschleife sein werden.
[![Attract-Personalbeschafferansicht zum Starten der Planung einer Gesprächsschleife](./media/schedule-start-over.png)](./media/schedule-start-over.png)   
    Wenn der Kandidat auf die Gesprächsverfügbarkeitsanforderung geantwortet hat, wird das Feld **Datum des Gesprächs** mit seiner Auswahl voraufgefüllt. Sie können bei Bedarf ein anderes Datum auswählen.
    
    Wenn Sie das Feld **Dies zu einem Gruppengespräch machen** auswählen, wird die Gruppe der Gesprächsleiter auf der linken Seite in eine Einzelgruppenschleife verschoben, um das Gespräch zu erstellen. Sie müssen dann einen bestimmten Nummernkreis für die Gespräche definieren.
    
    Der Gesprächszeitplan sollte der Verfügbarkeit der Teilnehmer bestmöglich entsprechen. Wenn es ein interner Kandidat ist, können Sie ihre Verfügbarkeit als Teil der Zeitplanempfehlung einbeziehen.
    
    Wählen Sie für eine Online-Besprechung das Feld **Skype-Besprechungen hinzufügen** aus, und für jedes Gesprächsereignis wird ein **Skype for Business**-Link verfügbar sein.

2. Wählen Sie die Gesprächsdauer für jedes Gesprächsereignis aus, und klicken Sie dann auf **OK**, um die Erstellung des Zeitplans zu starten.

    Wenn **Empfehlungen** ausgewählt werden, werden Vorschläge angezeigt und das Gesprächsraster wird voraufgefüllt. Sie sind dann in der Lage, die aktuelle Kalenderverfügbarkeit aller ausgewählten Gesprächsleiter anzuzeigen. Darüber hinaus können Sie den Kalender des Kandidaten anzeigen, wenn sie ein interner Kandidat sind.

3. Wenn keine Vorschläge verfügbar sind, klicken Sie in der Spalte **Gesprächsleiter** auf einen Zeitrahmen, geben Sie den Gesprächstitel und die Details an, und füllen Sie ggf. Informationen zum Ort auf. Falls gewünscht, können Sie den **Skype for Business**-Link für das Gespräch einbeziehen.

4. Um zusätzliche Gesprächsleiter einzubeziehen, klicken Sie auf die Rasterspalte **Gespräch hinzufügen**, um einen oder mehrere Gesprächsleiter auszuwählen. Mithilfe der Option der Auslassungspunkte (...) können Sie ein Gespräch aus der Schleife entfernen.
    
5. Wenn die Gespräche in einer anderen Zeitzone geplant werden, wählen Sie den erforderlichen Ort/die erforderliche Zeitzone aus der Dropdownliste oben rechts aus. Das Gesprächsleiterverfügbarkeitsraster wird mit der neuen Zeitzone aktualisiert. Diese Zeitzonen-Auswahl wird nun auch bei der Ansicht **Gesprächszusammenfassung** angezeigt, die für die Gesprächsleiter und den Kandidaten freigegeben wird. 

6. Klicken Sie auf **An Gesprächsleiter senden**, um die Besprechungseinladungen an die beteiligten Gesprächsleiter zu senden.

    Nachdem die Gesprächsanforderungen an die Gesprächsleiter gesendet wurden, können sie direkt aus der erhaltenen E-Mail-Einladung antworten.

    >[!NOTE]
    > Für alle 1:1-Gespräche werden Erinnerungen zu den Befragungspersonen alle 24 Stunden gesendet, wenn die Befragungsperson (angenommen oder abgelehnt) nicht auf die Gesprächsanforderung reagiert hat.

    > Für alle Bereichsgespräche gibt es keine automatischen Erinnerungen für die Gesprächsanforderung. Um eine Erinnerung manuell zu starten, bearbeiten Sie das Gespräch und verwenden Sie die **Aktualisieren und übermitteln** Option, um die Anforderung an die Befragungspersonen zu senden

    Gesprächsleiterantworten werden erfasst und in Attract angezeigt. Wenn ein Gesprächsleiter die Einladung ablehnt, werden Sie benachrichtigt, um eine Änderung vorzunehmen. Um ihre Antwort in der Rasteransicht **Planer** anzuzeigen, klicken Sie auf das Blasen-Symbol.

[![Attract-Personalbeschafferansicht einer Gesprächsleiterantwort](./media/schedule-interviewer-response.png)](./media/schedule-interviewer-response.png)

7. Wenn der Gesprächszeitplan für den Kandidaten freigegeben werden kann, klicken Sie auf **Zum Kandidaten senden** Sie können die Gesprächsleiternamen und -zeitrahmen für den Kandidaten ausblenden oder anzeigen.

8. Wählen Sie eine E-Mailvorlage aus und senden Sie die Gesprächszusammenfassung an den Kandidaten. Der Kandidat kann diese Informationen in seiner E-Mail sowie im Kandidatenportal anzeigen.
    
>[!NOTE] 
> Die Kalenderverfügbarkeit eines Kandidaten wird nur dann angezeigt, wenn der Kandidat intern ist. Ebenso können nur interne Kandidaten verwendet werden, um Gesprächszeitplanempfehlungen zu erweitern. Derzeit erhalten Kandidaten (extern oder intern) keine E-Mail-Besprechungseinladung. Stattdessen erhält der Kandidat nur eine Zusammenfassung der Gespräche.

## <a name="feedback-activity"></a>Feedback-Aktivität

Die Rückmeldungsaktivität einer Stellenvorlage ist optional. Diese Aktivität ermöglicht es Gesprächsteilnehmern, Empfehlungen oder Feedback-Kommentare für einen Bewerber einzugeben. Wenn das Feld **Feedbackteilnehmer von Einstellungsteam erben** ausgewählt ist, werden der Personalbeschaffer, der zukünftige Vorgesetzte und die Gesprächsleiter automatisch in der Rückmeldungs-Aktivität eingegeben. Organisationen können Gesprächsleitern erlauben, Feedback anderer Personen anzuzeigen, bevor sie ihr eigenes Feedback senden. Organisationen können Gesprächsleitern auch erlauben, ihr Feedback nach dem Senden zu bearbeiten. Gesprächsleiter werden daran erinnert, Rückmeldungen für die Gespräche zu senden, die sie vor kurzem auf Basis der Voreinstellungskonfiguration als Teil der Stellenvorlage geführt haben. Der zukünftige Vorgesetzte oder ein Personalbeschaffer für die Stelle kann einen Gesprächsleiter auch manuell daran erinnern, Feedback zu senden.

## <a name="interview-activity"></a>Gesprächsaktivität

Die Gesprächsaktivität ist eine optionale Aktivität mit drei Komponenten: Kandidatenverfügbarkeitsanforderung, Zeitplan und Rückmeldung. Verwenden Sie die Gesprächsaktivität in der Stellenvorlage, wenn Sie alle Kandidatenverfügbarkeitsanforderungen, Zeitpläne und Rückmeldungen im Rahmen des Prozesses statt einzeln im Rahmen des Einstellungsprozesses verwenden möchten.
