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
ms.openlocfilehash: d0b715e0c17263519a9bb1b3780170812271d93d
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813752"
---
# <a name="master-planning-and-multisite-functionality-overview"></a>Überblick über die Masterplanung und die standortübergreifende Funktionalität

[!include [banner](../includes/banner.md)]

Der Produktprogrammplan berücksichtigt die Einstellungen der Site Lagerortlagerdimensionen. 

Die Standortdimension ist obligatorisch, und Sie können festlegen, dass auch die Lagerortdimension obligatorisch sein soll.

Wenn eine Dimension obligatorisch ist, muss bei allen Lagerbuchungen ein Dimensionswert eingegeben werden. Daher sind bei der Produktprogrammplanung der Standort und der Lagerort für den Anfangsbedarf bekannt. Die Standortdimension ist auch konsistent, sodass sich der Standortwert während der Auflösung des Bedarfs auf niedrigerer Ebene nicht ändert.

Wenn der Lagerort nicht auf obligatorisch festgelegt ist, ist er möglicherweise nicht aus dem Anfangsbedarf bekannt. Das Planungsmodul muss den zu verwendenden Lagerort auf Grundlage der für den Artikel festgelegten Einstellungen, einzelner Lagerorte und der Details der Auftragsposition bestimmen.

In den folgenden Themen wird die Funktionsweise des Planungsmoduls bei Definition unterschiedlicher Einstellungen zur Bestimmung des zu verwendenden Lagerorts erläutert.

[Produktprogrammplanung für Disposition an Standort und Lagerort, Lagerort obligatorisch](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Hauptplanung für Standortdeckung, Lagerort obligatorisch](master-plan-site-coverage-warehouse-mandatory.md)

[Produktprogrammplanung für Disposition an Standort und Lagerort, Lagerort nicht obligatorisch](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Hauptplanung für Standortdeckung, Lagerort nicht obligatorisch](master-plan-site-coverage-warehouse-not-mandatory.md)

[Die Stücklistenversion bestimmen](master-plan-bom-version-determined.md)



