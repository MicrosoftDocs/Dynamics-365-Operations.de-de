---
title: Eine der Positionen wurde bereits geladen.
description: Auf dieser Seite wird erklärt, warum Sie möglicherweise die Fehlermeldung „Eine der Positionen wurde bereits geladen. Kann nicht an den Lagerort freigegeben werden.“ erhalten und wie Sie das Problem beheben können.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0bdfaed005b9c58f7bd5f87dd6dffe648de47261
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476494"
---
# <a name="one-of-the-lines-is-already-on-a-load"></a>Eine der Positionen wurde bereits geladen.

## <a name="symptoms"></a>Symptome

Bei der Arbeit mit Ladungserstellung und Lieferungen erhalten Sie möglicherweise die folgende Fehlermeldung:

> Eine der Positionen wurde bereits geladen. Kann nicht an den Lagerort freigegeben werden.

Wenn Sie Ladungen manuell erstellen oder den Prozess so festlegen, dass Ladungen bereits vor der Eingabe von Verkaufsauftragszeilen erstellt werden, wird davon ausgegangen, dass die anschließende Freigabe manuell erfolgt und dass der Arbeitsplan und die Einstufung aus der Ladung verwendet werden.

In einem anderen möglichen Szenario versuchen Sie, eine automatische Freigabe an das Lager durchzuführen, aber der Wellenprozess konnte keine Arbeit erstellen. Daher wird noch eine offene Sendung oder Ladung erstellt. Diese offene Sendung oder Ladung blockiert dann nachfolgende Versuche, den Auftrag automatisch freizugeben, bis Sie entweder die offene Sendung oder Ladung löschen oder die Welle manuell neu verarbeiten.

## <a name="resolution"></a>Lösung

Sie können die Freigabe über die Seite Verkaufsauftrag oder eine automatische Freigabe über die Seite für Freigabeaufträge nur dann durchführen, wenn vor der Freigabe an den Lagerort keine Ladung vorhanden ist. Die Ladung wird automatisch erstellt, nachdem die Welle verarbeitet wurde.
