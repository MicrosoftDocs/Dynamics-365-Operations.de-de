---
title: Planen Sie Belastungen mit Hilfe der Hub-Konsolidierungsübersicht.
description: Dieser Artikel beschreibt die Funktion zur Konsolidierung von Lieferungen in einem Hub bei der Lieferung von Waren aus unterschiedlichen Lagerorten an einen Kunden oder bei der Lieferung von mehreren Kreditoren an einen Lagerort.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, TMSParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbf84d551d7122516c8b5dd0be0246539e1e7e3f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005001"
---
# <a name="plan-loads-using-hub-consolidation-overview"></a>Planen Sie Belastungen mit Hilfe der Hub-Konsolidierungsübersicht.

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt die Funktion zur Konsolidierung von Lieferungen in einem Hub bei der Lieferung von Waren aus unterschiedlichen Lagerorten an einen Kunden oder bei der Lieferung von mehreren Kreditoren an einen Lagerort.

Die Konsolidierung von Lieferungen in einem Hub kann bei der Lieferung von Waren aus unterschiedlichen Lagerorten an einen Kunden oder bei der Lieferung von mehreren Kreditoren an einen Lagerort hilfreich sein.

## <a name="building-loads"></a>Erstellen von Ladungen
Bevor Sie die Hub-Konsolidierung verwenden können, müssen Sie die Option **In Transitplanung** auf der Seite **Transportverwaltungsparameter** aktivieren. Außerdem müssen Sie die Hubs für die Konsolidierung erstellen. Das folgende Diagramm zeigt ein Beispiel für die Hub-Konsolidierung. In diesem Fall gehen die Aufträge von verschiedenen Lagerorten an denselben Debitor. Die grundlegenden Ladungen werden ganz normal auf Basis von Aufträgen erstellt (über die Seite **Ladungsplanungsworkbench**). Um zwei Ladungen vor der Auslieferung in einem Hub zu konsolidieren, wählen Sie auf der Seite **Ladungsplanungsworkbench** im Feld **Transport** die Option **Hub-Konsolidierung**. Bei der Auswahl des richtigen Hubs für jede Ladung nutzen die Ladungen den Hub als "Abladeziel". Im Abschnitt **Beschaffung und Bedarf** auf der Seite **Ladungsplanungsworkbench** gibt es außerdem zwei "Transportanforderungspositionen". Sie können diese zwei Positionen dann zu einer neuen Ladung hinzufügen. Die neue Ladung umfasst beide Auftragspositionen und den Hub als "Aufladeadresse" sowie Kunde A als "Abladeziel". Die drei Ladungen können dann wie jede andere Ladung geroutet werden. Sie können jeden Spediteur auswählen, den das System für eine Ladung vorschlägt. [![Hub-Konsolidierung](./media/hubconsol.jpg)](./media/hubconsol.jpg) Die gleiche Methode können sie auch zur Konsolidierung von Ladungen für mehrere Umlagerungsauftrag nutzen. In diesem Fall ist Kunde A im obigen Diagramm ein Lagerort. Alternativ können Sie Ladungen für mehrere Aufträge, in denen Ladungen von unterschiedlichen Kreditoren an den selben Lagerort geliefert werden, konsolidieren. Sie können mehrere Konsolidierungs-Hubs nutzen und in mehreren Hubs für mehrere Ladungen aus verschiedenen Lagerorten konsolidieren. Nachdem Sie die grundlegenden Ladungen erstellt und die Option zur Hub-Konsolidierung verwendet haben, erstellen Sie über die konsolidierten Transportanforderungsposition neue Ladungen. Dann routen Sie die Ladungen.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]