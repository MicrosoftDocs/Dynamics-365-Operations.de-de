---
title: Integration mit Microsoft Dynamics 365 for Field Service
description: "Dieses Thema bietet einen Überblick über die Integration mit Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a57e23691a6b4d48c6b8dd6d1f61fc9730365b39
ms.openlocfilehash: 0c1268d2fddcf7b28ecfc3197f21e9d30a5a5855
ms.contentlocale: de-de
ms.lasthandoff: 05/31/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Integration mit Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations ermöglicht die Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Microsoft Dynamics 365 for Field Service. Die Integrationsszenarien werden mithilfe erweiterbarer Datenintegratorvorlagen und des Common Data Service (CDS) konfiguriert, um die Synchronisierung von Geschäftsprozessen zu ermöglichen.

[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)

Die erste Phase der Integration zwischen Field Service und Finance and Operations konzentriert sich darauf zu ermöglichen, dass Arbeitsaufträge und Vereinbarungen aus Field Service in Finance and Operations fakturiert werden. Die unterstützten Flüsse beginnen in Field Service, wo Informationen aus Arbeitsaufträgen mit Finance and Operations als Aufträge synchronisiert werden. In Finance and Operations werden die Aufträge fakturiert, um Rechnungsdokumente zu generieren. Darüber hinaus werden die Informationen aus Field Service-Vereinbarungsrechnungen mit Finance and Operations synchronisiert. Der Microsoft Dynamics 365-Datenenintegrator synchronisiert Daten mithilfe von anpassbaren Projekten. Standardvorlagen können verwendet werden, um benutzerdefinierte Integrationsprojekte zu erstellen, in denen zusätzliche standardmäßige und benutzerdefinierte Felder sowie auch Entitäten zugeordnet werden können, um die Integration anzupassen und bestimmte Anforderungen zu erfüllen.

Die erste Phase der Integration zwischen Field Service und Finance and Operations ermöglicht die Synchronisierung der folgenden Elemente:

- [Produkte in Finance and Operations mit Produkten in Field Service, die Produkttypinformationen enthalten](field-service-product.md)
- [Arbeitsaufträge in Field Service mit Aufträgen in Finance and Operations](field-service-work-order.md)
- [Rechnungen in Field Service mit Freitextrechnungen in Finance and Operations](field-service-invoice.md)

Um ein Beispiel zu sehen, wie Sie einen Arbeitsauftrag zwischen Field Service und Finance and Operations synchronisieren können, sehen Sie sich das kurze YouTube-Video [Arbeitsaufträge zwischen Dynamics 365 for Field Service und Finance and Operations synchronisieren](https://www.youtube.com/watch?v=hAB4TDVMjxU) an.

## <a name="system-requirements-for-finance-and-operations"></a>Systemanforderungen für Finance and Operations
Field Service-Integration unterstützt die folgenden Versionen:

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations Version 8.0 (April 2018) oder höher

- Dynamics 365 for Finance and Operations Version 8.0 (April 2018) wurde im April 2018 veröffentlicht und hat die Anwendungserstellungsnummer 8.0.30.8020 mit Plattformupdate 15 (7.0.4841.35234). 

## <a name="system-requirements-for-field-service"></a>Systemanforderungen für Field Service
Um die Field Service-Integrationslösung zu nutzen, müssen Sie Folgendes installieren:

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 for Field Service 9.0 oder höher

- Dynamics 365 for Field Service Version 1612 (9.0.1.733) (DB 9.0.1.733) online oder eine spätere Version.
- Interessent zu Bargeld (P2C)-Lösung für Dynamics 365, Version 1.15.0.1 oder eine spätere Version. Die Lösung ist unter [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3) zum Download verfügbar.
- Field Service-Integrationslösung für Dynamics 365, Version 1.0.0.0 oder eine spätere Version. Die Lösung ist unter [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration) zum Download verfügbar.

