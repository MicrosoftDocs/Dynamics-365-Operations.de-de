---
title: AND EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von AND bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
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
ms.openlocfilehash: 4a246496eca0d5a8538ac7f1577957e6b9eae4e3
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743469"
---
# <a name="and-er-function"></a>AND EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `AND` gibt den *booleschen* Wert **TRUE** zurück, wenn alle angegebenen Bedingungen wahr sind. Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück.

## <a name="syntax"></a>Syntax

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Argumente

`condition 1`: *Boolesch*

Ein gültiger Bedingungsausdruck, der getestet werden muss. Dieses Argument ist erforderlich.

`condition N`: *Boolesch*

Ein gültiger Bedingungsausdruck, der getestet werden muss. Diese zusätzlichen Argumente sind optional.

## <a name="return-values"></a>Rückgabewerte

*Aktiv*

Der resultierende *boolesche* Wert.

## <a name="usage-notes"></a>Anwendungshinweise

In den Argumenten logischer Funktionen können Sie Datenquellenverweise, numerische und Textwerte, Boolesche Werte, Vergleichsoperatoren und andere Funktionen für die elektronische Berichterstellung (EB) verwenden. Alle Argumente müssen jedoch mit dem *booleschen* Wert **TRUE** oder **FALSE** bewertet werden.

## <a name="example"></a>Beispiel

`AND (1=1, "a"="a")` gibt **TRUE** zurück.

`AND (1=2, "a"="a")` gibt **FALSE** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Logische Funktionen](er-functions-category-logical.md)
