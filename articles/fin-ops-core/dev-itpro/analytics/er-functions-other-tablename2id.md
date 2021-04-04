---
title: TABLENAME2ID EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der TABLENAME2ID-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 49370af4ebb7552dd3aff4512890fd93fa67c72d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563269"
---
# <a name="tablename2id-er-function"></a>TABLENAME2ID EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `TABLENAME2ID` gibt eine numerische Darstellung der Tabellen-ID für den angegebenen Tabellennamen mit dem Wert *Integer* zurück.

## <a name="syntax"></a>Syntax

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a>Argumente

`text`: *String*

Ein Textwert, der einen gültigen Tabellennamen darstellt.

## <a name="return-values"></a>Rückgabewerte

*Ganze Zahl*

Der resultierende numerische Wert.

## <a name="usage-notes"></a>Anwendungshinweise

Die Ausführung dieser Funktion kann in verschiedenen Instanzen von Microsoft Dynamics 365 Finance zu unterschiedlichen Ergebnissen führen, auch wenn derselbe Firmenname verwendet wird.

## <a name="example"></a>Beispiel

`TABLENAME2ID ("Intrastat")` gibt **1510** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Andere (geschäftsdomänenspezifische) Funktionen](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]