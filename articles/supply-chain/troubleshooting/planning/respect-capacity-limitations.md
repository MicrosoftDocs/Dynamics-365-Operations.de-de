---
title: Die Produktprogrammplanung terminiert mehr als die verfügbare Kapazität
description: Die Produktprogrammplanung scheint Kapazitätsbeschränkungen nicht zu respektieren und terminiert mehr als die verfügbare Kapazität
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
ms.openlocfilehash: 48b3d179bb923ff6f6cc5b6be291408b3eb34d98
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476458"
---
# <a name="master-planning-is-scheduling-more-than-the-available-capacity"></a>Die Produktprogrammplanung terminiert mehr als die verfügbare Kapazität

## <a name="symptoms"></a>Symptome

Die Produktprogrammplanung scheint Kapazitätsbeschränkungen nicht zu respektieren und terminiert mehr als die verfügbare Kapazität.

Wenn Sie eine Vorgangsterminierung verwenden, bei der es eine endliche Kapazität gibt und der Arbeitsplan eine Mischung aus Bedarfen sowohl für eine Ressourcengruppe als auch für einzelne Ressourcen angibt, besteht eine kleine Chance auf Überbuchung aufgrund der Art und Weise, wie der Algorithmus auf Kapazitätskonflikte prüft. Diese Überbuchung kann auftreten, wenn Sie Helfer zur Ausführung der Produktprogrammplanung verwenden. Sie tritt am ehesten auf, wenn es viele Aufträge gibt, die eine relativ kurze Laufzeit haben.

## <a name="resolution"></a>Lösung

Wenn es wichtig ist, dass bei der Vorgangsterminierung keine Überbuchung auftritt, können Sie den Terminierungsteil der Produktprogrammplanung single-threaded machen, indem Sie die Option **Genaue endliche Kapazität für Vorgangsterminierung** auf der Seite **Parameter der Produktprogrammplanung** aktivieren. Diese Option ist standardmäßig nicht verfügbar. Sie müssen sie manuell auf der Seite hinzufügen, indem Sie die Funktionen zur Personalisierung verwenden. Wenn Sie diese Option verwenden, läuft die Planung aufgrund der fehlenden Parallelverarbeitung langsamer.
