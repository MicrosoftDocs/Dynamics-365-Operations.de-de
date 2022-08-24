---
title: GUIDVALUE EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der GUIDVALUE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: cb706a3607b4443c283a91c42c4dc1c389972e44
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285184"
---
# <a name="guidvalue-er-function"></a>GUIDVALUE EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `GUIDVALUE` konvertiert die angegebene Eingabe des Datentyps *String* in ein Datenelement des Typs *GUID*.

## <a name="syntax"></a>Syntax

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a>Argumente

`input`: *String*

Der gültige Pfad einer Datenquelle des Typs *String*.

## <a name="return-values"></a>Rückgabewerte

*GUID*

Der resultierende GUID-Wert (Globally Unique Identifier).

## <a name="usage-notes"></a>Anwendungshinweise

Um eine Umwandlung in der entgegengesetzten Richtung auszuführen (das heißt, die angegebene Eingabe des Datentyps *GUID* in ein Datenelement des Datentyps *String* zu konvertieren), können Sie die Funktion [TEXT()](er-functions-text-text.md) verwenden.

## <a name="example"></a>Beispiel

Die folgenden Datenquellen definieren Sie in Ihrer Modellzuordnung:

- Die Datenquelle **myID** des Typs *Berechnetes Feld*, die den Ausdruck `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")` enthält
- Die Datenquelle **Benutzer** des Typs *Tabellendatensätze*, der auf die UserInfo-Tabelle verweist

Sie können dann einen Ausdruck wie `FILTER (Users, Users.objectId = myID)` verwenden, um die UserInfo-Tabelle nach dem Feld **objectID** des Datentyps *GUID* zu filtern.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
