---
title: Standardkostenaktualisierungen verwalten
description: 'Die Aktualisierung von Standardkostendaten kann auf zwei unterschiedliche Arten verwaltet werden: durch den Einzelversionsansatz oder durch den Zwei-Versionen-Ansatz.'
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d1d498b1a843415e106c90330dd661b78bc2865e
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="manage-standard-cost-updates"></a>Standardkostenaktualisierungen verwalten

[!include[banner](../includes/banner.md)]


Die Aktualisierung von Standardkostendaten kann auf zwei unterschiedliche Arten verwaltet werden: durch den Einzelversionsansatz oder durch den Zwei-Versionen-Ansatz. 

Beim Einzelversionsansatz wird eine Nachkalkulationsversion mit sämtlichen Kostendatensätzen verwendet. Diese Datensätze beinhalten die anfänglich definierten Kosten sowie allen Kostenaktualisierungen.
Beim Zwei-Versionen-Ansatz enthält eine Version die Datensätze der anfänglich definierten Kosten und eine zweite Version alle Datensätze der Kostenaktualisierungen. Einer der wichtigsten Vorteile des Zwei-Versionen-Ansatzes besteht in der übersichtlichen Darstellung sowie in der Nachverfolgung von Kostenaktualisierungen in einer eigenen Nachkalkulationsversion, ohne dass sich dies auf die ursprüngliche Nachkalkulationsversion auswirkt. Der Zwei-Versionen-Ansatz kann zur Erkennung mehrerer stufenweiser Aktualisierungen verwendet werden, bei denen jede einzelne stufenweise Aktualisierung eine eigene Nachkalkulationsversion mit den stufenweisen Kostendatensätzen besitzt. **Beispiel** Das folgende Beispiel veranschaulicht, wie der Einzelversions- und der Zwei-Versionen-Ansatz bei der Aktualisierung von Standardkosten in einer Fertigungsumgebung verwendet werden kann. Aktualisierungen geben beispielsweise neue Artikel oder Korrekturen wieder. Angenommen, eine einzelne Nachkalkulationsversion stellt die Standardkosten des aktuellen Jahres dar. Die Kennung für diese Version lautet "2016-STD". Version "2016-STD" enthält die derzeit aktiven Kosten für alle Artikel. Darüber hinaus enthält diese Version alle arbeitsgangsteuerungsbezogenen Kostenkategorien und Berechnungsformeln für Gemeinkosten, die zu Beginn des Jahres 2016 bekannt waren. "2016-STD" ist die ursprüngliche Nachkalkulationsversion.
-   **Einzelversionsansatz für die Aktualisierung von Kostendaten** − Beim Einzelversionsansatz enthält die ursprüngliche Nachkalkulationsversion "2016-STD" sämtliche Kostendatensätze. Kostenaktualisierungen werden in "2016-STD" erfasst und auf den Status "Ausstehend" festgelegt. Die ausstehenden Kosten können manuell für neue eingekaufte Artikel eingegeben werden, oder sie können für einen hergestellten Artikel berechnet werden, um Korrekturen widerzuspiegeln. Wenn der Einzelversionsansatz verwendet wird, benötigen die Stücklistenberechnungen keine Fallbackdatenquelle, da alle aktiven Kosten in der Nachkalkulationsversion enthalten sind. Nach Aktivierung der ausstehenden Kosten enthält die ursprüngliche Nachkalkulationsversion "2016-STD" auch wieder alle derzeit aktiven Kosten.
-   **Zwei-Versionen-Ansatz für die Aktualisierung von Kostendaten** − Für den Zwei-Versionen-Ansatz wird eine zusätzliche Nachkalkulationsversion benötigt, in der ausschließlich die Kostenaktualisierungen enthalten sind. Der Bezeichner für diese Version ist "2016-STD-ÄNDERUNGEN". Kostenaktualisierungen werden in "2016-STD-ÄNDERUNGEN" erfasst und mit einem Status "Ausstehend" festgelegt. Mit dem Zwei-Versionen-Ansatz ist für die Stücklistenberechnungen von ausstehenden Kosten für hergestellte Artikel eine Fallbackdatenquelle erforderlich. Denn die zusätzliche Nachkalkulationsversion "2016-STD-ÄNDERUNGEN" enthält lediglich einen Teil der Kostendaten. Das Fallback kann entweder als aktive Kosten oder als Nachkalkulationsversion "2016-STD" ausgedrückt werden, da beide die Quelle der Kostendaten identifizieren, wenn sie nicht in "2016-STD-ÄNDERUNGEN" enthalten sind. Nach der Aktivierung der ausstehenden Kosten, enthält die Nachkalkulationsversion "2016-STD-ÄNDERUNGEN"die derzeit aktiven Kosten, die die Aktualisierungen widerspiegeln, wohingegen die ursprüngliche Nachkalkulationsversion 2016-STD diese nicht enthält. Wenn Sie den Zwei-Versionen-Ansatz verwenden, sollten Sie Sperrrichtlinien für die ursprüngliche Nachkalkulationsversion einrichten, um Aktualisierungen zu verhindern. Für die zusätzliche Nachkalkulationsversion sollten exakt die gleichen Richtlinien eingerichtet werden. Davon ausgenommen sind das angegebene Anfangsdatum sowie die selektive Verwendung von Sperrrichtlinien, um Aktualisierungen zuzulassen. Das angegebene Anfangsdatum muss zur Berücksichtigung des geplanten Aktivierungsdatums bei jeder Änderung geändert werden.

In diesem Beispiel wurde eine zusätzliche Nachkalkulationsversion zum Verwalten von Aktualisierungen im Laufe des Jahres 2016 verwendet. Es können auch mehrere zusätzliche Nachkalkulationsversionen verwendet werden, beispielsweise getrennte Versionen für jede einzelne Änderung. Falls mehrere zusätzliche Nachkalkulationen verwendet werden, muss das Fallback als aktive Kosten ausgedrückt werden, da sie sich über mehrere Nachkalkulationsversionen erstrecken würden.






