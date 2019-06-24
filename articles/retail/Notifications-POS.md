---
title: Auftragsbenachrichtigungen in der Verkaufsstelle (POS) anzeigen
description: In diesem Thema wird beschrieben, wie Auftragsbenachrichtigungen in der Verkaufsstelle und im Benachrichtigungsframework aktiviert werden, die für andere Arbeitsgänge erweitert werden können.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6c813cfea9b570e8dfd5dbe7f3ca1f4ba8594420
ms.sourcegitcommit: ffc37f7c2a63bada3055f37856a30424040bc9a3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/16/2019
ms.locfileid: "1577979"
---
# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>Auftragsbenachrichtigungen in der Verkaufsstelle (POS) anzeigen

[!include [banner](includes/banner.md)]

In der heutigen, modernen Retailumgebung werden Filialmitarbeitern verschiedene Aufgaben zugewiesen, wie Kunden zu helfen, Transaktionen einzugeben, Lagerbestände zu zählen und Aufträge in der Filiale entgegenzunehmen. Der Verkaufsstellen-(POS)-Client ermöglicht es den Mitarbeitern, diese Aufgaben und noch viel mehr auszuführen, alles in eine einzigen Anwendung. Bei den verschiedenen Aufgaben, die im Lauf des Tages auszuführen sind, müssen Mitarbeiter möglicherweise darüber benachrichtigt werden, wenn etwas Ihre Aufmerksamkeit erfordert. Das Benachrichtigungsframework in der POS löst dieses Problem, indem es Einzelhändlern ermöglicht, rollenbasierte Benachrichtigungen zu konfigurieren. In Microsoft Dynamics 365 for Retail mit dem Anwendungsupdate 5 können diese Benachrichtigungen nur für POS-Arbeitsgänge konfiguriert werden.

So kann das System Auftragserfüllungsarbeitsgänge nur für Benachrichtigungen anzeigen. Da jedoch das Framework entwickelt wurde, um erweiterbar werden, sind alle Entwickler in der Lage, einen Benachrichtigungshandler für einen Arbeitsgang zu verfassen und die Benachrichtigungen für diesen Arbeitsgang im POS angezeigt.

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Aktivieren von Benachrichtigungen für Auftragserfüllungsarbeitsgänge

Um Benachrichtigungen für die Auftragserfüllungsarbeitsgänge zu aktivieren, beachten Sie die folgenden Schritte:

1. Wechseln Sie zu **Retail** &gt; **Kanaleinstellungen** &gt; **POS-Einstellungen** &gt; **POS** &gt; **Betrieb**.
2. Suchen Sie nach dem Arbeitsgang **Auftragserfüllung** und aktivieren Sie das Kontrollkästchen **Aktivieren Sie Benachrichtigungen** sodass das Benachrichtigungsframework aud den Handler für diesen Arbeitsgang hört. Wenn der Handler implementiert wird, werden Benachrichtigungen für diesen Arbeitsgang dann am Point-of-Sale angezeigt.
3. Gehen Sie zu **Retail** &gt; **Mitarbeiter** &gt; **Arbeitskräfte** &gt;, unter Registerkarte Retail, öffnen Sie POS-Berechtigungen, die der Arbeitskraft zugeordnet werden. Erweitern Sie das Inforegister **Benachrichtigungen**, fügen Sie den **Auftragserfüllung** Arbeitsgang hinzu, und legen Sie das Feld **Anzeigereihenfolge** auf **1** fest. Wenn mehrere Benachrichtigung konfiguriert sind, wird es dazu verwendet, die Benachrichtigungen anzuordnen. Benachrichtigungen, die geringer sind als der Wert **Anzeigereihenfolge** erscheinen über Benachrichtigungen, die einen höheren Wert haben. Benachrichtigungen, die einen Wert **Anzeigereihenfolge** **1** besitzen, werden oben angezeigt.

    Benachrichtigungen werden nur für Arbeitsgänge angezeigt, die auf dem Inforegister **Benachrichtigungen** hinzugefügt werden, und Sie können Arbeitsgänge dort hinzufügen, wenn das Kontrollkästchen **Aktivieren Sie Benachrichtigungen** für diese Einzelvorgänge auf der Seite **POS-Vorgängen** aktiviert wurde. Darüber hinaus werden Benachrichtigungen für einen Arbeitsgang angezeigt, wenn der Arbeitsgang zu den POS-Berechtigungen für diese Arbeitskräfte hinzugefügt wird.

    > [!NOTE]
    > Benachrichtigungen können in der Benutzerebene überschrieben werden. Öffnen Sie den Datensatz der Arbeitskraft, wählen Sie **POS-Berechtigungen** aus und bearbeiten Sie dann die Benachrichtigungsdauerauftrag des Benutzers.

