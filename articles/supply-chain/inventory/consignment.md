---
title: Sendung einrichten
description: In diesem Thema wird erläutert, wie eingehende Lieferungsbestandsprozesse verwendet werden.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentDraftReplenishmentOrderJournal, ConsignmentProductReceiptLines, ConsignmentReplenishmentOrder, ConsignmentVendorPortalOnHand, InventJournalOwnershipChange, InventOnHandItemListPage, PurchTable, PurchVendorPortalConfirmedOrders, DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 220834
ms.assetid: 3c9d6de4-45d4-459a-aef7-0d9ad2c22b3a
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 65c5702514a3bc9fe943959fd4ca032eb19bfe4c
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814443"
---
# <a name="set-up-consignment"></a>Sendung einrichten

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie eingehende Lieferungsbestandsprozesse verwendet werden.

Beim Lieferungsbestand handelt es sich um Bestand, der im Besitz eines Kreditors ist, der aber an Ihrem Standort gelagert ist. Wenn Sie bereit sind, den Bestand zu verbrauchen oder verwenden, übernehmen Sie den Besitz des Bestands. Dieses Thema enthält Informationen dazu, wie physisch Kreditor-eigener Lagerbestand empfangen wird, ohne Buchungen im Hauptbuch zu erstellen, wie ein Produktionsprozess beginnt, in dem der Kreditor-eigene Bestand physisch reserviert werden kann. und wie der Besitz des Rohmaterials ändert, um den Verbrauch als Teil des Produktionsauftragsverarbeitens zu verarbeiten. Es gibt auch einige Informationen dazu, wie Kreditoren den Verbrauch ihres Bestands mithilfe der Kreditoren-Zusammenarbeitschnittstelle überwachen können. 

## <a name="overview-of-the-consignment-process"></a>Überblick über den Lieferungsprozesses
In diesem Beispielszenario hat Unternehmen USMF eine Lieferungsvereinbarung mit Kreditor US-104 für das Rohmaterial M9211CI.

1.  Ein Lieferungswiederbeschaffungsauftrag wird manuell von einer Person bei USMF, basierend auf dem erwarteten Bedarf, erstellt. Der Auftrag wird für Kreditor US-104 erstellt und eine Position wird für Artikel MS9211CI hinzugefügt.
2.  Der Kreditor wird über die erwartete Lieferung informiert. Dies kann auf eine von drei Arten erfolgen:
    -   Jemand, der bei USMF arbeitet, sendet die Auftragsinformationen an den Kreditor.
    -   Der Kreditor kann den voraussichtlichen verfügbaren Lagerbestand mithilfe der Kreditoren-Zusammenarbeitschnittstelle überwachen.
    -   Jemand, der bei USMF arbeitet, filtert die Daten auf der Seite **Verfügbarer Lagerbestand**, sodass lediglich Datensätze für Kreditor US-104 angezeigt werden, bei denen der Empfangsstatus **Bestellt** ist, und er sendet dann diese Informationen zum Kreditor.
3.  Der Bestand wird von US-104 an USMF geliefert.
4.  Wenn das Material bei USMF ankommt, wird der Lieferungswiederbeschafftungs-Auftrag mit einem Produktzugang aktualisiert. Nur die physischen Mengen des Bestands, der im Besitz des Kreditors ist, werden erfasst. Es werden keine Hauptbuchtransaktionen erstellt, da der Bestand immer im Besitz des Kreditor ist.
5.  Der Kreditor überwacht Aktualisierungen des physische verfügbaren Lagerbestands mithilfe der Seite **Verfügbarer Lieferungsbestand**.
6.  Jetzt, da der physische Lagerbestand verfügbar ist, reserviert der Produktionsprozess den im Besitz des Kreditors befindlichen Bestand und beginnt den Produktionsauftrag für die fertigen Waren, die das Rohmaterial M9211CI verbrauchen werden.
7.  Der Besitzer der reservierter Rohmaterialien, die bei der heutigen Produktion verbraucht werden, wird von US-104 zu USMF geändert. Dies erfolgt mithilfe einer Bestandsbesitz-Änderungserfassung. Dieser Prozess erstellt Bestellungen, bei denen das Feld **Ursprung** auf **Lieferung** festgelegt ist.
8.  Der Kreditor überwacht den Verbrauch (Besitzänderung) auf der Seite **Vom Lieferungsbestand empfangene Produkte** und stellt auf Grundlage der Vereinbarungen zwischen den beiden Unternehmen eine Rechnung aus.
9.  Der Produktionsprozess verbraucht das Rohmaterial über eine Produktionskommissionierliste. Die physische Reservierung wird automatisch aktualisiert, um wiederzugeben, dass der verfügbare Lagerbestand im Besitz von USMF ist.
10. Die Rechnung von US-104 wird anhand der Bestellungen verarbeitet, die automatisch generiert wurden, als die Bestandsbesitz-Änderungserfassung verarbeitet wurde. Die Zahlung erfolgt an Kreditor US-104 für den Bestand, der verbraucht wurde.

