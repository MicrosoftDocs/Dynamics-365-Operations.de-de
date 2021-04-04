---
title: EMPTYRECORD EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der EMPTYRECORD-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 2d3c34cbff8551b84121201b9489250c07c7799e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563245"
---
# <a name="emptyrecord-er-function"></a>EMPTYRECORD EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `EMPTYRECORD` gibt für *Container (Datensatz)* den Wert null zurück, der dieselbe Struktur wie die angegebene Datensatzliste oder der angegebene Datensatz besitzt.

## <a name="syntax"></a>Syntax

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a>Argumente

`list`: *Datensatzliste* oder *Container (Datensatz)*

Der gültige Pfad einer Datenquelle des Typs *Datensatzliste* oder *Container (Datensatz)*.

## <a name="return-values"></a>Rückgabewerte

*Container (Datensatz)*

Der resultierende Datensatzwert.

## <a name="usage-notes"></a>Anwendungshinweise

> [!NOTE] 
> Ein Datensatz NULL ist ein Datensatz, in dem alle Felder einen leeren Wert haben. Ein leerer Wert ist **0** (null) für Zahlen, eine leere Zeichenfolge für Zeichenfolgen usw.

## <a name="example"></a>Beispiel

`EMPTYRECORD (SPLIT ("abc", 1))` gibt einen neuen leeren Datensatz zurück, der dieselbe Struktur wie die Liste hat, die durch die Funktion `SPLIT` zurückgegeben wird. Weitere Informationen finden Sie unter [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Datensatzfunktionen](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]