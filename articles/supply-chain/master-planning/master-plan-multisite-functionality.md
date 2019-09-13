---
title: Überblick über die Masterplanung und die standortübergreifende Funktionalität
description: Der Produktprogrammplan berücksichtigt die Einstellungen der Site Lagerortlagerdimensionen.
author: roxanadiaconu
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f05e3efd1716a27a659ae40145f37bb0b3d977f
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865402"
---
# <a name="master-planning-and-multisite-functionality-overview"></a>Überblick über die Masterplanung und die standortübergreifende Funktionalität

[!include [banner](../includes/banner.md)]

Der Produktprogrammplan berücksichtigt die Einstellungen der Site Lagerortlagerdimensionen. 

Die Standortdimension ist obligatorisch, und Sie können festlegen, dass auch die Lagerortdimension obligatorisch sein soll.

Wenn eine Dimension obligatorisch ist, muss bei allen Lagerbuchungen ein Dimensionswert eingegeben werden. Daher sind bei der Produktprogrammplanung der Standort und der Lagerort für den Anfangsbedarf bekannt. Die Standortdimension ist auch konsistent, sodass sich der Standortwert während der Auflösung des Bedarfs auf niedrigerer Ebene nicht ändert.

Wenn der Lagerort nicht auf obligatorisch festgelegt ist, ist er möglicherweise nicht aus dem Anfangsbedarf bekannt. Das Planungsmodul muss den zu verwendenden Lagerort auf Grundlage der für den Artikel festgelegten Einstellungen, einzelner Lagerorte und der Details der Auftragsposition bestimmen.

In den folgenden Themen wird die Funktionsweise des Planungsmoduls bei Definition unterschiedlicher Einstellungen zur Bestimmung des zu verwendenden Lagerorts erläutert.

[Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort obligatorisch](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort obligatorisch](master-plan-site-coverage-warehouse-mandatory.md)

[Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort nicht obligatorisch](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort nicht obligatorisch](master-plan-site-coverage-warehouse-not-mandatory.md)

[Produktprogrammplanungslauf - Ermittlung der Stücklistenversion](master-plan-bom-version-determined.md)