4. Klicken Sie auf **Retail und Handel** &gt; **Kanaleinrichtung** &gt; **POS-Einrichtung** &gt; **POS-Profil** &gt; **Funktionsprofile**. Wählen Sie im Feld **Benachrichtigungsintervall**, wieoft Benachrichtigungen abgerufen werden sollen. Für mehrere Benachrichtigungen muss der POS Echtzeitanrufe der Backofficebewerbung vornehmen. Diese Anrufe verbrauchen die Berechnungskapazität der Backofficebewerbung. Wenn das Benachrichtigungsintervall festlegen, sollten Sie Ihre geschäftlichen Anforderungen und die Auswirkung von Echtzeitanrufen der Backofficebewerbung berücksichtigen. Ein Wert **0** (Null) stellt Benachrichtigungen ab.
5. Klicken Sie auf **Einzelhandel** &gt; **Handel IT** &gt; **Vertriebsplan**. Wählen Sie den Zeitplan **1060** (**Mitarbeiter**) aus, um die Benachrichtungsabonnementeinstellungen zu synchronisieren, und klicken Sie dann auf **Jetzt ausführen**. Synchronisieren Sie danach das Berechtigungsintervall, indem Sie die **1070** (**Kanalkonfiguration**) auswählen, und klicken Sie dann auf **Jetzt ausführen**.

## <a name="view-notifications-in-the-pos"></a>Benachrichtigungen in POS anzeigen

Nachdem Sie die obigen Schritte ausgeführt haben, sind die Arbeitskräfte in der Lage, die Benachrichtigungen im POS anzuzeigen. Um die Benachrichtigungen anzuzeigen, klicken Sie auf das Benachrichtigungssymbol in der rechten oberen Ecke des POS. Dadurch wird das Benachrichtigungscenter mit den Benachrichtigungen für den Auftragserfüllungsarbeitsgang angezeigt. Das Benachrichtigungscenter sollte die folgenden Gruppen innerhalb des Auftragserfüllungsarbeitsgangs anzeigen:

- **Filialabholung** – In dieser Gruppe wird die Anzahl von Aufträgen angezeigt, die den Liefermodus **Abholung** haben, und ihre Abholung ist von der aktuellen Filiale geplant. Sie können die Nummer auf der Gruppen drücken, um die Seite **Bestellungs-Erfüllung** zu öffnen. In diesem Fall wird die Seite gefiltert, sodass diese nur die aktiven Aufträge anzeigt, die für "Keine Abholung" vom aktuellen Shop eingerichtet werden.
- **Von Filiale versenden** – In dieser Gruppe wird die Anzahl von Aufträgen angezeigt, die den Liefermodus **Versand** haben, und der Versand ist von der aktuellen Filiale geplant. Sie können die Nummer auf der Gruppen drücken, um die Seite **Bestellungs-Erfüllung** zu öffnen. In diesem Fall wird die Seite gefiltert, sodass diese nur die aktiven Aufträge anzeigt, die für "Keine Lieferung" vom aktuellen Shop eingerichtet werden.

