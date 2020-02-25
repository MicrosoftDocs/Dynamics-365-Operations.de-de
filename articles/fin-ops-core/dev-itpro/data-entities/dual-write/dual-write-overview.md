---
title: Datenintegration nahezu in Echtzeit mit Common Data Service
description: Dieser Artikel enthält eine Übersicht über die Integration zwischen Finance and Operations und Common Data Service.
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
ms.openlocfilehash: 1c09b0c0bb695e7695acb7a8821ffb99ae1f6f06
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019802"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a>Datenintegration nahezu in Echtzeit mit Common Data Service

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

In der derzeitigen digitalen Welt verwenden Geschäftsökosysteme die Microsoft Dynamics 365-Anwendungen als Ganzes. Da die Daten von Personen, Kunden, Arbeitsgängen und IoT-Geräten (Internet of Things) in eine Quelle fließen, gibt es eine Möglichkeit für digitale Rückmeldungsschleifen. Um dies zu erreichen, ist die Integration zwischen Finance and Operations-Apps und anderen Dynamics 365-Anwendungen unerlässlich. Einige Anwendungen basieren auf Common Data Service. Integration zwischen Finance and Operations-Apps Daten mit Common Data Service lassen Anwendungen kohärent und flüssig mit Finance and Operations kommunizieren.

Finance and Operations-Apps und Common Data Service bieten eine Datensynchronisierung zwischen Finance and Operations-Apps and anderen Dynamics 365-Anwendungen über ein Framework für duales Schreiben nahezu in Echtzeit. Die Deckung ist breit und umfasst 28 Oberflächenbereiche der Anwendung. Die Zielsetzung besteht darin, „eine Dynamics 365“-Benutzererfahrung über nahtlose Datenflüssen bereitzustellen, durch die Unternehmensprozesse über Anwendungen hinweg verbunden werden.

![Übersicht über die Architektur](media/dual-write-overview.jpg)

Die folgenden Wertvorschläge stehen zur Verfügung:

+ [Organisationshierarchie in Common Data Service](organization-mapping.md)
+ [Unternehmenskonzept in Common Data Service](company-data.md)
+ [Integrierte Masterdaten von Debitoren](customer-mapping.md)
+ [Integriertes Sachkonto](ledger-mapping.md)
+ [Einheitliche Produktumgebung](product-mapping.md)
+ [Integrierte Masterdaten von Kreditoren](vendor-mapping.md)
+ [Integrierte Standorte und Lagerorte](sites-warehouses-mapping.md)
+ [Integrierter Steuermaster](tax-mapping.md)

## <a name="system-requirements"></a>Systemanforderungen

Synchrone, bidirektionale Datenflüsse nahezu in Echtzeit erfordern die folgenden Versionen:

+ Microsoft Dynamics 365 for Finance and Operations-Version 10.0.4 (Juli 2019) mit Plattformaktualisierung 28 oder höher
+ Microsoft Dynamics 365 for Customer Engagement, Plattformversion 9.1 (4.2) oder höher

## <a name="setup-instructions"></a>Setupanweisungen

Folgen Sie diesen Schritten, um die Integration zwischen Finance and Operations-Apps und Common Data Service einzurichten.
    
1. Informationen zur Einrichtung des Systems zum dualen Schreibens finden Sie im [Schritt-für-Schritt-Handbuch](https://aka.ms/dualwrite-docs) zur Ankündigung der Vorschau des dualen Schreibens.
2. Laden Sie die Lösung aus der Gruppe [Fin Ops und CDS/CE-Integration über Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer herunter. Das Paket beinhaltet fünf Lösungen:

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Befolgen Sie die Ausführungsreihenfolge für die [Synchronisierung der ersten Referenzdaten](initial-sync.md).
4. Wenn Sie Probleme bei der Synchronisierung des dualen Schreibens feststellen, lesen Sie die Informationen im [Handbuch zur Problembehandlung für die Datenintegration](dual-write-troubleshooting.md).

> [!IMPORTANT]
> Duales Schreiben und [Prospect to cash](../../../../supply-chain/sales-marketing/prospect-to-cash.md) können nicht parallel ausgeführt werden. Wenn Sie die Prospect to cash-Lösung ausführen, müssen Sie sie deinstallieren. Sie müssen auch die Vorlagen des dualen Schreibens für Debitor und Kreditor deaktivieren, die Teil der Prospect to cash-Lösung sind.
