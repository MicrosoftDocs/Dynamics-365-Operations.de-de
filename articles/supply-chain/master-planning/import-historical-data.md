---
title: Wichtige historische Daten für Bedarfsplanungen
description: Um genaue Bedarfsplanungen zu erhalten, benötigen Sie historische Bedarfsdaten pro Artikel oder Artikelverteilungsschlüssel. In diesem Thema wird erläutert, wie Datenentitäten verwendet werden, um historische Bedarfsdaten aus jedem beliebigen System zu importieren, sodass Sie eine längere Historie von Bedarfsplanungsdaten haben.
author: roxanadiaconu
manager: tfehr
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: d415895bd05b9ab1a2311ab69cc3757047df91db
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204615"
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

## <a name="example"></a>Beispiel

Sie können die folgende Datei als Beispiel verwenden. Laden Sie Die [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/) herunter. Diese Datei enthält die historischen Bedarfsdaten für Artikel D0001. Sie enthält nur die folgenden Pflichtfelder: Standort, Menge und das Bedarfsdatum.

1. Wählen Sie das Unternehmen aus, in das die historischen Bedarfsdaten importiert werden sollen.
2. Öffnen Sie den Arbeitsbereich **Datenverwaltung**.
3. Wählen Sie die Kachel **Importieren** aus.
4. Geben Sie einen Namen für das Importprojekt ein, wie **Historischen Bedarf für Artikel D0001 importieren**.
5. Wählen Sie im Feld **Quelldatenformat** das Dateiformat der Datei aus, die Sie importieren. Um die HistoricalDemandData-Datei für dieses Beispiel zu importieren, wählen Sie **CSV** aus.
6. Wählen Sie im Feld **Entitätsname** die Option **Historischer externer Bedarf** aus.
7. Speichern Sie die Datei auf Ihrem Computer, und laden Sie sie dann hoch.
8. **Import** auswählen
9. Die Seite **Ausführungszusammenfassung** wird automatisch geöffnet. Überprüfen Sie die importierten Daten auf der Seite.

Nachdem Sie die historischen Bedarfsdaten importiert haben, können Sie eine Bedarfsplanung generieren.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Eine statistische Grundplanung generieren](generate-statistical-baseline-forecast.md)  
[Einzelvorgänge für Datenimport und ‑export – Übersicht](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]