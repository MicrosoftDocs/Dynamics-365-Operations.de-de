---
title: EMPTYRECORD EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der EMPTYRECORD-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: a02cdd085a236065bb3622b36f7d3284144d96e5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041279"
---
# <a name="EMPTYRECORD">EMPTYRECORD EB-Funktion</a>

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
