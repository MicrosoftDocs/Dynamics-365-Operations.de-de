---
title: INDEX EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der INDEX-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 05/20/2021
ms.topic: article
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
ms.openlocfilehash: 5a0fdb8958670efe8e2a37cee183bf836fa6c7e8
ms.sourcegitcommit: 047b0503868cc7d7b21868e24405d76af35db747
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087750"
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
