---
title: LIST EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der LIST-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 7a5f27baa248ec84c75725cf32a1f482841424c2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277631"
---
# <a name="list-er-function"></a>LIST EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `LIST` gibt den Wert *Datensatzliste* zurück, der aus einer neuen Liste an Datensätzen besteht, die anhand der angegebenen Argumente erstellt wird.

## <a name="syntax"></a>Syntax

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a>Argumente

`record 1`: *Container (Datensatz)*

Ein Verweis auf eine Datenquelle des Datensatztyps *Datensatz*. Dieses Argument ist erforderlich.

`record N`: *Container (Datensatz)*

Ein Verweis auf eine Datenquelle des Datensatztyps *Datensatz*. Diese zusätzlichen Argumente sind optional.

## <a name="return-values"></a>Rückgabewerte

*Datensatzliste*

Die resultierende Liste der Datensätze.

## <a name="usage-notes"></a>Anwendungshinweise

Die Struktur der Liste, die erstellt wird, enthält nur die Felder, die in der Struktur jedes Datensatzes dargestellt werden, der in den Argumenten erwähnt wird.

## <a name="example"></a>Beispiel

Sie geben die Datenquelle **Record 1** des Typs *Container* ein. Diese Datenquelle enthält die folgenden verschachtelten Felder des Typs *Berechnetes Feld*:

- **Code:** Dieses Feld enthält einen Ausdruck, der einen Wert vom Typ *String* zurückgibt.
- **Betrag:** Dieses Feld enthält einen Ausdruck, der einen Wert vom Typ *Real* zurückgibt.

Sie geben dann die Datenquelle **Record 2** des Typs *Container* ein. Diese Datenquelle enthält die folgenden verschachtelten Felder des Typs *Berechnetes Feld*:

- **Betrag:** Dieses Feld enthält einen Ausdruck, der einen Wert vom Typ *Real* zurückgibt.
- **IsValid:** Dieses Feld enthält einen Ausdruck, der einen Wert vom Typ *Boolesch* zurückgibt.

In diesem Fall gibt der Ausdruck `LIST('Record 1', 'Record 2')` eine neue Liste zurück, die zwei Datensätze enthält. Die Struktur dieser Liste besteht aus einem einzelnen Feld **Betrag** des Typs *Real*, da dieses Feld das einzige Feld ist, das in jedem Argument der aufgerufenen Funktion vorhanden ist.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Listenfunktionen](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
