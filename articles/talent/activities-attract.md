---
title: "Aktivitäten im Prozess"
description: "Dieses Thema enthält Informationen zu den unterschiedlichen Aktivitätstypen, die im Einstellungsprozess verwendet werden können."
author: 
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: ccd9e2d0ff1f7fb6825c6823936b4013b3054f5d
ms.contentlocale: de-de
ms.lasthandoff: 10/22/2018

---

# <a name="activities-in-the-hiring-processes"></a>Aktivitäten im Einstellungsprozess

[!include[banner](../includes/banner.md)]

Aktivitäten können als Teil des Einstellungsprozesses in Microsoft Dynamics 365 for Talent: Attract hinzugefügt werden. Aktivitäten können einer Prozessvorlage hinzugefügt werden, oder sie können in der Stelle direkt dem Einstellungsprozess hinzugefügt werden. Wenn eine Stelle definiert wird, wird eine Prozessvorlage ausgewählt, und die Aktivitäten, die in der Vorlage enthalten sind, werden auf die Stelle angewendet. Wenn die Vorlage nicht ausgewählt wird, wird die Standardvorlage verwendet. Der Einstellungsprozess kann für eine Stelle auch geändert werden, nachdem die Vorlage angewendet wurde.

> [!NOTE] 
> Prozessvorlagen sind mit dem umfassenden Add-On für Neueinstellungen verfügbar.

## <a name="prospect-activity"></a>Interessent-Aktivität

Die Interessentenaktivität steuert, ob Interessenten einer Stelle hinzugefügt werden können. Standardmäßig können Interessenten einer Stelle hinzugefügt werden. Um die Interessentenaktivität zu deaktivieren, legen Sie die Option **Interessenten aktivieren** auf **Aus** fest. Wenn die Interessentenaktivität aktiviert wird, können zukünftige Vorgesetzte Interessenten anzeigen und hinzufügen, und die Registerarte **Interessent** wird für die Stelle angezeigt.

## <a name="application-activity"></a>Bewerbungsaktivität

Die Bewerbungsaktivität ist in der Einstellungsprozessvorlage erforderlich. Um den Kandidaten eine E-Mail zu senden wenn sie ihre Bewerbung übermitteln oder sie der Bewerbungsphase hinzugefügt werden, legen Sie die Option **Schreiben zum Kandidaten senden** auf **Ein** fest.

## <a name="scheduler-activity"></a>Planungsaktivität

Die Planungsaktivität ist optional. Diese Aktivität besitzt zwei Teile: Kandidaten-Verfügbarkeit und Planung. Mit der Kandidatenverfügbarkeitskomponente können Sie E-Mail verwenden, um die Verfügbarkeit des Kandidaten anzufordern. Die Zeitplankomponente bietet die Möglichkeit, Gespräche mit dem Kandidaten und dem Einstellungsteam zu planen. In der Planungsaktivität können folgende Optionen konfiguriert werden: **Kandidatenverfügbarkeit anfordern**, **Onlinebesprechung** und **Schreiben zum Kandidaten senden**.

- Um den Kandidaten eine E-Mail zu senden, um ihre Verfügbarkeit anzufordern, legen Sie die Option **Kandidatenverfügbarkeit anfordern** auf **Ein** fest. Wenn Sie die Option auf **Aus** festlegen, wird dieser Schritt nicht im Einstellungsprozess für die Stelle angezeigt.
- Um mit Skype for Business einen Live-Stream oder eine Telefonkonferenz durchzuführen, legen Sie das Feld **Onlinebesprechung** auf **Skype for Business** fest. Der korrekte Link **Skype-Meeting beitreten** wird anschließend der Gesprächsterminanfrage hinzugefügt, die an Gesprächsleiter gesendet wird.
- Um den Kandidaten eine E-Mail zu senden, um die Planung abzuschließen, legen Sie die Option **E-Mail an Kandidaten senden** auf **Ein** fest. Wird die Option auf **Aus** festgelegt, erhalten Kandidaten den Gesprächsterminplan nur, wenn sie sich am Kandidatenportal anmelden.

## <a name="feedback-activity"></a>Feedback-Aktivität

