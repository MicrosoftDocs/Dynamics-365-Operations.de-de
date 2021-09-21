---
title: Fehler beim Ändern des Status von „Als erledigt gemeldet“ auf „Ende“
description: Sie erhalten möglicherweise einen Fehlerm wenn Sie den Status des Produktionsauftrags von „Als erledigt gemeldet“ auf „Ende“ ändern. Auf dieser Seite wird erklärt, wie das Problem gelöst werden kann.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 744637f5cccffe44b85f77c1a9df2034012fac40
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476450"
---
# <a name="error-when-changing-status-of-production-order-from-reported-as-finished-to-end"></a>Es ist ein Fehler beim Ändern des Status des Produktionsauftrags von „Fertig gemeldet“ auf „Ende“ aufgetreten

## <a name="symptoms"></a>Symptome

Wenn ich den Status eines Produktionsauftrags von „Als erledigt gemeldet“ auf „Ende“ ändere, erhalte ich folgende Fehlermeldung:

> Aktualisierungskonflikt. Die Standardkosten stimmen nicht mit dem Wert des finanziellen Bestands nach der Aktualisierung überein.

> Es ist ein kritischer Fehler in der Funktion InventCostMovement.checkVariance aufgetreten.

## <a name="cause"></a>Ursache

Dieses Problem tritt auf, weil die zugrunde liegenden Daten von einem anderen Prozess geändert wurden. Der Prozess versucht bis zu fünf Mal, die Daten zu aktualisieren. Wenn der Konflikt nach fünf Versuchen immer noch besteht, erhalten Sie eine der oben aufgeführten Fehlermeldungen:

## <a name="resolution"></a>Lösung

Dieses Verhalten ist beabsichtigt. Um das Problem zu beheben, setzen Sie den Batch-Job fort. Er sollte zu Ende laufen.

Wenn der Batch-Job nach der Wiederaufnahme immer wieder fehlschlägt, überprüfen Sie, ob die Rundungsgenauigkeit für die Standardwährung des Ledgers mit der Rundung übereinstimmt, die auf die Werte in der Tabelle InventSum angewendet wird. Wenn die Rundungsgenauigkeit auf einen nicht konformen Wert geändert wurde, müssen Sie sie wahrscheinlich wieder auf einen konformen Wert ändern. Suchen Sie nach **ModifiedDateTime**. In diesem Fall zeigt der Wert typischerweise an, dass die Rundungsgenauigkeit kürzlich geändert wurde.
