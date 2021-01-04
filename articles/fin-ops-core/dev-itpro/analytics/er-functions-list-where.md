---
title: WHERE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der WHERE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 1cc47c5001cf456b1fc600b326f826ea3b8b43ee
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687049"
---
# <a name="where-er-function"></a>WHERE EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `WHERE` gibt die angegebene Liste mit dem Wert *Datensatzliste* zurück, nachdem sie gemäß der angegebenen Bedingung gefiltert wurde.

## <a name="syntax"></a>Syntax

```vb
WHERE (list, condition)
```

## <a name="arguments"></a>Argumente

`list`: *Datensatzliste*

Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.

`condition`: *Boolesch*

Ein gültiger Bedingungsausdruck, mit dem Datensätze der angegebenen Liste gefiltert werden.

## <a name="return-values"></a>Rückgabewerte

*Datensatzliste*

Die resultierende Liste der Datensätze.

## <a name="usage-notes"></a>Anwendungshinweise

Diese Funktion unterscheidet sich von der Funktion [FILTER](er-functions-list-filter.md), da die angegebene Bedingung auf jede beliebige Datenquelle der elektronischen Berichterstellung (EB) des Typs *Datensatzliste* angewendet wird, die sich im Speicher befindet.

Wenn die Argumente, die für diese Funktion konfiguriert sind (`list` und `condition`), die Übersetzung dieser Anforderung für den direkten SQL-Aufruf zulassen, wird zur Entwurfszeit eine Warnmeldung ausgelöst. Diese Nachricht informiert den Benutzer darüber, dass die Leistung verbessert werden könnte, wenn die Funktion [FILTER ](er-functions-list-filter.md) anstelle von `WHERE` verwendet werden würde.

## <a name="example-1"></a>Beispiel 1

Wenn **Kreditor** als EB-Datenquelle konfiguriert wurde, die sich auf die Tabelle „VendTable“ bezieht, gibt der Ausdruck `WHERE (Vendors, Vendors.VendGroup = "40")` eine Liste von ausschließlich den Kreditoren zurück, die zur Kreditorengruppe 40 gehören.

## <a name="example-2"></a>Beispiel 2

Wenn Sie die Datenquelle **DS** des Typs *Berechnetes Feld* eingeben und sie den Ausdruck `SPLIT ("A|B|C", "|")` enthält, gibt der Ausdruck `WHERE( DS, DS.Value = "B")` eine Liste mit nur einem Datensatz zurück, der den Text **"B"** im Feld **Wert** enthält.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Listenfunktionen](er-functions-category-list.md)
