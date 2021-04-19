---
title: Integrierte Standorte und Lagerorte
description: In diesem Thema wird die Integration von Stand- und Lagerortdaten zwischen Finance and Operations and Dataverse beschrieben.
author: t-benebo
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 533635ece005636dcee4e24d1d132111e1e2b370
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750665"
---
# <a name="integrated-sites-and-warehouses"></a>Integrierte Standorte und Lagerorte

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



In diesem Thema wird die Integration von Stand- und Lagerortdaten zwischen Finance and Operations and Dataverse beschrieben. Betriebsstandorte und Lagerorte sind allgemeine Konzepte in einer Supply Chain Management-Anwendung. Sie werden verwendet, um die Lieferkette des Unternehmens zu modellieren.

## <a name="templates"></a>Vorlagen

Bei der Integration in Dataverse sind diese Konzepte und alle ihre zugehörigen Informationen in Dataverse mithilfe der Standort- und Lagerortdatentabellen in der folgenden Tabelle verfügbar.

Finance and Operations Apps | Sonstige Dynamics 365-Apps | Beschreibung
--------------------------|---------------------------|---
Websites | msdyn_operationalsites | 
Lagerorte | msdyn_warehouses | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]