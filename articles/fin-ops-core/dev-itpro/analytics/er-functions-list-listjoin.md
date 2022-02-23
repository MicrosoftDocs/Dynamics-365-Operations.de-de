---
title: LISTJOIN EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der LISTJOIN-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28f03e5e6af0f252a994f2e54b57a5ef654f4e67
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682242"
---
# <a name="listjoin-er-function"></a>LISTJOIN EB-Funktion

[!include [banner](../includes/banner.md)]

Die `LISTJOIN` Funktion gibt den Wert *Datensatzliste* zurück, der eine neue Liste von Datensätzen darstellt, die anhand der angegebenen Argumente erstellt wird.

## <a name="syntax"></a>Syntax

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a>Argumente

`list 1`: *Datensatzliste*

Ein Verweis auf eine Datenquelle des Datensatztyps *Datensatzliste*. Dieses Argument ist obligatorisch.

`list N`: *Datensatzliste*

Ein Verweis auf eine Datenquelle des Datensatztyps *Datensatzliste*. Diese zusätzlichen Argumente sind optional.

## <a name="return-values"></a>Rückgabewerte

*Datensatzliste*

Die resultierende Liste der Datensätze.

## <a name="usage-notes"></a>Anwendungshinweise

Die Struktur der Liste, die erstellt wird, zeigt nur die Felder, die in der Struktur jedes Datensatzes dargestellt werden, der in den Argumenten erwähnt wird.

## <a name="example"></a>Beispiel

Sie geben die Datenquelle **Record 1** des Typs `Container` ein. Diese Datenquelle enthält die folgenden verschachtelten Felder des Typs `Calculated field` Feld:

- **Code**: Dieses Feld enthält einen Ausdruck, der einen Wert vom Typ `String` zurückgibt.
- **Betrag**: Dieses Feld enthält einen Ausdruck, der einen Wert vom Typ `Real` zurückgibt.

Sie geben dann die Datenquelle **Record 2** des Typs `Container` ein. Diese Datenquelle enthält die folgenden verschachtelten Felder des Typs `Calculated field` Feld:

- **Betrag**: Dieses Feld enthält einen Ausdruck, der einen Wert vom Typ `Real` zurückgibt.
- **IsValid**: Dieses Feld enthält einen Ausdruck, der einen Wert vom Typ `Boolean` zurückgibt.

![ER-Modellzuordnungsdesigner – Seite](./media/er-functions-list-listjoin-image1.gif)

In diesem Fall gibt der Ausdruck `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` eine neue Liste zurück, die zwei Datensätze enthält.

![EB-Modelzuordnungsdesigner-Seite mit zwei Datensätzen](./media/er-functions-list-listjoin-image2.gif)

Die Struktur dieser Liste besteht aus einem einzelnen Feld **Betrag** des Typs `Real`, da dieses Feld das einzige Feld ist, das in jedem Argument der aufgerufenen Funktion vorhanden ist.

![Betragsfeld der EB-Modellzuordnungsdesigne-Seite](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Listenfunktionen](er-functions-category-list.md)

[Debuggen Sie Datenquellen eines ausgeführten EB-Formats, um den Datenfluss und die Transformation zu analysieren](er-debug-data-sources.md)