Die Feedback-Aktivität ist optional. Diese Aktivität ermöglicht es Gesprächsteilnehmern Empfehlungen für einen Bewerber einzugeben. Sie können auch jeden Feedback-Kommentar eingeben, den sie haben. Wenn Sie die Option **Feedbackteilnehmer von Einstellungsteam erben** aktivieren, werden der Personalbeschaffungsmitarbeiter, der zukünftige Vorgesetzte und die Gesprächsleiter automatisch in Feedback-Aktivität eingegeben. Organisationen können Gesprächsleitern erlauben, Feedback anderer Personen anzuzeigen, bevor sie ihr eigenes Feedback senden. Organisationen können Gesprächsleitern auch erlauben, ihr Feedback nach dem Senden zu bearbeiten.

## <a name="interview-activity"></a>Gesprächsaktivität

Die Gesprächsaktivität ist optional. Diese Aktivität besitzt drei Teile: Kandidatenverfügbarkeit, Planung und Feedback. Mit der Kandidatenverfügbarkeitskomponente können Sie E-Mail verwenden, um die Verfügbarkeit des Kandidaten anzufordern. Die Zeitplankomponente bietet die Möglichkeit, Gespräche mit dem Kandidaten und dem Einstellungsteam zu planen. In der Planungsaktivität können folgende Optionen konfiguriert werden: **Kandidatenverfügbarkeit anfordern**, **Onlinebesprechung** und **Schreiben zum Kandidaten senden**.

- Um den Kandidaten eine E-Mail zu senden, um ihre Verfügbarkeit anzufordern, legen Sie die Option **Kandidatenverfügbarkeit anfordern** auf **Ein** fest. Wenn Sie die Option auf **Aus** festlegen, wird dieser Schritt nicht im Einstellungsprozess für die Stelle angezeigt.
- Um mit Skype for Business einen Live-Stream oder eine Telefonkonferenz durchzuführen, legen Sie das Feld **Onlinebesprechung** auf **Skype for Business** fest. Der korrekte Link **Skype-Meeting beitreten** wird anschließend der Gesprächsterminanfrage hinzugefügt.
- Um den Kandidaten eine E-Mail zu senden, um die Planung abzuschließen, legen Sie die Option **E-Mail an Kandidaten senden** auf **Ein** fest. Wird die Option auf **Aus** festgelegt, erhalten Kandidaten den Gesprächsterminplan nur, wenn sie sich am Kandidatenportal anmelden.

Die Feedbackkomponente ermöglicht es Personen Empfehlungen für einen Bewerber einzugeben. Sie können auch jeden Feedback-Kommentar eingeben, den sie haben. Wenn Sie die Option **Feedbackteilnehmer von Einstellungsteam erben** aktivieren, werden der Personalbeschaffungsmitarbeiter, der zukünftige Vorgesetzte und die Gesprächsleiter automatisch in der Feedbackkomponente eingegeben. Organisationen können Gesprächsleitern erlauben, Feedback anderer Personen anzuzeigen, bevor sie ihr eigenes Feedback senden. Organisationen können Gesprächsleitern auch erlauben, ihr Feedback nach dem Senden zu bearbeiten.

## <a name="powerapps-activity"></a>PowerApps-Aktivität

Die PowerApps-Aktivität ermöglicht es Ihnen, eine Microsoft PowerApps-App in Ihrem Einstellungsprozess einzubetten. Die App kann für alle Bewerber, nur interne Bewerber, nur externe Bewerber oder keine Bewerber erforderlich gemacht werden. Wenn die App als erforderlich markiert wird, muss sie abgeschlossen werden, bevor die Phase gewechselt werden kann. Wenn die App nicht als erforderlich markiert ist, ist die Aktivität ein optionaler Schritt und die Phase kann gewechselt werden, auch wenn die App nicht abgeschlossen ist.