USMF führt zusätzliche periodische Prozesse durch:

-   Die physische Bewegung des im Besitz des Kreditors befindlichen Bestands zwischen verschiedenen Lagerorten wird mithilfe einer Umlagerungserfassung verarbeitet.
-   Der physische verfügbare Lagerbestand wird mithilfe einer Erfassung**Artikelinventur**aktualisiert. Die Inventur kann auch vom Kreditor verwendet werden, um den verfügbaren Lagerbestand zu aktualisieren, sofern sie dafür über die notwendige Berechtigung verfügen.

Der Kreditor, US-104, kann die Aktualisierungen mithilfe der Seite **Verfügbarer Lieferungsbestand** überwachen.

## <a name="consignment-replenishment-orders"></a>Unterlieferungs-Wiederbeschaffungsaufträge
Ein Lieferungswiederbeschaffungsauftrag ist ein Dokument, das verwendet wird, um Bestandsmengen von Produkten anzufordern und nachzuverfolgen, die ein Kreditor innerhalb eines bestimmten Datumsintervalls zu liefern beabsichtigt, und zwar mithilfe des Erstellens bestellter Bestandstransaktionen. In der Regel basiert dies auf der Planung und dem tatsächlichen Bedarf der spezifischen Produkte. Der Bestand, der für den Lieferungswiederbeschaffungsauftrag eingeht, bleibt im Besitz des Kreditors. Nur der Besitz der Produkte, der mit der Aktualisierung des physischen Zugangs verknüpft ist, wird aufgezeichnet, und deshalb erfolgen keine Aktualisierungen der Hauptbuchtransaktion. 

Die Dimension **Besitzer** wird verwendet, um Informationen darüber zu trennen, welcher Bestand sich im Besitz des Kreditors und welcher sich im Besitz der empfangenden juristischen Person befindet. Lieferungswiederbeschaffungsauftragspositionen haben einen **Offenen Auftrag**-Status, sofern die gesamte Menge der Positionen nicht eingegangenen oder storniert wurde. Wenn die gesamte Menge eingegangenen oder abgebrochen wurde, wird der Status in **Abgeschlossen** geändert. Der physische verfügbare Lagerbestand, der einem Lieferungswiederbeschaffungsauftrag zugeordnet ist, kann mithilfe eines Anmeldeprozesses sowie eines Produktzugangsaktualisierungsprozesses erfasst werden. Die Registrierung kann als Teil des Artikeleingangsprozesses erfolgen oder durch die manuelle Aktualisierung der Auftragspositionen. Wenn der Produktzugangs-Aktualisierungsprozess verwendet wird, wird ein Beleg in der Produktzugangserfassung erstellt, der zur Bestätigung des Zugangs von Waren an die Kreditoren verwendet werden kann.

[![Unterlieferungs-Wiederbeschaffungsauftrag](./media/consignment-replenishment-order.png)](./media/consignment-replenishment-order.png)

## <a name="inventory-ownership-change-journal"></a>Erfassung für die Änderung von Bestandseigentümern
Der Prozess der Änderung des Besitzers des Bestands vom Kreditor zur empfangenden juristischen Person erfolgt mithilfe einer Bestandsbesitzänderungs-Erfassung. Es werden keine voraussichtlichen Lagerbuchungen für die Erfassung erstellt. Es werden nur Lagerbuchungen erstellt, die einer gebuchten Erfassung zugeordnet sind. Wenn die Erfassung gebucht wird:

