---
title: Mehrere Lieferarten zur Abholung für Kundenaufträge
description: In diesem Thema wird die Funktionalität in Microsoft Dynamics 365 Commerce erklärt, mit der Sie Kundenaufträge für die Abholung in einem Ladengeschäft erstellen können.
author: hhainesms
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: c32ffc8435c05c644bf836bb184400d067269208
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796875"
---
# <a name="enable-multiple-pickup-delivery-modes-for-customer-orders"></a>Mehrere Lieferarten zur Abholung für Kundenaufträge

[!include [banner](includes/banner.md)]


In Microsoft Dynamics 365 Commerce Version 10.0.16 und höher können Organisationen mehrere Lieferarten definieren, zwischen denen Käufer oder Vertriebsmitarbeiter wählen können, wenn sie einen Auftrag erstellen, der in einem Ladengeschäft abgeholt wird. Auf diese Weise können Organisationen ihren Kunden mehrere Abholoptionen anbieten. Beispielsweise bieten viele Einzelhändler ihren Kunden jetzt die Wahl zwischen Abholung im Geschäft oder Abholung am Straßenrand für ihre Aufträge an. Commerce unterstützt die Konfiguration dieser verschiedenen Abhollieferarten. Benutzer können sie dann nutzen, wenn sie Kundenaufträge in irgendeinem unterstützten Commerce-Kanal (E-Commerce, Callcenter oder Geschäft) erstellen.

## <a name="enable-and-configure-pickup-delivery-modes"></a>Abhollieferarten aktivieren und konfigurieren

Um diese Funktionalität zu nutzen, aktivieren Sie die Funktion **Unterstützung für mehrere Abhollieferarten** im Arbeitsbereich **Funktionsverwaltung** in der Commerce-Zentralverwaltung. Nachdem Sie die Funktion aktiviert haben, ist eine zusätzliche Konfiguration erforderlich.

In Commerce Version 10.0.15 und früheren Versionen können Organisationen nur eine Lieferart als festgelegte Abhollieferart definieren. Diese Definition erfolgt auf der Seite **Commerce-Parameter**. In Version 10.0.16 und höher wird bei Aktivierung der Funktion **Unterstützung für mehrere Abhollieferarten** die zuvor auf der Seite **Commerce-Parameter** definierte Lieferart automatisch in die neue Konfiguration für Abhollieferarten kopiert.

![Abhollieferarten auf der Seite „Commerce-Parameter“](media/multiplepickupparameter.png)

Nachdem Sie die Funktion **Unterstützung für mehrere Abhollieferarten** aktivieren, können Sie mehrere Abhollieferarten im Raster **Abhollieferart** im Inforegister **Lieferarten** auf der Registerkarte **Kundenaufträge** auf der Seite **Commerce-Parameter** definieren.

Die Felder **Lieferart durchführen** und **Elektronische Lieferart** und die Option **Nur Spediteurartoptionen für Lieferaufträge anzeigen** wurden zu diesem Inforegister verlegt.

Bevor Sie zusätzliche Abhollieferarten konfigurieren, müssen Sie die Lieferarten definieren. Auf der Seite **Lieferarten** in der Commerce-Zentralverwaltung fügen Sie Lieferarten hinzu, die als Abhollieferarten gelten sollen. Stellen Sie sicher, dass die gesamte Konfiguration abgeschlossen ist. Stellen Sie beispielsweise sicher, dass die Lieferart mit den entsprechenden Kanälen und Artikeln verknüpft ist. Wenn Sie fertig sind, führen Sie den Einzelvorgang **Lieferarten verarbeiten** aus, um die Beziehungen zwischen den Lieferarten, Kanälen und Artikeln zu erstellen. Wenn die Ausführung des Einzelvorgangs beendet ist, öffnen Sie die Seite **Verteilungszeitplan** in der Commerce-Zentralverwaltung und führen Sie den Verteilungseinzelvorgang **1120** aus, um sicherzustellen, dass die relevanten Commerce-Kanaldatenbanken mit Ihrer neuen Lieferartkonfiguration aktualisiert werden.

![Beispiel für eine Lieferartkonfiguration für die Abholung am Straßenrand](media/pickupmodes.png)

Nachdem Sie die zusätzlichen Abhollieferarten definiert haben, fügen Sie diese dem Raster **Abhollieferart** auf der Seite **Commerce-Parameter** hinzu. Führen Sie dann die entsprechenden Verteilungseinzelvorgänge aus, um die relevanten Commerce-Kanaldatenbanken mit der Konfigurationsänderung zu aktualisieren.

