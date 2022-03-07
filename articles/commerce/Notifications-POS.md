---
title: Auftragsbenachrichtigungen in der Verkaufsstelle (POS) anzeigen
description: In diesem Thema wird beschrieben, wie Auftragsbenachrichtigungen in der Verkaufsstelle und im Benachrichtigungsframework aktiviert werden, die für andere Arbeitsgänge erweitert werden können.
author: ShalabhjainMSFT
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7166afdb43c7e835170c5768a0767f2943222b19c00c7d0aaf067263845651f8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714137"
---
# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>Auftragsbenachrichtigungen in der Verkaufsstelle (POS) anzeigen

[!include [banner](includes/banner.md)]

Shopmitarbeitern werden in ihrem Shop verschiedene Aufgaben zugewiesen, z. B. das Erledigen von Aufträgen, das Durchführen von Bestandsannahmen oder Bestandszählungen. Mithilfe des Verkaufsstellen-(POS)-Clients werden Mitarbeiter über diese Aufgaben informiert – in einer einzigen Anwendung. Das Benachrichtigungsframework in der POS löst dieses Problem, indem es Einzelhändlern ermöglicht, rollenbasierte Benachrichtigungen zu konfigurieren. Beginnend mit dem Anwendungsupdate 5 von Dynamics 365 Retail können diese Benachrichtigungen für POS-Vorgänge konfiguriert werden.

Das System kann Benachrichtigungen für den Vorgang *Auftragserfüllung* und ab Commerce-Version 10.0.18 sogar Benachrichtigungen für den Vorgang *Auftrag zurückrufen* anzeigen. Da jedoch das Framework für Erweiterbarkeit entwickelt wurde, sind alle Entwickler in der Lage, [einen Benachrichtigungshandler](dev-itpro/extend-pos-notification.md) für einen Vorgang zu verfassen und die Benachrichtigungen für diesen Arbeitsgang in POS anzuzeigen.

## <a name="enable-notifications-for-order-fulfillment-or-recall-order-operations"></a>Benachrichtigungen für Vorgänge zur Auftragserfüllung oder zu Auftragsrückrufen aktivieren

Um Benachrichtigungen für Auftragserfüllungs- oder Auftragsrückrufvorgänge zu aktivieren, befolgen Sie die folgenden Schritte:

1. Rufen Sie **Retail und Commerce \> Kanaleinrichtung \> POS-Einrichtung \> POS \> Vorgänge** auf.
1. Suchen Sie entweder nach dem Vorgang **Auftragserfüllung** oder dem Vorgang **Auftrag zurückrufen**. Wählen Sie nun für den Vorgang **Benachrichtigungen aktivieren** aus, damit das Benachrichtigungsframework auf den Handler für diesen Vorgang achtet. Wenn der Handler implementiert wird, werden Benachrichtigungen für diesen Arbeitsgang dann am Point-of-Sale angezeigt.
1. Rufen Sie **Retail und Commerce \> Mitarbeiter \> Arbeitskräfte** auf.
1. Wählen Sie die Registerkarte **Commerce** und eine Arbeitskraftzeile aus. Wählen Sie anschließend **POS-Berechtigungen** aus. Wählen Sie das Inforegister **Benachrichtigungen** aus, und erweitern Sie es. Fügen Sie dann die Vorgänge hinzu, für die Sie Benachrichtigungen aktiviert haben. Wenn Sie eine einzelne Benachrichtigung für eine Arbeitskraft konfigurieren, vergewissern Sie sich, dass der Wert **Anzeigereihenfolge** auf **1** gesetzt ist. Wenn Sie mehr als einen Vorgang konfigurieren, stellen Sie die **Anzeigereihenfolge**-Werte ein, um die Reihenfolge anzugeben, in der die Benachrichtigungen angezeigt werden sollen. 

      Benachrichtigungen werden nur für Vorgänge angezeigt, die dem Inforegister **Benachrichtigungen** hinzugefügt wurden. Sie können dort nur Vorgänge hinzufügen, wenn das Kontrollkästchen **Benachrichtigungen aktivieren** für diese Vorgänge auf der Seite **POS-Vorgänge** aktiviert worden ist. Darüber hinaus werden Benachrichtigungen für einen Vorgang Arbeitskräften nur angezeigt, wenn der Vorgang den POS-Berechtigungen für diese Arbeitskräfte hinzugefügt worden ist.

    > [!NOTE]
    > Benachrichtigungen können in der Benutzerebene überschrieben werden. Öffnen Sie dazu den Datensatz der Arbeitskraft, wählen Sie **POS-Berechtigungen** aus, und bearbeiten Sie dann die Benachrichtigungsdauerauftrag des Benutzers.

