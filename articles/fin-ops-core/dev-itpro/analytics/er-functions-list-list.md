---
title: LIST EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von LIST bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
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
ms.openlocfilehash: a31288885abda69873ae23b28a36e2a54852f593
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745152"
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
