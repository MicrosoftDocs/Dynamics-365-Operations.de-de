---
title: NOT EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der NOT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: da30e9a0092f594da7cef7b425e2b89af7bda491
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890484"
---
# <a name="not-er-function"></a>NOT EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `NOT` gibt den umgekehrten logischen Wert der angegebenen Bedingung als *booleschen* Wert zurück.

## <a name="syntax"></a>Syntax

```vb
NOT (condition)
```

## <a name="arguments"></a>Argumente

`condition`: *Boolesch*

Ein gültiger Bedingungsausdruck, der aufgehoben werden muss.

## <a name="return-values"></a>Rückgabewerte

*Aktiv*

Der resultierende *boolesche* Wert.

## <a name="example"></a>Beispiel

`NOT (TRUE)` gibt **FALSE** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Logische Funktionen](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]