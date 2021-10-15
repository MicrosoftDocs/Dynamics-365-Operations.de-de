---
title: Verkaufsangebotskopfzeilen und ‑positionen direkt von Sales zu Supply Chain Management synchronisieren
description: Das Thema erklärt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Verkaufsangebotskopfzeilen und -positionen direkt aus Dynamics 365 Sales mit Dynamics 365 Supply Chain Management zu synchronisieren.
author: Henrikan
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 46584f397e83bc68878ff5ef2848a251912811af
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566406"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a>Verkaufsangebotskopfzeilen und ‑positionen direkt von Sales zu Supply Chain Management synchronisieren

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Das Thema erklärt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Verkaufsangebotskopfzeilen und -positionen direkt aus Dynamics 365 Sales mit Dynamics 365 Supply Chain Management zu synchronisieren.

> [!NOTE]
> Damit Sie die Prospect to Cash-Lösung verwenden können, müssen Sie mit [Integration von Daten in Microsoft Dataverse for Apps](/powerapps/administrator/data-integrator) vertraut sein.

## <a name="data-flow-in-prospect-to-cash"></a>Datenfluss in Interessent nach Bargeld

Die Lösung Interessent nach Bargeld verwendet die Datenenintegrationsfunktion, um Daten über Instanzen von Supply Chain Management und Sales hinweg zu synchronisieren. Die „Interessent zu Bargeld“-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen zwischen Supply Chain Management und Sales. Die folgende Abbildung zeigt, wie Daten zwischen Supply Chain Management und Sales synchronisiert werden.

