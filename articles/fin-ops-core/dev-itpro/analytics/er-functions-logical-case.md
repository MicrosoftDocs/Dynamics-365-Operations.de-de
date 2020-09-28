---
title: CASE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der CASE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 605bd50005ee4e5866a5be9e16df6da3139ad19c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744766"
---
# <a name="case-er-function"></a>CASE EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `CASE` bewertet den Wert des angegebenen Ausdrucks anhand der angegebenen alternativen Optionen und gibt das Ergebnis der ersten Option zurück, die dem Wert des angegebenen Ausdrucks entspricht. Andernfalls wird ein optionales Standardergebnis zurückgegeben, wenn als letztes Argument der aufgerufenen Funktion ein Standardergebnis angegeben wird, dem keine Option vorangestellt ist. Der zurückgegebene Wert kann ein Wert eines beliebigen unterstützten Datentyps sein.

## <a name="syntax"></a>Syntax

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a>Argumente

`expression`: *Primitiver Datentyp* (Boolesch, numerisch oder Text)

Ein gültiger Ausdruck, der einen Wert des primitiven Datentyps zurückgibt.

`option 1`: *Primitiver Datentyp* (Boolesch, numerisch oder Text)

Ein gültiger Ausdruck, der einen Wert desselben primitiven Datentyps als Argument `expression` der aufgerufenen Funktion zurückgibt. Dieses Argument ist erforderlich.

`result 1`: *Beliebige der unterstützten Datentypen*

Das zurückgegebene Ergebnis, das der vorherigen Option entspricht. Dieses Argument ist erforderlich.

`option N`: *Primitiver Datentyp* (Boolesch, numerisch oder Text)

Ein gültiger Ausdruck, der einen Wert desselben primitiven Datentyps als Argument `expression` der aufgerufenen Funktion zurückgibt. Dieses Argument ist optional.

`result N`: *Beliebige der unterstützten Datentypen*

Das zurückgegebene Ergebnis, das der vorherigen Option entspricht. Dieses Argument ist optional.

`default result`: *Beliebige der unterstützten Datentypen*

Das Ergebnis, das zurückgegeben werden soll, wenn keine Übereinstimmung vorliegt. Dieses Argument ist optional.

## <a name="return-values"></a>Rückgabewerte

*Beliebige der unterstützten Datentypen*

Der resultierende Wert eines der unterstützten Datentypen.

## <a name="usage-notes"></a>Anwendungshinweise

Eine Ausnahme wird zur Laufzeit ausgelöst, wenn keine Übereinstimmung vorliegt und kein optionales Standardergebnis definiert ist.

Alle Ergebnisse müssen anhand desselben Datentyps angegeben werden. Eine Ausnahme wird zur Entwurfszeit ausgelöst, wenn die Datentypen der konfigurierten Ergebnisse nicht übereinstimmen.

Wenn der erste Ergebniswert und der zweite Ergebniswert *N*. des Datentyps *Container (Datensatz)* oder des Datentyps *Datensatzliste* sind, enthält das Ergebnis nur die Felder, die in beiden Werten vorhanden sind.

## <a name="example"></a>Beispiel

`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` gibt die Zeichenfolge **"WINTER"** zurück, wenn die aktuelle Anwendungssitzung zwischen Oktober und Dezember liegt. Andernfalls wird eine leere Zeichenfolge zurückgegeben.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Logische Funktionen](er-functions-category-logical.md)
