---
title: IF EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der IF-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: a69675e3c743154e8119ba6c04da5897f23a8422
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565903"
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