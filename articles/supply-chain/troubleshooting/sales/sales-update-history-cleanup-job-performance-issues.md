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
ms.openlocfilehash: c02273adf90afc67b7c0ae1b82c19d489bfbd3b1
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920073"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>Der Auftrag zur Bereinigung des Verkaufsaktualisierungsverlaufs schlägt fehl oder weist Leistungsprobleme auf

## <a name="symptoms"></a>Symptome

Der Batchauftrag **Aktualisierungshistorie für Verkauf bereinigen** schlägt fehl oder weist Leistungsprobleme auf.  

## <a name="cause"></a>Ursache

Dies kann auftreten, wenn Ihr System eine große Anzahl von Verkaufsaktualisierungen enthält, was zu einer großen Menge von Verkaufsaktualisierungsdaten führen kann. Der Bereinigungsauftrag versucht, alle diese Daten in einer Transaktion zu bereinigen. Daher kann die Ausführung des Auftrags sehr lange dauern oder sogar fehlschlagen.

## <a name="resolution"></a>Lösung

Eine neue Version des Batchauftrags **Aktualisierungshistorie für Verkauf bereinigen** ist für Supply Chain Management Version 10.0.19 und höher verfügbar. Diese Funktion ist standardmäßig nicht aktiviert. Einzelheiten zur Funktionsweise und zur Aktivierung in der Funktionsverwaltung finden Sie unter [Leistungsverbesserungen bei der Bereinigung des Umsatzverlaufs](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md).

