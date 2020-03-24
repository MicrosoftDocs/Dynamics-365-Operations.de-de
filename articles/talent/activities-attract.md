---
title: Aktivitäten einem Einstellungsprozess hinzufügen
description: Dieses Thema enthält Informationen zu den unterschiedlichen Aktivitätstypen, die Sie einem Einstellungsprozess in Microsoft Dynamics 365 Talent - Attract hinzufügen können.
author: hasrivas
manager: AnnBe
ms.date: 05/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ce8c0bd74a41b9857538b37d0875583d06e8c11d
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124772"
---
# <a name="add-activities-to-a-hiring-process"></a>Aktivitäten einem Einstellungsprozess hinzufügen

[!include [banner](includes/banner.md)]

Aktivitäten können als Teil des Einstellungsprozesses in Microsoft Dynamics 365 Talent: Attract hinzugefügt werden. Aktivitäten können einer Prozessvorlage hinzugefügt werden, oder sie können in der Stelle direkt dem Einstellungsprozess hinzugefügt werden. Wenn eine Stelle definiert wird, wird eine Prozessvorlage ausgewählt, und die Aktivitäten, die in der Vorlage enthalten sind, werden auf die Stelle angewendet. Wenn die Vorlage nicht ausgewählt wird, wird die Standardvorlage verwendet. Der Einstellungsprozess kann für eine Stelle auch geändert werden, nachdem die Vorlage angewendet wurde.

