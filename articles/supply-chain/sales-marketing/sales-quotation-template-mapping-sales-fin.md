---
title: Angebotskopfzeilen und -positionen direkt von Sales zu Finance and Operations synchronisieren
description: "Das Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Verkaufsangebotskopfzeilen und -positionen direkt von Microsoft Dynamics 365 for Sales mit Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, zu synchronisieren."
author: ChristianRytt
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: 8a75c6dd91020ab3e676e2bb40d5c822731e244f
ms.contentlocale: de-de
ms.lasthandoff: 11/14/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a>Angebotskopfzeilen und -positionen direkt von Sales zu Finance and Operations synchronisieren

[!include[banner](../includes/banner.md)]

Das Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Verkaufsangebotskopfzeilen und -positionen direkt von Microsoft Dynamics 365 for Sales mit Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, zu synchronisieren.

> [!NOTE]
> Damit Sie die Prospect to Cash-Lösung verwenden können, müssen Sie mit [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration) vertraut sein.

## <a name="template-and-tasks"></a>Vorlage und Aufgaben

Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Verkaufsangebotskopfzeilen und -positionen direkt von Sales mit Finance and Operations zu synchronisieren:

- **Name der Vorlage in der Datenintegration:** Verkaufsangebote (Sales zu Finance and Operations) - direkt
- **Namen der Aufgaben im Datenintegrationsprojekt:**

    - QuoteHeader
    - QuoteLine

Die folgenden Synchronisierungsaufgaben sind erforderlich, bevor die Synchronisierung von Verkaufsangebotskopfzeilen und -positionen erfolgen kann:

- Produkte (Finance and Operations nach Sales) - Direkt
- Konten (Sales nach Finance and Operations) - Direkt (wenn verwendet)
- Kontakte nach Debitoren (Sales nach Finance and Operations) - Direkt (wenn verwendet)

## <a name="entity-set"></a>Entitätssatz

| Vertrieb        | Finance and Operations     |
|--------------|----------------------------|
| Angebote       | CDS-Verkaufsangebotskopf |
| QuoteDetails | CDS-Verkaufsangebotspositionen  |

## <a name="entity-flow"></a>Entitätsfluss

Verkaufsangebote werden in Sales erstellt und mit Finance and Operations synchronisiert.

Verkaufsangebote aus Sales werden nur synchronisiert, wenn folgende Bedingungen erfüllt sind:

- Alle Angebote in den Verkaufsangebotspositionen werden extern verwaltet.
- Nachdem Sie **Angebot aktivieren** geklickt haben, ist das Verkaufsangebot aktiv.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to Cash-Lösung für Sales

Das Feld **Verfügt nur über extern verwaltete Produkte** ist der Entität **Angebot** hinzugefügt worden, um stets nachzuverfolgen, ob das Verkaufsangebot vollständig aus extern verwalteten Produkten besteht. Wenn ein Verkaufsangebot nur aus extern verwalteten Produkten besteht, werden die Produkte in Finance and Operations verwaltet. Mit diesem Verhalten wird sichergestellt, dass Sie nicht versuchen, Verkaufsangebotspositionen mit Produkten zu synchronisieren, die in Finance and Operations unbekannt sind.

Alle Angebotsprodukte im Vertriebsangebot werden mit der Information **Verfügt nur über extern verwaltete Produkte** aus der Vertriebsangebotskopfzeile aktualisiert. Diese Informationen können im Feld **Angebot hat nur extern verwaltete Produkte** in der Entität **QuoteDetails** gefunden werden.

Ein Rabatt kann zum Angebotsprodukt hinzugefügt werden wird anschließend mit Finance and Operations synchronisiert. Die Felder **Rabatt**, **Belastungen** und **Steuer** in der Kopfzeile werden durch komplizierte Einstellungen in Finance and Operations gesteuert. Diese Einstellungen unterstützen aktuell nicht die Integrationszuordnung. Im aktuellen Entwurf werden die Felder **Preis**, **Rabatt**, **Belastung** und **Steuer** in Finance and Operations verwaltet und gehandhabt.

In Sales versieht die Lösung die folgenden Felder mit einem Schreibschutz, da die Werte nicht mit Finance and Operations synchronisiert werden:

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

- Stellen Sie sicher, dass die erforderliche Wertzuordnung für **SalesUnitSymbol** in Finance and Operations vorhanden ist.
- Überprüfen Sie, dass die obligatorischen Einheiten in Sales definiert sind.

    Ein Vorlagenwert, eine der Wertzuordnung ist, wird für **oumid.name** auf **SalesUnitSymbol** festgelegt.

- Optional: Sie können die folgende Zuordnungen hinzufügen, um sicherzustellen, dass Verkaufsangebotspositionen nach Finance and Operations importiert werden, wenn es weder Standardinformationen vom Debitoren noch vom Produkt gibt:

    - **SiteId** – Ein Standort ist erforderlich, um in Finance and Operations Angebots- und Vertriebsauftragspositionen zu erstellen. Es gibt keinen Standardvorlagenwert für **SiteId**.
    - **WarehouseId** – Ein Lager ist erforderlich, um in Finance and Operations Angebots- und Vertriebsauftragspositionen verarbeiten zu können. Es gibt keinen Standardvorlagenwert für **WarehouseId**.

## <a name="template-mapping-in-data-integrator"></a>Vorlagenzuordnung im Datenintegrator

> [!NOTE]
> - Die Felder **Rabatt**, **Belastungen** und **Steuer** werden durch komplizierte Einstellungen in Finance and Operations gesteuert. Diese Einstellungen unterstützen aktuell nicht die Integrationszuordnung. Im aktuellen Entwurf werden die Felder **Preis**, **Rabatt**, **Belastung** und **Steuer** von Finance and Operations gehandhabt.
> - Die Felder **Zahlungsbedingungen**, **Frachtkonditionen**, **Lieferbedingungen**, **Liefermethode** und **Liefermodus** sind nicht Teil der Standardzuordnungen. Um diese Feldern zuzuordnen, müssen Sie eine Wertzuordnung einrichten, die spezifisch für die Daten in den Organisationen ist, zwischen denen die Entität synchronisiert wird.

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung im Datenintegrator.

### <a name="quoteheader"></a>QuoteHeader

![Vorlagenzuordnung im Datenintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![Vorlagenzuordnung im Datenintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Verwandte Themen

[Interessent zu Bargeld](prospect-to-cash.md)


