---
title: Integrierte Standorte und Lagerorte
description: In diesem Thema wird die Integration von Stand- und Lagerortdaten zwischen Finance and Operations und Common Data Service beschrieben.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
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
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 4cf402e2811aaf92ddfa78eaf6d8887d88d93cbc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770986"
---
# <a name="integrated-sites-and-warehouses"></a>Integrierte Standorte und Lagerorte

[!include [banner](../includes/banner.md)]

In diesem Thema wird die Integration von Stand- und Lagerortdaten zwischen Finance and Operations und Common Data Service beschrieben. Betriebsstandorte und Lagerorte sind allgemeine Konzepte in einer Supply Chain Management-Anwendung. Sie werden verwendet, um die Lieferkette des Unternehmens zu modellieren.

## <a name="templates"></a>Vorlagen

Bei der Integration in Common Data Service sind diese Konzepte und all ihre zugehörigen Informationen in Common Data Service mithilfe der Standort- und Lagerortdatenentitäten in der folgenden Tabelle verfügbar.

Finance and Operations-Apps | Sonstige Dynamics 365-Apps | Beschreibung
--------------------------|---------------------------|---
Websites | msdyn_operationalsites | 
Lagerorte | msdyn_warehouses | 

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [operational sites](dual-write/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](dual-write/InventWarehouseEntity-msdyn-warehouse.md)]

