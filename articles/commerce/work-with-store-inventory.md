---
title: Bestandsverwaltung im Laden
description: Dieser Artikel beschreibt die Dokumentarten, die Sie zum Verwalten des Bestands verwenden können.
author: rubencdelgado
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c4891f9dcb031f4cb8dfb91f3fe1a301aad9838e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793872"
---
# <a name="commerce-inventory-management"></a>Commerce-Bestandsverwaltung

[!include [banner](includes/banner.md)]

Wenn Sie mit Bestand in Microsoft Dynamics 365 Commerce arbeiten und eine der Commerce-Anwendungen nutzen, die mit einer Commerce Scale Unit (CSU) verbunden sind, ist es wichtig zu wissen, dass die Auftragsverarbeitungslogik in der CSU nur begrenzte Unterstützung für einige Bestandsdimensionen und einige Bestandsartikeltypen bietet. Commerce-Anwendungen unterstützen nicht alle Funktionen zur Artikelkonfiguration, die über die Artikelkonfigurationsoptionen in Dynamics 365 Supply Chain Management verfügbar sind.

Die Commerce-Anwendungen, die auf der CSU laufen, unterstützen folgende Produktdimensionen und Artikelkonfigurationen nicht:

- Konfigurationsproduktdimension und Stücklistenelemente (mit Ausnahme von Einzelhandels-Kit-Produkten, die einige Komponenten des Stücklisten-Frameworks verwenden)
- Artikelgewichtsartikel
- Versionsproduktdimensionsgesteuerte Artikel

Die Commerce-Anwendungen, die auf der CSU laufen, unterstützen folgende Rückverfolgungsangaben nicht:
- Eigentümerdimension

- Die POS-Anwendung (Point of Sale) kann eingeschränkten Support für die folgenden Dimensionen bieten. POS kann einige dieser Dimensionen automatisch in Bestandsbuchungen eingeben, basierend auf der Konfiguration des Lagerorts oder Shops. POS unterstützt die Dimensionen nicht vollständig in der Art und Weise, wie sie unterstützt werden, wenn ein Verkaufsvorgang manuell in der Commerce-Zentrale eingegeben wird. 

- **Lagerort** – Wenn die Benutzer die neuen POS-Vorgänge [Eingangsvorgang](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)und [Ausgangsvorgang](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) verwenden, können sie einen Lagerort auswählen, an dem Artikel empfangen oder ausgehende Transportauftragspositionen versendet werden sollen. Wenn sie den veralteten Vorgang **Entnahme und Empfang** verwenden, steht für den Empfang und Versand ausgehender Transportaufträge eine eingeschränkte Unterstützung für die Standortverwaltung zur Verfügung. Diese Unterstützung ist nur verfügbar, wenn die Option **Prozess der Lagerverwaltung verwenden** für den Artikel und das Lager aktiviert wurde. Ein Lagerort kann derzeit nicht mit dem Vorgang **Bestandsmenge** oder **Bestandssuche** verwendet werden.

- **Ladungsträger** – Ladungsträger gelten nur, wenn **Prozess der Lagerverwaltung verwenden** für den Artikel und den Filiallagerort aktiviert wurde. Im POS, wenn Bestand am Filiallagerort mithilfe des Vorgangs **Eingangsvorgang** oder **Entnahme und Empfang** empfangen wird, bei dem der Lagerverwaltungsprozess aktiviert wurde und der Standort, der für den Empfang der Artikel ausgewählt wurde, mit einen Lagerplatzprofil verknüpft ist, für das Kennzeichensteuerung erforderlich, wendet die POS-Anwendung systematisch einen Ladungsträger für die empfangende Position an. POS-Benutzer können diese Ladungsträgerdaten nicht ändern oder verwalten. Wenn die vollständige Verwaltung von Kennzeichen erforderlich ist, empfehlen wir, dass die Filiale die [Lagerort-App](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/install-configure-warehousing-app) oder den Backoffice-ERP-Client verwenden, um den Eingang dieser Artikel zu verwalten.

