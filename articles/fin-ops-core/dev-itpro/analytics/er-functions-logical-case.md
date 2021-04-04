---
title: CASE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der CASE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: f466e3ffe368bf30236060d820621e723106fc1d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562468"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]