-   Der im Besitz des Kreditors befindliche Bestand wird mithilfe einer Referenz **Besitzänderung** mit dem Status **Verkauft**ausgegeben.
-   Der verfügbare Lagerbestand wird von der juristischen Person empfangen, die ihn verbraucht. Dies erfolgt mithilfe einer durch den Produktzugang aktualisierten Bestandsbuchung zur Bestellung. Dadurch wird der Status des Auftrags auf **Eingegangen** festgelegt. Bei Bestellungen, die zur Lieferung verwendet werden, wird das Feld **Ursprung** auf **Lieferung** festgelegt.

Es ist nicht möglich, die Menge auf Lieferungsbestellpositionen zu aktualisieren, nachdem der Auftrag erstellt wurde.

[![Bestandeigentümer-Änderungserfassung](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Kreditorenzusammenarbeit in den Lieferungsprozessen
Die Kreditorenzusammenarbeitschnittstelle hat drei Seiten, die dem Prozess der eingehenden Lieferung zugeordnet sind:

-   **Bestellungen,**, **die Lieferungsbestand verbrauchen**  – Zeigt detaillierte Bestellungsinformationen zur Besitzänderung vom Lieferungsprozess an.
-   **Produkte, die aus dem Lieferungsbestand empfangen werden** – Zeigt Informationen zu Artikeln und Mengen an, bei denen die Produktzugänge während des Besitzänderungsprozesses aktualisiert werden.
-   **Verfügbarer Lieferungsbestand** – Zeigt Informationen zu den Lieferungsartikeln an, die sie erwartungsgemäß liefern sollen, sowie zu den Artikeln, die am Debitorenstandort bereits physisch verfügbar sind.

## <a name="inventory-owners"></a>Bestandsbesitzer
Um physischen, eingehenden Lieferungsbestand zu erfassen, müssen Sie einen Kreditoreneigentümer definieren. Dies erfolgt auf der Seite **Bestandseigentümer**. Wenn Sie ein **Kreditorenkonto** auswählen, generiert dies Standardwerte für die Felder **Name** und **Besitzer**. Der Wert im Feld **Besitzer** wird für den Kreditor angezeigt, somit möchten Sie ihn möglicherweise ändern, wenn die Namen Ihres Kreditorenkontos von externen Personen nicht einfach erkannt werden können. Es ist möglich, das Feld **Besitzer** zu bearbeiten. Dies gilt jedoch nur bis zu dem Zeiptunkt, an dem Sie den Datensatz **Bestandsbesitzer** speichern. Das Feld **Name** wird mit dem Namen der Partei aufgefüllt, dem das Kreditorenkonto zugeordnet ist, und dieser kann nicht geändert werden.

[![Bestandsbesitzer](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>Rückverfolgungsgruppe
Artikel, die bei Lieferungsprozessen verwendet werden, müssen einer **Rückverfolgungsangabengruppe** zugeordnet werden, wobei die Dimension **Besitzer** auf **Aktiv** festgelegt ist. Bei der „Besitzerdimension” sind die Optionen **Physischer Bestand** und **Wertmäßiger Bestand** immer aktiviert. Die Option **Disposition nach Dimensionen** ist nie aktiviert.

[![Rückverfolgungsangabengruppe](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)

## <a name="inventory-ownership-change-journal"></a>Erfassung für die Änderung von Bestandseigentümern
Die Erfassung **Bestandsbesitzänderung**wird verwendet, um die Übertragung des Besitzes des Lieferungsbestands vom Kreditor zur juristischen Person, die ihn verbraucht, aufzuzeichnen. Wie jede Bestandserfassung muss sie mit einem Bestandserfassungsname identifiziert werden. Diese Namen werden auf der Seite **Bestandserfassungsnamen** erstellt, und der **Erfassungstyp** muss auf **Besitzänderung** festgelegt werden.

[![Bestandeigentümer-Änderungserfassung](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Kreditorenzusammenarbeit in den Lieferungsprozessen
Wenn Ihre Kreditoren die Kreditorenzusammenarbeitschnittstelle verwenden, können sie diese verwenden, um den Verbrauch des Bestands an Ihrem Standort zu überwachen. Weitere Informationen zur Einrichtung von Kreditoren zur Verwendung der Kreditorenzusammenarbeit finden Sie unter [Benutzersicherheit für Kreditorenportal](../procurement/configure-security-vendor-portal-users.md)