1. Gehen Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Funktionsprofile**. Wählen Sie im Feld **Benachrichtigungsintervall**, wieoft Benachrichtigungen abgerufen werden sollen. Für mehrere Benachrichtigungen muss der POS Echtzeitanrufe der Backofficebewerbung vornehmen. Diese Anrufe verbrauchen die Berechnungskapazität der Backofficebewerbung. Wenn das Benachrichtigungsintervall festlegen, sollten Sie Ihre geschäftlichen Anforderungen und die Auswirkung von Echtzeitanrufen der Backofficebewerbung berücksichtigen. Ein Wert **0** (Null) stellt Benachrichtigungen ab.
1. Gehen Sie zu **Einzelhandel und Handel \> Einzelhandel und Handel IT \> Vertriebsplan**. Wählen Sie den Zeitplan **1060** (**Mitarbeiter**) aus, um die Benachrichtungsabonnementeinstellungen zu synchronisieren, und klicken Sie dann auf **Jetzt ausführen**. Synchronisieren Sie danach das Berechtigungsintervall, indem Sie die **1070** (**Kanalkonfiguration**) auswählen, und klicken Sie dann auf **Jetzt ausführen**.

## <a name="view-notifications-in-the-pos"></a>Benachrichtigungen in POS anzeigen

Nachdem Sie die obigen Schritte ausgeführt haben, sind die Arbeitskräfte in der Lage, die Benachrichtigungen im POS anzuzeigen. Um die Benachrichtigungen anzuzeigen, wählen Sie das Benachrichtigungssymbol in der rechten oberen Ecke von POS aus. Ein Benachrichtigungsfenster wird angezeigt und zeigt Benachrichtigungen für die für die Arbeitskraft konfigurierten Vorgänge an. 

Das Benachrichtigungsfenster zeigt die folgenden Gruppen für den Vorgang **Auftragserfüllung** an:

- **Filialabholung** – In dieser Gruppe wird die Anzahl einzelner Auftragspositionen angezeigt, die zur Abholung im aktuellen Shop geplant sind. Sie können die Nummer der Gruppe auswählen, um den Vorgang **Auftragserfüllung** mit einem Filter zu öffnen, sodass nur die aktiven Auftragspositionen angezeigt werden, die für die Abholung im aktuellen Shop eingerichtet sind.
- **Versand ab Filiale** – Diese Gruppe zeigt die Anzahl der einzelnen Auftragspositionen an, die für den Versand aus dem aktuellen Shop des Benutzers konfiguriert wurden. Sie können die Nummer der Gruppe auswählen, um den Vorgang **Auftragserfüllung** in einer gefilterten Ansicht zu öffnen, sodass nur die aktiven Auftragspositionen angezeigt werden, die für den Versand aus dem aktuellen Shop eingerichtet sind.

Das Benachrichtigungsfenster zeigt die folgenden Gruppen für den Vorgang **Auftrag zurückrufen** an:

- **Zu erfüllende Aufträge** – Diese Gruppe zeigt die Anzahl der Aufträge an, die entweder für die Abholung oder die Versandabwicklung im aktuellen Shop des Benutzers konfiguriert wurden. Sie können die Nummer der Gruppe auswählen, um den Vorgang **Auftrag zurückrufen** in einer gefilterten Ansicht zu öffnen, sodass nur die offenen Aufträge angezeigt werden, die vom aktuellen Shop des Benutzers entweder zur Abholung im Shop oder zum Versand ausgeführt werden müssen.
- **Aufträge zur Abholung** – In dieser Gruppe wird die Auftragsanzahl angezeigt, die zur Abholung im aktuellen Shop geplant sind. Sie können die Nummer der Gruppe auswählen, um den Vorgang **Auftrag zurückrufen** in einer gefilterten Ansicht zu öffnen, sodass nur die offenen Aufträge angezeigt werden, die vom aktuellen Shop des Benutzers zur Abholung im Shop ausgeführt werden müssen.
- **Aufträge zum Versand** – Diese Gruppe zeigt die Auftragsanzahl an, die vom aktuellen Shop des Benutzers versendet werden sollen. Sie können die Nummer der Gruppe auswählen, um den Vorgang **Auftrag zurückrufen** in einer gefilterten Ansicht zu öffnen, sodass nur die offenen Aufträge angezeigt werden, die vom aktuellen Shop des Benutzers zum Versand ausgeführt werden müssen.

