---
title: Der Bericht zu indirekten Kosten in Bearbeitung enthält gelöschte Produktionsaufträge
description: Der Bericht zu indirekten Kosten in Bearbeitung enthält Informationen zu Produktionsaufträgen, die teilweise bearbeitet und später gelöscht wurden.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 817802f1f2ad3ab07f35c28d3e833a14cd02cf8b9705c576325dc83933a0c6de
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751768"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a>Der Bericht zu indirekten Kosten in Bearbeitung enthält gelöschte Produktionsaufträge

KB-Nummer: 4612748

## <a name="symptoms"></a>Symptome

Der Bericht **Indirekte Kosten in Bearbeitung** enthält Informationen zu Produktionsaufträgen, die teilweise bearbeitet und später gelöscht wurden.

## <a name="resolution"></a>Lösung

Wenn Sie einen Produktionsauftrag stornieren, stornieren Sie auch alle Transaktionen dieses Produktionsauftrags. Wenn Sie den Produktionsauftrag löschen, behalten die Tabellen in untergeordneten Sachkonten und das Hauptbuch alle damit verbundenen Transaktionen bei. In den Berichten werden die Transaktionen in den Tabellen der untergeordneten Sachkonten angezeigt. Für den spezifischen Produktionsauftrag sollte der Nettowert 0,00 betragen.
