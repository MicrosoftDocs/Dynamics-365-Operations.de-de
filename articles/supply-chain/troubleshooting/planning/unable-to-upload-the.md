---
title: Sie können die geplanten Einstandspreise nicht aktualisieren, wenn Sie Bedarfsplanungsdatensätze importieren
description: Wenn Sie Datenentitäten zum Importieren von Bedarfsplanungsdatensätzen verwenden, wird der Einstandspreis für vorhandene Datensätze nicht aktualisiert, um mit den importierten Daten übereinzustimmen.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: de471da861785f283eeaa78f97b5d1e1a6b023d71de6fff72ae39edd6bb124cc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765369"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a>Sie können die geplanten Einstandspreise nicht aktualisieren, wenn Sie Bedarfsplanungsdatensätze importieren

KB-Nummer: 4614109

## <a name="symptoms"></a>Symptome

Wenn Sie Datenentitäten zum Importieren von Bedarfsplanungsdatensätzen verwenden, wird der Wert **Geplanter Einstandspreis** für vorhandene Datensätze nicht aktualisiert, um mit den importierten Daten übereinzustimmen.

## <a name="cause"></a>Ursache

**Geplanter Einstandspreis** ist ein schreibgeschütztes Feld. Der Wert basiert auf dem Produkteinstandspreis und kann nicht direkt durch Import festgelegt werden.

## <a name="resolution"></a>Lösung

Da das Feld schreibgeschützt ist, können Sie keine Werte dafür importieren. Der Wert wird gemäß der vorhandenen Geschäftslogik berechnet.
