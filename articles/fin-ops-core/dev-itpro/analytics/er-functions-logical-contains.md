---
title: CONTAINS ER-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der CONTAINS-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: kfend
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 0b2831f8aec4847279953ebcea583c9218d214a7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273127"
---
# <a name="contains-er-function"></a>CONTAINS ER-Funktion

[!include [banner](../includes/banner.md)]

Die `CONTAINS`-Funktion untersucht, ob die angegebene Eingabe den angegebenen Text enthält. Sie gibt einen *booleschen* Wert von **TRUE** zurück, wenn die angegebene Eingabe den angegebenen Text enthält. Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück.

## <a name="syntax"></a>Syntax

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a>Argumente

`input`: *String*

Der gültige Pfad eines Elements einer Datenquelle des *Zeichenfolge*-Typs oder eine Zeichenfolgenkonstante, deren Wert möglicherweise das zweite Argument enthält.

`search text`: *String*

Der gültige Pfad einer Datenquelle des *Zeichenfolge*-Datentyps oder eine Zeichenfolgenkonstante, deren Wert möglicherweise im ersten Argument enthalten ist.

## <a name="return-values"></a>Rückgabewerte

*Aktiv*

Der resultierende *boolesche* Wert.

## <a name="usage-notes"></a>Anwendungshinweise

Diese Funktion kann nur dann zur Angabe eines Bedingungsausdrucks der [FILTER](er-functions-list-filter.md)-Funktion verwendet werden, wenn die entsprechende Zuordnung in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) für den Zugriff auf [Microsoft Dataverse](/power-platform/admin/data-integrator) konfiguriert ist. Andernfalls wird während der Entwurfszeit eine Ausnahme ausgelöst. Die Nachricht, die Sie erhalten, empfiehlt, die [WHERE](er-functions-list-where.md)-Funktion anstelle der `FILTER`-Funktion zu verwenden.

## <a name="example-1"></a>Beispiel 1

Der Ausdruck `CONTAINS ("abc", "d")` gibt **FALSE** zurück, während der Ausdruck `CONTAINS ("abc", "C")` **TRUE** zurückgibt.

## <a name="example-2"></a>Beispiel 2

Der Ausdruck `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` gibt **TRUE** zurück, wenn der Wert des Feldes **Adresse** der Datenquelle **Modell** die Zeichenfolge **DEU** enthält. Andernfalls wird **FALSE** zurückgegeben.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Logische Funktionen](er-functions-category-logical.md)
