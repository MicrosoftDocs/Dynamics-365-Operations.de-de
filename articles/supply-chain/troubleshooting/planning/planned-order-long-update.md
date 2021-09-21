---
title: Die Aktualisierung geplanter Aufträge nimmt viel Zeit in Anspruch
description: Wenn Sie die Bedarfsmenge und/oder das Lieferdatum eines Planauftrags aktualisieren, dauert es normalerweise mindestens 30 Sekunden pro Auftrag, bis die Aktualisierung gespeichert ist
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ccf3305cc18ea0ccf2ac3e9ca0dd507fd12a9da7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476457"
---
# <a name="planned-orders-take-a-long-time-to-update"></a>Die Aktualisierung geplanter Aufträge nimmt viel Zeit in Anspruch

## <a name="symptoms"></a>Symptome

Wenn Sie die Bedarfsmenge und/oder das Lieferdatum eines Planauftrags aktualisieren, dauert es normalerweise mindestens 30 Sekunden pro Auftrag, bis die Aktualisierung gespeichert ist.

## <a name="resolution"></a>Lösung

Dies ist ein bekanntes Problem mit der integrierten Produktprogrammplanung. Es wird durch die zugrundeliegende Autoauflösung durch die Stücklisten-Struktur während der Bearbeitungen verursacht. Dieses Problem wird in der Planungsoptimierung behoben, wo ein Planer die relevanten Aufträge aktualisieren und genehmigen kann und, wenn gewünscht, einen Planungslauf auslöst, um die Planaufträge für die zugrunde liegende Stückliste zu aktualisieren.

Eine Möglichkeit, die Leistung mit der eingebauten Produktprogrammplanung zu verbessern, ist es, die folgenden Schritte auszuführen:

1. Wechseln Sie zu **Produktprogrammplanung \> Einrichtung \> Pläne \> Produktprogrammpläne**.
1. Wählen Sie einen Plan aus.
1. Erweitern Sie das Inforegister **Zeitfenster in Tagen**.
1. Legen Sie **Auflösung** auf *Ja* fest und setzen Sie das Feld unterhalb dieser Einstellung auf 0 (Null).

> [!NOTE]
> Dadurch wird der Zeitraum für Auflösungen, die für diesen Masterplan durchgeführt werden, auf einen Tag begrenzt.
