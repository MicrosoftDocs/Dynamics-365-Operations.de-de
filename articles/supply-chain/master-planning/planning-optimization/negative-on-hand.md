---
title: Mit negativen Vorgabemengen planen
description: In diesem Artikel wird erläutert, wie mit negativen Lagerbeständen umgegangen wird.
author: t-benebo
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
ms.author: benebotg
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: b4fc8b37fd800e3b4652513f150f9806bf1d5d67
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741121"
---
# <a name="planning-with-negative-on-hand-quantities"></a>Mit negativen Vorgabemengen planen

[!include [banner](../../includes/banner.md)]

Wenn das System eine negative aggregierte Bestandsmenge anzeigt, behandelt die Planungsmaschine die Menge als 0 (Null), um ein Überangebot zu vermeiden. Im Folgenden wird erläutert, wie diese Funktionalität funktioniert:

1. Die Masterplanung aggregiert die Bestandsmengen auf der untersten Ebene der Deckungsdimensionen. (Wenn z.B. *Lagerplatz* keine Deckungsdimension ist, aggregiert die Masterplanung die verfügbaren Mengen auf der Ebene *Lager*).
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

Wenn Sie den Lagerbestand anpassen, während physische Reservierungen vorhanden sind, können Sie eine Situation verursachen, in der eine Bestellung physisch gegen negativen Lagerbestand reserviert wird. Da in diesem Fall eine physische Reservierung besteht, müssen Sie einen Vorrat haben, um die reservierte Menge zu decken. Daher ist eine Wiederbeschaffung erforderlich, sodass das System entweder einen Auftragsvorschlag erstellt, um die Menge aufzufüllen, die nicht durch den vorhandenen Lagerbestand abgedeckt werden konnte, oder sie mit einer vorhandenen Bestellung für den Artikel abdeckt.

Das folgende Beispiel illustriert dieses Szenario.

### <a name="example"></a>Beispiel

Das System ist wie folgt konfiguriert:

- Produkt *FG* existiert und hat *10* Stk. verfügbaren Bestand.
- Die Produktkonfiguration erlaubt einen physischen Negativbestand.
- Ein Auftrag für eine Menge von *10* Stk. des Produkts *FG* liegt vor.
- Die Auftragsmenge wird physisch für den vorhandenen Lagerbestand reserviert.

Sie passen dann die Menge des Produkts *FG* an, sodass der verfügbare Bestand 5 wird. Da der verfügbare Produktbestand 5 beträgt, wird die Auftragsmenge jetzt für eine Menge reserviert, die nicht verfügbar ist (es wäre ähnlich, wenn der verfügbare Bestand 0 wäre, in diesem Fall würde der Auftrag gegen negativen Bestand reserviert werden). Wenn Sie jetzt die Produktprogrammplanung ausführen, wird ein Auftragsvorschlag der Menge 5 für *FG* zur Erledigung des Auftrags erstellt, da die Masterplanung immer vorhandenen Vorrat verwendet oder einen neuen Auftragsvorschlag zur Erledigung der physischen Reservierung erstellt.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
