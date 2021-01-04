---
title: MOD_97 EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der MOD_97-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2e4e40fbd953b31225ccc0f54912b26933ccc48
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680637"
---
# <a name="mod_97-er-function"></a>MOD_97 EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `MOD_97` gibt den Wert *String* zurück, der eine Gläubigerreferenz als MOD97-Ausdruck basierend auf den Ziffern der angegebenen Rechnungsnummer darstellt.

## <a name="syntax"></a>Syntax

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a>Argumente

`invoice number digits`: *String*

Ein Textwert, der die Ziffern einer Rechnungsnummer darstellt.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="example"></a>Beispiel

`MOD_97 ("VEND-200002")` gibt **"20000285"** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Andere (geschäftsdomänenspezifische) Funktionen](er-functions-category-other.md)