- **Seriennummer** – Die POS-Anwendung bietet eine begrenzte Unterstützung für die Registrierung einzelner Seriennummern in einer Transaktionsverkaufsposition für Aufträge, die in POS erstellt werden und serialisierte Artikel enthalten. Die Seriennummer wird nicht gegen registrierte Seriennummern geprüft, die bereits im Bestand sind. Wenn ein Auftrag in Callcenterkanal erstellt oder durch das Enterprise Resource Planning (ERP) erfüllt wird und während des Erfüllungsprozesses im ERP mehrere Seriennummern für eine einzelne Auftragsverkaufsposition erfasst werden, können diese Seriennummern nicht angewendet oder geprüft werden, wenn eine Rücklieferung im POS für diese Aufträge verarbeitet wird. Wenn der Bestand mithilfe des Vorgangs **Eingangsvorgang** empfangen wird, können Benutzer [die empfangenen Seriennummern registrieren oder bestätigen](https://docs.microsoft.com/dynamics365/commerce/pos-serialized-items).

- **Stapel-ID** – Die POS-Anwendung bietet begrenzte Unterstützung bei der Buchung von Kontoauszügen, wenn ein stapelgesteuerter Artikel verkauft wird. POS-Benutzer können jedoch nicht die Stapel-ID definieren, die bei Verwendung der POS-Anwendung verkauft oder kommissioniert wurde.

- **Bestandstatus** – Für Artikel, die den Lagerortverwaltungsprozess verwenden und einen Bestandsstatus benötigen, kann dieses Statusfeld nicht durch die POS-Anwendung festgelegt oder geändert werden. Der wie in der Filiallagerortkonfiguration definierte Standardbestandsstatus wird verwendet, wenn Artikel im Bestand entgegengenommen werden.

> [!NOTE]
> Alle Unternehmen müssen Artikelkonfigurationen über Commerce-Apps in Entwicklungs- oder Testumgebungen testen, bevor sie in Produktionsumgebungen eingesetzt werden können. Testen Sie Ihre Artikel, indem Sie sie verwenden, um regelmäßige Cash-and-Carry-Verkaufsbuchungen in POS durchzuführen, und erstellen Sie Debitorenaufträge (falls zutreffend) über POS, Callcenter oder E-Commerce, um zu überprüfen, ob sie vollständig unterstützt werden können. Sie sollten auch POS-Erfüllungs- und Inventarisierungsprozesse (z. B. Bestandserhalt und Auftragserfüllung) testen, bevor Sie neue Artikelkonfigurationen bereitstellen, um sicherzustellen, dass die POS-Anwendung diese unterstützen kann. Das Testen muss das Ausführen eines vollständigen Kontoauszugs-/Auftragsbuchungsprozesses in Ihrer Testumgebung und das Überprüfen, ob keine Buchungsprobleme auftreten, wenn Bestellungen für diese Artikel erstellt und in der Commerce-Zentrale gebucht werden, umfassen.
>
> Wenn Elemente auf eine Weise konfiguriert werden, die von den Commerce-Anwendungen nicht unterstützt wird, und keine entsprechenden Tests durchgeführt werden, können Datenfehler auftreten, die nicht einfach zu korrigieren sind oder möglicherweise überhaupt nicht korrigiert werden können.

## <a name="purchase-orders"></a>Bestellungen

Bestellungen werden in der Commerce-Zentrale erstellt. Wenn ein Filiallagerort im Bestellkopf oder in den Einkaufsbestellungspositionen enthalten ist, können die Positionen im Shop mithilfe des [Eingangsvorgangs](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) in POS empfangen werden. 

## <a name="transfer-orders"></a>Umlagerungsaufträge

Umlagerungsaufträge können in der Commerce-Zentrale oder über den [Eingangsvorgang](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)oder [Ausgehende Operation ](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) im POS erstellt werden. Verwenden Sie den POS-Vorgang **Eingangsvorgang** zum Erstellen einer Umlagerungsauftragsanforderung, um Bestand von einem anderen Lager oder Standort an den Shop senden zu lassen. Verwenden Sie den POS-Vorgang **Ausgangsvorgang** zum Erstellen einer Umlagerungsauftragsanforderung, um Bestand zu einem anderen Lager oder Standort vom Shop senden zu lassen. Nachdem ein Umlagerungsauftrag für ein Geschäft erstellt wurde, kann dieses Geschäft den Inventareingang für den Umlagerungsauftrag über **Eingangsvorgang** am POS verwalten. Wenn das Geschäft Bestand an einen anderen Ort versendet, wird der **Ausgangsvorgang** verwendet, um den ausgehenden Versandprozess dieses Geschäfts zu verwalten.

## <a name="stock-counts"></a>Bestandsmengen

Bestandsmengen können entweder geplant oder ungeplant sein. Geplante Bestandszählungen werden über die Commerce-Zentrale erstellt, indem eine Inventurerfassung erstellt wird, die mit dem Lager des Geschäfts verknüpft ist. Diese Erfassung gibt die Elemente an, die gezählt werden müssen. Das Geschäft kann dann auf diese vordefinierten Erfassungen zugreifen und diese mithilfe von **Bestandsmenge** am POS verwalten. Die Shopbenutzer initiieren eine außerplanmäßige Bestandszählung, wie sie bei Verwendung des POS-Vorgangs **Bestandszählung** erforderlich ist. Im Gegensatz zu geplanten Bestandsmengen haben ungeplante Bestandsmengen keine vordefinierte Liste mit Artikeln. Wenn eine Bestandsmenge eines beliebigen Typs in POS abgeschlossen wurde, wird sie kommissioniert und an die Zentrale gesendet. In der Zentrale muss die Zählung dann validiert und als separater Schritt in der Commerce-Zentrale veröffentlicht werden.

## <a name="inventory-lookup"></a>Bestandssuche

Die aktuell vorrätige Produktmenge für Mehrfachshops und Lagerorte kann auf der **Bestandssuchen**-Seite angezeigt werden. Neben der aktuellen verfügbaren Menge können auch künftige Verfügbarkeitszusagen-Mengen (ATP) für jede einzelne Filiale angezeigt werden. Wählen Sie die Filiale aus, für die die VfZ-Mengen angezeigt werden soll, und wählen Sie dann **Verfügbarkeit in Filiale anzeigen** aus. Informationen zu den verfügbaren Konfigurationsoptionen finden Sie unter [Berechnen der Bestandsverfügbarkeit für Einzelhandelskanäle ](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).


[!INCLUDE[footer-include](../includes/footer-banner.md)]