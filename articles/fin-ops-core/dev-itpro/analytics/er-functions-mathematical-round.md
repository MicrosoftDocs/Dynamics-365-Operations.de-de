---
title: ROUND EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ROUND-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 12af71a024a76fca98fc2e876da9b59e5762cf07
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744550"
---
# <a name="round-er-function"></a>ROUND EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `ROUND` gibt die angegebene Zahl mit dem Wert *Real* zurück, nachdem sie auf die angegebene Zahl der Dezimalstellen gerundet wurde.

## <a name="syntax"></a>Syntax

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a>Argumente

`number`: *Real*

Ein numerischer Wert, der gerundet werden muss.

`decimals`: *Integer*

Ein numerischer Wert, der die Anzahl der Dezimalstellen angibt.

## <a name="return-values"></a>Rückgabewerte

*Gleitkommazahl*

Der resultierende numerische Wert.

## <a name="usage-notes"></a>Anwendungshinweise

Wenn der Wert des Arguments `decimals` größer als 0 (null) ist, wird die angegebene Zahl auf genau so viele Dezimalstellen gerundet.

Wenn der Wert des Arguments `decimals` **0** (null) ist, wird die angegebene Zahl auf die nächste ganze Zahl gerundet.

Wenn der Wert des Arguments `decimals` kleiner als 0 (null) ist, wir die angegebene Zahl links der Dezimalstelle gerundet.

## <a name="example-1"></a>Beispiel 1

`ROUND (1200.767, 2)` rundet auf zwei Dezimalstellen und gibt den Wert **1200.77** zurück.

## <a name="example-2"></a>Beispiel 2

`ROUND (1200.767, -3)` rundet auf das nächste Vielfache von 1.000 und gibt den Wert **1000** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Rechenoperationen](er-functions-category-mathematical.md)
