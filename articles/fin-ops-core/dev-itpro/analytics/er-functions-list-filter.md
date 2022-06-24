---
title: FILTER EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der FILTER-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/14/2021
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
ms.openlocfilehash: dfa4afdcfad8c1855a10e1fa37c36cc5b20682ef
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884516"
---
# <a name="filter-er-function"></a>FILTER EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `FILTER` gibt die angegebene Liste als Wert *Datensatzliste* zurück, nachdem die Abfrage so geändert wurde, dass sie nach der angegebenen Bedingung filtert.

## <a name="syntax"></a>Syntax

```vb
FILTER (list, condition)
```

## <a name="arguments"></a>Argumente

`list`: *Datensatzliste*

Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.

`condition`: *Boolesch*

Ein gültiger Bedingungsausdruck, mit dem Datensätze der angegebenen Liste gefiltert werden.

## <a name="return-values"></a>Rückgabewerte

*Datensatzliste*

Die resultierende Liste der Datensätze.

## <a name="usage-notes"></a><a name="usage-notes"></a>Anwendungshinweise

Diese Funktion unterscheidet sich von der Funktion [WO](er-functions-list-where.md), da die angegebene Bedingung auf jede beliebige Datenquelle der elektronischen Berichtserstellung (EB) des Typs *Tabellendatensätze* auf Datenbankebene angewendet wird. Die Liste und die Bedingung können definiert werden, indem Tabellen und Relationen verwendet werden.

Wenn eines oder beide Argumente, die für diese Funktion konfiguriert sind (`list` und `condition`), nicht die Übersetzung dieser Anforderung für den direkten SQL-Aufruf zulassen, wird zur Entwurfszeit eine Ausnahme ausgelöst. Diese Ausnahme informiert den Benutzer darüber, dass entweder `list` oder `condition` nicht zum Abfragen der Datenbank verwendet werden kann.

> [!NOTE]
> Die Funktion `FILTER` verhält sich anders als die Funktion `WHERE`, wenn die Funktion [`VALUEIN`](er-functions-logical-valuein.md) zur Angabe der Auswahlkriterien verwendet wird.
> 
> - Wenn die Funktion `VALUEIN` im Rahmen der Funktion `WHERE` verwendet wird und das zweite Argument von `VALUEIN` auf eine Datenquelle verweist, die keine Datensätze liefert, wird der boolesche Wert *[Falsch](er-formula-supported-data-types-primitive.md#boolean)* berücksichtigt, den `VALUEIN` zurückgibt. Daher gibt der Ausdruck `WHERE(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` keine Datensätze von Lieferanten zurück, wenn die Datenquelle **VendGroups** keine Datensätze von Lieferantengruppen zurückgibt.
> - Wenn die Funktion `VALUEIN` im Rahmen der Funktion `FILTER` verwendet wird und das zweite Argument von `VALUEIN` auf eine Datenquelle verweist, die keine Datensätze zurückgibt, wird der boolesche Wert *[Falsch](er-formula-supported-data-types-primitive.md#boolean)*, den `VALUEIN` zurückgibt, ignoriert. Daher gibt der Ausdruck `FILTER(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` alle Datensätze der Datenquelle **Vendors** zurück, auch wenn die Datenquelle **VendGroups** keine Datensätze der Vendor Groups zurückgibt.

## <a name="example-1"></a>Beispiel 1

Wenn **Kreditor** als EB-Datenquelle konfiguriert wurde, die sich auf die Tabelle „VendTable“ bezieht, gibt der Ausdruck `FILTER (Vendors, Vendors.VendGroup = "40")` eine Liste von ausschließlich den Kreditoren zurück, die zur Kreditorengruppe 40 gehören.

## <a name="example-2"></a>Beispiel 2

Wenn **Kreditor** als EB-Datenquelle konfiguriert ist, die auf die Tabelle „VendTable“ verweist, und wenn **parmVendorBankGroup** als EB-Datenquelle konfiguriert ist, die einen Wert des Datentyps *String* zurückgibt, gibt der Ausdruck `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` eine Liste nur der Kreditorenkonten zurück, die zu einer bestimmten Bankengruppe gehören.

## <a name="example-3"></a>Beispiel 3

Sie geben die Datenquelle **DS** des Typs *Berechnetes Feld* ein, und sie enthält den Ausdruck `SPLIT ("A,B,C", ",")`. Sie geben dann einen anderen Ausdruck ein, `FILTER( DS, DS.Value = "B")`. Wenn Sie versuchen, diesen Ausdruck im EB-Formel-Designer zu speichern, wird die folgende Ausnahme ausgelöst: „Validierungsfehler: Der Listenausdruck der FILTER-Funktion kann nicht abgefragt werden.“

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Listenfunktionen](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
