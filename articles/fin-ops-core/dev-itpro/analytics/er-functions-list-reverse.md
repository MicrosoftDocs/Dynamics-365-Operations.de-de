---
title: REVERSE EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der REVERSE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 360878319bfa29395ae5deabec2e25e52d9e0fdc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284147"
---
# <a name="reverse-er-function"></a>REVERSE EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `REVERSE` gibt die angegebene Liste mit dem Wert *Datensatzliste* in umgekehrter Sortierreihenfolge zurück.

## <a name="syntax"></a>Syntax

```vb
REVERSE (list)
```

## <a name="arguments"></a>Argumente

`list`: *Datensatzliste*

Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.

## <a name="return-values"></a>Rückgabewerte

*Datensatzliste*

Die resultierende Liste der Datensätze.

## <a name="example-1"></a>Beispiel 1

Wenn Sie die Datenquelle **DS** des Typs *Berechnetes Feld* eingeben, und sie den Ausdruck `SPLIT ("C|B|A", "|")` enthält, gibt der Ausdruck `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` den Textwert **"C"** zurück.

## <a name="example-2"></a>Beispiel 2

Wenn **Kreditor** als Datenquelle der elektronischen Berichtserstellung (EB) konfiguriert ist, die sich auf die Tabelle „VendTable“ bezieht, gibt der Ausdruck `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` eine Liste von Kreditoren zurück, die nach Namen in absteigender Reihenfolge sortiert ist.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Listenfunktionen](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
