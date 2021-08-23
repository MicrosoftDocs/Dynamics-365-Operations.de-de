---
title: INDEX EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der INDEX-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 05/20/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e68f1690d6f852b0db560ef67a36fbde9e099715942a4b8a6e486d759af46682
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755778"
---
# <a name="index-er-function"></a>INDEX EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `INDEX` gibt den Wert *Container (Datensatz)* zurück, der unter Verwendung des angegebenen numerischen Index in der angegebenen Liste ausgewählt wird. Wenn sich der Index außerhalb des Bereichs für die Datensätze in der angegebenen Liste befindet, wird eine Ausnahme ausgelöst.

## <a name="syntax"></a>Syntax

```vb
INDEX (list, index)
```

## <a name="arguments"></a>Argumente

`list`: *Datensatzliste*

Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.

`index`: *Integer*

Ein numerischer Index, der die Position des gewünschten Datensatzes in der angegebenen Liste angibt.

> [!NOTE]
> Geben Sie den Wert an, da für diese Funktion eine einbasierte Nummerierung verwendet wird. Definieren Sie den Wert **1**, um den ersten Datensatz der angegebenen Liste zurückzugeben.

## <a name="return-values"></a>Rückgabewerte

*Container (Datensatz)*

Der resultierende Datensatzwert.

## <a name="example-1"></a>Beispiel 1

Wenn Sie die Datenquelle **DS** des Typs *Berechnetes Feld* eingeben und diese den Ausdruck `SPLIT ("A|B|C", "|")` enthält, gibt der Ausdruck `DS.Value` den Textwert **"B"** für den zweiten Datensatz dieser Datensatzliste zurück. Der Ausdruck `INDEX (SPLIT ("A|B|C", "|"), 2).Value` gibt auch den Textwert **"B"** zurück.

## <a name="example-2"></a>Beispiel 2

Wenn Sie die Datenquelle **DS** des Typs *Berechnetes Feld* eingeben, und sie den Ausdruck `SPLIT ("A|B|C", "|")` enthält, löst der Ausdruck `INDEX (SPLIT ("A|B|C", "|"), 4).Value` zur Laufzeit eine Ausnahme aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Listenfunktionen](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
