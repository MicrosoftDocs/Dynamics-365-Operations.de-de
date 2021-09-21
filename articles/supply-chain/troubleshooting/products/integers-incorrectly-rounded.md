---
title: Bei der Berechnung von Produktkonfigurationsmodellen werden ganze Zahlen falsch gerundet.
description: Bei der Berechnung von Produktkonfigurationsmodellen werden ganze Zahlen nicht immer korrekt gerundet. Beheben Sie das Problem mit einem zusätzlichen Dezimalattribut und einer Berechnung.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b17145d7d17cb784fe11b3fbf65ddf5aa5530f27
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476463"
---
# <a name="integers-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>Bei der Berechnung von Produktkonfigurationsmodellen werden ganze Zahlen falsch gerundet.

## <a name="symptoms"></a>Symptome

Dieses Problem kann auftreten, wenn Sie die folgende Reihe von Aktionen durchführen:

1. Legen Sie diese Attribute in einem Produktkonfigurationsmodell fest:

    - Eingabe (ganzzahlig)
    - Prozentsatz (dezimal)
    - Ergebnis (ganzzahlig)

2. Erstellen Sie eine Formel, die den folgenden Ausdruck hat:

    *Ergebnis* = *Eingabe* × *Prozent* ÷ 100

In diesem Fall wird das ganzzahlige Ergebnis nicht immer korrekt gerundet. Wenn die Eingabe beispielsweise 1.000 ist und der Prozentsatz 2,40 beträgt, wird das ganzzahlige Ergebnis 24 erwartet, da 2,40 Prozent von 1.000 24 (oder 24,00 in Dezimalschreibweise) sind. Stattdessen wird das Ergebnis als 23 angezeigt. Wenn der Prozentsatz jedoch 2,39 beträgt, wird die Berechnung auf 24 anstelle von 23 gerundet. Wenn der Prozentsatz 2,50 beträgt, wird die Berechnung wie erwartet auf 25 gerundet.

## <a name="cause"></a>Ursache

Dieses Problem tritt aufgrund der Art und Weise auf, wie Microsoft Solver Foundation intern Zahlen unter Verwendung von Brüchen darstellt. Im vorangegangenen Beispiel wird das Ergebnis der Berechnung, bei der der Prozentsatz 2,40 beträgt, als 27021597764222975 ÷ 1125899906842624 = 23,99999999999999911182158029987476766109466552734375 dargestellt. Wenn .NET diesen Wert in eine Ganzzahl umwandelt, wird 23 zurückgegeben.

## <a name="resolution"></a>Lösung

Dieses Verhalten wird nicht geändert, da andere Szenarien davon abhängen. Für das vorangegangene Beispiel können Sie das Problem beheben, indem Sie ein zusätzliches Dezimalattribut und Berechnungen einführen.

Legen Sie zum Beispiel die folgenden Attribute in einem Produktionskonfigurationsmodell fest:

- Eingabe (ganzzahlig)
- Prozentsatz (dezimal)
- ResultDecimal (dezimal)
- ResultInteger (ganzzahlig)

Sie können dann die folgenden Berechnungen hinzufügen:

- *ResultDecimal* = *Eingabe* × *Prozent* ÷ 100
- *ResultInteger* = *ResultDecimal*
