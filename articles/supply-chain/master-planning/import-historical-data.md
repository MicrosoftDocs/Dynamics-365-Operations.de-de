---
title: Wichtige historische Daten für Bedarfsplanungen
description: Um genaue Bedarfsplanungen zu erhalten, benötigen Sie historische Bedarfsdaten pro Artikel oder Artikelverteilungsschlüssel. In diesem Thema wird erläutert, wie Datenentitäten verwendet werden, um historische Bedarfsdaten aus jedem beliebigen System zu importieren, sodass Sie eine längere Historie von Bedarfsplanungsdaten haben.
author: roxanadiaconu
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b04ee246d4c28e934407ccb92d792692cc4347d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301649"
---
# <a name="import-historical-data-for-demand-forecasts"></a>Wichtige historische Daten für Bedarfsplanungen

[!include [banner](../includes/banner.md)]

Um die Genauigkeit von Bedarfsplanungen zu gewährleisten, benötigen Sie so viele historische Bedarfsdaten wie möglich pro Artikel oder Artikelvereilungsschlüssel. Wenn die historischen Bedarfsdaten nicht bereits importiert sind, verwenden Sie die Datenentität **Historischer externer Bedarf** (ReqDemPlanHistoricalExternalDemandEntity) in Dynamics 365 Supply Chain Management, um sie zu importieren.

Im Arbeitsbereich **Datenverwaltung** können Sie eine Übersicht aller Felder in der Entität anzeigen.

1. Öffnen Sie den Arbeitsbereich **Datenverwaltung**.
2. Wählen Sie die Kachel **Datenentitäten** aus.
3. Durchsuchen Sie die Entitätsliste nach **Historischer externer Bedarf**.
4. Wählen Sie **Zielfelder** aus. Die folgenden Entitätsfelder sind obligatorisch: Standort (**DeliveringSiteId**), Datum (**DemandDate**), Menge (**DemandQuantity**) sowie entweder Artikelnummer (**ItemNumber**) oder Artikelverteilungsschlüssel (**ProductAllocationKeyId**).

Um die Datenentität zu verwenden, müssen Sie über eine Microsoft Excel-Datei oder eine durch Trennzeichen getrennte Datei (CSV-Datei) verfügen, die die historischen Bedarfsdaten enthält. Das folgende Beispiel zeigt, wie die Daten aus einer CSV-Datei importiert werden.

Weitere Informationen zum Importieren von Daten, einschließlich zum Bereinigen von Daten nach einem Import, finden Sie unter [Übersicht zu Datenimportaufträgen und Datenexportaufträgen](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) und in den verwandten Themen.

Siehe auch [Erstellen einer statistischen Basisplanung](generate-statistical-baseline-forecast.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]