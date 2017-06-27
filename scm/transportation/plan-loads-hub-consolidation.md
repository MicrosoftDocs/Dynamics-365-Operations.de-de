---
title: Planen von Ladungen mit der Hubkonsolidierung
description: Dieser Artikel beschreibt die Funktion zur Konsolidierung von Lieferungen in einem Hub bei der Lieferung von Waren aus unterschiedlichen Lagerorten an einen Kunden oder bei der Lieferung von mehreren Kreditoren an einen Lagerort.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: e0bd837a441a17e53982d5c5a7a7983f40e471c5
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="plan-loads-using-hub-consolidation"></a>Planen von Ladungen mit der Hubkonsolidierung

[!include[banner](../includes/banner.md)]


Dieser Artikel beschreibt die Funktion zur Konsolidierung von Lieferungen in einem Hub bei der Lieferung von Waren aus unterschiedlichen Lagerorten an einen Kunden oder bei der Lieferung von mehreren Kreditoren an einen Lagerort.

Die Konsolidierung von Lieferungen in einem Hub kann bei der Lieferung von Waren aus unterschiedlichen Lagerorten an einen Kunden oder bei der Lieferung von mehreren Kreditoren an einen Lagerort hilfreich sein.

## <a name="building-loads"></a>Erstellen von Ladungen
Bevor Sie die Hub-Konsolidierung verwenden können, müssen Sie die Option **In Transitplanung** auf der Seite **Transportverwaltungsparameter** aktivieren. Außerdem müssen Sie die Hubs für die Konsolidierung erstellen. Das folgende Diagramm zeigt ein Beispiel für die Hub-Konsolidierung. In diesem Fall gehen die Aufträge von verschiedenen Lagerorten an denselben Debitor. Die grundlegenden Ladungen werden ganz normal auf Basis von Aufträgen erstellt (über die Seite **Ladungsplanungsworkbench**). Um zwei Ladungen vor der Auslieferung in einem Hub zu konsolidieren, wählen Sie auf der Seite **Ladungsplanungsworkbench** im Feld **Transport** die Option **Hub-Konsolidierung**. Bei der Auswahl des richtigen Hubs für jede Ladung nutzen die Ladungen den Hub als "Abladeziel". Im Abschnitt **Beschaffung und Bedarf** auf der Seite **Ladungsplanungsworkbench** gibt es außerdem zwei "Transportanforderungspositionen". Sie können diese zwei Positionen dann zu einer neuen Ladung hinzufügen. Die neue Ladung umfasst beide Auftragspositionen und den Hub als "Aufladeadresse" sowie Kunde A als "Abladeziel". Die drei Ladungen können dann wie jede andere Ladung geroutet werden. Sie können jeden Spediteur auswählen, den das System für eine Ladung vorschlägt. [![Hub-Konsolidierung](./media/hubconsol.jpg)](./media/hubconsol.jpg) Die gleiche Methode können sie auch zur Konsolidierung von Ladungen für mehrere Umlagerungsauftrag nutzen. In diesem Fall ist Kunde A im obigen Diagramm ein Lagerort. Alternativ können Sie Ladungen für mehrere Aufträge, in denen Ladungen von unterschiedlichen Kreditoren an den selben Lagerort geliefert werden, konsolidieren. Sie können mehrere Konsolidierungs-Hubs nutzen und in mehreren Hubs für mehrere Ladungen aus verschiedenen Lagerorten konsolidieren. Nachdem Sie die grundlegenden Ladungen erstellt und die Option zur Hub-Konsolidierung verwendet haben, erstellen Sie über die konsolidierten Transportanforderungsposition neue Ladungen. Dann routen Sie die Ladungen.




