---
title: Datenintegration zwischen Finance and Operations und Common Data Service nahezu in Echtzeit
description: Dieser Artikel enthält eine Übersicht über die Integration zwischen Microsoft Dynamics 365 for Finance and Operations und Common Data Service.
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
ms.openlocfilehash: aa614c8e6a79a3f7a4f8f2f99f1f1bd1a67ac921
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797227"
---
# <a name="near-real-time-data-integration-between-finance-and-operations-and-common-data-service"></a>Datenintegration zwischen Finance and Operations und Common Data Service nahezu in Echtzeit

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

In der derzeitigen digitalen Welt verwenden Geschäftsökosysteme die Microsoft Dynamics 365-Suite als Ganzes. Da die Daten von Personen, Kunden, Arbeitsgängen und IoT-Geräten (Internet of Things) in eine Quelle fließen, gibt es eine Möglichkeit für digitale Rückmeldungsschleifen. Um dies zu erreichen, ist die Integration zwischen Dynamics 365 for Finance and Operations und Dynamics 365 for Customer Engagement-Anwendungen unerlässlich. Customer Engagement-Anwendungen basieren auf Common Data Service. Durch die Integration zwischen Finance and Operations-Daten mit Common Data Service können Customer Engagement-Anwendungen kohärent und fließend mit Finance and Operations kommunizieren.

Finance and Operations und Common Data Service bieten eine Datensynchronisierung zwischen Finance and Operations and Customer Engagement-Anwendungen über ein Framework für duales Schreiben nahezu in Echtzeit. Die Deckung ist breit und umfasst 28 Oberflächenbereiche von Finance and Operations. Die Zielsetzung besteht darin, „eine Dynamics 365“-Benutzererfahrung über nahtlose Datenflüssen bereitzustellen, durch die Unternehmensprozesse über Anwendungen hinweg verbunden werden.

![Übersicht über die Architektur](media/dual-write-overview.jpg)

Die folgenden Wertvorschläge stehen für Debitoren zur Verfügung:

+ [Organisationshierarchie in Common Data Service](dual-write-organization.md)
+ [Unternehmenskonzept in Common Data Service](dual-write-company.md)
+ [Integrierte Masterdaten von Debitoren](dual-write-customer.md)
+ [Integrierte Masterdaten von Kreditoren](dual-write-vendor.md)
+ Einheitlicher Produktmaster

## <a name="system-requirements"></a>Systemanforderungen

Synchrone, bidirektionale Datenflüsse nahezu in Echtzeit erfordern die folgenden Versionen:

+ Microsoft Dynamics 365 for Finance and Operations-Version 10.0.4 (Juli 2019) mit Plattformaktualisierung 28 oder höher
+ Microsoft Dynamics 365 for Customer Engagement, Plattformversion 9.1 (4.2) oder höher

## <a name="setup-instructions"></a>Setupanweisungen

Führen Sie die folgenden Schritte aus, um die Integration zwischen Finance and Operations und Common Data Service einzurichten.
    
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