[![Datenfluss in Interessent nach Bargeld.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="template-and-tasks"></a>Vorlage und Aufgaben

Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Verkaufsangebotskopfzeilen und -positionen direkt von Sales mit Supply Chain Management zu synchronisieren:

- **Name der Vorlage in der Datenintegration:** Verkaufsangebote (Sales zu Supply Chain Management) - Direkt
- **Namen der Aufgaben im Datenintegrationsprojekt:**

    - QuoteHeader
    - QuoteLine

Die folgenden Synchronisierungsaufgaben sind erforderlich, bevor die Synchronisierung von Verkaufsangebotskopfzeilen und -positionen erfolgen kann:

- Produkte (Supply Chain Management zu Sales) – Direkt
- Konten (Sales zu Supply Chain Management) – Direkt (falls verwendet)
- Kontakte zu Kunden (Sales zu Supply Chain Management) – Direkt (falls verwendet)

## <a name="entity-set"></a>Entitätssatz

| Verk.        | Lieferkettenverwaltung     |
|--------------|----------------------------|
| Angebote       | Dataverse-Verkaufsangebotskopf |
| QuoteDetails | Dataverse-Verkaufsangebotspositionen  |

## <a name="entity-flow"></a>Entitätsfluss

Verkaufsangebote werden in Sales erstellt und mit Supply Chain Management synchronisiert.

Verkaufsangebote aus Sales werden nur synchronisiert, wenn folgende Bedingungen erfüllt sind:

- Alle Angebote in den Verkaufsangebotspositionen werden extern verwaltet.
- Nachdem Sie **Angebot aktivieren** geklickt haben, ist das Verkaufsangebot aktiv.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to Cash-Lösung für Sales

Das Feld **Verfügt nur über extern verwaltete Produkte** ist der Entität **Angebot** hinzugefügt worden, um stets nachzuverfolgen, ob das Verkaufsangebot vollständig aus extern verwalteten Produkten besteht. Wenn ein Verkaufsangebot nur aus extern verwalteten Produkten besteht, werden die Produkte in Supply Chain Management verwaltet. Mit diesem Verhalten wird sichergestellt, dass Sie nicht versuchen, Verkaufsangebotspositionen mit Produkten zu synchronisieren, die in Supply Chain Management unbekannt sind.

Alle Angebotsprodukte im Vertriebsangebot werden mit der Information **Verfügt nur über extern verwaltete Produkte** aus der Vertriebsangebotskopfzeile aktualisiert. Diese Informationen können im Feld **Angebot hat nur extern verwaltete Produkte** in der Entität **QuoteDetails** gefunden werden.

Ein Rabatt kann zum Angebotsprodukt hinzugefügt werden wird anschließend mit Supply Chain Management synchronisiert. Die Felder **Rabatt**, **Belastungen** und **Steuer** in der Kopfzeile werden durch komplizierte Einstellungen in Supply Chain Management gesteuert. Diese Einstellungen unterstützen aktuell nicht die Integrationszuordnung. Im aktuellen Entwurf werden die Felder **Preis**, **Rabatt**, **Belastung** und **Steuer** in Supply Chain Management verwaltet und gehandhabt.

In Sales versieht die Lösung die folgenden Felder mit einem Schreibschutz, da die Werte nicht mit Supply Chain Management synchronisiert werden:

- Schreibgeschützte Felder in de Verkaufsangebotskopfzeile: **Rabatt %**, **Rabatt** und **Frachtbetrag**
- Schreibgeschützte Felder auf Angebotsprodukten: **Steuer**

## <a name="preconditions-and-mapping-setup"></a>Voraussetzungen und Einrichtung der Zuordnung

Vor dem Synchronisieren von Verkaufsangeboten müssen die Systeme mit den folgenden Einstellungen synchronisiert werden:

### <a name="setup-in-sales"></a>Einrichtung in Sales

- Stellen Sie sicher, dass Berechtigungen für das Team, zu dem der Benutzer (aus Ihren Verbindungseinstellungen in Sales) zugewiesen ist, vorhanden sind. Werden Demodaten verwendet, hat in der Regel der Benutzer einen Administratorzugriff aber nicht das Team. Wenn dieses Team nicht Administratorzugriff hat, wenn Sie das Projekt vom Datenintegrator ausführen, erhalten Sie eine Fehlermeldung, die angibt, dass das Hauptteam fehlt.

    Wenn Sie Berechtigungen für das Team einrichten, gehen Sie &gt; zu **Einstellungen** **Sicherheit** &gt; **Teams**, und wählen Sie das zutreffende Team aus. Wählen Sie **Verwalten Sie Rollen** und dann eine Rolle, die die erforderlichen Berechtigungen verfügt, beispielsweise **Systemadministrator**.

- Gehen Sie zu &gt; Sie **Einstellungen** **Verwaltung** &gt; **Systemeinstellungen** &gt; **Sales** zu öffnen, und überprüfen Sie, ob die folgenden Einstellungen verwendet werden:

    - Die Option **Systempreisberechnungssystem verwenden** wird auf **Ja** festgelegt.
    - Das Feld **Rabattberechnungsmethode** wird auf **Positionsartikel** festgelegt.

### <a name="setup-in-the-data-integration-project"></a>Einrichtung im Datenenintegrationsprojekt

#### <a name="quoteheader"></a>QuoteHeader

- Vergewissern Sie sich, dass die erforderliche Zuordnung für **Shipto\_Land** zu **DeliveryAddressCountryRegionISOCode** vorhanden ist. In der Wertzuordnungen können Sie einen Standardwert definieren, der verwendet wird, wenn der Wert nicht aktiviert wird. Lassen Sie einfach die linken Seite leer, und legen die rechte Seite auf das gewünschte Land oder die Region fest. Auf diese Weise müssen Sie das Land oder die Region für Zahlungen nationaler Aufträge nicht eingeben.

    Der Vorlagenwert ist eine Wertzuordnung, in der verschiedene Länder/Regionen zugeordnet sind, und wo ein leerer Wert dem Wert **USA** entspricht.

#### <a name="quoteline"></a>QuoteLine

- Stellen Sie sicher, dass die erforderliche Wertzuordnung für **SalesUnitSymbol** in Supply Chain Management vorhanden ist.
- Überprüfen Sie, dass die obligatorischen Einheiten in Sales definiert sind.

    Ein Vorlagenwert, eine der Wertzuordnung ist, wird für **oumid.name** auf **SalesUnitSymbol** festgelegt.

- Optional: Sie können die folgende Zuordnungen hinzufügen, um sicherzustellen, dass Verkaufsangebotspositionen nach Supply Chain Management importiert werden, wenn es weder Standardinformationen vom Debitoren noch vom Produkt gibt:

    - **SiteId** – Ein Standort ist erforderlich, um in Supply Chain Management Angebots- und Vertriebsauftragspositionen zu erstellen. Es gibt keinen Standardvorlagenwert für **SiteId**.
    - **WarehouseId** – Ein Lager ist erforderlich, um in Supply Chain Management Angebots- und Vertriebsauftragspositionen verarbeiten zu können. Es gibt keinen Standardvorlagenwert für **WarehouseId**.

## <a name="template-mapping-in-data-integrator"></a>Vorlagenzuordnung im Datenintegrator

> [!NOTE]
> - Die Felder **Rabatt**, **Belastungen** und **Steuer** werden durch komplizierte Einstellungen in Supply Chain Management gesteuert. Diese Einstellungen unterstützen aktuell nicht die Integrationszuordnung. Im aktuellen Entwurf werden die Felder **Preis**, **Rabatt**, **Belastung** und **Steuer** von Supply Chain Management gehandhabt.
> - Die Felder **Zahlungsbedingungen**, **Frachtkonditionen**, **Lieferbedingungen**, **Liefermethode** und **Liefermodus** sind nicht Teil der Standardzuordnungen. Um diese Feldern zuzuordnen, müssen Sie eine Wertzuordnung einrichten, die spezifisch für die Daten in den Organisationen ist, zwischen denen die Entität synchronisiert wird.

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung im Datenintegrator.

### <a name="quoteheader"></a>QuoteHeader

![Vorlagenzuordnung im Datenintegrator, QuoteHeader.](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![Vorlagenzuordnung im Datenintegrator, QuoteLine.](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Verwandte Themen

[Prospect-to-Cash](prospect-to-cash.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]