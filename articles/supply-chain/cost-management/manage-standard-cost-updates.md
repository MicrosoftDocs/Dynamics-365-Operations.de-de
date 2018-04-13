---
title: Standardkostenaktualisierungen verwalten
description: Die Aktualisierung von Standardkostendaten kann auf zwei unterschiedliche Arten verwaltet werden - durch den Einzelversionsansatz oder durch den Zwei-Versionen-Ansatz.
author: AndersGirke
manager: AnnBe
ms.date: 10/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b64d9e53736fd3b81ee997ed28ccfa62ed7e9ce6
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="manage-standard-cost-updates"></a>Standardkostenaktualisierungen verwalten

[!INCLUDE [banner](../includes/banner.md)]

Die Aktualisierung von Standardkostendaten kann auf zwei unterschiedliche Arten verwaltet werden - durch den Einzelversionsansatz oder durch den Zwei-Versionen-Ansatz. 

Beim Einzelversionsansatz wird eine Nachkalkulationsversion mit sämtlichen Kostendatensätzen verwendet. Diese Datensätze beinhalten die anfänglich definierten Kosten sowie allen Kostenaktualisierungen.

Beim Zwei-Versionen-Ansatz enthält eine Version die Datensätze der anfänglich definierten Kosten und eine zweite Version alle Datensätze der Kostenaktualisierungen. Einer der wichtigsten Vorteile des Zwei-Versionen-Ansatzes besteht in der übersichtlichen Darstellung sowie in der Nachverfolgung von Kostenaktualisierungen in einer eigenen Nachkalkulationsversion, ohne dass sich dies auf die ursprüngliche Nachkalkulationsversion auswirkt. Der Zwei-Versionen-Ansatz kann zur Erkennung mehrerer stufenweiser Aktualisierungen verwendet werden, bei denen jede einzelne stufenweise Aktualisierung eine eigene Nachkalkulationsversion mit den stufenweisen Kostendatensätzen besitzt. 

**Beispiel** 

Das folgende Beispiel veranschaulicht, wie der Einzelversions- und der Zwei-Versionen-Ansatz bei der Aktualisierung von Standardkosten in einer Produktionsumgebung verwendet werden kann. Aktualisierungen geben beispielsweise neue Artikel oder Korrekturen wieder. Angenommen, eine einzelne Nachkalkulationsversion stellt die Standardkosten des aktuellen Jahres dar. Die Kennung für diese Version lautet "2016-STD". Version "2016-STD" enthält die derzeit aktiven Kosten für alle Artikel. Darüber hinaus enthält diese Version alle arbeitsgangsteuerungsbezogenen Kostenkategorien und Berechnungsformeln für Gemeinkosten, die zu Beginn des Jahres 2016 bekannt waren. "2016-STD" ist die ursprüngliche Nachkalkulationsversion.

-   **Einzelversionsansatz für die Aktualisierung von Kostendaten** − Beim Einzelversionsansatz enthält die ursprüngliche Nachkalkulationsversion "2016-STD" sämtliche Kostendatensätze. Kostenaktualisierungen werden in "2016-STD" erfasst und auf den Status "Ausstehend" festgelegt. Die ausstehenden Kosten können manuell für neue eingekaufte Artikel eingegeben oder als Folge einer Korrektur für einen produzierten Artikel berechnet werden. Beim Einzelversionsansatz wird für die Herstellkostenkalkulation keine Fallback-Datenquelle benötigt, da in der Nachkalkulationsversion alle aktiven Kosten enthalten sind. Nach Aktivierung der ausstehenden Kosten enthält die ursprüngliche Nachkalkulationsversion "2016-STD" auch wieder alle derzeit aktiven Kosten.
-   **Zwei-Versionen-Ansatz für die Aktualisierung von Kostendaten** − Für den Zwei-Versionen-Ansatz wird eine zusätzliche Nachkalkulationsversion benötigt, in der ausschließlich die Kostenaktualisierungen enthalten sind. Der Bezeichner für diese Version ist "2016-STD-ÄNDERUNGEN". Kostenaktualisierungen werden in "2016-STD-ÄNDERUNGEN" erfasst und auf den Status "Ausstehend" festgelegt. Beim Zwei-Versionen-Ansatz ist für die Herstellkostenkalkulation der ausstehenden Kosten für produzierte Artikel eine Fallback-Datenquelle erforderlich. Denn die zusätzliche Nachkalkulationsversion "2016-STD-ÄNDERUNGEN" enthält lediglich einen Teil der Kostendaten. Das Fallback kann entweder als aktive Kosten oder als Nachkalkulationsversion "2016-STD" ausgedrückt werden, da beide die Quelle der Kostendaten identifizieren, wenn sie nicht in "2016-STD-ÄNDERUNGEN" enthalten sind. Nach Aktivierung der ausstehenden Kosten enthält die Nachkalkulationsversion "2016-STD-ÄNDERUNGEN" die derzeit aktiven Kosten (also die Aktualisierungen), wohingegen die ursprüngliche Nachkalkulationsversion "2016-STD" unverändert bleibt. Beim Zwei-Versionen-Ansatz sollten Sperrrichtlinien eingerichtet werden, um eine Aktualisierung der ursprünglichen Nachkalkulationsversion zu verhindern. Für die zusätzliche Nachkalkulationsversion sollten exakt die gleichen Richtlinien eingerichtet werden. Davon ausgenommen sind das angegebene Anfangsdatum sowie die selektive Verwendung von Sperrrichtlinien, um Aktualisierungen zuzulassen. Das angegebene Anfangsdatum muss zur Berücksichtigung des geplanten Aktivierungsdatums bei jeder Änderung geändert werden.

In diesem Beispiel wurde eine zusätzliche Nachkalkulationsversion zum Verwalten von Aktualisierungen im Laufe des Jahres 2016 verwendet. Es können auch mehrere zusätzliche Nachkalkulationsversionen verwendet werden, beispielsweise getrennte Versionen für jede einzelne Änderung. Falls mehrere zusätzliche Nachkalkulationen verwendet werden, muss das Fallback als aktive Kosten ausgedrückt werden, da sie sich über mehrere Nachkalkulationsversionen erstrecken würden.






