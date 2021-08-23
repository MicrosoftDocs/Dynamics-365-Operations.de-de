---
title: NULLCONTAINER EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der NULLCONTAINER-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 13159d9d7c8d1871886beb3cb1938ca8b0097e0efb6f10a9d1b229c49b9ff947
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738575"
---
# <a name="nullcontainer-er-function"></a>NULLCONTAINER EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `NULLCONTAINER` gibt für *Container (Datensatz)* den Wert null zurück, der dieselbe Struktur wie die angegebene Datensatzliste oder der angegebene Datensatz besitzt.

## <a name="syntax"></a>Syntax

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a>Argumente

`list`: *Datensatzliste* oder *Container (Datensatz)*

Der gültige Pfad einer Datenquelle des Typs *Datensatzliste* oder *Container (Datensatz)*.

## <a name="return-values"></a>Rückgabewerte

*Container (Datensatz)*

Der resultierende Datensatzwert.

## <a name="usage-notes"></a>Anwendungshinweise

> [!NOTE] 
> Diese Funktion ist veraltet. Verwenden Sie stattdessen die Funktion `EMPTYRECORD`. Weitere Informationen finden Sie in [EMPTYRECORD](er-functions-record-emptyrecord.md).

## <a name="example"></a>Beispiel

`NULLCONTAINER (SPLIT ("abc", 1))` gibt einen neuen leeren Datensatz zurück, der dieselbe Struktur wie die Liste hat, die durch die Funktion `SPLIT` zurückgegeben wird. Weitere Informationen finden Sie unter [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Datensatzfunktionen](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]