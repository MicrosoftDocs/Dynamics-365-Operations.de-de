---
title: CONVERTCURRENCY EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der CONVERTCURRENCY-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 0f0d5bace9b62cf6f0d7576744a6cc271666bf73
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567639"
---
# <a name="convertcurrency-er-function"></a>CONVERTCURRENCY EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `CONVERTCURRENCY` gibt den Wert *Real* zurück, der das Konvertieren des angegebenen Geldbetrags aus der angegebenen Ausgangswährung in die angegebene Zielwährung darstellt, indem die Einstellungen des angegebenen Unternehmens am angegebenen Datum verwendet werden.

## <a name="syntax"></a>Syntax

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a>Argumente

`amount`: *Integer* oder *Real*

Ein numerischer Wert, der den umzurechnenden Geldbetrag darstellt.

`source currency`: *String*

Der Code der Ausgangswährung.

`target currency`: *String*

Der Code der Zielwährung.

`date`: *Date*

Der Wert *Datum*, der das Datum darstellt, mit dem der Wechselkurs für die Konvertierung bestimmt wird.

`company`: *String*

Der Wert *String*, der den Code einer Firma darstellt, die die für die Konvertierung verwendeten Einstellungen bereitstellt.

## <a name="return-values"></a>Rückgabewerte

*Gleitkommazahl*

Der resultierende numerische Wert.

## <a name="example"></a>Beispiel

`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` gibt die Entsprechung von einem Euro in US Dollar am Datum der aktuellen Sitzung basierend auf den Einstellungen für das **DEMF**-Unternehmen zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Andere (geschäftsdomänenspezifische) Funktionen](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]