Um die PowerApps-Aktivität für den Einstellungsprozess zu speichern, müssen Sie eine PowerApps-ID eingeben. Um die PowerApps-ID zu suchen, wechseln Sie zu [PowerApps](https://web.powerapps.com), wählen **App** und dann **Details** aus.

Wenn Sie die Option **Hinzufügen von Teilnehmern für diese Aktivität zulassen** auswählen, können zusätzliche Beteiligte für eine Anwendung hinzugefügt werden, die die PowerApps-Aktivität verwendet. Zum Beispiel hat eine Organisation eine PowerApps-App mit einer Bibliothek voller Gesprächsfragen für technische Rollen erstellt. Die Organisation sucht nun einen neuen Softwareentwickler und hat dem Einstellungsprozess die PowerApps-Aktivität für die Softwareentwicklerrolle hinzugefügt. Wenn die Option **Das Hinzufügen von Teilnehmern für die Aktivität zulassen** ausgewählt ist, kann ein Personalbeschaffungsmitarbeiter oder ein zukünftiger Vorgesetzter, der sich einen Bewerber für die Softwareentwicklerrolle ansieht, der PowerApps-Aktivität Personen hinzufügen. Diese Personen können die App mit den Gesprächsfragen anzeigen.

> [!NOTE]
> Die PowerApps-Aktivität ist nur mit dem umfassenden Add-On für Neueinstellungen verfügbar.

## <a name="youtube-activity"></a>YouTube-Aktivität

Mit der YouTube-Aktivität können Sie ein YouTube-Video als Teil des Einstellungsprozesses freigeben. Um die YouTube-Aktivität für den Einstellungsprozess zu speichern, müssen Sie die URL des YouTube-Videos angeben. Wie bei der PowerApps-Aktivität können Sie zulassen, das der Aktivität Teilnehmer hinzugefügt werden. Wenn Sie die Option **Nur dem Kandidaten anzeigen** auswählen, wird das Video als Teil der Kandidatenerfahrung angezeigt. Es wird Im Einstellungsprozess in Attract nicht angezeigt.

> [!NOTE]
> Die YouTube-Aktivität ist nur mit dem umfassenden Add-On für Neueinstellungen verfügbar.

## <a name="web-content-activity"></a>Webinhalt-Aktivität

Mit der Webinhalts-Aktivität können Sie Onlineinhalt in Ihrem Einstellungsprozess einbetten. Um die Webinhalt-Aktivität für den Einstellungsprozess zu speichern, müssen Sie die URL des Inhalts angeben. Wie bei den PowerApps- und der YouTube-Aktivitäten können Sie zulassen, das der Aktivität Teilnehmer hinzugefügt werden. Wenn Sie die Option **Nur dem Kandidaten anzeigen** auswählen, wird der Inhalt als Teil der Kandidatenerfahrung angezeigt. Es wird Im Einstellungsprozess in Attract nicht angezeigt. Sie können die Größe des Inhalts auswählen, der angezeigt wird.

> [!NOTE]
> Die Webinhalt-Aktivität ist nur mit dem umfassenden Add-On für Neueinstellungen verfügbar.

## <a name="microsoft-forms-activity"></a>Microsoft Forms-Aktivität

Die Microsoft Forms-Aktivität ermöglicht es Ihnen, ein Microsoft Forms-Formular in Ihrem Einstellungsprozess einzubetten. Mit Microsoft Forms können Sie Quize, Abstimmungen und Umfragen erstellen. Um die Microsoft Forms-Aktivität für den Einstellungsprozess zu speichern, müssen Sie die URL des Formulars angeben. Wie bei den PowerApps-, YouTube und Webinhalt-Aktivitäten können Sie zulassen, das der Aktivität Teilnehmer hinzugefügt werden. Wenn Sie die Option **Nur dem Kandidaten anzeigen** auswählen, wird das Formular als Teil der Kandidatenerfahrung angezeigt. Es wird Im Einstellungsprozess in Attract nicht angezeigt.

In Microsoft Forms können Autoren ihre Einstellungen ändern, um Benutzer außerhalb ihrer Organisation auf die Umfrage oder das Quiz antworten zu lassen. In diesem Fall senden Benutzer anonyme Antworten. Wenn Sie sehen möchten, wer Ihre Umfrage oder Ihr Quiz ausgefüllt hat, können Sie festlegen, dass die antwortende Seite als Teil der Umfrage oder des Quiz ihre Namen eingeben.

> [!NOTE]
> Die Microsoft Forms-Aktivität ist nur mit dem umfassenden Add-On für Neueinstellungen verfügbar.

