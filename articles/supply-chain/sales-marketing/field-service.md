---
title: Übersicht über die Integration mit Microsoft Dynamics 365 Field Service
description: Dieser Artikel enthält eine Übersicht über die Integration mit Microsoft Dynamics 365 Field Service.
author: Henrikan
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 12a9c57e2587150914c6087c041d63af9783c1f3
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103696"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a>Übersicht über die Integration mit Microsoft Dynamics 365 Field Service

[!include[banner](../includes/banner.md)]



Supply Chain Management ermöglicht die Synchronisierung von Geschäftsprozessen zwischen Dynamics 365 Supply Chain Management und Dynamics 365 Field Service. Die Integrationsszenarien werden mithilfe erweiterbarer Datenintegratorvorlagen und Microsoft Dataverse konfiguriert, um die Synchronisierung von Geschäftsprozessen zu ermöglichen.
Standardvorlagen können verwendet werden, um benutzerdefinierte Integrationsprojekte zu erstellen, in denen zusätzliche standardmäßige und benutzerdefinierte Spalten sowie auch Tabellen zugeordnet werden können, um die Integration anzupassen und bestimmte Geschäftsanforderungen zu erfüllen. 

Die Field Service Integration erstellt die vorhandenen Interessent-zu-Bargeldfunktionen.

![Synchronisierung von Geschäftsprozessen zwischen Supply Chain Management und Field Service.](./media/field-service-integration.png)

Die erste Phase der Integration zwischen Field Service und Supply Chain Management konzentriert sich darauf zu ermöglichen, dass Arbeitsaufträge und Vereinbarungen aus Field Service in Supply Chain Management fakturiert werden. Die unterstützten Flüsse beginnen in Field Service, wo Informationen aus Arbeitsaufträgen mit Supply Chain Management als Aufträge synchronisiert werden. In Supply Chain Management werden die Aufträge als Rechnungsdokumente generiert. Darüber hinaus werden die Informationen aus Field Service-Vereinbarungsrechnungen mit Supply Chain Management synchronisiert. Der Microsoft Dynamics 365-Datenenintegrator synchronisiert Daten mithilfe von anpassbaren Projekten. Standardvorlagen können verwendet werden, um benutzerdefinierte Integrationsprojekte zu erstellen, in denen zusätzliche standardmäßige und benutzerdefinierte Spalten sowie auch Tabellen zugeordnet werden können, um die Integration anzupassen und bestimmte Anforderungen zu erfüllen.

Die erste Phase der Integration zwischen Field Service und Supply Chain Management ermöglicht die Synchronisierung der folgenden Elemente:

- [Produkte von Supply Chain Management mit Produkten in Field Service synchronisieren](field-service-product.md)
- [Arbeitsaufträge in Field Service mit Aufträgen in Supply Chain Management synchronisieren](field-service-work-order.md)
- [Vereinbarungsrechnungen in Field Service mit Freitextrechnungen in Supply Chain Management synchronisieren](field-service-invoice.md)

Um ein Beispiel zu sehen, wie Sie einen Arbeitsauftrag zwischen Field Service und Supply Chain Management synchronisieren können, sehen Sie sich das kurze YouTube Video [Arbeitsaufträge zwischen Microsoft Dynamics 365 Integration](https://www.youtube.com/watch?v=46ylO7raZAo) an.

## <a name="integration-with-field-service-including-inventory-and-project-information"></a>Integration mit Field Service (inkl. Bestand- und Projektinformationen)

Die zusätzlichen Funktionen in der zweiten Phase geben Feldtechnikern Einblicke über die Möglichkeit von Bestandinformationen aus Supply Chain Management und ermöglichen es, Bestandebenen zu aktualisieren und Material zu übertragen. Zudem profitieren Unternehmen, die Verkaufswaren einrichten oder Instandhalten von besseren Kontrollen und besserer Sichtbarkeit zum vollständigen Vertriebs- und Servicevorgangs mit der Integration von Projekten.

### <a name="functionality-includes-integration-of"></a>Funktionen umfassen Integration aus:
- Lagerort-Information
- Verfügbare Bestandinformation
- Lagerumlagerungen
- Lagerbestandsregulierungen
- Supply Chain Management-Projekte verbunden mit Dynamics 365 Field Service-Arbeitsaufträgen
- Mit Dynamics 365 Field Service-Arbeitsaufträge verbundene Supply Chain Management-Projekte übernehmen diese Projektnummer in den -Auftrag, um die Rechnungsstellung vom Projekt aus zu ermöglichen. 

![Synchronisation von Geschäftsprozessen zwischen Supply Chain Management und Field Service, einschließlich Bestands- und Projektinformationen.](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a>Die zweitee Phase der Integration zwischen Field Service und Supply Chain Management ermöglicht die Synchronisierung der folgenden Vorlagen:
- Lagerorte (Supply Chain Management zu Field Service) - Lagerorte aus Supply Chain Management zu Field Service [Erweiterte Abfrage] 
- Produktbestand (Supply Chain Management zu Field Service) - Bestandebeneninformationen aus Supply Chain Management zu Field Service [Erweiterte Abfrage] 
- Bestandanpassung (Field Service zu Supply Chain Management) - Bestandanpassungen von Field Service zu Supply Chain Management [Erweiterte Abfrage] 
- Bestandsumbuchungen (Field Service zu Supply Chain Management) - Bestandsübertragungen von Field Service zu Supply Chain Management [Erweiterte Abfrage] 
- Projekte (Supply Chain Management zu Field Service) - Projektliste aus Supply Chain Management zu Field Service 
- Arbeitsaufträge mit Projekt (Field Serivce zu Supply Chain Management) - Arbeitsaufträge in Field Service zu Verkaufsaufträgen im Bereich Supply Chain Management mit Unterstützung für Projekt [Erweiterte Abfrage] 
- Field Service Produkte mit Bestandeinheit (Supply Chain Management zu Sales) - Supply Chain Management 'zu verkaufende freigegebene Produkte zu Verkaufsprodukten' für Field Service einschließlich Lagereinheit 

## <a name="system-requirements"></a>Systemanforderungen

### <a name="system-requirements-for-supply-chain-management"></a>Systemanforderungen für Supply Chain Management
Field Service-Integration unterstützt die folgenden Versionen:

- Dynamics 365 Finance and Operations Version 8.1.2 (Dezember 2018) wurde im Dezember 2018 veröffentlicht und hat eine Anwendungs-Build-Nummer 8.1.195 mit Plattform-Update 22 (7.0.5095). 

### <a name="system-requirements-for-field-service"></a>Systemanforderungen für Field Service
Um die Field Service-Integrationslösung zu nutzen, müssen Sie Folgendes installieren:

- Field Service (Version 8.2.0.286) oder eine höhere Version auf Dynamics 365 9.1.x – veröffentlicht im November 2018
- Interessent zu Bargeld (P2C)-Lösung für Dynamics 365, Version 1.15.0.1 oder eine spätere Version. Die Lösung ist aus [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3) zum Download verfügbar.
- 'Field Service-Integration, Projekt- und Bestandlösung für Dynamics 365, Version 2.0.0.0 oder eine spätere Version. Die Lösung ist aus [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2) zum Download verfügbar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
