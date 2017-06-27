---
title: Aktualisieren der Standardkosten in einer Produktionsumgebung
description: "Dieser Artikel bietet eine Anleitung zum Aktualisieren von Standardkosten in einer Umgebung ohne Produktionstätigkeit."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 74ad59504d6bbea0c604e0f0b83e74c915e84019
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="update-standard-costs-in-a-manufacturing-environment"></a>Aktualisieren der Standardkosten in einer Produktionsumgebung

[!include[banner](../includes/banner.md)]


Dieser Artikel bietet eine Anleitung zum Aktualisieren von Standardkosten in einer Umgebung ohne Produktionstätigkeit. 

Aktualisierungen können neue Artikel, Kostenkategorien oder Berechnungsformeln für indirekte Kosten darstellen. Sie können auch Korrekturen und Kostenänderungen wiedergeben. Der Typ der Aktualisierung beeinflusst die Schritte, die erforderlich sind, um Standardkosten zu aktualisieren, wie in den folgenden Fällen veranschaulicht wird.

-   Geben Sie die erwarteten Standardkostenänderungen für eingekaufte Artikel ein, und ändern Sie anschließend den Status der Artikelkostendatensätze für das entsprechende Datum auf **Aktiv**. Sie führen jedoch keine Neuberechnung der Kosten für produzierte Artikel durch, für die die eingekauften Artikel verwendet werden.
-   Sie geben die Standardkosten für einen neuen eingekauften Artikel ein, führen jedoch keine Neuberechnung der Kosten für produzierte Artikel mit einer Stücklistenversion (BOM) durch, die den neuen eingekauften Artikel als Komponente enthält.
-   Sie korrigieren oder ändern die Kosten eines eingekauften Artikels oder Sie ändern die Kostengruppe, die einem eingekauften Artikel zugewiesen ist und berechnen die Kosten für alle produzierten Artikel mit einer Stücklistenversion, die den eingekauften Artikel als Komponente enthält.
-   Sie ändern die Kosten für eine Kostenkategorie und berechnen die Kosten für alle produzierten Artikel mit einer Arbeitsplanversion, die Arbeitsgänge des Arbeitsplans mit dieser Kostenkategorie enthält.
-   Ändern Sie die Kostenkategorien, die Arbeitsgängen des Arbeitsplans zugewiesen sind, oder die Kostengruppe, die Kostenkategorien zugewiesen ist. Berechnen Sie anschließend die Kosten für alle produzierten Artikel mit einer Arbeitsplanversion, die Arbeitsgänge des Arbeitsplans mit dieser Kostenkategorie enthält.
-   Sie ändern eine Berechnungsformel für indirekte Kosten und berechnen die Kosten für alle produzierten Artikel, auf die sich diese Änderung auswirkt.
-   Sie ändern den Produktionsstandort eines produzierten Artikels oder fügen einen Produktionsstandort hinzu und berechnen die Produktionskosten des Artikels für diesen Standort.
-   Sie führen eine (Neu-)Berechnung der Kosten für einen produzierten Artikel durch und berechnen die Kosten für alle produzierten Artikel mit einer Stücklistenversion neu, die den produzierten Artikel als Komponente enthält.
-   Sie berechnen die Kosten für einen neuen produzierten Artikel auf Basis der Informationen zur definierten, genehmigten und aktiven Stückliste bzw. zum Arbeitsplan.

Überlegen Sie in jedem der aufgeführten Fälle sehr sorgfältig, wie die Standardkosten aktualisiert werden können.




