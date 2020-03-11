---
title: SPLIT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der SPLIT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52a89f744cd37c543294522cc706ae7f47660e75
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070620"
---
# <a name="SPLIT">SPLIT EB-Funktion</a>

[!include [banner](../includes/banner.md)]

Die Funktion `SPLIT` teilt die angegebene Eingabezeichenfolge in Teilzeichenfolgen auf und gibt das Ergebnis als neuen Wert *Datensatzliste* zurück.

## <a name="syntax-1"></a>Syntax 1

```vb
SPLIT (input, length)
```

Diese Syntax wird verwendet, um die angegebene Eingabezeichenfolge in Teilzeichenfolgen aufzuteilen, von denen jede die angegebene Länge hat.

## <a name="syntax-2"></a>Syntax 2

```vb
SPLIT (input, delimiter)
```

Diese Syntax wird verwendet, um die angegebene Eingabezeichenfolge in Teilzeichenfolgen zu teilen, von denen jede die angegebene Länge hat.

## <a name="arguments"></a>Argumente

`input`: *String*

Zu trennender Text.

`length`: *Integer*

Die maximale Länge einer einzelnen Teilzeichenfolge.

`delimiter`: *String*

Ein Trennzeichen, das zum Trennen von Teilzeichenfolgen verwendet wird.

## <a name="return-values"></a>Rückgabewerte

*Datensatzliste*

Die resultierende Liste der Datensätze.

## <a name="usage-notes"></a>Anwendungshinweise

Die Datensatzstruktur der zurückgegebenen Liste besteht aus dem Feld **Wert** des Typs *String*. Jeder Datensatz der zurückgegebenen Liste enthält generierte Teilzeichenfolgen in diesem Feld.

Wenn das Argument `delimiter` leer ist, besteht die neue Liste, die zurückgegeben wir, aus einem Datensatz, der das Feld **Wert** des Typs *String* enthält. Dieses Feld enthält den Eingabetext.

Falls das Argument `input` leer ist, wird eine neue leere Liste zurückgegeben. Wenn entweder das Argument `input` oder `delimiter` nicht definiert (null) ist, wird eine Anwendungsausnahme ausgelöst.

## <a name="example-1"></a>Beispiel 1

`SPLIT ("abcd", 3)` gibt eine neue Liste zurück, die aus zwei Datensätzen besteht, die das Feld **Wert** des Typs *String* aufweisen. Das Feld **Wert** im ersten Datensatz enthält den Text **"abc"**, und das Feld **Wert** im zweiten Datensatz enthält den Text **"d"**.

## <a name="example-2"></a>Beispiel 2

`SPLIT ("XAb aBy", "aB")` gibt eine neue Liste zurück, die aus drei Datensätzen besteht, die das Feld **Wert** des Typs *String* aufweisen. Das Feld **Wert** im ersten Datensatz enthält den Text **"X"**, das Feld **Wert** im zweiten Datensatz enthält den Text **"&nbsp;"**, und das Feld **Wert** im dritten Datensatz enthält den Text **"y"**. 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Listenfunktionen](er-functions-category-list.md)
