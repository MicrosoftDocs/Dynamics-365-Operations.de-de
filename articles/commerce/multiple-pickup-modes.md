---
title: Mehrere Lieferarten zur Abholung für Kundenaufträge
description: In diesem Artikel wird die Funktionalität in Microsoft Dynamics 365 Commerce erklärt, mit der Sie Kundenaufträge für die Abholung in einem Ladengeschäft erstellen können.
author: hhainesms
ms.date: 12/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: e4d8883b3dc1c4a0e12bcb00b6441f76d73da92e
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831583"
---
# <a name="enable-multiple-pickup-delivery-modes-for-customer-orders"></a>Mehrere Lieferarten zur Abholung für Kundenaufträge

[!include [banner](includes/banner.md)]


In Microsoft Dynamics 365 Commerce können Organisationen mehrere Lieferarten definieren, zwischen denen Käufer oder Vertriebsmitarbeiter wählen können, wenn sie einen Auftrag erstellen, der in einem Ladengeschäft abgeholt wird. Auf diese Weise können Organisationen ihren Kunden mehrere Abholoptionen anbieten. Beispielsweise bieten viele Einzelhändler ihren Kunden jetzt die Wahl zwischen Abholung im Geschäft oder Abholung am Straßenrand für ihre Aufträge an. Commerce unterstützt die Konfiguration dieser verschiedenen Abhollieferarten. Benutzer können sie dann nutzen, wenn sie Kundenaufträge in irgendeinem unterstützten Commerce-Kanal (E-Commerce, Callcenter oder Geschäft) erstellen.

## <a name="enable-and-configure-pickup-delivery-modes"></a>Abhollieferarten aktivieren und konfigurieren

Die Funktion **Unterstützung für mehrere Abhollieferarten** im Arbeitsbereich **Funktionsverwaltung** in Commerce headquarters wurde verpflichtend gemacht und sollte in der Umgebung aktiviert werden.

Wenn Sie zuvor auf der Seite **Commerce-Parameter** einen Abhol-Liefermodus definiert haben, wird dieser Modus in der aktuellen Konfiguration für Abhol-Liefermodi angezeigt.

![Abhollieferarten auf der Seite „Commerce-Parameter“.](media/multiplepickupparameter.png)

Sie können im Raster **Abholart der Lieferung** unter **Commerce-Parameter** > **Kundenbestellungen** mehrere Abhol-Liefermodi definieren Tab > **Lieferarten** FastTab.  

Die Felder **Lieferart durchführen** und **Elektronische Lieferart** und die Option **Nur Spediteurartoptionen für Lieferaufträge anzeigen** wurden zu diesem Inforegister verlegt.

Bevor Sie zusätzliche Abhollieferarten konfigurieren, müssen Sie die Lieferarten definieren. Auf der Seite **Lieferarten** in der Commerce-Zentralverwaltung fügen Sie Lieferarten hinzu, die als Abhollieferarten gelten sollen. Stellen Sie sicher, dass die gesamte Konfiguration abgeschlossen ist. Wenn Sie beispielsweise Ihren Online-Shoppern für bestimmte Geschäfte die Abholung bis zur Bordsteinkante als Lieferoption anbieten, müssen Sie hierfür einen neuen Liefermodus erstellen. Sie können diese Lieferart mit „Abholung am Straßenrand“ als Beschreibung erstellen. Stellen Sie dann sicher, dass die Lieferart „Abholung am Straßenrand“ allen E-Commerce-Kanälen zugeordnet ist, die sie anbieten können, einschließlich Online-Shops, die diese Option anbieten, und den einzelnen Shop-Kanälen, die diese Versandmethode anbieten. Auch die Lieferarten müssen mit den Produkten verknüpft sein. In diesem Beispiel müssen Sie sicherstellen, dass diese Artikel ausgeschlossen werden, wenn bestimmte Produkte nicht mit der „Abholung am Straßenrand“ geliefert werden können. Wenn Sie fertig alle neuen Lieferarten hinzugefügt haben, führen Sie den Einzelvorgang **Lieferarten verarbeiten** aus, um die Beziehungen zwischen den Lieferarten, Kanälen und Artikeln zu erstellen. Wenn die Ausführung des Einzelvorgangs beendet ist, öffnen Sie die Seite **Verteilungszeitplan** in der Commerce-Zentralverwaltung und führen Sie den Verteilungseinzelvorgang **1120** aus, um sicherzustellen, dass die relevanten Commerce-Kanaldatenbanken mit Ihrer neuen Lieferartkonfiguration aktualisiert werden.

![Beispiel für eine Lieferartkonfiguration für die Abholung am Straßenrand.](media/pickupmodes.png)

Nachdem Sie die zusätzlichen Abhollieferarten definiert haben, fügen Sie diese dem Raster **Abhollieferart** auf der Seite **Commerce-Parameter** hinzu. Führen Sie dann die entsprechenden Verteilungseinzelvorgänge aus, um die relevanten Commerce-Kanaldatenbanken mit der Konfigurationsänderung zu aktualisieren.

