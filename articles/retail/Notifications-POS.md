---
title: Auftragsbenachrichtigungen in der Verkaufsstelle anzeigen
description: "In diesem Thema wird beschrieben, wie Auftragsbenachrichtigungen in der Verkaufsstelle und im Benachrichtigungsframework aktiviert werden, die für andere Arbeitsgänge erweitert werden können."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: ec6cb212766dd90fa9db7719a2119419ecb935c7
ms.openlocfilehash: aea36591a81f727059e37a958efa62a9ebde9d9d
ms.contentlocale: de-de
ms.lasthandoff: 12/20/2017

---

# <a name="display-notifications-in-point-of-sale"></a>Benachrichtigungen in der Verkaufsstelle anzeigen

In der heutigen, modernen Einzelhandelsumgebung werden Filialmitarbeitern verschiedene Aufgaben zugewiesen, wie Kunden zu helfen, Transaktionen einzugeben, Lagerbestände zu zählen und Aufträge in der Filiale entgegenzunehmen. Der Verkaufsstellen-(POS)-Client ermöglicht es den Mitarbeitern, diese Aufgaben und noch viel mehr auszuführen, alles in eine einzigen Anwendung. Bei den verschiedenen Aufgaben, die im Lauf des Tages auszuführen sind, müssen Mitarbeiter möglicherweise darüber benachrichtigt werden, wenn etwas Ihre Aufmerksamkeit erfordert. Das Benachrichtigungsframework in der POS löst dieses Problem, indem es Einzelhändlern ermöglicht, rollenbasierte Benachrichtigungen zu konfigurieren. Mit Dynamics 365 for Retail mit Anwendung Update 5 können diese Benachrichtigungen nur für POS-Arbeitsgänge konfiguriert werden.

Aktuell bietet das System die Fähigkeit, Benachrichtigungen für Auftragserfüllungsarbeitsgänge anzuzeigen. Das Framework ist jedoch so konzipiert, dass es erweiterbar ist. In Zukunft können somit Entwickler einen Benachrichtigungshandler für jeden beliebigen Vorgang schreiben und die Benachrichtigungen in der POS anzeigen.  

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Aktivieren von Benachrichtigungen für Auftragserfüllungsarbeitsgänge

Um Benachrichtigungen für die Auftragserfüllungsarbeitsgänge zu aktivieren, beachten Sie die folgenden Schritte:

 - Wechseln Sie zur Seite **Arbeitsgänge** (**Einzelhandel** > **Kanaleinstellung** > **POS-Einstellung** > **Verkaufsstelle** > **Arbeitsgänge**).
 - Suchen Sie nach dem Auftragserfüllungsarbeitsgang und aktivieren Sie das Kontrollkästchen **Benachrichtigungen aktivieren** für diesen Arbeitsgang. Dadurch wird dem Benachrichtigungsframework angezeigt, auf den Handler für den Auftragserfüllungsarbeitsgang zu warten. Wenn der Handler implementiert ist, dann werden die Benachrichtigungen in der POS angezeigt, andernfalls werden die Benachrichtigung nicht für diesen Arbeitsgang angezeigt.
- Wechseln Sie zu den POS-Berechtigungen, die den Arbeitskräften und unter dem Inforegister **Benachrichtigungen** zugeordnet sind, fügen Sie den Auftragserfüllungsarbeitsgang mit der „Anzeigereihenfolge” als 1 hinzu. Wenn mehr als eine Benachrichtigung konfiguriert ist, wird die Anzeigereihenfolge verwendet, um die Benachrichtigung von oben nach unten anzuordnen, wobei 1 ganz oben ist. Nur solche Arbeitsgänge können hinzugefügt werden, für die das Kontrollkästchen **Benachrichtigungen aktivieren** aktiviert wurde. Die Benachrichtigungen werden auch nur für die Arbeitsgänge angezeigt, die hier hinzugefügt wurden und nur an solche Arbeitskräfte, für die die Arbeitsgänge zu den entsprechenden POS-Berechtigungen hinzugefügt wurden. 

