---
title: NULLDATE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der NULLDATE bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 657766a838fbcd32c6b8bb0ba1f728e9dbbac92e103c219f3eeeab7ecd8c747d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749751"
---
# <a name="nulldate-er-function"></a>NULLDATE EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `NULLDATE` gibt den Wert *Date* zurück, der das Datum **null** (01. Januar 1900) darstellt.

## <a name="syntax"></a>Syntax

```vb
NULLDATE () as 
```

## <a name="return-values"></a>Rückgabewerte

*Datum*

Der resultierende Datenwert.

## <a name="example-1"></a>Beispiel 1

`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` gibt das Datum **null**, 01. Januar 1900, mit **"1900-01-01"** basierend auf dem angegebenen benutzerdefinierten Format zurück.

## <a name="example-2"></a>Beispiel 2

Der Ausdruck `IF( Invoice.DocumentDate = NULLDATE(), true, false)` gibt **True** zurück, wenn der Wert des Feldes **DocumentDate** dem Datum **null** entspricht. In diesem Beispiel ist **Invoice** eine Datenquelle der elektronischen Berichterstellung (EB) des Typs **Finance/Tabellendatensätze** und bezieht sich auf die Tabelle „CustInvoiceJour“.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Datums- und Zeitfunktionen](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]