---
title: Synchronisieren von Verkaufsangebotskopfzeilen und -positionen von Sales mit Finance and Operations
description: "Das Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Verkaufsangebotskopfzeilen und -positionen von Microsoft Dynamics 365 for Sales mit Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, zu synchronisieren."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c8cfc484eed02423dbf0c7caaf8ac2337b6ac38d
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a>Synchronisieren von Verkaufsangebotskopfzeilen und -positionen von Sales mit Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Damit Sie die Prospect to Cash-Lösung verwenden können, müssen Sie mit [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration) vertraut sein. 

Das Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Verkaufsangebotskopfzeilen und -positionen von Microsoft Dynamics 365 for Sales (Sales) mit Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, (Finance and Operations) zu synchronisieren. 

## <a name="template-and-tasks"></a>Vorlage und Aufgaben

Die folgenden Vorlagen und die zugrunde liegenden Aufgaben werden verwendet, um Verkaufsangebotskopfzeilen und -positionen von Sales mit Finance and Operations zu synchronisieren:

- **Name der Vorlage:** Verkaufsangebote (Sales mit Finance and Operations)
- **Namen der Aufgaben im Projekt:**

    - QuoteHeader
    - QuoteLine

Die folgenden Synchronisierungsaufgaben sind erforderlich, bevor die Synchronisierung von Verkaufsangebotskopfzeilen und -positionen erfolgen kann:

- Produkte (Finance and Operations nach Sales)
- Konten (Sales nach Finance and Operations) (wenn verwendet)
- Kontakte nach Debitoren (Sales nach Finance and Operations) (wenn verwendet)

## <a name="entity-set"></a>Entitätssatz

| Vertrieb        | CDS           | Finance and Operations    |
|--------------|---------------|---------------------------|
| Angebote       | Angebot     | Verkaufsangebotskopfzeilen   |
| QuoteDetails | QuotationLine | CDS-Verkaufsangebotspositionen |

## <a name="entity-flow"></a>Entitätsfluss

Verkaufsangebote werden in Sales erstellt und mit Finance and Operations synchronisiert.

Verkaufsangebote aus Sales werden nur synchronisiert, wenn folgende Bedingungen erfüllt sind:

- Alle Produkte in den Verkaufsangebotspositionen werden extern verwaltet.
- Das Verkaufsangebot ist aktiv oder aktiviert.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to Cash-Lösung für Sales

Das Feld **Verfügt nur über extern verwaltete Produkte** ist der Entität „Angebot” hinzugefügt worden, um stets nachzuverfolgen, ob das Verkaufsangebot vollständig aus extern verwalteten Produkten besteht. Wenn ein Verkaufsangebot nur aus extern verwalteten Produkten besteht, werden die Produkte in Finance and Operations verwaltet. Mit diesem Verhalten wird sichergestellt, dass Sie nicht versuchen, Verkaufsangebotspositionen mit Produkten zu synchronisieren, die in Finance and Operations unbekannt sind.

Alle Produkte und Positionen im Angebot werden mit der Information **Verfügt nur über extern verwaltete Produkte** aus der Angebotskopfzeile aktualisiert. Diese Informationen können im Feld **Angebot hat nur extern verwaltete Produkte** in der Entität „Angebotsanforderungsposition” gefunden werden.

Die Felder **Rabatt**, **Belastungen** und **Steuer** werden durch komplizierte Einstellungen in Finance and Operations gesteuert. Diese Einstellungen unterstützen aktuell nicht die Integrationszuordnung. Im aktuellen Entwurf werden die Felder **Preis**, **Rabatt**, **Belastung** und **Steuer** von Finance and Operations gemastert und gehandhabt.

In Sales versieht die Lösung die folgenden Felder mit einem Schreibschutz, da die Werte nicht mit Finance and Operations synchronisiert werden:

- **Schreibgeschützte Felder in de Verkaufsangebotskopfzeile:** Rabatt %, Rabatt, Frachtgebühr
- **Schreibgeschützte Felder in Verkaufsangebotspositionen:** Steuer

## <a name="preconditions-and-mapping-setup"></a>Voraussetzungen und Einrichtung der Zuordnung

Vor dem Synchronisieren von Aufträgen müssen die Systeme mit den folgenden Einstellungen synchronisiert werden:

### <a name="setup-in-sales"></a>Einrichtung in Sales

- Wechseln Sie zu **Einstellungen** &gt; **Verwaltung** &gt; **Systemeinstellungen** &gt; **Vertrieb**, und stellen Sie sicher, dass das Feld **Rabattberechnungsmethode** auf **Pro Einheit** festgelegt ist. Diese Einstellung stellt sicher, dass der Positionsartikelrabatt von Sales mit der Einstellung in Finance and Operations übereinstimmt. Andernfalls ist der Rabatt in Finance and Operations nicht korrekt, da Finance and Operations den Rabatt als Rabatt pro Einheit liest, selbst wenn es ein Rabatt pro Position in Sales war.

### <a name="setup-in-finance-and-operations"></a>Einrichtung in Finance and Operations

- Wechseln Sie zu **Debitoren** &gt; **Einstellungen** &gt; **Debitorenparameter**. Auf der Registerkarte **Nummernkreis** wählen Sie den Nummernkreis für Verkaufsangebote aus, und klicken Sie dann auf **Details anzeigen**. Legen Sie dann unter **Allgemeine Einstellungen** das Feld **Manuell** auf **Ja** fest.
- Wechseln Sie zu **Debitoren** &gt; **Einstellungen** &gt; **Debitorenparameter**. Legen Sie anschließend auf der Registerkarte **Lieferungen** das Feld **Lieferdatumskontrolle** auf **Keine** fest. Diese Einstellung trägt dazu bei zu verhindern, dass die Synchronisierung für Verkaufsangebote fehlschlägt.

