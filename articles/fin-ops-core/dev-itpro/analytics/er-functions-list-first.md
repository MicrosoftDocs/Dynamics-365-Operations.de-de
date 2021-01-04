---
title: FIRST EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der FIRST-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: a5c52d3f999b4c6fbdea0685977ab13fca1e8ffb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679413"
---
# <a name="first-er-function"></a>FIRST EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `FIRST` gibt den ersten Datensatz der angegebenen Liste mit dem Wert *Container (Datensatz)* zurück, wenn diese Liste nicht leer ist. Wenn die Liste leer ist, löst diese Funktion eine Ausnahme aus.

## <a name="syntax"></a>Syntax

```vb
FIRST (list)
```

## <a name="arguments"></a>Argumente

`list`: *Datensatzliste*

Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.

## <a name="return-values"></a>Rückgabewerte

*Container (Datensatz)*

Der resultierende Datensatzwert.

## <a name="example-1"></a>Beispiel 1

Der Ausdruck `FIRST(SPLIT("ABC",1)).Value` gibt den Textwert **"A"** zurück.

## <a name="example-2"></a>Beispiel 2

Der Ausdruck `FIRST(SPLIT("",1)).Value` löst zur Laufzeit eine Ausnahme aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Listenfunktionen](er-functions-category-list.md)
