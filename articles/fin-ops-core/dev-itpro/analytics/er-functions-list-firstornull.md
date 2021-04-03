---
title: FIRSTORNULL EB-Funktion
description: In diesem Thema wir die Verwendung der FIRSTORNULL-Funktion bei der elektronischen Berichterstellung (EB) erklärt
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 53284333507ef1264d3eb66b0c7141eb69f32392
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564624"
---
# <a name="firstornull-er-function"></a>FIRSTORNULL EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `FIRSTORNULL` gibt den ersten Datensatz der angegebenen Liste mit dem Wert *Container (Datensatz)* zurück, wenn dieser Datensatz nicht leer ist. Wenn der Datensatz leer ist, gibt diese Funktion den Wert null für *Container (Datensatz)* zurück.

## <a name="syntax"></a>Syntax

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a>Argumente

`list`: *Datensatzliste*

Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.

## <a name="return-values"></a>Rückgabewerte

*Container (Datensatz)*

Der resultierende Datensatzwert.

## <a name="example"></a>Beispiel

Der Ausdruck `FIRSTORNULL(SPLIT("",1)).Value` gibt eine leere Zeichenkette zurück (**""**).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Listenfunktionen](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]