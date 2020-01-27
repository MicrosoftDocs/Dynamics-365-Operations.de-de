---
title: REVERSE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der REVERSE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 3343ad788cef29a79f9b110bf29809cd5f0e5c63
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917234"
---
# <a name="REVERSE">REVERSE EB-Funktion</a>

[!include [banner](../includes/banner.md)]

Die Funktion `REVERSE` gibt die angegebene Liste mit dem Wert *Datensatzliste* in umgekehrter Sortierreihenfolge zurück.

## <a name="syntax"></a>Syntax

```
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