Wenn neue Aufträge im Prozess aufgenommen werden, ändert sich das Benachrichtigungssymbol sowohl bei den Benachrichtigungen zur Auftragserfüllung als auch zum Auftragsrückruf, um die neuen Benachrichtigungen anzuzeigen. Die Anzahl der entsprechenden Gruppen wird aktualisiert. Obwohl die Gruppen in regelmäßigen Zeitabständen aktualisiert werden, können POS-Benutzer die Gruppen jederzeit manuell aktualisieren, indem Sie auf **Aktualisieren** neben der Gruppe klicken. Wenn eine Gruppe einen neuen Artikel hat, den die aktuelle Arbeitskraft nicht angezeigt hat, zeigt die Gruppe ein Burstsymbol an, um neuen Inhalt anzuzeigen.

## <a name="enable-live-content-on-pos-buttons"></a>Aktivieren Sie Liveinhalt auf POS-Schaltflächen

POS-Schaltflächen können jetzt eine Anzahl anzeigen, damit Arbeitskräfte einfach bestimmen können welche Aufgaben ihre umgehende Aufmerksamkeit erfordern. Um diese Nummer in einer POS-Schaltfläche anzuzeigen, müssen Sie die Einstellungen Benachrichtigung abschließen, die weiter oben in diesem Thema beschrieben werden (das heißt, Sie müssen Benachrichtigungen für einen Arbeitsgang aktivieren und richten ein Benachrichtigungsintervall und die POS-Berechtigungsgruppe für die Arbeitskraft ein.) Darüber hinaus müssen Sie das Schaltflächenrasterdesigner öffnen, die Eigenschaften der Schaltfläche anzeigen und **Aktivieren Sie Liveinhalt** aktivieren. Im Feld **Inhalts-Ausrichtung** können Sie auswählen, ob die Anzahl in der oberen rechten Ecke der Schaltfläche (**Oben rechts**) oder im Verteilzentrum (**Mitte**) angezeigt wird.

> [!NOTE]
> Der Liveinhalt kann für Arbeitsgänge aktiviert werden, wenn das Feld **Aktivieren Sie Benachrichtigungen** auf der Seite **POS-Vorgängen** aktiviert wurde, wie weiter oben in diesem Thema beschrieben wurde.

Die folgende Abbildung zeigt die Inhaltseinstellungen, die im Schaltflächenrasterdesigner angezeigt werden.

![Einstellungen für Live-Inhalte in der Schaltfläche Raster-Designer.](./media/ButtonGridDesigner.png "Einstellungen für Live-Inhalte in der Schaltfläche Raster-Designer")

Um die Benachrichtigungsanzahl auf einer Schaltfläche anzuzeigen, müssen Sie sicherstellen, dass das korrekte Bildschirmlayout aktualisiert wird. Um das Bildschirmlayout zu bestimmen, das vom POS verwendet wird, wählen Sie das Symbol **Einstellungen** in der oberen rechten Ecke aus und beachten Sie die **Bildschirmlayoutkennung** und die **Layoutlösung**. Wechseln Sie jetzt mithilfe des Edge-Browsers zur Seite **Bildschirmlayout**, suchen Sie die oben identifizierte **Bildschirmlayoutkennung** und **Layoutauflösung** und aktivieren Sie das Kontrollkästchen **Liveinhalt aktivieren**. Wechseln Sie zu **Einzelhandel und Handel \> Einzelhandel und Handel IT \> Vertriebsplan** und führen Sie den Einzelvorgang 1090 (Register) aus, um Layoutänderungen zu synchronisieren.

![Suchen Sie das Bildschirmlayout, das vom POS verwendet wird.](./media/Choose_screen_layout.png "Bildschirmlayouts suchen")

Die folgende Abbildung zeigt die Auswirkungen der Auswahl **Oben rechts** versus **Mitte** im Feld **Inhalts-Ausrichtung** für Schaltflächen für verschiedene Mengen an.

![Liveinhalt auf POS-Schaltflächen.](./media/ButtonsWithLiveContent.png "Liveinhalt auf POS-Schaltflächen")

[!INCLUDE[footer-include](../includes/footer-banner.md)]
