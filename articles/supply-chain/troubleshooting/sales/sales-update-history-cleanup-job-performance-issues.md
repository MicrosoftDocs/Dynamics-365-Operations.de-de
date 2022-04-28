---
title: Der Auftrag zur Bereinigung des Verkaufsaktualisierungsverlaufs schlägt fehl oder weist Leistungsprobleme auf
description: Der Batchauftrag zum Bereinigen des Verkaufsverlaufs kann fehlschlagen oder sehr lange dauern, wenn eine große Menge an Verkaufsaktualisierungsdaten vorhanden ist.
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 124fb90ecafd4f4cccbd8a8bb443694c95365732
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570309"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>Der Auftrag zur Bereinigung des Verkaufsaktualisierungsverlaufs schlägt fehl oder weist Leistungsprobleme auf

## <a name="symptoms"></a>Symptome

Der Batchauftrag **Aktualisierungshistorie für Verkauf bereinigen** schlägt fehl oder weist Leistungsprobleme auf.  

## <a name="cause"></a>Ursache

Dies kann auftreten, wenn Ihr System eine große Anzahl von Verkaufsaktualisierungen enthält, was zu einer großen Menge von Verkaufsaktualisierungsdaten führen kann. Der Bereinigungsauftrag versucht, alle diese Daten in einer Transaktion zu bereinigen. Daher kann die Ausführung des Auftrags sehr lange dauern oder sogar fehlschlagen.

## <a name="resolution"></a>Lösung

Eine neue Version des Batchauftrags **Aktualisierungshistorie für Verkauf bereinigen** ist für Supply Chain Management Version 10.0.19 und höher verfügbar. Diese Funktion ist standardmäßig nicht aktiviert. Einzelheiten zur Funktionsweise und zur Aktivierung in der Funktionsverwaltung finden Sie unter [Datenbereinigung der Verkaufshistorie planen](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md).