> [!NOTE]
> Benachrichtigungen können auf der Benutzerebene überschrieben werden, indem Sie zum Datensatz der Arbeitskraft navigieren und **POS-Berechtigungen** auswählen und dann das Benachrichtigungsabonnement des Benutzers bearbeiten.

 - Wechseln Sie zur Seite **Funktionsprofil** (**Einzelhandel** > **Kanaleinstellung** > **POS-Einstellung** > **POS-Profile** > **Funktionsprofile**). Aktualisieren Sie die Eigenschaft **Benachrichtigungsintervall**, um das Intervall in Minuten festzulegen, zu denen die Benachrichtigungen abgerufen werden sollen. Es wird empfohlen, diesen Wert auf 10 Minuten festzulegen, um unnötige Kommunikation mit der Unternehmenszentrale zu vermeiden. Durch das Festlegen des Benachrichtigungsintervalls auf „0” werden die Benachrichtungen ausgeschaltet.  

 - Wechseln Sie zu **Einzelhandel** > **Einzelhandels-IT** > **Verteilungszeitplan**. Wählen Sie den Zeitplan „1060-Mitarbeiter” aus, um die Benachrichtungsabonnementeinstellungen zu synchronisieren, und klicken Sie dann auf **Jetzt ausführen**. Synchronisieren Sie danach das Berechtigungsintervall, indem Sie die „1070-Kanalkonfiguration” auswählen, und klicken Sie dann auf **Jetzt ausführen**. 

## <a name="view-notifications-in-pos"></a>Benachrichtigungen in POS anzeigen

Nachdem die oben genannten Schritte abgeschlossen sind, können die Arbeitskräfte, für die die Benachrichtigungen eingerichtet wurden, die Benachrichtigungen in POS anzeigen. Um die Benachrichtigungen anzuzeigen, klicken Sie auf das Benachrichtigungssymbol in der Titelleiste der POS. Dadurch wird das Benachrichtigungscenter mit den Benachrichtigungen für den Auftragserfüllungsarbeitsgang angezeigt. Das Benachrichtigungscenter sollte die folgenden Gruppen innerhalb des Auftragserfüllungsarbeitsgangs anzeigen: 

- **Ausstehende Aufträge** – In dieser Gruppe wird die Anzahl der Aufträge angezeigt, die sich im ausstehenden Status befinden, wie beispielsweise Aufträge, die von einer POS-Arbeitskraft akzeptiert werden müssen, die die erforderlichen Berechtigungen für die Filialerfüllung besitzt. Durch Klicken auf die Nummer in der Gruppe wird die Seite **Auftragserfüllung** geöffnet. Sie ist gefiltert, sodass nur die ausstehenden Aufträge angezeigt werden, die der Filiale zur Erfüllung zugewiesen sind. Wenn die Aufträge automatisch für die Filiale akzeptiert werden, wird die Anzahl für diese Gruppe null sein.

- **Filialabholung** – In dieser Gruppe wird die Anzahl von Aufträgen angezeigt, die den Liefermodus **Abholung** haben, und ihre Abholung ist von der aktuellen Filiale geplant. Durch Klicken auf die Nummer in der Gruppe wird die Seite **Auftragserfüllung** geöffnet. Sie ist gefiltert, sodass die aktiven Aufträge angezeigt werden, die so eingerichtet sind, dass sie von der aktuellen Filiale abgeholt werden.

- **Von Filiale versenden** – In dieser Gruppe wird die Anzahl von Aufträgen angezeigt, die den Liefermodus **Versand** haben, und der Versand ist von der aktuellen Filiale geplant. Durch Klicken auf die Nummer in der Gruppe wird die Seite **Auftragserfüllung** geöffnet. Sie ist gefiltert, sodass die aktiven Aufträge angezeigt werden, die so eingerichtet sind, dass sie von der aktuellen Filiale versendet werden.

Wenn neue Aufträge der Filiale zur Erfüllung zugewiesen werden, ändert sich das Benachrichtigungssymbol, um die neuen Benachrichtigungen anzuzeigen, und die Anzahl der entsprechenden Gruppen wird aktualisiert. Der Benutzer kann auch auf das Aktualisierungssymbol neben dem Arbeitsgangnamen klicken, um die Anzahl der Gruppen sofort zu aktualisieren. Die Anzahl wird auch in dem vordefinierten Intervall aktualisiert. Von jeder Gruppe, die einen neuen Artikel hat, der nicht von der aktuellen Arbeitskraft gesehen wird, wird ein Blitzsymbol angezeigt, das anzeigt, dass diese Gruppe einen neuen Artikel hat. Durch Klicken auf die Kacheln innerhalb der Benachrichtigungen wird der spezifische Arbeitsgang geöffnet, für den diese Benachrichtigung konfiguriert ist. In den vorstehenden Szenarien wird durch das Anklicken der Benachrichtigungen die Seite **Auftragserfüllung** geöffnet, und die entsprechenden Parameter werden übergeben: ausstehende Aufträge, Filialabholung und Versand ab Filiale. 

> [!NOTE]
> Ausstehende Auftragsbenachrichtigungen werden bei einem bevorstehenden Update von Dynamics 365 for Retail ermöglicht. 


