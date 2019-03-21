---
title: Integration mit Microsoft Dynamics 365 for Field Service
description: Dieser Artikel enthält eine Übersicht über die Integration mit Microsoft Dynamics 365 for Field Service
author: ChristianRytt
manager: AnnBe
ms.date: 02/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: efda4e39f63155785386ecec6d21973e01a0f69f
ms.sourcegitcommit: 704d273485dcdc25c97a222bc0ef0695aad334d2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2019
ms.locfileid: "770892"
---
# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Integration mit Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations ermöglicht die Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Microsoft Dynamics 365 for Field Service. Die Integrationsszenarien werden mithilfe erweiterbarer Datenintegratorvorlagen und des Common Data Service (CDS) konfiguriert, um die Synchronisierung von Geschäftsprozessen zu ermöglichen.
Standardvorlagen können verwendet werden, um benutzerdefinierte Integrationsprojekte zu erstellen, in denen zusätzliche standardmäßige und benutzerdefinierte Felder sowie auch Entitäten zugeordnet werden können, um die Integration anzupassen und bestimmte Geschäftsanforderungen zu erfüllen. 

Die Field Service Integration erstellt die vorhandenen Interessent-zu-Bargeldfunktionen.

![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/field-service-integration.png)

Die erste Phase der Integration zwischen Field Service und Finance and Operations konzentriert sich darauf zu ermöglichen, dass Arbeitsaufträge und Vereinbarungen aus Field Service in Finance and Operations fakturiert werden. Die unterstützten Flüsse beginnen in Field Service, wo Informationen aus Arbeitsaufträgen mit Finance and Operations als Aufträge synchronisiert werden. In Finance and Operations werden die Aufträge fakturiert, um Rechnungsdokumente zu generieren. Darüber hinaus werden die Informationen aus Field Service-Vereinbarungsrechnungen mit Finance and Operations synchronisiert. Der Microsoft Dynamics 365-Datenenintegrator synchronisiert Daten mithilfe von anpassbaren Projekten. Standardvorlagen können verwendet werden, um benutzerdefinierte Integrationsprojekte zu erstellen, in denen zusätzliche standardmäßige und benutzerdefinierte Felder sowie auch Entitäten zugeordnet werden können, um die Integration anzupassen und bestimmte Anforderungen zu erfüllen.

Die erste Phase der Integration zwischen Field Service und Finance and Operations ermöglicht die Synchronisierung der folgenden Elemente:

- [Produkte in Finance and Operations mit Produkten in Field Service, die Produkttypinformationen enthalten](field-service-product.md)
- [Arbeitsaufträge in Field Service mit Aufträgen in Finance and Operations](field-service-work-order.md)
- [Rechnungen in Field Service mit Freitextrechnungen in Finance and Operations](field-service-invoice.md)

Um ein Beispiel zu sehen, wie Sie einen Arbeitsauftrag zwischen Field Service und Finance and Operations synchronisieren können, sehen Sie sich das kurze YouTube Video [Arbeitsaufträge zwischen Microsoft Dynamics 365 Integration ](https://www.youtube.com/watch?v=46ylO7raZAo) an.

## <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a>Integration mit Microsoft Dynamics 365 for Field Service (inkl. Bestand- und Projektinformationen)

Die zusätzlichen Funktionen in der zweiten Phase geben Feldtechnikern Einblicke über die Möglichkeit von Bestandinformationen aus Finance and Operations und ermöglichen es, Bestandebenen zu aktualisieren und Material zu übertragen. Zudem profitieren Unternehmen, die Verkaufswaren einrichten oder Instandhalten von besseren Kontrollen und besserer Sichtbarkeit zum vollständigen Vertriebs- und Servicevorgangs mit der Integration von Projekten.

### <a name="functionality-includes-integration-of"></a>Funktionen umfassen Integration aus:
- Lagerort-Information
- Verfügbare Bestandinformation
- Lagerumlagerungen
- Lagerbestandsregulierungen
- Mit Dynamics 365 for Field Service-Arbeitsaufträgen verbundene Dynamics 365 for Finance and Operations-Projekte
- Mit Dynamics 365 for Field Service-Arbeitsaufträge verbundene Dynamics 365 for Finance and Operations-Projekte übernehmen diese Projektnummer in den Dynamics 365 for Finance and Operations-Auftrag, um die Rechnungsstellung vom Projekt aus zu ermöglichen. 

![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a>Die zweitee Phase der Integration zwischen Field Service und Finance and Operations ermöglicht die Synchronisierung der folgenden Vorlagen:
- Lagerorte (Fin and Ops zu Field Service) - Lagerorte aus Finance and Operations zu Field Service [erweiterte Abfrage] 
- Produktbestand (Fin and Ops zu Field Service) - Bestandebeneinformation aus Finance and Operations zu Field Service [erweiterte Abfrage] 
- Bestandanpassung (Field SErvice zu Fin und Ops) - Bestandebeneinformation aus Field Service zu Finance and Operations [erweiterte Abfrage] 
- Bestandandübertrag (Field SErvice zu Fin und Ops) - Bestandübertrag aus Field Service zu Finance and Operations [erweiterte Abfrage] 
- Projekte (Fin and Ops zu Field Service) - Projektliste aus Finance and Operations zu Field Service [erweiterte Abfrage] 
- Arbeitsaufträge mit Projekt (Field Serivce zu Fin und Ops) - Arbeitsaufträge in Field Service zu Verkaufsaufträgen im Bereich Finance and Operations mit Unterstützung für Projekt [Erweiterte Abfrage] 
- Field Service Produkte mit Bestandeinheit (Fin und Ops zu Sales) - Finance and Operations 'zu verkaufende freigegebene Produkte zu Verkaufsprodukten' für Field Service einschließlich Lagereinheit 

## <a name="system-requirements"></a>Systemanforderungen

### <a name="system-requirements-for-finance-and-operations"></a>Systemanforderungen für Finance and Operations
Field Service-Integration unterstützt die folgenden Versionen:

- Dynamics 365 for Finance and Operations Version 8.1.2 (Dezember 2018) wurde im Dezember 2018 freigegeben und hat die Anwendungs-Build-Nummer 8.1.195 mit Plattform-Update 22 (7.0.5095). 

### <a name="system-requirements-for-field-service"></a>Systemanforderungen für Field Service
Um die Field Service-Integrationslösung zu nutzen, müssen Sie Folgendes installieren:

- Field Service for Dynamics 365 (Version 8.2.0.286) oder eine höhere Version auf Dynamics 365 9.1.x – veröffentlicht im November 2018
- Interessent zu Bargeld (P2C)-Lösung für Dynamics 365, Version 1.15.0.1 oder eine spätere Version. Die Lösung ist aus [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3) zum Download verfügbar.
- 'Field Service-Integration, Projekt- und Bestandlösung für Dynamics 365, Version 2.0.0.0 oder eine spätere Version. Die Lösung ist aus [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2) zum Download verfügbar.
