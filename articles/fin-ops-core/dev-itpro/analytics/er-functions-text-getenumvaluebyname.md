---
title: GETENUMVALUEBYNAME EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der GETENUMVALUEBYNAME-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 33ccf358dc5355cd00d5ff41ebd8148a334cba38
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743854"
---
# <a name="getenumvaluebyname-er-function"></a>GETENUMVALUEBYNAME EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `GETENUMVALUEBYNAME` sucht nach dem bestimmten Wert *Enum* in der angegebenen Aufzählungsdatenquelle unter Verwendung des Aufzählungsnamens, der mit dem Wert *String* angegeben ist. Wenn der Wert *Enum* gefunden wird, gibt die Funktion ihn zurück. Andernfalls gibt die Funktion den Aufzählungswert **Null** zurück.

## <a name="syntax"></a>Syntax

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>Argumente

`enumeration data source path`: *Aufzählung*

Der gültige Pfad einer Datenquelle eines der folgenden Aufzählungstypen:

- Modellenumeration für die elektronische Berichterstellung (EB)
- EB-Formatenumeration
- Microsoft Dynamics 365 Finance-Enumeration

`enumeration value text`: *String*

Ein Zeichenfolgewert, der den Namen eines einzelnen Aufzählungswerts darstellt.

## <a name="return-values"></a>Rückgabewerte

Nullbar *Enum*

Der resultierende Aufzählungswert.

## <a name="usage-notes"></a>Anwendungshinweise

Es wird keine Ausnahme ausgelöst, wenn ein Wert *Enum* nicht unter Verwendung des Namens des Aufzählungswerts gefunden wird, der mit dem Wert *String* angegeben ist.

## <a name="example"></a>Beispiel

In der folgenden Abbildung wird die Aufzählung **ReportDirection** in einem Datenmodell eingeführt. Beachten Sie, dass Beschriftungen für Enumerationswerte definiert werden.

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Die folgende Abbildung zeigt diese Details an:

- Die Datenquelle **$Direction** wird in einem EB-Bericht konfiguriert. Diese Datenquelle wird basierend auf der Modellenumeration **ReportDirection** konfiguriert.
- Der Ausdruck `$IsArrivals` ist dazu konzipiert, die auf der Modellenumeration basierende Datenquelle **$Direction** als Parameter dieser Funktion zu verwenden.
- Der Wert dieses Vergleichswerts lautet **TRUE**.

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)
