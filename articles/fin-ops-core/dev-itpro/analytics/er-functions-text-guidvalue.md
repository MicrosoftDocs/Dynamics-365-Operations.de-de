---
title: GUIDVALUE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der GUIDVALUE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: a7b8c782aff488a433c40a49ab7f4fe2d0e944e4
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041168"
---
# <a name="GUIDVALUE">GUIDVALUE EB-Funktion</a>

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