> [!NOTE] 
> Prozessvorlagen sind mit dem umfassenden Add-On für Neueinstellungen verfügbar. Weitere Informationen finden Sie unter [Welche Version von Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

## <a name="prospect-activity"></a>Interessent-Aktivität

Die Interessentenaktivität steuert, ob Interessenten einer Stelle hinzugefügt werden können. Standardmäßig können Interessenten einer Stelle hinzugefügt werden. Um die Interessentenaktivität zu deaktivieren, legen Sie die Option **Interessenten aktivieren** auf **Aus** fest. Wenn die Interessentenaktivität aktiviert wird, können zukünftige Vorgesetzte Interessenten anzeigen und hinzufügen, und die Registerarte **Interessent** wird für die Stelle angezeigt.

> [!NOTE]
> Wenn Sie die einer Stelle hinzugefügt werden LinkedIn von Kandidaten zu ermöglichen, müssen Sie die Option **Aktivieren Sie Interessenten** auf **Aktiviert** festlegen.

## <a name="application-activity"></a>Bewerbungsaktivität

Die Bewerbungsaktivität ist in der Einstellungsprozessvorlage erforderlich. Um den Kandidaten eine E-Mail zu senden wenn sie ihre Bewerbung übermitteln oder sie der Bewerbungsphase hinzugefügt werden, legen Sie die Option **Schreiben zum Kandidaten senden** auf **Ein** fest.

## <a name="interview-schedule-and-feedback-activity"></a>Gesprächszeitplanungs- und -rückmeldungsaktivität

Diese Aktivität besitzt drei Teile: Kandidatenverfügbarkeitsanforderung, Zeitplan und Rückmeldung. Verwenden Sie die Gesprächsaktivität in der Stellenvorlage, wenn Sie die Kandidatenverfügbarkeitsanforderung, den Zeitplan und die Rückmeldung als Teil des Prozesses einbeziehen möchten, anstatt sie einzeln als Teil des Einrichtungsprozesses zu verwenden. Weitere Informationen finden Sie unter [Gesprächsplanung und -rückmeldung](interview-scheduling-feedback.md).

## <a name="power-apps-activity"></a>Power Apps-Aktivität

Die Power Apps-Aktivität ermöglicht es Ihnen, eine Microsoft Power Apps-App in Ihren Einstellungsprozess einzubetten. Die App kann für alle Bewerber, nur interne Bewerber, nur externe Bewerber oder keine Bewerber erforderlich gemacht werden. Wenn die App als erforderlich markiert wird, muss sie abgeschlossen werden, bevor die Phase gewechselt werden kann. Um als abgeschlossen zu gelten, muss das Feld **JobApplicationStatus** auf **Abgeschlossen** festgelegt sein. Dieses Feld befindet sich in der JobApplicationActivity-Entität, also muss die Power Apps-App dieses Feld aktualisieren, bevor die Phase erweitert werden kann. Wenn die App nicht als erforderlich markiert ist, ist die Aktivität ein optionaler Schritt und die Phase kann gewechselt werden, auch wenn die App nicht abgeschlossen ist.

Um die Power Apps-Aktivität für den Einstellungsprozess zu speichern, müssen Sie eine Power Apps-ID eingeben. Um die Power Apps-ID zu suchen, wechseln Sie zu [Power Apps](https://web.powerapps.com), wählen**Apps** und dann **Details** aus.

Standardmäßig steht die Power Apps-Aktivität dem zukünftigen Vorgesetzten, Personalbeschaffungsmitarbeiter und deren zugehörigen Stellvertretern zur Verfügung. Wenn Sie die Option **Hinzufügen von Teilnehmern für diese Aktivität zulassen** auswählen, können zusätzliche Teilnehmer aus dem Einstellungsteam für eine Anwendung hinzugefügt werden, die die Power Apps-Aktivität verwendet. Zum Beispiel hat eine Organisation eine Power Apps-App mit einer Bibliothek voller Gesprächsfragen für technische Rollen erstellt. Die Organisation sucht nun einen neuen Softwareentwickler und hat dem Einstellungsprozess die Power Apps-Aktivität für die Softwareentwicklerrolle hinzugefügt. Wenn die Option **Das Hinzufügen von Teilnehmern für diese Aktivität zulassen** ausgewählt ist, kann ein Personalbeschaffungsmitarbeiter oder ein zukünftiger Vorgesetzter, der sich einen Bewerber für die Softwareentwicklerrolle ansieht, der Power Apps-Aktivität Gesprächsleiter hinzufügen. Diese Personen können die App mit den Gesprächsfragen anzeigen.

> [!NOTE]
> Die Power Apps-Aktivität ist nur mit dem umfassenden Add-On für Neueinstellungen verfügbar. Weitere Informationen finden Sie unter [Welche Version von Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

## <a name="youtube-activity"></a>YouTube-Aktivität

Mit der YouTube-Aktivität können Sie ein YouTube-Video als Teil des Einstellungsprozesses freigeben. Um die YouTube-Aktivität für den Einstellungsprozess zu speichern, müssen Sie die URL des YouTube-Videos angeben. Sie können wählen, den Inhalt dem **Einstellungsteam**, **Nur internen Kandidaten**, **Nur externen Kandidaten** oder **Allen Kandidaten** anzeigen. Wie bei der Power Apps-Aktivität können Sie zulassen, das der Aktivität Teilnehmer des Einstellungsteams hinzugefügt werden. Wenn Sie wählen, den Inhalt Kandidaten anzuzeigen, wird das Video nur als Teil der Kandidatenerfahrung und nicht des Einstellungsprozesses angezeigt.

> [!NOTE]
> Die YouTube-Aktivität ist nur mit dem umfassenden Add-On für Neueinstellungen verfügbar. Weitere Informationen finden Sie unter [Welche Version von Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

## <a name="web-content-activity"></a>Webinhalt-Aktivität

Mit der Webinhalts-Aktivität können Sie Onlineinhalt in Ihrem Einstellungsprozess einbetten. Um die Webinhalt-Aktivität für den Einstellungsprozess zu speichern, müssen Sie die URL des Inhalts angeben. Sie können wählen, den Inhalt dem **Einstellungsteam**, **Nur internen Kandidaten**, **Nur externen Kandidaten** oder **Allen Kandidaten** anzeigen. Wie bei den Power Apps- und YouTube-Aktivitäten können Sie zulassen, dass der Aktivität Teilnehmer des Einstellungsteams hinzugefügt werden. Wenn Sie wählen, den Inhalt Kandidaten anzuzeigen, wird der Webinhalt nur als Teil der Kandidatenerfahrung und nicht des Einstellungsprozesses angezeigt. Sie können die Größe des Inhalts auswählen, der angezeigt wird.

> [!NOTE]
> Die Webinhalt-Aktivität ist nur mit dem umfassenden Add-On für Neueinstellungen verfügbar. Weitere Informationen finden Sie unter [Welche Version von Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

## <a name="microsoft-forms-activity"></a>Microsoft Forms-Aktivität

Die Microsoft Forms-Aktivität ermöglicht es Ihnen, eine Microsoft Forms-Aktivität in Ihrem Einstellungsprozess einzubetten. Mit Microsoft Forms können Sie Quize, Abstimmungen und Umfragen erstellen. Um die Microsoft Forms-Aktivität für den Einstellungsprozess zu speichern, müssen Sie die URL des Formulars angeben. Sie können wählen, den Inhalt dem **Einstellungsteam**, **Nur internen Kandidaten**, **Nur externen Kandidaten** oder **Allen Kandidaten** anzeigen. Wie bei den Power Apps-, YouTube- und Webinhalts-Aktivitäten können Sie zulassen, dass der Aktivität Teilnehmer des Einstellungsteams hinzugefügt werden. Wenn Sie wählen, den Inhalt Kandidaten anzuzeigen, wird das Formular nur als Teil der Kandidatenerfahrung und nicht des Einstellungsprozesses angezeigt.

In Microsoft Forms können Autoren ihre Einstellungen ändern, um Benutzer außerhalb ihrer Organisation auf die Umfrage oder das Quiz antworten zu lassen. In diesem Fall senden Benutzer anonyme Antworten. Wenn Sie sehen möchten, wer Ihre Umfrage oder Ihr Quiz ausgefüllt hat, können Sie festlegen, dass die antwortende Seite als Teil der Umfrage oder des Quiz ihre Namen eingeben.

> [!NOTE]
> Die Microsoft Forms-Aktivität ist nur mit dem umfassenden Add-On für Neueinstellungen verfügbar. Weitere Informationen finden Sie unter [Welche Version von Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

## <a name="offer-activity"></a>Angebotsaktivität

Die Einstellungsprozessvorlage erfordert die Angebotsaktivität. Um die integrierte Angebotsverwaltung-App zu verwenden, legen Sie **Angebotsverwaltung-App starten** auf **Ein** fest. Wenn diese Einstellung „Aus” ist, wird der Kandidat nicht in der Angebot-App angezeigt. Sie müssen daher Aktualisierungen einer Angebotsaktivität eines Kandidaten manuell nachverfolgen. Um zu definieren, ob Einstellungsmanager das Angebot für den Kandidaten in der Angebot-App vorbereiten können, legen Sie **Einstellungsleiter können Angebot vorbereiten** auf **Ein** fest. Wenn der Stelle mehrere Positionen zugeordnet sind, können Sie entscheiden, ob Sie mehrere Angebote für dieselbe Positionsnummer erstellen möchten. Wenn Sie nur ein Angebot pro Position pro Stelle zulassen möchten, legen Sie **Wiederverwendung von Positionen innerhalb von Stelle zulassen** auf **Aus** fest.

> [!NOTE]
> Die integrierte Angebotsverwaltung-App ist nur mit dem Umfassenden Einstellungs-Add-On verfügbar. Weitere Informationen finden Sie unter [Welche Version von Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).


