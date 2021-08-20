---
title: Planung mit negativen Vorgabemengen
description: In diesem Thema wird erläutert, wie mit dem Negativ-Bestand umgegangen wird, wenn Sie die Planungsoptimierung einsetzen.
author: ChristianRytt
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 97688e09aae9706dd85e7965aa08c7ea873a44d81391c39406e2e6367660e0d0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758543"
---
# <a name="planning-with-negative-on-hand-quantities"></a>Planung mit negativen Vorgabemengen

[!include [banner](../../includes/banner.md)]

Wenn das System eine negative aggregierte Bestandsmenge anzeigt, behandelt die Planungsmaschine die Menge als 0 (Null), um ein Überangebot zu vermeiden. Im Folgenden wird erläutert, wie diese Funktionalität funktioniert:

1. Die Planungsoptimierung aggregiert die Bestandsmengen auf der untersten Ebene der Deckungsdimensionen. (Wenn z.B. *Lagerplatz* keine Deckungsdimension ist, aggregiert die Planungsoptimierung die verfügbaren Mengen auf der Ebene *Lager*).
1. Wenn die aggregierte Bestandsmenge auf der untersten Ebene der Deckungsdimensionen negativ ist, geht das System davon aus, dass die Bestandsmenge tatsächlich 0 (Null) ist.

> [!IMPORTANT]
> Das Planungssystem kann nur so genau sein wie die Eingabedaten. Wenn die Eingabedaten ungenau sind, zeigen negative Datensätze auf dem Datenbestand an, dass die Bestandsinformationen in Microsoft Dynamics 365 Supply Chain Management nicht mit der realen Welt übereinstimmen. Daher wird das Planungsergebnis fehlerhaft sein. Um ein präzises Planungsergebnis zu erhalten, sollten Sie die Anzahl der Datensätze, die eine negative Bestandsmenge aufweisen, minimieren.

## <a name="example-1"></a>Beispiel 1

Lager 13 ist wie folgt konfiguriert:

- **Deckungscode:** Min./Max.
- **Minimum:** 15 Stück (Stk.)
- **Maximal:** 25 Stk.

Die niedrigste Ebene der Deckungsdimensionen ist *Lager*, und die folgenden vorrätigen Mengen werden auf der Ebene *Lagerplatz* erfasst:

- **Standort 1, Lager 13, Lagerplatz 1:** 20 Stk.
- **Standort 1 Lager 13, Lagerplatz 2:** &minus;8 Stk.

Somit beträgt die aggregierte Bestandsmenge für Lager 13 12 Stk. (= 20 Stk. &minus; 8 Stk.).

In diesem Fall verwendet die Planungsmaschine eine Aggregat-Bestandsmenge von 12 Stk. für Lager 13.

Das Ergebnis ist ein Planauftrag von 13 Stück. (= 25 Stk. &minus; 12 Stk.), um Lager 13 aus 12 Stk. wieder aufzufüllen. auf 25 Stk.

## <a name="example-2"></a>Beispiel 2

Lager 13 ist wie folgt konfiguriert:

- **Abdeckungscode:** Min./Max.
- **Minimum:** 15 Stk.
- **Maximum:** 25 Stk.

Die niedrigste Ebene der Deckungsdimensionen ist *Lager*, und die folgenden vorrätigen Mengen werden auf der Ebene *Lagerplatz* erfasst:

- **Standort 1, Lager 13, Lagerplatz 1:** 4 Stk.
- **Standort 1 Lager 13, Lagerplatz 2:** &minus;8 Stk.

Daher beträgt die gesamte verfügbare Menge für Lager 13 &minus;4 Stk. (= 4 Stk. &minus; 8 Stk.). Mit anderen Worten, sie ist weniger als 0 (Null).

In diesem Fall geht das Planungsmodul davon aus, dass die vorrätige Menge für Lager 13 0 St. beträgt. statt &minus;4 Stk.

Das Ergebnis ist ein Planauftrag von 25 Stück. (= 25 Stk. &minus; 0 Stk.), um Lager 13 aus 0 Stk. wieder aufzufüllen. auf 25 Stk.

## <a name="planning-when-there-is-a-reservation-against-negative-on-hand-inventory"></a>Planung, wenn eine Reservierung gegen negativen verfügbaren Lagerbestand vorliegt

Wenn Sie den Lagerbestand anpassen, während physische Reservierungen vorhanden sind, können Sie eine Situation verursachen, in der eine Bestellung physisch gegen negativen Lagerbestand reserviert wird. Da in diesem Fall eine physische Reservierung vorhanden ist, geht die Planungsoptimierung davon aus, dass diese vom verfügbaren Lagerbestand gedeckt wird, auch wenn der Eingang des verfügbar Lagerbestands noch nicht im System eingetragen ist. Daher wird davon ausgegangen, dass keine Wiederbeschaffung erforderlich ist, und es wird kein Bestellvorschlag erstellt, um die Auftragsmenge aufzufüllen.

Das folgende Beispiel illustriert dieses Szenario.

### <a name="example"></a>Beispiel

Das System ist wie folgt konfiguriert:

- Produkt *FG* existiert und hat *10* Stk. verfügbaren Bestand.
- Die Produktkonfiguration erlaubt einen physischen Negativbestand.
- Ein Auftrag für eine Menge von *10* Stk. des Produkts *FG* liegt vor.
- Die Auftragsmenge wird physisch für den vorhandenen Lagerbestand reserviert.

Sie passen dann die Menge des Produkts *FG* an, sodass der verfügbare Bestand 0 (null) wird. Da der verfügbare Produktbestand null ist, wird die Auftragsmenge jetzt für den negativen Bestand reserviert. Wenn Sie jedoch jetzt die Produktprogrammplanung ausführen, wird kein Bestellvorschlag zur Erledigung des Auftrags erstellt, da die Planungsoptimierung davon ausgeht, dass der erforderliche verfügbare Lagerbestand für die Erledigung der physischen Reservierung vorhanden ist.

## <a name="related-resources"></a>Zugehörige Ressourcen

- [Übersicht zur Planungsoptimierung](planning-optimization-overview.md)
- [Erste Schritte mit der Planungsoptimierung](get-started.md)
- [Planungsoptimierung Fit-Analyse](planning-optimization-fit-analysis.md)
- [Planhistorie und Planungsprotokolle anzeigen](plan-history-logs.md)
- [Abbrechen eines Planungsauftrags](cancel-planning-job.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