Wenn neue Aufträge der Filiale zur Erfüllung zugewiesen werden, ändert sich das Benachrichtigungssymbol, um die neuen Benachrichtigungen anzuzeigen, und die Anzahl der entsprechenden Gruppen wird aktualisiert. Obwohl die Gruppen in regelmäßigen Zeitabständen aktualisiert werden, können POS-Benutzer die Gruppen jederzeit manuell aktualisieren, indem Sie die Schaltfläche **Aktualisieren** neben der Gruppe auswählen. Wenn eine Gruppe einen neuen Artikel hat, den die aktuelle Arbeitskraft nicht angezeigt hat, zeigt die Gruppe ein Burstsymbol an, um neuen Inhalt anzuzeigen.

## <a name="enable-live-content-on-pos-buttons"></a>Aktivieren Sie Liveinhalt auf POS-Schaltflächen

POS-Schaltflächen können jetzt eine Anzahl anzeigen, damit Arbeitskräfte einfach bestimmen können welche Aufgaben ihre umgehende Aufmerksamkeit erfordern. Um diese Nummer in einer POS-Schaltfläche anzuzeigen, müssen Sie die Einstellungen Benachrichtigung abschließen, die weiter oben in diesem Thema beschrieben werden (das heißt, Sie müssen Benachrichtigungen für einen Arbeitsgang aktivieren und richten ein Benachrichtigungsintervall und die POS-Berechtigungsgruppe für die Arbeitskraft ein.) Darüber hinaus müssen Sie das Schaltflächenrasterdesigner öffnen, die Eigenschaften der Schaltfläche anzeigen und **Aktivieren Sie Liveinhalt** aktivieren. Im Feld **Inhalts-Ausrichtung** können Sie auswählen, ob die Anzahl in der oberen rechten Ecke der Schaltfläche (**Oben rechts**) oder im Verteilzentrum (**Mitte**) angezeigt wird.

> [!NOTE]
> Der Liveinhalt kann für Arbeitsgänge aktiviert werden, wenn das Feld **Aktivieren Sie Benachrichtigungen** auf der Seite **POS-Vorgängen** aktiviert wurde, wie weiter oben in diesem Thema beschrieben wurde.

Die folgende Abbildung zeigt die Inhaltseinstellungen, die im Schaltflächenrasterdesigner angezeigt werden.

![Live-Inhaltseinstellungen im Schaltflächenrasterdesigner](./media/ButtonGridDesigner.png "Live-Inhaltseinstellungen im Schaltflächenrasterdesigner")

Um die Benachrichtigungsanzahl auf einer Schaltfläche anzuzeigen, müssen Sie sicherstellen, dass das korrekte Bildschirmlayout aktualisiert wird. Um das Bildschirmlayout zu bestimmen, das vom POS verwendet wird, wählen Sie das Symbol **Einstellungen** in der oberen rechten Ecke aus und beachten Sie die **Bildschirmlayoutkennung** und die **Layoutlösung**. Wechseln Sie jetzt mithilfe des Edge-Browsers zur Seite **Bildschirmlayout** in Dynamics 365 for Finance and Operations, suchen Sie die oben identifizierte **Bildschirmlayoutkennung** und **Layoutauflösung** und aktivieren Sie das Kontrollkästchen **Liveinhalt aktivieren**. Wechseln Sie zu **Einzelhandel \> IT (Einzelhandel) \> Vertriebsplan** und führen Sie den Einzelvorgang 1090 (Register) aus, um Layoutänderungen zu synchronisieren.

![Suchen Sie das von POS verwendete Bildschirmlayout](./media/Choose_screen_layout.png "Suchen Sie das von POS verwendete Bildschirmlayout ")

Die folgende Abbildung zeigt die Auswirkungen der Auswahl **Oben rechts** versus **Mitte** im Feld **Inhalts-Ausrichtung** für Schaltflächen für verschiedene Mengen an.

![Live Inalt auf POS-Schaltfläche](./media/ButtonsWithLiveContent.png "Live Inalt auf POS-Schaltfläche")
