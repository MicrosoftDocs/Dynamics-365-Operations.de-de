---
title: Liste der EB-Funktionen in der logischen Kategorie
description: Dieses Thema enthält Informationen zu den logischen Funktionen, die in der elektronischen Berichterstellung (EB) unterstützt werden.
author: NickSelin
manager: kfend
ms.date: 02/11/2021
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
ms.openlocfilehash: 7310c2b269c3f4be03102160aebe0ed164a23a5c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561661"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>Liste der EB-Funktionen in der logischen Kategorie

[!include [banner](../includes/banner.md)]

Logische elektronische Berichtsfunktionen (EB) können verwendet werden, um mit logischen Werten zu arbeiten und mehr als einen Vergleich in einem einzelnen Ausdruck durchzuführen oder mehrere Bedingungen zu testen. Dieses Thema enthält eine Zusammenfassung dieser Funktionen.

## <a name="list-of-supported-functions"></a>Liste der unterstützten Funktionen

| Funktion | Beschreibung |
|----------|-------------|
| [Und](er-functions-logical-and.md)                       | Diese Funktion gibt den *booleschen* Wert **TRUE** zurück, wenn alle angegebenen Bedingungen wahr sind. Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück. |
| [Behälter](er-functions-logical-case.md)                     | Diese Funktion bewertet den Wert des angegebenen Ausdrucks anhand der angegebenen alternativen Optionen und gibt das Ergebnis der ersten Option zurück, die dem Wert des angegebenen Ausdrucks entspricht. Andernfalls wird ein optionales Standardergebnis zurückgegeben, wenn als letztes Argument der aufgerufenen Funktion ein Standardergebnis angegeben wird, dem keine Option vorangestellt ist. Der zurückgegebene Wert kann ein Wert eines beliebigen unterstützten Datentyps sein. |
| [Enthält](er-functions-logical-contains.md)             | Diese Funktion untersucht, ob die angegebene Eingabe den angegebenen Text enthält. Sie gibt einen *booleschen* Wert von **TRUE** zurück, wenn die angegebene Eingabe den angegebenen Text enthält. Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück. |
| [EndsWith](er-functions-logical-endswith.md)             | Diese Funktion untersucht, ob die angegebene Eingabe mit dem angegebenen Text endet. Sie gibt einen *booleschen* Wert von **TRUE** zurück, wenn die angegebene Eingabe mit dem angegebenen Text endet. Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück. |
| [Falls](er-functions-logical-if.md)                         | Diese Funktion gibt den ersten angegebenen Wert zurück, wenn die angegebene Bedingung zutrifft. Sie gibt andernfalls den zweiten angegebenen Wert zurück. Der zurückgegebene Wert kann ein Wert eines beliebigen unterstützten Datentyps sein. |
| [Nicht](er-functions-logical-not.md)                       | Diese Funktion gibt den umgekehrten logischen Wert der angegebenen Bedingung als *booleschen* Wert zurück. |
| [Or](er-functions-logical-or.md)                         | Diese Funktion gibt den *booleschen* Wert **FALSE** zurück, wenn alle angegebenen Bedingungen falsch sind. Wenn eine der angegebenen Bedingungen wahr ist, gibt die Funktion den *booleschen* Wert **TRUE** zurück. |
| [StartsWith](er-functions-logical-startswith.md)         | Diese Funktion untersucht, ob die angegebene Eingabe mit dem angegebenen Text beginnt. Sie gibt einen *booleschen* Wert von **TRUE** zurück, wenn die angegebene Eingabe mit dem angegebenen Text beginnt. Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück. |
| [ValueIn](er-functions-logical-valuein.md)               | Diese Funktion bestimmt, ob die Eingabe mit einem angegebenen Wert eines angegebenen Artikels in der angegebenen Liste übereinstimmt. Sie gibt den *booleschen* Wert **TRUE** zurück, wenn die angegebene Eingabe mit dem Ergebnis der Ausführung des angegebenen Ausdrucks für mindestens einen Datensatz der entsprechenden Liste übereinstimmt. Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück. |
| [ValueInLarge](er-functions-logical-valueinlarge.md)     | Diese Funktion bestimmt, ob die angegebene Eingabe des Typs *Int64* oder *Integer* mit irgendeinem Wert eines angegebenen Artikels in der angegebenen Liste übereinstimmt. Sie gibt den *booleschen* Wert **TRUE** zurück, wenn die angegebene Eingabe mit dem Ergebnis der Ausführung des angegebenen Ausdrucks für mindestens einen Datensatz der entsprechenden Liste übereinstimmt. Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück. |


## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)

[Formeldesigner in der elektronischen Berichterstellung](general-electronic-reporting-formula-designer.md)

[Formelsprache in der elektronischen Berichterstellung](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]