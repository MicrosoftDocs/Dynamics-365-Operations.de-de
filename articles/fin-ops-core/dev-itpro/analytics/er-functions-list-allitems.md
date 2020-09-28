---
title: ALLITEMS EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von ALLITEMS bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 47113d52e15d3d61f00b3c54229e286eb0f1a8d7
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745392"
---
# <a name="allitems-er-function"></a>ALLITEMS EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `ALLITEMS` führt eine speicherinterne Auswahl durch und gibt einen neuen vereinfachten Wert *Datensatzliste* als Liste der Datensätze zurück, die alle Elemente darstellen, die dem angegebenen Pfad entsprechen.

## <a name="syntax"></a>Syntax

```vb
ALLITEMS (path)
```

## <a name="arguments"></a>Argumente

`path`: *Datensatzliste*

Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.

## <a name="return-values"></a>Rückgabewerte

*Datensatzliste*

Die resultierende Liste der Datensätze.

## <a name="usage-notes"></a>Anwendungshinweise

Der Pfad muss als gültiger Datenquellenpfad eines Datenquellenelements eines *Datensatzlisten*-Datentyps definiert werden. Datenelemente, wie beispielsweise die Pfadzeichenfolge und Datum, sollten ein Fehler im Ausdrucksgenerator der elektronischen Berichterstellung (EB) zur Entwurfszeit erzeugen.

Es wird nicht empfohlen, diese Funktion für Transaktionsdatenquellen zu verwenden, die möglicherweise ein großes Datenvolumen enthalten. Verwenden Sie stattdessen die Funktion [ALLTEMSQUERY ](er-functions-list-allitemsquery.md).

## <a name="example-1"></a>Beispiel 1

Wenn Sie `SPLIT("abcdef" , 2)` als Datenquelle **DS** eingeben, gibt der Ausdruck `COUNT( ALLITEMS (DS))` **3** zurück.

## <a name="example-2"></a>Beispiel 2

Wenn Sie **Vend** als Datenquelle des Datentyps *Datensatzliste* eingeben, der auf die VendTable-Anwendungstabelle verweist, gibt der Ausdruck `ALLITEMS (Vend.'<Relations'.ContactPerson)` eine vereinfachte Liste an Datensätzen zurück, die die Tabellenstruktur **ContactPerson** aufweist und alle Kontaktpersonen enthält, auf die durch Verwendung der Beziehung **ContactPerson.ContactForParty == VendTable.Party** zugegriffen werden kann, und die für alle Kreditoren über die referenzierte Kreditorentabelle verfügbar ist.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Listenfunktionen](er-functions-category-list.md)
