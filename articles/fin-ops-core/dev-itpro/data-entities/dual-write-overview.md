---
title: Datenintegration nahezu in Echtzeit mit Common Data Service
description: In diesem Thema wird eine Übersicht über die Integration zwischen Finance and Operations und Common Data Service aufgeführt.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 11a5792c9c039eb76337309ef2fdb2b994ce191a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772386"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a>Datenintegration nahezu in Echtzeit mit Common Data Service

[!include [banner](../includes/banner.md)]

In der derzeitigen digitalen Welt verwenden Geschäftsökosysteme die Microsoft Dynamics 365-Anwendungen als Ganzes. Da die Daten von Personen, Kunden, Arbeitsgängen und IoT-Geräten (Internet of Things) in eine Quelle fließen, gibt es eine Möglichkeit für digitale Rückmeldungsschleifen. Um dies zu erreichen, ist die Integration zwischen Finance and Operations-Apps und anderen Dynamics 365-Anwendungen unerlässlich. Einige Anwendungen basieren auf Common Data Service. Durch die Integration zwischen Finance and Operations-App-Daten mit Common Data Service können andere Anwendungen kohärent und fließend mit Finance and Operations kommunizieren.

Finance and Operations-Apps und Common Data Service bieten eine Datensynchronisierung zwischen Finance and Operations-Apps and anderen Dynamics 365-Anwendungen über ein Framework für duales Schreiben nahezu in Echtzeit. Die Deckung ist breit und umfasst 28 Oberflächenbereiche der Anwendung. Die Zielsetzung besteht darin, „eine Dynamics 365“-Benutzererfahrung über nahtlose Datenflüssen bereitzustellen, durch die Unternehmensprozesse über Anwendungen hinweg verbunden werden.

![Übersicht über die Architektur](media/dual-write-overview.jpg)

Die folgenden Wertvorschläge stehen zur Verfügung:

+ [Organisationshierarchie in Common Data Service](dual-write-organization.md)
+ [Unternehmenskonzept in Common Data Service](dual-write-company.md)
+ [Integrierte Masterdaten von Debitoren](dual-write-customer.md)
+ [Integriertes Sachkonto](dual-write-ledger.md)
+ [Einheitliche Produktumgebung](dual-write-product.md)
+ [Integrierte Masterdaten von Kreditoren](dual-write-vendor.md)
+ [Integrierte Standorte und Lagerorte](dual-write-sites-and-warehouses.md)
+ [Integrierter Steuermaster](dual-write-tax.md)

## <a name="system-requirements"></a>Systemanforderungen

Synchrone, bidirektionale Datenflüsse nahezu in Echtzeit erfordern die folgenden Versionen:

+ Microsoft Dynamics 365 for Finance and Operations-Version 10.0.4 (Juli 2019) mit Plattformaktualisierung 28 oder höher
+ Microsoft Dynamics 365 for Customer Engagement, Plattformversion 9.1 (4.2) oder höher

## <a name="setup-instructions"></a>Setupanweisungen

Führen Sie die folgenden Schritte aus, um die Integration zwischen Finance and Operations-Apps und Common Data Service einzurichten.
    
1. Informationen zur Einrichtung des Systems zum dualen Schreibens finden Sie im [Schritt-für-Schritt-Handbuch](https://aka.ms/dualwrite-docs) zur Ankündigung der Vorschau des dualen Schreibens.
2. Laden Sie die Lösung aus der Yammer-Gruppe [Finance and Operations-, Common Data Service- und Customer Engagement-Integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) herunter und installieren Sie sie. Das Paket beinhaltet fünf Lösungen:

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Befolgen Sie die Ausführungsreihenfolge für die [Synchronisierung der ersten Referenzdaten](dual-write-initial.md).
4. Wenn Sie Probleme bei der Synchronisierung des dualen Schreibens feststellen, lesen Sie die Informationen im [Handbuch zur Problembehandlung für die Datenintegration](dual-write-troubleshooting.md).

> [!IMPORTANT]
> Duales Schreiben und [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) können nicht parallel ausgeführt werden. Wenn Sie die Prospect to cash-Lösung ausführen, müssen Sie sie deinstallieren. Sie müssen auch die Vorlagen des dualen Schreibens für Debitor und Kreditor deaktivieren, die Teil der Prospect to cash-Lösung sind.
