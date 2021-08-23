---
title: COUNT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der COUNT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 0fc122dafd6be90d090ba3b79a8c2eccab74d77441f82db71cb5e08d13d13518
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753645"
---
# <a name="count-er-function"></a>COUNT EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `COUNT` gibt den Wert *Integer* zurück, der die Anzahl der Datensätze in der angegebenen Liste darstellt, wenn die Liste nicht leer ist. Wenn die Liste leer ist, gibt diese Funktion **0** (Null) zurück.

## <a name="syntax"></a>Syntax

```vb
COUNT (list)
```

## <a name="arguments"></a>Argumente

`list`: *Datensatzliste*

Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.

## <a name="return-values"></a>Rückgabewerte

*Ganze Zahl*

Der resultierende numerische Wert.

## <a name="example"></a>Beispiel

`COUNT (SPLIT("abcd" , 3))` gibt **2** zurück, da die Funktion `SPLIT`, die in diesem Beispiel verwendet wird, eine Liste erstellt, die aus zwei Datensätzen besteht.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Listenfunktionen](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]