### <a name="setup-in-the-data-integration-project"></a>Einrichtung im Datenenintegrationsprojekt

#### <a name="quoteheader"></a>QuoteHeader

- Das Feld **Angefordertes Lieferdatum** ist in Finance and Operations erforderlich, und die Synchronisierung schlägt fehl, wenn das Feld leer bleibt. Um dieses Problem zu verhindern, wenn das Feld leer ist, wird ein Standarddatum von **Quelle &gt; CDS** übernommen. Das Datum sollte auf einen bevorzugten Wert aktualisiert werden. Gegenwärtig können Sie keinen Wert wie beispielsweise **Heute** eingeben, um das heutige Datum anzugeben. Sie müssen ein spezifisches Datum eingeben. Der Standardvorlagenwert für **Angefordertes Lieferdatum** ist **01.01.2020**.
- Das Feld **Adressland-Regionscode** ist in Finance and Operations erforderlich. Um Synchronisierungsfehler zu vermeiden, können Sie einen Standardwert angeben, der verwendet wird, wenn das Feld in Sales leer bleibt. Dieser Standardwert ist auch hilfreich, da Sie im Feld **Landregion** keinen Wert manuell für lokale Adressen eingeben müssen. Es gibt keinen Standardvorlagenwert für **DeliveryAddressCountryRegionISOCode**.
- Aktualisieren Sie die Zuordnung für **CDS Organisationskennung** in **Quelle &gt; CDS**, sodass sie **CD-Organisation** in der Organisationsentität entspricht:

    - Der Standardvorlagenwert für **Organization_OrganizationId** ist **ORG001**.
    - Der Standardvorlagenwert für **Account_Organization_OrganizationId** ist **ORG001**.
    - Der Standardvorlagenwert für **InvoiceAccount_OrganizationId** ist **ORG001**.

#### <a name="quoteline"></a>QuoteLine

- Aktualisieren Sie die Zuordnung für **CDS Organisationskennung** in **Quelle &gt; CDS**, sodass sie **CD-Organisation** in der Organisationsentität entspricht:

    - Der Standardvorlagenwert für **Organization_OrganizationId** ist **ORG001**.
    - Der Standardvorlagenwert für **Product_Organization_Organization_OrganizationId** ist **ORG001**.
    - Der Standardvorlagenwert für **Quotation_Organization_Organization_OrganizationId** ist **ORG001**.

- Das Feld **Angefordertes Lieferdatum** ist in Finance and Operations erforderlich, und die Synchronisierung schlägt fehl, wenn das Feld leer bleibt. Um dieses Problem zu verhindern, wenn das Feld leer ist, wird ein Standarddatum von **Quelle &gt; CDS** übernommen. Das Datum sollte auf einen bevorzugten Wert aktualisiert werden. Gegenwärtig können Sie keinen Wert wie beispielsweise **Heute** eingeben, um das heutige Datum anzugeben. Sie müssen ein spezifisches Datum eingeben. Der Standardvorlagenwert für **Angefordertes Lieferdatum** ist **01.01.2020**.
- Sie können die folgende Zuordnungen von **CDS &gt; Ziel** hinzufügen, um sicherzustellen, dass Angebotspositionen nach Finance and Operations importiert werden, wenn es weder Standardinformationen vom Debitoren noch vom Produkt gibt:

    - **SiteId** – Ein Standort ist erforderlich, um in Finance and Operations Angebots- und Vertriebsauftragspositionen zu erstellen. Es gibt keinen Standardvorlagenwert für **SiteId**.
    - **WarehouseId** – Ein Lager ist erforderlich, um in Finance and Operations Angebots- und Vertriebsauftragspositionen verarbeiten zu können. Es gibt keinen Standardvorlagenwert für **WarehouseId**.

- Vergewissern Sie sich, dass die erforderliche Wertzuordnung für die Verkaufsmaßeinheit (ME) in Finance and Operations in der Zuordnung **CDS &gt; Ziel** für **Mengenmaßeinheit** bis **VERKAUFSEINHEITSSYMBOL** vorhanden ist.

## <a name="template-mapping-in-data-integrator"></a>Vorlagenzuordnung im Datenintegrator

> [!NOTE]
> - Die Felder **Rabatt**, **Belastungen** und **Steuer** werden durch komplizierte Einstellungen in Finance and Operations gesteuert. Diese Einstellungen unterstützen aktuell nicht die Integrationszuordnung. Im aktuellen Entwurf werden die Felder **Preis**, **Rabatt**, **Belastung** und **Steuer** von Finance and Operations gehandhabt.
> - Die Felder **Zahlungsbedingungen**, **Frachtkonditionen**, **Lieferbedingungen**, **Liefermethode** und **Liefermodus** sind nicht Teil der Standardzuordnungen. Um diese Feldern zuzuordnen, müssen Sie eine Wertzuordnung einrichten, die spezifisch für die Daten in den Organisationen ist, zwischen denen die Entität synchronisiert wird.

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung im Datenintegrator.

### <a name="quoteheader"></a>QuoteHeader

![Vorlagenzuordnung im Datenintegrator](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Vorlagenzuordnung im Datenintegrator](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a>QuoteLine

![Vorlagenzuordnung im Datenintegrator](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Vorlagenzuordnung im Datenintegrator](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Verwandte Themen

[Synchronisierung von Produkten aus Finance and Operations für Produkte in Sales](products-template-mapping.md)

[Konten von Sales mit Debitoren in Finance and Operations synchronisieren](accounts-template-mapping.md)

[Synchronisierung von Kontakten aus Sales für Kontakte oder Kunden in Finance and Operations](contacts-template-mapping.md)