> [!NOTE]
> Abgesehen von der vorhandenen Abhollieferart, die in das Raster **Abhollieferart** kopiert wird, wenn Sie die Fu‭nktion **Unterstützung für mehrere Abhollieferarten** aktivieren, sollten Sie für jede zusätzliche Abhollieferartkonfiguration, die Sie erstellen, neue Lieferarten konfigurieren. Wenn Sie dem Raster **Abhollieferart** Lieferarten hinzufügen, überprüft Commerce, ob irgendwelche aktiven offenen Verkaufspositionen sie bereits verwenden. Wenn irgendwelche offenen Verkaufspositionen gefunden werden, erhalten Sie eine Fehlermeldung. Lieferarten gelten erst als Abhollieferarten, wenn alle offenen Verkaufspositionen, die sie verwenden, geschlossen wurden (entweder fakturiert oder storniert).


### <a name="e-commerce-site-configurations"></a>E-Commerce-Websitekonfigurationen

Wenn die Funktion **Unterstützung für mehrere Abhollieferarten** aktiviert ist, zeigen die folgenden Module auf den E-Commerce-Seiten die neuen Abhollieferarten als konfiguriert an:

- Kauffeld
- Shopauswahl
- Einkaufskorb
- Abholinformationen
- Auftragsbestätigung
- Auftragsdetails

Auf E-Commerce-Seiten sind keine zusätzlichen Schritte erforderlich, um die Abhollieferarten verfügbar zu machen.

## <a name="work-with-multiple-pickup-delivery-modes"></a>Mit mehreren Abhollieferarten arbeiten

Wenn für einen Kanal mehrere Abhollieferarten verfügbar sind, wird Kunden eine erweiterte Umgebung bereitgestellt, wenn sie Produkte einkaufen, die abgeholt werden. 

- In E-Commerce-Kanälen können Einkäufer jede beliebige gültige Abhollieferart auswählen, die verfügbar ist. Beispielsweise definiert ein Einzelhändler zwei Abhollieferarten (Abholung im Laden und Abholung am Straßenrand), beide werden im Raster **Abhollieferart** konfiguriert und beide sind für den Auftragserfüllungskanal sowie das Produkt, das der Einkäufer aktuell kauft, gültig. In diesem Fall kann der Käufer seine bevorzugte Abhollieferart auswählen. Die bevorzugte Abhollieferart wird dann die Lieferart, die mit der Auftragsposition verknüpft wird, wenn der Auftrag in der Commerce-Zentralverwaltung erstellt wird.

    ![Auswahl einer Abholoption in E-Commerce.](media/pickupecommerce.png)

- In Geschäftskanälen, wenn ein Kundenauftrag zur Abholung über die Verkaufsstellen-(POS)-Anwendung erstellt wird, wird der Vertriebsmitarbeiter dazu aufgefordert, aus den verfügbaren Abhollieferarten auszuwählen, sofern welche konfiguriert wurden. Wenn nur eine gültige Abhollieferart für den Kanal und Artikel verfügbar ist, wird der Vertriebsmitarbeiter nicht dazu aufgefordert, sie auszuwählen. Stattdessen wird die verfügbare Abhollieferart automatisch auf die Auftragspositionen angewendet.

    ![Auswahl einer Abholoption in der POS-Anwendung.](media/pickuppos.png)

- Wenn in Callcenterkanälen Benutzer Abholaufträge erstellen, können sie manuell jede beliebige definierte Abhollieferart auswählen, die mit dem Callcenterkanal verknüpft ist. Das System überprüft dann, ob die ausgewählte Abhollieferart verwendet werden kann, wenn der Artikel, der mit ihr verknüpft wird, bestellt wird. Wenn in Callcenterkanälen eine Abhollieferart ausgewählt wird, müssen die Auftragspositionen mit einem gültigen Geschäftslagerort verknüpft sein. Wenn für eine Callcenterverkaufsposition ein nicht zum Geschäft gehöriger Lagerort definiert wird, kann für diese Verkaufsposition keine Abhollieferart festgelegt werden.
- Vertriebsmitarbeiter können den Vorgang **Auftragsrückruf** oder **Auftragserfüllung** in der POS-Anwendung verwenden, um eine Auftragsliste oder Auftragspositionen für die Abholung abzurufen. Wenn ein Vertriebsmitarbeiter einen vordefinierten Suchfilter verwendet, um alle Aufträge anzuzeigen, die im aktuellen Geschäft abgeholt werden, werden die Abfragen geändert, um sicherzustellen, dass die Suchergebnisse alle in Frage kommenden Aufträge umfassen, die irgendeine Abhollieferart verwenden. POS-Benutzer können auch vorhandene Filter verwenden, um die Liste der Aufträge auf eine bestimmte Abhollieferart einzugrenzen. Beispielsweise können sie nur Auftrage für die Abholung am Straßenrand anzeigen.

    ![Filter für Abhollieferarten, der auf eine Liste von Rückrufaufträgen angewendet wird.](media/pickuprecallorder.png)

## <a name="considerations-for-distributed-order-management"></a>Berücksichtigungen bei der verteilten Auftragsverwaltung

Die [verteilte Auftragsverwaltung (DOM)](./dom.md)-Funktionen in Commerce ignorieren jegliche Verkaufspositionen, die für die Abholung im Geschäft markiert sind. Diese Funktionen wurden aktualisiert, um sicherzustellen, dass Verkaufspositionen, die mit konfigurierten Abhollieferarten verknüpft sind, die DOM-Logik umgehen und nicht einem neuen Erfüllungslagerort neu zugeordnet werden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
