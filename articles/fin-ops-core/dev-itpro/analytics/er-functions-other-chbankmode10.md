---
title: CH_BANK_MOD_10 EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der CH_BANK_MOD_10-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: d634f074338831c9c767697a8b6d782289f43b0f4d4a33ea4d29f81f7d71f111
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719392"
---
# <a name="ch_bank_mod_10-er-function"></a>CH_BANK_MOD_10 EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `CH_BANK_MOD_10` gibt den Wert *String* zurück, der eine Gläubigerreferenz als MOD10-Ausdruck basierend auf den Ziffern der angegebenen Rechnungsnummer darstellt.

## <a name="syntax"></a>Syntax

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a>Argumente

`invoice number digits`: *String*

Ein Textwert, der die Ziffern einer Rechnungsnummer darstellt.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="example"></a>Beispiel

`CH_BANK_MOD_10 ("VEND-200002")` gibt **3** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Andere (geschäftsdomänenspezifische) Funktionen](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]