---
title: REVERSE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der REVERSE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
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
ms.openlocfilehash: 746a736c8797c1c1c5bd71d7d803be4212984595
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755203"
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