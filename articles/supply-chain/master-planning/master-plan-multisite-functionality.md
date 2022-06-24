---
title: Überblick über die Masterplanung und die standortübergreifende Funktionalität
description: Der Produktprogrammplan berücksichtigt die Einstellungen der Site Lagerortlagerdimensionen.
author: t-benebo
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2434"
- intro-internal
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 289763931703eb354ae78fa18f37cd00f1102de8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844908"
---
# <a name="master-planning-and-multisite-functionality-overview"></a>Überblick über die Masterplanung und die standortübergreifende Funktionalität

[!include [banner](../includes/banner.md)]

Der Produktprogrammplan berücksichtigt die Einstellungen der Site Lagerortlagerdimensionen. 

Die Standortdimension ist obligatorisch, und Sie können festlegen, dass auch die Lagerortdimension obligatorisch sein soll.

Wenn eine Dimension obligatorisch ist, muss bei allen Lagerbuchungen ein Dimensionswert eingegeben werden. Daher sind bei der Produktprogrammplanung der Standort und der Lagerort für den Anfangsbedarf bekannt. Die Standortdimension ist auch konsistent, sodass sich der Standortwert während der Auflösung des Bedarfs auf niedrigerer Ebene nicht ändert.

Wenn der Lagerort nicht auf obligatorisch festgelegt ist, ist er möglicherweise nicht aus dem Anfangsbedarf bekannt. Das Planungsmodul muss den zu verwendenden Lagerort auf Grundlage der für den Artikel festgelegten Einstellungen, einzelner Lagerorte und der Details der Auftragsposition bestimmen.

In den folgenden Artikeln wird die Funktionsweise des Planungsmoduls bei Definition unterschiedlicher Einstellungen zur Bestimmung des zu verwendenden Lagerorts erläutert.

[Produktprogrammplanung für Disposition an Standort und Lagerort, Lagerort obligatorisch](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Hauptplanung für Standortdeckung, Lagerort obligatorisch](master-plan-site-coverage-warehouse-mandatory.md)

[Produktprogrammplanung für Disposition an Standort und Lagerort, Lagerort nicht obligatorisch](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Hauptplanung für Standortdeckung, Lagerort nicht obligatorisch](master-plan-site-coverage-warehouse-not-mandatory.md)

[Die Stücklistenversion bestimmen](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]