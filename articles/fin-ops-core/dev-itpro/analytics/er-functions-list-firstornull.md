---
title: FIRSTORNULL EB-Funktion
description: In diesem Thema wir die Verwendung der FIRSTORNULL-Funktion bei der elektronischen Berichterstellung (EB) erklärt
author: NickSelin
manager: kfend
ms.date: 11/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86c8a0ae21ffeb6268efbbd198f7c709c2ad54f6
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042112"
---
# <a name="FIRSTORNULL">FIRSTORNULL EB-Funktion</a>

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
