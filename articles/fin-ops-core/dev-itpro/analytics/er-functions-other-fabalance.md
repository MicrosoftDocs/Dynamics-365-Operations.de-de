---
title: FA_BALANCE EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der FA_BALANCE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: f9bb52643b60fd1b9423d798c08d731565c70f81
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285244"
---
# <a name="fa_balance-er-function"></a>FA_BALANCE EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `FA_BALANCE` gibt den Wert *Container (Datensatz)* zurück, der aus Daten für den Anlagensaldo für die angegebene Anlagenposition, dem Wertmodellcode, dem Berichtsjahr und dem Berichtsdatum besteht.

## <a name="syntax"></a>Syntax

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a>Argumente

`fixed asset code`: *String*

Der Wert *String*, der den Code eines Gegenstands des Anlagevermögens darstellt, für den der Saldo berechnet wird.

`value model code`: *String*

Der Wert *String*, der den Code eines Gegenstands des Wertmodells darstellt, für das der Saldo berechnet wird.

`reporting year`: *Aufzählungswert*

Ein Aufzählungswert der Anwendungsaufzählung **AssetYear**, der einen Zeitraum für die Saldenberechnung definiert.

`reporting date`: *Date*

Der Wert *Date*, der ein Datum für die Saldenberechnung definiert.

## <a name="return-values"></a>Rückgabewerte

*Container (Datensatz)*

Der resultierende Datensatzwert.

## <a name="example"></a>Beispiel

`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` gibt den vorbereiteten Datencontainer von Salden für Anlage **COMP-000001** zurück, der das Wertmodell **Current** zum aktuellen Anwendungs-Sitzungsdatum hat.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Andere (geschäftsdomänenspezifische) Funktionen](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
