---
title: IF EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der IF-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 066cffaebc415305a2481e3bf0f0a5f4e108fabc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844557"
---
# <a name="if-er-function"></a>IF EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `IF` gibt den ersten angegebenen Wert zurück, wenn die angegebene Bedingung zutrifft. Sie gibt andernfalls den zweiten angegebenen Wert zurück. Der zurückgegebene Wert kann ein Wert eines beliebigen unterstützten Datentyps sein.

## <a name="syntax"></a>Syntax

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a>Argumente

`condition`: *Boolesch*

Ein gültiger Bedingungsausdruck, der getestet werden muss.

`first value`: *Beliebige der unterstützten Datentypen*

Das Ergebnis, das zurückgegeben wird, wenn die Bedingung erfüllt ist.

`second value`: *Beliebige der unterstützten Datentypen*

Das Ergebnis, das zurückgegeben wird, wenn die Bedingung nicht erfüllt ist.

## <a name="return-values"></a>Rückgabewerte

*Beliebige der unterstützten Datentypen*

Der resultierende Wert eines der unterstützten Datentypen.

## <a name="usage-notes"></a>Anwendungshinweise

Die Argumente `first value` und `second value` müssen anhand desselben Datentyps angegeben werden. Eine Ausnahme wird zur Entwurfszeit ausgelöst, wenn die Datentypen der konfigurierten Werte nicht übereinstimmen.

Wenn der erste Wert und der zweite Wert Werte des Datentyps *Container (Datensatz)* oder *Datensatzliste* sind, enthält das Ergebnis nur die Felder, die in beiden Werten vorhanden sind.

## <a name="example"></a>Beispiel

`IF (1=2, "condition is met", "condition is not met")` gibt die Zeichenfolge **"Bedingung nicht erfüllt"** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Logische Funktionen](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]