> [!NOTE]
> Abgesehen von der vorhandenen Abhollieferart, die in das Raster **Abhollieferart** kopiert wird, wenn Sie die Fu‭nktion **Unterstützung für mehrere Abhollieferarten** aktivieren, sollten Sie für jede zusätzliche Abhollieferartkonfiguration, die Sie erstellen, neue Lieferarten konfigurieren. Wenn Sie dem Raster **Abhollieferart** Lieferarten hinzufügen, überprüft Commerce, ob irgendwelche aktiven offenen Verkaufspositionen sie bereits verwenden. Wenn irgendwelche offenen Verkaufspositionen gefunden werden, erhalten Sie eine Fehlermeldung. Lieferarten gelten erst als Abhollieferarten, wenn alle offenen Verkaufspositionen, die sie verwenden, geschlossen wurden (entweder fakturiert oder storniert).

> [!IMPORTANT]
> Nachdem Sie mehr als eine Abhollieferart auf der Seite **Commerce-Parameter** definiert haben, wird die Funktion **Unterstützung für mehrere Abhollieferarten** obligatorisch und kann nicht mehr deaktiviert werden. Wenn Sie die Funktion deaktivieren müssen, entfernen Sie alle Abhollieferarten aus dem Raster **Abhollieferart** mit Ausnahme von einer. Wenn nur eine Abhollieferart definiert ist, gilt die Funktion nicht mehr als obligatorisch und kann deaktiviert werden.

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

    ![Auswahl einer Abholoption in E-Commerce](media/pickupecommerce.png)

- In Geschäftskanälen, wenn ein Kundenauftrag zur Abholung über die Verkaufsstellen-(POS)-Anwendung erstellt wird, wird der Vertriebsmitarbeiter dazu aufgefordert, aus den verfügbaren Abhollieferarten auszuwählen, sofern welche konfiguriert wurden. Wenn nur eine gültige Abhollieferart für den Kanal und Artikel verfügbar ist, wird der Vertriebsmitarbeiter nicht dazu aufgefordert, sie auszuwählen. Stattdessen wird die verfügbare Abhollieferart automatisch auf die Auftragspositionen angewendet.

    ![Auswahl einer Abholoption in der POS-Anwendung](media/pickuppos.png)

- Wenn in Callcenterkanälen Benutzer Abholaufträge erstellen, können sie manuell jede beliebige definierte Abhollieferart auswählen, die mit dem Callcenterkanal verknüpft ist. Das System überprüft dann, ob die ausgewählte Abhollieferart verwendet werden kann, wenn der Artikel, der mit ihr verknüpft wird, bestellt wird. Wenn in Callcenterkanälen eine Abhollieferart ausgewählt wird, müssen die Auftragspositionen mit einem gültigen Geschäftslagerort verknüpft sein. Wenn für eine Callcenterverkaufsposition ein nicht zum Geschäft gehöriger Lagerort definiert wird, kann für diese Verkaufsposition keine Abhollieferart festgelegt werden.
- Vertriebsmitarbeiter können den Vorgang **Auftragsrückruf** oder **Auftragserfüllung** in der POS-Anwendung verwenden, um eine Auftragsliste oder Auftragspositionen für die Abholung abzurufen. Wenn ein Vertriebsmitarbeiter einen vordefinierten Suchfilter verwendet, um alle Aufträge anzuzeigen, die im aktuellen Geschäft abgeholt werden, werden die Abfragen geändert, um sicherzustellen, dass die Suchergebnisse alle in Frage kommenden Aufträge umfassen, die irgendeine Abhollieferart verwenden. POS-Benutzer können auch vorhandene Filter verwenden, um die Liste der Aufträge auf eine bestimmte Abhollieferart einzugrenzen. Beispielsweise können sie nur Auftrage für die Abholung am Straßenrand anzeigen.

    ![Filter für Abhollieferarten, der auf eine Liste von Rückrufaufträgen angewendet wird](media/pickuprecallorder.png)

## <a name="considerations-for-distributed-order-management"></a>Berücksichtigungen bei der verteilten Auftragsverwaltung

Die [verteilte Auftragsverwaltung (DOM)](https://docs.microsoft.com/dynamics365/commerce/dom)-Funktionen in Commerce ignorieren jegliche Verkaufspositionen, die für die Abholung im Geschäft markiert sind. Diese Funktionen wurden aktualisiert, um sicherzustellen, dass Verkaufspositionen, die mit konfigurierten Abhollieferarten verknüpft sind, die DOM-Logik umgehen und nicht einem neuen Erfüllungslagerort neu zugeordnet werden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]