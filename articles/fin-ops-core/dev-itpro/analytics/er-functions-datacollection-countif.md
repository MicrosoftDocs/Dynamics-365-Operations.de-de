---
title: COUNTIF EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von COUNTIF bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: a2946a855929dd4dc9647b1e53f0f8a739c522ef8703570e11a4b43636be77dd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714586"
---
# <a name="countif-er-function"></a>COUNTIF EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `COUNTIF` gibt den Wert *Integer* zurück, der die Anzahl der Formatelemente darstellt, die erfasst wurden, als die Formatelemente zum Generieren eines ausgehenden Dokuments während der Formatausführung verwendet wurden, und der die angegebene Bedingung erfüllt. Die Bedingung besteht aus einem Schlüsselbereich und einem Schlüsselwert.

## <a name="syntax"></a>Syntax

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a>Argumente

`condition range`: *String*

Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselname** einer Komponente im elektronischen Berichterstellungsformat konfiguriert wird.

`condition value`: *String*

Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselwert** einer Komponente im elektronischen Berichterstellungsformat konfiguriert wird.

## <a name="return-values"></a>Rückgabewerte

*Ganze Zahl*

Der resultierende numerische Wert.

## <a name="usage-notes"></a>Anwendungshinweise

Die Eigenschaften **Gesammelter Datenschlüsselname** und **Gesammelter Datenschlüsselwert** können entweder für die Komponente **Reihenfolge** oder die Komponente **XML-Element** eines EB-Formats konfiguriert werden, das sich unter der Komponente **Allgemeine\\Datei** befindet, in der die Option **Ausgabendetails sammeln** aktiviert ist.

Diese Funktion gibt den Wert **0** (null) zurück, wenn die Option **Ausgabedetails sammeln** der aktiven Komponente **Allgemeine\\Datei** deaktiviert ist.

Im `condition range`-Argument können Platzhalterzeichen **"\*"** verwendet werden, um mehrere beliebige Zeichen darzustellen.

Im `condition value`-Argument können Platzhalterzeichen **"\*"** verwendet werden, um mehrere beliebige Zeichen darzustellen.

## <a name="example"></a>Beispiel

Um mehr darüber zu erfahren, wie diese Funktion verwendet wird, finden Sie Informationen im Aufgabenleitfaden [EB – Verwendung von Daten der Formatausgabe für Inventur und Summierungen](tasks/er-format-counting-summing-1.md), der Teil des Geschäftsprozesses **IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln** ist.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Datensammlungsfunktionen](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]