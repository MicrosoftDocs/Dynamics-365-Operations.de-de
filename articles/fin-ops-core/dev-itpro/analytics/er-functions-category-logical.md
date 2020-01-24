---
title: Liste der EB-Funktionen in der logischen Kategorie
description: Dieses Thema enthält Informationen zu den logischen Funktionen, die in der elektronischen Berichterstellung (EB) unterstützt werden.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 408b3c5ec37b24e0ccf6e368012a936701eedf0f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916636"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>Liste der EB-Funktionen in der logischen Kategorie

[!include [banner](../includes/banner.md)]

Logische elektronische Berichtsfunktionen (EB) können verwendet werden, um mit logischen Werten zu arbeiten und mehr als einen Vergleich in einem einzelnen Ausdruck durchzuführen oder mehrere Bedingungen zu testen. Dieses Thema enthält eine Zusammenfassung dieser Funktionen.

## <a name="list-of-supported-functions"></a>Liste der unterstützten Funktionen

| Funktion | Beschreibung |
|----------|-------------|
| [Und](er-functions-logical-and.md)                       | Diese Funktion gibt den *booleschen* Wert **TRUE** zurück, wenn alle angegebenen Bedingungen wahr sind. Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück. |
| [Behälter](er-functions-logical-case.md)                     | Diese Funktion bewertet den Wert des angegebenen Ausdrucks anhand der angegebenen alternativen Optionen und gibt das Ergebnis der ersten Option zurück, die dem Wert des angegebenen Ausdrucks entspricht. Andernfalls wird ein optionales Standardergebnis zurückgegeben, wenn als letztes Argument der aufgerufenen Funktion ein Standardergebnis angegeben wird, dem keine Option vorangestellt ist. Der zurückgegebene Wert kann ein Wert eines beliebigen unterstützten Datentyps sein. |
| [Falls](er-functions-logical-if.md)                         | Diese Funktion gibt den ersten angegebenen Wert zurück, wenn die angegebene Bedingung zutrifft. Sie gibt andernfalls den zweiten angegebenen Wert zurück. Der zurückgegebene Wert kann ein Wert eines beliebigen unterstützten Datentyps sein. |
| [Nicht](er-functions-logical-not.md)                       | Diese Funktion gibt den umgekehrten logischen Wert der angegebenen Bedingung als *booleschen* Wert zurück. |
| [Or](er-functions-logical-or.md)                         | Diese Funktion gibt den *booleschen* Wert **FALSE** zurück, wenn alle angegebenen Bedingungen falsch sind. Wenn eine der angegebenen Bedingungen wahr ist, gibt die Funktion den *booleschen* Wert **TRUE** zurück. |
| [ValueIn](er-functions-logical-valuein.md)               | Diese Funktion bestimmt, ob die Eingabe mit einem angegebenen Wert eines angegebenen Artikels in der angegebenen Liste übereinstimmt. Sie gibt den *booleschen* Wert **TRUE** zurück, wenn die angegebene Eingabe mit dem Ergebnis der Ausführung des angegebenen Ausdrucks für mindestens einen Datensatz der entsprechenden Liste übereinstimmt. Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)

[Formeldesigner in der elektronischen Berichterstellung](general-electronic-reporting-formula-designer.md)

[Formelsprache in der elektronischen Berichterstellung](er-formula-language.md)
