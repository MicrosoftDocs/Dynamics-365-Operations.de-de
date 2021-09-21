---
title: Die Produktionsplanung berücksichtigt nicht die Sicherheitsmargen
description: Die Produktionsplanung berücksichtigt nicht die Sicherheitsmargen, die in der Elementabdeckung für Bedarfsverursacher festgelegt sind
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
ms.openlocfilehash: 738296b7570ded0a4ee806e4445204a68e6a08c8
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476423"
---
# <a name="production-scheduling-doesnt-consider-the-safety-margins"></a>Die Produktionsplanung berücksichtigt nicht die Sicherheitsmargen

## <a name="symptoms"></a>Symptome

Die Produktprogrammplanung berücksichtigt die Sicherheitsabstände. Bei der Terminierung von geplanten Produktionsaufträgen werden die Sicherheitsmargen jedoch ignoriert.

## <a name="resolution"></a>Lösung

Ränder werden nur bei der Produktprogrammplanung berücksichtigt, nicht bei der manuellen Terminierung. Die Sicherheitsmargen sind als Puffer während der Planungsphase gedacht, um einen gewissen „Spielraum“ für den tatsächlichen Prozess zu haben.

Um das gewünschte Ergebnis zu erhalten, können Sie die Marge entfernen. Der Arbeitsplan muss dann so aktualisiert werden, dass er die gewünschte Zeit enthält (z. B. als Warteschlangenzeit). Sowohl die Produktprogrammplanung als auch die manuelle Terminierung sollten dann das gleiche Ergebnis liefern.
