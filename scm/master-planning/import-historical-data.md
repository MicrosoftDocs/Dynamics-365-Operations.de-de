---
title: "Wichtige historische Daten für Bedarfsplanungen"
description: "Um genaue Bedarfsplanungen zu erhalten, benötigen Sie historische Bedarfsdaten pro Artikel oder Artikelverteilungsschlüssel. In diesem Thema wird erläutert, wie Datenentitäten verwendet werden, um historische Bedarfsdaten aus jedem beliebigen System zu importieren, sodass Sie eine längere Historie von Bedarfsplanungsdaten haben."
author: YuyuScheller
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0d1e2b9a51c2d7a7c30c2458b7babf8ac5c08118
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="import-historical-data-for-demand-forecasts"></a>Wichtige historische Daten für Bedarfsplanungen

[!include[banner](../includes/banner.md)]

Um die Genauigkeit von Bedarfsplanungen zu gewährleisten, benötigen Sie so viele historische Bedarfsdaten wie möglich pro Artikel oder Artikelvereilungsschlüssel. Wenn die historischen Bedarfsdaten nicht bereits importiert sind, verwenden Sie die Datenentität **Historischer externer Bedarf** (ReqDemPlanHistoricalExternalDemandEntity) in Microsoft Dynamics 365 for Operations, um sie zu importieren.

Im Arbeitsbereich **Datenverwaltung** können Sie eine Übersicht aller Felder in der Entität anzeigen.

1. Öffnen Sie den Arbeitsbereich **Datenverwaltung**.
2. Klicken Sie auf die Kachel **Datenentitäten**.
3. Durchsuchen Sie die Entitätsliste nach **Historischer externer Bedarf**.
4. Klicken Sie auf **Zielfelder**. Die folgenden Entitätsfelder sind obligatorisch: Standort (**DeliveringSiteId**), Datum (**DemandDate**), Menge (**DemandQuantity**) sowie entweder Artikelnummer (**ItemNumber**) oder Artikelverteilungsschlüssel (**ProductAllocationKeyId**).

Um die Datenentität zu verwenden, müssen Sie über eine Microsoft Excel-Datei oder eine durch Trennzeichen getrennte Datei (CSV-Datei) verfügen, die die historischen Bedarfsdaten enthält. Das folgende Beispiel zeigt, wie die Daten aus einer CSV-Datei importiert werden.

## <a name="example"></a>Beispiel

Sie können die folgende Datei als Beispiel verwenden. Laden Sie Die [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast) herunter. Diese Datei enthält die historischen Bedarfsdaten für Artikel D0001. Sie enthält nur die folgenden Pflichtfelder: Standort, Menge und das Bedarfsdatum.

1. Wählen Sie das Unternehmen aus, in das die historischen Bedarfsdaten importiert werden sollen.
2. Öffnen Sie den Arbeitsbereich **Datenverwaltung**.
3. Klicken Sie auf die Kachel **Importieren**.
4. Geben Sie einen Namen für das Importprojekt ein, wie **Historischen Bedarf für Artikel D0001 importieren**.
5. Wählen Sie im Feld **Quelldatenformat** das Dateiformat der Datei aus, die Sie importieren. Um die HistoricalDemandData-Datei für dieses Beispiel zu importieren, wählen Sie **CSV** aus.
6. Wählen Sie im Feld **Entitätsname** die Option **Historischer externer Bedarf** aus.
7. Speichern Sie die Datei auf Ihrem Computer, und laden Sie sie dann hoch.
8. Klicken Sie auf **Import**.
9. Die Seite **Ausführungszusammenfassung** wird automatisch geöffnet. Überprüfen Sie die importierten Daten auf der Seite.

Nachdem Sie die historischen Bedarfsdaten importiert haben, können Sie eine Bedarfsplanung generieren.

## <a name="see-also"></a>Siehe auch

[Eine statistische Grundplanung generieren](generate-statistical-baseline-forecast.md)

